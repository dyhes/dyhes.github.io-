---
title: 【Java】Enum
date: 2024-07-14 00:00:00+0000
image: /covers/cover19.png
categories: 
    - nutrition
tags:
    - Java
---


Java enums are a special type of class used to define collections of constants. They provide a way to represent a fixed set of values, which can be useful for categorizing data and ensuring type safety.
## Key Points
* Implicitly final and static: Enum constants are implicitly public, static, and final.
* values() method: Every enum has a static values() method that returns an array of all enum constants.
* valueOf(String) method: This static method returns the **enum constant** with the specified name.
* The name() method returns the name of the enum constant as declared in its enum declaration. It's an instance method available on all enum constants.
* valueOf(String) and name() provide a way to convert between the Enum and String.
* ordinal() method: Returns the **position** of the enum constant (zero-based).
* Constructors, Fields, and Methods: Enums can have constructors, fields, and methods, allowing you to associate data and behavior with each constant.
* Implementing Interfaces: Enums can implement interfaces, providing a way to define behavior for each constant.
* EnumSet and EnumMap: These are specialized Set and Map implementations for use with enum types, offering **better performance** than their general-purpose counterparts.
* Constant-specific method implementation: You can **override methods for specific enum** constants, allowing for different behavior per constant.
* Abstract methods in enums: You can define abstract methods in an enum, forcing each constant to provide its own implementation.
## example
```java
// Basic enum definition
public enum Day {
    MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY, SATURDAY, SUNDAY
}

// Enum with constructor, fields, and methods
public enum Planet {
    MERCURY(3.303e+23, 2.4397e6),
    VENUS(4.869e+24, 6.0518e6),
    EARTH(5.976e+24, 6.37814e6);

    private final double mass;   // in kilograms
    private final double radius; // in meters

    Planet(double mass, double radius) {
        this.mass = mass;
        this.radius = radius;
    }

    public double getMass() {
        return mass;
    }

    public double getRadius() {
        return radius;
    }

    // Enum constant-specific method implementation
    public double surfaceGravity() {
        return 6.67300E-11 * mass / (radius * radius);
    }
}

// Usage examples
public class EnumExample {
    public static void main(String[] args) {
        // Basic usage
        Day today = Day.MONDAY;
        System.out.println("Today is " + today);

        // Switch statement with enum
        switch (today) {
            case MONDAY:
                System.out.println("Start of the work week");
                break;
            case FRIDAY:
                System.out.println("TGIF!");
                break;
            default:
                System.out.println("Midweek");
        }

        // Using enum methods
        Planet earth = Planet.EARTH;
        System.out.println("Earth's mass: " + earth.getMass());
        System.out.println("Earth's surface gravity: " + earth.surfaceGravity());

        // Iterating over enum values
        for (Planet planet : Planet.values()) {
            System.out.println(planet.name() + ": " + planet.surfaceGravity());
        }
    }
}
```

## Usage with Pageable
```java
public enum UserSortField {
    ID("id"),
    FIRST_NAME("firstName"),
    LAST_NAME("lastName"),
    EMAIL("email"),
    CREATED_DATE("createdDate");

    private final String fieldName;

    UserSortField(String fieldName) {
        this.fieldName = fieldName;
    }

    public String getFieldName() {
        return fieldName;
    }
}

@RestController
@RequestMapping("/api/users")
public class UserController {
    @Autowired
    private UserService userService;

    @GetMapping
    public ResponseEntity<Map<String, Object>> getAllUsers(
            @RequestParam(defaultValue = "0") int page,
            @RequestParam(defaultValue = "10") int size,
            @RequestParam(defaultValue = "ID") UserSortField sortBy) {
        
        Page<User> userPage = userService.getAllUsers(page, size, sortBy);

        // ... rest of the method remains the same
    }
}

@Service
public class UserService {
    @Autowired
    private UserRepository userRepository;

    public Page<User> getAllUsers(int page, int size, UserSortField sortBy) {
        Pageable pageable = PageRequest.of(page, size, Sort.by(sortBy.getFieldName()));
        return userRepository.findAll(pageable);
    }
}
```
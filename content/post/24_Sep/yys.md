---
title: 【阴阳师】藏宝阁出号感悟
date: 2024-09-08 00:00:00+0000
categories: 
    - deer
---

永远对利益保持谨慎，事前充分了解机制

public record emailDto(Long id, String email){};
    @PostMapping("email/request")
    public BasicApiResponseEntity updateemail(@RequestBody emailDto dto) {
        if (dto.id == null || dto.email == null) {
            throw new BadRequestException();
        }
        userService.updateUseremail(dto.id, dto.email);
        return BasicApiResponseEntity.ok("succeed!");
    }
---
title: 【UML需求建模】笔记
date: 2023-06-06 00:00:00+0000
categories: 
  - star
---

## 组成要素

* **基本构造块**

  建模元素，模型的主体

* **规则**

  支配基本构造块如何组织的规则

* **公共机制**

  运用于整个UML模型中的公共机制、拓展机制

![image-20221130102037371](https://i.ibb.co/Gppv7YV/image-20221130102037371.png)

## 基本构造块

### 事物构造块

**结构事物**

静态部分，描述概念或物理元素

**行为事物**

动态部分

**分组事物**

组织模型

**注释事物**

描述模型

#### 结构事物

**类（class）和对象（object）**

类为一组同质对象的**抽象**，对象为类的**实例**

**接口（interface）**

描述某个类或构件的一个**服务操作集**

**主动类（active class）**

其对象至少拥有一个进程或线程，能够启动**控制活动**的类

**用例（use case）**

用例实例是在系统中执行的**一系列动作**，这些动作将生成特定执行者可见的价值结果

一个用例定义一组用例实例

**协作（Collaboration）**

协作定义了一个**交互**，它是由一组共同工作以提供某协作行为的角色和其他元素构成的一个群体。

对于某个用例的实现就可以表示为一个协作

**构件（Component）**

比“类”更大的实体

**节点（Node）**

运行时存在的物理元素，它表示了一种**可计算的资源**，通常至少有存储空间和处理能力

#### 行为事物

**交互（interaction）**

是在特定语境中，共同完成某个任务的一组对象之间**交换的信息集合** 交互的表示法很简单，就是一条**有向直线**，并在上面标有**操作名**

**状态机（state machine）**

一个**对象或交互**在生命周期内响应事件所经历的状态序列

#### 分组事物

对结构事物、行为事物进行分组以更加有效地对其进行**整合**，生成或简或繁、或宏观或微观的模型，在UML中，提供了 “包（Package）”来完成这一目标

### 关系构造块

![image-20221130104903476](https://i.ibb.co/FY6MdCF/image-20221130104903476.png)

## 规则

* 命名
* 范围（作用域）
* 可见性

## 公共机制

* 规格描述
* 构造型
* 标记值
* 约束

#### 需求定义

* 用户为了**解决问题或达到某些目标**所需要的条件或能力
* 系统或系统部件为了**满足合同、标准、 规范或其它正式文档所规定的要求**而需要具备的条件或能力； 
* 对上述两种情况中的**一个条件或一种能力**的一种**文档化表述**

#### 需求内涵

![image-20220421105940379](https://i.ibb.co/QH69wTm/image-20220421105940379.png)

###### 问题域

当现实的状况与人们期望的状况产生**差距**时，就产生了问题

要解决问题，就需要改变现实当中某些实体的**状态**或改变实体状态变化的**演进顺序**，使其达到期望的状态或演进顺序

这些**实体和状态**构成了**问题解决的基本范围**，称为该问题的问题域（Problem Domain）

####### 特性

问题域自治的规律性

* 结构特性
* 行为特性
* 约束
* 假设

###### 解系统

**软件系统**通过**影响问题域**，能够帮助人们解决问题，称为解系统 。

###### 共享现象

软件系统能够与问题域进行交互和相互影响的原因在于，软件系统中的某些部分对问题域中的某些部分的具有模拟特性

问题域中的某些信息能够和模型中的信息建立映射关系

这些通过映射建立的共同知识，就是问题域和解系统之间的 共享现象

![image-20220421110304191](https://i.ibb.co/y6PLKGS/image-20220421110304191.png)

###### 需求

需求是用户对**问题域**当中的实体状态或事件的**期望描述**

###### 规格说明

规格说明是解系统为满足用户需求而提供的解决方案，规定了**解系统的行为特征** 

主要包括两个部分：

 – （1）对共享现象（模型）的描述；

 – （2）系统对共享现象所施加的操作的描述

也可以看作是一种**需求** 

– 完全针对系统行为发出的期望 

– 一种理想的、完全不需要进行任何额外努力即可以转换为系统行为的需求。

###### 需求工程

* 描述明确的问题域特性E; 

* 定义良好的系统行为S ; 

* 预期的需求R；

需求工程的目的就是根据E，构建S，使得 E, S |-> R

####### 困难之处

– （1）不存在描述明确的E； 

– （2）不存在确定的针对S的评估标准R； 

– （3） E, S => R 是一个创造性的过程 

####### 主要工作

* 需求开发,确定R
* 研究问题背景，描述问题域特性E
* 构建解系统，描述解系统行为S ，使得 E, S |-> R

#### 需求分类

* 功能需求（Functional Requirement）

  和**系统主要工作相关**的需求，即在不考虑物理约束的情况下， 用户希望系统所能够执行的活动，这些活动可以帮助用户完 成任务。功能需求主要表现为**系统和环境之间的行为交互**

* 性能需求（Performance Requirement）

  系统整体或系统组成部分应该拥有的性能特征，例如CPU使 用率、内存使用率等。

* 质量属性（Quality Attribute）

  系统完成工作的质量，即系统需要在一个“好的程度”上实 现功能需求，例如可靠性程度、可维护性程度等。

* 对外接口（External Interface）

  系统**和环境中其他系统之间**需要建立的接口，包括硬件接口、软件接口、数据库接口等等

  * 接口的用途  
  * 接口的输入输出 
  * 数据格式 
  * 命令格式 
  * 异常处理要求

* 约束（Constraint）

  进行系统构造时需要遵守的约束，例如编程语言、硬 件设施等

* 系统需求（System Requirement）

  * 硬件需求（Hardware Requirement）
  * 软件需求（Software Requirement）
  * 其他需求

###### 功能需求

![image-20220421111647430](https://i.ibb.co/5KnpgSX/image-20220421111647430.png)

* 业务需求

  系统建立的战略出发点，表现为高层次的目标（Objective），它描述了组织为什么要开发系统

  为了满足用户的业务需求，需求工程师需要描述系统高层次的解决方案，定义系统应该具备的特性（Feature）

  参与各方必须要对高层次的解决方案达成一致， 以建立一个共同的前景（Vision） 

  特性说明了系统为用户提供的各项功能，它限定了系统的范围（Scope）

* 用户需求

  执行实际工作的用户对系统所能完成的具体任务的期望，描述了系统能够**帮助用户**做些什么

* 系统需求

  **用户**对**系统行为**的期望，一系列的系统行为联系在一起可以帮助用户完成任务，满足业务需求

**用户需求**转化为**系统需求**：

* 首先需要分析问题领域及其特性，从中发现问题域和计算机 系统的共享知识，建立系统的知识模型；
* 然后将用户需求部署到系统模型当中，即**定义系列的系统行 为**，让它们联合起来实现用户需求，每一个系统行为即为一 个系统需求。
* 该过程就是需求工程当中最为重要的**需求分析**活动 ，又称建模与分析活动

#### 需求工程路线

* 问题分析和背景分析
  * 明确问题
  * 定义业务需求
  * 指定解决方案
  * 确定系统特性

* 需求获取
* 需求分析
  * 建立综合考虑问题域特性和需求的系统模型
  * 根据系统模型将用户需求转化为系统需求
* 文档化和验证
  * 产生规格说明
  * 进行验证

#### 优秀需求

* 完整性
* 正确性
* 精确性
* 可行性
* 必要性
* 无歧义
* 可验证：通过分析、检查、模拟或者测试等方法能够判断需求是否被 满足

#### 过程

![image-20220421115021192](https://i.ibb.co/zfb7bSq/image-20220421115021192.png)

* 需求开发
* 需求管理

![image-20220421114354571](https://i.ibb.co/86mzZ2m/image-20220421114354571.png)



#### 需求开发

![image-20220421114446279](https://i.ibb.co/x7thByJ/image-20220421114446279.png)

###### 需求获取

是从**人、文档或者环境**当中获取需求的过程

需求获取和需求分析是**交织**在一起的

* 收集背景资料
* 定义项目前景和范围
* 选择信息的来源
* 选择获取方法，执行获取
* 记录获取结果

###### 需求分析

建模来**整合**各种信息，以使得人们更好的理解问题 

为问题定义出一个**需求集合**，这个集合能够为问题界定一个有效的解决方案 

检查需求当中存在的错误、遗漏、不一致等各种缺陷，并加以修正

* 背景分析
* 确定系统边界
* 需求建模
* 需求细化
* 确定优先级
* 需求协商

###### 需求规格说明

获取的需求需要被编写成文档，主要目的是为了在**系统涉众之间交流**需求信息 

* 业务需求被写入项目前景和范围文档 

* 用户需求被写入用户需求文档（或者用例文档） 

* 系统需求被写入需求规格说明

###### 需求验证

确保需求规格说明文档能正确、准确的反映用户的意图

#### 需求管理

保证需求作用在整个软件的产品生命周期中的 续、稳定和有效发挥

* 建立和维护需求基线集
* 建立需求跟踪信息
* 进行变更控制

#### 并发和迭代

![image-20220421115203298](https://i.ibb.co/hBsgqr7/image-20220421115203298.png)

#### 过程模型

软件开发过程



###### 瀑布式模型

![image-20220421115332421](https://i.ibb.co/z6YBZ02/image-20220421115332421.png)

各阶段之间是紧密相关的，后一阶段的工作是依据前一阶段的工作结果而开展的。

###### 快速原型模型

![image-20220421115533344](https://i.ibb.co/H7k69qc/image-20220421115533344.png)

###### 螺旋式模型

将瀑布式模型与快速原型模型**结合**到一起，并加上**风险分析**。

将瀑布式模型与快速原型模型结合到一起，并加上风险分析。

![image-20220421120002130](https://i.ibb.co/hBsgqr7/image-20220421115203298.png)

#### 来源

* 涉众
  * 用户
  * 客户
  * 领域专家
  * 市场人员、销售人员等其他用户代替源
* 相关产品
  * 原有系统
  * 竞争产品
  * 协作产品（与解系统存在接口的其他软件系统）
* 硬数据
  * 登记表格、单据、报表等定量文档
  * 备忘录、日志等定性文档
* 重要文档
  * 原有系统的规格说明
  * 竞争产品的规格说明
  * 协作产品的规格说明
  * 客户的需求文档（委托开发的规格说明、招标书）
* 相关技术标准和法规
  * 相关法律、法规及规章制度
  * 行业规范、行业标准

#### 方法

* 传统方法

  面谈、问卷调查、硬数据分析、文档检查、需求剥离等

* 集体获取方法

  头脑风暴（Brainstorming）、专题讨论会（Workshop）、JAD

* 原型

* 认知方法

  任务分析（Task Analysis）、协议分析（Protocol Analysis）

* 基于上下文的方法

  观察、民族志（Ethnography）和话语分析（Conversation Analysis）

#### 前景和范围

* 前景

  所有的涉众都从共同认同的项目前景出发，理解和描述问题域及需求

* 范围

  范围内的事物和事件是描述的目标

###### 问题分析

* 明确问题
* 发现业务需求

* 确定高层次的解决方案
* 确定系统特性和解决方案的**边界**
* 确定解决方案的约束

###### 建立系统边界

将所有问题的解决方案进行综合，就可以得到整个解系统的功能和边界

系统边界的常用技术描述手段是系统用例图和上下文图

###### 文档

**业务需求、高层次解决方案和系统特性**都应该被定义到项目前景与范围文档之中

#### 涉众分析与硬数据采样

##### 涉众分析

**涉众**：所有能够影响软件系统的实现，或者会被 实现后的软件系统所影响的个人和团体

###### 主要内容

* 根据功能前景寻找涉众
* 从涉众对象获取需求
* 分析涉众的赢输条件，实施共赢策略

##### 硬数据采样

* 定量硬数据
  * 统计报表
* 定性硬数据
  * 组织描述文档
  * 业务指导文档
  * 业务备忘

#### 面谈

###### 类型

* 结构化面谈

  完全按照事先的问题和结构来控制面谈

* 半结构化面谈

  事先需要根据面谈内容准备面谈的问题和面谈结构，但在面 谈过程当中，会见者可以根据实际情况采取一些灵活的策略

* 非结构化面谈

  没有事先预定的议程安排 

  甚至会在没有太多事前准备的情况下就直接到访被会见者的 工作地，就某个主题开展会谈 

  会见者和被会见者谈话的主题可能非常广泛，而且每个主题 都不会非常深入 

  也可能在非结构面谈中仅就某个特殊的主题进行深入的讨

#### 原型

“原型是一个系统，它内化了（capture）一 个更迟系统（later system）的本质特征。 原型系统通常被构造为不完整的系统，以 在将来进行改进、补充或者替代。 ”

###### 类别

* 根据开发方法

  * 探索式（exploratory）
  * 实验式（experimental）
  * 演化式（evolutionary）

  前两种又被称为抛弃式原型

* 根据构建技术

  * 水平原型方法（horizontal prototyping）

    仅仅实现选定功能的某些**特定层次**

  * 垂直原型方法（vertical prototyping）

    触及到选定功能实现的**所有层次**

###### 过程

![image-20220421124152722](https://i.ibb.co/2Y8WDSb/image-20220421124235805.png)

####### 需求内容

* 角色

  指原型物件在用户工作中的价值，也就是说它为什么是对用户有用的。

  原型物件到底能够帮助用户完成什么样的工作

* 外观

  指用户对原型物件的具体感觉体验，即用户在使用原型物件时会看到什么、听到什么和感觉到什么

* 实现

  指原型物件完成功能的细节技术和方法

![image-20220421124406617](https://i.ibb.co/DDG1gcP/image-20220421124406617.png)

####### 评估

####### 修正

## 根本任务

![image-20220422163814670](https://i.ibb.co/6cMgv0T/image-20220422163908238.png)

#### 建立分析模型

 将复杂的系统分解成为简单的**部分**以及它们之间的**联系**，确定**本质特征**

 和用户达成对信息内容的**共同理解**

分析的活动主要包括**识别、定义和结构化**，它的目的是获取某个可以转换为知识的事物的信息

###### 模型

“模型是**对事物的抽象**，帮助人们在创建一个事物之前可以有更好的理解”

集中关注问题的**计算特性**（数据、功能、规则等等）
“它是对系统进行思考和推理的一种方式。建模的目标是建立系统的一个表示，这个表示以精确一致的方式描述系统，使得系统的使用更加容易”
建模方法

* 抽象
  只关注重要的信息，忽略次要的内容

* 分解

  将单个复杂和难以理解的问题分解成多个相对更容易的子问题，并掌握各子问题之间的联系

* 投影
  多视点方法

###### 类别

####### 业务模型

* 使用**问题域中的重要概念**作为模型的**组元**
* 使用**概念之间的业务联系**作为组元之间的关系

使用了业务描述的方式，具有**非形式**化特征

####### 计算模型

* 使用软件的构成单位作为模型的组元
* 软件构建单位之间的关系作为模型组元之间的关系

基于计算科学建立的，具有**形式化**的特征

####### 软件分析模型

* 介于业务模型和计算模型二者之间的模型形式

* 使用了计算模型的组元形式

* 在组元的表现上采用了业务模型的表现方式

具有**半形式化**的特征

#### 创建解决方案

将一个问题分解成独立的、更简单和易于管理的**子问题**来帮助寻找解决方案

帮助开发者建立问题的**定义**，并确定被定义的事物之间的**逻辑关系**

![image-20220422172629026](https://i.ibb.co/DQpc7R4/image-20220422172629026.png)

## 常用技术

* 结构化技术
  * 过程建模
    * 数据流图 DAata Flow Diagram
    * 上下文图 Context Diagram
    * 微规格说明 Mini-Specification
    * 数据字典 Data Dictionary
  * 数据建模
    * 实体关系图 Entity Relationship Diagram
  * 行为建模
    * 状态（转换）图/矩阵 State (Transition) Diagram/Matrix
  * 过程/数据关系建模
    * 功能实体矩阵Function/Entity Matrix
  * 信息工程方法
    * 功能分解图 Function Decomposition Diagram
    * 过程依赖图 Process Dependency Diagram

* 面向对象技术
  * UML
    * 用例图 Use-Case Diagram
    * 类图 Class Diagram
    * 交互图（顺序图/通信图） Interaction ( Sequence/communication ) Diagram
    * 活动图 Activity Diagram
    * 对象约束语言 Object Constraint Language
    * 状态图 State Chart Diagram

## 结构化需求建模

#### 过程建模

结构化分析的核心是数据。数据包括**在分析、设计和实现中涉及的概念、术语、属性等所有内容**，并把这些内容定义在**数据字典**中。围绕数据字典，完成**功能/过程模型、数据模型和行为模型**的结构化建模过程。

![image-20220422184634737](https://i.ibb.co/yNwgvgK/image-20220422184634737.png)





###### 数据流图

![image-20220422190620697](https://i.ibb.co/pQ4W9YB/image-20220422190620697.png)

####### 基本元素

* 数据加工过程

  过程是指**施加于数据的动作或者行为**，它们使得数据发生变化，包括**被转换（transformed）、被存储（stored）或者被分布（distributed）**
  可能是由软件系统控制的，也可能是由人工执行的，它重在数据发生变化的效果而不是其执行者
  可能会表现为不同的抽象层次，其中内容足够细节和具体，能够对其直接进行“编码”处理的过程被称为原始过程（Primitive Process，又称为基本过程Elementary Process）

* 外部实体

  外部实体是指**处于待构建系统之外的人、组织、设备或者其他软件系统**，它们不受系统的控制，开发者不能以任何方式操纵它们
  需要进行建模的外部实体是那些和待构建的软件系统之间**存在着数据交互**的外部实体，它们是待构建系统的**数据源或者数据目的地**
  所有的外部实体联合起来构成了软件系统的**外部上下文环境**

* 数据流

  数据流是指数据的运动，它是系**统与其环境之间或者系统内两个过程之间的通信形式**
  数据流可以**分割和组合**

  ![image-20220422191044022](https://i.ibb.co/ZcZWm04/image-20220422191044022.png)

  **数据字典和实体关系图ERD**通常被用来描述DFD的详细内容

* 数据存储

  数据存储是软件系统需要在**内部收集、保存，以供日后使用的数据集合**
  数据存储的详细内容通常也是用**数据字典和ERD**来进行描述的

####### 构建规则

* **过程是对数据的处理**，必须有输入，也必须有输出，而且输入数据集和输出数据集应该存在**差异**
* 数据流是必须和过程**产生关联**的，它要么是过程的数据输入，要么是过程的数据输出
* DFD当中所有的对象都应该有一个可以唯一标识自己的名称
  * 过程使用动词
  * 外部实体、数据流和数据存储使用名词

####### 层次结构

依据所含过程的不同抽象程度，DFD可以在**不同的抽象层次**上进行系统的描述
一个比较抽象的过程可以被展开为一个子过程更加具体的DFD图

* 上下文图 Context diagram

  将整个系统看做是一个过程，这个过程实现系统的所有功能 ，是系统功能的**最高抽象**。上下文图中**存在且仅存在一个过程**，表示整个系统。这个单一的过程通常编号为0。上下文图中需要表示出**所有和系统交互的外部实体**，并描述交互的数据流，包括**系统输入和系统输出**。上下文图中不会出现数据存储实例，它非常适合于**描述系统的应用环境、定义系统的边界**

* 0层图（顶层图）Level-0 diagram

  位于上下文图下面一层，是上下文图中**单一过程的细节描述**，是对该单一过程的**第一次功能分解**， 是整个系统的**功能概图** 

  0层图应该被描述的简洁、清晰，需求工程师要根据系统的复杂度掌握0层图中过程的抽象程度

* N层图 Level-N diagram

  对0层图的过程分解产生的子图称为1层图，对N层图的过程分解后产生的子图称为N+1层图（N>0） ，过程分解是可以持续进行的， 直至最终产生的子图都是原始DFD图：

  * 所有过程都已经被简化为一个选择、计算或者数据库操作；
  * 所有数据存储都仅仅表示了一个单独的数据实体；
  * 用户已经不关心比子图更为细节的内容，或者子图的描述已经详细的足以支持后续的开发活动；
  * 每一个数据流都已经不需要进行更详细的切分，以展示对不同数据的不同处理方式；
  * 每一个业务表单、事务、计算机的屏幕显示（computer online display）和业务报表都已经被表示为一个单独的数据流；
  * 系统的每一个最低层菜单选项都能在子图中找到独立的过程

  原始DFD图可以进一步展开为

  * 微规格说明
  * 数据字典

  在低于0层图的子图上通常**不显示外部实体**

####### 验证

* 验证DFD的语法
  * 确保DFD中不会发生语法错误
* 验证DFD的结构
  * 验证DFD层次结构之间的一致性
  * 验证DFD层次结构说明的完备性
* 验证DFD的语义
  * 确保DFD所说明内容的正确性和准确性

###### 微规格说明

* 目的：细化原始DFD图 
* 方式 
  * 结构化英语/伪码 
  * 行为图 
  * 决策表 
  * 决策树

###### 数据字典

数据字典以**结构化方式**定义了在建模过程中涉及到的所有数据信息、控制信息。
它是当前系统的软件词典，提供用户和软件人员的概念解释，也提供在系统开发过程中各种有关数据和控制的描述信息，使得系统所有的相关人员对信息有共同的、一致的理解。
常用方式 

* 词条描述

  词条描述为每个数据元素组织描述信息

  ![image-20220422195803167](https://i.ibb.co/rG9pGty/image-20220422195803167.png)

* 定义式

  定义式要求对数据元素（尤其是其结构）的描述要精确、严格和明确

  ![image-20220422195840225](https://i.ibb.co/XpGD5PG/image-20220422195840225.png)

#### 数据建模

数据模型：描述数据的定义、结构和关系等特性的模型说明了问题域和解系统共享的事物、对共享事物的描述和共享事物之间的关系能够反映企业业务的核心知识
建立数据模型的过程被称为数据建模

## 面向对象分析与UML建模

UML（Unified Modeling Language）是一种统一的、标准化的建模语言

* OMT (James Rumbaugh)
* Booch方法(Grady Booch)
* OOSE (Ivar Jacobson）

#### 组成元素

* 基本构造块

  也就是建模元素，是模型的主体

* UML规则

  也就是支配基本构造块如何放在一起的规则

* 公共机制

  运用于整个UML模型中的公共机制、扩展机制

![image-20220422210117052](https://i.ibb.co/vDgtm8Q/image-20220422210117052.png)



##### 基本构造块

* 事物构造块

  对模型中**最具有代表性的成分**的抽象

  * 结构事物：UML中的**名词**，它是模型的静态部分，描述概念或物理元素。

    * 类（class）和对象（object）

      UML中类是用一个矩形表示的，它包含三个区域，最上面是类名、中间是类的属性、最下面是类的方法

      对象则是类的一个实例

    * 接口（interface）

      接口是描述某个类或构件的一个**服务操作集**

    * 主动类（active class）

      主动类实际上是一种特殊的类。引用它的原因，实际上是在开发中需要有一些类能够起到**启动控制活动**的作用

      主动类是指其对象**至少拥有一个进程或线程，能够启动控制活动**的类

    * 用例（use case）

      用例实例是**在系统中执行的一系列动作**，这些动作将生成特定执行者可见的价值结果

       一个用例定义一组用例实例

    * 协作（collaboration）

      定义了**一个交互**，它是由一组共同工作以提供某协作行为的角色和其他元素构成的一个**群体**。

    * 构件（component）

      构件是**系统设计的一个模块化部分**，它隐藏了内部的实现，对外提供了一组外部接口。在系统中满足相同接口的组件可以自由地替换
      可以用来描述实际的PC机、打印机、服务器等软件运行的基础硬件

    * 节点（node）

      运行时存在的**物理元素**，它表示了一种可计算的资源，通常至少有存储空间和处理能力

  * 行为事物：UML中的**动词**，它是模型中的动态部分，是一种跨越时间、空间的行为。

    * 交互（Interaction）

      共同完成某个任务的一组对象之间交换的**信息集合**

    * 状态机（state machine）

      是一个**对象或交互**在生命周期内响应事件所经历的**状态序列**

  * 分组事物：UML中的**容器**，用来组织模型，使模型更加的结构化。

    对于一个中大型的软件系统而言，通常会包含大量的类， 因此也就会存在大量的结构事物、行为事物，为了能够 更加有效地对其进行整合，生成或简或繁、或宏观或微 观的模型，就需要对其进行分组。在UML中，提供了 **“包（Package）”**来完成这一目标

  * 注释事物：UML中的**解释部分**，和代码中的注释语句一样，是用来描述模型的

* 关系构造块

  * 关联关系

    表示两个类之间存在某种**语义上的联系**。关联关系提供了通信的路径，它是所有关系中最通用、语义最弱的。

    在UML中，使用一条实线来表示关联关系

    在关联关系中，有两种比较特殊的关系：聚合和组合

    * 聚合关系：聚合（Aggregation）是一种特殊形式的关联。聚合表
      示类之间的关系是整体与部分的关系
    * 组合关系：如果发现“部分”类的存在，是完全依赖于“整体”类的，那么
      就应该使用“组合”关系来描述

  * 泛化关系

    描述了一般事物与该事物中的特殊种类之间的关系，也就是父类与子类之间的关系

  * 实现关系

    用来规**定接口和实现接口的类或组件之间**的关系。接口是操作的集合，这些操作用于规定类或组件的服务。

  * 拓展关系

    表示将一个**构造型**附加到一个元类（metaclass）上，使得元类的定义中包括这个构造型

  * 依赖关系

    有两个元素X、Y，如果修改元素X的定义可能会引起对另一个元素Y的定义的修改，则称元素Y依赖（Dependency）于元素X

    ![image-20220422211529933](https://i.ibb.co/PNCmVw6/image-20220422211529933.png)

* 图

  ![image-20220422215006859](https://i.ibb.co/BgGhsTv/image-20220422215006859.png)

##### 规则

![image-20220422212655915](https://i.ibb.co/gMKMVkZ/image-20220422212655915.png)

##### 公共机制

* 规格描述

  在图形表示法的每个部分后面都有一个规格描述（也称为详述），它用来对构造块的语法和语义进行文字叙述。 这种构思，也就使可视化视图和文字视图的分离

* 扩展机制

  * 构造型

    在实际的建模过程中，可能会需要定义一些**特定于某个领域或某个系统**的构造块

  * 标记值

    用来为事物**添加新特性**。标记值的表示方法是用形如“{标记信息}”的字符串

  * 约束

    是用来**增加新的语义或改变已存在规则**的一种机制。约束的表示法和标记值法类似，都是使用花括号括起来的串来表示，不过它是不能够放在元素中的，而是放在相关的元素附近

#### 模型划分

* 用例模型 Use Case Model

  描述使用系统功能的角色和系统相关的功能，是需求建模的重要工具

* 静态模型（领域模型）

  * 类图（class diagram）

    类图是系统模型的基础，描述系统的静态结构

    * 对象层：描述系统实体以及承载的系统责任 
    * 特征层：描述实体抽象的特征 
    * 关系层：实体类的固有关系

  * 包图（package diagram）

    描述系统的组织模型，为控制表示的复杂性

* 动态模型（行为模型）

  * 顺序图（sequence diagram）

    描述按时间顺序排列的对象交互

  * 协作图（collaboration diagram）

    表示交互对象的行为组织结构

  * 状态转换图（state chart diagram）

    描述对象在生命周期内，响应事件的状态转换过程，以及响应事件后所做的反映

  * 活动图（activity diagram）

    用来描述任务流程或算法过程，可用来分析系统并发事务流程

* 物理实现

  * 部署图（deplotment diagram）

    用来描述**系统中计算结点的拓扑结构**，一个系统只有一个部署图，可用来分析分布式系统

  * 构件图（component diagram）

    描述一组构件以及相互间的关系，是系统实现的物理建模

#### 建模过程

![image-20220422215919066](https://i.ibb.co/CMw2wDQ/image-20220422215919066.png)

#### 用例模型

用例图（Use Case）用于对**系统的功能及与系统进行交互的外部事物**建模

![image-20220422220151742](https://i.ibb.co/37st6wk/image-20220422220151742.png)

##### 用例

一个用例描述系统的**一项功能**，该项功能可被描述为参与者可视的**一组操作**，其中的每个操作表示参与者与系统的**一个交互过程**

用例描述系统外部可见的功能需求，只描述做什么，不描述怎么做
多数是由参与者发起的动作，也允许系统发起的动作，例如：异常情况处理

##### 用例关系

* 包含关系《include》：描述用例间具有的公用行为
* 扩展关系《extend》 ：描述用例间可选的独立行为
* 泛化关系 generalization ： 用例之间的继承关系

#### 静态模型

###### 面向对象建模

类图，是系统建模过程中最重要的部分，也是花费精力最大的活动。类图描述系统中各个对象之间存在的关系，表达系统的静态结构，也叫做“对象建模”

###### 接口类

把类的公共可见性操作组织在一起， 提供的服务集合

接口类作为类之间**交互操作的契约**

###### 包图

包是对模型成分分组的机制

多个包可以形成严格的树形层次结构，用于描述系统的组织结构

一个包可以嵌套在另一个包内，内层的包成分，同时属于内层和外层两个包。

#### 动态模型

...

#### 物理实现

构件图Component Diagram 与部署图Deployment Diagram 是在系统设计时，用来表示系统软件成分以及之间关系结构的工具

分析构件及其间的关系，并对它们在运行节点上的成分给与描述，也叫“物理事物建模”

##### 构件图

类表示逻辑抽象，是逻辑模块，构件表示机器空间中的物理模块，是逻辑元素及协作关系的物理实现

类有属性和操作，构件仅通过接口向外提供可请求的操作

###### 构件种类

* 部署构件

  可用于构造的执行系统，如：动态连接库（DLL）和可执行程序（EXE）

* 产品构件

  开发过程的产物，包括创建部署构件的源代码文件及数据文件等

* 可执行构件

  由执行系统创建的构件

##### 部署图

分析构件及其间的关系，并对它们在运行节点上的成分给与描述，也叫“物理事物建模”

构件是系统执行的事物，节点是执行构件的事物。
构件代表逻辑元素的物理打包，节点可表示构件的物理部署

节点上可以有一个或多个构件，一个构件也可以部署在一个或多个节点上。

## 需求验证

#### 方法

* 评审

  由作者之外的其他人来检查产品问题的方法
  是**主要的静态分析手段**
  原则上，每一条需求都应该进行评审

* 原型与测试

* 开发测试用例

  如果无法为某条需求定义完备的测试用例，那么它可能就存在着模糊、信息遗漏、不正确等缺陷

* 用户手册编制

* 利用跟踪关系

  * 业务需求 -> 用户需求 -> 系统需求

    如果业务需求和用户需求没有得到后项需求（用户需求和系统需求）的充分支持，那么软件需求规格说明文档就存在不完备的缺陷。

  * 系统需求 -> 用户需求 -> 业务需求

    如果不能依据跟踪关系找到一条系统需求的前项用户需求和前项业务需求，那么该需求就属于非必要的需求。

* 自动化分析

## 需求管理

* 维护需求基线
* 实现需求跟踪
* 控制变更

#### 需求基线

已经通过**正式评审和批准**的规格说明或产品，它可以作为进一步开发的基础，并且只有通过**正式的变更控制过程**才能修改它
定义：是被明确和固定下来的需求集合，是项目团队需要在某一特定产品版本中实现的特征和需求集合

![image-20220422230125870](https://i.ibb.co/MVBfJHz/image-20220422230125870.png)

##### 描述内容

* 标识符（ID），为后续的项目工作提供一个共同的交流参照。
* 当前版本号（Version），保证项目的各项工作都建立在最新的一致需求基础之上。
* 源头（Source），在需要进一步深入理解或者改变需求时，可以回溯到需求的源头。
* 理由（Rational），提供需求产生的背景知识。
* 优先级（Priority），后续的项目工作可以参照优先级进行安排和调度。
* 状态（Status），交流和具体需求相关的项目工作状况。
* 成本、工作量、风险、可变性（Cost、Effort、Risk、Volatility），为需求的设计和实现提供参考信息，驱动设计和实现工作。
* 需求创建的日期；
* 和需求相关的项目工作人员，包括需求的作者、设计者、实现者、测试者等；
* 需求涉及的子系统；
* 需求涉及的产品版本号；

#### 需求跟踪

避免在开发过程或者演化过程中与需求基线不一致或者偏离的风险

* 前向跟踪是指被定义到软件需求规格说明文档之前的需求演化过程
  * 向前跟踪到需求：说明涉众的需要和目标产生了哪些软件需求
  * 从需求向后回溯：说明软件需求来源于哪些涉众的需要和目标
* 后向跟踪是指被定义到软件需求规格说明文档之后的需求演化过程
  * 从需求向前跟踪：说明软件需求是如何被后续的开发物件支持和实现的
  * 回溯到需求的跟踪：说明各种系统开发的物件是因为什么原因（软件需求）而被开发出来的

#### 需求变更控制

以可控、一致的方式进行需求基线中需求的变更处理，包括对变化的评估、协调、批准或拒绝、实现和验证
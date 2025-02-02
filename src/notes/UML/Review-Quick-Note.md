---
title: UML复习简记
# cover: /assets/images/cover1.jpg
icon: page
# This control sidebar order
order: 1
author: chiichen
date: 2024-01-06
category:
  - 课程笔记
tag:
  - UML
# this page is sticky in article list
sticky: false
# this page will appear in starred articles
star: false
footer:
isOriginal: true
copyright: 转载请注明出处
---

## 第一章

- 分析-设计：提出问题-解决问题
- 用例(use case)：人们使用应用的情节或者场景
- 领域模型(domain model)：不是对软件对象的描述，是对真实世界中的概念的一种可视化，也被称为概念对象模型。
- 顺序图(交互图的一种)：用来描述软件对象之间的信息流
- 设计类图(design class deagram)：表述软件类，缩小代码和领域模型之间的差距，被称为低表示差距(lower representational gap)
- UML 的三种应用方法：草图、蓝图(逆向工程：代码可视化，便于理解；前向工程：指导代码生成)、编程语言
- 敏捷建模(agile modeling)强调了把 UML 作为草图的方式
- UML 的三种透视图：概念透视图(描述现实世界中的事务)，规格说明软件透视图(描述软件的接口等信息，但是不约定特定实现)，实现透视图(描述在指定技术例如 java 中的实现)
- 相对应的，在这三种图中的 UML 类被分别称为概念类(conceptual class)、软件类和实现类

## 第二章

- 瀑布模型相对的是迭代和进化式开发
- RUP：RUP 是一个以用例驱动、以体系结构为核心、迭代及增量的软件过程模型，由 UML 方法和工具支持，广泛应用于各类面向对象项目。
- 统一过程(UP)：可以引入其他迭代方法中的有用实践，可以应用于敏捷过程。
- 时间定量：迭代必须严格按照时间进行(2-6 周)。如果不能实现，应该去除一些任务需求，而不是延期。
- 瀑布模型：试图在编程之前就详细定义大部分需求，并且进行完整的设计。
- UP 提倡风险驱动和客户驱动相结合的迭代计划，而前者包含了以架构为中心(architecture-centric)迭代开发的实践
- 敏捷开发包含多种具体实践，敏捷原则：持续交付、需求变更、开发与业务合作
- 敏捷建模：不是画一大堆图然后给别人写成代码，模型是用来理解、共享的，开发者应该为自己的 OO 设计建模，
- 敏捷 UP：对项目不要有详细的计划，指定预估结束日期和主要里程碑的高阶计划(阶段计划)。对里程碑也不能有细粒度的步骤，只能预先对一个迭代指定详细计划(迭代计划)
- UP 的四个阶段：初始、细化、构造、移交
- UP 的科目(discipline)：就是在 UP 开发的时候干的活，例如建模、设计、需求、实现等
- UP 的制品(artifact)：就是对科目中产出的东西的统称，例如代码、图、文档、模型。
- 开发案例：就是描述 UP 制品的开发文档

## 第三章

- POS 机：不同用户可能有不同的业务规则，因此需要我们能够提供这种灵活性和定制能力。
- 大富翁游戏

## 第四章 初始不是需求阶段

- 初始阶段就是用来预估项目的范围、业务案例，以及确定项目的可行性等问题。以及包含第一次需求研讨会和第一次迭代计划的制定。
- 大多数需求分析是在细化阶段进行的，伴随着具有产品品质的早期编程和测试。
- 初始阶段会完成一部分的制品，在后续迭代中进行精化，除非认定制品很可能具有实用价值，不然就不应该创建。
- 初始阶段可以列出大部分期望的用例名称和参与者的姓名，然后详细描述其中的 10%，来对问题范围获取一定的认知。

## 第五章 进化式需求

- 需求就是项目必须提供的能力和必须遵守的条件。
- UP 推崇“用一种系统的方法来寻找、记录、组织和追踪系统不断变更的需求”，而不是试图在第一个阶段就固化所有需求。
- 在 UP 和大多数进化式方法中，编程和测试要远大于大多数需求的分析或者规格化。可能只会完成 10-20%的需求规格说明，而这些需求也是具有重要架构意义、重大风险、高业务价值的需求。
- 瀑布方法是传统大规模制造业项目所采用的方法，其低变更率、可预测性与软件行业的高变更率与不可预测性恰好相反，软件项目平均需求变更率为 25%，因此试图在开始就定义、固化所有需求的方法都有本质上的缺陷。
- FURPS+：在 UP 中，需求按照 FURPS+模型进行分类，包括**功能性(Functional)**，**可用性(Usability)**(帮助、文档等)，**可靠性(Reliability)**，**性能(Performance)**，**可支持性(Supportability)**(国际化、可配置性等)。FURPS+中的"+"是指其他辅助性和次要的因素，例如实现(Implementation)(资源限制、语言工具、硬件等)，接口(Interface)，操作(Operation)，包装(Packaging)，授权(Legal)(许可证或其他)
- 可用性、可靠性、性能、可支持性被称为**质量属性**、质量需求或者“某属性”。一般使用中，按照功能性(行为的)和非功能性(所有非行为的)来进行区分。
- UP 的关键制品：
  - **用例模型**
  - **补充性规格说明**(用例之外的所有内容，用于所有**非功能需求**，例如性能和许可发布，也可以记录没有表示为用例的功能特性，例如报表生成)
  - **词汇表**(定义术语，包含数据字典——记录了对数据的需求，例如有效性规则、容许值等。还可以记录对象属性、操作的参数、报表布局等信息)
  - **设想**(概括了高阶需求)
  - **业务规则**：描述了凌驾于某一项目的需求或政策，通常是由领域或业务所要求的，例如税收法规

## 第六章 用例

- 用例是文本形式的情节描述，说明参与者使用系统以实现目标。例如：
  - 处理销售：顾客携带所购买的商品到达收银台。收银员用 POS 系统记录每件商品。系统连续显示累积总额，并逐行显示细目。顾客输入支付信息，系统对支付信息进行验证和记录。系统更新库存信息。故可从系统得到购物小票，然后携带商品离开。
- 参与者可以是人、计算机系统或者组织
- 场景是参与者和系统之间一系列特定的活动和交互，也成为用例实例
- 用例就是一组相关的成功和失败场景的集合。
- 一组用例的实例，其中每个实例都是系统执行的一系列活动，这些活动产生了对某个参与者而言可观察的返回值
- 用例是文本文档而非图形，用例建模是编写文本的活动而非制图。
- 用例就是需求，主要是 F(功能)类需求，另一种观点认为用例定义了系统行为的契约。
- 参与者是任何具有行为的事务，在**所讨论系统(Ststem under Discussion, SuD)** 调用其他系统的服务时，SuD 也是参与者。相对于 SuD，有三种外部参与者：
  - 主要参与者(primary actor)：具有用户目标，通过使用 SuD 的服务完成。例如收银员。确定主要参与者来发现驱动用例的用户目标
  - 协助参与者(supporting actor)：为 SuD 提供服务。如自动付费授权服务。协助者通常为计算机系统，但也可以是组织或人。
  - 幕后参与者(offstage actor)：在用例行为中有影响或者有利益，但不是主要或协助参与者，例如政府税收机构。
- 用例的三种常用形式：摘要、非正式、详述
- 详述用例：看 pdf 的 68 页到 73 页：
  - 范围：范围界定了要设计的系统。有描述系统的**系统用例**和描述使用者使用方法的**业务用例**
  - 级别：**用户目标级别** 常用，描述了实现主要参与者目标的场景，大致相当于业务流程工程中的基本业务流程,例如支付。**子功能级别** 用例描述支持用户目标所需的子步骤，通常当多个用例有共享的重复子步骤时，就将其分离出来，例如使用信用卡支付。
  - 主要参与者：就是主要参与者
  - 涉众及其关注点列表(**重要** )：用例应当包含满足所有涉众关注点的事务。
  - 前置条件：给出在用例中场景开始前必须永远为真的条件，在用例中不会检查前置条件(指的是没有 if-else 来确定其为真)。而前置条件隐含已经成功完成的其他用例场景，例如登录。只传达值得注意的假设，例如“应当有电”这种条件时无意义的。
  - 成功保证(后置条件)：给出用例成功后必须为真的事务，包括**主成功场景及其替代路径**
  - 主成功场景和步骤(或基本流程)：也被称为理想路径或者基本流程。它不包括任何条件或者分支，条件和分支处理都放到扩展部分。场景记录三个步骤：参与者之间的交互，确认过程，系统完成的状态变更。
  - 扩展：例如在主成功场景的第三步的三个分支，就会分别被标记为"3a"和"3b"，扩展由条件和处理两部分组成，尽可能使用系统或者参与者能够检测到的事务作为条件。
  - 特殊需求：例如对质量的约束(可靠性、性能)和设计约束(I/O 设备)
  - 技术和数据变元表：记录在实现系统的过程中产生的变元，例如用户可以用条码扫描器或者键盘输入商品 ID、暂时是纸质前面，但是预估两年后会使用数字签名
- 本质(essential)风格的用例编写：摒除用户界面，而关注参与者的意图，例如管理员进行身份认证
- 具体风格的用例编写：例如管理员在对话框中输入 ID 和口令进行身份认证。应在早期需求工作中避免。
- 黑盒用例：不描述系统内部的工作，只描述系统的职责，例如系统要做什么。
- 发现用例的过程：
  1. 选择系统边界：个人 or 组织？软件 or 硬件+软件？如果设计的不明确，可以通过后面对系统外部事务(外部主要参与者和协助参与者)的定义加以明确。
  2. 确定主要参与者
  3. 确定每个主要参与者的目标
  4. 定义满足用户目标的用例。每个目标都应有一个以动词开头的用例，例如处理销售，例外时 CRUD 可以合并为一个用例"管理 XX"
- 用例测试：
  - 老板测试：老板问你做了什么，你说登陆系统！老板不满意，就没通过测试，但是没通过老板测试并不意味不重要，例如用户认证
  - EBP 测试(Elementary Business Process)：即基本业务过程测试，类似于老板测试，强调业务价值可量化，用例包括多个步骤，但是也不会持续数日，可能是几分钟到一小时，强调用例增加的可观察或可量化的业务价值。
  - 规模测试：就是不能把步骤当成了用例，例如输入 ID 是一个步骤，而不是用例
    ![[用例测试.png]]
- 用例图是用来与参与者-目标列表关联的简单图

![[resource/大二下/UML/用例图.png]]

- 非功能性需求、报表布局、领域规则等写入 UP 的补充性规格说明中去。
- 在例如应用服务器、数据库产品这种特性驱动型项目中，用例就不是那么合适了，就适合用详细特性列表而不是用例。
- UP 提倡用例驱动开发：功能需求首先记录在用例中，用例也是迭代计划的重要部分。功能或系统测试应当符合用例的场景。
- 用例编写阶段：
  - 初始阶段：会着重编写大部分需要关注的、复杂的、具有风险的用例，平均每个花费两分钟，然后以详述形式编写其中的 10-20%的用例
  - 细化阶段：详细编写 80-90%的用例列表，以详述形式编写和重新编写更多的用例
  - 构造阶段：着重于完成系统，只需要编写一些次要案例和偶尔的需求分析会。

## 第七章 其他需求

- 不是 OOA/D 的需求，因此可以略过，等回来再看

## 第八章 细化迭代 1——基础

- 迭代中的需求和用例是不断增加的，同一用例也是增量式开发的
- 初始阶段发生了什么：
  ![[初始阶段发生了什么.png]]
- 一句话来概括细化：构建核心架构、解决高风险元素、定义大部分需求、以及预计总体进度和资源
- 细化过程中搭建的核心架构不是一个实验性的架构，而是会成为将来系统的一个子集。
- 通过风险、覆盖范围和关键程度来组织需求和迭代。

## 第九章 领域模型

- 对领域模型应用 UML 类图表示法会产生概念透视图(conceptual perspective)模型
- 确定一组概念类是 OO 分析的核心。
- 领域模型是对领域内概念类或者现实世界中对象的可视化表示，又被称为概念模型，领域对象模型、分析对象模型。
- UP 对领域模型的定义是，在业务建模中创建的制品之一。准确的说，UP 领域模型是 UP 业务对象模型(BOM)的特化，应用 UML 表示法，英语模型被描述为一组没有定义操作的类图。它提供了概念透视图。可以表示：
  - 领域对象或者概念类、概念类之间的关联、概念类的属性。
- 领域模型又被称为“可视化字典”，因为它通过抽象的形式展示了领域内元素之间的联系
  ![[领域模型避免.png]]
- 概念类可以从符号、内涵、外延三个来考虑，例如考虑购买交易事件的概念类，那么可以用符号 Sale 来命名、把 Sale 的内涵陈述为“表示购买交易的事件”，Sale 的外延就是所有销售的例子，也就是世界上所有销售实例的集合。
- 领域模型不是数据模型，领域模型允许没有属性的概念类
- 找到概念类的三条策略：

  1. 重用和修改现有的模型。许多领域都有以及设计好、绘制好的领域模型和数据模型
  2. 使用分类列表
     ![[分类列表.png]]
  3. 确定名词短语：从对领域的文本性描述中识别名词和名词短语，作为候选的概念类或者属性。
     ![[名词分析.png]]

- 关联以“类名——动词短语——类名”的方式命名。关联的方向箭头没有含义，关联的每一端称为角色
  ![[角色多重性.png]]

- 属性：大部分属性默认为私有
  ![[属性.png]]
- 导出属性：如果某些值可以通过关联的多重性的实际值计算出来就被表示为导出属性。
  ![[属性表示.png]]
- 属性应该是数据类型：就是普通的结构体或者枚举，不应该把一个复杂的像类一样的东西当成属性，而应该把它用关联链接
- 任何属性都不应该表示外键(就是与其它对象相关联的属性)
  ![[属性与外键.png]]

## 第十章 系统顺序图

- 系统顺序图(SSD)是阐述系统相关的输入输出事件简单创建的制品。它们是操作契约和(最重要的)对象设计的输入。
- SSD 中的操作可以在操作契约中进行分析，在词汇表中被详细描述，而且(最重要的)作为设计协作对象的起点。
  ![[UP制品关系.png]]
- 参与者对系统发起系统时间，通常需要某些系统操作对这些事件加以处理
- 下图为系统顺序图，并使用交互框(interaction frame)来表示顺序图中的循环
  ![[流程图.png]]

## 第十一章 操作契约

- 操作契约使用前置和后置条件的形式，描述领域模型里对象的详细变化，并作为系统操作的结果。
  ![[操作契约.png]]
- 后置条件：不是操作过程中执行的操作，而是对领域模型对象观察的结果，大概有三种类型：创建或删除示例、属性值的变化、形成或消除关联
- 创建契约：
  1. 从 SSD 中确定系统操作。
  2. 如果系统操作复杂，结果可能不明显，或者用例不清楚，可以为其构造契约。
  3. 通过三种类型来描述后置条件

## 第十二章 从需求到设计——迭代进化

- 尽早引起变更，分析和建模实际上只需要几小时或者几天。

## 第十三章 逻辑架构和 UML 包图

- 逻辑架构(LA)是软件类的宏观组织结构，它将软件类组织为包(或者命名空间)、子系统和层等。
- 相应的，如果确定了如何在不同操作系统进程或网络中物理的计算机上对这些元素进行部署的架构被称为部署架构。
- 严格分层架构中，上层只能调用与其相邻的下层的服务，在网络协议栈中常见，通常使用宽松的分层架构，高层可以调用其下任何层的服务。
- UML 的依赖线是有箭头的虚线，箭头指向被依赖的包。
- 应用逻辑层更准确的名字是架构的领域层，其内的软件对象称为领域对象。
- 垂直分层(layer)和水平分区(partition)
  ![[垂直分层和水平分区.png]]
- 试图把外部资源放在低于基础层的层中是错误的，因为外部资源例如数据库是部署视图的内容

![[外部资源.png]]

- 模型——视图分离，或者进一步的 MVC 模型——视图——控制器模型都要求模型对象不直接与视图对象连接

## 第十四章 迈向对象设计

- 对象模型有两种类型：动态和静态，动态模型有助于设计逻辑、代码行为和方法体，例如 UML 交互图(顺序图或者通信图)，静态模型有助于设计包、类名、属性和方法特征标记，例如 UML 类图。
- 我们应该把时间花费在交互图而不仅是类图上

## 第十五章 UML 交互图

- 交互图包括顺序图和通信图
  ![[顺序图.png]]
  ![[通信图.png]]
  ![[顺序图与通信图优劣.png]]

- 生命线框图并不完全等于类的实例
  ![[生命线框图.png]]

- 基于生命线框图的顺序图基本表示法

![[顺序图画法1.png]]

- 顺序图中消息的返回结果可以用消息返回语法 return Var = message(para)或者在活动条末端使用应答消息线
  ![[顺序图画法2.png]]
  ![[顺序图画法3.png]]
  ![[顺序图画法4.png]]
  ![[顺序图画法5.png]]
  ![[顺序图画法6.png]]
  ![[顺序图画法7.png]]
  ![[顺序图画法8.png]]
  ![[顺序图画法9.png]]
  ![[顺序图画法10.png]]

- 通信的链和消息：
  ![[通信图画法1.png]]
  ![[通信图画法2.png]]
  ![[通信图画法3.png]]
  ![[通信图画法4.png]]
  ![[通信图的画法5.png]]
  ![[通信图画法6.png]]
  ![[通信图画法7.png]]
  ![[通信图画法8.png]]
  ![[通信图画法9.png]]

## 第十六章 UML 类图

![[类图画法1.png]]

- 在概念透视图里，类图可以用于将领域模型可视化，为了区分使用在软件透视图和设计透视图中的类图。此时常用的建模术语是设计类图(Design Class Diagram, DCD)，所有 DCD 集合形成了设计模型的一部分，设计模型其他部分还包括 UML 交互图和包图。
  ![[类图画法2.png]]
- 何时使用属性文本，何时使用关联线？
  ![[类图画法3.png]]
- 集合属性的表示
  ![[类图画法4.png]]
- 类图中表示方法体
  ![[类图画法5.png]]

- 在类图中，使用虚线依赖线来描述对象之间的全局变量、参数变量、局部变量和静态方法的依赖
  ![[类图画法6.png]]

- 接口的画法：
  ![[类图画法7.png]]

- 约束的三种画法：
  ![[类图画法8.png]]

- 限定约束，例如 Catalog 中有许多 Description，而可以通过唯一的 ID 选择一个 description
  ![[类图画法9.png]]

- 关联类，允许将关联本身作为类，例如公司雇佣了许多人，用 Employ 作为关联，那么关联类中就会包含工资、起聘日期等信息
  ![[类图画法10.png]]

- 单例模式：
  ![[类图画法11.png]]

- 模板类略过，主动类：
  ![[类图画法12.png]]

- 交互图与类图之间的关系：
  ![[类图画法13.png]]

## 第十七章 GRASP 基于职责设计对象

- RDD：职责驱动设计
- 对于 OO 设计来说，分配职责的基本模式是 GRASP，对于更高级的设计思想应该用 GoF 模式。
- 创建者模式：但是在对象创建较为复杂的时候，通常会采用工厂模式而不是创建者模式。
  ![[创建者模式.png]]

- 信息专家模式：完成职责需要其他对象信息，因此拥有这些信息多少最好被分配职责，例如 Square 都聚集在 Board 中，那么需要 Square 完成的职责就最好被分配在 Board 中。
  ![[信息专家模式.png]]

- 低耦合
  ![[低耦合.png]]

- 控制器：控制器回答了在 UI 层之上哪个对象首先从 UI 层接收该消息
  ![[控制器.png]]

- 高内聚：实际上如果低内聚就必然带来高耦合

## 第十八章 使用 GRASP 的对象设计示例

- 用例指出了 SSD 中所示的系统操作，而领域层交互图阐述了对象如何交互以完成所需的任务。
- 详见书本十八章

## 第十九章 可见性设计

- 属性可见性——B 是 A 的属性
- 参数可见性——B 是 A 中方法的参数
- 局部可见性——B 是 A 中方法的局部对象(不是参数)
- 全局可见性——B 具有某种方式的全局可见性

## 第二十章 将设计映射为代码

- 类的实现要按照耦合度最低到耦合度最高的顺序来完成
- 测试驱动开发：先写测试，然后写一点代码，确保能通过测试之后再写一点测试和代码

## 第二十一章 测试驱动开发和重构

- 极限编程所提倡的就是先编写测试，以及不断重构代码以改进质量
- 测试驱动开发(TDD)是迭代和敏捷 XP 方法所提倡的
- 提炼方法、提炼常量、引入解释变量、用工厂方法代替构造器都是重构的方法

## 第二十二章 UML 工具和 UML 蓝图

无内容

## 第二十三章 迭代 2：更多模式

- 迭代一结束的时候，所有软件都已经被充分测试
- 迭代二着重于用职责和 GRASP 进行对象设计，并应用一些 GoF 设计模式。

## 第二十四章 快速地更新分析

- 因为本次迭代增加了对例如税金计算器等外部资源的使用，因此需要更新 SSD
  ![[ssd更新.png]]

## 第二十五章 GRASP：更多具有职责的对象

- 多态：不要测试对象的类型、也不要使用条件逻辑来执行基于类型的不同选择
  ![[多态.png]]

- 纯虚构：比如要实现数据库存储，没有领域对象是适合实现这个方法的，那么我们就会创建一个 PersistenStroage 类专门用来和数据库通信，它不是领域概念，知识为了便于软件开发凭空捏造或虚构的概念。
- 间接性：为了避免过多耦合，将职责分配给外部对象
  ![[间接性.png]]

- 防止变异：就是防止某一部分的变化或不稳定性对其他部分产生不良影响，常见的做法就是预测会发生变化的地方，并用接口或者间接性的方法来做中介
  ![[防止变异1.png]]
  ![[防止变异2.png]]

- 不要和陌生人讲话：指的是不要和过远的对象通信，反例如下：
  ![[不要和陌生人讲话.png]]

## 第二十六章 应用 GoF 设计模式

- 适配器模式：
  ![[适配器模式.png]]
- GoF 和 GRASP 的关系
  ![[GoF和GRASP的关系.png]]

- 工厂模式
  ![[工厂模式.png]]

- 单例模式：通常用于工厂对象和外观模式
  ![[单实例模式.png]]
- 策略模式：例如销售策略、定价策略、折扣策略是经常变化的，怎么容纳这么频繁的变化，语境对象例如 Sale，需要策略对象的属性可见性，策略对象拥有 Sale 的属性可见性
  ![[策略模式.png]]

- 组合：可能同时有多种策略，这些策略可能同时使用一部分，那么 Sale 就要不停判断如何去分派任务，这种时候就要把一组策略放在一个组合中
  ![[组合模式1.png]]
  ![[组合模式2.png]]
- 外观：就是把一堆对象、接口、实现封装在一个外观对象中，使得需要使用这一堆对象的地方只会和这个外观对象耦合，而不会和一堆对象耦合，通常也是用单实例类进行访问的。
  ![[外观.png]]

- 观察者模式：用来避免领域层对 UI 层的访问，例如 Sale 更新后要更新 UI，通过让 UI 监听 Sale 来避免这种访问。
  ![[观察者模式.png]]
  ![[观察者模式2.png]]

## 第二十七章 迭代三——中级主题

- 迭代三：更多 GoF 模式、架构分析，尤其是 N+1 视图模型，UML 活动图

## 第二十八章 UML 活动图及其建模

- 活动图包括动作(action)、分区(partition)、分叉点(fork)、连接点(join)和对象节点(object node) 等
  ![[活动图画法1.png]]
- 数据流建模(DFD)
  ![[数据流建模.png]]
  ![[数据流建模2.png]]

- 活动图其他画法：
  ![[活动图画法2.png]]
- 对于简单的业务过程，用例文本就足够了，活动图用来描述复杂的业务过程
- 可以使用多级的活动图，来表示不同抽象水平的对象
- 过程活动图示例：
  ![[活动图画法3.png]]
- 统一过程的规程之一是业务建模，而业务建模的关键制品是业务对象模型(UP 中领域模型的超集)。

## 第二十九章 状态机图和建模

![[状态机图1.png]]

- 如果对象对某事件的响应总是相同，就说这个对象对这个事件状态无关，对所有事件都无关的对象称为状态无关对象。相反，状态依赖对象对事件的响应根据对象的状态或模式而不同。

- 转换可以有一个条件测试，只有测试通过才发生转换，又被监护条件
  ![[状态机图2.png]]
  ![[状态机图3.png]]

## 第三十章 用例关联

- 用文本和图形两种形式，使用包含和扩展关联将用例联系在一起
- 包含关系：
  ![[用例包含关系.png]]

- 异步事件包含关系：
  ![[包含关系2.png]]

- 具体用例指的是一个完整行为，通常是基本业务过程用例。例如处理销售。抽象用例永远不能被自己实例化，只能作为其他用例的子功能用例。例如处理信用卡支付是抽象用例，它不能独立存在，只能作为例如处理销售用例的一部分
- 而包含其他用例或者被其他用例扩展、泛化的用例被称为基础用例，例如处理销售包括处理信用卡支付，它就是一个基础用例。而被包含、或者扩展其他用例的用例被称为附加用例，例如处理信用卡支付。附加用例通常是抽象用例。基础用例通常是具体用例。

- 扩展用例：在不修改原始文本的前提下，向用例添加内容
  ![[扩展用例.png]]

- 用例图：
  ![[用例图 1.png]]

## 第三十一章 领域模型的精化

- 概念分类列表：
  ![[概念分类列表.png]]

- 名词短语识别：
  ![[名词短语识别.png]]
- 泛化就是把一组相似的概念组织成一个泛化——特化类层次结构(或简称类层次结构)
  ![[泛化.png]]
- 概念超类的定义必须 100%适用于子类，子类的属性和关联必须 100%与超类一致
  ![[子类超类一致性.png]]
- 子类是超类集合的一个成员，换句话说，概念子类是”一种“(is a kind of)超类。这种一致性被称为 is-a 规则，也就是子类是一种(is-a)超类。每个子类都要满足 100%规则核 Is-a 规则。
- 如果一个类的实例必须是其特化的某个子类实例之一，那么就是抽象概念类
  ![[抽象概念类.png]]

- 对变化的状态的建模，要么就建模为一个状态类超类，要么就不在领域模型中表示，在状态图中反映。
- 关联类：如果某个属性与关联有关、或者关联类的实例依赖于关联的生命周期、或者两个概念之间有多对关联，且存在与关联自身相关的信息
- 关联的每一端都是一个角色
  ![[关联角色.png]]

- 导出元素可以由其他元素确定，属性和关联是最常见的导出元素
  ![[导出元素.png]]

- 包的引用和依赖
  ![[包的引用.png]]
  ![[包的依赖.png]]

## 第三十二章 更多的 SSD 和契约

- 略 可见书 32 章

## 第三十三章 架构分析

- 在 UP 中，甚至早于第一次开发迭代时就应开始架构分析，例如多语言、高并发等问题要在开始就确定。
- 架构分析是在功能性需求的语境中，识别和处理系统非功能性需求的活动。包括识别变化点和最具可能性的进化点。
- 记录架构的选择、决策以及动机，被称为技术备忘录、问题卡、架构途经文档(SEI 架构建议)
- 关注分离：模块化、装饰者、面向切片编程
- 架构性因素(或者需求)被记录在补充规格说明中，解决这些需求的决策被记录在软件架构文档(SAD)中

## 第三十四章 逻辑架构的精化

32 章之后的卓越班老师没讲，就过一遍就好了。

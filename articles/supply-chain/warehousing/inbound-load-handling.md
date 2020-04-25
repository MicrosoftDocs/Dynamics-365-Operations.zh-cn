---
title: 仓库对采购订单入站负荷的处理
description: 此主题介绍仓库对采购订单入站负荷的处理流程。
author: omulvad
manager: AnnBe
ms.date: 03/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2020-03-21
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 709a75a259b1f8daa5b72e76b56942573c403f43
ms.sourcegitcommit: 3a823444005d316bd95fc663e2dbc8252ac7d93a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261304"
---
# <a name="warehouse-handling-of-inbound-loads-for-purchase-orders"></a>仓库对采购订单入站负荷的处理

此主题介绍仓库对采购订单入站负荷的处理流程。

对于每项入站负荷，系统中应该已经有了一个相关采购订单，并且还可能有相关负荷规范和/或运输计划。 有关如何创建和管理入站负荷的详细信息，请参阅[业务流程：计划入站负荷的运输](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/business-process-planning-transportation-for-inbound-loads)。

## <a name="overview-how-inbound-loads-are-created-registered-and-received"></a>概述：如何创建、登记和接收入站负荷

下图显示具有采购订单数量的入站负荷到达仓库时的典型处理流程。

![入站负荷处理流程](media/inbound-process.png "入站负荷处理流程")

1. **供应商确认采购订单。**

    当采购订单被输入系统，然后交付给确认该订单的供应商时，此流程开始。 必须已有采购订单，才能创建入站负荷记录。 但是，即使尚未确认订单，也可以创建入站负荷。 有关详细信息，请参阅[审核和确认采购订单](../procurement/purchase-order-approval-confirmation.md)。

1. **创建采购订单记录是为了计划到达及其内容。**

    入站负荷表示供应商装运了一个或多个采购订单的内容。 负荷应该作为一个物理运输单元（如整车）到达仓库。 入站负荷记录用于计划用途，可供物流协调员跟踪负荷从供应商开始的进度。 还用于通过仓库操作（如到达和入库工作）登记订单行数量和管理进度。 负荷可以自动或手动创建，还可以基于采购订单或供应商的发货通知 (ASN)。 有关详细信息，请参阅[创建或修改入站负荷](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/create-or-modify-an-inbound-load)。

1. **供应商确认负荷分派。**

    供应商分派负荷后，收货仓库的物流协调员将确认负荷装运。 如果收货公司在使用**运输管理**模块，确认入站装运将触发与入站负荷关联的其他负荷管理流程。 有关详细信息，请参阅[确认装运的负荷](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/confirm-a-load-for-shipping)。

1. **负荷到达仓库，工作人员登记数量。**

    整车到达仓库收货台时，仓库工作人员将登记负荷数量。 如果使用**仓库管理**模块，工作人员可以使用移动设备进行登记。 有关详细信息，请参阅[针对采购订单的物料收货 - 登记](../procurement/product-receipt-against-purchase-orders.md#registration)和[为入站负荷登记到达的物料数量](#register-item-quantities-arriving)部分。

1. **将针对采购订单过帐登记的负荷数量。**

    将负荷数量登记为已到达之后，必须将这些数量的收货过帐到公司的库存分类帐，以便记录物理库存增长。 有关详细信息，请参阅[针对采购订单的物料收货 - 物料收货](../procurement/product-receipt-against-purchase-orders.md#product-receipt)和[针对采购订单过帐登记的物料数量](#post-registered-quantities)。

## <a name="register-item-quantities-that-arrive-on-an-inbound-load"></a><a name="register-item-quantities-arriving"></a>为入站负荷登记到达的物料数量

Microsoft Dynamics 365 Supply Chain Management 支持使用多种操作方法记录所订购物料的到达。 因此，您可以配置系统以匹配您的特定业务需求。 此部分介绍当在系统中开启了高级仓库管理的情况下如何使用移动设备登记传入物料的数量。 但是，还有一种备用流以使用物料到达日记帐为基础，而不是使用移动设备。 有关这种流的详细信息，请参阅[使用物料到达日记帐登记启用了高级仓库的物料](tasks/register-items-advanced-warehousing.md)。

当入站负荷首先到达仓库时，仓库工作人员必须登记装运中包含的物料数量。 他们通常使用手持扫描仪。 仅当系统中有以下项目时，才能执行此工作流：

- **用于描述装运中应该包含的物料数量的入站负荷记录**

    供应商通常会装运到达仓库之前确认入站负荷记录。 因此，负荷的状态为_已装运_。 但是，仓库工作人员也可以登记状态为_未结_或_已收到_的负荷的物料数量。

- **配置为支持负荷接收的移动设备菜单**

    适用于移动设备的 [Dynamics 365 for Finance and Operations – Warehousing 应用](install-configure-warehousing-app.md) 支持以下工作创建流程：

    - 加载物料接收
    - 加载物料接收和储存
    - 混合牌照接收，其中移动设备菜单项的**原始凭证行标识方法**字段设置为_负荷物料收货_。 有关详细信息，请参阅[混合牌照接收](mixed-license-plate-receiving.md)。
    - 混合牌照接收加入库处理，其中移动设备菜单项的**原始凭证行标识方法**字段设置为_负荷物料收货_。 有关详细信息，请参阅[混合牌照接收](mixed-license-plate-receiving.md)。

    > [!NOTE]
    > 无论执行哪种流程，系统都会生成工作以接收收货位置登记的数量，然后将其存储到常规存储位置中。 如果使用_负荷物料收货加入库处理_或_混合牌照接收和入库处理_流程，设备还将指示负荷数量的登记工作人员在登记工作中执行入库处理工作。 相对而言，对于_负荷物料收货_和_混合牌照接收_流程，则假设入库处理工作与登记任务分开。

- **用于定义传入负荷的领料和放置工作的工作模板**

    此项与前面的项有关。 _采购订单_工作订单类型必须至少有一个工作模板，并且其中必须包含一组领料/放置工作类型。

移动设备将指导仓库验收员完成负荷数量登记流程。 此流程中至少包含针对各负荷 ID 的以下步骤：

1. 输入负荷 ID。
2. 输入接收的物料的物料编号。
3. 输入收到该物料编号的数量。
4. 如果未将系统设置为自动生成物料初始位置的牌照编号，输入该编号。
5. 轻击**确定**。

工作人员完成这些步骤之后，系统将对相应实体进行以下更新，前提是采购订单行数量到达一个负荷且已经登记了所有数量：

| 实体 | 更新 | 票据 |
|---|---|---|
| 装入 | 将把负荷行中的**创建的工作数量**字段更新为显示登记的数量。 | 如果尚未为负荷运行装运确认，**负荷状态**值仍将为_已装运_或_未结_。 如果已经开始了至少一行入库处理工作，则将更改为_进行中_。 |
| 已登记了其关联的负荷数量的采购订单的库存交易记录 |<p>将更新以下字段：</p><ul><li><b>收货</b>字段将设置为<i>已登记</i>。</li><li>将使用收货台位置代码更新<b>位置</b>字段。 （此字段是在各仓库的<b>默认收货位置</b>字段中指定的。）</li><li>将使用登记期间输入或生成的牌照编号更新<b>牌照</b>字段。</li><li>将使用登记了其数量的负荷的编号更新<b>负荷 ID</b> 字段。 （请参见注释。）</li></ul> | 版本 10.0.9 中引入了采购订单库存交易记录与针对负荷登记的数量之间的链接，这是可选功能，名称为_将采购订单库存交易记录与负荷相关联_。 此功能特别适合以下操作流程：所订购货物的一个订单分为多个负荷交付，或一个负荷中包含多个采购订单的数量。 |
| 仓库入库处理 | 工作将基于工作模板创建，以指示工作人员将登记的数量从收货位置移到常规存储位置。 | 放置位置指令控制对存储位置的选择。 如果未定义位置指令，则工作的入库处理位置为空。 |

请注意，仓库工作人员无需使用_负荷物料收货_流程即可使用一个或多个关联负荷注册采购订单的收货。 提供以下方法：

- **在移动设备中：** 使用_采购订单行接收_和_采购订单行接收加入库处理_流程。 （如果采购订单行数量有多个负荷，则工作人员不能使用_采购订单行接收_流程。 而是会指示工作人员使用与_负荷物料收货_流程关联的设备操作。）
- **在客户端上：** 使用物料到达日记帐。
- **在客户端上：** 使用可从采购订单行访问的**登记**操作。

> [!NOTE]
> 如果使用前面的任何方法登记采购订单收货，则不在采购订单库存交易记录与负荷之间创建链接，即使开启了_将采购订单库存交易记录与负荷相关联_功能。 此规则的一项例外是在使用**采购订单行接收**选项时，并且只有一个负荷的订单行的状态可以不是_已接收_。

### <a name="handle-discrepancies-during-registration-of-inbound-load-quantities"></a>处理登记入站负荷数量期间出现的差异

仓库工作人员可以执行部分负荷数量接收登记。 然后，每个部分负荷数量接收都将创建一个单独的库存交易记录，该交易记录的收货登记数量状态为_已登记_，并且批次 ID 引用原始采购订单行。

#### <a name="load-under-receiving"></a>负荷收货不足under-receiving

当负荷到达时，如果物料数量比负荷记录中记载的数量少，仓库收货人员可以直接在客户端中工作，以通过减少负荷行中的数量来确认此差异，以使其与到达并登记的实际数量匹配。

#### <a name="load-over-receiving"></a><a name="load-over-receiving"></a>负荷超收

当负荷到达且物料数量超过预期负荷行数量时，发生超收。 可以控制负荷登记期间是否允许超收，允许超收达到哪种程度。

可使用相关移动设备菜单项的**负荷超收**字段控制仓库工作人员尝试登记超交时的结果。 此字段可用于使用以下类型的工作创建流程的移动设备菜单项：

- 加载物料接收
- 加载物料接收和储存
- 混合牌照接收（当**原始凭证行标识方法**字段设置为_负荷物料收货_时）
- 混合牌照接收加入库处理（当**原始凭证行标识方法**字段设置为_负荷物料收货_时）

下表介绍**负荷超收**字段的可用选项。

| 值 | 说明 |
|---|---|
| 允许 | 工作人员可以登记超过所选负荷剩余未登记数量的数量的接收，但是仅当登记数量总数未超过与负荷关联的采购订单行数量时（在调整超交百分比之后）才可用。 |
| 锁定 | <p>工作人员不能登记超过所选负荷剩余未登记数量的数量的接收（在调整超交百分比之后）。 尝试登记收货的工作人员将遇到错误，并且不能继续操作，直到登记等于或小于剩余未登记负荷数量的数量时。</p><p>默认情况下，将从关联的采购订单行复制负荷行中的超交百分比值。 当<b>负荷超收</b>字段设置为<i>阻止</i>时，系统使用超交百分比值计算可以为负荷行登记的总数量。 但是，可以根据需要为各负荷覆盖该值。 当接收流程期间表示订单行超交百分比的部分或所有多余数量在多个负荷中按比例分布时，与此行为有关。 下面是一个示例方案：</p><ul><li>一个采购订单行有多个负荷。</li><li>该采购订单行的超交百分比大于 0（零）。</li><li>已经在未纳入超交百分比的情况下登记了一个或多个负荷的数量。</li><li>最后一个负荷的超交数量。</li></ul><p>在此情况下，仅当仓库主管将相关负荷行的超交百分比从默认值提高到足够在最后一个负荷中登记整个超交的值时，才可使用移动设备登记最后一个负荷的多余数量。</p> |
| 仅对已结算负荷阻止 | 工作人员可以超收未结负荷的负荷行数量，但是不能超收状态为_已接收_的负荷的负荷行数量。 |

> [!NOTE]
> **负荷超收**的默认值为_允许_。 如果使用此值，行为将与在版本 10.0.11 中引入_负荷数量超收_功能之前提供的标准行为相符。

### <a name="put-away-the-registered-quantities"></a>入库处理登记的数量

在移动设备中完成了登记后，_数量接收登记_操作将更新库存和仓库记录，以指示数量现在位于收货台位置，可预留。 但是，公司的仓库操作通常会要求将数量从收货台移到常规仓库存储，以便进行后续的领料流程。 入库处理说明在将入站负荷登记为已接收时自动生成的入库处理工作中捕获。

当仓库工作人员完成了入库处理工作时，系统将通过更新多个实体（如下表中的汇总）来记录和跟踪结果。

| 实体 | 更新 | 票据 |
|---|---|---|
| 装入 | <p>将更新以下字段：</p><ul><li><b>负荷状态</b>值更改为<i>进行中</i>。</li><li><b>工作状态</b>值更改为<i>工作完成 100.00%</i>。</li></ul> | 当工作人员开始为至少一个入库处理工作行执行入库处理任务时，**负荷状态**值将更改为_进行中_。 |
| 已经对其的关联数量进行了入库处理的工作的库存交易记录 | 将更新**接收**和**位置**字段，以体现从接收位置到存储位置的移动。 | 采购订单库存交易记录的**收货状态**值保持为_已登记_。 |
| 仓库入库处理 | **工作状态**值将更改为_已结束_。 | |

## <a name="post-registered-product-quantities-against-purchase-orders"></a><a name="post-registered-quantities"></a>针对采购订单过帐登记的物料数量

入站物料数量在系统中登记之后，可以在销售和其他出站和内部操作中预留。 但是，系统尚未更新库存（临时）帐户。 仅当运营团队过帐登记的物料收货时，才进行此更新。

若要打开可过帐物料收货的页面，运营团队成员可以执行下面的任何_一个_步骤：

- 打开相关负荷记录，然后选择**物料收货**操作。
- 转到**仓库管理 \> 定期任务 \> 更新物料收货**，然后在**负荷 ID** 字段中指定要过帐的负荷。
- 打开相关采购订单，然后选择**物料收货**操作。
- 转到**采购 \> 采购订单 \> 接收产品 \> 过帐产品收货作业**。

**负荷**页（和更新作业的等效页，即**更新物料收货**页）中的可用**物料收货**操作只能更新状态为_已登记_的采购订单数量的物料收货数量。 但是，**采购订单**页中的可用**物料收货**操作中可以包含两种处理状态（_已订购_和_已登记_）的数量。 还可以通过更多参数（如_当前接收量_和_登记数量和服务_）控制物料收货过帐范围。

只能对状态为_已确认_的订单的物料收货进行过帐。 对于未确认采购订单，**物料收货**操作将显示为不可用。

### <a name="post-registered-quantities-from-the-load-page"></a>从“负荷”页过帐登记数量

若要从**负荷**页对登记数量进行物料收货过帐，必须满足以下先决条件：

- 负荷必须有至少一个状态为_已登记_的数量单元。
- 负荷状态必须为_已装运_。
- 与负荷关联的采购订单的状态必须为_已确认_。

> [!NOTE]
> 如果负荷状态尚未设置为_已装运_，系统将在运行物料收货更新之前自动确认该负荷。 （当用户登记负荷的入站装运时，将把负荷状态设置为_已装运_。）

若要对与所选负荷关联的到达登记进行产品收货过帐，工作人员需要在**负荷**页中选择**物料收货**操作。 打开的页面中有以下关键详细信息：

- **设置**选项卡上**参数**部分中的**数量**字段显示_登记数量_。 此处无其他选项。
- **概览**快速选项卡上的网格列出所选负荷中包含的所有采购订单。
- **行**快速选项卡上的网格列出具有登记数量的所有订单行。

> [!NOTE]
> **行**选项卡上显示的订单行的数量计算方法不同，具体取决于您的 Supply Chain Management 版本中是否有且开启了_允许一个负荷多次物料收货_功能。
>
> | 版本 | 计算 |
> |---|---|
> | 低于 10.0.10 的版本和未开启_允许一个负荷多次物料收货_功能的较高版本 | 行数量是_该采购订单行_的所有登记数量的总和，无论登记是否是对多个负荷，独立于负荷，从移动设备还是客户端进行的均不受影响。 |
> | 其中开启了_允许一个负荷多次物料收货_功能的版本 10.0.10 及更高版本 | 行数量是开始执行**物料收货过帐**操作的_负荷记录_的所有登记数量之和。 |

当用户选择**确定**以确认物料收货过帐时，系统将对相应实体执行以下关键更新。

| 实体 | 更新 |
|---|---|
| 过帐范围中包含其行数量的采购订单行的库存交易记录 | <p>将更新以下字段（但是请注意，还会进行其他多项更新）：</p><ul><li><b>收货</b>字段将设置为<i>已接收</i>。</li><li>将使用过帐日期更新<b>实际日期</b>字段。</li></ul> |
| 用户过帐的产品收货的来源负荷 | 对负荷的更新取决于所用版本和**允许一个负荷多次物料收货**字段的设置。 本部分后文中的表介绍这些规则。 |

**允许一个负荷多次物料收货**字段可供公司选择入站负荷收货策略。 公司可以根据操作流程选择允许还是不允许对同一个负荷进行多次物料收货过帐。 建议物流经理将**允许一个负荷多次物料收货**字段设置为以下值之一：

- **否** – 如果仓库验收员始终为指定的时间范围内的每个负荷登记到达的所有订单数量，请选择此值。 如果不登记任何负荷数量，系统将假设这些负荷数量未到达或不在负荷中，因此不应视为负荷的一部分。 从负荷运行的物料收货过帐采用同样的假设。 除了对所有登记数量进行物料收货更新（其主功能），还会声明负荷完整并结束，以进行进一步的处理。 在此情况下，将把所有负荷行数量自动更新为登记数量，删除无登记数量的负荷行，并将负荷状态更改为_已接收_。
- **是** – 如果仓库验收员需要更多时间来为负荷登记到达的所有数量，但是同时，必须对已登记的数量进行物料收货过帐，请选择此值。 在此情况下，物流经理需要让负荷保持未结状态，即使在运行物料收货过帐作业后也不例外，以便登记剩余负荷数量和根据现状对日记帐进行物料收货更新。
- **提示** – 如果采用混合负荷收货，并且每次运行物料收货过帐时都需要做出决定，请选择此值。

下表总结了**允许一个负荷多次物料收货**设置的结果。

| 允许一个负荷多次物料收货 | 负荷数量 | 负荷状态 | 票据 |
|---|---|---|---|
| 当此字段不可用时（10.0.10 之前版本） | <p>设置负荷数量，使其等于登记数量。</p><p>如果将负荷数量更新为 0（零）（这意味着未进行任何登记），将删除负荷行。</p><p>如果负荷中无负荷行，将删除负荷。</p> | _已收到_ | 如果订单行的登记数量有多个负荷，则仅把收货的过帐来源负荷的状态更新为_已接收_。 |
| 无 | <p>将设置负荷数量，使其等于与负荷 ID 关联的登记数量。</p><p>如果没有为库存交易记录记录任何负荷 ID，则行为与 10.0.10 之前版本中的行为相符。</p> | _已收到_ | |
| 是 | 无更新 | _已接收_如果登记的负荷数量总数等于或大于负荷数量 | |
| 是 | 无更新 | _已装运_或_进行中_，如果登记的负荷数量总数小于负荷数量 | |

**负荷状态**字段设置为_已接收_之后，不能再对该负荷进行物料收货过帐。 但是，在以下情况下，工作人员可以对收到的负荷登记剩余订单数量。 （有关详细信息，请参阅本主题前文的[负荷超收](#load-over-receiving)部分。）

- Supply Chain Management 版本低于版本 10.0.11。
- 已开启_负荷数量超收_功能，并且负荷物料收货操作的移动设备菜单项中的**订单行数量超收**字段设置为_允许_。

若要针对状态为_已接收_的负荷的更多登记负荷数量执行物料收货过帐，用户必须从关联的采购订单运行过帐操作。

### <a name="post-registered-quantities-from-the-purchase-order-page"></a>从“采购订单”页过帐登记数量

若要从**采购订单**页对登记数量进行物料收货过帐，用户需要在选择**物料收货**操作前完成以下任务：

- 将**设置**选项卡上**参数**部分中的**数量**字段设置为_登记数量_。
- 在**物料收货**字段中，设置过帐中包含的采购订单数量。

> [!NOTE]
> 过帐范围中将包含的行数量是该订单行的所有登记数量的总和，无论数量登记是否是对多个负荷，独立于负荷，从移动设备还是客户端进行的均不受影响。 从负荷运行物料收货过帐，并且**允许一个负荷多次物料收货**字段不可用或未启用，则应用同样的规则。

当用户选择**确定**以确认物料收货过帐时，系统将对相应实体执行以下关键更新。

| 实体 | 更新 |
|---|---|
| 过帐范围中包含其行数量的采购订单行的库存交易记录 | <p>将更新以下字段（但是请注意，还会进行其他多项更新）：</p><ul><li><b>收货</b>字段将设置为<i>已接收</i>。</li><li>将使用物料收货过帐操作更新<b>实际日期</b>字段。</li></ul> |
| 装入 | 对负荷的更新取决于**允许一个负荷多次物料收货**字段是否可用并启用。 下一个表中描述这些规则。 |

下表总结了**允许一个负荷多次物料收货**设置的结果。

| 允许对每批负荷进行多次物料收货 | 负荷数量 | 负荷状态 | 票据 |
|---|---|---|---|
| 当此字段已禁用或不可用时（在 10.0.10 之前版本中） | 无更新 | 未进行更新。 （状态保持为_未结_、_已装运_或_进行中_。） | 因为物料收货过帐是从采购订单开始的，所以更新逻辑中不包含有关其范围内的登记数量与记录的登记针对的负荷之间的关联的信息。 因此，不能为状态更新选择负荷。 |
| 已启用 | 无更新 | <p>将进行以下操作之一：</p><ul><li>如果采购订单库存交易记录的收货数量和采购数量总和超过或等于关联的负荷数量，则状态将更改为<i>已接收</i>。</li><li>如果负荷中的所有行均满足前面的条件，则状态保持为<i>未结</i>、<i>已装运</i>或<i>进行中</i>。</li></ul> | |

### <a name="select-the-appropriate-product-receipt-posting-option-for-your-logistics-operations"></a>为物料操作选择相应的产品收货过帐选项

前面说明，系统提供两个物料收货过帐选项。 可以在以下位置访问这些选项：

- 在**负荷**页，或以更新作业的形式从**仓库管理 \> 定期任务**菜单
- 在**采购订单**页，或作为更新作业从**采购 \> 采购订单 \> 接收物料**菜单

建议使用负荷规划和管理对其入站订单的运输和仓库处理的公司使用以下功能（这些功能专用于处理负荷）：

- 仓库移动设备上的**负荷物料接收**操作，用于针对负荷登记产品数量到达
- 从负荷启动的**物料收货过帐**操作，用于更新库存分类帐

> [!NOTE]
> 可使用其他数量登记和物料收货过帐功能支持相应入站操作流程。 但是，如果互换使用它们，而不是使用专注负荷的专用功能，则可能会破坏负荷记录的数据精确性，从而破坏负荷管理流程的无缝性。

## <a name="example-scenarios"></a>示例方案

### <a name="prepare-your-system-to-run-the-sample-scenarios"></a>准备系统以运行示例方案

若要演练本部分中介绍的示例方案，必须先确保在系统中开启所有必需功能。 系统中还必须有必需的演示数据。

#### <a name="turn-on-the-required-features"></a>开启必需功能

这些方案需要_一个负荷多次物料收货过帐_功能及其先决功能。 管理员可以按照以下步骤开启这些功能。

1. 打开**功能管理**工作区。 （有关如何找到并使用此工作区的完整详细信息，请参阅[功能管理概述](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)。）

1. 按照下面的方法开启列出的_将采购订单库存交易记录与负荷相关联_功能：

    - **模块：**_仓库管理_
    - **功能名称：**_将采购订单库存交易记录与负荷相关联_

1. 按照下面的方法开启列出的_一个负荷多次物料收货过帐_功能：

    - **模块：**_仓库管理_
    - **功能名称：**_一个负荷多次物料收货过帐_

#### <a name="enable-sample-data"></a>启用示例数据

若要使用指定的示例记录和值演练这些方案，使用的系统中必须已安装标准演示数据。 开始前，还必须选择 **USMF** 法人。

#### <a name="add-a-menu-item-for-receiving-load-items-when-a-mobile-device-is-used"></a>添加一个菜单项，用于在使用移动设备时接收负荷物料

仓库验收员使用移动设备登记链接到负荷的入站库存之前，必须先为该目的创建一个移动设备菜单项。

此部分中，将创建一个移动设备菜单项并将其添加到现有菜单中。 然后，仓库工作人员可以在 Warehousing 应用中选择该菜单项。

1. 转到**仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单项**，并确保您的移动设备菜单中包含具有以下设置的菜单项：

    - **模式：**_工作_
    - **工作创建流程：**_负荷物料接收_
    - **生成牌照：**_是_

    可以让其他所有设置保留其默认值。

    ![移动设备菜单项设置](media/inbound-mobile-menu-items.png "移动设备菜单项设置")

    有关如何设置移动设备菜单项的详细信息，请参阅[为仓库工作设置移动设备](configure-mobile-devices-warehouse.md)。

2. 设置完菜单项之后，转到**仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单项**，然后将其添加到您的移动设备的菜单结构中。

### <a name="example-scenario-1-register-a-load-where-some-items-are-missing"></a>示例方案 1：登记缺少某些物料的负荷

此方案显示如何为并非所有预期数量均存在的入站负荷登记数量。 然后显示如何过帐采购订单的物料收货。

#### <a name="create-a-load-to-plan-receipt-of-a-purchase-order"></a>创建负荷以计划采购订单的收货

在此过程中，将手动创建采购订单和关联的负荷。 然后更新该负荷以模拟其已从供应商装运（这将更新负荷状态）。 然后，仓库规划员可按**负荷状态**筛选负荷以找到所需传入负荷。

1. 转到**采购 \> 采购订单 \> 所有采购订单**。
1. 选择**新建**。
1. 在**创建采购订单**对话框中，将**供应商帐户**字段设置为 _1001_。
1. 选择**确定**关闭对话框并创建采购订单。
1. 新采购订单中**采购订单行**下已经有一行。 设置此行的以下值：

    - **物料编号：**_A0001_
    - **仓库：**_24_
    - **数量：**_10_

1. 在操作窗格上的**采购**选项卡上，选择**操作 \> 确认**。 订单状态现在为_已确认_。
1. 在操作窗格上的**仓库**选项卡上，选择**操作 \> 负荷计划工作台**。
1. 在**负荷计划工作台**页操作窗格的**供应与需求**选项卡上，选择**添加 \> 至新负荷**。
1. 在**负荷模板分配**对话框中，将**负荷模板 ID** 字段设置为 _20' 容器_。
1. 选择**确定**关闭对话框并返回到工作台。
1. 在**负荷**部分中，选择**负荷 ID** 打开新创建的负荷。
1. 查看负荷标题和行详细信息，并注意下面的点：

    - 在**负荷**快速选项卡上，**负荷状态**字段设置为_未结_。
    - 在**负荷行**部分中，有一行中的**数量**字段设置为 _10_，**创建的工作数量**字段设置为 _0_（零）。

    ![负荷明细](media/inbound-load-details.png "负荷明细")

1. 在操作窗格上**装运和接收**选项卡上，选择**确认 \> 入站装运**。 请注意，**负荷状态**已更改为_已装运_。
1. 记下**负荷 ID** 值，以便在下一个过程中使用。

#### <a name="register-receipt-of-the-quantities-that-arrived-on-the-load"></a>在负荷中登记到达的数量收货

当负荷到达仓库收货台时，验收员将在移动设备中登记负荷数量。

1. 使用移动设备登录到仓库 24。 （在标准演示数据中，使用 _24_ 作为用户 ID 和 _1_ 作为密码登录。）
1. 选择为此方案创建的_负荷物料接收_菜单项。
1. 按照屏幕上的数据输入说明输入以下值。 （顺序可能会有所不同，具体取决于您使用的移动设备或仿真器。）

    - **负荷** – 输入您在上一个过程中创建的负荷 ID。
    - **物料** – 输入 _A0001_，这是此负荷所需物料。
    - **数量** – 输入 _9_ 作为负荷中的实际数量。 请注意，此数量小于预期数量。

1. 继续工作流，并将其他所有字段保留为空或保留其默认值，直到设备通知您已完成工作。

负荷收货任务现在已完成，验收员可以继续自己的下一项任务。 但是，仓库收货人员最终将检查负荷记录，并且可以发现收货数量小于预期数量。 然后，他们将使用 Web 客户端完成以下过程。

1. 转到**仓库管理 \> 负荷 \> 所有负荷**。
1. 在列表中，找到刚收货的负荷。 （可能必须选中**显示已结**复选框以包括负荷状态为_已装运_的入站负荷。）然后选择**负荷 ID** 列中的链接打开该负荷。
1. 请注意，负荷记录中的**负荷状态**值保留为_已装运_，但是负载行中的**创建的工作数量**值已变为 _9_。
1. 转到**采购 \> 采购订单 \> 所有采购订单**。
1. 在列表中，找到刚才收到的订购，然后选择**采购订单**列中的链接打开订单。
\
1. 在**采购订单行**快速选项卡上，选择**库存 \> 查看 \> 交易记录**。
1. 查看这两个采购订单交易记录的详细信息。 （可能必须个性化**库存交易记录**页以查看网格的**负荷 ID** 字段。）应该会看到两个交易记录：

    - 其中一项收货的状态为_已登记_的交易记录提供使用移动设备对特定负载运行的登记数量 _9_。 **负荷 ID** 与有问题的交易记录关联。
    - 其中一项收货的状态为_已订购_的交易记录提供剩余未登记订单行数量 _1_。

#### <a name="product-receiptpost-the-registered-load-quantities-against-purchase-orders"></a>针对采购订单对登记的负荷数量进行物料收货过帐

在此过程中，将对为负荷登记的库存进行物料收货过帐。 因此将把收到的库存及其相关成本添加到公司的总帐。

1. 转到**仓库管理 \> 负荷 \> 所有负荷**。
1. 在列表中，找到收货的负荷。 （可能必须选中**显示已结**复选框以包括负荷状态为_已装运_的入站负荷。）然后选择**负荷 ID** 列中的链接打开该负荷。
1. 在操作窗格上**装运和接收**选项卡上，选择**收货 \> 物料收货**。 如果提示确认操作，请选择**是**。
1. 在**过帐物料收货**对话框中**行**快速选项卡上，检查网格。 应该会看到针对所选负荷登记了其数量的采购订单行。

    > [!NOTE]
    > 在_一个负荷多次物料收货过帐_功能不可用或未启用的版本中，**负荷行**网格中显示的默认数量将为对与采购订单行关联的所有负荷登记的总数量。

1. 在**概览**快速选项卡上，检查网格中的**物料收货**字段。 请注意，应该将其设置为包含所选负荷的 ID 的编号。
1. 选择**确定**过帐物料收货，然后关闭**过帐物料收货**对话框。
1. 您将返回到负荷详细信息。 请注意以下点：

    - **负荷状态**字段设置为_已接收_。
    - 在负荷行中，负荷的**数量**值已从 _10_ 更改为 _9_ 件，以便匹配登记数量，但是**创建的工作数量**值仍然为 _9_。

如果采购团队预计供应商要交付的剩余订单数量不是 1，则可通过将行的剩余交货量更新为 _0_ 来结束订单。 但是，如果很快发现缺少的物品到达了原始负荷，仓库人员可以执行下面的一个操作：

- 针对同一个负荷登记数量。 在此情况下，**负荷状态**字段将重置为_已装运_，而**创建的工作数量**值将更新为 _10_。 只有以下情况下此选择才可用：

    - _负荷数量超收_功能不可用或未启用。
    - _负荷数量超收_功能可用且已启用，并且**负荷行数量超收**字段设置为_允许_。

- 将该数量添加到新负荷或现有负荷，然后正常处理。
- 以不涉及负荷处理的方式登记和/或接收数量。

### <a name="example-scenario-2-register-quantities-that-arrive-on-multiple-inbound-loads-where-some-items-are-missing"></a>示例方案 2：到达缺少某些物料的多个入站负荷的数量

在此方案中，将把与一个采购订单行关联的入站装运拆分为两个负荷。 例如，可以因为重量和/或体积的物理负荷限制将一个采购订单行拆分为多个负荷。

此方案还显示如何处理同一个负荷的多个物料收货过帐。 您将登记到达多个入站负荷的数量，但是该数量与预期数量不匹配。 将对同一个负荷多次通过物料收货过帐更新成本。

#### <a name="set-up-load-receiving-policies"></a>设置负荷收货策略

在此过程中，将启用来自同一个负荷的多个物料收货过帐。

1. 转到**仓库管理 \> 设置 \> 仓库管理参数**。
1. 在**负荷**选项卡上，将**允许一个负荷多次物料收货**字段设置为_是_。

#### <a name="create-two-loads-to-plan-receipt-of-a-purchase-order"></a>创建两个负荷以计划采购订单的收货

在此过程中，将创建一个采购订单和两个负荷。 然后手动更新每个负荷以模拟其为供应商装运（这将更新负荷状态）。 然后，仓库规划员可按**负荷状态**筛选负荷以找到所需传入负荷。

您还将了解如何设置采购订单行，以便接收比为行指定的数量多 20% 的数量。

1. 转到**采购 \> 采购订单 \> 所有采购订单**。
1. 选择**新建**。
1. 在**供应商**快速选项卡上，将**供应商帐户**字段设置为 _1001_，然后选择**确定**。
1. 您的新采购订单将打开，并且在**采购订单行**网格中将有一个空行。 设置此订单行的以下值：

    - **物料编号：**_A0001_
    - **仓库：**_24_
    - **数量：**_10_

1. 在**行详细信息**快速选项卡上的**交货**选项卡中，将**超交**字段设置为 _20_。
1. 在操作窗格上的**采购**选项卡上，选择**操作 \> 确认**。 订单状态现在为_已确认_。
1. 在操作窗格上的**仓库**选项卡上，选择**操作 \> 负荷计划工作台**。
1. 在**负荷计划工作台**页操作窗格的**供应与需求**选项卡上，选择**添加 \> 至新负荷**。
1. 在**负荷模板分配**对话框中，将**负荷模板 ID** 字段设置为 _20' 容器_。 在**详细信息**选项卡上，将**数量**值从 _10_ 更改为 _5_，以部分添加采购订单行数量。
1. 选择**确定**应用设置并关闭对话框。
1. 重复步骤 8 到 10，以创建第二个负荷。 此时，**数量**字段已经设置为 _5_。
1. 在**负荷计划工作台**页面的**负荷**网格中，选择创建的第一个负荷的**负荷 ID** 值。 将显示**负荷详细信息**页，其中显示所选负荷。 遵循以下步骤:

    1. 在操作窗格上**装运和接收**选项卡上，选择**确认 \> 入站装运**。
    1. 请注意，**负荷状态**值已更改为_已装运_。
    1. 选择关闭按钮返回**负荷计划工作台**页。

1. 对您创建的第二个负荷重复上一步。
1. 记下**负荷**网格中显示的两个**负荷 ID** 值。

#### <a name="register-partial-receipt-of-the-quantities-that-arrived-on-the-first-load-and-post-the-registered-load-quantities"></a>等级到达第一个负荷的数量的部分收货并过帐登记的负荷数量

当负荷到达仓库收货台时，验收员将在移动设备中登记负荷数量。 然后通过基于负荷过帐采购订单物料收货，在公司的总帐中更新链接到该负荷的已登记库存的成本。

此过程显示验收员如何在移动设备中登记负荷数量。

1. 使用移动设备登录到仓库 24。 （在标准演示数据中，使用 _24_ 作为用户 ID 和 _1_ 作为密码登录。）
1. 选择为此方案创建的_负荷物料接收_菜单项。
1. 按照屏幕上的数据输入说明输入以下值。 （顺序可能会有所不同，具体取决于您使用的移动设备或仿真器。）

    - **负荷** – 输入您在上一个过程中创建的第一个负荷 ID。
    - **物料** – 输入 _A0001_，这是此负荷所需物料。
    - **数量** – 输入 _3_。 请注意，此数量小于预期数量。 对于此方案，假设您作为验收员没有时间登记此负荷的所有数量。 在此过程的后面，您将通过重复此步骤并将**数量**字段设置为 _2_ 来登记剩余物料。

1. 继续工作流，并将其他所有字段保留为空或保留其默认值，直到设备通知您已完成工作。
1. 在 Web 客户端中，转到**仓库管理 \> 负荷 \> 所有负荷**。
1. 在列表中，找到刚收到的负荷，然后选择**负荷 ID** 值打开负荷。 请注意，负荷记录中的**负荷状态**值保留为_已装运_，但是负载行中的**创建的工作数量**值已变为 _3_。
1. 在操作窗格上**装运和接收**选项卡上，选择**收货 \> 物料收货**。 如果提示确认操作，请选择**是**。
1. 在**过帐物料收货**对话框中，查看当不更改显示的值，然后选择**确定**。
1. 将回到所选负荷的**负荷详细信息**页。 请注意以下点：

    - **负荷状态**字段仍然设置为_已装运_。
    - 在负荷行中，负荷的**数量**值仍然为 _5_ 件，这是原始负荷数量，而**创建的工作数量**值仍然为 _3_。

1. 重复此过程完成此负荷剩余数量的登记。 但是在步骤 3 中，将**数量**字段设置为 _2_。

现在已完成了第一个负荷的收货任务。 已经创建了两个物料收货日记帐，您运行的两个物料收货更新分别一个。

#### <a name="register-receipt-of-the-quantities-that-arrived-on-the-second-load-and-account-for-the-overdelivered-quantity"></a>登记到达第二个负荷的数量的收货并纳入超交数量

对于此方案，验收员将对超过负荷的现有数量的数量进行入站登记。 将允许超收，因为系统设置为允许超交。

1. 使用移动设备登录到仓库 24。 （在标准演示数据中，使用 _24_ 作为用户 ID 和 _1_ 作为密码登录。）
1. 选择为此方案创建的_负荷物料接收_菜单项。
1. 按照屏幕上的数据输入说明输入以下值。 （顺序可能会有所不同，具体取决于您使用的移动设备或仿真器。）

    - **负荷** – 输入您前面创建的第二个负荷 ID。
    - **物料** – 输入 _A0001_，这是此负荷所需物料。
    - **数量** – 输入 _7_，这是总计 12（其中 10 为原始订单数量，2 为允许的 20% 超交数量）的采购订单数量中授权供应商交付的剩余数量。 请注意，已经对第一个负荷登记了 5 件。

现在已经使用数量 7 更新了第二个负荷，并且可以根据此数量对其进行物料收货更新。
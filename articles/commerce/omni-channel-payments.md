---
title: 全渠道付款概述
description: 本文提供有关 Dynamics 365 Commerce 中的全渠道付款的概述。
author: BrianShook
ms.date: 11/04/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom:
- "141393"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 8.1.3
ms.openlocfilehash: a5cc0725b383ca6657bd19b9dd25b0c60b364467
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746117"
---
# <a name="omni-channel-payments-overview"></a>全渠道付款概述

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

本文提供有关 Dynamics 365 Commerce 中的全渠道付款的概述。 其中包括丰富的受支持方案列表、有关功能的信息、设置、疑难解答和某些典型问题的说明。

## <a name="key-terms"></a>重要术语

| 术语 | 说明 |
|---|---|
| 标志 | 支付处理程序作为引用提供的数据字符串。 标志可以提供付款卡号、付款授权和以前的付款捕获。 标志非常重要，因为可以将敏感数据保存在销售点 (POS) 系统外部。 它们有时也称为 *引用*。 |
| 卡标志 | 付款处理程序提供来存储到 POS 系统中的标志。 只有卡标志的接收商家才能使用卡标志。 卡标志有时也称为 *卡引用*。 |
| 授权标志 | POS 系统创建了授权请求之后付款流程作为发送给 POS 的响应的一部分提供的唯一 ID。 如果调用了处理程序以执行撤销或废除授权之类操作，则可在以后使用授权标志。 但是，最常用于在履行订单或完成交易记录时捕获资金。 授权标志有时也称为 *授权引用*。 |
| 捕获标志 | 完成或捕获付款时付款处理程序提供给 POS 系统的引用。 然后，可将捕获标志用于在后续操作（如退款请求）中引用付款捕获。 | 
| 无卡 | 表示不存在实体卡的付款交易记录的术语。 例如，电子商务或呼叫中心方案中可能会出现此类交易记录。 对于此类交易记录，将在电子商务网站、呼叫中心流或 POS 或付款终端中手动输入与付款有关的信息。 |
| 有卡 | 表示实体卡存在且在与 Microsoft Dynamics 365 POS 系统相连的付款终端中使用的付款交易记录的术语。 |

## <a name="overview"></a>概览

一般来说，术语 *全渠道付款* 描述在一个渠道中创建订单，然后在另一个渠道中履行的能力。 全渠道付款支持的关键是维护付款详细信息和订单的其余详细信息，然后在另一个渠道中重新调用或处理订单时使用这些付款详细信息。 “在线购买，店内提货”方案就是一个经典示例。 在此方案中，付款详细信息是当在线创建订单时添加的。 然后提货时在 POS 重新调用，以便向客户的付款卡扣款。 

本文中介绍的所有方案都可以通过使用 Commerce 随附的标准付款软件开发套件 (SDK) 实施。 [适用于 Adyen 的 Dynamics 365 Payment Connector](/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3) 提供此处介绍的每种方案的现成实施。 

### <a name="prerequisites"></a>先决条件

本文中介绍的每种方案都需要支持全渠道付款的付款连接器。 也可以使用现成的 Adyen 连接器，因为它支持通过付款 SDK 提供的方案。 有关如何实施付款连接器的详细信息，以及有关 Retail SDK 的常规信息，请访问[面向 IT 专业人员和开发人员的 Retail 主页](/dynamics365/unified-operations/retail/dev-itpro/dev-retail-home-page#payment-connectors)。

#### <a name="supported-versions"></a>支持的版本

本文中介绍的全渠道付款功能是在 Microsoft Dynamics 365 for Retail 版本 8.1.3 中发布的。 

#### <a name="card-present-and-card-not-present-connectors"></a>“有卡”和“无卡”连接器

付款 SDK 依赖两组应用程序编程接口 (API) 进行付款。 第一组 API 称为 **iPaymentProcessor**。 用于实施可在呼叫中心中使用的“无卡”付款连接器和带有 Microsoft Dynamics 电子商务平台的“无卡”付款连接器。 有关 **iPaymentProcessor** 接口的详细信息，请参阅[实施付款连接器和付款设备](https://download.microsoft.com/download/e/2/7/e2735c65-1e66-4b8d-8a3c-e6ef3a319137/The%20Guide%20to%20Implementing%20Payment%20Connector%20and%20Payment%20Device_update.pdf)白皮书，其中介绍了付款。 

第二组 API 称为 **iNamedRequestHandler**。 它支持实施使用付款终端的“有卡”付款集成。 有关 **iNamedRequestHandler** 接口的详细信息，请参阅[为付款终端创建付款集成](/dynamics365/unified-operations/retail/dev-itpro/end-to-end-payment-extension)。 

### <a name="setup-and-configuration"></a>设置和配置

需要以下组件和设置步骤：

- **电子商务集成：** 需要与 Commerce 集成以支持订单源于在线店面的方案。 有关 Retail 电子商务 SDK 的详细信息，请参阅[电子商务平台软件开发套件 (SDK)](/dynamics365/unified-operations/retail/dev-itpro/ecommerce-platform-sdk)。 在演示环境中，引用店面支持全渠道付款方案。 
- **在线付款配置：** 设置在线渠道必须包括已经更新为支持全渠道付款的付款连接器。 也可以使用现成的付款连接器。 有关如何针对在线商店配置 Adyen 付款连接器的信息，请参阅 [Adyen 付款连接器](/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3#e-commerce)。 除了该文章中介绍的电子商务设置步骤，还必须在 Adyen 连接器的设置中将 **允许在电子商务中保存付款信息** 参数设置为 **True**。 
- **全渠道付款配置：** 在后端，转到 **Retail 和 Commerce \> 总部设置 \> 参数 \> Commerce 共享参数**。 然后在 **全渠道付款** 选项卡中，将 **使用全渠道付款** 选项设置为 **是**。 在 Commerce 版本 10.0.12 及更高版本中，此设置位于 **功能管理** 工作区。 选择 **全渠道付款** 功能，单击 **立即启用**。 
- **付款服务：** 呼叫中心使用 **付款服务** 页中的默认付款连接器处理付款。 若要支持“呼叫中心购买，店内提货”之类方案，这个默认付款连接器必须为 Adyen 付款连接器或满足全渠道付款实施要求的付款连接器。
- **EFT 服务：** 必须在硬件配置文件的 **EFT 服务** 快速选项卡中设置通过付款终端的付款。 Adyen 连接器支持现成的全渠道付款方案。 如果其他支持 **iNamedRequestHandler** 接口的付款连接器支持全渠道付款，也可以使用这些连接器。
- **付款连接器可用性：** 重新调用订单时，与订单一起重新调用的付款支付行中包括用于创建与该订单关联的授权的付款连接器的名称。 履行该订单时，付款 SDK 将尝试使用用于创建原始授权的同一个连接器。 因此，必须可以捕获具有相同商家属性的付款连接器。 
- **卡类型：** 要让全渠道方案正常工作，每个渠道可用于全渠道的支付方式的设置必须相同。 此设置中包括付款方式 ID 和卡类型 ID。 例如，如果 **卡** 支付方式在在线商店设置中的 ID 为 **2**，则在零售商店设置中应具有同一个 ID。 同样的要求适用于卡类型 ID。 如果卡号 **12** 在在线商店中设置为 **VISA**，则应该为零售商店设置同一个 ID。 
- 带内置硬件工作站的适用于 Windows 或 Android 的 Retail Modern POS   -或-
- 带连接的共享硬件工作站的适用于 iOS 的 Modern POS 或 Cloud POS。 

### <a name="basic-principle-supporting-omni-channel-payments"></a>支持全渠道付款的基本原则

付款连接器和付款处理程序使用标志（也称为引用）来引用与卡付款有关的交互。 例如，在请求付款授权时，将提供该授权的引用。 因此，可以在以后履行期间捕获资金时引用该授权。 此授权对商家、付款连接器和处理程序是唯一的。 

如果正在商店中为在线创建的订单提货，必须重新调用和使用该订单的相同付款详细信息。 在请求捕获针对原始授权的付款期间提供原始详细信息时，付款处理程序可以处理该请求和捕获付款。 

若要正确引用在线订单，还必须提供支持相同处理程序的“无卡”付款连接器。 这样，POS 系统就可以有一个处理程序来处理“有卡”付款，但是也可以通过使用不同付款处理程序来访问其他付款处理程序以履行在其他渠道中创建的订单。 

## <a name="supported-scenarios"></a>支持的方案

支持下列全渠道付款方案：

- 在线购买，店内提货
- 呼叫中心购买，店内提货
- 商店 A 购买，商店 B 提货
- 商店 A 购买，发货给客户

    > [!NOTE]
    > 在呼叫中心进行的映射到“普通”付款功能的付款必须标记为 **预付** = **是**，以在 POS 中撤回订单时反映在到期金额中。 在 POS 中撤回订单时，不会识别“普通”类型的非预付付款。 

也支持验证这些方案。 例如，一个在线订单中可能同时包含要发货给客户的行和店内提货的行。 将通过全渠道付款支持所有订单履行选项。 

下列章节介绍每个方案的步骤，并显示如何通过使用演示数据运行方案。 

### <a name="buy-online-pick-up-in-store"></a>在线购买，店内提货

首先，请确保满足以下先决条件：

- 您有配置了 Adyen 连接器的引用店面。
- **Commerce 共享参数** 页中的 **全渠道付款** 选项设置为 **True**。 在以后的版本中，此设置将移到 **功能管理** 工作区，您可以在其中选择 **全渠道付款** 功能，然后单击 **立即启用**。 
- 为休斯顿 POS 收银机配置了 Adyen 付款连接器。
- 带内置硬件工作站的适用于 Windows 或 Android 的 Retail Modern POS   -或-
- 带连接的共享硬件工作站的适用于 iOS 的 Modern POS 或 Cloud POS。 

执行下列步骤运行方案。

1. 在引用店面中，为店内提货创建一个订单。 务必选择 **休斯顿** 商店。 
2. 执行结帐步骤，然后使用测试选项卡号付款。 可以在 [Adyen 测试卡号](https://docs.adyen.com/development-resources/test-cards/test-card-numbers/#description)页中找到测试信用卡号。
3. 在 Commerce 中，使用 **同步订单** 批处理作业和 **P-001** 配送计划在后端创建订单。
4. 在 POS 中的欢迎页，选择 **提货订单** 操作查看店内提货订单。 
5. 从在引用店面中创建的订单选择一行或多行，然后选择 **提货**。

    将从后端检索订单。 

6. 从后端检索订单行详细信息，并且检测到可用于全渠道的卡付款时，将通知您有付款方式可用。
7. 选择 **使用可用的付款方式** 通过使用在引用店面中输入的卡详细信息完成交易记录。

    将在交易记录页中加载订单行，而结欠金额为 0（零）。 

8. 选择 **付款** 选项卡查看从在线订单提取的支付方式行。 
9. 选择任何付款方式完成交易记录。 

### <a name="buy-in-call-center-pick-up-in-store"></a>呼叫中心购买，店内提货

1. 在 Commerce 中 **客户服务** 页的搜索栏中，输入 **Karen Berg**，然后选择 **搜索**。 
3. 在搜索结果中选择 **Karen Berg**。
4. Karen 加载到 **客户服务** 页中，选择 **新建销售订单**。
5. 在新的销售订单页中，选择 **抬头** 查看订单抬头。 
6. 在 **订单抬头** 页中，将站点设置为 **中心**，将仓库设置为 **休斯敦**。
7. 在 **交货** 选项卡中，将 **交货方式** 字段设置为 **60** 表示客户提货。
8. 选择 **行**，然后向订单添加一行或多行。 
9. 选择 **完成** 以进入订单完成流程。
10. 向下滚动到付款部分，选择 **添加**，然后选择付款方式类型设置为 **卡** 的行。 
11. 选择加号 (**+**) 添加卡付款。 
12. 输入在 [Adyen 测试卡号](https://docs.adyen.com/development-resources/test-cards/test-card-numbers/#description)页中找到的测试信用卡号的详细信息，然后选择 **确定**。

    > [!NOTE]
    > 如果输入的卡号的卡品牌与启动付款时选择的品牌不同，付款仍将继续。 但是，会过帐到映射到您在步骤 10 中选择的卡品牌的帐户。

12. 再次选择 **确定** 关闭 **订单完成付款** 对话框。
13. 在 **销售订单摘要** 页中，选择 **提交**。
14. 在 POS 中的欢迎页，选择 **提货订单** 操作查看店内提货订单。 
15. 从在引用店面中创建的订单选择一行或多行，然后选择 **提货**。

    将从后端检索订单。 

16. 从后端检索订单行详细信息，并且检测到可用于全渠道的卡付款时，将通知您有付款方式可用。
17. 选择 **使用可用的付款方式** 通过使用在引用店面中输入的卡详细信息完成交易记录。

    将在交易记录页中加载订单行，而结欠金额为 0（零）。

18. 选择 **付款** 选项卡查看从在线订单提取的支付方式行。 
19. 选择任何付款方式完成交易记录。 

### <a name="buy-in-store-a-pick-up-in-store-b"></a>商店 A 购买，商店 B 提货

1. 启动休斯顿商店的 POS。
2. 在 **交易记录** 页中，通过使用数字小键盘输入 **2001** 来将 Karen Berg 添加到交易记录。
3. 向交易记录添加一行或多行。
4. 选择 **订单** 以查看订单选项。
5. 选择 **全部提货**，然后在系统提示时选择 **客户订单**。
6. 在搜索栏中，输入 **西雅图**，然后选择 **西雅图** 商店提货。 
7. 选择 **确定** 接受当前日期作为提货日期。
9. 选择 **卡支付** 启动付款。
10. 为卡付款支付存款结欠金额。
11. 在付款终端完成存款付款。 
12. 支付存款后，选择使用同一张卡履行的选项，然后等待订单完成。 如果支付了 100% 的保证金（在上面的步骤 10 中），会立即从卡捕获资金，在开票时不会提供授权令牌，因为资金已捕获，跟踪状态为已支付。
13. 启动西雅图商店的 POS。
14. 在 POS 中的欢迎页，选择 **提货订单** 操作查看店内提货订单。 
15. 从在引用店面中创建的订单选择一行或多行，然后选择 **提货**。

    将从后端检索订单。 

16. 从后端检索订单行详细信息，并且检测到可用于全渠道的卡付款时，将通知您有付款方式可用。
17. 选择 **使用可用的付款方式** 通过使用在引用店面中输入的卡详细信息完成交易记录。

    将在交易记录页中加载订单行，而结欠金额为 0（零）。

18. 选择 **付款** 选项卡查看从在线订单提取的支付方式行。 
19. 选择任何付款方式完成交易记录。 

### <a name="buy-in-store-a-ship-to-customer"></a>商店 A 购买，发货给客户

1. 启动休斯顿商店的 POS。
2. 在 **交易记录** 页中，通过使用数字小键盘输入 **2001** 来将 Karen Berg 添加到交易记录。
3. 向交易记录添加一行或多行。
4. 选择 **订单** 以查看订单选项。
5. 选择 **全部装运**，然后在系统提示时选择 **客户订单**。
6. 在装运方式页面中，选择 **标准隔夜**，然后选择 **确定** 接受今天的日期作为装运日期。 
7. 选择 **确定** 接受当前日期作为提货日期。
8. 选择 **卡支付** 启动付款。
9. 为卡付款支付存款结欠金额。 
10. 在付款终端完成存款付款。 
11. 支付存款后，选择使用同一张卡履行的选项，然后等待订单完成。 如果支付了 100% 的保证金（在上面的步骤 9 中），会立即从卡捕获资金，在开票时不会提供授权令牌，因为资金已捕获，跟踪状态为已支付。

为订单提货、包装和在后端开票时，将把在 POS 中提供的付款详细信息用于捕获正在装运给客户的获取的资金。 

## <a name="scenario-details"></a>方案详细信息

除了刚才介绍的基本方案，还对付款 SDK 进行了若干增强以支持全渠道付款。 

### <a name="pos"></a>POS

#### <a name="single-swipedip-for-customer-orders"></a>客户订单单次刷卡

在实施全渠道付款功能之前，在 POS 中创建包含存款的客户订单时，客户需要刷卡两次：一次存款，一次标志化卡以便后续履行订单。 开启全渠道标志化功能后，客户只需刷卡一次即可存款和为以后将履行的商品结欠金额授权。 在履行时，将捕获授权的资金。 实施全渠道标志化功能之前，将仅创建一个循环卡标志来后续履行订单。 因此，不为已挂起履行的资金授权，并且因为针对这笔具体购买冻结了资金，所以不太可能在以后捕获。

> [!NOTE]
> Retail 版本 8.1.3 不支持单次刷卡。 版本 8.1.3 中的客户订单使用实施全渠道标志化功能之前使用的相同流程。 

### <a name="cards-that-cant-issue-recurring-card-tokens"></a>不能颁发循环卡标志的卡

某些卡不能用于全渠道付款，因为不支持颁发循环卡标志。 在 POS 中创建订单时，如果存款是通过使用不支持循环卡标志的卡支付的，则使用之前的标志化流程。 因此，希望提供将用于后续履行订单的付款的客户必须再提供一张卡。 如果第二张卡不支持循环卡标志，将拒绝标志化操作，并提醒收银员请客户提供其他卡。 

### <a name="using-a-different-card"></a>使用其他卡

到店提货的客户可以选择使用其他卡。 如果在订单提货时收银员收到 **使用可用的付款方式** 提示时，该收银员可以询问客户是否要使用同一张卡。 如果客户用于创建订单的卡丢失，并且希望使用其他卡为订单付款，收银员可以选择 **使用其他付款方式**。 如果客户以后回来提取同一个订单的更多商品，并且原始卡授权仍然有效，收银员可以再次询问客户是否要使用该卡。

### <a name="invalid-authorizations"></a>无效授权

如果用于创建订单的卡不再有效，选择要提取的产品时，付款捕获请求将失败。 然后，POS 付款连接器将使用相同卡详细信息尝试创建新的授权和捕获。 如果新授权或捕获失败，将通知收银员无法处理该付款。 然后，收银员必须请客户进行新的付款。 

### <a name="multiple-available-payments"></a>多个可用付款

为具有多种支付方式和多行的订单提货时，收银员首先会收到 **使用可用的付款方式** 提示。 如果有多张卡，在收银员选择 **使用可用的付款方式** 时，将捕获现有卡支付方式行，直到余额达到正在提货的商品的要求。 收银员不能选择应该用于正在提货的商品的卡。 

## <a name="related-articles"></a>相关文章

- [付款常见问题](/dynamics365/unified-operations/retail/dev-itpro/payments-retail)
- [适用于 Adyen 的 Dynamics 365 付款连接器](/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3)
- [在 Dynamics 365 Commerce 评估环境中配置 BOPIS](./cpe-bopis.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]

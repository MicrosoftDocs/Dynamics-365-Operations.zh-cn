---
title: 销售点 (POS) 中的客户订单
description: 本主题提供有关销售点 (POS) 中客户订单的信息。 客户订单也称为特殊订单。 此主题中包含对相关参数和交易记录流的讨论。
author: josaw1
manager: AnnBe
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 9e5770de82638e6cef6d4c1dffd1dc85549fb11f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410472"
---
# <a name="customer-orders-in-point-of-sale-pos"></a>销售点 (POS) 中的客户订单

[!include [banner](includes/banner.md)]

本主题提供有关如何在销售点 (POS) 中创建和管理客户订单的信息。 客户订单可用于捕获购物者希望以后提货，从其他位置提货或将商品发给客户的销售。 

在全渠道商业环境中，许多零售商提供客户订单（即特殊订单）选项，以满足各种产品和履行要求。 下面是一些典型方案：

- 客户希望将产品在特定日期发到特定地址。
- 客户希望从非购买产品的商店或位置取货。
- 商店内的一位客户希望当天订购产品，以后再从同一家商店提货。

零售商可以使用客户订单将库存不足可能导致的失单降到最低，因为可以在其他时间或位置发货或提货。

## <a name="set-up-customer-orders"></a>设置客户订单
尝试使用 POS 中的客户订单功能之前，请确保在 Commerce 总部中完成所有必需配置。

### <a name="configure-modes-of-delivery"></a>配置交货方式

若要使用客户订单，必须配置商店渠道可以使用的交付方式。 必须定义至少一种在从商店向客户装运订单行时可使用的交货方式。 还必须定义至少一种在从商店为订单行提货时可使用的交货提货方式。 交货方式在 Commerce 总部中 **交货方式** 页面定义。 有关如何为 Commerce 渠道设置交货方式的详细信息，请参阅[定义交货方式](https://docs.microsoft.com/dynamics365/commerce/configure-call-center-delivery#define-delivery-modes)。

![“交货方式”页面](media/customer-order-modes-of-delivery.png)


### <a name="set-up-fulfillment-groups"></a>设置履行组

某些商店或仓库库位可能无法履行客户订单。 通过配置履行组，组织可以指定哪些商店和仓库库位对在 POS 中创建客户订单的用户显示为选项。 履行组在 **履行组** 页中定义。 组织可以根据需要创建任意数量的履行组。 定义履行组后，可通过使用 **商店** 页操作窗格上的 **设置** 选项卡上的按钮将其链接到商店。

在 Commerce 版本 10.0.12 及更高版本中，组织可以定义是否可以将在履行组中定义的仓库或仓库/商店组合用于装运和/或提货。 因此，商店可以更灵活地驱动对为提货创建订单和装运订单的用户显示的仓库和商店选项。 若要利用这些配置选项，必须打开 **用于在履行组中将位置指定为已启用的装运或提货** 功能。 如果链接到履行组的仓库不是商店，则只能将其配置为装运位置。 在 POS 中配置提货订单时不能使用。

![“履行组”页面](media/customer-order-fulfillment-group.png)

### <a name="configure-channel-settings"></a>配置渠道设置

在 POS 中处理客户订单时，必须考虑商店渠道的某些设置。 这些设置位于 Commerce 总部中的 **商店** 页面。

- **仓库** – 此字段指示用于履行配置为从商店装运的订单的仓库。
- **履行组分配** – 选择此按钮（位于操作窗格中的 **设置** 选项卡上）将链接引用来在 POS 中创建客户订单时显示提货位置或装运来源的选项的履行组。
- **使用基于目的地的税金**  – 此选项指示是否使用装运地址来确定应用于要装运到客户地址的订单行的税组。
- **使用基于客户的税金**  – 此选项指示是否使用为客户的交货地址定义的税组对在 POS 中创建的要运送到客户家中的客户订单征税。

![“商店”页面中的商店渠道设置](media/customer-order-all-stores.png)

### <a name="set-up-customer-order-parameters"></a>设置客户订单参数

尝试在 POS 中创建客户订单之前，必须在 Commerce 总部中配置适当的参数。 这些参数位于 **Commerce 参数** 页面的 **客户订单** 选项卡中。

- **默认订单类型**   –可以指定默认分配给在 POS 中创建的客户订单的订单类型。 这些客户订单可以是销售订单或报价订单。 无论哪种默认订单类型，用户都可以从 POS 创建销售订单和客户订单。
- **默认保证金百分比** – 指定确认订单前客户必须以存款的形式支付的订单总金额百分比。 如果为交易记录屏幕布局在 POS 中配置了 **保证金覆盖** 操作，售货员可能可以根据自己的权限使用该操作覆盖此金额。
- **交货的提货方式** – 指定应该在 POS 中为交货配置的销售订单行应用的交货方式。
- **交货的自提方式** – 指定应该应用于在创建混合购物车时视为自提订单行的销售订单行的交货方式，其中部分行将提货或装运，其他行则由立即自提。
- **取消费百分比** – 如果取消客户订单时应收取费用，请指定这笔费用的金额。
- **取消费代码**  – 指定在通过 POS 向取消的客户订单收取取消费时应使用的应收帐款费用代码。 费用代码定义取消费的财务过帐逻辑。
- **装运费用代码**  – 如果 **使用高级自动收费** 选项设置为 **是** ，此参数设置无效。 如果该选项设置为 **否** ，系统会提示用户在 POS 中创建客户订单时手动输入装运费用。 此参数用于映射在客户输入装运费用时应用于订单的应收帐款费用代码。 费用代码定义装运费用的财务过帐逻辑。
- **使用高级自动收费** – 将此选项设置为 **是** 将在 POS 中创建客户订单时使用系统计算的自动收费。 这些自动收费可用于计算装运费用或其他订单或物料特定的费用。 有关如何设置和使用高级自动收费功能的详细信息，请参阅[全渠道高级自动收费](https://docs.microsoft.com/dynamics365/commerce/omni-auto-charges)。

![“Commerce 参数”页面中的“客户订单”选项卡](media/customer-order-parameters.png)

### <a name="update-transaction-screen-layouts-in-pos"></a>更新 POS 中的交易记录屏幕布局

确保 POS 的[屏幕布局](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts)配置为支持创建和管理客户订单，并且配置所有必需的 POS 操作。 建议使用下面的一些 POS 操作来正确支持创建和管理客户订单：
- **装运所有产品** – 此操作用于指定将把交易记录购物车中的所有行装运到目的地。
- **装运所选产品** – 此操作用于指定将把交易记录购物车中的所选行装运到目的地。
- **提取所有产品** – 此操作用于指定交易记录购物车中将从所选商店位置提货的所有行。
- **提取所选产品** – 此操作用于指定交易记录购物车中将从所选商店位置提货的所选行。
- **自提所有产品** – 此操作用于指定交易记录购物车中将自提的所有行。如果在 POS 中使用此操作，将把客户订单转换为付款自提交易记录。
- **自提所选产品** – 此操作用于指定交易记录购物车中客户将在购买时自提的所选行。 此操作只有在[混合订单](https://docs.microsoft.com/dynamics365/commerce/hybrid-customer-orders)方案中才有用。
- **撤回订单** – 此操作用于搜索和检索客户订单，以便 POS 用户根据需要编辑、取消或对其执行与履行有关的操作。
- **更改交货方式** – 此操作可用于快速更改已经配置为要装运的行的交货方式，无需用户再次完成“装运所有产品”或“装运所选产品”流。
- **保证金覆盖** – 此操作可用于更改客户将为所选客户订单支付的保证金金额。

![POS 交易记录屏幕中的操作](media/customer-order-screen-layout.png)

## <a name="working-with-customer-orders-in-pos"></a>在 POS 中处理客户订单

### <a name="create-a-customer-order-for-products-that-will-be-shipped-to-the-customer"></a>为将装运到客户的产品创建客户订单

1. 在 POS 交易记录屏幕中，向交易记录添加客户。
2. 向购物车添加产品
3. 选择 **装运所选** 或 **全部装运** 将产品装运到客户帐户中的地址。
4. 选择用于创建客户订单的选项。
5. 确认或更改“发货”位置，确认或更改送货地址，然后选择发货方式。
6. 输入客户所需的订单装运日期。
7. 使用付款功能支付到期的所有计算金额，或使用 **保证金覆盖** 操作更改到期金额，然后应用付款。
8. 如果未支付全部订单总金额，请输入将在为订单开票时订单中的到期余额捕获的信用卡。

### <a name="create-a-customer-order-for-products-that-the-customer-will-pick-up"></a>为客户将提货的产品创建客户订单

1. 在 POS 交易记录屏幕中，向交易记录添加客户。
2. 向购物车添加产品
3. 选择 **提取所选产品** 或 **全部提货** 启动订单提货配置。
4. 选择客户提取所选产品的商店位置。
5. 选择提货日期。
6. 使用付款功能支付到期的所有计算金额，或使用 **保证金覆盖** 操作更改到期金额，然后应用付款。
7. 如果未支付全部订单总金额，请选择客户将在以后（提货时）提供付款，还是立即标记化信用卡，然后在提货时使用和捕获。

### <a name="edit-an-existing-customer-order"></a>编辑现有客户订单

可以根据需要通过 POS 撤回和编辑在线或在商店渠道中创建的零售订单。

> [!IMPORTANT]
> 如果为呼叫中心渠道开启了[启用订单完成](https://docs.microsoft.com/dynamics365/commerce/set-up-order-processing-options#enable-order-completion)设置，则不能通过 POS 编辑该呼叫中心渠道中创建的订单。 为了确保正确处理付款，必须通过 Commerce 总部中的呼叫中心应用程序编辑源自呼叫中心渠道并使用“启用订单完成功能”的订单。

在 Commerce 版本 10.0.13 及更低版本中，仅当订单完全打开时，用户才能通过 POS 编辑支持的客户订单。 如果已经将订单的任何行处理到履行（提货、打包等）阶段，该订单将锁定以在 POS 中进行编辑。

> [!NOTE]
> 在 Commerce 版本 10.0.14 中，POS 用户可使用[公开预览版](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms)中已发布的功能通过 POS 编辑客户订单，即使已经履行了订单中的一部分。 但是，仍然不能通过 POS 编辑已全部开票的订单。 若要测试此预览版功能和提供更多反馈，请在 **功能管理** 工作区中开启 **（预览版）在销售点中编辑部分履行的订单** 功能。 即使启用了“启用订单完成”功能，也不能编辑源自呼叫中心渠道并使用此功能的客户订单。

1. 选择 **撤回订单**。
2. 使用 **搜索** 输入筛选器以查找订单，然后选择 **应用**。
3. 在结果列表中选择订单，然后选择 **编辑**。 如果 **编辑** 按钮不可用，则订单处于不可编辑状态。
4. 在交易记录购物车中对客户订单进行必要的更改。 编辑过程中可能会禁止某些更改。
5. 通过选择付款操作完成编辑过程。
6. 若要退出编辑过程但不保存任何更改，可以使用 **取消交易** 操作。



### <a name="cancel-a-customer-order"></a>取消客户订单

1. 选择 **撤回订单**。
2. 使用 **搜索** 输入筛选器以查找订单，然后选择 **应用**。
3. 在结果列表中选择订单，然后选择 **取消**。 如果 **取消** 按钮不可用，则订单处于不可取消状态。
4. 如果配置了取消费用，请确认这些费用。 确认取消费用之前，可以根据需要调整取消费用。 
5. 在交易记录购物车中，通过选择付款操作完成取消过程。 如果支付的保证金超过了取消费用，退款付款可能到期。
6. 若要退出取消过程但不保存任何更改，可以使用 **取消交易** 操作。

## <a name="finalizing-the-customer-order-shipment-or-pickup-from-pos"></a>从 POS 完成客户订单装运或提货

创建订单后，物料将根据订单的配置由客户从商店提货或发货。 有关此过程的详细信息，请参阅[商店订单履行](https://docs.microsoft.com/dynamics365/commerce/order-fulfillment-overview)文档。

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>客户订单的异步交易记录流

可以在同步模式或异步模式下，从 POS 创建客户订单。 如果在 POS 中创建客户订单时发现了性能问题或用户延迟，请考虑开启异步订单创建功能。

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>将客户订单设置为可在异步模式下创建

1. 在 Commerce 总部的 **功能配置文件** 页面中，选择与要配置的商店对应的功能配置文件。
2. 在 **常规** 快速选项卡上，将 **在异步模式下创建客户订单** 选项设置为 **是**。

当 **在异步模式下创建客户订单** 选项设置为 **是**，将始终在异步模式下创建客户订单，即使 Retail Transaction Service (RTS) 可用。 如果将此选项设置为 **否**，将始终通过使用 RTS 在同步模式下创建客户订单。 如果客户订单是在异步模式下创建的，则这些订单是在 Commerce 总部中从 Commerce 提取 (P) 作业作为零食交易记录提取和创建的。 手动或通过批处理流程运行 **同步订单** 时，将创建零售交易记录的相应销售订单。

## <a name="additional-resources"></a>其他资源

[混合客户订单](hybrid-customer-orders.md)

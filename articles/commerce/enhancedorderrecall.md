---
title: POS 中的撤回订单操作
description: 本主题说明了可用于 POS 中改进的订单撤回页面的功能。
author: hhainesms
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 43d6b2e4e5d923b16b02337432fc5259f66c0bf1a8ba1dbf311fb76cb3f085e1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6737596"
---
# <a name="recall-order-operation-in-pos"></a>POS 中的撤回订单操作

[!include [banner](includes/banner.md)]

Commerce 销售点 (POS) 中的 **撤回订单** 操作提供更新的订单搜索和筛选功能以及订单特定信息。 Commerce 版本 10.0.15 及更高版本中提供此功能。

若要启用此功能，请在 Commerce Headquarters 的 **功能管理** 工作区中打开 **改进的 POS 中的撤回订单操作** 功能。 启用该功能后，请考虑在 POS 中更新您的[屏幕布局](pos-screen-layouts.md)以利用某些已更改的功能。

**撤回订单** 操作按钮的配置使组织可以使用预定义的显示来部署操作。

![按钮网格配置。](media/recallorderbuttongrid.png)

显示选项如下。
- **无** – 此选项将部署操作，而不显示任何特定内容。 当用户使用此配置打开操作时，将提示他们搜索和查找订单，或从预定义的订单筛选器中进行选择。
- **履行订单** – 当用户启动该操作时，将自动运行查询以搜索并显示用户当前商店要履行的订单列表。 这些订单配置为店内取货或商店发货，而这些订单行尚未领料或包装。
- **提货订单** – 当用户启动该操作时，将自动运行查询以搜索并显示配置为在用户的当前商店店内取货的订单列表。
- **装运订单** – 当用户启动该操作时，将自动运行查询以搜索并显示配置为从用户的当前商店装运的订单列表。

当从 POS 启动 **撤回订单** 操作时，如果显示配置为 **无**，用户将能够采用以下一种方法搜索和检索订单。
- 扫描订单条码。 这将搜索订单号、渠道引用和收据 ID 字段以查找匹配项。
- 在 AppBar 上选择 **搜索订单** 或 **搜索和筛选** 图标，以使用筛选机制来查找符合筛选条件的订单。
- 从 **显示订单** 下拉菜单的预定义筛选器中进行选择（履行订单、提货订单或转运订单）。

![RecallOrderMainMenu。](media/recallordermain.png)

应用搜索条件后，应用程序将显示匹配的销售订单列表。 重要的是要注意，使用搜索/筛选选项时，检索到的订单不必是链接到用户当前商店的订单。 该搜索过程将检索并显示与搜索条件匹配的任何客户订单，即使该订单已创建或者设置为由另一个商店/渠道或仓库位置来完成。

![RecallOrderDetail。](media/orderrecalldetail.png)

用户可以在列表上选择一个订单以查看其他详细信息。 屏幕右侧的信息面板显示所选订单的具体信息，包括订单行详细信息、交货详细信息和履行详细信息。

用户可以从 AppBar 中选择一个操作。 根据订单的状态，某些操作可能无法启用。

- **退货** – 启动为选定客户订单上的任何已开票产品创建退货的过程。

- **取消** – 对所选销售订单发起完全取消。 此选项不适用于通过呼叫中心渠道发起的订单，也不能用于部分取消订单。

- **履行** – 将用户转到订单履行页面，该页面将针对所选订单进行预筛选。 仅显示打开以供用户的商店履行所选订单的订单行。

- **编辑** – 允许用户更改所选的客户订单。 仅在[某些情况](customer-orders-overview.md#edit-an-existing-customer-order)可编辑订单。

- **提货** – 如果订单有一个或多个指定用于在用户当前商店提货的行，则此选项将可用。 此操作将启动提货流程，使用户可以选择要提货的产品并创建提货销售交易。

## <a name="add-notifications-to-the-recall-order-operation"></a>向撤回订单操作添加通知

在 10.0.18 版本和更高版本中，如果需要，您可以为 **订单撤回** 操作配置 POS 通知和动态磁贴预警。 有关更多信息，请参见[在销售点 (POS) 显示订单通知](notifications-pos.md)。  

[!INCLUDE[footer-include](../includes/footer-banner.md)]

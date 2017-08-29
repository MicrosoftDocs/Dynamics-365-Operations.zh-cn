---
title: "供应商与客户协作"
description: "本主题介绍您在 Finance and Operations 中如何使用供应商协作处理采购订单和监控托运库存。"
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ConsignmentProductReceiptLines, ConsignmentVendorPortalOnHand, PurchVendorPortalConfirmedOrders, PurchVendorPortalOriginalOrder, PurchVendorPortalResponsesHistoryList, PurchVendorPortalResponsesPart
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221234
ms.assetid: 6e69fb8b-6d3a-46ef-88cf-6d01212aa7c3
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 41436dab710a5fee0fe0800dff1ebefefa841afc
ms.contentlocale: zh-cn
ms.lasthandoff: 06/13/2017

---

# <a name="vendor-collaboration-with-customers"></a>供应商与客户协作

[!include[banner](../includes/banner.md)]


本主题介绍您在 Finance and Operations 中如何使用供应商协作处理采购订单和监控托运库存。

本主题介绍您在 Microsoft Finance and Operations 中如何使用供应商协作处理客户。 包括关于如何监控和响应采购订单，以及如何监控托运库存的信息。 还可以使用供应商协作处理发票。 有关详细信息，请参阅[供应商协作开票工作区](/dynamics365/unified-operations/financials/accounts-payable/vendor-portal-invoicing-workspace)。

## <a name="working-with-purchase-orders"></a>处理采购订单
“**采购订单确认**”工作区允许您响应发送给您审核的采购订单。 您还可以查看正在等待客户操作的采购订单的信息，以及已确认但仍然未结的采购订单的信息。 “**采购订单确认**”工作区有三个列表：

-   **要审核的采购订单** - 此列表显示已经发送给您并且正在等待您响应的采购订单。 您做出响应后，采购订单将从列表中消失。 如果在您响应采购订单之前，客户向您发送了采购订单的新版本，则仅显示最新版本。
-   **正在等待客户操作** - 此列表可以查看您已经响应，但客户尚未确认的采购订单。 如果您接受了 PO，您可以在此列表中进行监控，直到状态更改为“**已确认**”。 如果您拒绝 PO 或更改后接受，您可以在此处监控 PO，直到客户发送新版本。
-   **打开已确认的采购订单** - 此列表包含您的帐户中状态为“**已确认**”的所有 PO。 PO 上的产品或服务全部收到后，PO 从此列表中消失。

以下列表显示了您处理采购订单时可以使用的四个页面，其中两个页面包含与工作区中的列表相同的信息：

-   **要审核的采购订单**（见上文）
-   **采购订单供应商确认历史记录** - 此页包含已经发生给供应商的所有 PO 和 PO 的所有版本，以及供应商已经返回的所有响应。
-   **打开已确认的采购订单**（见上文）
-   **所有已确认的采购订单** - 此页包含已确认的所有 PO，包括已经收到产品或服务的 PO。 您可以使用此列表监控您可以发送发票的 PO。

### <a name="responding-to-purchase-orders"></a>响应采购订单

客户发送给您审核的采购订单在**采购订单确认**工作区和**要审核的采购订单**页面可见。 打开 PO 后，您可以选择接受、拒绝或更改后接受。 可以在 PO 标头或单独的行中添加附件。 您也可以在您在 PO 标头或单独行上的响应添加信息。 例如，您可以为某一行建议一种替代物料。 您可以使用“**预览/打印**”选项预览 PO 和打印成 PDF 文件。 您可以使用“**显示维度**”操作隐藏或显示以下维度列：站点、仓库、颜色、尺寸、样式、配置。 如果您使用**更改后接受**选项，您可以接受或拒绝单独的行。 您也可以对行进行以下更改：

-   更改日期或数量。 如果您要更新所有行上的已确认交货日期，则使用 PO 标头上的“**更新交货日期**”选项。
-   拆分不同交货日期或数量的行
-   替换物料。  为此，请在“**行详细信息**”部分的“**外部**”字段中输入物料描述和您的物料编号。

您无法更改价格信息或费用，但您可以使用附注建议更改。 如果您的客户向您发送 PO 的新版本，将有一个版本后缀，表示是先前传递的 PO 的修订版本。 **采购订单供应商确认历史记录**页允许您跟踪每个订单的历史记录。

## <a name="monitoring-consignment-inventory"></a>监控托运库存
如果正在使用托运库存，您可以使用供应商协作界面查看有关以下页面的信息：

-   **使用托运库存的采购订单** - 客户获得库存的所有权时，生成托运库存的采购订单。 这些托运采购订单仅显示在“**使用托运库存的采购订单**”页面上。 它们不包括在“**所有已确认的采购订单**”页上。
-   **从托运库存接收的产品** - 此页列出产品所有权转移至使用库存的公司的所有交易记录。 您可以使用此信息对客户开票。
-   **现有托运库存** - 此页显示客户仓库现有的您的公司拥有的现有托运库存。


<a name="see-also"></a>请参阅
--------

[管理供应商协作用户](manage-vendor-collaboration-users.md)





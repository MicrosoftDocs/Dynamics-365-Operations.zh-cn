---
title: 创建呼叫中心订单
description: 本文逐步演示一个示例过程，其中呼叫中心用户在 Microsoft Dynamics 365 Commerce 中查找客户、创建新订单、搜索产品以及收取客户付款。
author: josaw1
ms.date: 08/05/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 16d483896ce131e9a7bc60ab5ea7b8fa01a3bea8
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228502"
---
# <a name="create-call-center-orders"></a>创建呼叫中心订单

[!include [banner](../includes/banner.md)]

本文逐步演示一个示例过程，其中呼叫中心用户在 Microsoft Dynamics 365 Commerce 中查找客户、创建新订单、搜索产品以及收取客户付款。 此过程使用 USRT 演示数据公司，旨在供销售订单职员使用。 

## <a name="prerequisites"></a>先决条件

必须将完成此过程的用户设置为呼叫中心用户。 （可选）可以发布包含至少一段源代码的 Fabrikam 半年度目录。

### <a name="add-yourself-as-a-call-center-user"></a>将自己添加为呼叫中心用户

要将您自己添加为呼叫中心用户，请执行以下步骤。

1. 在 Commerce Headquarters 中，转到 **Retail 和 Commerce \> 渠道 \> 呼叫中心 \> 所有呼叫中心**。
1. 在 **用户** 字段中，选择 **渠道用户**。
1. 在操作窗格上，选择 **新建**。
1. 在 **用户 ID** 字段中，输入您的用户 ID。
1. 在 **名称** 字段中输入您的用户名。 用户名可以与用户 ID 相同。
1. 在操作窗格上，选择 **保存**。
1. 返回到 **Retail 和 Commerce \> 渠道 \> 呼叫中心 \> 所有呼叫中心**。
1. 选择呼叫中心的零售渠道 ID。
1. 确认 **启用订单完成** 选项设置为 **是**。 如果该选项不可见，则可以跳过此步骤。

## <a name="complete-the-example-call-center-procedure"></a>完成示例呼叫中心过程

若要完成示例呼叫中心过程，请执行以下步骤。

1. 转到 **Retail 和 Commerce \> 客户 \> 客户服务**。
1. 在 **客户搜索** 选项卡上，输入搜索条件以查找客户。 对于此示例过程，输入 **Karen**。
1. 选择 **搜索**。 **客户搜索** 对话框会显示并列出搜索结果。
1. 选择客户帐号为 **2001** 的 **Karen Berg** 的客户记录，然后选择 **选择**。
1. 在操作窗格上选择 **新建销售订单**。
1. 在右侧，选择 **标题** 选项卡。
1. 在 **交货** 快速选项卡上，在 **交货方式** 字段中，选择 **99 标准**。

    ![选择交付方式。](../media/Select_Mode_of_Delivery.png)

1. 在右侧，选择 **行** 选项卡。
1. 在 **销售订单行** 部分中，在新销售行的对应新行上，在 **物料编号** 字段中输入要搜索的物料编号。 对于此示例过程，请输入 **81327**，然后在下拉列表中选择产品以将其添加到销售订单。
1. 在 **数量** 字段中输入销售数量。
1. 在 **源代码** 字段中，选择目录的源代码。 如果没有活动源代码，您可以跳过此步骤。
1. 在操作窗格上，选择 **完成** 以捕获客户付款。 此操作将打开 **销售订单摘要** 对话框，该对话框显示到期的总金额。 此操作还会触发任何费用（如装运和搬运费用）的计算，并在 **销售订单摘要** 对话框中显示它们。

    ![“完成”按钮。](../media/Complete_button.png)

1. 在 **销售订单摘要** 对话框的 **付款** 快速选项卡上，选择 **添加** 以捕获付款。

    ![“销售订单摘要”对话框。](../media/order_summary.png)

1. 在 **输入客户付款信息** 对话框内的 **付款方式** 字段中，选择付款方式。 对于此示例过程，选择 **现金**。
1. 在 **付款金额** 字段中，输入付款金额。 对于此示例，输入 **120.00**，这等于 **销售订单摘要** 对话框中显示的订单余额。 通过输入此金额，您能够以全额付清形式完成订单。
1. 选择 **确定**。
1. 选择 **提交**。

## <a name="additional-resources"></a>其他资源

[按交货方式自定义事务电子邮件](../customize-email-delivery-mode.md)

[在 POS 上更改交货方式](../pos-change-delivery-mode.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

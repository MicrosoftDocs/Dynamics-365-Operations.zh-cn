---
title: 编辑并审计现金和结转及现金管理交易记录
description: 本主题介绍如何在 Microsoft Dynamics 365 Commerce 中编辑并审计现金和结转及现金管理交易记录。
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 296dbf03ed65c1994562149a2c4b8fccd9073f0d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221911"
---
# <a name="edit-and-audit-cash-and-carry-and-cash-management-transactions"></a>编辑并审计现金和结转及现金管理交易记录

[!include [banner](../includes/banner.md)]

本主题介绍如何在 Microsoft Dynamics 365 Commerce 中编辑并审计现金和结转及现金管理交易记录。

## <a name="overview"></a>概览

Dynamics 365 Commerce 客户使用第一方销售点 (POS) 应用程序和第三方 POS 应用程序。 使用第一方应用程序时，可以通过批处理将渠道中的商店交易记录导入到 Commerce Headquarters。 使用第三方应用程序时，可以通过集成将交易记录导入到 Commerce Headquarters。 在这两种情况下，将交易记录导入到 Commerce Headquarters 后，必须执行一致性检查过程。 此过程对交易记录执行多项验证，并且只有已成功通过验证的交易记录才会导入到报表中，以便可以在 Commerce Headquarters 中对这些交易记录进行过帐。

Commerce 交易记录可能会由于各种原因而验证失败。 集成代码或 POS 应用程序中的 Bug 可能会导致数据不一致。 另外，用户错误也可能会导致数据不一致。 例如，用户在产品同步到渠道后删除了该产品，或者用户未过帐会计期间的交易记录即关闭了该期间。 尽管这些交易记录已标记并从对帐单中排除，但是它们会干扰客户将每日销售过账到财务的每日流程。 在 Commerce 中，可以编辑验证失败的交易记录，同时还保持对所有更改的审计。

## <a name="edit-transactions"></a>编辑交易记录

在 Commerce 版本 10.0.5 中，可以编辑的交易记录只有现金和结转交易记录，例如销售和退货。 无法编辑客户订单和在线订单。 在 Commerce 版本 10.0.6 和更高版本中，也可以编辑现金管理交易记录。

要在 Commerce Headquarters 中编辑交易记录，请按照下列步骤操作。

1. 安装 [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview)。
1. 在 Commerce Headquarters 中，打开 **商店财务** 工作区。 **交易记录验证失败** 磁贴提供在一个或多个验证规则中验证失败的交易记录页面的预筛选视图。
1. 打开交易记录页面，选择验证失败的记录，选择 **Office 加载项**，然后选择 **编辑所选交易记录**。 此时将打开一个 Excel 文件，其中显示了所选交易记录的详细信息。 该文件包含以下工作表：

    - **行** - 此工作表包含该交易记录的标头、产品行和相关数据。
    - **付款** - 此工作表包含该交易记录的付款行的详细信息。
    - **折扣** - 此工作表包含该交易记录的折扣相关详细信息。
    - **纳税** - 此工作表包含该交易记录的纳税相关详细信息。
    - **费用** - 此工作表包含该交易记录的费用相关数据。

1. 在 Excel 文件中，修改相应的字段，然后使用 Dynamics Excel 加载项发布功能将数据重新上传到 Commerce Headquarters。 发布数据后，所做的更改将反映在系统中。 在发布期间，将不会对用户所做的更改进行验证。
1. 通过选择标头级别更改的 **零售交易记录** 标头中的 **查看审计线索**，以及在相应交易记录页面的相关部分和记录中，可以查看所做更改的完整审计线索。 例如，与销售行相关的所有更改都将显示在 **销售交易记录** 页面上，所有与付款相关的更改都将显示在 **付款交易记录** 页面上。 将保持更改的以下审计详细信息：

    - 修改日期和时间
    - 字段
    - 原值
    - 新值
    - 修改者

1. 在做出更改并发布后，请运行 **验证商店交易记录**，以验证这些更改是否一致和有效。

> [!NOTE]
> 只能编辑验证失败的交易记录。 如果要编辑通过验证的交易记录，请将该交易记录的验证状态更改为 **错误** 或者 **无**，然后发布该更改。 接下来，可以编辑该交易记录的标头或者任何其他子记录中的数据，然后发布该标头或记录。

## <a name="bulk-edit-transactions-that-are-linked-to-a-statement"></a>批量编辑链接到对帐单的交易记录

Commerce 版本 10.0.6 及更高版本支持在对帐单级别批量编辑交易记录的选项。

要在 Commerce Headquarters 中批量编辑链接到对帐单的交易记录，请按照下列步骤操作。

1. 打开 **对帐单** 页面，然后选择包含必须编辑的交易记录的对帐单。
1. 选择 **在 Microsoft Office 中打开** 按钮。
1. 根据必须编辑的内容，选择以下选项之一：

    - **编辑现金和结转交易记录** - 通过此选项可以编辑对帐单中包含的所有现金和结转交易记录。 提供了以下 Excel 工作表：

        - **交易记录** - 此工作表包含销售交易记录的所有标头级别信息。
        - **销售交易记录** - 此工作表包含销售交易记录的所有行级别信息。
        - **付款交易记录** - 此工作表包含销售交易记录的所有付款行信息。
        - **折扣交易记录** - 此工作表包含销售交易记录的所有折扣行信息。
        - **纳税交易记录** - 此工作表包含销售交易记录的所有纳税行信息。
        - **费用交易记录** - 此工作表包含销售交易记录的所有费用行信息。

    - **编辑现金管理交易记录** - 通过此选项可以编辑对帐单中包含的所有现金管理交易记录。 提供了以下 Excel 工作表：

        - **交易记录** - 此工作表包含现金管理交易记录的所有标头级别信息。
        - **银行支付交易记录** - 此工作表包含所有银行投箱交易记录详细信息。
        - **金库支付交易记录** - 此工作表包含所有金库投箱交易记录详细信息。
        - **钱币清点** - 此工作表包含所有钱币清点交易记录详细信息。
        - **收入 - 支出交易记录** - 此工作表包含所有收入 - 支出交易记录行详细信息。
        - **付款交易记录** - 此工作表包含 **付款账单** 操作以及收入 - 支出交易记录的所有付款相关信息。

1. 编辑所需交易记录。

    > [!NOTE]
    > 发布批量编辑的交易记录时，将不会执行验证。 您必须确保您的所有编辑都是准确的，并保持各工作表的数据真实可靠。 例如，如果想要更改交易记录日期，以便可以管理结帐未结交易记录的会计或库存期间的方案，则您必须更改具有 **业务日期** 列的所有 Excel 工作表的日期。 要在编辑交易记录之后对其进行验证，可以选择 **对帐单** 页面上的 **重新验证交易记录**。 请等待验证作业运行完成，然后再过帐对帐单。

1. 如果已经生成聚合值，请打开 **聚合交易记录** 页面，然后选择 **重新生成销售订单 xml**。

## <a name="bulk-edit-transactions-that-arent-linked-to-a-statement"></a>批量编辑未链接到对帐单的交易记录

Commerce 版本 10.0.10 及更高版本支持对验证失败但未链接到对帐单的交易记录进行批量编辑。

要在 Commerce Headquarters 中批量编辑未链接到对帐单的交易记录，请按照下列步骤操作。

1. 打开 **所有商店** 页面，然后选择必须编辑其交易记录的商店。
1. 选择 **在 Microsoft Office 中打开** 按钮，然后选择 **编辑现金和结转交易记录**。
1. 编辑所需的交易记录，然后将其发布。

## <a name="additional-resources"></a>其他资源

[编辑并审计在线订单和异步客户订单交易记录](edit-order-trans.md)

[编辑零售交易记录的财务维度](edit-financial-dim.md)

[创建 Excel 工作簿以编辑零售交易记录](create-excel-edit.md)

[将字段添加到 Excel 工作簿以编辑零售交易记录](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
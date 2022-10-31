---
title: 编辑并审计在线订单和异步客户订单交易记录
description: 本文将介绍如何在 Microsoft Dynamics 365 Commerce 中编辑并审计在线订单和异步客户订单交易记录。
author: josaw1
ms.date: 10/21/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.industry: Retail
ms.openlocfilehash: dbeeff47446c1617da44f34ae56f333717f577a1
ms.sourcegitcommit: 18b7a02c497709e8d9c7b943d82f1fcc3dafa4cd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/21/2022
ms.locfileid: "9712099"
---
# <a name="edit-and-audit-online-order-and-asynchronous-customer-order-transactions"></a>编辑并审计在线订单和异步客户订单交易记录

[!include [banner](../includes/banner.md)]

本文将介绍如何在 Microsoft Dynamics 365 Commerce 中编辑并审计在线订单和异步客户订单交易记录。

## <a name="overview"></a>概览

在 Commerce 版本 10.0.5 和 10.0.6 中，增加了对编辑现金和结转交易记录（例如销售和退货）及现金管理交易记录（例如浮动条目和支付方式删除）的支持。 在 Commerce 版本 10.0.7 中，增加了对编辑在线订单交易记录和异步客户订单交易记录的支持。

## <a name="edit-and-audit-order-transactions"></a>编辑和审计订单交易记录

要在 Commerce Headquarters 中编辑和审计订单交易记录，请按照下列步骤操作。

1. 安装 [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview)。
1. 在 **Commerce 参数** 页面、**客户订单** 选项卡、**订单** 快速选项卡上，为 **订单同步错误的暂停代码** 指定暂停代码。
2. 暂停与您的编辑和审计时间冲突的其他订单同步作业。
3. 打开 **商店财务** 工作区。 **在线订单同步错误** 和 **客户订单同步错误** 磁贴提供零售交易记录页面的预筛选视图。 每个磁贴都显示对应订单类型中同步失败的交易记录。
4. 打开 **在线订单同步错误** 页面或 **客户订单同步错误** 页面。 选择一条记录以查看同步错误详细信息。 **同步状态** 快速选项卡提供以下错误详细信息：

    - 待定订单状态
    - 订单错误详细信息
    - 修改日期和时间
    - 重试计数

1. 如果错误详细信息指示必须修复该记录，请选择 **Office 加载项**，然后选择 **编辑所选交易记录**。 此时将打开一个 Excel 文件，其中显示了所选交易记录的详细信息。

    - 如果正在编辑的交易记录是在线订单交易记录，则该 Excel 文件包含以下工作表：

        - **交易记录** - 此工作表包含该交易记录的标头详细信息。
        - **销售交易记录** - 此工作表包含该交易记录的行详细信息。
        - **付款交易记录** - 此工作表包含该交易记录的付款行的详细信息。
        - **折扣交易记录** - 此工作表包含该交易记录的折扣相关详细信息。
        - **纳税交易记录** - 此工作表包含该交易记录的纳税相关详细信息。
        - **费用交易记录** - 此工作表包含该交易记录的费用相关数据。

    - 如果正在编辑的交易记录是异步客户订单交易记录，则该 Excel 文件包含以下工作表：

        - **行** - 此工作表包含该交易记录的标头和行详细信息。
        - **付款** - 此工作表包含该交易记录的付款行的详细信息。
        - **折扣** - 此工作表包含该交易记录的折扣相关详细信息。
        - **纳税** - 此工作表包含该交易记录的纳税相关详细信息。
        - **费用** - 此工作表包含该交易记录的费用相关数据。

1. 在 Excel 文件的 **待定订单状态** 字段中，输入 **正在编辑**，然后发布该更改。 这样，可以防止正在以批处理模式运行的 **同步订单** 作业在处理过程中跳过此记录。
1. 在 Excel 文件中，修改相应的字段，然后使用 Dynamics Excel 加载项发布功能将数据重新上传到 Commerce Headquarters。 发布数据后，所做的更改将反映在系统中。 在发布期间，将不会对用户所做的更改进行验证。
    > [!NOTE]
    > 如果找不到需要编辑的字段，请按照下列步骤在工作表中添加缺少的字段。
    >   1. 在数据连接器中选择 **设计**。
    >   1. 选择要在其中添加字段的表格旁边的铅笔图标。
    >   1. 选择 **可用字段** 部分中的字段，然后选择 **添加**。
    >   1. 根据需要添加任意数量的字段，然后选择 **更新**。
    >   1. 完成更新后，您可能需要选择 **刷新** 以更新值。

3. 通过选择标头级别更改的 **零售交易记录** 标头中的 **查看审核线索**，以及在相应交易记录页面的相关部分和记录中，可以查看所做更改的完整审核线索。 例如，与销售行相关的所有更改都将显示在 **销售交易记录** 页面上，所有与付款相关的更改都将显示在 **付款交易记录** 页面上。 将保持更改的以下审计详细信息：

    - 修改日期和时间
    - 字段
    - 原值
    - 新值
    - 修改者

1. 在做出更改并发布后，请选择 **同步订单** 以立即启动同步过程。 或者，您可以等待正在以批处理模式运行的同步过程完成，然后再处理该交易记录。

默认情况下，成功同步订单后，将根据 Commerce 参数中定义的暂停代码，将订单置于保留状态。 必须先取消对订单的保留，然后才能进一步处理订单以进行履行或其他操作。

## <a name="additional-resources"></a>其他资源

[编辑并审计现金和结转及现金管理交易记录](edit-cash-trans.md)

[编辑零售交易记录的财务维度](edit-financial-dim.md)

[创建 Excel 工作簿以编辑零售交易记录](create-excel-edit.md)

[将字段添加到 Excel 工作簿以编辑零售交易记录](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

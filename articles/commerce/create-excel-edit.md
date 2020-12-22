---
title: 创建 Excel 工作簿以编辑零售交易记录
description: 本主题介绍如何创建 Excel 工作簿，以便您可以在 Microsoft Dynamics 365 Commerce 中编辑零售交易记录。
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: b2b6e98db54e7747912aad26f4b8ae24b9ad5a6d
ms.sourcegitcommit: ce51ff2b6099c75dceb99de6dea9d53baf99772d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/04/2020
ms.locfileid: "4458570"
---
# <a name="create-an-excel-workbook-to-edit-retail-transactions"></a>创建 Excel 工作簿以编辑零售交易记录

[!include [banner](../includes/banner.md)]

本主题介绍如何创建 Excel 工作簿，以便您可以在 Microsoft Dynamics 365 Commerce 中编辑零售交易记录。

## <a name="overview"></a>概览

提供了一个预定义的 Excel 模板，客户可以从系统的不同部分访问该模板，以及将其用于编辑和审计零售交易记录。 但是，客户也可以针对此目的创建一个自定义的 Excel 工作簿。

## <a name="create-and-configure-an-excel-workbook"></a>创建和配置 Excel 工作簿

要创建和配置 Excel 工作簿，以便您可以编辑零售交易记录，请按照下列步骤操作。

1. 打开 Excel，并创建一个空白工作簿。
1. 在 **插入** 选项卡上，选择 **我的加载项**。
1. 在右侧窗格中，选择 **添加服务器信息** 链接。
1. 输入服务器 URL，然后选择 **确定**。
1. 如果收到“找不到小程序注册”错误消息，请按照以下步骤操作来解决问题：

    1. 在 Commerce 中，转到 **系统管理 \> 设置 \> Office 应用参数**。
    1. 在 **应用参数** 快速选项卡上，选择 **初始化应用参数**。
    1. 在确认消息框中，选择 **确定**。
    1. 在 **已注册的小程序** 快速选项卡上，选择 **初始化小程序注册**。
    1. 根据需要，重复前面的三个步骤。

1. 选择 **设计**，然后选择 **添加表**。
1. 根据必须修改的数据，选择必须添加到 Excel 工作簿中以进行编辑的实体。 使用下表作为参考。

    | 交易记录类型 | 要使用的数据实体 |
    |------------------|----------------------|
    | 现金和结转交易、在线订单、异步客户订单、异步客户报价 | 交易记录（可审计）、销售交易记录（可审计）、付款交易记录（可审计）、纳税交易记录（可审计）、折扣交易记录（可审计）、费用交易记录（可审计） |
    | 银行投箱 | 交易记录（可审计）、银行支付交易记录（可审计） |
    | 金库投箱 | 交易记录（可审计）、金库支付交易记录（可审计） |
    | 钱币清点 | 交易记录（可审计）、钱币清点交易记录（可审计） |
    | 收入、支出 | 交易记录（可审计）、收入/支出交易记录（可审计）、付款交易记录（可审计） |
    | 清点起始金额、支付方式删除、浮动条目、找零支付方式、账单付款、客户存款 | 交易记录（可审计）、付款交易记录（可审计） |

    > [!NOTE]
    > 务必注意，只能向每个 Excel 工作簿添加一个数据实体。 此外，必须将钥匙符号标记的所有字段都添加到相关工作簿中。

1. 配置工作簿后，应用所需的筛选器。 请确保对文件中的所有工作表应用相同的筛选器。 避免将大量数据加载到 Excel 文件中。 否则，可能会影响性能，并且 Excel 和您的系统运行速度可能会变慢。 我们建议您始终使用“公司”和“报表编号”或“交易记录编号”作为文件的筛选器。
1. 配置筛选器后，选择 **刷新** 以加载数据。
1. 编辑所需的数据，然后将其发布。 如果 **发布** 按钮不可用，原因可能是某些关键字段未添加到 Excel 工作簿中。

## <a name="additional-resources"></a>其他资源

[编辑并审计现金和结转及现金管理交易记录](edit-cash-trans.md)

[编辑并审计在线订单和异步客户订单交易记录](edit-order-trans.md)

[编辑零售交易记录的财务维度](edit-financial-dim.md)

[将字段添加到 Excel 工作簿以编辑零售交易记录](add-fields-excel.md)

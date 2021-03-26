---
title: 编辑零售交易记录的财务维度
description: 本主题介绍如何在 Microsoft Dynamics 365 Commerce 中编辑零售交易记录的财务维度。
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
ms.openlocfilehash: 4d4b7e383ca2089ee98e70d23ccd890d0e6a86c5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221790"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a>编辑零售交易记录的财务维度

[!include [banner](../includes/banner.md)]

本主题介绍如何在 Microsoft Dynamics 365 Commerce 中编辑零售交易记录的财务维度。

## <a name="edit-financial-dimensions"></a>编辑财务维度

要在 Commerce Headquarters 中编辑零售交易记录的财务维度，请按照下列步骤操作。

1. 打开 **用于集成应用程序的财务维度配置** 页面。
1. 选择有效的 **默认维度集成** 记录。
1. 在 **财务维度** 快速选项卡上，确保您要在 Excel 工作表中编辑的所有维度都存在于 **已选择** 列表中。 有关详细信息，请参阅[数据实体](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration#data-entities)。
1. 从 **商店财务** 工作区的 **对帐单** 页面、**零售交易记录** 页面或 **交易记录验证失败** 磁贴中下载并打开 Excel 文件。
1. 要更改交易记录财务维度，请选择 **设计**，然后选择 **交易记录（可审计）** 行旁边的铅笔符号。
1. 找到并选择 **FinancialDimensionDisplayValue** 字段，在 Excel 工作表的标头部分中选择一个单元格，然后选择 **添加标签**。
1. 选择在上一步中选择的单元格下方的一个单元格，选择 **添加值**，然后选择 **刷新**。 将财务维度添加到 Excel 工作表中，然后可以对其进行编辑并发布。
1. 要更改交易记录行上的维度，请选择 **销售交易记录（可审计）** 行，选择铅笔符号，然后重复步骤 6 和 7。
1. 要更改付款行上的维度，请选择 **付款交易记录（可审计）** 行，选择铅笔符号，然后重复步骤 6 和 7。

## <a name="additional-resources"></a>其他资源

[编辑并审计现金和结转及现金管理交易记录](edit-cash-trans.md)

[编辑并审计在线订单和异步客户订单交易记录](edit-order-trans.md)

[创建 Excel 工作簿以编辑零售交易记录](create-excel-edit.md)

[将字段添加到 Excel 工作簿以编辑零售交易记录](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
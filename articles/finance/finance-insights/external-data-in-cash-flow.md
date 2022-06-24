---
title: 在现金流预测中的外部数据
description: 本文介绍了要将外部数据输入或导入到现金流预测中必须完成的设置步骤。
author: RyanCCarlson2
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f0cb05770dc2fbd4e13af261b5f0a0e117a2f6d7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846935"
---
# <a name="external-data-in-cash-flow-forecasts"></a>在现金流预测中的外部数据

[!include [banner](../includes/banner.md)]

可以将外部数据输入或导入现金流预测中。 本文描述了特定于外部数据的使用和将外部数据添加到现金流预测中的设置步骤。

## <a name="external-data-setup"></a>外部数据设置

使用 **现金流预测设置** 页面（**现金和银行管理 \> 现金流预测 \> 现金流预测设置**）上的 **外部源** 选项卡输入支持在现金流预测中使用外部数据的设置。

可以将外部数据输入或导入现金流预测中。 在输入或导入外部数据之前，必须设置外部源。 在 **外部源** 选项卡上，设置外部现金流类别。 类别可以是 **传出** 或 **传出**。 应选择 **流动性** 作为过帐类型。 在 **法人设置** 网格中，选择外部现金流类别适用的法人和相应的主科目。

有关如何设置现金流预测的详细信息，请参阅[现金流预测](../cash-bank-management/cash-flow-forecasting.md)。

## <a name="enter-external-data"></a>输入外部数据

要为现金流预测输入和修改外部数据，可以使用 **在 Excel 中打开** 体验。 在 **现金流预测设置** 工作区页面上选择 **外部数据** 按钮，然后选择 **添加外部数据** 或 **编辑现有外部数据**。 Microsoft Excel 文件打开后，可以在以下字段中输入信息：

- **分录 ID**（唯一）
- **描述**（可选）
- **外部源名称** – 在设置 Finance Insights 时定义的列表中选择一个值。
- **法人**
- **日期**
- **金额(交易币种)**
- **币种代码**
- **默认维度**（可选）
- **文档编号**（可选）
- **科目编号**（可选）
- **科目名称**（可选）

## <a name="importing-external-data-by-using-the-data-management-framework"></a>使用数据管理框架导入外部数据

可以使用 **数据管理** 工作区和名称为 **现金流预测外部源输入** 的实体为现金流预测导入外部数据。

此外，如果必须将设置数据从一个环境移动到另一个环境，可为所需设置表使用以下实体：

- 现金流量预测外部源设置
- 现金流量预测外部源法人设置

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

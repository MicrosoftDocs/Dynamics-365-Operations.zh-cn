---
title: 通过重新应用 Excel 模板修改电子报告格式
description: 本文介绍如何通过重新应用经修改的 Excel 模板修改用于生成业务文档的电子报告 (ER) 格式。
author: kfend
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
ms.openlocfilehash: 02423a75d96bef0452b8555f8c7a9f0aca0b6771
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283519"
---
# <a name="modify-electronic-reporting-formats-by-reapplying-excel-templates"></a>通过重新应用 Excel 模板修改电子申报格式

[!include [banner](../includes/banner.md)]

电子报告 (ER) 工具用于生成电子格式的业务文档。 若要生成业务文档，您必须创建 ER 格式，然后使用 ER 设计器来定义业务文档的布局并指定其应包括的数据。 随后您可以运行 ER 格式以生成业务文档。

ER 工具可用于将业务文档生成为 Microsoft Excel 文件。 可以使用 Excel 文档作为这些文档的模板。 若要在 ER 设计器中定义文档布局，可以将您要用作模板的 Excel 文档的内容导入到定义的 ER 格式中。 若要了解详细信息并实践此方案，播放任务指南 **ER 设计用于生成 OPENXML 格式的报表的配置**（7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677) 业务流程的一部分）。 在导入 Excel 模板的任务指南步骤中，请使用付款报表 Excel 文件 [SampleVendPaymWsReport](https://download.microsoft.com/download/e/6/b/e6bb79f0-cc08-44af-96fa-49c7929d4fb8/SampleVendPaymWsReport.xlsx) 的初始模板。

如果编辑用作业务文档模板的 Excel 文档，新的 ER 功能让您可以将更新的模板应用到 ER 格式。 ER 格式然后会更新，以便符合更新的模板。 有关此功能的更多详细信息，请播放任务指南 **ER 通过重新应用 Excel 模板修改格式**（7.5.5.3 获取/开发 IT 服务/解决方案组件 (10683) 业务流程的一部分）。 在导入更新的模板的任务指南步骤中，请使用付款报表 Excel 文件 [SampleVendPaymWsReport2](https://download.microsoft.com/download/3/1/0/3104d397-c9c5-4227-b68e-f98625313801/SampleVendPaymWsReport2.xlsx) 的已修改模板。

## <a name="additional-resources"></a>其他资源

[更新模板](er-fillable-excel.md#update-a-template)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

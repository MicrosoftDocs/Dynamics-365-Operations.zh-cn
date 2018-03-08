---
title: "通过重新应用 Microsoft Excel 模板修改电子申报格式"
description: "此主题提供有关如何通过重新应用经修改的 Excel 模板修改用于生成业务文档的电子报告 (ER) 格式的信息。"
author: NickSelin
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2bc175ceec7ee8771e09f1dac4ede7b3fa619322
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---
# <a name="modify-an-electronic-reporting-format-by-reapplying-a-microsoft-excel-template"></a>通过重新应用 Microsoft Excel 模板修改电子申报格式

[!include[banner](../includes/banner.md)]

电子报告 (ER) 工具用于生成电子格式的业务文档。 若要生成业务文档，您必须创建 ER 格式，然后使用 ER 设计器来定义业务文档的布局并指定其应包括的数据。 随后您可以运行 ER 格式以生成业务文档。

ER 工具可用于将业务文档生成为 Microsoft Excel 文件。 可以使用 Excel 文档作为这些文档的模板。 若要在 ER 设计器中定义文档布局，可以将您要用作模板的 Excel 文档的内容导入到定义的 ER 格式中。 若要了解详细信息并实践此方案，播放任务指南 **ER 设计用于生成 OPENXML 格式的报表的配置**（7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677) 业务流程的一部分）。

如果编辑用作业务文档模板的 Excel 文档，新的 ER 功能让您可以将更新的模板应用到 ER 格式。 ER 格式然后会更新，以便符合更新的模板。 有关此功能的更多详细信息，请播放任务指南 **ER 通过重新应用 Excel 模板修改格式**（7.5.5.3 获取/开发 IT 服务/解决方案组件 (10683) 业务流程的一部分）。 在导入更新的模板的任务指南步骤中，请使用付款报表 Excel 文件 SampleVendPaymWsReport2 修改后的模板作为模板。


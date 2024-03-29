---
title: 使用 ER 创建电子单据和更新应用程序数据
description: 您可以设计可在应用程序中用来生成传出电子文档的电子申报 (ER) 格式。
author: kfend
ms.date: 04/23/2021
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
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
ms.openlocfilehash: 1be618d16be2ce9e50c2a43864040dfd23a8ff69
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269652"
---
# <a name="generate-electronic-documents-and-update-application-data-by-using-er"></a>使用 ER 生成电子文档并更新应用程序数据

[!include [banner](../includes/banner.md)]

您可以设计可在应用程序中用来生成传出电子文档的电子申报 (ER) 格式。 您还可以设计用于分析传入电子文档并使用这些文档中的内容更新应用程序数据的 ER 格式。

借助此功能，可使用单个 ER 格式生成传出电子文档后再更新应用程序数据。 此功能还可用于以下方案：

- 为了防止在后续流程中重复使用应用程序数据，您可以在使用应用程序数据生成电子文档后立即标记该数据。 例如，您可以将付款交易记录包含在生成的付款消息中后立即将其标记为已处理。
- 使用 ER 逻辑存储已生成的电子文档的处理详细信息。 例如，使用 ER 表达式生成的唯一付款消息标识符。 该表达式基于在运行 ER 格式生成文档时在 ER 对话框中输入的信息。

要了解有关此功能的更多信息，请播放一组 ER 生成带应用程序数据更新的文档任务指南（7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677) 业务流程的一部分），这些任务指南将带您浏览内部统计报告和存档的详细信息。 完成这些任务指南中的特定步骤需要以下文件。 将这些文件下载和保存到您的本地计算机。

- [ER 数据模型配置：内部统计（模型）](https://download.microsoft.com/download/9/c/e/9ceeacbe-c13e-422e-96f2-594c4a6b45b7/Intrastatmodel.xml)
- [ER 模型映射配置：内部统计（映射）](https://download.microsoft.com/download/2/1/d/21ddaaeb-64c5-4408-a35f-1ccb922d40a4/Intrastatmapping.xml)
- [ER 格式配置：内部统计（格式）](https://download.microsoft.com/download/8/b/b/8bbb8891-e88d-4739-b92a-2d1d2fffcb79/Intrastatformat.xml)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

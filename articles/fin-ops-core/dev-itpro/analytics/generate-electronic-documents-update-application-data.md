---
title: 使用 ER 创建电子单据和更新应用程序数据
description: 您可以设计可在应用程序中用来生成传出电子文档的电子申报 (ER) 格式。
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ae3405a882ac37fd9758d8ff0902896562fa06b
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093865"
---
# <a name="generate-electronic-documents-and-update-application-data-by-using-er"></a>使用 ER 生成电子文档并更新应用程序数据

[!include [banner](../includes/banner.md)]

您可以设计可在应用程序中用来生成传出电子文档的电子申报 (ER) 格式。 您还可以设计用于分析传入电子文档并使用这些文档中的内容更新应用程序数据的 ER 格式。

借助此功能，可使用单个 ER 格式生成传出电子文档后再更新应用程序数据。 此功能还可用于以下方案：

- 为了防止在后续流程中重复使用应用程序数据，您可以在使用应用程序数据生成电子文档后立即标记该数据。 例如，您可以将付款交易记录包含在生成的付款消息中后立即将其标记为已处理。
- 使用 ER 逻辑存储已生成的电子文档的处理详细信息。 例如，使用 ER 表达式生成的唯一付款消息标识符。 该表达式基于在运行 ER 格式生成文档时在 ER 对话框中输入的信息。

要了解有关此功能的更多信息，请播放一组 ER 生成带应用程序数据更新的文档任务指南（7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677) 业务流程的一部分），这些任务指南将带您浏览内部统计报告和存档的详细信息。 完成这些任务指南中的特定步骤需要以下文件。 将这些文件下载和保存到您的本地计算机。

- [ER 数据模型配置：内部统计（模型）](https://go.microsoft.com/fwlink/?linkid=849038)
- [ER 模型映射配置：内部统计（映射）](https://go.microsoft.com/fwlink/?linkid=849038)
- [ER 格式配置：内部统计（格式）](https://go.microsoft.com/fwlink/?linkid=849038)

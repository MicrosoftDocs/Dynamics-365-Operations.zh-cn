---
title: 分析 JSON 格式的传入文档
description: 本主题介绍如何设置电子申报 (ER) 格式以分析 JavaScript Object Notation (JSON) 格式的传入文档。
author: kfend
manager: AnnBe
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 8be4e225507a18a92d642ff0f3a6ca3d0ff68564
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772527"
---
# <a name="parse-incoming-documents-in-json-format"></a>分析 JSON 格式的传入文档

[!include[banner](../includes/banner.md)]

可设计电子申报 (ER) 格式以分析其中包含文本格式的数据且基于 JavaScript 的传入电子文档（换句话说，JavaScript Object Notation \[JSON\] 格式的文件）。

若要了解此功能的详细信息，请下载下表中的文件，然后播放“ER 创建格式配置以从外部 JSON 文件导入数据”任务指南。 此任务指南显示如何使用 ER 格式分析传入的 JSON 文件以更新应用程序数据。

| 称谓                                  | 文件名 |
|----------------------------------------|-----------|
| ER 格式配置                | [用于导入供应商的 trans_JSON.xml 的格式](https://go.microsoft.com/fwlink/?linkid=874111) |
| .csv 格式的传入文件示例 | [1099entries_JSON.txt](https://go.microsoft.com/fwlink/?linkid=874111) |

## <a name="requirements"></a>要求

必须先满足以下要求，再完成“ER 创建格式配置以从外部 JSON 文件导入数据”任务指南：

- JSON 文件中的父元素只能是对象元素。
- 对象的嵌套元素应该是属性元素，这样才能创建有效的 JSON 结构。
- 对象的属性元素的嵌套元素只能是 JSON 数组。
- JSON 数组中只能包含 JSON 对象。 不能包含直接字符串/数值和嵌套数组。 将按这些数组中的元素在格式中指定时的顺序对其进行分析。 将考虑每个 JSON 对象的多样性设置。

此外，如果尚未完成 [ER 创建要从外部文件导入数据所需的配置](tasks/er-required-configurations-import-data.md)任务指南，必须先完成。 请下载以下文件以完成此任务指南。

| 称谓                  | 文件名 |
|------------------------|-----------|
| ER 模型配置 | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=874111) |

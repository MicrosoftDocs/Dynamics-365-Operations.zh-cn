---
title: 分析 JSON 格式的传入文档
description: 本主题介绍如何设置电子申报 (ER) 格式以分析 JavaScript Object Notation (JSON) 格式的传入文档。
author: kfend
manager: AnnBe
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: d39a697876641b4c9647dc1a55243ac2ca7cb9e7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564487"
---
# <a name="parse-incoming-documents-in-json-format"></a><span data-ttu-id="ddd9b-103">分析 JSON 格式的传入文档</span><span class="sxs-lookup"><span data-stu-id="ddd9b-103">Parse incoming documents in JSON format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ddd9b-104">可设计电子申报 (ER) 格式以分析其中包含文本格式的数据且基于 JavaScript 的传入电子文档（换句话说，JavaScript Object Notation \[JSON\] 格式的文件）。</span><span class="sxs-lookup"><span data-stu-id="ddd9b-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents that represent data in a text format that is based on JavaScript (in other words, files in JavaScript Object Notation \[JSON\] format).</span></span>

<span data-ttu-id="ddd9b-105">若要了解此功能的详细信息，请下载下表中的文件，然后播放“ER 创建格式配置以从外部 JSON 文件导入数据”任务指南。</span><span class="sxs-lookup"><span data-stu-id="ddd9b-105">To learn more about this feature, download the files in the following table, and then play the ER Create a format configuration to import data from an external JSON file task guide.</span></span> <span data-ttu-id="ddd9b-106">此任务指南显示如何使用 ER 格式分析传入的 JSON 文件以更新应用程序数据。</span><span class="sxs-lookup"><span data-stu-id="ddd9b-106">This task guide shows how an ER format can be used to parse an incoming JSON file to update application data.</span></span>

| <span data-ttu-id="ddd9b-107">称谓</span><span class="sxs-lookup"><span data-stu-id="ddd9b-107">Title</span></span>                                  | <span data-ttu-id="ddd9b-108">文件名</span><span class="sxs-lookup"><span data-stu-id="ddd9b-108">File name</span></span> |
|----------------------------------------|-----------|
| <span data-ttu-id="ddd9b-109">ER 格式配置</span><span class="sxs-lookup"><span data-stu-id="ddd9b-109">ER format configuration</span></span>                | [<span data-ttu-id="ddd9b-110">用于导入供应商的 trans_JSON.xml 的格式</span><span class="sxs-lookup"><span data-stu-id="ddd9b-110">Format for importing vendors' trans_JSON.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |
| <span data-ttu-id="ddd9b-111">.csv 格式的传入文件示例</span><span class="sxs-lookup"><span data-stu-id="ddd9b-111">Sample of incoming file in .csv format</span></span> | [<span data-ttu-id="ddd9b-112">1099entries_JSON.txt</span><span class="sxs-lookup"><span data-stu-id="ddd9b-112">1099entries_JSON.txt</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |

## <a name="requirements"></a><span data-ttu-id="ddd9b-113">要求</span><span class="sxs-lookup"><span data-stu-id="ddd9b-113">Requirements</span></span>

<span data-ttu-id="ddd9b-114">必须先满足以下要求，再完成“ER 创建格式配置以从外部 JSON 文件导入数据”任务指南：</span><span class="sxs-lookup"><span data-stu-id="ddd9b-114">Before you complete the ER Create a format configuration to import data from an external JSON file task guide, the following requirement must be met:</span></span>

- <span data-ttu-id="ddd9b-115">JSON 文件中的父元素只能是对象元素。</span><span class="sxs-lookup"><span data-stu-id="ddd9b-115">Parent elements in the JSON file can be only object elements.</span></span>
- <span data-ttu-id="ddd9b-116">对象的嵌套元素应该是属性元素，这样才能创建有效的 JSON 结构。</span><span class="sxs-lookup"><span data-stu-id="ddd9b-116">Nested elements for an object should be property elements, so that a valid JSON structure is created.</span></span>
- <span data-ttu-id="ddd9b-117">对象的属性元素的嵌套元素只能是 JSON 数组。</span><span class="sxs-lookup"><span data-stu-id="ddd9b-117">JSON arrays can be only nested elements of the property elements of an object.</span></span>
- <span data-ttu-id="ddd9b-118">JSON 数组中只能包含 JSON 对象。</span><span class="sxs-lookup"><span data-stu-id="ddd9b-118">JSON arrays can contain only JSON objects.</span></span> <span data-ttu-id="ddd9b-119">不能包含直接字符串/数值和嵌套数组。</span><span class="sxs-lookup"><span data-stu-id="ddd9b-119">They can't contain direct string/numeric values and nested arrays.</span></span> <span data-ttu-id="ddd9b-120">将按这些数组中的元素在格式中指定时的顺序对其进行分析。</span><span class="sxs-lookup"><span data-stu-id="ddd9b-120">Elements in these arrays will be parsed in order, as they are specified in the format.</span></span> <span data-ttu-id="ddd9b-121">将考虑每个 JSON 对象的多样性设置。</span><span class="sxs-lookup"><span data-stu-id="ddd9b-121">Multiplicity settings on each JSON object will be considered.</span></span>

<span data-ttu-id="ddd9b-122">此外，如果尚未完成 [ER 创建要从外部文件导入数据所需的配置](tasks/er-required-configurations-import-data.md)任务指南，必须先完成。</span><span class="sxs-lookup"><span data-stu-id="ddd9b-122">Additionally, you must complete the [ER Create required configurations to import data from an external file](tasks/er-required-configurations-import-data.md) task guide if you haven't already completed it.</span></span> <span data-ttu-id="ddd9b-123">请下载以下文件以完成此任务指南。</span><span class="sxs-lookup"><span data-stu-id="ddd9b-123">Download the following file to complete the task guide.</span></span>

| <span data-ttu-id="ddd9b-124">称谓</span><span class="sxs-lookup"><span data-stu-id="ddd9b-124">Title</span></span>                  | <span data-ttu-id="ddd9b-125">文件名</span><span class="sxs-lookup"><span data-stu-id="ddd9b-125">File name</span></span> |
|------------------------|-----------|
| <span data-ttu-id="ddd9b-126">ER 模型配置</span><span class="sxs-lookup"><span data-stu-id="ddd9b-126">ER model configuration</span></span> | [<span data-ttu-id="ddd9b-127">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="ddd9b-127">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
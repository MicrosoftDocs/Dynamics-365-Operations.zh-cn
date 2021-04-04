---
title: 容器类别的 ER 函数列表
description: 本主题提供有关电子报告 (ER) 支持的容器函数的信息。
author: NickSelin
manager: kfend
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: b7e7d770c334647f8f11338d49b39a2e9cb5c04c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561750"
---
# <a name="list-of-er-functions-in-the-container-category"></a><span data-ttu-id="4f660-103">容器类别的 ER 函数列表</span><span class="sxs-lookup"><span data-stu-id="4f660-103">List of ER functions in the container category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4f660-104">[电子报告 (ER)](general-electronic-reporting.md) 容器 [函数](er-formula-language.md#functions)可用于执行涉及 *容器* 数据类型的数据源的操作。</span><span class="sxs-lookup"><span data-stu-id="4f660-104">[Electronic reporting (ER)](general-electronic-reporting.md) container [functions](er-formula-language.md#functions) can be used to perform operations that involve data sources of the *Container* data type.</span></span> <span data-ttu-id="4f660-105">当处理数据表示二进制大型对象 (BLOB) 格式的二进制数据的集合时，将发生这些操作。</span><span class="sxs-lookup"><span data-stu-id="4f660-105">These operations occur when the processing data represents a collection of binary data in binary large object (BLOB) format.</span></span> <span data-ttu-id="4f660-106">本主题提供这些函数的概要。</span><span class="sxs-lookup"><span data-stu-id="4f660-106">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="4f660-107">支持的函数列表</span><span class="sxs-lookup"><span data-stu-id="4f660-107">List of supported functions</span></span>

| <span data-ttu-id="4f660-108">函数</span><span class="sxs-lookup"><span data-stu-id="4f660-108">Function</span></span> | <span data-ttu-id="4f660-109">说明</span><span class="sxs-lookup"><span data-stu-id="4f660-109">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="4f660-110">Base64StringToContainer</span><span class="sxs-lookup"><span data-stu-id="4f660-110">Base64StringToContainer</span></span>](er-functions-container-base64stringtocontainer.md) | <span data-ttu-id="4f660-111">此函数返回一个 *容器* 值，此值由从表示二进制到文本编码方案 Base64 组的指定 ASCII 字符串解码的二进制内容组成。</span><span class="sxs-lookup"><span data-stu-id="4f660-111">This function returns a *Container* value that consists of binary content that is decoded from the specified ASCII string that represents a Base64 group of binary-to-text encoding schemes.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="4f660-112">其他资源</span><span class="sxs-lookup"><span data-stu-id="4f660-112">Additional resources</span></span>

[<span data-ttu-id="4f660-113">电子申报概览</span><span class="sxs-lookup"><span data-stu-id="4f660-113">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="4f660-114">电子报告中的配方设计器</span><span class="sxs-lookup"><span data-stu-id="4f660-114">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="4f660-115">电子申报公式语言</span><span class="sxs-lookup"><span data-stu-id="4f660-115">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
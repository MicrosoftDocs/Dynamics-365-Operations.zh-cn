---
title: FORMATELEMENTNAME ER 函数
description: 本主题提供有关 FORMATELEMENTNAME 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e8be55d9a90e841d64288b0c618c0012912ddbab
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745625"
---
# <a name="formatelementname-er-function"></a><span data-ttu-id="bc004-103">FORMATELEMENTNAME ER 函数</span><span class="sxs-lookup"><span data-stu-id="bc004-103">FORMATELEMENTNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bc004-104">`FORMATELEMENTNAME` 函数返回一个*字符串*值，此值代表当前电子申报 (ER) 格式元素的名称。</span><span class="sxs-lookup"><span data-stu-id="bc004-104">The `FORMATELEMENTNAME` function returns a *String* value that represents the name of the current Electronic reporting (ER) format's element.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc004-105">语法</span><span class="sxs-lookup"><span data-stu-id="bc004-105">Syntax</span></span>

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a><span data-ttu-id="bc004-106">返回值</span><span class="sxs-lookup"><span data-stu-id="bc004-106">Return values</span></span>

<span data-ttu-id="bc004-107">*字符串*</span><span class="sxs-lookup"><span data-stu-id="bc004-107">*String*</span></span>

<span data-ttu-id="bc004-108">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="bc004-108">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="bc004-109">使用说明</span><span class="sxs-lookup"><span data-stu-id="bc004-109">Usage notes</span></span>

<span data-ttu-id="bc004-110">可以在为 ER 格式组件（来自位于**收集输出详细信息**选项已打开的**常见\\文件**组件下的**文本**组）的**已收集的数据键名**和**已收集的数据键值**属性配置的 ER 表达式中调用此函数。</span><span class="sxs-lookup"><span data-stu-id="bc004-110">This function can be called in ER expressions that were configured for the **Collected data key name** and **Collected data key value** properties of an ER format component from the **Text** group that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="example"></a><span data-ttu-id="bc004-111">示例</span><span class="sxs-lookup"><span data-stu-id="bc004-111">Example</span></span>

<span data-ttu-id="bc004-112">有关如何使用此函数的详细信息，请参阅[盘点和合计格式输出的 ER 使用数据](tasks/er-format-counting-summing-1.md)任务指南，这是**购置/开发 IT 服务/解决方案组件**业务流程的一部分。</span><span class="sxs-lookup"><span data-stu-id="bc004-112">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bc004-113">其他资源</span><span class="sxs-lookup"><span data-stu-id="bc004-113">Additional resources</span></span>

[<span data-ttu-id="bc004-114">数据收集功能</span><span class="sxs-lookup"><span data-stu-id="bc004-114">Data collection functions</span></span>](er-functions-category-data-collection.md)

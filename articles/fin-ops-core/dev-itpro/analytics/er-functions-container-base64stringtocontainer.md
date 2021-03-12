---
title: Base64StringToContainer ER 函数
description: 本主题提供有关 Base64StringToContainer 电子报告 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 0e92ae41a3e0f03cb14d4791ab768f096f2a0523
ms.sourcegitcommit: e8a46e127d70986539c138b27a641bff6f6874d0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/15/2020
ms.locfileid: "4739059"
---
# <a name="base64stringtocontainer-er-function"></a><span data-ttu-id="cddaa-103">Base64StringToContainer ER 函数</span><span class="sxs-lookup"><span data-stu-id="cddaa-103">Base64StringToContainer ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cddaa-104">`BASE64STRINGTOCONTAINER` [函数](er-formula-language.md#functions)将 *字符串* 类型的指定输入转换为 *[容器](er-functions-category-container.md)* 类型的数据项。</span><span class="sxs-lookup"><span data-stu-id="cddaa-104">The `BASE64STRINGTOCONTAINER` [function](er-formula-language.md#functions) converts the specified input of the *String* type to a data item of the *[Container](er-functions-category-container.md)* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="cddaa-105">语法</span><span class="sxs-lookup"><span data-stu-id="cddaa-105">Syntax</span></span>

```vb
BASE64STRINGTOCONTAINER (input)
```

## <a name="arguments"></a><span data-ttu-id="cddaa-106">参数</span><span class="sxs-lookup"><span data-stu-id="cddaa-106">Arguments</span></span>

<span data-ttu-id="cddaa-107">`input`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="cddaa-107">`input`: *String*</span></span>

<span data-ttu-id="cddaa-108">*字符串* 类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="cddaa-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="cddaa-109">返回值</span><span class="sxs-lookup"><span data-stu-id="cddaa-109">Return values</span></span>

<span data-ttu-id="cddaa-110">*集装箱*</span><span class="sxs-lookup"><span data-stu-id="cddaa-110">*Container*</span></span>

<span data-ttu-id="cddaa-111">二进制大型对象 (BLOB) 格式的结果二进制值。</span><span class="sxs-lookup"><span data-stu-id="cddaa-111">The resulting binary value in binary large object (BLOB) format.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="cddaa-112">使用说明</span><span class="sxs-lookup"><span data-stu-id="cddaa-112">Usage notes</span></span>

<span data-ttu-id="cddaa-113">如果输入字符串未提供正确的二进制到文本编码方案的 Base64 组，则会引发“参数无效”异常。</span><span class="sxs-lookup"><span data-stu-id="cddaa-113">The "Parameter is not valid" exception is thrown if the input string doesn't provide a correct Base64 group of binary-to-text encoding schemes.</span></span>

## <a name="example"></a><span data-ttu-id="cddaa-114">示例</span><span class="sxs-lookup"><span data-stu-id="cddaa-114">Example</span></span>

<span data-ttu-id="cddaa-115">在模型映射中定义以下数据源：</span><span class="sxs-lookup"><span data-stu-id="cddaa-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="cddaa-116">引用 **DocuTypeGroup** 应用程序枚举的 *Dynamics 365 for Operations/枚举* 类型的根 **DocuTypeGroupEnum** 数据源</span><span class="sxs-lookup"><span data-stu-id="cddaa-116">The root **DocuTypeGroupEnum** data source of the *Dynamics 365 for Operations / Enumeration* type that refers to the **DocuTypeGroup** application enumeration</span></span>
- <span data-ttu-id="cddaa-117">引用 **CustTable** 应用程序表的 *Dynamics 365 for Operations/表记录* 类型的根 **Customer** 数据源</span><span class="sxs-lookup"><span data-stu-id="cddaa-117">The root **Customer** data source of the *Dynamics 365 for Operations / Table records* type that refers to the **CustTable** application table</span></span>
- <span data-ttu-id="cddaa-118">如下配置的 *计算字段* 类型的 **\#Media** 数据源：</span><span class="sxs-lookup"><span data-stu-id="cddaa-118">The **\#Media** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="cddaa-119">被添加为 **Customer** 数据源的子数据源。</span><span class="sxs-lookup"><span data-stu-id="cddaa-119">It's added as a child data source of the **Customer** data source.</span></span>
    - <span data-ttu-id="cddaa-120">包含 `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)` 表达式。</span><span class="sxs-lookup"><span data-stu-id="cddaa-120">It contains the expression `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.</span></span>

- <span data-ttu-id="cddaa-121">如下配置的 *计算字段* 类型的 **\#MediaAsBase64String** 数据源：</span><span class="sxs-lookup"><span data-stu-id="cddaa-121">The **\#MediaAsBase64String** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="cddaa-122">被添加为 **Customer.'\#Media'** 数据源的子数据源。</span><span class="sxs-lookup"><span data-stu-id="cddaa-122">It's added as a child data source of the **Customer.'\#Media'** data source.</span></span>
    - <span data-ttu-id="cddaa-123">包含 `Customer.'#Media'.'getFileContentAsBase64String()'` 表达式。</span><span class="sxs-lookup"><span data-stu-id="cddaa-123">It contains the expression `Customer.'#Media'.'getFileContentAsBase64String()'`.</span></span>

- <span data-ttu-id="cddaa-124">如下配置的 *计算字段* 类型的 **\#BlobFomBase64** 数据源：</span><span class="sxs-lookup"><span data-stu-id="cddaa-124">The **\#BlobFomBase64** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="cddaa-125">被添加为 **Customer.'\#Media'** 数据源的子数据源。</span><span class="sxs-lookup"><span data-stu-id="cddaa-125">It's added as a child data source of the **Customer.'\#Media'** data source.</span></span>
    - <span data-ttu-id="cddaa-126">包含 `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'` 表达式。</span><span class="sxs-lookup"><span data-stu-id="cddaa-126">It contains the expression `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.</span></span>

<span data-ttu-id="cddaa-127">在此示例中，**\#MediaAsBase64String** 数据源将当前媒体附件的二进制内容编码为表示二进制到文本编码方案的 Base64 组的文本。</span><span class="sxs-lookup"><span data-stu-id="cddaa-127">In this example, the **\#MediaAsBase64String** data source encodes the binary content of the current media attachment as text that represents a Base64 group of binary-to-text encoding schemes.</span></span> <span data-ttu-id="cddaa-128">**\#BlobFomBase64** 数据源对 Base64 字符串进行解码，以 BLOB 格式返回二进制值。</span><span class="sxs-lookup"><span data-stu-id="cddaa-128">The **\#BlobFomBase64** data source decodes the Base64 string and returns a binary value in BLOB format.</span></span>

![ER 模型映射设计器页上的示例数据源](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a><span data-ttu-id="cddaa-130">其他资源</span><span class="sxs-lookup"><span data-stu-id="cddaa-130">Additional resources</span></span>

[<span data-ttu-id="cddaa-131">容器函数</span><span class="sxs-lookup"><span data-stu-id="cddaa-131">Container functions</span></span>](er-functions-category-container.md)

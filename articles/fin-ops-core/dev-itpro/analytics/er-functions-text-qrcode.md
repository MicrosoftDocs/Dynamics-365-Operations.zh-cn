---
title: QRCODE ER 函数
description: 本主题提供有关 QRCODE 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b62ed829202028ca0cbf95a0dbc3460d047ca5a5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682959"
---
# <a name="qrcode-er-function"></a><span data-ttu-id="9c031-103">QRCODE ER 函数</span><span class="sxs-lookup"><span data-stu-id="9c031-103">QRCODE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c031-104">`QRCODE` 函数返回一个 *容器* 值，该值以二进制格式显示指定字符串的快速响应代码（QR 代码）图像。</span><span class="sxs-lookup"><span data-stu-id="9c031-104">The `QRCODE` function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c031-105">语法</span><span class="sxs-lookup"><span data-stu-id="9c031-105">Syntax</span></span>

```vb
QRCODE (text)
```

## <a name="arguments"></a><span data-ttu-id="9c031-106">参数</span><span class="sxs-lookup"><span data-stu-id="9c031-106">Arguments</span></span>

<span data-ttu-id="9c031-107">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="9c031-107">`text`: *String*</span></span>

<span data-ttu-id="9c031-108">代表原始文本的 *字符串* 值。</span><span class="sxs-lookup"><span data-stu-id="9c031-108">A *String* value that represents the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="9c031-109">返回值</span><span class="sxs-lookup"><span data-stu-id="9c031-109">Return values</span></span>

<span data-ttu-id="9c031-110">*容器*</span><span class="sxs-lookup"><span data-stu-id="9c031-110">*Container*</span></span>

<span data-ttu-id="9c031-111">生成的二进制流。</span><span class="sxs-lookup"><span data-stu-id="9c031-111">The resulting binary stream.</span></span>

## <a name="example"></a><span data-ttu-id="9c031-112">示例</span><span class="sxs-lookup"><span data-stu-id="9c031-112">Example</span></span>

<span data-ttu-id="9c031-113">您可以配置电子申报 (ER) 格式以使用预定义的模板使用 Microsoft Office 格式（Excel 工作簿或 Word 文档）生成传出文档。</span><span class="sxs-lookup"><span data-stu-id="9c031-113">You can configure an Electronic reporting (ER) format to generate an outbound document in Microsoft Office format (Excel workbooks or Word documents) by using a predefined template.</span></span> <span data-ttu-id="9c031-114">此模板可能包含 **图片** 对象（Excel 工作簿）或 **图片内容控制**（Word 文档）作为 QR 代码图像的占位符。</span><span class="sxs-lookup"><span data-stu-id="9c031-114">This template may contain a **Picture** object (Excel workbook) or a **Picture Content Control** (Word document) as a placeholder for a QR code image.</span></span> <span data-ttu-id="9c031-115">您需要将已配置的 ER 格式添加到用于填充此占位符的 **单元格** 元素。</span><span class="sxs-lookup"><span data-stu-id="9c031-115">You need to add to the configured ER format a **Cell** element that will be used to fill this placeholder in.</span></span> <span data-ttu-id="9c031-116">要指定将哪些信息存储在 QR 代码中，您需要为此 **单元格** 元素定义绑定。</span><span class="sxs-lookup"><span data-stu-id="9c031-116">To specify what information will be stored in a QR code, you need to define a binding for this **Cell** element.</span></span> <span data-ttu-id="9c031-117">例如，您可以将此绑定配置为包含以下表达式：</span><span class="sxs-lookup"><span data-stu-id="9c031-117">For example, you can configure such binding as containing the following expression:</span></span>

```vb
QRCODE (model.ListOfShelfLabels.LabelText)`
```

<span data-ttu-id="9c031-118">运行配置的 ER 格式时，**model.ListOfShelfLabels** 数据源的 **LabelText** 字段的文本值将用于生成 QR 代码图像。</span><span class="sxs-lookup"><span data-stu-id="9c031-118">When you run the configured ER format, the text value of the **LabelText** field of the **model.ListOfShelfLabels** data source will be used to generate a QR code image.</span></span> <span data-ttu-id="9c031-119">此图像将替换用于生成出站文档的文档模板中的 QR 代码图像占位符。</span><span class="sxs-lookup"><span data-stu-id="9c031-119">This image will replace a QR code image placeholder in the document template using to generate an outbound document.</span></span> <span data-ttu-id="9c031-120">扫描生成的文档的此图像时，将返回从 **model.ListOfShelfLabels** 数据源的 **LabelText** 字段获取的文本。</span><span class="sxs-lookup"><span data-stu-id="9c031-120">When this image of the generated document is scanned, it returns the text that was taken from the **LabelText** field of the **model.ListOfShelfLabels** data source.</span></span> <span data-ttu-id="9c031-121">有关详细信息，请参阅[使用 ER 在您生成的文档中嵌入图像和形状](electronic-reporting-embed-images-shapes.md)。</span><span class="sxs-lookup"><span data-stu-id="9c031-121">For more information, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9c031-122">其他资源</span><span class="sxs-lookup"><span data-stu-id="9c031-122">Additional resources</span></span>

[<span data-ttu-id="9c031-123">文本函数</span><span class="sxs-lookup"><span data-stu-id="9c031-123">Text functions</span></span>](er-functions-category-text.md)

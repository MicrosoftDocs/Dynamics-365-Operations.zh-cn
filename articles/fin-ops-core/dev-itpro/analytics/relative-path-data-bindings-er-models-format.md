---
title: 在 ER 模型和格式的数据绑定中使用相对路径
description: 您可以通过电子报告工具定义电子格式结构，然后描述应如何填充这些结构。
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 321a85c675439b91b99ec5988494d7514a5c53f4
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093129"
---
# <a name="use-a-relative-path-in-data-bindings-of-er-models-and-formats"></a><span data-ttu-id="4a12a-103">在 ER 模型和格式的数据绑定中使用相对路径</span><span class="sxs-lookup"><span data-stu-id="4a12a-103">Use a relative path in data bindings of ER models and formats</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="4a12a-104">用户可通过电子申报 (ER) 工具定义电子格式结构，然后描述应如何使用应用程序中的数据和算法填充这些结构。</span><span class="sxs-lookup"><span data-stu-id="4a12a-104">The Electronic reporting (ER) tool lets users define electronic format structures and then describe how those structures should be filled by using data and algorithms that exist in the application.</span></span> <span data-ttu-id="4a12a-105">有关详细信息，请参阅[创建电子申报 (ER) 配置](electronic-reporting-configuration.md)。</span><span class="sxs-lookup"><span data-stu-id="4a12a-105">For more information, see [Create Electronic reporting (ER) configurations](electronic-reporting-configuration.md).</span></span> <span data-ttu-id="4a12a-106">若要指定用于检索 Finance and Operations 数据并将其用于生成电子文档的数据流，需要执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="4a12a-106">To specify the data flow for retrieving Finance and Operations data and using it to generate  an electronic document, you need to do the following:</span></span>

- <span data-ttu-id="4a12a-107">将配置的数据源绑定到特定于域的所设计[数据模型](general-electronic-reporting.md#data-model-and-model-mapping-components)的元素。</span><span class="sxs-lookup"><span data-stu-id="4a12a-107">Bind configured data sources to elements of the designed domain-specific [data model](general-electronic-reporting.md#data-model-and-model-mapping-components).</span></span> <span data-ttu-id="4a12a-108">模型结构和所选数据源可能是复杂层次结构的组成部分。</span><span class="sxs-lookup"><span data-stu-id="4a12a-108">The model structure and selected data sources might be part of a complex hierarchical structure.</span></span> <span data-ttu-id="4a12a-109">因此，最终绑定可能相当大，并且包含不同类型的大量元素（例如，关系、表和方法）。</span><span class="sxs-lookup"><span data-stu-id="4a12a-109">Because of this, final bindings can be quite large and contain many elements of different types (for example, relations, tables, and methods,).</span></span> <span data-ttu-id="4a12a-110">绑定可能变得可读性不高且相当复杂，难以查看和理解，尤其是对于非负责人而言。</span><span class="sxs-lookup"><span data-stu-id="4a12a-110">The bindings can become less readable and quite complex to review and understand, especially for non-owners.</span></span> 
- <span data-ttu-id="4a12a-111">将[格式](general-electronic-reporting.md#FormatComponentOutbound)组件用于定义使用来自数据模型的哪些数据进行填充的数据模型元素绑定到生成的格式的输出。</span><span class="sxs-lookup"><span data-stu-id="4a12a-111">Bind data model elements with [format](general-electronic-reporting.md#FormatComponentOutbound) components to define what data will be populated from the data model to the generated format’s output.</span></span>

<span data-ttu-id="4a12a-112">为了提高 ER 映射设计器的可用性，已发布了[相对路径](er-formula-language.md#relative-path)功能。</span><span class="sxs-lookup"><span data-stu-id="4a12a-112">To improve usability of ER mapping designers, the [relative path](er-formula-language.md#relative-path) feature has been released.</span></span> <span data-ttu-id="4a12a-113">默认情况下，将为应用程序的所有新实例（其中启用了 ER 设计体验，即 Microsoft Dynamics 365 Finance、Microsoft Regulatory Configuration Service）开启相对路径表示选项。</span><span class="sxs-lookup"><span data-stu-id="4a12a-113">By default, the relative path representation option is turned on for any new instance of the application where ER design experience is enabled (Microsoft Dynamics 365 Finance, Microsoft Regulatory Configuration Service).</span></span> <span data-ttu-id="4a12a-114">实施相对路径参数是为了让用户在使用 ER 绑定的此表示时继续使用完整路径。</span><span class="sxs-lookup"><span data-stu-id="4a12a-114">We implemented the relative path parameter so that users can keep using the full path when work with this presentation of ER bindings.</span></span>

<span data-ttu-id="4a12a-115">[![用户参数](./media/relative-path-01.png)](./media/relative-path-01.png)</span><span class="sxs-lookup"><span data-stu-id="4a12a-115">[![User parameters](./media/relative-path-01.png)](./media/relative-path-01.png)</span></span>

 
<span data-ttu-id="4a12a-116">开启相对路径使用参数后，将在当前模型元素的绑定中使用一个 @ 字符替换父项的路径。</span><span class="sxs-lookup"><span data-stu-id="4a12a-116">When the relative path usage parameter is turned on, a single @ character replaces the path to the parent item in the binding of the current model element.</span></span> <span data-ttu-id="4a12a-117">整个绑定路径将变短，从而让整个映射更明显，更容易理解。</span><span class="sxs-lookup"><span data-stu-id="4a12a-117">The entire binding path becomes shorter, which makes the entire mapping more obvious and easier to understand.</span></span> <span data-ttu-id="4a12a-118">大多数情况下，不需要在 ER 设计器中再滚动即可查看数据模型的所有绑定。</span><span class="sxs-lookup"><span data-stu-id="4a12a-118">In most cases, no additional scrolling is required in the ER designer to view all the bindings of the data model.</span></span>

<span data-ttu-id="4a12a-119">[![模型映射设计器](./media/relative-path-02.png)](./media/relative-path-02.png)</span><span class="sxs-lookup"><span data-stu-id="4a12a-119">[![Model mapping designer](./media/relative-path-02.png)](./media/relative-path-02.png)</span></span>
 
<span data-ttu-id="4a12a-120">开始设计新的 ER 表达式时，只需输入一个字符即可定义与父项之间的绑定。</span><span class="sxs-lookup"><span data-stu-id="4a12a-120">When you start designing a new ER expression, you need to enter only one character to define a binding to a field of the parent item.</span></span>

<span data-ttu-id="4a12a-121">[![配方设计器](./media/relative-path-03.png)](./media/relative-path-03.png)</span><span class="sxs-lookup"><span data-stu-id="4a12a-121">[![Formula designer](./media/relative-path-03.png)](./media/relative-path-03.png)</span></span>
 
<span data-ttu-id="4a12a-122">如果决定使用绝对路径更改模型父项的数据源，则必须将此模型项和所有嵌套项重新绑定到新数据源。</span><span class="sxs-lookup"><span data-stu-id="4a12a-122">When you decide to change the data source of the parent model item, with absolute path usage, you have to manually rebind this model item, as well as all nested items, to a new data source.</span></span> <span data-ttu-id="4a12a-123">开启使用相对路径并选择要绑定到父项的新数据源之后，将提供一个选项，单击一次即可自动重新绑定此父项的所有嵌套元素。</span><span class="sxs-lookup"><span data-stu-id="4a12a-123">When relative path usage is turned on, and you select a new data source to be bound to a parent item, you are offered an option to automatically rebind all nested elements of this parent item with one click.</span></span>

<span data-ttu-id="4a12a-124">[![替换现有路径消息](./media/relative-path-04.png)](./media/relative-path-04.png)</span><span class="sxs-lookup"><span data-stu-id="4a12a-124">[![Replace existing path message](./media/relative-path-04.png)](./media/relative-path-04.png)</span></span>
 
<span data-ttu-id="4a12a-125">如果确认重新绑定嵌套项，则将把新父项放到包含现有父项的每个嵌套项的路径中。</span><span class="sxs-lookup"><span data-stu-id="4a12a-125">If you confirm rebinding of nested items, the new parent item will be placed to the path of each nested item containing the existing parent item.</span></span>
<span data-ttu-id="4a12a-126">此功能不会破坏 ER 框架的向后兼容性。</span><span class="sxs-lookup"><span data-stu-id="4a12a-126">This feature does not break the backward compatibility of the ER framework.</span></span> <span data-ttu-id="4a12a-127">以前设计的所有 ER 配置都支持这项新功能，不需要升级或转换。</span><span class="sxs-lookup"><span data-stu-id="4a12a-127">All previously designed ER configurations will work with this new feature, and no upgrades or conversions are required.</span></span>

> [!NOTE]
> <span data-ttu-id="4a12a-128">将把通过大量修改模型映射中嵌套元素的绑定造成的所有更改正确保存到配置增量（即更改跟踪）中。</span><span class="sxs-lookup"><span data-stu-id="4a12a-128">All changes that are introduced by mass modification of bindings of nested elements in model mappings are correctly saved in a configuration delta (trace of changes).</span></span> <span data-ttu-id="4a12a-129">这样，客户就可以将其模型映射派生版本的基本值重定为使用这项新功能修改的任何新基础版本。</span><span class="sxs-lookup"><span data-stu-id="4a12a-129">This allows customers to rebase their derived version of model mappings to any new base version of it that has been modified by using this new feature.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4a12a-130">其他资源</span><span class="sxs-lookup"><span data-stu-id="4a12a-130">Additional resources</span></span>

[<span data-ttu-id="4a12a-131">ER 公式语言</span><span class="sxs-lookup"><span data-stu-id="4a12a-131">ER formula language</span></span>](er-formula-language.md)

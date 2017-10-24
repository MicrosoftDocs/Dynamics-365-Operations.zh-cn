---
title: "查看和导出字段描述"
description: "本文介绍了如何查看字段描述以及如何使用字段描述页导出描述。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: FieldDescriptions
audience: Application User, Developer, IT Pro
ms.reviewer: rschloma
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 11534
ms.assetid: e2795f51-a8a7-4c74-bdb9-b1be93bdd358
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 1052338522ca1f2967f6a429f81a25493b89dee0
ms.contentlocale: zh-cn
ms.lasthandoff: 07/18/2017

---

# <a name="view-and-export-field-descriptions"></a><span data-ttu-id="cb207-103">查看和导出字段描述</span><span class="sxs-lookup"><span data-stu-id="cb207-103">View and export field descriptions</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="cb207-104">本文介绍了如何查看字段描述以及如何使用字段描述页导出描述。</span><span class="sxs-lookup"><span data-stu-id="cb207-104">This article describes how to view field descriptions and how to use the Field descriptions page to export descriptions.</span></span>

<span data-ttu-id="cb207-105">Microsoft Dynamics 365 for Finance and Operations 具有某些较为复杂的字段的描述。</span><span class="sxs-lookup"><span data-stu-id="cb207-105">Microsoft Dynamics 365 for Finance and Operations has descriptions for some of the more complex fields.</span></span> <span data-ttu-id="cb207-106">在您将鼠标悬停在某个字段时，这些描述将显示。</span><span class="sxs-lookup"><span data-stu-id="cb207-106">These descriptions appear when you hover over a field.</span></span> <span data-ttu-id="cb207-107">您还可以在**字段描述**页查看和导出描述。</span><span class="sxs-lookup"><span data-stu-id="cb207-107">You can also view and export descriptions on the **Field descriptions** page.</span></span> 

<span data-ttu-id="cb207-108">并非所有页都有字段描述。</span><span class="sxs-lookup"><span data-stu-id="cb207-108">Not all pages have field descriptions.</span></span> <span data-ttu-id="cb207-109">我们只为较为复杂的字段提供描述，不为用法明显的字段提供。</span><span class="sxs-lookup"><span data-stu-id="cb207-109">We want to provide descriptions only for the more complex fields, not where the use of the field is obvious.</span></span> <span data-ttu-id="cb207-110">因此，某些页没有任何字段描述，某些页有一些描述，而一些较复杂的页面（如很多参数页）有很多描述。</span><span class="sxs-lookup"><span data-stu-id="cb207-110">Therefore, some pages don't have any field descriptions, some pages have a few descriptions, and some of the more complex pages, such as many of the parameters pages, have many descriptions.</span></span> 

<span data-ttu-id="cb207-111">如果您有权访问 Finance and Operations 开发环境，则可添加新字段描述并自定义现有描述。</span><span class="sxs-lookup"><span data-stu-id="cb207-111">If you have access to the Finance and Operations development environment, you can add new field descriptions and customize existing descriptions.</span></span> <span data-ttu-id="cb207-112">例如，您可以添加特定于公司的信息到字段描述。</span><span class="sxs-lookup"><span data-stu-id="cb207-112">For example, you can add company-specific information to a field description.</span></span> <span data-ttu-id="cb207-113">有关详细信息，请参阅[自定义字段帮助](/dynamics365/unified-operations/dev-itpro/user-interface/customize-field-help)。</span><span class="sxs-lookup"><span data-stu-id="cb207-113">For more information, see [Customize field help](/dynamics365/unified-operations/dev-itpro/user-interface/customize-field-help).</span></span>

## <a name="see-field-descriptions-in-the-user-interface"></a><span data-ttu-id="cb207-114">参阅用户界面的字段描述</span><span class="sxs-lookup"><span data-stu-id="cb207-114">See field descriptions in the user interface</span></span>
<span data-ttu-id="cb207-115">您可以通过将鼠标悬停到字段上查看字段描述。</span><span class="sxs-lookup"><span data-stu-id="cb207-115">You can view field descriptions by hovering over a field.</span></span> <span data-ttu-id="cb207-116">如果没有提供描述，当您将鼠标悬停在字段上时将看到字段名。</span><span class="sxs-lookup"><span data-stu-id="cb207-116">If no description is available, you see the field name when you hover over the field.</span></span> <span data-ttu-id="cb207-117">（注意：在版本 Dynamics AX 7.0（2016 年 2 月）中，仅可在**字段描述**页上查看字段描述。）下面的插图显示将鼠标悬停在**盘点期间锁定物料**字段上时将显示的字段描述。</span><span class="sxs-lookup"><span data-stu-id="cb207-117">(Note: In Dynamics AX 7.0 (February 2016), field descriptions can be viewed only on the **Field descriptions** page.) The following illustration shows the field description that appears when you hover over the **Lock items during count** field.</span></span> 

<span data-ttu-id="cb207-118">[![字段描述的示例](./media/field-description.png)](./media/field-description.png)</span><span class="sxs-lookup"><span data-stu-id="cb207-118">[![Example of a field description](./media/field-description.png)](./media/field-description.png)</span></span>

## <a name="use-the-field-descriptions-page-to-view-and-export-field-help"></a><span data-ttu-id="cb207-119">使用字段说明页查看和导出字段帮助</span><span class="sxs-lookup"><span data-stu-id="cb207-119">Use the Field descriptions page to view and export field help</span></span>
<span data-ttu-id="cb207-120">**字段描述**页允许查看和导出字段描述。</span><span class="sxs-lookup"><span data-stu-id="cb207-120">The **Field descriptions** page lets you view and export field descriptions.</span></span> <span data-ttu-id="cb207-121">您可以一次查看一页的可用描述。</span><span class="sxs-lookup"><span data-stu-id="cb207-121">You can see the descriptions that are available for one page at a time.</span></span>

### <a name="view-the-descriptions-for-a-page"></a><span data-ttu-id="cb207-122">查看页的描述</span><span class="sxs-lookup"><span data-stu-id="cb207-122">View the descriptions for a page</span></span>

<span data-ttu-id="cb207-123">要查看页的描述，请按以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="cb207-123">To view the descriptions for a page, follow this step.</span></span>

-   <span data-ttu-id="cb207-124">在**选择页面**字段中，键入页面的名称。</span><span class="sxs-lookup"><span data-stu-id="cb207-124">In the **Select a page** field, type the name of the page.</span></span> <span data-ttu-id="cb207-125">或者，单击箭头打开所有页的列表，然后浏览或筛选列表。</span><span class="sxs-lookup"><span data-stu-id="cb207-125">Alternatively, click the arrow to open a list of all the pages, and then browse or filter the list.</span></span>

<span data-ttu-id="cb207-126">您可以使用在用户界面 (UI) 显示的页面名称（例如，**客户**），或在右键单击页面时出现的代码名称（AOT 名称）（例如，**CustTable**）。</span><span class="sxs-lookup"><span data-stu-id="cb207-126">You can use either the name of the page that is shown in the user interface (UI) (for example, **Customers**) or the code name (AOT name) that's available when you right-click a page (for example, **CustTable**).</span></span> 

<span data-ttu-id="cb207-127">有关筛选页面列表的各种方式的信息，请参阅本文下文的“搜索页面”部分。</span><span class="sxs-lookup"><span data-stu-id="cb207-127">For information about the various ways to filter the list of pages, see the "Searching for a page" section later in this article.</span></span> 

<span data-ttu-id="cb207-128">如果设置**包含字段，但不带描述**选项为**是**，页面中的所有字段都将显示，即使它们没有字段描述。</span><span class="sxs-lookup"><span data-stu-id="cb207-128">If you set the **Include fields without a description** option to **Yes**, all the fields on the page are shown, even if they don't have a field description.</span></span>

### <a name="export-the-descriptions-for-a-page"></a><span data-ttu-id="cb207-129">导出页的描述</span><span class="sxs-lookup"><span data-stu-id="cb207-129">Export the descriptions for a page</span></span>

<span data-ttu-id="cb207-130">要导出页的描述，请按以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="cb207-130">To export the descriptions for a page, follow these steps.</span></span>

1.  <span data-ttu-id="cb207-131">在**选择页面**字段中，选择一个页面。</span><span class="sxs-lookup"><span data-stu-id="cb207-131">In the **Select a page** field, select a page.</span></span>
2.  <span data-ttu-id="cb207-132">单击右上角的**在 Microsoft Office 中打开**按钮，然后单击 **FieldDescriptionTmp**。</span><span class="sxs-lookup"><span data-stu-id="cb207-132">Click the **Open in Microsoft Office** button in the upper-right corner, and then click **FieldDescriptionTmp**.</span></span>

### <a name="searching-for-a-page"></a><span data-ttu-id="cb207-133">搜索页</span><span class="sxs-lookup"><span data-stu-id="cb207-133">Searching for a page</span></span>

<span data-ttu-id="cb207-134">可通过多种方法在**选择页面**字段中搜索页。</span><span class="sxs-lookup"><span data-stu-id="cb207-134">There are several ways to search for a page in the **Select a page** field.</span></span> <span data-ttu-id="cb207-135">在许多情况下，必须单击**选择页面**字段中的箭头才能打开下拉列表，然后在筛选后的页列表中进行选择。</span><span class="sxs-lookup"><span data-stu-id="cb207-135">In many cases, you must click the arrow in the **Select a page** field to open the drop-down list, and then select from a filtered list of pages.</span></span>

-   <span data-ttu-id="cb207-136">键入名称的一部分，然后打开下拉列表以从筛选后的页列表中进行选择。</span><span class="sxs-lookup"><span data-stu-id="cb207-136">Type part of the name, and then open the drop-down list to select from a filtered list of pages.</span></span>
-   <span data-ttu-id="cb207-137">打开下拉列表，然后单击列表顶部的**页面名称**标题，或**页面 AOT 名称**标题。</span><span class="sxs-lookup"><span data-stu-id="cb207-137">Open the drop-down list, and then click either the **Page name** heading at the top of the list or the **Page AOT name** heading.</span></span> <span data-ttu-id="cb207-138">这将出现一个对话框，供您使用高级筛选选项，如**页面名称开始于**。</span><span class="sxs-lookup"><span data-stu-id="cb207-138">A dialog box appears, where you can use advanced filtering options, such as **Page name begins with**.</span></span>
-   <span data-ttu-id="cb207-139">键入页面的全名。</span><span class="sxs-lookup"><span data-stu-id="cb207-139">Type the full name of the page.</span></span> <span data-ttu-id="cb207-140">如果使用此选项，最好打开下拉列表，看看列表中的其他选项，即使显示了字段描述。</span><span class="sxs-lookup"><span data-stu-id="cb207-140">When you use this option, it's best to open the drop-down list and see what else is in the list, even if field descriptions are shown.</span></span>
    -   <span data-ttu-id="cb207-141">如果名称只有一个精确匹配项，将显示该页的字段描述。</span><span class="sxs-lookup"><span data-stu-id="cb207-141">If there is a single exact match to the name, the field descriptions for that page are shown.</span></span>
    -   <span data-ttu-id="cb207-142">如果有多个精确匹配，则不显示描述。</span><span class="sxs-lookup"><span data-stu-id="cb207-142">If there is more than one exact match, no descriptions are shown.</span></span> <span data-ttu-id="cb207-143">您必须打开下拉列表并选择所需的网页。</span><span class="sxs-lookup"><span data-stu-id="cb207-143">You must open the drop-down list and select the page that you want.</span></span>
    -   <span data-ttu-id="cb207-144">如果您键入的名称是另一个页面的名称的一部分，您会看到您的页面的描述。</span><span class="sxs-lookup"><span data-stu-id="cb207-144">If the name that you typed is part of the name of another page, you see the descriptions for your page.</span></span> <span data-ttu-id="cb207-145">但是，如果打开下拉列表，您将看到包含该名称的其他页面。</span><span class="sxs-lookup"><span data-stu-id="cb207-145">However, if you open the drop-down list, you see additional pages that contain that name.</span></span>

<span data-ttu-id="cb207-146">例如，当您在 ****选择页面**** 字段键入**盘点**时，将不显示描述。</span><span class="sxs-lookup"><span data-stu-id="cb207-146">For example, no descriptions are shown when you type **Counting** in the ****Select a page**** field.</span></span> <span data-ttu-id="cb207-147">您打开下拉列表，将看到具有名称**盘点**的两个页面，以及名称中包含字词“盘点”的若干页面。</span><span class="sxs-lookup"><span data-stu-id="cb207-147">You open the drop-down list, and see that there are two pages that have the name **Counting** and several pages that contain the word "Counting" in the name.</span></span> <span data-ttu-id="cb207-148">如果选择 AOT 名称为 **InventJournalCount** 的页，将显示该页的字段描述。</span><span class="sxs-lookup"><span data-stu-id="cb207-148">If you select the page that has the AOT name **InventJournalCount**, the field descriptions are shown for that page.</span></span> <span data-ttu-id="cb207-149">但是，如果再次打开下拉列表，将看到列表中现在包含 AOT 名中包含“InventJournalCount”的所有页。</span><span class="sxs-lookup"><span data-stu-id="cb207-149">However, if you open the drop-down list again, you will see that the list now contains all pages that have "InventJournalCount" as part of their AOT name.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="cb207-150">疑难解答</span><span class="sxs-lookup"><span data-stu-id="cb207-150">Troubleshooting</span></span>
<span data-ttu-id="cb207-151">此部分提供的信息帮助您解决使用字段描述页时可能遇到的问题。</span><span class="sxs-lookup"><span data-stu-id="cb207-151">This section provides information to help you troubleshoot issues that you might encounter when you use field descriptions.</span></span>

### <a name="i-cant-find-a-field-description"></a><span data-ttu-id="cb207-152">我找不到字段描述</span><span class="sxs-lookup"><span data-stu-id="cb207-152">I can't find a field description</span></span>

<span data-ttu-id="cb207-153">我们正在为较为复杂的字段添加描述。</span><span class="sxs-lookup"><span data-stu-id="cb207-153">We’re in the process of adding descriptions for the more complex fields.</span></span> <span data-ttu-id="cb207-154">如果您需要有关特定字段的帮助，请通过评论此主题告知我们。</span><span class="sxs-lookup"><span data-stu-id="cb207-154">If you require help for a particular field, let us know by adding a comment for this topic.</span></span>

### <a name="the-field-description-isnt-helpful"></a><span data-ttu-id="cb207-155">此字段描述没有帮助</span><span class="sxs-lookup"><span data-stu-id="cb207-155">The field description isn't helpful</span></span>

<span data-ttu-id="cb207-156">请通过评论此主题告知我们。</span><span class="sxs-lookup"><span data-stu-id="cb207-156">Let us know by adding a comment for this topic.</span></span> <span data-ttu-id="cb207-157">如果可能，请描述所需的其他信息。</span><span class="sxs-lookup"><span data-stu-id="cb207-157">If you can, describe the additional information that you require.</span></span>

### <a name="i-cant-find-a-field-on-the-field-descriptions-page"></a><span data-ttu-id="cb207-158">我在字段描述页上找不到字段</span><span class="sxs-lookup"><span data-stu-id="cb207-158">I can't find a field on the Field descriptions page</span></span>

<span data-ttu-id="cb207-159">要显示某页中的所有字段，请将**包含字段，但不带描述**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="cb207-159">To show all the fields on a page, set the **Include fields without a description** option to **Yes**.</span></span> <span data-ttu-id="cb207-160">单击**选择页面**字段，以确认选择了正确的页面。</span><span class="sxs-lookup"><span data-stu-id="cb207-160">Click the **Select a page** field to verify that you've selected the correct page.</span></span> <span data-ttu-id="cb207-161">如果您键入的名称是另一个字段名称的一部分，您可能已经选择了具有更长名称的页面。</span><span class="sxs-lookup"><span data-stu-id="cb207-161">If the name that you typed is part of another field name, you might have selected the page that has the longer name.</span></span>

### <a name="i-cant-find-a-page-on-the-field-descriptions-page"></a><span data-ttu-id="cb207-162">我在字段描述页上找不到页面</span><span class="sxs-lookup"><span data-stu-id="cb207-162">I can't find a page on the Field descriptions page</span></span>

<span data-ttu-id="cb207-163">有关查找页面的各种方式的信息，请参阅本文先前部分的“搜索页面”部分。</span><span class="sxs-lookup"><span data-stu-id="cb207-163">For information about the various way to find pages, see the "Searching for pages" section earlier in this article.</span></span> <span data-ttu-id="cb207-164">如果已键入了页的精确名称，但是多页同名，可能不显示字段描述。</span><span class="sxs-lookup"><span data-stu-id="cb207-164">If you've typed the exact name of the page, the field descriptions might not be shown if more than one page has the same name.</span></span> <span data-ttu-id="cb207-165">单击**选择页面**字段中的箭头打开筛选后的可用页列表。</span><span class="sxs-lookup"><span data-stu-id="cb207-165">Click the arrow in the **Select a page** field to open a filtered list of the pages that are available.</span></span>

<a name="see-also"></a><span data-ttu-id="cb207-166">请参阅</span><span class="sxs-lookup"><span data-stu-id="cb207-166">See also</span></span>
--------

[<span data-ttu-id="cb207-167">自定义字段帮助</span><span class="sxs-lookup"><span data-stu-id="cb207-167">Customize field help</span></span>](/dynamics365/unified-operations/dev-itpro/user-interface/customize-field-help)





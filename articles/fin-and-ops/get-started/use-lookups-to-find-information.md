---
title: "使用查询查找信息"
description: "在 Microsoft Dynamics 365 for Finance and Operations 中，许多字段有查询功能，可帮助您轻松找到正确或需要的值。 已为查询增加了多项增强，提高了这些控件的可用性，提高了用户的工作效率。 在此主题中，您将了解这些新的查询功能，以及一些有用的提示，从而充分利用系统中的查询功能。"
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 269934
ms.assetid: f20cbd2c-14e0-47e7-b351-8e60d3537f96
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 013901724864092571099835b2c71b297710ff03
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="use-lookups-to-find-information"></a><span data-ttu-id="d1549-105">使用查询查找信息</span><span class="sxs-lookup"><span data-stu-id="d1549-105">Use lookups to find information</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d1549-106">在 Microsoft Dynamics 365 for Finance and Operations 中，许多字段有查询功能，可帮助您轻松找到正确或需要的值。</span><span class="sxs-lookup"><span data-stu-id="d1549-106">In Microsoft Dynamics 365 for Finance and Operations, many fields have lookups that can help you easily find the correct or desired value.</span></span> <span data-ttu-id="d1549-107">已为查询增加了多项增强，提高了这些控件的可用性，提高了用户的工作效率。</span><span class="sxs-lookup"><span data-stu-id="d1549-107">Several enhancements have been added to lookups that make these controls more usable and make users more productive.</span></span> <span data-ttu-id="d1549-108">在此主题中，您将了解这些新的查询功能，以及一些有用的提示，从而充分利用系统中的查询功能。</span><span class="sxs-lookup"><span data-stu-id="d1549-108">In this topic, you will learn about these new lookup features and will receive some helpful tips to get the optimal use out of lookups in the system.</span></span>  

<a name="responsive-lookups"></a><span data-ttu-id="d1549-109">查询响应速度快</span><span class="sxs-lookup"><span data-stu-id="d1549-109">Responsive lookups</span></span>
------------------

<span data-ttu-id="d1549-110">在以前版本的 Finance and Operations 中，与查询控件交互时，用户必须采取明确的操作才能打开下拉菜单。</span><span class="sxs-lookup"><span data-stu-id="d1549-110">In previous versions of Finance and Operations, when interacting with a lookup control, a user would have to take an explicit action to open the drop-down menu.</span></span> <span data-ttu-id="d1549-111">具体方法可能是，在控件中键入星号 (\*) 以基于控件的当前值筛选查询，单击下拉按钮，或使用 **Alt**+**向下键**键盘快捷方式。</span><span class="sxs-lookup"><span data-stu-id="d1549-111">This may have been by typing an asterisk (\*) in the control to filter the lookup based on the current value of the control, clicking the drop-down button, or by using the **Alt**+**Down arrow** keyboard shortcut.</span></span> <span data-ttu-id="d1549-112">已在以下方面修改了查询控件，以便更好地适应当前 Web 实践：</span><span class="sxs-lookup"><span data-stu-id="d1549-112">Lookup controls have been modified in the following ways to better align with current web practices:</span></span>

-   <span data-ttu-id="d1549-113">现在在键入时如果稍作暂停，将自动打开查询下拉菜单，并根据查询控件的值筛选下拉菜单内容。</span><span class="sxs-lookup"><span data-stu-id="d1549-113">Lookup drop-down menus will now open automatically after a slight pause in typing, with the drop-down menu contents filtered based on the lookup control's value.</span></span>
    -   <span data-ttu-id="d1549-114">请注意，已弃用了键入星号 (\*) 后自动打开下拉菜单这一原有行为。</span><span class="sxs-lookup"><span data-stu-id="d1549-114">Note that the old behavior of automatic opening of the dropdown after typing an asterisk (\*) has been deprecated.</span></span>
-   <span data-ttu-id="d1549-115">打开查询下拉菜单之后，将发生以下行为：</span><span class="sxs-lookup"><span data-stu-id="d1549-115">After the lookup drop-down menu has opened, the following will occur:</span></span>
    -   <span data-ttu-id="d1549-116">光标留在查询控件中（而不是移到下拉菜单内），所以您可以继续修改控件的值。</span><span class="sxs-lookup"><span data-stu-id="d1549-116">The cursor will stay in the lookup control (instead of focus moving into the drop-down menu) so you can continue to make modifications to the control's value.</span></span> <span data-ttu-id="d1549-117">但是，用户仍然可以使用**向上键**和**向下键**更改下拉菜单中的行，并输入以选中下拉菜单中的当前行。</span><span class="sxs-lookup"><span data-stu-id="d1549-117">However, the user can still use the **Up arrow** and **Down arrow** to change rows in the drop-down menu, and enter to select the current row in the drop-down menu.</span></span>
    -   <span data-ttu-id="d1549-118">对查询控件的值进行任何修改之后，将调整下拉菜单的内容。</span><span class="sxs-lookup"><span data-stu-id="d1549-118">The contents of the drop-down menu will adjust after any modifications are made to the lookup control's value.</span></span>

<span data-ttu-id="d1549-119">例如，假设一个查询字段的名称为**城市**。</span><span class="sxs-lookup"><span data-stu-id="d1549-119">For example, consider a lookup field called **City**.</span></span> 

<span data-ttu-id="d1549-120">焦点到**城市**字段中后，可以通过键入一些字母（如“col”）查找所需城市。</span><span class="sxs-lookup"><span data-stu-id="d1549-120">When focus is in the **City** field, you can start looking for the city that you want by typing a few letters, like "col."</span></span>  <span data-ttu-id="d1549-121">停止键入后，查询将自动打开，并筛选出以“col”开头的城市。</span><span class="sxs-lookup"><span data-stu-id="d1549-121">After you stop typing, the lookup will open automatically, filtered to those cities that begin with "col".</span></span> 

<span data-ttu-id="d1549-122">[![typeaheadLookupExample](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png)</span><span class="sxs-lookup"><span data-stu-id="d1549-122">[![typeaheadLookupExample](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png)</span></span> 

<span data-ttu-id="d1549-123">此时，光标仍在查询字段中。</span><span class="sxs-lookup"><span data-stu-id="d1549-123">At this point, the cursor is still in the lookup field.</span></span> <span data-ttu-id="d1549-124">如果继续键入，让该值为“colum”，查询内容将自动调整以体现控件中的最新值。</span><span class="sxs-lookup"><span data-stu-id="d1549-124">If you continue typing so the value is "colum," the lookup contents adjust automatically to reflect the latest value in the control.</span></span> 

![updateFilterLookupExample](./media/updatefilterlookupexample.png) 

<span data-ttu-id="d1549-126">即时焦点仍在查询控件中，您也可以使用**向上键**或**向下键**突出显示所选行。</span><span class="sxs-lookup"><span data-stu-id="d1549-126">Even though focus is still in the lookup control, you can also use the **Up arrow** or **Down arrow** keys to highlight the row that you want to select.</span></span> <span data-ttu-id="d1549-127">如果按 **Enter**，将从查询中选中突出显示的行，并更新控件的值。</span><span class="sxs-lookup"><span data-stu-id="d1549-127">If you press **Enter** the highlighted row will be selected from the lookup and the control's value will be updated.</span></span> 

![changingSelectionLookup](./media/changingselectionlookup.png)

## <a name="typing-in-more-than-ids"></a><span data-ttu-id="d1549-129">键入多个 ID</span><span class="sxs-lookup"><span data-stu-id="d1549-129">Typing in more than IDs</span></span>
<span data-ttu-id="d1549-130">输入数据时，用户自然会尝试通过名称而不是表示实体的标识来确定实体（如客户还是供应商）。</span><span class="sxs-lookup"><span data-stu-id="d1549-130">When entering data, it's natural for users to attempt to identify an entity, such as a customer or vendor, in terms of the name rather than an identifier representing the entity.</span></span> <span data-ttu-id="d1549-131">在当前版本的 Finance and Operations 中，大量（而非全部）查询限制允许上下文数据输入。</span><span class="sxs-lookup"><span data-stu-id="d1549-131">In the current version of Finance and Operations, many (but not all) lookups now allow contextual data entry.</span></span> <span data-ttu-id="d1549-132">用户可通过这项强大的功能在查询控件中键入 ID 或相应名称。</span><span class="sxs-lookup"><span data-stu-id="d1549-132">This powerful feature allows the user to type the ID or the corresponding name into the lookup control.</span></span> 

<span data-ttu-id="d1549-133">例如，创建销售订单时考虑**客户帐户**。</span><span class="sxs-lookup"><span data-stu-id="d1549-133">For example, consider the **Customer account** field when creating a sales order.</span></span> <span data-ttu-id="d1549-134">此字段显示客户的**帐户 ID**，但是创建销售订单时，用户通常更愿意为该字段输入**帐户名称**而不是**帐户 ID**，如“Forest Wholesales”而不是“US-003”。</span><span class="sxs-lookup"><span data-stu-id="d1549-134">This field shows the **Account ID** for the customer, but a user would typically prefer to enter an **Account name** instead of an **Account ID** for this field when creating a sales order, such as "Forest Wholesales" instead of "US-003."</span></span>

<span data-ttu-id="d1549-135">如果用户开始在查询控件中输入**帐户 ID**，将按照上一部分中所述自动打开下拉菜单，而用户将看到如下所示的查询。</span><span class="sxs-lookup"><span data-stu-id="d1549-135">If the user started to enter an **Account ID** into the lookup control, the drop-down menu would automatically open as described in the previous section and the user would see the lookup as shown below.</span></span>

<span data-ttu-id="d1549-136">[![输入了客户帐户 ID 时的上下文查询](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)</span><span class="sxs-lookup"><span data-stu-id="d1549-136">[![Contextual lookup when a customer account ID is entered](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)</span></span>

<span data-ttu-id="d1549-137">但是，用户现在也可以输入**帐户名称**的开头。</span><span class="sxs-lookup"><span data-stu-id="d1549-137">However, the user can also now enter the beginning of an **Account name** as well.</span></span> <span data-ttu-id="d1549-138">如果检测到此行为，用户将看到以下查询。</span><span class="sxs-lookup"><span data-stu-id="d1549-138">If this is detected, then the user will see the following lookup.</span></span> <span data-ttu-id="d1549-139">请注意**名称**列如何移动并成为查询中的第一列，以及如何根据**名称**列为查询排序和筛选。</span><span class="sxs-lookup"><span data-stu-id="d1549-139">Notice how the **Name** column is moved to be the first column in the lookup, and how the lookup is sorted and filtered based on the **Name** column.</span></span>

<span data-ttu-id="d1549-140">[![输入了客户名称时的上下文查询](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)</span><span class="sxs-lookup"><span data-stu-id="d1549-140">[![Contextual lookup when a customer name is entered](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)</span></span>

## <a name="using-grid-column-headers-for-more-advanced-filtering-and-sorting"></a><span data-ttu-id="d1549-141">使用网格列标题以执行更高级的筛选和排序</span><span class="sxs-lookup"><span data-stu-id="d1549-141">Using grid column headers for more advanced filtering and sorting</span></span>
<span data-ttu-id="d1549-142">前两部分中讨论的查询增强大大提高了用户根据查询中的 **ID** 或**名称**字段的“开始”搜索浏览查询中的行的能力。</span><span class="sxs-lookup"><span data-stu-id="d1549-142">The lookup enhancements discussed in the previous two sections greatly improve a user's ability to navigate the rows in a lookup based on a "begins with" search of the **ID** or **Name** field in the lookup.</span></span> <span data-ttu-id="d1549-143">但是，有些情况需要更高级的筛选（或排序）才能找到正确的行。</span><span class="sxs-lookup"><span data-stu-id="d1549-143">However, there are situations in which more advanced filtering (or sorting) is needed to find the correct row.</span></span> <span data-ttu-id="d1549-144">在这些情况下，用户需要使用查询中网格列标题内的筛选和排序选项。</span><span class="sxs-lookup"><span data-stu-id="d1549-144">In these situations, the user needs to use the filtering and sorting options in the grid column headers inside the lookup.</span></span> <span data-ttu-id="d1549-145">例如，假设需要找到产品为正确的“电缆”的员工输入销售订单行。</span><span class="sxs-lookup"><span data-stu-id="d1549-145">For example, consider an employee entering a sales order line who needs to locate the right "cable" as the product.</span></span> <span data-ttu-id="d1549-146">在**物料编号**控件中键入“电缆”没有用，因为没有产品名称以“电缆”开始。</span><span class="sxs-lookup"><span data-stu-id="d1549-146">Typing "cable" into the **Item number** control isn't helpful, as there are no product names that begin with "cable."</span></span> 

![emptyitemlookup](./media/emptyitemlookup.png) 

<span data-ttu-id="d1549-148">相反，用户需要清除查询控件的值，打开查询下拉菜单，然后使用网格列标题筛选下拉菜单，如下所示。</span><span class="sxs-lookup"><span data-stu-id="d1549-148">Instead, the user needs to clear the value of the lookup control, open the lookup drop-down menu, and filter the drop-down menu using the grid column header, as shown below.</span></span> <span data-ttu-id="d1549-149">鼠标（或触控）用户只需单击（或点按）任何列标题即可访问该列的筛选和排序选项。</span><span class="sxs-lookup"><span data-stu-id="d1549-149">A mouse (or touch) user can simply click (or touch) any column header to access the filtering and sorting options for that column.</span></span> <span data-ttu-id="d1549-150">对于键盘用户，用户只需再次按 **Alt**+**向下****键**将焦点移到下拉菜单中，之后，用户可以切换到正确的列，然后按 **Ctrl**+**G** 打开网格列标题下拉菜单。</span><span class="sxs-lookup"><span data-stu-id="d1549-150">For a keyboard user, the user simply needs to press **Alt**+**Down** **arrow** a second time to move focus into the drop-down menu, after which the user can tab to the correct column, and then press **Ctrl**+**G** to open the grid column header drop-down menu.</span></span> 

<span data-ttu-id="d1549-151">[![gridfilteritemlookup](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png)</span><span class="sxs-lookup"><span data-stu-id="d1549-151">[![gridfilteritemlookup](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png)</span></span> 

<span data-ttu-id="d1549-152">应用筛选器之后（见下图），用户可以照常找到并选择行。</span><span class="sxs-lookup"><span data-stu-id="d1549-152">After the filter has been applied (see the image below), the user can find and select the row as usual.</span></span> 

![filtereditemlookup](./media/filtereditemlookup.png)





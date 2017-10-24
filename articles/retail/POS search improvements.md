---
title: "POS 中的产品搜索和客户搜索"
description: "此主题概述 Dynamics 365 for Retail 中的产品和客户搜索的增强功能。"
author: shalabhjain
manager: AnnBe
ms.date: 08/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.search.scope: Operations, Retail
ms.custom: 141393
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Retail April 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 66859535ee118ffc04a847dfe6e8e0bae1cd9d6c
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="overview-of-product-and-customer-search-in-point-of-sale"></a><span data-ttu-id="946b0-103">销售点中的产品和客户搜索概述</span><span class="sxs-lookup"><span data-stu-id="946b0-103">Overview of product and customer search in Point of Sale</span></span>

<span data-ttu-id="946b0-104">现代销售点 (MPOS) 和云销售点 (CPOS) 提供易于使用的搜索功能，便于商店员工快速搜索产品和客户。</span><span class="sxs-lookup"><span data-stu-id="946b0-104">Modern Point of Sale (MPOS) and Cloud Point of Sale (CPOS) provide easy-to-use search functionality that lets store employees quickly search for products and customers.</span></span> <span data-ttu-id="946b0-105">搜索栏始终显示在 MPOS 和 CPOS 的顶部，因此员工可以快速查找产品和客户。</span><span class="sxs-lookup"><span data-stu-id="946b0-105">The search bar is always present at the top of MPOS and CPOS, so that employees can quickly find products and customers.</span></span>

<span data-ttu-id="946b0-106">员工可以在与当前商店关联的分类和目录中以及与公司中的任何其他商店关联的分类和目录中搜索产品。</span><span class="sxs-lookup"><span data-stu-id="946b0-106">Employees can search for products in the assortments and catalogs that are associated with the current store, and in the assortments and catalogs that are associated with any other store in the company.</span></span> <span data-ttu-id="946b0-107">因此，出纳可以销售和退回商店分类以外的产品。</span><span class="sxs-lookup"><span data-stu-id="946b0-107">Therefore, cashiers can sell and return products outside the store assortment.</span></span> <span data-ttu-id="946b0-108">同样，员工可以搜索与当前商店或公司中的任何其他商店关联的客户。</span><span class="sxs-lookup"><span data-stu-id="946b0-108">Similarly, employees can search for customers that are associated with the current store or any other store in the company.</span></span> <span data-ttu-id="946b0-109">此外，员工可以搜索与父组织中的不同公司关联的客户。</span><span class="sxs-lookup"><span data-stu-id="946b0-109">Additionally, employees can search for customers that are associated with a different company in the parent organization.</span></span>

## <a name="product-search"></a><span data-ttu-id="946b0-110">产品搜索</span><span class="sxs-lookup"><span data-stu-id="946b0-110">Product search</span></span> 

<span data-ttu-id="946b0-111">默认情况下，产品搜索在商店分类中完成。</span><span class="sxs-lookup"><span data-stu-id="946b0-111">By default, a product search is done on the store assortment.</span></span> <span data-ttu-id="946b0-112">此类搜索被称为*本地产品搜索*。</span><span class="sxs-lookup"><span data-stu-id="946b0-112">This type of search is known as a *local product search*.</span></span> <span data-ttu-id="946b0-113">但是，员工可以轻松切换到与当前商店关联的任何目录，或在不同商店中进行搜索。</span><span class="sxs-lookup"><span data-stu-id="946b0-113">However, employees can easily switch to any catalog that is associated with the current store, or they can search in a different store.</span></span> <span data-ttu-id="946b0-114">此类搜索被称为*远程产品搜索*。</span><span class="sxs-lookup"><span data-stu-id="946b0-114">This type of search is known as a *remote product search*.</span></span> <span data-ttu-id="946b0-115">若要更改目录，请选择页面左侧的**类别**按钮。</span><span class="sxs-lookup"><span data-stu-id="946b0-115">To change the catalog, select the **Categories** button on the left side of the page.</span></span> <span data-ttu-id="946b0-116">在显示的窗格顶部，选择**更改目录**按钮，然后选择一个可用的目录进行浏览。</span><span class="sxs-lookup"><span data-stu-id="946b0-116">At the top of the pane that appears, select the **Change catalog** button, and then select one of the available catalogs to browse it.</span></span> <span data-ttu-id="946b0-117">系统将在选定目录中搜索产品。</span><span class="sxs-lookup"><span data-stu-id="946b0-117">The system will search the selected catalog for products.</span></span>

<span data-ttu-id="946b0-118">在**更改目录**页上，员工可以轻松选择任何商店，或者可以跨所有商店搜索产品。</span><span class="sxs-lookup"><span data-stu-id="946b0-118">On the **Change catalog** page, employees can easily select any store, or they can search for products across all stores.</span></span>

<span data-ttu-id="946b0-119">![更改目录](./media/Changecatalog.png "更改目录")</span><span class="sxs-lookup"><span data-stu-id="946b0-119">![Changing the catalog](./media/Changecatalog.png "Changing the catalog")</span></span>
 
<span data-ttu-id="946b0-120">本地产品搜索在以下产品属性中进行搜索：</span><span class="sxs-lookup"><span data-stu-id="946b0-120">A local product search searches within the following product properties:</span></span>

- <span data-ttu-id="946b0-121">产品编号</span><span class="sxs-lookup"><span data-stu-id="946b0-121">Product number</span></span>
- <span data-ttu-id="946b0-122">产品名称</span><span class="sxs-lookup"><span data-stu-id="946b0-122">Product name</span></span>
- <span data-ttu-id="946b0-123">说明</span><span class="sxs-lookup"><span data-stu-id="946b0-123">Description</span></span>
- <span data-ttu-id="946b0-124">维度</span><span class="sxs-lookup"><span data-stu-id="946b0-124">Dimensions</span></span>
- <span data-ttu-id="946b0-125">条码</span><span class="sxs-lookup"><span data-stu-id="946b0-125">Barcode</span></span>
- <span data-ttu-id="946b0-126">搜索名称</span><span class="sxs-lookup"><span data-stu-id="946b0-126">Search name</span></span>

### <a name="enhancements-to-local-product-searches"></a><span data-ttu-id="946b0-127">本地产品搜索增强功能</span><span class="sxs-lookup"><span data-stu-id="946b0-127">Enhancements to local product searches</span></span>

<span data-ttu-id="946b0-128">本地产品搜索的体验对用户更加方便。</span><span class="sxs-lookup"><span data-stu-id="946b0-128">The experience for local product searches has been made more user friendly.</span></span> <span data-ttu-id="946b0-129">我们实现了以下增强功能：</span><span class="sxs-lookup"><span data-stu-id="946b0-129">The following enhancements have been made:</span></span>

- <span data-ttu-id="946b0-130">在搜索栏中添加了产品和客户下拉菜单，使员工在执行搜索前可以选择**产品**或**客户**。</span><span class="sxs-lookup"><span data-stu-id="946b0-130">Product and customer drop-down menus have been added to the search bar, so that employees can select either **Product** or **Customer** before they do the search.</span></span> <span data-ttu-id="946b0-131">默认情况下，选择**产品**，如下图中所示。</span><span class="sxs-lookup"><span data-stu-id="946b0-131">By default, **Product** is selected, as shown in the illustration that follows.</span></span>
- <span data-ttu-id="946b0-132">对于多个关键字搜索（即使用搜索词的搜索），零售商可以配置搜索结果是否包括匹配任何搜索词的结果或仅包括匹配所有搜索词的结果。</span><span class="sxs-lookup"><span data-stu-id="946b0-132">For multiple-keyword searches (that is, for searches that use search terms), retailers can configure whether the search results include results that match any search term or only results that match all search terms.</span></span> <span data-ttu-id="946b0-133">此设置在 POS 功能配置文件中命名为**产品搜索**的新组中可用。</span><span class="sxs-lookup"><span data-stu-id="946b0-133">This setting is available in the POS functionality profile, under a new group that is named **Product search**.</span></span> <span data-ttu-id="946b0-134">默认设置为**匹配任何搜索词**。</span><span class="sxs-lookup"><span data-stu-id="946b0-134">The default setting is **Match any search term**.</span></span> <span data-ttu-id="946b0-135">此设置也是建议的设置。</span><span class="sxs-lookup"><span data-stu-id="946b0-135">This setting is also the recommended setting.</span></span> <span data-ttu-id="946b0-136">当使用**匹配任何搜索词**设置时，完全或部分匹配一个或多个搜索词的所有产品返回为结果，且结果自动按（完全或部分）匹配最多关键字的产品开始进行升序排序。</span><span class="sxs-lookup"><span data-stu-id="946b0-136">When the **Match any search term** setting is used, all products that fully or partially match one or more search terms are returned as results, and the results are automatically sorted in ascending order of products that have the most keyword matches (full or partial).</span></span>

    <span data-ttu-id="946b0-137">**匹配所有搜索词**设置仅返回（完全或部分）匹配所有搜索词的产品。</span><span class="sxs-lookup"><span data-stu-id="946b0-137">The **Match all search terms** setting returns only products that match all the search terms (full or partial).</span></span> <span data-ttu-id="946b0-138">当产品名称较长，且员工只想查看搜索结果中的有限产品时，此设置有用。</span><span class="sxs-lookup"><span data-stu-id="946b0-138">This setting is helpful when the product names are lengthy, and employees want to see only limited products in the search results.</span></span> <span data-ttu-id="946b0-139">但是，该搜索类型有两个限制：</span><span class="sxs-lookup"><span data-stu-id="946b0-139">However, this type of search has two limitations:</span></span>

    - <span data-ttu-id="946b0-140">对单独的产品属性进行搜索。</span><span class="sxs-lookup"><span data-stu-id="946b0-140">The search is done on individual product properties.</span></span> <span data-ttu-id="946b0-141">例如，仅返回在至少一个产品属性中具有所有搜索关键字的产品。</span><span class="sxs-lookup"><span data-stu-id="946b0-141">For example, only products that have all the searched keywords in at least one product property are returned.</span></span>
    - <span data-ttu-id="946b0-142">不搜索维度。</span><span class="sxs-lookup"><span data-stu-id="946b0-142">Dimensions aren't searched.</span></span>

- <span data-ttu-id="946b0-143">零售商现在可以将产品搜索配置为当用户键入产品名称时显示搜索建议。</span><span class="sxs-lookup"><span data-stu-id="946b0-143">Retailers can now configure product search to show search suggestions as users type product names.</span></span> <span data-ttu-id="946b0-144">此功能的新设置在 POS 功能配置文件中命名为**产品搜索**的组中可用。</span><span class="sxs-lookup"><span data-stu-id="946b0-144">A new setting for this functionality is available in the POS functionality profile, under a group that is named **Product search**.</span></span> <span data-ttu-id="946b0-145">设置命名为**在键入时显示搜索建议**。</span><span class="sxs-lookup"><span data-stu-id="946b0-145">The setting is named **Show search suggestions while typing**.</span></span> <span data-ttu-id="946b0-146">此功能使员工无需手动键入全部名称，因此可以帮助员工快速查找其搜索的产品。</span><span class="sxs-lookup"><span data-stu-id="946b0-146">This functionality can help employees quickly find the product that they are searching for, because they don't have to type the whole name manually.</span></span>
- <span data-ttu-id="946b0-147">产品搜索算法现在可以搜索在产品的**搜索名称**属性中搜索的词语。</span><span class="sxs-lookup"><span data-stu-id="946b0-147">The product search algorithm now also searches for the searched terms in the **Search name** property of the product.</span></span>

<span data-ttu-id="946b0-148">![产品建议](./media/Productsuggestions.png "产品建议")</span><span class="sxs-lookup"><span data-stu-id="946b0-148">![Product suggestions](./media/Productsuggestions.png "Product suggestions")</span></span>

## <a name="customer-search"></a><span data-ttu-id="946b0-149">客户搜索</span><span class="sxs-lookup"><span data-stu-id="946b0-149">Customer search</span></span>

<span data-ttu-id="946b0-150">客户搜索用于根据不同目的查找客户。</span><span class="sxs-lookup"><span data-stu-id="946b0-150">Customer search is used to find customers for various purposes.</span></span> <span data-ttu-id="946b0-151">例如，出纳可能想要查看客户的愿望列表或购买历史记录，或将客户添加到交易记录。</span><span class="sxs-lookup"><span data-stu-id="946b0-151">For example, cashiers might want to view a customer's wish list or purchase history, or add the customer to a transaction.</span></span> <span data-ttu-id="946b0-152">在多个关键字搜索的情况下，客户搜索算法返回与任何搜索的关键字匹配的所有客户。</span><span class="sxs-lookup"><span data-stu-id="946b0-152">In the case of multiple-keyword searches, the customer search algorithm returns all customers that match any of the searched keywords.</span></span> <span data-ttu-id="946b0-153">但是，匹配最多关键字的客户显示在结果的顶部。</span><span class="sxs-lookup"><span data-stu-id="946b0-153">However, the customers that match the most keywords appear at the top of the results.</span></span> <span data-ttu-id="946b0-154">此行为与其他搜索引擎显示结果的方式类似。</span><span class="sxs-lookup"><span data-stu-id="946b0-154">This behavior is analogous to the way that other search engines show results.</span></span> <span data-ttu-id="946b0-155">先显示匹配最多搜索词的结果，然后显示部分匹配搜索关键字的结果。</span><span class="sxs-lookup"><span data-stu-id="946b0-155">They first show the results that match the most searched terms, and then they show the results that partially match the search keywords.</span></span> <span data-ttu-id="946b0-156">出现出纳使用多个关键字进行搜索，但其中一个关键字拼写错误的情况下，此行为有用。</span><span class="sxs-lookup"><span data-stu-id="946b0-156">This behavior helps cashiers in situations where they are using multiple keywords for their search, but one of the keywords has a spelling mistake.</span></span>

<span data-ttu-id="946b0-157">默认情况下，客户搜索在与商店关联的客户通讯簿中执行。</span><span class="sxs-lookup"><span data-stu-id="946b0-157">By default, a customer search is done on the customer address books that are associated with the store.</span></span> <span data-ttu-id="946b0-158">此类搜索被称为*本地客户搜索*。</span><span class="sxs-lookup"><span data-stu-id="946b0-158">This type of search is known as a *local customer search*.</span></span> <span data-ttu-id="946b0-159">但是，员工也可以搜索全局客户。</span><span class="sxs-lookup"><span data-stu-id="946b0-159">However, employees can also search for customers globally.</span></span> <span data-ttu-id="946b0-160">换而言之，他们可以跨公司及所有其他法人的商店进行搜索。</span><span class="sxs-lookup"><span data-stu-id="946b0-160">In other words, they can search across the stores of the company and across all other legal entities.</span></span> <span data-ttu-id="946b0-161">此类搜索被称为*远程客户搜索*。</span><span class="sxs-lookup"><span data-stu-id="946b0-161">This type of search is known as a *remote customer search*.</span></span>

<span data-ttu-id="946b0-162">要执行全局搜索，员工可以选择页面底部的**筛选结果**按钮，然后选择**搜索所有商店**选项，如下图中所示。</span><span class="sxs-lookup"><span data-stu-id="946b0-162">To search globally, employees can select the **Filter results** button at the bottom of the page and then select the **Search all stores** option, as shown in the illustration that follows.</span></span> <span data-ttu-id="946b0-163">在这种情况下，不止返回客户。</span><span class="sxs-lookup"><span data-stu-id="946b0-163">In this case, not only customers are returned.</span></span> <span data-ttu-id="946b0-164">也返回属于总部中的任何通讯簿的所有类型的相关方。</span><span class="sxs-lookup"><span data-stu-id="946b0-164">All types of parties that are part of any address book in the headquarters are also returned.</span></span> <span data-ttu-id="946b0-165">这些相关方包括工作人员、供应商、联系人和竞争对手。</span><span class="sxs-lookup"><span data-stu-id="946b0-165">These parties include workers, vendors, contacts, and competitors.</span></span>

> [!NOTE]
> <span data-ttu-id="946b0-166">远程客户搜索中必须输入至少四个字符才能返回结果。</span><span class="sxs-lookup"><span data-stu-id="946b0-166">A minimum of four characters must be entered for a remote customer search to return results.</span></span>

<span data-ttu-id="946b0-167">在远程客户搜索中，不显示来自其他法人的客户的客户 ID，因为没有在当前公司为这些相关方创建客户 ID。</span><span class="sxs-lookup"><span data-stu-id="946b0-167">In a remote customer search, the customer ID isn't shown for customers from the other legal entities, because no customer ID has been created for those parties in the current company.</span></span> <span data-ttu-id="946b0-168">但是，如果员工打开客户详细信息页，系统将自动为相关方生成一个客户 ID，且将商店的客户通讯簿与该客户相关联。</span><span class="sxs-lookup"><span data-stu-id="946b0-168">However, if an employee opens the customer details page, the system automatically generates a customer ID for the party and also associates the store's customer address books with the customer.</span></span> <span data-ttu-id="946b0-169">因此，该客户将在以后执行的本地商店搜索中可见。</span><span class="sxs-lookup"><span data-stu-id="946b0-169">Therefore, the customer will be visible in local store searches that are done later.</span></span>

<span data-ttu-id="946b0-170">![全局客户搜索](./media/Globalcustomersearch.png "全局客户搜索")</span><span class="sxs-lookup"><span data-stu-id="946b0-170">![Global customer search](./media/Globalcustomersearch.png "Global customer search")</span></span>

### <a name="enhancements-to-local-customer-searches"></a><span data-ttu-id="946b0-171">本地客户搜索增强功能</span><span class="sxs-lookup"><span data-stu-id="946b0-171">Enhancements to local customer searches</span></span>

<span data-ttu-id="946b0-172">本地客户搜索有助于员工根据电话号码快速查找客户。</span><span class="sxs-lookup"><span data-stu-id="946b0-172">Local customer searches help employees quickly find customers by phone number.</span></span> <span data-ttu-id="946b0-173">员工无需键入添加到客户电话号码中的任何特殊字符，如空格、连字符或括号。</span><span class="sxs-lookup"><span data-stu-id="946b0-173">Employees don't have to type any special characters that have been added to a customer's phone number, such as spaces, hyphens, or brackets.</span></span> <span data-ttu-id="946b0-174">尽管出纳可以使用任何格式存储电话号码（如，可以包括括号、连字符、符号等），但他们可以通过键入部分电话号码来搜索客户。</span><span class="sxs-lookup"><span data-stu-id="946b0-174">Although cashiers can store phone numbers in any format (for example, they can include brackets, hyphens, symbols, and so on), they can search for customers by typing a partial phone number.</span></span> <span data-ttu-id="946b0-175">如果出纳在输入电话号码时包括特殊字符，则其他出纳可以通过键入在特殊字符后面显示的数字来查找客户。</span><span class="sxs-lookup"><span data-stu-id="946b0-175">If a cashier included special characters when he or she entered a phone number, other cashiers can find the customer by typing the numbers that appear after the special characters.</span></span> <span data-ttu-id="946b0-176">例如，如果输入的客户电话号码为 **1123-456-7890**，则出纳可以通过键入 **123**、**456**、**7890** 或 **51234567890** 来搜索客户，也可以通过部分输入电话号码的前几个数字来搜索客户。</span><span class="sxs-lookup"><span data-stu-id="946b0-176">For example, if a customer's phone number was entered as **123-456-7890**, a cashier can search for the customer by typing **123**, **456**, **7890**, or **1234567890**, or by partially entering the first few numbers of the phone number.</span></span>

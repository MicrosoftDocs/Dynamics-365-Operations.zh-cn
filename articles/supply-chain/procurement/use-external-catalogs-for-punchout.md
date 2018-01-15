---
title: "针对电子采购发包使用外部目录"
description: "本主题说明如何使用外部目录创建和提交申请。"
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 577204b49355a470769237eb46ad74e7f319a55e
ms.openlocfilehash: a81382e19a0d9446a419402d8fa8a00ca66c3378
ms.contentlocale: zh-cn
ms.lasthandoff: 01/15/2018

---

# <a name="use-external-catalogs-for-punchout-eprocurement"></a><span data-ttu-id="ab937-103">针对电子采购发包使用外部目录</span><span class="sxs-lookup"><span data-stu-id="ab937-103">Use external catalogs for PunchOut eProcurement</span></span>
<span data-ttu-id="ab937-104">通过针对电子采购发包使用外部目录，您不必再在自己的主数据中维护与您的供应商的产品有关的信息。</span><span class="sxs-lookup"><span data-stu-id="ab937-104">By using external catalogs for PunchOut e-procurement, you don't have to maintain information about your vendors' products in your own master data.</span></span> <span data-ttu-id="ab937-105">相反，供应商网站上的购物车将转换为具有正确产品信息的申请行。</span><span class="sxs-lookup"><span data-stu-id="ab937-105">Instead, the shopping cart on a vendor's website is converted to requisition lines that have the correct product information.</span></span> 

<span data-ttu-id="ab937-106">您应该避免在您自己的产品主数据中维护供应商产品的描述和价格。</span><span class="sxs-lookup"><span data-stu-id="ab937-106">You should avoid maintaining the descriptions and prices of your vendors’ products in your own product master data.</span></span> <span data-ttu-id="ab937-107">相反，应针对电子采购发包使用外部目录。</span><span class="sxs-lookup"><span data-stu-id="ab937-107">Instead, use external catalogs for PunchOut e-procurement.</span></span> <span data-ttu-id="ab937-108">之后当员工创建申请时，他们可以“发包”到供应商的外部目录站点（换言之，他们离开您的系统，前往供应商站点）。</span><span class="sxs-lookup"><span data-stu-id="ab937-108">Then, when employees create requisitions, they can “punch out” to a vendor’s external catalog site (in other words, they leave your system and go to the vendor’s site).</span></span> <span data-ttu-id="ab937-109">在供应商的网站上添加到购物车的产品随后可以转换为申请行。</span><span class="sxs-lookup"><span data-stu-id="ab937-109">The products that are added to the shopping cart on the vendor’s website can then be converted to requisition lines.</span></span> <span data-ttu-id="ab937-110">因此，您将获得正确的产品信息：产品 ID、名称、价格等。</span><span class="sxs-lookup"><span data-stu-id="ab937-110">Therefore, you get the correct product information: product ID, name, price, and so on.</span></span>

<span data-ttu-id="ab937-111">若要使用外部目录，员工必须创建在**我的采购申请**页创建申请。</span><span class="sxs-lookup"><span data-stu-id="ab937-111">To use external catalogs, an employee must create a requisition on the **My purchase requisitions** page.</span></span>

<span data-ttu-id="ab937-112">创建申请的员工被称为申请准备人。</span><span class="sxs-lookup"><span data-stu-id="ab937-112">The employee who creates a requisition is referred to as the preparer of the requisition.</span></span> <span data-ttu-id="ab937-113">作为准备人，您可以完成以下任务。</span><span class="sxs-lookup"><span data-stu-id="ab937-113">As a preparer, you can complete the following tasks.</span></span>

<span data-ttu-id="ab937-114">使用**外部目录**行操作打开一个页面，该页面包含对指定申请者、购买法人和接收运营单位可用的所有外部目录。</span><span class="sxs-lookup"><span data-stu-id="ab937-114">Use the **External catalogs** line action to open a page that includes all external catalogs that are available for the specified requester, buying legal entity, and receiving operating unit.</span></span>

<span data-ttu-id="ab937-115">根据您的权限，更改申请者、购买法人和接收运营单位。</span><span class="sxs-lookup"><span data-stu-id="ab937-115">Depending on your permissions, change the requester, buying legal entity, and receiving operating unit.</span></span> <span data-ttu-id="ab937-116">更改这些值可能会更改对申请者可用的外部目录的列表。</span><span class="sxs-lookup"><span data-stu-id="ab937-116">A change in those values might change the list of external catalogs that are available to a requester.</span></span> <span data-ttu-id="ab937-117">可用的外部目录取决于购买法人或接收运营单位的当前有效的采购策略。</span><span class="sxs-lookup"><span data-stu-id="ab937-117">The external catalogs that are available depend on the current active purchasing policies for the buying legal entity or the receiving operating unit.</span></span> <span data-ttu-id="ab937-118">这些策略可以允许或阻止访问特定采购类别。</span><span class="sxs-lookup"><span data-stu-id="ab937-118">These policies can allow or prevent access to specific procurement categories.</span></span> <span data-ttu-id="ab937-119">因此，映射到这些采购类别的外部目录的列表可能受到影响。</span><span class="sxs-lookup"><span data-stu-id="ab937-119">Therefore, the list of external catalogs that are mapped to these procurement categories can be affected.</span></span>

<span data-ttu-id="ab937-120">有关策略的详细信息，请参阅 [采购策略](../procurement/purchase-policies.md)。</span><span class="sxs-lookup"><span data-stu-id="ab937-120">For more information about policies, see [Purchasing policies](../procurement/purchase-policies.md).</span></span>

- <span data-ttu-id="ab937-121">若要查找特定采购类别的外部目录，请在目录搜索字段输入文本。</span><span class="sxs-lookup"><span data-stu-id="ab937-121">To find external catalogs for specific procurement categories, enter text in the catalog search field.</span></span>
- <span data-ttu-id="ab937-122">若要添加来自供应商网站上的供应商外部目录的产品，请单击外部目录。</span><span class="sxs-lookup"><span data-stu-id="ab937-122">To add products from a vendor’s external catalog on the vendor’s website, click the external catalog.</span></span> <span data-ttu-id="ab937-123">然后将产品添加到购物车，再签出。购物车行将转移到 Microsoft Dynamics 365。</span><span class="sxs-lookup"><span data-stu-id="ab937-123">Then add products to the shopping cart, and check out. The shopping cart lines will be transferred to Microsoft Dynamics 365.</span></span>

<span data-ttu-id="ab937-124">如果有多个采购类别选项，在您将行添加到申请前，请选择正确的采购类别。</span><span class="sxs-lookup"><span data-stu-id="ab937-124">If there are multiple options for procurement categories, select the correct procurement category before you add the lines to the requisition.</span></span>
<span data-ttu-id="ab937-125">将行添加到申请后，不使用外部目录也可以添加更多行。</span><span class="sxs-lookup"><span data-stu-id="ab937-125">After lines have been added to a requisition, you can add more lines without using external catalogs.</span></span> <span data-ttu-id="ab937-126">或者，您可以继续使用外部目录添加行。</span><span class="sxs-lookup"><span data-stu-id="ab937-126">Alternatively, you can continue to use external catalogs to add lines.</span></span>

<span data-ttu-id="ab937-127">申请准备就绪后，使用**工作流** > **提交**操作进行提交以供审核。</span><span class="sxs-lookup"><span data-stu-id="ab937-127">When the requisition is ready, use the **Workflow** > **Submit** action to submit it for approval.</span></span>


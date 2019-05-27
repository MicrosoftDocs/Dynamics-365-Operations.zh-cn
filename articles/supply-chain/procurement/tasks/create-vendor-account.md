---
title: 创建供应商帐户
description: 该过程会显示如何创建供应商帐户，以及添加地址和联系信息。
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddressGrid, DirPartyLookup, LogisticsPostalAddress, SysLookupMultiSelectGrid
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 22c7a1a2b7468f00aa25a67a2c5f62b088e2fe7c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546171"
---
# <a name="create-a-vendor-account"></a><span data-ttu-id="d3590-103">创建供应商帐户</span><span class="sxs-lookup"><span data-stu-id="d3590-103">Create a vendor account</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d3590-104">该过程会显示如何创建供应商帐户，以及添加地址和联系信息。</span><span class="sxs-lookup"><span data-stu-id="d3590-104">This procedure shows how to create a vendor account, and add an address and contact information.</span></span> <span data-ttu-id="d3590-105">该过程不会显示如何填充所有字段，以用于采购和财务目的。</span><span class="sxs-lookup"><span data-stu-id="d3590-105">The procedure does not show how to populate all fields for purchasing and financial purposes.</span></span> <span data-ttu-id="d3590-106">若要了解关于这些字段的更多信息，请阅读字段描述。</span><span class="sxs-lookup"><span data-stu-id="d3590-106">To learn more about those fields, please read the field descriptions.</span></span> <span data-ttu-id="d3590-107">您可以使用演示数据公司 USMF，也可使用您自己的数据运行该过程。</span><span class="sxs-lookup"><span data-stu-id="d3590-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="d3590-108">供应商帐户通常由采购专业人员或应收账款人员创建。</span><span class="sxs-lookup"><span data-stu-id="d3590-108">Vendor accounts are typically created by a procurement professional or accounts receivable personnel.</span></span>


## <a name="create-a-vendor-account"></a><span data-ttu-id="d3590-109">创建供应商帐户</span><span class="sxs-lookup"><span data-stu-id="d3590-109">Create a vendor account</span></span>
1. <span data-ttu-id="d3590-110">转到“采购”>“供应商”>“所有供应商”。</span><span class="sxs-lookup"><span data-stu-id="d3590-110">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="d3590-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="d3590-111">Click New.</span></span>
3. <span data-ttu-id="d3590-112">在“供应商帐户”字段中，输入一个供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="d3590-112">In the Vendor account field, type a value.</span></span>
    * <span data-ttu-id="d3590-113">值可以自动填充。</span><span class="sxs-lookup"><span data-stu-id="d3590-113">The value may be populated automatically.</span></span> <span data-ttu-id="d3590-114">如果是这样，您可以跳过此步骤。</span><span class="sxs-lookup"><span data-stu-id="d3590-114">If so, you can skip this step.</span></span>  
    * <span data-ttu-id="d3590-115">您可以为某个人或组织创建供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="d3590-115">You can create vendor accounts for a person or organization.</span></span> <span data-ttu-id="d3590-116">这将影响到哪些字段可用。</span><span class="sxs-lookup"><span data-stu-id="d3590-116">This will affect which fields are available.</span></span> <span data-ttu-id="d3590-117">在此示例中，我们将为一个组织创建供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="d3590-117">In this example, we’ll create a vendor account for an organization.</span></span>   
4. <span data-ttu-id="d3590-118">在“名称”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="d3590-118">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="d3590-119">如果您的供应商在您的系统中是已登记的当事方，您可以使用下拉功能，在此字段中选择他们，并且新的供应商帐户将会继承已登记的地址和联系信息。</span><span class="sxs-lookup"><span data-stu-id="d3590-119">If your vendor is an already a registered party in your system you can use drop down and select them in this field and the new vendor account will inherit the address and contact information that’s already registered.</span></span>  
5. <span data-ttu-id="d3590-120">在“组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="d3590-120">In the Group field, enter or select a value.</span></span>
    * <span data-ttu-id="d3590-121">供应商组用于对具有以下任何共同参数的供应商进行分组：“付款条款”、结算期间、库存过帐会计科目（包括销售税组）、默认会计科目、产品筛选器代码或供应预测配置。</span><span class="sxs-lookup"><span data-stu-id="d3590-121">The vendor group is used to group vendors that have any of the following parameters in common: Terms of payment , settle period,  inventory posting ledger accounts – including the sales tax group, default ledger accounts, product filter codes, or supply forecast configuration.</span></span>  
6. <span data-ttu-id="d3590-122">在“员工数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="d3590-122">In the Number of employees field, enter a number.</span></span>
7. <span data-ttu-id="d3590-123">在“组织数量”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d3590-123">In the Organization number field, type a value.</span></span>

## <a name="add-an-address"></a><span data-ttu-id="d3590-124">添加地址</span><span class="sxs-lookup"><span data-stu-id="d3590-124">Add an address</span></span>
1. <span data-ttu-id="d3590-125">展开“地址”部分。</span><span class="sxs-lookup"><span data-stu-id="d3590-125">Expand the Addresses section.</span></span>
2. <span data-ttu-id="d3590-126">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="d3590-126">Click Add.</span></span>
3. <span data-ttu-id="d3590-127">在“用途”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="d3590-127">In the Purpose field, enter or select a value.</span></span>
    * <span data-ttu-id="d3590-128">您可以选择一个或多个用途。</span><span class="sxs-lookup"><span data-stu-id="d3590-128">You can select one or more purposes.</span></span> <span data-ttu-id="d3590-129">这些用于为指定用途选择正确的地址。</span><span class="sxs-lookup"><span data-stu-id="d3590-129">These are used to select the correct address for a given purpose.</span></span> <span data-ttu-id="d3590-130">例如，如果用途是“发票”，则在您发送发票时将使用该地址。</span><span class="sxs-lookup"><span data-stu-id="d3590-130">For example, if the purpose is “Invoice” that address will be used when you send invoices.</span></span>  
4. <span data-ttu-id="d3590-131">在“名称”或“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d3590-131">In the Name or description field, type a value.</span></span>
5. <span data-ttu-id="d3590-132">在“国家/地区”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="d3590-132">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="d3590-133">输入地址详情。</span><span class="sxs-lookup"><span data-stu-id="d3590-133">Enter the address details.</span></span> <span data-ttu-id="d3590-134">您选定的国家/地区将确定您使用与该国家/地区对应的地址格式显示的字段。</span><span class="sxs-lookup"><span data-stu-id="d3590-134">The country/region that you selected will determine the fields you are presented with, corresponding to the address format for the country/region.</span></span>   
6. <span data-ttu-id="d3590-135">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d3590-135">Click OK.</span></span>

## <a name="add-contact-information"></a><span data-ttu-id="d3590-136">添加联系信息</span><span class="sxs-lookup"><span data-stu-id="d3590-136">Add contact information</span></span>
1. <span data-ttu-id="d3590-137">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="d3590-137">Click Add.</span></span>
2. <span data-ttu-id="d3590-138">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d3590-138">In the Description field, type a value.</span></span>
3. <span data-ttu-id="d3590-139">在“类型”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="d3590-139">In the Type field, select an option.</span></span>
4. <span data-ttu-id="d3590-140">在“联系电话/地址”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d3590-140">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="d3590-141">如果这是主要联系人，您可以选中“主要”复选框。</span><span class="sxs-lookup"><span data-stu-id="d3590-141">You can select the Primary check box if this is the primary contact.</span></span>  
5. <span data-ttu-id="d3590-142">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="d3590-142">Click Save.</span></span>
6. <span data-ttu-id="d3590-143">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d3590-143">Close the page.</span></span>
7. <span data-ttu-id="d3590-144">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d3590-144">Close the page.</span></span>


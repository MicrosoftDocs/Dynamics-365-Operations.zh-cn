---
title: 设置供应商发票策略
description: 本主题说明如何设置供应商发票策略。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 678ef8f0b7df00aec615af26cbcadec984331060
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220051"
---
# <a name="set-up-vendor-invoice-policies"></a><span data-ttu-id="d1892-103">设置供应商发票策略</span><span class="sxs-lookup"><span data-stu-id="d1892-103">Set up vendor invoice policies</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d1892-104">本主题说明如何设置供应商发票策略。</span><span class="sxs-lookup"><span data-stu-id="d1892-104">This topic explains how to set up vendor invoice policies.</span></span> <span data-ttu-id="d1892-105">在您通过使用供应商发票页面过帐供应商发票，以及打开供应商发票政策违规页面时，将运行供应商发票政策。</span><span class="sxs-lookup"><span data-stu-id="d1892-105">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="d1892-106">您还可以配置供应商发票工作流每次运行供应商发票策略发票您提交到工作流。</span><span class="sxs-lookup"><span data-stu-id="d1892-106">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

- <span data-ttu-id="d1892-107">供应商发票此策略不适用于在发票登记簿或发票日志中创建的发票。</span><span class="sxs-lookup"><span data-stu-id="d1892-107">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span>  
- <span data-ttu-id="d1892-108">发票匹配验证并不使用供应商发票政策，但是，需在应付帐款参数页面进行设置。</span><span class="sxs-lookup"><span data-stu-id="d1892-108">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>  
- <span data-ttu-id="d1892-109">此记录使用 USMF 公司演示。</span><span class="sxs-lookup"><span data-stu-id="d1892-109">This recording uses the USMF demo company.</span></span> <span data-ttu-id="d1892-110">应付帐款经理或会计经理将执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="d1892-110">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="d1892-111">在您开始前，请确保选择发票匹配 Configuration Key。</span><span class="sxs-lookup"><span data-stu-id="d1892-111">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="d1892-112">准备为供应商发票策略</span><span class="sxs-lookup"><span data-stu-id="d1892-112">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="d1892-113">转到 **导航窗格 > 应付帐款 > 设置 > 应付帐款参数**。</span><span class="sxs-lookup"><span data-stu-id="d1892-113">Go to **Navigation pane > Modules > Accounts payable > Setup > Accounts payable parameters**.</span></span>
2. <span data-ttu-id="d1892-114">选择 **发票验证** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="d1892-114">Select the **Invoice validation** tab.</span></span>
3. <span data-ttu-id="d1892-115">选中或清除 **自动更新发票抬头状态** 复选框。</span><span class="sxs-lookup"><span data-stu-id="d1892-115">Select or clear the **Automatically update invoice header** status check box.</span></span>
4. <span data-ttu-id="d1892-116">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="d1892-116">Select **OK**.</span></span>
5. <span data-ttu-id="d1892-117">在 **过帐发票差异** 字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="d1892-117">In the **Post invoice with discrepancies** field, select an option.</span></span>
6. <span data-ttu-id="d1892-118">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d1892-118">Close the page.</span></span>
7. <span data-ttu-id="d1892-119">找到 **导航窗格 > 模块 > 应付帐款 > 策略设置 > 供应商发票策略**。</span><span class="sxs-lookup"><span data-stu-id="d1892-119">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
8. <span data-ttu-id="d1892-120">选择 **参数**。</span><span class="sxs-lookup"><span data-stu-id="d1892-120">Select **Parameters**.</span></span>
9. <span data-ttu-id="d1892-121">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="d1892-121">Select **Add**.</span></span>
10. <span data-ttu-id="d1892-122">关闭此页面将返回到主页。</span><span class="sxs-lookup"><span data-stu-id="d1892-122">Close the page to return to the home page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="d1892-123">创建或更新供应商发票政策规则类型</span><span class="sxs-lookup"><span data-stu-id="d1892-123">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="d1892-124">找到 **导航窗格 > 模块 > 应付帐款 > 策略设置 > 供应商发票策略规则类型**。</span><span class="sxs-lookup"><span data-stu-id="d1892-124">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policy rule types**.</span></span>
2. <span data-ttu-id="d1892-125">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="d1892-125">Select **New**.</span></span>
3. <span data-ttu-id="d1892-126">在 **规则名称** 和 **说明** 字段中输入值。</span><span class="sxs-lookup"><span data-stu-id="d1892-126">In the **Rule name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="d1892-127">在 **查询名称** 字段中，选择下拉按钮以打开查找，然后选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="d1892-127">In the **Query name** field, select the drop-down button to open the lookup, then select the desired record.</span></span>
5. <span data-ttu-id="d1892-128">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="d1892-128">Select **Save**.</span></span>
6. <span data-ttu-id="d1892-129">关闭此页面将返回到主页。</span><span class="sxs-lookup"><span data-stu-id="d1892-129">Close the page to return to the home page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="d1892-130">定义一个供应商发票策略</span><span class="sxs-lookup"><span data-stu-id="d1892-130">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="d1892-131">找到 **导航窗格 > 模块 > 应付帐款 > 策略设置 > 供应商发票策略**。</span><span class="sxs-lookup"><span data-stu-id="d1892-131">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
2. <span data-ttu-id="d1892-132">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="d1892-132">Select **New**.</span></span>
3. <span data-ttu-id="d1892-133">在 **名称** 和 **说明** 字段中输入值。</span><span class="sxs-lookup"><span data-stu-id="d1892-133">In the **Name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="d1892-134">展开或折叠 **策略组织** 部分。</span><span class="sxs-lookup"><span data-stu-id="d1892-134">Expand or collapse the **Policy organizations** section.</span></span>
5. <span data-ttu-id="d1892-135">在树结构中，选择 **美国 Contoso 娱乐系统**。</span><span class="sxs-lookup"><span data-stu-id="d1892-135">In the tree, select **Contoso Entertainment System USA**.</span></span>
6. <span data-ttu-id="d1892-136">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="d1892-136">Select **Add**.</span></span>
7. <span data-ttu-id="d1892-137">展开或折叠 **策略规则** 部分。</span><span class="sxs-lookup"><span data-stu-id="d1892-137">Expand or collapse the **Policy rules** section.</span></span>
8. <span data-ttu-id="d1892-138">选择 **创建策略规则**。</span><span class="sxs-lookup"><span data-stu-id="d1892-138">Select **Create policy rule**.</span></span>
9. <span data-ttu-id="d1892-139">在 **策略规则描述** 字段中，输入一项描述。</span><span class="sxs-lookup"><span data-stu-id="d1892-139">In the **Policy rule description** field, type a value.</span></span>
10. <span data-ttu-id="d1892-140">选择 **筛选器**。</span><span class="sxs-lookup"><span data-stu-id="d1892-140">Select **Filter**.</span></span>
11. <span data-ttu-id="d1892-141">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="d1892-141">Select **Add**.</span></span> <span data-ttu-id="d1892-142">选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="d1892-142">Select the desired record.</span></span>
12. <span data-ttu-id="d1892-143">在 **表**、**派生表** 和 **字段** 字段中，从下拉菜单选择选项或输入选项。</span><span class="sxs-lookup"><span data-stu-id="d1892-143">In the **Table**, **Derived table**, and **Field** fields, select or enter options from the drop-down menus.</span></span>
13. <span data-ttu-id="d1892-144">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d1892-144">Close the page.</span></span>
14. <span data-ttu-id="d1892-145">在 **条件** 字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="d1892-145">In the **Criteria** field, type a value.</span></span>
15. <span data-ttu-id="d1892-146">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="d1892-146">Select **OK**.</span></span>
16. <span data-ttu-id="d1892-147">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="d1892-147">Select **OK**.</span></span>
17. <span data-ttu-id="d1892-148">关闭页面将返回到主页。</span><span class="sxs-lookup"><span data-stu-id="d1892-148">Close the pages to return to the home page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: "预算计划理由文档"
description: "理由文档让请求预算的人员可以说明为何必须获得特定预算。"
author: ryansandness
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanJustificationTemplate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: cae6334cd39a91eaf3a2a79f30edc705f484bc8c
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---

# <a name="budget-planning-justification-documents"></a><span data-ttu-id="7d94e-103">预算计划理由文档</span><span class="sxs-lookup"><span data-stu-id="7d94e-103">Budget planning justification documents</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d94e-104">理由文档让请求预算的人员可以说明为何必须获得特定预算。</span><span class="sxs-lookup"><span data-stu-id="7d94e-104">Justification documents provide a narrative for those requesting a budget to explain why a specific budget is necessary.</span></span> 

<span data-ttu-id="7d94e-105">预算计划模板由预算经理在 Microsoft Word 中创建，并分配给当前预算计划流程。</span><span class="sxs-lookup"><span data-stu-id="7d94e-105">A budget plan template is created by the budget manager in Microsoft Word and assigned to the current budget planning process.</span></span> <span data-ttu-id="7d94e-106">然后，预算所有者可以打开该模板，并根据预算请求在 Word 中自动填充数据。</span><span class="sxs-lookup"><span data-stu-id="7d94e-106">Budget owners can then open the template and have data automatically populated in Word based on their budget request.</span></span> <span data-ttu-id="7d94e-107">保存个性化理由文档并附加到预算计划之前，可以添加更多文本或数据。</span><span class="sxs-lookup"><span data-stu-id="7d94e-107">They can then add additional text or data prior to saving and attaching their personalized justification document to their budget plan.</span></span>

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a><span data-ttu-id="7d94e-108">设置 Microsoft Dynamics Office Add-in for Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="7d94e-108">Set up Microsoft Dynamics Office Add-in for Microsoft Word</span></span>

1.  <span data-ttu-id="7d94e-109">打开一个新的 Microsoft Word 文档。</span><span class="sxs-lookup"><span data-stu-id="7d94e-109">Open a new Microsoft Word document.</span></span>
2.  <span data-ttu-id="7d94e-110">单击功能区中的**插入**，然后单击**应用商店**。</span><span class="sxs-lookup"><span data-stu-id="7d94e-110">Click **Insert** on the ribbon, and click **Store**.</span></span>
3.  <span data-ttu-id="7d94e-111">搜索 Microsoft Dynamics Office Add-in，然后单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="7d94e-111">Search for Microsoft Dynamics Office Add-in and click **Add**.</span></span>
4.  <span data-ttu-id="7d94e-112">在 Word 的右窗格中，单击**添加服务器信息**。</span><span class="sxs-lookup"><span data-stu-id="7d94e-112">In Word, in the right pane, click **Add server information**.</span></span>
5.  <span data-ttu-id="7d94e-113">输入或粘贴服务器 URL，然后单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="7d94e-113">Type or paste the server URL and click **OK**.</span></span>

##### <a name="define-the-justification-template-in-microsoft-word"></a><span data-ttu-id="7d94e-114">在 Microsoft Word 中定义理由模板</span><span class="sxs-lookup"><span data-stu-id="7d94e-114">Define the Justification template in Microsoft Word</span></span>

1.  <span data-ttu-id="7d94e-115">登录后，单击 Microsoft Dynamics Office Add-in 中的**设计**。</span><span class="sxs-lookup"><span data-stu-id="7d94e-115">Click **Design** in the Microsoft Dynamics Office Add-in after you’ve logged in.</span></span>
2.  <span data-ttu-id="7d94e-116">对于标题信息，请使用**添加字段**按钮。</span><span class="sxs-lookup"><span data-stu-id="7d94e-116">For header information, use the **Add fields** button.</span></span>
3.  <span data-ttu-id="7d94e-117">选择实体数据源 BudgetPlanJustification，然后单击**下一步**。</span><span class="sxs-lookup"><span data-stu-id="7d94e-117">Select the entity data source of BudgetPlanJustification, and click **Next**.</span></span> <span data-ttu-id="7d94e-118">**注释：** 所有理由文档都需要此实体。</span><span class="sxs-lookup"><span data-stu-id="7d94e-118">**Note:** This entity is required for any justification document.</span></span> <span data-ttu-id="7d94e-119">可以使用其他实体，但是如果不包含此实体，上传回 Microsoft Dynamics 365 for Finance and Operations 将失败。</span><span class="sxs-lookup"><span data-stu-id="7d94e-119">Other entities can be used but the upload back to Microsoft Dynamics 365 for Finance and Operations will fail if this entity isn’t included.</span></span>
4.  <span data-ttu-id="7d94e-120">在 Word 文档中添加 BudgetPlanName、BudgetPlanPreparer、ResponsibilityCenter 和 DocumentNumber 标签和值。</span><span class="sxs-lookup"><span data-stu-id="7d94e-120">Add the BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter, and DocumentNumber labels and values in the Word document.</span></span> <span data-ttu-id="7d94e-121">**注释：** 如果需要，您可以使用之间的自定义标签，而不是标准标签。</span><span class="sxs-lookup"><span data-stu-id="7d94e-121">**Note:** You can use your own custom labels, rather than the standard labels, if needed.</span></span>
5.  <span data-ttu-id="7d94e-122">单击**完成**完成标题部分。</span><span class="sxs-lookup"><span data-stu-id="7d94e-122">Click **Done** to complete the header section.</span></span>
6.  <span data-ttu-id="7d94e-123">对于预算计划金额的行级别详细信息，请单击**添加表**。</span><span class="sxs-lookup"><span data-stu-id="7d94e-123">For line level detail of budget plan amounts, click **Add table**.</span></span>
7.  <span data-ttu-id="7d94e-124">再次选择实体数据源 BudgetPlanJustification，然后单击**下一步**。</span><span class="sxs-lookup"><span data-stu-id="7d94e-124">Again, select the entity data source of BudgetPlanJustification, and click **Next**.</span></span>
8.  <span data-ttu-id="7d94e-125">为 EffectiveDate、ScenarioName、AccountDisplayValue 和 AccountingCurrencyExpenseAmount 添加标签。</span><span class="sxs-lookup"><span data-stu-id="7d94e-125">Add fields for EffectiveDate, ScenarioName, AccountDisplayValue, and AccountingCurrencyExpenseAmount.</span></span> <span data-ttu-id="7d94e-126">**注释：** 如果可以在单个预算计划行内添加注释，可以在此处将其添加到表。</span><span class="sxs-lookup"><span data-stu-id="7d94e-126">**Note:** If comments are available to add within individual budget plan lines, those can be added to the table here.</span></span>
9.  <span data-ttu-id="7d94e-127">添加任何附加说明以提供给最终用户，并对文档执行任何必要的格式或样式设置。</span><span class="sxs-lookup"><span data-stu-id="7d94e-127">Add any additional instructions to provide to the end user, and perform any necessary formatting or styling to the document.</span></span>
10. <span data-ttu-id="7d94e-128">将该文档保持到您的本地计算机，然后在继续操作之前关闭该文件。</span><span class="sxs-lookup"><span data-stu-id="7d94e-128">Save the document to your local computer and close the file before continuing.</span></span>

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a><span data-ttu-id="7d94e-129">设置预算计划流程以使用理由模板</span><span class="sxs-lookup"><span data-stu-id="7d94e-129">Set up the Budget planning process to use the Justification template</span></span>

1.  <span data-ttu-id="7d94e-130">在 Finance and Operations 中，转至**预算编制** &gt; **设置** &gt; **预算计划** &gt; **理由文档模板**。</span><span class="sxs-lookup"><span data-stu-id="7d94e-130">In Finance and Operations, go to **Budgeting** &gt; **Setup** &gt; **Budget planning** &gt; **Justification document templates**.</span></span>
2.  <span data-ttu-id="7d94e-131">单击**新建**并浏览至新创建的 Microsoft Word 文档。</span><span class="sxs-lookup"><span data-stu-id="7d94e-131">Click **New** and browse to your newly created Microsoft Word document.</span></span>
3.  <span data-ttu-id="7d94e-132">输入模板显示名称和描述。</span><span class="sxs-lookup"><span data-stu-id="7d94e-132">Enter a template display name and description.</span></span> <span data-ttu-id="7d94e-133">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="7d94e-133">Click **OK**.</span></span>
4.  <span data-ttu-id="7d94e-134">转至**预算编制** &gt; **设置** &gt; **预算** **计划** &gt; **预算计划流程**。</span><span class="sxs-lookup"><span data-stu-id="7d94e-134">Go to **Budgeting** &gt; **Setup** &gt; **Budget** **planning** &gt; **Budget planning process**.</span></span>
5.  <span data-ttu-id="7d94e-135">选择应使用理由模板的流程，然后单击**编辑**。</span><span class="sxs-lookup"><span data-stu-id="7d94e-135">Select the process where the justification template should be used, and click **Edit**.</span></span>
6.  <span data-ttu-id="7d94e-136">在**理由文档模板**字段中，选择相应模板并保存。</span><span class="sxs-lookup"><span data-stu-id="7d94e-136">In the **Justification document template** field, select the appropriate template and save.</span></span>

##### <a name="edit-and-save-personalized-justification-documents"></a><span data-ttu-id="7d94e-137">编辑并保存个性化的理由文档</span><span class="sxs-lookup"><span data-stu-id="7d94e-137">Edit and save personalized justification documents</span></span>

1.  <span data-ttu-id="7d94e-138">在 Finance and Operations 中，新建预算计划或打开现有预算计划。</span><span class="sxs-lookup"><span data-stu-id="7d94e-138">In Finance and Operations, create a new budget plan or open an existing budget plan.</span></span>
2.  <span data-ttu-id="7d94e-139">在**理由**下拉菜单中，选择**创建新理由**。</span><span class="sxs-lookup"><span data-stu-id="7d94e-139">In the **Justification** drop-down menu, select **Create new justification**.</span></span>
3.  <span data-ttu-id="7d94e-140">填写详细信息之后，选择从**理由**下拉菜单上传个性化的文档。</span><span class="sxs-lookup"><span data-stu-id="7d94e-140">After filling in the details, select to upload the personalized document from the **Justification** drop-down menu.</span></span>






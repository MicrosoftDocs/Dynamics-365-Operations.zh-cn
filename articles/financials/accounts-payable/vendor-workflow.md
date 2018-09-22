---
title: "供应商工作流"
description: "修改供应商信息和使用工作流进行审核。"
author: mikefalkner
manager: annbe
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: Vendor
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: 950a1852acf9f3e4747ce2d55738c0eb3a646897
ms.contentlocale: zh-cn
ms.lasthandoff: 08/31/2018

---

# <a name="vendor-workflow"></a><span data-ttu-id="593e8-103">供应商工作流</span><span class="sxs-lookup"><span data-stu-id="593e8-103">Vendor workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="593e8-104">如果使用供应商工作流，将先把对特定字段进行的更改发送到工作流进行审核，之后才能将其添加到供应商。</span><span class="sxs-lookup"><span data-stu-id="593e8-104">When the vendor workflow is used, changes that are made to specific fields are sent to the workflow for approval before they are added to the vendor.</span></span>

## <a name="set-up-the-vendor-workflow"></a><span data-ttu-id="593e8-105">设置供应商工作流</span><span class="sxs-lookup"><span data-stu-id="593e8-105">Set up the vendor workflow</span></span>

<span data-ttu-id="593e8-106">此工作流功能必须经过启用才能使用。</span><span class="sxs-lookup"><span data-stu-id="593e8-106">Before you can use the workflow feature, you must enable it.</span></span>

1. <span data-ttu-id="593e8-107">转到**应付帐款 \>设置 \> 应付帐款参数**。</span><span class="sxs-lookup"><span data-stu-id="593e8-107">Go to **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
2. <span data-ttu-id="593e8-108">在**常规**选项卡的**供应商审核**快速选项卡上，将**启用供应商审核**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="593e8-108">On the **General** tab, on the **Vendor approval** FastTab, set the **Enable vendor approvals** option to **Yes**.</span></span>
3. <span data-ttu-id="593e8-109">在**数据实体行为**字段中，选择应在导入字段时使用的行为：</span><span class="sxs-lookup"><span data-stu-id="593e8-109">In the **Data entity behavior** field, select the behavior that should be used when data is imported:</span></span>

    - <span data-ttu-id="593e8-110">**允许在不审核的情况下进行更改** – 此数据实体可以在不通过工作流进行处理的情况下更新供应商记录。</span><span class="sxs-lookup"><span data-stu-id="593e8-110">**Allow changes without approval** – The data entity can update the vendor record without processing it through the workflow.</span></span>
    - <span data-ttu-id="593e8-111">**拒绝更改** – 不能对供应商记录进行更改。</span><span class="sxs-lookup"><span data-stu-id="593e8-111">**Reject changes** – Changes can't be made to the vendor record.</span></span> <span data-ttu-id="593e8-112">为工作流启用的字段的导入将失败。</span><span class="sxs-lookup"><span data-stu-id="593e8-112">The import will fail for the fields that are enabled for the workflow.</span></span>
    - <span data-ttu-id="593e8-113">**创建更改方案** – 将更改除为工作流启用的字段以外的所有字段。</span><span class="sxs-lookup"><span data-stu-id="593e8-113">**Create change proposals** – All fields will be changed except the fields that are enabled for the workflow.</span></span> <span data-ttu-id="593e8-114">将把这些字段的新值作为建议的更改添加到供应商，并自动启动工作流。</span><span class="sxs-lookup"><span data-stu-id="593e8-114">The new values for those fields will be added to the vendor as proposed changes, and the workflow will be started automatically.</span></span>

4. <span data-ttu-id="593e8-115">在供应商字段列表中，选中进行更改前必须先批准的每个字段的**启用**复选框。</span><span class="sxs-lookup"><span data-stu-id="593e8-115">In the list of vendor fields, select the **Enable** check box for every field that must be approved before the changes can be made.</span></span>
5. <span data-ttu-id="593e8-116">转到**应付帐款 \>设置 \> 应付帐款工作流**。</span><span class="sxs-lookup"><span data-stu-id="593e8-116">Go to **Accounts payable \> Setup \> Accounts payable workflows**.</span></span>
6. <span data-ttu-id="593e8-117">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="593e8-117">Select **New**.</span></span>
7. <span data-ttu-id="593e8-118">选择**建议的供应商更改工作流**。</span><span class="sxs-lookup"><span data-stu-id="593e8-118">Select **Proposed vendor changes workflow**.</span></span> 
8. <span data-ttu-id="593e8-119">设置工作流，使其与您的审核流程匹配。</span><span class="sxs-lookup"><span data-stu-id="593e8-119">Set up the workflow so that it matches your approval process.</span></span> <span data-ttu-id="593e8-120">**建议的供应商更改的工作流审核**工作流审核元素将应用对供应商的更改。</span><span class="sxs-lookup"><span data-stu-id="593e8-120">The **Workflow approval for proposed vendor change** workflow approval element will apply the changes to the vendor.</span></span>

## <a name="change-vendor-information-and-submit-the-changes-to-the-workflow"></a><span data-ttu-id="593e8-121">更改供应商信息并将更改提交给工作流</span><span class="sxs-lookup"><span data-stu-id="593e8-121">Change vendor information and submit the changes to the workflow</span></span>

<span data-ttu-id="593e8-122">更改为工作流启用的字段时，将显示**建议的更改**页。</span><span class="sxs-lookup"><span data-stu-id="593e8-122">When you change a field that is enabled for the workflow, the **Proposed changes** page appears.</span></span> <span data-ttu-id="593e8-123">此页显示字段的原始值和您输入的新值。</span><span class="sxs-lookup"><span data-stu-id="593e8-123">This page shows the original value of the field and the new value that you entered.</span></span> <span data-ttu-id="593e8-124">将把您更改的字段恢复为原始值。</span><span class="sxs-lookup"><span data-stu-id="593e8-124">The field that you changed is reverted to its original value.</span></span> <span data-ttu-id="593e8-125">还会通过状态消息告知您尚未提交您的更改。</span><span class="sxs-lookup"><span data-stu-id="593e8-125">A status message also informs you that your changes haven't been submitted.</span></span> 

<span data-ttu-id="593e8-126">只要更改了为工作流启用的字段，都将把该字段添加到**建议的更改**页上的列表中。</span><span class="sxs-lookup"><span data-stu-id="593e8-126">Every time that you change a field that is enabled for the workflow, that field is added to the list on the **Proposed changes** page.</span></span> <span data-ttu-id="593e8-127">若要放弃字段的建议值，请使用列表中该字段旁边的**放弃**按钮。</span><span class="sxs-lookup"><span data-stu-id="593e8-127">To discard the proposed value for a field, use the **Discard** button next to the field in the list.</span></span> <span data-ttu-id="593e8-128">若要放弃所有更改，请使用页面底部的**放弃所有更改**按钮。</span><span class="sxs-lookup"><span data-stu-id="593e8-128">To discard all changes, use the **Discard all changes** button at the bottom of the page.</span></span> <span data-ttu-id="593e8-129">选择**确定**关闭页面。</span><span class="sxs-lookup"><span data-stu-id="593e8-129">Select **OK** to close the page.</span></span>

<span data-ttu-id="593e8-130">至少执行一项建议的更改之后，操作窗格中将显示两个额外的选项卡：**建议的更改**和**工作流**。</span><span class="sxs-lookup"><span data-stu-id="593e8-130">After you have at least one proposed change, two additional tabs appear on the action pane: **Proposed changes** and **Workflow**.</span></span>

1. <span data-ttu-id="593e8-131">选择 **建议的更改**打开**建议的更改** 页并查看您的更改。</span><span class="sxs-lookup"><span data-stu-id="593e8-131">Select **Proposed changes** to open the **Proposed changes** page and review your changes.</span></span>
2. <span data-ttu-id="593e8-132">选择**工作流 \> 提交**以提交对工作流的更改。</span><span class="sxs-lookup"><span data-stu-id="593e8-132">Select **Workflow \> Submit to submit the changes to workflow**.</span></span>

    <span data-ttu-id="593e8-133">页面上的状态更改为**更改待审核**。</span><span class="sxs-lookup"><span data-stu-id="593e8-133">The status on the page is changed to **Changes pending approval**.</span></span>

<span data-ttu-id="593e8-134">此工作流执行 Microsoft Dynamics 365 for Finance and Operations 中的标准工作流流程。</span><span class="sxs-lookup"><span data-stu-id="593e8-134">The workflow follows the standard workflow process in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="593e8-135">将把审核者定向到**供应商**页面，可在此处查看**建议的更改**页中的更改，然后选择**工作流 \> 审核**以审核工作流。</span><span class="sxs-lookup"><span data-stu-id="593e8-135">The approver is directed to the **Vendor** page, where he or she can review the changes on the **Proposed changes** page and then select **Workflow \> Approve** to approve the workflow.</span></span> <span data-ttu-id="593e8-136">完成所有审核之后，将使用您建议的值更新字段。</span><span class="sxs-lookup"><span data-stu-id="593e8-136">After all approvals are completed, the fields are updated with the values that you proposed.</span></span>


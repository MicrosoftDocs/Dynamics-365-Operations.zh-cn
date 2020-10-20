---
title: 客户工作流
description: 本主题提供有关客户工作流的信息。 您更改客户的特定字段，然后在将字段添加到客户前使用工作流发送这些更改进行审核。
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: cb8519db2f5d52d4e317b485d6ecc910956788cb
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975308"
---
# <a name="customer-workflow"></a><span data-ttu-id="6480f-104">客户工作流</span><span class="sxs-lookup"><span data-stu-id="6480f-104">Customer workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6480f-105">客户工作流已添加至版本 8.0.4。</span><span class="sxs-lookup"><span data-stu-id="6480f-105">The customer workflow has been added to version 8.0.4.</span></span> <span data-ttu-id="6480f-106">您可以更改客户的特定字段，然后在将字段添加到客户前使用工作流发送这些更改进行审核。</span><span class="sxs-lookup"><span data-stu-id="6480f-106">You can change specific fields for a customer and then send those changes for approval by using the workflow before they are added to the customer.</span></span>

## <a name="set-up-the-customer-workflow"></a><span data-ttu-id="6480f-107">设置客户工作流</span><span class="sxs-lookup"><span data-stu-id="6480f-107">Set up the customer workflow</span></span>

<span data-ttu-id="6480f-108">在使用客户工作流功能之前，您必须先启用。</span><span class="sxs-lookup"><span data-stu-id="6480f-108">Before you can use the customer workflow feature, you must enable it.</span></span>

1. <span data-ttu-id="6480f-109">转至**应收帐款 \> 设置 \> 应收帐款参数**。</span><span class="sxs-lookup"><span data-stu-id="6480f-109">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="6480f-110">在**常规**选项卡上，在**客户审核**快速选项卡上，将**启用客户审核**选项设置为**是**来启用此功能。</span><span class="sxs-lookup"><span data-stu-id="6480f-110">On the **General** tab, on the **Customer approval** FastTab, set the **Enable customer approvals** option to **Yes** to enable the feature.</span></span>
3. <span data-ttu-id="6480f-111">在**数据实体行为**字段中，选择导入数据时数据实体应使用的行为：</span><span class="sxs-lookup"><span data-stu-id="6480f-111">In the **Data entity behavior** field, select the behavior that the data entities should use when data is imported:</span></span>

    - <span data-ttu-id="6480f-112">**允许在不审核的情况下进行更改** - 实体可以通过工作流在不处理客户记录的情况下更新记录。</span><span class="sxs-lookup"><span data-stu-id="6480f-112">**Allow changes without approval** – An entity can update the customer record without processing it through the workflow.</span></span>
    - <span data-ttu-id="6480f-113">**拒绝更改** - 不能对客户记录进行更改。</span><span class="sxs-lookup"><span data-stu-id="6480f-113">**Reject changes** – Changes can't be made to the customer record.</span></span> <span data-ttu-id="6480f-114">导入为工作流启用的字段将失败。</span><span class="sxs-lookup"><span data-stu-id="6480f-114">The import will fail for the fields that are enabled for the workflow.</span></span>
    - <span data-ttu-id="6480f-115">**创建更改方案** - 除为工作流启用的字段外，所有字段都会被更改。</span><span class="sxs-lookup"><span data-stu-id="6480f-115">**Create change proposals** – All fields will be changed except the fields that are enabled for the workflow.</span></span> <span data-ttu-id="6480f-116">这些字段的新值将作为建议的更改添加到客户，工作流将自动开始。</span><span class="sxs-lookup"><span data-stu-id="6480f-116">The new values for those fields will be added to the customer as proposed changes, and the workflow will be started automatically.</span></span>

4. <span data-ttu-id="6480f-117">在客户字段列表中，选择在进行更改前必须审核的每个字段的**启用**复选框。</span><span class="sxs-lookup"><span data-stu-id="6480f-117">In the list of customer fields, select then **Enable** check box for every field that must be approved before the changes can be made.</span></span>
5. <span data-ttu-id="6480f-118">转至**应收帐款 \> 设置 \> 应收帐款工作流**。</span><span class="sxs-lookup"><span data-stu-id="6480f-118">Go to **Accounts receivable \> Setup \> Accounts receivable workflows**.</span></span>
6. <span data-ttu-id="6480f-119">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="6480f-119">Select **New**.</span></span>
7. <span data-ttu-id="6480f-120">选择**建议的客户更改工作流**。</span><span class="sxs-lookup"><span data-stu-id="6480f-120">Select **Proposed customer change workflow**.</span></span> 
8. <span data-ttu-id="6480f-121">设置工作流，使其与您的审核流程匹配。</span><span class="sxs-lookup"><span data-stu-id="6480f-121">Set up the workflow so that it matches your approval process.</span></span> <span data-ttu-id="6480f-122">**建议的客户更改的工作流审核**工作流审核元素将更改应用于客户。</span><span class="sxs-lookup"><span data-stu-id="6480f-122">The **Workflow approval for proposed customer change** workflow approval element will apply the changes to the customer.</span></span>

## <a name="change-customer-information-and-submit-the-changes-to-the-workflow"></a><span data-ttu-id="6480f-123">更改客户信息并向工作流提交更改</span><span class="sxs-lookup"><span data-stu-id="6480f-123">Change customer information and submit the changes to the workflow</span></span>

<span data-ttu-id="6480f-124">在更改为工作流启用的字段时，**建议的更改**页面会显示。</span><span class="sxs-lookup"><span data-stu-id="6480f-124">When you change a field that is enabled for the workflow, the **Proposed changes** page appears.</span></span> <span data-ttu-id="6480f-125">此页面显示字段的原始值和您输入的新值。</span><span class="sxs-lookup"><span data-stu-id="6480f-125">This page shows the original value of the field and the new value that you entered.</span></span> <span data-ttu-id="6480f-126">您更改的字段还原为原始值。</span><span class="sxs-lookup"><span data-stu-id="6480f-126">The field that you changed is reverted to its original value.</span></span> <span data-ttu-id="6480f-127">页面上的状态消息通知您更改尚未提交。</span><span class="sxs-lookup"><span data-stu-id="6480f-127">A status message on the page informs you that your changes haven't been submitted.</span></span>

<span data-ttu-id="6480f-128">每次更改为工作流启用的字段时，该字段将添加到建议的更改列表中。</span><span class="sxs-lookup"><span data-stu-id="6480f-128">Every time that you change a field that is enabled for the workflow, that field is added to the list of proposed changes.</span></span> <span data-ttu-id="6480f-129">若要放弃字段的建议值，使用列表中字段旁边的**放弃**按钮。</span><span class="sxs-lookup"><span data-stu-id="6480f-129">To discard the proposed value for a field, use the **Discard** button next to the field in the list.</span></span> <span data-ttu-id="6480f-130">若要放弃所有更改，使用页面底部的**放弃所有更改**按钮。</span><span class="sxs-lookup"><span data-stu-id="6480f-130">To discard all changes, use the **Discard all change** button at the bottom of the page.</span></span> <span data-ttu-id="6480f-131">选择**确定**关闭页面。</span><span class="sxs-lookup"><span data-stu-id="6480f-131">Select **OK** to close the page.</span></span>

<span data-ttu-id="6480f-132">在您至少有一项建议的更改后，操作窗格上将另外出现两个菜单：**建议的更改**和**工作流**。</span><span class="sxs-lookup"><span data-stu-id="6480f-132">After you have at least one proposed change, two additional menus appear on the Action Pane: **Proposed changes** and **Workflow**.</span></span>

1. <span data-ttu-id="6480f-133">选择**建议的更改**打开**建议的更改**页面并查看您的更改。</span><span class="sxs-lookup"><span data-stu-id="6480f-133">Select **Proposed changes** to open the **Proposed changes** page and review your changes.</span></span>
2. <span data-ttu-id="6480f-134">选择**工作流 \> 提交**将更改提交到工作流。</span><span class="sxs-lookup"><span data-stu-id="6480f-134">Select **Workflow \> Submit** to submit the changes to the workflow.</span></span>

    <span data-ttu-id="6480f-135">页面上的状态将更改为**更改待审核**。</span><span class="sxs-lookup"><span data-stu-id="6480f-135">The status on the page is changed to **Changes pending approval**.</span></span>

<span data-ttu-id="6480f-136">工作流执行应用程序中的标准工作流程。</span><span class="sxs-lookup"><span data-stu-id="6480f-136">The workflow follows the standard workflow process in the application.</span></span> <span data-ttu-id="6480f-137">审核人被定向到**客户**页面，在这里用户可以查看**建议的更改**页面的更改，然后选择**工作流 \> 审核**审核工作流。</span><span class="sxs-lookup"><span data-stu-id="6480f-137">The approver is directed to the **Customer** page, where he or she can review the changes on the **Proposed changes** page and then select **Workflow \> Approve** to approve the workflow.</span></span> <span data-ttu-id="6480f-138">在完成所有审核后，字段将更新为您建议的值。</span><span class="sxs-lookup"><span data-stu-id="6480f-138">After all approvals are completed, the fields are updated with the values that you proposed.</span></span>

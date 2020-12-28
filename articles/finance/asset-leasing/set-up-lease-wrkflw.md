---
title: 设置租赁审批工作流
description: 该主题说明如何设置在创建新租赁时将运行的审批工作流。
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 58c0fd781710b7ab8efeaa7a6874f412279a5924
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4440942"
---
# <a name="set-up-lease-approval-workflows"></a><span data-ttu-id="a6181-103">设置租赁审批工作流</span><span class="sxs-lookup"><span data-stu-id="a6181-103">Set up lease approval workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a6181-104">该主题说明如何设置在创建新租赁时将运行的审批工作流。</span><span class="sxs-lookup"><span data-stu-id="a6181-104">The topic explains how to set up an approval workflow that will run when a new lease is created.</span></span> <span data-ttu-id="a6181-105">有关如何使用此工作流的详细信息，请参阅[使用审批工作流](use-create-lease-wrkflw.md)。</span><span class="sxs-lookup"><span data-stu-id="a6181-105">For information about how to use the workflow, see [Use lease approval workflows](use-create-lease-wrkflw.md).</span></span> 

1. <span data-ttu-id="a6181-106">转到 **资产租赁 \> 设置 \> 租赁工作流**。</span><span class="sxs-lookup"><span data-stu-id="a6181-106">Go to **Asset leasing \> Setup \> Lease workflow**.</span></span>
2. <span data-ttu-id="a6181-107">在 **租赁工作流** 页面上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="a6181-107">On the **Lease workflow** page, select **New**.</span></span>
3. <span data-ttu-id="a6181-108">在出现的对话框中 **工作流类型** 下，选择 **租赁工作流** 链接。</span><span class="sxs-lookup"><span data-stu-id="a6181-108">In the dialog box that appears, under **Workflow type**, select the **Lease workflow** link.</span></span>

    <span data-ttu-id="a6181-109">将打开该应用程序。</span><span class="sxs-lookup"><span data-stu-id="a6181-109">The application is opened.</span></span> <span data-ttu-id="a6181-110">运行后，登录到要重定向到工作流应用程序的 Azure Active Directory (Azure AD)。</span><span class="sxs-lookup"><span data-stu-id="a6181-110">After it runs, sign in to Azure Active Directory (Azure AD) to be redirected to the workflow application.</span></span>

4. <span data-ttu-id="a6181-111">将 **租赁工作流审批** 元素添加到工作流中。</span><span class="sxs-lookup"><span data-stu-id="a6181-111">Drag the **Lease workflow approval** element onto the workflow.</span></span>
5. <span data-ttu-id="a6181-112">将一个节点从 **开始** 连接到 **租赁工作流审批**。</span><span class="sxs-lookup"><span data-stu-id="a6181-112">Connect one node from **Start** to **Lease workflow approval**.</span></span> <span data-ttu-id="a6181-113">然后将 **租赁工作流审批** 连接到 **结束**。</span><span class="sxs-lookup"><span data-stu-id="a6181-113">Then connect **Lease workflow approval** to **End**.</span></span>
6. <span data-ttu-id="a6181-114">双击 **租赁工作流审批**。</span><span class="sxs-lookup"><span data-stu-id="a6181-114">Double-click **Lease workflow approval**.</span></span>
7. <span data-ttu-id="a6181-115">选择 **属性**，然后在 **基本设置** 下输入工作流的名称。</span><span class="sxs-lookup"><span data-stu-id="a6181-115">Select **Properties**, and then, under **Basic settings**, enter a name for the workflow.</span></span>

    <span data-ttu-id="a6181-116">在此页面上，您还可以为工作流设置更多参数。</span><span class="sxs-lookup"><span data-stu-id="a6181-116">On this page, you can also set more parameters for the workflow.</span></span> <span data-ttu-id="a6181-117">如果您已开启 **自动操作**，系统将自动执行特定操作。</span><span class="sxs-lookup"><span data-stu-id="a6181-117">If you've turned on **Automatic actions**, the system will automatically take a specific action.</span></span> <span data-ttu-id="a6181-118">如果在 **通知** 选项卡上指定了通知，则可以发送通知。在 **高级设置** 选项卡中，您可以指定最终审批者，设置时间限制，以及指定必须完成的特定操作。</span><span class="sxs-lookup"><span data-stu-id="a6181-118">Notifications can be sent if they are specified on the **Notifications** tab. On the **Advanced settings** tab, you can specify a final approver, set a time limit, and designate specific actions that must be completed.</span></span>

8. <span data-ttu-id="a6181-119">完成工作流参数的设置后，请选择 **关闭**。</span><span class="sxs-lookup"><span data-stu-id="a6181-119">When you've finished setting the workflow parameters, select **Close**.</span></span>
9. <span data-ttu-id="a6181-120">选择 **步骤 1**，然后选择 **属性**。</span><span class="sxs-lookup"><span data-stu-id="a6181-120">Select **Step 1**, and then select **Properties**.</span></span>
10. <span data-ttu-id="a6181-121">在 **基本设置** 下，输入步骤的名称，为审批创建主题行，然后指定审批说明。</span><span class="sxs-lookup"><span data-stu-id="a6181-121">Under **Basic settings**, enter a name for the step, create a subject line for the approval, and specify instructions for the approval.</span></span>
11. <span data-ttu-id="a6181-122">在 **分配** 页面上，选择分配类型。</span><span class="sxs-lookup"><span data-stu-id="a6181-122">On the **Assignment** page, select the assignment type.</span></span>
12. <span data-ttu-id="a6181-123">要为审批分配特定用户，请选择 **用户**，选择审批租赁的用户，然后选择 **关闭**。</span><span class="sxs-lookup"><span data-stu-id="a6181-123">To assign specific users to the approval, select **User**, select the users who approve leases, and then select **Close**.</span></span>
13. <span data-ttu-id="a6181-124">选择 **保存并关闭** 以创建工作流。</span><span class="sxs-lookup"><span data-stu-id="a6181-124">Select **Save and close** to create the workflow.</span></span> <span data-ttu-id="a6181-125">然后，在系统提示时，选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="a6181-125">Then, when you're prompted, select **OK**.</span></span>
14. <span data-ttu-id="a6181-126">在 **创建工作流** 页面上，选择 **关闭**。</span><span class="sxs-lookup"><span data-stu-id="a6181-126">On the **Create workflow** page, select **Close**.</span></span>
14. <span data-ttu-id="a6181-127">选择新工作流，然后选择 **版本号**。</span><span class="sxs-lookup"><span data-stu-id="a6181-127">Select the new workflow, and then select **Versions**.</span></span> <span data-ttu-id="a6181-128">然后选择 **激活** 以确保工作流处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="a6181-128">Then select **Make active** to ensure that the workflow is active.</span></span>
15. <span data-ttu-id="a6181-129">选择 **关闭**。</span><span class="sxs-lookup"><span data-stu-id="a6181-129">Select **Close**.</span></span> <span data-ttu-id="a6181-130">将显示新的活动版本。</span><span class="sxs-lookup"><span data-stu-id="a6181-130">The new active version appears.</span></span>

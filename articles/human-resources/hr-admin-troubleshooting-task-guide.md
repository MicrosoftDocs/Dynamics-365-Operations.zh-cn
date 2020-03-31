---
title: 将任务指南保存到 LCS 并重新播放它们
description: 本文说明如何将任务指南保存到 Microsoft Dynamics Lifecycle Services (LCS) 然后重新播放它们。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b55937c0867117809471f50f1987f7bf12a4b25d
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008294"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a><span data-ttu-id="4dc08-103">将任务指南保存到 LCS 并重新播放它们</span><span class="sxs-lookup"><span data-stu-id="4dc08-103">Save task guides to LCS and replay them</span></span>

<span data-ttu-id="4dc08-104">**环境详细信息**</span><span class="sxs-lookup"><span data-stu-id="4dc08-104">**Environment details**</span></span> 

<span data-ttu-id="4dc08-105">Microsoft Dynamics 365 Human Resources 通过 Microsoft Dynamics Lifecycle Services (LCS) 部署</span><span class="sxs-lookup"><span data-stu-id="4dc08-105">Microsoft Dynamics 365 Human Resources, which was deployed via Microsoft Dynamics Lifecycle Services (LCS)</span></span>

<span data-ttu-id="4dc08-106">**发货**</span><span class="sxs-lookup"><span data-stu-id="4dc08-106">**Issue**</span></span>

<span data-ttu-id="4dc08-107">客户希望将新任务录制保存到其 LCS 项目，然后重新播放保存的任务指南。</span><span class="sxs-lookup"><span data-stu-id="4dc08-107">The customer wants to save new task recordings to his or her LCS project, and then replay the saved task guides.</span></span>

<span data-ttu-id="4dc08-108">**分辨率**</span><span class="sxs-lookup"><span data-stu-id="4dc08-108">**Resolution**</span></span>

<span data-ttu-id="4dc08-109">请执行以下步骤将任务录制保存到 LCS。</span><span class="sxs-lookup"><span data-stu-id="4dc08-109">Follow these steps to save a task recording to LCS.</span></span>

1. <span data-ttu-id="4dc08-110">登录到 LCS，并选择项目。</span><span class="sxs-lookup"><span data-stu-id="4dc08-110">Sign in to LCS, and select the project.</span></span>
2. <span data-ttu-id="4dc08-111">选择**业务流程建模器**磁贴。</span><span class="sxs-lookup"><span data-stu-id="4dc08-111">Select the **Business process modeler** tile.</span></span>
3. <span data-ttu-id="4dc08-112">在“更新的 BPM 体验”中查看此页面。</span><span class="sxs-lookup"><span data-stu-id="4dc08-112">View the page in the "Updated BPM experience."</span></span>
4. <span data-ttu-id="4dc08-113">选择库，然后选择**复制**。</span><span class="sxs-lookup"><span data-stu-id="4dc08-113">Select a library, and then select **Copy**.</span></span>
5. <span data-ttu-id="4dc08-114">为业务流程建模器 (BPM) 模型输入一个名称。</span><span class="sxs-lookup"><span data-stu-id="4dc08-114">Enter a name for the Business process modeler (BPM) model.</span></span>
6. <span data-ttu-id="4dc08-115">从 LCS 登录到 Human Resources。</span><span class="sxs-lookup"><span data-stu-id="4dc08-115">Sign in to Human Resources from LCS.</span></span>
7. <span data-ttu-id="4dc08-116">在**搜索**字段中，输入**帮助**。</span><span class="sxs-lookup"><span data-stu-id="4dc08-116">In the **Search** field, enter **help**.</span></span> <span data-ttu-id="4dc08-117">Lifecycle Services 帮助将打开。</span><span class="sxs-lookup"><span data-stu-id="4dc08-117">Lifecycle Services Help is opened.</span></span>
8. <span data-ttu-id="4dc08-118">选择 Lifecycle Services 帮助配置的**刷新**按钮。</span><span class="sxs-lookup"><span data-stu-id="4dc08-118">Select the **Refresh** button for Lifecycle Services Help configuration.</span></span>

    <span data-ttu-id="4dc08-119">您的新 BPM 库应会出现，它应是活动的。</span><span class="sxs-lookup"><span data-stu-id="4dc08-119">Your new BPM library should appear, and it should be active.</span></span>

9. <span data-ttu-id="4dc08-120">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4dc08-120">Close the page.</span></span>
10. <span data-ttu-id="4dc08-121">创建任务录制。</span><span class="sxs-lookup"><span data-stu-id="4dc08-121">Create a task recording.</span></span>
11. <span data-ttu-id="4dc08-122">当您完成时，选择**保存到 Lifecycle Services**。</span><span class="sxs-lookup"><span data-stu-id="4dc08-122">When you've finished, select **Save to Lifecycle Services**.</span></span>

    ![保存到 Lifecycle Services](media/task-guides.png)

12. <span data-ttu-id="4dc08-124">选择要保存任务录制的 BPM 库和节点。</span><span class="sxs-lookup"><span data-stu-id="4dc08-124">Select the BPM library and node to save the task recording to.</span></span>

<span data-ttu-id="4dc08-125">执行以下步骤从 LCS 重新播放任务指南。</span><span class="sxs-lookup"><span data-stu-id="4dc08-125">Follow these steps to replay a task guide from LCS.</span></span>

1. <span data-ttu-id="4dc08-126">启动任务录制器</span><span class="sxs-lookup"><span data-stu-id="4dc08-126">Start Task recorder.</span></span>
2. <span data-ttu-id="4dc08-127">选择**从 LCS 打开**。</span><span class="sxs-lookup"><span data-stu-id="4dc08-127">Select **Open from LCS**.</span></span>
3. <span data-ttu-id="4dc08-128">选择包含保存的任务指南的库和 BPM 节点。</span><span class="sxs-lookup"><span data-stu-id="4dc08-128">Select the library and the BPM node that have the saved task guide.</span></span>
4. <span data-ttu-id="4dc08-129">打开任务指南。</span><span class="sxs-lookup"><span data-stu-id="4dc08-129">Open the task guide.</span></span>
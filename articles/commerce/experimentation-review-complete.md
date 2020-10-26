---
title: 促进变体和完成试验
description: 本主题介绍了如何在 Dynamics 365 Commerce 中促进成功的变体和完成试验。
author: sushma-rao
manager: AnnBe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 2e011f10e908d6a2efe2e928fc5e0abc7659cb8b
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930144"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a><span data-ttu-id="a5d65-103">促进变体和完成试验</span><span class="sxs-lookup"><span data-stu-id="a5d65-103">Promote a variation and complete an experiment</span></span>

<span data-ttu-id="a5d65-104">本主题描述了如何促进在试验中产生最佳结果的变体，以及如何完成试验。</span><span class="sxs-lookup"><span data-stu-id="a5d65-104">This topic describes how to promote the variation that produced the best results in your experiment, and how to complete the experiment.</span></span> <span data-ttu-id="a5d65-105">下图显示了在 Dynamics 365 Commerce 中的电子商务网站上设置和运行试验所涉及的所有步骤。</span><span class="sxs-lookup"><span data-stu-id="a5d65-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="a5d65-106">其他步骤在单独的主题中介绍。</span><span class="sxs-lookup"><span data-stu-id="a5d65-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="a5d65-107">[![试验用户旅程 - 审查和完成](./media/experimentation_review_complete.svg)](./media/experimentation_review_complete.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="a5d65-107">[ ![Experimentation user journey - Review & Complete](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span></span>

<span data-ttu-id="a5d65-108">在[运行试验](experimentation-run-monitor.md)并收集了足够的数据来确定您要在活动站点上使用哪种变体后，您将促进变体并结束试验。</span><span class="sxs-lookup"><span data-stu-id="a5d65-108">After you've [run your experiment](experimentation-run-monitor.md) and collected sufficient data to determine which variation you want to use on your live site, you'll promote the variation and end the experiment.</span></span>

## <a name="promote-a-variation"></a><span data-ttu-id="a5d65-109">促进变体</span><span class="sxs-lookup"><span data-stu-id="a5d65-109">Promote a variation</span></span>
<span data-ttu-id="a5d65-110">使用与第三方服务中的试验相关的数据和分析来确定哪种变体产生了最佳结果。</span><span class="sxs-lookup"><span data-stu-id="a5d65-110">Use the data and analytics related to the experiment in the third-party service to decide which variation produced the best results.</span></span> <span data-ttu-id="a5d65-111">若要将活动站点上的当前内容替换为最佳变体，以供您的网站的所有用户使用，请执行以下操作。</span><span class="sxs-lookup"><span data-stu-id="a5d65-111">To replace the current content on the live site with the winning variation so that it's available to all users of your website, do the following.</span></span> 

1. <span data-ttu-id="a5d65-112">在站点构建器中，转到**试验**选项卡，然后选择试验。</span><span class="sxs-lookup"><span data-stu-id="a5d65-112">Go to the **Experiments** tab in site builder and select the experiment.</span></span>
1. <span data-ttu-id="a5d65-113">选择顶部栏上的**完成试验**。</span><span class="sxs-lookup"><span data-stu-id="a5d65-113">Select **Complete experiment** on the top bar.</span></span>
1. <span data-ttu-id="a5d65-114">在**完成试验**对话框菜单中，选择**查看试验数据**。</span><span class="sxs-lookup"><span data-stu-id="a5d65-114">In the **Complete the experiment** dialog menu, select **Review the experiment data**.</span></span> <span data-ttu-id="a5d65-115">将打开第三方服务，您可以在其中验证指标并确定哪种变体表现最好。</span><span class="sxs-lookup"><span data-stu-id="a5d65-115">The third-party service opens where you can validate the metrics and determine which variation performed the best.</span></span>
1. <span data-ttu-id="a5d65-116">在站点构建器的**完成试验**对话框菜单中，选择最佳变体，然后选择**下一步**。</span><span class="sxs-lookup"><span data-stu-id="a5d65-116">In the **Complete the experiment** dialog menu in site builder, select the winning variation and then select **Next**.</span></span>
1. <span data-ttu-id="a5d65-117">打开第三方服务并停止试验。</span><span class="sxs-lookup"><span data-stu-id="a5d65-117">Open the third-party service and stop the experiment.</span></span>
1. <span data-ttu-id="a5d65-118">在站点构建器中，选择**完成**以覆盖原始活动页面并发布最佳变体，以供您的网站的所有用户使用。</span><span class="sxs-lookup"><span data-stu-id="a5d65-118">In site builder, select **Complete** to overwrite the original live page and publish the winning variation so that it's available to all users of your website.</span></span> 

> [!NOTE]
> <span data-ttu-id="a5d65-119">如果您选择保留当前的活动页面而不发布变体，请选择**重新发布原始页面**。</span><span class="sxs-lookup"><span data-stu-id="a5d65-119">If you choose to keep the current live page and not publish a variation, select **Republish the original page**.</span></span>

## <a name="delete-your-experiment"></a><span data-ttu-id="a5d65-120">删除试验</span><span class="sxs-lookup"><span data-stu-id="a5d65-120">Delete your experiment</span></span>
<span data-ttu-id="a5d65-121">虽然不需要在 Commerce 中删除完成的试验，但您可以选择删除它以节省空间或清理工作区。</span><span class="sxs-lookup"><span data-stu-id="a5d65-121">While it's not required that you delete a completed experiment in Commerce, you may choose to delete it to save space or clean up your workspace.</span></span> <span data-ttu-id="a5d65-122">若要删除试验，请执行以下操作。</span><span class="sxs-lookup"><span data-stu-id="a5d65-122">To delete an experiment, do the following.</span></span>

1. <span data-ttu-id="a5d65-123">在站点构建器中，转到**试验**选项卡，然后选择试验。</span><span class="sxs-lookup"><span data-stu-id="a5d65-123">Go to the **Experiments** tab in site builder and select the experiment.</span></span> 
    > [!NOTE]
    > <span data-ttu-id="a5d65-124">如果试验仍处于活动状态，请先在第三方服务中停止试验，然后再继续。</span><span class="sxs-lookup"><span data-stu-id="a5d65-124">If the experiment is still active, stop the experiment in the third-party service before proceeding.</span></span>
1. <span data-ttu-id="a5d65-125">在命令栏中选择**取消发布**，以从活动站点中删除变体内容。</span><span class="sxs-lookup"><span data-stu-id="a5d65-125">Select **Unpublish** in the command bar to remove the variation content from the live site.</span></span>
1. <span data-ttu-id="a5d65-126">在命令栏中选择**删除**以删除试验。</span><span class="sxs-lookup"><span data-stu-id="a5d65-126">Select **Delete** in the command bar to delete the experiment.</span></span>

## <a name="previous-step"></a><span data-ttu-id="a5d65-127">上一步</span><span class="sxs-lookup"><span data-stu-id="a5d65-127">Previous step</span></span>
[<span data-ttu-id="a5d65-128">运行和监视试验</span><span class="sxs-lookup"><span data-stu-id="a5d65-128">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)

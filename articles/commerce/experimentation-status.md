---
title: 查看试验的状态
description: 本主题说明了试验在 Dynamics 365 Commerce 的试验生命周期中有哪些状态。
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
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
ms.openlocfilehash: 097206c0aa487e14499bdf3907465e17b7d337e2
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930145"
---
# <a name="review-the-status-of-an-experiment"></a><span data-ttu-id="24e64-103">查看试验的状态</span><span class="sxs-lookup"><span data-stu-id="24e64-103">Review the status of an experiment</span></span>
<span data-ttu-id="24e64-104">在 Dynamics 365 Commerce 中设置和运行试验涉及许多步骤。</span><span class="sxs-lookup"><span data-stu-id="24e64-104">There are many steps involved in setting up and running an experiment in Dynamics 365 Commerce.</span></span> <span data-ttu-id="24e64-105">有关试验生命周期的信息，请参阅 [Dynamics 365 Commerce 中的试验](experimentation-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="24e64-105">For information about the experimentation lifecycle, see [Experimentation in Dynamics 365 Commerce](experimentation-overview.md).</span></span>

<span data-ttu-id="24e64-106">若要了解试验在生命周期中的位置，请转到站点构建器中的**试验**选项卡。</span><span class="sxs-lookup"><span data-stu-id="24e64-106">To learn where an experiment is in the lifecycle, go to the **Experiments** tab in site builder.</span></span> <span data-ttu-id="24e64-107">将显示试验列表，其中包含 Commerce 和用于创建试验、分配变体和分析数据的第三方服务中每个试验的状态。</span><span class="sxs-lookup"><span data-stu-id="24e64-107">A list of experiments is displayed with the status of each experiment in both Commerce and the third-party service that is being used to enable the creation of experiments, assign variations, and analyze data.</span></span>

<span data-ttu-id="24e64-108">在 **Commerce 状态**列中，可能会显示以下值。</span><span class="sxs-lookup"><span data-stu-id="24e64-108">In the **Commerce status** column, the following values may be displayed.</span></span> 
- <span data-ttu-id="24e64-109">**草稿** - 试验已连接到 Commerce 中的一个页面或片段，将进行编辑。</span><span class="sxs-lookup"><span data-stu-id="24e64-109">**Draft** - The experiment is connected to a page or fragment in Commerce and is being edited.</span></span>
- <span data-ttu-id="24e64-110">**已发布** - 试验变体已准备好在您的网站上显示。</span><span class="sxs-lookup"><span data-stu-id="24e64-110">**Published** - The experiment variations are ready to be displayed on your website.</span></span> <span data-ttu-id="24e64-111">如果试验在第三方服务中运行，则网站用户将看到由第三方服务选择的页面或片段变体。</span><span class="sxs-lookup"><span data-stu-id="24e64-111">If the experiment is running in the third-party service, website users will see a variation of the page or fragment as selected by the third-party service.</span></span>
- <span data-ttu-id="24e64-112">**取消发布** - 试验在您的网站上不再可用。</span><span class="sxs-lookup"><span data-stu-id="24e64-112">**Unpublished** - The experiment is no longer available on your website.</span></span> <span data-ttu-id="24e64-113">即使试验在第三方服务中运行，网站用户也只能看到默认版本的页面或片段。</span><span class="sxs-lookup"><span data-stu-id="24e64-113">Website users will only see the default version of the page or fragment even if the experiment is running in the third-party service.</span></span>
- <span data-ttu-id="24e64-114">**已完成** - 试验已经完成，并推广了变体以供所有网站用户使用。</span><span class="sxs-lookup"><span data-stu-id="24e64-114">**Completed** - The experiment has run its course and a variation was promoted to live for all website users.</span></span>

<span data-ttu-id="24e64-115">同样，在**第三方状态**列中，可能会显示以下值，以指示试验在第三方服务中有哪些状态。</span><span class="sxs-lookup"><span data-stu-id="24e64-115">Similarly, in the **third-party status** column, the following values may be displayed to indicate what status the experiments are in the third-party service.</span></span>
- <span data-ttu-id="24e64-116">**草稿** - 试验在第三方服务中设置，但尚未启动。</span><span class="sxs-lookup"><span data-stu-id="24e64-116">**Draft** - The experiment is set up in the third-party service but hasn't been started.</span></span>
- <span data-ttu-id="24e64-117">**运行** - 试验已在第三方服务中启动，正在收集数据。</span><span class="sxs-lookup"><span data-stu-id="24e64-117">**Running** - The experiment was started in the third-party service and is collecting data.</span></span>
- <span data-ttu-id="24e64-118">**已暂停** - 试验已暂停且未在收集数据。</span><span class="sxs-lookup"><span data-stu-id="24e64-118">**Paused** - The experiment is paused and not collecting data.</span></span> <span data-ttu-id="24e64-119">您必须恢复试验才能再次收集数据。</span><span class="sxs-lookup"><span data-stu-id="24e64-119">You must resume the experiment for it to collect data again.</span></span>
- <span data-ttu-id="24e64-120">**已存档** - 试验已经完成，并已归类在第三方服务中以供将来引用。</span><span class="sxs-lookup"><span data-stu-id="24e64-120">**Archived** - The experiment has run its course and has been cataloged in the third-party service for future reference.</span></span>

<span data-ttu-id="24e64-121">下图显示了两种状态以及它们之间的关系。</span><span class="sxs-lookup"><span data-stu-id="24e64-121">The diagram below shows both sets of statuses and how they relate to each other.</span></span>

<span data-ttu-id="24e64-122">[![试验状态](./media/experimentation_statuses.svg)](./media/experimentation_statuses.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="24e64-122">[ ![Experimentation statuses](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)</span></span>

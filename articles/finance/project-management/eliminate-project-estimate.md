---
title: 清除项目评估
description: 本主题提供有关在项目评估完成后清除项目评估的信息。
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: eb323bdeb2a4701cdc9383b8da29e05a4cab107c
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410194"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="bc1c7-103">清除项目评估</span><span class="sxs-lookup"><span data-stu-id="bc1c7-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bc1c7-104">项目评估提供为项目估计和计划的工作的财务观点。</span><span class="sxs-lookup"><span data-stu-id="bc1c7-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="bc1c7-105">若要使用某一项目的评估，则必须将该项目附加到某一评估项目。</span><span class="sxs-lookup"><span data-stu-id="bc1c7-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="bc1c7-106">评估项目始终基于现有项目，但是，多个项目可以引用单个评估项目。</span><span class="sxs-lookup"><span data-stu-id="bc1c7-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="bc1c7-107">只能附加固定价格项目和投资项目来评估项目，并且这些项目必须与评估项目属于同一项目组。</span><span class="sxs-lookup"><span data-stu-id="bc1c7-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="bc1c7-108">若要清除评估项目，该项目必须已完成。</span><span class="sxs-lookup"><span data-stu-id="bc1c7-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="bc1c7-109">以下步骤说明如何清除评估。</span><span class="sxs-lookup"><span data-stu-id="bc1c7-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="bc1c7-110">转到**项目管理与核算** > **所有项目**，打开项目。</span><span class="sxs-lookup"><span data-stu-id="bc1c7-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="bc1c7-111">在**管理**选项卡上，选择**评估**，然后在**评估**页面上选择**评估**。</span><span class="sxs-lookup"><span data-stu-id="bc1c7-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="bc1c7-112">在**常规**选项卡上的**清除评估**页面，设置以下选项：</span><span class="sxs-lookup"><span data-stu-id="bc1c7-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="bc1c7-113">**期间代码**：选择期间代码以挑选相应的评估项目。</span><span class="sxs-lookup"><span data-stu-id="bc1c7-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="bc1c7-114">**评估日期**：选择有关的评估日期以进行清除。</span><span class="sxs-lookup"><span data-stu-id="bc1c7-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="bc1c7-115">**WIP 消除警告**：启用此选项可在清除与进行中的工作 (WIP) 关联的评估时提供通知。</span><span class="sxs-lookup"><span data-stu-id="bc1c7-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="bc1c7-116">如果未启用此选项，如果存在任何未评估的交易，将无法继续清除。</span><span class="sxs-lookup"><span data-stu-id="bc1c7-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="bc1c7-117">仅当对评估项目应用清除时，此选项才可用。</span><span class="sxs-lookup"><span data-stu-id="bc1c7-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="bc1c7-118">如果您使用的定期过帐，它不可用。</span><span class="sxs-lookup"><span data-stu-id="bc1c7-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="bc1c7-119">此设置在**存在未估计的交易时允许清除**字段组中，与**项目参数**页面上**评估**选项卡上的设置一起使用。</span><span class="sxs-lookup"><span data-stu-id="bc1c7-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="bc1c7-120">**将阶段设置为已完成**：启用此选项可在运行清除后将评估项目的阶段设置为**已完成**。</span><span class="sxs-lookup"><span data-stu-id="bc1c7-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="bc1c7-121">**打印评估列表**：选择在打印评估列表时所要包括的信息。</span><span class="sxs-lookup"><span data-stu-id="bc1c7-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="bc1c7-122">**显示信息日志**：启用此选项可以显示信息日志。</span><span class="sxs-lookup"><span data-stu-id="bc1c7-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="bc1c7-123">**过帐日期**：选择评估的分类帐过帐日期。</span><span class="sxs-lookup"><span data-stu-id="bc1c7-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="bc1c7-124">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="bc1c7-124">Select **OK**.</span></span>
5. <span data-ttu-id="bc1c7-125">清除流程完成后，清除的评估项目将显示，其中包含负值。</span><span class="sxs-lookup"><span data-stu-id="bc1c7-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="bc1c7-126">如果您不打算清除评估，您可以选择清除的评估，然后选择**反向清除**。</span><span class="sxs-lookup"><span data-stu-id="bc1c7-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   

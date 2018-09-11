--- 
title: "停用生产流版本"
description: "如果不再需要某个有效生产流版本，可将其停用。"
author: cvocph
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 04ed71ab3501be7c9670748d4c7001843ed96c81
ms.contentlocale: zh-cn
ms.lasthandoff: 09/11/2018

---
# <a name="deactivate-a-production-flow-version"></a><span data-ttu-id="600ae-103">停用生产流版本</span><span class="sxs-lookup"><span data-stu-id="600ae-103">Deactivate a production flow version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="600ae-104">如果不再需要某个有效生产流版本，可将其停用。</span><span class="sxs-lookup"><span data-stu-id="600ae-104">When an active production flow version is no longer needed, it can be deactivated.</span></span> <span data-ttu-id="600ae-105">仅当所有看板规则和活动已结束且将不再激活，才应使用此选项。</span><span class="sxs-lookup"><span data-stu-id="600ae-105">You should only use this option if all kanban rules and activities have ended and will not be activated again.</span></span> <span data-ttu-id="600ae-106">请注意，将使用当前日期和时间更新与此生产流版本有关的所有看板规则的到期日期。</span><span class="sxs-lookup"><span data-stu-id="600ae-106">Note that the expiry date of all kanban rules related to this production flow version will be updated with the current date and time.</span></span> 

<span data-ttu-id="600ae-107">若要修改有效生产流版本，请考虑设置有效版本的到期日期和创建新版本。</span><span class="sxs-lookup"><span data-stu-id="600ae-107">To modify an active production flow version, consider setting an expiry date for the active version and create a new version.</span></span> <span data-ttu-id="600ae-108">这样您就可以继续生产操作，同时准备新版本和相关看板规则。</span><span class="sxs-lookup"><span data-stu-id="600ae-108">This will allow you to continue your production operations while preparing the new version and related kanban rules.</span></span> 

<span data-ttu-id="600ae-109">若要让有效生产流版本到期，需要设置到期日期。</span><span class="sxs-lookup"><span data-stu-id="600ae-109">To expire an active production flow version, you need to set an expiry date.</span></span> <span data-ttu-id="600ae-110">在这种情况下，停用更像异常，而不是规则。</span><span class="sxs-lookup"><span data-stu-id="600ae-110">In that sense, deactivation is more like an exception than a rule.</span></span> 

<span data-ttu-id="600ae-111">对于此过程，您需要具有可停用版本的生产流。</span><span class="sxs-lookup"><span data-stu-id="600ae-111">For this procedure you need a production flow with a version that can be deactivated.</span></span> <span data-ttu-id="600ae-112">除非您百分百确定版本已完全过时，否则请勿在生产环境中尝试此操作。</span><span class="sxs-lookup"><span data-stu-id="600ae-112">Do not try this in a production environment unless you are 100% positive that the version is fully obsolete.</span></span>


## <a name="deactivate-a-production-flow-version"></a><span data-ttu-id="600ae-113">停用生产流版本</span><span class="sxs-lookup"><span data-stu-id="600ae-113">Deactivate a production flow version</span></span>
1. <span data-ttu-id="600ae-114">转到“生产控制”>“设置”>“精益生产流程”>“生产流程”。</span><span class="sxs-lookup"><span data-stu-id="600ae-114">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="600ae-115">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="600ae-115">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="600ae-116">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="600ae-116">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="600ae-117">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="600ae-117">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="600ae-118">单击“停用”。</span><span class="sxs-lookup"><span data-stu-id="600ae-118">Click Deactivate.</span></span>
    * <span data-ttu-id="600ae-119">如果不是百分百确定此生产流版本已过时，否则请勿继续操作。</span><span class="sxs-lookup"><span data-stu-id="600ae-119">Do not proceed if you are not 100% positive that this production flow version is obsolete.</span></span> <span data-ttu-id="600ae-120">单击“确定”将让所有有效看板规则过期，并立即停止此生产流版本的所有生产和补货活动。</span><span class="sxs-lookup"><span data-stu-id="600ae-120">Clicking Ok will expire all active kanban rules and put an immediate stop to all production and replenishment activities of this production flow version.</span></span>  
6. <span data-ttu-id="600ae-121">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="600ae-121">Click OK.</span></span>



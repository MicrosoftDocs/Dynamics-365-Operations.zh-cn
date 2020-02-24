---
title: 配置影响零售对帐单的参数
description: 此主题演示 Commerce 参数的配置，这些参数会影响如何创建和过帐对帐单。
author: josaw1
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d8cae6d2fa7c469f50fa92141a6cb5a0af1df4b0
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021727"
---
# <a name="configure-parameters-that-affect-retail-statements"></a><span data-ttu-id="cd3d1-103">配置影响零售对帐单的参数</span><span class="sxs-lookup"><span data-stu-id="cd3d1-103">Configure parameters that affect retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="cd3d1-104">此主题演示 Commerce 参数的配置，这些参数会影响如何创建和过帐对帐单。</span><span class="sxs-lookup"><span data-stu-id="cd3d1-104">This topic demonstrates configurations for Commerce parameters that affect how statements get created and posted.</span></span> <span data-ttu-id="cd3d1-105">此程序使用 USRT 演示公司。</span><span class="sxs-lookup"><span data-stu-id="cd3d1-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="cd3d1-106">在导航窗格中，转到**模块 > Retail 和 Commerce > 总部设置 > 参数 > Commerce 参数**。</span><span class="sxs-lookup"><span data-stu-id="cd3d1-106">In the navigation pane, go to **Modules > Retail and Commerce > Headquarters setup  > Parameters > Commerce parameters**.</span></span>
2. <span data-ttu-id="cd3d1-107">选择**过帐**选项卡。</span><span class="sxs-lookup"><span data-stu-id="cd3d1-107">Select the **Posting** tab.</span></span>
    - <span data-ttu-id="cd3d1-108">如果您想要专门过帐定期折扣金额，请选择**是**。</span><span class="sxs-lookup"><span data-stu-id="cd3d1-108">Select **Yes** if you want to post the periodic discount amounts specifically.</span></span>  
    - <span data-ttu-id="cd3d1-109">选择**标准**以使用默认科目，或者如果您想要定义每个定期折扣使用哪个科目，则选择**定期**。</span><span class="sxs-lookup"><span data-stu-id="cd3d1-109">Select **Standard** to use default accounts, or select **Periodic** if you want to define which account to use for each periodic discount.</span></span>  
      - <span data-ttu-id="cd3d1-110">如果库存行应尽可能进行合计，请选择**摘要**。</span><span class="sxs-lookup"><span data-stu-id="cd3d1-110">Select **Summary** if inventory lines should get aggregated whenever possible.</span></span>  
      - <span data-ttu-id="cd3d1-111">如果发票和付款应作为报表过帐流程的一部分自动结算，请选择**是**。</span><span class="sxs-lookup"><span data-stu-id="cd3d1-111">Select **Yes** if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
      - <span data-ttu-id="cd3d1-112">如果金库投箱交易应进行合计，请选择**是**。</span><span class="sxs-lookup"><span data-stu-id="cd3d1-112">Select **Yes** if Safe drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="cd3d1-113">如果金库投箱交易应进行合计，请选择**是**。</span><span class="sxs-lookup"><span data-stu-id="cd3d1-113">Select **Yes** if Bank drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="cd3d1-114">选择**是**以打开合并，以过帐报表。</span><span class="sxs-lookup"><span data-stu-id="cd3d1-114">Select **Yes** to turn aggregation on for Statement posting.</span></span>  
      - <span data-ttu-id="cd3d1-115">将报表过帐时，选择**是**，以并行创建和处理订单。</span><span class="sxs-lookup"><span data-stu-id="cd3d1-115">Select **Yes** to create and process orders in parallel when statements are posted.</span></span>  
      - <span data-ttu-id="cd3d1-116">输入每个批处理作业任务中处理的最大订单数。</span><span class="sxs-lookup"><span data-stu-id="cd3d1-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="cd3d1-117">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="cd3d1-117">Select **Save**.</span></span>


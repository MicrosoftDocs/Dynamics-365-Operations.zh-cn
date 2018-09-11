--- 
title: "零售报表的参数配置"
description: "此程序会演示零售参数的配置，这些参数会影响如何创建和过帐零售报表。"
author: josaw1
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 94a54dddae341febf1568369545477780c176019
ms.contentlocale: zh-cn
ms.lasthandoff: 09/11/2018

---
# <a name="parameter-configurations-for-retail-statements"></a><span data-ttu-id="4df1a-103">零售报表的参数配置</span><span class="sxs-lookup"><span data-stu-id="4df1a-103">Parameter configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="4df1a-104">此程序会演示零售参数的配置，这些参数会影响如何创建和过帐零售报表。</span><span class="sxs-lookup"><span data-stu-id="4df1a-104">This procedure demonstrates configurations for Retail parameters that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="4df1a-105">此程序使用 USRT 演示公司。</span><span class="sxs-lookup"><span data-stu-id="4df1a-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="4df1a-106">转到“零售和商业”>“总部设置”>“参数”>“零售参数”。</span><span class="sxs-lookup"><span data-stu-id="4df1a-106">Go to Retail and commerce > Headquarters setup  > Parameters > Retail parameters.</span></span>
2. <span data-ttu-id="4df1a-107">单击“过帐”选项卡。</span><span class="sxs-lookup"><span data-stu-id="4df1a-107">Click the Posting tab.</span></span>
    * <span data-ttu-id="4df1a-108">如果您想要专门过帐定期折扣金额，请选择“是”。</span><span class="sxs-lookup"><span data-stu-id="4df1a-108">Select "Yes" if you want to post the periodic discount amounts specifically.</span></span>  
    * <span data-ttu-id="4df1a-109">选择“标准”以使用默认科目，或者如果您想要定义每个定期折扣使用哪个科目，则选择“定期”。</span><span class="sxs-lookup"><span data-stu-id="4df1a-109">Select "Standard" to use default accounts, or select "Periodic" if you want to define which account to use for each periodic discount.</span></span>  
    * <span data-ttu-id="4df1a-110">如果库存行应尽可能进行合计，请选择“摘要”。</span><span class="sxs-lookup"><span data-stu-id="4df1a-110">Select "Summary" if inventory lines should get aggregated whenever possible.</span></span>  
    * <span data-ttu-id="4df1a-111">如果发票和付款应作为报表过帐流程的一部分自动结算，请选择“是”。</span><span class="sxs-lookup"><span data-stu-id="4df1a-111">Select "Yes" if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
    * <span data-ttu-id="4df1a-112">如果金库投箱交易应进行合计，请选择“是”。</span><span class="sxs-lookup"><span data-stu-id="4df1a-112">Select "Yes" if Safe drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="4df1a-113">如果金库投箱交易应进行合计，请选择“是”。</span><span class="sxs-lookup"><span data-stu-id="4df1a-113">Select "Yes" if Bank drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="4df1a-114">选择“是”以打开合并，以过帐报表。</span><span class="sxs-lookup"><span data-stu-id="4df1a-114">Select "Yes" to turn aggregation on for Statement posting.</span></span>  
    * <span data-ttu-id="4df1a-115">将报表过帐时，选择“是”，以并行创建和处理订单。</span><span class="sxs-lookup"><span data-stu-id="4df1a-115">Select "Yes" to create and process orders in parallel when statements are posted.</span></span>  
    * <span data-ttu-id="4df1a-116">输入每个批处理作业任务中处理的最大订单数。</span><span class="sxs-lookup"><span data-stu-id="4df1a-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="4df1a-117">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="4df1a-117">Click Save.</span></span>



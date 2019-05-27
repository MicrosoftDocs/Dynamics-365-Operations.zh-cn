---
title: 零售报表的商店配置
description: 此程序会逐步演示零售商店的配置（这会影响到如何创建和过帐零售报表）。
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9fddeb8434d916df1613d61da88110dec8fb4465
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563636"
---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="f1285-103">零售报表的商店配置</span><span class="sxs-lookup"><span data-stu-id="f1285-103">Store configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="f1285-104">此程序会逐步演示零售商店的配置（这会影响到如何创建和过帐零售报表）。</span><span class="sxs-lookup"><span data-stu-id="f1285-104">This procedure walks through configurations for the Retail store that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="f1285-105">零售商店的财务维度将在另一个程序中论述。</span><span class="sxs-lookup"><span data-stu-id="f1285-105">Financial dimensions on Retail stores are covered in another procedure.</span></span> <span data-ttu-id="f1285-106">此程序使用 USRT 演示公司。</span><span class="sxs-lookup"><span data-stu-id="f1285-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="f1285-107">转至“零售和商业”>“渠道”>“零售商店”>“所有零售商店”。</span><span class="sxs-lookup"><span data-stu-id="f1285-107">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="f1285-108">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="f1285-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f1285-109">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="f1285-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f1285-110">“报表/结算”部分中的设置会影响到商店的报表创建、验证和过帐。</span><span class="sxs-lookup"><span data-stu-id="f1285-110">The settings in the Statement/closing section affect the statement creation, validation, and posting for the store.</span></span>  <span data-ttu-id="f1285-111">打开“报表/结算”部分。</span><span class="sxs-lookup"><span data-stu-id="f1285-111">Open the Statement/closing section.</span></span>  
    * <span data-ttu-id="f1285-112">选择您想要用于对报表行进行分组的方法。</span><span class="sxs-lookup"><span data-stu-id="f1285-112">Select the method you want to use to to group the statement lines by.</span></span>  
    * <span data-ttu-id="f1285-113">如果在从报表创建批处理作业创建报表时，每天仅可创建一份报表，请选择“是”。</span><span class="sxs-lookup"><span data-stu-id="f1285-113">Select "Yes" if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
    * <span data-ttu-id="f1285-114">“清偿申报计算”字段定义了清偿申报是否应合计或是否应使用最后一个。</span><span class="sxs-lookup"><span data-stu-id="f1285-114">The Tender declaration calculation field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
    * <span data-ttu-id="f1285-115">选择将舍入差额过帐到其中的会计科目。</span><span class="sxs-lookup"><span data-stu-id="f1285-115">Select the ledger account to post rounding differences into.</span></span>  
    * <span data-ttu-id="f1285-116">在“最大舍入差额”字段中，您可以输入允许的最大舍入差额。</span><span class="sxs-lookup"><span data-stu-id="f1285-116">In the Maximum rounding difference field, you can enter the maximum rounding difference allowed.</span></span>  
    * <span data-ttu-id="f1285-117">在“过帐”字段中，您可以输入报表允许的最大总过帐差额。</span><span class="sxs-lookup"><span data-stu-id="f1285-117">In the Posting field, you can enter the maximum total posting difference allowed for a statement.</span></span>  
    * <span data-ttu-id="f1285-118">在“班次”字段中，您可以输入报表班次中的最大总过帐差额。</span><span class="sxs-lookup"><span data-stu-id="f1285-118">In the Shift field, you can enter the maximum total difference within a shift in a statement.</span></span>  
    * <span data-ttu-id="f1285-119">在“交易”字段中，您可以输入报表行中的最大总过帐差额。</span><span class="sxs-lookup"><span data-stu-id="f1285-119">In the Transaction field, you can enter the maximum total difference in a statement line.</span></span>  
    * <span data-ttu-id="f1285-120">在“结算方法”字段中，您可以确定将包括在报表中的交易是已结算的班次的一部分，还是定义的日期/时间范围内的任何交易。</span><span class="sxs-lookup"><span data-stu-id="f1285-120">In the Closing method field, you can define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
    * <span data-ttu-id="f1285-121">在“工作日结束时”字段中，您可以输入一个时间，如果午夜之后发生的交易应随前一天过帐。</span><span class="sxs-lookup"><span data-stu-id="f1285-121">In the End of business day field, you can enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
    * <span data-ttu-id="f1285-122">如果午夜之后发生的交易应过帐为前一天的一部分，请选择“是”。</span><span class="sxs-lookup"><span data-stu-id="f1285-122">Select "Yes" if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
    * <span data-ttu-id="f1285-123">选择“是”，以为定义的每种报表方法创建报表。</span><span class="sxs-lookup"><span data-stu-id="f1285-123">Select "Yes" to get statements created for each statement method defined.</span></span> <span data-ttu-id="f1285-124">如果需要为交易数量高的商店提高过帐性能，这可能很有用，因为它将创建许多可并行处理的较小的报表。</span><span class="sxs-lookup"><span data-stu-id="f1285-124">This can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
    * <span data-ttu-id="f1285-125">在“默认客户”字段中，您可以选择客户科目，以用于未经预约而来的客户的销售。</span><span class="sxs-lookup"><span data-stu-id="f1285-125">In the Default customer field, you can select the customer account to use for sales to walk-in customers.</span></span>  


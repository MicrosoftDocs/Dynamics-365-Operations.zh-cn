---
title: 更新非制造环境中的标准成本
description: 本文提供在非制造环境中更新标准成本的指导。
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 79723
ms.assetid: 7ba0c408-2450-4042-9542-6fdf83c12e6c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 09dca3012952b739a75a6930908752fba73a4550
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4422946"
---
# <a name="update-standard-costs-in-a-non-manufacturing-environment"></a><span data-ttu-id="0f19c-103">更新非制造环境中的标准成本</span><span class="sxs-lookup"><span data-stu-id="0f19c-103">Update standard costs in a non-manufacturing environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f19c-104">本文提供在非制造环境中更新标准成本的指导。</span><span class="sxs-lookup"><span data-stu-id="0f19c-104">This article provides guidance for updating standard costs in a non-manufacturing environment.</span></span>

<span data-ttu-id="0f19c-105">以下准则假定将双版本方法用于更新标准成本。</span><span class="sxs-lookup"><span data-stu-id="0f19c-105">The following guidelines assume that you use a two-version approach to update standard cost.</span></span> <span data-ttu-id="0f19c-106">在此方法中，一个成本计算版本包含为冻结期间最初定义的标准成本，并且第二个成本计算版本包含增量更新。</span><span class="sxs-lookup"><span data-stu-id="0f19c-106">In this approach, one costing version contains the standard costs that were originally defined for the frozen period, and the second costing version contains the incremental updates.</span></span> <span data-ttu-id="0f19c-107">每次更新作为在第二个成本计算版本包括的成本记录输入，并且最终启用。</span><span class="sxs-lookup"><span data-stu-id="0f19c-107">Each update is entered as a cost record that is enclosed in the second costing version, and eventually it's enabled.</span></span> <span data-ttu-id="0f19c-108">备选方案，一个版本方法使用最初定义的标准成本集。</span><span class="sxs-lookup"><span data-stu-id="0f19c-108">An alternative, one-version approach uses the set of standard costs that was originally defined.</span></span> <span data-ttu-id="0f19c-109">双版本方法需要您定义第二个成本计算版本。</span><span class="sxs-lookup"><span data-stu-id="0f19c-109">The two-version approach requires that you define a second costing version.</span></span> <span data-ttu-id="0f19c-110">以下是定义此成本计算版本的准则：</span><span class="sxs-lookup"><span data-stu-id="0f19c-110">Here are the guidelines for defining this costing version:</span></span>

-   <span data-ttu-id="0f19c-111">分配 **标准成本** 的成本计算类型。</span><span class="sxs-lookup"><span data-stu-id="0f19c-111">Assign a costing type of **Standard costs**.</span></span>
-   <span data-ttu-id="0f19c-112">分配指示成本计算版本内容的有意义的标识符，例如 **2016-UPDATES**。</span><span class="sxs-lookup"><span data-stu-id="0f19c-112">Assign a meaningful identifier that indicates the contents of the costing version, such as **2016-UPDATES**.</span></span>
-   <span data-ttu-id="0f19c-113">请确保内容包括成本记录。</span><span class="sxs-lookup"><span data-stu-id="0f19c-113">Make sure that the content includes cost records.</span></span>
-   <span data-ttu-id="0f19c-114">允许输入所有站点的成本记录。</span><span class="sxs-lookup"><span data-stu-id="0f19c-114">Allow cost records to be entered for all sites.</span></span> <span data-ttu-id="0f19c-115">如果您指定某一站点，成本记录可以只为该站点输入。</span><span class="sxs-lookup"><span data-stu-id="0f19c-115">If you specify a site, cost records can be entered only for that site.</span></span>
-   <span data-ttu-id="0f19c-116">指示回退原则为 **无**。</span><span class="sxs-lookup"><span data-stu-id="0f19c-116">Indicate a fallback principle of **None**.</span></span> <span data-ttu-id="0f19c-117">该回退原则只应用于制造物料的成本计算。</span><span class="sxs-lookup"><span data-stu-id="0f19c-117">The fallback principle applies only to cost calculations for manufactured items.</span></span>

<span data-ttu-id="0f19c-118">若要纠正、调整或更新新物料的标准成本，请完成以下这些步骤。</span><span class="sxs-lookup"><span data-stu-id="0f19c-118">To correct, adjust, or update standard costs for new items, follow these steps.</span></span>

1.  <span data-ttu-id="0f19c-119">使用 **成本计算版本设置** 页可以使成本数据输入到第二个成本计算版本中。</span><span class="sxs-lookup"><span data-stu-id="0f19c-119">Use the **Costing version** **setup** page to enable cost data to be entered into the second costing version.</span></span> <span data-ttu-id="0f19c-120">可以选择阻止启用未决成本，以便在未决成本已完全和精确定义后允许启用。</span><span class="sxs-lookup"><span data-stu-id="0f19c-120">Optionally, prevent the activation of pending costs, so that activation will be allowed after pending costs have been completely and accurately defined.</span></span> <span data-ttu-id="0f19c-121">您还可以选择在 **开始日期** 字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="0f19c-121">You can also optionally enter a date in the **From date** field.</span></span> <span data-ttu-id="0f19c-122">一般而言，使用您想要启用增量更新时的日期。</span><span class="sxs-lookup"><span data-stu-id="0f19c-122">As a general guideline, use the date when you intend to enable the incremental updates.</span></span> <span data-ttu-id="0f19c-123">或者，则将成本计算版本的 **开始日期** 字段留空，则在每个成本记录的 **开始日期** 字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="0f19c-123">Alternatively, leave the **From date** field blank for the costing version, and then enter a date in the **From date** field for each cost record.</span></span>
2.  <span data-ttu-id="0f19c-124">使用 **物料价格** 页可以输入更新为在第二个成本计算版本报告的物料成本记录。</span><span class="sxs-lookup"><span data-stu-id="0f19c-124">Use the **Item price** page to enter updates as item cost records that are enclosed in the second costing version.</span></span>
3.  <span data-ttu-id="0f19c-125">使用 **物料价格** 报表验证包括在第二个成本计算版本的物料成本记录的完整性和精确性。</span><span class="sxs-lookup"><span data-stu-id="0f19c-125">Use the **Item prices** report to verify the completeness and accuracy of the item cost records that are enclosed in the second costing version.</span></span>
4.  <span data-ttu-id="0f19c-126">使用 **成本计算版本维护** 页更改锁定标志，以便允许启用在第二个成本计算版本中的未决成本记录。</span><span class="sxs-lookup"><span data-stu-id="0f19c-126">Use the **Costing version maintenance** page to change the blocking flag to allow activation of the pending cost records that are enclosed in the second costing version.</span></span>
5.  <span data-ttu-id="0f19c-127">使用 **启用价格** 页（您从 **成本计算版本维护** 页打开的页面）启用第二个成本计算版本中的所有未决物料成本记录。</span><span class="sxs-lookup"><span data-stu-id="0f19c-127">Use the **Activate prices** page (which you open from the **Costing version maintenance** page) to activate all pending item cost records that are enclosed in the second costing version.</span></span> <span data-ttu-id="0f19c-128">您还可以通过单击 **物料价格** 页上的 **启用未决价格** 按钮，启用单独物料的未决成本记录。</span><span class="sxs-lookup"><span data-stu-id="0f19c-128">You can also activate the pending cost records for individual items by clicking the **Activate pending price** button on the **Item price** page.</span></span>
6.  <span data-ttu-id="0f19c-129">若要阻止进一步的数据维护，使用 **成本计算版本设置** 页更改在第二个成本计算版本内的锁定标志。</span><span class="sxs-lookup"><span data-stu-id="0f19c-129">To prevent additional data maintenance, use the **Costing version setup** page to change the blocking flags that are enclosed in the second costing version.</span></span> <span data-ttu-id="0f19c-130">这些锁定策略将阻止输入新的未决成本和启用未决成本。</span><span class="sxs-lookup"><span data-stu-id="0f19c-130">The blocking policies will prevent the entry of new pending costs and the activation of pending costs.</span></span>





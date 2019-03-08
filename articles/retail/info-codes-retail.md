---
title: 信息代码和信息代码组
description: 本文提供有关信息代码、信息代码组以及如何使用它们的概览。
author: mugunthanm
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailInfocodeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 22761
ms.assetid: 99877dba-a6e3-4d88-ba0a-ee5913aea17e
ms.search.region: global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c9cd9197f395b69f65137a59392a4d83d692f6fa
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "340813"
---
# <a name="info-codes-and-info-code-groups"></a><span data-ttu-id="71aee-103">信息代码和信息代码组</span><span class="sxs-lookup"><span data-stu-id="71aee-103">Info codes and info code groups</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="71aee-104">本文提供有关信息代码、信息代码组以及如何使用它们的概览。</span><span class="sxs-lookup"><span data-stu-id="71aee-104">This article provides an overview about info codes, info code groups, and how to use them.</span></span>

<span data-ttu-id="71aee-105">信息代码为您提供一个在销售终端 (POS) 收银机捕获数据的方法。</span><span class="sxs-lookup"><span data-stu-id="71aee-105">Info codes provide a way for you to capture data at a point-of-sale (POS) register.</span></span> <span data-ttu-id="71aee-106">您可以使用此信息代码提示出纳在各种 POS 操作（例如物料销售，物料退还或选择客户）期间输入信息。</span><span class="sxs-lookup"><span data-stu-id="71aee-106">You can use info codes to prompt the cashier to enter information during various actions at the POS, such as item sales, item returns, or selecting customers.</span></span> <span data-ttu-id="71aee-107">出纳可以从列表中选择输入或输入代码、数字、日期或文本。</span><span class="sxs-lookup"><span data-stu-id="71aee-107">Cashiers can select input from a list or enter it as a code, number, date, or text.</span></span> <span data-ttu-id="71aee-108">您可以将信息代码分配给预定义的商店操作、零售物料、付款方式、客户或特定的销售终端活动。</span><span class="sxs-lookup"><span data-stu-id="71aee-108">You can assign info codes to predefined store actions, retail items, payment methods, customers, or specific point-of-sale activities.</span></span> <span data-ttu-id="71aee-109">您可以使用信息代码进行以下操作：</span><span class="sxs-lookup"><span data-stu-id="71aee-109">You can use info codes to do the following:</span></span>

- <span data-ttu-id="71aee-110">在交易记录时间捕获附加信息，例如航班号或退货原因。</span><span class="sxs-lookup"><span data-stu-id="71aee-110">Capture additional information at transaction time, such as a flight number or the reason for a return.</span></span>
- <span data-ttu-id="71aee-111">提示暂存器出纳从特定产品的价格列表中选择。</span><span class="sxs-lookup"><span data-stu-id="71aee-111">Prompt the register cashier to select from a list of prices for specific products.</span></span>
- <span data-ttu-id="71aee-112">执行特定活动时，将子代码链接到信息代码以提示出纳输入。</span><span class="sxs-lookup"><span data-stu-id="71aee-112">Link a subcode to an info code to prompt the cashier for input when performing a specific activity.</span></span> <span data-ttu-id="71aee-113">例如，当客户退回产品时，您可以提示出纳该产品被退回的原因。</span><span class="sxs-lookup"><span data-stu-id="71aee-113">For example, when a customer returns a product, you can prompt the cashier to ask why the product is being returned.</span></span> <span data-ttu-id="71aee-114">然后您可以使用子代码显示出纳可以从中选择的原因列表。</span><span class="sxs-lookup"><span data-stu-id="71aee-114">Then you can use subcodes to display a list of reasons that the cashier can choose from.</span></span>
- <span data-ttu-id="71aee-115">销售的产品为常规销售、折扣销售或免费产品。</span><span class="sxs-lookup"><span data-stu-id="71aee-115">Sell a product as a regular sale, discounted sale, or free product.</span></span>
- <span data-ttu-id="71aee-116">当出纳代在未执行销售操作时打开暂存器抽屉时，提示出纳输入值或从子代码列表中选择。</span><span class="sxs-lookup"><span data-stu-id="71aee-116">Prompt the cashier to enter a value or select from a list of subcodes when the register drawer is opened without performing a sales operation.</span></span>

## <a name="info-codes-group"></a><span data-ttu-id="71aee-117">信息代码组</span><span class="sxs-lookup"><span data-stu-id="71aee-117">Info codes group</span></span>

<span data-ttu-id="71aee-118">在 Dynamics 365 for Retail 中，您可以创建信息代码组。</span><span class="sxs-lookup"><span data-stu-id="71aee-118">In Dynamics 365 for Retail, you can create groups of info codes.</span></span> <span data-ttu-id="71aee-119">信息代码组通过允许您定义少数的信息代码来增加灵活性，然后以更多样化的方式使用它们。</span><span class="sxs-lookup"><span data-stu-id="71aee-119">Info code groups add flexibility by enabling you to define fewer info codes and then use them in more versatile ways.</span></span> <span data-ttu-id="71aee-120">您可以通过以下方式使用信息代码组：</span><span class="sxs-lookup"><span data-stu-id="71aee-120">You can use info code groups in the following ways:</span></span>

- <span data-ttu-id="71aee-121">定义少数信息代码，轻松重复使用。</span><span class="sxs-lookup"><span data-stu-id="71aee-121">Define fewer info codes and easily re-use them.</span></span> <span data-ttu-id="71aee-122">信息代码组中包括的信息代码没有预定义依赖其他信息代码。</span><span class="sxs-lookup"><span data-stu-id="71aee-122">Info codes that are included in info code groups have no predefined dependencies on other info codes.</span></span> <span data-ttu-id="71aee-123">多个信息代码组可以包含相同的信息代码，然后使用优先级按照在任意情形下都有效的顺序为相同的信息代码排序。</span><span class="sxs-lookup"><span data-stu-id="71aee-123">You can include the same info code in multiple info code groups and then use prioritization to present the same info codes in the order that makes sense in any particular situation.</span></span>
- <span data-ttu-id="71aee-124">将信息代码链接到其他信息代码或信息代码组以收集关于产品或交易的信息，而无需为每个场景定义单独的信息代码或链接的信息代码。</span><span class="sxs-lookup"><span data-stu-id="71aee-124">Link info codes to other info codes or info code groups to gather information about a product or transaction without having to define a separate info code or linked info code for each scenario.</span></span>

## <a name="info-code-examples"></a><span data-ttu-id="71aee-125">信息代码示例</span><span class="sxs-lookup"><span data-stu-id="71aee-125">Info code examples</span></span>

<span data-ttu-id="71aee-126">**示例 1：重复使用信息代码**</span><span class="sxs-lookup"><span data-stu-id="71aee-126">**Example 1: Reuse info codes**</span></span>

<span data-ttu-id="71aee-127">您可以链接信息代码，以便在一个信息代码被触发时，另一个信息代码也在之后被立即触发。</span><span class="sxs-lookup"><span data-stu-id="71aee-127">You can link info codes so that when one info code is triggered, another info code is triggered immediately after it.</span></span> <span data-ttu-id="71aee-128">例如，在您销售某些产品时，您可以提示出纳询问客户是否需要购买电池和产品担保。</span><span class="sxs-lookup"><span data-stu-id="71aee-128">For example, when you sell certain products, you can prompt the cashier to ask the customer if they want to purchase batteries and a product warranty.</span></span> <span data-ttu-id="71aee-129">在您销售其他产品时，您可以提示出纳询问客户是否需要购买电池，并收集客户的邮政编码。</span><span class="sxs-lookup"><span data-stu-id="71aee-129">For other products, you can prompt the cashier to ask the customer if they want to purchase batteries and collect their postal code.</span></span> <span data-ttu-id="71aee-130">如果您为这些场景创建链接了的信息代码，必须设置信息代码的每个变量，以便提示出纳索要正确的信息。</span><span class="sxs-lookup"><span data-stu-id="71aee-130">If you create linked info codes for these scenarios, you must set up every variation of the info code so that the cashier is prompted to ask for the right information.</span></span> <span data-ttu-id="71aee-131">如果您使用信息代码组、常用信息代码，例如请求电池，可以设置一次，然后在多个信息代码组中重复使用。</span><span class="sxs-lookup"><span data-stu-id="71aee-131">If you use info code groups, common info codes, such as asking for batteries, can be set up once and then reused in multiple info code groups.</span></span> <span data-ttu-id="71aee-132">您也可以在信息代码组中使用优先级标识显示提示的顺序。</span><span class="sxs-lookup"><span data-stu-id="71aee-132">You can also use prioritization in the info code groups to identify the order in which the prompts are displayed.</span></span>

<span data-ttu-id="71aee-133">**示例 2：将信息代码链接到信息代码组**</span><span class="sxs-lookup"><span data-stu-id="71aee-133">**Example 2: Link info codes to info code groups**</span></span>

<span data-ttu-id="71aee-134">在您销售特定产品时，例如移动设备，总想收集一组特定信息，比如电话号码、移动设备标识 (MEID) 和序列号。</span><span class="sxs-lookup"><span data-stu-id="71aee-134">When you sell certain products, for example mobile devices, you always want to collect a specific set of information, such as telephone number, mobile equipment identifier (MEID), and serial number.</span></span> <span data-ttu-id="71aee-135">但是您还想收集平板电脑与移动电话的区别。</span><span class="sxs-lookup"><span data-stu-id="71aee-135">However, you also want to collect different information for a tablet versus a mobile phone.</span></span> <span data-ttu-id="71aee-136">您可以设置包括提示电话号码、MEID 和序列号的信息代码组，然后将信息代码组链接到单个信息代码。</span><span class="sxs-lookup"><span data-stu-id="71aee-136">You can set up an info code group that includes prompts for the telephone number, MEID, and the serial number, and then link the info code group to an individual info code.</span></span> <span data-ttu-id="71aee-137">在产品特殊化信息代码被触发后，接下来会触发信息代码组以使您能够收集常用数据，而不必为每台设备定义多个链接信息代码集。</span><span class="sxs-lookup"><span data-stu-id="71aee-137">When the product-specific info code is triggered, the info code group can be triggered next to enable you to collect the common data without having to define multiple sets of linked info codes for each device.</span></span>

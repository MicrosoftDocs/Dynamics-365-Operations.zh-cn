---
title: 创建提单
description: 此主题介绍在使用仓库管理流程时如何创建提单。
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8d5caed5553ad1c7aec5db83591024129aab1264
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552061"
---
# <a name="create-a-bill-of-lading"></a><span data-ttu-id="71dc3-103">创建提单</span><span class="sxs-lookup"><span data-stu-id="71dc3-103">Create a bill of lading</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71dc3-104">此主题介绍在使用仓库管理流程时如何创建提单。</span><span class="sxs-lookup"><span data-stu-id="71dc3-104">This topic describes how to create a bill of lading when using warehouse management processes.</span></span>  

<span data-ttu-id="71dc3-105">提单是装运物料的公司和承运人之间的法律文档。</span><span class="sxs-lookup"><span data-stu-id="71dc3-105">A bill of lading is a legal document between the company that ships the items and the carrier.</span></span> <span data-ttu-id="71dc3-106">此文档随装运的物料一并提供，在物料在目的地交货时充当装运收据。</span><span class="sxs-lookup"><span data-stu-id="71dc3-106">The document accompanies the shipped items, and it serves as a receipt of shipment when the items are delivered at the destination.</span></span> <span data-ttu-id="71dc3-107">如果您使用仓库管理，有两种方法生成提单：</span><span class="sxs-lookup"><span data-stu-id="71dc3-107">If you're using warehouse management, there are two ways to generate a bill of lading:</span></span>

  -   <span data-ttu-id="71dc3-108">使用**提单**页面手动创建报表。</span><span class="sxs-lookup"><span data-stu-id="71dc3-108">Create the report manually, using the **Bill of lading** page.</span></span>
  -   <span data-ttu-id="71dc3-109">从**装载计划工作台**生成报表。</span><span class="sxs-lookup"><span data-stu-id="71dc3-109">Generate the report from the **Load planning workbench**.</span></span>

<span data-ttu-id="71dc3-110">如果您从**装载计划工作台**生成提单，负荷状态必须为**已装运**。</span><span class="sxs-lookup"><span data-stu-id="71dc3-110">If you generate the bill of lading from the **Load planning workbench**, the load status must be **Shipped.**</span></span> <span data-ttu-id="71dc3-111">如果一个负荷中有多个装运，提单为每个装运创建。</span><span class="sxs-lookup"><span data-stu-id="71dc3-111">If there's more than one shipment in the load, a bill of lading is created for each shipment.</span></span> <span data-ttu-id="71dc3-112">提单创建后，您可以在**提单**页面对其进行更改。</span><span class="sxs-lookup"><span data-stu-id="71dc3-112">After a bill of lading has been created you can make changes to it on the **Bill of lading** page.</span></span>

## <a name="master-bill-of-lading"></a><span data-ttu-id="71dc3-113">主提单</span><span class="sxs-lookup"><span data-stu-id="71dc3-113">Master bill of lading</span></span>
<span data-ttu-id="71dc3-114">当负荷中存在多个装运，您可以生成主提单。</span><span class="sxs-lookup"><span data-stu-id="71dc3-114">If there's more than one shipment in the load, you can generate a master bill of lading.</span></span> <span data-ttu-id="71dc3-115">这与提单有相同的布局和信息，但包含所有装运的汇总内容。</span><span class="sxs-lookup"><span data-stu-id="71dc3-115">This has the same layout and information as a bill of lading, but contains the summarized content for all the shipments.</span></span> <span data-ttu-id="71dc3-116">如果**当负荷上存在多个装运时创建主提单**在**运输管理参数**页面选项设置为**是**，如果您从**装载计划工作台**创建提单，并且具有多个装运，主提单将自动生成。</span><span class="sxs-lookup"><span data-stu-id="71dc3-116">If the **Create a master bill of lading when there's more than one shipment on a load** option is set to **Yes** on the **Transportation management parameters** page, a master bill of lading is automatically generated if you create a bill of lading from the **Load planning workbench**, and there's more than one shipment.</span></span> <span data-ttu-id="71dc3-117">您还可以通过单击**相关信息** &gt; **提单**获取提单的列表。</span><span class="sxs-lookup"><span data-stu-id="71dc3-117">You can also get a list of the bills of lading by clicking **Related information** &gt; **Bill of lading**.</span></span> <span data-ttu-id="71dc3-118">如果手动创建提单，则可以在**提单**页面创建主提单。</span><span class="sxs-lookup"><span data-stu-id="71dc3-118">If you're creating bills of lading manually, you can create a master bill of lading on the **Bill of lading** page.</span></span>




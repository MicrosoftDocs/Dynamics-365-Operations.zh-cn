---
title: 危险物料
description: 本主题提供有关危险物料文档的信息以及您环境中存储的信息。
author: lachlancashMS
manager: tfehr
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5006f06d90ddcc314a51878e9e21337de7d493e7
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208448"
---
# <a name="hazardous-materials"></a><span data-ttu-id="3cb05-103">危险物料</span><span class="sxs-lookup"><span data-stu-id="3cb05-103">Hazardous materials</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3cb05-104">有关危险物料的信息在产品信息管理中设置。</span><span class="sxs-lookup"><span data-stu-id="3cb05-104">Information about hazardous materials is set up in Product information management.</span></span> <span data-ttu-id="3cb05-105">此模块还提供可以通过仓库管理打印的文档。</span><span class="sxs-lookup"><span data-stu-id="3cb05-105">This module also provides documents that can be printed through warehouse management.</span></span>

<span data-ttu-id="3cb05-106">当您运输分类为危险货物的物料时，必须在装运中提供附加文件。</span><span class="sxs-lookup"><span data-stu-id="3cb05-106">When you ship materials that are classified as dangerous goods, additional paperwork must be included with the shipments.</span></span> <span data-ttu-id="3cb05-107">危险物料功能使客户可以存储分类信息，并将其关联以发放物料。</span><span class="sxs-lookup"><span data-stu-id="3cb05-107">The hazardous materials functionality lets customers store classification information and relate it to release items.</span></span> <span data-ttu-id="3cb05-108">然后，可以使用此信息来帮助准备装运文档。</span><span class="sxs-lookup"><span data-stu-id="3cb05-108">This information can then be used to help prepare shipping documentation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3cb05-109">为了帮助管理危险货物的装运，Microsoft Dynamics 365 Supply Chain Management 使您可以设置与产品相关的附加参考信息。</span><span class="sxs-lookup"><span data-stu-id="3cb05-109">To help manage shipments of dangerous goods, Microsoft Dynamics 365 Supply Chain Management lets you set up additional reference information that is related to products.</span></span> <span data-ttu-id="3cb05-110">您还可以设置附加装运文档。</span><span class="sxs-lookup"><span data-stu-id="3cb05-110">You can also set up additional shipment documents.</span></span> <span data-ttu-id="3cb05-111">但是，系统不会自动遵守您所在国家或地区的法规。</span><span class="sxs-lookup"><span data-stu-id="3cb05-111">However, the system isn't automatically compliant with your country's or region's regulations.</span></span> <span data-ttu-id="3cb05-112">而是充当可以帮助您实施总体计划的工具。</span><span class="sxs-lookup"><span data-stu-id="3cb05-112">Instead, it's a tool that can help your overall program.</span></span>

<span data-ttu-id="3cb05-113">在使用此功能之前，需要进行以下设置：</span><span class="sxs-lookup"><span data-stu-id="3cb05-113">Before you can use this functionality, the following setup is required:</span></span>

- <span data-ttu-id="3cb05-114">**产品信息管理：** 设置可应用于已发布产品的代码。</span><span class="sxs-lookup"><span data-stu-id="3cb05-114">**Product information management:** Set up codes that can be applied to released products.</span></span>
- <span data-ttu-id="3cb05-115">**仓库管理：** 使用附加装运文档打印装运信息。</span><span class="sxs-lookup"><span data-stu-id="3cb05-115">**Warehouse management:** Use additional shipping documents to print shipment information.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="3cb05-116">产品信息管理</span><span class="sxs-lookup"><span data-stu-id="3cb05-116">Product information management</span></span>

<span data-ttu-id="3cb05-117">在“产品信息管理”中，有一系列设置表，您可以在其中添加陆运、空运和海运危险货物清单中提供的参考信息。</span><span class="sxs-lookup"><span data-stu-id="3cb05-117">In Product information management, there is a range of setup tables where you can add the reference information that is provided in the dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="3cb05-118">以下是一些经常引用的法规：</span><span class="sxs-lookup"><span data-stu-id="3cb05-118">Here are some of the regulations that are often referenced:</span></span>

- <span data-ttu-id="3cb05-119">**ADR** – 与国际陆运危险货物有关的法规</span><span class="sxs-lookup"><span data-stu-id="3cb05-119">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="3cb05-120">**CFR 49** – 美国危险货物运输法规</span><span class="sxs-lookup"><span data-stu-id="3cb05-120">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="3cb05-121">**IMDG** – 国际海运危险货物 (IMDG) 法规</span><span class="sxs-lookup"><span data-stu-id="3cb05-121">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="3cb05-122">**IATA** – 国际航空运输协会 (IATA) 危险货物法规</span><span class="sxs-lookup"><span data-stu-id="3cb05-122">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="3cb05-123">这些法规中的每一个都有包含参考代码的危险货物清单。</span><span class="sxs-lookup"><span data-stu-id="3cb05-123">Each of these regulations has a dangerous goods list that includes reference codes.</span></span> <span data-ttu-id="3cb05-124">每种运输类型的清单在共享国际分类中合并在一起。</span><span class="sxs-lookup"><span data-stu-id="3cb05-124">The lists for each type of transport are combined on shared international classifications.</span></span> <span data-ttu-id="3cb05-125">Supply Chain Management 为这些清单中的共享代码提供了参考表。</span><span class="sxs-lookup"><span data-stu-id="3cb05-125">Supply Chain Management provides a reference table for the shared codes in those lists.</span></span> <span data-ttu-id="3cb05-126">每个列表还包含一些可以定义的唯一代码。</span><span class="sxs-lookup"><span data-stu-id="3cb05-126">Each list also has some unique codes that can be defined.</span></span>

<span data-ttu-id="3cb05-127">要开始配置此信息，请创建可用于配置初始参数的规则。</span><span class="sxs-lookup"><span data-stu-id="3cb05-127">To start to configure this information, create a regulation that you can use to configure the initial parameters.</span></span>

## <a name="warehouse-management"></a><span data-ttu-id="3cb05-128">仓库管理</span><span class="sxs-lookup"><span data-stu-id="3cb05-128">Warehouse management</span></span>

<span data-ttu-id="3cb05-129">准备好装运后，可以打印几个新报告。</span><span class="sxs-lookup"><span data-stu-id="3cb05-129">When a shipment is prepared, several new reports can be printed.</span></span> <span data-ttu-id="3cb05-130">这些报告使用您在“产品信息管理”中设置的信息。</span><span class="sxs-lookup"><span data-stu-id="3cb05-130">These reports use the information that you set up in Product information management.</span></span>

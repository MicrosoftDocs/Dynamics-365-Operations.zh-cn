---
title: 危险物料概述
description: 本主题概括介绍与在产品信息管理和仓库管理期间处理和记录危险物料有关的功能。
author: dasani-madipalli
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 34c0a19308bb5159faa9a4ab06bf65e58da0deb1
ms.sourcegitcommit: 5bb36b74935ffe140367fd6ecf956b4857ad12e5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/14/2020
ms.locfileid: "3802741"
---
# <a name="hazardous-materials-overview"></a><span data-ttu-id="4a643-103">危险物料概述</span><span class="sxs-lookup"><span data-stu-id="4a643-103">Hazardous materials overview</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="4a643-104">为了始终遵守装运和运输法规，装运被分类为危险货物的物料的组织必须在装运中提供其他文件。</span><span class="sxs-lookup"><span data-stu-id="4a643-104">To remain compliant with shipping and transport regulations, organizations that ship materials that are classified as dangerous goods must include additional paperwork with their shipments.</span></span> <span data-ttu-id="4a643-105">危险物料功能使客户可以存储与已发布物料有关的信息。</span><span class="sxs-lookup"><span data-stu-id="4a643-105">The hazardous materials feature lets customers store information that is related to released items.</span></span> <span data-ttu-id="4a643-106">然后，可以使用此信息来帮助准备装运文档。</span><span class="sxs-lookup"><span data-stu-id="4a643-106">This information can then be used to help prepare shipping documentation.</span></span> <span data-ttu-id="4a643-107">装运危险货物的组织必须有自己的流程和程序来管理装运流程。</span><span class="sxs-lookup"><span data-stu-id="4a643-107">An organization that ships dangerous goods must have its own processes and procedures for managing the shipping process.</span></span> <span data-ttu-id="4a643-108">Microsoft Dynamics 365 Supply Chain Management 只是可以帮助生成所需文档的工具。</span><span class="sxs-lookup"><span data-stu-id="4a643-108">Microsoft Dynamics 365 Supply Chain Management is just a tool that can help generate the required documents.</span></span>

<span data-ttu-id="4a643-109">下图说明了设置和使用危险物料功能所需的步骤。</span><span class="sxs-lookup"><span data-stu-id="4a643-109">The following diagram illustrates the steps needed to set up and use the hazardous materials feature.</span></span>

<span data-ttu-id="4a643-110">![设置和使用危险物料功能](media/hazmat-overview.png "设置和使用危险物料功能")</span><span class="sxs-lookup"><span data-stu-id="4a643-110">![Setup and use of the hazardous materials feature](media/hazmat-overview.png "Setup and use of the hazardous materials feature")</span></span>

<span data-ttu-id="4a643-111">危险物料功能在“产品信息管理”中设置，提供可通过“仓库管理”打印的文档。</span><span class="sxs-lookup"><span data-stu-id="4a643-111">The hazardous materials feature is set up in Product information management and provides documents that can be printed through Warehouse management.</span></span> <span data-ttu-id="4a643-112">因此，从广义上讲，以下区域是您将检查、设置和使用此功能的功能的两个主要区域：</span><span class="sxs-lookup"><span data-stu-id="4a643-112">Therefore, broadly speaking, those areas are the two main areas where you will review, set up, and use this feature's functionality:</span></span>

- <span data-ttu-id="4a643-113">**产品信息管理** – 设置将应用于已发布产品的代码。</span><span class="sxs-lookup"><span data-stu-id="4a643-113">**Product information management** – Set up the codes that will be applied to a released product.</span></span>
- <span data-ttu-id="4a643-114">**仓库管理** – 处理将要为装运打印的其他装运文档。</span><span class="sxs-lookup"><span data-stu-id="4a643-114">**Warehouse management** – Work with additional shipping documents that will be printed for shipments.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4a643-115">Supply Chain Management 中的危险物料功能提供了一组有用的产品信息字段和相关功能，可以帮助您记录和引用与危险物料有关的信息。</span><span class="sxs-lookup"><span data-stu-id="4a643-115">The hazardous materials features in Supply Chain Management provide a collection of useful product information fields and related functionality that can help you record and reference information that is related to your hazardous products.</span></span> <span data-ttu-id="4a643-116">这些功能还可以帮助您设计和打印包含有关您所装运的任何危险物料的某些信息的装运文档。</span><span class="sxs-lookup"><span data-stu-id="4a643-116">These features can also help you design and print shipment documents that include some of the same information about any hazardous materials that you're shipping.</span></span> <span data-ttu-id="4a643-117">但是，系统不会自动使您遵守您所在国家或地区的所有适用法规。</span><span class="sxs-lookup"><span data-stu-id="4a643-117">However, the system won't automatically make you compliant with all applicable regulations in your country or region.</span></span> <span data-ttu-id="4a643-118">虽然这些工具的目的是帮助您遵守常见法规，但它们本身并不足够，也不能保证一定合规。</span><span class="sxs-lookup"><span data-stu-id="4a643-118">Although these tools are intended to help you comply with common regulations, they are neither sufficient in themselves nor guaranteed to be so.</span></span> <span data-ttu-id="4a643-119">您的组织有责任了解所有适用法规，并采取所有必要的步骤来遵守这些法规。</span><span class="sxs-lookup"><span data-stu-id="4a643-119">Your organization is responsible for being aware of all applicable regulations and for taking all necessary steps to comply with them.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="4a643-120">产品信息管理</span><span class="sxs-lookup"><span data-stu-id="4a643-120">Product information management</span></span>

<span data-ttu-id="4a643-121">“产品信息管理”提供一系列设置表，您可以在其中为各个陆运、空运和海运危险货物清单输入参考信息。</span><span class="sxs-lookup"><span data-stu-id="4a643-121">Product information management provides a range of setup tables where you can enter reference information for the various dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="4a643-122">开发此功能时，参考了以下常见法规：</span><span class="sxs-lookup"><span data-stu-id="4a643-122">The following common regulations were referenced when this functionality was developed:</span></span>

- <span data-ttu-id="4a643-123">**ADR** – 与国际陆运危险货物有关的法规</span><span class="sxs-lookup"><span data-stu-id="4a643-123">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="4a643-124">**CFR 49** – 美国危险货物运输法规</span><span class="sxs-lookup"><span data-stu-id="4a643-124">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="4a643-125">**IMDG** – 国际海运危险货物 (IMDG) 法规</span><span class="sxs-lookup"><span data-stu-id="4a643-125">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="4a643-126">**IATA** – 国际航空运输协会 (IATA) 危险货物法规</span><span class="sxs-lookup"><span data-stu-id="4a643-126">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="4a643-127">每组法规均提供危险货物和参考代码的标准化列表。</span><span class="sxs-lookup"><span data-stu-id="4a643-127">Each set of regulations provides standardized lists of dangerous goods and reference codes.</span></span> <span data-ttu-id="4a643-128">因此，Supply Chain Management 为这些列表中的通用代码提供了参考表。</span><span class="sxs-lookup"><span data-stu-id="4a643-128">Therefore, Supply Chain Management provides a reference table for the common codes on those lists.</span></span> <span data-ttu-id="4a643-129">每个列表还包含一些可以定义的唯一代码。</span><span class="sxs-lookup"><span data-stu-id="4a643-129">Each list also has some unique codes that you can define.</span></span>

<span data-ttu-id="4a643-130">有关如何为危险物料设置法规和值以及如何将值分配给相关产品的详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="4a643-130">For more information about how to set up regulations and values for hazardous materials, and how to assign the values to relevant products, see the following topics:</span></span>

- [<span data-ttu-id="4a643-131">设置危险物料</span><span class="sxs-lookup"><span data-stu-id="4a643-131">Set up hazardous materials</span></span>](hazmat-setup.md)
- [<span data-ttu-id="4a643-132">产品、订单、装运和负荷中的危险物料</span><span class="sxs-lookup"><span data-stu-id="4a643-132">Hazardous materials in products, orders, shipments, and loads</span></span>](hazmat-items.md)

## <a name="warehouse-management"></a><span data-ttu-id="4a643-133">仓库管理</span><span class="sxs-lookup"><span data-stu-id="4a643-133">Warehouse management</span></span>

<span data-ttu-id="4a643-134">在“仓库管理”中准备装运时，您能够打印使用您在“产品信息管理”中设置的信息的多个新报表。</span><span class="sxs-lookup"><span data-stu-id="4a643-134">When you prepare a shipment in Warehouse management, you will be able to print several new reports that use the information that you set up in Product information management.</span></span> <span data-ttu-id="4a643-135">有关可用报表以及如何使用它们的详细信息，请参阅[危险物料查询和报表](hazmat-reports.md)。</span><span class="sxs-lookup"><span data-stu-id="4a643-135">For more information about the available reports and how to use them, see [Hazardous materials inquiries and reports](hazmat-reports.md).</span></span>

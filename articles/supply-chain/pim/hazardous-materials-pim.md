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
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: kamaybac
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: d27ec5b65cc607c22d97c1dc44bb573bc2772611
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243169"
---
# <a name="hazardous-materials"></a><span data-ttu-id="63c86-103">危险物料</span><span class="sxs-lookup"><span data-stu-id="63c86-103">Hazardous materials</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="63c86-104">有关危险物料的信息在产品信息管理中设置。</span><span class="sxs-lookup"><span data-stu-id="63c86-104">Information about hazardous materials is set up in Product information management.</span></span> <span data-ttu-id="63c86-105">此模块还提供可以通过仓库管理打印的文档。</span><span class="sxs-lookup"><span data-stu-id="63c86-105">This module also provides documents that can be printed through warehouse management.</span></span>

<span data-ttu-id="63c86-106">当您运输分类为危险货物的物料时，必须在装运中提供附加文件。</span><span class="sxs-lookup"><span data-stu-id="63c86-106">When you ship materials that are classified as dangerous goods, additional paperwork must be included with the shipments.</span></span> <span data-ttu-id="63c86-107">危险物料功能使客户可以存储分类信息，并将其关联以发放物料。</span><span class="sxs-lookup"><span data-stu-id="63c86-107">The hazardous materials functionality lets customers store classification information and relate it to release items.</span></span> <span data-ttu-id="63c86-108">然后，可以使用此信息来帮助准备装运文档。</span><span class="sxs-lookup"><span data-stu-id="63c86-108">This information can then be used to help prepare shipping documentation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="63c86-109">Microsoft Dynamics 365 Supply Chain Management 中的危险物料功能提供了一组有用的产品信息字段和相关功能，可以帮助您记录和引用与危险物料有关的信息。</span><span class="sxs-lookup"><span data-stu-id="63c86-109">The hazardous materials features in Microsoft Dynamics 365 Supply Chain Management provide a collection of useful product information fields and related functionality that can help you record and reference information that is related to your hazardous products.</span></span> <span data-ttu-id="63c86-110">这些功能还可以帮助您设计和打印包含有关您所装运的任何危险物料的某些信息的装运文档。</span><span class="sxs-lookup"><span data-stu-id="63c86-110">These features can also help you design and print shipment documents that include some of the same information about any hazardous materials that you're shipping.</span></span> <span data-ttu-id="63c86-111">但是，系统不会自动使您遵守您所在国家或地区的所有适用法规。</span><span class="sxs-lookup"><span data-stu-id="63c86-111">However, the system won't automatically make you compliant with all applicable regulations in your country or region.</span></span> <span data-ttu-id="63c86-112">虽然这些工具的目的是帮助您遵守常见法规，但它们本身并不足够，也不能保证一定合规。</span><span class="sxs-lookup"><span data-stu-id="63c86-112">Although these tools are intended to help you comply with common regulations, they are neither sufficient in themselves nor guaranteed to be so.</span></span> <span data-ttu-id="63c86-113">您的组织有责任了解所有适用法规，并采取所有必要的步骤来遵守这些法规。</span><span class="sxs-lookup"><span data-stu-id="63c86-113">Your organization is responsible for being aware of all applicable regulations and for taking all necessary steps to comply with them.</span></span>

<span data-ttu-id="63c86-114">在使用此功能之前，需要进行以下设置：</span><span class="sxs-lookup"><span data-stu-id="63c86-114">Before you can use this functionality, the following setup is required:</span></span>

- <span data-ttu-id="63c86-115">**产品信息管理：** 设置可应用于已发布产品的代码。</span><span class="sxs-lookup"><span data-stu-id="63c86-115">**Product information management:** Set up codes that can be applied to released products.</span></span>
- <span data-ttu-id="63c86-116">**仓库管理：** 使用附加装运文档打印装运信息。</span><span class="sxs-lookup"><span data-stu-id="63c86-116">**Warehouse management:** Use additional shipping documents to print shipment information.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="63c86-117">产品信息管理</span><span class="sxs-lookup"><span data-stu-id="63c86-117">Product information management</span></span>

<span data-ttu-id="63c86-118">在“产品信息管理”中，有一系列设置表，您可以在其中添加陆运、空运和海运危险货物清单中提供的参考信息。</span><span class="sxs-lookup"><span data-stu-id="63c86-118">In Product information management, there is a range of setup tables where you can add the reference information that is provided in the dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="63c86-119">以下是一些经常引用的法规：</span><span class="sxs-lookup"><span data-stu-id="63c86-119">Here are some of the regulations that are often referenced:</span></span>

- <span data-ttu-id="63c86-120">**ADR** – 与国际陆运危险货物有关的法规</span><span class="sxs-lookup"><span data-stu-id="63c86-120">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="63c86-121">**CFR 49** – 美国危险货物运输法规</span><span class="sxs-lookup"><span data-stu-id="63c86-121">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="63c86-122">**IMDG** – 国际海运危险货物 (IMDG) 法规</span><span class="sxs-lookup"><span data-stu-id="63c86-122">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="63c86-123">**IATA** – 国际航空运输协会 (IATA) 危险货物法规</span><span class="sxs-lookup"><span data-stu-id="63c86-123">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="63c86-124">这些法规中的每一个都有包含参考代码的危险货物清单。</span><span class="sxs-lookup"><span data-stu-id="63c86-124">Each of these regulations has a dangerous goods list that includes reference codes.</span></span> <span data-ttu-id="63c86-125">每种运输类型的清单在共享国际分类中合并在一起。</span><span class="sxs-lookup"><span data-stu-id="63c86-125">The lists for each type of transport are combined on shared international classifications.</span></span> <span data-ttu-id="63c86-126">Supply Chain Management 为这些清单中的共享代码提供了参考表。</span><span class="sxs-lookup"><span data-stu-id="63c86-126">Supply Chain Management provides a reference table for the shared codes in those lists.</span></span> <span data-ttu-id="63c86-127">每个列表还包含一些可以定义的唯一代码。</span><span class="sxs-lookup"><span data-stu-id="63c86-127">Each list also has some unique codes that can be defined.</span></span>

<span data-ttu-id="63c86-128">要开始配置此信息，请创建可用于配置初始参数的规则。</span><span class="sxs-lookup"><span data-stu-id="63c86-128">To start to configure this information, create a regulation that you can use to configure the initial parameters.</span></span>

## <a name="warehouse-management"></a><span data-ttu-id="63c86-129">仓库管理</span><span class="sxs-lookup"><span data-stu-id="63c86-129">Warehouse management</span></span>

<span data-ttu-id="63c86-130">准备好装运后，可以打印几个新报告。</span><span class="sxs-lookup"><span data-stu-id="63c86-130">When a shipment is prepared, several new reports can be printed.</span></span> <span data-ttu-id="63c86-131">这些报告使用您在“产品信息管理”中设置的信息。</span><span class="sxs-lookup"><span data-stu-id="63c86-131">These reports use the information that you set up in Product information management.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
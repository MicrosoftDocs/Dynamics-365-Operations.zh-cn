---
title: Dynamics 365 全球化服务
description: 本主题提供 Microsoft Dynamics 365 全球化服务的概述。
author: JaneA07
manager: AnnBe
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 8c6f3b7fb4dec0dffe55014e9e2d60620dc3b193
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893040"
---
# <a name="dynamics-365-globalization-services"></a><span data-ttu-id="663aa-103">Dynamics 365 全球化服务</span><span class="sxs-lookup"><span data-stu-id="663aa-103">Dynamics 365 globalization services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="663aa-104">可以配置以下全球化服务以扩展某些 Microsoft Dynamics 365 联机服务中存在的功能：</span><span class="sxs-lookup"><span data-stu-id="663aa-104">The following globalization services can be configured to extend the capabilities that exist in some Microsoft Dynamics 365 online services:</span></span>

- <span data-ttu-id="663aa-105">**Regulatory Configuration Service (RCS)** 支持配置不同类型的电子文档和报表。</span><span class="sxs-lookup"><span data-stu-id="663aa-105">**Regulatory Configuration Service (RCS)** supports the configuration of different types of electronic documents and reports.</span></span> <span data-ttu-id="663aa-106">RCS 提供电子报告 (ER) 设计器的增强版本，其中配置存储库是独立服务。</span><span class="sxs-lookup"><span data-stu-id="663aa-106">RCS provides an enhanced version of the Electronic reporting (ER) designer where the configuration repository is a standalone service.</span></span> <span data-ttu-id="663aa-107">有关详细信息，请参阅 [Regulatory Configuration Service](rcs-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="663aa-107">For more information, see [Regulatory Configuration Service](rcs-overview.md).</span></span>
- <span data-ttu-id="663aa-108">**电子开票** 将转换的可配置格式、数字签名和连接性的可配置集成与外部 Web 服务（包括认证和响应处理）集成在一起。</span><span class="sxs-lookup"><span data-stu-id="663aa-108">**Electronic Invoicing** brings together configurable formats for transformations, digital signatures, and configurable integrations for connectivity with external web services, including certification and response handling.</span></span> <span data-ttu-id="663aa-109">有关详细信息，请参阅[电子开票](e-invoicing-service-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="663aa-109">For more information, see [Electronic Invoicing](e-invoicing-service-overview.md).</span></span>
- <span data-ttu-id="663aa-110">**税务计算** 通过支持多个纳税人标识号、税码确定、税务计算设计器和运行时引擎提供增强的灵活性，以符合全球范围的复杂税务法规。</span><span class="sxs-lookup"><span data-stu-id="663aa-110">**Tax Calculation** provides enhanced flexibility by supporting multiple tax IDs, tax code determination, the tax calculation designer, and a runtime engine to comply with complex tax regulations worldwide.</span></span> <span data-ttu-id="663aa-111">有关详细信息，请参阅[税务计算](global-tax-calcuation-service-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="663aa-111">For more information, see [Tax Calculation](global-tax-calcuation-service-overview.md).</span></span>

<span data-ttu-id="663aa-112">这些全球化服务提供与以下 Dynamics 365 联机服务的现成集成。</span><span class="sxs-lookup"><span data-stu-id="663aa-112">These globalization services provide out-of-box integration with the following Dynamics 365 online services.</span></span>

| <span data-ttu-id="663aa-113">联机服务</span><span class="sxs-lookup"><span data-stu-id="663aa-113">Online service</span></span> | <span data-ttu-id="663aa-114">RCS</span><span class="sxs-lookup"><span data-stu-id="663aa-114">RCS</span></span> | <span data-ttu-id="663aa-115">电子开票</span><span class="sxs-lookup"><span data-stu-id="663aa-115">Electronic Invoicing</span></span> | <span data-ttu-id="663aa-116">税款计算(预览版)</span><span class="sxs-lookup"><span data-stu-id="663aa-116">Tax Calculation (Preview)</span></span> |
|----------------|-----|----------------------|---------------------------|
| <span data-ttu-id="663aa-117">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="663aa-117">Dynamics 365 Finance</span></span> | <span data-ttu-id="663aa-118">是</span><span class="sxs-lookup"><span data-stu-id="663aa-118">Yes</span></span> | <span data-ttu-id="663aa-119">是</span><span class="sxs-lookup"><span data-stu-id="663aa-119">Yes</span></span> | <span data-ttu-id="663aa-120">是</span><span class="sxs-lookup"><span data-stu-id="663aa-120">Yes</span></span> | 
| <span data-ttu-id="663aa-121">Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="663aa-121">Dynamics 365 Supply Chain Management</span></span> | <span data-ttu-id="663aa-122">是</span><span class="sxs-lookup"><span data-stu-id="663aa-122">Yes</span></span> | <span data-ttu-id="663aa-123">是</span><span class="sxs-lookup"><span data-stu-id="663aa-123">Yes</span></span> | <span data-ttu-id="663aa-124">是</span><span class="sxs-lookup"><span data-stu-id="663aa-124">Yes</span></span> | 
| <span data-ttu-id="663aa-125">Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="663aa-125">Dynamics 365 Project Operations</span></span> | <span data-ttu-id="663aa-126">是</span><span class="sxs-lookup"><span data-stu-id="663aa-126">Yes</span></span> | <span data-ttu-id="663aa-127">是</span><span class="sxs-lookup"><span data-stu-id="663aa-127">Yes</span></span> | <span data-ttu-id="663aa-128">不适用</span><span class="sxs-lookup"><span data-stu-id="663aa-128">Not applicable</span></span> | 
| <span data-ttu-id="663aa-129">Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="663aa-129">Dynamics 365 Commerce</span></span> | <span data-ttu-id="663aa-130">是</span><span class="sxs-lookup"><span data-stu-id="663aa-130">Yes</span></span> | <span data-ttu-id="663aa-131">不适用</span><span class="sxs-lookup"><span data-stu-id="663aa-131">Not applicable</span></span> | <span data-ttu-id="663aa-132">不适用</span><span class="sxs-lookup"><span data-stu-id="663aa-132">Not applicable</span></span> | 

> [!NOTE]
> <span data-ttu-id="663aa-133">由于 RCS 的 Azure 地理位置（地区）的可用性不同，此服务的配置可能会导致客户数据传输到为适用 Dynamics 365 联机服务选择的地区之外。</span><span class="sxs-lookup"><span data-stu-id="663aa-133">Because of differences in the availability of Azure geographic locations (geos) for RCS, configuration of this service might cause customer data to be transferred outside the geo that is selected for the applicable Dynamics 365 online service.</span></span> <span data-ttu-id="663aa-134">有关详细信息，请参阅 [Dynamics 365 和 Power Platform：可用性、数据位置、语言和本地化](https://aka.ms/rcs/D365Productavailabilityguide)。</span><span class="sxs-lookup"><span data-stu-id="663aa-134">For more information, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/rcs/D365Productavailabilityguide).</span></span>
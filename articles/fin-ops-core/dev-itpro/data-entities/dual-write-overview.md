---
title: 与 Common Data Service 的近实时数据集成
description: 本主题提供 Finance and Operations 与 Common Data Service 之间的集成概述。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 11a5792c9c039eb76337309ef2fdb2b994ce191a
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772379"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a><span data-ttu-id="c1ed9-103">与 Common Data Service 的近实时数据集成</span><span class="sxs-lookup"><span data-stu-id="c1ed9-103">Near-real-time data integration with Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c1ed9-104">在现在的数字世界中，业务生态系统把 Microsoft Dynamics 365 应用程序作为整体使用。</span><span class="sxs-lookup"><span data-stu-id="c1ed9-104">In the current digital world, business ecosystems use Microsoft Dynamics 365 applications as a whole.</span></span> <span data-ttu-id="c1ed9-105">因为来自人员、客户、运营和物联网 (IoT) 设备的数据传输到一个源，所以可能发生数字反馈循环。</span><span class="sxs-lookup"><span data-stu-id="c1ed9-105">Because data from people, customers, operations, and Internet of Things (IoT) devices flows into one source, there is an opportunity for digital feedback loops.</span></span> <span data-ttu-id="c1ed9-106">Finance and Operations 应用与其他 Dynamics 365 应用程序之间的集成对实现此体验至关重要。</span><span class="sxs-lookup"><span data-stu-id="c1ed9-106">To achieve this experience, integration between Finance and Operations apps and other Dynamics 365 applications is essential.</span></span> <span data-ttu-id="c1ed9-107">有些应用程序以 Common Data Service 为基础。</span><span class="sxs-lookup"><span data-stu-id="c1ed9-107">Some applications are built on top of Common Data Service.</span></span> <span data-ttu-id="c1ed9-108">Finance and Operations 应用数据与 Common Data Service 之间的集成让其他应用程序可以与 Finance and Operations 之间连贯、流畅地通信。</span><span class="sxs-lookup"><span data-stu-id="c1ed9-108">Integration between Finance and Operations apps data with Common Data Service lets other applications communicate coherently and fluently with Finance and Operations.</span></span>

<span data-ttu-id="c1ed9-109">Finance and Operations 应用和 Common Data Service 通过双写入框架提供 Finance and Operations 应用与其他 Dynamics 365 应用程序之间的近实时数据同步。</span><span class="sxs-lookup"><span data-stu-id="c1ed9-109">Finance and Operations apps and Common Data Service provide near-real-time data synchronization between Finance and Operations apps and other Dynamics 365 applications via a dual-write framework.</span></span> <span data-ttu-id="c1ed9-110">范围广阔，跨越应用程序的 28 个外围应用。</span><span class="sxs-lookup"><span data-stu-id="c1ed9-110">The coverage is broad and spans 28 surface areas of the application.</span></span> <span data-ttu-id="c1ed9-111">目的是通过用于连接应用程序之间的业务流程的无缝数据流来提供“单 Dynamics 365”用户体验。</span><span class="sxs-lookup"><span data-stu-id="c1ed9-111">The goal is to provide a "One Dynamics 365" user experience through seamless data flows that connect business processes across applications.</span></span>

![体系结构概览图](media/dual-write-overview.jpg)

<span data-ttu-id="c1ed9-113">可以采用以下价值主张：</span><span class="sxs-lookup"><span data-stu-id="c1ed9-113">The following value propositions are available:</span></span>

+ [<span data-ttu-id="c1ed9-114">Common Data Service 中的组织层次结构</span><span class="sxs-lookup"><span data-stu-id="c1ed9-114">Organization hierarchy in Common Data Service</span></span>](dual-write-organization.md)
+ [<span data-ttu-id="c1ed9-115">Common Data Service 中的公司概念</span><span class="sxs-lookup"><span data-stu-id="c1ed9-115">Company concept in Common Data Service</span></span>](dual-write-company.md)
+ [<span data-ttu-id="c1ed9-116">集成客户主控</span><span class="sxs-lookup"><span data-stu-id="c1ed9-116">Integrated customer master</span></span>](dual-write-customer.md)
+ [<span data-ttu-id="c1ed9-117">集成的分类帐</span><span class="sxs-lookup"><span data-stu-id="c1ed9-117">Integrated ledger</span></span>](dual-write-ledger.md)
+ [<span data-ttu-id="c1ed9-118">通用产品体验</span><span class="sxs-lookup"><span data-stu-id="c1ed9-118">Unified product experience</span></span>](dual-write-product.md)
+ [<span data-ttu-id="c1ed9-119">集成供应商主控</span><span class="sxs-lookup"><span data-stu-id="c1ed9-119">Integrated vendor master</span></span>](dual-write-vendor.md)
+ [<span data-ttu-id="c1ed9-120">集成的站点和仓库</span><span class="sxs-lookup"><span data-stu-id="c1ed9-120">Integrated sites and warehouses</span></span>](dual-write-sites-and-warehouses.md)
+ [<span data-ttu-id="c1ed9-121">集成的税收主数据</span><span class="sxs-lookup"><span data-stu-id="c1ed9-121">Integrated tax master</span></span>](dual-write-tax.md)

## <a name="system-requirements"></a><span data-ttu-id="c1ed9-122">系统要求</span><span class="sxs-lookup"><span data-stu-id="c1ed9-122">System requirements</span></span>

<span data-ttu-id="c1ed9-123">同步、双向、近实时数据流需要以下版本：</span><span class="sxs-lookup"><span data-stu-id="c1ed9-123">Synchronous, bidirectional, near-real-time data flows require the following versions:</span></span>

+ <span data-ttu-id="c1ed9-124">带平台更新 28 或更高版本的 Microsoft Dynamics 365 for Finance and Operations 版本 10.0.4（2019 年 7 月）</span><span class="sxs-lookup"><span data-stu-id="c1ed9-124">Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019) with Platform update 28, or later</span></span>
+ <span data-ttu-id="c1ed9-125">Microsoft Dynamics 365 for Customer Engagement，平台版本 9.1 (4.2) 或更高版本</span><span class="sxs-lookup"><span data-stu-id="c1ed9-125">Microsoft Dynamics 365 for Customer Engagement, Platform version 9.1 (4.2) or later</span></span>

## <a name="setup-instructions"></a><span data-ttu-id="c1ed9-126">设置说明</span><span class="sxs-lookup"><span data-stu-id="c1ed9-126">Setup instructions</span></span>

<span data-ttu-id="c1ed9-127">按照以下步骤设置 Finance and Operations 应用与 Common Data Service 之间的集成。</span><span class="sxs-lookup"><span data-stu-id="c1ed9-127">Follow these steps to set up integration between Finance and Operations apps and Common Data Service.</span></span>
    
1. <span data-ttu-id="c1ed9-128">有关设置双写入系统，请参阅[分步指南](https://aka.ms/dualwrite-docs)中的“发布双写入预览版”。</span><span class="sxs-lookup"><span data-stu-id="c1ed9-128">For the setup of the dual-write system, see the [step-by-step guide](https://aka.ms/dualwrite-docs) on Announcing Dual Write Preview.</span></span>
2. <span data-ttu-id="c1ed9-129">从[Finance and Operations、Common Data Service 和 Customer Engagement 集成](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer 组下载和安装解决方案。</span><span class="sxs-lookup"><span data-stu-id="c1ed9-129">Download and install the solution from the [Finance and Operations, Common Data Service, and Customer Engagement Integration](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer group.</span></span> <span data-ttu-id="c1ed9-130">包中包含五个解决方案：</span><span class="sxs-lookup"><span data-stu-id="c1ed9-130">The package contains five solutions:</span></span>

    + <span data-ttu-id="c1ed9-131">Dynamics365Company</span><span class="sxs-lookup"><span data-stu-id="c1ed9-131">Dynamics365Company</span></span>
    + <span data-ttu-id="c1ed9-132">CurrencyExchangeRates</span><span class="sxs-lookup"><span data-stu-id="c1ed9-132">CurrencyExchangeRates</span></span>
    + <span data-ttu-id="c1ed9-133">Dynamics365FinanceAndOperationsCommon</span><span class="sxs-lookup"><span data-stu-id="c1ed9-133">Dynamics365FinanceAndOperationsCommon</span></span>
    + <span data-ttu-id="c1ed9-134">Dynamics365FinanceCommon</span><span class="sxs-lookup"><span data-stu-id="c1ed9-134">Dynamics365FinanceCommon</span></span>
    + <span data-ttu-id="c1ed9-135">Dynamics365SupplyChainCommon</span><span class="sxs-lookup"><span data-stu-id="c1ed9-135">Dynamics365SupplyChainCommon</span></span>

3. <span data-ttu-id="c1ed9-136">遵循[同步初始参考数据](dual-write-initial.md)的执行顺序。</span><span class="sxs-lookup"><span data-stu-id="c1ed9-136">Follow the execution order for [synchronizing initial reference data](dual-write-initial.md).</span></span>
4. <span data-ttu-id="c1ed9-137">如果遇到双写入同步问题，请参阅[数据集成疑难解答指南](dual-write-troubleshooting.md)。</span><span class="sxs-lookup"><span data-stu-id="c1ed9-137">If you encounter dual-write synchronization issues, see the [Troubleshooting guide for data integration](dual-write-troubleshooting.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c1ed9-138">不能并排运行双写入和[目标客户到现金](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct)。</span><span class="sxs-lookup"><span data-stu-id="c1ed9-138">You can’t run dual-write and [Prospect to cash](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) side-by-side.</span></span> <span data-ttu-id="c1ed9-139">如果正在运行目标客户到现金解决方案，则必须将其卸载。</span><span class="sxs-lookup"><span data-stu-id="c1ed9-139">If you're running the Prospect to cash solution, you must uninstall it.</span></span> <span data-ttu-id="c1ed9-140">还必须禁用目标客户到现金解决方案中的客户和供应商双写入模板。</span><span class="sxs-lookup"><span data-stu-id="c1ed9-140">You must also disable the customer and vendor dual-write templates that are part of the Prospect to cash solution.</span></span>

---
title: Finance and Operations 与 Common Data Service 之间的近实时数据集成
description: 本主题提供 Microsoft Dynamics 365 for Finance and Operations 与 Common Data Service 之间的集成概述。
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
ms.openlocfilehash: aa614c8e6a79a3f7a4f8f2f99f1f1bd1a67ac921
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797220"
---
# <a name="near-real-time-data-integration-between-finance-and-operations-and-common-data-service"></a><span data-ttu-id="1aa3c-103">Finance and Operations 与 Common Data Service 之间的近实时数据集成</span><span class="sxs-lookup"><span data-stu-id="1aa3c-103">Near-real-time data integration between Finance and Operations and Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="1aa3c-104">在现在的数字世界中，业务生态系统把 Microsoft Dynamics 365 套件作为整体使用。</span><span class="sxs-lookup"><span data-stu-id="1aa3c-104">In the current digital world, business ecosystems use the Microsoft Dynamics 365 suite as a whole.</span></span> <span data-ttu-id="1aa3c-105">因为来自人员、客户、运营和物联网 (IoT) 设备的数据传输到一个源，所以可能发生数字反馈循环。</span><span class="sxs-lookup"><span data-stu-id="1aa3c-105">Because data from people, customers, operations, and Internet of Things (IoT) devices flows into one source, there is an opportunity for digital feedback loops.</span></span> <span data-ttu-id="1aa3c-106">Dynamics 365 for Finance and Operations 与 Dynamics 365 for Customer Engagement 应用程序之间的集成对实现此体验至关重要。</span><span class="sxs-lookup"><span data-stu-id="1aa3c-106">To achieve this experience, integration between Dynamics 365 for Finance and Operations and Dynamics 365 for Customer Engagement applications is essential.</span></span> <span data-ttu-id="1aa3c-107">Customer Engagement 应用程序以 Common Data Service 为基础。</span><span class="sxs-lookup"><span data-stu-id="1aa3c-107">Customer Engagement applications are built on top of Common Data Service.</span></span> <span data-ttu-id="1aa3c-108">Finance and Operations 数据与 Common Data Service 之间的集成让 Customer Engagement 应用程序可以与 Finance and Operations 之间连贯、流畅地通信。</span><span class="sxs-lookup"><span data-stu-id="1aa3c-108">Integration between Finance and Operations data with Common Data Service lets Customer Engagement applications communicate coherently and fluently with Finance and Operations.</span></span>

<span data-ttu-id="1aa3c-109">Finance and Operations 和 Common Data Service 通过双写入框架提供 Finance and Operations 与 Customer Engagement 应用程序之间的近实时数据同步。</span><span class="sxs-lookup"><span data-stu-id="1aa3c-109">Finance and Operations and Common Data Service provide near-real-time data synchronization between Finance and Operations and Customer Engagement applications via a dual-write framework.</span></span> <span data-ttu-id="1aa3c-110">范围广阔，跨越 Finance and Operations 的 28 个外围应用。</span><span class="sxs-lookup"><span data-stu-id="1aa3c-110">The coverage is broad and spans 28 surface areas of Finance and Operations.</span></span> <span data-ttu-id="1aa3c-111">目的是通过用于连接应用程序之间的业务流程的无缝数据流来提供“单 Dynamics 365”用户体验。</span><span class="sxs-lookup"><span data-stu-id="1aa3c-111">The goal is to provide a "One Dynamics 365" user experience through seamless data flows that connect business processes across applications.</span></span>

![体系结构概览图](media/dual-write-overview.jpg)

<span data-ttu-id="1aa3c-113">客户可以采用以下价值主张：</span><span class="sxs-lookup"><span data-stu-id="1aa3c-113">The following value propositions are available for customers:</span></span>

+ [<span data-ttu-id="1aa3c-114">Common Data Service 中的组织层次结构</span><span class="sxs-lookup"><span data-stu-id="1aa3c-114">Organization hierarchy in Common Data Service</span></span>](dual-write-organization.md)
+ [<span data-ttu-id="1aa3c-115">Common Data Service 中的公司概念</span><span class="sxs-lookup"><span data-stu-id="1aa3c-115">Company concept in Common Data Service</span></span>](dual-write-company.md)
+ [<span data-ttu-id="1aa3c-116">集成客户主控</span><span class="sxs-lookup"><span data-stu-id="1aa3c-116">Integrated customer master</span></span>](dual-write-customer.md)
+ [<span data-ttu-id="1aa3c-117">集成供应商主控</span><span class="sxs-lookup"><span data-stu-id="1aa3c-117">Integrated vendor master</span></span>](dual-write-vendor.md)
+ <span data-ttu-id="1aa3c-118">统一基础产品</span><span class="sxs-lookup"><span data-stu-id="1aa3c-118">Unified product master</span></span>

## <a name="system-requirements"></a><span data-ttu-id="1aa3c-119">系统要求</span><span class="sxs-lookup"><span data-stu-id="1aa3c-119">System requirements</span></span>

<span data-ttu-id="1aa3c-120">同步、双向、近实时数据流需要以下版本：</span><span class="sxs-lookup"><span data-stu-id="1aa3c-120">Synchronous, bidirectional, near-real-time data flows require the following versions:</span></span>

+ <span data-ttu-id="1aa3c-121">带平台更新 28 或更高版本的 Microsoft Dynamics 365 for Finance and Operations 版本 10.0.4（2019 年 7 月）</span><span class="sxs-lookup"><span data-stu-id="1aa3c-121">Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019) with Platform update 28, or later</span></span>
+ <span data-ttu-id="1aa3c-122">Microsoft Dynamics 365 for Customer Engagement，平台版本 9.1 (4.2) 或更高版本</span><span class="sxs-lookup"><span data-stu-id="1aa3c-122">Microsoft Dynamics 365 for Customer Engagement, Platform version 9.1 (4.2) or later</span></span>

## <a name="setup-instructions"></a><span data-ttu-id="1aa3c-123">设置说明</span><span class="sxs-lookup"><span data-stu-id="1aa3c-123">Setup instructions</span></span>

<span data-ttu-id="1aa3c-124">按照以下步骤设置 Finance and Operations 与 Common Data Service 之间的集成。</span><span class="sxs-lookup"><span data-stu-id="1aa3c-124">Follow these steps to set up integration between Finance and Operations and Common Data Service.</span></span>
    
1. <span data-ttu-id="1aa3c-125">有关设置双写入系统，请参阅[分步指南](https://aka.ms/dualwrite-docs)中的“发布双写入预览版”。</span><span class="sxs-lookup"><span data-stu-id="1aa3c-125">For the setup of the dual-write system, see the [step-by-step guide](https://aka.ms/dualwrite-docs) on Announcing Dual Write Preview.</span></span>
2. <span data-ttu-id="1aa3c-126">从[Finance and Operations、Common Data Service 和 Customer Engagement 集成](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer 组下载和安装解决方案。</span><span class="sxs-lookup"><span data-stu-id="1aa3c-126">Download and install the solution from the [Finance and Operations, Common Data Service, and Customer Engagement Integration](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer group.</span></span> <span data-ttu-id="1aa3c-127">包中包含五个解决方案：</span><span class="sxs-lookup"><span data-stu-id="1aa3c-127">The package contains five solutions:</span></span>

    + <span data-ttu-id="1aa3c-128">Dynamics365Company</span><span class="sxs-lookup"><span data-stu-id="1aa3c-128">Dynamics365Company</span></span>
    + <span data-ttu-id="1aa3c-129">CurrencyExchangeRates</span><span class="sxs-lookup"><span data-stu-id="1aa3c-129">CurrencyExchangeRates</span></span>
    + <span data-ttu-id="1aa3c-130">Dynamics365FinanceAndOperationsCommon</span><span class="sxs-lookup"><span data-stu-id="1aa3c-130">Dynamics365FinanceAndOperationsCommon</span></span>
    + <span data-ttu-id="1aa3c-131">Dynamics365FinanceCommon</span><span class="sxs-lookup"><span data-stu-id="1aa3c-131">Dynamics365FinanceCommon</span></span>
    + <span data-ttu-id="1aa3c-132">Dynamics365SupplyChainCommon</span><span class="sxs-lookup"><span data-stu-id="1aa3c-132">Dynamics365SupplyChainCommon</span></span>

3. <span data-ttu-id="1aa3c-133">遵循[同步初始参考数据](dual-write-initial.md)的执行顺序。</span><span class="sxs-lookup"><span data-stu-id="1aa3c-133">Follow the execution order for [synchronizing initial reference data](dual-write-initial.md).</span></span>
4. <span data-ttu-id="1aa3c-134">如果遇到双写入同步问题，请参阅[数据集成疑难解答指南](dual-write-troubleshooting.md)。</span><span class="sxs-lookup"><span data-stu-id="1aa3c-134">If you encounter dual-write synchronization issues, see the [Troubleshooting guide for data integration](dual-write-troubleshooting.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1aa3c-135">不能并排运行双写入和[目标客户到现金](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct)。</span><span class="sxs-lookup"><span data-stu-id="1aa3c-135">You can’t run dual-write and [Prospect to cash](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) side-by-side.</span></span> <span data-ttu-id="1aa3c-136">如果正在运行目标客户到现金解决方案，则必须将其卸载。</span><span class="sxs-lookup"><span data-stu-id="1aa3c-136">If you're running the Prospect to cash solution, you must uninstall it.</span></span> <span data-ttu-id="1aa3c-137">还必须禁用目标客户到现金解决方案中的客户和供应商双写入模板。</span><span class="sxs-lookup"><span data-stu-id="1aa3c-137">You must also disable the customer and vendor dual-write templates that are part of the Prospect to cash solution.</span></span>

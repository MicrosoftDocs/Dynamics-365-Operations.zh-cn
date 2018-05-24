---
title: "从目标客户到现金"
description: "本主题提供在 Microsoft Dynamics 365 for Finance and Operations 与 Microsoft Dynamics 365 for Sales 之间从目标客户到现金解决方案的概述。"
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f43b3943ce27c44cc0b4756d1d5f23e3be093273
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="prospect-to-cash"></a><span data-ttu-id="c1eeb-103">从目标客户到现金</span><span class="sxs-lookup"><span data-stu-id="c1eeb-103">Prospect to cash</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c1eeb-104">从目标客户到现金解决方案提供跨 Dynamics 365 for Finance and Operations 与 Dynamics 365 for Sales 的直接同步。</span><span class="sxs-lookup"><span data-stu-id="c1eeb-104">The Prospect to cash solution provides direct synchronization across Dynamics 365 for Finance and Operations, and Dynamics 365 for Sales.</span></span> <span data-ttu-id="c1eeb-105">提供“数据集成”功能的“从目标客户到现金”模板启用 Finance and Operations 与 Sales 之间的帐户、联系人、产品、销售报价、销售订单和销售发票的数据流。</span><span class="sxs-lookup"><span data-stu-id="c1eeb-105">The Prospect to cash templates that are available with the Data Integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="c1eeb-106">当数据在 Finance and Operations 与 Sales 之间流动时，您可以在 Sales 中执行销售和市场营销活动，并可以使用 Finance and Operations 中的库存管理处理订单履行。</span><span class="sxs-lookup"><span data-stu-id="c1eeb-106">While data is flowing between Finance and Operations and Sales, you can perform sales and marketing activities in Sales, and you can handle order fulfillment by using inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="c1eeb-107">有关“从目标客户到现金”集成的详细信息，请观看下面的 YouTube 短视频：</span><span class="sxs-lookup"><span data-stu-id="c1eeb-107">For more information about the Prospect to cash integration, watch the short YouTube video:</span></span>

> [!Video https://www.youtube.com/embed/AVV9x5x-XCg]

[<span data-ttu-id="c1eeb-108">现金集成的目标客户（YouTube 视频）</span><span class="sxs-lookup"><span data-stu-id="c1eeb-108">Prospect to cash integration (YouTube video)</span></span>](https://youtu.be/AVV9x5x-XCg) 

<span data-ttu-id="c1eeb-109">在当前版本中，从目标客户到现金解决方案提供以下类型的直接同步：</span><span class="sxs-lookup"><span data-stu-id="c1eeb-109">In the current version, the Prospect to cash solution provides the following types of direct synchronization:</span></span>

- [<span data-ttu-id="c1eeb-110">维护 Sales 中的帐户并将它们直接从 Sales 同步到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c1eeb-110">Maintain accounts in Sales and sync them directly from Sales to Finance and Operations</span></span>](accounts-template-mapping-direct.md)
- [<span data-ttu-id="c1eeb-111">维护 Finance and Operations 中的产品并将其直接同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="c1eeb-111">Maintain products in Finance and Operations and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
- [<span data-ttu-id="c1eeb-112">维护 Sales 中的联系人并将其直接同步到 Finance and Operations 的联系人或客户</span><span class="sxs-lookup"><span data-stu-id="c1eeb-112">Maintain contacts in Sales and sync them directly to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)
- [<span data-ttu-id="c1eeb-113">将 Sales 中的销售报价单直接同步到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c1eeb-113">Synchronize sales quotation directly from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping-sales-fin.md)
- [<span data-ttu-id="c1eeb-114">直接在 Sales 和 Finance and Operations 之间同步销售订单</span><span class="sxs-lookup"><span data-stu-id="c1eeb-114">Synchronize sales orders directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-direct-two-ways.md)
- [<span data-ttu-id="c1eeb-115">将 Finance and Operations 中的销售发票直接同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="c1eeb-115">Synchronize sales invoice directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="c1eeb-116">Finance and Operations 的系统要求</span><span class="sxs-lookup"><span data-stu-id="c1eeb-116">System requirements for Finance and Operations</span></span>
<span data-ttu-id="c1eeb-117">以下版本支持“从目标客户到现金”集成：</span><span class="sxs-lookup"><span data-stu-id="c1eeb-117">Prospect to cash integration is supported on the following versions:</span></span>

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a><span data-ttu-id="c1eeb-118">Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3（2017 年 12 月）</span><span class="sxs-lookup"><span data-stu-id="c1eeb-118">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (December 2017)</span></span>

- <span data-ttu-id="c1eeb-119">Dynamics 365 for Finance and Operations Enterprise Edition（2017 年 12 月）- 使用平台更新 12 的应用程序版本 7.3.11971.56116 (7.0.4709.41129)</span><span class="sxs-lookup"><span data-stu-id="c1eeb-119">Dynamics 365 for Finance and Operations, Enterprise edition (December 2017) - Application build 7.3.11971.56116 with Platform Update 12 (7.0.4709.41129)</span></span>

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a><span data-ttu-id="c1eeb-120">Dynamics 365 for Finance and Operations Enterprise Edition（2017 年 7 月）</span><span class="sxs-lookup"><span data-stu-id="c1eeb-120">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017)</span></span>

- <span data-ttu-id="c1eeb-121">Dynamics 365 for Finance and Operations Enterprise Edition（2017 年 7 月）- 具有平台更新 8（使用平台版本 7.0.4565.16212 的应用程序版本 7.2.11792.56024）。</span><span class="sxs-lookup"><span data-stu-id="c1eeb-121">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) - with platform update 8 (application build 7.2.11792.56024 with platform build 7.0.4565.16212).</span></span>
- <span data-ttu-id="c1eeb-122">必须包含以下修补程序：</span><span class="sxs-lookup"><span data-stu-id="c1eeb-122">The following hotfixes are required:</span></span>

  - <span data-ttu-id="c1eeb-123">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – 此修补程序可以通过数据集成功能将销售订单从 Sales 同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="c1eeb-123">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – This hotfix enables sales order synchronization from Sales to Finance and Operations via the Data Integration feature.</span></span> <span data-ttu-id="c1eeb-124">它还提供多个其他增强。</span><span class="sxs-lookup"><span data-stu-id="c1eeb-124">It also provides several other enhancements.</span></span>
  - <span data-ttu-id="c1eeb-125">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – 此修补程序可以通过数据集成功能将销售订单行从 Finance and Operations 同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="c1eeb-125">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order line synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>
  - <span data-ttu-id="c1eeb-126">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – 此修补程序可以通过数据集成功能将销售订单从 Finance and Operations 同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="c1eeb-126">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c1eeb-127">您只需安装 KB4045570，因为该安装包括来自其他修补程序的更改。</span><span class="sxs-lookup"><span data-stu-id="c1eeb-127">You only have to install KB4045570 because the installation includes the changes from other hotfixes.</span></span> 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a><span data-ttu-id="c1eeb-128">Dynamics 365 for Finance and Operations 版本 1611（2016 年 11 月）</span><span class="sxs-lookup"><span data-stu-id="c1eeb-128">Dynamics 365 for Finance and Operations version 1611 (November 2016)</span></span>

- <span data-ttu-id="c1eeb-129">具有平台更新 8 或更高版本的 Dynamics 365 for Finance and Operations 版本 1611（2016 年 11 月）</span><span class="sxs-lookup"><span data-stu-id="c1eeb-129">Dynamics 365 for Finance and Operations version 1611 (November 2016)  with platform update 8 or higher</span></span>

- <span data-ttu-id="c1eeb-130">必须包含以下修补程序：</span><span class="sxs-lookup"><span data-stu-id="c1eeb-130">The following hotfixes are required:</span></span>

  - <span data-ttu-id="c1eeb-131">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - 使用数据集成器将销售订单从 Finance and Operations 同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="c1eeb-131">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Enable sales order synchronization with Data integrator from Finance and Operations to Sales.</span></span> 
  - <span data-ttu-id="c1eeb-132">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - 使用数据集成器将销售订单头和行从 Finance and Operations 同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="c1eeb-132">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Enable sales order header and line synchronization with Data integrator from Finance and Operations to Sales.</span></span>
  - <span data-ttu-id="c1eeb-133">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - 需要支持通过数据实体进行从目标客户到现金的集成。</span><span class="sxs-lookup"><span data-stu-id="c1eeb-133">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Support for prospect to cash integration through data entities is required.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="c1eeb-134">安装修补程序后，您必须从 **SalesPopulateProspectToCash** 窗体触发以下批处理作业。</span><span class="sxs-lookup"><span data-stu-id="c1eeb-134">After you install the hotfixes, you must trigger the following batch job from the **SalesPopulateProspectToCash** form.</span></span> <span data-ttu-id="c1eeb-135">因为只需要一次，因此此窗体会隐藏。</span><span class="sxs-lookup"><span data-stu-id="c1eeb-135">This form is hidden because you only need it once.</span></span> <span data-ttu-id="c1eeb-136">若要访问此窗体，请登录环境，然后将以下信息添加到您的浏览器地址中的 URL：*&mi=action:SalesPopulateProspectToCash*，例如，`https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`。</span><span class="sxs-lookup"><span data-stu-id="c1eeb-136">To access the form, log in to the environment and add the following to the URL in your browser address: *&mi=action:SalesPopulateProspectToCash*, for example, `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span></span> <span data-ttu-id="c1eeb-137">打开窗体后，单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="c1eeb-137">When the form opens, click OK.</span></span> <span data-ttu-id="c1eeb-138">这将在 **SalesLine**、**SalesQuotationLine** 和 **CustInvoiceTrans** 表中使用唯一值填充新的 **LineCreationSequnceNumber** 字段，并刷新产品列表。</span><span class="sxs-lookup"><span data-stu-id="c1eeb-138">This will populate a new **LineCreationSequnceNumber** field in the **SalesLine**, **SalesQuotationLine**, and **CustInvoiceTrans** tables with unique values, and the product list will be refreshed.</span></span> <span data-ttu-id="c1eeb-139">这是执行从目标客户到现金的集成所必需的。</span><span class="sxs-lookup"><span data-stu-id="c1eeb-139">This is required for the Prospect to cash integration to work.</span></span>


## <a name="system-requirements-for-sales"></a><span data-ttu-id="c1eeb-140">Sales 的系统要求</span><span class="sxs-lookup"><span data-stu-id="c1eeb-140">System requirements for Sales</span></span>

<span data-ttu-id="c1eeb-141">若要使用从目标客户到现金解决方案，必须安装以下组件：</span><span class="sxs-lookup"><span data-stu-id="c1eeb-141">To use the Prospect to cash solution, you must install the following components:</span></span>

- <span data-ttu-id="c1eeb-142">Dynamics 365 for Sales 版本 1612 (8.2.1.207) (DB 8.2.1.207) 联机或更高版本</span><span class="sxs-lookup"><span data-stu-id="c1eeb-142">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online or a later version</span></span>
- <span data-ttu-id="c1eeb-143">Dynamics 365 for Sales 版本 1.15.0.0 或更高版本的从目标客户到现金解决方案。</span><span class="sxs-lookup"><span data-stu-id="c1eeb-143">Prospect to cash solution for Dynamics 365 for Sales, version 1.15.0.0 or a later version.</span></span> <span data-ttu-id="c1eeb-144">可从 AppSource 下载此解决方案。</span><span class="sxs-lookup"><span data-stu-id="c1eeb-144">The solution is available for download from AppSource.</span></span> <span data-ttu-id="c1eeb-145">[下载 Dynamics 365 从目标客户到现金](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3)。</span><span class="sxs-lookup"><span data-stu-id="c1eeb-145">[Download Dynamics 365, Prospect to Cash](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>


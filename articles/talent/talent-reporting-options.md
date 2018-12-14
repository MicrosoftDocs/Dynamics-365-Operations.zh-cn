---
title: "Talent 中的报告选项"
description: "本主题说明如何解决客户想要自定义 Microsoft Dynamics 365 for Talent 报表或创建新报表的问题。"
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 2007e6adec7255b0b3abda7490c2103a8583393f
ms.contentlocale: zh-cn
ms.lasthandoff: 12/04/2018

---

# <a name="reporting-options-in-talent"></a><span data-ttu-id="2aaa9-103">Talent 中的报告选项</span><span class="sxs-lookup"><span data-stu-id="2aaa9-103">Reporting options in Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2aaa9-104">**环境详细信息**</span><span class="sxs-lookup"><span data-stu-id="2aaa9-104">**Environment details**</span></span>

<span data-ttu-id="2aaa9-105">此问题适用于所有环境。</span><span class="sxs-lookup"><span data-stu-id="2aaa9-105">This issue applies to all environments.</span></span>

<span data-ttu-id="2aaa9-106">**故障**</span><span class="sxs-lookup"><span data-stu-id="2aaa9-106">**Symptom**</span></span>

<span data-ttu-id="2aaa9-107">客户想要自定义 Microsoft Dynamics 365 for Talent 报表或创建新报表。</span><span class="sxs-lookup"><span data-stu-id="2aaa9-107">The customer wants to customize Microsoft Dynamics 365 for Talent reports or create new reports.</span></span>

<span data-ttu-id="2aaa9-108">**发货**</span><span class="sxs-lookup"><span data-stu-id="2aaa9-108">**Issue**</span></span>

<span data-ttu-id="2aaa9-109">用户无法自定义嵌入的 Microsoft Power BI 报表。</span><span class="sxs-lookup"><span data-stu-id="2aaa9-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="2aaa9-110">**解决方案**</span><span class="sxs-lookup"><span data-stu-id="2aaa9-110">**Solution**</span></span>

- <span data-ttu-id="2aaa9-111">流向 Common Data Service for Apps 的 Core HR 数据可以通过 Power BI Desktop 的 PowerApps CDS 连接器报告。</span><span class="sxs-lookup"><span data-stu-id="2aaa9-111">The Core HR data that flows to Common Data Service for Apps can be reported on via the PowerApps CDS connector to Power BI Desktop.</span></span> <span data-ttu-id="2aaa9-112">请注意，Common Data Service for Apps 包含 Core HR 数据的子集。</span><span class="sxs-lookup"><span data-stu-id="2aaa9-112">Note that Common Data Service for Apps contains a subset of Core HR data.</span></span> <span data-ttu-id="2aaa9-113">有关 Power BI 和仪表板的详细信息，请参阅[使用 PowerApps Common Data Service 创建 Power BI 报表和仪表板](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi)。</span><span class="sxs-lookup"><span data-stu-id="2aaa9-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with PowerApps Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="2aaa9-114">电子申报 (ER) 对 Talent 中的某些报表可用。</span><span class="sxs-lookup"><span data-stu-id="2aaa9-114">Electronic reporting (ER) is available for some reports in Talent.</span></span> <span data-ttu-id="2aaa9-115">客户驱动的自定义可以通过 ER 配置选项完成。</span><span class="sxs-lookup"><span data-stu-id="2aaa9-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="2aaa9-116">数据可以使用 Talent 通过 Microsoft Office 集成提供的不同数据实体导出到 Microsoft Excel 或 Microsoft Word。</span><span class="sxs-lookup"><span data-stu-id="2aaa9-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Talent provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="2aaa9-117">**长期解决方案**</span><span class="sxs-lookup"><span data-stu-id="2aaa9-117">**Long-term solution**</span></span>

<span data-ttu-id="2aaa9-118">将推出更多 Power BI 选项，更多数据和实体将成为 Common Data Service for Apps 的一部分。</span><span class="sxs-lookup"><span data-stu-id="2aaa9-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service for Apps.</span></span>


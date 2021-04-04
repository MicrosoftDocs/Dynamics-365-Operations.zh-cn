---
title: 报告选项
description: 本文说明如何解决客户想要自定义 Microsoft Dynamics 365 Human Resources 报表或创建新报表的问题。
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 66581331dceacc1c0fa1816bf336339693db5339
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463278"
---
# <a name="reporting-options"></a><span data-ttu-id="0a8a0-103">报告选项</span><span class="sxs-lookup"><span data-stu-id="0a8a0-103">Reporting options</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="0a8a0-104">**环境详细信息**</span><span class="sxs-lookup"><span data-stu-id="0a8a0-104">**Environment details**</span></span>

<span data-ttu-id="0a8a0-105">此问题适用于所有环境。</span><span class="sxs-lookup"><span data-stu-id="0a8a0-105">This issue applies to all environments.</span></span>

<span data-ttu-id="0a8a0-106">**故障**</span><span class="sxs-lookup"><span data-stu-id="0a8a0-106">**Symptom**</span></span>

<span data-ttu-id="0a8a0-107">客户想要自定义 Microsoft Dynamics 365 Human Resources 报表或创建新报表。</span><span class="sxs-lookup"><span data-stu-id="0a8a0-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="0a8a0-108">**签发**</span><span class="sxs-lookup"><span data-stu-id="0a8a0-108">**Issue**</span></span>

<span data-ttu-id="0a8a0-109">用户无法自定义嵌入的 Microsoft Power BI 报表。</span><span class="sxs-lookup"><span data-stu-id="0a8a0-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="0a8a0-110">**解决方案**</span><span class="sxs-lookup"><span data-stu-id="0a8a0-110">**Solution**</span></span>

- <span data-ttu-id="0a8a0-111">流向 Dataverse 的 Human Resources 数据可以通过 Power Apps Dataverse 连接器报告给 Power BI Desktop。</span><span class="sxs-lookup"><span data-stu-id="0a8a0-111">The Human Resources data that flows to Dataverse can be reported on via the Power Apps Dataverse connector to Power BI Desktop.</span></span> <span data-ttu-id="0a8a0-112">请注意，Dataverse 包含 Human Resources 数据的子集。</span><span class="sxs-lookup"><span data-stu-id="0a8a0-112">Note that Dataverse contains a subset of Human Resources data.</span></span> <span data-ttu-id="0a8a0-113">有关 Power BI 和仪表板的详细信息，请参阅[使用 Power Apps Common Data Service 创建 Power BI 报表和仪表板](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi)。</span><span class="sxs-lookup"><span data-stu-id="0a8a0-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="0a8a0-114">电子申报 (ER) 对 Human Resources 中的某些报表可用。</span><span class="sxs-lookup"><span data-stu-id="0a8a0-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="0a8a0-115">客户驱动的自定义可以通过 ER 配置选项完成。</span><span class="sxs-lookup"><span data-stu-id="0a8a0-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="0a8a0-116">数据可以使用 Human Resources 通过Microsoft Office 集成提供的不同数据实体导出到 Microsoft Excel 或 Microsoft Word。</span><span class="sxs-lookup"><span data-stu-id="0a8a0-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="0a8a0-117">**长期解决方案**</span><span class="sxs-lookup"><span data-stu-id="0a8a0-117">**Long-term solution**</span></span>

<span data-ttu-id="0a8a0-118">将推出更多 Power BI 选项，更多数据和实体将成为 Dataverse 的一部分。</span><span class="sxs-lookup"><span data-stu-id="0a8a0-118">Additional Power BI options will be available, and more data and entities will be part of Dataverse.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
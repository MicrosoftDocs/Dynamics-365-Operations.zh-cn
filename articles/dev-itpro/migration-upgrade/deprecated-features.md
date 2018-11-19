---
title: "已删除或弃用的功能"
description: "本主题介绍已经删除或计划删除的功能。"
author: sericks007
manager: AnnBe
ms.date: 10/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 21821
ms.assetid: 31019808-4cbf-47d7-b1ba-d791db4281ae
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: 6750cfc62e2d151ddf760ff3dc36bab9c078b2d9
ms.contentlocale: zh-cn
ms.lasthandoff: 11/01/2018

---

# <a name="removed-or-deprecated-features"></a><span data-ttu-id="06a59-103">已移除或弃用的功能</span><span class="sxs-lookup"><span data-stu-id="06a59-103">Removed or deprecated features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06a59-104">本主题介绍已从 Dynamics 365 for Finance and Operations 移除或弃用的功能。</span><span class="sxs-lookup"><span data-stu-id="06a59-104">This topic describes features that have been removed or deprecated for Dynamics 365 for Finance and Operations.</span></span>

- <span data-ttu-id="06a59-105">*已移除*的功能在产品中不再可用。</span><span class="sxs-lookup"><span data-stu-id="06a59-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="06a59-106">*已弃用*的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="06a59-107">此列表旨在帮助您在您自己的计划中考虑这些功能的移除和弃用。</span><span class="sxs-lookup"><span data-stu-id="06a59-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!Note]
> <span data-ttu-id="06a59-108">从具有平台更新 8 的 Dynamics 365 for Finance and Operations 2017 年 7 月版开始，每一个已移除或弃用的功能均备注了部署类型。</span><span class="sxs-lookup"><span data-stu-id="06a59-108">Starting with the Dynamics 365 for Finance and Operations July 2017 release with platform update 8, the type of deployments are noted for each removed or deprecated feature.</span></span> <span data-ttu-id="06a59-109">本主题中提及的所有之前的版本仅支持云部署。</span><span class="sxs-lookup"><span data-stu-id="06a59-109">All of the previous releases mentioned in this topic supported cloud deployments only.</span></span>

> [!Note]
> <span data-ttu-id="06a59-110">[技术参考报告](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep)中提供了有关 Finance and Operations 中的对象的详细信息。</span><span class="sxs-lookup"><span data-stu-id="06a59-110">Detailed information about objects in Finance and Operations can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="06a59-111">可比较这些报告的不同版本，以了解 Finance and Operations 各版本中已更改或已删除的对象。</span><span class="sxs-lookup"><span data-stu-id="06a59-111">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations.</span></span>

## <a name="dynamics-365-for-finance-and-operations-81-with-platform-update-20"></a><span data-ttu-id="06a59-112">具有平台更新 20 的 Dynamics 365 for Finance and Operations 8.1</span><span class="sxs-lookup"><span data-stu-id="06a59-112">Dynamics 365 for Finance and Operations 8.1 with platform update 20</span></span>

### <a name="batch-transfer-rules-for-subledger-journal-account-entries"></a><span data-ttu-id="06a59-113">子分类日记帐科目分录的批处理转移规则</span><span class="sxs-lookup"><span data-stu-id="06a59-113">Batch transfer rules for subledger journal account entries</span></span>
<span data-ttu-id="06a59-114">总帐参数中已弃用了同步转移模式。</span><span class="sxs-lookup"><span data-stu-id="06a59-114">The Synchronous transfer mode is being deprecated in the General ledger parameters.</span></span>  <span data-ttu-id="06a59-115">此模式刚被异步和计划批处理，后者表示为转移选项。</span><span class="sxs-lookup"><span data-stu-id="06a59-115">This mode is replaced by Asynchronous and scheduled batch only, which already exist as options for transfer.</span></span> 

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-116">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-116">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-117">因为对系统存在影响，我们将移除同步选项。</span><span class="sxs-lookup"><span data-stu-id="06a59-117">We are removing the synchronous option due to performance impact to the system.</span></span> |
| <span data-ttu-id="06a59-118">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-118">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-119">异步和计划批处理选项取代了同步。</span><span class="sxs-lookup"><span data-stu-id="06a59-119">Asynchronous and scheduled batch are options to use in place of Synchronous.</span></span>   |
| <span data-ttu-id="06a59-120">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-120">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-121">总帐、应付帐款、应收帐款、采购、支出</span><span class="sxs-lookup"><span data-stu-id="06a59-121">General Ledger, Accounts payable, Accounts Receivable, Procurement, Expense</span></span>    |
| <span data-ttu-id="06a59-122">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="06a59-122">**Deployment option**</span></span>              | <span data-ttu-id="06a59-123">所有</span><span class="sxs-lookup"><span data-stu-id="06a59-123">All</span></span>  |
| <span data-ttu-id="06a59-124">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-124">**Status**</span></span>                         | <span data-ttu-id="06a59-125">已弃用 - 移除功能的目标时间范围为 10.0 版本。</span><span class="sxs-lookup"><span data-stu-id="06a59-125">Deprecated - Target timeframe for the functionality to be removed is the 10.0 version.</span></span>|

### <a name="electronic-reporting-for-russia"></a><span data-ttu-id="06a59-126">俄罗斯的电子报告格式</span><span class="sxs-lookup"><span data-stu-id="06a59-126">Electronic reporting for Russia</span></span>
<span data-ttu-id="06a59-127">用于配置申报的 .txt 和 .xml 文件格式的功能。</span><span class="sxs-lookup"><span data-stu-id="06a59-127">Feature for configuring .txt and .xml file formats of declarations.</span></span> 

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-128">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-128">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-129">已被电子申报取代。</span><span class="sxs-lookup"><span data-stu-id="06a59-129">Replaced with Electronic reporting.</span></span> |
| <span data-ttu-id="06a59-130">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-130">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-131">是。</span><span class="sxs-lookup"><span data-stu-id="06a59-131">Yes.</span></span> |
| <span data-ttu-id="06a59-132">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-132">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-133">总帐</span><span class="sxs-lookup"><span data-stu-id="06a59-133">General Ledger</span></span> |
| <span data-ttu-id="06a59-134">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="06a59-134">**Deployment option**</span></span>              | <span data-ttu-id="06a59-135">所有</span><span class="sxs-lookup"><span data-stu-id="06a59-135">All</span></span> |
| <span data-ttu-id="06a59-136">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-136">**Status**</span></span>                         | <span data-ttu-id="06a59-137">已从带平台更新 20 的 Dynamics 365 for Finance and Operations 8.1 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-137">Removed as of Dynamics 365 for Finance and Operations 8.1 with platform update 20.</span></span> |

### <a name="financial-reports-generator-for-russia"></a><span data-ttu-id="06a59-138">俄罗斯的财务报表生成器</span><span class="sxs-lookup"><span data-stu-id="06a59-138">Financial reports generator for Russia</span></span>
<span data-ttu-id="06a59-139">用于设置会计和纳税报表的数据收集，以及用于将数据导出到 XLS 和 DOC 报表模板的工具。</span><span class="sxs-lookup"><span data-stu-id="06a59-139">A tool for setting up data collection for accounting and tax reports, and to export data to XLS and DOC report templates.</span></span> <span data-ttu-id="06a59-140">功能部件：已移除了将数据导出到 XLS 和 DOC 报表模板、查询和固定必备项这一功能。</span><span class="sxs-lookup"><span data-stu-id="06a59-140">Functional parts: Export data to XLS and DOC report templates, queries, fixed requisites are removed.</span></span> 

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-141">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-141">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-142">移除的部件已被电子申报取代。</span><span class="sxs-lookup"><span data-stu-id="06a59-142">Removed parts are replaced with Electronic reporting.</span></span> |
| <span data-ttu-id="06a59-143">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-143">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-144">是。</span><span class="sxs-lookup"><span data-stu-id="06a59-144">Yes.</span></span> <span data-ttu-id="06a59-145">应使用财务报表设置用户界面按总帐科目和税务登记簿设置数据收集规则。</span><span class="sxs-lookup"><span data-stu-id="06a59-145">Financial reports setup user interface should be used for setting up data collection rules by GL accounts or tax registers.</span></span> <span data-ttu-id="06a59-146">应在电子申报中配置将数据导出到各种文件类型、固定必备项和类似查询的数据收集规则。</span><span class="sxs-lookup"><span data-stu-id="06a59-146">Export data to various file types, fixed requisites and query-like data collection rules should be configured in Electronic reporting.</span></span> |
| <span data-ttu-id="06a59-147">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-147">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-148">总帐。</span><span class="sxs-lookup"><span data-stu-id="06a59-148">General ledger.</span></span> |
| <span data-ttu-id="06a59-149">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="06a59-149">**Deployment option**</span></span>              | <span data-ttu-id="06a59-150">所有</span><span class="sxs-lookup"><span data-stu-id="06a59-150">All</span></span> |
| <span data-ttu-id="06a59-151">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-151">**Status**</span></span>                         | <span data-ttu-id="06a59-152">已从带平台更新 20 的 Dynamics 365 for Finance and Operations 8.1 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-152">Removed as of Dynamics 365 for Finance and Operations 8.1 with platform update 20.</span></span> |

### <a name="integration-with-external-providers-for-sending-electronic-reporting-through-communication-channels-for-russia"></a><span data-ttu-id="06a59-153">俄罗斯的与外部提供商集成以通过通信通道发送电子报告</span><span class="sxs-lookup"><span data-stu-id="06a59-153">Integration with external providers for sending electronic reporting through communication channels for Russia</span></span>
<span data-ttu-id="06a59-154">用于将生成的电子版申报文件导出到文件夹以进一步发送给正式的电子申报提供商和导入回状态的功能。</span><span class="sxs-lookup"><span data-stu-id="06a59-154">Feature exporting generated electronic files of declarations to folder for further sending to official providers of electronic reporting as well as importing state back.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-155">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-155">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-156">已被电子消息可配置功能取代。</span><span class="sxs-lookup"><span data-stu-id="06a59-156">Replaced with electronic messages configurable feature.</span></span> |
| <span data-ttu-id="06a59-157">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-157">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-158">是。</span><span class="sxs-lookup"><span data-stu-id="06a59-158">Yes.</span></span>  |
| <span data-ttu-id="06a59-159">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-159">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-160">总帐、税务</span><span class="sxs-lookup"><span data-stu-id="06a59-160">General Ledger, Tax</span></span> |
| <span data-ttu-id="06a59-161">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="06a59-161">**Deployment option**</span></span>              | <span data-ttu-id="06a59-162">所有</span><span class="sxs-lookup"><span data-stu-id="06a59-162">All</span></span> |
| <span data-ttu-id="06a59-163">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-163">**Status**</span></span>                         | <span data-ttu-id="06a59-164">已从带平台更新 20 的 Dynamics 365 for Finance and Operations 8.1 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-164">Removed as of Dynamics 365 for Finance and Operations 8.1 with platform update 20.</span></span> |

## <a name="dynamics-365-for-finance-and-operations-80-with-platform-update-15"></a><span data-ttu-id="06a59-165">具有平台更新 15 的 Dynamics 365 for Finance and Operations 8.0</span><span class="sxs-lookup"><span data-stu-id="06a59-165">Dynamics 365 for Finance and Operations 8.0 with platform update 15</span></span>
<span data-ttu-id="06a59-166">此版本中未移除或弃用任何功能。</span><span class="sxs-lookup"><span data-stu-id="06a59-166">No features have been removed or deprecated with this release.</span></span> <span data-ttu-id="06a59-167">平台更新 15 是累积功能，其中包含平台更新 13、14 和 15 中的新增功能或更改功能。</span><span class="sxs-lookup"><span data-stu-id="06a59-167">Platform update 15 is cumulative and contains new or changed features from Platform update 13, Platform update 14, and Platform update 15.</span></span>

## <a name="dynamics-365-for-finance-and-operations-enterprise-edition-73-with-platform-update-12"></a><span data-ttu-id="06a59-168">具有平台更新 12 的 Dynamics 365 for Finance and Operations Enterprise Edition 7.3</span><span class="sxs-lookup"><span data-stu-id="06a59-168">Dynamics 365 for Finance and Operations, Enterprise edition 7.3 with platform update 12</span></span>

### <a name="personalized-product-recommendations"></a><span data-ttu-id="06a59-169">个性化产品建议</span><span class="sxs-lookup"><span data-stu-id="06a59-169">Personalized product recommendations</span></span> 
<span data-ttu-id="06a59-170">从 2018 年 2 月 15 日开始，零售商再也不能显示有关销售点 (POS) 设备的个性化产品建议。</span><span class="sxs-lookup"><span data-stu-id="06a59-170">Starting February 15, 2018, retailers will no longer be able to display personalized product recommendations on a point of sale (POS) device.</span></span> <span data-ttu-id="06a59-171">有关详细信息，请参见[个性化产品建议](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/personalized-product-recommendations)。</span><span class="sxs-lookup"><span data-stu-id="06a59-171">For more information, see [Personalized product recommendations](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/personalized-product-recommendations).</span></span>  

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-172">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-172">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-173">我们将移除当前的产品建议服务版本，因为我们为这项功能重新设计了更出色的算法和更新的面向零售的功能。</span><span class="sxs-lookup"><span data-stu-id="06a59-173">We are removing the current version of the product recommendation service as we redesign this feature with a better algorithm and newer retail-oriented capabilities.</span></span>  |
| <span data-ttu-id="06a59-174">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-174">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-175">编号</span><span class="sxs-lookup"><span data-stu-id="06a59-175">No.</span></span> <span data-ttu-id="06a59-176">但是，我们计划在 2018 年春季之后恢复此功能，以利用新的建议服务。</span><span class="sxs-lookup"><span data-stu-id="06a59-176">However, after Spring 2018, we plan to bring back this feature to leverage a new recommendation service.</span></span>   |
| <span data-ttu-id="06a59-177">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-177">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-178">POS 中的个性化产品建议。</span><span class="sxs-lookup"><span data-stu-id="06a59-178">Personalized product recommendations in POS.</span></span>                                                    |
| <span data-ttu-id="06a59-179">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="06a59-179">**Deployment option**</span></span>              | <span data-ttu-id="06a59-180">全部</span><span class="sxs-lookup"><span data-stu-id="06a59-180">All</span></span>                                                                                      |
| <span data-ttu-id="06a59-181">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-181">**Status**</span></span>                         |<span data-ttu-id="06a59-182">从 2018 年 2 月 15 日开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-182">Removed as of February 15, 2018.</span></span> <span data-ttu-id="06a59-183">这将影响运行 Dynamics 365 for Operations 1611 及更高版本的客户。</span><span class="sxs-lookup"><span data-stu-id="06a59-183">This affects customers running Dynamics 365 for Operations 1611 and later.</span></span>  |

### <a name="extension-of-the-list-of-electronic-reporting-er-functions"></a><span data-ttu-id="06a59-184">电子申报 (ER) 功能列表扩展</span><span class="sxs-lookup"><span data-stu-id="06a59-184">Extension of the list of Electronic reporting (ER) functions</span></span>
<span data-ttu-id="06a59-185">可以引入在 ER 表达式生成器中使用的自定义功能（有关详细信息，请参阅[扩展电子申报功能列表](../../dev-itpro/analytics/general-electronic-reporting-formulas-list-extension.md)）的这一特性不再受支持。</span><span class="sxs-lookup"><span data-stu-id="06a59-185">The possibility to introduce custom functions to be used in the ER expression builder (for more information, see [Extend the list of Electronic reporting functions](../../dev-itpro/analytics/general-electronic-reporting-formulas-list-extension.md)) is not supported any more.</span></span> <span data-ttu-id="06a59-186">由于 ER API 发生变更，从 ER 表达式生成器调用内置函数的 API 变成内部 API，并且无法再进行扩展。</span><span class="sxs-lookup"><span data-stu-id="06a59-186">Due to changes of the ER APIs, the API to call built-in functions from the ER expression builder became internal and can’t be extended any longer.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-187">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-187">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-188">代码密封计划</span><span class="sxs-lookup"><span data-stu-id="06a59-188">Code sealing initiative</span></span>  |
| <span data-ttu-id="06a59-189">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-189">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-190">无。</span><span class="sxs-lookup"><span data-stu-id="06a59-190">None.</span></span> <span data-ttu-id="06a59-191">每当需要一个新的内置函数时，必须向 ER 框架团队提交新扩展请求。</span><span class="sxs-lookup"><span data-stu-id="06a59-191">Whenever a new built-in function is needed, a new extension request must be addressed to the ER framework team.</span></span><br><br><span data-ttu-id="06a59-192">在 ER 团队开发请求的函数时，作为临时解决方案，可以将需要的逻辑作为一种自定义应用程序类方法进行编程。</span><span class="sxs-lookup"><span data-stu-id="06a59-192">As a temporary work around while the requested function is under development by the ER team, the required logic can be programmed as a method of a custom application class.</span></span> <span data-ttu-id="06a59-193">此方法可以作为引用该自定义应用程序类的**应用程序\类**类型的已添加 ER 数据源的属性在 ER 表达式中访问。</span><span class="sxs-lookup"><span data-stu-id="06a59-193">This method can be accessed in an ER expression as a property of the added ER data source of the **Application\Class** type that refers to that custom application class.</span></span>  |
| <span data-ttu-id="06a59-194">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-194">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-195">电子申报框架</span><span class="sxs-lookup"><span data-stu-id="06a59-195">Electronic reporting framework</span></span>                                                      |
| <span data-ttu-id="06a59-196">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="06a59-196">**Deployment option**</span></span>              | <span data-ttu-id="06a59-197">全部</span><span class="sxs-lookup"><span data-stu-id="06a59-197">All</span></span>                                                                                      |
| <span data-ttu-id="06a59-198">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-198">**Status**</span></span>                         | <span data-ttu-id="06a59-199">从 Dynamics 365 for Finance and Operations Enterprise Edition 7.3 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-199">Removed as of Dynamics 365 for Finance and Operations, Enterprise edition 7.3.</span></span>    |

### <a name="inventory-by-item-group-and-inventory-by-inventory-dimension-aging-reports"></a><span data-ttu-id="06a59-200">按物料组的库存和按库存维度的库存帐龄分析表</span><span class="sxs-lookup"><span data-stu-id="06a59-200">Inventory by item group and Inventory by inventory dimension aging reports</span></span>

<span data-ttu-id="06a59-201">这两个分析表在 Finance and Operations 中不再受支持。</span><span class="sxs-lookup"><span data-stu-id="06a59-201">These two reports are no longer supported in Finance and Operations.</span></span> <span data-ttu-id="06a59-202">相反，可使用**库存帐龄**分析表改善用户体验。</span><span class="sxs-lookup"><span data-stu-id="06a59-202">Instead, the **Inventory aging** report can be used to improve the user experience.</span></span>

|   |  |
|--------------|-----------------------|
| <span data-ttu-id="06a59-203">**折旧的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-203">**Reason for deprecation**</span></span>       | <span data-ttu-id="06a59-204">重复的功能</span><span class="sxs-lookup"><span data-stu-id="06a59-204">Duplicate functionality</span></span>  |
| <span data-ttu-id="06a59-205">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-205">**Replaced by another feature?**</span></span> | <span data-ttu-id="06a59-206">是。</span><span class="sxs-lookup"><span data-stu-id="06a59-206">Yes.</span></span> <span data-ttu-id="06a59-207">这两个分析表已替换为**库存帐龄**分析表。</span><span class="sxs-lookup"><span data-stu-id="06a59-207">The two reports have been replaced by the **Inventory aging** report.</span></span>     |
| <span data-ttu-id="06a59-208">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-208">**Product areas affected**</span></span>       | <span data-ttu-id="06a59-209">库存管理、成本管理</span><span class="sxs-lookup"><span data-stu-id="06a59-209">Inventory management, Cost management</span></span>        |
| <span data-ttu-id="06a59-210">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="06a59-210">**Deployment option**</span></span>        | <span data-ttu-id="06a59-211">全部</span><span class="sxs-lookup"><span data-stu-id="06a59-211">All</span></span>|
| <span data-ttu-id="06a59-212">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-212">**Status**</span></span>                       | <span data-ttu-id="06a59-213">已弃用：两个分析表的菜单项在版本 7.3 中已移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-213">Deprecated: The menu items for the two reports have been removed in version 7.3.</span></span> <span data-ttu-id="06a59-214">但这些分析表的代码仍然保留在产品中。</span><span class="sxs-lookup"><span data-stu-id="06a59-214">However, the code for the reports remains in the product.</span></span> <span data-ttu-id="06a59-215">在将来的发行中计划移除该代码。</span><span class="sxs-lookup"><span data-stu-id="06a59-215">The plan is to remove the code in a future release.</span></span> |

### <a name="power-bi-content-packs-available-on-appsource"></a><span data-ttu-id="06a59-216">AppSource 中的 Power BI 内容包</span><span class="sxs-lookup"><span data-stu-id="06a59-216">Power BI content packs available on AppSource</span></span>
<span data-ttu-id="06a59-217">[Microsoft AppSource](https://appsource.microsoft.com) 上提供的**成本管理**、**财务绩效**和**零售渠道绩效**内容包因为 Microsoft Power BI 中的产品更新而被弃用。</span><span class="sxs-lookup"><span data-stu-id="06a59-217">The **Cost management**, **Financial performance**, and **Retail channel performance** content packs, available on the [Microsoft AppSource](https://appsource.microsoft.com) site, are deprecated as a consequence of product updates in Microsoft Power BI.</span></span> <span data-ttu-id="06a59-218">过去将这些内容包部署到 PowerBI.com 的系统管理窗体在 Finance and Operations 中也被弃用。</span><span class="sxs-lookup"><span data-stu-id="06a59-218">System administration forms used to deploy these content packs to PowerBI.com are also being deprecated in Finance and Operations.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-219">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-219">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-220">Microsoft Power BI 中进行产品更新。</span><span class="sxs-lookup"><span data-stu-id="06a59-220">Product updates in Microsoft Power BI.</span></span> |
| <span data-ttu-id="06a59-221">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-221">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-222">[AppSource](https://appsource.microsoft.com) 站点上提供的**成本管理**、**财务绩效**和**零售渠道绩效**内容包将被分析应用程序替代，以便在数据库级别集成解决方案。</span><span class="sxs-lookup"><span data-stu-id="06a59-222">The **Cost management**, **Financial performance**, and **Retail channel performance** content packs, available on the [AppSource](https://appsource.microsoft.com) site, are being replaced by analytical applications which allow for solution integrations at the database level.</span></span> <span data-ttu-id="06a59-223">有关分析应用程序的详细信息，请参阅[工作区中的嵌入式 Power BI](../../dev-itpro/analytics/embed-power-bi-workspaces.md)。</span><span class="sxs-lookup"><span data-stu-id="06a59-223">For more information about analytical applications, see [Embedded Power BI in workspackes](../../dev-itpro/analytics/embed-power-bi-workspaces.md).</span></span>    |
| <span data-ttu-id="06a59-224">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-224">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-225">成本管理、财务和零售</span><span class="sxs-lookup"><span data-stu-id="06a59-225">Cost management, Finance, and Retail</span></span>                                                                                               |
| <span data-ttu-id="06a59-226">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="06a59-226">**Deployment option**</span></span>              | <span data-ttu-id="06a59-227">仅适用于云（在本地部署中不再支持与 PowerBI.com 集成）。</span><span class="sxs-lookup"><span data-stu-id="06a59-227">Cloud only (Integration with PowerBI.com is not supported in on-premises deployments.)</span></span>                                                                                                            |
| <span data-ttu-id="06a59-228">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-228">**Status**</span></span>                         | <span data-ttu-id="06a59-229">已弃用：移除功能的目标时间范围为 2018 年第二季度。</span><span class="sxs-lookup"><span data-stu-id="06a59-229">Deprecated: Target timeframe for the functionality removal is Q2 2018.</span></span>    |

### <a name="standard-ui-in-data-management-workspace"></a><span data-ttu-id="06a59-230">数据管理工作区中的标准 UI</span><span class="sxs-lookup"><span data-stu-id="06a59-230">Standard UI in data management workspace</span></span>

<span data-ttu-id="06a59-231">数据管理中的标准 UI 为旧 UI，是当用户访问数据管理工作区时呈现给用户的默认 UI。</span><span class="sxs-lookup"><span data-stu-id="06a59-231">The standard UI in data management is the legacy UI, which is the default UI presented to the users when they visit the data management workspace.</span></span>

|   |  |
|------------------|-------------------------|
| <span data-ttu-id="06a59-232">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-232">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-233">我们正努力在新的 UI 中为用户提供新的体验。</span><span class="sxs-lookup"><span data-stu-id="06a59-233">We are investing in providing new user experiences in the new UI.</span></span>             |
| <span data-ttu-id="06a59-234">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-234">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-235">新 UI 称为*增强型视图*，它将取代旧 UI。</span><span class="sxs-lookup"><span data-stu-id="06a59-235">The new UI called *Enhanced views* is replacing the old UI.</span></span>            |
| <span data-ttu-id="06a59-236">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-236">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-237">数据管理工作区</span><span class="sxs-lookup"><span data-stu-id="06a59-237">Data management workspace</span></span>                                                     |
| <span data-ttu-id="06a59-238">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="06a59-238">**Deployment option**</span></span>              | <span data-ttu-id="06a59-239">全部</span><span class="sxs-lookup"><span data-stu-id="06a59-239">All</span></span>                                                                           |
| <span data-ttu-id="06a59-240">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-240">**Status**</span></span>                         | <span data-ttu-id="06a59-241">已弃用：移除功能的目标时间范围为 2018 年第二季度。</span><span class="sxs-lookup"><span data-stu-id="06a59-241">Deprecated: Target timeframe for the functionality to be removed is Q2 2018.</span></span> |

### <a name="excise-sales-tax-service-tax-for-india"></a><span data-ttu-id="06a59-242">适用于印度的消费税、销售税、服务税</span><span class="sxs-lookup"><span data-stu-id="06a59-242">Excise, Sales Tax, Service Tax for India</span></span>

<span data-ttu-id="06a59-243">这些税项已归入印度 GST。</span><span class="sxs-lookup"><span data-stu-id="06a59-243">These taxes have been subsumed into Indian GST.</span></span>

|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="06a59-244">**移除或弃用的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-244">**Reason for removal or deprecation**</span></span>       | <span data-ttu-id="06a59-245">这些税项已归入印度 GST。</span><span class="sxs-lookup"><span data-stu-id="06a59-245">These taxes have been subsumed into Indian GST.</span></span>                          |
| <span data-ttu-id="06a59-246">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-246">**Replaced by another feature?**</span></span>            | <span data-ttu-id="06a59-247">印度 GST</span><span class="sxs-lookup"><span data-stu-id="06a59-247">Indian GST</span></span>                                                              |
| <span data-ttu-id="06a59-248">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-248">**Product areas affected**</span></span>                  | <span data-ttu-id="06a59-249">税金</span><span class="sxs-lookup"><span data-stu-id="06a59-249">Tax</span></span>                                                                     |
| <span data-ttu-id="06a59-250">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="06a59-250">**Deployment option**</span></span>                       | <span data-ttu-id="06a59-251">所有模块</span><span class="sxs-lookup"><span data-stu-id="06a59-251">All modules</span></span>                                                   |
| <span data-ttu-id="06a59-252">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-252">**Status**</span></span>                                  | <span data-ttu-id="06a59-253">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-253">Deprecated: A removal date has not been set for this feature.</span></span> |    

### <a name="file-validation-utility-fvu-for-india"></a><span data-ttu-id="06a59-254">印度文件验证实用工具 (FVU)</span><span class="sxs-lookup"><span data-stu-id="06a59-254">File Validation Utility (FVU) for India</span></span>

|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="06a59-255">**移除或弃用的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-255">**Reason for removal or deprecation**</span></span>       | <span data-ttu-id="06a59-256">缺少客户使用</span><span class="sxs-lookup"><span data-stu-id="06a59-256">Lack of customer usage</span></span>                                                  |
| <span data-ttu-id="06a59-257">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-257">**Replaced by another feature?**</span></span>            | <span data-ttu-id="06a59-258">无</span><span class="sxs-lookup"><span data-stu-id="06a59-258">No</span></span>                                                                      |
| <span data-ttu-id="06a59-259">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-259">**Product areas affected**</span></span>                  | <span data-ttu-id="06a59-260">印度预缴税金</span><span class="sxs-lookup"><span data-stu-id="06a59-260">Indian withholding tax</span></span>                                                  |
| <span data-ttu-id="06a59-261">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="06a59-261">**Deployment option**</span></span>                       | <span data-ttu-id="06a59-262">所有模块</span><span class="sxs-lookup"><span data-stu-id="06a59-262">All modules</span></span>                                                                    |
| <span data-ttu-id="06a59-263">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-263">**Status**</span></span>                                  | <span data-ttu-id="06a59-264">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-264">Deprecated: A removal date has not been set for this feature.</span></span>   |        

### <a name="tdstcs-certificate-for-india"></a><span data-ttu-id="06a59-265">印度 TDS/TCS 证书</span><span class="sxs-lookup"><span data-stu-id="06a59-265">TDS/TCS certificate for India</span></span>

<span data-ttu-id="06a59-266">用户可从政府门户下载。</span><span class="sxs-lookup"><span data-stu-id="06a59-266">Users can download this from the government portal.</span></span>

|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="06a59-267">**移除或弃用的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-267">**Reason for removal or deprecation**</span></span>       | <span data-ttu-id="06a59-268">缺少客户使用</span><span class="sxs-lookup"><span data-stu-id="06a59-268">Lack of customer usage</span></span>                                                  |
| <span data-ttu-id="06a59-269">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-269">**Replaced by another feature?**</span></span>            | <span data-ttu-id="06a59-270">无</span><span class="sxs-lookup"><span data-stu-id="06a59-270">No</span></span>                                                                      |
| <span data-ttu-id="06a59-271">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-271">**Product areas affected**</span></span>                  | <span data-ttu-id="06a59-272">印度预缴税金</span><span class="sxs-lookup"><span data-stu-id="06a59-272">Indian withholding tax</span></span>                                                  |
| <span data-ttu-id="06a59-273">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="06a59-273">**Deployment option**</span></span>                       | <span data-ttu-id="06a59-274">所有模块</span><span class="sxs-lookup"><span data-stu-id="06a59-274">All modules</span></span>                                                                   |
| <span data-ttu-id="06a59-275">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-275">**Status**</span></span>                                  | <span data-ttu-id="06a59-276">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-276">Deprecated: A removal date has not been set for this feature.</span></span>     |    

### <a name="exportimport-exim-incentive-scheme-for-india"></a><span data-ttu-id="06a59-277">导出/导入 (EXIM) 印度激励方案</span><span class="sxs-lookup"><span data-stu-id="06a59-277">Export/import (EXIM) incentive scheme for India</span></span>


|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="06a59-278">**移除或弃用的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-278">**Reason for removal or deprecation**</span></span>       | <span data-ttu-id="06a59-279">缺少客户使用</span><span class="sxs-lookup"><span data-stu-id="06a59-279">Lack of customer usage</span></span>                                                  |
| <span data-ttu-id="06a59-280">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-280">**Replaced by another feature?**</span></span>            | <span data-ttu-id="06a59-281">无</span><span class="sxs-lookup"><span data-stu-id="06a59-281">No</span></span>                                                                      |
| <span data-ttu-id="06a59-282">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-282">**Product areas affected**</span></span>                  | <span data-ttu-id="06a59-283">导入和导出</span><span class="sxs-lookup"><span data-stu-id="06a59-283">Import and export</span></span>                                                       |
| <span data-ttu-id="06a59-284">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="06a59-284">**Deployment option**</span></span>                       | <span data-ttu-id="06a59-285">所有模块</span><span class="sxs-lookup"><span data-stu-id="06a59-285">All modules</span></span>                                                                    |
| <span data-ttu-id="06a59-286">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-286">**Status**</span></span>                                  | <span data-ttu-id="06a59-287">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-287">Deprecated: A removal date has not been set for this feature.</span></span>  |    


## <a name="dynamics-365-for-retail-72"></a><span data-ttu-id="06a59-288">Dynamics 365 for Retail 7.2</span><span class="sxs-lookup"><span data-stu-id="06a59-288">Dynamics 365 for Retail 7.2</span></span>

### <a name="personalized-product-recommendations"></a><span data-ttu-id="06a59-289">个性化产品建议</span><span class="sxs-lookup"><span data-stu-id="06a59-289">Personalized product recommendations</span></span> 
<span data-ttu-id="06a59-290">从 2018 年 2 月 15 日开始，零售商再也不能显示有关销售点 (POS) 设备的个性化产品建议。</span><span class="sxs-lookup"><span data-stu-id="06a59-290">Starting February 15, 2018, retailers will no longer be able to display personalized product recommendations on a point of sale (POS) device.</span></span> <span data-ttu-id="06a59-291">有关详细信息，请参见[个性化产品建议](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/personalized-product-recommendations)。</span><span class="sxs-lookup"><span data-stu-id="06a59-291">For more information, see [Personalized product recommendations](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/personalized-product-recommendations).</span></span>  

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-292">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-292">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-293">我们将移除当前的产品建议服务版本，因为我们为这项功能重新设计了更出色的算法和更新的面向零售的功能。</span><span class="sxs-lookup"><span data-stu-id="06a59-293">We are removing the current version of the product recommendation service as we redesign this feature with a better algorithm and newer retail-oriented capabilities.</span></span>  |
| <span data-ttu-id="06a59-294">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-294">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-295">编号</span><span class="sxs-lookup"><span data-stu-id="06a59-295">No.</span></span> <span data-ttu-id="06a59-296">但是，我们计划在 2018 年春季之后恢复此功能，以利用新的建议服务。</span><span class="sxs-lookup"><span data-stu-id="06a59-296">However, after Spring 2018, we plan to bring back this feature to leverage a new recommendation service.</span></span>   |
| <span data-ttu-id="06a59-297">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-297">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-298">POS 中的个性化产品建议。</span><span class="sxs-lookup"><span data-stu-id="06a59-298">Personalized product recommendations in POS.</span></span>                                                    |
| <span data-ttu-id="06a59-299">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="06a59-299">**Deployment option**</span></span>              | <span data-ttu-id="06a59-300">全部</span><span class="sxs-lookup"><span data-stu-id="06a59-300">All</span></span>                                                                                      |
| <span data-ttu-id="06a59-301">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-301">**Status**</span></span>                         |<span data-ttu-id="06a59-302">从 2018 年 2 月 15 日开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-302">Removed as of February 15, 2018.</span></span> <span data-ttu-id="06a59-303">这将影响运行 Dynamics 365 for Retail 7.2 及更高版本的客户。</span><span class="sxs-lookup"><span data-stu-id="06a59-303">This affects customers running Dynamics 365 for Retail 7.2  and later.</span></span> |


## <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-with-platform-update-8"></a><span data-ttu-id="06a59-304">具有平台更新 8 的 Dynamics 365 for Finance and Operations Enterprise Edition 2017 年 7 月</span><span class="sxs-lookup"><span data-stu-id="06a59-304">Dynamics 365 for Finance and Operations, Enterprise edition July 2017 with platform update 8</span></span>

### <a name="currency-conversion-for-accounting-and-reporting-currencies"></a><span data-ttu-id="06a59-305">记帐币种和申报币种的币种转换</span><span class="sxs-lookup"><span data-stu-id="06a59-305">Currency conversion for accounting and reporting currencies</span></span>

<span data-ttu-id="06a59-306">引入欧元时，也引入了记帐币种和申报币种的币种转换。</span><span class="sxs-lookup"><span data-stu-id="06a59-306">Currency conversion for accounting and reporting currencies was introduced when the euro was introduced.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-307">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-307">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-308">“复制法人”功能作为替代方法的使用和添加受限。</span><span class="sxs-lookup"><span data-stu-id="06a59-308">Limited usage and addition of the Copy legal entity functionality as a replacement.</span></span>      |
| <span data-ttu-id="06a59-309">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-309">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-310">否，但是增加了“复制法人”和“配置”功能，从而可以更轻松地迁移到核心需求不断变化的公司。</span><span class="sxs-lookup"><span data-stu-id="06a59-310">No, but the Copy legal entity and Configurations features were added to make it easier to move to a company that has changing core requirements.</span></span> |
| <span data-ttu-id="06a59-311">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-311">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-312">财务管理</span><span class="sxs-lookup"><span data-stu-id="06a59-312">Financial management</span></span>     |
| <span data-ttu-id="06a59-313">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-313">**Status**</span></span>                         | <span data-ttu-id="06a59-314">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-314">Deprecated: A removal date has not been set for this feature.</span></span>   |


### <a name="warehouse-mobile-devices-portal"></a><span data-ttu-id="06a59-315">仓库移动设备门户</span><span class="sxs-lookup"><span data-stu-id="06a59-315">Warehouse mobile devices portal</span></span>

<span data-ttu-id="06a59-316">仓库移动设备门户 (WMDP) 是用于本地自行部署的单独组件。</span><span class="sxs-lookup"><span data-stu-id="06a59-316">Warehouse mobile devices portal (WMDP) was a standalone component that was intended for on-premises self-deployment.</span></span> <span data-ttu-id="06a59-317">此组件在 Finance and Operations 中不再受支持。</span><span class="sxs-lookup"><span data-stu-id="06a59-317">This component is no longer supported in Finance and Operations.</span></span> <span data-ttu-id="06a59-318">一个可提高用户体验的本机应用已替代 WMDP 的功能。</span><span class="sxs-lookup"><span data-stu-id="06a59-318">A native app that improves the user experience has replaced the functionality of WMDP.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-319">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-319">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-320">重复的功能。</span><span class="sxs-lookup"><span data-stu-id="06a59-320">Duplicate functionality.</span></span>       |
| <span data-ttu-id="06a59-321">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-321">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-322">是。</span><span class="sxs-lookup"><span data-stu-id="06a59-322">Yes.</span></span> <span data-ttu-id="06a59-323">此功能已经由 Finance and Operations - Warehousing 取代。</span><span class="sxs-lookup"><span data-stu-id="06a59-323">This feature has been replaced by Finance and Operations - Warehousing.</span></span> <span data-ttu-id="06a59-324">有关设置和先决条件的详细信息，请参阅 [安装和配置 Microsoft Dynamics 365 for Finance and Operations - Warehousing](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/install-configure-warehousing-app)。</span><span class="sxs-lookup"><span data-stu-id="06a59-324">For more information about setup and prerequisites, see [Install and configure Microsoft Dynamics 365 for Finance and Operations - Warehousing](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/install-configure-warehousing-app).</span></span> |
| <span data-ttu-id="06a59-325">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-325">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-326">仓库管理，运输管理</span><span class="sxs-lookup"><span data-stu-id="06a59-326">Warehouse management, Transportation management</span></span>     |
| <span data-ttu-id="06a59-327">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="06a59-327">**Deployment option**</span></span>              | <span data-ttu-id="06a59-328">仓库移动设备门户 (WMDP) 是用于本地自行部署的单独组件。</span><span class="sxs-lookup"><span data-stu-id="06a59-328">Warehouse mobile devices portal (WMDP) was a standalone component that was intended for on-premises self-deployment.</span></span>               |
| <span data-ttu-id="06a59-329">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-329">**Status**</span></span>                         | <span data-ttu-id="06a59-330">已弃用：移除功能的目标时间范围为 2019 年第四季度。</span><span class="sxs-lookup"><span data-stu-id="06a59-330">Deprecated: Target timeframe for the functionality to be removed is Q4 2019.</span></span>   |

### <a name="advanced-bank-reconciliation-matching-rule-for-manual-matching"></a><span data-ttu-id="06a59-331">用于手动匹配的高级银行对帐匹配规则</span><span class="sxs-lookup"><span data-stu-id="06a59-331">Advanced bank reconciliation matching rule for manual matching</span></span>

<span data-ttu-id="06a59-332">匹配规则用于在对帐工作表中手动匹配单据时选择和标记银行单据。</span><span class="sxs-lookup"><span data-stu-id="06a59-332">A matching rule was used to select and mark a bank document when documents were manually matched in the reconciliation worksheet.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-333">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-333">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-334">有限使用。</span><span class="sxs-lookup"><span data-stu-id="06a59-334">Limited usage.</span></span>                                                                         |
| <span data-ttu-id="06a59-335">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-335">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-336">编号</span><span class="sxs-lookup"><span data-stu-id="06a59-336">No.</span></span> <span data-ttu-id="06a59-337">应使用列筛选功能查找用于对帐的单据。</span><span class="sxs-lookup"><span data-stu-id="06a59-337">Column filtering capabilities should be used to find documents for reconciliation.</span></span> |
| <span data-ttu-id="06a59-338">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-338">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-339">现金和银行管理</span><span class="sxs-lookup"><span data-stu-id="06a59-339">Cash and bank management</span></span>                                                               |
| <span data-ttu-id="06a59-340">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="06a59-340">**Deployment option**</span></span>              | <span data-ttu-id="06a59-341">全部</span><span class="sxs-lookup"><span data-stu-id="06a59-341">All</span></span>                                                                                    |
| <span data-ttu-id="06a59-342">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-342">**Status**</span></span>                         | <span data-ttu-id="06a59-343">从 2017 年 7 月开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-343">Removed as of July 2017.</span></span>                                                               |

## <a name="dynamics-365-for-operations-1611-with-platform-update-3"></a><span data-ttu-id="06a59-344">具有平台更新 3 的 Dynamics 365 for Operations 1611</span><span class="sxs-lookup"><span data-stu-id="06a59-344">Dynamics 365 for Operations 1611 with platform update 3</span></span>

### <a name="aeb-payment-formats-for-spain"></a><span data-ttu-id="06a59-345">西班牙的 AEB 付款格式</span><span class="sxs-lookup"><span data-stu-id="06a59-345">AEB payment formats for Spain</span></span>

<span data-ttu-id="06a59-346">Consejo Superior Bancario 付款格式过去用于将汇款文件发送到客户付款和供应商付款的银行。</span><span class="sxs-lookup"><span data-stu-id="06a59-346">The Consejo Superior Bancario payment formats were used to send remittance files to the bank for customer payments and vendor payments.</span></span> <span data-ttu-id="06a59-347">由 Asociación Española de Banca 确定这些格式的内容。</span><span class="sxs-lookup"><span data-stu-id="06a59-347">The content of these formats was determined by the Asociación Española de Banca.</span></span> <span data-ttu-id="06a59-348">它包含 Cuaderno 19、32、58、34。</span><span class="sxs-lookup"><span data-stu-id="06a59-348">It covers Cuaderno 19, 32, 58, 34.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-349">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-349">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-350">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="06a59-350">The payment formats are no longer used.</span></span>                                  |
| <span data-ttu-id="06a59-351">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-351">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-352">是，西班牙的 ISO20022 贷方转帐和直接借记付款格式</span><span class="sxs-lookup"><span data-stu-id="06a59-352">Yes, ISO20022 Credit transfer and Direct debit payment formats for Spain</span></span> |
| <span data-ttu-id="06a59-353">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-353">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-354">应付账款，应收账款</span><span class="sxs-lookup"><span data-stu-id="06a59-354">Accounts payable, Accounts receivable</span></span>                                    |
| <span data-ttu-id="06a59-355">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-355">**Status**</span></span>                         | <span data-ttu-id="06a59-356">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-356">Deprecated: A removal date has not been set for this feature.</span></span>           |

### <a name="bank-payments-transfer-for-lithuania"></a><span data-ttu-id="06a59-357">立陶宛银行付款转帐</span><span class="sxs-lookup"><span data-stu-id="06a59-357">Bank payments transfer for Lithuania</span></span>

<span data-ttu-id="06a59-358">过去使用立陶宛付款转账 (LT) 导出格式生成并打印银行付款转账。</span><span class="sxs-lookup"><span data-stu-id="06a59-358">Bank payment transfers were generated and printed by using the Payment transfer (LT) export format for Lithuania.</span></span> <span data-ttu-id="06a59-359">立陶宛市场于 2005 年开始使用 LITAS，统一电子银行系统。</span><span class="sxs-lookup"><span data-stu-id="06a59-359">The Lithuanian market began to use LITAS, the unified electronic banking system, in 2005.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-360">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-360">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-361">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="06a59-361">The payment formats are no longer used.</span></span>                        |
| <span data-ttu-id="06a59-362">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-362">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-363">是，立陶宛 ISO20022 贷方转帐付款格式</span><span class="sxs-lookup"><span data-stu-id="06a59-363">Yes, ISO20022 Credit transfer payment format for Lithuania</span></span>     |
| <span data-ttu-id="06a59-364">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-364">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-365">应付帐款</span><span class="sxs-lookup"><span data-stu-id="06a59-365">Accounts payable</span></span>                                               |
| <span data-ttu-id="06a59-366">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-366">**Status**</span></span>                         | <span data-ttu-id="06a59-367">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-367">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="bbs-direkte-remittering-payment-formats-for-norway"></a><span data-ttu-id="06a59-368">挪威 BBS Direkte Remittering 付款格式</span><span class="sxs-lookup"><span data-stu-id="06a59-368">BBS Direkte Remittering payment formats for Norway</span></span>

<span data-ttu-id="06a59-369">BBS Direkte Remittering 付款格式包括客户收款导出（直接借记）和返回消息导入。</span><span class="sxs-lookup"><span data-stu-id="06a59-369">BBS Direkte Remittering payment formats include customer payment collection export (direct debit) and return message import.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-370">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-370">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-371">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="06a59-371">The payment formats are no longer used.</span></span>  |
| <span data-ttu-id="06a59-372">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-372">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-373">挪威的 AvtaleGiro 客户付款格式可用于生成直接借记消息。</span><span class="sxs-lookup"><span data-stu-id="06a59-373">The AvtaleGiro customer payment format for Norway can be used to generate direct debit messages.</span></span> <span data-ttu-id="06a59-374">未来版本中将实施返回消息导入。</span><span class="sxs-lookup"><span data-stu-id="06a59-374">Return message import will be implemented in future releases.</span></span> |
| <span data-ttu-id="06a59-375">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-375">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-376">应付账款，应收账款</span><span class="sxs-lookup"><span data-stu-id="06a59-376">Accounts payable, Accounts receivable</span></span>   |
| <span data-ttu-id="06a59-377">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-377">**Status**</span></span>                         | <span data-ttu-id="06a59-378">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-378">Deprecated: A removal date has not been set for this feature.</span></span>                                                                                                 |

### <a name="chart-of-accounts-tool-for-spain"></a><span data-ttu-id="06a59-379">西班牙会计科目表工具</span><span class="sxs-lookup"><span data-stu-id="06a59-379">Chart of Accounts tool for Spain</span></span>

<span data-ttu-id="06a59-380">西班牙会计科目表要求重大更改时使用此工具。</span><span class="sxs-lookup"><span data-stu-id="06a59-380">This tool is used when a chart of accounts in Spain requires major changes.</span></span> <span data-ttu-id="06a59-381">用户可以导入新的 Microsoft Excel 或文本格式的会计科目表，也可以导入财务报表。</span><span class="sxs-lookup"><span data-stu-id="06a59-381">Users can import a new chart of accounts in Microsoft Excel or text format, and can also import financial statements.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-382">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-382">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-383">有限使用</span><span class="sxs-lookup"><span data-stu-id="06a59-383">Limited usage</span></span>                                                  |
| <span data-ttu-id="06a59-384">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-384">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-385">无</span><span class="sxs-lookup"><span data-stu-id="06a59-385">No</span></span>                                                             |
| <span data-ttu-id="06a59-386">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-386">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-387">总帐</span><span class="sxs-lookup"><span data-stu-id="06a59-387">General ledger</span></span>                                                 |
| <span data-ttu-id="06a59-388">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-388">**Status**</span></span>                         | <span data-ttu-id="06a59-389">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-389">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="dom80-payment-format-for-belgium"></a><span data-ttu-id="06a59-390">比利时的 Dom80 付款格式</span><span class="sxs-lookup"><span data-stu-id="06a59-390">Dom80 payment format for Belgium</span></span>

<span data-ttu-id="06a59-391">付款托收的比利时传统付款格式（直接借记）。</span><span class="sxs-lookup"><span data-stu-id="06a59-391">Legacy Belgian payment format for payment collection (direct debit).</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-392">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-392">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-393">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="06a59-393">The payment format is no longer used.</span></span>                          |
| <span data-ttu-id="06a59-394">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-394">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-395">是，比利时 ISO 20022 直接借记付款格式</span><span class="sxs-lookup"><span data-stu-id="06a59-395">Yes, ISO 20022 Direct debit payment format for Belgium</span></span>         |
| <span data-ttu-id="06a59-396">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-396">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-397">应收帐款</span><span class="sxs-lookup"><span data-stu-id="06a59-397">Accounts receivable</span></span>                                            |
| <span data-ttu-id="06a59-398">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-398">**Status**</span></span>                         | <span data-ttu-id="06a59-399">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-399">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="dtaezag-payment-formats-for-switzerland"></a><span data-ttu-id="06a59-400">瑞士的 DTA/EZAG 付款格式</span><span class="sxs-lookup"><span data-stu-id="06a59-400">DTA/EZAG payment formats for Switzerland</span></span>

<span data-ttu-id="06a59-401">DTA/EZAG 格式集成在 ESR 系统中，因为他们可以持有参考编号。</span><span class="sxs-lookup"><span data-stu-id="06a59-401">DTA/EZAG formats are integrated into the ESR system, because they can carry on the reference number.</span></span> <span data-ttu-id="06a59-402">由于参考编号不是必需的，因此可以使用这些格式处理任何供应商付款。</span><span class="sxs-lookup"><span data-stu-id="06a59-402">Because the reference number isn’t mandatory, these formats can be used to process any vendor payments.</span></span> <span data-ttu-id="06a59-403">银行帐户位置不在“Postfinance”的公司使用这些格式。</span><span class="sxs-lookup"><span data-stu-id="06a59-403">These formats are used by companies that have a bank account in a location other than “Postfinance.”</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-404">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-404">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-405">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="06a59-405">The payment formats are no longer used.</span></span>                        |
| <span data-ttu-id="06a59-406">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-406">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-407">是，瑞士 ISO20022 贷方转帐付款格式</span><span class="sxs-lookup"><span data-stu-id="06a59-407">Yes, ISO20022 Credit transfer payment format for Switzerland</span></span>   |
| <span data-ttu-id="06a59-408">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-408">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-409">应付帐款</span><span class="sxs-lookup"><span data-stu-id="06a59-409">Accounts payable</span></span>                                               |
| <span data-ttu-id="06a59-410">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-410">**Status**</span></span>                         | <span data-ttu-id="06a59-411">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-411">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="edifact-dirdeb-payment-format-for-austria"></a><span data-ttu-id="06a59-412">奥地利 EDIFACT-DIRDEB 付款格式</span><span class="sxs-lookup"><span data-stu-id="06a59-412">EDIFACT-DIRDEB payment format for Austria</span></span>

<span data-ttu-id="06a59-413">付款托收的 EDIFACT-DIRDEB 付款格式（直接借记）。</span><span class="sxs-lookup"><span data-stu-id="06a59-413">EDIFACT-DIRDEB payment format for payment collection (direct debit).</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-414">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-414">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-415">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="06a59-415">The payment format is no longer used.</span></span>                          |
| <span data-ttu-id="06a59-416">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-416">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-417">是，奥地利 ISO 20022 直接借记付款格式</span><span class="sxs-lookup"><span data-stu-id="06a59-417">Yes, ISO 20022 Direct debit payment format for Austria</span></span>         |
| <span data-ttu-id="06a59-418">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-418">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-419">应收帐款</span><span class="sxs-lookup"><span data-stu-id="06a59-419">Accounts receivable</span></span>                                            |
| <span data-ttu-id="06a59-420">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-420">**Status**</span></span>                         | <span data-ttu-id="06a59-421">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-421">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="edivat-for-belgium"></a><span data-ttu-id="06a59-422">比利时的 EDIVAT</span><span class="sxs-lookup"><span data-stu-id="06a59-422">EDIVAT for Belgium</span></span>

<span data-ttu-id="06a59-423">EDIVAT 是比利时通过安全电子邮件进行电子申报的已过时的标准做法。</span><span class="sxs-lookup"><span data-stu-id="06a59-423">EDIVAT is an obsolete Belgian standard for electronic declaration via secure mail.</span></span> <span data-ttu-id="06a59-424">Microsoft Dynamics AX 2012 保留启用历史数据访问权限的只读解决方案。</span><span class="sxs-lookup"><span data-stu-id="06a59-424">Microsoft Dynamics AX 2012 retains the read-only solution to enable access to the historical data.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-425">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-425">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-426">此功能不再使用。</span><span class="sxs-lookup"><span data-stu-id="06a59-426">The functionality is no longer used.</span></span>                           |
| <span data-ttu-id="06a59-427">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-427">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-428">无</span><span class="sxs-lookup"><span data-stu-id="06a59-428">No</span></span>                                                             |
| <span data-ttu-id="06a59-429">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-429">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-430">总帐</span><span class="sxs-lookup"><span data-stu-id="06a59-430">General ledger</span></span>                                                 |
| <span data-ttu-id="06a59-431">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-431">**Status**</span></span>                         | <span data-ttu-id="06a59-432">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-432">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="egiro-edifact-cremul-payment-import-format-for-norway"></a><span data-ttu-id="06a59-433">挪威的 eGiro EDIFACT CREMUL 付款导入格式</span><span class="sxs-lookup"><span data-stu-id="06a59-433">eGiro EDIFACT CREMUL payment import format for Norway</span></span>

<span data-ttu-id="06a59-434">eGiro 基于国际 UN EDIFACT CREMUL（多重贷记通知消息）标准，用于客户付款的自动过帐。</span><span class="sxs-lookup"><span data-stu-id="06a59-434">eGiro is based on the international UN EDIFACT CREMUL (Multiple Credit Advice Message) standard that is used for automatic posting of customer payments.</span></span> <span data-ttu-id="06a59-435">在 Microsoft Dynamics AX 中，eGiro 作为客户付款导入格式实施。</span><span class="sxs-lookup"><span data-stu-id="06a59-435">In Microsoft Dynamics AX, eGiro is implemented as a customer payment import format.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-436">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-436">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-437">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="06a59-437">The payment format is no longer used.</span></span>                                                     |
| <span data-ttu-id="06a59-438">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-438">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-439">编号</span><span class="sxs-lookup"><span data-stu-id="06a59-439">No.</span></span> <span data-ttu-id="06a59-440">格式在未来版本中将被 ISO 20022 报表导入格式所取代。</span><span class="sxs-lookup"><span data-stu-id="06a59-440">The format will be replaced by ISO 20022 statement import formats in future releases.</span></span> |
| <span data-ttu-id="06a59-441">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-441">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-442">应收帐款</span><span class="sxs-lookup"><span data-stu-id="06a59-442">Accounts receivable</span></span>                                                                       |
| <span data-ttu-id="06a59-443">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-443">**Status**</span></span>                         | <span data-ttu-id="06a59-444">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-444">Deprecated: A removal date has not been set for this feature.</span></span>                            |

### <a name="external-inventory-for-poland"></a><span data-ttu-id="06a59-445">波兰的外部库存</span><span class="sxs-lookup"><span data-stu-id="06a59-445">External inventory for Poland</span></span>

<span data-ttu-id="06a59-446">来自供应商用于销售且无需购买的货物的证据。</span><span class="sxs-lookup"><span data-stu-id="06a59-446">Evidence of goods that are taken from a vendor for sales without purchase.</span></span> <span data-ttu-id="06a59-447">在外部库存中处理的货物不影响标准库存，可以销售，然后被自动购买。</span><span class="sxs-lookup"><span data-stu-id="06a59-447">Goods that are handled in external inventory don’t affect standard inventory, and can be sold and then purchased automatically.</span></span> <span data-ttu-id="06a59-448">此流程创建实际库存变动。</span><span class="sxs-lookup"><span data-stu-id="06a59-448">This process creates real inventory movements.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-449">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-449">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-450">替换为另一个功能</span><span class="sxs-lookup"><span data-stu-id="06a59-450">Replaced by another feature</span></span>                                    |
| <span data-ttu-id="06a59-451">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-451">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-452">是，为核心入站托运功能</span><span class="sxs-lookup"><span data-stu-id="06a59-452">Yes, the core Inbound consignment functionality</span></span>                |
| <span data-ttu-id="06a59-453">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-453">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-454">应付账款，库存管理</span><span class="sxs-lookup"><span data-stu-id="06a59-454">Accounts payable, Inventory management</span></span>                         |
| <span data-ttu-id="06a59-455">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-455">**Status**</span></span>                         | <span data-ttu-id="06a59-456">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-456">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="financial-reports-generator-for-eastern-europe"></a><span data-ttu-id="06a59-457">东欧的财务报表生成器</span><span class="sxs-lookup"><span data-stu-id="06a59-457">Financial reports generator for Eastern Europe</span></span>

<span data-ttu-id="06a59-458">用于设置会计和纳税报表的数据收集，以及用于将数据导出到 XLS 和 DOC 报表模板的工具。</span><span class="sxs-lookup"><span data-stu-id="06a59-458">A tool is used to set up data collection for accounting and tax reports, and to export data to XLS and DOC report templates.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-459">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-459">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-460">有限使用</span><span class="sxs-lookup"><span data-stu-id="06a59-460">Limited usage</span></span>                                                                            |
| <span data-ttu-id="06a59-461">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-461">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-462">编号</span><span class="sxs-lookup"><span data-stu-id="06a59-462">No.</span></span> <span data-ttu-id="06a59-463">工具在未来版本中将被电子申报配置所取代。</span><span class="sxs-lookup"><span data-stu-id="06a59-463">The tool will be replaced by Electronic reporting configurations in future releases.</span></span> |
| <span data-ttu-id="06a59-464">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-464">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-465">总帐</span><span class="sxs-lookup"><span data-stu-id="06a59-465">General Ledger</span></span>                                                                           |
| <span data-ttu-id="06a59-466">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-466">**Status**</span></span>                         | <span data-ttu-id="06a59-467">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-467">Deprecated: A removal date has not been set for this feature.</span></span>                           |

### <a name="import-of-customer-payment-transactions-for-finland"></a><span data-ttu-id="06a59-468">芬兰的客户付款交易记录导入</span><span class="sxs-lookup"><span data-stu-id="06a59-468">Import of customer payment transactions for Finland</span></span>

<span data-ttu-id="06a59-469">您可以为从银行提供的外部文件导入客户付款交易记录的芬兰付款选择导入格式。</span><span class="sxs-lookup"><span data-stu-id="06a59-469">You can select an import format for Finnish payments to import customer payment transactions from an external file that the bank provides.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-470">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-470">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-471">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="06a59-471">The payment format is no longer used.</span></span>                                                     |
| <span data-ttu-id="06a59-472">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-472">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-473">编号</span><span class="sxs-lookup"><span data-stu-id="06a59-473">No.</span></span> <span data-ttu-id="06a59-474">格式在未来版本中将被 ISO 20022 报表导入格式所取代。</span><span class="sxs-lookup"><span data-stu-id="06a59-474">The format will be replaced by ISO 20022 statement import formats in future releases.</span></span> |
| <span data-ttu-id="06a59-475">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-475">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-476">应收帐款</span><span class="sxs-lookup"><span data-stu-id="06a59-476">Accounts receivable</span></span>                                                                       |
| <span data-ttu-id="06a59-477">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-477">**Status**</span></span>                         | <span data-ttu-id="06a59-478">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-478">Deprecated: A removal date has not been set for this feature.</span></span>                            |

### <a name="import-of-payment-transactions-into-a-general-ledger-journal-for-finland"></a><span data-ttu-id="06a59-479">付款交易记录导入到芬兰的总帐日志帐中</span><span class="sxs-lookup"><span data-stu-id="06a59-479">Import of payment transactions into a general ledger journal for Finland</span></span>

<span data-ttu-id="06a59-480">用于芬兰将会计交易记录导入到总帐的特定格式。</span><span class="sxs-lookup"><span data-stu-id="06a59-480">A format that is specific to Finland is used to import accounting transactions into the general ledger.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-481">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-481">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-482">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="06a59-482">The payment format is no longer used.</span></span>                                                     |
| <span data-ttu-id="06a59-483">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-483">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-484">编号</span><span class="sxs-lookup"><span data-stu-id="06a59-484">No.</span></span> <span data-ttu-id="06a59-485">格式在未来版本中将被 ISO 20022 报表导入格式所取代。</span><span class="sxs-lookup"><span data-stu-id="06a59-485">The format will be replaced by ISO 20022 statement import formats in future releases.</span></span> |
| <span data-ttu-id="06a59-486">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-486">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-487">应收帐款</span><span class="sxs-lookup"><span data-stu-id="06a59-487">Accounts receivable</span></span>                                                                       |
| <span data-ttu-id="06a59-488">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-488">**Status**</span></span>                         | <span data-ttu-id="06a59-489">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-489">Deprecated: A removal date has not been set for this feature.</span></span>                            |

### <a name="integration-with-isabel-synchronized-cis-for-belgium"></a><span data-ttu-id="06a59-490">比利时与 Isabel 同步 (CIS) 集成</span><span class="sxs-lookup"><span data-stu-id="06a59-490">Integration with Isabel synchronized (CIS) for Belgium</span></span>

<span data-ttu-id="06a59-491">Isabel 是欧洲电子银行的框架和比利时的事实标准。</span><span class="sxs-lookup"><span data-stu-id="06a59-491">Isabel is the framework for electronic banking in Europe and is a de-facto standard in Belgium.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-492">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-492">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-493">与 Isabel 客户端的集成已停止。</span><span class="sxs-lookup"><span data-stu-id="06a59-493">Integration with Isabel client has been discontinued.</span></span>   |
| <span data-ttu-id="06a59-494">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-494">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-495">编号</span><span class="sxs-lookup"><span data-stu-id="06a59-495">No.</span></span> <span data-ttu-id="06a59-496">付款格式不再使用，被比利时的 ISO20022 贷方转帐付款格式所取代。</span><span class="sxs-lookup"><span data-stu-id="06a59-496">The payment formats that are no longer used are replaced by ISO20022 Credit transfer payment format for Belgium.</span></span> |
| <span data-ttu-id="06a59-497">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-497">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-498">应付帐款</span><span class="sxs-lookup"><span data-stu-id="06a59-498">Accounts payable</span></span>     |
| <span data-ttu-id="06a59-499">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-499">**Status**</span></span>                         | <span data-ttu-id="06a59-500">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-500">Deprecated: A removal date has not been set for this feature.</span></span>    |

### <a name="modifications-in-the-chart-of-accounts-and-accounting-rules-for-spain"></a><span data-ttu-id="06a59-501">修改西班牙的会计科目表和会计规则</span><span class="sxs-lookup"><span data-stu-id="06a59-501">Modifications in the chart of accounts and accounting rules for Spain</span></span>

<span data-ttu-id="06a59-502">此功能用于修改西班牙的会计科目表和会计规则。</span><span class="sxs-lookup"><span data-stu-id="06a59-502">This feature is used for changes in the chart of accounts and accounting rules in Spain.</span></span> <span data-ttu-id="06a59-503">它映射帐户，以帮助将旧的会计科目表转换到新的会计科目表，将上一个会计年度与新的会计年度相比较，即使是当它们过帐到不同的科目编号时。</span><span class="sxs-lookup"><span data-stu-id="06a59-503">It maps accounts to help transform the old chart of accounts into the new chart of accounts, and compares the previous fiscal year with the new fiscal year, even if they were posted to different account numbers.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-504">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-504">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-505">有限使用</span><span class="sxs-lookup"><span data-stu-id="06a59-505">Limited usage</span></span>                                                  |
| <span data-ttu-id="06a59-506">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-506">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-507">无</span><span class="sxs-lookup"><span data-stu-id="06a59-507">No</span></span>                                                             |
| <span data-ttu-id="06a59-508">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-508">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-509">总帐</span><span class="sxs-lookup"><span data-stu-id="06a59-509">General ledger</span></span>                                                 |
| <span data-ttu-id="06a59-510">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-510">**Status**</span></span>                         | <span data-ttu-id="06a59-511">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-511">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="pagamento-fornittori-vendor-payment-format"></a><span data-ttu-id="06a59-512">Pagamento Fornittori 供应商付款格式</span><span class="sxs-lookup"><span data-stu-id="06a59-512">Pagamento Fornittori vendor payment format</span></span>

<span data-ttu-id="06a59-513">传统意大利贷方转帐付款格式</span><span class="sxs-lookup"><span data-stu-id="06a59-513">Legacy Italian payment format for credit transfers.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-514">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-514">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-515">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="06a59-515">The payment format is no longer used.</span></span>                          |
| <span data-ttu-id="06a59-516">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-516">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-517">是，意大利 ISO20022 贷方转帐付款格式</span><span class="sxs-lookup"><span data-stu-id="06a59-517">Yes, ISO20022 Credit transfer payment format for Italy</span></span>         |
| <span data-ttu-id="06a59-518">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-518">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-519">应付帐款</span><span class="sxs-lookup"><span data-stu-id="06a59-519">Accounts payable</span></span>                                               |
| <span data-ttu-id="06a59-520">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-520">**Status**</span></span>                         | <span data-ttu-id="06a59-521">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-521">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="payment-export-formats-for-estonia"></a><span data-ttu-id="06a59-522">爱沙尼亚付款导出格式</span><span class="sxs-lookup"><span data-stu-id="06a59-522">Payment export formats for Estonia</span></span>

<span data-ttu-id="06a59-523">Telehansa 和 Teleservice 格式为银行付款导出使用。</span><span class="sxs-lookup"><span data-stu-id="06a59-523">The Telehansa and Teleservice formats are used for bank payment export.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-524">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-524">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-525">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="06a59-525">The payment formats are no longer used.</span></span>                        |
| <span data-ttu-id="06a59-526">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-526">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-527">是，爱沙尼亚 ISO20022 贷方转帐付款格式</span><span class="sxs-lookup"><span data-stu-id="06a59-527">Yes, ISO20022 Credit transfer payment format for Estonia</span></span>       |
| <span data-ttu-id="06a59-528">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-528">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-529">应付帐款</span><span class="sxs-lookup"><span data-stu-id="06a59-529">Accounts payable</span></span>                                               |
| <span data-ttu-id="06a59-530">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-530">**Status**</span></span>                         | <span data-ttu-id="06a59-531">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-531">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="payment-file-archive-for-norway"></a><span data-ttu-id="06a59-532">挪威付款文件存档</span><span class="sxs-lookup"><span data-stu-id="06a59-532">Payment file archive for Norway</span></span>

<span data-ttu-id="06a59-533">在生成付款文件时，文件存档自动存档所有创建的文件，甚至包括以前写入或读取的文件。</span><span class="sxs-lookup"><span data-stu-id="06a59-533">When payment files are generated, the file archive automatically archives all files that are created, even files that were previously written or read.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-534">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-534">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-535">替换为另一个功能</span><span class="sxs-lookup"><span data-stu-id="06a59-535">Replaced by another feature</span></span>                                        |
| <span data-ttu-id="06a59-536">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-536">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-537">是，电子申报已存档作业</span><span class="sxs-lookup"><span data-stu-id="06a59-537">Yes, Electronic reporting archived jobs</span></span>                            |
| <span data-ttu-id="06a59-538">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-538">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-539">应付账款，应收账款，组织管理</span><span class="sxs-lookup"><span data-stu-id="06a59-539">Accounts payable, Accounts receivable, Organization administration</span></span> |
| <span data-ttu-id="06a59-540">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-540">**Status**</span></span>                         | <span data-ttu-id="06a59-541">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-541">Deprecated: A removal date has not been set for this feature.</span></span>     |

### <a name="payment-import-formats-for-estonia"></a><span data-ttu-id="06a59-542">爱沙尼亚付款导入格式</span><span class="sxs-lookup"><span data-stu-id="06a59-542">Payment import formats for Estonia</span></span>

<span data-ttu-id="06a59-543">Telehansa 和 TeleTeenus 格式为银行付款导入使用。</span><span class="sxs-lookup"><span data-stu-id="06a59-543">The Telehansa and TeleTeenus formats are used for bank payment import.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-544">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-544">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-545">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="06a59-545">The payment formats are no longer used.</span></span>                                                    |
| <span data-ttu-id="06a59-546">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-546">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-547">编号</span><span class="sxs-lookup"><span data-stu-id="06a59-547">No.</span></span> <span data-ttu-id="06a59-548">格式在未来版本中将被 ISO 20022 报表导入格式所取代。</span><span class="sxs-lookup"><span data-stu-id="06a59-548">The formats will be replaced by ISO 20022 statement import formats in future releases.</span></span> |
| <span data-ttu-id="06a59-549">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-549">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-550">应收帐款</span><span class="sxs-lookup"><span data-stu-id="06a59-550">Accounts receivable</span></span>                                                                        |
| <span data-ttu-id="06a59-551">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-551">**Status**</span></span>                         | <span data-ttu-id="06a59-552">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-552">Deprecated: A removal date has not been set for this feature.</span></span>                             |

### <a name="payroll-information-in-human-resources"></a><span data-ttu-id="06a59-553">人力资源中的工资单信息</span><span class="sxs-lookup"><span data-stu-id="06a59-553">Payroll information in Human Resources</span></span>

<span data-ttu-id="06a59-554">人力资源工资单信息</span><span class="sxs-lookup"><span data-stu-id="06a59-554">Human Resources Payroll information</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-555">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-555">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-556">此功能已由工资单和人力资源页取代。</span><span class="sxs-lookup"><span data-stu-id="06a59-556">This functionality has been replaced by core Payroll and Human Resources pages.</span></span>  |
| <span data-ttu-id="06a59-557">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-557">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-558">**福利**、**收入**和已经位于美国工资单中的其他相关页已被重新配置，现在是核心人力资源配置的一部分，可帮助支持外部工资单处理。</span><span class="sxs-lookup"><span data-stu-id="06a59-558">**Benefits**, **Earnings**, and other related pages that were previously in US Payroll have been reconfigured, and are now part of the core Human Resources configuration to help support external payroll processing.</span></span> <span data-ttu-id="06a59-559">此功能可通过使用**人力资源 1** \> **工资单**配置键访问到。</span><span class="sxs-lookup"><span data-stu-id="06a59-559">This functionality is accessed by using the **Human Resources 1** \> **Payroll** configuration key.</span></span> |
| <span data-ttu-id="06a59-560">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-560">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-561">人力资源、工资单</span><span class="sxs-lookup"><span data-stu-id="06a59-561">Human Resources, Payroll</span></span>   |
| <span data-ttu-id="06a59-562">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-562">**Status**</span></span>                         | <span data-ttu-id="06a59-563">从 Dynamics 365 for Operations 版本 1611 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-563">Removed as of Dynamics 365 for Operations version 1611.</span></span>    |

### <a name="performance-management-goal-workflow"></a><span data-ttu-id="06a59-564">绩效管理目标工作流</span><span class="sxs-lookup"><span data-stu-id="06a59-564">Performance management goal workflow</span></span>

<span data-ttu-id="06a59-565">绩效管理包括目标管理和与绩效审核集成。</span><span class="sxs-lookup"><span data-stu-id="06a59-565">Performance management includes goal management and integration with performance reviews.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-566">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-566">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-567">绩效管理经过重新设计，减少了目标页数，以简化流程。</span><span class="sxs-lookup"><span data-stu-id="06a59-567">Performance management was redesigned, and the number of goal pages was reduced to simplify the process.</span></span>                 |
| <span data-ttu-id="06a59-568">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-568">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-569">编号</span><span class="sxs-lookup"><span data-stu-id="06a59-569">No.</span></span> <span data-ttu-id="06a59-570">目标通过经理自助服务门户对经理可见，并且可由经理进行更改和查看。</span><span class="sxs-lookup"><span data-stu-id="06a59-570">Goals are visible to managers through the Manager Self Service portal, and can be changed and viewed by the manager.</span></span> |
| <span data-ttu-id="06a59-571">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-571">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-572">人力资本管理</span><span class="sxs-lookup"><span data-stu-id="06a59-572">Human capital management</span></span>       |
| <span data-ttu-id="06a59-573">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-573">**Status**</span></span>                         | <span data-ttu-id="06a59-574">从 Dynamics 365 for Operations 版本 1611 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-574">Removed as of Dynamics 365 for Operations version 1611.</span></span>    |

### <a name="postgirot-and-postgirot-utland-payment-formats-for-sweden"></a><span data-ttu-id="06a59-575">瑞典的 Postgirot 和 Postgirot Utland 付款格式</span><span class="sxs-lookup"><span data-stu-id="06a59-575">Postgirot and Postgirot Utland payment formats for Sweden</span></span>

<span data-ttu-id="06a59-576">瑞典的 Postgirot 和 Postgirot Utland 付款格式。</span><span class="sxs-lookup"><span data-stu-id="06a59-576">Postgirot and Postgirot Utland payment formats for Sweden.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-577">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-577">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-578">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="06a59-578">The payment formats are no longer used.</span></span>                        |
| <span data-ttu-id="06a59-579">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-579">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-580">是，瑞典 ISO20022 贷方转帐付款格式</span><span class="sxs-lookup"><span data-stu-id="06a59-580">Yes, ISO20022 Credit transfer payment format for Sweden</span></span>        |
| <span data-ttu-id="06a59-581">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-581">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-582">应付帐款</span><span class="sxs-lookup"><span data-stu-id="06a59-582">Accounts payable</span></span>                                               |
| <span data-ttu-id="06a59-583">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-583">**Status**</span></span>                         | <span data-ttu-id="06a59-584">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-584">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="radio-frequency-identifier"></a><span data-ttu-id="06a59-585">射频标识</span><span class="sxs-lookup"><span data-stu-id="06a59-585">Radio frequency identifier</span></span>

<span data-ttu-id="06a59-586">无线射频标识 (RFID) 是一种使用电子标签存储标识数据的数据收集技术和一种捕获标识数据的无行视域需求阅读器。</span><span class="sxs-lookup"><span data-stu-id="06a59-586">Radio Frequency Identification (RFID) is a data-collection technology that uses electronic tags to store identification data and a no-line-of-sight requirement reader to capture the identification data.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-587">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-587">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-588">低客户使用率和有限功能集。</span><span class="sxs-lookup"><span data-stu-id="06a59-588">Low customer usage and a limited feature set.</span></span>   |
| <span data-ttu-id="06a59-589">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-589">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-590">无</span><span class="sxs-lookup"><span data-stu-id="06a59-590">No</span></span>                                              |
| <span data-ttu-id="06a59-591">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-591">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-592">库存管理</span><span class="sxs-lookup"><span data-stu-id="06a59-592">Inventory management</span></span>                            |
| <span data-ttu-id="06a59-593">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-593">**Status**</span></span>                         | <span data-ttu-id="06a59-594">从 Dynamics 365 for Operations 1611 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-594">Removed as of Dynamics 365 for Operations 1611.</span></span> |

### <a name="report-about-state-invoices-numbering-for-latvia"></a><span data-ttu-id="06a59-595">有关拉脱维亚国家发票编号的报表</span><span class="sxs-lookup"><span data-stu-id="06a59-595">Report about state invoices numbering for Latvia</span></span>

<span data-ttu-id="06a59-596">拉脱维亚法律提供有关销售发票应如何编号的特定规则。</span><span class="sxs-lookup"><span data-stu-id="06a59-596">Latvian legislation provides specific rules about the numbering of sales invoices.</span></span> <span data-ttu-id="06a59-597">此功能允许您基于用户或用户组向销售发票分配具体编号。</span><span class="sxs-lookup"><span data-stu-id="06a59-597">The functionality lets you assign specific numbers to sales invoices, based on the user or user group.</span></span> <span data-ttu-id="06a59-598">之后您可以生成报表或 XML 文件。</span><span class="sxs-lookup"><span data-stu-id="06a59-598">You can then generate a report or an XML file.</span></span> <span data-ttu-id="06a59-599">您还可以打印有关已使用发票编号的报表。</span><span class="sxs-lookup"><span data-stu-id="06a59-599">You can also print a report about invoice numbers that are used.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-600">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-600">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-601">国家发票编号不必再进行维护。</span><span class="sxs-lookup"><span data-stu-id="06a59-601">The state invoice numbering no longer has to be maintained.</span></span> <span data-ttu-id="06a59-602">不再要求有关已使用发票编号的报表。</span><span class="sxs-lookup"><span data-stu-id="06a59-602">The report about used invoice numbers is no longer required.</span></span> |
| <span data-ttu-id="06a59-603">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-603">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-604">无</span><span class="sxs-lookup"><span data-stu-id="06a59-604">No</span></span>       |
| <span data-ttu-id="06a59-605">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-605">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-606">应收帐款</span><span class="sxs-lookup"><span data-stu-id="06a59-606">Accounts receivable</span></span>    |
| <span data-ttu-id="06a59-607">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-607">**Status**</span></span>                         | <span data-ttu-id="06a59-608">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-608">Deprecated: A removal date has not been set for this feature.</span></span>  |

### <a name="set-up-the-names-of-the-manager-and-general-accountant-of-a-company-for-lithuania"></a><span data-ttu-id="06a59-609">设置立陶宛公司的经理和会计主管的姓名</span><span class="sxs-lookup"><span data-stu-id="06a59-609">Set up the names of the manager and general accountant of a company for Lithuania</span></span>

<span data-ttu-id="06a59-610">公司经理和会计主管的姓名可以在公司信息中指定，并用于不同的本地报表打印输出。</span><span class="sxs-lookup"><span data-stu-id="06a59-610">The names of the manager and the general accountant of a company can be specified in the company information and used in different local report printouts.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-611">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-611">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-612">替换为另一个功能</span><span class="sxs-lookup"><span data-stu-id="06a59-612">Replaced by another feature</span></span>                                     |
| <span data-ttu-id="06a59-613">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-613">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-614">是，专员设置可用于同一个目的。</span><span class="sxs-lookup"><span data-stu-id="06a59-614">Yes, the setup of officials can be used for the same purpose.</span></span>   |
| <span data-ttu-id="06a59-615">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-615">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-616">应付账款、应收账款、现金和银行管理</span><span class="sxs-lookup"><span data-stu-id="06a59-616">Accounts payable, Accounts receivable, Cash and bank management</span></span> |
| <span data-ttu-id="06a59-617">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-617">**Status**</span></span>                         | <span data-ttu-id="06a59-618">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-618">Deprecated: A removal date has not been set for this feature.</span></span>  |

### <a name="shipping-carrier-interface"></a><span data-ttu-id="06a59-619">装运承运人界面</span><span class="sxs-lookup"><span data-stu-id="06a59-619">Shipping carrier interface</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-620">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-620">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-621">重复的功能</span><span class="sxs-lookup"><span data-stu-id="06a59-621">Duplicate functionality</span></span>   |
| <span data-ttu-id="06a59-622">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-622">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-623">部分由运输管理取代</span><span class="sxs-lookup"><span data-stu-id="06a59-623">Partially replaced by Transportation management</span></span> |
| <span data-ttu-id="06a59-624">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-624">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-625">销售和市场营销、库存管理</span><span class="sxs-lookup"><span data-stu-id="06a59-625">Sales and marketing, Inventory management</span></span>  |
| <span data-ttu-id="06a59-626">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-626">**Status**</span></span>                         | <span data-ttu-id="06a59-627">从 Dynamics 365 for Operations 版本 1611 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-627">Removed as of Dynamics 365 for Operations version 1611.</span></span>  |

### <a name="telepay-payment-formats-for-norway"></a><span data-ttu-id="06a59-628">挪威 Telepay 付款格式</span><span class="sxs-lookup"><span data-stu-id="06a59-628">Telepay payment formats for Norway</span></span>

<span data-ttu-id="06a59-629">Telepay 付款格式包括供应商付款导出（贷方转帐）和客户付款托收（直接借记）。</span><span class="sxs-lookup"><span data-stu-id="06a59-629">Telepay payment formats include vendor payment export (credit transfer) and customer payment collection (direct debit).</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-630">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-630">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-631">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="06a59-631">The payment formats are no longer used.</span></span>                                                        |
| <span data-ttu-id="06a59-632">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-632">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-633">是，挪威的 ISO20022 贷方转帐付款格式和 AvtaleGiro 客户付款格式</span><span class="sxs-lookup"><span data-stu-id="06a59-633">Yes, ISO20022 Credit transfer payment format and AvtaleGiro customer payment format for Norway</span></span> |
| <span data-ttu-id="06a59-634">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-634">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-635">应付账款，应收账款</span><span class="sxs-lookup"><span data-stu-id="06a59-635">Accounts payable, Accounts receivable</span></span>                                                          |
| <span data-ttu-id="06a59-636">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-636">**Status**</span></span>                         | <span data-ttu-id="06a59-637">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-637">Deprecated: A removal date has not been set for this feature.</span></span>                                 |

### <a name="vendor-payment-export-formats-for-finland"></a><span data-ttu-id="06a59-638">芬兰的供应商付款导出格式</span><span class="sxs-lookup"><span data-stu-id="06a59-638">Vendor payment export formats for Finland</span></span>

<span data-ttu-id="06a59-639">两个导出付款格式可用于芬兰。</span><span class="sxs-lookup"><span data-stu-id="06a59-639">Two formats for exporting payments are available for Finland.</span></span> <span data-ttu-id="06a59-640">LM02 (FI) 用于国内付款，LUM2 (FI) 用于国外付款。</span><span class="sxs-lookup"><span data-stu-id="06a59-640">LM02 (FI) is used for domestic payments, and LUM2 (FI) is used for foreign payments.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-641">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-641">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-642">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="06a59-642">The payment formats are no longer used.</span></span>                        |
| <span data-ttu-id="06a59-643">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-643">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-644">是，芬兰 ISO20022 贷方转帐付款格式</span><span class="sxs-lookup"><span data-stu-id="06a59-644">Yes, ISO20022 Credit transfer payment format for Finland</span></span>       |
| <span data-ttu-id="06a59-645">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-645">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-646">应付帐款</span><span class="sxs-lookup"><span data-stu-id="06a59-646">Accounts payable</span></span>                                               |
| <span data-ttu-id="06a59-647">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-647">**Status**</span></span>                         | <span data-ttu-id="06a59-648">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-648">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="warehouse-management-ii"></a><span data-ttu-id="06a59-649">仓库管理 II</span><span class="sxs-lookup"><span data-stu-id="06a59-649">Warehouse management II</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-650">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-650">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-651">**库存管理**模块中可用的仓库管理 II 解决方案 (WMS II) 与在 Microsoft Dynamics AX 2012 R3 中发布的**仓库管理**模块中的功能重复。</span><span class="sxs-lookup"><span data-stu-id="06a59-651">The Warehouse management II solution (WMS II) that was available in the **Inventory management** module duplicates functionality that is in the **Warehouse management** module that was released in Microsoft Dynamics AX 2012 R3.</span></span>                                                                         |
| <span data-ttu-id="06a59-652">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-652">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-653">在 AX 2012 R3、Microsoft Dynamics AX 2012 R3 CU8 和 Dynamics AX 2012 R3 CU9 中发布的**仓库管理**模块取代仓库管理 II 功能。</span><span class="sxs-lookup"><span data-stu-id="06a59-653">The **Warehouse management** module that was released in AX 2012 R3, Microsoft Dynamics AX 2012 R3 CU8, and Dynamics AX 2012 R3 CU9 replaces the Warehouse management II features.</span></span> <span data-ttu-id="06a59-654">新模块具有比仓库管理 II 更高级的功能和更灵活的仓库管理流程。</span><span class="sxs-lookup"><span data-stu-id="06a59-654">The new module has more advanced features and more flexible warehouse management processes than Warehouse management II.</span></span> |
| <span data-ttu-id="06a59-655">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-655">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-656">库存管理、销售和市场营销、采购</span><span class="sxs-lookup"><span data-stu-id="06a59-656">Inventory management, Sales and marketing, Procurement and sourcing</span></span>   |
| <span data-ttu-id="06a59-657">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-657">**Status**</span></span>                         | <span data-ttu-id="06a59-658">从 Dynamics 365 for Operations 版本 1611 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-658">Removed as of Dynamics 365 for Operations version 1611.</span></span>    |

### <a name="worker-reminders-in-human-resources"></a><span data-ttu-id="06a59-659">人力资源中的工作人员提醒</span><span class="sxs-lookup"><span data-stu-id="06a59-659">Worker reminders in Human Resources</span></span>

<span data-ttu-id="06a59-660">人力资源工资单信息</span><span class="sxs-lookup"><span data-stu-id="06a59-660">Human Resources Payroll information</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-661">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-661">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-662">低使用率</span><span class="sxs-lookup"><span data-stu-id="06a59-662">Low usage</span></span>                                                           |
| <span data-ttu-id="06a59-663">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-663">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-664">无</span><span class="sxs-lookup"><span data-stu-id="06a59-664">No</span></span>                                                                  |
| <span data-ttu-id="06a59-665">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-665">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-666">人力资源</span><span class="sxs-lookup"><span data-stu-id="06a59-666">Human resources</span></span>                                                     |
| <span data-ttu-id="06a59-667">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-667">**Status**</span></span>                         | <span data-ttu-id="06a59-668">从 Dynamics 365 for Operations 版本 1611 开始移除</span><span class="sxs-lookup"><span data-stu-id="06a59-668">Removed as of Dynamics 365 for Operations version 1611</span></span> |

### <a name="workflow-for-creating-goals"></a><span data-ttu-id="06a59-669">创建目标的工作流</span><span class="sxs-lookup"><span data-stu-id="06a59-669">Workflow for creating goals</span></span>

<span data-ttu-id="06a59-670">管理员工目标创建的工作流是多个可用工作流的其中一个，帮助协调绩效管理流程。</span><span class="sxs-lookup"><span data-stu-id="06a59-670">A workflow for managing the creation of employee goals is one of several workflows that were available to help coordinate the performance management process.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-671">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-671">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-672">绩效管理在 Microsoft Dynamics 365 for Finance and Operations 中已经完全重新设计。</span><span class="sxs-lookup"><span data-stu-id="06a59-672">Performance management has been completely redesigned in Microsoft Dynamics 365 for Finance and Operations.</span></span>     |
| <span data-ttu-id="06a59-673">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-673">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-674">经过重新设计的绩效管理功能能够更好地控制目标内容、用来跟踪进度的衡量指标以及支持文档的附加。</span><span class="sxs-lookup"><span data-stu-id="06a59-674">The redesigned Performance management feature gives more control over the content of the goals, the measurements that are used to track progress, and the attachment of supporting documentation.</span></span> <span data-ttu-id="06a59-675">目标可以存储为模板并重复使用。</span><span class="sxs-lookup"><span data-stu-id="06a59-675">Goals can be stored as templates and then reused.</span></span> <span data-ttu-id="06a59-676">此功能可以帮助您更加快速地为您的员工设置额外目标。</span><span class="sxs-lookup"><span data-stu-id="06a59-676">This feature can help you set up additional goals for your employees more quickly.</span></span> |
| <span data-ttu-id="06a59-677">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-677">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-678">人力资本管理</span><span class="sxs-lookup"><span data-stu-id="06a59-678">Human capital management</span></span>                 |
| <span data-ttu-id="06a59-679">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-679">**Status**</span></span>                         | <span data-ttu-id="06a59-680">从 Dynamics 365 for Operations 版本 1611 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-680">Removed as of Dynamics 365 for Operations version 1611.</span></span> |

## <a name="dynamics-ax-70"></a><span data-ttu-id="06a59-681">Dynamics AX 7.0</span><span class="sxs-lookup"><span data-stu-id="06a59-681">Dynamics AX 7.0</span></span> 


### <a name="ability-to-cancel-changes-to-a-vendor-invoice"></a><span data-ttu-id="06a59-682">能够取消对供应商发票的更改</span><span class="sxs-lookup"><span data-stu-id="06a59-682">Ability to cancel changes to a vendor invoice</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-683">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-683">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-684">性能改进</span><span class="sxs-lookup"><span data-stu-id="06a59-684">Performance enhancement</span></span>        |
| <span data-ttu-id="06a59-685">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-685">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-686">无</span><span class="sxs-lookup"><span data-stu-id="06a59-686">No</span></span>                             |
| <span data-ttu-id="06a59-687">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-687">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-688">应付帐款</span><span class="sxs-lookup"><span data-stu-id="06a59-688">Accounts payable</span></span>               |
| <span data-ttu-id="06a59-689">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-689">**Status**</span></span>                         | <span data-ttu-id="06a59-690">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-690">Removed as of Dynamics AX 7.0.</span></span> |

### <a name="aif-axd-and-axbc-integrations"></a><span data-ttu-id="06a59-691">AIF、Axd 和 AxBC 集成</span><span class="sxs-lookup"><span data-stu-id="06a59-691">AIF, AxD, and AxBC integrations</span></span>

<span data-ttu-id="06a59-692">在应用集成框架 (AIF) 中，数据可以通过显示为服务的业务逻辑与外部系统交换。</span><span class="sxs-lookup"><span data-stu-id="06a59-692">In Application Integration Framework (AIF), data can be exchanged with external systems through business logic that is exposed as services.</span></span> <span data-ttu-id="06a59-693">Dynamics AX 包括基于文档和 .NET Business Connector (AxBC) 的服务。</span><span class="sxs-lookup"><span data-stu-id="06a59-693">Dynamics AX includes services that are based on documents and .NET Business Connector (AxBC).</span></span> <span data-ttu-id="06a59-694">文档是通过使用 XML 创建的。</span><span class="sxs-lookup"><span data-stu-id="06a59-694">A document is created by using XML.</span></span> <span data-ttu-id="06a59-695">XML 包括标题信息，添加该信息的目的是创建可在 Dynamics AX 内外传送的*消息*。</span><span class="sxs-lookup"><span data-stu-id="06a59-695">The XML includes header information that is added to create a *message* that can be transferred into or out of Dynamics AX.</span></span> <span data-ttu-id="06a59-696">文档的示例包括销售订单和采购订单。</span><span class="sxs-lookup"><span data-stu-id="06a59-696">Examples of documents include sales orders and purchase orders.</span></span> <span data-ttu-id="06a59-697">但是，几乎所有实体（例如客户）都可以被文档代表。</span><span class="sxs-lookup"><span data-stu-id="06a59-697">However, almost any entity, such as a customer, can be represented by a document.</span></span> <span data-ttu-id="06a59-698">基于文档的服务使用 **Axd \<文档\>** 类。</span><span class="sxs-lookup"><span data-stu-id="06a59-698">Services that are based on documents use the **Axd \<Document\>** classes.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-699">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-699">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-700">AIF 和 AxDs 的体系结构不能扩展到云服务。</span><span class="sxs-lookup"><span data-stu-id="06a59-700">The architecture of AIF and AxDs could not be scaled to a cloud service.</span></span> <span data-ttu-id="06a59-701">批量导入有性能问题。</span><span class="sxs-lookup"><span data-stu-id="06a59-701">There were performance issues around bulk import.</span></span>                                        |
| <span data-ttu-id="06a59-702">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-702">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-703">此功能由数据导入/导出框架取代，该框架支持重复执行的批量导入/导出。</span><span class="sxs-lookup"><span data-stu-id="06a59-703">This feature is replaced by the Data Import/Export framework, which supports recurring bulk import/export.</span></span> <span data-ttu-id="06a59-704">对于 AxBC，我们建议您使用实际表。</span><span class="sxs-lookup"><span data-stu-id="06a59-704">For AxBC, we recommend that you use the actual tables.</span></span> |
| <span data-ttu-id="06a59-705">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-705">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-706">AxDs、AxBC 和 AIF</span><span class="sxs-lookup"><span data-stu-id="06a59-706">AxDs, AxBCs, and AIF</span></span>   |
| <span data-ttu-id="06a59-707">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-707">**Status**</span></span>                         | <span data-ttu-id="06a59-708">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-708">Removed as of Dynamics AX 7.0.</span></span>   |

### <a name="boms-without-bom-versions"></a><span data-ttu-id="06a59-709">没有物料清单版本的物料清单</span><span class="sxs-lookup"><span data-stu-id="06a59-709">BOMs without BOM versions</span></span>

<span data-ttu-id="06a59-710">当禁用**物料清单版本**配置键时，物料清单版本在所有窗体中处于隐藏状态，系统将在已发布的产品和物料清单之间强制 1:1 关系。</span><span class="sxs-lookup"><span data-stu-id="06a59-710">When the **BOM versions** configuration key was disabled, bill of materials (BOM) versions were hidden in all forms, and the system forced a 1:1 relationship between released products and BOMs.</span></span> <span data-ttu-id="06a59-711">在 Dynamics AX 的当前版本中，**物料清单版本**配置键不能禁用。</span><span class="sxs-lookup"><span data-stu-id="06a59-711">In the current version of Dynamics AX, the **BOM versions** configuration key can't be disabled.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-712">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-712">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-713">使用配置键控制物料清单版本不会在云环境中扩展。</span><span class="sxs-lookup"><span data-stu-id="06a59-713">Using a configuration key to control BOM versions doesn't scale in a cloud environment.</span></span> |
| <span data-ttu-id="06a59-714">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-714">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-715">无</span><span class="sxs-lookup"><span data-stu-id="06a59-715">No</span></span>                                                                                      |
| <span data-ttu-id="06a59-716">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-716">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-717">产品信息管理、库存管理</span><span class="sxs-lookup"><span data-stu-id="06a59-717">Product information management, Inventory management</span></span>                                    |
| <span data-ttu-id="06a59-718">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-718">**Status**</span></span>                         | <span data-ttu-id="06a59-719">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-719">Removed as of Dynamics AX 7.0.</span></span>                                                          |

### <a name="brazilian-bordero"></a><span data-ttu-id="06a59-720">巴西 Bordero</span><span class="sxs-lookup"><span data-stu-id="06a59-720">Brazilian Bordero</span></span>

<span data-ttu-id="06a59-721">巴西公司的特定付款方式</span><span class="sxs-lookup"><span data-stu-id="06a59-721">Specific method of payment for Brazilian companies</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-722">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-722">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-723">对巴西 Bordero 付款方式的支持已经在巴西本地化中被中断。</span><span class="sxs-lookup"><span data-stu-id="06a59-723">Support for the Brazilian Bordero method of payment has been discontinued from Brazilian localization</span></span> |
| <span data-ttu-id="06a59-724">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-724">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-725">无</span><span class="sxs-lookup"><span data-stu-id="06a59-725">No</span></span>   |
| <span data-ttu-id="06a59-726">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-726">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-727">应付帐款</span><span class="sxs-lookup"><span data-stu-id="06a59-727">Accounts payable</span></span>   |
| <span data-ttu-id="06a59-728">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-728">**Status**</span></span>                         | <span data-ttu-id="06a59-729">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-729">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="brazilian-sintegra-statement"></a><span data-ttu-id="06a59-730">巴西 Sintegra 报表</span><span class="sxs-lookup"><span data-stu-id="06a59-730">Brazilian Sintegra statement</span></span>

<span data-ttu-id="06a59-731">ICMS 税联邦报税单</span><span class="sxs-lookup"><span data-stu-id="06a59-731">Federal tax statement for ICMS tax</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-732">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-732">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-733">此报表在巴西的部分州不再适用。</span><span class="sxs-lookup"><span data-stu-id="06a59-733">This statement is no longer applicable in some Brazilian states.</span></span> |
| <span data-ttu-id="06a59-734">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-734">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-735">编号</span><span class="sxs-lookup"><span data-stu-id="06a59-735">No.</span></span> <span data-ttu-id="06a59-736">在某些特定情况下，用户可以使用通用电子申报工具配置报表。</span><span class="sxs-lookup"><span data-stu-id="06a59-736">Users can use Generic Electronic reporting tool to configure the statement if required under specific situations.</span></span> |
| <span data-ttu-id="06a59-737">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-737">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-738">会计帐簿</span><span class="sxs-lookup"><span data-stu-id="06a59-738">Fiscal books</span></span>    |
| <span data-ttu-id="06a59-739">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-739">**Status**</span></span>                         | <span data-ttu-id="06a59-740">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-740">Deprecated: A removal date has not been set for this feature.</span></span>   |

### <a name="brazilian-scan-contingency-mode-for-nf-e"></a><span data-ttu-id="06a59-741">巴西的 SCAN NF-e 意外事故模式</span><span class="sxs-lookup"><span data-stu-id="06a59-741">Brazilian SCAN contingency mode for NF-e</span></span>

<span data-ttu-id="06a59-742">(SCAN) 意外事故环境用于在 Secretaria da Fazenda (SEFAZ) 环境不可用时生成、导出和导入 Nota Fiscal eletrônica (NF-e) 的状态。</span><span class="sxs-lookup"><span data-stu-id="06a59-742">(SCAN) contingency environment is used to generate, export, and import the status of a Nota Fiscal eletrônica (NF-e) when the environment of Secretaria da Fazenda (SEFAZ) is not available.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-743">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-743">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-744">此意外事故方法在巴西所有州中不再适用。</span><span class="sxs-lookup"><span data-stu-id="06a59-744">This method of contingency is no longer applicable in all Brazilian states</span></span> |
| <span data-ttu-id="06a59-745">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-745">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-746">无</span><span class="sxs-lookup"><span data-stu-id="06a59-746">No</span></span>                                                                          |
| <span data-ttu-id="06a59-747">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-747">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-748">应收帐款</span><span class="sxs-lookup"><span data-stu-id="06a59-748">Accounts receivable</span></span>                                                         |
| <span data-ttu-id="06a59-749">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-749">**Status**</span></span>                         | <span data-ttu-id="06a59-750">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-750">Deprecated: A removal date has not been set for this feature.</span></span>              |

### <a name="business-analyzer"></a><span data-ttu-id="06a59-751">业务分析器</span><span class="sxs-lookup"><span data-stu-id="06a59-751">Business Analyzer</span></span>

<span data-ttu-id="06a59-752">此移动应用程序能让用户查看关键业务度量。</span><span class="sxs-lookup"><span data-stu-id="06a59-752">This mobile application let users review key business metrics.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-753">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-753">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-754">此功能已被另一个功能取代。</span><span class="sxs-lookup"><span data-stu-id="06a59-754">This functionality has been replaced by another feature.</span></span>   |
| <span data-ttu-id="06a59-755">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-755">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-756">Microsoft Power BI 的监控财务业绩目录包将包括已经在 Business Analyzer 中可用的关键财务度量。</span><span class="sxs-lookup"><span data-stu-id="06a59-756">The Monitor financial performance content pack for Microsoft Power BI will include key financial metrics that were previously available in Business Analyzer.</span></span> |
| <span data-ttu-id="06a59-757">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-757">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-758">总帐</span><span class="sxs-lookup"><span data-stu-id="06a59-758">General ledger</span></span>      |
| <span data-ttu-id="06a59-759">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-759">**Status**</span></span>                         | <span data-ttu-id="06a59-760">已弃用：业务分析器的使用已被弃用。</span><span class="sxs-lookup"><span data-stu-id="06a59-760">Deprecated: The use of Business Analyzer has been deprecated.</span></span>    |

### <a name="business-statistics"></a><span data-ttu-id="06a59-761">业务统计</span><span class="sxs-lookup"><span data-stu-id="06a59-761">Business statistics</span></span>

<span data-ttu-id="06a59-762">设置业务统计查询，以帮助您分析组织的绩效</span><span class="sxs-lookup"><span data-stu-id="06a59-762">The setup of business statistics inquiries that can help you analyze the performance of the organization</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-763">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-763">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-764">商业智能 (BI)、低客户使用率和有限功能集的传统方法</span><span class="sxs-lookup"><span data-stu-id="06a59-764">Legacy approach to business intelligence (BI), low customer usage, and a limited feature set</span></span> |
| <span data-ttu-id="06a59-765">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-765">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-766">Dynamics AX 的当前版本的新 BI 解决方案</span><span class="sxs-lookup"><span data-stu-id="06a59-766">New BI solutions for the current version of Dynamics AX</span></span>                                      |
| <span data-ttu-id="06a59-767">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-767">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-768">采购、应付账款、销售和市场营销、应收账款</span><span class="sxs-lookup"><span data-stu-id="06a59-768">Procurement and sourcing, Accounts payable, Sales and marketing, Accounts receivable</span></span>         |
| <span data-ttu-id="06a59-769">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-769">**Status**</span></span>                         | <span data-ttu-id="06a59-770">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-770">Removed as of Dynamics AX 7.0.</span></span>                                                               |

### <a name="change-document-date-function-in-invoice-approval-journal"></a><span data-ttu-id="06a59-771">更改发票审核日记帐的单据日期功能</span><span class="sxs-lookup"><span data-stu-id="06a59-771">Change document date function in Invoice approval journal</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-772">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-772">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-773">低使用率</span><span class="sxs-lookup"><span data-stu-id="06a59-773">Low usage</span></span>                                                               |
| <span data-ttu-id="06a59-774">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-774">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-775">是。</span><span class="sxs-lookup"><span data-stu-id="06a59-775">Yes.</span></span> <span data-ttu-id="06a59-776">可以更改已过帐供应商交易记录的单据日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-776">The document date on the posted vendor transaction can be changed.</span></span> |
| <span data-ttu-id="06a59-777">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-777">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-778">应付帐款</span><span class="sxs-lookup"><span data-stu-id="06a59-778">Accounts payable</span></span>                                                        |
| <span data-ttu-id="06a59-779">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-779">**Status**</span></span>                         | <span data-ttu-id="06a59-780">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-780">Removed as of Dynamics AX 7.0.</span></span>                                          |

### <a name="clieop03-payment-format-for-the-netherlands"></a><span data-ttu-id="06a59-781">针对荷兰的 ClieOp03 付款格式</span><span class="sxs-lookup"><span data-stu-id="06a59-781">ClieOp03 payment format for the Netherlands</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-782">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-782">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-783">该格式不再适用于荷兰，因为它已被 SEPA 功能取代。</span><span class="sxs-lookup"><span data-stu-id="06a59-783">The format is no longer applicable in the Netherlands, because it has been replaced by SEPA functionality.</span></span> |
| <span data-ttu-id="06a59-784">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-784">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-785">SEPA 付款导出</span><span class="sxs-lookup"><span data-stu-id="06a59-785">SEPA payments export</span></span>  |
| <span data-ttu-id="06a59-786">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-786">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-787">所有模块</span><span class="sxs-lookup"><span data-stu-id="06a59-787">All modules</span></span>     |
| <span data-ttu-id="06a59-788">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-788">**Status**</span></span>                         | <span data-ttu-id="06a59-789">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-789">Deprecated: A removal date has not been set for this feature.</span></span>   |

### <a name="compliance-center"></a><span data-ttu-id="06a59-790">遵从性中心</span><span class="sxs-lookup"><span data-stu-id="06a59-790">Compliance Center</span></span>

<span data-ttu-id="06a59-791">遵从性中心是一个企业门户站点，用于管理与 Sarbanes-Oxley 法案有关的遵从性计划的文档要求。</span><span class="sxs-lookup"><span data-stu-id="06a59-791">The Compliance Center was an Enterprise Portal site for managing the documentation requirements for compliance initiatives that are related to the Sarbanes-Oxley law.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-792">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-792">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-793">缺少客户使用。</span><span class="sxs-lookup"><span data-stu-id="06a59-793">Lack of customer usage.</span></span> <span data-ttu-id="06a59-794">Microsoft SharePoint 包括和遵从性中心功能相同的功能。</span><span class="sxs-lookup"><span data-stu-id="06a59-794">Microsoft SharePoint includes the same capability that was available in the Compliance Center.</span></span> |
| <span data-ttu-id="06a59-795">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-795">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-796">无</span><span class="sxs-lookup"><span data-stu-id="06a59-796">No</span></span>   |
| <span data-ttu-id="06a59-797">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-797">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-798">符合性和内部控制</span><span class="sxs-lookup"><span data-stu-id="06a59-798">Compliance and internal controls</span></span>  |
| <span data-ttu-id="06a59-799">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-799">**Status**</span></span>                         | <span data-ttu-id="06a59-800">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-800">Removed as of Dynamics AX 7.0.</span></span>    |

### <a name="connector-for-microsoft-dynamics"></a><span data-ttu-id="06a59-801">Connector for Microsoft Dynamics</span><span class="sxs-lookup"><span data-stu-id="06a59-801">Connector for Microsoft Dynamics</span></span>

<span data-ttu-id="06a59-802">此工具用于集成从 Microsoft Dynamics CRM 到 Microsoft Dynamics ERP 应用程序的重要数据。</span><span class="sxs-lookup"><span data-stu-id="06a59-802">This tool was used to integrate key data from Microsoft Dynamics CRM to Microsoft Dynamics ERP applications.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-803">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-803">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-804">此功能已被另一个功能取代。</span><span class="sxs-lookup"><span data-stu-id="06a59-804">This functionality has been replaced by another feature.</span></span> |
| <span data-ttu-id="06a59-805">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-805">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-806">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="06a59-806">Common data service</span></span>                                      |
| <span data-ttu-id="06a59-807">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-807">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-808">Connector for Microsoft Dynamics</span><span class="sxs-lookup"><span data-stu-id="06a59-808">Connector for Microsoft Dynamics</span></span>                         |
| <span data-ttu-id="06a59-809">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-809">**Status**</span></span>                         | <span data-ttu-id="06a59-810">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-810">Removed as of Dynamics AX 7.0.</span></span>                           |

### <a name="container-unit-and-multi-dimension-on-hand"></a><span data-ttu-id="06a59-811">容器单位和多维现有量</span><span class="sxs-lookup"><span data-stu-id="06a59-811">Container unit and multi dimension on-hand</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-812">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-812">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-813">重复的功能</span><span class="sxs-lookup"><span data-stu-id="06a59-813">Duplicate functionality</span></span> |
| <span data-ttu-id="06a59-814">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-814">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-815">是。</span><span class="sxs-lookup"><span data-stu-id="06a59-815">Yes.</span></span> <span data-ttu-id="06a59-816">自 AX 2012 起，此功能已由合并的批次订单功能集替换。</span><span class="sxs-lookup"><span data-stu-id="06a59-816">Since AX 2012, this functionality has been replaced by the consolidated batch orders feature set.</span></span> <span data-ttu-id="06a59-817">此功能集包括合并的现有量视图。</span><span class="sxs-lookup"><span data-stu-id="06a59-817">This feature set includes the consolidated on-hand view.</span></span> |
| <span data-ttu-id="06a59-818">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-818">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-819">产品信息控制管理、生产控制、库存管理、销售和市场营销</span><span class="sxs-lookup"><span data-stu-id="06a59-819">Product information management, Production control, Inventory management, Sales and marketing</span></span>  |
| <span data-ttu-id="06a59-820">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-820">**Status**</span></span>                         | <span data-ttu-id="06a59-821">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-821">Removed as of Dynamics AX 7.0.</span></span> |

### <a name="cue-group-metadata"></a><span data-ttu-id="06a59-822">提示组元数据</span><span class="sxs-lookup"><span data-stu-id="06a59-822">Cue group metadata</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-823">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-823">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-824">提示组用于在 FactBox 区域中显示一个或多个提示。</span><span class="sxs-lookup"><span data-stu-id="06a59-824">Cue groups were used to display one or more Cues in the FactBox area.</span></span> <span data-ttu-id="06a59-825">由于父窗体中的记录更改会导致提示组中每个提示对应一个查询，因此它的接受程度有限，而且还存在性能顾虑。</span><span class="sxs-lookup"><span data-stu-id="06a59-825">There was limited uptake, and there were also performance concerns, because a record change in a parent form caused one query per Cue in the Cue group.</span></span> |
| <span data-ttu-id="06a59-826">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-826">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-827">无</span><span class="sxs-lookup"><span data-stu-id="06a59-827">No</span></span>      |
| <span data-ttu-id="06a59-828">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-828">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-829">所有模块</span><span class="sxs-lookup"><span data-stu-id="06a59-829">All modules</span></span>    |
| <span data-ttu-id="06a59-830">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-830">**Status**</span></span>                         | <span data-ttu-id="06a59-831">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-831">Removed as of Dynamics AX 7.0.</span></span>  |

### <a name="cue-metadata"></a><span data-ttu-id="06a59-832">提示元数据</span><span class="sxs-lookup"><span data-stu-id="06a59-832">Cue metadata</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-833">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-833">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-834">提示元数据仅限于计数或合计信息。</span><span class="sxs-lookup"><span data-stu-id="06a59-834">Cue metadata was limited to count or sum information.</span></span>    |
| <span data-ttu-id="06a59-835">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-835">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-836">引入了磁贴元数据，可为建模提供更多灵活性。</span><span class="sxs-lookup"><span data-stu-id="06a59-836">Tile metadata was introduced to provide more flexibility for modeling.</span></span> <span data-ttu-id="06a59-837">例如，您可以对当前计数、导航和关键绩效指标 (KPI) 进行建模。</span><span class="sxs-lookup"><span data-stu-id="06a59-837">For example, you can model current counts, navigation, and key performance indicators (KPIs).</span></span> <span data-ttu-id="06a59-838">计数磁贴元数据是提示元数据的直接取代。</span><span class="sxs-lookup"><span data-stu-id="06a59-838">Count tile metadata is the direct replacement of the Cue metadata.</span></span> |
| <span data-ttu-id="06a59-839">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-839">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-840">所有模块</span><span class="sxs-lookup"><span data-stu-id="06a59-840">All modules</span></span>           |
| <span data-ttu-id="06a59-841">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-841">**Status**</span></span>                         | <span data-ttu-id="06a59-842">从 Dynamics AX 7.0 开始移除</span><span class="sxs-lookup"><span data-stu-id="06a59-842">Removed as of Dynamics AX 7.0</span></span>      |

### <a name="danish-check-format"></a><span data-ttu-id="06a59-843">丹麦支票格式</span><span class="sxs-lookup"><span data-stu-id="06a59-843">Danish check format</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-844">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-844">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-845">对丹麦支票格式布局的支持已终止，并且报告已经从 DK 本地化中删除。</span><span class="sxs-lookup"><span data-stu-id="06a59-845">Support for the Danish check format layout has been discontinued, and the report has been removed from DK localization.</span></span> |
| <span data-ttu-id="06a59-846">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-846">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-847">无</span><span class="sxs-lookup"><span data-stu-id="06a59-847">No</span></span>    |
| <span data-ttu-id="06a59-848">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-848">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-849">所有模块</span><span class="sxs-lookup"><span data-stu-id="06a59-849">All modules</span></span>    |
| <span data-ttu-id="06a59-850">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-850">**Status**</span></span>                         | <span data-ttu-id="06a59-851">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-851">Deprecated: A removal date has not been set for this feature.</span></span>  |

### <a name="data-partitions"></a><span data-ttu-id="06a59-852">数据分区</span><span class="sxs-lookup"><span data-stu-id="06a59-852">Data partitions</span></span>

<span data-ttu-id="06a59-853">数据分区在 Microsoft Dynamics AX 数据库中提供数据的逻辑界定。</span><span class="sxs-lookup"><span data-stu-id="06a59-853">Data partitions provide a logical separation of data in the Microsoft Dynamics AX database.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-854">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-854">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-855">数据分区在 Microsoft Dynamics AX 2012 R2 引入以启用数据隔离。</span><span class="sxs-lookup"><span data-stu-id="06a59-855">Data partitions were introduced in Microsoft Dynamics AX 2012 R2 to enable data isolation.</span></span> <span data-ttu-id="06a59-856">在常见情况中，公司有子公司，一个子公司的数据不应对另一个子公司可见，即使两个子公司均由相同的 IT 部门管理。</span><span class="sxs-lookup"><span data-stu-id="06a59-856">In a common scenario, a company has subsidiaries, and the data from one subsidiary should not be visible to another subsidiary, even though both subsidiaries are managed by the same IT department.</span></span> <span data-ttu-id="06a59-857">不过，整个程序都需要额外的脚本和管理开销来创建新的分区并填充数据，以及备份分区数据。</span><span class="sxs-lookup"><span data-stu-id="06a59-857">However, extra scripts and management overhead throughout the program were required in order to create new partitions and populate them with data, and to back up partition data.</span></span> <span data-ttu-id="06a59-858">在云中，在其中我们有访问平台即服务 (PaaS) 数据库服务（Microsoft SQL Azure 数据库）的权限，则使用数据库作为隔离容器比在程序中执行隔离要高效得多。</span><span class="sxs-lookup"><span data-stu-id="06a59-858">In the cloud, where we have access to platform as a service (PaaS) database services (Microsoft Azure SQL Database), it's much more efficient to use a database as the isolation container than to do isolation in the program.</span></span> <span data-ttu-id="06a59-859">不管是子公司、多个租户，或只为规模需要进行数据分区，我们认为通过多个 Finance and Operations 实例都可以更好地处理这种情况。</span><span class="sxs-lookup"><span data-stu-id="06a59-859">Regardless of whether data partitioning is required for subsidiaries, for multiple tenants, or just for scale, we believe that the scenarios can be handled better through multiple instances of Finance and Operations.</span></span> |
| <span data-ttu-id="06a59-860">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-860">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-861">如果数据库级别分隔是关键问题，使用数据分区的客户必须使用多个 Finance and Operations 实例。</span><span class="sxs-lookup"><span data-stu-id="06a59-861">Customers using data partitions must use multiple instances of Finance and Operations if database level separation is a critical issue.</span></span>    |
| <span data-ttu-id="06a59-862">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-862">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-863">所有模块</span><span class="sxs-lookup"><span data-stu-id="06a59-863">All modules</span></span>  |
| <span data-ttu-id="06a59-864">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-864">**Status**</span></span>                         | <span data-ttu-id="06a59-865">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-865">Removed as of Dynamics AX 7.0.</span></span>  |


### <a name="database-and-file-share-storage-for-attachments"></a><span data-ttu-id="06a59-866">数据库和文件共享附件存储</span><span class="sxs-lookup"><span data-stu-id="06a59-866">Database and file share storage for attachments</span></span>

<span data-ttu-id="06a59-867">Microsoft Dynamics AX 2012 允许在数据库和文件共享中存储附件。</span><span class="sxs-lookup"><span data-stu-id="06a59-867">Microsoft Dynamics AX 2012 allowed storage of attachments in the database and in file shares.</span></span> <span data-ttu-id="06a59-868">这两个选项都不再受支持。</span><span class="sxs-lookup"><span data-stu-id="06a59-868">Both of those options are no longer supported.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-869">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-869">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-870">云托管的环境无法再与本地文件共享通信，因此文件共享存储不再受支持。</span><span class="sxs-lookup"><span data-stu-id="06a59-870">Files share storage is no longer supported because cloud-hosted environments cannot communicate with local file shares.</span></span> <span data-ttu-id="06a59-871">为了支持 Azure Blob 存储，数据库存储已弃用。</span><span class="sxs-lookup"><span data-stu-id="06a59-871">Database storage has been deprecated in favor of Azure Blob storage.</span></span> <span data-ttu-id="06a59-872">Azure Blob 存储相当于数据库中的存储，因为文档仅可以通过 Dynamics 365 for Finance and Operations 客户端窗体进行访问。</span><span class="sxs-lookup"><span data-stu-id="06a59-872">Azure Blob storage is equivalent to storage in the database, as documents can only be accessed through Dynamics 365 for Finance and Operations client forms.</span></span> <span data-ttu-id="06a59-873">这提供额外好处，即提供存储不会对数据库的性能造成不利影响。</span><span class="sxs-lookup"><span data-stu-id="06a59-873">This provides the added benefit of providing storage that doesn't negatively affect the performance of the database.</span></span> <span data-ttu-id="06a59-874">Blob 存储是文档管理的默认存储机制并立即生效。</span><span class="sxs-lookup"><span data-stu-id="06a59-874">Blob storage is the default storage mechanism for Document Management and works immediately.</span></span> |
| <span data-ttu-id="06a59-875">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-875">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-876">为了支持 Azure Blob 存储，数据库存储已弃用。</span><span class="sxs-lookup"><span data-stu-id="06a59-876">Database storage has been deprecated in favor of Azure Blob storage.</span></span>   |
| <span data-ttu-id="06a59-877">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-877">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-878">所有模块</span><span class="sxs-lookup"><span data-stu-id="06a59-878">All modules</span></span>  |
| <span data-ttu-id="06a59-879">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-879">**Status**</span></span>                         | <span data-ttu-id="06a59-880">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-880">Removed as of Dynamics AX 7.0.</span></span>   |

### <a name="delimitation"></a><span data-ttu-id="06a59-881">界定</span><span class="sxs-lookup"><span data-stu-id="06a59-881">Delimitation</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-882">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-882">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-883">找不到该功能的使用。</span><span class="sxs-lookup"><span data-stu-id="06a59-883">No use of the functionality was found.</span></span> |
| <span data-ttu-id="06a59-884">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-884">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-885">无</span><span class="sxs-lookup"><span data-stu-id="06a59-885">No</span></span>                                     |
| <span data-ttu-id="06a59-886">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-886">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-887">考勤管理</span><span class="sxs-lookup"><span data-stu-id="06a59-887">Time and attendance</span></span>                    |
| <span data-ttu-id="06a59-888">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-888">**Status**</span></span>                         | <span data-ttu-id="06a59-889">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-889">Removed as of Dynamics AX 7.0.</span></span>         |

### <a name="desktop-client"></a><span data-ttu-id="06a59-890">桌面客户端</span><span class="sxs-lookup"><span data-stu-id="06a59-890">Desktop client</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-891">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-891">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-892">Dynamics AX 客户端体验已被重新设计，可提高在多个平台和设备上的可用性。</span><span class="sxs-lookup"><span data-stu-id="06a59-892">The Dynamics AX client experience has been redesigned to improve usability across multiple platforms and devices.</span></span>                      |
| <span data-ttu-id="06a59-893">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-893">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-894">新的 Web 客户端基于已经过修改可提供丰富 Web 平台的桌面窗体元数据和编程模型。</span><span class="sxs-lookup"><span data-stu-id="06a59-894">The new web client is based on the desktop Form metadata and programming model that have been modified to provide a rich web platform.</span></span> |
| <span data-ttu-id="06a59-895">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-895">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-896">所有模块</span><span class="sxs-lookup"><span data-stu-id="06a59-896">All modules</span></span>  |
| <span data-ttu-id="06a59-897">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-897">**Status**</span></span>                         | <span data-ttu-id="06a59-898">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-898">Removed as of Dynamics AX 7.0.</span></span>   |

### <a name="direct-database-connection"></a><span data-ttu-id="06a59-899">直接数据库连接</span><span class="sxs-lookup"><span data-stu-id="06a59-899">Direct database connection</span></span>

<span data-ttu-id="06a59-900">在 Dynamics AX 2012 R3 中，Retail Modern POS 可以直接连接到与 Enterprise POS 方式相似的通道 DB。</span><span class="sxs-lookup"><span data-stu-id="06a59-900">In Dynamics AX 2012 R3, Retail Modern POS could connect directly to the Channel DB in similar fashion to Enterprise POS.</span></span> <span data-ttu-id="06a59-901">这是除通过 Retail Server 的 Retail Modern POS 通信的标准通信方法以外的方法。</span><span class="sxs-lookup"><span data-stu-id="06a59-901">This was in addition to the standard communication method of Retail Modern POS communicating through Retail Server.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-902">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-902">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-903">直接数据库连接要求较低的安全协议，主要用于达到最高性能级别。</span><span class="sxs-lookup"><span data-stu-id="06a59-903">Direct database connectivity required lower security protocols and was primarily used to achieve the highest levels of performance.</span></span> <span data-ttu-id="06a59-904">由于 Finance and Operations 发生的性能和安全性提高，此功能现在导致的问题比解决的问题更多。</span><span class="sxs-lookup"><span data-stu-id="06a59-904">Due to the performance and security enhancements that have occurred in Finance and Operations, this functionality now causes more issues than it solves.</span></span> |
| <span data-ttu-id="06a59-905">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-905">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-906">编号</span><span class="sxs-lookup"><span data-stu-id="06a59-906">No.</span></span> <span data-ttu-id="06a59-907">现在只支持标准零售服务器通信。</span><span class="sxs-lookup"><span data-stu-id="06a59-907">Only standard Retail Server communication is now supported.</span></span>  |
| <span data-ttu-id="06a59-908">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-908">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-909">通道 DB/Retail Modern POS</span><span class="sxs-lookup"><span data-stu-id="06a59-909">Channel DB/Retail Modern POS</span></span>   |
| <span data-ttu-id="06a59-910">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-910">**Status**</span></span>                         | <span data-ttu-id="06a59-911">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-911">Removed as of Dynamics AX 7.0.</span></span>  |

### <a name="dutch-swift-mt940"></a><span data-ttu-id="06a59-912">荷兰 SWIFT MT940</span><span class="sxs-lookup"><span data-stu-id="06a59-912">Dutch SWIFT MT940</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-913">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-913">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-914">现在使用的是通用功能，而不是本地化功能。</span><span class="sxs-lookup"><span data-stu-id="06a59-914">Generic functionality is now used instead of localized functionality.</span></span>                    |
| <span data-ttu-id="06a59-915">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-915">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-916">是，此功能已被高级银行对帐功能取代。</span><span class="sxs-lookup"><span data-stu-id="06a59-916">Yes, this functionality has been replaced by Advanced bank reconciliation functionality.</span></span> |
| <span data-ttu-id="06a59-917">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-917">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-918">所有模块</span><span class="sxs-lookup"><span data-stu-id="06a59-918">All modules</span></span>                                                                              |
| <span data-ttu-id="06a59-919">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-919">**Status**</span></span>                         | <span data-ttu-id="06a59-920">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-920">Deprecated: A removal date has not been set for this feature.</span></span>                           |

### <a name="ebilanz-xbrl-for-germany"></a><span data-ttu-id="06a59-921">eBilanz（针对德国的 XBRL）</span><span class="sxs-lookup"><span data-stu-id="06a59-921">eBilanz (XBRL for Germany)</span></span>

<span data-ttu-id="06a59-922">此功能专门针对德国 eBilanz 分类提供了可扩展业务报告语言 (XBRL) 输出。</span><span class="sxs-lookup"><span data-stu-id="06a59-922">This functionality provided eXtensible Business Reporting Language (XBRL) output that is intended specifically for the German eBilanz taxonomy.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-923">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-923">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-924">缺少客户使用</span><span class="sxs-lookup"><span data-stu-id="06a59-924">Lack of customer usage</span></span>  |
| <span data-ttu-id="06a59-925">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-925">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-926">此功能尚未被另一个功能取代，不过，多个提供丰富 XBRL 功能的专用 XBRL 程序包对德国市场可用。</span><span class="sxs-lookup"><span data-stu-id="06a59-926">This feature hasn't been replaced by another feature, but multiple specialized XBRL packages that provide rich XBRL functionality are available for the German market.</span></span> |
| <span data-ttu-id="06a59-927">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-927">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-928">Management Reporter</span><span class="sxs-lookup"><span data-stu-id="06a59-928">Management Reporter</span></span>      |
| <span data-ttu-id="06a59-929">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-929">**Status**</span></span>                         | <span data-ttu-id="06a59-930">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-930">Deprecated: A removal date has not been set for this feature.</span></span>  |

### <a name="enterprise-portal-client"></a><span data-ttu-id="06a59-931">企业门户客户端</span><span class="sxs-lookup"><span data-stu-id="06a59-931">Enterprise Portal client</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-932">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-932">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-933">提供了一个客户端平台。</span><span class="sxs-lookup"><span data-stu-id="06a59-933">A single client platform has been provided.</span></span>  |
| <span data-ttu-id="06a59-934">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-934">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-935">新的 Web 客户端基于已经过修改可提供丰富 Web 平台的桌面窗体元数据和编程模型。</span><span class="sxs-lookup"><span data-stu-id="06a59-935">The new web client is based on the desktop form metadata and programming model that have been modified to provide a rich web platform.</span></span> |
| <span data-ttu-id="06a59-936">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-936">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-937">所有模块</span><span class="sxs-lookup"><span data-stu-id="06a59-937">All modules</span></span>  |
| <span data-ttu-id="06a59-938">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-938">**Status**</span></span>                         | <span data-ttu-id="06a59-939">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-939">Removed as of Dynamics AX 7.0.</span></span>   |

### <a name="environmental-sustainability"></a><span data-ttu-id="06a59-940">环境可持续性</span><span class="sxs-lookup"><span data-stu-id="06a59-940">Environmental sustainability</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-941">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-941">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-942">低客户使用率和有限功能集</span><span class="sxs-lookup"><span data-stu-id="06a59-942">Low customer usage and a limited feature set</span></span>  |
| <span data-ttu-id="06a59-943">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-943">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-944">无</span><span class="sxs-lookup"><span data-stu-id="06a59-944">No</span></span>              |
| <span data-ttu-id="06a59-945">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-945">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-946">遵从性和内部控制、应付账款</span><span class="sxs-lookup"><span data-stu-id="06a59-946">Compliance and internal controls, Accounts payable</span></span>  |
| <span data-ttu-id="06a59-947">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-947">**Status**</span></span>                         | <span data-ttu-id="06a59-948">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-948">Removed as of Dynamics AX 7.0.</span></span> |

### <a name="form-activex-and-managed-host-controls"></a><span data-ttu-id="06a59-949">窗体 ActiveX 和托管主机控件</span><span class="sxs-lookup"><span data-stu-id="06a59-949">Form ActiveX and Managed Host controls</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-950">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-950">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-951">ActiveX 和托管主机控件基于已废弃的桌面客户端。</span><span class="sxs-lookup"><span data-stu-id="06a59-951">The ActiveX and Managed Host controls are based on the deprecated desktop client.</span></span> |
| <span data-ttu-id="06a59-952">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-952">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-953">可扩展控件框架支持构建新的基于 HTML、CSS 和 JavaScript 的控件，并且是 Microsoft Visual Studio 工具环境中的一流控件。</span><span class="sxs-lookup"><span data-stu-id="06a59-953">The extensible control framework supports building new controls that are based on HTML, CSS, and JavaScript, and is a first-class control in the Microsoft Visual Studio Tooling environment.</span></span> |
| <span data-ttu-id="06a59-954">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-954">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-955">所有模块</span><span class="sxs-lookup"><span data-stu-id="06a59-955">All modules</span></span>     |
| <span data-ttu-id="06a59-956">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-956">**Status**</span></span>                         | <span data-ttu-id="06a59-957">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-957">Removed as of Dynamics AX 7.0.</span></span>       |

### <a name="generate-prenotes-by-using-a-batch"></a><span data-ttu-id="06a59-958">通过使用批处理生成预验证</span><span class="sxs-lookup"><span data-stu-id="06a59-958">Generate prenotes by using a batch</span></span>

<span data-ttu-id="06a59-959">预验证生成无法通过使用批处理完成，但仍可以由用户完成。</span><span class="sxs-lookup"><span data-stu-id="06a59-959">Prenote generation can't be done by using a batch, but it can still be done by a user.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-960">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-960">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-961">在通过使用批处理生成预验证文件时，没有窗体持续存在并且显示生成的预验证文件。</span><span class="sxs-lookup"><span data-stu-id="06a59-961">No form exists to persist and display the resulting prenote file when it's generated by using a batch.</span></span> |
| <span data-ttu-id="06a59-962">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-962">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-963">预验证仍可以生成，并且用户能够控制该文件的保存位置。</span><span class="sxs-lookup"><span data-stu-id="06a59-963">Prenotes can still be generated, and the user has control over the location where the file is saved.</span></span>   |
| <span data-ttu-id="06a59-964">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-964">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-965">应付账款、应收账款、现金和银行管理</span><span class="sxs-lookup"><span data-stu-id="06a59-965">Accounts payable, Accounts receivable, Cash and bank management</span></span>  |
| <span data-ttu-id="06a59-966">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-966">**Status**</span></span>                         | <span data-ttu-id="06a59-967">从 AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-967">Removed as of AX 7.0.</span></span>    |

### <a name="german-dtaus-payment-export-and-account-statement-import-totals-and-transactions"></a><span data-ttu-id="06a59-968">德国 DTAUS 付款导出和帐户对账单导入（合计和交易记录）</span><span class="sxs-lookup"><span data-stu-id="06a59-968">German DTAUS payment export and account statement import (totals and transactions)</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-969">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-969">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-970">该格式不再适用于德国，因为它已被单一欧元支付区 (SEPA) 功能取代。</span><span class="sxs-lookup"><span data-stu-id="06a59-970">The format is no longer applicable in Germany, because it has been replaced by Single Euro Payments Area (SEPA) functionality.</span></span>                    |
| <span data-ttu-id="06a59-971">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-971">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-972">是，此功能已被 SEPA 付款导出和高级银行对帐功能（用于导入帐户对账单）取代。</span><span class="sxs-lookup"><span data-stu-id="06a59-972">Yes, this functionality has been replaced by SEPA payment export and advanced bank reconciliation functionality for importing account statements.</span></span> |
| <span data-ttu-id="06a59-973">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-973">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-974">所有模块</span><span class="sxs-lookup"><span data-stu-id="06a59-974">All modules</span></span>  |
| <span data-ttu-id="06a59-975">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-975">**Status**</span></span>                         | <span data-ttu-id="06a59-976">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-976">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="german-dtazv-payment-format"></a><span data-ttu-id="06a59-977">德国 DTAZV 付款格式</span><span class="sxs-lookup"><span data-stu-id="06a59-977">German DTAZV payment format</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-978">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-978">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-979">该格式不再适用于德国，因为它已被 SEPA 功能取代。</span><span class="sxs-lookup"><span data-stu-id="06a59-979">The format is no longer applicable in Germany, because it has been replaced by SEPA functionality.</span></span> |
| <span data-ttu-id="06a59-980">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-980">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-981">SEPA 付款导出</span><span class="sxs-lookup"><span data-stu-id="06a59-981">SEPA payments export</span></span>    |
| <span data-ttu-id="06a59-982">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-982">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-983">所有模块</span><span class="sxs-lookup"><span data-stu-id="06a59-983">All modules</span></span>   |
| <span data-ttu-id="06a59-984">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-984">**Status**</span></span>                         | <span data-ttu-id="06a59-985">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-985">Deprecated: A removal date has not been set for this feature.</span></span>    |

### <a name="german-mt940-import"></a><span data-ttu-id="06a59-986">德国 MT940 导入</span><span class="sxs-lookup"><span data-stu-id="06a59-986">German MT940 import</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-987">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-987">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-988">现在使用的是通用功能，而不是本地化功能。</span><span class="sxs-lookup"><span data-stu-id="06a59-988">Generic functionality is now used instead of localized functionality.</span></span>                    |
| <span data-ttu-id="06a59-989">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-989">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-990">是，此功能已被高级银行对帐功能取代。</span><span class="sxs-lookup"><span data-stu-id="06a59-990">Yes, this functionality has been replaced by Advanced bank reconciliation functionality.</span></span> |
| <span data-ttu-id="06a59-991">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-991">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-992">所有模块</span><span class="sxs-lookup"><span data-stu-id="06a59-992">All modules</span></span>                                                                              |
| <span data-ttu-id="06a59-993">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-993">**Status**</span></span>                         | <span data-ttu-id="06a59-994">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-994">Deprecated: A removal date has not been set for this feature.</span></span>                           |

### <a name="german-xml-eu-sales-list"></a><span data-ttu-id="06a59-995">德国 XML 欧盟销售清单</span><span class="sxs-lookup"><span data-stu-id="06a59-995">German XML EU Sales list</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-996">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-996">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-997">不再支持德国欧盟销售清单报表的 XML 格式。</span><span class="sxs-lookup"><span data-stu-id="06a59-997">The XML format for German EU Sales List reporting is no longer supported.</span></span> <span data-ttu-id="06a59-998">仅 ELMA5 文本文件格式可用于将欧盟销售清单报表提交给德国税务局。</span><span class="sxs-lookup"><span data-stu-id="06a59-998">Only the ELMA5 text file format can be used to submit the EU Sales List report to the German Tax Office.</span></span> |
| <span data-ttu-id="06a59-999">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-999">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-1000">无</span><span class="sxs-lookup"><span data-stu-id="06a59-1000">No</span></span>         |
| <span data-ttu-id="06a59-1001">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-1001">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-1002">税金</span><span class="sxs-lookup"><span data-stu-id="06a59-1002">Tax</span></span>        |
| <span data-ttu-id="06a59-1003">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-1003">**Status**</span></span>                         | <span data-ttu-id="06a59-1004">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-1004">Deprecated: A removal date has not been set for this feature.</span></span>   |

### <a name="gl-ssrs-reports"></a><span data-ttu-id="06a59-1005">GL SSRS 报表</span><span class="sxs-lookup"><span data-stu-id="06a59-1005">GL SSRS reports</span></span>

<span data-ttu-id="06a59-1006">包括以下菜单项的报表已被删除：**试算平衡表(汇总)**、**试算平衡表(明细)**、**会计科目表**、**审计线索**、**余额**和**余额表**。</span><span class="sxs-lookup"><span data-stu-id="06a59-1006">Reports that include the following menu items have been removed: **Summary trial balance**, **Detailed trial balance**, **Chart of accounts**, **Audit trail**, **Balances**, and **Balance list**.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-1007">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-1007">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-1008">财务 Microsoft SQL Server Reporting Services (SSRS) 报表已经被 Management Reporter 功能和默认报表取代。</span><span class="sxs-lookup"><span data-stu-id="06a59-1008">Financial Microsoft SQL Server Reporting Services (SSRS) reports have been replaced by Management Reporter capabilities and default reports.</span></span> |
| <span data-ttu-id="06a59-1009">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-1009">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-1010">Management Reporter（在 Dynamics AX 的当前版本中标记为**财务报告**。）</span><span class="sxs-lookup"><span data-stu-id="06a59-1010">Management Reporter (labeled **Financial reporting** in the current version of Dynamics AX)</span></span>    |
| <span data-ttu-id="06a59-1011">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-1011">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-1012">总帐</span><span class="sxs-lookup"><span data-stu-id="06a59-1012">General ledger</span></span>   |
| <span data-ttu-id="06a59-1013">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-1013">**Status**</span></span>                         | <span data-ttu-id="06a59-1014">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-1014">Removed as of Dynamics AX 7.0.</span></span>   |

### <a name="infopart-and-formpart-metadata"></a><span data-ttu-id="06a59-1015">InfoPart 和 FormPart 元数据</span><span class="sxs-lookup"><span data-stu-id="06a59-1015">InfoPart and FormPart metadata</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-1016">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-1016">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-1017">InfoPart 和 FormPart 元数据支持为两个不同的客户端创建 FactBox。</span><span class="sxs-lookup"><span data-stu-id="06a59-1017">InfoPart and FormPart metadata enabled the creation of FactBoxes for two different clients.</span></span> |
| <span data-ttu-id="06a59-1018">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-1018">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-1019">InfoPart 元数据，是一种简化的窗体定义，由升级工具转换为窗体。</span><span class="sxs-lookup"><span data-stu-id="06a59-1019">InfoPart metadata, which was a simplified form definition, is converted into a Form by upgrade tooling.</span></span> <span data-ttu-id="06a59-1020">引用窗体的 FormPart 元数据已被升级工具所创建的更直接引用取代。</span><span class="sxs-lookup"><span data-stu-id="06a59-1020">FormPart metadata, which referenced a Form, is replaced by a more direct reference that is created by upgrade tooling.</span></span> |
| <span data-ttu-id="06a59-1021">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-1021">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-1022">所有模块</span><span class="sxs-lookup"><span data-stu-id="06a59-1022">All modules</span></span>    |
| <span data-ttu-id="06a59-1023">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-1023">**Status**</span></span>                         | <span data-ttu-id="06a59-1024">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-1024">Removed as of Dynamics AX 7.0.</span></span>        |

### <a name="main-account-list-page"></a><span data-ttu-id="06a59-1025">主科目列表页</span><span class="sxs-lookup"><span data-stu-id="06a59-1025">Main account list page</span></span>

<span data-ttu-id="06a59-1026">法人的帐户列表和相关余额信息</span><span class="sxs-lookup"><span data-stu-id="06a59-1026">A list of accounts for the legal entity and related balance information</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-1027">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-1027">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-1028">余额信息现在在**试算余额表**列表页上按帐户和维度提供。</span><span class="sxs-lookup"><span data-stu-id="06a59-1028">Balance information is available on the **Trial balance** list page by account and dimension.</span></span>  |
| <span data-ttu-id="06a59-1029">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-1029">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-1030">**主科目**包含**主科目**列表页所包含的相同科目列表。</span><span class="sxs-lookup"><span data-stu-id="06a59-1030">**Main accounts** contains the same list of accounts that the **Main account** list page contained.</span></span> <span data-ttu-id="06a59-1031">**主科目**中的网格视图还显示一个更小的、如网格般的视图。</span><span class="sxs-lookup"><span data-stu-id="06a59-1031">The grid view in **Main accounts** also shows an even smaller, grid-like view.</span></span> |
| <span data-ttu-id="06a59-1032">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-1032">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-1033">总帐</span><span class="sxs-lookup"><span data-stu-id="06a59-1033">General ledger</span></span>      |
| <span data-ttu-id="06a59-1034">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-1034">**Status**</span></span>                         | <span data-ttu-id="06a59-1035">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-1035">Removed as of Dynamics AX 7.0.</span></span>    |

### <a name="malaysia-and-singapore-bank-cash-flow-report"></a><span data-ttu-id="06a59-1036">马来西亚和新加坡银行现金流量报表</span><span class="sxs-lookup"><span data-stu-id="06a59-1036">Malaysia and Singapore bank cash flow report</span></span>

<span data-ttu-id="06a59-1037">此功能能让用户打印现金流量报表，以显示特定日期范围或所选银行帐户的现金流入量和流出量的交易记录和详细信息。</span><span class="sxs-lookup"><span data-stu-id="06a59-1037">This feature let the user print a cash flow report that shows transactions and details of the cash inflows and outflows for a specific date range for selected bank accounts.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-1038">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-1038">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-1039">同样的信息可以从查询银行交易记录中获得。</span><span class="sxs-lookup"><span data-stu-id="06a59-1039">The same information can be obtained from the Inquiry bank transaction.</span></span> |
| <span data-ttu-id="06a59-1040">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-1040">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-1041">查询银行交易记录</span><span class="sxs-lookup"><span data-stu-id="06a59-1041">The Inquiry bank transaction</span></span>                                            |
| <span data-ttu-id="06a59-1042">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-1042">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-1043">现金和银行管理</span><span class="sxs-lookup"><span data-stu-id="06a59-1043">Cash and bank management</span></span>                                                |
| <span data-ttu-id="06a59-1044">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-1044">**Status**</span></span>                         | <span data-ttu-id="06a59-1045">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-1045">Deprecated: A removal date has not been set for this feature.</span></span>          |

### <a name="mexican-cfd-electronic-invoice"></a><span data-ttu-id="06a59-1046">墨西哥 CFD 电子发票</span><span class="sxs-lookup"><span data-stu-id="06a59-1046">Mexican CFD electronic invoice</span></span>

<span data-ttu-id="06a59-1047">此功能支持通过使用 Comprobante Fiscal Digital (CFD) 方法生成墨西哥电子发票，在该方法中公司通过请求来自政府的相关主管机构签署发票。</span><span class="sxs-lookup"><span data-stu-id="06a59-1047">This feature enabled the generation of Mexican electronic invoices by using the Comprobante Fiscal Digital (CFD) method, where the company signs the invoice by requesting the related authorization from the government.</span></span> <span data-ttu-id="06a59-1048">此功能还提供一个每月报表，其包括在该期间签发的所有电子发票。</span><span class="sxs-lookup"><span data-stu-id="06a59-1048">This feature also provides a monthly report that includes all electronics invoices that were issued in the period.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-1049">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-1049">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-1050">此方法不再适用。</span><span class="sxs-lookup"><span data-stu-id="06a59-1050">The method is no longer applicable.</span></span> <span data-ttu-id="06a59-1051">通过使用 CFD 方法生成电子发票已被税务主管机构废弃，并已被 Comprobante Fiscal Digital a través de Internet (CFDI) 方法取代，在该方法中签名委托给第三方提供商 (PAC)。</span><span class="sxs-lookup"><span data-stu-id="06a59-1051">The generation of electronic invoices by using the CFD method was deprecated by the tax authorities and replaced by the Comprobante Fiscal Digital a través de Internet (CFDI) method, where the signing is delegated to the third-party provider (PAC).</span></span> <span data-ttu-id="06a59-1052">删除了每月报表，并且，查询选项能让用户查询历史交易记录。</span><span class="sxs-lookup"><span data-stu-id="06a59-1052">The monthly report has been removed, and an inquiry option lets users inquire about historical transactions.</span></span> |
| <span data-ttu-id="06a59-1053">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-1053">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-1054">无</span><span class="sxs-lookup"><span data-stu-id="06a59-1054">No</span></span>    |
| <span data-ttu-id="06a59-1055">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-1055">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-1056">应收账款、项目</span><span class="sxs-lookup"><span data-stu-id="06a59-1056">Account receivables, Project</span></span>   |
| <span data-ttu-id="06a59-1057">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-1057">**Status**</span></span>                         | <span data-ttu-id="06a59-1058">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-1058">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="mexico-realized-and-unrealized-vat"></a><span data-ttu-id="06a59-1059">墨西哥实现和未实现的增值税</span><span class="sxs-lookup"><span data-stu-id="06a59-1059">Mexico realized and unrealized VAT</span></span>

<span data-ttu-id="06a59-1060">Microsoft Dynamics AX 2012 通过使用“未实现的增值税”的墨西哥特定功能管理未实现的增值税 (VAT)。</span><span class="sxs-lookup"><span data-stu-id="06a59-1060">Microsoft Dynamics AX 2012 managed unrealized value-added tax (VAT) by using Mexico-specific functionality for unrealized tax.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-1061">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-1061">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-1062">重复的功能</span><span class="sxs-lookup"><span data-stu-id="06a59-1062">Duplicate functionality</span></span>  |
| <span data-ttu-id="06a59-1063">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-1063">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-1064">是，此功能已被使用核心提供的标准特定销售增值税功能取代。</span><span class="sxs-lookup"><span data-stu-id="06a59-1064">Yes, this functionality has been replaced by standard conditional sales tax functionality that is provided by Core.</span></span> |
| <span data-ttu-id="06a59-1065">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-1065">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-1066">税金</span><span class="sxs-lookup"><span data-stu-id="06a59-1066">Tax</span></span>   |
| <span data-ttu-id="06a59-1067">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-1067">**Status**</span></span>                         | <span data-ttu-id="06a59-1068">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="06a59-1068">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="microsoft-outlook-integration"></a><span data-ttu-id="06a59-1069">Microsoft Outlook 集成</span><span class="sxs-lookup"><span data-stu-id="06a59-1069">Microsoft Outlook integration</span></span>


|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-1070">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-1070">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-1071">此功能已由 Microsoft Exchange Server 集成替换。</span><span class="sxs-lookup"><span data-stu-id="06a59-1071">This functionality has been replaced by Microsoft Exchange Server integration.</span></span> |
| <span data-ttu-id="06a59-1072">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-1072">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-1073">是</span><span class="sxs-lookup"><span data-stu-id="06a59-1073">Yes</span></span>                                                                            |
| <span data-ttu-id="06a59-1074">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-1074">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-1075">销售和市场营销</span><span class="sxs-lookup"><span data-stu-id="06a59-1075">Sales and marketing</span></span>                                                            |
| <span data-ttu-id="06a59-1076">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-1076">**Status**</span></span>                         | <span data-ttu-id="06a59-1077">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-1077">Removed as of Dynamics AX 7.0.</span></span>                                                 |

### <a name="private-blocking-of-inventory-and-warehouse-management-journals"></a><span data-ttu-id="06a59-1078">库存和仓库管理日记帐的专用锁定</span><span class="sxs-lookup"><span data-stu-id="06a59-1078">Private blocking of inventory and warehouse management journals</span></span>

<span data-ttu-id="06a59-1079">库存和仓库日记帐不再支持针对所选用户将日记帐标记为专用的功能。</span><span class="sxs-lookup"><span data-stu-id="06a59-1079">The inventory and warehouse journals no longer support the ability to mark a journal as private for a selected user.</span></span> <span data-ttu-id="06a59-1080">仅支持针对用户组将日记帐锁定为专用和在编辑期间锁定的流程。</span><span class="sxs-lookup"><span data-stu-id="06a59-1080">Only the process of blocking journals as private for user groups and blocking during editing is supported.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-1081">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-1081">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-1082">找不到该功能的使用。</span><span class="sxs-lookup"><span data-stu-id="06a59-1082">No use of the functionality was found.</span></span> |
| <span data-ttu-id="06a59-1083">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-1083">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-1084">无</span><span class="sxs-lookup"><span data-stu-id="06a59-1084">No</span></span>                                     |
| <span data-ttu-id="06a59-1085">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-1085">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-1086">库存管理</span><span class="sxs-lookup"><span data-stu-id="06a59-1086">Inventory management</span></span>                   |
| <span data-ttu-id="06a59-1087">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-1087">**Status**</span></span>                         | <span data-ttu-id="06a59-1088">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-1088">Removed as of Dynamics AX 7.0.</span></span>         |

### <a name="product-builder"></a><span data-ttu-id="06a59-1089">产品生成器</span><span class="sxs-lookup"><span data-stu-id="06a59-1089">Product builder</span></span>

<span data-ttu-id="06a59-1090">产品生成器用于从销售订单、采购订单、生产订单、销售报价单、项目报价单或物料需求动态配置物料。</span><span class="sxs-lookup"><span data-stu-id="06a59-1090">Product builder was used to dynamically configure items from a sales order, purchase order, production order, sales quotation, project quotation, or item requirement.</span></span> <span data-ttu-id="06a59-1091">基于具有建模变量的产品模型，用户可以选择值以满足用户需求并获取具有物料清单和工艺路线的唯一产品变型。</span><span class="sxs-lookup"><span data-stu-id="06a59-1091">Based on a product model that had modeling variables, the user could select values to meet the customer requirements and get a unique product variant that had a BOM and route.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-1092">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-1092">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-1093">产品生成器向最终用户显示了 X++ 代码，在 Dynamics AX 的当前版本中不受支持。</span><span class="sxs-lookup"><span data-stu-id="06a59-1093">Product builder exposed X++ code to end users and isn't supported in the current version of Dynamics AX.</span></span> <span data-ttu-id="06a59-1094">它已被删除，从而避免在重叠的、庞大的代码库中进行重复的维护工作。</span><span class="sxs-lookup"><span data-stu-id="06a59-1094">It has been removed to avoid duplicate maintenance efforts on overlapping, sizeable codebases.</span></span>  |
| <span data-ttu-id="06a59-1095">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-1095">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-1096">是。</span><span class="sxs-lookup"><span data-stu-id="06a59-1096">Yes.</span></span> <span data-ttu-id="06a59-1097">已经公布在将来的版本中弃用产品生成器的 Dynamics AX 2012 中引入了基于约束的配置。</span><span class="sxs-lookup"><span data-stu-id="06a59-1097">The constraint-based configuration was introduced in Dynamics AX 2012 where the depreciation of Product builder in future versions was already announced.</span></span> <span data-ttu-id="06a59-1098">在基础产品上选择基于约束的配置技术，以启用配置。</span><span class="sxs-lookup"><span data-stu-id="06a59-1098">The constraint-based configuration technology is selected on the product masters to enable the configuration.</span></span> <span data-ttu-id="06a59-1099">若要了解更多信息，请参阅[生成产品配置模型](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/pim/build-product-configuration-model)。</span><span class="sxs-lookup"><span data-stu-id="06a59-1099">To learn more, see [Build a product configuration model](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/pim/build-product-configuration-model).</span></span> |
| <span data-ttu-id="06a59-1100">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-1100">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-1101">产品信息管理、销售和市场营销</span><span class="sxs-lookup"><span data-stu-id="06a59-1101">Product information management, Sales and marketing</span></span>  |
| <span data-ttu-id="06a59-1102">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-1102">**Status**</span></span>                         | <span data-ttu-id="06a59-1103">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-1103">Removed as of Dynamics AX 7.0.</span></span>      |

### <a name="rename-product-dimension"></a><span data-ttu-id="06a59-1104">重命名产品维度</span><span class="sxs-lookup"><span data-stu-id="06a59-1104">Rename product dimension</span></span>

<span data-ttu-id="06a59-1105">此功能能让您将三个标准维度（大小、颜色或样式）之一的名称更改为一个更好地满足您的业务需求的名称。</span><span class="sxs-lookup"><span data-stu-id="06a59-1105">This feature let you change the name of one of the three standard product dimensions (size, color, or style) to a name that better suited your business requirements.</span></span> <span data-ttu-id="06a59-1106">重命名包括其中使用了产品维度名称的所有标签。</span><span class="sxs-lookup"><span data-stu-id="06a59-1106">Renaming included all the labels where the product dimension name was used.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-1107">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-1107">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-1108">Dynamics AX 的当前版本在运行时不支持标签。</span><span class="sxs-lookup"><span data-stu-id="06a59-1108">The current version of Dynamics AX doesn't support label changes at run time.</span></span> |
| <span data-ttu-id="06a59-1109">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-1109">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-1110">无</span><span class="sxs-lookup"><span data-stu-id="06a59-1110">No</span></span>                                                                            |
| <span data-ttu-id="06a59-1111">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-1111">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-1112">产品信息管理</span><span class="sxs-lookup"><span data-stu-id="06a59-1112">Product information management</span></span>                                                |
| <span data-ttu-id="06a59-1113">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-1113">**Status**</span></span>                         | <span data-ttu-id="06a59-1114">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-1114">Removed as of Dynamics AX 7.0.</span></span>                                                |

### <a name="retail-server-connectivity-using-http"></a><span data-ttu-id="06a59-1115">使用 HTTP 的零售服务器连接</span><span class="sxs-lookup"><span data-stu-id="06a59-1115">Retail Server connectivity using HTTP</span></span>

<span data-ttu-id="06a59-1116">在 Dynamics AX 2012 R3 中，零售服务器可以使用 HTTP 通信（不受安全保护）运行。</span><span class="sxs-lookup"><span data-stu-id="06a59-1116">In Dynamics AX 2012 R3, the Retail Server could function using HTTP communication (non-secured).</span></span> <span data-ttu-id="06a59-1117">这是除使用 HTTPS 的标准通信之外的方法。</span><span class="sxs-lookup"><span data-stu-id="06a59-1117">This was in addition to the standard communication using HTTPS.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-1118">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-1118">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-1119">因为新的安全要求，现在只支持使用 TLS 1.2（或更高版本，如果可用）的安全通信。</span><span class="sxs-lookup"><span data-stu-id="06a59-1119">Due to new security requirements, only secured communication using TLS 1.2 (or above, as available) is now supported.</span></span> <span data-ttu-id="06a59-1120">自助服务安装程序将自动配置此通信的计算机。</span><span class="sxs-lookup"><span data-stu-id="06a59-1120">The self-service installer will automatically configure the computer for this communication.</span></span> |
| <span data-ttu-id="06a59-1121">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-1121">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-1122">编号</span><span class="sxs-lookup"><span data-stu-id="06a59-1122">No.</span></span> <span data-ttu-id="06a59-1123">现在只支持标准 HTTPS 通信。</span><span class="sxs-lookup"><span data-stu-id="06a59-1123">Only standard HTTPS communication is now supported.</span></span> |
| <span data-ttu-id="06a59-1124">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-1124">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-1125">零售服务器</span><span class="sxs-lookup"><span data-stu-id="06a59-1125">Retail Server</span></span>  |
| <span data-ttu-id="06a59-1126">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-1126">**Status**</span></span>                         | <span data-ttu-id="06a59-1127">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-1127">Removed as of Dynamics AX 7.0.</span></span> |

### <a name="role-center-pages"></a><span data-ttu-id="06a59-1128">角色中心页</span><span class="sxs-lookup"><span data-stu-id="06a59-1128">Role Center pages</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-1129">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-1129">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-1130">角色中心页基于已废弃的企业门户平台而构建，该平台已被 Dynamics AX 的当前版本中的新 Web 客户端平台取代。</span><span class="sxs-lookup"><span data-stu-id="06a59-1130">Role Center pages were built on the deprecated Enterprise Portal platform, which has been replaced by the new web client platform in the current version of Dynamics AX.</span></span> |
| <span data-ttu-id="06a59-1131">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-1131">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-1132">新工作区窗体模式为用户提供一个以流程为中心的设计，从而便于访问该流程中的常用任务。</span><span class="sxs-lookup"><span data-stu-id="06a59-1132">The new Workspace form pattern provides users with a process-centered design that provides easy access to commonly used tasks within that process.</span></span>                       |
| <span data-ttu-id="06a59-1133">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-1133">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-1134">所有模块</span><span class="sxs-lookup"><span data-stu-id="06a59-1134">All modules</span></span>    |
| <span data-ttu-id="06a59-1135">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-1135">**Status**</span></span>                         | <span data-ttu-id="06a59-1136">从 Dynamics AX 7.0 开始移除</span><span class="sxs-lookup"><span data-stu-id="06a59-1136">Removed as of Dynamics AX 7.0</span></span>   |

### <a name="sales-tax-jurisdictions"></a><span data-ttu-id="06a59-1137">销售税区域</span><span class="sxs-lookup"><span data-stu-id="06a59-1137">Sales tax jurisdictions</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-1138">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-1138">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-1139">低客户使用率和有限功能集</span><span class="sxs-lookup"><span data-stu-id="06a59-1139">Low customer usage and a limited feature set</span></span> |
| <span data-ttu-id="06a59-1140">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-1140">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-1141">无</span><span class="sxs-lookup"><span data-stu-id="06a59-1141">No</span></span>                                           |
| <span data-ttu-id="06a59-1142">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-1142">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-1143">美国销售税</span><span class="sxs-lookup"><span data-stu-id="06a59-1143">US sales tax</span></span>                                 |
| <span data-ttu-id="06a59-1144">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-1144">**Status**</span></span>                         | <span data-ttu-id="06a59-1145">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-1145">Removed as of Dynamics AX 7.0.</span></span>               |

### <a name="sites-services"></a><span data-ttu-id="06a59-1146">站点服务</span><span class="sxs-lookup"><span data-stu-id="06a59-1146">Sites Services</span></span>

<span data-ttu-id="06a59-1147">站点服务允许您构建将您的业务流程扩展到 Internet 的网站，而无需 IT 支持。</span><span class="sxs-lookup"><span data-stu-id="06a59-1147">Sites Services let you build websites that extend your business processes to the Internet without IT support.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-1148">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-1148">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-1149">Dynamics AX 的 Microsoft Azure 基础结构具有可以使用的新功能（例如，Azure 站点）。</span><span class="sxs-lookup"><span data-stu-id="06a59-1149">The Microsoft Azure infrastructure that is used by Dynamics AX has new capabilities that can be used instead (for example, Azure sites).</span></span> |
| <span data-ttu-id="06a59-1150">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-1150">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-1151">无</span><span class="sxs-lookup"><span data-stu-id="06a59-1151">No</span></span>   |
| <span data-ttu-id="06a59-1152">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-1152">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-1153">人力资源招聘、案例管理、询价、供应商注册、机会和市场活动协作工作区</span><span class="sxs-lookup"><span data-stu-id="06a59-1153">HR recruiting, Case management, Request for quotes, Vendor registration, Collaborative workspaces for opportunities and campaigns</span></span>  |
| <span data-ttu-id="06a59-1154">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-1154">**Status**</span></span>                         | <span data-ttu-id="06a59-1155">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-1155">Removed as of Dynamics AX 7.0.</span></span>    |

### <a name="ssas-demand-forecasting-strategy"></a><span data-ttu-id="06a59-1156">SSAS 需求预测策略</span><span class="sxs-lookup"><span data-stu-id="06a59-1156">SSAS demand forecasting strategy</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-1157">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-1157">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-1158">新的云体系结构中不支持设计此功能。</span><span class="sxs-lookup"><span data-stu-id="06a59-1158">The design of the feature cannot be supported in the new cloud architecture.</span></span> |
| <span data-ttu-id="06a59-1159">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-1159">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-1160">Azure 机器学习需求预测策略</span><span class="sxs-lookup"><span data-stu-id="06a59-1160">Azure Machine Learning demand forecasting strategy</span></span>                           |
| <span data-ttu-id="06a59-1161">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-1161">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-1162">主计划</span><span class="sxs-lookup"><span data-stu-id="06a59-1162">Master planning</span></span>                                                              |
| <span data-ttu-id="06a59-1163">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-1163">**Status**</span></span>                         | <span data-ttu-id="06a59-1164">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-1164">Removed as of Dynamics AX 7.0.</span></span>                                               |

### <a name="vendor-invoice-pool-excluding-posting-details"></a><span data-ttu-id="06a59-1165">供应商发票池(不包括过帐)详细信息</span><span class="sxs-lookup"><span data-stu-id="06a59-1165">Vendor invoice pool excluding posting details</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-1166">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-1166">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-1167">低使用率。</span><span class="sxs-lookup"><span data-stu-id="06a59-1167">Low usage.</span></span> <span data-ttu-id="06a59-1168">此功能已被具有工作流功能的发票日记帐取代。</span><span class="sxs-lookup"><span data-stu-id="06a59-1168">This functionality has been replaced by the Invoice journal that has workflow functionality.</span></span> |
| <span data-ttu-id="06a59-1169">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-1169">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-1170">发票日记帐的工作流功能。</span><span class="sxs-lookup"><span data-stu-id="06a59-1170">Workflow capabilities of the Invoice journal.</span></span>     |
| <span data-ttu-id="06a59-1171">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-1171">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-1172">应付帐款</span><span class="sxs-lookup"><span data-stu-id="06a59-1172">Accounts payable</span></span> |
| <span data-ttu-id="06a59-1173">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-1173">**Status**</span></span>                         | <span data-ttu-id="06a59-1174">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-1174">Removed as of Dynamics AX 7.0.</span></span>    |


### <a name="virtual-company-accounts"></a><span data-ttu-id="06a59-1175">虚拟公司帐户</span><span class="sxs-lookup"><span data-stu-id="06a59-1175">Virtual company accounts</span></span>

<span data-ttu-id="06a59-1176">Dynamics AX 中不再支持虚拟公司功能。</span><span class="sxs-lookup"><span data-stu-id="06a59-1176">The virtual companies feature is no longer supported in Dynamics AX.</span></span> <span data-ttu-id="06a59-1177">虚拟公司功能允许用户设置可以由一组公司共享的表。</span><span class="sxs-lookup"><span data-stu-id="06a59-1177">The virtual companies feature let users set up tables that could be shared by a set of companies.</span></span> <span data-ttu-id="06a59-1178">有关该功能的描述，请参阅[公司帐户和虚拟公司帐户](https://msdn.microsoft.com/en-us/library/aa834382(v=ax.10).aspx)。</span><span class="sxs-lookup"><span data-stu-id="06a59-1178">For a description of the feature, see [Company accounts and Virtual company accounts](https://msdn.microsoft.com/en-us/library/aa834382(v=ax.10).aspx).</span></span> <span data-ttu-id="06a59-1179">该功能的工作原理是将表分组到集合，然后集合分配给虚拟公司，即现有的“实际”公司的组。</span><span class="sxs-lookup"><span data-stu-id="06a59-1179">The feature works by grouping tables into collections that are assigned to virtual companies, which are groups of existing “real” companies.</span></span> <span data-ttu-id="06a59-1180">创建查询，以便虚拟公司中的所有公司可以访问关联表集合的表中的数据。</span><span class="sxs-lookup"><span data-stu-id="06a59-1180">Queries are created so that all the companies in the virtual company can access the data in the tables of the associated table collections.</span></span>

|   |  | 
|------------|--------------------|
| <span data-ttu-id="06a59-1181">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-1181">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-1182">- 将数据存储在表中之前，必须先设置虚拟公司。</span><span class="sxs-lookup"><span data-stu-id="06a59-1182">- Virtual companies must be set up before data is stored in the tables.</span></span> <span data-ttu-id="06a59-1183">将虚拟公司更新到现有实施上是很困难的。</span><span class="sxs-lookup"><span data-stu-id="06a59-1183">Retrofitting virtual companies onto an existing implementation is very difficult.</span></span><br><br><span data-ttu-id="06a59-1184">- 由于 Dynamics AX 的当前版本中有如此多数据标准化，要了解将什么添加到表集合将会很困难。</span><span class="sxs-lookup"><span data-stu-id="06a59-1184">- Because there has been so much data normalization in the current version of Dynamics AX, it has become difficult to know what to add to the table collections.</span></span> <span data-ttu-id="06a59-1185">例如，要知道共享哪些表很难。</span><span class="sxs-lookup"><span data-stu-id="06a59-1185">For example, it's difficult to know which tables to share.</span></span> <span data-ttu-id="06a59-1186">还必须添加从虚拟公司中的表引用的所有表。</span><span class="sxs-lookup"><span data-stu-id="06a59-1186">All the tables referenced from tables that are in a virtual company must also added.</span></span> <span data-ttu-id="06a59-1187">由于表标准化，即使遍布许多表中的简单主数据也必须是虚拟公司的一部分。</span><span class="sxs-lookup"><span data-stu-id="06a59-1187">Because of table normalization, even simple master data that is spread across multiple tables must be part of the virtual company.</span></span> <span data-ttu-id="06a59-1188">此处所犯的任何错误都将导致功能问题。</span><span class="sxs-lookup"><span data-stu-id="06a59-1188">Any mistake that is made here will cause functional issues.</span></span><br><br><span data-ttu-id="06a59-1189">- 当表是虚拟公司的一部分时，它会丢失有关数据来源的信息，并且只记录虚拟公司。</span><span class="sxs-lookup"><span data-stu-id="06a59-1189">- When a table is part of a virtual company, it loses information about the origin of the data, and only the virtual company is recorded.</span></span>   |
| <span data-ttu-id="06a59-1190">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-1190">**Replaced by another feature?**</span></span> | <span data-ttu-id="06a59-1191">全局表可用于使表可从所有公司访问到。</span><span class="sxs-lookup"><span data-stu-id="06a59-1191">Global tables can be used to make tables accessible from all companies.</span></span> <span data-ttu-id="06a59-1192">当前不替换。</span><span class="sxs-lookup"><span data-stu-id="06a59-1192">Currently, there is no replacement.</span></span> |   
| <span data-ttu-id="06a59-1193">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-1193">**Product areas affected**</span></span>       | <span data-ttu-id="06a59-1194">所有模块</span><span class="sxs-lookup"><span data-stu-id="06a59-1194">All modules</span></span> |   
| <span data-ttu-id="06a59-1195">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-1195">**Status**</span></span>                       | <span data-ttu-id="06a59-1196">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-1196">Removed as of Dynamics AX 7.0.</span></span>   |   

### <a name="windows-8-tablet-app"></a><span data-ttu-id="06a59-1197">Windows 8 平板电脑应用</span><span class="sxs-lookup"><span data-stu-id="06a59-1197">Windows 8 tablet app</span></span>

<span data-ttu-id="06a59-1198">Windows 8 平板电脑应用提供用于费用录入和审核的功能。</span><span class="sxs-lookup"><span data-stu-id="06a59-1198">The Windows 8 tablet app provided functionality for expense entry and approval.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-1199">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-1199">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-1200">Finance and Operations 与平板电脑兼容。</span><span class="sxs-lookup"><span data-stu-id="06a59-1200">Finance and Operations is compatible with tablets.</span></span> <span data-ttu-id="06a59-1201">无需再使用平板电脑应用。</span><span class="sxs-lookup"><span data-stu-id="06a59-1201">The tablet app is no longer required.</span></span>    |
| <span data-ttu-id="06a59-1202">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-1202">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-1203">编号</span><span class="sxs-lookup"><span data-stu-id="06a59-1203">No.</span></span>          |
| <span data-ttu-id="06a59-1204">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-1204">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-1205">费用报销管理</span><span class="sxs-lookup"><span data-stu-id="06a59-1205">Expense management</span></span>   |
| <span data-ttu-id="06a59-1206">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-1206">**Status**</span></span>                         | <span data-ttu-id="06a59-1207">已移除：此功能仅对 Dynamics AX 2012 R3 可用。</span><span class="sxs-lookup"><span data-stu-id="06a59-1207">Removed: This functionality is only available for Dynamics AX 2012 R3.</span></span> |

### <a name="workplanner"></a><span data-ttu-id="06a59-1208">工作进度表</span><span class="sxs-lookup"><span data-stu-id="06a59-1208">Workplanner</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="06a59-1209">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="06a59-1209">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a59-1210">低使用率</span><span class="sxs-lookup"><span data-stu-id="06a59-1210">Low usage</span></span> |
| <span data-ttu-id="06a59-1211">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="06a59-1211">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a59-1212">否，但从**模板组**页打开的**模板关系**页支持与弃用的**工作进度表**页相同的业务方案。</span><span class="sxs-lookup"><span data-stu-id="06a59-1212">No, but the **Profile relation** page, which is opened from the **Profile groups** page, supports the same business scenario as the deprecated **Workplanner** page.</span></span> |
| <span data-ttu-id="06a59-1213">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="06a59-1213">**Product areas affected**</span></span>         | <span data-ttu-id="06a59-1214">考勤管理</span><span class="sxs-lookup"><span data-stu-id="06a59-1214">Time and attendance</span></span>     |
| <span data-ttu-id="06a59-1215">**状态**</span><span class="sxs-lookup"><span data-stu-id="06a59-1215">**Status**</span></span>                         | <span data-ttu-id="06a59-1216">此代码尚未移除。</span><span class="sxs-lookup"><span data-stu-id="06a59-1216">The code has not been removed.</span></span> <span data-ttu-id="06a59-1217">但窗体 JmgWorkPlanner 未迁移。</span><span class="sxs-lookup"><span data-stu-id="06a59-1217">However, the form, JmgWorkPlanner, was not migrated.</span></span>    |

### <a name="x-financial-statements"></a><span data-ttu-id="06a59-1218">X++ 财务报表</span><span class="sxs-lookup"><span data-stu-id="06a59-1218">X++ financial statements</span></span>

|                                                 |                                                                                                          |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06a59-1219"><strong>弃用/移除的原因</strong></span><span class="sxs-lookup"><span data-stu-id="06a59-1219"><strong>Reason for deprecation/removal</strong></span></span> |                         <span data-ttu-id="06a59-1220">此功能已被另一个功能取代。</span><span class="sxs-lookup"><span data-stu-id="06a59-1220">This functionality has been replaced by another feature.</span></span>                         |
|  <span data-ttu-id="06a59-1221"><strong>被另一个功能取代？</strong></span><span class="sxs-lookup"><span data-stu-id="06a59-1221"><strong>Replaced by another feature?</strong></span></span>  | <span data-ttu-id="06a59-1222">Management Reporter（在 Dynamics AX 的当前版本中标记为<strong>财务报告</strong>。）</span><span class="sxs-lookup"><span data-stu-id="06a59-1222">Management Reporter (labeled <strong>Financial reporting</strong> in the current version of Dynamics AX)</span></span> |
|     <span data-ttu-id="06a59-1223"><strong>影响的产品区域</strong></span><span class="sxs-lookup"><span data-stu-id="06a59-1223"><strong>Product areas affected</strong></span></span>     |                                              <span data-ttu-id="06a59-1224">总帐</span><span class="sxs-lookup"><span data-stu-id="06a59-1224">General ledger</span></span>                                              |
|             <span data-ttu-id="06a59-1225"><strong>状态</strong></span><span class="sxs-lookup"><span data-stu-id="06a59-1225"><strong>Status</strong></span></span>             |                                      <span data-ttu-id="06a59-1226">从 Dynamics AX 2012 开始移除</span><span class="sxs-lookup"><span data-stu-id="06a59-1226">Removed as of Dynamics AX 2012</span></span>                                      |



---
title: "已删除或弃用的功能"
description: "本主题介绍已经删除或计划删除的功能。"
author: sericks007
manager: AnnBe
ms.date: 12/10/2018
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
ms.sourcegitcommit: 88b28ad1ff4142d04288b3d8807e61bb38a642be
ms.openlocfilehash: 8f4413573f2e269e5a523940fbb841358e178d10
ms.contentlocale: zh-cn
ms.lasthandoff: 12/13/2018

---

# <a name="removed-or-deprecated-features"></a><span data-ttu-id="cf8f7-103">已移除或弃用的功能</span><span class="sxs-lookup"><span data-stu-id="cf8f7-103">Removed or deprecated features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cf8f7-104">本主题介绍已从 Dynamics 365 for Finance and Operations 移除或弃用的功能。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-104">This topic describes features that have been removed or deprecated for Dynamics 365 for Finance and Operations.</span></span>

- <span data-ttu-id="cf8f7-105">*已移除*的功能在产品中不再可用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="cf8f7-106">*已弃用*的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="cf8f7-107">此列表旨在帮助您在您自己的计划中考虑这些功能的移除和弃用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!Note]
> <span data-ttu-id="cf8f7-108">从具有平台更新 8 的 Dynamics 365 for Finance and Operations 2017 年 7 月版开始，每一个已移除或弃用的功能均备注了部署类型。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-108">Starting with the Dynamics 365 for Finance and Operations July 2017 release with platform update 8, the type of deployments are noted for each removed or deprecated feature.</span></span> <span data-ttu-id="cf8f7-109">本主题中提及的所有之前的版本仅支持云部署。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-109">All of the previous releases mentioned in this topic supported cloud deployments only.</span></span>

> [!Note]
> <span data-ttu-id="cf8f7-110">[技术参考报告](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep)中提供了有关 Finance and Operations 中的对象的详细信息。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-110">Detailed information about objects in Finance and Operations can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="cf8f7-111">可比较这些报告的不同版本，以了解 Finance and Operations 各版本中已更改或已删除的对象。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-111">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations.</span></span>

## <a name="dynamics-365-for-finance-and-operations-81-with-platform-update-20"></a><span data-ttu-id="cf8f7-112">具有平台更新 20 的 Dynamics 365 for Finance and Operations 8.1</span><span class="sxs-lookup"><span data-stu-id="cf8f7-112">Dynamics 365 for Finance and Operations 8.1 with platform update 20</span></span>

### <a name="batch-transfer-rules-for-subledger-journal-account-entries"></a><span data-ttu-id="cf8f7-113">子分类日记帐科目分录的批处理转移规则</span><span class="sxs-lookup"><span data-stu-id="cf8f7-113">Batch transfer rules for subledger journal account entries</span></span>
<span data-ttu-id="cf8f7-114">总帐参数中已弃用了同步转移模式。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-114">The Synchronous transfer mode is being deprecated in the General ledger parameters.</span></span>  <span data-ttu-id="cf8f7-115">此模式刚被异步和计划批处理，后者表示为转移选项。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-115">This mode is replaced by Asynchronous and scheduled batch only, which already exist as options for transfer.</span></span> 

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-116">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-116">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-117">因为对系统存在影响，我们将移除同步选项。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-117">We are removing the synchronous option due to performance impact to the system.</span></span> |
| <span data-ttu-id="cf8f7-118">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-118">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-119">异步和计划批处理选项取代了同步。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-119">Asynchronous and scheduled batch are options to use in place of Synchronous.</span></span>   |
| <span data-ttu-id="cf8f7-120">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-120">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-121">总帐、应付帐款、应收帐款、采购、支出</span><span class="sxs-lookup"><span data-stu-id="cf8f7-121">General Ledger, Accounts payable, Accounts Receivable, Procurement, Expense</span></span>    |
| <span data-ttu-id="cf8f7-122">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-122">**Deployment option**</span></span>              | <span data-ttu-id="cf8f7-123">所有</span><span class="sxs-lookup"><span data-stu-id="cf8f7-123">All</span></span>  |
| <span data-ttu-id="cf8f7-124">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-124">**Status**</span></span>                         | <span data-ttu-id="cf8f7-125">已弃用 - 移除功能的目标时间范围为 10.0 版本。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-125">Deprecated - Target timeframe for the functionality to be removed is the 10.0 version.</span></span>|

### <a name="electronic-reporting-for-russia"></a><span data-ttu-id="cf8f7-126">俄罗斯的电子报告格式</span><span class="sxs-lookup"><span data-stu-id="cf8f7-126">Electronic reporting for Russia</span></span>
<span data-ttu-id="cf8f7-127">用于配置申报的 .txt 和 .xml 文件格式的功能。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-127">Feature for configuring .txt and .xml file formats of declarations.</span></span> 

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-128">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-128">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-129">已被电子申报取代。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-129">Replaced with Electronic reporting.</span></span> |
| <span data-ttu-id="cf8f7-130">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-130">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-131">是。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-131">Yes.</span></span> |
| <span data-ttu-id="cf8f7-132">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-132">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-133">总帐</span><span class="sxs-lookup"><span data-stu-id="cf8f7-133">General Ledger</span></span> |
| <span data-ttu-id="cf8f7-134">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-134">**Deployment option**</span></span>              | <span data-ttu-id="cf8f7-135">所有</span><span class="sxs-lookup"><span data-stu-id="cf8f7-135">All</span></span> |
| <span data-ttu-id="cf8f7-136">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-136">**Status**</span></span>                         | <span data-ttu-id="cf8f7-137">已从带平台更新 20 的 Dynamics 365 for Finance and Operations 8.1 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-137">Removed as of Dynamics 365 for Finance and Operations 8.1 with platform update 20.</span></span> |

### <a name="financial-reports-generator-for-russia"></a><span data-ttu-id="cf8f7-138">俄罗斯的财务报表生成器</span><span class="sxs-lookup"><span data-stu-id="cf8f7-138">Financial reports generator for Russia</span></span>
<span data-ttu-id="cf8f7-139">用于设置会计和纳税报表的数据收集，以及用于将数据导出到 XLS 和 DOC 报表模板的工具。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-139">A tool for setting up data collection for accounting and tax reports, and to export data to XLS and DOC report templates.</span></span> <span data-ttu-id="cf8f7-140">功能部件：已移除了将数据导出到 XLS 和 DOC 报表模板、查询和固定必备项这一功能。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-140">Functional parts: Export data to XLS and DOC report templates, queries, fixed requisites are removed.</span></span> 

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-141">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-141">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-142">移除的部件已被电子申报取代。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-142">Removed parts are replaced with Electronic reporting.</span></span> |
| <span data-ttu-id="cf8f7-143">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-143">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-144">是。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-144">Yes.</span></span> <span data-ttu-id="cf8f7-145">应使用财务报表设置用户界面按总帐科目和税务登记簿设置数据收集规则。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-145">Financial reports setup user interface should be used for setting up data collection rules by GL accounts or tax registers.</span></span> <span data-ttu-id="cf8f7-146">应在电子申报中配置将数据导出到各种文件类型、固定必备项和类似查询的数据收集规则。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-146">Export data to various file types, fixed requisites and query-like data collection rules should be configured in Electronic reporting.</span></span> |
| <span data-ttu-id="cf8f7-147">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-147">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-148">总帐。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-148">General ledger.</span></span> |
| <span data-ttu-id="cf8f7-149">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-149">**Deployment option**</span></span>              | <span data-ttu-id="cf8f7-150">所有</span><span class="sxs-lookup"><span data-stu-id="cf8f7-150">All</span></span> |
| <span data-ttu-id="cf8f7-151">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-151">**Status**</span></span>                         | <span data-ttu-id="cf8f7-152">已从带平台更新 20 的 Dynamics 365 for Finance and Operations 8.1 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-152">Removed as of Dynamics 365 for Finance and Operations 8.1 with platform update 20.</span></span> |

### <a name="integration-with-external-providers-for-sending-electronic-reporting-through-communication-channels-for-russia"></a><span data-ttu-id="cf8f7-153">俄罗斯的与外部提供商集成以通过通信通道发送电子报告</span><span class="sxs-lookup"><span data-stu-id="cf8f7-153">Integration with external providers for sending electronic reporting through communication channels for Russia</span></span>
<span data-ttu-id="cf8f7-154">用于将生成的电子版申报文件导出到文件夹以进一步发送给正式的电子申报提供商和导入回状态的功能。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-154">Feature exporting generated electronic files of declarations to folder for further sending to official providers of electronic reporting as well as importing state back.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-155">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-155">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-156">已被电子消息可配置功能取代。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-156">Replaced with electronic messages configurable feature.</span></span> |
| <span data-ttu-id="cf8f7-157">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-157">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-158">是。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-158">Yes.</span></span>  |
| <span data-ttu-id="cf8f7-159">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-159">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-160">总帐、税务</span><span class="sxs-lookup"><span data-stu-id="cf8f7-160">General Ledger, Tax</span></span> |
| <span data-ttu-id="cf8f7-161">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-161">**Deployment option**</span></span>              | <span data-ttu-id="cf8f7-162">所有</span><span class="sxs-lookup"><span data-stu-id="cf8f7-162">All</span></span> |
| <span data-ttu-id="cf8f7-163">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-163">**Status**</span></span>                         | <span data-ttu-id="cf8f7-164">已从带平台更新 20 的 Dynamics 365 for Finance and Operations 8.1 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-164">Removed as of Dynamics 365 for Finance and Operations 8.1 with platform update 20.</span></span> |


### <a name="profit-tax-register-wizard"></a><span data-ttu-id="cf8f7-165">利润税登记向导</span><span class="sxs-lookup"><span data-stu-id="cf8f7-165">Profit tax register wizard</span></span>
<span data-ttu-id="cf8f7-166">为新利润税登记创建模板的功能。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-166">Feature for creating templates for new profit tax registers.</span></span> <span data-ttu-id="cf8f7-167">此功能为新登记创建 X++ 对象，其然后被创建为添加了适当的计算逻辑的模板。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-167">This feature creates X++ objects for new registers, which are then  created as templates with the appropriate calculation logic added in.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-168">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-168">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-169">功能与 Dynamics 365 for Finance and Operations 延伸性模型不兼容。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-169">Feature is not compatible with the Dynamics 365 for Finance and Operations extensibility model.</span></span> |
| <span data-ttu-id="cf8f7-170">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-170">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-171">无</span><span class="sxs-lookup"><span data-stu-id="cf8f7-171">No</span></span> |
| <span data-ttu-id="cf8f7-172">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-172">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-173">税金</span><span class="sxs-lookup"><span data-stu-id="cf8f7-173">Tax</span></span> |
| <span data-ttu-id="cf8f7-174">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-174">**Deployment option**</span></span>              | <span data-ttu-id="cf8f7-175">所有</span><span class="sxs-lookup"><span data-stu-id="cf8f7-175">All</span></span> |
| <span data-ttu-id="cf8f7-176">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-176">**Status**</span></span>                         | <span data-ttu-id="cf8f7-177">已从带平台更新 20 的 Dynamics 365 for Finance and Operations 8.1 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-177">Removed as of Dynamics 365 for Finance and Operations 8.1 with platform update 20.</span></span> |


## <a name="dynamics-365-for-finance-and-operations-80-with-platform-update-15"></a><span data-ttu-id="cf8f7-178">具有平台更新 15 的 Dynamics 365 for Finance and Operations 8.0</span><span class="sxs-lookup"><span data-stu-id="cf8f7-178">Dynamics 365 for Finance and Operations 8.0 with platform update 15</span></span>
<span data-ttu-id="cf8f7-179">此版本中未移除或弃用任何功能。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-179">No features have been removed or deprecated with this release.</span></span> <span data-ttu-id="cf8f7-180">平台更新 15 是累积功能，其中包含平台更新 13、14 和 15 中的新增功能或更改功能。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-180">Platform update 15 is cumulative and contains new or changed features from Platform update 13, Platform update 14, and Platform update 15.</span></span>

## <a name="dynamics-365-for-finance-and-operations-enterprise-edition-73-with-platform-update-12"></a><span data-ttu-id="cf8f7-181">具有平台更新 12 的 Dynamics 365 for Finance and Operations Enterprise Edition 7.3</span><span class="sxs-lookup"><span data-stu-id="cf8f7-181">Dynamics 365 for Finance and Operations, Enterprise edition 7.3 with platform update 12</span></span>

### <a name="personalized-product-recommendations"></a><span data-ttu-id="cf8f7-182">个性化产品建议</span><span class="sxs-lookup"><span data-stu-id="cf8f7-182">Personalized product recommendations</span></span> 
<span data-ttu-id="cf8f7-183">从 2018 年 2 月 15 日开始，零售商再也不能显示有关销售点 (POS) 设备的个性化产品建议。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-183">Starting February 15, 2018, retailers will no longer be able to display personalized product recommendations on a point of sale (POS) device.</span></span> <span data-ttu-id="cf8f7-184">有关详细信息，请参见[个性化产品建议](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/personalized-product-recommendations)。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-184">For more information, see [Personalized product recommendations](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/personalized-product-recommendations).</span></span>  

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-185">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-185">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-186">我们将移除当前的产品建议服务版本，因为我们为这项功能重新设计了更出色的算法和更新的面向零售的功能。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-186">We are removing the current version of the product recommendation service as we redesign this feature with a better algorithm and newer retail-oriented capabilities.</span></span>  |
| <span data-ttu-id="cf8f7-187">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-187">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-188">编号</span><span class="sxs-lookup"><span data-stu-id="cf8f7-188">No.</span></span> <span data-ttu-id="cf8f7-189">但是，我们计划在 2018 年春季之后恢复此功能，以利用新的建议服务。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-189">However, after Spring 2018, we plan to bring back this feature to leverage a new recommendation service.</span></span>   |
| <span data-ttu-id="cf8f7-190">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-190">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-191">POS 中的个性化产品建议。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-191">Personalized product recommendations in POS.</span></span>                                                    |
| <span data-ttu-id="cf8f7-192">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-192">**Deployment option**</span></span>              | <span data-ttu-id="cf8f7-193">全部</span><span class="sxs-lookup"><span data-stu-id="cf8f7-193">All</span></span>                                                                                      |
| <span data-ttu-id="cf8f7-194">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-194">**Status**</span></span>                         |<span data-ttu-id="cf8f7-195">从 2018 年 2 月 15 日开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-195">Removed as of February 15, 2018.</span></span> <span data-ttu-id="cf8f7-196">这将影响运行 Dynamics 365 for Operations 1611 及更高版本的客户。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-196">This affects customers running Dynamics 365 for Operations 1611 and later.</span></span>  |

### <a name="extension-of-the-list-of-electronic-reporting-er-functions"></a><span data-ttu-id="cf8f7-197">电子申报 (ER) 功能列表扩展</span><span class="sxs-lookup"><span data-stu-id="cf8f7-197">Extension of the list of Electronic reporting (ER) functions</span></span>
<span data-ttu-id="cf8f7-198">可以引入在 ER 表达式生成器中使用的自定义功能（有关详细信息，请参阅[扩展电子申报功能列表](../../dev-itpro/analytics/general-electronic-reporting-formulas-list-extension.md)）的这一特性不再受支持。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-198">The possibility to introduce custom functions to be used in the ER expression builder (for more information, see [Extend the list of Electronic reporting functions](../../dev-itpro/analytics/general-electronic-reporting-formulas-list-extension.md)) is not supported any more.</span></span> <span data-ttu-id="cf8f7-199">由于 ER API 发生变更，从 ER 表达式生成器调用内置函数的 API 变成内部 API，并且无法再进行扩展。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-199">Due to changes of the ER APIs, the API to call built-in functions from the ER expression builder became internal and can’t be extended any longer.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-200">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-200">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-201">代码密封计划</span><span class="sxs-lookup"><span data-stu-id="cf8f7-201">Code sealing initiative</span></span>  |
| <span data-ttu-id="cf8f7-202">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-202">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-203">无。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-203">None.</span></span> <span data-ttu-id="cf8f7-204">每当需要一个新的内置函数时，必须向 ER 框架团队提交新扩展请求。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-204">Whenever a new built-in function is needed, a new extension request must be addressed to the ER framework team.</span></span><br><br><span data-ttu-id="cf8f7-205">在 ER 团队开发请求的函数时，作为临时解决方案，可以将需要的逻辑作为一种自定义应用程序类方法进行编程。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-205">As a temporary work around while the requested function is under development by the ER team, the required logic can be programmed as a method of a custom application class.</span></span> <span data-ttu-id="cf8f7-206">此方法可以作为引用该自定义应用程序类的**应用程序\类**类型的已添加 ER 数据源的属性在 ER 表达式中访问。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-206">This method can be accessed in an ER expression as a property of the added ER data source of the **Application\Class** type that refers to that custom application class.</span></span>  |
| <span data-ttu-id="cf8f7-207">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-207">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-208">电子申报框架</span><span class="sxs-lookup"><span data-stu-id="cf8f7-208">Electronic reporting framework</span></span>                                                      |
| <span data-ttu-id="cf8f7-209">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-209">**Deployment option**</span></span>              | <span data-ttu-id="cf8f7-210">全部</span><span class="sxs-lookup"><span data-stu-id="cf8f7-210">All</span></span>                                                                                      |
| <span data-ttu-id="cf8f7-211">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-211">**Status**</span></span>                         | <span data-ttu-id="cf8f7-212">从 Dynamics 365 for Finance and Operations Enterprise Edition 7.3 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-212">Removed as of Dynamics 365 for Finance and Operations, Enterprise edition 7.3.</span></span>    |

### <a name="inventory-by-item-group-and-inventory-by-inventory-dimension-aging-reports"></a><span data-ttu-id="cf8f7-213">按物料组的库存和按库存维度的库存帐龄分析表</span><span class="sxs-lookup"><span data-stu-id="cf8f7-213">Inventory by item group and Inventory by inventory dimension aging reports</span></span>

<span data-ttu-id="cf8f7-214">这两个分析表在 Finance and Operations 中不再受支持。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-214">These two reports are no longer supported in Finance and Operations.</span></span> <span data-ttu-id="cf8f7-215">相反，可使用**库存帐龄**分析表改善用户体验。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-215">Instead, the **Inventory aging** report can be used to improve the user experience.</span></span>

|   |  |
|--------------|-----------------------|
| <span data-ttu-id="cf8f7-216">**折旧的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-216">**Reason for deprecation**</span></span>       | <span data-ttu-id="cf8f7-217">重复的功能</span><span class="sxs-lookup"><span data-stu-id="cf8f7-217">Duplicate functionality</span></span>  |
| <span data-ttu-id="cf8f7-218">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-218">**Replaced by another feature?**</span></span> | <span data-ttu-id="cf8f7-219">是。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-219">Yes.</span></span> <span data-ttu-id="cf8f7-220">这两个分析表已替换为**库存帐龄**分析表。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-220">The two reports have been replaced by the **Inventory aging** report.</span></span>     |
| <span data-ttu-id="cf8f7-221">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-221">**Product areas affected**</span></span>       | <span data-ttu-id="cf8f7-222">库存管理、成本管理</span><span class="sxs-lookup"><span data-stu-id="cf8f7-222">Inventory management, Cost management</span></span>        |
| <span data-ttu-id="cf8f7-223">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-223">**Deployment option**</span></span>        | <span data-ttu-id="cf8f7-224">全部</span><span class="sxs-lookup"><span data-stu-id="cf8f7-224">All</span></span>|
| <span data-ttu-id="cf8f7-225">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-225">**Status**</span></span>                       | <span data-ttu-id="cf8f7-226">已弃用：两个分析表的菜单项在版本 7.3 中已移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-226">Deprecated: The menu items for the two reports have been removed in version 7.3.</span></span> <span data-ttu-id="cf8f7-227">但这些分析表的代码仍然保留在产品中。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-227">However, the code for the reports remains in the product.</span></span> <span data-ttu-id="cf8f7-228">在将来的发行中计划移除该代码。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-228">The plan is to remove the code in a future release.</span></span> |

### <a name="power-bi-content-packs-available-on-appsource"></a><span data-ttu-id="cf8f7-229">AppSource 中的 Power BI 内容包</span><span class="sxs-lookup"><span data-stu-id="cf8f7-229">Power BI content packs available on AppSource</span></span>
<span data-ttu-id="cf8f7-230">[Microsoft AppSource](https://appsource.microsoft.com) 上提供的**成本管理**、**财务绩效**和**零售渠道绩效**内容包因为 Microsoft Power BI 中的产品更新而被弃用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-230">The **Cost management**, **Financial performance**, and **Retail channel performance** content packs, available on the [Microsoft AppSource](https://appsource.microsoft.com) site, are deprecated as a consequence of product updates in Microsoft Power BI.</span></span> <span data-ttu-id="cf8f7-231">过去将这些内容包部署到 PowerBI.com 的系统管理窗体在 Finance and Operations 中也被弃用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-231">System administration forms used to deploy these content packs to PowerBI.com are also being deprecated in Finance and Operations.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-232">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-232">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-233">Microsoft Power BI 中进行产品更新。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-233">Product updates in Microsoft Power BI.</span></span> |
| <span data-ttu-id="cf8f7-234">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-234">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-235">[AppSource](https://appsource.microsoft.com) 站点上提供的**成本管理**、**财务绩效**和**零售渠道绩效**内容包将被分析应用程序替代，以便在数据库级别集成解决方案。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-235">The **Cost management**, **Financial performance**, and **Retail channel performance** content packs, available on the [AppSource](https://appsource.microsoft.com) site, are being replaced by analytical applications which allow for solution integrations at the database level.</span></span> <span data-ttu-id="cf8f7-236">有关分析应用程序的详细信息，请参阅[工作区中的嵌入式 Power BI](../../dev-itpro/analytics/embed-power-bi-workspaces.md)。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-236">For more information about analytical applications, see [Embedded Power BI in workspackes](../../dev-itpro/analytics/embed-power-bi-workspaces.md).</span></span>    |
| <span data-ttu-id="cf8f7-237">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-237">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-238">成本管理、财务和零售</span><span class="sxs-lookup"><span data-stu-id="cf8f7-238">Cost management, Finance, and Retail</span></span>                                                                                               |
| <span data-ttu-id="cf8f7-239">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-239">**Deployment option**</span></span>              | <span data-ttu-id="cf8f7-240">仅适用于云（在本地部署中不再支持与 PowerBI.com 集成）。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-240">Cloud only (Integration with PowerBI.com is not supported in on-premises deployments.)</span></span>                                                                                                            |
| <span data-ttu-id="cf8f7-241">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-241">**Status**</span></span>                         | <span data-ttu-id="cf8f7-242">已弃用：移除功能的目标时间范围为 2018 年第二季度。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-242">Deprecated: Target timeframe for the functionality removal is Q2 2018.</span></span>    |

### <a name="standard-ui-in-data-management-workspace"></a><span data-ttu-id="cf8f7-243">数据管理工作区中的标准 UI</span><span class="sxs-lookup"><span data-stu-id="cf8f7-243">Standard UI in data management workspace</span></span>

<span data-ttu-id="cf8f7-244">数据管理中的标准 UI 为旧 UI，是当用户访问数据管理工作区时呈现给用户的默认 UI。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-244">The standard UI in data management is the legacy UI, which is the default UI presented to the users when they visit the data management workspace.</span></span>

|   |  |
|------------------|-------------------------|
| <span data-ttu-id="cf8f7-245">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-245">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-246">我们正努力在新的 UI 中为用户提供新的体验。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-246">We are investing in providing new user experiences in the new UI.</span></span>             |
| <span data-ttu-id="cf8f7-247">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-247">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-248">新 UI 称为*增强型视图*，它将取代旧 UI。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-248">The new UI called *Enhanced views* is replacing the old UI.</span></span>            |
| <span data-ttu-id="cf8f7-249">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-249">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-250">数据管理工作区</span><span class="sxs-lookup"><span data-stu-id="cf8f7-250">Data management workspace</span></span>                                                     |
| <span data-ttu-id="cf8f7-251">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-251">**Deployment option**</span></span>              | <span data-ttu-id="cf8f7-252">全部</span><span class="sxs-lookup"><span data-stu-id="cf8f7-252">All</span></span>                                                                           |
| <span data-ttu-id="cf8f7-253">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-253">**Status**</span></span>                         | <span data-ttu-id="cf8f7-254">已弃用：移除功能的目标时间范围为 2018 年第二季度。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-254">Deprecated: Target timeframe for the functionality to be removed is Q2 2018.</span></span> |

### <a name="excise-sales-tax-service-tax-for-india"></a><span data-ttu-id="cf8f7-255">适用于印度的消费税、销售税、服务税</span><span class="sxs-lookup"><span data-stu-id="cf8f7-255">Excise, Sales Tax, Service Tax for India</span></span>

<span data-ttu-id="cf8f7-256">这些税项已归入印度 GST。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-256">These taxes have been subsumed into Indian GST.</span></span>

|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="cf8f7-257">**移除或弃用的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-257">**Reason for removal or deprecation**</span></span>       | <span data-ttu-id="cf8f7-258">这些税项已归入印度 GST。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-258">These taxes have been subsumed into Indian GST.</span></span>                          |
| <span data-ttu-id="cf8f7-259">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-259">**Replaced by another feature?**</span></span>            | <span data-ttu-id="cf8f7-260">印度 GST</span><span class="sxs-lookup"><span data-stu-id="cf8f7-260">Indian GST</span></span>                                                              |
| <span data-ttu-id="cf8f7-261">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-261">**Product areas affected**</span></span>                  | <span data-ttu-id="cf8f7-262">税金</span><span class="sxs-lookup"><span data-stu-id="cf8f7-262">Tax</span></span>                                                                     |
| <span data-ttu-id="cf8f7-263">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-263">**Deployment option**</span></span>                       | <span data-ttu-id="cf8f7-264">所有模块</span><span class="sxs-lookup"><span data-stu-id="cf8f7-264">All modules</span></span>                                                   |
| <span data-ttu-id="cf8f7-265">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-265">**Status**</span></span>                                  | <span data-ttu-id="cf8f7-266">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-266">Deprecated: A removal date has not been set for this feature.</span></span> |    

### <a name="file-validation-utility-fvu-for-india"></a><span data-ttu-id="cf8f7-267">印度文件验证实用工具 (FVU)</span><span class="sxs-lookup"><span data-stu-id="cf8f7-267">File Validation Utility (FVU) for India</span></span>

|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="cf8f7-268">**移除或弃用的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-268">**Reason for removal or deprecation**</span></span>       | <span data-ttu-id="cf8f7-269">缺少客户使用</span><span class="sxs-lookup"><span data-stu-id="cf8f7-269">Lack of customer usage</span></span>                                                  |
| <span data-ttu-id="cf8f7-270">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-270">**Replaced by another feature?**</span></span>            | <span data-ttu-id="cf8f7-271">无</span><span class="sxs-lookup"><span data-stu-id="cf8f7-271">No</span></span>                                                                      |
| <span data-ttu-id="cf8f7-272">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-272">**Product areas affected**</span></span>                  | <span data-ttu-id="cf8f7-273">印度预缴税金</span><span class="sxs-lookup"><span data-stu-id="cf8f7-273">Indian withholding tax</span></span>                                                  |
| <span data-ttu-id="cf8f7-274">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-274">**Deployment option**</span></span>                       | <span data-ttu-id="cf8f7-275">所有模块</span><span class="sxs-lookup"><span data-stu-id="cf8f7-275">All modules</span></span>                                                                    |
| <span data-ttu-id="cf8f7-276">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-276">**Status**</span></span>                                  | <span data-ttu-id="cf8f7-277">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-277">Deprecated: A removal date has not been set for this feature.</span></span>   |        

### <a name="tdstcs-certificate-for-india"></a><span data-ttu-id="cf8f7-278">印度 TDS/TCS 证书</span><span class="sxs-lookup"><span data-stu-id="cf8f7-278">TDS/TCS certificate for India</span></span>

<span data-ttu-id="cf8f7-279">用户可从政府门户下载。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-279">Users can download this from the government portal.</span></span>

|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="cf8f7-280">**移除或弃用的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-280">**Reason for removal or deprecation**</span></span>       | <span data-ttu-id="cf8f7-281">缺少客户使用</span><span class="sxs-lookup"><span data-stu-id="cf8f7-281">Lack of customer usage</span></span>                                                  |
| <span data-ttu-id="cf8f7-282">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-282">**Replaced by another feature?**</span></span>            | <span data-ttu-id="cf8f7-283">无</span><span class="sxs-lookup"><span data-stu-id="cf8f7-283">No</span></span>                                                                      |
| <span data-ttu-id="cf8f7-284">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-284">**Product areas affected**</span></span>                  | <span data-ttu-id="cf8f7-285">印度预缴税金</span><span class="sxs-lookup"><span data-stu-id="cf8f7-285">Indian withholding tax</span></span>                                                  |
| <span data-ttu-id="cf8f7-286">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-286">**Deployment option**</span></span>                       | <span data-ttu-id="cf8f7-287">所有模块</span><span class="sxs-lookup"><span data-stu-id="cf8f7-287">All modules</span></span>                                                                   |
| <span data-ttu-id="cf8f7-288">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-288">**Status**</span></span>                                  | <span data-ttu-id="cf8f7-289">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-289">Deprecated: A removal date has not been set for this feature.</span></span>     |    

### <a name="exportimport-exim-incentive-scheme-for-india"></a><span data-ttu-id="cf8f7-290">导出/导入 (EXIM) 印度激励方案</span><span class="sxs-lookup"><span data-stu-id="cf8f7-290">Export/import (EXIM) incentive scheme for India</span></span>


|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="cf8f7-291">**移除或弃用的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-291">**Reason for removal or deprecation**</span></span>       | <span data-ttu-id="cf8f7-292">缺少客户使用</span><span class="sxs-lookup"><span data-stu-id="cf8f7-292">Lack of customer usage</span></span>                                                  |
| <span data-ttu-id="cf8f7-293">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-293">**Replaced by another feature?**</span></span>            | <span data-ttu-id="cf8f7-294">无</span><span class="sxs-lookup"><span data-stu-id="cf8f7-294">No</span></span>                                                                      |
| <span data-ttu-id="cf8f7-295">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-295">**Product areas affected**</span></span>                  | <span data-ttu-id="cf8f7-296">导入和导出</span><span class="sxs-lookup"><span data-stu-id="cf8f7-296">Import and export</span></span>                                                       |
| <span data-ttu-id="cf8f7-297">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-297">**Deployment option**</span></span>                       | <span data-ttu-id="cf8f7-298">所有模块</span><span class="sxs-lookup"><span data-stu-id="cf8f7-298">All modules</span></span>                                                                    |
| <span data-ttu-id="cf8f7-299">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-299">**Status**</span></span>                                  | <span data-ttu-id="cf8f7-300">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-300">Deprecated: A removal date has not been set for this feature.</span></span>  |    


## <a name="dynamics-365-for-retail-72"></a><span data-ttu-id="cf8f7-301">Dynamics 365 for Retail 7.2</span><span class="sxs-lookup"><span data-stu-id="cf8f7-301">Dynamics 365 for Retail 7.2</span></span>

### <a name="personalized-product-recommendations"></a><span data-ttu-id="cf8f7-302">个性化产品建议</span><span class="sxs-lookup"><span data-stu-id="cf8f7-302">Personalized product recommendations</span></span> 
<span data-ttu-id="cf8f7-303">从 2018 年 2 月 15 日开始，零售商再也不能显示有关销售点 (POS) 设备的个性化产品建议。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-303">Starting February 15, 2018, retailers will no longer be able to display personalized product recommendations on a point of sale (POS) device.</span></span> <span data-ttu-id="cf8f7-304">有关详细信息，请参见[个性化产品建议](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/personalized-product-recommendations)。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-304">For more information, see [Personalized product recommendations](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/personalized-product-recommendations).</span></span>  

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-305">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-305">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-306">我们将移除当前的产品建议服务版本，因为我们为这项功能重新设计了更出色的算法和更新的面向零售的功能。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-306">We are removing the current version of the product recommendation service as we redesign this feature with a better algorithm and newer retail-oriented capabilities.</span></span>  |
| <span data-ttu-id="cf8f7-307">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-307">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-308">编号</span><span class="sxs-lookup"><span data-stu-id="cf8f7-308">No.</span></span> <span data-ttu-id="cf8f7-309">但是，我们计划在 2018 年春季之后恢复此功能，以利用新的建议服务。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-309">However, after Spring 2018, we plan to bring back this feature to leverage a new recommendation service.</span></span>   |
| <span data-ttu-id="cf8f7-310">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-310">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-311">POS 中的个性化产品建议。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-311">Personalized product recommendations in POS.</span></span>                                                    |
| <span data-ttu-id="cf8f7-312">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-312">**Deployment option**</span></span>              | <span data-ttu-id="cf8f7-313">全部</span><span class="sxs-lookup"><span data-stu-id="cf8f7-313">All</span></span>                                                                                      |
| <span data-ttu-id="cf8f7-314">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-314">**Status**</span></span>                         |<span data-ttu-id="cf8f7-315">从 2018 年 2 月 15 日开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-315">Removed as of February 15, 2018.</span></span> <span data-ttu-id="cf8f7-316">这将影响运行 Dynamics 365 for Retail 7.2 及更高版本的客户。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-316">This affects customers running Dynamics 365 for Retail 7.2  and later.</span></span> |


## <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-with-platform-update-8"></a><span data-ttu-id="cf8f7-317">具有平台更新 8 的 Dynamics 365 for Finance and Operations Enterprise Edition 2017 年 7 月</span><span class="sxs-lookup"><span data-stu-id="cf8f7-317">Dynamics 365 for Finance and Operations, Enterprise edition July 2017 with platform update 8</span></span>

### <a name="currency-conversion-for-accounting-and-reporting-currencies"></a><span data-ttu-id="cf8f7-318">记帐币种和申报币种的币种转换</span><span class="sxs-lookup"><span data-stu-id="cf8f7-318">Currency conversion for accounting and reporting currencies</span></span>

<span data-ttu-id="cf8f7-319">引入欧元时，也引入了记帐币种和申报币种的币种转换。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-319">Currency conversion for accounting and reporting currencies was introduced when the euro was introduced.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-320">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-320">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-321">“复制法人”功能作为替代方法的使用和添加受限。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-321">Limited usage and addition of the Copy legal entity functionality as a replacement.</span></span>      |
| <span data-ttu-id="cf8f7-322">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-322">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-323">否，但是增加了“复制法人”和“配置”功能，从而可以更轻松地迁移到核心需求不断变化的公司。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-323">No, but the Copy legal entity and Configurations features were added to make it easier to move to a company that has changing core requirements.</span></span> |
| <span data-ttu-id="cf8f7-324">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-324">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-325">财务管理</span><span class="sxs-lookup"><span data-stu-id="cf8f7-325">Financial management</span></span>     |
| <span data-ttu-id="cf8f7-326">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-326">**Status**</span></span>                         | <span data-ttu-id="cf8f7-327">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-327">Deprecated: A removal date has not been set for this feature.</span></span>   |


### <a name="warehouse-mobile-devices-portal"></a><span data-ttu-id="cf8f7-328">仓库移动设备门户</span><span class="sxs-lookup"><span data-stu-id="cf8f7-328">Warehouse mobile devices portal</span></span>

<span data-ttu-id="cf8f7-329">仓库移动设备门户 (WMDP) 是用于本地自行部署的单独组件。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-329">Warehouse mobile devices portal (WMDP) was a standalone component that was intended for on-premises self-deployment.</span></span> <span data-ttu-id="cf8f7-330">此组件在 Finance and Operations 中不再受支持。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-330">This component is no longer supported in Finance and Operations.</span></span> <span data-ttu-id="cf8f7-331">一个可提高用户体验的本机应用已替代 WMDP 的功能。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-331">A native app that improves the user experience has replaced the functionality of WMDP.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-332">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-332">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-333">重复的功能。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-333">Duplicate functionality.</span></span>       |
| <span data-ttu-id="cf8f7-334">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-334">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-335">是。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-335">Yes.</span></span> <span data-ttu-id="cf8f7-336">此功能已经由 Finance and Operations - Warehousing 取代。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-336">This feature has been replaced by Finance and Operations - Warehousing.</span></span> <span data-ttu-id="cf8f7-337">有关设置和先决条件的详细信息，请参阅 [安装和配置 Microsoft Dynamics 365 for Finance and Operations - Warehousing](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/install-configure-warehousing-app)。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-337">For more information about setup and prerequisites, see [Install and configure Microsoft Dynamics 365 for Finance and Operations - Warehousing](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/install-configure-warehousing-app).</span></span> |
| <span data-ttu-id="cf8f7-338">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-338">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-339">仓库管理，运输管理</span><span class="sxs-lookup"><span data-stu-id="cf8f7-339">Warehouse management, Transportation management</span></span>     |
| <span data-ttu-id="cf8f7-340">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-340">**Deployment option**</span></span>              | <span data-ttu-id="cf8f7-341">仓库移动设备门户 (WMDP) 是用于本地自行部署的单独组件。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-341">Warehouse mobile devices portal (WMDP) was a standalone component that was intended for on-premises self-deployment.</span></span>               |
| <span data-ttu-id="cf8f7-342">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-342">**Status**</span></span>                         | <span data-ttu-id="cf8f7-343">已弃用：移除功能的目标时间范围为 2019 年第四季度。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-343">Deprecated: Target timeframe for the functionality to be removed is Q4 2019.</span></span>   |

### <a name="advanced-bank-reconciliation-matching-rule-for-manual-matching"></a><span data-ttu-id="cf8f7-344">用于手动匹配的高级银行对帐匹配规则</span><span class="sxs-lookup"><span data-stu-id="cf8f7-344">Advanced bank reconciliation matching rule for manual matching</span></span>

<span data-ttu-id="cf8f7-345">匹配规则用于在对帐工作表中手动匹配单据时选择和标记银行单据。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-345">A matching rule was used to select and mark a bank document when documents were manually matched in the reconciliation worksheet.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-346">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-346">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-347">有限使用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-347">Limited usage.</span></span>                                                                         |
| <span data-ttu-id="cf8f7-348">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-348">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-349">编号</span><span class="sxs-lookup"><span data-stu-id="cf8f7-349">No.</span></span> <span data-ttu-id="cf8f7-350">应使用列筛选功能查找用于对帐的单据。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-350">Column filtering capabilities should be used to find documents for reconciliation.</span></span> |
| <span data-ttu-id="cf8f7-351">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-351">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-352">现金和银行管理</span><span class="sxs-lookup"><span data-stu-id="cf8f7-352">Cash and bank management</span></span>                                                               |
| <span data-ttu-id="cf8f7-353">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-353">**Deployment option**</span></span>              | <span data-ttu-id="cf8f7-354">全部</span><span class="sxs-lookup"><span data-stu-id="cf8f7-354">All</span></span>                                                                                    |
| <span data-ttu-id="cf8f7-355">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-355">**Status**</span></span>                         | <span data-ttu-id="cf8f7-356">从 2017 年 7 月开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-356">Removed as of July 2017.</span></span>                                                               |

## <a name="dynamics-365-for-operations-1611-with-platform-update-3"></a><span data-ttu-id="cf8f7-357">具有平台更新 3 的 Dynamics 365 for Operations 1611</span><span class="sxs-lookup"><span data-stu-id="cf8f7-357">Dynamics 365 for Operations 1611 with platform update 3</span></span>

### <a name="aeb-payment-formats-for-spain"></a><span data-ttu-id="cf8f7-358">西班牙的 AEB 付款格式</span><span class="sxs-lookup"><span data-stu-id="cf8f7-358">AEB payment formats for Spain</span></span>

<span data-ttu-id="cf8f7-359">Consejo Superior Bancario 付款格式过去用于将汇款文件发送到客户付款和供应商付款的银行。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-359">The Consejo Superior Bancario payment formats were used to send remittance files to the bank for customer payments and vendor payments.</span></span> <span data-ttu-id="cf8f7-360">由 Asociación Española de Banca 确定这些格式的内容。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-360">The content of these formats was determined by the Asociación Española de Banca.</span></span> <span data-ttu-id="cf8f7-361">它包含 Cuaderno 19、32、58、34。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-361">It covers Cuaderno 19, 32, 58, 34.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-362">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-362">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-363">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-363">The payment formats are no longer used.</span></span>                                  |
| <span data-ttu-id="cf8f7-364">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-364">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-365">是，西班牙的 ISO20022 贷方转帐和直接借记付款格式</span><span class="sxs-lookup"><span data-stu-id="cf8f7-365">Yes, ISO20022 Credit transfer and Direct debit payment formats for Spain</span></span> |
| <span data-ttu-id="cf8f7-366">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-366">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-367">应付账款，应收账款</span><span class="sxs-lookup"><span data-stu-id="cf8f7-367">Accounts payable, Accounts receivable</span></span>                                    |
| <span data-ttu-id="cf8f7-368">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-368">**Status**</span></span>                         | <span data-ttu-id="cf8f7-369">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-369">Deprecated: A removal date has not been set for this feature.</span></span>           |

### <a name="bank-payments-transfer-for-lithuania"></a><span data-ttu-id="cf8f7-370">立陶宛银行付款转帐</span><span class="sxs-lookup"><span data-stu-id="cf8f7-370">Bank payments transfer for Lithuania</span></span>

<span data-ttu-id="cf8f7-371">过去使用立陶宛付款转账 (LT) 导出格式生成并打印银行付款转账。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-371">Bank payment transfers were generated and printed by using the Payment transfer (LT) export format for Lithuania.</span></span> <span data-ttu-id="cf8f7-372">立陶宛市场于 2005 年开始使用 LITAS，统一电子银行系统。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-372">The Lithuanian market began to use LITAS, the unified electronic banking system, in 2005.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-373">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-373">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-374">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-374">The payment formats are no longer used.</span></span>                        |
| <span data-ttu-id="cf8f7-375">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-375">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-376">是，立陶宛 ISO20022 贷方转帐付款格式</span><span class="sxs-lookup"><span data-stu-id="cf8f7-376">Yes, ISO20022 Credit transfer payment format for Lithuania</span></span>     |
| <span data-ttu-id="cf8f7-377">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-377">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-378">应付帐款</span><span class="sxs-lookup"><span data-stu-id="cf8f7-378">Accounts payable</span></span>                                               |
| <span data-ttu-id="cf8f7-379">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-379">**Status**</span></span>                         | <span data-ttu-id="cf8f7-380">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-380">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="bbs-direkte-remittering-payment-formats-for-norway"></a><span data-ttu-id="cf8f7-381">挪威 BBS Direkte Remittering 付款格式</span><span class="sxs-lookup"><span data-stu-id="cf8f7-381">BBS Direkte Remittering payment formats for Norway</span></span>

<span data-ttu-id="cf8f7-382">BBS Direkte Remittering 付款格式包括客户收款导出（直接借记）和返回消息导入。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-382">BBS Direkte Remittering payment formats include customer payment collection export (direct debit) and return message import.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-383">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-383">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-384">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-384">The payment formats are no longer used.</span></span>  |
| <span data-ttu-id="cf8f7-385">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-385">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-386">挪威的 AvtaleGiro 客户付款格式可用于生成直接借记消息。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-386">The AvtaleGiro customer payment format for Norway can be used to generate direct debit messages.</span></span> <span data-ttu-id="cf8f7-387">未来版本中将实施返回消息导入。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-387">Return message import will be implemented in future releases.</span></span> |
| <span data-ttu-id="cf8f7-388">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-388">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-389">应付账款，应收账款</span><span class="sxs-lookup"><span data-stu-id="cf8f7-389">Accounts payable, Accounts receivable</span></span>   |
| <span data-ttu-id="cf8f7-390">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-390">**Status**</span></span>                         | <span data-ttu-id="cf8f7-391">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-391">Deprecated: A removal date has not been set for this feature.</span></span>                                                                                                 |

### <a name="chart-of-accounts-tool-for-spain"></a><span data-ttu-id="cf8f7-392">西班牙会计科目表工具</span><span class="sxs-lookup"><span data-stu-id="cf8f7-392">Chart of Accounts tool for Spain</span></span>

<span data-ttu-id="cf8f7-393">西班牙会计科目表要求重大更改时使用此工具。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-393">This tool is used when a chart of accounts in Spain requires major changes.</span></span> <span data-ttu-id="cf8f7-394">用户可以导入新的 Microsoft Excel 或文本格式的会计科目表，也可以导入财务报表。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-394">Users can import a new chart of accounts in Microsoft Excel or text format, and can also import financial statements.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-395">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-395">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-396">有限使用</span><span class="sxs-lookup"><span data-stu-id="cf8f7-396">Limited usage</span></span>                                                  |
| <span data-ttu-id="cf8f7-397">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-397">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-398">无</span><span class="sxs-lookup"><span data-stu-id="cf8f7-398">No</span></span>                                                             |
| <span data-ttu-id="cf8f7-399">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-399">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-400">总帐</span><span class="sxs-lookup"><span data-stu-id="cf8f7-400">General ledger</span></span>                                                 |
| <span data-ttu-id="cf8f7-401">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-401">**Status**</span></span>                         | <span data-ttu-id="cf8f7-402">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-402">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="dom80-payment-format-for-belgium"></a><span data-ttu-id="cf8f7-403">比利时的 Dom80 付款格式</span><span class="sxs-lookup"><span data-stu-id="cf8f7-403">Dom80 payment format for Belgium</span></span>

<span data-ttu-id="cf8f7-404">付款托收的比利时传统付款格式（直接借记）。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-404">Legacy Belgian payment format for payment collection (direct debit).</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-405">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-405">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-406">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-406">The payment format is no longer used.</span></span>                          |
| <span data-ttu-id="cf8f7-407">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-407">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-408">是，比利时 ISO 20022 直接借记付款格式</span><span class="sxs-lookup"><span data-stu-id="cf8f7-408">Yes, ISO 20022 Direct debit payment format for Belgium</span></span>         |
| <span data-ttu-id="cf8f7-409">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-409">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-410">应收帐款</span><span class="sxs-lookup"><span data-stu-id="cf8f7-410">Accounts receivable</span></span>                                            |
| <span data-ttu-id="cf8f7-411">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-411">**Status**</span></span>                         | <span data-ttu-id="cf8f7-412">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-412">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="dtaezag-payment-formats-for-switzerland"></a><span data-ttu-id="cf8f7-413">瑞士的 DTA/EZAG 付款格式</span><span class="sxs-lookup"><span data-stu-id="cf8f7-413">DTA/EZAG payment formats for Switzerland</span></span>

<span data-ttu-id="cf8f7-414">DTA/EZAG 格式集成在 ESR 系统中，因为他们可以持有参考编号。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-414">DTA/EZAG formats are integrated into the ESR system, because they can carry on the reference number.</span></span> <span data-ttu-id="cf8f7-415">由于参考编号不是必需的，因此可以使用这些格式处理任何供应商付款。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-415">Because the reference number isn’t mandatory, these formats can be used to process any vendor payments.</span></span> <span data-ttu-id="cf8f7-416">银行帐户位置不在“Postfinance”的公司使用这些格式。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-416">These formats are used by companies that have a bank account in a location other than “Postfinance.”</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-417">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-417">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-418">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-418">The payment formats are no longer used.</span></span>                        |
| <span data-ttu-id="cf8f7-419">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-419">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-420">是，瑞士 ISO20022 贷方转帐付款格式</span><span class="sxs-lookup"><span data-stu-id="cf8f7-420">Yes, ISO20022 Credit transfer payment format for Switzerland</span></span>   |
| <span data-ttu-id="cf8f7-421">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-421">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-422">应付帐款</span><span class="sxs-lookup"><span data-stu-id="cf8f7-422">Accounts payable</span></span>                                               |
| <span data-ttu-id="cf8f7-423">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-423">**Status**</span></span>                         | <span data-ttu-id="cf8f7-424">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-424">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="edifact-dirdeb-payment-format-for-austria"></a><span data-ttu-id="cf8f7-425">奥地利 EDIFACT-DIRDEB 付款格式</span><span class="sxs-lookup"><span data-stu-id="cf8f7-425">EDIFACT-DIRDEB payment format for Austria</span></span>

<span data-ttu-id="cf8f7-426">付款托收的 EDIFACT-DIRDEB 付款格式（直接借记）。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-426">EDIFACT-DIRDEB payment format for payment collection (direct debit).</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-427">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-427">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-428">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-428">The payment format is no longer used.</span></span>                          |
| <span data-ttu-id="cf8f7-429">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-429">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-430">是，奥地利 ISO 20022 直接借记付款格式</span><span class="sxs-lookup"><span data-stu-id="cf8f7-430">Yes, ISO 20022 Direct debit payment format for Austria</span></span>         |
| <span data-ttu-id="cf8f7-431">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-431">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-432">应收帐款</span><span class="sxs-lookup"><span data-stu-id="cf8f7-432">Accounts receivable</span></span>                                            |
| <span data-ttu-id="cf8f7-433">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-433">**Status**</span></span>                         | <span data-ttu-id="cf8f7-434">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-434">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="edivat-for-belgium"></a><span data-ttu-id="cf8f7-435">比利时的 EDIVAT</span><span class="sxs-lookup"><span data-stu-id="cf8f7-435">EDIVAT for Belgium</span></span>

<span data-ttu-id="cf8f7-436">EDIVAT 是比利时通过安全电子邮件进行电子申报的已过时的标准做法。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-436">EDIVAT is an obsolete Belgian standard for electronic declaration via secure mail.</span></span> <span data-ttu-id="cf8f7-437">Microsoft Dynamics AX 2012 保留启用历史数据访问权限的只读解决方案。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-437">Microsoft Dynamics AX 2012 retains the read-only solution to enable access to the historical data.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-438">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-438">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-439">此功能不再使用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-439">The functionality is no longer used.</span></span>                           |
| <span data-ttu-id="cf8f7-440">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-440">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-441">无</span><span class="sxs-lookup"><span data-stu-id="cf8f7-441">No</span></span>                                                             |
| <span data-ttu-id="cf8f7-442">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-442">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-443">总帐</span><span class="sxs-lookup"><span data-stu-id="cf8f7-443">General ledger</span></span>                                                 |
| <span data-ttu-id="cf8f7-444">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-444">**Status**</span></span>                         | <span data-ttu-id="cf8f7-445">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-445">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="egiro-edifact-cremul-payment-import-format-for-norway"></a><span data-ttu-id="cf8f7-446">挪威的 eGiro EDIFACT CREMUL 付款导入格式</span><span class="sxs-lookup"><span data-stu-id="cf8f7-446">eGiro EDIFACT CREMUL payment import format for Norway</span></span>

<span data-ttu-id="cf8f7-447">eGiro 基于国际 UN EDIFACT CREMUL（多重贷记通知消息）标准，用于客户付款的自动过帐。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-447">eGiro is based on the international UN EDIFACT CREMUL (Multiple Credit Advice Message) standard that is used for automatic posting of customer payments.</span></span> <span data-ttu-id="cf8f7-448">在 Microsoft Dynamics AX 中，eGiro 作为客户付款导入格式实施。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-448">In Microsoft Dynamics AX, eGiro is implemented as a customer payment import format.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-449">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-449">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-450">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-450">The payment format is no longer used.</span></span>                                                     |
| <span data-ttu-id="cf8f7-451">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-451">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-452">编号</span><span class="sxs-lookup"><span data-stu-id="cf8f7-452">No.</span></span> <span data-ttu-id="cf8f7-453">格式在未来版本中将被 ISO 20022 报表导入格式所取代。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-453">The format will be replaced by ISO 20022 statement import formats in future releases.</span></span> |
| <span data-ttu-id="cf8f7-454">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-454">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-455">应收帐款</span><span class="sxs-lookup"><span data-stu-id="cf8f7-455">Accounts receivable</span></span>                                                                       |
| <span data-ttu-id="cf8f7-456">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-456">**Status**</span></span>                         | <span data-ttu-id="cf8f7-457">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-457">Deprecated: A removal date has not been set for this feature.</span></span>                            |

### <a name="external-inventory-for-poland"></a><span data-ttu-id="cf8f7-458">波兰的外部库存</span><span class="sxs-lookup"><span data-stu-id="cf8f7-458">External inventory for Poland</span></span>

<span data-ttu-id="cf8f7-459">来自供应商用于销售且无需购买的货物的证据。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-459">Evidence of goods that are taken from a vendor for sales without purchase.</span></span> <span data-ttu-id="cf8f7-460">在外部库存中处理的货物不影响标准库存，可以销售，然后被自动购买。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-460">Goods that are handled in external inventory don’t affect standard inventory, and can be sold and then purchased automatically.</span></span> <span data-ttu-id="cf8f7-461">此流程创建实际库存变动。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-461">This process creates real inventory movements.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-462">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-462">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-463">替换为另一个功能</span><span class="sxs-lookup"><span data-stu-id="cf8f7-463">Replaced by another feature</span></span>                                    |
| <span data-ttu-id="cf8f7-464">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-464">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-465">是，为核心入站托运功能</span><span class="sxs-lookup"><span data-stu-id="cf8f7-465">Yes, the core Inbound consignment functionality</span></span>                |
| <span data-ttu-id="cf8f7-466">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-466">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-467">应付账款，库存管理</span><span class="sxs-lookup"><span data-stu-id="cf8f7-467">Accounts payable, Inventory management</span></span>                         |
| <span data-ttu-id="cf8f7-468">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-468">**Status**</span></span>                         | <span data-ttu-id="cf8f7-469">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-469">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="financial-reports-generator-for-eastern-europe"></a><span data-ttu-id="cf8f7-470">东欧的财务报表生成器</span><span class="sxs-lookup"><span data-stu-id="cf8f7-470">Financial reports generator for Eastern Europe</span></span>

<span data-ttu-id="cf8f7-471">用于设置会计和纳税报表的数据收集，以及用于将数据导出到 XLS 和 DOC 报表模板的工具。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-471">A tool is used to set up data collection for accounting and tax reports, and to export data to XLS and DOC report templates.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-472">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-472">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-473">有限使用</span><span class="sxs-lookup"><span data-stu-id="cf8f7-473">Limited usage</span></span>                                                                            |
| <span data-ttu-id="cf8f7-474">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-474">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-475">编号</span><span class="sxs-lookup"><span data-stu-id="cf8f7-475">No.</span></span> <span data-ttu-id="cf8f7-476">工具在未来版本中将被电子申报配置所取代。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-476">The tool will be replaced by Electronic reporting configurations in future releases.</span></span> |
| <span data-ttu-id="cf8f7-477">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-477">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-478">总帐</span><span class="sxs-lookup"><span data-stu-id="cf8f7-478">General Ledger</span></span>                                                                           |
| <span data-ttu-id="cf8f7-479">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-479">**Status**</span></span>                         | <span data-ttu-id="cf8f7-480">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-480">Deprecated: A removal date has not been set for this feature.</span></span>                           |

### <a name="import-of-customer-payment-transactions-for-finland"></a><span data-ttu-id="cf8f7-481">芬兰的客户付款交易记录导入</span><span class="sxs-lookup"><span data-stu-id="cf8f7-481">Import of customer payment transactions for Finland</span></span>

<span data-ttu-id="cf8f7-482">您可以为从银行提供的外部文件导入客户付款交易记录的芬兰付款选择导入格式。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-482">You can select an import format for Finnish payments to import customer payment transactions from an external file that the bank provides.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-483">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-483">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-484">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-484">The payment format is no longer used.</span></span>                                                     |
| <span data-ttu-id="cf8f7-485">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-485">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-486">编号</span><span class="sxs-lookup"><span data-stu-id="cf8f7-486">No.</span></span> <span data-ttu-id="cf8f7-487">格式在未来版本中将被 ISO 20022 报表导入格式所取代。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-487">The format will be replaced by ISO 20022 statement import formats in future releases.</span></span> |
| <span data-ttu-id="cf8f7-488">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-488">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-489">应收帐款</span><span class="sxs-lookup"><span data-stu-id="cf8f7-489">Accounts receivable</span></span>                                                                       |
| <span data-ttu-id="cf8f7-490">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-490">**Status**</span></span>                         | <span data-ttu-id="cf8f7-491">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-491">Deprecated: A removal date has not been set for this feature.</span></span>                            |

### <a name="import-of-payment-transactions-into-a-general-ledger-journal-for-finland"></a><span data-ttu-id="cf8f7-492">付款交易记录导入到芬兰的总帐日志帐中</span><span class="sxs-lookup"><span data-stu-id="cf8f7-492">Import of payment transactions into a general ledger journal for Finland</span></span>

<span data-ttu-id="cf8f7-493">用于芬兰将会计交易记录导入到总帐的特定格式。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-493">A format that is specific to Finland is used to import accounting transactions into the general ledger.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-494">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-494">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-495">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-495">The payment format is no longer used.</span></span>                                                     |
| <span data-ttu-id="cf8f7-496">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-496">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-497">编号</span><span class="sxs-lookup"><span data-stu-id="cf8f7-497">No.</span></span> <span data-ttu-id="cf8f7-498">格式在未来版本中将被 ISO 20022 报表导入格式所取代。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-498">The format will be replaced by ISO 20022 statement import formats in future releases.</span></span> |
| <span data-ttu-id="cf8f7-499">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-499">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-500">应收帐款</span><span class="sxs-lookup"><span data-stu-id="cf8f7-500">Accounts receivable</span></span>                                                                       |
| <span data-ttu-id="cf8f7-501">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-501">**Status**</span></span>                         | <span data-ttu-id="cf8f7-502">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-502">Deprecated: A removal date has not been set for this feature.</span></span>                            |

### <a name="integration-with-isabel-synchronized-cis-for-belgium"></a><span data-ttu-id="cf8f7-503">比利时与 Isabel 同步 (CIS) 集成</span><span class="sxs-lookup"><span data-stu-id="cf8f7-503">Integration with Isabel synchronized (CIS) for Belgium</span></span>

<span data-ttu-id="cf8f7-504">Isabel 是欧洲电子银行的框架和比利时的事实标准。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-504">Isabel is the framework for electronic banking in Europe and is a de-facto standard in Belgium.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-505">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-505">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-506">与 Isabel 客户端的集成已停止。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-506">Integration with Isabel client has been discontinued.</span></span>   |
| <span data-ttu-id="cf8f7-507">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-507">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-508">编号</span><span class="sxs-lookup"><span data-stu-id="cf8f7-508">No.</span></span> <span data-ttu-id="cf8f7-509">付款格式不再使用，被比利时的 ISO20022 贷方转帐付款格式所取代。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-509">The payment formats that are no longer used are replaced by ISO20022 Credit transfer payment format for Belgium.</span></span> |
| <span data-ttu-id="cf8f7-510">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-510">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-511">应付帐款</span><span class="sxs-lookup"><span data-stu-id="cf8f7-511">Accounts payable</span></span>     |
| <span data-ttu-id="cf8f7-512">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-512">**Status**</span></span>                         | <span data-ttu-id="cf8f7-513">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-513">Deprecated: A removal date has not been set for this feature.</span></span>    |

### <a name="modifications-in-the-chart-of-accounts-and-accounting-rules-for-spain"></a><span data-ttu-id="cf8f7-514">修改西班牙的会计科目表和会计规则</span><span class="sxs-lookup"><span data-stu-id="cf8f7-514">Modifications in the chart of accounts and accounting rules for Spain</span></span>

<span data-ttu-id="cf8f7-515">此功能用于修改西班牙的会计科目表和会计规则。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-515">This feature is used for changes in the chart of accounts and accounting rules in Spain.</span></span> <span data-ttu-id="cf8f7-516">它映射帐户，以帮助将旧的会计科目表转换到新的会计科目表，将上一个会计年度与新的会计年度相比较，即使是当它们过帐到不同的科目编号时。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-516">It maps accounts to help transform the old chart of accounts into the new chart of accounts, and compares the previous fiscal year with the new fiscal year, even if they were posted to different account numbers.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-517">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-517">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-518">有限使用</span><span class="sxs-lookup"><span data-stu-id="cf8f7-518">Limited usage</span></span>                                                  |
| <span data-ttu-id="cf8f7-519">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-519">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-520">无</span><span class="sxs-lookup"><span data-stu-id="cf8f7-520">No</span></span>                                                             |
| <span data-ttu-id="cf8f7-521">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-521">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-522">总帐</span><span class="sxs-lookup"><span data-stu-id="cf8f7-522">General ledger</span></span>                                                 |
| <span data-ttu-id="cf8f7-523">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-523">**Status**</span></span>                         | <span data-ttu-id="cf8f7-524">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-524">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="pagamento-fornittori-vendor-payment-format"></a><span data-ttu-id="cf8f7-525">Pagamento Fornittori 供应商付款格式</span><span class="sxs-lookup"><span data-stu-id="cf8f7-525">Pagamento Fornittori vendor payment format</span></span>

<span data-ttu-id="cf8f7-526">传统意大利贷方转帐付款格式</span><span class="sxs-lookup"><span data-stu-id="cf8f7-526">Legacy Italian payment format for credit transfers.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-527">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-527">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-528">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-528">The payment format is no longer used.</span></span>                          |
| <span data-ttu-id="cf8f7-529">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-529">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-530">是，意大利 ISO20022 贷方转帐付款格式</span><span class="sxs-lookup"><span data-stu-id="cf8f7-530">Yes, ISO20022 Credit transfer payment format for Italy</span></span>         |
| <span data-ttu-id="cf8f7-531">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-531">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-532">应付帐款</span><span class="sxs-lookup"><span data-stu-id="cf8f7-532">Accounts payable</span></span>                                               |
| <span data-ttu-id="cf8f7-533">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-533">**Status**</span></span>                         | <span data-ttu-id="cf8f7-534">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-534">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="payment-export-formats-for-estonia"></a><span data-ttu-id="cf8f7-535">爱沙尼亚付款导出格式</span><span class="sxs-lookup"><span data-stu-id="cf8f7-535">Payment export formats for Estonia</span></span>

<span data-ttu-id="cf8f7-536">Telehansa 和 Teleservice 格式为银行付款导出使用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-536">The Telehansa and Teleservice formats are used for bank payment export.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-537">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-537">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-538">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-538">The payment formats are no longer used.</span></span>                        |
| <span data-ttu-id="cf8f7-539">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-539">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-540">是，爱沙尼亚 ISO20022 贷方转帐付款格式</span><span class="sxs-lookup"><span data-stu-id="cf8f7-540">Yes, ISO20022 Credit transfer payment format for Estonia</span></span>       |
| <span data-ttu-id="cf8f7-541">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-541">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-542">应付帐款</span><span class="sxs-lookup"><span data-stu-id="cf8f7-542">Accounts payable</span></span>                                               |
| <span data-ttu-id="cf8f7-543">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-543">**Status**</span></span>                         | <span data-ttu-id="cf8f7-544">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-544">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="payment-file-archive-for-norway"></a><span data-ttu-id="cf8f7-545">挪威付款文件存档</span><span class="sxs-lookup"><span data-stu-id="cf8f7-545">Payment file archive for Norway</span></span>

<span data-ttu-id="cf8f7-546">在生成付款文件时，文件存档自动存档所有创建的文件，甚至包括以前写入或读取的文件。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-546">When payment files are generated, the file archive automatically archives all files that are created, even files that were previously written or read.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-547">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-547">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-548">替换为另一个功能</span><span class="sxs-lookup"><span data-stu-id="cf8f7-548">Replaced by another feature</span></span>                                        |
| <span data-ttu-id="cf8f7-549">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-549">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-550">是，电子申报已存档作业</span><span class="sxs-lookup"><span data-stu-id="cf8f7-550">Yes, Electronic reporting archived jobs</span></span>                            |
| <span data-ttu-id="cf8f7-551">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-551">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-552">应付账款，应收账款，组织管理</span><span class="sxs-lookup"><span data-stu-id="cf8f7-552">Accounts payable, Accounts receivable, Organization administration</span></span> |
| <span data-ttu-id="cf8f7-553">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-553">**Status**</span></span>                         | <span data-ttu-id="cf8f7-554">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-554">Deprecated: A removal date has not been set for this feature.</span></span>     |

### <a name="payment-import-formats-for-estonia"></a><span data-ttu-id="cf8f7-555">爱沙尼亚付款导入格式</span><span class="sxs-lookup"><span data-stu-id="cf8f7-555">Payment import formats for Estonia</span></span>

<span data-ttu-id="cf8f7-556">Telehansa 和 TeleTeenus 格式为银行付款导入使用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-556">The Telehansa and TeleTeenus formats are used for bank payment import.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-557">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-557">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-558">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-558">The payment formats are no longer used.</span></span>                                                    |
| <span data-ttu-id="cf8f7-559">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-559">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-560">编号</span><span class="sxs-lookup"><span data-stu-id="cf8f7-560">No.</span></span> <span data-ttu-id="cf8f7-561">格式在未来版本中将被 ISO 20022 报表导入格式所取代。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-561">The formats will be replaced by ISO 20022 statement import formats in future releases.</span></span> |
| <span data-ttu-id="cf8f7-562">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-562">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-563">应收帐款</span><span class="sxs-lookup"><span data-stu-id="cf8f7-563">Accounts receivable</span></span>                                                                        |
| <span data-ttu-id="cf8f7-564">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-564">**Status**</span></span>                         | <span data-ttu-id="cf8f7-565">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-565">Deprecated: A removal date has not been set for this feature.</span></span>                             |

### <a name="payroll-information-in-human-resources"></a><span data-ttu-id="cf8f7-566">人力资源中的工资单信息</span><span class="sxs-lookup"><span data-stu-id="cf8f7-566">Payroll information in Human Resources</span></span>

<span data-ttu-id="cf8f7-567">人力资源工资单信息</span><span class="sxs-lookup"><span data-stu-id="cf8f7-567">Human Resources Payroll information</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-568">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-568">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-569">此功能已由工资单和人力资源页取代。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-569">This functionality has been replaced by core Payroll and Human Resources pages.</span></span>  |
| <span data-ttu-id="cf8f7-570">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-570">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-571">**福利**、**收入**和已经位于美国工资单中的其他相关页已被重新配置，现在是核心人力资源配置的一部分，可帮助支持外部工资单处理。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-571">**Benefits**, **Earnings**, and other related pages that were previously in US Payroll have been reconfigured, and are now part of the core Human Resources configuration to help support external payroll processing.</span></span> <span data-ttu-id="cf8f7-572">此功能可通过使用**人力资源 1** \> **工资单**配置键访问到。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-572">This functionality is accessed by using the **Human Resources 1** \> **Payroll** configuration key.</span></span> |
| <span data-ttu-id="cf8f7-573">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-573">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-574">人力资源、工资单</span><span class="sxs-lookup"><span data-stu-id="cf8f7-574">Human Resources, Payroll</span></span>   |
| <span data-ttu-id="cf8f7-575">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-575">**Status**</span></span>                         | <span data-ttu-id="cf8f7-576">从 Dynamics 365 for Operations 版本 1611 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-576">Removed as of Dynamics 365 for Operations version 1611.</span></span>    |

### <a name="performance-management-goal-workflow"></a><span data-ttu-id="cf8f7-577">绩效管理目标工作流</span><span class="sxs-lookup"><span data-stu-id="cf8f7-577">Performance management goal workflow</span></span>

<span data-ttu-id="cf8f7-578">绩效管理包括目标管理和与绩效审核集成。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-578">Performance management includes goal management and integration with performance reviews.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-579">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-579">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-580">绩效管理经过重新设计，减少了目标页数，以简化流程。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-580">Performance management was redesigned, and the number of goal pages was reduced to simplify the process.</span></span>                 |
| <span data-ttu-id="cf8f7-581">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-581">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-582">编号</span><span class="sxs-lookup"><span data-stu-id="cf8f7-582">No.</span></span> <span data-ttu-id="cf8f7-583">目标通过经理自助服务门户对经理可见，并且可由经理进行更改和查看。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-583">Goals are visible to managers through the Manager Self Service portal, and can be changed and viewed by the manager.</span></span> |
| <span data-ttu-id="cf8f7-584">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-584">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-585">人力资本管理</span><span class="sxs-lookup"><span data-stu-id="cf8f7-585">Human capital management</span></span>       |
| <span data-ttu-id="cf8f7-586">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-586">**Status**</span></span>                         | <span data-ttu-id="cf8f7-587">从 Dynamics 365 for Operations 版本 1611 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-587">Removed as of Dynamics 365 for Operations version 1611.</span></span>    |

### <a name="postgirot-and-postgirot-utland-payment-formats-for-sweden"></a><span data-ttu-id="cf8f7-588">瑞典的 Postgirot 和 Postgirot Utland 付款格式</span><span class="sxs-lookup"><span data-stu-id="cf8f7-588">Postgirot and Postgirot Utland payment formats for Sweden</span></span>

<span data-ttu-id="cf8f7-589">瑞典的 Postgirot 和 Postgirot Utland 付款格式。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-589">Postgirot and Postgirot Utland payment formats for Sweden.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-590">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-590">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-591">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-591">The payment formats are no longer used.</span></span>                        |
| <span data-ttu-id="cf8f7-592">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-592">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-593">是，瑞典 ISO20022 贷方转帐付款格式</span><span class="sxs-lookup"><span data-stu-id="cf8f7-593">Yes, ISO20022 Credit transfer payment format for Sweden</span></span>        |
| <span data-ttu-id="cf8f7-594">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-594">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-595">应付帐款</span><span class="sxs-lookup"><span data-stu-id="cf8f7-595">Accounts payable</span></span>                                               |
| <span data-ttu-id="cf8f7-596">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-596">**Status**</span></span>                         | <span data-ttu-id="cf8f7-597">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-597">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="radio-frequency-identifier"></a><span data-ttu-id="cf8f7-598">射频标识</span><span class="sxs-lookup"><span data-stu-id="cf8f7-598">Radio frequency identifier</span></span>

<span data-ttu-id="cf8f7-599">无线射频标识 (RFID) 是一种使用电子标签存储标识数据的数据收集技术和一种捕获标识数据的无行视域需求阅读器。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-599">Radio Frequency Identification (RFID) is a data-collection technology that uses electronic tags to store identification data and a no-line-of-sight requirement reader to capture the identification data.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-600">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-600">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-601">低客户使用率和有限功能集。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-601">Low customer usage and a limited feature set.</span></span>   |
| <span data-ttu-id="cf8f7-602">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-602">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-603">无</span><span class="sxs-lookup"><span data-stu-id="cf8f7-603">No</span></span>                                              |
| <span data-ttu-id="cf8f7-604">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-604">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-605">库存管理</span><span class="sxs-lookup"><span data-stu-id="cf8f7-605">Inventory management</span></span>                            |
| <span data-ttu-id="cf8f7-606">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-606">**Status**</span></span>                         | <span data-ttu-id="cf8f7-607">从 Dynamics 365 for Operations 1611 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-607">Removed as of Dynamics 365 for Operations 1611.</span></span> |

### <a name="report-about-state-invoices-numbering-for-latvia"></a><span data-ttu-id="cf8f7-608">有关拉脱维亚国家发票编号的报表</span><span class="sxs-lookup"><span data-stu-id="cf8f7-608">Report about state invoices numbering for Latvia</span></span>

<span data-ttu-id="cf8f7-609">拉脱维亚法律提供有关销售发票应如何编号的特定规则。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-609">Latvian legislation provides specific rules about the numbering of sales invoices.</span></span> <span data-ttu-id="cf8f7-610">此功能允许您基于用户或用户组向销售发票分配具体编号。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-610">The functionality lets you assign specific numbers to sales invoices, based on the user or user group.</span></span> <span data-ttu-id="cf8f7-611">之后您可以生成报表或 XML 文件。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-611">You can then generate a report or an XML file.</span></span> <span data-ttu-id="cf8f7-612">您还可以打印有关已使用发票编号的报表。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-612">You can also print a report about invoice numbers that are used.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-613">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-613">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-614">国家发票编号不必再进行维护。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-614">The state invoice numbering no longer has to be maintained.</span></span> <span data-ttu-id="cf8f7-615">不再要求有关已使用发票编号的报表。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-615">The report about used invoice numbers is no longer required.</span></span> |
| <span data-ttu-id="cf8f7-616">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-616">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-617">无</span><span class="sxs-lookup"><span data-stu-id="cf8f7-617">No</span></span>       |
| <span data-ttu-id="cf8f7-618">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-618">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-619">应收帐款</span><span class="sxs-lookup"><span data-stu-id="cf8f7-619">Accounts receivable</span></span>    |
| <span data-ttu-id="cf8f7-620">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-620">**Status**</span></span>                         | <span data-ttu-id="cf8f7-621">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-621">Deprecated: A removal date has not been set for this feature.</span></span>  |

### <a name="set-up-the-names-of-the-manager-and-general-accountant-of-a-company-for-lithuania"></a><span data-ttu-id="cf8f7-622">设置立陶宛公司的经理和会计主管的姓名</span><span class="sxs-lookup"><span data-stu-id="cf8f7-622">Set up the names of the manager and general accountant of a company for Lithuania</span></span>

<span data-ttu-id="cf8f7-623">公司经理和会计主管的姓名可以在公司信息中指定，并用于不同的本地报表打印输出。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-623">The names of the manager and the general accountant of a company can be specified in the company information and used in different local report printouts.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-624">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-624">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-625">替换为另一个功能</span><span class="sxs-lookup"><span data-stu-id="cf8f7-625">Replaced by another feature</span></span>                                     |
| <span data-ttu-id="cf8f7-626">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-626">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-627">是，专员设置可用于同一个目的。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-627">Yes, the setup of officials can be used for the same purpose.</span></span>   |
| <span data-ttu-id="cf8f7-628">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-628">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-629">应付账款、应收账款、现金和银行管理</span><span class="sxs-lookup"><span data-stu-id="cf8f7-629">Accounts payable, Accounts receivable, Cash and bank management</span></span> |
| <span data-ttu-id="cf8f7-630">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-630">**Status**</span></span>                         | <span data-ttu-id="cf8f7-631">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-631">Deprecated: A removal date has not been set for this feature.</span></span>  |

### <a name="shipping-carrier-interface"></a><span data-ttu-id="cf8f7-632">装运承运人界面</span><span class="sxs-lookup"><span data-stu-id="cf8f7-632">Shipping carrier interface</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-633">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-633">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-634">重复的功能</span><span class="sxs-lookup"><span data-stu-id="cf8f7-634">Duplicate functionality</span></span>   |
| <span data-ttu-id="cf8f7-635">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-635">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-636">部分由运输管理取代</span><span class="sxs-lookup"><span data-stu-id="cf8f7-636">Partially replaced by Transportation management</span></span> |
| <span data-ttu-id="cf8f7-637">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-637">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-638">销售和市场营销、库存管理</span><span class="sxs-lookup"><span data-stu-id="cf8f7-638">Sales and marketing, Inventory management</span></span>  |
| <span data-ttu-id="cf8f7-639">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-639">**Status**</span></span>                         | <span data-ttu-id="cf8f7-640">从 Dynamics 365 for Operations 版本 1611 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-640">Removed as of Dynamics 365 for Operations version 1611.</span></span>  |

### <a name="telepay-payment-formats-for-norway"></a><span data-ttu-id="cf8f7-641">挪威 Telepay 付款格式</span><span class="sxs-lookup"><span data-stu-id="cf8f7-641">Telepay payment formats for Norway</span></span>

<span data-ttu-id="cf8f7-642">Telepay 付款格式包括供应商付款导出（贷方转帐）和客户付款托收（直接借记）。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-642">Telepay payment formats include vendor payment export (credit transfer) and customer payment collection (direct debit).</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-643">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-643">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-644">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-644">The payment formats are no longer used.</span></span>                                                        |
| <span data-ttu-id="cf8f7-645">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-645">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-646">是，挪威的 ISO20022 贷方转帐付款格式和 AvtaleGiro 客户付款格式</span><span class="sxs-lookup"><span data-stu-id="cf8f7-646">Yes, ISO20022 Credit transfer payment format and AvtaleGiro customer payment format for Norway</span></span> |
| <span data-ttu-id="cf8f7-647">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-647">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-648">应付账款，应收账款</span><span class="sxs-lookup"><span data-stu-id="cf8f7-648">Accounts payable, Accounts receivable</span></span>                                                          |
| <span data-ttu-id="cf8f7-649">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-649">**Status**</span></span>                         | <span data-ttu-id="cf8f7-650">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-650">Deprecated: A removal date has not been set for this feature.</span></span>                                 |

### <a name="vendor-payment-export-formats-for-finland"></a><span data-ttu-id="cf8f7-651">芬兰的供应商付款导出格式</span><span class="sxs-lookup"><span data-stu-id="cf8f7-651">Vendor payment export formats for Finland</span></span>

<span data-ttu-id="cf8f7-652">两个导出付款格式可用于芬兰。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-652">Two formats for exporting payments are available for Finland.</span></span> <span data-ttu-id="cf8f7-653">LM02 (FI) 用于国内付款，LUM2 (FI) 用于国外付款。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-653">LM02 (FI) is used for domestic payments, and LUM2 (FI) is used for foreign payments.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-654">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-654">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-655">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-655">The payment formats are no longer used.</span></span>                        |
| <span data-ttu-id="cf8f7-656">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-656">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-657">是，芬兰 ISO20022 贷方转帐付款格式</span><span class="sxs-lookup"><span data-stu-id="cf8f7-657">Yes, ISO20022 Credit transfer payment format for Finland</span></span>       |
| <span data-ttu-id="cf8f7-658">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-658">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-659">应付帐款</span><span class="sxs-lookup"><span data-stu-id="cf8f7-659">Accounts payable</span></span>                                               |
| <span data-ttu-id="cf8f7-660">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-660">**Status**</span></span>                         | <span data-ttu-id="cf8f7-661">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-661">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="warehouse-management-ii"></a><span data-ttu-id="cf8f7-662">仓库管理 II</span><span class="sxs-lookup"><span data-stu-id="cf8f7-662">Warehouse management II</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-663">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-663">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-664">**库存管理**模块中可用的仓库管理 II 解决方案 (WMS II) 与在 Microsoft Dynamics AX 2012 R3 中发布的**仓库管理**模块中的功能重复。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-664">The Warehouse management II solution (WMS II) that was available in the **Inventory management** module duplicates functionality that is in the **Warehouse management** module that was released in Microsoft Dynamics AX 2012 R3.</span></span>                                                                         |
| <span data-ttu-id="cf8f7-665">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-665">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-666">在 AX 2012 R3、Microsoft Dynamics AX 2012 R3 CU8 和 Dynamics AX 2012 R3 CU9 中发布的**仓库管理**模块取代仓库管理 II 功能。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-666">The **Warehouse management** module that was released in AX 2012 R3, Microsoft Dynamics AX 2012 R3 CU8, and Dynamics AX 2012 R3 CU9 replaces the Warehouse management II features.</span></span> <span data-ttu-id="cf8f7-667">新模块具有比仓库管理 II 更高级的功能和更灵活的仓库管理流程。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-667">The new module has more advanced features and more flexible warehouse management processes than Warehouse management II.</span></span> |
| <span data-ttu-id="cf8f7-668">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-668">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-669">库存管理、销售和市场营销、采购</span><span class="sxs-lookup"><span data-stu-id="cf8f7-669">Inventory management, Sales and marketing, Procurement and sourcing</span></span>   |
| <span data-ttu-id="cf8f7-670">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-670">**Status**</span></span>                         | <span data-ttu-id="cf8f7-671">从 Dynamics 365 for Operations 版本 1611 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-671">Removed as of Dynamics 365 for Operations version 1611.</span></span>    |

### <a name="worker-reminders-in-human-resources"></a><span data-ttu-id="cf8f7-672">人力资源中的工作人员提醒</span><span class="sxs-lookup"><span data-stu-id="cf8f7-672">Worker reminders in Human Resources</span></span>

<span data-ttu-id="cf8f7-673">人力资源工资单信息</span><span class="sxs-lookup"><span data-stu-id="cf8f7-673">Human Resources Payroll information</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-674">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-674">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-675">低使用率</span><span class="sxs-lookup"><span data-stu-id="cf8f7-675">Low usage</span></span>                                                           |
| <span data-ttu-id="cf8f7-676">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-676">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-677">无</span><span class="sxs-lookup"><span data-stu-id="cf8f7-677">No</span></span>                                                                  |
| <span data-ttu-id="cf8f7-678">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-678">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-679">人力资源</span><span class="sxs-lookup"><span data-stu-id="cf8f7-679">Human resources</span></span>                                                     |
| <span data-ttu-id="cf8f7-680">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-680">**Status**</span></span>                         | <span data-ttu-id="cf8f7-681">从 Dynamics 365 for Operations 版本 1611 开始移除</span><span class="sxs-lookup"><span data-stu-id="cf8f7-681">Removed as of Dynamics 365 for Operations version 1611</span></span> |

### <a name="workflow-for-creating-goals"></a><span data-ttu-id="cf8f7-682">创建目标的工作流</span><span class="sxs-lookup"><span data-stu-id="cf8f7-682">Workflow for creating goals</span></span>

<span data-ttu-id="cf8f7-683">管理员工目标创建的工作流是多个可用工作流的其中一个，帮助协调绩效管理流程。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-683">A workflow for managing the creation of employee goals is one of several workflows that were available to help coordinate the performance management process.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-684">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-684">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-685">绩效管理在 Microsoft Dynamics 365 for Finance and Operations 中已经完全重新设计。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-685">Performance management has been completely redesigned in Microsoft Dynamics 365 for Finance and Operations.</span></span>     |
| <span data-ttu-id="cf8f7-686">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-686">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-687">经过重新设计的绩效管理功能能够更好地控制目标内容、用来跟踪进度的衡量指标以及支持文档的附加。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-687">The redesigned Performance management feature gives more control over the content of the goals, the measurements that are used to track progress, and the attachment of supporting documentation.</span></span> <span data-ttu-id="cf8f7-688">目标可以存储为模板并重复使用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-688">Goals can be stored as templates and then reused.</span></span> <span data-ttu-id="cf8f7-689">此功能可以帮助您更加快速地为您的员工设置额外目标。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-689">This feature can help you set up additional goals for your employees more quickly.</span></span> |
| <span data-ttu-id="cf8f7-690">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-690">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-691">人力资本管理</span><span class="sxs-lookup"><span data-stu-id="cf8f7-691">Human capital management</span></span>                 |
| <span data-ttu-id="cf8f7-692">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-692">**Status**</span></span>                         | <span data-ttu-id="cf8f7-693">从 Dynamics 365 for Operations 版本 1611 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-693">Removed as of Dynamics 365 for Operations version 1611.</span></span> |

## <a name="dynamics-ax-70"></a><span data-ttu-id="cf8f7-694">Dynamics AX 7.0</span><span class="sxs-lookup"><span data-stu-id="cf8f7-694">Dynamics AX 7.0</span></span> 


### <a name="ability-to-cancel-changes-to-a-vendor-invoice"></a><span data-ttu-id="cf8f7-695">能够取消对供应商发票的更改</span><span class="sxs-lookup"><span data-stu-id="cf8f7-695">Ability to cancel changes to a vendor invoice</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-696">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-696">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-697">性能改进</span><span class="sxs-lookup"><span data-stu-id="cf8f7-697">Performance enhancement</span></span>        |
| <span data-ttu-id="cf8f7-698">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-698">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-699">无</span><span class="sxs-lookup"><span data-stu-id="cf8f7-699">No</span></span>                             |
| <span data-ttu-id="cf8f7-700">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-700">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-701">应付帐款</span><span class="sxs-lookup"><span data-stu-id="cf8f7-701">Accounts payable</span></span>               |
| <span data-ttu-id="cf8f7-702">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-702">**Status**</span></span>                         | <span data-ttu-id="cf8f7-703">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-703">Removed as of Dynamics AX 7.0.</span></span> |

### <a name="aif-axd-and-axbc-integrations"></a><span data-ttu-id="cf8f7-704">AIF、Axd 和 AxBC 集成</span><span class="sxs-lookup"><span data-stu-id="cf8f7-704">AIF, AxD, and AxBC integrations</span></span>

<span data-ttu-id="cf8f7-705">在应用集成框架 (AIF) 中，数据可以通过显示为服务的业务逻辑与外部系统交换。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-705">In Application Integration Framework (AIF), data can be exchanged with external systems through business logic that is exposed as services.</span></span> <span data-ttu-id="cf8f7-706">Dynamics AX 包括基于文档和 .NET Business Connector (AxBC) 的服务。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-706">Dynamics AX includes services that are based on documents and .NET Business Connector (AxBC).</span></span> <span data-ttu-id="cf8f7-707">文档是通过使用 XML 创建的。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-707">A document is created by using XML.</span></span> <span data-ttu-id="cf8f7-708">XML 包括标题信息，添加该信息的目的是创建可在 Dynamics AX 内外传送的*消息*。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-708">The XML includes header information that is added to create a *message* that can be transferred into or out of Dynamics AX.</span></span> <span data-ttu-id="cf8f7-709">文档的示例包括销售订单和采购订单。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-709">Examples of documents include sales orders and purchase orders.</span></span> <span data-ttu-id="cf8f7-710">但是，几乎所有实体（例如客户）都可以被文档代表。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-710">However, almost any entity, such as a customer, can be represented by a document.</span></span> <span data-ttu-id="cf8f7-711">基于文档的服务使用 **Axd \<文档\>** 类。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-711">Services that are based on documents use the **Axd \<Document\>** classes.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-712">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-712">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-713">AIF 和 AxDs 的体系结构不能扩展到云服务。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-713">The architecture of AIF and AxDs could not be scaled to a cloud service.</span></span> <span data-ttu-id="cf8f7-714">批量导入有性能问题。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-714">There were performance issues around bulk import.</span></span>                                        |
| <span data-ttu-id="cf8f7-715">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-715">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-716">此功能由数据导入/导出框架取代，该框架支持重复执行的批量导入/导出。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-716">This feature is replaced by the Data Import/Export framework, which supports recurring bulk import/export.</span></span> <span data-ttu-id="cf8f7-717">对于 AxBC，我们建议您使用实际表。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-717">For AxBC, we recommend that you use the actual tables.</span></span> |
| <span data-ttu-id="cf8f7-718">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-718">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-719">AxDs、AxBC 和 AIF</span><span class="sxs-lookup"><span data-stu-id="cf8f7-719">AxDs, AxBCs, and AIF</span></span>   |
| <span data-ttu-id="cf8f7-720">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-720">**Status**</span></span>                         | <span data-ttu-id="cf8f7-721">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-721">Removed as of Dynamics AX 7.0.</span></span>   |

### <a name="boms-without-bom-versions"></a><span data-ttu-id="cf8f7-722">没有物料清单版本的物料清单</span><span class="sxs-lookup"><span data-stu-id="cf8f7-722">BOMs without BOM versions</span></span>

<span data-ttu-id="cf8f7-723">当禁用**物料清单版本**配置键时，物料清单版本在所有窗体中处于隐藏状态，系统将在已发布的产品和物料清单之间强制 1:1 关系。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-723">When the **BOM versions** configuration key was disabled, bill of materials (BOM) versions were hidden in all forms, and the system forced a 1:1 relationship between released products and BOMs.</span></span> <span data-ttu-id="cf8f7-724">在 Dynamics AX 的当前版本中，**物料清单版本**配置键不能禁用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-724">In the current version of Dynamics AX, the **BOM versions** configuration key can't be disabled.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-725">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-725">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-726">使用配置键控制物料清单版本不会在云环境中扩展。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-726">Using a configuration key to control BOM versions doesn't scale in a cloud environment.</span></span> |
| <span data-ttu-id="cf8f7-727">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-727">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-728">无</span><span class="sxs-lookup"><span data-stu-id="cf8f7-728">No</span></span>                                                                                      |
| <span data-ttu-id="cf8f7-729">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-729">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-730">产品信息管理、库存管理</span><span class="sxs-lookup"><span data-stu-id="cf8f7-730">Product information management, Inventory management</span></span>                                    |
| <span data-ttu-id="cf8f7-731">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-731">**Status**</span></span>                         | <span data-ttu-id="cf8f7-732">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-732">Removed as of Dynamics AX 7.0.</span></span>                                                          |

### <a name="brazilian-bordero"></a><span data-ttu-id="cf8f7-733">巴西 Bordero</span><span class="sxs-lookup"><span data-stu-id="cf8f7-733">Brazilian Bordero</span></span>

<span data-ttu-id="cf8f7-734">巴西公司的特定付款方式</span><span class="sxs-lookup"><span data-stu-id="cf8f7-734">Specific method of payment for Brazilian companies</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-735">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-735">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-736">对巴西 Bordero 付款方式的支持已经在巴西本地化中被中断。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-736">Support for the Brazilian Bordero method of payment has been discontinued from Brazilian localization</span></span> |
| <span data-ttu-id="cf8f7-737">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-737">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-738">无</span><span class="sxs-lookup"><span data-stu-id="cf8f7-738">No</span></span>   |
| <span data-ttu-id="cf8f7-739">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-739">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-740">应付帐款</span><span class="sxs-lookup"><span data-stu-id="cf8f7-740">Accounts payable</span></span>   |
| <span data-ttu-id="cf8f7-741">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-741">**Status**</span></span>                         | <span data-ttu-id="cf8f7-742">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-742">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="brazilian-sintegra-statement"></a><span data-ttu-id="cf8f7-743">巴西 Sintegra 报表</span><span class="sxs-lookup"><span data-stu-id="cf8f7-743">Brazilian Sintegra statement</span></span>

<span data-ttu-id="cf8f7-744">ICMS 税联邦报税单</span><span class="sxs-lookup"><span data-stu-id="cf8f7-744">Federal tax statement for ICMS tax</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-745">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-745">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-746">此报表在巴西的部分州不再适用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-746">This statement is no longer applicable in some Brazilian states.</span></span> |
| <span data-ttu-id="cf8f7-747">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-747">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-748">编号</span><span class="sxs-lookup"><span data-stu-id="cf8f7-748">No.</span></span> <span data-ttu-id="cf8f7-749">在某些特定情况下，用户可以使用通用电子申报工具配置报表。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-749">Users can use Generic Electronic reporting tool to configure the statement if required under specific situations.</span></span> |
| <span data-ttu-id="cf8f7-750">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-750">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-751">会计帐簿</span><span class="sxs-lookup"><span data-stu-id="cf8f7-751">Fiscal books</span></span>    |
| <span data-ttu-id="cf8f7-752">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-752">**Status**</span></span>                         | <span data-ttu-id="cf8f7-753">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-753">Deprecated: A removal date has not been set for this feature.</span></span>   |

### <a name="brazilian-scan-contingency-mode-for-nf-e"></a><span data-ttu-id="cf8f7-754">巴西的 SCAN NF-e 意外事故模式</span><span class="sxs-lookup"><span data-stu-id="cf8f7-754">Brazilian SCAN contingency mode for NF-e</span></span>

<span data-ttu-id="cf8f7-755">(SCAN) 意外事故环境用于在 Secretaria da Fazenda (SEFAZ) 环境不可用时生成、导出和导入 Nota Fiscal eletrônica (NF-e) 的状态。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-755">(SCAN) contingency environment is used to generate, export, and import the status of a Nota Fiscal eletrônica (NF-e) when the environment of Secretaria da Fazenda (SEFAZ) is not available.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-756">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-756">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-757">此意外事故方法在巴西所有州中不再适用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-757">This method of contingency is no longer applicable in all Brazilian states</span></span> |
| <span data-ttu-id="cf8f7-758">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-758">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-759">无</span><span class="sxs-lookup"><span data-stu-id="cf8f7-759">No</span></span>                                                                          |
| <span data-ttu-id="cf8f7-760">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-760">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-761">应收帐款</span><span class="sxs-lookup"><span data-stu-id="cf8f7-761">Accounts receivable</span></span>                                                         |
| <span data-ttu-id="cf8f7-762">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-762">**Status**</span></span>                         | <span data-ttu-id="cf8f7-763">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-763">Deprecated: A removal date has not been set for this feature.</span></span>              |

### <a name="business-analyzer"></a><span data-ttu-id="cf8f7-764">业务分析器</span><span class="sxs-lookup"><span data-stu-id="cf8f7-764">Business Analyzer</span></span>

<span data-ttu-id="cf8f7-765">此移动应用程序能让用户查看关键业务度量。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-765">This mobile application let users review key business metrics.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-766">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-766">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-767">此功能已被另一个功能取代。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-767">This functionality has been replaced by another feature.</span></span>   |
| <span data-ttu-id="cf8f7-768">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-768">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-769">Microsoft Power BI 的监控财务业绩目录包将包括已经在 Business Analyzer 中可用的关键财务度量。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-769">The Monitor financial performance content pack for Microsoft Power BI will include key financial metrics that were previously available in Business Analyzer.</span></span> |
| <span data-ttu-id="cf8f7-770">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-770">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-771">总帐</span><span class="sxs-lookup"><span data-stu-id="cf8f7-771">General ledger</span></span>      |
| <span data-ttu-id="cf8f7-772">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-772">**Status**</span></span>                         | <span data-ttu-id="cf8f7-773">已弃用：业务分析器的使用已被弃用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-773">Deprecated: The use of Business Analyzer has been deprecated.</span></span>    |

### <a name="business-statistics"></a><span data-ttu-id="cf8f7-774">业务统计</span><span class="sxs-lookup"><span data-stu-id="cf8f7-774">Business statistics</span></span>

<span data-ttu-id="cf8f7-775">设置业务统计查询，以帮助您分析组织的绩效</span><span class="sxs-lookup"><span data-stu-id="cf8f7-775">The setup of business statistics inquiries that can help you analyze the performance of the organization</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-776">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-776">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-777">商业智能 (BI)、低客户使用率和有限功能集的传统方法</span><span class="sxs-lookup"><span data-stu-id="cf8f7-777">Legacy approach to business intelligence (BI), low customer usage, and a limited feature set</span></span> |
| <span data-ttu-id="cf8f7-778">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-778">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-779">Dynamics AX 的当前版本的新 BI 解决方案</span><span class="sxs-lookup"><span data-stu-id="cf8f7-779">New BI solutions for the current version of Dynamics AX</span></span>                                      |
| <span data-ttu-id="cf8f7-780">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-780">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-781">采购、应付账款、销售和市场营销、应收账款</span><span class="sxs-lookup"><span data-stu-id="cf8f7-781">Procurement and sourcing, Accounts payable, Sales and marketing, Accounts receivable</span></span>         |
| <span data-ttu-id="cf8f7-782">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-782">**Status**</span></span>                         | <span data-ttu-id="cf8f7-783">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-783">Removed as of Dynamics AX 7.0.</span></span>                                                               |

### <a name="change-document-date-function-in-invoice-approval-journal"></a><span data-ttu-id="cf8f7-784">更改发票审核日记帐的单据日期功能</span><span class="sxs-lookup"><span data-stu-id="cf8f7-784">Change document date function in Invoice approval journal</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-785">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-785">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-786">低使用率</span><span class="sxs-lookup"><span data-stu-id="cf8f7-786">Low usage</span></span>                                                               |
| <span data-ttu-id="cf8f7-787">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-787">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-788">是。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-788">Yes.</span></span> <span data-ttu-id="cf8f7-789">可以更改已过帐供应商交易记录的单据日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-789">The document date on the posted vendor transaction can be changed.</span></span> |
| <span data-ttu-id="cf8f7-790">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-790">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-791">应付帐款</span><span class="sxs-lookup"><span data-stu-id="cf8f7-791">Accounts payable</span></span>                                                        |
| <span data-ttu-id="cf8f7-792">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-792">**Status**</span></span>                         | <span data-ttu-id="cf8f7-793">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-793">Removed as of Dynamics AX 7.0.</span></span>                                          |

### <a name="clieop03-payment-format-for-the-netherlands"></a><span data-ttu-id="cf8f7-794">针对荷兰的 ClieOp03 付款格式</span><span class="sxs-lookup"><span data-stu-id="cf8f7-794">ClieOp03 payment format for the Netherlands</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-795">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-795">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-796">该格式不再适用于荷兰，因为它已被 SEPA 功能取代。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-796">The format is no longer applicable in the Netherlands, because it has been replaced by SEPA functionality.</span></span> |
| <span data-ttu-id="cf8f7-797">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-797">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-798">SEPA 付款导出</span><span class="sxs-lookup"><span data-stu-id="cf8f7-798">SEPA payments export</span></span>  |
| <span data-ttu-id="cf8f7-799">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-799">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-800">所有模块</span><span class="sxs-lookup"><span data-stu-id="cf8f7-800">All modules</span></span>     |
| <span data-ttu-id="cf8f7-801">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-801">**Status**</span></span>                         | <span data-ttu-id="cf8f7-802">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-802">Deprecated: A removal date has not been set for this feature.</span></span>   |

### <a name="compliance-center"></a><span data-ttu-id="cf8f7-803">遵从性中心</span><span class="sxs-lookup"><span data-stu-id="cf8f7-803">Compliance Center</span></span>

<span data-ttu-id="cf8f7-804">遵从性中心是一个企业门户站点，用于管理与 Sarbanes-Oxley 法案有关的遵从性计划的文档要求。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-804">The Compliance Center was an Enterprise Portal site for managing the documentation requirements for compliance initiatives that are related to the Sarbanes-Oxley law.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-805">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-805">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-806">缺少客户使用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-806">Lack of customer usage.</span></span> <span data-ttu-id="cf8f7-807">Microsoft SharePoint 包括和遵从性中心功能相同的功能。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-807">Microsoft SharePoint includes the same capability that was available in the Compliance Center.</span></span> |
| <span data-ttu-id="cf8f7-808">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-808">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-809">无</span><span class="sxs-lookup"><span data-stu-id="cf8f7-809">No</span></span>   |
| <span data-ttu-id="cf8f7-810">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-810">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-811">符合性和内部控制</span><span class="sxs-lookup"><span data-stu-id="cf8f7-811">Compliance and internal controls</span></span>  |
| <span data-ttu-id="cf8f7-812">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-812">**Status**</span></span>                         | <span data-ttu-id="cf8f7-813">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-813">Removed as of Dynamics AX 7.0.</span></span>    |

### <a name="connector-for-microsoft-dynamics"></a><span data-ttu-id="cf8f7-814">Connector for Microsoft Dynamics</span><span class="sxs-lookup"><span data-stu-id="cf8f7-814">Connector for Microsoft Dynamics</span></span>

<span data-ttu-id="cf8f7-815">此工具用于集成从 Microsoft Dynamics CRM 到 Microsoft Dynamics ERP 应用程序的重要数据。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-815">This tool was used to integrate key data from Microsoft Dynamics CRM to Microsoft Dynamics ERP applications.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-816">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-816">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-817">此功能已被另一个功能取代。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-817">This functionality has been replaced by another feature.</span></span> |
| <span data-ttu-id="cf8f7-818">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-818">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-819">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="cf8f7-819">Common data service</span></span>                                      |
| <span data-ttu-id="cf8f7-820">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-820">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-821">Connector for Microsoft Dynamics</span><span class="sxs-lookup"><span data-stu-id="cf8f7-821">Connector for Microsoft Dynamics</span></span>                         |
| <span data-ttu-id="cf8f7-822">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-822">**Status**</span></span>                         | <span data-ttu-id="cf8f7-823">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-823">Removed as of Dynamics AX 7.0.</span></span>                           |

### <a name="container-unit-and-multi-dimension-on-hand"></a><span data-ttu-id="cf8f7-824">容器单位和多维现有量</span><span class="sxs-lookup"><span data-stu-id="cf8f7-824">Container unit and multi dimension on-hand</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-825">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-825">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-826">重复的功能</span><span class="sxs-lookup"><span data-stu-id="cf8f7-826">Duplicate functionality</span></span> |
| <span data-ttu-id="cf8f7-827">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-827">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-828">是。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-828">Yes.</span></span> <span data-ttu-id="cf8f7-829">自 AX 2012 起，此功能已由合并的批次订单功能集替换。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-829">Since AX 2012, this functionality has been replaced by the consolidated batch orders feature set.</span></span> <span data-ttu-id="cf8f7-830">此功能集包括合并的现有量视图。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-830">This feature set includes the consolidated on-hand view.</span></span> |
| <span data-ttu-id="cf8f7-831">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-831">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-832">产品信息控制管理、生产控制、库存管理、销售和市场营销</span><span class="sxs-lookup"><span data-stu-id="cf8f7-832">Product information management, Production control, Inventory management, Sales and marketing</span></span>  |
| <span data-ttu-id="cf8f7-833">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-833">**Status**</span></span>                         | <span data-ttu-id="cf8f7-834">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-834">Removed as of Dynamics AX 7.0.</span></span> |

### <a name="cue-group-metadata"></a><span data-ttu-id="cf8f7-835">提示组元数据</span><span class="sxs-lookup"><span data-stu-id="cf8f7-835">Cue group metadata</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-836">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-836">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-837">提示组用于在 FactBox 区域中显示一个或多个提示。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-837">Cue groups were used to display one or more Cues in the FactBox area.</span></span> <span data-ttu-id="cf8f7-838">由于父窗体中的记录更改会导致提示组中每个提示对应一个查询，因此它的接受程度有限，而且还存在性能顾虑。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-838">There was limited uptake, and there were also performance concerns, because a record change in a parent form caused one query per Cue in the Cue group.</span></span> |
| <span data-ttu-id="cf8f7-839">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-839">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-840">无</span><span class="sxs-lookup"><span data-stu-id="cf8f7-840">No</span></span>      |
| <span data-ttu-id="cf8f7-841">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-841">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-842">所有模块</span><span class="sxs-lookup"><span data-stu-id="cf8f7-842">All modules</span></span>    |
| <span data-ttu-id="cf8f7-843">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-843">**Status**</span></span>                         | <span data-ttu-id="cf8f7-844">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-844">Removed as of Dynamics AX 7.0.</span></span>  |

### <a name="cue-metadata"></a><span data-ttu-id="cf8f7-845">提示元数据</span><span class="sxs-lookup"><span data-stu-id="cf8f7-845">Cue metadata</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-846">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-846">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-847">提示元数据仅限于计数或合计信息。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-847">Cue metadata was limited to count or sum information.</span></span>    |
| <span data-ttu-id="cf8f7-848">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-848">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-849">引入了磁贴元数据，可为建模提供更多灵活性。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-849">Tile metadata was introduced to provide more flexibility for modeling.</span></span> <span data-ttu-id="cf8f7-850">例如，您可以对当前计数、导航和关键绩效指标 (KPI) 进行建模。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-850">For example, you can model current counts, navigation, and key performance indicators (KPIs).</span></span> <span data-ttu-id="cf8f7-851">计数磁贴元数据是提示元数据的直接取代。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-851">Count tile metadata is the direct replacement of the Cue metadata.</span></span> |
| <span data-ttu-id="cf8f7-852">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-852">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-853">所有模块</span><span class="sxs-lookup"><span data-stu-id="cf8f7-853">All modules</span></span>           |
| <span data-ttu-id="cf8f7-854">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-854">**Status**</span></span>                         | <span data-ttu-id="cf8f7-855">从 Dynamics AX 7.0 开始移除</span><span class="sxs-lookup"><span data-stu-id="cf8f7-855">Removed as of Dynamics AX 7.0</span></span>      |

### <a name="danish-check-format"></a><span data-ttu-id="cf8f7-856">丹麦支票格式</span><span class="sxs-lookup"><span data-stu-id="cf8f7-856">Danish check format</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-857">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-857">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-858">对丹麦支票格式布局的支持已终止，并且报告已经从 DK 本地化中删除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-858">Support for the Danish check format layout has been discontinued, and the report has been removed from DK localization.</span></span> |
| <span data-ttu-id="cf8f7-859">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-859">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-860">无</span><span class="sxs-lookup"><span data-stu-id="cf8f7-860">No</span></span>    |
| <span data-ttu-id="cf8f7-861">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-861">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-862">所有模块</span><span class="sxs-lookup"><span data-stu-id="cf8f7-862">All modules</span></span>    |
| <span data-ttu-id="cf8f7-863">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-863">**Status**</span></span>                         | <span data-ttu-id="cf8f7-864">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-864">Deprecated: A removal date has not been set for this feature.</span></span>  |

### <a name="data-partitions"></a><span data-ttu-id="cf8f7-865">数据分区</span><span class="sxs-lookup"><span data-stu-id="cf8f7-865">Data partitions</span></span>

<span data-ttu-id="cf8f7-866">数据分区在 Microsoft Dynamics AX 数据库中提供数据的逻辑界定。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-866">Data partitions provide a logical separation of data in the Microsoft Dynamics AX database.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-867">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-867">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-868">数据分区在 Microsoft Dynamics AX 2012 R2 引入以启用数据隔离。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-868">Data partitions were introduced in Microsoft Dynamics AX 2012 R2 to enable data isolation.</span></span> <span data-ttu-id="cf8f7-869">在常见情况中，公司有子公司，一个子公司的数据不应对另一个子公司可见，即使两个子公司均由相同的 IT 部门管理。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-869">In a common scenario, a company has subsidiaries, and the data from one subsidiary should not be visible to another subsidiary, even though both subsidiaries are managed by the same IT department.</span></span> <span data-ttu-id="cf8f7-870">不过，整个程序都需要额外的脚本和管理开销来创建新的分区并填充数据，以及备份分区数据。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-870">However, extra scripts and management overhead throughout the program were required in order to create new partitions and populate them with data, and to back up partition data.</span></span> <span data-ttu-id="cf8f7-871">在云中，在其中我们有访问平台即服务 (PaaS) 数据库服务（Microsoft SQL Azure 数据库）的权限，则使用数据库作为隔离容器比在程序中执行隔离要高效得多。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-871">In the cloud, where we have access to platform as a service (PaaS) database services (Microsoft Azure SQL Database), it's much more efficient to use a database as the isolation container than to do isolation in the program.</span></span> <span data-ttu-id="cf8f7-872">不管是子公司、多个租户，或只为规模需要进行数据分区，我们认为通过多个 Finance and Operations 实例都可以更好地处理这种情况。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-872">Regardless of whether data partitioning is required for subsidiaries, for multiple tenants, or just for scale, we believe that the scenarios can be handled better through multiple instances of Finance and Operations.</span></span> |
| <span data-ttu-id="cf8f7-873">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-873">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-874">如果数据库级别分隔是关键问题，使用数据分区的客户必须使用多个 Finance and Operations 实例。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-874">Customers using data partitions must use multiple instances of Finance and Operations if database level separation is a critical issue.</span></span>    |
| <span data-ttu-id="cf8f7-875">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-875">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-876">所有模块</span><span class="sxs-lookup"><span data-stu-id="cf8f7-876">All modules</span></span>  |
| <span data-ttu-id="cf8f7-877">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-877">**Status**</span></span>                         | <span data-ttu-id="cf8f7-878">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-878">Removed as of Dynamics AX 7.0.</span></span>  |


### <a name="database-and-file-share-storage-for-attachments"></a><span data-ttu-id="cf8f7-879">数据库和文件共享附件存储</span><span class="sxs-lookup"><span data-stu-id="cf8f7-879">Database and file share storage for attachments</span></span>

<span data-ttu-id="cf8f7-880">Microsoft Dynamics AX 2012 允许在数据库和文件共享中存储附件。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-880">Microsoft Dynamics AX 2012 allowed storage of attachments in the database and in file shares.</span></span> <span data-ttu-id="cf8f7-881">这两个选项都不再受支持。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-881">Both of those options are no longer supported.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-882">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-882">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-883">云托管的环境无法再与本地文件共享通信，因此文件共享存储不再受支持。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-883">Files share storage is no longer supported because cloud-hosted environments cannot communicate with local file shares.</span></span> <span data-ttu-id="cf8f7-884">为了支持 Azure Blob 存储，数据库存储已弃用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-884">Database storage has been deprecated in favor of Azure Blob storage.</span></span> <span data-ttu-id="cf8f7-885">Azure Blob 存储相当于数据库中的存储，因为文档仅可以通过 Dynamics 365 for Finance and Operations 客户端窗体进行访问。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-885">Azure Blob storage is equivalent to storage in the database, as documents can only be accessed through Dynamics 365 for Finance and Operations client forms.</span></span> <span data-ttu-id="cf8f7-886">这提供额外好处，即提供存储不会对数据库的性能造成不利影响。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-886">This provides the added benefit of providing storage that doesn't negatively affect the performance of the database.</span></span> <span data-ttu-id="cf8f7-887">Blob 存储是文档管理的默认存储机制并立即生效。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-887">Blob storage is the default storage mechanism for Document Management and works immediately.</span></span> |
| <span data-ttu-id="cf8f7-888">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-888">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-889">为了支持 Azure Blob 存储，数据库存储已弃用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-889">Database storage has been deprecated in favor of Azure Blob storage.</span></span>   |
| <span data-ttu-id="cf8f7-890">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-890">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-891">所有模块</span><span class="sxs-lookup"><span data-stu-id="cf8f7-891">All modules</span></span>  |
| <span data-ttu-id="cf8f7-892">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-892">**Status**</span></span>                         | <span data-ttu-id="cf8f7-893">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-893">Removed as of Dynamics AX 7.0.</span></span>   |

### <a name="delimitation"></a><span data-ttu-id="cf8f7-894">界定</span><span class="sxs-lookup"><span data-stu-id="cf8f7-894">Delimitation</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-895">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-895">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-896">找不到该功能的使用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-896">No use of the functionality was found.</span></span> |
| <span data-ttu-id="cf8f7-897">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-897">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-898">无</span><span class="sxs-lookup"><span data-stu-id="cf8f7-898">No</span></span>                                     |
| <span data-ttu-id="cf8f7-899">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-899">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-900">考勤管理</span><span class="sxs-lookup"><span data-stu-id="cf8f7-900">Time and attendance</span></span>                    |
| <span data-ttu-id="cf8f7-901">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-901">**Status**</span></span>                         | <span data-ttu-id="cf8f7-902">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-902">Removed as of Dynamics AX 7.0.</span></span>         |

### <a name="desktop-client"></a><span data-ttu-id="cf8f7-903">桌面客户端</span><span class="sxs-lookup"><span data-stu-id="cf8f7-903">Desktop client</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-904">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-904">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-905">Dynamics AX 客户端体验已被重新设计，可提高在多个平台和设备上的可用性。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-905">The Dynamics AX client experience has been redesigned to improve usability across multiple platforms and devices.</span></span>                      |
| <span data-ttu-id="cf8f7-906">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-906">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-907">新的 Web 客户端基于已经过修改可提供丰富 Web 平台的桌面窗体元数据和编程模型。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-907">The new web client is based on the desktop Form metadata and programming model that have been modified to provide a rich web platform.</span></span> |
| <span data-ttu-id="cf8f7-908">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-908">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-909">所有模块</span><span class="sxs-lookup"><span data-stu-id="cf8f7-909">All modules</span></span>  |
| <span data-ttu-id="cf8f7-910">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-910">**Status**</span></span>                         | <span data-ttu-id="cf8f7-911">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-911">Removed as of Dynamics AX 7.0.</span></span>   |

### <a name="direct-database-connection"></a><span data-ttu-id="cf8f7-912">直接数据库连接</span><span class="sxs-lookup"><span data-stu-id="cf8f7-912">Direct database connection</span></span>

<span data-ttu-id="cf8f7-913">在 Dynamics AX 2012 R3 中，Retail Modern POS 可以直接连接到与 Enterprise POS 方式相似的通道 DB。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-913">In Dynamics AX 2012 R3, Retail Modern POS could connect directly to the Channel DB in similar fashion to Enterprise POS.</span></span> <span data-ttu-id="cf8f7-914">这是除通过 Retail Server 的 Retail Modern POS 通信的标准通信方法以外的方法。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-914">This was in addition to the standard communication method of Retail Modern POS communicating through Retail Server.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-915">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-915">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-916">直接数据库连接要求较低的安全协议，主要用于达到最高性能级别。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-916">Direct database connectivity required lower security protocols and was primarily used to achieve the highest levels of performance.</span></span> <span data-ttu-id="cf8f7-917">由于 Finance and Operations 发生的性能和安全性提高，此功能现在导致的问题比解决的问题更多。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-917">Due to the performance and security enhancements that have occurred in Finance and Operations, this functionality now causes more issues than it solves.</span></span> |
| <span data-ttu-id="cf8f7-918">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-918">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-919">编号</span><span class="sxs-lookup"><span data-stu-id="cf8f7-919">No.</span></span> <span data-ttu-id="cf8f7-920">现在只支持标准零售服务器通信。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-920">Only standard Retail Server communication is now supported.</span></span>  |
| <span data-ttu-id="cf8f7-921">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-921">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-922">通道 DB/Retail Modern POS</span><span class="sxs-lookup"><span data-stu-id="cf8f7-922">Channel DB/Retail Modern POS</span></span>   |
| <span data-ttu-id="cf8f7-923">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-923">**Status**</span></span>                         | <span data-ttu-id="cf8f7-924">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-924">Removed as of Dynamics AX 7.0.</span></span>  |

### <a name="dutch-swift-mt940"></a><span data-ttu-id="cf8f7-925">荷兰 SWIFT MT940</span><span class="sxs-lookup"><span data-stu-id="cf8f7-925">Dutch SWIFT MT940</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-926">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-926">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-927">现在使用的是通用功能，而不是本地化功能。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-927">Generic functionality is now used instead of localized functionality.</span></span>                    |
| <span data-ttu-id="cf8f7-928">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-928">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-929">是，此功能已被高级银行对帐功能取代。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-929">Yes, this functionality has been replaced by Advanced bank reconciliation functionality.</span></span> |
| <span data-ttu-id="cf8f7-930">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-930">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-931">所有模块</span><span class="sxs-lookup"><span data-stu-id="cf8f7-931">All modules</span></span>                                                                              |
| <span data-ttu-id="cf8f7-932">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-932">**Status**</span></span>                         | <span data-ttu-id="cf8f7-933">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-933">Deprecated: A removal date has not been set for this feature.</span></span>                           |

### <a name="ebilanz-xbrl-for-germany"></a><span data-ttu-id="cf8f7-934">eBilanz（针对德国的 XBRL）</span><span class="sxs-lookup"><span data-stu-id="cf8f7-934">eBilanz (XBRL for Germany)</span></span>

<span data-ttu-id="cf8f7-935">此功能专门针对德国 eBilanz 分类提供了可扩展业务报告语言 (XBRL) 输出。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-935">This functionality provided eXtensible Business Reporting Language (XBRL) output that is intended specifically for the German eBilanz taxonomy.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-936">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-936">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-937">缺少客户使用</span><span class="sxs-lookup"><span data-stu-id="cf8f7-937">Lack of customer usage</span></span>  |
| <span data-ttu-id="cf8f7-938">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-938">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-939">此功能尚未被另一个功能取代，不过，多个提供丰富 XBRL 功能的专用 XBRL 程序包对德国市场可用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-939">This feature hasn't been replaced by another feature, but multiple specialized XBRL packages that provide rich XBRL functionality are available for the German market.</span></span> |
| <span data-ttu-id="cf8f7-940">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-940">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-941">Management Reporter</span><span class="sxs-lookup"><span data-stu-id="cf8f7-941">Management Reporter</span></span>      |
| <span data-ttu-id="cf8f7-942">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-942">**Status**</span></span>                         | <span data-ttu-id="cf8f7-943">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-943">Deprecated: A removal date has not been set for this feature.</span></span>  |

### <a name="enterprise-portal-client"></a><span data-ttu-id="cf8f7-944">企业门户客户端</span><span class="sxs-lookup"><span data-stu-id="cf8f7-944">Enterprise Portal client</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-945">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-945">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-946">提供了一个客户端平台。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-946">A single client platform has been provided.</span></span>  |
| <span data-ttu-id="cf8f7-947">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-947">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-948">新的 Web 客户端基于已经过修改可提供丰富 Web 平台的桌面窗体元数据和编程模型。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-948">The new web client is based on the desktop form metadata and programming model that have been modified to provide a rich web platform.</span></span> |
| <span data-ttu-id="cf8f7-949">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-949">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-950">所有模块</span><span class="sxs-lookup"><span data-stu-id="cf8f7-950">All modules</span></span>  |
| <span data-ttu-id="cf8f7-951">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-951">**Status**</span></span>                         | <span data-ttu-id="cf8f7-952">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-952">Removed as of Dynamics AX 7.0.</span></span>   |

### <a name="environmental-sustainability"></a><span data-ttu-id="cf8f7-953">环境可持续性</span><span class="sxs-lookup"><span data-stu-id="cf8f7-953">Environmental sustainability</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-954">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-954">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-955">低客户使用率和有限功能集</span><span class="sxs-lookup"><span data-stu-id="cf8f7-955">Low customer usage and a limited feature set</span></span>  |
| <span data-ttu-id="cf8f7-956">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-956">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-957">无</span><span class="sxs-lookup"><span data-stu-id="cf8f7-957">No</span></span>              |
| <span data-ttu-id="cf8f7-958">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-958">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-959">遵从性和内部控制、应付账款</span><span class="sxs-lookup"><span data-stu-id="cf8f7-959">Compliance and internal controls, Accounts payable</span></span>  |
| <span data-ttu-id="cf8f7-960">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-960">**Status**</span></span>                         | <span data-ttu-id="cf8f7-961">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-961">Removed as of Dynamics AX 7.0.</span></span> |

### <a name="form-activex-and-managed-host-controls"></a><span data-ttu-id="cf8f7-962">窗体 ActiveX 和托管主机控件</span><span class="sxs-lookup"><span data-stu-id="cf8f7-962">Form ActiveX and Managed Host controls</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-963">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-963">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-964">ActiveX 和托管主机控件基于已废弃的桌面客户端。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-964">The ActiveX and Managed Host controls are based on the deprecated desktop client.</span></span> |
| <span data-ttu-id="cf8f7-965">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-965">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-966">可扩展控件框架支持构建新的基于 HTML、CSS 和 JavaScript 的控件，并且是 Microsoft Visual Studio 工具环境中的一流控件。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-966">The extensible control framework supports building new controls that are based on HTML, CSS, and JavaScript, and is a first-class control in the Microsoft Visual Studio Tooling environment.</span></span> |
| <span data-ttu-id="cf8f7-967">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-967">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-968">所有模块</span><span class="sxs-lookup"><span data-stu-id="cf8f7-968">All modules</span></span>     |
| <span data-ttu-id="cf8f7-969">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-969">**Status**</span></span>                         | <span data-ttu-id="cf8f7-970">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-970">Removed as of Dynamics AX 7.0.</span></span>       |

### <a name="generate-prenotes-by-using-a-batch"></a><span data-ttu-id="cf8f7-971">通过使用批处理生成预验证</span><span class="sxs-lookup"><span data-stu-id="cf8f7-971">Generate prenotes by using a batch</span></span>

<span data-ttu-id="cf8f7-972">预验证生成无法通过使用批处理完成，但仍可以由用户完成。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-972">Prenote generation can't be done by using a batch, but it can still be done by a user.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-973">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-973">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-974">在通过使用批处理生成预验证文件时，没有窗体持续存在并且显示生成的预验证文件。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-974">No form exists to persist and display the resulting prenote file when it's generated by using a batch.</span></span> |
| <span data-ttu-id="cf8f7-975">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-975">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-976">预验证仍可以生成，并且用户能够控制该文件的保存位置。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-976">Prenotes can still be generated, and the user has control over the location where the file is saved.</span></span>   |
| <span data-ttu-id="cf8f7-977">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-977">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-978">应付账款、应收账款、现金和银行管理</span><span class="sxs-lookup"><span data-stu-id="cf8f7-978">Accounts payable, Accounts receivable, Cash and bank management</span></span>  |
| <span data-ttu-id="cf8f7-979">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-979">**Status**</span></span>                         | <span data-ttu-id="cf8f7-980">从 AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-980">Removed as of AX 7.0.</span></span>    |

### <a name="german-dtaus-payment-export-and-account-statement-import-totals-and-transactions"></a><span data-ttu-id="cf8f7-981">德国 DTAUS 付款导出和帐户对账单导入（合计和交易记录）</span><span class="sxs-lookup"><span data-stu-id="cf8f7-981">German DTAUS payment export and account statement import (totals and transactions)</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-982">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-982">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-983">该格式不再适用于德国，因为它已被单一欧元支付区 (SEPA) 功能取代。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-983">The format is no longer applicable in Germany, because it has been replaced by Single Euro Payments Area (SEPA) functionality.</span></span>                    |
| <span data-ttu-id="cf8f7-984">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-984">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-985">是，此功能已被 SEPA 付款导出和高级银行对帐功能（用于导入帐户对账单）取代。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-985">Yes, this functionality has been replaced by SEPA payment export and advanced bank reconciliation functionality for importing account statements.</span></span> |
| <span data-ttu-id="cf8f7-986">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-986">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-987">所有模块</span><span class="sxs-lookup"><span data-stu-id="cf8f7-987">All modules</span></span>  |
| <span data-ttu-id="cf8f7-988">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-988">**Status**</span></span>                         | <span data-ttu-id="cf8f7-989">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-989">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="german-dtazv-payment-format"></a><span data-ttu-id="cf8f7-990">德国 DTAZV 付款格式</span><span class="sxs-lookup"><span data-stu-id="cf8f7-990">German DTAZV payment format</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-991">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-991">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-992">该格式不再适用于德国，因为它已被 SEPA 功能取代。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-992">The format is no longer applicable in Germany, because it has been replaced by SEPA functionality.</span></span> |
| <span data-ttu-id="cf8f7-993">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-993">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-994">SEPA 付款导出</span><span class="sxs-lookup"><span data-stu-id="cf8f7-994">SEPA payments export</span></span>    |
| <span data-ttu-id="cf8f7-995">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-995">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-996">所有模块</span><span class="sxs-lookup"><span data-stu-id="cf8f7-996">All modules</span></span>   |
| <span data-ttu-id="cf8f7-997">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-997">**Status**</span></span>                         | <span data-ttu-id="cf8f7-998">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-998">Deprecated: A removal date has not been set for this feature.</span></span>    |

### <a name="german-mt940-import"></a><span data-ttu-id="cf8f7-999">德国 MT940 导入</span><span class="sxs-lookup"><span data-stu-id="cf8f7-999">German MT940 import</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-1000">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1000">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-1001">现在使用的是通用功能，而不是本地化功能。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1001">Generic functionality is now used instead of localized functionality.</span></span>                    |
| <span data-ttu-id="cf8f7-1002">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1002">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-1003">是，此功能已被高级银行对帐功能取代。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1003">Yes, this functionality has been replaced by Advanced bank reconciliation functionality.</span></span> |
| <span data-ttu-id="cf8f7-1004">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1004">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-1005">所有模块</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1005">All modules</span></span>                                                                              |
| <span data-ttu-id="cf8f7-1006">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1006">**Status**</span></span>                         | <span data-ttu-id="cf8f7-1007">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1007">Deprecated: A removal date has not been set for this feature.</span></span>                           |

### <a name="german-xml-eu-sales-list"></a><span data-ttu-id="cf8f7-1008">德国 XML 欧盟销售清单</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1008">German XML EU Sales list</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-1009">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1009">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-1010">不再支持德国欧盟销售清单报表的 XML 格式。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1010">The XML format for German EU Sales List reporting is no longer supported.</span></span> <span data-ttu-id="cf8f7-1011">仅 ELMA5 文本文件格式可用于将欧盟销售清单报表提交给德国税务局。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1011">Only the ELMA5 text file format can be used to submit the EU Sales List report to the German Tax Office.</span></span> |
| <span data-ttu-id="cf8f7-1012">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1012">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-1013">无</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1013">No</span></span>         |
| <span data-ttu-id="cf8f7-1014">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1014">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-1015">税金</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1015">Tax</span></span>        |
| <span data-ttu-id="cf8f7-1016">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1016">**Status**</span></span>                         | <span data-ttu-id="cf8f7-1017">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1017">Deprecated: A removal date has not been set for this feature.</span></span>   |

### <a name="gl-ssrs-reports"></a><span data-ttu-id="cf8f7-1018">GL SSRS 报表</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1018">GL SSRS reports</span></span>

<span data-ttu-id="cf8f7-1019">包括以下菜单项的报表已被删除：**试算平衡表(汇总)**、**试算平衡表(明细)**、**会计科目表**、**审计线索**、**余额**和**余额表**。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1019">Reports that include the following menu items have been removed: **Summary trial balance**, **Detailed trial balance**, **Chart of accounts**, **Audit trail**, **Balances**, and **Balance list**.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-1020">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1020">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-1021">财务 Microsoft SQL Server Reporting Services (SSRS) 报表已经被 Management Reporter 功能和默认报表取代。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1021">Financial Microsoft SQL Server Reporting Services (SSRS) reports have been replaced by Management Reporter capabilities and default reports.</span></span> |
| <span data-ttu-id="cf8f7-1022">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1022">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-1023">Management Reporter（在 Dynamics AX 的当前版本中标记为**财务报告**。）</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1023">Management Reporter (labeled **Financial reporting** in the current version of Dynamics AX)</span></span>    |
| <span data-ttu-id="cf8f7-1024">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1024">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-1025">总帐</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1025">General ledger</span></span>   |
| <span data-ttu-id="cf8f7-1026">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1026">**Status**</span></span>                         | <span data-ttu-id="cf8f7-1027">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1027">Removed as of Dynamics AX 7.0.</span></span>   |

### <a name="infopart-and-formpart-metadata"></a><span data-ttu-id="cf8f7-1028">InfoPart 和 FormPart 元数据</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1028">InfoPart and FormPart metadata</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-1029">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1029">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-1030">InfoPart 和 FormPart 元数据支持为两个不同的客户端创建 FactBox。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1030">InfoPart and FormPart metadata enabled the creation of FactBoxes for two different clients.</span></span> |
| <span data-ttu-id="cf8f7-1031">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1031">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-1032">InfoPart 元数据，是一种简化的窗体定义，由升级工具转换为窗体。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1032">InfoPart metadata, which was a simplified form definition, is converted into a Form by upgrade tooling.</span></span> <span data-ttu-id="cf8f7-1033">引用窗体的 FormPart 元数据已被升级工具所创建的更直接引用取代。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1033">FormPart metadata, which referenced a Form, is replaced by a more direct reference that is created by upgrade tooling.</span></span> |
| <span data-ttu-id="cf8f7-1034">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1034">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-1035">所有模块</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1035">All modules</span></span>    |
| <span data-ttu-id="cf8f7-1036">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1036">**Status**</span></span>                         | <span data-ttu-id="cf8f7-1037">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1037">Removed as of Dynamics AX 7.0.</span></span>        |

### <a name="main-account-list-page"></a><span data-ttu-id="cf8f7-1038">主科目列表页</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1038">Main account list page</span></span>

<span data-ttu-id="cf8f7-1039">法人的帐户列表和相关余额信息</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1039">A list of accounts for the legal entity and related balance information</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-1040">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1040">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-1041">余额信息现在在**试算余额表**列表页上按帐户和维度提供。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1041">Balance information is available on the **Trial balance** list page by account and dimension.</span></span>  |
| <span data-ttu-id="cf8f7-1042">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1042">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-1043">**主科目**包含**主科目**列表页所包含的相同科目列表。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1043">**Main accounts** contains the same list of accounts that the **Main account** list page contained.</span></span> <span data-ttu-id="cf8f7-1044">**主科目**中的网格视图还显示一个更小的、如网格般的视图。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1044">The grid view in **Main accounts** also shows an even smaller, grid-like view.</span></span> |
| <span data-ttu-id="cf8f7-1045">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1045">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-1046">总帐</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1046">General ledger</span></span>      |
| <span data-ttu-id="cf8f7-1047">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1047">**Status**</span></span>                         | <span data-ttu-id="cf8f7-1048">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1048">Removed as of Dynamics AX 7.0.</span></span>    |

### <a name="malaysia-and-singapore-bank-cash-flow-report"></a><span data-ttu-id="cf8f7-1049">马来西亚和新加坡银行现金流量报表</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1049">Malaysia and Singapore bank cash flow report</span></span>

<span data-ttu-id="cf8f7-1050">此功能能让用户打印现金流量报表，以显示特定日期范围或所选银行帐户的现金流入量和流出量的交易记录和详细信息。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1050">This feature let the user print a cash flow report that shows transactions and details of the cash inflows and outflows for a specific date range for selected bank accounts.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-1051">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1051">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-1052">同样的信息可以从查询银行交易记录中获得。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1052">The same information can be obtained from the Inquiry bank transaction.</span></span> |
| <span data-ttu-id="cf8f7-1053">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1053">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-1054">查询银行交易记录</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1054">The Inquiry bank transaction</span></span>                                            |
| <span data-ttu-id="cf8f7-1055">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1055">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-1056">现金和银行管理</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1056">Cash and bank management</span></span>                                                |
| <span data-ttu-id="cf8f7-1057">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1057">**Status**</span></span>                         | <span data-ttu-id="cf8f7-1058">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1058">Deprecated: A removal date has not been set for this feature.</span></span>          |

### <a name="mexican-cfd-electronic-invoice"></a><span data-ttu-id="cf8f7-1059">墨西哥 CFD 电子发票</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1059">Mexican CFD electronic invoice</span></span>

<span data-ttu-id="cf8f7-1060">此功能支持通过使用 Comprobante Fiscal Digital (CFD) 方法生成墨西哥电子发票，在该方法中公司通过请求来自政府的相关主管机构签署发票。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1060">This feature enabled the generation of Mexican electronic invoices by using the Comprobante Fiscal Digital (CFD) method, where the company signs the invoice by requesting the related authorization from the government.</span></span> <span data-ttu-id="cf8f7-1061">此功能还提供一个每月报表，其包括在该期间签发的所有电子发票。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1061">This feature also provides a monthly report that includes all electronics invoices that were issued in the period.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-1062">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1062">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-1063">此方法不再适用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1063">The method is no longer applicable.</span></span> <span data-ttu-id="cf8f7-1064">通过使用 CFD 方法生成电子发票已被税务主管机构废弃，并已被 Comprobante Fiscal Digital a través de Internet (CFDI) 方法取代，在该方法中签名委托给第三方提供商 (PAC)。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1064">The generation of electronic invoices by using the CFD method was deprecated by the tax authorities and replaced by the Comprobante Fiscal Digital a través de Internet (CFDI) method, where the signing is delegated to the third-party provider (PAC).</span></span> <span data-ttu-id="cf8f7-1065">删除了每月报表，并且，查询选项能让用户查询历史交易记录。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1065">The monthly report has been removed, and an inquiry option lets users inquire about historical transactions.</span></span> |
| <span data-ttu-id="cf8f7-1066">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1066">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-1067">无</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1067">No</span></span>    |
| <span data-ttu-id="cf8f7-1068">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1068">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-1069">应收账款、项目</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1069">Account receivables, Project</span></span>   |
| <span data-ttu-id="cf8f7-1070">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1070">**Status**</span></span>                         | <span data-ttu-id="cf8f7-1071">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1071">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="mexico-realized-and-unrealized-vat"></a><span data-ttu-id="cf8f7-1072">墨西哥实现和未实现的增值税</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1072">Mexico realized and unrealized VAT</span></span>

<span data-ttu-id="cf8f7-1073">Microsoft Dynamics AX 2012 通过使用“未实现的增值税”的墨西哥特定功能管理未实现的增值税 (VAT)。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1073">Microsoft Dynamics AX 2012 managed unrealized value-added tax (VAT) by using Mexico-specific functionality for unrealized tax.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-1074">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1074">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-1075">重复的功能</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1075">Duplicate functionality</span></span>  |
| <span data-ttu-id="cf8f7-1076">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1076">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-1077">是，此功能已被使用核心提供的标准特定销售增值税功能取代。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1077">Yes, this functionality has been replaced by standard conditional sales tax functionality that is provided by Core.</span></span> |
| <span data-ttu-id="cf8f7-1078">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1078">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-1079">税金</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1079">Tax</span></span>   |
| <span data-ttu-id="cf8f7-1080">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1080">**Status**</span></span>                         | <span data-ttu-id="cf8f7-1081">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1081">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="microsoft-outlook-integration"></a><span data-ttu-id="cf8f7-1082">Microsoft Outlook 集成</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1082">Microsoft Outlook integration</span></span>


|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-1083">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1083">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-1084">此功能已由 Microsoft Exchange Server 集成替换。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1084">This functionality has been replaced by Microsoft Exchange Server integration.</span></span> |
| <span data-ttu-id="cf8f7-1085">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1085">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-1086">是</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1086">Yes</span></span>                                                                            |
| <span data-ttu-id="cf8f7-1087">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1087">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-1088">销售和市场营销</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1088">Sales and marketing</span></span>                                                            |
| <span data-ttu-id="cf8f7-1089">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1089">**Status**</span></span>                         | <span data-ttu-id="cf8f7-1090">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1090">Removed as of Dynamics AX 7.0.</span></span>                                                 |

### <a name="private-blocking-of-inventory-and-warehouse-management-journals"></a><span data-ttu-id="cf8f7-1091">库存和仓库管理日记帐的专用锁定</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1091">Private blocking of inventory and warehouse management journals</span></span>

<span data-ttu-id="cf8f7-1092">库存和仓库日记帐不再支持针对所选用户将日记帐标记为专用的功能。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1092">The inventory and warehouse journals no longer support the ability to mark a journal as private for a selected user.</span></span> <span data-ttu-id="cf8f7-1093">仅支持针对用户组将日记帐锁定为专用和在编辑期间锁定的流程。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1093">Only the process of blocking journals as private for user groups and blocking during editing is supported.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-1094">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1094">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-1095">找不到该功能的使用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1095">No use of the functionality was found.</span></span> |
| <span data-ttu-id="cf8f7-1096">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1096">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-1097">无</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1097">No</span></span>                                     |
| <span data-ttu-id="cf8f7-1098">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1098">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-1099">库存管理</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1099">Inventory management</span></span>                   |
| <span data-ttu-id="cf8f7-1100">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1100">**Status**</span></span>                         | <span data-ttu-id="cf8f7-1101">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1101">Removed as of Dynamics AX 7.0.</span></span>         |

### <a name="product-builder"></a><span data-ttu-id="cf8f7-1102">产品生成器</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1102">Product builder</span></span>

<span data-ttu-id="cf8f7-1103">产品生成器用于从销售订单、采购订单、生产订单、销售报价单、项目报价单或物料需求动态配置物料。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1103">Product builder was used to dynamically configure items from a sales order, purchase order, production order, sales quotation, project quotation, or item requirement.</span></span> <span data-ttu-id="cf8f7-1104">基于具有建模变量的产品模型，用户可以选择值以满足用户需求并获取具有物料清单和工艺路线的唯一产品变型。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1104">Based on a product model that had modeling variables, the user could select values to meet the customer requirements and get a unique product variant that had a BOM and route.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-1105">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1105">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-1106">产品生成器向最终用户显示了 X++ 代码，在 Dynamics AX 的当前版本中不受支持。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1106">Product builder exposed X++ code to end users and isn't supported in the current version of Dynamics AX.</span></span> <span data-ttu-id="cf8f7-1107">它已被删除，从而避免在重叠的、庞大的代码库中进行重复的维护工作。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1107">It has been removed to avoid duplicate maintenance efforts on overlapping, sizeable codebases.</span></span>  |
| <span data-ttu-id="cf8f7-1108">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1108">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-1109">是。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1109">Yes.</span></span> <span data-ttu-id="cf8f7-1110">已经公布在将来的版本中弃用产品生成器的 Dynamics AX 2012 中引入了基于约束的配置。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1110">The constraint-based configuration was introduced in Dynamics AX 2012 where the depreciation of Product builder in future versions was already announced.</span></span> <span data-ttu-id="cf8f7-1111">在基础产品上选择基于约束的配置技术，以启用配置。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1111">The constraint-based configuration technology is selected on the product masters to enable the configuration.</span></span> <span data-ttu-id="cf8f7-1112">若要了解更多信息，请参阅[生成产品配置模型](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/pim/build-product-configuration-model)。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1112">To learn more, see [Build a product configuration model](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/pim/build-product-configuration-model).</span></span> |
| <span data-ttu-id="cf8f7-1113">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1113">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-1114">产品信息管理、销售和市场营销</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1114">Product information management, Sales and marketing</span></span>  |
| <span data-ttu-id="cf8f7-1115">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1115">**Status**</span></span>                         | <span data-ttu-id="cf8f7-1116">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1116">Removed as of Dynamics AX 7.0.</span></span>      |

### <a name="production-floor-app"></a><span data-ttu-id="cf8f7-1117">生产车间应用</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1117">Production Floor app</span></span>
<span data-ttu-id="cf8f7-1118">这是适用于运行 Windows 8.1 RT 和 Windows 8.1 Pro 的平板设备的应用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1118">This is the app for tablet devices running Windows 8.1 RT and Windows 8.1 Pro.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-1119">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1119">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-1120">通过对基于 Web 的客户端的更改，可以通过本机 Dynamics AX 7.0 客户端提供类似的功能。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1120">With the change to a web-based client, it is possible to deliver similar functionality through the native Dynamics AX 7.0 client.</span></span> <span data-ttu-id="cf8f7-1121">作业卡设备提供为触摸和平板窗体因子优化的生产车间用户界面。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1121">The Job Card Device provides a production floor user interface that is optimized for touch and tablet form factors.</span></span> |
| <span data-ttu-id="cf8f7-1122">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1122">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-1123">是。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1123">Yes.</span></span> <span data-ttu-id="cf8f7-1124">作业卡设备是 Dynamics AX 7.0 的一个本机部分。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1124">The Job Card Device, which is a native part of Dynamics AX 7.0.</span></span>                                                                           |
| <span data-ttu-id="cf8f7-1125">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1125">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-1126">生产控制</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1126">Production control</span></span>                                                |
| <span data-ttu-id="cf8f7-1127">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1127">**Status**</span></span>                         | <span data-ttu-id="cf8f7-1128">已弃用：从 Microsoft Store 的删除日期尚未为此功能设置。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1128">Deprecated: A removal date from the Microsoft store has not yet been set for this feature.</span></span>                                                |


### <a name="rename-product-dimension"></a><span data-ttu-id="cf8f7-1129">重命名产品维度</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1129">Rename product dimension</span></span>

<span data-ttu-id="cf8f7-1130">此功能能让您将三个标准维度（大小、颜色或样式）之一的名称更改为一个更好地满足您的业务需求的名称。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1130">This feature let you change the name of one of the three standard product dimensions (size, color, or style) to a name that better suited your business requirements.</span></span> <span data-ttu-id="cf8f7-1131">重命名包括其中使用了产品维度名称的所有标签。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1131">Renaming included all the labels where the product dimension name was used.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-1132">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1132">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-1133">Dynamics AX 的当前版本在运行时不支持标签。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1133">The current version of Dynamics AX doesn't support label changes at run time.</span></span> |
| <span data-ttu-id="cf8f7-1134">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1134">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-1135">无</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1135">No</span></span>                                                                            |
| <span data-ttu-id="cf8f7-1136">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1136">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-1137">产品信息管理</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1137">Product information management</span></span>                                                |
| <span data-ttu-id="cf8f7-1138">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1138">**Status**</span></span>                         | <span data-ttu-id="cf8f7-1139">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1139">Removed as of Dynamics AX 7.0.</span></span>                                                |

### <a name="retail-server-connectivity-using-http"></a><span data-ttu-id="cf8f7-1140">使用 HTTP 的零售服务器连接</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1140">Retail Server connectivity using HTTP</span></span>

<span data-ttu-id="cf8f7-1141">在 Dynamics AX 2012 R3 中，零售服务器可以使用 HTTP 通信（不受安全保护）运行。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1141">In Dynamics AX 2012 R3, the Retail Server could function using HTTP communication (non-secured).</span></span> <span data-ttu-id="cf8f7-1142">这是除使用 HTTPS 的标准通信之外的方法。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1142">This was in addition to the standard communication using HTTPS.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-1143">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1143">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-1144">因为新的安全要求，现在只支持使用 TLS 1.2（或更高版本，如果可用）的安全通信。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1144">Due to new security requirements, only secured communication using TLS 1.2 (or above, as available) is now supported.</span></span> <span data-ttu-id="cf8f7-1145">自助服务安装程序将自动配置此通信的计算机。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1145">The self-service installer will automatically configure the computer for this communication.</span></span> |
| <span data-ttu-id="cf8f7-1146">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1146">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-1147">编号</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1147">No.</span></span> <span data-ttu-id="cf8f7-1148">现在只支持标准 HTTPS 通信。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1148">Only standard HTTPS communication is now supported.</span></span> |
| <span data-ttu-id="cf8f7-1149">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1149">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-1150">零售服务器</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1150">Retail Server</span></span>  |
| <span data-ttu-id="cf8f7-1151">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1151">**Status**</span></span>                         | <span data-ttu-id="cf8f7-1152">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1152">Removed as of Dynamics AX 7.0.</span></span> |

### <a name="role-center-pages"></a><span data-ttu-id="cf8f7-1153">角色中心页</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1153">Role Center pages</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-1154">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1154">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-1155">角色中心页基于已废弃的企业门户平台而构建，该平台已被 Dynamics AX 的当前版本中的新 Web 客户端平台取代。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1155">Role Center pages were built on the deprecated Enterprise Portal platform, which has been replaced by the new web client platform in the current version of Dynamics AX.</span></span> |
| <span data-ttu-id="cf8f7-1156">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1156">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-1157">新工作区窗体模式为用户提供一个以流程为中心的设计，从而便于访问该流程中的常用任务。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1157">The new Workspace form pattern provides users with a process-centered design that provides easy access to commonly used tasks within that process.</span></span>                       |
| <span data-ttu-id="cf8f7-1158">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1158">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-1159">所有模块</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1159">All modules</span></span>    |
| <span data-ttu-id="cf8f7-1160">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1160">**Status**</span></span>                         | <span data-ttu-id="cf8f7-1161">从 Dynamics AX 7.0 开始移除</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1161">Removed as of Dynamics AX 7.0</span></span>   |

### <a name="sales-tax-jurisdictions"></a><span data-ttu-id="cf8f7-1162">销售税区域</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1162">Sales tax jurisdictions</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-1163">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1163">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-1164">低客户使用率和有限功能集</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1164">Low customer usage and a limited feature set</span></span> |
| <span data-ttu-id="cf8f7-1165">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1165">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-1166">无</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1166">No</span></span>                                           |
| <span data-ttu-id="cf8f7-1167">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1167">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-1168">美国销售税</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1168">US sales tax</span></span>                                 |
| <span data-ttu-id="cf8f7-1169">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1169">**Status**</span></span>                         | <span data-ttu-id="cf8f7-1170">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1170">Removed as of Dynamics AX 7.0.</span></span>               |

### <a name="sites-services"></a><span data-ttu-id="cf8f7-1171">站点服务</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1171">Sites Services</span></span>

<span data-ttu-id="cf8f7-1172">站点服务允许您构建将您的业务流程扩展到 Internet 的网站，而无需 IT 支持。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1172">Sites Services let you build websites that extend your business processes to the Internet without IT support.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-1173">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1173">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-1174">Dynamics AX 的 Microsoft Azure 基础结构具有可以使用的新功能（例如，Azure 站点）。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1174">The Microsoft Azure infrastructure that is used by Dynamics AX has new capabilities that can be used instead (for example, Azure sites).</span></span> |
| <span data-ttu-id="cf8f7-1175">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1175">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-1176">无</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1176">No</span></span>   |
| <span data-ttu-id="cf8f7-1177">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1177">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-1178">人力资源招聘、案例管理、询价、供应商注册、机会和市场活动协作工作区</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1178">HR recruiting, Case management, Request for quotes, Vendor registration, Collaborative workspaces for opportunities and campaigns</span></span>  |
| <span data-ttu-id="cf8f7-1179">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1179">**Status**</span></span>                         | <span data-ttu-id="cf8f7-1180">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1180">Removed as of Dynamics AX 7.0.</span></span>    |

### <a name="ssas-demand-forecasting-strategy"></a><span data-ttu-id="cf8f7-1181">SSAS 需求预测策略</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1181">SSAS demand forecasting strategy</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-1182">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1182">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-1183">新的云体系结构中不支持设计此功能。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1183">The design of the feature cannot be supported in the new cloud architecture.</span></span> |
| <span data-ttu-id="cf8f7-1184">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1184">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-1185">Azure 机器学习需求预测策略</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1185">Azure Machine Learning demand forecasting strategy</span></span>                           |
| <span data-ttu-id="cf8f7-1186">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1186">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-1187">主计划</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1187">Master planning</span></span>                                                              |
| <span data-ttu-id="cf8f7-1188">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1188">**Status**</span></span>                         | <span data-ttu-id="cf8f7-1189">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1189">Removed as of Dynamics AX 7.0.</span></span>                                               |

### <a name="vendor-invoice-pool-excluding-posting-details"></a><span data-ttu-id="cf8f7-1190">供应商发票池(不包括过帐)详细信息</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1190">Vendor invoice pool excluding posting details</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-1191">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1191">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-1192">低使用率。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1192">Low usage.</span></span> <span data-ttu-id="cf8f7-1193">此功能已被具有工作流功能的发票日记帐取代。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1193">This functionality has been replaced by the Invoice journal that has workflow functionality.</span></span> |
| <span data-ttu-id="cf8f7-1194">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1194">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-1195">发票日记帐的工作流功能。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1195">Workflow capabilities of the Invoice journal.</span></span>     |
| <span data-ttu-id="cf8f7-1196">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1196">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-1197">应付帐款</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1197">Accounts payable</span></span> |
| <span data-ttu-id="cf8f7-1198">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1198">**Status**</span></span>                         | <span data-ttu-id="cf8f7-1199">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1199">Removed as of Dynamics AX 7.0.</span></span>    |


### <a name="virtual-company-accounts"></a><span data-ttu-id="cf8f7-1200">虚拟公司帐户</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1200">Virtual company accounts</span></span>

<span data-ttu-id="cf8f7-1201">Dynamics AX 中不再支持虚拟公司功能。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1201">The virtual companies feature is no longer supported in Dynamics AX.</span></span> <span data-ttu-id="cf8f7-1202">虚拟公司功能允许用户设置可以由一组公司共享的表。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1202">The virtual companies feature let users set up tables that could be shared by a set of companies.</span></span> <span data-ttu-id="cf8f7-1203">有关该功能的描述，请参阅[公司帐户和虚拟公司帐户](https://msdn.microsoft.com/en-us/library/aa834382(v=ax.10).aspx)。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1203">For a description of the feature, see [Company accounts and Virtual company accounts](https://msdn.microsoft.com/en-us/library/aa834382(v=ax.10).aspx).</span></span> <span data-ttu-id="cf8f7-1204">该功能的工作原理是将表分组到集合，然后集合分配给虚拟公司，即现有的“实际”公司的组。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1204">The feature works by grouping tables into collections that are assigned to virtual companies, which are groups of existing “real” companies.</span></span> <span data-ttu-id="cf8f7-1205">创建查询，以便虚拟公司中的所有公司可以访问关联表集合的表中的数据。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1205">Queries are created so that all the companies in the virtual company can access the data in the tables of the associated table collections.</span></span>

|   |  | 
|------------|--------------------|
| <span data-ttu-id="cf8f7-1206">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1206">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-1207">- 将数据存储在表中之前，必须先设置虚拟公司。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1207">- Virtual companies must be set up before data is stored in the tables.</span></span> <span data-ttu-id="cf8f7-1208">将虚拟公司更新到现有实施上是很困难的。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1208">Retrofitting virtual companies onto an existing implementation is very difficult.</span></span><br><br><span data-ttu-id="cf8f7-1209">- 由于 Dynamics AX 的当前版本中有如此多数据标准化，要了解将什么添加到表集合将会很困难。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1209">- Because there has been so much data normalization in the current version of Dynamics AX, it has become difficult to know what to add to the table collections.</span></span> <span data-ttu-id="cf8f7-1210">例如，要知道共享哪些表很难。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1210">For example, it's difficult to know which tables to share.</span></span> <span data-ttu-id="cf8f7-1211">还必须添加从虚拟公司中的表引用的所有表。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1211">All the tables referenced from tables that are in a virtual company must also added.</span></span> <span data-ttu-id="cf8f7-1212">由于表标准化，即使遍布许多表中的简单主数据也必须是虚拟公司的一部分。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1212">Because of table normalization, even simple master data that is spread across multiple tables must be part of the virtual company.</span></span> <span data-ttu-id="cf8f7-1213">此处所犯的任何错误都将导致功能问题。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1213">Any mistake that is made here will cause functional issues.</span></span><br><br><span data-ttu-id="cf8f7-1214">- 当表是虚拟公司的一部分时，它会丢失有关数据来源的信息，并且只记录虚拟公司。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1214">- When a table is part of a virtual company, it loses information about the origin of the data, and only the virtual company is recorded.</span></span>   |
| <span data-ttu-id="cf8f7-1215">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1215">**Replaced by another feature?**</span></span> | <span data-ttu-id="cf8f7-1216">全局表可用于使表可从所有公司访问到。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1216">Global tables can be used to make tables accessible from all companies.</span></span> <span data-ttu-id="cf8f7-1217">当前不替换。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1217">Currently, there is no replacement.</span></span> |   
| <span data-ttu-id="cf8f7-1218">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1218">**Product areas affected**</span></span>       | <span data-ttu-id="cf8f7-1219">所有模块</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1219">All modules</span></span> |   
| <span data-ttu-id="cf8f7-1220">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1220">**Status**</span></span>                       | <span data-ttu-id="cf8f7-1221">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1221">Removed as of Dynamics AX 7.0.</span></span>   |   

### <a name="windows-8-tablet-app"></a><span data-ttu-id="cf8f7-1222">Windows 8 平板电脑应用</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1222">Windows 8 tablet app</span></span>

<span data-ttu-id="cf8f7-1223">Windows 8 平板电脑应用提供用于费用录入和审核的功能。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1223">The Windows 8 tablet app provided functionality for expense entry and approval.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-1224">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1224">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-1225">Finance and Operations 与平板电脑兼容。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1225">Finance and Operations is compatible with tablets.</span></span> <span data-ttu-id="cf8f7-1226">无需再使用平板电脑应用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1226">The tablet app is no longer required.</span></span>    |
| <span data-ttu-id="cf8f7-1227">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1227">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-1228">编号</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1228">No.</span></span>          |
| <span data-ttu-id="cf8f7-1229">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1229">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-1230">费用报销管理</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1230">Expense management</span></span>   |
| <span data-ttu-id="cf8f7-1231">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1231">**Status**</span></span>                         | <span data-ttu-id="cf8f7-1232">已移除：此功能仅对 Dynamics AX 2012 R3 可用。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1232">Removed: This functionality is only available for Dynamics AX 2012 R3.</span></span> |

### <a name="workplanner"></a><span data-ttu-id="cf8f7-1233">工作进度表</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1233">Workplanner</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="cf8f7-1234">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1234">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="cf8f7-1235">低使用率</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1235">Low usage</span></span> |
| <span data-ttu-id="cf8f7-1236">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1236">**Replaced by another feature?**</span></span>   | <span data-ttu-id="cf8f7-1237">否，但从**模板组**页打开的**模板关系**页支持与弃用的**工作进度表**页相同的业务方案。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1237">No, but the **Profile relation** page, which is opened from the **Profile groups** page, supports the same business scenario as the deprecated **Workplanner** page.</span></span> |
| <span data-ttu-id="cf8f7-1238">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1238">**Product areas affected**</span></span>         | <span data-ttu-id="cf8f7-1239">考勤管理</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1239">Time and attendance</span></span>     |
| <span data-ttu-id="cf8f7-1240">**状态**</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1240">**Status**</span></span>                         | <span data-ttu-id="cf8f7-1241">此代码尚未移除。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1241">The code has not been removed.</span></span> <span data-ttu-id="cf8f7-1242">但窗体 JmgWorkPlanner 未迁移。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1242">However, the form, JmgWorkPlanner, was not migrated.</span></span>    |

### <a name="x-financial-statements"></a><span data-ttu-id="cf8f7-1243">X++ 财务报表</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1243">X++ financial statements</span></span>

|                                                 |                                                                                                          |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf8f7-1244"><strong>弃用/移除的原因</strong></span><span class="sxs-lookup"><span data-stu-id="cf8f7-1244"><strong>Reason for deprecation/removal</strong></span></span> |                         <span data-ttu-id="cf8f7-1245">此功能已被另一个功能取代。</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1245">This functionality has been replaced by another feature.</span></span>                         |
|  <span data-ttu-id="cf8f7-1246"><strong>被另一个功能取代？</strong></span><span class="sxs-lookup"><span data-stu-id="cf8f7-1246"><strong>Replaced by another feature?</strong></span></span>  | <span data-ttu-id="cf8f7-1247">Management Reporter（在 Dynamics AX 的当前版本中标记为<strong>财务报告</strong>。）</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1247">Management Reporter (labeled <strong>Financial reporting</strong> in the current version of Dynamics AX)</span></span> |
|     <span data-ttu-id="cf8f7-1248"><strong>影响的产品区域</strong></span><span class="sxs-lookup"><span data-stu-id="cf8f7-1248"><strong>Product areas affected</strong></span></span>     |                                              <span data-ttu-id="cf8f7-1249">总帐</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1249">General ledger</span></span>                                              |
|             <span data-ttu-id="cf8f7-1250"><strong>状态</strong></span><span class="sxs-lookup"><span data-stu-id="cf8f7-1250"><strong>Status</strong></span></span>             |                                      <span data-ttu-id="cf8f7-1251">从 Dynamics AX 2012 开始移除</span><span class="sxs-lookup"><span data-stu-id="cf8f7-1251">Removed as of Dynamics AX 2012</span></span>                                      |



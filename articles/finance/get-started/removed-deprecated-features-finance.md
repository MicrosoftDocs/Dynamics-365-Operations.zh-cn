---
title: Dynamics 365 Finance 中已删除或弃用的功能
description: 本主题介绍 Dynamics 365 Finance 中已经删除或计划删除的功能。
author: roschlom
ms.date: 04/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: e6a391b10ddaef79e68f47afae7d77135a1c333a
ms.sourcegitcommit: cb282e8d2306ab71adf80a84346a6863d2d019e8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2021
ms.locfileid: "6184117"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a><span data-ttu-id="4340b-103">Dynamics 365 Finance 中已删除或弃用的功能</span><span class="sxs-lookup"><span data-stu-id="4340b-103">Removed or deprecated features in Dynamics 365 Finance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4340b-104">本主题介绍 Dynamics 365 Finance 中已经删除或计划删除的功能。</span><span class="sxs-lookup"><span data-stu-id="4340b-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Finance.</span></span>

- <span data-ttu-id="4340b-105">*已移除* 的功能在产品中不再可用。</span><span class="sxs-lookup"><span data-stu-id="4340b-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="4340b-106">*已弃用* 的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。</span><span class="sxs-lookup"><span data-stu-id="4340b-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="4340b-107">此列表旨在帮助您在您自己的计划中考虑这些功能的移除和弃用。</span><span class="sxs-lookup"><span data-stu-id="4340b-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="4340b-108">[技术参考报告](/dynamics/s-e/global/axtechrefrep_61)中提供了有关 Finance and Operations应用中的对象的详细信息。</span><span class="sxs-lookup"><span data-stu-id="4340b-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](/dynamics/s-e/global/axtechrefrep_61).</span></span> <span data-ttu-id="4340b-109">可比较这些报告的不同版本，以了解 Finance and Operations 应用各版本中已更改或已删除的对象。</span><span class="sxs-lookup"><span data-stu-id="4340b-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-finance-10020-release"></a><span data-ttu-id="4340b-110">Finance 10.0.20 版本中已经删除或弃用的功能</span><span class="sxs-lookup"><span data-stu-id="4340b-110">Features removed or deprecated in the Finance 10.0.20 release</span></span>

### <a name="rtir-query-invoice-data-request-hu-electronic-reporting-er-format-configuration"></a><span data-ttu-id="4340b-111">“RTIR 查询发票数据请求 (HU)”电子报告 (ER) 格式配置</span><span class="sxs-lookup"><span data-stu-id="4340b-111">"RTIR Query Invoice Data Request (HU)" Electronic reporting (ER) format configuration</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="4340b-112">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="4340b-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="4340b-113">从与匈牙利语在线开票系统互操作的电子消息处理中排除</span><span class="sxs-lookup"><span data-stu-id="4340b-113">Excluded from electronic messaging processing of interoperation with Hungarian online invoicing system</span></span> |
| <span data-ttu-id="4340b-114">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="4340b-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="4340b-115">无</span><span class="sxs-lookup"><span data-stu-id="4340b-115">No</span></span> |
| <span data-ttu-id="4340b-116">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="4340b-116">**Product areas affected**</span></span>         | <span data-ttu-id="4340b-117">申请</span><span class="sxs-lookup"><span data-stu-id="4340b-117">Application</span></span> |
| <span data-ttu-id="4340b-118">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="4340b-118">**Deployment option**</span></span>              | <span data-ttu-id="4340b-119">所有</span><span class="sxs-lookup"><span data-stu-id="4340b-119">All</span></span> |
| <span data-ttu-id="4340b-120">**状态**</span><span class="sxs-lookup"><span data-stu-id="4340b-120">**Status**</span></span>                         | <span data-ttu-id="4340b-121">已弃用：到 2022 年 4 月 15 日，我们计划不再支持“RTIR 查询发票数据请求 (HU)”格式配置。</span><span class="sxs-lookup"><span data-stu-id="4340b-121">Deprecated: By April 15, 2022, we plan to no longer support "RTIR Query Invoice Data Request (HU)" format configuration.</span></span> |

### <a name="french-fec-audit-file-electronic-reporting-er-format-for-france-under-german-audit-file-output-format"></a><span data-ttu-id="4340b-122">“德国审计文件输出”格式下的法国的“法国 FEC 审计文件”电子报告 (ER) 格式</span><span class="sxs-lookup"><span data-stu-id="4340b-122">"French FEC audit file" Electronic reporting (ER) format for France under "German audit file output" format</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="4340b-123">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="4340b-123">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="4340b-124">替换为新的“FEC 审计文件 (FR)”格式</span><span class="sxs-lookup"><span data-stu-id="4340b-124">Replaced with new "FEC audit file (FR)" format</span></span> |
| <span data-ttu-id="4340b-125">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="4340b-125">**Replaced by another feature?**</span></span>   | <span data-ttu-id="4340b-126">是</span><span class="sxs-lookup"><span data-stu-id="4340b-126">Yes</span></span> |
| <span data-ttu-id="4340b-127">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="4340b-127">**Product areas affected**</span></span>         | <span data-ttu-id="4340b-128">申请</span><span class="sxs-lookup"><span data-stu-id="4340b-128">Application</span></span> |
| <span data-ttu-id="4340b-129">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="4340b-129">**Deployment option**</span></span>              | <span data-ttu-id="4340b-130">所有</span><span class="sxs-lookup"><span data-stu-id="4340b-130">All</span></span> |
| <span data-ttu-id="4340b-131">**状态**</span><span class="sxs-lookup"><span data-stu-id="4340b-131">**Status**</span></span>                         | <span data-ttu-id="4340b-132">弃用：到 2022 年 5 月 1 日，我们计划不再支持“德国审计文件输出”格式下的法国的“法国 FEC 审计文件”电子报告 (ER) 格式。</span><span class="sxs-lookup"><span data-stu-id="4340b-132">Deprecated: by May 1, 2022, we plan to no longer support "French FEC audit file" Electronic reporting (ER) format for France under "German audit file output" format.</span></span> <span data-ttu-id="4340b-133">而是在“数据导出模型”下引入新的 FEC 审计文件 (FR) 格式。</span><span class="sxs-lookup"><span data-stu-id="4340b-133">New FEC audit file (FR) format is introduced instead under the "Data export model".</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-10017-release"></a><span data-ttu-id="4340b-134">Finance 10.0.17 版本中已经删除或弃用的功能</span><span class="sxs-lookup"><span data-stu-id="4340b-134">Features removed or deprecated in the Finance 10.0.17 release</span></span>

### <a name="lcs-repository-as-a-storage-option-for-electronic-reporting-configurations"></a><span data-ttu-id="4340b-135">作为电子报告配置的存储选项的 LCS 储存库</span><span class="sxs-lookup"><span data-stu-id="4340b-135">LCS repository as a storage option for Electronic reporting configurations</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="4340b-136">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="4340b-136">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="4340b-137">替换为新的监管配置服务 (RCS) 全局存储库</span><span class="sxs-lookup"><span data-stu-id="4340b-137">Replaced with the new Regulatory Configuration Service (RCS) Global repository</span></span> |
| <span data-ttu-id="4340b-138">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="4340b-138">**Replaced by another feature?**</span></span>   | <span data-ttu-id="4340b-139">是</span><span class="sxs-lookup"><span data-stu-id="4340b-139">Yes</span></span> |
| <span data-ttu-id="4340b-140">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="4340b-140">**Product areas affected**</span></span>         | <span data-ttu-id="4340b-141">Dynamics 365 Finance、Supply Chain Management 和 Project Operations</span><span class="sxs-lookup"><span data-stu-id="4340b-141">Dynamics 365 Finance, Supply Chain Management, and Project Operations products</span></span>|
| <span data-ttu-id="4340b-142">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="4340b-142">**Deployment option**</span></span>              | <span data-ttu-id="4340b-143">所有</span><span class="sxs-lookup"><span data-stu-id="4340b-143">All</span></span> |
| <span data-ttu-id="4340b-144">**状态**</span><span class="sxs-lookup"><span data-stu-id="4340b-144">**Status**</span></span>                         | <span data-ttu-id="4340b-145">已弃用：到 2022 年 4 月 1 日，我们计划不再支持 Microsoft Dynamics Lifecycle Services (LCS) 存储库作为电子报告 (ER) 配置的存储选项。</span><span class="sxs-lookup"><span data-stu-id="4340b-145">Deprecated: By April 01, 2022, we plan to no longer support the Microsoft Dynamics Lifecycle Services (LCS) repository as a storage option for Electronic reporting (ER) configurations.</span></span> <span data-ttu-id="4340b-146">将发布新的 Microsoft ER 配置，以专门从全局存储库下载。</span><span class="sxs-lookup"><span data-stu-id="4340b-146">New Microsoft ER configurations will be published for download exclusively from the Global repository.</span></span> <span data-ttu-id="4340b-147">可以从 Dynamics 365 产品和 RCS 访问全局存储库。</span><span class="sxs-lookup"><span data-stu-id="4340b-147">The Global repository can be accessed from the Dynamics 365 products and RCS.</span></span> <span data-ttu-id="4340b-148">有关详细信息，请参阅[从 RCS 导入 ER 配置](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md)和 [Regulatory Configuration Service - Lifecycle Services 存储弃用](../localizations/rcs-lcs-repo-dep-faq.md)。</span><span class="sxs-lookup"><span data-stu-id="4340b-148">For more information, see [Import ER configurations from RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md) and [Regulatory Configuration Service - Lifecycle Services storage deprecation](../localizations/rcs-lcs-repo-dep-faq.md).</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-10016-release"></a><span data-ttu-id="4340b-149">Finance 10.0.16 版本中已经删除或弃用的功能</span><span class="sxs-lookup"><span data-stu-id="4340b-149">Features removed or deprecated in the Finance 10.0.16 release</span></span>

### <a name="vat-declaration-cz-and-control-statement-export-cz-electronic-reporting-formats-for-czech-republic"></a><span data-ttu-id="4340b-150">捷克共和国的“增值税申报 (CZ)”和“控制对帐单导出 (CZ)”电子报告格式</span><span class="sxs-lookup"><span data-stu-id="4340b-150">"VAT declaration (CZ)" and "Control statement export (CZ)" Electronic reporting formats for Czech Republic</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="4340b-151">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="4340b-151">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="4340b-152">替换为新格式</span><span class="sxs-lookup"><span data-stu-id="4340b-152">Replaced with new formats</span></span> |
| <span data-ttu-id="4340b-153">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="4340b-153">**Replaced by another feature?**</span></span>   | <span data-ttu-id="4340b-154">是</span><span class="sxs-lookup"><span data-stu-id="4340b-154">Yes</span></span> |
| <span data-ttu-id="4340b-155">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="4340b-155">**Product areas affected**</span></span>         | <span data-ttu-id="4340b-156">申请</span><span class="sxs-lookup"><span data-stu-id="4340b-156">Application</span></span> |
| <span data-ttu-id="4340b-157">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="4340b-157">**Deployment option**</span></span>              | <span data-ttu-id="4340b-158">所有</span><span class="sxs-lookup"><span data-stu-id="4340b-158">All</span></span> |
| <span data-ttu-id="4340b-159">**状态**</span><span class="sxs-lookup"><span data-stu-id="4340b-159">**Status**</span></span>                         | <span data-ttu-id="4340b-160">弃用：到 2022 年 1 月 22 日，我们计划不再支持“增值税申报 (CZ)”、“控制对帐单导出 (CZ)”电子报告 (ER) 格式。</span><span class="sxs-lookup"><span data-stu-id="4340b-160">Deprecated: By January 22, 2022, we plan to no longer support "VAT declaration (CZ)", "Control statement export (CZ)" Electronic reporting (ER) formats.</span></span> <span data-ttu-id="4340b-161">而是在“税申报”模型下引入新的增值税申报 XML (CZ)、增值税申报 Excel (CZ)、增值税控制对帐单 XML (CZ) 格式。</span><span class="sxs-lookup"><span data-stu-id="4340b-161">New VAT declaration XML (CZ), VAT declaration Excel (CZ), VAT control statement XML (CZ) formats are introduced instead under the "Tax declaration" model.</span></span> |

### <a name="ledger-transaction-export-format-be-electronic-reporting-format-and-respective-ledger-transaction-export-be-model-for-belgium"></a><span data-ttu-id="4340b-162">比利时的“分类帐交易导出格式 (BE)”电子申报格式和相应的“分类帐交易导出 (BE)”模型</span><span class="sxs-lookup"><span data-stu-id="4340b-162">"Ledger transaction export format (BE)" Electronic reporting format and respective "Ledger transaction export (BE)" model for Belgium</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="4340b-163">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="4340b-163">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="4340b-164">在“标准审核文件 (SAF-T)”模型下替换为了新的 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="4340b-164">Replaced with new ER format under "Standard Audit File (SAF-T)" model.</span></span>  |
| <span data-ttu-id="4340b-165">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="4340b-165">**Replaced by another feature?**</span></span>   | <span data-ttu-id="4340b-166">是</span><span class="sxs-lookup"><span data-stu-id="4340b-166">Yes</span></span> |
| <span data-ttu-id="4340b-167">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="4340b-167">**Product areas affected**</span></span>         | <span data-ttu-id="4340b-168">申请</span><span class="sxs-lookup"><span data-stu-id="4340b-168">Application</span></span> |
| <span data-ttu-id="4340b-169">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="4340b-169">**Deployment option**</span></span>              | <span data-ttu-id="4340b-170">所有</span><span class="sxs-lookup"><span data-stu-id="4340b-170">All</span></span> |
| <span data-ttu-id="4340b-171">**状态**</span><span class="sxs-lookup"><span data-stu-id="4340b-171">**Status**</span></span>                         | <span data-ttu-id="4340b-172">已弃用：到 2021 年 12 月 1 日，我们计划不再支持“分类帐交易导出格式 (BE)”电子申报 (ER) 格式和相应的“分类帐交易导出 (BE)”模型。</span><span class="sxs-lookup"><span data-stu-id="4340b-172">Deprecated: By December 1, 2021, we plan to no longer support the "Ledger transaction export format (BE)" Electronic reporting (ER) format and respective "Ledger transaction export (BE)" model.</span></span> <span data-ttu-id="4340b-173">而是在“标准审核文件 (SAF-T)”模型下引入新的“总帐数据导出 (BE)”格式以及“总帐数据模型映射”。</span><span class="sxs-lookup"><span data-stu-id="4340b-173">A new "General ledger data export (BE)" format together with "General ledger data model mapping" are introduced instead under the "Standard Audit File (SAF-T)" model.</span></span> |

### <a name="vat-100-report-for-the-united-kingdom-in-ssrs-format"></a><span data-ttu-id="4340b-174">SSRS 格式的英国“VAT 100”报表</span><span class="sxs-lookup"><span data-stu-id="4340b-174">"VAT 100" report for the United Kingdom in SSRS format</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="4340b-175">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="4340b-175">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="4340b-176">“税申报模型”下已替换为新的 ER 格式 -“增值税申报 Excel (UK)”格式。</span><span class="sxs-lookup"><span data-stu-id="4340b-176">Replaced with new ER format - "VAT Declaration Excel (UK)" format under "Tax declaration model".</span></span>  |
| <span data-ttu-id="4340b-177">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="4340b-177">**Replaced by another feature?**</span></span>   | <span data-ttu-id="4340b-178">是</span><span class="sxs-lookup"><span data-stu-id="4340b-178">Yes</span></span> |
| <span data-ttu-id="4340b-179">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="4340b-179">**Product areas affected**</span></span>         | <span data-ttu-id="4340b-180">申请</span><span class="sxs-lookup"><span data-stu-id="4340b-180">Application</span></span> |
| <span data-ttu-id="4340b-181">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="4340b-181">**Deployment option**</span></span>              | <span data-ttu-id="4340b-182">所有</span><span class="sxs-lookup"><span data-stu-id="4340b-182">All</span></span> |
| <span data-ttu-id="4340b-183">**状态**</span><span class="sxs-lookup"><span data-stu-id="4340b-183">**Status**</span></span>                         | <span data-ttu-id="4340b-184">已弃用：到 2021 年 12 月 1 日，我们计划不再支持 SSRS 格式的“增值税 100 报表”。</span><span class="sxs-lookup"><span data-stu-id="4340b-184">Deprecated: By December 1, 2021, we plan to no longer support the "VAT 100 report" in SSRS format.</span></span> <span data-ttu-id="4340b-185">在 [MTD 增值税功能](../localizations/emea-gbr-mtd-vat-integration.md)中“税申报模型”下引入了新的“增值税申报 Excel (UK)”格式。</span><span class="sxs-lookup"><span data-stu-id="4340b-185">A new "VAT Declaration Excel (UK)" format under "Tax declaration model" was introduced in the [MTD VAT feature](../localizations/emea-gbr-mtd-vat-integration.md).</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-10015-release"></a><span data-ttu-id="4340b-186">Finance 10.0.15 版本中已经删除或弃用的功能</span><span class="sxs-lookup"><span data-stu-id="4340b-186">Features removed or deprecated in the Finance 10.0.15 release</span></span>

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a><span data-ttu-id="4340b-187">Dynamics 365 不再支持 Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="4340b-187">Internet Explorer 11 support for Dynamics 365 is deprecated</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="4340b-188">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="4340b-188">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="4340b-189">从 2020 年 12 月开始，所有 Dynamics 365 产品的 Microsoft Internet Explorer 11 支持已弃用，2021 年 8 月之后，将不再支持 Internet Explorer 11。</span><span class="sxs-lookup"><span data-stu-id="4340b-189">Effective December 2020, Microsoft Internet Explorer 11 support for all Dynamics 365 products is deprecated, and Internet Explorer 11 won’t be supported after August 2021.</span></span><br><br><span data-ttu-id="4340b-190">这将影响所用 Dynamics 365 产品设计为通过 Internet Explorer 11 界面使用的客户。</span><span class="sxs-lookup"><span data-stu-id="4340b-190">This will impact customers who use Dynamics 365 products that are designed to be used through an Internet Explorer 11 interface.</span></span> <span data-ttu-id="4340b-191">2021 年 8 月之后，此类 Dynamics 365 产品将不支持 Internet Explorer 11。</span><span class="sxs-lookup"><span data-stu-id="4340b-191">After August 2021, Internet Explorer 11 won't be supported for such Dynamics 365 products.</span></span> |
| <span data-ttu-id="4340b-192">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="4340b-192">**Replaced by another feature?**</span></span>   | <span data-ttu-id="4340b-193">我们建议客户转换到 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="4340b-193">We recommend that customers transition to Microsoft Edge.</span></span>|
| <span data-ttu-id="4340b-194">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="4340b-194">**Product areas affected**</span></span>         | <span data-ttu-id="4340b-195">所有 Dynamics 365 产品</span><span class="sxs-lookup"><span data-stu-id="4340b-195">All Dynamics 365 products</span></span> |
| <span data-ttu-id="4340b-196">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="4340b-196">**Deployment option**</span></span>              | <span data-ttu-id="4340b-197">所有</span><span class="sxs-lookup"><span data-stu-id="4340b-197">All</span></span>|
| <span data-ttu-id="4340b-198">**状态**</span><span class="sxs-lookup"><span data-stu-id="4340b-198">**Status**</span></span>                         | <span data-ttu-id="4340b-199">已弃用。</span><span class="sxs-lookup"><span data-stu-id="4340b-199">Deprecated.</span></span> <span data-ttu-id="4340b-200">2021 年 8 月之后将不再支持 Internet Explorer 11。</span><span class="sxs-lookup"><span data-stu-id="4340b-200">Internet Explorer 11 won’t be supported after August 2021.</span></span>|

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a><span data-ttu-id="4340b-201">Finance 10.0.12 版本中已经删除或弃用的功能</span><span class="sxs-lookup"><span data-stu-id="4340b-201">Features removed or deprecated in the Finance 10.0.12 release</span></span>

### <a name="not-deprecated-polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a><span data-ttu-id="4340b-202">未弃用：波兰语 SSRS 报表：销售增值税登记簿、采购增值税登记簿、欧盟增值税汇总登记簿 – 功能引用 PL-00014</span><span class="sxs-lookup"><span data-stu-id="4340b-202">Not deprecated: Polish SSRS reports: Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="4340b-203">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="4340b-203">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="4340b-204">非法律要求。</span><span class="sxs-lookup"><span data-stu-id="4340b-204">Not legally required.</span></span>  |
| <span data-ttu-id="4340b-205">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="4340b-205">**Replaced by another feature?**</span></span>   | <span data-ttu-id="4340b-206">是（包含增值税申报的标准审计文件的 Excel 格式 - JPK_VDEK）</span><span class="sxs-lookup"><span data-stu-id="4340b-206">Yes (Excel format for Standard Audit File with VAT declaration - JPK_VDEK)</span></span> |
| <span data-ttu-id="4340b-207">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="4340b-207">**Product areas affected**</span></span>         | <span data-ttu-id="4340b-208">申请</span><span class="sxs-lookup"><span data-stu-id="4340b-208">Application</span></span> |
| <span data-ttu-id="4340b-209">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="4340b-209">**Deployment option**</span></span>              | <span data-ttu-id="4340b-210">所有</span><span class="sxs-lookup"><span data-stu-id="4340b-210">All</span></span> |
| <span data-ttu-id="4340b-211">**状态**</span><span class="sxs-lookup"><span data-stu-id="4340b-211">**Status**</span></span>                         | <span data-ttu-id="4340b-212">未弃用：我们计划从 2021 年 4 月 27 日开始继续支持 SSRS 报表：**销售增值税登记簿、采购增值税登记簿、欧盟增值税汇总登记簿 – 功能引用 PL-00014**。</span><span class="sxs-lookup"><span data-stu-id="4340b-212">Not deprecated: As of April 27, 2021, we plan to continue to support the SSRS reports: **Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014**.</span></span> <span data-ttu-id="4340b-213">已经引入包含增值税申报的标准审计文件的 Excel 格式示例 (JPK_VDEK)。</span><span class="sxs-lookup"><span data-stu-id="4340b-213">Excel format example for Standard Audit File with VAT declaration (JPK_VDEK) has also been introduced.</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a><span data-ttu-id="4340b-214">Finance 10.0.11 版本中已经删除或弃用的功能</span><span class="sxs-lookup"><span data-stu-id="4340b-214">Features removed or deprecated in the Finance 10.0.11 release</span></span>

### <a name="norwegian-standard-main-accounts"></a><span data-ttu-id="4340b-215">挪威标准主科目</span><span class="sxs-lookup"><span data-stu-id="4340b-215">Norwegian Standard main accounts</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="4340b-216">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="4340b-216">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="4340b-217">重新设计</span><span class="sxs-lookup"><span data-stu-id="4340b-217">Redesign</span></span>  |
| <span data-ttu-id="4340b-218">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="4340b-218">**Replaced by another feature?**</span></span>   | <span data-ttu-id="4340b-219">是（已被 ER 格式应用程序特定参数取代）</span><span class="sxs-lookup"><span data-stu-id="4340b-219">Yes (Replaced with ER format application-specific parameters)</span></span> |
| <span data-ttu-id="4340b-220">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="4340b-220">**Product areas affected**</span></span>         | <span data-ttu-id="4340b-221">申请表</span><span class="sxs-lookup"><span data-stu-id="4340b-221">Application</span></span> |
| <span data-ttu-id="4340b-222">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="4340b-222">**Deployment option**</span></span>              | <span data-ttu-id="4340b-223">所有</span><span class="sxs-lookup"><span data-stu-id="4340b-223">All</span></span> |
| <span data-ttu-id="4340b-224">**状态**</span><span class="sxs-lookup"><span data-stu-id="4340b-224">**Status**</span></span>                         | <span data-ttu-id="4340b-225">已弃用：我们计划从 2021 年 4 月 1 日开始不再支持与标准主科目有关的功能：“引用”字段、相关表、数据实体。</span><span class="sxs-lookup"><span data-stu-id="4340b-225">Deprecated: By April 1, 2021, we plan to no longer support functionality related to Standard main accounts: Reference field, related table, data entity.</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a><span data-ttu-id="4340b-226">Finance 10.0.7 版本中已经删除或弃用的功能</span><span class="sxs-lookup"><span data-stu-id="4340b-226">Features removed or deprecated in the Finance 10.0.7 release</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="4340b-227">“工作流请求更改”对话框中不再包含用户选择下拉列表</span><span class="sxs-lookup"><span data-stu-id="4340b-227">Workflow request change dialog box no longer includes user selection drop-down list</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="4340b-228">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="4340b-228">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="4340b-229">更改为带帐户组选择的功能。</span><span class="sxs-lookup"><span data-stu-id="4340b-229">Changed to the feature with account groups selection.</span></span>  |
| <span data-ttu-id="4340b-230">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="4340b-230">**Replaced by another feature?**</span></span>   | <span data-ttu-id="4340b-231">是</span><span class="sxs-lookup"><span data-stu-id="4340b-231">Yes</span></span> |
| <span data-ttu-id="4340b-232">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="4340b-232">**Product areas affected**</span></span>         | <span data-ttu-id="4340b-233">工作流</span><span class="sxs-lookup"><span data-stu-id="4340b-233">Workflow</span></span> |
| <span data-ttu-id="4340b-234">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="4340b-234">**Deployment option**</span></span>              | <span data-ttu-id="4340b-235">所有</span><span class="sxs-lookup"><span data-stu-id="4340b-235">All</span></span> |
| <span data-ttu-id="4340b-236">**状态**</span><span class="sxs-lookup"><span data-stu-id="4340b-236">**Status**</span></span>                         | <span data-ttu-id="4340b-237">弃用：到 2020 年 12 月 1 日，我们计划不再支持不带帐户组选择的中国凭证类型设置。</span><span class="sxs-lookup"><span data-stu-id="4340b-237">Deprecated: By December 1, 2020, we plan to no longer support Chinese voucher types setup without Account groups selection.</span></span> <span data-ttu-id="4340b-238">请在 [10.0.7 的新增功能](whats-new-changed-10-0-7.md)中查找有关新设计的更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="4340b-238">Find more details about the new design in [What's new in 10.0.7](whats-new-changed-10-0-7.md).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="4340b-239">之前有关已删除或已弃用功能的声明</span><span class="sxs-lookup"><span data-stu-id="4340b-239">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="4340b-240">若要了解有关早期版本中已删除或已弃用功能的详细信息，请参阅[早期版本中已删除或已弃用的功能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md)。</span><span class="sxs-lookup"><span data-stu-id="4340b-240">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

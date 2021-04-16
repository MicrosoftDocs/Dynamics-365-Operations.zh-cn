---
title: Dynamics 365 Finance 中已删除或弃用的功能
description: 本主题介绍 Dynamics 365 Finance 中已经删除或计划删除的功能。
author: roschlom
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 5a8f5dbc52eab78697de0d3a48d8cceb42c36540
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836905"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a><span data-ttu-id="722fa-103">Dynamics 365 Finance 中已删除或弃用的功能</span><span class="sxs-lookup"><span data-stu-id="722fa-103">Removed or deprecated features in Dynamics 365 Finance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="722fa-104">本主题介绍 Dynamics 365 Finance 中已经删除或计划删除的功能。</span><span class="sxs-lookup"><span data-stu-id="722fa-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Finance.</span></span>

- <span data-ttu-id="722fa-105">*已移除* 的功能在产品中不再可用。</span><span class="sxs-lookup"><span data-stu-id="722fa-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="722fa-106">*已弃用* 的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。</span><span class="sxs-lookup"><span data-stu-id="722fa-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="722fa-107">此列表旨在帮助您在您自己的计划中考虑这些功能的移除和弃用。</span><span class="sxs-lookup"><span data-stu-id="722fa-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="722fa-108">[技术参考报告](https://docs.microsoft.com/dynamics/s-e/global/axtechrefrep_61)中提供了有关 Finance and Operations应用中的对象的详细信息。</span><span class="sxs-lookup"><span data-stu-id="722fa-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://docs.microsoft.com/dynamics/s-e/global/axtechrefrep_61).</span></span> <span data-ttu-id="722fa-109">可比较这些报告的不同版本，以了解 Finance and Operations 应用各版本中已更改或已删除的对象。</span><span class="sxs-lookup"><span data-stu-id="722fa-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-finance-10017-release"></a><span data-ttu-id="722fa-110">Finance 10.0.17 版本中已经删除或弃用的功能</span><span class="sxs-lookup"><span data-stu-id="722fa-110">Features removed or deprecated in the Finance 10.0.17 release</span></span>

### <a name="lcs-repository-as-a-storage-option-for-electronic-reporting-configurations"></a><span data-ttu-id="722fa-111">作为电子报告配置的存储选项的 LCS 储存库</span><span class="sxs-lookup"><span data-stu-id="722fa-111">LCS repository as a storage option for Electronic reporting configurations</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="722fa-112">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="722fa-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="722fa-113">替换为新的监管配置服务 (RCS) 全局存储库</span><span class="sxs-lookup"><span data-stu-id="722fa-113">Replaced with the new Regulatory Configuration Service (RCS) Global repository</span></span> |
| <span data-ttu-id="722fa-114">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="722fa-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="722fa-115">是</span><span class="sxs-lookup"><span data-stu-id="722fa-115">Yes</span></span> |
| <span data-ttu-id="722fa-116">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="722fa-116">**Product areas affected**</span></span>         | <span data-ttu-id="722fa-117">Dynamics 365 Finance、Supply Chain Management 和 Project Operations</span><span class="sxs-lookup"><span data-stu-id="722fa-117">Dynamics 365 Finance, Supply Chain Management, and Project Operations products</span></span>|
| <span data-ttu-id="722fa-118">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="722fa-118">**Deployment option**</span></span>              | <span data-ttu-id="722fa-119">所有</span><span class="sxs-lookup"><span data-stu-id="722fa-119">All</span></span> |
| <span data-ttu-id="722fa-120">**状态**</span><span class="sxs-lookup"><span data-stu-id="722fa-120">**Status**</span></span>                         | <span data-ttu-id="722fa-121">已弃用：到 2022 年 4 月 1 日，我们计划不再支持 Microsoft Dynamics Lifecycle Services (LCS) 存储库作为电子报告 (ER) 配置的存储选项。</span><span class="sxs-lookup"><span data-stu-id="722fa-121">Deprecated: By April 01, 2022, we plan to no longer support the Microsoft Dynamics Lifecycle Services (LCS) repository as a storage option for Electronic reporting (ER) configurations.</span></span> <span data-ttu-id="722fa-122">将发布新的 Microsoft ER 配置，以专门从全局存储库下载。</span><span class="sxs-lookup"><span data-stu-id="722fa-122">New Microsoft ER configurations will be published for download exclusively from the Global repository.</span></span> <span data-ttu-id="722fa-123">可以从 Dynamics 365 产品和 RCS 访问全局存储库。</span><span class="sxs-lookup"><span data-stu-id="722fa-123">The Global repository can be accessed from the Dynamics 365 products and RCS.</span></span> <span data-ttu-id="722fa-124">有关详细信息，请参阅[从 RCS 导入 ER 配置](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md)。</span><span class="sxs-lookup"><span data-stu-id="722fa-124">For more information, see [Import ER configurations from RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-10016-release"></a><span data-ttu-id="722fa-125">Finance 10.0.16 版本中已经删除或弃用的功能</span><span class="sxs-lookup"><span data-stu-id="722fa-125">Features removed or deprecated in the Finance 10.0.16 release</span></span>

### <a name="vat-declaration-cz-and-control-statement-export-cz-electronic-reporting-formats-for-czech-republic"></a><span data-ttu-id="722fa-126">捷克共和国的“增值税申报 (CZ)”和“控制对帐单导出 (CZ)”电子报告格式</span><span class="sxs-lookup"><span data-stu-id="722fa-126">"VAT declaration (CZ)" and "Control statement export (CZ)" Electronic reporting formats for Czech Republic</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="722fa-127">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="722fa-127">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="722fa-128">替换为新格式</span><span class="sxs-lookup"><span data-stu-id="722fa-128">Replaced with new formats</span></span> |
| <span data-ttu-id="722fa-129">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="722fa-129">**Replaced by another feature?**</span></span>   | <span data-ttu-id="722fa-130">是</span><span class="sxs-lookup"><span data-stu-id="722fa-130">Yes</span></span> |
| <span data-ttu-id="722fa-131">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="722fa-131">**Product areas affected**</span></span>         | <span data-ttu-id="722fa-132">申请</span><span class="sxs-lookup"><span data-stu-id="722fa-132">Application</span></span> |
| <span data-ttu-id="722fa-133">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="722fa-133">**Deployment option**</span></span>              | <span data-ttu-id="722fa-134">所有</span><span class="sxs-lookup"><span data-stu-id="722fa-134">All</span></span> |
| <span data-ttu-id="722fa-135">**状态**</span><span class="sxs-lookup"><span data-stu-id="722fa-135">**Status**</span></span>                         | <span data-ttu-id="722fa-136">弃用：到 2022 年 1 月 22 日，我们计划不再支持“增值税申报 (CZ)”、“控制对帐单导出 (CZ)”电子报告 (ER) 格式。</span><span class="sxs-lookup"><span data-stu-id="722fa-136">Deprecated: By January 22, 2022, we plan to no longer support "VAT declaration (CZ)", "Control statement export (CZ)" Electronic reporting (ER) formats.</span></span> <span data-ttu-id="722fa-137">而是在“税申报”模型下引入新的增值税申报 XML (CZ)、增值税申报 Excel (CZ)、增值税控制对帐单 XML (CZ) 格式。</span><span class="sxs-lookup"><span data-stu-id="722fa-137">New VAT declaration XML (CZ), VAT declaration Excel (CZ), VAT control statement XML (CZ) formats are introduced instead under the "Tax declaration" model.</span></span> |

### <a name="ledger-transaction-export-format-be-electronic-reporting-format-and-respective-ledger-transaction-export-be-model-for-belgium"></a><span data-ttu-id="722fa-138">比利时的“分类帐交易导出格式 (BE)”电子申报格式和相应的“分类帐交易导出 (BE)”模型</span><span class="sxs-lookup"><span data-stu-id="722fa-138">"Ledger transaction export format (BE)" Electronic reporting format and respective "Ledger transaction export (BE)" model for Belgium</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="722fa-139">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="722fa-139">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="722fa-140">在“标准审核文件 (SAF-T)”模型下替换为了新的 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="722fa-140">Replaced with new ER format under "Standard Audit File (SAF-T)" model.</span></span>  |
| <span data-ttu-id="722fa-141">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="722fa-141">**Replaced by another feature?**</span></span>   | <span data-ttu-id="722fa-142">是</span><span class="sxs-lookup"><span data-stu-id="722fa-142">Yes</span></span> |
| <span data-ttu-id="722fa-143">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="722fa-143">**Product areas affected**</span></span>         | <span data-ttu-id="722fa-144">申请</span><span class="sxs-lookup"><span data-stu-id="722fa-144">Application</span></span> |
| <span data-ttu-id="722fa-145">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="722fa-145">**Deployment option**</span></span>              | <span data-ttu-id="722fa-146">所有</span><span class="sxs-lookup"><span data-stu-id="722fa-146">All</span></span> |
| <span data-ttu-id="722fa-147">**状态**</span><span class="sxs-lookup"><span data-stu-id="722fa-147">**Status**</span></span>                         | <span data-ttu-id="722fa-148">已弃用：到 2021 年 12 月 1 日，我们计划不再支持“分类帐交易导出格式 (BE)”电子申报 (ER) 格式和相应的“分类帐交易导出 (BE)”模型。</span><span class="sxs-lookup"><span data-stu-id="722fa-148">Deprecated: By December 1, 2021, we plan to no longer support the "Ledger transaction export format (BE)" Electronic reporting (ER) format and respective "Ledger transaction export (BE)" model.</span></span> <span data-ttu-id="722fa-149">而是在“标准审核文件 (SAF-T)”模型下引入新的“总帐数据导出 (BE)”格式以及“总帐数据模型映射”。</span><span class="sxs-lookup"><span data-stu-id="722fa-149">A new "General ledger data export (BE)" format together with "General ledger data model mapping" are introduced instead under the "Standard Audit File (SAF-T)" model.</span></span> |

### <a name="vat-100-report-for-the-united-kingdom-in-ssrs-format"></a><span data-ttu-id="722fa-150">SSRS 格式的英国“VAT 100”报表</span><span class="sxs-lookup"><span data-stu-id="722fa-150">"VAT 100" report for the United Kingdom in SSRS format</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="722fa-151">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="722fa-151">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="722fa-152">“税申报模型”下已替换为新的 ER 格式 -“增值税申报 Excel (UK)”格式。</span><span class="sxs-lookup"><span data-stu-id="722fa-152">Replaced with new ER format - "VAT Declaration Excel (UK)" format under "Tax declaration model".</span></span>  |
| <span data-ttu-id="722fa-153">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="722fa-153">**Replaced by another feature?**</span></span>   | <span data-ttu-id="722fa-154">是</span><span class="sxs-lookup"><span data-stu-id="722fa-154">Yes</span></span> |
| <span data-ttu-id="722fa-155">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="722fa-155">**Product areas affected**</span></span>         | <span data-ttu-id="722fa-156">申请</span><span class="sxs-lookup"><span data-stu-id="722fa-156">Application</span></span> |
| <span data-ttu-id="722fa-157">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="722fa-157">**Deployment option**</span></span>              | <span data-ttu-id="722fa-158">所有</span><span class="sxs-lookup"><span data-stu-id="722fa-158">All</span></span> |
| <span data-ttu-id="722fa-159">**状态**</span><span class="sxs-lookup"><span data-stu-id="722fa-159">**Status**</span></span>                         | <span data-ttu-id="722fa-160">已弃用：到 2021 年 12 月 1 日，我们计划不再支持 SSRS 格式的“增值税 100 报表”。</span><span class="sxs-lookup"><span data-stu-id="722fa-160">Deprecated: By December 1, 2021, we plan to no longer support the "VAT 100 report" in SSRS format.</span></span> <span data-ttu-id="722fa-161">在 [MTD 增值税功能](../localizations/emea-gbr-mtd-vat-integration.md)中“税申报模型”下引入了新的“增值税申报 Excel (UK)”格式。</span><span class="sxs-lookup"><span data-stu-id="722fa-161">A new "VAT Declaration Excel (UK)" format under "Tax declaration model" was introduced in the [MTD VAT feature](../localizations/emea-gbr-mtd-vat-integration.md).</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-10015-release"></a><span data-ttu-id="722fa-162">Finance 10.0.15 版本中已经删除或弃用的功能</span><span class="sxs-lookup"><span data-stu-id="722fa-162">Features removed or deprecated in the Finance 10.0.15 release</span></span>

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a><span data-ttu-id="722fa-163">Dynamics 365 不再支持 Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="722fa-163">Internet Explorer 11 support for Dynamics 365 is deprecated</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="722fa-164">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="722fa-164">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="722fa-165">从 2020 年 12 月开始，所有 Dynamics 365 产品的 Microsoft Internet Explorer 11 支持已弃用，2021 年 8 月之后，将不再支持 Internet Explorer 11。</span><span class="sxs-lookup"><span data-stu-id="722fa-165">Effective December 2020, Microsoft Internet Explorer 11 support for all Dynamics 365 products is deprecated, and Internet Explorer 11 won’t be supported after August 2021.</span></span><br><br><span data-ttu-id="722fa-166">这将影响所用 Dynamics 365 产品设计为通过 Internet Explorer 11 界面使用的客户。</span><span class="sxs-lookup"><span data-stu-id="722fa-166">This will impact customers who use Dynamics 365 products that are designed to be used through an Internet Explorer 11 interface.</span></span> <span data-ttu-id="722fa-167">2021 年 8 月之后，此类 Dynamics 365 产品将不支持 Internet Explorer 11。</span><span class="sxs-lookup"><span data-stu-id="722fa-167">After August 2021, Internet Explorer 11 won't be supported for such Dynamics 365 products.</span></span> |
| <span data-ttu-id="722fa-168">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="722fa-168">**Replaced by another feature?**</span></span>   | <span data-ttu-id="722fa-169">我们建议客户转换到 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="722fa-169">We recommend that customers transition to Microsoft Edge.</span></span>|
| <span data-ttu-id="722fa-170">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="722fa-170">**Product areas affected**</span></span>         | <span data-ttu-id="722fa-171">所有 Dynamics 365 产品</span><span class="sxs-lookup"><span data-stu-id="722fa-171">All Dynamics 365 products</span></span> |
| <span data-ttu-id="722fa-172">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="722fa-172">**Deployment option**</span></span>              | <span data-ttu-id="722fa-173">所有</span><span class="sxs-lookup"><span data-stu-id="722fa-173">All</span></span>|
| <span data-ttu-id="722fa-174">**状态**</span><span class="sxs-lookup"><span data-stu-id="722fa-174">**Status**</span></span>                         | <span data-ttu-id="722fa-175">已弃用。</span><span class="sxs-lookup"><span data-stu-id="722fa-175">Deprecated.</span></span> <span data-ttu-id="722fa-176">2021 年 8 月之后将不再支持 Internet Explorer 11。</span><span class="sxs-lookup"><span data-stu-id="722fa-176">Internet Explorer 11 won’t be supported after August 2021.</span></span>|

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a><span data-ttu-id="722fa-177">Finance 10.0.12 版本中已经删除或弃用的功能</span><span class="sxs-lookup"><span data-stu-id="722fa-177">Features removed or deprecated in the Finance 10.0.12 release</span></span>

### <a name="polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a><span data-ttu-id="722fa-178">波兰语 SSRS 报表：销售增值税登记簿、采购增值税登记簿、欧盟增值税汇总登记簿 – 功能引用 PL-00014</span><span class="sxs-lookup"><span data-stu-id="722fa-178">Polish SSRS reports: Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="722fa-179">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="722fa-179">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="722fa-180">非法律要求。</span><span class="sxs-lookup"><span data-stu-id="722fa-180">Not legally required.</span></span>  |
| <span data-ttu-id="722fa-181">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="722fa-181">**Replaced by another feature?**</span></span>   | <span data-ttu-id="722fa-182">是（包含增值税申报的标准审计文件的 Excel 格式 - JPK_VDEK）</span><span class="sxs-lookup"><span data-stu-id="722fa-182">Yes (Excel format for Standard Audit File with VAT declaration - JPK_VDEK)</span></span> |
| <span data-ttu-id="722fa-183">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="722fa-183">**Product areas affected**</span></span>         | <span data-ttu-id="722fa-184">申请表</span><span class="sxs-lookup"><span data-stu-id="722fa-184">Application</span></span> |
| <span data-ttu-id="722fa-185">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="722fa-185">**Deployment option**</span></span>              | <span data-ttu-id="722fa-186">所有</span><span class="sxs-lookup"><span data-stu-id="722fa-186">All</span></span> |
| <span data-ttu-id="722fa-187">**状态**</span><span class="sxs-lookup"><span data-stu-id="722fa-187">**Status**</span></span>                         | <span data-ttu-id="722fa-188">已弃用：我们计划从 2021 年 7 月 1 日开始不再支持 SSRS 报表：**销售增值税登记簿、采购增值税登记簿、欧盟增值税汇总登记簿 – 功能引用 PL-00014**。</span><span class="sxs-lookup"><span data-stu-id="722fa-188">Deprecated: By July 1, 2021, we plan to no longer support the SSRS reports: **Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014**.</span></span> <span data-ttu-id="722fa-189">将改为引入包含增值税申报的标准审计文件的 Excel 格式示例 (JPK_VDEK)。</span><span class="sxs-lookup"><span data-stu-id="722fa-189">Excel format example for Standard Audit File with VAT declaration (JPK_VDEK) will be introduced instead.</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a><span data-ttu-id="722fa-190">Finance 10.0.11 版本中已经删除或弃用的功能</span><span class="sxs-lookup"><span data-stu-id="722fa-190">Features removed or deprecated in the Finance 10.0.11 release</span></span>

### <a name="norwegian-standard-main-accounts"></a><span data-ttu-id="722fa-191">挪威标准主科目</span><span class="sxs-lookup"><span data-stu-id="722fa-191">Norwegian Standard main accounts</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="722fa-192">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="722fa-192">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="722fa-193">重新设计</span><span class="sxs-lookup"><span data-stu-id="722fa-193">Redesign</span></span>  |
| <span data-ttu-id="722fa-194">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="722fa-194">**Replaced by another feature?**</span></span>   | <span data-ttu-id="722fa-195">是（已被 ER 格式应用程序特定参数取代）</span><span class="sxs-lookup"><span data-stu-id="722fa-195">Yes (Replaced with ER format application-specific parameters)</span></span> |
| <span data-ttu-id="722fa-196">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="722fa-196">**Product areas affected**</span></span>         | <span data-ttu-id="722fa-197">申请表</span><span class="sxs-lookup"><span data-stu-id="722fa-197">Application</span></span> |
| <span data-ttu-id="722fa-198">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="722fa-198">**Deployment option**</span></span>              | <span data-ttu-id="722fa-199">所有</span><span class="sxs-lookup"><span data-stu-id="722fa-199">All</span></span> |
| <span data-ttu-id="722fa-200">**状态**</span><span class="sxs-lookup"><span data-stu-id="722fa-200">**Status**</span></span>                         | <span data-ttu-id="722fa-201">已弃用：我们计划从 2021 年 4 月 1 日开始不再支持与标准主科目有关的功能：“引用”字段、相关表、数据实体。</span><span class="sxs-lookup"><span data-stu-id="722fa-201">Deprecated: By April 1, 2021, we plan to no longer support functionality related to Standard main accounts: Reference field, related table, data entity.</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a><span data-ttu-id="722fa-202">Finance 10.0.7 版本中已经删除或弃用的功能</span><span class="sxs-lookup"><span data-stu-id="722fa-202">Features removed or deprecated in the Finance 10.0.7 release</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="722fa-203">“工作流请求更改”对话框中不再包含用户选择下拉列表</span><span class="sxs-lookup"><span data-stu-id="722fa-203">Workflow request change dialog box no longer includes user selection drop-down list</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="722fa-204">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="722fa-204">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="722fa-205">更改为带帐户组选择的功能。</span><span class="sxs-lookup"><span data-stu-id="722fa-205">Changed to the feature with account groups selection.</span></span>  |
| <span data-ttu-id="722fa-206">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="722fa-206">**Replaced by another feature?**</span></span>   | <span data-ttu-id="722fa-207">是</span><span class="sxs-lookup"><span data-stu-id="722fa-207">Yes</span></span> |
| <span data-ttu-id="722fa-208">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="722fa-208">**Product areas affected**</span></span>         | <span data-ttu-id="722fa-209">工作流</span><span class="sxs-lookup"><span data-stu-id="722fa-209">Workflow</span></span> |
| <span data-ttu-id="722fa-210">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="722fa-210">**Deployment option**</span></span>              | <span data-ttu-id="722fa-211">所有</span><span class="sxs-lookup"><span data-stu-id="722fa-211">All</span></span> |
| <span data-ttu-id="722fa-212">**状态**</span><span class="sxs-lookup"><span data-stu-id="722fa-212">**Status**</span></span>                         | <span data-ttu-id="722fa-213">弃用：到 2020 年 12 月 1 日，我们计划不再支持不带帐户组选择的中国凭证类型设置。</span><span class="sxs-lookup"><span data-stu-id="722fa-213">Deprecated: By December 1, 2020, we plan to no longer support Chinese voucher types setup without Account groups selection.</span></span> <span data-ttu-id="722fa-214">请在 [10.0.7 的新增功能](whats-new-changed-10-0-7.md)中查找有关新设计的更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="722fa-214">Find more details about the new design in [What's new in 10.0.7](whats-new-changed-10-0-7.md).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="722fa-215">之前有关已删除或已弃用功能的声明</span><span class="sxs-lookup"><span data-stu-id="722fa-215">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="722fa-216">若要了解有关早期版本中已删除或已弃用功能的详细信息，请参阅[早期版本中已删除或已弃用的功能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md)。</span><span class="sxs-lookup"><span data-stu-id="722fa-216">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

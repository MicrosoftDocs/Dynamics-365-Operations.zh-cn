---
title: Dynamics 365 Finance 中已删除或弃用的功能
description: 本主题介绍 Dynamics 365 Finance 中已经删除或计划删除的功能。
author: roschlom
manager: AnnBe
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: a406db6d78302fa05596a58fffb7464222d4bfea
ms.sourcegitcommit: 069ed5789517b550065e5e2317658fec4027359e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/07/2020
ms.locfileid: "4689486"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a><span data-ttu-id="7c21b-103">Dynamics 365 Finance 中已删除或弃用的功能</span><span class="sxs-lookup"><span data-stu-id="7c21b-103">Removed or deprecated features in Dynamics 365 Finance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7c21b-104">本主题介绍 Dynamics 365 Finance 中已经删除或计划删除的功能。</span><span class="sxs-lookup"><span data-stu-id="7c21b-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Finance.</span></span>

- <span data-ttu-id="7c21b-105">*已移除* 的功能在产品中不再可用。</span><span class="sxs-lookup"><span data-stu-id="7c21b-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="7c21b-106">*已弃用* 的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。</span><span class="sxs-lookup"><span data-stu-id="7c21b-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="7c21b-107">此列表旨在帮助您在您自己的计划中考虑这些功能的移除和弃用。</span><span class="sxs-lookup"><span data-stu-id="7c21b-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="7c21b-108">[技术参考报告](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep)中提供了有关 Finance and Operations应用中的对象的详细信息。</span><span class="sxs-lookup"><span data-stu-id="7c21b-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="7c21b-109">可比较这些报告的不同版本，以了解 Finance and Operations 应用各版本中已更改或已删除的对象。</span><span class="sxs-lookup"><span data-stu-id="7c21b-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-finance-10016-release"></a><span data-ttu-id="7c21b-110">Finance 10.0.16 版本中已经删除或弃用的功能</span><span class="sxs-lookup"><span data-stu-id="7c21b-110">Features removed or deprecated in the Finance 10.0.16 release</span></span>

### <a name="ledger-transaction-export-format-be-electronic-reporting-format-and-respective-ledger-transaction-export-be-model-for-belgium"></a><span data-ttu-id="7c21b-111">比利时的“分类帐交易导出格式 (BE)”电子申报格式和相应的“分类帐交易导出 (BE)”模型</span><span class="sxs-lookup"><span data-stu-id="7c21b-111">"Ledger transaction export format (BE)" Electronic reporting format and respective "Ledger transaction export (BE)" model for Belgium</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="7c21b-112">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="7c21b-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="7c21b-113">在“标准审核文件 (SAF-T)”模型下替换为了新的 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="7c21b-113">Replaced with new ER format under "Standard Audit File (SAF-T)" model.</span></span>  |
| <span data-ttu-id="7c21b-114">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="7c21b-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="7c21b-115">是</span><span class="sxs-lookup"><span data-stu-id="7c21b-115">Yes</span></span> |
| <span data-ttu-id="7c21b-116">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="7c21b-116">**Product areas affected**</span></span>         | <span data-ttu-id="7c21b-117">申请</span><span class="sxs-lookup"><span data-stu-id="7c21b-117">Application</span></span> |
| <span data-ttu-id="7c21b-118">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="7c21b-118">**Deployment option**</span></span>              | <span data-ttu-id="7c21b-119">所有</span><span class="sxs-lookup"><span data-stu-id="7c21b-119">All</span></span> |
| <span data-ttu-id="7c21b-120">**状态**</span><span class="sxs-lookup"><span data-stu-id="7c21b-120">**Status**</span></span>                         | <span data-ttu-id="7c21b-121">已弃用：到 2021 年 12 月 1 日，我们计划不再支持“分类帐交易导出格式 (BE)”电子申报 (ER) 格式和相应的“分类帐交易导出 (BE)”模型。</span><span class="sxs-lookup"><span data-stu-id="7c21b-121">Deprecated: By December 1, 2021, we plan to no longer support the "Ledger transaction export format (BE)" Electronic reporting (ER) format and respective "Ledger transaction export (BE)" model.</span></span> <span data-ttu-id="7c21b-122">而是在“标准审核文件 (SAF-T)”模型下引入新的“总帐数据导出 (BE)”格式以及“总帐数据模型映射”。</span><span class="sxs-lookup"><span data-stu-id="7c21b-122">A new "General ledger data export (BE)" format together with "General ledger data model mapping" are introduced instead under the "Standard Audit File (SAF-T)" model.</span></span> |

### <a name="vat-100-report-for-the-united-kingdom-in-ssrs-format"></a><span data-ttu-id="7c21b-123">SSRS 格式的英国“VAT 100”报表</span><span class="sxs-lookup"><span data-stu-id="7c21b-123">"VAT 100" report for the United Kingdom in SSRS format</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="7c21b-124">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="7c21b-124">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="7c21b-125">“税申报模型”下已替换为新的 ER 格式 -“增值税申报 Excel (UK)”格式。</span><span class="sxs-lookup"><span data-stu-id="7c21b-125">Replaced with new ER format - "VAT Declaration Excel (UK)" format under "Tax declaration model".</span></span>  |
| <span data-ttu-id="7c21b-126">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="7c21b-126">**Replaced by another feature?**</span></span>   | <span data-ttu-id="7c21b-127">是</span><span class="sxs-lookup"><span data-stu-id="7c21b-127">Yes</span></span> |
| <span data-ttu-id="7c21b-128">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="7c21b-128">**Product areas affected**</span></span>         | <span data-ttu-id="7c21b-129">申请</span><span class="sxs-lookup"><span data-stu-id="7c21b-129">Application</span></span> |
| <span data-ttu-id="7c21b-130">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="7c21b-130">**Deployment option**</span></span>              | <span data-ttu-id="7c21b-131">所有</span><span class="sxs-lookup"><span data-stu-id="7c21b-131">All</span></span> |
| <span data-ttu-id="7c21b-132">**状态**</span><span class="sxs-lookup"><span data-stu-id="7c21b-132">**Status**</span></span>                         | <span data-ttu-id="7c21b-133">已弃用：到 2021 年 12 月 1 日，我们计划不再支持 SSRS 格式的“增值税 100 报表”。</span><span class="sxs-lookup"><span data-stu-id="7c21b-133">Deprecated: By December 1, 2021, we plan to no longer support the "VAT 100 report" in SSRS format.</span></span> <span data-ttu-id="7c21b-134">在 [MTD 增值税功能](../localizations/emea-gbr-mtd-vat-integration.md)中“税申报模型”下引入了新的“增值税申报 Excel (UK)”格式。</span><span class="sxs-lookup"><span data-stu-id="7c21b-134">A new "VAT Declaration Excel (UK)" format under "Tax declaration model" was introduced in the [MTD VAT feature](../localizations/emea-gbr-mtd-vat-integration.md).</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-10015-release"></a><span data-ttu-id="7c21b-135">Finance 10.0.15 版本中已经删除或弃用的功能</span><span class="sxs-lookup"><span data-stu-id="7c21b-135">Features removed or deprecated in the Finance 10.0.15 release</span></span>

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a><span data-ttu-id="7c21b-136">Dynamics 365 不再支持 Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="7c21b-136">Internet Explorer 11 support for Dynamics 365 is deprecated</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="7c21b-137">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="7c21b-137">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="7c21b-138">从 2020 年 12 月开始，所有 Dynamics 365 产品不再支持 Microsoft Internet Explorer 11，2021 年 8 月之后，不再支持 Internet Explorer 11。</span><span class="sxs-lookup"><span data-stu-id="7c21b-138">Effective December 2020, Microsoft Internet Explorer 11 support for all Dynamics 365 products is deprecated, and Internet Explorer 11 won’t be supported after August 2021.</span></span><br><br><span data-ttu-id="7c21b-139">这将影响所用 Dynamics 365 产品设计为通过 Internet Explorer 11 界面使用的客户。</span><span class="sxs-lookup"><span data-stu-id="7c21b-139">This will impact customers who use Dynamics 365 products that are designed to be used through an Internet Explorer 11 interface.</span></span> <span data-ttu-id="7c21b-140">2021 年 8 月之后，此类 Dynamics 365 产品将不支持 Internet Explorer 11。</span><span class="sxs-lookup"><span data-stu-id="7c21b-140">After August 2021, Internet Explorer 11 won't be supported for such Dynamics 365 products.</span></span> |
| <span data-ttu-id="7c21b-141">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="7c21b-141">**Replaced by another feature?**</span></span>   | <span data-ttu-id="7c21b-142">我们建议客户过渡到 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="7c21b-142">We recommend that customers transition to Microsoft Edge.</span></span>|
| <span data-ttu-id="7c21b-143">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="7c21b-143">**Product areas affected**</span></span>         | <span data-ttu-id="7c21b-144">所有 Dynamics 365 产品</span><span class="sxs-lookup"><span data-stu-id="7c21b-144">All Dynamics 365 products</span></span> |
| <span data-ttu-id="7c21b-145">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="7c21b-145">**Deployment option**</span></span>              | <span data-ttu-id="7c21b-146">所有</span><span class="sxs-lookup"><span data-stu-id="7c21b-146">All</span></span>|
| <span data-ttu-id="7c21b-147">**状态**</span><span class="sxs-lookup"><span data-stu-id="7c21b-147">**Status**</span></span>                         | <span data-ttu-id="7c21b-148">已弃用。</span><span class="sxs-lookup"><span data-stu-id="7c21b-148">Deprecated.</span></span> <span data-ttu-id="7c21b-149">2021 年 8 月之后将不再支持 Internet Explorer 11。</span><span class="sxs-lookup"><span data-stu-id="7c21b-149">Internet Explorer 11 won’t be supported after August 2021.</span></span>|

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a><span data-ttu-id="7c21b-150">Finance 10.0.12 版本中已经删除或弃用的功能</span><span class="sxs-lookup"><span data-stu-id="7c21b-150">Features removed or deprecated in the Finance 10.0.12 release</span></span>

### <a name="polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a><span data-ttu-id="7c21b-151">波兰语 SSRS 报表：销售增值税登记簿、采购增值税登记簿、欧盟增值税汇总登记簿 – 功能引用 PL-00014</span><span class="sxs-lookup"><span data-stu-id="7c21b-151">Polish SSRS reports: Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="7c21b-152">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="7c21b-152">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="7c21b-153">非法律要求。</span><span class="sxs-lookup"><span data-stu-id="7c21b-153">Not legally required.</span></span>  |
| <span data-ttu-id="7c21b-154">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="7c21b-154">**Replaced by another feature?**</span></span>   | <span data-ttu-id="7c21b-155">是（包含增值税申报的标准审计文件的 Excel 格式 - JPK_VDEK）</span><span class="sxs-lookup"><span data-stu-id="7c21b-155">Yes (Excel format for Standard Audit File with VAT declaration - JPK_VDEK)</span></span> |
| <span data-ttu-id="7c21b-156">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="7c21b-156">**Product areas affected**</span></span>         | <span data-ttu-id="7c21b-157">申请表</span><span class="sxs-lookup"><span data-stu-id="7c21b-157">Application</span></span> |
| <span data-ttu-id="7c21b-158">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="7c21b-158">**Deployment option**</span></span>              | <span data-ttu-id="7c21b-159">所有</span><span class="sxs-lookup"><span data-stu-id="7c21b-159">All</span></span> |
| <span data-ttu-id="7c21b-160">**状态**</span><span class="sxs-lookup"><span data-stu-id="7c21b-160">**Status**</span></span>                         | <span data-ttu-id="7c21b-161">已弃用：我们计划从 2021 年 7 月 1 日开始不再支持 SSRS 报表：**销售增值税登记簿、采购增值税登记簿、欧盟增值税汇总登记簿 – 功能引用 PL-00014**。</span><span class="sxs-lookup"><span data-stu-id="7c21b-161">Deprecated: By July 1, 2021, we plan to no longer support the SSRS reports: **Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014**.</span></span> <span data-ttu-id="7c21b-162">将改为引入包含增值税申报的标准审计文件的 Excel 格式示例 (JPK_VDEK)。</span><span class="sxs-lookup"><span data-stu-id="7c21b-162">Excel format example for Standard Audit File with VAT declaration (JPK_VDEK) will be introduced instead.</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a><span data-ttu-id="7c21b-163">Finance 10.0.11 版本中已经删除或弃用的功能</span><span class="sxs-lookup"><span data-stu-id="7c21b-163">Features removed or deprecated in the Finance 10.0.11 release</span></span>

### <a name="norwegian-standard-main-accounts"></a><span data-ttu-id="7c21b-164">挪威标准主科目</span><span class="sxs-lookup"><span data-stu-id="7c21b-164">Norwegian Standard main accounts</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="7c21b-165">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="7c21b-165">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="7c21b-166">重新设计</span><span class="sxs-lookup"><span data-stu-id="7c21b-166">Redesign</span></span>  |
| <span data-ttu-id="7c21b-167">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="7c21b-167">**Replaced by another feature?**</span></span>   | <span data-ttu-id="7c21b-168">是（已被 ER 格式应用程序特定参数取代）</span><span class="sxs-lookup"><span data-stu-id="7c21b-168">Yes (Replaced with ER format application-specific parameters)</span></span> |
| <span data-ttu-id="7c21b-169">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="7c21b-169">**Product areas affected**</span></span>         | <span data-ttu-id="7c21b-170">申请表</span><span class="sxs-lookup"><span data-stu-id="7c21b-170">Application</span></span> |
| <span data-ttu-id="7c21b-171">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="7c21b-171">**Deployment option**</span></span>              | <span data-ttu-id="7c21b-172">所有</span><span class="sxs-lookup"><span data-stu-id="7c21b-172">All</span></span> |
| <span data-ttu-id="7c21b-173">**状态**</span><span class="sxs-lookup"><span data-stu-id="7c21b-173">**Status**</span></span>                         | <span data-ttu-id="7c21b-174">已弃用：我们计划从 2021 年 4 月 1 日开始不再支持与标准主科目有关的功能：“引用”字段、相关表、数据实体。</span><span class="sxs-lookup"><span data-stu-id="7c21b-174">Deprecated: By April 1, 2021, we plan to no longer support functionality related to Standard main accounts: Reference field, related table, data entity.</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a><span data-ttu-id="7c21b-175">Finance 10.0.7 版本中已经删除或弃用的功能</span><span class="sxs-lookup"><span data-stu-id="7c21b-175">Features removed or deprecated in the Finance 10.0.7 release</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="7c21b-176">“工作流请求更改”对话框中不再包含用户选择下拉列表</span><span class="sxs-lookup"><span data-stu-id="7c21b-176">Workflow request change dialog box no longer includes user selection drop-down list</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="7c21b-177">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="7c21b-177">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="7c21b-178">更改为带帐户组选择的功能。</span><span class="sxs-lookup"><span data-stu-id="7c21b-178">Changed to the feature with account groups selection.</span></span>  |
| <span data-ttu-id="7c21b-179">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="7c21b-179">**Replaced by another feature?**</span></span>   | <span data-ttu-id="7c21b-180">是</span><span class="sxs-lookup"><span data-stu-id="7c21b-180">Yes</span></span> |
| <span data-ttu-id="7c21b-181">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="7c21b-181">**Product areas affected**</span></span>         | <span data-ttu-id="7c21b-182">工作流</span><span class="sxs-lookup"><span data-stu-id="7c21b-182">Workflow</span></span> |
| <span data-ttu-id="7c21b-183">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="7c21b-183">**Deployment option**</span></span>              | <span data-ttu-id="7c21b-184">所有</span><span class="sxs-lookup"><span data-stu-id="7c21b-184">All</span></span> |
| <span data-ttu-id="7c21b-185">**状态**</span><span class="sxs-lookup"><span data-stu-id="7c21b-185">**Status**</span></span>                         | <span data-ttu-id="7c21b-186">弃用：到 2020 年 12 月 1 日，我们计划不再支持不带帐户组选择的中国凭证类型设置。</span><span class="sxs-lookup"><span data-stu-id="7c21b-186">Deprecated: By December 1, 2020, we plan to no longer support Chinese voucher types setup without Account groups selection.</span></span> <span data-ttu-id="7c21b-187">请在 [10.0.7 的新增功能](whats-new-changed-10-0-7.md)中查找有关新设计的更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="7c21b-187">Find more details about the new design in [What's new in 10.0.7](whats-new-changed-10-0-7.md).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="7c21b-188">之前有关已删除或已弃用功能的声明</span><span class="sxs-lookup"><span data-stu-id="7c21b-188">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="7c21b-189">若要了解有关早期版本中已删除或已弃用功能的详细信息，请参阅[早期版本中已删除或已弃用的功能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md)。</span><span class="sxs-lookup"><span data-stu-id="7c21b-189">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span></span>

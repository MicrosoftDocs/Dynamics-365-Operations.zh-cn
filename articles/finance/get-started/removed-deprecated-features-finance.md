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
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 7090a7461c7b77d74f081afd8f22db100cdf0792
ms.sourcegitcommit: 79621e667cd7f48ba3bdbf2731f6f33d8e9f57f6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5154169"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a><span data-ttu-id="f9fc1-103">Dynamics 365 Finance 中已删除或弃用的功能</span><span class="sxs-lookup"><span data-stu-id="f9fc1-103">Removed or deprecated features in Dynamics 365 Finance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f9fc1-104">本主题介绍 Dynamics 365 Finance 中已经删除或计划删除的功能。</span><span class="sxs-lookup"><span data-stu-id="f9fc1-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Finance.</span></span>

- <span data-ttu-id="f9fc1-105">*已移除* 的功能在产品中不再可用。</span><span class="sxs-lookup"><span data-stu-id="f9fc1-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="f9fc1-106">*已弃用* 的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。</span><span class="sxs-lookup"><span data-stu-id="f9fc1-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="f9fc1-107">此列表旨在帮助您在您自己的计划中考虑这些功能的移除和弃用。</span><span class="sxs-lookup"><span data-stu-id="f9fc1-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="f9fc1-108">[技术参考报告](https://docs.microsoft.com/dynamics/s-e/)中提供了有关 Finance and Operations应用中的对象的详细信息。</span><span class="sxs-lookup"><span data-stu-id="f9fc1-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://docs.microsoft.com/dynamics/s-e/).</span></span> <span data-ttu-id="f9fc1-109">可比较这些报告的不同版本，以了解 Finance and Operations 应用各版本中已更改或已删除的对象。</span><span class="sxs-lookup"><span data-stu-id="f9fc1-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-finance-10016-release"></a><span data-ttu-id="f9fc1-110">Finance 10.0.16 版本中已经删除或弃用的功能</span><span class="sxs-lookup"><span data-stu-id="f9fc1-110">Features removed or deprecated in the Finance 10.0.16 release</span></span>

### <a name="vat-declaration-cz-and-control-statement-export-cz-electronic-reporting-formats-for-czech-republic"></a><span data-ttu-id="f9fc1-111">捷克共和国的“增值税申报 (CZ)”和“控制对帐单导出 (CZ)”电子报告格式</span><span class="sxs-lookup"><span data-stu-id="f9fc1-111">"VAT declaration (CZ)" and "Control statement export (CZ)" Electronic reporting formats for Czech Republic</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="f9fc1-112">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="f9fc1-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="f9fc1-113">替换为新格式</span><span class="sxs-lookup"><span data-stu-id="f9fc1-113">Replaced with new formats</span></span> |
| <span data-ttu-id="f9fc1-114">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="f9fc1-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="f9fc1-115">是</span><span class="sxs-lookup"><span data-stu-id="f9fc1-115">Yes</span></span> |
| <span data-ttu-id="f9fc1-116">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="f9fc1-116">**Product areas affected**</span></span>         | <span data-ttu-id="f9fc1-117">申请</span><span class="sxs-lookup"><span data-stu-id="f9fc1-117">Application</span></span> |
| <span data-ttu-id="f9fc1-118">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="f9fc1-118">**Deployment option**</span></span>              | <span data-ttu-id="f9fc1-119">所有</span><span class="sxs-lookup"><span data-stu-id="f9fc1-119">All</span></span> |
| <span data-ttu-id="f9fc1-120">**状态**</span><span class="sxs-lookup"><span data-stu-id="f9fc1-120">**Status**</span></span>                         | <span data-ttu-id="f9fc1-121">弃用：到 2022 年 1 月 22 日，我们计划不再支持“增值税申报 (CZ)”、“控制对帐单导出 (CZ)”电子报告 (ER) 格式。</span><span class="sxs-lookup"><span data-stu-id="f9fc1-121">Deprecated: By January 22, 2022, we plan to no longer support "VAT declaration (CZ)", "Control statement export (CZ)" Electronic reporting (ER) formats.</span></span> <span data-ttu-id="f9fc1-122">而是在“税申报”模型下引入新的增值税申报 XML (CZ)、增值税申报 Excel (CZ)、增值税控制对帐单 XML (CZ) 格式。</span><span class="sxs-lookup"><span data-stu-id="f9fc1-122">New VAT declaration XML (CZ), VAT declaration Excel (CZ), VAT control statement XML (CZ) formats are introduced instead under the "Tax declaration" model.</span></span> |

### <a name="ledger-transaction-export-format-be-electronic-reporting-format-and-respective-ledger-transaction-export-be-model-for-belgium"></a><span data-ttu-id="f9fc1-123">比利时的“分类帐交易导出格式 (BE)”电子申报格式和相应的“分类帐交易导出 (BE)”模型</span><span class="sxs-lookup"><span data-stu-id="f9fc1-123">"Ledger transaction export format (BE)" Electronic reporting format and respective "Ledger transaction export (BE)" model for Belgium</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="f9fc1-124">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="f9fc1-124">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="f9fc1-125">在“标准审核文件 (SAF-T)”模型下替换为了新的 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="f9fc1-125">Replaced with new ER format under "Standard Audit File (SAF-T)" model.</span></span>  |
| <span data-ttu-id="f9fc1-126">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="f9fc1-126">**Replaced by another feature?**</span></span>   | <span data-ttu-id="f9fc1-127">是</span><span class="sxs-lookup"><span data-stu-id="f9fc1-127">Yes</span></span> |
| <span data-ttu-id="f9fc1-128">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="f9fc1-128">**Product areas affected**</span></span>         | <span data-ttu-id="f9fc1-129">申请</span><span class="sxs-lookup"><span data-stu-id="f9fc1-129">Application</span></span> |
| <span data-ttu-id="f9fc1-130">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="f9fc1-130">**Deployment option**</span></span>              | <span data-ttu-id="f9fc1-131">所有</span><span class="sxs-lookup"><span data-stu-id="f9fc1-131">All</span></span> |
| <span data-ttu-id="f9fc1-132">**状态**</span><span class="sxs-lookup"><span data-stu-id="f9fc1-132">**Status**</span></span>                         | <span data-ttu-id="f9fc1-133">已弃用：到 2021 年 12 月 1 日，我们计划不再支持“分类帐交易导出格式 (BE)”电子申报 (ER) 格式和相应的“分类帐交易导出 (BE)”模型。</span><span class="sxs-lookup"><span data-stu-id="f9fc1-133">Deprecated: By December 1, 2021, we plan to no longer support the "Ledger transaction export format (BE)" Electronic reporting (ER) format and respective "Ledger transaction export (BE)" model.</span></span> <span data-ttu-id="f9fc1-134">而是在“标准审核文件 (SAF-T)”模型下引入新的“总帐数据导出 (BE)”格式以及“总帐数据模型映射”。</span><span class="sxs-lookup"><span data-stu-id="f9fc1-134">A new "General ledger data export (BE)" format together with "General ledger data model mapping" are introduced instead under the "Standard Audit File (SAF-T)" model.</span></span> |

### <a name="vat-100-report-for-the-united-kingdom-in-ssrs-format"></a><span data-ttu-id="f9fc1-135">SSRS 格式的英国“VAT 100”报表</span><span class="sxs-lookup"><span data-stu-id="f9fc1-135">"VAT 100" report for the United Kingdom in SSRS format</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="f9fc1-136">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="f9fc1-136">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="f9fc1-137">“税申报模型”下已替换为新的 ER 格式 -“增值税申报 Excel (UK)”格式。</span><span class="sxs-lookup"><span data-stu-id="f9fc1-137">Replaced with new ER format - "VAT Declaration Excel (UK)" format under "Tax declaration model".</span></span>  |
| <span data-ttu-id="f9fc1-138">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="f9fc1-138">**Replaced by another feature?**</span></span>   | <span data-ttu-id="f9fc1-139">是</span><span class="sxs-lookup"><span data-stu-id="f9fc1-139">Yes</span></span> |
| <span data-ttu-id="f9fc1-140">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="f9fc1-140">**Product areas affected**</span></span>         | <span data-ttu-id="f9fc1-141">申请</span><span class="sxs-lookup"><span data-stu-id="f9fc1-141">Application</span></span> |
| <span data-ttu-id="f9fc1-142">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="f9fc1-142">**Deployment option**</span></span>              | <span data-ttu-id="f9fc1-143">所有</span><span class="sxs-lookup"><span data-stu-id="f9fc1-143">All</span></span> |
| <span data-ttu-id="f9fc1-144">**状态**</span><span class="sxs-lookup"><span data-stu-id="f9fc1-144">**Status**</span></span>                         | <span data-ttu-id="f9fc1-145">已弃用：到 2021 年 12 月 1 日，我们计划不再支持 SSRS 格式的“增值税 100 报表”。</span><span class="sxs-lookup"><span data-stu-id="f9fc1-145">Deprecated: By December 1, 2021, we plan to no longer support the "VAT 100 report" in SSRS format.</span></span> <span data-ttu-id="f9fc1-146">在 [MTD 增值税功能](../localizations/emea-gbr-mtd-vat-integration.md)中“税申报模型”下引入了新的“增值税申报 Excel (UK)”格式。</span><span class="sxs-lookup"><span data-stu-id="f9fc1-146">A new "VAT Declaration Excel (UK)" format under "Tax declaration model" was introduced in the [MTD VAT feature](../localizations/emea-gbr-mtd-vat-integration.md).</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-10015-release"></a><span data-ttu-id="f9fc1-147">Finance 10.0.15 版本中已经删除或弃用的功能</span><span class="sxs-lookup"><span data-stu-id="f9fc1-147">Features removed or deprecated in the Finance 10.0.15 release</span></span>

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a><span data-ttu-id="f9fc1-148">Dynamics 365 不再支持 Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="f9fc1-148">Internet Explorer 11 support for Dynamics 365 is deprecated</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="f9fc1-149">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="f9fc1-149">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="f9fc1-150">从 2020 年 12 月开始，所有 Dynamics 365 产品的 Microsoft Internet Explorer 11 支持已弃用，2021 年 8 月之后，将不再支持 Internet Explorer 11。</span><span class="sxs-lookup"><span data-stu-id="f9fc1-150">Effective December 2020, Microsoft Internet Explorer 11 support for all Dynamics 365 products is deprecated, and Internet Explorer 11 won’t be supported after August 2021.</span></span><br><br><span data-ttu-id="f9fc1-151">这将影响所用 Dynamics 365 产品设计为通过 Internet Explorer 11 界面使用的客户。</span><span class="sxs-lookup"><span data-stu-id="f9fc1-151">This will impact customers who use Dynamics 365 products that are designed to be used through an Internet Explorer 11 interface.</span></span> <span data-ttu-id="f9fc1-152">2021 年 8 月之后，此类 Dynamics 365 产品将不支持 Internet Explorer 11。</span><span class="sxs-lookup"><span data-stu-id="f9fc1-152">After August 2021, Internet Explorer 11 won't be supported for such Dynamics 365 products.</span></span> |
| <span data-ttu-id="f9fc1-153">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="f9fc1-153">**Replaced by another feature?**</span></span>   | <span data-ttu-id="f9fc1-154">我们建议客户转换到 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="f9fc1-154">We recommend that customers transition to Microsoft Edge.</span></span>|
| <span data-ttu-id="f9fc1-155">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="f9fc1-155">**Product areas affected**</span></span>         | <span data-ttu-id="f9fc1-156">所有 Dynamics 365 产品</span><span class="sxs-lookup"><span data-stu-id="f9fc1-156">All Dynamics 365 products</span></span> |
| <span data-ttu-id="f9fc1-157">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="f9fc1-157">**Deployment option**</span></span>              | <span data-ttu-id="f9fc1-158">所有</span><span class="sxs-lookup"><span data-stu-id="f9fc1-158">All</span></span>|
| <span data-ttu-id="f9fc1-159">**状态**</span><span class="sxs-lookup"><span data-stu-id="f9fc1-159">**Status**</span></span>                         | <span data-ttu-id="f9fc1-160">已弃用。</span><span class="sxs-lookup"><span data-stu-id="f9fc1-160">Deprecated.</span></span> <span data-ttu-id="f9fc1-161">2021 年 8 月之后将不再支持 Internet Explorer 11。</span><span class="sxs-lookup"><span data-stu-id="f9fc1-161">Internet Explorer 11 won’t be supported after August 2021.</span></span>|

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a><span data-ttu-id="f9fc1-162">Finance 10.0.12 版本中已经删除或弃用的功能</span><span class="sxs-lookup"><span data-stu-id="f9fc1-162">Features removed or deprecated in the Finance 10.0.12 release</span></span>

### <a name="polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a><span data-ttu-id="f9fc1-163">波兰语 SSRS 报表：销售增值税登记簿、采购增值税登记簿、欧盟增值税汇总登记簿 – 功能引用 PL-00014</span><span class="sxs-lookup"><span data-stu-id="f9fc1-163">Polish SSRS reports: Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="f9fc1-164">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="f9fc1-164">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="f9fc1-165">非法律要求。</span><span class="sxs-lookup"><span data-stu-id="f9fc1-165">Not legally required.</span></span>  |
| <span data-ttu-id="f9fc1-166">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="f9fc1-166">**Replaced by another feature?**</span></span>   | <span data-ttu-id="f9fc1-167">是（包含增值税申报的标准审计文件的 Excel 格式 - JPK_VDEK）</span><span class="sxs-lookup"><span data-stu-id="f9fc1-167">Yes (Excel format for Standard Audit File with VAT declaration - JPK_VDEK)</span></span> |
| <span data-ttu-id="f9fc1-168">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="f9fc1-168">**Product areas affected**</span></span>         | <span data-ttu-id="f9fc1-169">申请表</span><span class="sxs-lookup"><span data-stu-id="f9fc1-169">Application</span></span> |
| <span data-ttu-id="f9fc1-170">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="f9fc1-170">**Deployment option**</span></span>              | <span data-ttu-id="f9fc1-171">所有</span><span class="sxs-lookup"><span data-stu-id="f9fc1-171">All</span></span> |
| <span data-ttu-id="f9fc1-172">**状态**</span><span class="sxs-lookup"><span data-stu-id="f9fc1-172">**Status**</span></span>                         | <span data-ttu-id="f9fc1-173">已弃用：我们计划从 2021 年 7 月 1 日开始不再支持 SSRS 报表：**销售增值税登记簿、采购增值税登记簿、欧盟增值税汇总登记簿 – 功能引用 PL-00014**。</span><span class="sxs-lookup"><span data-stu-id="f9fc1-173">Deprecated: By July 1, 2021, we plan to no longer support the SSRS reports: **Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014**.</span></span> <span data-ttu-id="f9fc1-174">将改为引入包含增值税申报的标准审计文件的 Excel 格式示例 (JPK_VDEK)。</span><span class="sxs-lookup"><span data-stu-id="f9fc1-174">Excel format example for Standard Audit File with VAT declaration (JPK_VDEK) will be introduced instead.</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a><span data-ttu-id="f9fc1-175">Finance 10.0.11 版本中已经删除或弃用的功能</span><span class="sxs-lookup"><span data-stu-id="f9fc1-175">Features removed or deprecated in the Finance 10.0.11 release</span></span>

### <a name="norwegian-standard-main-accounts"></a><span data-ttu-id="f9fc1-176">挪威标准主科目</span><span class="sxs-lookup"><span data-stu-id="f9fc1-176">Norwegian Standard main accounts</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="f9fc1-177">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="f9fc1-177">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="f9fc1-178">重新设计</span><span class="sxs-lookup"><span data-stu-id="f9fc1-178">Redesign</span></span>  |
| <span data-ttu-id="f9fc1-179">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="f9fc1-179">**Replaced by another feature?**</span></span>   | <span data-ttu-id="f9fc1-180">是（已被 ER 格式应用程序特定参数取代）</span><span class="sxs-lookup"><span data-stu-id="f9fc1-180">Yes (Replaced with ER format application-specific parameters)</span></span> |
| <span data-ttu-id="f9fc1-181">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="f9fc1-181">**Product areas affected**</span></span>         | <span data-ttu-id="f9fc1-182">申请表</span><span class="sxs-lookup"><span data-stu-id="f9fc1-182">Application</span></span> |
| <span data-ttu-id="f9fc1-183">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="f9fc1-183">**Deployment option**</span></span>              | <span data-ttu-id="f9fc1-184">所有</span><span class="sxs-lookup"><span data-stu-id="f9fc1-184">All</span></span> |
| <span data-ttu-id="f9fc1-185">**状态**</span><span class="sxs-lookup"><span data-stu-id="f9fc1-185">**Status**</span></span>                         | <span data-ttu-id="f9fc1-186">已弃用：我们计划从 2021 年 4 月 1 日开始不再支持与标准主科目有关的功能：“引用”字段、相关表、数据实体。</span><span class="sxs-lookup"><span data-stu-id="f9fc1-186">Deprecated: By April 1, 2021, we plan to no longer support functionality related to Standard main accounts: Reference field, related table, data entity.</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a><span data-ttu-id="f9fc1-187">Finance 10.0.7 版本中已经删除或弃用的功能</span><span class="sxs-lookup"><span data-stu-id="f9fc1-187">Features removed or deprecated in the Finance 10.0.7 release</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="f9fc1-188">“工作流请求更改”对话框中不再包含用户选择下拉列表</span><span class="sxs-lookup"><span data-stu-id="f9fc1-188">Workflow request change dialog box no longer includes user selection drop-down list</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="f9fc1-189">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="f9fc1-189">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="f9fc1-190">更改为带帐户组选择的功能。</span><span class="sxs-lookup"><span data-stu-id="f9fc1-190">Changed to the feature with account groups selection.</span></span>  |
| <span data-ttu-id="f9fc1-191">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="f9fc1-191">**Replaced by another feature?**</span></span>   | <span data-ttu-id="f9fc1-192">是</span><span class="sxs-lookup"><span data-stu-id="f9fc1-192">Yes</span></span> |
| <span data-ttu-id="f9fc1-193">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="f9fc1-193">**Product areas affected**</span></span>         | <span data-ttu-id="f9fc1-194">工作流</span><span class="sxs-lookup"><span data-stu-id="f9fc1-194">Workflow</span></span> |
| <span data-ttu-id="f9fc1-195">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="f9fc1-195">**Deployment option**</span></span>              | <span data-ttu-id="f9fc1-196">所有</span><span class="sxs-lookup"><span data-stu-id="f9fc1-196">All</span></span> |
| <span data-ttu-id="f9fc1-197">**状态**</span><span class="sxs-lookup"><span data-stu-id="f9fc1-197">**Status**</span></span>                         | <span data-ttu-id="f9fc1-198">弃用：到 2020 年 12 月 1 日，我们计划不再支持不带帐户组选择的中国凭证类型设置。</span><span class="sxs-lookup"><span data-stu-id="f9fc1-198">Deprecated: By December 1, 2020, we plan to no longer support Chinese voucher types setup without Account groups selection.</span></span> <span data-ttu-id="f9fc1-199">请在 [10.0.7 的新增功能](whats-new-changed-10-0-7.md)中查找有关新设计的更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="f9fc1-199">Find more details about the new design in [What's new in 10.0.7](whats-new-changed-10-0-7.md).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="f9fc1-200">之前有关已删除或已弃用功能的声明</span><span class="sxs-lookup"><span data-stu-id="f9fc1-200">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="f9fc1-201">若要了解有关早期版本中已删除或已弃用功能的详细信息，请参阅[早期版本中已删除或已弃用的功能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md)。</span><span class="sxs-lookup"><span data-stu-id="f9fc1-201">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span></span>

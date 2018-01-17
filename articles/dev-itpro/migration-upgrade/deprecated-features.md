---
title: "弃用功能"
description: "本主题介绍已经删除或计划删除的功能。"
author: sericks007
manager: AnnBe
ms.date: 11/28/2017
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
ms.sourcegitcommit: 0ca19ab9ed7a52328c5dd5252c418bb9343bdc2b
ms.openlocfilehash: addd8c62ba034b47d8abbec29fa8682deb9698b1
ms.contentlocale: zh-cn
ms.lasthandoff: 12/14/2017

---

# <a name="removed-or-deprecated-features"></a><span data-ttu-id="b5304-103">已移除或弃用的功能</span><span class="sxs-lookup"><span data-stu-id="b5304-103">Removed or deprecated features</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b5304-104">本主题介绍已从 Dynamics 365 for Finance and Operations Enterprise Edition 移除或弃用的功能。</span><span class="sxs-lookup"><span data-stu-id="b5304-104">This topic describes features that have been removed or deprecated for Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

- <span data-ttu-id="b5304-105">*已移除*的功能在产品中不再可用。</span><span class="sxs-lookup"><span data-stu-id="b5304-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="b5304-106">*已弃用*的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="b5304-107">此列表旨在帮助您在您自己的计划中考虑这些功能的移除和弃用。</span><span class="sxs-lookup"><span data-stu-id="b5304-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!Note]
> <span data-ttu-id="b5304-108">从具有平台更新 8 的 Dynamics 365 for Finance and Operations Enterprise Edition 2017 年 7 月版开始，每一个已移除或弃用的功能均备注了部署类型。</span><span class="sxs-lookup"><span data-stu-id="b5304-108">Starting with the Dynamics 365 for Finance and Operations, Enterprise edition July 2017 release with platform update 8, the type of deployments are noted for each removed or deprecated feature.</span></span> <span data-ttu-id="b5304-109">本主题中提及的所有之前的版本仅支持云部署。</span><span class="sxs-lookup"><span data-stu-id="b5304-109">All of the previous releases mentioned in this topic supported cloud deployments only.</span></span>

## <a name="dynamics-365-for-finance-and-operations-enterprise-edition-73-with-platform-update-12"></a><span data-ttu-id="b5304-110">具有平台更新 12 的 Dynamics 365 for Finance and Operations Enterprise Edition 7.3</span><span class="sxs-lookup"><span data-stu-id="b5304-110">Dynamics 365 for Finance and Operations, Enterprise edition 7.3 with platform update 12</span></span>

### <a name="extension-of-the-list-of-electronic-reporting-er-functions"></a><span data-ttu-id="b5304-111">电子申报 (ER) 功能列表扩展</span><span class="sxs-lookup"><span data-stu-id="b5304-111">Extension of the list of Electronic reporting (ER) functions</span></span>
<span data-ttu-id="b5304-112">可以引入在 ER 表达式生成器中使用的自定义功能（有关详细信息，请参阅[扩展电子申报功能列表](../../dev-itpro/analytics/general-electronic-reporting-formulas-list-extension.md)）的这一特性不再受支持。</span><span class="sxs-lookup"><span data-stu-id="b5304-112">The possibility to introduce custom functions to be used in the ER expression builder (for more information, see [Extend the list of Electronic reporting functions](../../dev-itpro/analytics/general-electronic-reporting-formulas-list-extension.md)) is not supported any more.</span></span> <span data-ttu-id="b5304-113">由于 ER API 发生变更，从 ER 表达式生成器调用内置函数的 API 变成内部 API，并且无法再进行扩展。</span><span class="sxs-lookup"><span data-stu-id="b5304-113">Due to changes of the ER APIs, the API to call built-in functions from the ER expression builder became internal and can’t be extended any longer.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-114">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-114">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-115">代码密封计划</span><span class="sxs-lookup"><span data-stu-id="b5304-115">Code sealing initiative</span></span>  |
| <span data-ttu-id="b5304-116">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-116">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-117">无。</span><span class="sxs-lookup"><span data-stu-id="b5304-117">None.</span></span> <span data-ttu-id="b5304-118">每当需要一个新的内置函数时，必须向 ER 框架团队提交新扩展请求。</span><span class="sxs-lookup"><span data-stu-id="b5304-118">Whenever a new built-in function is needed, a new extension request must be addressed to the ER framework team.</span></span><br><br><span data-ttu-id="b5304-119">在 ER 团队开发请求的函数时，作为临时解决方案，可以将需要的逻辑作为一种自定义应用程序类方法进行编程。</span><span class="sxs-lookup"><span data-stu-id="b5304-119">As a temporary work around while the requested function is under development by the ER team, the required logic can be programmed as a method of a custom application class.</span></span> <span data-ttu-id="b5304-120">此方法可以作为引用该自定义应用程序类的**应用程序\类**类型的已添加 ER 数据源的属性在 ER 表达式中访问。</span><span class="sxs-lookup"><span data-stu-id="b5304-120">This method can be accessed in an ER expression as a property of the added ER data source of the **Application\Class** type that refers to that custom application class.</span></span>  |
| <span data-ttu-id="b5304-121">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-121">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-122">电子申报框架</span><span class="sxs-lookup"><span data-stu-id="b5304-122">Electronic reporting framework</span></span>                                                      |
| <span data-ttu-id="b5304-123">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="b5304-123">**Deployment option**</span></span>              | <span data-ttu-id="b5304-124">全部</span><span class="sxs-lookup"><span data-stu-id="b5304-124">All</span></span>                                                                                      |
| <span data-ttu-id="b5304-125">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-125">**Status**</span></span>                         | <span data-ttu-id="b5304-126">从 Dynamics 365 for Finance and Operations Enterprise Edition 7.3 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-126">Removed as of Dynamics 365 for Finance and Operations, Enterprise edition 7.3.</span></span>    |

### <a name="inventory-by-item-group-and-inventory-by-inventory-dimension-aging-reports"></a><span data-ttu-id="b5304-127">按物料组的库存和按库存维度的库存帐龄分析表</span><span class="sxs-lookup"><span data-stu-id="b5304-127">Inventory by item group and Inventory by inventory dimension aging reports</span></span>

<span data-ttu-id="b5304-128">这两个分析表在 Finance and Operations 中不再受支持。</span><span class="sxs-lookup"><span data-stu-id="b5304-128">These two reports are no longer supported in Finance and Operations.</span></span> <span data-ttu-id="b5304-129">相反，可使用**库存帐龄**分析表改善用户体验。</span><span class="sxs-lookup"><span data-stu-id="b5304-129">Instead, the **Inventory aging** report can be used to improve the user experience.</span></span>

|   |  |
|--------------|-----------------------|
| <span data-ttu-id="b5304-130">**折旧的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-130">**Reason for deprecation**</span></span>       | <span data-ttu-id="b5304-131">重复的功能</span><span class="sxs-lookup"><span data-stu-id="b5304-131">Duplicate functionality</span></span>  |
| <span data-ttu-id="b5304-132">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-132">**Replaced by another feature?**</span></span> | <span data-ttu-id="b5304-133">是。</span><span class="sxs-lookup"><span data-stu-id="b5304-133">Yes.</span></span> <span data-ttu-id="b5304-134">这两个分析表已替换为**库存帐龄**分析表。</span><span class="sxs-lookup"><span data-stu-id="b5304-134">The two reports have been replaced by the **Inventory aging** report.</span></span>     |
| <span data-ttu-id="b5304-135">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-135">**Product areas affected**</span></span>       | <span data-ttu-id="b5304-136">库存管理、成本管理</span><span class="sxs-lookup"><span data-stu-id="b5304-136">Inventory management, Cost management</span></span>        |
| <span data-ttu-id="b5304-137">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="b5304-137">**Deployment option**</span></span>        | <span data-ttu-id="b5304-138">全部</span><span class="sxs-lookup"><span data-stu-id="b5304-138">All</span></span>|
| <span data-ttu-id="b5304-139">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-139">**Status**</span></span>                       | <span data-ttu-id="b5304-140">已弃用：两个分析表的菜单项在版本 7.3 中已移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-140">Deprecated: The menu items for the two reports have been removed in version 7.3.</span></span> <span data-ttu-id="b5304-141">但这些分析表的代码仍然保留在产品中。</span><span class="sxs-lookup"><span data-stu-id="b5304-141">However, the code for the reports remains in the product.</span></span> <span data-ttu-id="b5304-142">在将来的发行中计划移除该代码。</span><span class="sxs-lookup"><span data-stu-id="b5304-142">The plan is to remove the code in a future release.</span></span> |

### <a name="power-bi-content-packs-published-to-powerbicom"></a><span data-ttu-id="b5304-143">Power BI 内容包发布到 PowerBI.com</span><span class="sxs-lookup"><span data-stu-id="b5304-143">Power BI content packs published to PowerBI.com</span></span>
<span data-ttu-id="b5304-144">已发布到 PowerBI.com 站点的**成本管理**、**财务绩效**和**零售渠道绩效**内容包因为 Microsoft Power BI 中的产品更新而被弃用。</span><span class="sxs-lookup"><span data-stu-id="b5304-144">The **Cost management**, **Financial performance**, and **Retail channel performance** content packs, which were published to the PowerBI.com site, are deprecated as a consequence of product updates in Microsoft Power BI.</span></span> <span data-ttu-id="b5304-145">过去将这些内容包部署到 PowerBI.com 的系统管理窗体在 Finance and Operations 中也被弃用。</span><span class="sxs-lookup"><span data-stu-id="b5304-145">System administration forms used to deploy these content packs to PowerBI.com are also being deprecated in Finance and Operations.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-146">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-146">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-147">Microsoft Power BI 中进行产品更新。</span><span class="sxs-lookup"><span data-stu-id="b5304-147">Product updates in Microsoft Power BI.</span></span> |
| <span data-ttu-id="b5304-148">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-148">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-149">Power BI 内容包（发布到 PowerBI.com）由分析应用程序取代，该应用程序支持数据库级别的解决方案集成。</span><span class="sxs-lookup"><span data-stu-id="b5304-149">Power BI content packs (published to PowerBI.com) are being replaced by analytical applications which allow for solution integrations at the database level.</span></span> <span data-ttu-id="b5304-150">有关分析应用程序的详细信息，请参阅[工作区中的嵌入式 Power BI](../../dev-itpro/analytics/embed-power-bi-workspaces.md)。</span><span class="sxs-lookup"><span data-stu-id="b5304-150">For more information about analytical applications, see [Embedded Power BI in workspackes](../../dev-itpro/analytics/embed-power-bi-workspaces.md).</span></span>    |
| <span data-ttu-id="b5304-151">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-151">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-152">成本管理、财务和零售</span><span class="sxs-lookup"><span data-stu-id="b5304-152">Cost management, Finance, and Retail</span></span>                                                                                               |
| <span data-ttu-id="b5304-153">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="b5304-153">**Deployment option**</span></span>              | <span data-ttu-id="b5304-154">仅适用于云（在本地部署中不再支持与 PowerBI.com 集成）。</span><span class="sxs-lookup"><span data-stu-id="b5304-154">Cloud only (Integration with PowerBI.com is not supported in on-premises deployments.)</span></span>                                                                                                            |
| <span data-ttu-id="b5304-155">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-155">**Status**</span></span>                         | <span data-ttu-id="b5304-156">已弃用：移除功能的目标时间范围为 2018 年第二季度。</span><span class="sxs-lookup"><span data-stu-id="b5304-156">Deprecated: Target timeframe for the functionality removal is Q2 2018.</span></span>    |

### <a name="standard-ui-in-data-management-workspace"></a><span data-ttu-id="b5304-157">数据管理工作区中的标准 UI</span><span class="sxs-lookup"><span data-stu-id="b5304-157">Standard UI in data management workspace</span></span>

<span data-ttu-id="b5304-158">数据管理中的标准 UI 为旧 UI，是当用户访问数据管理工作区时呈现给用户的默认 UI。</span><span class="sxs-lookup"><span data-stu-id="b5304-158">The standard UI in data management is the legacy UI, which is the default UI presented to the users when they visit the data management workspace.</span></span>

|   |  |
|------------------|-------------------------|
| <span data-ttu-id="b5304-159">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-159">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-160">我们正努力在新的 UI 中为用户提供新的体验。</span><span class="sxs-lookup"><span data-stu-id="b5304-160">We are investing in providing new user experiences in the new UI.</span></span>             |
| <span data-ttu-id="b5304-161">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-161">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-162">新 UI 称为*增强型视图*，它将取代旧 UI。</span><span class="sxs-lookup"><span data-stu-id="b5304-162">The new UI called *Enhanced views* is replacing the old UI.</span></span>            |
| <span data-ttu-id="b5304-163">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-163">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-164">数据管理工作区</span><span class="sxs-lookup"><span data-stu-id="b5304-164">Data management workspace</span></span>                                                     |
| <span data-ttu-id="b5304-165">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="b5304-165">**Deployment option**</span></span>              | <span data-ttu-id="b5304-166">全部</span><span class="sxs-lookup"><span data-stu-id="b5304-166">All</span></span>                                                                           |
| <span data-ttu-id="b5304-167">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-167">**Status**</span></span>                         | <span data-ttu-id="b5304-168">已弃用：移除功能的目标时间范围为 2018 年第一季度。</span><span class="sxs-lookup"><span data-stu-id="b5304-168">Deprecated: Target timeframe for the functionality to be removed is Q1 2018.</span></span> |

### <a name="excise-sales-tax-service-tax-for-india"></a><span data-ttu-id="b5304-169">适用于印度的消费税、销售税、服务税</span><span class="sxs-lookup"><span data-stu-id="b5304-169">Excise, Sales Tax, Service Tax for India</span></span>

<span data-ttu-id="b5304-170">这些税项已归入印度 GST。</span><span class="sxs-lookup"><span data-stu-id="b5304-170">These taxes have been subsumed into Indian GST.</span></span>

|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b5304-171">**移除或弃用的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-171">**Reason for removal or deprecation**</span></span>       | <span data-ttu-id="b5304-172">这些税项已归入印度 GST。</span><span class="sxs-lookup"><span data-stu-id="b5304-172">These taxes have been subsumed into Indian GST.</span></span>                          |
| <span data-ttu-id="b5304-173">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-173">**Replaced by another feature?**</span></span>            | <span data-ttu-id="b5304-174">印度 GST</span><span class="sxs-lookup"><span data-stu-id="b5304-174">Indian GST</span></span>                                                              |
| <span data-ttu-id="b5304-175">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-175">**Product areas affected**</span></span>                  | <span data-ttu-id="b5304-176">税金</span><span class="sxs-lookup"><span data-stu-id="b5304-176">Tax</span></span>                                                                     |
| <span data-ttu-id="b5304-177">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="b5304-177">**Deployment option**</span></span>                       | <span data-ttu-id="b5304-178">所有模块</span><span class="sxs-lookup"><span data-stu-id="b5304-178">All modules</span></span>                                                   |
| <span data-ttu-id="b5304-179">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-179">**Status**</span></span>                                  | <span data-ttu-id="b5304-180">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-180">Deprecated: A removal date has not been set for this feature.</span></span> |    

### <a name="file-validation-utility-fvu-for-india"></a><span data-ttu-id="b5304-181">印度文件验证实用工具 (FVU)</span><span class="sxs-lookup"><span data-stu-id="b5304-181">File Validation Utility (FVU) for India</span></span>

|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b5304-182">**移除或弃用的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-182">**Reason for removal or deprecation**</span></span>       | <span data-ttu-id="b5304-183">缺少客户使用</span><span class="sxs-lookup"><span data-stu-id="b5304-183">Lack of customer usage</span></span>                                                  |
| <span data-ttu-id="b5304-184">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-184">**Replaced by another feature?**</span></span>            | <span data-ttu-id="b5304-185">无</span><span class="sxs-lookup"><span data-stu-id="b5304-185">No</span></span>                                                                      |
| <span data-ttu-id="b5304-186">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-186">**Product areas affected**</span></span>                  | <span data-ttu-id="b5304-187">印度预缴税金</span><span class="sxs-lookup"><span data-stu-id="b5304-187">Indian withholding tax</span></span>                                                  |
| <span data-ttu-id="b5304-188">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="b5304-188">**Deployment option**</span></span>                       | <span data-ttu-id="b5304-189">所有模块</span><span class="sxs-lookup"><span data-stu-id="b5304-189">All modules</span></span>                                                                    |
| <span data-ttu-id="b5304-190">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-190">**Status**</span></span>                                  | <span data-ttu-id="b5304-191">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-191">Deprecated: A removal date has not been set for this feature.</span></span>   |        

### <a name="tdstcs-certificate-for-india"></a><span data-ttu-id="b5304-192">印度 TDS/TCS 证书</span><span class="sxs-lookup"><span data-stu-id="b5304-192">TDS/TCS certificate for India</span></span>

<span data-ttu-id="b5304-193">用户可从政府门户下载。</span><span class="sxs-lookup"><span data-stu-id="b5304-193">Users can download this from the government portal.</span></span>

|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b5304-194">**移除或弃用的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-194">**Reason for removal or deprecation**</span></span>       | <span data-ttu-id="b5304-195">缺少客户使用</span><span class="sxs-lookup"><span data-stu-id="b5304-195">Lack of customer usage</span></span>                                                  |
| <span data-ttu-id="b5304-196">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-196">**Replaced by another feature?**</span></span>            | <span data-ttu-id="b5304-197">无</span><span class="sxs-lookup"><span data-stu-id="b5304-197">No</span></span>                                                                      |
| <span data-ttu-id="b5304-198">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-198">**Product areas affected**</span></span>                  | <span data-ttu-id="b5304-199">印度预缴税金</span><span class="sxs-lookup"><span data-stu-id="b5304-199">Indian withholding tax</span></span>                                                  |
| <span data-ttu-id="b5304-200">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="b5304-200">**Deployment option**</span></span>                       | <span data-ttu-id="b5304-201">所有模块</span><span class="sxs-lookup"><span data-stu-id="b5304-201">All modules</span></span>                                                                   |
| <span data-ttu-id="b5304-202">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-202">**Status**</span></span>                                  | <span data-ttu-id="b5304-203">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-203">Deprecated: A removal date has not been set for this feature.</span></span>     |    

### <a name="exportimport-exim-incentive-scheme-for-india"></a><span data-ttu-id="b5304-204">导出/导入 (EXIM) 印度激励方案</span><span class="sxs-lookup"><span data-stu-id="b5304-204">Export/import (EXIM) incentive scheme for India</span></span>


|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b5304-205">**移除或弃用的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-205">**Reason for removal or deprecation**</span></span>       | <span data-ttu-id="b5304-206">缺少客户使用</span><span class="sxs-lookup"><span data-stu-id="b5304-206">Lack of customer usage</span></span>                                                  |
| <span data-ttu-id="b5304-207">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-207">**Replaced by another feature?**</span></span>            | <span data-ttu-id="b5304-208">无</span><span class="sxs-lookup"><span data-stu-id="b5304-208">No</span></span>                                                                      |
| <span data-ttu-id="b5304-209">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-209">**Product areas affected**</span></span>                  | <span data-ttu-id="b5304-210">导入和导出</span><span class="sxs-lookup"><span data-stu-id="b5304-210">Import and export</span></span>                                                       |
| <span data-ttu-id="b5304-211">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="b5304-211">**Deployment option**</span></span>                       | <span data-ttu-id="b5304-212">所有模块</span><span class="sxs-lookup"><span data-stu-id="b5304-212">All modules</span></span>                                                                    |
| <span data-ttu-id="b5304-213">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-213">**Status**</span></span>                                  | <span data-ttu-id="b5304-214">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-214">Deprecated: A removal date has not been set for this feature.</span></span>  |    



## <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-with-platform-update-8"></a><span data-ttu-id="b5304-215">具有平台更新 8 的 Dynamics 365 for Finance and Operations Enterprise Edition 2017 年 7 月</span><span class="sxs-lookup"><span data-stu-id="b5304-215">Dynamics 365 for Finance and Operations, Enterprise edition July 2017 with platform update 8</span></span>

### <a name="warehouse-mobile-devices-portal"></a><span data-ttu-id="b5304-216">仓库移动设备门户</span><span class="sxs-lookup"><span data-stu-id="b5304-216">Warehouse mobile devices portal</span></span>

<span data-ttu-id="b5304-217">仓库移动设备门户 (WMDP) 是用于本地自行部署的单独组件。</span><span class="sxs-lookup"><span data-stu-id="b5304-217">Warehouse mobile devices portal (WMDP) was a standalone component that was intended for on-premises self-deployment.</span></span> <span data-ttu-id="b5304-218">此组件在 Finance and Operations 中不再受支持。</span><span class="sxs-lookup"><span data-stu-id="b5304-218">This component is no longer supported in Finance and Operations.</span></span> <span data-ttu-id="b5304-219">一个可提高用户体验的本机应用已替代 WMDP 的功能。</span><span class="sxs-lookup"><span data-stu-id="b5304-219">A native app that improves the user experience has replaced the functionality of WMDP.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-220">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-220">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-221">重复的功能。</span><span class="sxs-lookup"><span data-stu-id="b5304-221">Duplicate functionality.</span></span>       |
| <span data-ttu-id="b5304-222">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-222">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-223">是。</span><span class="sxs-lookup"><span data-stu-id="b5304-223">Yes.</span></span> <span data-ttu-id="b5304-224">此功能已经由 Finance and Operations - Warehousing 取代。</span><span class="sxs-lookup"><span data-stu-id="b5304-224">This feature has been replaced by Finance and Operations - Warehousing.</span></span> <span data-ttu-id="b5304-225">有关设置和先决条件的详细信息，请参阅 [安装和配置 Microsoft Dynamics 365 for Finance and Operations - Warehousing](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/install-configure-warehousing-app)。</span><span class="sxs-lookup"><span data-stu-id="b5304-225">For more information about setup and prerequisites, see [Install and configure Microsoft Dynamics 365 for Finance and Operations - Warehousing](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/install-configure-warehousing-app).</span></span> |
| <span data-ttu-id="b5304-226">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-226">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-227">仓库管理，运输管理</span><span class="sxs-lookup"><span data-stu-id="b5304-227">Warehouse management, Transportation management</span></span>     |
| <span data-ttu-id="b5304-228">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="b5304-228">**Deployment option**</span></span>              | <span data-ttu-id="b5304-229">仓库移动设备门户 (WMDP) 是用于本地自行部署的单独组件。</span><span class="sxs-lookup"><span data-stu-id="b5304-229">Warehouse mobile devices portal (WMDP) was a standalone component that was intended for on-premises self-deployment.</span></span>               |
| <span data-ttu-id="b5304-230">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-230">**Status**</span></span>                         | <span data-ttu-id="b5304-231">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-231">Deprecated: A removal date has not been set for this feature.</span></span>   |

### <a name="advanced-bank-reconciliation-matching-rule-for-manual-matching"></a><span data-ttu-id="b5304-232">用于手动匹配的高级银行对帐匹配规则</span><span class="sxs-lookup"><span data-stu-id="b5304-232">Advanced bank reconciliation matching rule for manual matching</span></span>

<span data-ttu-id="b5304-233">匹配规则用于在对帐工作表中手动匹配单据时选择和标记银行单据。</span><span class="sxs-lookup"><span data-stu-id="b5304-233">A matching rule was used to select and mark a bank document when documents were manually matched in the reconciliation worksheet.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-234">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-234">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-235">有限使用。</span><span class="sxs-lookup"><span data-stu-id="b5304-235">Limited usage.</span></span>                                                                         |
| <span data-ttu-id="b5304-236">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-236">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-237">编号</span><span class="sxs-lookup"><span data-stu-id="b5304-237">No.</span></span> <span data-ttu-id="b5304-238">应使用列筛选功能查找用于对帐的单据。</span><span class="sxs-lookup"><span data-stu-id="b5304-238">Column filtering capabilities should be used to find documents for reconciliation.</span></span> |
| <span data-ttu-id="b5304-239">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-239">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-240">现金和银行管理</span><span class="sxs-lookup"><span data-stu-id="b5304-240">Cash and bank management</span></span>                                                               |
| <span data-ttu-id="b5304-241">**部署选项**</span><span class="sxs-lookup"><span data-stu-id="b5304-241">**Deployment option**</span></span>              | <span data-ttu-id="b5304-242">全部</span><span class="sxs-lookup"><span data-stu-id="b5304-242">All</span></span>                                                                                    |
| <span data-ttu-id="b5304-243">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-243">**Status**</span></span>                         | <span data-ttu-id="b5304-244">从 2017 年 7 月开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-244">Removed as of July 2017.</span></span>                                                               |

## <a name="dynamics-365-for-operations-1611-with-platform-update-3"></a><span data-ttu-id="b5304-245">具有平台更新 3 的 Dynamics 365 for Operations 1611</span><span class="sxs-lookup"><span data-stu-id="b5304-245">Dynamics 365 for Operations 1611 with platform update 3</span></span>

### <a name="aeb-payment-formats-for-spain"></a><span data-ttu-id="b5304-246">西班牙的 AEB 付款格式</span><span class="sxs-lookup"><span data-stu-id="b5304-246">AEB payment formats for Spain</span></span>

<span data-ttu-id="b5304-247">Consejo Superior Bancario 付款格式过去用于将汇款文件发送到客户付款和供应商付款的银行。</span><span class="sxs-lookup"><span data-stu-id="b5304-247">The Consejo Superior Bancario payment formats were used to send remittance files to the bank for customer payments and vendor payments.</span></span> <span data-ttu-id="b5304-248">由 Asociación Española de Banca 确定这些格式的内容。</span><span class="sxs-lookup"><span data-stu-id="b5304-248">The content of these formats was determined by the Asociación Española de Banca.</span></span> <span data-ttu-id="b5304-249">它包含 Cuaderno 19、32、58、34。</span><span class="sxs-lookup"><span data-stu-id="b5304-249">It covers Cuaderno 19, 32, 58, 34.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-250">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-250">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-251">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="b5304-251">The payment formats are no longer used.</span></span>                                  |
| <span data-ttu-id="b5304-252">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-252">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-253">是，西班牙的 ISO20022 贷方转帐和直接借记付款格式</span><span class="sxs-lookup"><span data-stu-id="b5304-253">Yes, ISO20022 Credit transfer and Direct debit payment formats for Spain</span></span> |
| <span data-ttu-id="b5304-254">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-254">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-255">应付账款，应收账款</span><span class="sxs-lookup"><span data-stu-id="b5304-255">Accounts payable, Accounts receivable</span></span>                                    |
| <span data-ttu-id="b5304-256">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-256">**Status**</span></span>                         | <span data-ttu-id="b5304-257">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-257">Deprecated: A removal date has not been set for this feature.</span></span>           |

### <a name="bank-payments-transfer-for-lithuania"></a><span data-ttu-id="b5304-258">立陶宛银行付款转帐</span><span class="sxs-lookup"><span data-stu-id="b5304-258">Bank payments transfer for Lithuania</span></span>

<span data-ttu-id="b5304-259">过去使用立陶宛付款转账 (LT) 导出格式生成并打印银行付款转账。</span><span class="sxs-lookup"><span data-stu-id="b5304-259">Bank payment transfers were generated and printed by using the Payment transfer (LT) export format for Lithuania.</span></span> <span data-ttu-id="b5304-260">立陶宛市场于 2005 年开始使用 LITAS，统一电子银行系统。</span><span class="sxs-lookup"><span data-stu-id="b5304-260">The Lithuanian market began to use LITAS, the unified electronic banking system, in 2005.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-261">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-261">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-262">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="b5304-262">The payment formats are no longer used.</span></span>                        |
| <span data-ttu-id="b5304-263">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-263">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-264">是，立陶宛 ISO20022 贷方转帐付款格式</span><span class="sxs-lookup"><span data-stu-id="b5304-264">Yes, ISO20022 Credit transfer payment format for Lithuania</span></span>     |
| <span data-ttu-id="b5304-265">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-265">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-266">应付帐款</span><span class="sxs-lookup"><span data-stu-id="b5304-266">Accounts payable</span></span>                                               |
| <span data-ttu-id="b5304-267">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-267">**Status**</span></span>                         | <span data-ttu-id="b5304-268">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-268">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="bbs-direkte-remittering-payment-formats-for-norway"></a><span data-ttu-id="b5304-269">挪威 BBS Direkte Remittering 付款格式</span><span class="sxs-lookup"><span data-stu-id="b5304-269">BBS Direkte Remittering payment formats for Norway</span></span>

<span data-ttu-id="b5304-270">BBS Direkte Remittering 付款格式包括客户收款导出（直接借记）和返回消息导入。</span><span class="sxs-lookup"><span data-stu-id="b5304-270">BBS Direkte Remittering payment formats include customer payment collection export (direct debit) and return message import.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-271">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-271">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-272">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="b5304-272">The payment formats are no longer used.</span></span>  |
| <span data-ttu-id="b5304-273">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-273">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-274">挪威的 AvtaleGiro 客户付款格式可用于生成直接借记消息。</span><span class="sxs-lookup"><span data-stu-id="b5304-274">The AvtaleGiro customer payment format for Norway can be used to generate direct debit messages.</span></span> <span data-ttu-id="b5304-275">未来版本中将实施返回消息导入。</span><span class="sxs-lookup"><span data-stu-id="b5304-275">Return message import will be implemented in future releases.</span></span> |
| <span data-ttu-id="b5304-276">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-276">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-277">应付账款，应收账款</span><span class="sxs-lookup"><span data-stu-id="b5304-277">Accounts payable, Accounts receivable</span></span>   |
| <span data-ttu-id="b5304-278">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-278">**Status**</span></span>                         | <span data-ttu-id="b5304-279">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-279">Deprecated: A removal date has not been set for this feature.</span></span>                                                                                                 |

### <a name="chart-of-accounts-tool-for-spain"></a><span data-ttu-id="b5304-280">西班牙会计科目表工具</span><span class="sxs-lookup"><span data-stu-id="b5304-280">Chart of Accounts tool for Spain</span></span>

<span data-ttu-id="b5304-281">西班牙会计科目表要求重大更改时使用此工具。</span><span class="sxs-lookup"><span data-stu-id="b5304-281">This tool is used when a chart of accounts in Spain requires major changes.</span></span> <span data-ttu-id="b5304-282">用户可以导入新的 Microsoft Excel 或文本格式的会计科目表，也可以导入财务报表。</span><span class="sxs-lookup"><span data-stu-id="b5304-282">Users can import a new chart of accounts in Microsoft Excel or text format, and can also import financial statements.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-283">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-283">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-284">有限使用</span><span class="sxs-lookup"><span data-stu-id="b5304-284">Limited usage</span></span>                                                  |
| <span data-ttu-id="b5304-285">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-285">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-286">无</span><span class="sxs-lookup"><span data-stu-id="b5304-286">No</span></span>                                                             |
| <span data-ttu-id="b5304-287">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-287">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-288">总帐</span><span class="sxs-lookup"><span data-stu-id="b5304-288">General ledger</span></span>                                                 |
| <span data-ttu-id="b5304-289">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-289">**Status**</span></span>                         | <span data-ttu-id="b5304-290">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-290">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="dom80-payment-format-for-belgium"></a><span data-ttu-id="b5304-291">比利时的 Dom80 付款格式</span><span class="sxs-lookup"><span data-stu-id="b5304-291">Dom80 payment format for Belgium</span></span>

<span data-ttu-id="b5304-292">付款托收的比利时传统付款格式（直接借记）。</span><span class="sxs-lookup"><span data-stu-id="b5304-292">Legacy Belgian payment format for payment collection (direct debit).</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-293">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-293">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-294">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="b5304-294">The payment format is no longer used.</span></span>                          |
| <span data-ttu-id="b5304-295">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-295">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-296">是，比利时 ISO 20022 直接借记付款格式</span><span class="sxs-lookup"><span data-stu-id="b5304-296">Yes, ISO 20022 Direct debit payment format for Belgium</span></span>         |
| <span data-ttu-id="b5304-297">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-297">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-298">应收帐款</span><span class="sxs-lookup"><span data-stu-id="b5304-298">Accounts receivable</span></span>                                            |
| <span data-ttu-id="b5304-299">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-299">**Status**</span></span>                         | <span data-ttu-id="b5304-300">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-300">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="dtaezag-payment-formats-for-switzerland"></a><span data-ttu-id="b5304-301">瑞士的 DTA/EZAG 付款格式</span><span class="sxs-lookup"><span data-stu-id="b5304-301">DTA/EZAG payment formats for Switzerland</span></span>

<span data-ttu-id="b5304-302">DTA/EZAG 格式集成在 ESR 系统中，因为他们可以持有参考编号。</span><span class="sxs-lookup"><span data-stu-id="b5304-302">DTA/EZAG formats are integrated into the ESR system, because they can carry on the reference number.</span></span> <span data-ttu-id="b5304-303">由于参考编号不是必需的，因此可以使用这些格式处理任何供应商付款。</span><span class="sxs-lookup"><span data-stu-id="b5304-303">Because the reference number isn’t mandatory, these formats can be used to process any vendor payments.</span></span> <span data-ttu-id="b5304-304">银行帐户位置不在“Postfinance”的公司使用这些格式。</span><span class="sxs-lookup"><span data-stu-id="b5304-304">These formats are used by companies that have a bank account in a location other than “Postfinance.”</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-305">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-305">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-306">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="b5304-306">The payment formats are no longer used.</span></span>                        |
| <span data-ttu-id="b5304-307">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-307">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-308">是，瑞士 ISO20022 贷方转帐付款格式</span><span class="sxs-lookup"><span data-stu-id="b5304-308">Yes, ISO20022 Credit transfer payment format for Switzerland</span></span>   |
| <span data-ttu-id="b5304-309">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-309">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-310">应付帐款</span><span class="sxs-lookup"><span data-stu-id="b5304-310">Accounts payable</span></span>                                               |
| <span data-ttu-id="b5304-311">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-311">**Status**</span></span>                         | <span data-ttu-id="b5304-312">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-312">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="edifact-dirdeb-payment-format-for-austria"></a><span data-ttu-id="b5304-313">奥地利 EDIFACT-DIRDEB 付款格式</span><span class="sxs-lookup"><span data-stu-id="b5304-313">EDIFACT-DIRDEB payment format for Austria</span></span>

<span data-ttu-id="b5304-314">付款托收的 EDIFACT-DIRDEB 付款格式（直接借记）。</span><span class="sxs-lookup"><span data-stu-id="b5304-314">EDIFACT-DIRDEB payment format for payment collection (direct debit).</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-315">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-315">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-316">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="b5304-316">The payment format is no longer used.</span></span>                          |
| <span data-ttu-id="b5304-317">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-317">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-318">是，奥地利 ISO 20022 直接借记付款格式</span><span class="sxs-lookup"><span data-stu-id="b5304-318">Yes, ISO 20022 Direct debit payment format for Austria</span></span>         |
| <span data-ttu-id="b5304-319">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-319">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-320">应收帐款</span><span class="sxs-lookup"><span data-stu-id="b5304-320">Accounts receivable</span></span>                                            |
| <span data-ttu-id="b5304-321">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-321">**Status**</span></span>                         | <span data-ttu-id="b5304-322">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-322">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="edivat-for-belgium"></a><span data-ttu-id="b5304-323">比利时的 EDIVAT</span><span class="sxs-lookup"><span data-stu-id="b5304-323">EDIVAT for Belgium</span></span>

<span data-ttu-id="b5304-324">EDIVAT 是比利时通过安全电子邮件进行电子申报的已过时的标准做法。</span><span class="sxs-lookup"><span data-stu-id="b5304-324">EDIVAT is an obsolete Belgian standard for electronic declaration via secure mail.</span></span> <span data-ttu-id="b5304-325">Microsoft Dynamics AX 2012 保留启用历史数据访问权限的只读解决方案。</span><span class="sxs-lookup"><span data-stu-id="b5304-325">Microsoft Dynamics AX 2012 retains the read-only solution to enable access to the historical data.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-326">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-326">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-327">此功能不再使用。</span><span class="sxs-lookup"><span data-stu-id="b5304-327">The functionality is no longer used.</span></span>                           |
| <span data-ttu-id="b5304-328">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-328">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-329">无</span><span class="sxs-lookup"><span data-stu-id="b5304-329">No</span></span>                                                             |
| <span data-ttu-id="b5304-330">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-330">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-331">总帐</span><span class="sxs-lookup"><span data-stu-id="b5304-331">General ledger</span></span>                                                 |
| <span data-ttu-id="b5304-332">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-332">**Status**</span></span>                         | <span data-ttu-id="b5304-333">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-333">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="egiro-edifact-cremul-payment-import-format-for-norway"></a><span data-ttu-id="b5304-334">挪威的 eGiro EDIFACT CREMUL 付款导入格式</span><span class="sxs-lookup"><span data-stu-id="b5304-334">eGiro EDIFACT CREMUL payment import format for Norway</span></span>

<span data-ttu-id="b5304-335">eGiro 基于国际 UN EDIFACT CREMUL（多重贷记通知消息）标准，用于客户付款的自动过帐。</span><span class="sxs-lookup"><span data-stu-id="b5304-335">eGiro is based on the international UN EDIFACT CREMUL (Multiple Credit Advice Message) standard that is used for automatic posting of customer payments.</span></span> <span data-ttu-id="b5304-336">在 Microsoft Dynamics AX 中，eGiro 作为客户付款导入格式实施。</span><span class="sxs-lookup"><span data-stu-id="b5304-336">In Microsoft Dynamics AX, eGiro is implemented as a customer payment import format.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-337">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-337">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-338">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="b5304-338">The payment format is no longer used.</span></span>                                                     |
| <span data-ttu-id="b5304-339">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-339">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-340">编号</span><span class="sxs-lookup"><span data-stu-id="b5304-340">No.</span></span> <span data-ttu-id="b5304-341">格式在未来版本中将被 ISO 20022 报表导入格式所取代。</span><span class="sxs-lookup"><span data-stu-id="b5304-341">The format will be replaced by ISO 20022 statement import formats in future releases.</span></span> |
| <span data-ttu-id="b5304-342">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-342">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-343">应收帐款</span><span class="sxs-lookup"><span data-stu-id="b5304-343">Accounts receivable</span></span>                                                                       |
| <span data-ttu-id="b5304-344">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-344">**Status**</span></span>                         | <span data-ttu-id="b5304-345">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-345">Deprecated: A removal date has not been set for this feature.</span></span>                            |

### <a name="external-inventory-for-poland"></a><span data-ttu-id="b5304-346">波兰的外部库存</span><span class="sxs-lookup"><span data-stu-id="b5304-346">External inventory for Poland</span></span>

<span data-ttu-id="b5304-347">来自供应商用于销售且无需购买的货物的证据。</span><span class="sxs-lookup"><span data-stu-id="b5304-347">Evidence of goods that are taken from a vendor for sales without purchase.</span></span> <span data-ttu-id="b5304-348">在外部库存中处理的货物不影响标准库存，可以销售，然后被自动购买。</span><span class="sxs-lookup"><span data-stu-id="b5304-348">Goods that are handled in external inventory don’t affect standard inventory, and can be sold and then purchased automatically.</span></span> <span data-ttu-id="b5304-349">此流程创建实际库存变动。</span><span class="sxs-lookup"><span data-stu-id="b5304-349">This process creates real inventory movements.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-350">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-350">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-351">替换为另一个功能</span><span class="sxs-lookup"><span data-stu-id="b5304-351">Replaced by another feature</span></span>                                    |
| <span data-ttu-id="b5304-352">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-352">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-353">是，为核心入站托运功能</span><span class="sxs-lookup"><span data-stu-id="b5304-353">Yes, the core Inbound consignment functionality</span></span>                |
| <span data-ttu-id="b5304-354">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-354">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-355">应付账款，库存管理</span><span class="sxs-lookup"><span data-stu-id="b5304-355">Accounts payable, Inventory management</span></span>                         |
| <span data-ttu-id="b5304-356">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-356">**Status**</span></span>                         | <span data-ttu-id="b5304-357">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-357">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="financial-reports-generator-for-eastern-europe"></a><span data-ttu-id="b5304-358">东欧的财务报表生成器</span><span class="sxs-lookup"><span data-stu-id="b5304-358">Financial reports generator for Eastern Europe</span></span>

<span data-ttu-id="b5304-359">用于设置会计和纳税报表的数据收集，以及用于将数据导出到 XLS 和 DOC 报表模板的工具。</span><span class="sxs-lookup"><span data-stu-id="b5304-359">A tool is used to set up data collection for accounting and tax reports, and to export data to XLS and DOC report templates.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-360">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-360">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-361">有限使用</span><span class="sxs-lookup"><span data-stu-id="b5304-361">Limited usage</span></span>                                                                            |
| <span data-ttu-id="b5304-362">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-362">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-363">编号</span><span class="sxs-lookup"><span data-stu-id="b5304-363">No.</span></span> <span data-ttu-id="b5304-364">工具在未来版本中将被电子申报配置所取代。</span><span class="sxs-lookup"><span data-stu-id="b5304-364">The tool will be replaced by Electronic reporting configurations in future releases.</span></span> |
| <span data-ttu-id="b5304-365">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-365">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-366">总帐</span><span class="sxs-lookup"><span data-stu-id="b5304-366">General Ledger</span></span>                                                                           |
| <span data-ttu-id="b5304-367">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-367">**Status**</span></span>                         | <span data-ttu-id="b5304-368">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-368">Deprecated: A removal date has not been set for this feature.</span></span>                           |

### <a name="import-of-customer-payment-transactions-for-finland"></a><span data-ttu-id="b5304-369">芬兰的客户付款交易记录导入</span><span class="sxs-lookup"><span data-stu-id="b5304-369">Import of customer payment transactions for Finland</span></span>

<span data-ttu-id="b5304-370">您可以为从银行提供的外部文件导入客户付款交易记录的芬兰付款选择导入格式。</span><span class="sxs-lookup"><span data-stu-id="b5304-370">You can select an import format for Finnish payments to import customer payment transactions from an external file that the bank provides.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-371">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-371">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-372">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="b5304-372">The payment format is no longer used.</span></span>                                                     |
| <span data-ttu-id="b5304-373">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-373">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-374">编号</span><span class="sxs-lookup"><span data-stu-id="b5304-374">No.</span></span> <span data-ttu-id="b5304-375">格式在未来版本中将被 ISO 20022 报表导入格式所取代。</span><span class="sxs-lookup"><span data-stu-id="b5304-375">The format will be replaced by ISO 20022 statement import formats in future releases.</span></span> |
| <span data-ttu-id="b5304-376">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-376">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-377">应收帐款</span><span class="sxs-lookup"><span data-stu-id="b5304-377">Accounts receivable</span></span>                                                                       |
| <span data-ttu-id="b5304-378">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-378">**Status**</span></span>                         | <span data-ttu-id="b5304-379">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-379">Deprecated: A removal date has not been set for this feature.</span></span>                            |

### <a name="import-of-payment-transactions-into-a-general-ledger-journal-for-finland"></a><span data-ttu-id="b5304-380">付款交易记录导入到芬兰的总帐日志帐中</span><span class="sxs-lookup"><span data-stu-id="b5304-380">Import of payment transactions into a general ledger journal for Finland</span></span>

<span data-ttu-id="b5304-381">用于芬兰将会计交易记录导入到总帐的特定格式。</span><span class="sxs-lookup"><span data-stu-id="b5304-381">A format that is specific to Finland is used to import accounting transactions into the general ledger.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-382">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-382">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-383">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="b5304-383">The payment format is no longer used.</span></span>                                                     |
| <span data-ttu-id="b5304-384">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-384">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-385">编号</span><span class="sxs-lookup"><span data-stu-id="b5304-385">No.</span></span> <span data-ttu-id="b5304-386">格式在未来版本中将被 ISO 20022 报表导入格式所取代。</span><span class="sxs-lookup"><span data-stu-id="b5304-386">The format will be replaced by ISO 20022 statement import formats in future releases.</span></span> |
| <span data-ttu-id="b5304-387">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-387">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-388">应收帐款</span><span class="sxs-lookup"><span data-stu-id="b5304-388">Accounts receivable</span></span>                                                                       |
| <span data-ttu-id="b5304-389">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-389">**Status**</span></span>                         | <span data-ttu-id="b5304-390">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-390">Deprecated: A removal date has not been set for this feature.</span></span>                            |

### <a name="integration-with-isabel-synchronized-cis-for-belgium"></a><span data-ttu-id="b5304-391">比利时与 Isabel 同步 (CIS) 集成</span><span class="sxs-lookup"><span data-stu-id="b5304-391">Integration with Isabel synchronized (CIS) for Belgium</span></span>

<span data-ttu-id="b5304-392">Isabel 是欧洲电子银行的框架和比利时的事实标准。</span><span class="sxs-lookup"><span data-stu-id="b5304-392">Isabel is the framework for electronic banking in Europe and is a de-facto standard in Belgium.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-393">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-393">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-394">与 Isabel 客户端的集成已停止。</span><span class="sxs-lookup"><span data-stu-id="b5304-394">Integration with Isabel client has been discontinued.</span></span>   |
| <span data-ttu-id="b5304-395">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-395">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-396">编号</span><span class="sxs-lookup"><span data-stu-id="b5304-396">No.</span></span> <span data-ttu-id="b5304-397">付款格式不再使用，被比利时的 ISO20022 贷方转帐付款格式所取代。</span><span class="sxs-lookup"><span data-stu-id="b5304-397">The payment formats that are no longer used are replaced by ISO20022 Credit transfer payment format for Belgium.</span></span> |
| <span data-ttu-id="b5304-398">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-398">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-399">应付帐款</span><span class="sxs-lookup"><span data-stu-id="b5304-399">Accounts payable</span></span>     |
| <span data-ttu-id="b5304-400">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-400">**Status**</span></span>                         | <span data-ttu-id="b5304-401">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-401">Deprecated: A removal date has not been set for this feature.</span></span>    |

### <a name="modifications-in-the-chart-of-accounts-and-accounting-rules-for-spain"></a><span data-ttu-id="b5304-402">修改西班牙的会计科目表和会计规则</span><span class="sxs-lookup"><span data-stu-id="b5304-402">Modifications in the chart of accounts and accounting rules for Spain</span></span>

<span data-ttu-id="b5304-403">此功能用于修改西班牙的会计科目表和会计规则。</span><span class="sxs-lookup"><span data-stu-id="b5304-403">This feature is used for changes in the chart of accounts and accounting rules in Spain.</span></span> <span data-ttu-id="b5304-404">它映射帐户，以帮助将旧的会计科目表转换到新的会计科目表，将上一个会计年度与新的会计年度相比较，即使是当它们过帐到不同的科目编号时。</span><span class="sxs-lookup"><span data-stu-id="b5304-404">It maps accounts to help transform the old chart of accounts into the new chart of accounts, and compares the previous fiscal year with the new fiscal year, even if they were posted to different account numbers.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-405">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-405">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-406">有限使用</span><span class="sxs-lookup"><span data-stu-id="b5304-406">Limited usage</span></span>                                                  |
| <span data-ttu-id="b5304-407">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-407">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-408">无</span><span class="sxs-lookup"><span data-stu-id="b5304-408">No</span></span>                                                             |
| <span data-ttu-id="b5304-409">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-409">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-410">总帐</span><span class="sxs-lookup"><span data-stu-id="b5304-410">General ledger</span></span>                                                 |
| <span data-ttu-id="b5304-411">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-411">**Status**</span></span>                         | <span data-ttu-id="b5304-412">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-412">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="pagamento-fornittori-vendor-payment-format"></a><span data-ttu-id="b5304-413">Pagamento Fornittori 供应商付款格式</span><span class="sxs-lookup"><span data-stu-id="b5304-413">Pagamento Fornittori vendor payment format</span></span>

<span data-ttu-id="b5304-414">传统意大利贷方转帐付款格式</span><span class="sxs-lookup"><span data-stu-id="b5304-414">Legacy Italian payment format for credit transfers.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-415">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-415">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-416">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="b5304-416">The payment format is no longer used.</span></span>                          |
| <span data-ttu-id="b5304-417">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-417">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-418">是，意大利 ISO20022 贷方转帐付款格式</span><span class="sxs-lookup"><span data-stu-id="b5304-418">Yes, ISO20022 Credit transfer payment format for Italy</span></span>         |
| <span data-ttu-id="b5304-419">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-419">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-420">应付帐款</span><span class="sxs-lookup"><span data-stu-id="b5304-420">Accounts payable</span></span>                                               |
| <span data-ttu-id="b5304-421">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-421">**Status**</span></span>                         | <span data-ttu-id="b5304-422">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-422">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="payment-export-formats-for-estonia"></a><span data-ttu-id="b5304-423">爱沙尼亚付款导出格式</span><span class="sxs-lookup"><span data-stu-id="b5304-423">Payment export formats for Estonia</span></span>

<span data-ttu-id="b5304-424">Telehansa 和 Teleservice 格式为银行付款导出使用。</span><span class="sxs-lookup"><span data-stu-id="b5304-424">The Telehansa and Teleservice formats are used for bank payment export.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-425">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-425">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-426">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="b5304-426">The payment formats are no longer used.</span></span>                        |
| <span data-ttu-id="b5304-427">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-427">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-428">是，爱沙尼亚 ISO20022 贷方转帐付款格式</span><span class="sxs-lookup"><span data-stu-id="b5304-428">Yes, ISO20022 Credit transfer payment format for Estonia</span></span>       |
| <span data-ttu-id="b5304-429">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-429">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-430">应付帐款</span><span class="sxs-lookup"><span data-stu-id="b5304-430">Accounts payable</span></span>                                               |
| <span data-ttu-id="b5304-431">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-431">**Status**</span></span>                         | <span data-ttu-id="b5304-432">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-432">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="payment-file-archive-for-norway"></a><span data-ttu-id="b5304-433">挪威付款文件存档</span><span class="sxs-lookup"><span data-stu-id="b5304-433">Payment file archive for Norway</span></span>

<span data-ttu-id="b5304-434">在生成付款文件时，文件存档自动存档所有创建的文件，甚至包括以前写入或读取的文件。</span><span class="sxs-lookup"><span data-stu-id="b5304-434">When payment files are generated, the file archive automatically archives all files that are created, even files that were previously written or read.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-435">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-435">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-436">替换为另一个功能</span><span class="sxs-lookup"><span data-stu-id="b5304-436">Replaced by another feature</span></span>                                        |
| <span data-ttu-id="b5304-437">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-437">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-438">是，电子申报已存档作业</span><span class="sxs-lookup"><span data-stu-id="b5304-438">Yes, Electronic reporting archived jobs</span></span>                            |
| <span data-ttu-id="b5304-439">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-439">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-440">应付账款，应收账款，组织管理</span><span class="sxs-lookup"><span data-stu-id="b5304-440">Accounts payable, Accounts receivable, Organization administration</span></span> |
| <span data-ttu-id="b5304-441">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-441">**Status**</span></span>                         | <span data-ttu-id="b5304-442">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-442">Deprecated: A removal date has not been set for this feature.</span></span>     |

### <a name="payment-import-formats-for-estonia"></a><span data-ttu-id="b5304-443">爱沙尼亚付款导入格式</span><span class="sxs-lookup"><span data-stu-id="b5304-443">Payment import formats for Estonia</span></span>

<span data-ttu-id="b5304-444">Telehansa 和 TeleTeenus 格式为银行付款导入使用。</span><span class="sxs-lookup"><span data-stu-id="b5304-444">The Telehansa and TeleTeenus formats are used for bank payment import.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-445">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-445">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-446">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="b5304-446">The payment formats are no longer used.</span></span>                                                    |
| <span data-ttu-id="b5304-447">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-447">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-448">编号</span><span class="sxs-lookup"><span data-stu-id="b5304-448">No.</span></span> <span data-ttu-id="b5304-449">格式在未来版本中将被 ISO 20022 报表导入格式所取代。</span><span class="sxs-lookup"><span data-stu-id="b5304-449">The formats will be replaced by ISO 20022 statement import formats in future releases.</span></span> |
| <span data-ttu-id="b5304-450">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-450">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-451">应收帐款</span><span class="sxs-lookup"><span data-stu-id="b5304-451">Accounts receivable</span></span>                                                                        |
| <span data-ttu-id="b5304-452">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-452">**Status**</span></span>                         | <span data-ttu-id="b5304-453">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-453">Deprecated: A removal date has not been set for this feature.</span></span>                             |

### <a name="payroll-information-in-human-resources"></a><span data-ttu-id="b5304-454">人力资源中的工资单信息</span><span class="sxs-lookup"><span data-stu-id="b5304-454">Payroll information in Human Resources</span></span>

<span data-ttu-id="b5304-455">人力资源工资单信息</span><span class="sxs-lookup"><span data-stu-id="b5304-455">Human Resources Payroll information</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-456">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-456">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-457">此功能已由工资单和人力资源页取代。</span><span class="sxs-lookup"><span data-stu-id="b5304-457">This functionality has been replaced by core Payroll and Human Resources pages.</span></span>  |
| <span data-ttu-id="b5304-458">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-458">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-459">**福利**、**收入**和已经位于美国工资单中的其他相关页已被重新配置，现在是核心人力资源配置的一部分，可帮助支持外部工资单处理。</span><span class="sxs-lookup"><span data-stu-id="b5304-459">**Benefits**, **Earnings**, and other related pages that were previously in US Payroll have been reconfigured, and are now part of the core Human Resources configuration to help support external payroll processing.</span></span> <span data-ttu-id="b5304-460">此功能可通过使用**人力资源 1** \> **工资单**配置键访问到。</span><span class="sxs-lookup"><span data-stu-id="b5304-460">This functionality is accessed by using the **Human Resources 1** \> **Payroll** configuration key.</span></span> |
| <span data-ttu-id="b5304-461">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-461">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-462">人力资源、工资单</span><span class="sxs-lookup"><span data-stu-id="b5304-462">Human Resources, Payroll</span></span>   |
| <span data-ttu-id="b5304-463">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-463">**Status**</span></span>                         | <span data-ttu-id="b5304-464">从 Dynamics 365 for Operations 版本 1611 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-464">Removed as of Dynamics 365 for Operations version 1611.</span></span>    |

### <a name="performance-management-goal-workflow"></a><span data-ttu-id="b5304-465">绩效管理目标工作流</span><span class="sxs-lookup"><span data-stu-id="b5304-465">Performance management goal workflow</span></span>

<span data-ttu-id="b5304-466">绩效管理包括目标管理和与绩效审核集成。</span><span class="sxs-lookup"><span data-stu-id="b5304-466">Performance management includes goal management and integration with performance reviews.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-467">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-467">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-468">绩效管理经过重新设计，减少了目标页数，以简化流程。</span><span class="sxs-lookup"><span data-stu-id="b5304-468">Performance management was redesigned, and the number of goal pages was reduced to simplify the process.</span></span>                 |
| <span data-ttu-id="b5304-469">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-469">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-470">编号</span><span class="sxs-lookup"><span data-stu-id="b5304-470">No.</span></span> <span data-ttu-id="b5304-471">目标通过经理自助服务门户对经理可见，并且可由经理进行更改和查看。</span><span class="sxs-lookup"><span data-stu-id="b5304-471">Goals are visible to managers through the Manager Self Service portal, and can be changed and viewed by the manager.</span></span> |
| <span data-ttu-id="b5304-472">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-472">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-473">人力资本管理</span><span class="sxs-lookup"><span data-stu-id="b5304-473">Human capital management</span></span>       |
| <span data-ttu-id="b5304-474">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-474">**Status**</span></span>                         | <span data-ttu-id="b5304-475">从 Dynamics 365 for Operations 版本 1611 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-475">Removed as of Dynamics 365 for Operations version 1611.</span></span>    |

### <a name="postgirot-and-postgirot-utland-payment-formats-for-sweden"></a><span data-ttu-id="b5304-476">瑞典的 Postgirot 和 Postgirot Utland 付款格式</span><span class="sxs-lookup"><span data-stu-id="b5304-476">Postgirot and Postgirot Utland payment formats for Sweden</span></span>

<span data-ttu-id="b5304-477">瑞典的 Postgirot 和 Postgirot Utland 付款格式。</span><span class="sxs-lookup"><span data-stu-id="b5304-477">Postgirot and Postgirot Utland payment formats for Sweden.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-478">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-478">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-479">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="b5304-479">The payment formats are no longer used.</span></span>                        |
| <span data-ttu-id="b5304-480">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-480">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-481">是，瑞典 ISO20022 贷方转帐付款格式</span><span class="sxs-lookup"><span data-stu-id="b5304-481">Yes, ISO20022 Credit transfer payment format for Sweden</span></span>        |
| <span data-ttu-id="b5304-482">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-482">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-483">应付帐款</span><span class="sxs-lookup"><span data-stu-id="b5304-483">Accounts payable</span></span>                                               |
| <span data-ttu-id="b5304-484">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-484">**Status**</span></span>                         | <span data-ttu-id="b5304-485">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-485">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="radio-frequency-identifier"></a><span data-ttu-id="b5304-486">射频标识</span><span class="sxs-lookup"><span data-stu-id="b5304-486">Radio frequency identifier</span></span>

<span data-ttu-id="b5304-487">无线射频标识 (RFID) 是一种使用电子标签存储标识数据的数据收集技术和一种捕获标识数据的无行视域需求阅读器。</span><span class="sxs-lookup"><span data-stu-id="b5304-487">Radio Frequency Identification (RFID) is a data-collection technology that uses electronic tags to store identification data and a no-line-of-sight requirement reader to capture the identification data.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-488">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-488">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-489">低客户使用率和有限功能集。</span><span class="sxs-lookup"><span data-stu-id="b5304-489">Low customer usage and a limited feature set.</span></span>   |
| <span data-ttu-id="b5304-490">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-490">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-491">无</span><span class="sxs-lookup"><span data-stu-id="b5304-491">No</span></span>                                              |
| <span data-ttu-id="b5304-492">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-492">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-493">库存管理</span><span class="sxs-lookup"><span data-stu-id="b5304-493">Inventory management</span></span>                            |
| <span data-ttu-id="b5304-494">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-494">**Status**</span></span>                         | <span data-ttu-id="b5304-495">从 Dynamics 365 for Operations 1611 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-495">Removed as of Dynamics 365 for Operations 1611.</span></span> |

### <a name="report-about-state-invoices-numbering-for-latvia"></a><span data-ttu-id="b5304-496">有关拉脱维亚国家发票编号的报表</span><span class="sxs-lookup"><span data-stu-id="b5304-496">Report about state invoices numbering for Latvia</span></span>

<span data-ttu-id="b5304-497">拉脱维亚法律提供有关销售发票应如何编号的特定规则。</span><span class="sxs-lookup"><span data-stu-id="b5304-497">Latvian legislation provides specific rules about the numbering of sales invoices.</span></span> <span data-ttu-id="b5304-498">此功能允许您基于用户或用户组向销售发票分配具体编号。</span><span class="sxs-lookup"><span data-stu-id="b5304-498">The functionality lets you assign specific numbers to sales invoices, based on the user or user group.</span></span> <span data-ttu-id="b5304-499">之后您可以生成报表或 XML 文件。</span><span class="sxs-lookup"><span data-stu-id="b5304-499">You can then generate a report or an XML file.</span></span> <span data-ttu-id="b5304-500">您还可以打印有关已使用发票编号的报表。</span><span class="sxs-lookup"><span data-stu-id="b5304-500">You can also print a report about invoice numbers that are used.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-501">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-501">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-502">国家发票编号不必再进行维护。</span><span class="sxs-lookup"><span data-stu-id="b5304-502">The state invoice numbering no longer has to be maintained.</span></span> <span data-ttu-id="b5304-503">不再要求有关已使用发票编号的报表。</span><span class="sxs-lookup"><span data-stu-id="b5304-503">The report about used invoice numbers is no longer required.</span></span> |
| <span data-ttu-id="b5304-504">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-504">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-505">无</span><span class="sxs-lookup"><span data-stu-id="b5304-505">No</span></span>       |
| <span data-ttu-id="b5304-506">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-506">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-507">应收帐款</span><span class="sxs-lookup"><span data-stu-id="b5304-507">Accounts receivable</span></span>    |
| <span data-ttu-id="b5304-508">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-508">**Status**</span></span>                         | <span data-ttu-id="b5304-509">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-509">Deprecated: A removal date has not been set for this feature.</span></span>  |

### <a name="set-up-the-names-of-the-manager-and-general-accountant-of-a-company-for-lithuania"></a><span data-ttu-id="b5304-510">设置立陶宛公司的经理和会计主管的姓名</span><span class="sxs-lookup"><span data-stu-id="b5304-510">Set up the names of the manager and general accountant of a company for Lithuania</span></span>

<span data-ttu-id="b5304-511">公司经理和会计主管的姓名可以在公司信息中指定，并用于不同的本地报表打印输出。</span><span class="sxs-lookup"><span data-stu-id="b5304-511">The names of the manager and the general accountant of a company can be specified in the company information and used in different local report printouts.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-512">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-512">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-513">替换为另一个功能</span><span class="sxs-lookup"><span data-stu-id="b5304-513">Replaced by another feature</span></span>                                     |
| <span data-ttu-id="b5304-514">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-514">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-515">是，专员设置可用于同一个目的。</span><span class="sxs-lookup"><span data-stu-id="b5304-515">Yes, the setup of officials can be used for the same purpose.</span></span>   |
| <span data-ttu-id="b5304-516">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-516">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-517">应付账款、应收账款、现金和银行管理</span><span class="sxs-lookup"><span data-stu-id="b5304-517">Accounts payable, Accounts receivable, Cash and bank management</span></span> |
| <span data-ttu-id="b5304-518">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-518">**Status**</span></span>                         | <span data-ttu-id="b5304-519">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-519">Deprecated: A removal date has not been set for this feature.</span></span>  |

### <a name="shipping-carrier-interface"></a><span data-ttu-id="b5304-520">装运承运人界面</span><span class="sxs-lookup"><span data-stu-id="b5304-520">Shipping carrier interface</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-521">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-521">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-522">重复的功能</span><span class="sxs-lookup"><span data-stu-id="b5304-522">Duplicate functionality</span></span>   |
| <span data-ttu-id="b5304-523">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-523">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-524">部分由运输管理取代</span><span class="sxs-lookup"><span data-stu-id="b5304-524">Partially replaced by Transportation management</span></span> |
| <span data-ttu-id="b5304-525">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-525">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-526">销售和市场营销、库存管理</span><span class="sxs-lookup"><span data-stu-id="b5304-526">Sales and marketing, Inventory management</span></span>  |
| <span data-ttu-id="b5304-527">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-527">**Status**</span></span>                         | <span data-ttu-id="b5304-528">从 Dynamics 365 for Operations 版本 1611 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-528">Removed as of Dynamics 365 for Operations version 1611.</span></span>  |

### <a name="telepay-payment-formats-for-norway"></a><span data-ttu-id="b5304-529">挪威 Telepay 付款格式</span><span class="sxs-lookup"><span data-stu-id="b5304-529">Telepay payment formats for Norway</span></span>

<span data-ttu-id="b5304-530">Telepay 付款格式包括供应商付款导出（贷方转帐）和客户付款托收（直接借记）。</span><span class="sxs-lookup"><span data-stu-id="b5304-530">Telepay payment formats include vendor payment export (credit transfer) and customer payment collection (direct debit).</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-531">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-531">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-532">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="b5304-532">The payment formats are no longer used.</span></span>                                                        |
| <span data-ttu-id="b5304-533">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-533">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-534">是，挪威的 ISO20022 贷方转帐付款格式和 AvtaleGiro 客户付款格式</span><span class="sxs-lookup"><span data-stu-id="b5304-534">Yes, ISO20022 Credit transfer payment format and AvtaleGiro customer payment format for Norway</span></span> |
| <span data-ttu-id="b5304-535">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-535">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-536">应付账款，应收账款</span><span class="sxs-lookup"><span data-stu-id="b5304-536">Accounts payable, Accounts receivable</span></span>                                                          |
| <span data-ttu-id="b5304-537">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-537">**Status**</span></span>                         | <span data-ttu-id="b5304-538">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-538">Deprecated: A removal date has not been set for this feature.</span></span>                                 |

### <a name="vendor-payment-export-formats-for-finland"></a><span data-ttu-id="b5304-539">芬兰的供应商付款导出格式</span><span class="sxs-lookup"><span data-stu-id="b5304-539">Vendor payment export formats for Finland</span></span>

<span data-ttu-id="b5304-540">两个导出付款格式可用于芬兰。</span><span class="sxs-lookup"><span data-stu-id="b5304-540">Two formats for exporting payments are available for Finland.</span></span> <span data-ttu-id="b5304-541">LM02 (FI) 用于国内付款，LUM2 (FI) 用于国外付款。</span><span class="sxs-lookup"><span data-stu-id="b5304-541">LM02 (FI) is used for domestic payments, and LUM2 (FI) is used for foreign payments.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-542">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-542">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-543">付款格式不再使用。</span><span class="sxs-lookup"><span data-stu-id="b5304-543">The payment formats are no longer used.</span></span>                        |
| <span data-ttu-id="b5304-544">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-544">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-545">是，芬兰 ISO20022 贷方转帐付款格式</span><span class="sxs-lookup"><span data-stu-id="b5304-545">Yes, ISO20022 Credit transfer payment format for Finland</span></span>       |
| <span data-ttu-id="b5304-546">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-546">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-547">应付帐款</span><span class="sxs-lookup"><span data-stu-id="b5304-547">Accounts payable</span></span>                                               |
| <span data-ttu-id="b5304-548">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-548">**Status**</span></span>                         | <span data-ttu-id="b5304-549">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-549">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="warehouse-management-ii"></a><span data-ttu-id="b5304-550">仓库管理 II</span><span class="sxs-lookup"><span data-stu-id="b5304-550">Warehouse management II</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-551">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-551">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-552">**库存管理**模块中可用的仓库管理 II 解决方案 (WMS II) 与在 Microsoft Dynamics AX 2012 R3 中发布的**仓库管理**模块中的功能重复。</span><span class="sxs-lookup"><span data-stu-id="b5304-552">The Warehouse management II solution (WMS II) that was available in the **Inventory management** module duplicates functionality that is in the **Warehouse management** module that was released in Microsoft Dynamics AX 2012 R3.</span></span>                                                                         |
| <span data-ttu-id="b5304-553">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-553">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-554">在 AX 2012 R3、Microsoft Dynamics AX 2012 R3 CU8 和 Dynamics AX 2012 R3 CU9 中发布的**仓库管理**模块取代仓库管理 II 功能。</span><span class="sxs-lookup"><span data-stu-id="b5304-554">The **Warehouse management** module that was released in AX 2012 R3, Microsoft Dynamics AX 2012 R3 CU8, and Dynamics AX 2012 R3 CU9 replaces the Warehouse management II features.</span></span> <span data-ttu-id="b5304-555">新模块具有比仓库管理 II 更高级的功能和更灵活的仓库管理流程。</span><span class="sxs-lookup"><span data-stu-id="b5304-555">The new module has more advanced features and more flexible warehouse management processes than Warehouse management II.</span></span> |
| <span data-ttu-id="b5304-556">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-556">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-557">库存管理、销售和市场营销、采购</span><span class="sxs-lookup"><span data-stu-id="b5304-557">Inventory management, Sales and marketing, Procurement and sourcing</span></span>   |
| <span data-ttu-id="b5304-558">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-558">**Status**</span></span>                         | <span data-ttu-id="b5304-559">从 Dynamics 365 for Operations 版本 1611 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-559">Removed as of Dynamics 365 for Operations version 1611.</span></span>    |

### <a name="worker-reminders-in-human-resources"></a><span data-ttu-id="b5304-560">人力资源中的工作人员提醒</span><span class="sxs-lookup"><span data-stu-id="b5304-560">Worker reminders in Human Resources</span></span>

<span data-ttu-id="b5304-561">人力资源工资单信息</span><span class="sxs-lookup"><span data-stu-id="b5304-561">Human Resources Payroll information</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-562">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-562">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-563">低使用率</span><span class="sxs-lookup"><span data-stu-id="b5304-563">Low usage</span></span>                                                           |
| <span data-ttu-id="b5304-564">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-564">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-565">无</span><span class="sxs-lookup"><span data-stu-id="b5304-565">No</span></span>                                                                  |
| <span data-ttu-id="b5304-566">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-566">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-567">人力资源</span><span class="sxs-lookup"><span data-stu-id="b5304-567">Human resources</span></span>                                                     |
| <span data-ttu-id="b5304-568">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-568">**Status**</span></span>                         | <span data-ttu-id="b5304-569">从 Dynamics 365 for Operations 版本 1611 开始移除</span><span class="sxs-lookup"><span data-stu-id="b5304-569">Removed as of Dynamics 365 for Operations version 1611</span></span> |

### <a name="workflow-for-creating-goals"></a><span data-ttu-id="b5304-570">创建目标的工作流</span><span class="sxs-lookup"><span data-stu-id="b5304-570">Workflow for creating goals</span></span>

<span data-ttu-id="b5304-571">管理员工目标创建的工作流是多个可用工作流的其中一个，帮助协调绩效管理流程。</span><span class="sxs-lookup"><span data-stu-id="b5304-571">A workflow for managing the creation of employee goals is one of several workflows that were available to help coordinate the performance management process.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-572">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-572">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-573">绩效管理在 Microsoft Dynamics 365 for Finance and Operations 中已经完全重新设计。</span><span class="sxs-lookup"><span data-stu-id="b5304-573">Performance management has been completely redesigned in Microsoft Dynamics 365 for Finance and Operations.</span></span>     |
| <span data-ttu-id="b5304-574">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-574">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-575">经过重新设计的绩效管理功能能够更好地控制目标内容、用来跟踪进度的衡量指标以及支持文档的附加。</span><span class="sxs-lookup"><span data-stu-id="b5304-575">The redesigned Performance management feature gives more control over the content of the goals, the measurements that are used to track progress, and the attachment of supporting documentation.</span></span> <span data-ttu-id="b5304-576">目标可以存储为模板并重复使用。</span><span class="sxs-lookup"><span data-stu-id="b5304-576">Goals can be stored as templates and then reused.</span></span> <span data-ttu-id="b5304-577">此功能可以帮助您更加快速地为您的员工设置额外目标。</span><span class="sxs-lookup"><span data-stu-id="b5304-577">This feature can help you set up additional goals for your employees more quickly.</span></span> |
| <span data-ttu-id="b5304-578">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-578">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-579">人力资本管理</span><span class="sxs-lookup"><span data-stu-id="b5304-579">Human capital management</span></span>                 |
| <span data-ttu-id="b5304-580">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-580">**Status**</span></span>                         | <span data-ttu-id="b5304-581">从 Dynamics 365 for Operations 版本 1611 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-581">Removed as of Dynamics 365 for Operations version 1611.</span></span> |

## <a name="dynamics-ax-70"></a><span data-ttu-id="b5304-582">Dynamics AX 7.0</span><span class="sxs-lookup"><span data-stu-id="b5304-582">Dynamics AX 7.0</span></span> 


### <a name="ability-to-cancel-changes-to-a-vendor-invoice"></a><span data-ttu-id="b5304-583">能够取消对供应商发票的更改</span><span class="sxs-lookup"><span data-stu-id="b5304-583">Ability to cancel changes to a vendor invoice</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-584">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-584">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-585">性能改进</span><span class="sxs-lookup"><span data-stu-id="b5304-585">Performance enhancement</span></span>        |
| <span data-ttu-id="b5304-586">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-586">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-587">无</span><span class="sxs-lookup"><span data-stu-id="b5304-587">No</span></span>                             |
| <span data-ttu-id="b5304-588">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-588">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-589">应付帐款</span><span class="sxs-lookup"><span data-stu-id="b5304-589">Accounts payable</span></span>               |
| <span data-ttu-id="b5304-590">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-590">**Status**</span></span>                         | <span data-ttu-id="b5304-591">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-591">Removed as of Dynamics AX 7.0.</span></span> |

### <a name="aif-axd-and-axbc-integrations"></a><span data-ttu-id="b5304-592">AIF、Axd 和 AxBC 集成</span><span class="sxs-lookup"><span data-stu-id="b5304-592">AIF, AxD, and AxBC integrations</span></span>

<span data-ttu-id="b5304-593">在应用集成框架 (AIF) 中，数据可以通过显示为服务的业务逻辑与外部系统交换。</span><span class="sxs-lookup"><span data-stu-id="b5304-593">In Application Integration Framework (AIF), data can be exchanged with external systems through business logic that is exposed as services.</span></span> <span data-ttu-id="b5304-594">Dynamics AX 包括基于文档和 .NET Business Connector (AxBC) 的服务。</span><span class="sxs-lookup"><span data-stu-id="b5304-594">Dynamics AX includes services that are based on documents and .NET Business Connector (AxBC).</span></span> <span data-ttu-id="b5304-595">文档是通过使用 XML 创建的。</span><span class="sxs-lookup"><span data-stu-id="b5304-595">A document is created by using XML.</span></span> <span data-ttu-id="b5304-596">XML 包括标题信息，添加该信息的目的是创建可在 Dynamics AX 内外传送的*消息*。</span><span class="sxs-lookup"><span data-stu-id="b5304-596">The XML includes header information that is added to create a *message* that can be transferred into or out of Dynamics AX.</span></span> <span data-ttu-id="b5304-597">文档的示例包括销售订单和采购订单。</span><span class="sxs-lookup"><span data-stu-id="b5304-597">Examples of documents include sales orders and purchase orders.</span></span> <span data-ttu-id="b5304-598">但是，几乎所有实体（例如客户）都可以被文档代表。</span><span class="sxs-lookup"><span data-stu-id="b5304-598">However, almost any entity, such as a customer, can be represented by a document.</span></span> <span data-ttu-id="b5304-599">基于文档的服务使用 **Axd \<文档\>**类。</span><span class="sxs-lookup"><span data-stu-id="b5304-599">Services that are based on documents use the **Axd \<Document\>** classes.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-600">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-600">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-601">AIF 和 AxDs 的体系结构不能扩展到云服务。</span><span class="sxs-lookup"><span data-stu-id="b5304-601">The architecture of AIF and AxDs could not be scaled to a cloud service.</span></span> <span data-ttu-id="b5304-602">批量导入有性能问题。</span><span class="sxs-lookup"><span data-stu-id="b5304-602">There were performance issues around bulk import.</span></span>                                        |
| <span data-ttu-id="b5304-603">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-603">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-604">此功能由数据导入/导出框架取代，该框架支持重复执行的批量导入/导出。</span><span class="sxs-lookup"><span data-stu-id="b5304-604">This feature is replaced by the Data Import/Export framework, which supports recurring bulk import/export.</span></span> <span data-ttu-id="b5304-605">对于 AxBC，我们建议您使用实际表。</span><span class="sxs-lookup"><span data-stu-id="b5304-605">For AxBC, we recommend that you use the actual tables.</span></span> |
| <span data-ttu-id="b5304-606">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-606">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-607">AxDs、AxBC 和 AIF</span><span class="sxs-lookup"><span data-stu-id="b5304-607">AxDs, AxBCs, and AIF</span></span>   |
| <span data-ttu-id="b5304-608">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-608">**Status**</span></span>                         | <span data-ttu-id="b5304-609">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-609">Removed as of Dynamics AX 7.0.</span></span>   |

### <a name="boms-without-bom-versions"></a><span data-ttu-id="b5304-610">没有物料清单版本的物料清单</span><span class="sxs-lookup"><span data-stu-id="b5304-610">BOMs without BOM versions</span></span>

<span data-ttu-id="b5304-611">当禁用**物料清单版本**配置键时，物料清单版本在所有窗体中处于隐藏状态，系统将在已发布的产品和物料清单之间强制 1:1 关系。</span><span class="sxs-lookup"><span data-stu-id="b5304-611">When the **BOM versions** configuration key was disabled, bill of materials (BOM) versions were hidden in all forms, and the system forced a 1:1 relationship between released products and BOMs.</span></span> <span data-ttu-id="b5304-612">在 Dynamics AX 的当前版本中，**物料清单版本**配置键不能禁用。</span><span class="sxs-lookup"><span data-stu-id="b5304-612">In the current version of Dynamics AX, the **BOM versions** configuration key can't be disabled.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-613">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-613">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-614">使用配置键控制物料清单版本不会在云环境中扩展。</span><span class="sxs-lookup"><span data-stu-id="b5304-614">Using a configuration key to control BOM versions doesn't scale in a cloud environment.</span></span> |
| <span data-ttu-id="b5304-615">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-615">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-616">无</span><span class="sxs-lookup"><span data-stu-id="b5304-616">No</span></span>                                                                                      |
| <span data-ttu-id="b5304-617">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-617">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-618">产品信息管理、库存管理</span><span class="sxs-lookup"><span data-stu-id="b5304-618">Product information management, Inventory management</span></span>                                    |
| <span data-ttu-id="b5304-619">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-619">**Status**</span></span>                         | <span data-ttu-id="b5304-620">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-620">Removed as of Dynamics AX 7.0.</span></span>                                                          |

### <a name="brazilian-bordero"></a><span data-ttu-id="b5304-621">巴西 Bordero</span><span class="sxs-lookup"><span data-stu-id="b5304-621">Brazilian Bordero</span></span>

<span data-ttu-id="b5304-622">巴西公司的特定付款方式</span><span class="sxs-lookup"><span data-stu-id="b5304-622">Specific method of payment for Brazilian companies</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-623">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-623">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-624">对巴西 Bordero 付款方式的支持已经在巴西本地化中被中断。</span><span class="sxs-lookup"><span data-stu-id="b5304-624">Support for the Brazilian Bordero method of payment has been discontinued from Brazilian localization</span></span> |
| <span data-ttu-id="b5304-625">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-625">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-626">无</span><span class="sxs-lookup"><span data-stu-id="b5304-626">No</span></span>   |
| <span data-ttu-id="b5304-627">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-627">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-628">应付帐款</span><span class="sxs-lookup"><span data-stu-id="b5304-628">Accounts payable</span></span>   |
| <span data-ttu-id="b5304-629">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-629">**Status**</span></span>                         | <span data-ttu-id="b5304-630">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-630">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="brazilian-sintegra-statement"></a><span data-ttu-id="b5304-631">巴西 Sintegra 报表</span><span class="sxs-lookup"><span data-stu-id="b5304-631">Brazilian Sintegra statement</span></span>

<span data-ttu-id="b5304-632">ICMS 税联邦报税单</span><span class="sxs-lookup"><span data-stu-id="b5304-632">Federal tax statement for ICMS tax</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-633">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-633">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-634">此报表在巴西的部分州不再适用。</span><span class="sxs-lookup"><span data-stu-id="b5304-634">This statement is no longer applicable in some Brazilian states.</span></span> |
| <span data-ttu-id="b5304-635">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-635">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-636">编号</span><span class="sxs-lookup"><span data-stu-id="b5304-636">No.</span></span> <span data-ttu-id="b5304-637">在某些特定情况下，用户可以使用通用电子申报工具配置报表。</span><span class="sxs-lookup"><span data-stu-id="b5304-637">Users can use Generic Electronic reporting tool to configure the statement if required under specific situations.</span></span> |
| <span data-ttu-id="b5304-638">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-638">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-639">会计帐簿</span><span class="sxs-lookup"><span data-stu-id="b5304-639">Fiscal books</span></span>    |
| <span data-ttu-id="b5304-640">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-640">**Status**</span></span>                         | <span data-ttu-id="b5304-641">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-641">Deprecated: A removal date has not been set for this feature.</span></span>   |

### <a name="brazilian-scan-contingency-mode-for-nf-e"></a><span data-ttu-id="b5304-642">巴西的 SCAN NF-e 意外事故模式</span><span class="sxs-lookup"><span data-stu-id="b5304-642">Brazilian SCAN contingency mode for NF-e</span></span>

<span data-ttu-id="b5304-643">(SCAN) 意外事故环境用于在 Secretaria da Fazenda (SEFAZ) 环境不可用时生成、导出和导入 Nota Fiscal eletrônica (NF-e) 的状态。</span><span class="sxs-lookup"><span data-stu-id="b5304-643">(SCAN) contingency environment is used to generate, export, and import the status of a Nota Fiscal eletrônica (NF-e) when the environment of Secretaria da Fazenda (SEFAZ) is not available.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-644">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-644">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-645">此意外事故方法在巴西所有州中不再适用。</span><span class="sxs-lookup"><span data-stu-id="b5304-645">This method of contingency is no longer applicable in all Brazilian states</span></span> |
| <span data-ttu-id="b5304-646">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-646">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-647">无</span><span class="sxs-lookup"><span data-stu-id="b5304-647">No</span></span>                                                                          |
| <span data-ttu-id="b5304-648">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-648">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-649">应收帐款</span><span class="sxs-lookup"><span data-stu-id="b5304-649">Accounts receivable</span></span>                                                         |
| <span data-ttu-id="b5304-650">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-650">**Status**</span></span>                         | <span data-ttu-id="b5304-651">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-651">Deprecated: A removal date has not been set for this feature.</span></span>              |

### <a name="business-analyzer"></a><span data-ttu-id="b5304-652">业务分析器</span><span class="sxs-lookup"><span data-stu-id="b5304-652">Business Analyzer</span></span>

<span data-ttu-id="b5304-653">此移动应用程序能让用户查看关键业务度量。</span><span class="sxs-lookup"><span data-stu-id="b5304-653">This mobile application let users review key business metrics.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-654">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-654">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-655">此功能已被另一个功能取代。</span><span class="sxs-lookup"><span data-stu-id="b5304-655">This functionality has been replaced by another feature.</span></span>   |
| <span data-ttu-id="b5304-656">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-656">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-657">Microsoft Power BI 的监控财务业绩目录包将包括已经在 Business Analyzer 中可用的关键财务度量。</span><span class="sxs-lookup"><span data-stu-id="b5304-657">The Monitor financial performance content pack for Microsoft Power BI will include key financial metrics that were previously available in Business Analyzer.</span></span> |
| <span data-ttu-id="b5304-658">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-658">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-659">总帐</span><span class="sxs-lookup"><span data-stu-id="b5304-659">General ledger</span></span>      |
| <span data-ttu-id="b5304-660">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-660">**Status**</span></span>                         | <span data-ttu-id="b5304-661">已弃用：业务分析器的使用已被弃用。</span><span class="sxs-lookup"><span data-stu-id="b5304-661">Deprecated: The use of Business Analyzer has been deprecated.</span></span>    |

### <a name="business-statistics"></a><span data-ttu-id="b5304-662">业务统计</span><span class="sxs-lookup"><span data-stu-id="b5304-662">Business statistics</span></span>

<span data-ttu-id="b5304-663">设置业务统计查询，以帮助您分析组织的绩效</span><span class="sxs-lookup"><span data-stu-id="b5304-663">The setup of business statistics inquiries that can help you analyze the performance of the organization</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-664">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-664">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-665">商业智能 (BI)、低客户使用率和有限功能集的传统方法</span><span class="sxs-lookup"><span data-stu-id="b5304-665">Legacy approach to business intelligence (BI), low customer usage, and a limited feature set</span></span> |
| <span data-ttu-id="b5304-666">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-666">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-667">Dynamics AX 的当前版本的新 BI 解决方案</span><span class="sxs-lookup"><span data-stu-id="b5304-667">New BI solutions for the current version of Dynamics AX</span></span>                                      |
| <span data-ttu-id="b5304-668">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-668">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-669">采购、应付账款、销售和市场营销、应收账款</span><span class="sxs-lookup"><span data-stu-id="b5304-669">Procurement and sourcing, Accounts payable, Sales and marketing, Accounts receivable</span></span>         |
| <span data-ttu-id="b5304-670">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-670">**Status**</span></span>                         | <span data-ttu-id="b5304-671">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-671">Removed as of Dynamics AX 7.0.</span></span>                                                               |

### <a name="change-document-date-function-in-invoice-approval-journal"></a><span data-ttu-id="b5304-672">更改发票审核日记帐的单据日期功能</span><span class="sxs-lookup"><span data-stu-id="b5304-672">Change document date function in Invoice approval journal</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-673">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-673">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-674">低使用率</span><span class="sxs-lookup"><span data-stu-id="b5304-674">Low usage</span></span>                                                               |
| <span data-ttu-id="b5304-675">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-675">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-676">是。</span><span class="sxs-lookup"><span data-stu-id="b5304-676">Yes.</span></span> <span data-ttu-id="b5304-677">可以更改已过帐供应商交易记录的单据日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-677">The document date on the posted vendor transaction can be changed.</span></span> |
| <span data-ttu-id="b5304-678">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-678">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-679">应付帐款</span><span class="sxs-lookup"><span data-stu-id="b5304-679">Accounts payable</span></span>                                                        |
| <span data-ttu-id="b5304-680">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-680">**Status**</span></span>                         | <span data-ttu-id="b5304-681">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-681">Removed as of Dynamics AX 7.0.</span></span>                                          |

### <a name="clieop03-payment-format-for-the-netherlands"></a><span data-ttu-id="b5304-682">针对荷兰的 ClieOp03 付款格式</span><span class="sxs-lookup"><span data-stu-id="b5304-682">ClieOp03 payment format for the Netherlands</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-683">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-683">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-684">该格式不再适用于荷兰，因为它已被 SEPA 功能取代。</span><span class="sxs-lookup"><span data-stu-id="b5304-684">The format is no longer applicable in the Netherlands, because it has been replaced by SEPA functionality.</span></span> |
| <span data-ttu-id="b5304-685">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-685">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-686">SEPA 付款导出</span><span class="sxs-lookup"><span data-stu-id="b5304-686">SEPA payments export</span></span>  |
| <span data-ttu-id="b5304-687">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-687">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-688">所有模块</span><span class="sxs-lookup"><span data-stu-id="b5304-688">All modules</span></span>     |
| <span data-ttu-id="b5304-689">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-689">**Status**</span></span>                         | <span data-ttu-id="b5304-690">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-690">Deprecated: A removal date has not been set for this feature.</span></span>   |

### <a name="compliance-center"></a><span data-ttu-id="b5304-691">遵从性中心</span><span class="sxs-lookup"><span data-stu-id="b5304-691">Compliance Center</span></span>

<span data-ttu-id="b5304-692">遵从性中心是一个企业门户站点，用于管理与 Sarbanes-Oxley 法案有关的遵从性计划的文档要求。</span><span class="sxs-lookup"><span data-stu-id="b5304-692">The Compliance Center was an Enterprise Portal site for managing the documentation requirements for compliance initiatives that are related to the Sarbanes-Oxley law.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-693">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-693">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-694">缺少客户使用。</span><span class="sxs-lookup"><span data-stu-id="b5304-694">Lack of customer usage.</span></span> <span data-ttu-id="b5304-695">Microsoft SharePoint 包括和遵从性中心功能相同的功能。</span><span class="sxs-lookup"><span data-stu-id="b5304-695">Microsoft SharePoint includes the same capability that was available in the Compliance Center.</span></span> |
| <span data-ttu-id="b5304-696">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-696">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-697">无</span><span class="sxs-lookup"><span data-stu-id="b5304-697">No</span></span>   |
| <span data-ttu-id="b5304-698">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-698">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-699">符合性和内部控制</span><span class="sxs-lookup"><span data-stu-id="b5304-699">Compliance and internal controls</span></span>  |
| <span data-ttu-id="b5304-700">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-700">**Status**</span></span>                         | <span data-ttu-id="b5304-701">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-701">Removed as of Dynamics AX 7.0.</span></span>    |

### <a name="connector-for-microsoft-dynamics"></a><span data-ttu-id="b5304-702">Connector for Microsoft Dynamics</span><span class="sxs-lookup"><span data-stu-id="b5304-702">Connector for Microsoft Dynamics</span></span>

<span data-ttu-id="b5304-703">此工具用于集成从 Microsoft Dynamics CRM 到 Microsoft Dynamics ERP 应用程序的重要数据。</span><span class="sxs-lookup"><span data-stu-id="b5304-703">This tool was used to integrate key data from Microsoft Dynamics CRM to Microsoft Dynamics ERP applications.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-704">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-704">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-705">此功能已被另一个功能取代。</span><span class="sxs-lookup"><span data-stu-id="b5304-705">This functionality has been replaced by another feature.</span></span> |
| <span data-ttu-id="b5304-706">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-706">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-707">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="b5304-707">Common data service</span></span>                                      |
| <span data-ttu-id="b5304-708">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-708">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-709">Connector for Microsoft Dynamics</span><span class="sxs-lookup"><span data-stu-id="b5304-709">Connector for Microsoft Dynamics</span></span>                         |
| <span data-ttu-id="b5304-710">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-710">**Status**</span></span>                         | <span data-ttu-id="b5304-711">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-711">Removed as of Dynamics AX 7.0.</span></span>                           |

### <a name="container-unit-and-multi-dimension-on-hand"></a><span data-ttu-id="b5304-712">容器单位和多维现有量</span><span class="sxs-lookup"><span data-stu-id="b5304-712">Container unit and multi dimension on-hand</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-713">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-713">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-714">重复的功能</span><span class="sxs-lookup"><span data-stu-id="b5304-714">Duplicate functionality</span></span> |
| <span data-ttu-id="b5304-715">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-715">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-716">是。</span><span class="sxs-lookup"><span data-stu-id="b5304-716">Yes.</span></span> <span data-ttu-id="b5304-717">自 AX 2012 起，此功能已由合并的批次订单功能集替换。</span><span class="sxs-lookup"><span data-stu-id="b5304-717">Since AX 2012, this functionality has been replaced by the consolidated batch orders feature set.</span></span> <span data-ttu-id="b5304-718">此功能集包括合并的现有量视图。</span><span class="sxs-lookup"><span data-stu-id="b5304-718">This feature set includes the consolidated on-hand view.</span></span> |
| <span data-ttu-id="b5304-719">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-719">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-720">产品信息控制管理、生产控制、库存管理、销售和市场营销</span><span class="sxs-lookup"><span data-stu-id="b5304-720">Product information management, Production control, Inventory management, Sales and marketing</span></span>  |
| <span data-ttu-id="b5304-721">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-721">**Status**</span></span>                         | <span data-ttu-id="b5304-722">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-722">Removed as of Dynamics AX 7.0.</span></span> |

### <a name="cue-group-metadata"></a><span data-ttu-id="b5304-723">提示组元数据</span><span class="sxs-lookup"><span data-stu-id="b5304-723">Cue group metadata</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-724">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-724">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-725">提示组用于在 FactBox 区域中显示一个或多个提示。</span><span class="sxs-lookup"><span data-stu-id="b5304-725">Cue groups were used to display one or more Cues in the FactBox area.</span></span> <span data-ttu-id="b5304-726">由于父窗体中的记录更改会导致提示组中每个提示对应一个查询，因此它的接受程度有限，而且还存在性能顾虑。</span><span class="sxs-lookup"><span data-stu-id="b5304-726">There was limited uptake, and there were also performance concerns, because a record change in a parent form caused one query per Cue in the Cue group.</span></span> |
| <span data-ttu-id="b5304-727">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-727">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-728">无</span><span class="sxs-lookup"><span data-stu-id="b5304-728">No</span></span>      |
| <span data-ttu-id="b5304-729">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-729">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-730">所有模块</span><span class="sxs-lookup"><span data-stu-id="b5304-730">All modules</span></span>    |
| <span data-ttu-id="b5304-731">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-731">**Status**</span></span>                         | <span data-ttu-id="b5304-732">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-732">Removed as of Dynamics AX 7.0.</span></span>  |

### <a name="cue-metadata"></a><span data-ttu-id="b5304-733">提示元数据</span><span class="sxs-lookup"><span data-stu-id="b5304-733">Cue metadata</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-734">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-734">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-735">提示元数据仅限于计数或合计信息。</span><span class="sxs-lookup"><span data-stu-id="b5304-735">Cue metadata was limited to count or sum information.</span></span>    |
| <span data-ttu-id="b5304-736">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-736">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-737">引入了磁贴元数据，可为建模提供更多灵活性。</span><span class="sxs-lookup"><span data-stu-id="b5304-737">Tile metadata was introduced to provide more flexibility for modeling.</span></span> <span data-ttu-id="b5304-738">例如，您可以对当前计数、导航和关键绩效指标 (KPI) 进行建模。</span><span class="sxs-lookup"><span data-stu-id="b5304-738">For example, you can model current counts, navigation, and key performance indicators (KPIs).</span></span> <span data-ttu-id="b5304-739">计数磁贴元数据是提示元数据的直接取代。</span><span class="sxs-lookup"><span data-stu-id="b5304-739">Count tile metadata is the direct replacement of the Cue metadata.</span></span> |
| <span data-ttu-id="b5304-740">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-740">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-741">所有模块</span><span class="sxs-lookup"><span data-stu-id="b5304-741">All modules</span></span>           |
| <span data-ttu-id="b5304-742">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-742">**Status**</span></span>                         | <span data-ttu-id="b5304-743">从 Dynamics AX 7.0 开始移除</span><span class="sxs-lookup"><span data-stu-id="b5304-743">Removed as of Dynamics AX 7.0</span></span>      |

### <a name="danish-check-format"></a><span data-ttu-id="b5304-744">丹麦支票格式</span><span class="sxs-lookup"><span data-stu-id="b5304-744">Danish check format</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-745">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-745">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-746">对丹麦支票格式布局的支持已终止，并且报告已经从 DK 本地化中删除。</span><span class="sxs-lookup"><span data-stu-id="b5304-746">Support for the Danish check format layout has been discontinued, and the report has been removed from DK localization.</span></span> |
| <span data-ttu-id="b5304-747">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-747">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-748">无</span><span class="sxs-lookup"><span data-stu-id="b5304-748">No</span></span>    |
| <span data-ttu-id="b5304-749">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-749">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-750">所有模块</span><span class="sxs-lookup"><span data-stu-id="b5304-750">All modules</span></span>    |
| <span data-ttu-id="b5304-751">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-751">**Status**</span></span>                         | <span data-ttu-id="b5304-752">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-752">Deprecated: A removal date has not been set for this feature.</span></span>  |

### <a name="data-partitions"></a><span data-ttu-id="b5304-753">数据分区</span><span class="sxs-lookup"><span data-stu-id="b5304-753">Data partitions</span></span>

<span data-ttu-id="b5304-754">数据分区在 Microsoft Dynamics AX 数据库中提供数据的逻辑界定。</span><span class="sxs-lookup"><span data-stu-id="b5304-754">Data partitions provide a logical separation of data in the Microsoft Dynamics AX database.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-755">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-755">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-756">数据分区在 Microsoft Dynamics AX 2012 R2 引入以启用数据隔离。</span><span class="sxs-lookup"><span data-stu-id="b5304-756">Data partitions were introduced in Microsoft Dynamics AX 2012 R2 to enable data isolation.</span></span> <span data-ttu-id="b5304-757">在常见情况中，公司有子公司，一个子公司的数据不应对另一个子公司可见，即使两个子公司均由相同的 IT 部门管理。</span><span class="sxs-lookup"><span data-stu-id="b5304-757">In a common scenario, a company has subsidiaries, and the data from one subsidiary should not be visible to another subsidiary, even though both subsidiaries are managed by the same IT department.</span></span> <span data-ttu-id="b5304-758">不过，整个程序都需要额外的脚本和管理开销来创建新的分区并填充数据，以及备份分区数据。</span><span class="sxs-lookup"><span data-stu-id="b5304-758">However, extra scripts and management overhead throughout the program were required in order to create new partitions and populate them with data, and to back up partition data.</span></span> <span data-ttu-id="b5304-759">在云中，在其中我们有访问平台即服务 (PaaS) 数据库服务（Microsoft SQL Azure 数据库）的权限，则使用数据库作为隔离容器比在程序中执行隔离要高效得多。</span><span class="sxs-lookup"><span data-stu-id="b5304-759">In the cloud, where we have access to platform as a service (PaaS) database services (Microsoft Azure SQL Database), it's much more efficient to use a database as the isolation container than to do isolation in the program.</span></span> <span data-ttu-id="b5304-760">不管是子公司、多个租户，或只为规模需要进行数据分区，我们认为通过多个 Finance and Operations 实例都可以更好地处理这种情况。</span><span class="sxs-lookup"><span data-stu-id="b5304-760">Regardless of whether data partitioning is required for subsidiaries, for multiple tenants, or just for scale, we believe that the scenarios can be handled better through multiple instances of Finance and Operations.</span></span> |
| <span data-ttu-id="b5304-761">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-761">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-762">如果数据库级别分隔是关键问题，使用数据分区的客户必须使用多个 Finance and Operations 实例。</span><span class="sxs-lookup"><span data-stu-id="b5304-762">Customers using data partitions must use multiple instances of Finance and Operations if database level separation is a critical issue.</span></span>    |
| <span data-ttu-id="b5304-763">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-763">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-764">所有模块</span><span class="sxs-lookup"><span data-stu-id="b5304-764">All modules</span></span>  |
| <span data-ttu-id="b5304-765">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-765">**Status**</span></span>                         | <span data-ttu-id="b5304-766">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-766">Removed as of Dynamics AX 7.0.</span></span>  |


### <a name="database-and-file-share-storage-for-attachments"></a><span data-ttu-id="b5304-767">数据库和文件共享附件存储</span><span class="sxs-lookup"><span data-stu-id="b5304-767">Database and file share storage for attachments</span></span>

<span data-ttu-id="b5304-768">Microsoft Dynamics AX 2012 允许在数据库和文件共享中存储附件。</span><span class="sxs-lookup"><span data-stu-id="b5304-768">Microsoft Dynamics AX 2012 allowed storage of attachments in the database and in file shares.</span></span> <span data-ttu-id="b5304-769">这两个选项都不再受支持。</span><span class="sxs-lookup"><span data-stu-id="b5304-769">Both of those options are no longer supported.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-770">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-770">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-771">云托管的环境无法再与本地文件共享通信，因此文件共享存储不再受支持。</span><span class="sxs-lookup"><span data-stu-id="b5304-771">Files share storage is no longer supported because cloud-hosted environments cannot communicate with local file shares.</span></span> <span data-ttu-id="b5304-772">为了支持 Azure Blob 存储，数据库存储已弃用。</span><span class="sxs-lookup"><span data-stu-id="b5304-772">Database storage has been deprecated in favor of Azure Blob storage.</span></span> <span data-ttu-id="b5304-773">Azure Blob 存储相当于数据库中的存储，因为文档仅可以通过 Dynamics 365 for Finance and Operations 客户端窗体进行访问。</span><span class="sxs-lookup"><span data-stu-id="b5304-773">Azure Blob storage is equivalent to storage in the database, as documents can only be accessed through Dynamics 365 for Finance and Operations client forms.</span></span> <span data-ttu-id="b5304-774">这提供额外好处，即提供存储不会对数据库的性能造成不利影响。</span><span class="sxs-lookup"><span data-stu-id="b5304-774">This provides the added benefit of providing storage that doesn't negatively affect the performance of the database.</span></span> <span data-ttu-id="b5304-775">Blob 存储是文档管理的默认存储机制并立即生效。</span><span class="sxs-lookup"><span data-stu-id="b5304-775">Blob storage is the default storage mechanism for Document Management and works immediately.</span></span> |
| <span data-ttu-id="b5304-776">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-776">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-777">为了支持 Azure Blob 存储，数据库存储已弃用。</span><span class="sxs-lookup"><span data-stu-id="b5304-777">Database storage has been deprecated in favor of Azure Blob storage.</span></span>   |
| <span data-ttu-id="b5304-778">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-778">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-779">所有模块</span><span class="sxs-lookup"><span data-stu-id="b5304-779">All modules</span></span>  |
| <span data-ttu-id="b5304-780">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-780">**Status**</span></span>                         | <span data-ttu-id="b5304-781">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-781">Removed as of Dynamics AX 7.0.</span></span>   |

### <a name="delimitation"></a><span data-ttu-id="b5304-782">界定</span><span class="sxs-lookup"><span data-stu-id="b5304-782">Delimitation</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-783">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-783">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-784">找不到该功能的使用。</span><span class="sxs-lookup"><span data-stu-id="b5304-784">No use of the functionality was found.</span></span> |
| <span data-ttu-id="b5304-785">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-785">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-786">无</span><span class="sxs-lookup"><span data-stu-id="b5304-786">No</span></span>                                     |
| <span data-ttu-id="b5304-787">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-787">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-788">考勤管理</span><span class="sxs-lookup"><span data-stu-id="b5304-788">Time and attendance</span></span>                    |
| <span data-ttu-id="b5304-789">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-789">**Status**</span></span>                         | <span data-ttu-id="b5304-790">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-790">Removed as of Dynamics AX 7.0.</span></span>         |

### <a name="desktop-client"></a><span data-ttu-id="b5304-791">桌面客户端</span><span class="sxs-lookup"><span data-stu-id="b5304-791">Desktop client</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-792">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-792">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-793">Dynamics AX 客户端体验已被重新设计，可提高在多个平台和设备上的可用性。</span><span class="sxs-lookup"><span data-stu-id="b5304-793">The Dynamics AX client experience has been redesigned to improve usability across multiple platforms and devices.</span></span>                      |
| <span data-ttu-id="b5304-794">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-794">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-795">新的 Web 客户端基于已经过修改可提供丰富 Web 平台的桌面窗体元数据和编程模型。</span><span class="sxs-lookup"><span data-stu-id="b5304-795">The new web client is based on the desktop Form metadata and programming model that have been modified to provide a rich web platform.</span></span> |
| <span data-ttu-id="b5304-796">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-796">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-797">所有模块</span><span class="sxs-lookup"><span data-stu-id="b5304-797">All modules</span></span>  |
| <span data-ttu-id="b5304-798">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-798">**Status**</span></span>                         | <span data-ttu-id="b5304-799">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-799">Removed as of Dynamics AX 7.0.</span></span>   |

### <a name="direct-database-connection"></a><span data-ttu-id="b5304-800">直接数据库连接</span><span class="sxs-lookup"><span data-stu-id="b5304-800">Direct database connection</span></span>

<span data-ttu-id="b5304-801">在 Dynamics AX 2012 R3 中，Retail Modern POS 可以直接连接到与 Enterprise POS 方式相似的通道 DB。</span><span class="sxs-lookup"><span data-stu-id="b5304-801">In Dynamics AX 2012 R3, Retail Modern POS could connect directly to the Channel DB in similar fashion to Enterprise POS.</span></span> <span data-ttu-id="b5304-802">这是除通过 Retail Server 的 Retail Modern POS 通信的标准通信方法以外的方法。</span><span class="sxs-lookup"><span data-stu-id="b5304-802">This was in addition to the standard communication method of Retail Modern POS communicating through Retail Server.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-803">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-803">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-804">直接数据库连接要求较低的安全协议，主要用于达到最高性能级别。</span><span class="sxs-lookup"><span data-stu-id="b5304-804">Direct database connectivity required lower security protocols and was primarily used to achieve the highest levels of performance.</span></span> <span data-ttu-id="b5304-805">由于 Finance and Operations 发生的性能和安全性提高，此功能现在导致的问题比解决的问题更多。</span><span class="sxs-lookup"><span data-stu-id="b5304-805">Due to the performance and security enhancements that have occurred in Finance and Operations, this functionality now causes more issues than it solves.</span></span> |
| <span data-ttu-id="b5304-806">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-806">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-807">编号</span><span class="sxs-lookup"><span data-stu-id="b5304-807">No.</span></span> <span data-ttu-id="b5304-808">现在只支持标准零售服务器通信。</span><span class="sxs-lookup"><span data-stu-id="b5304-808">Only standard Retail Server communication is now supported.</span></span>  |
| <span data-ttu-id="b5304-809">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-809">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-810">通道 DB/Retail Modern POS</span><span class="sxs-lookup"><span data-stu-id="b5304-810">Channel DB/Retail Modern POS</span></span>   |
| <span data-ttu-id="b5304-811">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-811">**Status**</span></span>                         | <span data-ttu-id="b5304-812">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-812">Removed as of Dynamics AX 7.0.</span></span>  |

### <a name="dutch-swift-mt940"></a><span data-ttu-id="b5304-813">荷兰 SWIFT MT940</span><span class="sxs-lookup"><span data-stu-id="b5304-813">Dutch SWIFT MT940</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-814">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-814">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-815">现在使用的是通用功能，而不是本地化功能。</span><span class="sxs-lookup"><span data-stu-id="b5304-815">Generic functionality is now used instead of localized functionality.</span></span>                    |
| <span data-ttu-id="b5304-816">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-816">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-817">是，此功能已被高级银行对帐功能取代。</span><span class="sxs-lookup"><span data-stu-id="b5304-817">Yes, this functionality has been replaced by Advanced bank reconciliation functionality.</span></span> |
| <span data-ttu-id="b5304-818">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-818">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-819">所有模块</span><span class="sxs-lookup"><span data-stu-id="b5304-819">All modules</span></span>                                                                              |
| <span data-ttu-id="b5304-820">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-820">**Status**</span></span>                         | <span data-ttu-id="b5304-821">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-821">Deprecated: A removal date has not been set for this feature.</span></span>                           |

### <a name="ebilanz-xbrl-for-germany"></a><span data-ttu-id="b5304-822">eBilanz（针对德国的 XBRL）</span><span class="sxs-lookup"><span data-stu-id="b5304-822">eBilanz (XBRL for Germany)</span></span>

<span data-ttu-id="b5304-823">此功能专门针对德国 eBilanz 分类提供了可扩展业务报告语言 (XBRL) 输出。</span><span class="sxs-lookup"><span data-stu-id="b5304-823">This functionality provided eXtensible Business Reporting Language (XBRL) output that is intended specifically for the German eBilanz taxonomy.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-824">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-824">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-825">缺少客户使用</span><span class="sxs-lookup"><span data-stu-id="b5304-825">Lack of customer usage</span></span>  |
| <span data-ttu-id="b5304-826">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-826">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-827">此功能尚未被另一个功能取代，不过，多个提供丰富 XBRL 功能的专用 XBRL 程序包对德国市场可用。</span><span class="sxs-lookup"><span data-stu-id="b5304-827">This feature hasn't been replaced by another feature, but multiple specialized XBRL packages that provide rich XBRL functionality are available for the German market.</span></span> |
| <span data-ttu-id="b5304-828">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-828">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-829">Management Reporter</span><span class="sxs-lookup"><span data-stu-id="b5304-829">Management Reporter</span></span>      |
| <span data-ttu-id="b5304-830">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-830">**Status**</span></span>                         | <span data-ttu-id="b5304-831">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-831">Deprecated: A removal date has not been set for this feature.</span></span>  |

### <a name="enterprise-portal-client"></a><span data-ttu-id="b5304-832">企业门户客户端</span><span class="sxs-lookup"><span data-stu-id="b5304-832">Enterprise Portal client</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-833">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-833">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-834">提供了一个客户端平台。</span><span class="sxs-lookup"><span data-stu-id="b5304-834">A single client platform has been provided.</span></span>  |
| <span data-ttu-id="b5304-835">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-835">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-836">新的 Web 客户端基于已经过修改可提供丰富 Web 平台的桌面窗体元数据和编程模型。</span><span class="sxs-lookup"><span data-stu-id="b5304-836">The new web client is based on the desktop form metadata and programming model that have been modified to provide a rich web platform.</span></span> |
| <span data-ttu-id="b5304-837">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-837">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-838">所有模块</span><span class="sxs-lookup"><span data-stu-id="b5304-838">All modules</span></span>  |
| <span data-ttu-id="b5304-839">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-839">**Status**</span></span>                         | <span data-ttu-id="b5304-840">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-840">Removed as of Dynamics AX 7.0.</span></span>   |

### <a name="environmental-sustainability"></a><span data-ttu-id="b5304-841">环境可持续性</span><span class="sxs-lookup"><span data-stu-id="b5304-841">Environmental sustainability</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-842">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-842">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-843">低客户使用率和有限功能集</span><span class="sxs-lookup"><span data-stu-id="b5304-843">Low customer usage and a limited feature set</span></span>  |
| <span data-ttu-id="b5304-844">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-844">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-845">无</span><span class="sxs-lookup"><span data-stu-id="b5304-845">No</span></span>              |
| <span data-ttu-id="b5304-846">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-846">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-847">遵从性和内部控制、应付账款</span><span class="sxs-lookup"><span data-stu-id="b5304-847">Compliance and internal controls, Accounts payable</span></span>  |
| <span data-ttu-id="b5304-848">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-848">**Status**</span></span>                         | <span data-ttu-id="b5304-849">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-849">Removed as of Dynamics AX 7.0.</span></span> |

### <a name="form-activex-and-managed-host-controls"></a><span data-ttu-id="b5304-850">窗体 ActiveX 和托管主机控件</span><span class="sxs-lookup"><span data-stu-id="b5304-850">Form ActiveX and Managed Host controls</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-851">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-851">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-852">ActiveX 和托管主机控件基于已废弃的桌面客户端。</span><span class="sxs-lookup"><span data-stu-id="b5304-852">The ActiveX and Managed Host controls are based on the deprecated desktop client.</span></span> |
| <span data-ttu-id="b5304-853">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-853">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-854">可扩展控件框架支持构建新的基于 HTML、CSS 和 JavaScript 的控件，并且是 Microsoft Visual Studio 工具环境中的一流控件。</span><span class="sxs-lookup"><span data-stu-id="b5304-854">The extensible control framework supports building new controls that are based on HTML, CSS, and JavaScript, and is a first-class control in the Microsoft Visual Studio Tooling environment.</span></span> |
| <span data-ttu-id="b5304-855">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-855">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-856">所有模块</span><span class="sxs-lookup"><span data-stu-id="b5304-856">All modules</span></span>     |
| <span data-ttu-id="b5304-857">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-857">**Status**</span></span>                         | <span data-ttu-id="b5304-858">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-858">Removed as of Dynamics AX 7.0.</span></span>       |

### <a name="generate-prenotes-by-using-a-batch"></a><span data-ttu-id="b5304-859">通过使用批处理生成预验证</span><span class="sxs-lookup"><span data-stu-id="b5304-859">Generate prenotes by using a batch</span></span>

<span data-ttu-id="b5304-860">预验证生成无法通过使用批处理完成，但仍可以由用户完成。</span><span class="sxs-lookup"><span data-stu-id="b5304-860">Prenote generation can't be done by using a batch, but it can still be done by a user.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-861">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-861">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-862">在通过使用批处理生成预验证文件时，没有窗体持续存在并且显示生成的预验证文件。</span><span class="sxs-lookup"><span data-stu-id="b5304-862">No form exists to persist and display the resulting prenote file when it's generated by using a batch.</span></span> |
| <span data-ttu-id="b5304-863">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-863">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-864">预验证仍可以生成，并且用户能够控制该文件的保存位置。</span><span class="sxs-lookup"><span data-stu-id="b5304-864">Prenotes can still be generated, and the user has control over the location where the file is saved.</span></span>   |
| <span data-ttu-id="b5304-865">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-865">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-866">应付账款、应收账款、现金和银行管理</span><span class="sxs-lookup"><span data-stu-id="b5304-866">Accounts payable, Accounts receivable, Cash and bank management</span></span>  |
| <span data-ttu-id="b5304-867">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-867">**Status**</span></span>                         | <span data-ttu-id="b5304-868">从 AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-868">Removed as of AX 7.0.</span></span>    |

### <a name="german-dtaus-payment-export-and-account-statement-import-totals-and-transactions"></a><span data-ttu-id="b5304-869">德国 DTAUS 付款导出和帐户对账单导入（合计和交易记录）</span><span class="sxs-lookup"><span data-stu-id="b5304-869">German DTAUS payment export and account statement import (totals and transactions)</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-870">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-870">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-871">该格式不再适用于德国，因为它已被单一欧元支付区 (SEPA) 功能取代。</span><span class="sxs-lookup"><span data-stu-id="b5304-871">The format is no longer applicable in Germany, because it has been replaced by Single Euro Payments Area (SEPA) functionality.</span></span>                    |
| <span data-ttu-id="b5304-872">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-872">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-873">是，此功能已被 SEPA 付款导出和高级银行对帐功能（用于导入帐户对账单）取代。</span><span class="sxs-lookup"><span data-stu-id="b5304-873">Yes, this functionality has been replaced by SEPA payment export and advanced bank reconciliation functionality for importing account statements.</span></span> |
| <span data-ttu-id="b5304-874">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-874">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-875">所有模块</span><span class="sxs-lookup"><span data-stu-id="b5304-875">All modules</span></span>  |
| <span data-ttu-id="b5304-876">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-876">**Status**</span></span>                         | <span data-ttu-id="b5304-877">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-877">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="german-dtazv-payment-format"></a><span data-ttu-id="b5304-878">德国 DTAZV 付款格式</span><span class="sxs-lookup"><span data-stu-id="b5304-878">German DTAZV payment format</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-879">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-879">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-880">该格式不再适用于德国，因为它已被 SEPA 功能取代。</span><span class="sxs-lookup"><span data-stu-id="b5304-880">The format is no longer applicable in Germany, because it has been replaced by SEPA functionality.</span></span> |
| <span data-ttu-id="b5304-881">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-881">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-882">SEPA 付款导出</span><span class="sxs-lookup"><span data-stu-id="b5304-882">SEPA payments export</span></span>    |
| <span data-ttu-id="b5304-883">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-883">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-884">所有模块</span><span class="sxs-lookup"><span data-stu-id="b5304-884">All modules</span></span>   |
| <span data-ttu-id="b5304-885">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-885">**Status**</span></span>                         | <span data-ttu-id="b5304-886">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-886">Deprecated: A removal date has not been set for this feature.</span></span>    |

### <a name="german-mt940-import"></a><span data-ttu-id="b5304-887">德国 MT940 导入</span><span class="sxs-lookup"><span data-stu-id="b5304-887">German MT940 import</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-888">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-888">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-889">现在使用的是通用功能，而不是本地化功能。</span><span class="sxs-lookup"><span data-stu-id="b5304-889">Generic functionality is now used instead of localized functionality.</span></span>                    |
| <span data-ttu-id="b5304-890">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-890">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-891">是，此功能已被高级银行对帐功能取代。</span><span class="sxs-lookup"><span data-stu-id="b5304-891">Yes, this functionality has been replaced by Advanced bank reconciliation functionality.</span></span> |
| <span data-ttu-id="b5304-892">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-892">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-893">所有模块</span><span class="sxs-lookup"><span data-stu-id="b5304-893">All modules</span></span>                                                                              |
| <span data-ttu-id="b5304-894">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-894">**Status**</span></span>                         | <span data-ttu-id="b5304-895">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-895">Deprecated: A removal date has not been set for this feature.</span></span>                           |

### <a name="german-xml-eu-sales-list"></a><span data-ttu-id="b5304-896">德国 XML 欧盟销售清单</span><span class="sxs-lookup"><span data-stu-id="b5304-896">German XML EU Sales list</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-897">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-897">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-898">不再支持德国欧盟销售清单报表的 XML 格式。</span><span class="sxs-lookup"><span data-stu-id="b5304-898">The XML format for German EU Sales List reporting is no longer supported.</span></span> <span data-ttu-id="b5304-899">仅 ELMA5 文本文件格式可用于将欧盟销售清单报表提交给德国税务局。</span><span class="sxs-lookup"><span data-stu-id="b5304-899">Only the ELMA5 text file format can be used to submit the EU Sales List report to the German Tax Office.</span></span> |
| <span data-ttu-id="b5304-900">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-900">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-901">无</span><span class="sxs-lookup"><span data-stu-id="b5304-901">No</span></span>         |
| <span data-ttu-id="b5304-902">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-902">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-903">税金</span><span class="sxs-lookup"><span data-stu-id="b5304-903">Tax</span></span>        |
| <span data-ttu-id="b5304-904">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-904">**Status**</span></span>                         | <span data-ttu-id="b5304-905">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-905">Deprecated: A removal date has not been set for this feature.</span></span>   |

### <a name="gl-ssrs-reports"></a><span data-ttu-id="b5304-906">GL SSRS 报表</span><span class="sxs-lookup"><span data-stu-id="b5304-906">GL SSRS reports</span></span>

<span data-ttu-id="b5304-907">包括以下菜单项的报表已被删除：**“试算平衡表(汇总)”**、**“试算平衡表(明细)”**、**“会计科目表”**、**“审计线索”**、**“余额”**和**“余额表”**。</span><span class="sxs-lookup"><span data-stu-id="b5304-907">Reports that include the following menu items have been removed: **Summary trial balance**, **Detailed trial balance**, **Chart of accounts**, **Audit trail**, **Balances**, and **Balance list**.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-908">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-908">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-909">财务 Microsoft SQL Server Reporting Services (SSRS) 报表已经被 Management Reporter 功能和默认报表取代。</span><span class="sxs-lookup"><span data-stu-id="b5304-909">Financial Microsoft SQL Server Reporting Services (SSRS) reports have been replaced by Management Reporter capabilities and default reports.</span></span> |
| <span data-ttu-id="b5304-910">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-910">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-911">Management Reporter（在 Dynamics AX 的当前版本中标记为**“财务报告”**。）</span><span class="sxs-lookup"><span data-stu-id="b5304-911">Management Reporter (labeled **Financial reporting** in the current version of Dynamics AX)</span></span>    |
| <span data-ttu-id="b5304-912">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-912">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-913">总帐</span><span class="sxs-lookup"><span data-stu-id="b5304-913">General ledger</span></span>   |
| <span data-ttu-id="b5304-914">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-914">**Status**</span></span>                         | <span data-ttu-id="b5304-915">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-915">Removed as of Dynamics AX 7.0.</span></span>   |

### <a name="infopart-and-formpart-metadata"></a><span data-ttu-id="b5304-916">InfoPart 和 FormPart 元数据</span><span class="sxs-lookup"><span data-stu-id="b5304-916">InfoPart and FormPart metadata</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-917">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-917">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-918">InfoPart 和 FormPart 元数据支持为两个不同的客户端创建 FactBox。</span><span class="sxs-lookup"><span data-stu-id="b5304-918">InfoPart and FormPart metadata enabled the creation of FactBoxes for two different clients.</span></span> |
| <span data-ttu-id="b5304-919">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-919">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-920">InfoPart 元数据，是一种简化的窗体定义，由升级工具转换为窗体。</span><span class="sxs-lookup"><span data-stu-id="b5304-920">InfoPart metadata, which was a simplified form definition, is converted into a Form by upgrade tooling.</span></span> <span data-ttu-id="b5304-921">引用窗体的 FormPart 元数据已被升级工具所创建的更直接引用取代。</span><span class="sxs-lookup"><span data-stu-id="b5304-921">FormPart metadata, which referenced a Form, is replaced by a more direct reference that is created by upgrade tooling.</span></span> |
| <span data-ttu-id="b5304-922">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-922">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-923">所有模块</span><span class="sxs-lookup"><span data-stu-id="b5304-923">All modules</span></span>    |
| <span data-ttu-id="b5304-924">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-924">**Status**</span></span>                         | <span data-ttu-id="b5304-925">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-925">Removed as of Dynamics AX 7.0.</span></span>        |

### <a name="main-account-list-page"></a><span data-ttu-id="b5304-926">主科目列表页</span><span class="sxs-lookup"><span data-stu-id="b5304-926">Main account list page</span></span>

<span data-ttu-id="b5304-927">法人的帐户列表和相关余额信息</span><span class="sxs-lookup"><span data-stu-id="b5304-927">A list of accounts for the legal entity and related balance information</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-928">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-928">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-929">余额信息现在在**“试算余额表”**列表页上按帐户和维度提供。</span><span class="sxs-lookup"><span data-stu-id="b5304-929">Balance information is available on the **Trial balance** list page by account and dimension.</span></span>  |
| <span data-ttu-id="b5304-930">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-930">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-931">**“主科目”**包含**“主科目”**列表页所包含的相同科目列表。</span><span class="sxs-lookup"><span data-stu-id="b5304-931">**Main accounts** contains the same list of accounts that the **Main account** list page contained.</span></span> <span data-ttu-id="b5304-932">**“主科目”**中的网格视图还显示一个更小的、如网格般的视图。</span><span class="sxs-lookup"><span data-stu-id="b5304-932">The grid view in **Main accounts** also shows an even smaller, grid-like view.</span></span> |
| <span data-ttu-id="b5304-933">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-933">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-934">总帐</span><span class="sxs-lookup"><span data-stu-id="b5304-934">General ledger</span></span>      |
| <span data-ttu-id="b5304-935">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-935">**Status**</span></span>                         | <span data-ttu-id="b5304-936">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-936">Removed as of Dynamics AX 7.0.</span></span>    |

### <a name="malaysia-and-singapore-bank-cash-flow-report"></a><span data-ttu-id="b5304-937">马来西亚和新加坡银行现金流量报表</span><span class="sxs-lookup"><span data-stu-id="b5304-937">Malaysia and Singapore bank cash flow report</span></span>

<span data-ttu-id="b5304-938">此功能能让用户打印现金流量报表，以显示特定日期范围或所选银行帐户的现金流入量和流出量的交易记录和详细信息。</span><span class="sxs-lookup"><span data-stu-id="b5304-938">This feature let the user print a cash flow report that shows transactions and details of the cash inflows and outflows for a specific date range for selected bank accounts.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-939">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-939">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-940">同样的信息可以从查询银行交易记录中获得。</span><span class="sxs-lookup"><span data-stu-id="b5304-940">The same information can be obtained from the Inquiry bank transaction.</span></span> |
| <span data-ttu-id="b5304-941">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-941">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-942">查询银行交易记录</span><span class="sxs-lookup"><span data-stu-id="b5304-942">The Inquiry bank transaction</span></span>                                            |
| <span data-ttu-id="b5304-943">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-943">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-944">现金和银行管理</span><span class="sxs-lookup"><span data-stu-id="b5304-944">Cash and bank management</span></span>                                                |
| <span data-ttu-id="b5304-945">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-945">**Status**</span></span>                         | <span data-ttu-id="b5304-946">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-946">Deprecated: A removal date has not been set for this feature.</span></span>          |

### <a name="mexican-cfd-electronic-invoice"></a><span data-ttu-id="b5304-947">墨西哥 CFD 电子发票</span><span class="sxs-lookup"><span data-stu-id="b5304-947">Mexican CFD electronic invoice</span></span>

<span data-ttu-id="b5304-948">此功能支持通过使用 Comprobante Fiscal Digital (CFD) 方法生成墨西哥电子发票，在该方法中公司通过请求来自政府的相关主管机构签署发票。</span><span class="sxs-lookup"><span data-stu-id="b5304-948">This feature enabled the generation of Mexican electronic invoices by using the Comprobante Fiscal Digital (CFD) method, where the company signs the invoice by requesting the related authorization from the government.</span></span> <span data-ttu-id="b5304-949">此功能还提供一个每月报表，其包括在该期间签发的所有电子发票。</span><span class="sxs-lookup"><span data-stu-id="b5304-949">This feature also provides a monthly report that includes all electronics invoices that were issued in the period.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-950">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-950">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-951">此方法不再适用。</span><span class="sxs-lookup"><span data-stu-id="b5304-951">The method is no longer applicable.</span></span> <span data-ttu-id="b5304-952">通过使用 CFD 方法生成电子发票已被税务主管机构废弃，并已被 Comprobante Fiscal Digital a través de Internet (CFDI) 方法取代，在该方法中签名委托给第三方提供商 (PAC)。</span><span class="sxs-lookup"><span data-stu-id="b5304-952">The generation of electronic invoices by using the CFD method was deprecated by the tax authorities and replaced by the Comprobante Fiscal Digital a través de Internet (CFDI) method, where the signing is delegated to the third-party provider (PAC).</span></span> <span data-ttu-id="b5304-953">删除了每月报表，并且，查询选项能让用户查询历史交易记录。</span><span class="sxs-lookup"><span data-stu-id="b5304-953">The monthly report has been removed, and an inquiry option lets users inquire about historical transactions.</span></span> |
| <span data-ttu-id="b5304-954">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-954">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-955">无</span><span class="sxs-lookup"><span data-stu-id="b5304-955">No</span></span>    |
| <span data-ttu-id="b5304-956">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-956">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-957">应收账款、项目</span><span class="sxs-lookup"><span data-stu-id="b5304-957">Account receivables, Project</span></span>   |
| <span data-ttu-id="b5304-958">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-958">**Status**</span></span>                         | <span data-ttu-id="b5304-959">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-959">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="mexico-realized-and-unrealized-vat"></a><span data-ttu-id="b5304-960">墨西哥实现和未实现的增值税</span><span class="sxs-lookup"><span data-stu-id="b5304-960">Mexico realized and unrealized VAT</span></span>

<span data-ttu-id="b5304-961">Microsoft Dynamics AX 2012 通过使用“未实现的增值税”的墨西哥特定功能管理未实现的增值税 (VAT)。</span><span class="sxs-lookup"><span data-stu-id="b5304-961">Microsoft Dynamics AX 2012 managed unrealized value-added tax (VAT) by using Mexico-specific functionality for unrealized tax.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-962">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-962">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-963">重复的功能</span><span class="sxs-lookup"><span data-stu-id="b5304-963">Duplicate functionality</span></span>  |
| <span data-ttu-id="b5304-964">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-964">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-965">是，此功能已被使用核心提供的标准特定销售增值税功能取代。</span><span class="sxs-lookup"><span data-stu-id="b5304-965">Yes, this functionality has been replaced by standard conditional sales tax functionality that is provided by Core.</span></span> |
| <span data-ttu-id="b5304-966">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-966">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-967">税金</span><span class="sxs-lookup"><span data-stu-id="b5304-967">Tax</span></span>   |
| <span data-ttu-id="b5304-968">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-968">**Status**</span></span>                         | <span data-ttu-id="b5304-969">已弃用：尚未确定此功能的移除日期。</span><span class="sxs-lookup"><span data-stu-id="b5304-969">Deprecated: A removal date has not been set for this feature.</span></span> |

### <a name="microsoft-outlook-integration"></a><span data-ttu-id="b5304-970">Microsoft Outlook 集成</span><span class="sxs-lookup"><span data-stu-id="b5304-970">Microsoft Outlook integration</span></span>


|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-971">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-971">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-972">此功能已由 Microsoft Exchange Server 集成替换。</span><span class="sxs-lookup"><span data-stu-id="b5304-972">This functionality has been replaced by Microsoft Exchange Server integration.</span></span> |
| <span data-ttu-id="b5304-973">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-973">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-974">是</span><span class="sxs-lookup"><span data-stu-id="b5304-974">Yes</span></span>                                                                            |
| <span data-ttu-id="b5304-975">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-975">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-976">销售和市场营销</span><span class="sxs-lookup"><span data-stu-id="b5304-976">Sales and marketing</span></span>                                                            |
| <span data-ttu-id="b5304-977">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-977">**Status**</span></span>                         | <span data-ttu-id="b5304-978">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-978">Removed as of Dynamics AX 7.0.</span></span>                                                 |

### <a name="private-blocking-of-inventory-and-warehouse-management-journals"></a><span data-ttu-id="b5304-979">库存和仓库管理日记帐的专用锁定</span><span class="sxs-lookup"><span data-stu-id="b5304-979">Private blocking of inventory and warehouse management journals</span></span>

<span data-ttu-id="b5304-980">库存和仓库日记帐不再支持针对所选用户将日记帐标记为专用的功能。</span><span class="sxs-lookup"><span data-stu-id="b5304-980">The inventory and warehouse journals no longer support the ability to mark a journal as private for a selected user.</span></span> <span data-ttu-id="b5304-981">仅支持针对用户组将日记帐锁定为专用和在编辑期间锁定的流程。</span><span class="sxs-lookup"><span data-stu-id="b5304-981">Only the process of blocking journals as private for user groups and blocking during editing is supported.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-982">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-982">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-983">找不到该功能的使用。</span><span class="sxs-lookup"><span data-stu-id="b5304-983">No use of the functionality was found.</span></span> |
| <span data-ttu-id="b5304-984">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-984">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-985">无</span><span class="sxs-lookup"><span data-stu-id="b5304-985">No</span></span>                                     |
| <span data-ttu-id="b5304-986">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-986">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-987">库存管理</span><span class="sxs-lookup"><span data-stu-id="b5304-987">Inventory management</span></span>                   |
| <span data-ttu-id="b5304-988">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-988">**Status**</span></span>                         | <span data-ttu-id="b5304-989">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-989">Removed as of Dynamics AX 7.0.</span></span>         |

### <a name="product-builder"></a><span data-ttu-id="b5304-990">产品生成器</span><span class="sxs-lookup"><span data-stu-id="b5304-990">Product builder</span></span>

<span data-ttu-id="b5304-991">产品生成器用于从销售订单、采购订单、生产订单、销售报价单、项目报价单或物料需求动态配置物料。</span><span class="sxs-lookup"><span data-stu-id="b5304-991">Product builder was used to dynamically configure items from a sales order, purchase order, production order, sales quotation, project quotation, or item requirement.</span></span> <span data-ttu-id="b5304-992">基于具有建模变量的产品模型，用户可以选择值以满足用户需求并获取具有物料清单和工艺路线的唯一产品变型。</span><span class="sxs-lookup"><span data-stu-id="b5304-992">Based on a product model that had modeling variables, the user could select values to meet the customer requirements and get a unique product variant that had a BOM and route.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-993">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-993">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-994">产品生成器向最终用户显示了 X++ 代码，在 Dynamics AX 的当前版本中不受支持。</span><span class="sxs-lookup"><span data-stu-id="b5304-994">Product builder exposed X++ code to end users and isn't supported in the current version of Dynamics AX.</span></span> <span data-ttu-id="b5304-995">它已被删除，从而避免在重叠的、庞大的代码库中进行重复的维护工作。</span><span class="sxs-lookup"><span data-stu-id="b5304-995">It has been removed to avoid duplicate maintenance efforts on overlapping, sizeable codebases.</span></span>  |
| <span data-ttu-id="b5304-996">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-996">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-997">是。</span><span class="sxs-lookup"><span data-stu-id="b5304-997">Yes.</span></span> <span data-ttu-id="b5304-998">已经公布在将来的版本中弃用产品生成器的 Dynamics AX 2012 中引入了基于约束的配置。</span><span class="sxs-lookup"><span data-stu-id="b5304-998">The constraint-based configuration was introduced in Dynamics AX 2012 where the depreciation of Product builder in future versions was already announced.</span></span> <span data-ttu-id="b5304-999">在基础产品上选择基于约束的配置技术，以启用配置。</span><span class="sxs-lookup"><span data-stu-id="b5304-999">The constraint-based configuration technology is selected on the product masters to enable the configuration.</span></span> <span data-ttu-id="b5304-1000">若要了解更多信息，请参阅[生成产品配置模型](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/pim/build-product-configuration-model)。</span><span class="sxs-lookup"><span data-stu-id="b5304-1000">To learn more, see [Build a product configuration model](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/pim/build-product-configuration-model).</span></span> |
| <span data-ttu-id="b5304-1001">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-1001">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-1002">产品信息管理、销售和市场营销</span><span class="sxs-lookup"><span data-stu-id="b5304-1002">Product information management, Sales and marketing</span></span>  |
| <span data-ttu-id="b5304-1003">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-1003">**Status**</span></span>                         | <span data-ttu-id="b5304-1004">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-1004">Removed as of Dynamics AX 7.0.</span></span>      |

### <a name="rename-product-dimension"></a><span data-ttu-id="b5304-1005">重命名产品维度</span><span class="sxs-lookup"><span data-stu-id="b5304-1005">Rename product dimension</span></span>

<span data-ttu-id="b5304-1006">此功能能让您将三个标准维度（大小、颜色或样式）之一的名称更改为一个更好地满足您的业务需求的名称。</span><span class="sxs-lookup"><span data-stu-id="b5304-1006">This feature let you change the name of one of the three standard product dimensions (size, color, or style) to a name that better suited your business requirements.</span></span> <span data-ttu-id="b5304-1007">重命名包括其中使用了产品维度名称的所有标签。</span><span class="sxs-lookup"><span data-stu-id="b5304-1007">Renaming included all the labels where the product dimension name was used.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-1008">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-1008">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-1009">Dynamics AX 的当前版本在运行时不支持标签。</span><span class="sxs-lookup"><span data-stu-id="b5304-1009">The current version of Dynamics AX doesn't support label changes at run time.</span></span> |
| <span data-ttu-id="b5304-1010">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-1010">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-1011">无</span><span class="sxs-lookup"><span data-stu-id="b5304-1011">No</span></span>                                                                            |
| <span data-ttu-id="b5304-1012">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-1012">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-1013">产品信息管理</span><span class="sxs-lookup"><span data-stu-id="b5304-1013">Product information management</span></span>                                                |
| <span data-ttu-id="b5304-1014">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-1014">**Status**</span></span>                         | <span data-ttu-id="b5304-1015">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-1015">Removed as of Dynamics AX 7.0.</span></span>                                                |

### <a name="retail-server-connectivity-using-http"></a><span data-ttu-id="b5304-1016">使用 HTTP 的零售服务器连接</span><span class="sxs-lookup"><span data-stu-id="b5304-1016">Retail Server connectivity using HTTP</span></span>

<span data-ttu-id="b5304-1017">在 Dynamics AX 2012 R3 中，零售服务器可以使用 HTTP 通信（不受安全保护）运行。</span><span class="sxs-lookup"><span data-stu-id="b5304-1017">In Dynamics AX 2012 R3, the Retail Server could function using HTTP communication (non-secured).</span></span> <span data-ttu-id="b5304-1018">这是除使用 HTTPS 的标准通信之外的方法。</span><span class="sxs-lookup"><span data-stu-id="b5304-1018">This was in addition to the standard communication using HTTPS.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-1019">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-1019">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-1020">因为新的安全要求，现在只支持使用 TLS 1.2（或更高版本，如果可用）的安全通信。</span><span class="sxs-lookup"><span data-stu-id="b5304-1020">Due to new security requirements, only secured communication using TLS 1.2 (or above, as available) is now supported.</span></span> <span data-ttu-id="b5304-1021">自助服务安装程序将自动配置此通信的计算机。</span><span class="sxs-lookup"><span data-stu-id="b5304-1021">The self-service installer will automatically configure the computer for this communication.</span></span> |
| <span data-ttu-id="b5304-1022">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-1022">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-1023">编号</span><span class="sxs-lookup"><span data-stu-id="b5304-1023">No.</span></span> <span data-ttu-id="b5304-1024">现在只支持标准 HTTPS 通信。</span><span class="sxs-lookup"><span data-stu-id="b5304-1024">Only standard HTTPS communication is now supported.</span></span> |
| <span data-ttu-id="b5304-1025">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-1025">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-1026">零售服务器</span><span class="sxs-lookup"><span data-stu-id="b5304-1026">Retail Server</span></span>  |
| <span data-ttu-id="b5304-1027">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-1027">**Status**</span></span>                         | <span data-ttu-id="b5304-1028">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-1028">Removed as of Dynamics AX 7.0.</span></span> |

### <a name="role-center-pages"></a><span data-ttu-id="b5304-1029">角色中心页</span><span class="sxs-lookup"><span data-stu-id="b5304-1029">Role Center pages</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-1030">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-1030">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-1031">角色中心页基于已废弃的企业门户平台而构建，该平台已被 Dynamics AX 的当前版本中的新 Web 客户端平台取代。</span><span class="sxs-lookup"><span data-stu-id="b5304-1031">Role Center pages were built on the deprecated Enterprise Portal platform, which has been replaced by the new web client platform in the current version of Dynamics AX.</span></span> |
| <span data-ttu-id="b5304-1032">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-1032">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-1033">新工作区窗体模式为用户提供一个以流程为中心的设计，从而便于访问该流程中的常用任务。</span><span class="sxs-lookup"><span data-stu-id="b5304-1033">The new Workspace form pattern provides users with a process-centered design that provides easy access to commonly used tasks within that process.</span></span>                       |
| <span data-ttu-id="b5304-1034">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-1034">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-1035">所有模块</span><span class="sxs-lookup"><span data-stu-id="b5304-1035">All modules</span></span>    |
| <span data-ttu-id="b5304-1036">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-1036">**Status**</span></span>                         | <span data-ttu-id="b5304-1037">从 Dynamics AX 7.0 开始移除</span><span class="sxs-lookup"><span data-stu-id="b5304-1037">Removed as of Dynamics AX 7.0</span></span>   |

### <a name="sales-tax-jurisdictions"></a><span data-ttu-id="b5304-1038">销售税区域</span><span class="sxs-lookup"><span data-stu-id="b5304-1038">Sales tax jurisdictions</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-1039">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-1039">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-1040">低客户使用率和有限功能集</span><span class="sxs-lookup"><span data-stu-id="b5304-1040">Low customer usage and a limited feature set</span></span> |
| <span data-ttu-id="b5304-1041">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-1041">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-1042">无</span><span class="sxs-lookup"><span data-stu-id="b5304-1042">No</span></span>                                           |
| <span data-ttu-id="b5304-1043">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-1043">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-1044">美国销售税</span><span class="sxs-lookup"><span data-stu-id="b5304-1044">US sales tax</span></span>                                 |
| <span data-ttu-id="b5304-1045">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-1045">**Status**</span></span>                         | <span data-ttu-id="b5304-1046">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-1046">Removed as of Dynamics AX 7.0.</span></span>               |

### <a name="sites-services"></a><span data-ttu-id="b5304-1047">站点服务</span><span class="sxs-lookup"><span data-stu-id="b5304-1047">Sites Services</span></span>

<span data-ttu-id="b5304-1048">站点服务允许您构建将您的业务流程扩展到 Internet 的网站，而无需 IT 支持。</span><span class="sxs-lookup"><span data-stu-id="b5304-1048">Sites Services let you build websites that extend your business processes to the Internet without IT support.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-1049">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-1049">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-1050">Dynamics AX 的 Microsoft Azure 基础结构具有可以使用的新功能（例如，Azure 站点）。</span><span class="sxs-lookup"><span data-stu-id="b5304-1050">The Microsoft Azure infrastructure that is used by Dynamics AX has new capabilities that can be used instead (for example, Azure sites).</span></span> |
| <span data-ttu-id="b5304-1051">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-1051">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-1052">无</span><span class="sxs-lookup"><span data-stu-id="b5304-1052">No</span></span>   |
| <span data-ttu-id="b5304-1053">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-1053">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-1054">人力资源招聘、案例管理、询价、供应商注册、机会和市场活动协作工作区</span><span class="sxs-lookup"><span data-stu-id="b5304-1054">HR recruiting, Case management, Request for quotes, Vendor registration, Collaborative workspaces for opportunities and campaigns</span></span>  |
| <span data-ttu-id="b5304-1055">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-1055">**Status**</span></span>                         | <span data-ttu-id="b5304-1056">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-1056">Removed as of Dynamics AX 7.0.</span></span>    |

### <a name="ssas-demand-forecasting-strategy"></a><span data-ttu-id="b5304-1057">SSAS 需求预测策略</span><span class="sxs-lookup"><span data-stu-id="b5304-1057">SSAS demand forecasting strategy</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-1058">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-1058">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-1059">新的云体系结构中不支持设计此功能。</span><span class="sxs-lookup"><span data-stu-id="b5304-1059">The design of the feature cannot be supported in the new cloud architecture.</span></span> |
| <span data-ttu-id="b5304-1060">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-1060">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-1061">Azure 机器学习需求预测策略</span><span class="sxs-lookup"><span data-stu-id="b5304-1061">Azure Machine Learning demand forecasting strategy</span></span>                           |
| <span data-ttu-id="b5304-1062">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-1062">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-1063">主计划</span><span class="sxs-lookup"><span data-stu-id="b5304-1063">Master planning</span></span>                                                              |
| <span data-ttu-id="b5304-1064">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-1064">**Status**</span></span>                         | <span data-ttu-id="b5304-1065">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-1065">Removed as of Dynamics AX 7.0.</span></span>                                               |

### <a name="vendor-invoice-pool-excluding-posting-details"></a><span data-ttu-id="b5304-1066">供应商发票池(不包括过帐)详细信息</span><span class="sxs-lookup"><span data-stu-id="b5304-1066">Vendor invoice pool excluding posting details</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-1067">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-1067">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-1068">低使用率。</span><span class="sxs-lookup"><span data-stu-id="b5304-1068">Low usage.</span></span> <span data-ttu-id="b5304-1069">此功能已被具有工作流功能的发票日记帐取代。</span><span class="sxs-lookup"><span data-stu-id="b5304-1069">This functionality has been replaced by the Invoice journal that has workflow functionality.</span></span> |
| <span data-ttu-id="b5304-1070">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-1070">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-1071">发票日记帐的工作流功能。</span><span class="sxs-lookup"><span data-stu-id="b5304-1071">Workflow capabilities of the Invoice journal.</span></span>     |
| <span data-ttu-id="b5304-1072">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-1072">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-1073">应付帐款</span><span class="sxs-lookup"><span data-stu-id="b5304-1073">Accounts payable</span></span> |
| <span data-ttu-id="b5304-1074">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-1074">**Status**</span></span>                         | <span data-ttu-id="b5304-1075">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-1075">Removed as of Dynamics AX 7.0.</span></span>    |


### <a name="virtual-company-accounts"></a><span data-ttu-id="b5304-1076">虚拟公司帐户</span><span class="sxs-lookup"><span data-stu-id="b5304-1076">Virtual company accounts</span></span>

<span data-ttu-id="b5304-1077">Dynamics AX 中不再支持虚拟公司功能。</span><span class="sxs-lookup"><span data-stu-id="b5304-1077">The virtual companies feature is no longer supported in Dynamics AX.</span></span> <span data-ttu-id="b5304-1078">虚拟公司功能允许用户设置可以由一组公司共享的表。</span><span class="sxs-lookup"><span data-stu-id="b5304-1078">The virtual companies feature let users set up tables that could be shared by a set of companies.</span></span> <span data-ttu-id="b5304-1079">有关该功能的描述，请参阅[公司帐户和虚拟公司帐户](https://msdn.microsoft.com/en-us/library/aa834382(v=ax.10).aspx)。</span><span class="sxs-lookup"><span data-stu-id="b5304-1079">For a description of the feature, see [Company accounts and Virtual company accounts](https://msdn.microsoft.com/en-us/library/aa834382(v=ax.10).aspx).</span></span> <span data-ttu-id="b5304-1080">该功能的工作原理是将表分组到集合，然后集合分配给虚拟公司，即现有的“实际”公司的组。</span><span class="sxs-lookup"><span data-stu-id="b5304-1080">The feature works by grouping tables into collections that are assigned to virtual companies, which are groups of existing “real” companies.</span></span> <span data-ttu-id="b5304-1081">创建查询，以便虚拟公司中的所有公司可以访问关联表集合的表中的数据。</span><span class="sxs-lookup"><span data-stu-id="b5304-1081">Queries are created so that all the companies in the virtual company can access the data in the tables of the associated table collections.</span></span>

|   |  | 
|------------|--------------------|
| <span data-ttu-id="b5304-1082">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-1082">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-1083">- 将数据存储在表中之前，必须先设置虚拟公司。</span><span class="sxs-lookup"><span data-stu-id="b5304-1083">- Virtual companies must be set up before data is stored in the tables.</span></span> <span data-ttu-id="b5304-1084">将虚拟公司更新到现有实施上是很困难的。</span><span class="sxs-lookup"><span data-stu-id="b5304-1084">Retrofitting virtual companies onto an existing implementation is very difficult.</span></span><br><br><span data-ttu-id="b5304-1085">- 由于 Dynamics AX 的当前版本中有如此多数据标准化，要了解将什么添加到表集合将会很困难。</span><span class="sxs-lookup"><span data-stu-id="b5304-1085">- Because there has been so much data normalization in the current version of Dynamics AX, it has become difficult to know what to add to the table collections.</span></span> <span data-ttu-id="b5304-1086">例如，要知道共享哪些表很难。</span><span class="sxs-lookup"><span data-stu-id="b5304-1086">For example, it's difficult to know which tables to share.</span></span> <span data-ttu-id="b5304-1087">还必须添加从虚拟公司中的表引用的所有表。</span><span class="sxs-lookup"><span data-stu-id="b5304-1087">All the tables referenced from tables that are in a virtual company must also added.</span></span> <span data-ttu-id="b5304-1088">由于表标准化，即使遍布许多表中的简单主数据也必须是虚拟公司的一部分。</span><span class="sxs-lookup"><span data-stu-id="b5304-1088">Because of table normalization, even simple master data that is spread across multiple tables must be part of the virtual company.</span></span> <span data-ttu-id="b5304-1089">此处所犯的任何错误都将导致功能问题。</span><span class="sxs-lookup"><span data-stu-id="b5304-1089">Any mistake that is made here will cause functional issues.</span></span><br><br><span data-ttu-id="b5304-1090">- 当表是虚拟公司的一部分时，它会丢失有关数据来源的信息，并且只记录虚拟公司。</span><span class="sxs-lookup"><span data-stu-id="b5304-1090">- When a table is part of a virtual company, it loses information about the origin of the data, and only the virtual company is recorded.</span></span>   |
| <span data-ttu-id="b5304-1091">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-1091">**Replaced by another feature?**</span></span> | <span data-ttu-id="b5304-1092">全局表可用于使表可从所有公司访问到。</span><span class="sxs-lookup"><span data-stu-id="b5304-1092">Global tables can be used to make tables accessible from all companies.</span></span> <span data-ttu-id="b5304-1093">当前不替换。</span><span class="sxs-lookup"><span data-stu-id="b5304-1093">Currently, there is no replacement.</span></span> |   
| <span data-ttu-id="b5304-1094">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-1094">**Product areas affected**</span></span>       | <span data-ttu-id="b5304-1095">所有模块</span><span class="sxs-lookup"><span data-stu-id="b5304-1095">All modules</span></span> |   
| <span data-ttu-id="b5304-1096">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-1096">**Status**</span></span>                       | <span data-ttu-id="b5304-1097">从 Dynamics AX 7.0 开始移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-1097">Removed as of Dynamics AX 7.0.</span></span>   |   

### <a name="windows-8-tablet-app"></a><span data-ttu-id="b5304-1098">Windows 8 平板电脑应用</span><span class="sxs-lookup"><span data-stu-id="b5304-1098">Windows 8 tablet app</span></span>

<span data-ttu-id="b5304-1099">Windows 8 平板电脑应用提供用于费用录入和审核的功能。</span><span class="sxs-lookup"><span data-stu-id="b5304-1099">The Windows 8 tablet app provided functionality for expense entry and approval.</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-1100">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-1100">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-1101">Finance and Operations 与平板电脑兼容。</span><span class="sxs-lookup"><span data-stu-id="b5304-1101">Finance and Operations is compatible with tablets.</span></span> <span data-ttu-id="b5304-1102">无需再使用平板电脑应用。</span><span class="sxs-lookup"><span data-stu-id="b5304-1102">The tablet app is no longer required.</span></span>    |
| <span data-ttu-id="b5304-1103">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-1103">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-1104">编号</span><span class="sxs-lookup"><span data-stu-id="b5304-1104">No.</span></span>          |
| <span data-ttu-id="b5304-1105">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-1105">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-1106">费用报销管理</span><span class="sxs-lookup"><span data-stu-id="b5304-1106">Expense management</span></span>   |
| <span data-ttu-id="b5304-1107">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-1107">**Status**</span></span>                         | <span data-ttu-id="b5304-1108">已移除：此功能仅对 Dynamics AX 2012 R3 可用。</span><span class="sxs-lookup"><span data-stu-id="b5304-1108">Removed: This functionality is only available for Dynamics AX 2012 R3.</span></span> |

### <a name="workplanner"></a><span data-ttu-id="b5304-1109">工作进度表</span><span class="sxs-lookup"><span data-stu-id="b5304-1109">Workplanner</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-1110">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-1110">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-1111">低使用率</span><span class="sxs-lookup"><span data-stu-id="b5304-1111">Low usage</span></span> |
| <span data-ttu-id="b5304-1112">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-1112">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-1113">否，但从**模板组**页打开的**模板关系**页支持与弃用的**工作进度表**页相同的业务方案。</span><span class="sxs-lookup"><span data-stu-id="b5304-1113">No, but the **Profile relation** page, which is opened from the **Profile groups** page, supports the same business scenario as the deprecated **Workplanner** page.</span></span> |
| <span data-ttu-id="b5304-1114">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-1114">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-1115">考勤管理</span><span class="sxs-lookup"><span data-stu-id="b5304-1115">Time and attendance</span></span>     |
| <span data-ttu-id="b5304-1116">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-1116">**Status**</span></span>                         | <span data-ttu-id="b5304-1117">此代码尚未移除。</span><span class="sxs-lookup"><span data-stu-id="b5304-1117">The code has not been removed.</span></span> <span data-ttu-id="b5304-1118">但窗体 JmgWorkPlanner 未迁移。</span><span class="sxs-lookup"><span data-stu-id="b5304-1118">However, the form, JmgWorkPlanner, was not migrated.</span></span>    |

### <a name="x-financial-statements"></a><span data-ttu-id="b5304-1119">X++ 财务报表</span><span class="sxs-lookup"><span data-stu-id="b5304-1119">X++ financial statements</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b5304-1120">**弃用/移除的原因**</span><span class="sxs-lookup"><span data-stu-id="b5304-1120">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b5304-1121">此功能已被另一个功能取代。</span><span class="sxs-lookup"><span data-stu-id="b5304-1121">This functionality has been replaced by another feature.</span></span>                                    |
| <span data-ttu-id="b5304-1122">**被另一个功能取代？**</span><span class="sxs-lookup"><span data-stu-id="b5304-1122">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b5304-1123">Management Reporter（在 Dynamics AX 的当前版本中标记为**“财务报告”**。）</span><span class="sxs-lookup"><span data-stu-id="b5304-1123">Management Reporter (labeled **Financial reporting** in the current version of Dynamics AX)</span></span> |
| <span data-ttu-id="b5304-1124">**影响的产品区域**</span><span class="sxs-lookup"><span data-stu-id="b5304-1124">**Product areas affected**</span></span>         | <span data-ttu-id="b5304-1125">总帐</span><span class="sxs-lookup"><span data-stu-id="b5304-1125">General ledger</span></span>                                                                              |
| <span data-ttu-id="b5304-1126">**状态**</span><span class="sxs-lookup"><span data-stu-id="b5304-1126">**Status**</span></span>                         | <span data-ttu-id="b5304-1127">从 Dynamics AX 2012 开始移除</span><span class="sxs-lookup"><span data-stu-id="b5304-1127">Removed as of Dynamics AX 2012</span></span>                                                              |


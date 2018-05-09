--- 
title: "针对电子申报 (ER) 将已创建格式的组件映射到数据模型元素"
description: "以下过程显示属于系统管理员或电子报表开发人员的用户如何将数据模型元素映射到创建的电子申报 (ER) 配置的组件，该配置用于定义付款业务域的电子单据格式。"
author: NickSelin
manager: AnnBe
ms.date: 02/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 921e00051e8d9647f16b1e29dfbda8821f28c7e5
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---
# <a name="map-components-of-the-created-format-to-data-model-elements-for-electronic-reporting-er"></a><span data-ttu-id="7b005-103">针对电子申报 (ER) 将已创建格式的组件映射到数据模型元素</span><span class="sxs-lookup"><span data-stu-id="7b005-103">Map components of the created format to data model elements for electronic reporting (ER)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7b005-104">以下过程显示属于系统管理员或电子报表开发人员的用户如何将数据模型元素映射到创建的电子申报 (ER) 配置的组件，该配置用于定义付款业务域的电子单据格式。</span><span class="sxs-lookup"><span data-stu-id="7b005-104">The following procedure shows how a user in either the System administrator or Electronic reporting developer role can map data model elements to components of the created Electronic reporting (ER) configuration, which defines an electronic document format for the payments business domain.</span></span> <span data-ttu-id="7b005-105">后面将使用此格式生成用于处理付款的电子单据。</span><span class="sxs-lookup"><span data-stu-id="7b005-105">This format will be used later to generate electronic documents for processing payments.</span></span> <span data-ttu-id="7b005-106">在此示例中，您将创建示例公司“Litware 公司”的格式配置。</span><span class="sxs-lookup"><span data-stu-id="7b005-106">In this example, you will create a format configuration for the sample company, ‘Litware, Inc.’.</span></span> <span data-ttu-id="7b005-107">这些步骤适用于所有公司，因为所有公司共享 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="7b005-107">These steps can be performed in any company as ER configurations are shared for all companies.</span></span> <span data-ttu-id="7b005-108">为了完成这些步骤，您首先必须完成任务指南“创建格式配置”中的步骤。</span><span class="sxs-lookup"><span data-stu-id="7b005-108">To complete these steps, you must first complete the steps in the “Create a format configuration” task guide.</span></span>


## <a name="select-a-format-configuration"></a><span data-ttu-id="7b005-109">选择格式配置</span><span class="sxs-lookup"><span data-stu-id="7b005-109">Select a format configuration</span></span>
1. <span data-ttu-id="7b005-110">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="7b005-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="7b005-111">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="7b005-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="7b005-112">在树结构中，展开“付款（简化模型）”。</span><span class="sxs-lookup"><span data-stu-id="7b005-112">In the tree, expand 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="7b005-113">在树结构中，选择“付款（简化模型）\BACS（英国虚构）”。</span><span class="sxs-lookup"><span data-stu-id="7b005-113">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>
5. <span data-ttu-id="7b005-114">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="7b005-114">Click Designer.</span></span>

## <a name="map-format-components-to-data-model-elements"></a><span data-ttu-id="7b005-115">映射格式部分到数据模型元素</span><span class="sxs-lookup"><span data-stu-id="7b005-115">Map format components to data model elements</span></span>
1. <span data-ttu-id="7b005-116">单击”展开/折叠“。</span><span class="sxs-lookup"><span data-stu-id="7b005-116">Click Expand/collapse.</span></span>
2. <span data-ttu-id="7b005-117">单击“映射”选项卡。</span><span class="sxs-lookup"><span data-stu-id="7b005-117">Click the Mapping tab.</span></span>
3. <span data-ttu-id="7b005-118">在树结构中，展开“模型”。</span><span class="sxs-lookup"><span data-stu-id="7b005-118">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="7b005-119">在树结构中，选择“Xml\消息\处理日期\日期时间”。</span><span class="sxs-lookup"><span data-stu-id="7b005-119">In the tree, select 'Xml\Message\ProcessingDate\DateTime'.</span></span>
5. <span data-ttu-id="7b005-120">在树结构中，选择“模型\处理日期时间”。</span><span class="sxs-lookup"><span data-stu-id="7b005-120">In the tree, select 'model\ProcessingDateTime'.</span></span>
6. <span data-ttu-id="7b005-121">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="7b005-121">Click Bind.</span></span>
7. <span data-ttu-id="7b005-122">在树结构中，选择“Xml\消息\消息 ID\字符串”。</span><span class="sxs-lookup"><span data-stu-id="7b005-122">In the tree, select 'Xml\Message\MessageId\String'.</span></span>
8. <span data-ttu-id="7b005-123">在树结构中，选择“模型\消息标识”。</span><span class="sxs-lookup"><span data-stu-id="7b005-123">In the tree, select 'model\MessageIdentification'.</span></span>
9. <span data-ttu-id="7b005-124">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="7b005-124">Click Bind.</span></span>
10. <span data-ttu-id="7b005-125">在树结构中，展开“模型\付款”。</span><span class="sxs-lookup"><span data-stu-id="7b005-125">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="7b005-126">在树结构中，选择“Xml\消息\付款\项\金额\字符串”。</span><span class="sxs-lookup"><span data-stu-id="7b005-126">In the tree, select 'Xml\Message\Payments\Item\Amount\String'.</span></span>
12. <span data-ttu-id="7b005-127">在树结构中，选择“模型\付款\指示金额”。</span><span class="sxs-lookup"><span data-stu-id="7b005-127">In the tree, select 'model\Payments\InstructedAmount'.</span></span>
13. <span data-ttu-id="7b005-128">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="7b005-128">Click Bind.</span></span>
14. <span data-ttu-id="7b005-129">在树结构中，选择“Xml\消息\付款\项\交易日期\日期时间”。</span><span class="sxs-lookup"><span data-stu-id="7b005-129">In the tree, select 'Xml\Message\Payments\Item\TransDate\DateTime'.</span></span>
15. <span data-ttu-id="7b005-130">在树结构中，选择“模型\付款\交易日期”。</span><span class="sxs-lookup"><span data-stu-id="7b005-130">In the tree, select 'model\Payments\TransactionDate'.</span></span>
16. <span data-ttu-id="7b005-131">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="7b005-131">Click Bind.</span></span>
17. <span data-ttu-id="7b005-132">在树结构中，选择“Xml\消息\付款\项\描述\字符串”。</span><span class="sxs-lookup"><span data-stu-id="7b005-132">In the tree, select 'Xml\Message\Payments\Item\Description\String'.</span></span>
18. <span data-ttu-id="7b005-133">在树结构中，选择“模型\付款\描述”。</span><span class="sxs-lookup"><span data-stu-id="7b005-133">In the tree, select 'model\Payments\Description'.</span></span>
19. <span data-ttu-id="7b005-134">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="7b005-134">Click Bind.</span></span>
20. <span data-ttu-id="7b005-135">在树结构中，选择“Xml\消息\付款\项\货币\字符串”。</span><span class="sxs-lookup"><span data-stu-id="7b005-135">In the tree, select 'Xml\Message\Payments\Item\Currency\String'.</span></span>
21. <span data-ttu-id="7b005-136">在树结构中，选择“模型\付款\货币”。</span><span class="sxs-lookup"><span data-stu-id="7b005-136">In the tree, select 'model\Payments\Currency'.</span></span>
22. <span data-ttu-id="7b005-137">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="7b005-137">Click Bind.</span></span>
23. <span data-ttu-id="7b005-138">在树结构中，选择“Xml\消息\付款\项\ID”。</span><span class="sxs-lookup"><span data-stu-id="7b005-138">In the tree, select 'Xml\Message\Payments\Item\Id'.</span></span>
24. <span data-ttu-id="7b005-139">在树结构中，选择“模型\付款\End2EndID”。</span><span class="sxs-lookup"><span data-stu-id="7b005-139">In the tree, select 'model\Payments\End2EndID'.</span></span>
25. <span data-ttu-id="7b005-140">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="7b005-140">Click Bind.</span></span>
26. <span data-ttu-id="7b005-141">在树结构中，展开“模型\付款\贷方”。</span><span class="sxs-lookup"><span data-stu-id="7b005-141">In the tree, expand 'model\Payments\Creditor'.</span></span>
27. <span data-ttu-id="7b005-142">在树结构中，展开“模型\付款\贷方\金额”。</span><span class="sxs-lookup"><span data-stu-id="7b005-142">In the tree, expand 'model\Payments\Creditor\Account'.</span></span>
28. <span data-ttu-id="7b005-143">在树结构中，展开“模型\付款\贷方\代理”。</span><span class="sxs-lookup"><span data-stu-id="7b005-143">In the tree, expand 'model\Payments\Creditor\Agent'.</span></span>
29. <span data-ttu-id="7b005-144">在树结构中，选择“Xml\消息\付款\项\供应商\名称\字符串”。</span><span class="sxs-lookup"><span data-stu-id="7b005-144">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
30. <span data-ttu-id="7b005-145">在树结构中，展开“模型\付款\贷方\名称”。</span><span class="sxs-lookup"><span data-stu-id="7b005-145">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
31. <span data-ttu-id="7b005-146">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="7b005-146">Click Bind.</span></span>
32. <span data-ttu-id="7b005-147">在树结构中，选择“Xml\消息\付款\项\供应商\银行\银行代号\字符串”。</span><span class="sxs-lookup"><span data-stu-id="7b005-147">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber\String'.</span></span>
33. <span data-ttu-id="7b005-148">在树结构中，选择“模型\付款\贷方\代理\银行代号”。</span><span class="sxs-lookup"><span data-stu-id="7b005-148">In the tree, select 'model\Payments\Creditor\Agent\RoutingNumber'.</span></span>
34. <span data-ttu-id="7b005-149">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="7b005-149">Click Bind.</span></span>
35. <span data-ttu-id="7b005-150">在树结构中，选择“Xml\消息\付款\项\供应商\银行\帐号\字符串”。</span><span class="sxs-lookup"><span data-stu-id="7b005-150">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber\String'.</span></span>
36. <span data-ttu-id="7b005-151">在树结构中，选择“模型\付款\贷方\帐户\编号”。</span><span class="sxs-lookup"><span data-stu-id="7b005-151">In the tree, select 'model\Payments\Creditor\Account\Number'.</span></span>
37. <span data-ttu-id="7b005-152">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="7b005-152">Click Bind.</span></span>
38. <span data-ttu-id="7b005-153">在树结构中，选择“Xml\消息\付款\项\付款人\名称\字符串”。</span><span class="sxs-lookup"><span data-stu-id="7b005-153">In the tree, select 'Xml\Message\Payments\Item\Payer\Name\String'.</span></span>
39. <span data-ttu-id="7b005-154">在树结构中，展开“模型\付款\借方”。</span><span class="sxs-lookup"><span data-stu-id="7b005-154">In the tree, expand 'model\Payments\Debtor'.</span></span>
40. <span data-ttu-id="7b005-155">在树结构中，展开“模型\付款\借方\金额”。</span><span class="sxs-lookup"><span data-stu-id="7b005-155">In the tree, expand 'model\Payments\Debtor\Account'.</span></span>
41. <span data-ttu-id="7b005-156">在树结构中，展开“模型\付款\借方\代理”。</span><span class="sxs-lookup"><span data-stu-id="7b005-156">In the tree, expand 'model\Payments\Debtor\Agent'.</span></span>
42. <span data-ttu-id="7b005-157">在树结构中，展开“模型\付款\借方\名称”。</span><span class="sxs-lookup"><span data-stu-id="7b005-157">In the tree, select 'model\Payments\Debtor\Name'.</span></span>
43. <span data-ttu-id="7b005-158">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="7b005-158">Click Bind.</span></span>
44. <span data-ttu-id="7b005-159">在树结构中，选择“Xml\消息\付款\项\付款人\银行\银行代号\字符串”。</span><span class="sxs-lookup"><span data-stu-id="7b005-159">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber\String'.</span></span>
45. <span data-ttu-id="7b005-160">在树结构中，选择“模型\付款\借方\代理\银行代号”。</span><span class="sxs-lookup"><span data-stu-id="7b005-160">In the tree, select 'model\Payments\Debtor\Agent\RoutingNumber'.</span></span>
46. <span data-ttu-id="7b005-161">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="7b005-161">Click Bind.</span></span>
47. <span data-ttu-id="7b005-162">在树结构中，选择“Xml\消息\付款\项\付款人\银行\帐号\字符串”。</span><span class="sxs-lookup"><span data-stu-id="7b005-162">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber\String'.</span></span>
48. <span data-ttu-id="7b005-163">在树结构中，选择“模型\付款\借方\帐户\编号”。</span><span class="sxs-lookup"><span data-stu-id="7b005-163">In the tree, select 'model\Payments\Debtor\Account\Number'.</span></span>
49. <span data-ttu-id="7b005-164">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="7b005-164">Click Bind.</span></span>
50. <span data-ttu-id="7b005-165">在树结构中，选择“Xml\消息\付款\项”。</span><span class="sxs-lookup"><span data-stu-id="7b005-165">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="7b005-166">在树结构中，选择“模型\付款”。</span><span class="sxs-lookup"><span data-stu-id="7b005-166">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="7b005-167">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="7b005-167">Click Bind.</span></span>
53. <span data-ttu-id="7b005-168">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="7b005-168">Click Save.</span></span>

## <a name="validate-format-mapping"></a><span data-ttu-id="7b005-169">验证格式映射</span><span class="sxs-lookup"><span data-stu-id="7b005-169">Validate format mapping</span></span>
1. <span data-ttu-id="7b005-170">单击“验证”。</span><span class="sxs-lookup"><span data-stu-id="7b005-170">Click Validate.</span></span>
    * <span data-ttu-id="7b005-171">验证新映射以确保所有绑定正常。</span><span class="sxs-lookup"><span data-stu-id="7b005-171">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="7b005-172">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="7b005-172">Close the page.</span></span>

## <a name="change-status-of-the-current-version-of-format-configuration"></a><span data-ttu-id="7b005-173">更改格式配置的当前版本状态</span><span class="sxs-lookup"><span data-stu-id="7b005-173">Change status of the current version of format configuration</span></span>
    * <span data-ttu-id="7b005-174">在下一步骤中，您将把格式配置的状态从“草稿”更改为“已完成”，以使其可用于生成付款单据。</span><span class="sxs-lookup"><span data-stu-id="7b005-174">In the next steps, you’ll change the status of the format configuration from Draft to Completed to make it available for payment document generation.</span></span>  
1. <span data-ttu-id="7b005-175">单击“更改状态”。</span><span class="sxs-lookup"><span data-stu-id="7b005-175">Click Change status.</span></span>
2. <span data-ttu-id="7b005-176">单击“完成”。</span><span class="sxs-lookup"><span data-stu-id="7b005-176">Click Complete.</span></span>
3. <span data-ttu-id="7b005-177">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="7b005-177">In the Description field, type a value.</span></span>
    * <span data-ttu-id="7b005-178">例如，“版本 1”。</span><span class="sxs-lookup"><span data-stu-id="7b005-178">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="7b005-179">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="7b005-179">Click OK.</span></span>
5. <span data-ttu-id="7b005-180">选择当前配置的已完成版本。</span><span class="sxs-lookup"><span data-stu-id="7b005-180">Select completed version of the current configuration.</span></span>
    * <span data-ttu-id="7b005-181">请注意配置保存为已完成版本 1.1：即基于数据模型的第 1 版本的格式的第 1 版本。</span><span class="sxs-lookup"><span data-stu-id="7b005-181">Note that the configuration is saved as completed version 1.1: version 1 of the format based on the version 1 of the data model.</span></span>  

## <a name="define-effective-date-for-completed-version-of-format"></a><span data-ttu-id="7b005-182">定义已完成格式版本的生效日期</span><span class="sxs-lookup"><span data-stu-id="7b005-182">Define effective date for completed version of format</span></span>
    * <span data-ttu-id="7b005-183">每个格式版本可配置为从特定日期开始可供使用。</span><span class="sxs-lookup"><span data-stu-id="7b005-183">Each format version can be configured as available for usage starting from a certain date.</span></span> <span data-ttu-id="7b005-184">当多个格式版本在特定日期有效时，将选择使用最新格式（根据版本号）。</span><span class="sxs-lookup"><span data-stu-id="7b005-184">When more than one format version is active on a certain date, the latest format (based on version number) will be selected for usage.</span></span> <span data-ttu-id="7b005-185">此会话日期值将用于选择相应的版本。</span><span class="sxs-lookup"><span data-stu-id="7b005-185">The session date value is used for proper version selection.</span></span>  

## <a name="restrict-access-to-created-format-from-companies"></a><span data-ttu-id="7b005-186">限制公司对创建的格式的访问</span><span class="sxs-lookup"><span data-stu-id="7b005-186">Restrict access to created format from companies</span></span>
1. <span data-ttu-id="7b005-187">展开“ISO 国家/地区代码”部分。</span><span class="sxs-lookup"><span data-stu-id="7b005-187">Expand the ISO Country/region codes section.</span></span>
    * <span data-ttu-id="7b005-188">每种格式访问可通过识别格式适用的特定国家/地区来设定限制。</span><span class="sxs-lookup"><span data-stu-id="7b005-188">Each format access can be restricted by identifying particular countries/regions in which a format is applicable.</span></span> <span data-ttu-id="7b005-189">如果特定格式的国家/地区列表为空，此格式可供所有公司使用。</span><span class="sxs-lookup"><span data-stu-id="7b005-189">When the list of countries/regions for particular format is empty, this format can be used in any company.</span></span> <span data-ttu-id="7b005-190">在该国家/地区列表中插入某些 ISO 国家/地区代码时，此格式仅可以在其主要地址位于该国家/地区中的公司中使用。</span><span class="sxs-lookup"><span data-stu-id="7b005-190">When some ISO country/region codes are inserted in the list of countries/regions, the format can only be use in companies if the primary address is in the country/region.</span></span>  



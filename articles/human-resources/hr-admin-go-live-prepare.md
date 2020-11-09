---
title: 准备 Human Resources 实行
description: 该页面提供了有关如何准备实行 Dynamics 365 Human Resources 的指南。
author: rachel-profitt
manager: tfehr
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 59d7274c3b40e78209d90960c4514321b736876a
ms.sourcegitcommit: d66fd72342931fad25a696b251c05781280d36c4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/14/2020
ms.locfileid: "4011403"
---
# <a name="prepare-for-human-resources-go-live"></a><span data-ttu-id="c0a5a-103">准备 Human Resources 实行</span><span class="sxs-lookup"><span data-stu-id="c0a5a-103">Prepare for Human Resources go-live</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c0a5a-104">本主题介绍了如何使用 Microsoft Dynamics Lifecycle Services (LCS) 准备实行 Dynamics 365 Human Resources 项目。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-104">This topic describes how to prepare to go live with a Dynamics 365 Human Resources project by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> 

<span data-ttu-id="c0a5a-105">此图显示了实行流程的各个阶段。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-105">This graphic shows the phases of the go-live process.</span></span> 

![实行流程](./media/hr-admin-go-live-prepare-process.png)

<span data-ttu-id="c0a5a-107">下表列出了流程中的所有步骤、预期持续时间以及行为负责人。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-107">The following table lists all the steps in the process, the expected duration, and who is responsible for the action.</span></span>

| <span data-ttu-id="c0a5a-108">阶段</span><span class="sxs-lookup"><span data-stu-id="c0a5a-108">Phase</span></span> | <span data-ttu-id="c0a5a-109">行为</span><span class="sxs-lookup"><span data-stu-id="c0a5a-109">Action</span></span> | <span data-ttu-id="c0a5a-110">持续时间/时间</span><span class="sxs-lookup"><span data-stu-id="c0a5a-110">Duration/When</span></span> | <span data-ttu-id="c0a5a-111">人员</span><span class="sxs-lookup"><span data-stu-id="c0a5a-111">Who</span></span> | <span data-ttu-id="c0a5a-112">说明</span><span class="sxs-lookup"><span data-stu-id="c0a5a-112">Notes</span></span> |
| --- | --- | --- | --- |--- |
| <span data-ttu-id="c0a5a-113">1</span><span class="sxs-lookup"><span data-stu-id="c0a5a-113">1</span></span> | <span data-ttu-id="c0a5a-114">在 LCS 中更新实行日期</span><span class="sxs-lookup"><span data-stu-id="c0a5a-114">Update go-live date in LCS</span></span> | <span data-ttu-id="c0a5a-115">最迟提前 2-3 个月</span><span class="sxs-lookup"><span data-stu-id="c0a5a-115">At the latest 2-3 months in advance</span></span> | <span data-ttu-id="c0a5a-116">合作伙伴/客户</span><span class="sxs-lookup"><span data-stu-id="c0a5a-116">Partner/Customer</span></span> | <span data-ttu-id="c0a5a-117">里程碑日期应该不断更新。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-117">The milestone dates should be kept up to date on an ongoing basis.</span></span> |
| <span data-ttu-id="c0a5a-118">2</span><span class="sxs-lookup"><span data-stu-id="c0a5a-118">2</span></span> | <span data-ttu-id="c0a5a-119">完成并发送清单</span><span class="sxs-lookup"><span data-stu-id="c0a5a-119">Complete and send checklist</span></span> | <span data-ttu-id="c0a5a-120">用户验收测试 (UAT) 完成之后</span><span class="sxs-lookup"><span data-stu-id="c0a5a-120">After user acceptance testing (UAT) is complete</span></span> | <span data-ttu-id="c0a5a-121">合作伙伴/客户</span><span class="sxs-lookup"><span data-stu-id="c0a5a-121">Partner/Customer</span></span> | <span data-ttu-id="c0a5a-122">请按照 [FastTrack 实行评估](hr-admin-go-live-prepare.md#fasttrack-go-live-assessment)中提供的说明操作。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-122">Follow the instructions provided in [FastTrack go-live assessment](hr-admin-go-live-prepare.md#fasttrack-go-live-assessment).</span></span> |
| <span data-ttu-id="c0a5a-123">3</span><span class="sxs-lookup"><span data-stu-id="c0a5a-123">3</span></span> | <span data-ttu-id="c0a5a-124">项目评估 (FastTrack)</span><span class="sxs-lookup"><span data-stu-id="c0a5a-124">Project assessment (FastTrack)</span></span> | <span data-ttu-id="c0a5a-125">FastTrack 架构师\*</span><span class="sxs-lookup"><span data-stu-id="c0a5a-125">FastTrack Architect\*</span></span> | <span data-ttu-id="c0a5a-126">架构师在收到清单后进行评估并继续进行审核，直到确定问题并采取缓解措施（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-126">Architect delivers assessment after checklist is received and continues review until questions are clarified and mitigations are in place, if applicable.</span></span> |
| <span data-ttu-id="c0a5a-127">4</span><span class="sxs-lookup"><span data-stu-id="c0a5a-127">4</span></span> | <span data-ttu-id="c0a5a-128">项目研讨会 (FastTrack)</span><span class="sxs-lookup"><span data-stu-id="c0a5a-128">Project workshop (FastTrack)</span></span> | <span data-ttu-id="c0a5a-129">FastTrack 架构师\*</span><span class="sxs-lookup"><span data-stu-id="c0a5a-129">FastTrack Architect\*</span></span> | |
| <span data-ttu-id="c0a5a-130">5</span><span class="sxs-lookup"><span data-stu-id="c0a5a-130">5</span></span> | <span data-ttu-id="c0a5a-131">数据包导入</span><span class="sxs-lookup"><span data-stu-id="c0a5a-131">Data package imports</span></span> | <span data-ttu-id="c0a5a-132">取决于项目</span><span class="sxs-lookup"><span data-stu-id="c0a5a-132">Depends on the project</span></span> | <span data-ttu-id="c0a5a-133">合作伙伴/客户</span><span class="sxs-lookup"><span data-stu-id="c0a5a-133">Partner/Customer</span></span> | <span data-ttu-id="c0a5a-134">请按照[数据管理概述](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages)中的说明操作。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-134">Follow the instructions in [Data management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages).</span></span>|
| <span data-ttu-id="c0a5a-135">6</span><span class="sxs-lookup"><span data-stu-id="c0a5a-135">6</span></span> | <span data-ttu-id="c0a5a-136">生产准备</span><span class="sxs-lookup"><span data-stu-id="c0a5a-136">Production ready</span></span> | <span data-ttu-id="c0a5a-137">在完成前面的所有步骤之后</span><span class="sxs-lookup"><span data-stu-id="c0a5a-137">After all previous steps have been completed</span></span> | <span data-ttu-id="c0a5a-138">合作伙伴/客户</span><span class="sxs-lookup"><span data-stu-id="c0a5a-138">Partner/Customer</span></span> | <span data-ttu-id="c0a5a-139">合作伙伴/客户可以控制生产环境。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-139">Partner/Customer can take control of the production environment.</span></span>|
| <span data-ttu-id="c0a5a-140">7</span><span class="sxs-lookup"><span data-stu-id="c0a5a-140">7</span></span> | <span data-ttu-id="c0a5a-141">直接转换活动</span><span class="sxs-lookup"><span data-stu-id="c0a5a-141">Cutover activities</span></span> | <span data-ttu-id="c0a5a-142">取决于项目</span><span class="sxs-lookup"><span data-stu-id="c0a5a-142">Depends on the project</span></span> | <span data-ttu-id="c0a5a-143">合作伙伴/客户</span><span class="sxs-lookup"><span data-stu-id="c0a5a-143">Partner/Customer</span></span> | |
| <span data-ttu-id="c0a5a-144">8</span><span class="sxs-lookup"><span data-stu-id="c0a5a-144">8</span></span> | <span data-ttu-id="c0a5a-145">实行</span><span class="sxs-lookup"><span data-stu-id="c0a5a-145">Go live</span></span> | <span data-ttu-id="c0a5a-146">取决于项目</span><span class="sxs-lookup"><span data-stu-id="c0a5a-146">Depends on the project</span></span> | <span data-ttu-id="c0a5a-147">客户</span><span class="sxs-lookup"><span data-stu-id="c0a5a-147">Customer</span></span> | |

> [!IMPORTANT]
> <span data-ttu-id="c0a5a-148">\*仅针对符合 FastTrack 资格的客户完成步骤 3 和 4。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-148">\*Steps 3 and 4 are only completed for customers who qualify for FastTrack.</span></span>

## <a name="completing-the-lcs-methodology"></a><span data-ttu-id="c0a5a-149">完成 LCS 方法</span><span class="sxs-lookup"><span data-stu-id="c0a5a-149">Completing the LCS methodology</span></span>

<span data-ttu-id="c0a5a-150">每个实施项目中的重要里程碑都是到生产环境的直接转换。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-150">A major milestone in each implementation project is the cutover to the production environment.</span></span> 

<span data-ttu-id="c0a5a-151">为了帮助确保生产环境用于实时操作，在完成 LCS 方法中的所需活动后，Microsoft 仅在实施接近 **运行** 阶段时才预配生产实例。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-151">To help ensure the production environment is used for live operations, Microsoft provisions the production instance only when the implementation is approaching the **Operate** phase, after the required activities in the LCS methodology are completed.</span></span> <span data-ttu-id="c0a5a-152">有关您订阅中的环境的详细信息，请参阅  [Dynamics 365 许可指南](https://go.microsoft.com/fwlink/?LinkId=866544)。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-152">For more information about the environments in your subscription, see the [Dynamics 365 Licensing Guide](https://go.microsoft.com/fwlink/?LinkId=866544).</span></span> 

<span data-ttu-id="c0a5a-153">客户必须完成 LCS 方法中的 **分析** 、 **设计和开发** 和 **测试** 阶段，用于请求生产环境的 **配置** 按钮才可用。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-153">Customers must complete the **Analysis** , **Design and Develop** , and **Test** phases in the LCS methodology before the  **Configure** button for requesting the production environment becomes available.</span></span> <span data-ttu-id="c0a5a-154">若要完成 LCS 中的某个阶段，您必须首先完成该阶段中的每个必需步骤。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-154">To complete a phase in LCS, you must first complete every required step in that phase.</span></span> <span data-ttu-id="c0a5a-155">完成阶段中的所有步骤后，您可以完成整个阶段。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-155">When all the steps in a phase are completed, you can complete the whole phase.</span></span> <span data-ttu-id="c0a5a-156">如果必须进行更改，您可以在以后始终重新打开阶段。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-156">You can always reopen a phase later if you must make changes.</span></span> <span data-ttu-id="c0a5a-157">有关详细信息，请参阅 [适用于 Finance and Operations 应用客户的 Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs)。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-157">For more information, see [Lifecycle Services (LCS) for Finance and Operations apps customers](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs).</span></span> 

<span data-ttu-id="c0a5a-158">完成步骤的流程分为两个部分：</span><span class="sxs-lookup"><span data-stu-id="c0a5a-158">The process of completing a step has two parts:</span></span> 

- <span data-ttu-id="c0a5a-159">执行实际工作，例如填补差距分析或用户验收测试 (UAT)。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-159">Do the actual work, such as a fit-gap analysis or user acceptance testing (UAT).</span></span> 
- <span data-ttu-id="c0a5a-160">将 LCS 方法中的相应步骤标记为已完成。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-160">Mark the corresponding step in the LCS methodology as completed.</span></span> 

<span data-ttu-id="c0a5a-161">合理的做法是在实施流程中完成方法中的步骤。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-161">It's a good practice to complete the steps in the methodology as you make progress with the implementation.</span></span> <span data-ttu-id="c0a5a-162">尽早完成工作。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-162">Don't wait until the last minute.</span></span> <span data-ttu-id="c0a5a-163">不要仅仅单击所有步骤，以便获得生产环境。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-163">Don't just click through all the steps so you can get a production environment.</span></span> <span data-ttu-id="c0a5a-164">进行可靠的实施符合客户的最大利益。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-164">It's in the customer's best interest to have a solid implementation.</span></span> 

## <a name="uat-for-your-solution"></a><span data-ttu-id="c0a5a-165">适用于您的解决方案的 UAT</span><span class="sxs-lookup"><span data-stu-id="c0a5a-165">UAT for your solution</span></span>

<span data-ttu-id="c0a5a-166">在 UAT 阶段，您必须在实施项目的沙盒环境中测试已实施的所有业务流程以及所做的任何自定义。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-166">During the UAT phase, you must test all the business processes you've implemented, and any customizations you've made, in a Sandbox environment in the implementation project.</span></span> <span data-ttu-id="c0a5a-167">为了帮助确保成功实行，在完成 UAT 阶段时应考虑以下事项：</span><span class="sxs-lookup"><span data-stu-id="c0a5a-167">To help ensure a successful go-live, you should consider the following as you complete the UAT phase:</span></span> 

- <span data-ttu-id="c0a5a-168">测试用例涵盖整个需求范围。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-168">Test cases cover the entire scope of requirements.</span></span> 
- <span data-ttu-id="c0a5a-169">使用迁移的数据进行测试。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-169">Test by using migrated data.</span></span> <span data-ttu-id="c0a5a-170">此数据应包括主数据，例如工作人员、工作和职位。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-170">This data should include master data such as workers, jobs, and positions.</span></span> <span data-ttu-id="c0a5a-171">还包括期初余额，例如休假和缺勤应计。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-171">Also include opening balances, like leave and absence accruals.</span></span> <span data-ttu-id="c0a5a-172">最后，包括未结交易，例如当前的福利登记。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-172">Finally, include open transactions, such as current benefits enrollments.</span></span> <span data-ttu-id="c0a5a-173">即使未完成数据集，也可以使用所有类型的数据完成测试。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-173">Complete testing with all types of data, even if the data set isn't finalized.</span></span> 
- <span data-ttu-id="c0a5a-174">使用分配给用户的正确安全角色（默认角色和自定义角色）进行测试。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-174">Test by using the correct security roles (default roles and custom roles) that are assigned to users.</span></span> 
- <span data-ttu-id="c0a5a-175">确保解决方案符合任何公司和行业特定的法规要求。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-175">Make sure that the solution complies with any company- and industry-specific regulatory requirements.</span></span> 
- <span data-ttu-id="c0a5a-176">记录所有功能，并获得客户的审批和签核。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-176">Document all features and obtain approval and sign-off from the customer.</span></span> 

## <a name="fasttrack-go-live-assessment"></a><span data-ttu-id="c0a5a-177">FastTrack 实行评估</span><span class="sxs-lookup"><span data-stu-id="c0a5a-177">FastTrack go-live assessment</span></span>

<span data-ttu-id="c0a5a-178">符合 FastTrack 资格并与 FastTrack 解决方案架构师合作的客户将通过 Microsoft FastTrack 完成实行审核。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-178">Customers who are qualified for FastTrack and are engaged with a FastTrack Solution Architect will complete a go-live review with Microsoft FastTrack.</span></span> <span data-ttu-id="c0a5a-179">有关详细信息，请参阅  [Microsoft FastTrack](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview)。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-179">For more information, see [Microsoft FastTrack](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview).</span></span> 

<span data-ttu-id="c0a5a-180">大约在实行前的八周内，FastTrack 团队会要求您填写[实行清单](https://go.microsoft.com/fwlink/?linkid=2146013)。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-180">About eight weeks before go-live, the FastTrack team will ask you to fill in a [Go-live checklist](https://go.microsoft.com/fwlink/?linkid=2146013).</span></span>

<span data-ttu-id="c0a5a-181">项目经理或关键项目成员必须在项目的预先实行阶段完成实行清单。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-181">The project manager or a key project member must complete the go-live checklist during the pre-go-live phase of the project.</span></span> <span data-ttu-id="c0a5a-182">通常，当 UAT 已完成或几乎完成时，清单将在建议的实行日期之前四到六周内完成。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-182">Typically, the checklist is completed four to six weeks before the proposed go-live date, when UAT is completed or almost completed.</span></span> 

<span data-ttu-id="c0a5a-183">完成实行清单后，通过电子邮件将其发送给 FastTrack 解决方案架构师。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-183">When you've completed the go-live checklist, email it to your FastTrack Solution Architect.</span></span> <span data-ttu-id="c0a5a-184">始终在电子邮件中包括来自客户和实施合作伙伴的关键利益相关者。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-184">Always include a key stakeholder from the customer and the implementation partner on the email.</span></span> 

<span data-ttu-id="c0a5a-185">提交清单后，您的 FastTrack 解决方案架构师将审查该项目并提供评估，以描述潜在风险、最佳实践以及成功实行项目的建议。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-185">After you submit the checklist, your FastTrack Solution Architect will review the project and provide an assessment that describes the potential risks, best practices, and recommendations for a successful go-live of the project.</span></span> <span data-ttu-id="c0a5a-186">在某些情况下，解决方案架构师可能会强调风险因素并要求制定缓解计划。</span><span class="sxs-lookup"><span data-stu-id="c0a5a-186">In some cases, the solution architect might highlight risk factors and ask for a mitigation plan.</span></span> 

## <a name="see-also"></a><span data-ttu-id="c0a5a-187">请参阅</span><span class="sxs-lookup"><span data-stu-id="c0a5a-187">See also</span></span>

[<span data-ttu-id="c0a5a-188">实施常见问题</span><span class="sxs-lookup"><span data-stu-id="c0a5a-188">Go-live FAQ</span></span>](hr-admin-go-live-faq.md)
---
title: 准备 Human Resources 实行
description: 该页面提供了有关如何准备实行 Dynamics 365 Human Resources 的指南。
author: rachel-profitt
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 2f6dbcbd92a99699ce8d7e91c1a7e89a6063035f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795133"
---
# <a name="prepare-for-human-resources-go-live"></a><span data-ttu-id="fb189-103">准备 Human Resources 实行</span><span class="sxs-lookup"><span data-stu-id="fb189-103">Prepare for Human Resources go-live</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fb189-104">本主题介绍了如何使用 Microsoft Dynamics Lifecycle Services (LCS) 准备实行 Dynamics 365 Human Resources 项目。</span><span class="sxs-lookup"><span data-stu-id="fb189-104">This topic describes how to prepare to go live with a Dynamics 365 Human Resources project by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> 

<span data-ttu-id="fb189-105">此图显示了实行流程的各个阶段。</span><span class="sxs-lookup"><span data-stu-id="fb189-105">This graphic shows the phases of the go-live process.</span></span> 

![实行流程](./media/hr-admin-go-live-prepare-process.png)

<span data-ttu-id="fb189-107">下表列出了流程中的所有步骤、预期持续时间以及行为负责人。</span><span class="sxs-lookup"><span data-stu-id="fb189-107">The following table lists all the steps in the process, the expected duration, and who is responsible for the action.</span></span>

| <span data-ttu-id="fb189-108">阶段</span><span class="sxs-lookup"><span data-stu-id="fb189-108">Phase</span></span> | <span data-ttu-id="fb189-109">行为</span><span class="sxs-lookup"><span data-stu-id="fb189-109">Action</span></span> | <span data-ttu-id="fb189-110">持续时间/时间</span><span class="sxs-lookup"><span data-stu-id="fb189-110">Duration/When</span></span> | <span data-ttu-id="fb189-111">人员</span><span class="sxs-lookup"><span data-stu-id="fb189-111">Who</span></span> | <span data-ttu-id="fb189-112">说明</span><span class="sxs-lookup"><span data-stu-id="fb189-112">Notes</span></span> |
| --- | --- | --- | --- |--- |
| <span data-ttu-id="fb189-113">1</span><span class="sxs-lookup"><span data-stu-id="fb189-113">1</span></span> | <span data-ttu-id="fb189-114">在 LCS 中更新实行日期</span><span class="sxs-lookup"><span data-stu-id="fb189-114">Update go-live date in LCS</span></span> | <span data-ttu-id="fb189-115">最迟提前 2-3 个月</span><span class="sxs-lookup"><span data-stu-id="fb189-115">At the latest 2-3 months in advance</span></span> | <span data-ttu-id="fb189-116">合作伙伴/客户</span><span class="sxs-lookup"><span data-stu-id="fb189-116">Partner/Customer</span></span> | <span data-ttu-id="fb189-117">里程碑日期应该不断更新。</span><span class="sxs-lookup"><span data-stu-id="fb189-117">The milestone dates should be kept up to date on an ongoing basis.</span></span> |
| <span data-ttu-id="fb189-118">2</span><span class="sxs-lookup"><span data-stu-id="fb189-118">2</span></span> | <span data-ttu-id="fb189-119">完成并发送清单</span><span class="sxs-lookup"><span data-stu-id="fb189-119">Complete and send checklist</span></span> | <span data-ttu-id="fb189-120">用户验收测试 (UAT) 完成之后</span><span class="sxs-lookup"><span data-stu-id="fb189-120">After user acceptance testing (UAT) is complete</span></span> | <span data-ttu-id="fb189-121">合作伙伴/客户</span><span class="sxs-lookup"><span data-stu-id="fb189-121">Partner/Customer</span></span> | <span data-ttu-id="fb189-122">请按照 [FastTrack 实行评估](hr-admin-go-live-prepare.md#fasttrack-go-live-assessment)中提供的说明操作。</span><span class="sxs-lookup"><span data-stu-id="fb189-122">Follow the instructions provided in [FastTrack go-live assessment](hr-admin-go-live-prepare.md#fasttrack-go-live-assessment).</span></span> |
| <span data-ttu-id="fb189-123">3</span><span class="sxs-lookup"><span data-stu-id="fb189-123">3</span></span> | <span data-ttu-id="fb189-124">项目评估 (FastTrack)</span><span class="sxs-lookup"><span data-stu-id="fb189-124">Project assessment (FastTrack)</span></span> | <span data-ttu-id="fb189-125">FastTrack 架构师\*</span><span class="sxs-lookup"><span data-stu-id="fb189-125">FastTrack Architect\*</span></span> | <span data-ttu-id="fb189-126">架构师在收到清单后进行评估并继续进行审核，直到确定问题并采取缓解措施（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="fb189-126">Architect delivers assessment after checklist is received and continues review until questions are clarified and mitigations are in place, if applicable.</span></span> |
| <span data-ttu-id="fb189-127">4</span><span class="sxs-lookup"><span data-stu-id="fb189-127">4</span></span> | <span data-ttu-id="fb189-128">项目研讨会 (FastTrack)</span><span class="sxs-lookup"><span data-stu-id="fb189-128">Project workshop (FastTrack)</span></span> | <span data-ttu-id="fb189-129">FastTrack 架构师\*</span><span class="sxs-lookup"><span data-stu-id="fb189-129">FastTrack Architect\*</span></span> | |
| <span data-ttu-id="fb189-130">5</span><span class="sxs-lookup"><span data-stu-id="fb189-130">5</span></span> | <span data-ttu-id="fb189-131">数据包导入</span><span class="sxs-lookup"><span data-stu-id="fb189-131">Data package imports</span></span> | <span data-ttu-id="fb189-132">取决于项目</span><span class="sxs-lookup"><span data-stu-id="fb189-132">Depends on the project</span></span> | <span data-ttu-id="fb189-133">合作伙伴/客户</span><span class="sxs-lookup"><span data-stu-id="fb189-133">Partner/Customer</span></span> | <span data-ttu-id="fb189-134">请按照[数据管理概述](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages)中的说明操作。</span><span class="sxs-lookup"><span data-stu-id="fb189-134">Follow the instructions in [Data management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages).</span></span>|
| <span data-ttu-id="fb189-135">6</span><span class="sxs-lookup"><span data-stu-id="fb189-135">6</span></span> | <span data-ttu-id="fb189-136">生产准备</span><span class="sxs-lookup"><span data-stu-id="fb189-136">Production ready</span></span> | <span data-ttu-id="fb189-137">在完成前面的所有步骤之后</span><span class="sxs-lookup"><span data-stu-id="fb189-137">After all previous steps have been completed</span></span> | <span data-ttu-id="fb189-138">合作伙伴/客户</span><span class="sxs-lookup"><span data-stu-id="fb189-138">Partner/Customer</span></span> | <span data-ttu-id="fb189-139">合作伙伴/客户可以控制生产环境。</span><span class="sxs-lookup"><span data-stu-id="fb189-139">Partner/Customer can take control of the production environment.</span></span>|
| <span data-ttu-id="fb189-140">7</span><span class="sxs-lookup"><span data-stu-id="fb189-140">7</span></span> | <span data-ttu-id="fb189-141">直接转换活动</span><span class="sxs-lookup"><span data-stu-id="fb189-141">Cutover activities</span></span> | <span data-ttu-id="fb189-142">取决于项目</span><span class="sxs-lookup"><span data-stu-id="fb189-142">Depends on the project</span></span> | <span data-ttu-id="fb189-143">合作伙伴/客户</span><span class="sxs-lookup"><span data-stu-id="fb189-143">Partner/Customer</span></span> | |
| <span data-ttu-id="fb189-144">8</span><span class="sxs-lookup"><span data-stu-id="fb189-144">8</span></span> | <span data-ttu-id="fb189-145">实行</span><span class="sxs-lookup"><span data-stu-id="fb189-145">Go live</span></span> | <span data-ttu-id="fb189-146">取决于项目</span><span class="sxs-lookup"><span data-stu-id="fb189-146">Depends on the project</span></span> | <span data-ttu-id="fb189-147">客户</span><span class="sxs-lookup"><span data-stu-id="fb189-147">Customer</span></span> | |

> [!IMPORTANT]
> <span data-ttu-id="fb189-148">\*仅针对符合 FastTrack 资格的客户完成步骤 3 和 4。</span><span class="sxs-lookup"><span data-stu-id="fb189-148">\*Steps 3 and 4 are only completed for customers who qualify for FastTrack.</span></span>

## <a name="completing-the-lcs-methodology"></a><span data-ttu-id="fb189-149">完成 LCS 方法</span><span class="sxs-lookup"><span data-stu-id="fb189-149">Completing the LCS methodology</span></span>

<span data-ttu-id="fb189-150">每个实施项目中的重要里程碑都是到生产环境的直接转换。</span><span class="sxs-lookup"><span data-stu-id="fb189-150">A major milestone in each implementation project is the cutover to the production environment.</span></span> <span data-ttu-id="fb189-151">完成步骤的流程分为两个部分：</span><span class="sxs-lookup"><span data-stu-id="fb189-151">The process of completing a step has two parts:</span></span> 

- <span data-ttu-id="fb189-152">执行实际工作，例如填补差距分析或用户验收测试 (UAT)。</span><span class="sxs-lookup"><span data-stu-id="fb189-152">Do the actual work, such as a fit-gap analysis or user acceptance testing (UAT).</span></span> 
- <span data-ttu-id="fb189-153">将 LCS 方法中的相应步骤标记为已完成。</span><span class="sxs-lookup"><span data-stu-id="fb189-153">Mark the corresponding step in the LCS methodology as completed.</span></span> 

<span data-ttu-id="fb189-154">合理的做法是在实施流程中完成方法中的步骤。</span><span class="sxs-lookup"><span data-stu-id="fb189-154">It's a good practice to complete the steps in the methodology as you make progress with the implementation.</span></span> <span data-ttu-id="fb189-155">尽早完成工作。</span><span class="sxs-lookup"><span data-stu-id="fb189-155">Don't wait until the last minute.</span></span> <span data-ttu-id="fb189-156">进行可靠的实施符合客户的最大利益。</span><span class="sxs-lookup"><span data-stu-id="fb189-156">It's in the customer's best interest to have a solid implementation.</span></span> 

## <a name="uat-for-your-solution"></a><span data-ttu-id="fb189-157">适用于您的解决方案的 UAT</span><span class="sxs-lookup"><span data-stu-id="fb189-157">UAT for your solution</span></span>

<span data-ttu-id="fb189-158">在 UAT 阶段，您必须在实施项目的沙盒环境中测试已实施的所有业务流程以及所做的任何自定义。</span><span class="sxs-lookup"><span data-stu-id="fb189-158">During the UAT phase, you must test all the business processes you've implemented, and any customizations you've made, in a Sandbox environment in the implementation project.</span></span> <span data-ttu-id="fb189-159">为了帮助确保成功实行，在完成 UAT 阶段时应考虑以下事项：</span><span class="sxs-lookup"><span data-stu-id="fb189-159">To help ensure a successful go-live, you should consider the following as you complete the UAT phase:</span></span> 

- <span data-ttu-id="fb189-160">我们建议您的 UAT 流程从一个洁净的全新环境开始，您的 GOLD 配置中的数据将在 UAT 流程开始之前复制到该环境中。</span><span class="sxs-lookup"><span data-stu-id="fb189-160">We recommend that your UAT process starts with a clean and fresh environment where the data from your GOLD configuration is copied into the environment prior to the start of the UAT process.</span></span> <span data-ttu-id="fb189-161">我们建议您在实施前将此生产环境用作您的 GOLD 环境，实施时该环境将成为生产环境。</span><span class="sxs-lookup"><span data-stu-id="fb189-161">We recommend that you use the production environment as your GOLD environment until you go-live, at which point the environment becomes production.</span></span>
- <span data-ttu-id="fb189-162">测试用例涵盖整个需求范围。</span><span class="sxs-lookup"><span data-stu-id="fb189-162">Test cases cover the entire scope of requirements.</span></span> 
- <span data-ttu-id="fb189-163">使用迁移的数据进行测试。</span><span class="sxs-lookup"><span data-stu-id="fb189-163">Test by using migrated data.</span></span> <span data-ttu-id="fb189-164">此数据应包括主数据，例如工作人员、工作和职位。</span><span class="sxs-lookup"><span data-stu-id="fb189-164">This data should include master data such as workers, jobs, and positions.</span></span> <span data-ttu-id="fb189-165">还包括期初余额，例如休假和缺勤应计。</span><span class="sxs-lookup"><span data-stu-id="fb189-165">Also include opening balances, like leave and absence accruals.</span></span> <span data-ttu-id="fb189-166">最后，包括未结交易，例如当前的福利登记。</span><span class="sxs-lookup"><span data-stu-id="fb189-166">Finally, include open transactions, such as current benefits enrollments.</span></span> <span data-ttu-id="fb189-167">即使未完成数据集，也可以使用所有类型的数据完成测试。</span><span class="sxs-lookup"><span data-stu-id="fb189-167">Complete testing with all types of data, even if the data set isn't finalized.</span></span> 
- <span data-ttu-id="fb189-168">使用分配给用户的正确安全角色（默认角色和自定义角色）进行测试。</span><span class="sxs-lookup"><span data-stu-id="fb189-168">Test by using the correct security roles (default roles and custom roles) that are assigned to users.</span></span> 
- <span data-ttu-id="fb189-169">确保解决方案符合任何公司和行业特定的法规要求。</span><span class="sxs-lookup"><span data-stu-id="fb189-169">Make sure that the solution complies with any company- and industry-specific regulatory requirements.</span></span> 
- <span data-ttu-id="fb189-170">记录所有功能，并获得客户的审批和签核。</span><span class="sxs-lookup"><span data-stu-id="fb189-170">Document all features and obtain approval and sign-off from the customer.</span></span> 

## <a name="mock-go-live"></a><span data-ttu-id="fb189-171">模拟实施</span><span class="sxs-lookup"><span data-stu-id="fb189-171">Mock go-live</span></span>

<span data-ttu-id="fb189-172">在实施之前，您必须执行模拟实施，来测试从旧系统直接转换到新系统所需的步骤。</span><span class="sxs-lookup"><span data-stu-id="fb189-172">Prior to your go-live, you must perform a mock go-live to test the steps required to cutover from your legacy systems to the new system.</span></span> <span data-ttu-id="fb189-173">您应该在沙盒环境中执行模拟实施，并将所有步骤包括在直接转换计划中。</span><span class="sxs-lookup"><span data-stu-id="fb189-173">You should perform your mock go-live in a sandbox environment and include all the steps in your cutover plan.</span></span>

- <span data-ttu-id="fb189-174">我们建议您在实施之前将生产环境用作 GOLD 配置环境。</span><span class="sxs-lookup"><span data-stu-id="fb189-174">We recommend you use the production environment as the GOLD configuration environment until the go-live.</span></span>
- <span data-ttu-id="fb189-175">请确保您有一个强大的治理流程来保护生产环境，使其在实施之前免受意外交易或更新的影响。</span><span class="sxs-lookup"><span data-stu-id="fb189-175">Ensure that you have a strong governance process in place to protect the production environment from accidental transactions or updates prior to the go-live.</span></span>
- <span data-ttu-id="fb189-176">当您准备好执行 UAT 或模拟实施时，请从生产环境刷新沙盒环境。</span><span class="sxs-lookup"><span data-stu-id="fb189-176">When you're ready to perform UAT or the mock go-live, refresh the sandbox environment from the production environment.</span></span> <span data-ttu-id="fb189-177">有关详细信息，请参阅[复制实例](hr-admin-setup-copy-instance.md)。</span><span class="sxs-lookup"><span data-stu-id="fb189-177">For more information, see [Copy an instance](hr-admin-setup-copy-instance.md).</span></span>
- <span data-ttu-id="fb189-178">在沙盒环境中测试直接转换计划的每个步骤，然后通过执行抽查或从环境中的 UAT 脚本执行测试来验证沙盒环境。</span><span class="sxs-lookup"><span data-stu-id="fb189-178">Test each step of your cutover plan in the sandbox environment and then validate the sandbox environment by performing spot checks or performing tests from your UAT scripts in the environment.</span></span>
  - <span data-ttu-id="fb189-179">测试应包括所有数据迁移，包括实施所需的转换。</span><span class="sxs-lookup"><span data-stu-id="fb189-179">Tests should include all data migrations including transformations needed for the go-live.</span></span>
  - <span data-ttu-id="fb189-180">此流程应包括所有旧系统的实践截止日期。</span><span class="sxs-lookup"><span data-stu-id="fb189-180">The process should include a practice cutoff of any legacy systems.</span></span>
  - <span data-ttu-id="fb189-181">确保在模拟直接转换中包括任何集成直接转换步骤或外部系统步骤。</span><span class="sxs-lookup"><span data-stu-id="fb189-181">Be sure to include any integration cutover steps or external system steps in your mock cutover.</span></span>
- <span data-ttu-id="fb189-182">如果您在模拟转换期间发现任何问题，可能需要进行第二次模拟转换。</span><span class="sxs-lookup"><span data-stu-id="fb189-182">If you find any issues during the mock cutover, a second mock-cutover may be required.</span></span> <span data-ttu-id="fb189-183">因此，我们建议您在项目计划中计划两个模拟转换。</span><span class="sxs-lookup"><span data-stu-id="fb189-183">For this reason, we recommend that you plan for two mock cutovers in your project plan.</span></span>

## <a name="fasttrack-go-live-assessment"></a><span data-ttu-id="fb189-184">FastTrack 实行评估</span><span class="sxs-lookup"><span data-stu-id="fb189-184">FastTrack go-live assessment</span></span>

<span data-ttu-id="fb189-185">符合 FastTrack 资格并与 FastTrack 解决方案架构师合作的客户将通过 Microsoft FastTrack 完成实行审核。</span><span class="sxs-lookup"><span data-stu-id="fb189-185">Customers who are qualified for FastTrack and are engaged with a FastTrack Solution Architect will complete a go-live review with Microsoft FastTrack.</span></span> <span data-ttu-id="fb189-186">有关详细信息，请参阅  [Microsoft FastTrack](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview)。</span><span class="sxs-lookup"><span data-stu-id="fb189-186">For more information, see [Microsoft FastTrack](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview).</span></span> 

<span data-ttu-id="fb189-187">大约在实行前的八周内，FastTrack 团队会要求您填写[实行清单](https://go.microsoft.com/fwlink/?linkid=2146013)。</span><span class="sxs-lookup"><span data-stu-id="fb189-187">About eight weeks before go-live, the FastTrack team will ask you to fill in a [Go-live checklist](https://go.microsoft.com/fwlink/?linkid=2146013).</span></span>

<span data-ttu-id="fb189-188">项目经理或关键项目成员必须在项目的预先实行阶段完成实行清单。</span><span class="sxs-lookup"><span data-stu-id="fb189-188">The project manager or a key project member must complete the go-live checklist during the pre-go-live phase of the project.</span></span> <span data-ttu-id="fb189-189">通常，当 UAT 已完成或几乎完成时，清单将在建议的实行日期之前四到六周内完成。</span><span class="sxs-lookup"><span data-stu-id="fb189-189">Typically, the checklist is completed four to six weeks before the proposed go-live date, when UAT is completed or almost completed.</span></span> 

<span data-ttu-id="fb189-190">完成实行清单后，通过电子邮件将其发送给 FastTrack 解决方案架构师。</span><span class="sxs-lookup"><span data-stu-id="fb189-190">When you've completed the go-live checklist, email it to your FastTrack Solution Architect.</span></span> <span data-ttu-id="fb189-191">始终在电子邮件中包括来自客户和实施合作伙伴的关键利益相关者。</span><span class="sxs-lookup"><span data-stu-id="fb189-191">Always include a key stakeholder from the customer and the implementation partner on the email.</span></span> 

<span data-ttu-id="fb189-192">提交清单后，您的 FastTrack 解决方案架构师将审查该项目并提供评估，以描述潜在风险、最佳实践以及成功实行项目的建议。</span><span class="sxs-lookup"><span data-stu-id="fb189-192">After you submit the checklist, your FastTrack Solution Architect will review the project and provide an assessment that describes the potential risks, best practices, and recommendations for a successful go-live of the project.</span></span> <span data-ttu-id="fb189-193">在某些情况下，解决方案架构师可能会强调风险因素并要求制定缓解计划。</span><span class="sxs-lookup"><span data-stu-id="fb189-193">In some cases, the solution architect might highlight risk factors and ask for a mitigation plan.</span></span> 

## <a name="see-also"></a><span data-ttu-id="fb189-194">请参阅</span><span class="sxs-lookup"><span data-stu-id="fb189-194">See also</span></span>

[<span data-ttu-id="fb189-195">实施常见问题</span><span class="sxs-lookup"><span data-stu-id="fb189-195">Go-live FAQ</span></span>](hr-admin-go-live-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
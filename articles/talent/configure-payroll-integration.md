---
title: 配置 Talent 与 Dayforce 之间的工资单集成
description: 本主题说明如何配置 Microsoft Dynamics 365 for Talent 与 Ceridian Dayforce 之间的集成，以便处理付薪。
author: jcart1106
manager: AnnBe
ms.date: 07/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fcddf82cffb9f0ba94b83eb21809b810585ebc9e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "303393"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="aace0-103">配置 Talent 和 Dayforce 之间的工资单集成</span><span class="sxs-lookup"><span data-stu-id="aace0-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="aace0-104">Microsoft Dynamics 365 for Talent 与 Ceridian Dayforce 之间的集成依赖于本主题中介绍的几个配置步骤。</span><span class="sxs-lookup"><span data-stu-id="aace0-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="aace0-105">必须先在 Talent 和 Dayforce 中配置集成，才能处理付薪。</span><span class="sxs-lookup"><span data-stu-id="aace0-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="aace0-106">使用 Dayforce 之类服务完成付薪时，必须在 Talent 中启用集成。</span><span class="sxs-lookup"><span data-stu-id="aace0-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="aace0-107">此集成需要来自 Talent 的特定数据。</span><span class="sxs-lookup"><span data-stu-id="aace0-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="aace0-108">因此，必须验证已按照支持集成的方式在 Talent 中配置了映射到 Dayforce 的数据。</span><span class="sxs-lookup"><span data-stu-id="aace0-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="aace0-109">此集成使用下面的各种数据类别：</span><span class="sxs-lookup"><span data-stu-id="aace0-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="aace0-110">人力资源数据</span><span class="sxs-lookup"><span data-stu-id="aace0-110">Human resources data</span></span>
- <span data-ttu-id="aace0-111">薪酬数据</span><span class="sxs-lookup"><span data-stu-id="aace0-111">Compensation data</span></span>
- <span data-ttu-id="aace0-112">工资单数据，如付薪周期、付薪期间和收入代码</span><span class="sxs-lookup"><span data-stu-id="aace0-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="aace0-113">工作人员数据</span><span class="sxs-lookup"><span data-stu-id="aace0-113">Worker data</span></span>

<span data-ttu-id="aace0-114">此主题介绍要启用集成必须执行的步骤。</span><span class="sxs-lookup"><span data-stu-id="aace0-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="aace0-115">还介绍了集成所需的数据类型和配置详细信息。</span><span class="sxs-lookup"><span data-stu-id="aace0-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="aace0-116">启用集成</span><span class="sxs-lookup"><span data-stu-id="aace0-116">Enable the integration</span></span>

<span data-ttu-id="aace0-117">在 Talent 中，必须开启集成并输入配置信息，才能连接到 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="aace0-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="aace0-118">如果要将生成的的总帐交易记录导入 Microsoft Dynamics 365 for Finance and Operations 中，还必须在 Finance and Operations 只不过设置 Microsoft Azure 存储帐户和输入 Azure Storage 连接字符串。</span><span class="sxs-lookup"><span data-stu-id="aace0-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="aace0-119">要在 Talent 中开启集成，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="aace0-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="aace0-120">在**系统管理**页中，选择 **集成配置**。</span><span class="sxs-lookup"><span data-stu-id="aace0-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="aace0-121">输入安全文件传输协议 (FTP) 终结点和安全 FTP 文件夹路径。</span><span class="sxs-lookup"><span data-stu-id="aace0-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="aace0-122">输入将访问安全 FTP 终结点和文件夹路径的用户的用户名和密码。</span><span class="sxs-lookup"><span data-stu-id="aace0-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="aace0-123">根据需要测试连接，然后将**启用工资单集成**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="aace0-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="aace0-124">开启集成后，将创建数据导出包和文件，并设置频率。</span><span class="sxs-lookup"><span data-stu-id="aace0-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="aace0-125">可根据需要更改此频率。</span><span class="sxs-lookup"><span data-stu-id="aace0-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="aace0-126">有关 Azure ML 存储帐户和 Azure 存储连接字符串的详细信息，请参阅以下 Azure ML 主题：</span><span class="sxs-lookup"><span data-stu-id="aace0-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="aace0-127">关于 Azure 存储帐户</span><span class="sxs-lookup"><span data-stu-id="aace0-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="aace0-128">配置 Azure 存储连接字符串</span><span class="sxs-lookup"><span data-stu-id="aace0-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a><span data-ttu-id="aace0-129">配置数据</span><span class="sxs-lookup"><span data-stu-id="aace0-129">Configure your data</span></span> 

<span data-ttu-id="aace0-130">要处理工资单，必须在 Talent 中配置人力资源数据。</span><span class="sxs-lookup"><span data-stu-id="aace0-130">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="aace0-131">必须设置组织数据（如工作和职位），以及福利和薪酬信息。</span><span class="sxs-lookup"><span data-stu-id="aace0-131">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="aace0-132">这些信息提供生成员工付薪所需雇用、付薪和扣缴信息。</span><span class="sxs-lookup"><span data-stu-id="aace0-132">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="aace0-133">人力资源数据</span><span class="sxs-lookup"><span data-stu-id="aace0-133">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="aace0-134">福利</span><span class="sxs-lookup"><span data-stu-id="aace0-134">Benefits</span></span> 

<span data-ttu-id="aace0-135">人力资源提供工具，用于设置和维护组织提供或为其工作人员处理的福利、扣缴和工作人员薪酬计划。</span><span class="sxs-lookup"><span data-stu-id="aace0-135">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="aace0-136">创建福利时，请注意 Dayforce 中使用的以下数据和配置。</span><span class="sxs-lookup"><span data-stu-id="aace0-136">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="aace0-137">福利计划</span><span class="sxs-lookup"><span data-stu-id="aace0-137">Benefit plans</span></span>

- <span data-ttu-id="aace0-138">计划（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-138">Plan (required)</span></span>
- <span data-ttu-id="aace0-139">类型（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-139">Type (required)</span></span>
- <span data-ttu-id="aace0-140">工资单影响（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-140">Payroll impact (required)</span></span>
- <span data-ttu-id="aace0-141">恢复欠款</span><span class="sxs-lookup"><span data-stu-id="aace0-141">Recover arrears</span></span>
- <span data-ttu-id="aace0-142">扣除方法</span><span class="sxs-lookup"><span data-stu-id="aace0-142">Deduction method</span></span>
- <span data-ttu-id="aace0-143">扣除优先级</span><span class="sxs-lookup"><span data-stu-id="aace0-143">Deduction priority</span></span>
- <span data-ttu-id="aace0-144">限制期</span><span class="sxs-lookup"><span data-stu-id="aace0-144">Limit period</span></span>
- <span data-ttu-id="aace0-145">限额</span><span class="sxs-lookup"><span data-stu-id="aace0-145">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="aace0-146">福利</span><span class="sxs-lookup"><span data-stu-id="aace0-146">Benefits</span></span>

- <span data-ttu-id="aace0-147">计划（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-147">Plan (required)</span></span>
- <span data-ttu-id="aace0-148">类型（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-148">Type (required)</span></span>
- <span data-ttu-id="aace0-149">选项（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-149">Option (required)</span></span>
- <span data-ttu-id="aace0-150">福利 ID（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-150">Benefit ID (required)</span></span>
- <span data-ttu-id="aace0-151">频率</span><span class="sxs-lookup"><span data-stu-id="aace0-151">Frequency</span></span>
- <span data-ttu-id="aace0-152">基础</span><span class="sxs-lookup"><span data-stu-id="aace0-152">Basis</span></span>
- <span data-ttu-id="aace0-153">金额或费率</span><span class="sxs-lookup"><span data-stu-id="aace0-153">Amount or rate</span></span>
- <span data-ttu-id="aace0-154">收入代码</span><span class="sxs-lookup"><span data-stu-id="aace0-154">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="aace0-155">支持的频率</span><span class="sxs-lookup"><span data-stu-id="aace0-155">Supported frequencies</span></span> 

- <span data-ttu-id="aace0-156">每周</span><span class="sxs-lookup"><span data-stu-id="aace0-156">Weekly</span></span>
- <span data-ttu-id="aace0-157">两周一次</span><span class="sxs-lookup"><span data-stu-id="aace0-157">Bi-weekly</span></span>
- <span data-ttu-id="aace0-158">每半月</span><span class="sxs-lookup"><span data-stu-id="aace0-158">Semi-monthly</span></span>
- <span data-ttu-id="aace0-159">每月</span><span class="sxs-lookup"><span data-stu-id="aace0-159">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="aace0-160">支持的库</span><span class="sxs-lookup"><span data-stu-id="aace0-160">Supported bases</span></span> 

- <span data-ttu-id="aace0-161">固定金额</span><span class="sxs-lookup"><span data-stu-id="aace0-161">Fixed amount</span></span>
- <span data-ttu-id="aace0-162">收入百分比</span><span class="sxs-lookup"><span data-stu-id="aace0-162">Percent of earnings</span></span>
- <span data-ttu-id="aace0-163">工作时数</span><span class="sxs-lookup"><span data-stu-id="aace0-163">Productive hours</span></span>

<span data-ttu-id="aace0-164">Dayforce 根据福利计划中定义的工资单影响创建以下扣缴。</span><span class="sxs-lookup"><span data-stu-id="aace0-164">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="aace0-165">Talent 中的选择</span><span class="sxs-lookup"><span data-stu-id="aace0-165">Selection in Talent</span></span>        | <span data-ttu-id="aace0-166">Dayforce 中的结果</span><span class="sxs-lookup"><span data-stu-id="aace0-166">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="aace0-167">None</span><span class="sxs-lookup"><span data-stu-id="aace0-167">None</span></span>                       | <span data-ttu-id="aace0-168">不创建扣缴。</span><span class="sxs-lookup"><span data-stu-id="aace0-168">No deduction is created.</span></span>                      |
| <span data-ttu-id="aace0-169">仅扣除</span><span class="sxs-lookup"><span data-stu-id="aace0-169">Deduction only</span></span>             | <span data-ttu-id="aace0-170">创建员工扣缴。</span><span class="sxs-lookup"><span data-stu-id="aace0-170">An employee deduction is created.</span></span>             |
| <span data-ttu-id="aace0-171">仅缴纳</span><span class="sxs-lookup"><span data-stu-id="aace0-171">Contribution only</span></span>          | <span data-ttu-id="aace0-172">创建雇主扣缴。</span><span class="sxs-lookup"><span data-stu-id="aace0-172">An employer deduction is created.</span></span>             |
| <span data-ttu-id="aace0-173">扣除和缴纳</span><span class="sxs-lookup"><span data-stu-id="aace0-173">Deduction and contribution</span></span> | <span data-ttu-id="aace0-174">创建员工扣缴和雇主扣缴。</span><span class="sxs-lookup"><span data-stu-id="aace0-174">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="aace0-175">有关如何定义和管理福利计划的详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="aace0-175">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="aace0-176">交付员工福利计划</span><span class="sxs-lookup"><span data-stu-id="aace0-176">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="aace0-177">创建新福利</span><span class="sxs-lookup"><span data-stu-id="aace0-177">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="aace0-178">定义福利资格规则和策略</span><span class="sxs-lookup"><span data-stu-id="aace0-178">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="aace0-179">登记和删除工作人员的福利</span><span class="sxs-lookup"><span data-stu-id="aace0-179">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="aace0-180">薪酬</span><span class="sxs-lookup"><span data-stu-id="aace0-180">Compensation</span></span> 

<span data-ttu-id="aace0-181">薪酬管理用于控制基本工资和奖励的发放。</span><span class="sxs-lookup"><span data-stu-id="aace0-181">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="aace0-182">员工的固定基本工资和业绩调薪是通过固定薪酬计划控制的。</span><span class="sxs-lookup"><span data-stu-id="aace0-182">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="aace0-183">激励性的付款，例如额外津贴、绩效奖、股票期权和赠与以及一次性奖励，是通过可变薪酬计划控制的。</span><span class="sxs-lookup"><span data-stu-id="aace0-183">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="aace0-184">Dayforce 使用薪酬信息计算员工的时薪或年薪。</span><span class="sxs-lookup"><span data-stu-id="aace0-184">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="aace0-185">需要固定薪酬计划和付薪比率转换。</span><span class="sxs-lookup"><span data-stu-id="aace0-185">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="aace0-186">必须将员工与固定薪酬计划关联。</span><span class="sxs-lookup"><span data-stu-id="aace0-186">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="aace0-187">有关薪酬计划的详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="aace0-187">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="aace0-188">创建固定薪酬计划</span><span class="sxs-lookup"><span data-stu-id="aace0-188">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="aace0-189">创建可变薪酬计划</span><span class="sxs-lookup"><span data-stu-id="aace0-189">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="aace0-190">制订薪水/薪酬结构和计划</span><span class="sxs-lookup"><span data-stu-id="aace0-190">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="aace0-191">薪酬流程</span><span class="sxs-lookup"><span data-stu-id="aace0-191">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="aace0-192">定义薪酬流程并计算结果</span><span class="sxs-lookup"><span data-stu-id="aace0-192">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="aace0-193">在固定薪酬计划中登记员工</span><span class="sxs-lookup"><span data-stu-id="aace0-193">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="aace0-194">在可变薪酬计划中登记员工</span><span class="sxs-lookup"><span data-stu-id="aace0-194">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="aace0-195">工作</span><span class="sxs-lookup"><span data-stu-id="aace0-195">Jobs</span></span> 

<span data-ttu-id="aace0-196">作业是执行作业的人员需要承担的任务和责任的集合。</span><span class="sxs-lookup"><span data-stu-id="aace0-196">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="aace0-197">有关详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="aace0-197">For more information, see the following topics:</span></span>

- [<span data-ttu-id="aace0-198">设置作业组件</span><span class="sxs-lookup"><span data-stu-id="aace0-198">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="aace0-199">定义新工作</span><span class="sxs-lookup"><span data-stu-id="aace0-199">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="aace0-200">职位</span><span class="sxs-lookup"><span data-stu-id="aace0-200">Positions</span></span>

<span data-ttu-id="aace0-201">位置是工作的单个实例。</span><span class="sxs-lookup"><span data-stu-id="aace0-201">A position is an individual instance of a job.</span></span> <span data-ttu-id="aace0-202">例如，“销售经理（东部）”职位是与“销售经理”工作关联的职位。</span><span class="sxs-lookup"><span data-stu-id="aace0-202">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="aace0-203">职位存在于部门中。</span><span class="sxs-lookup"><span data-stu-id="aace0-203">A position exists in a department.</span></span> <span data-ttu-id="aace0-204">每个职位只能与一个工作人员关联。</span><span class="sxs-lookup"><span data-stu-id="aace0-204">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="aace0-205">设置职位时，请注意以下数据和配置：</span><span class="sxs-lookup"><span data-stu-id="aace0-205">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="aace0-206">职位（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-206">Position (required)</span></span>
- <span data-ttu-id="aace0-207">描述（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-207">Description (required)</span></span>
- <span data-ttu-id="aace0-208">工作（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-208">Job (required)</span></span>
- <span data-ttu-id="aace0-209">部门（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-209">Department (required)</span></span>
- <span data-ttu-id="aace0-210">职位类型（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-210">Position type (required)</span></span>
- <span data-ttu-id="aace0-211">全职等价</span><span class="sxs-lookup"><span data-stu-id="aace0-211">Full-time equivalent</span></span>
- <span data-ttu-id="aace0-212">年度常规时间（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-212">Annual regular hours (required)</span></span>
- <span data-ttu-id="aace0-213">由法人支付（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-213">Paid by legal entity (required)</span></span>
- <span data-ttu-id="aace0-214">付薪周期（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-214">Pay cycle (required)</span></span>
- <span data-ttu-id="aace0-215">默认财务维度 – 成本中心（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-215">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="aace0-216">工作人员分配 – 工作人员、分配开始时间、分配结束时间、原因代码</span><span class="sxs-lookup"><span data-stu-id="aace0-216">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="aace0-217">如果同一个部门中多个职位与同一个工作关联，应在 Dayforce 中将这些职位合并为一个位置。</span><span class="sxs-lookup"><span data-stu-id="aace0-217">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="aace0-218">有关详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="aace0-218">For more information, see the following topics:</span></span>

- [<span data-ttu-id="aace0-219">使用部门、工作和职位组织您的劳动力</span><span class="sxs-lookup"><span data-stu-id="aace0-219">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="aace0-220">设置职位</span><span class="sxs-lookup"><span data-stu-id="aace0-220">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="aace0-221">部门</span><span class="sxs-lookup"><span data-stu-id="aace0-221">Departments</span></span>

<span data-ttu-id="aace0-222">部门是一个运营单位，表示组织的类别或功能区域。</span><span class="sxs-lookup"><span data-stu-id="aace0-222">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="aace0-223">部门负责组织的特定区域，例如，销售、会计或人力资源。</span><span class="sxs-lookup"><span data-stu-id="aace0-223">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="aace0-224">您可以在功能区中使用要上报的部门。</span><span class="sxs-lookup"><span data-stu-id="aace0-224">You can use departments to report on functional areas.</span></span> <span data-ttu-id="aace0-225">部门可能具有损益职责。</span><span class="sxs-lookup"><span data-stu-id="aace0-225">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="aace0-226">有关详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="aace0-226">For more information, see the following topics:</span></span>

- [<span data-ttu-id="aace0-227">创建一个部门并将其与部门层次结构关联</span><span class="sxs-lookup"><span data-stu-id="aace0-227">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="aace0-228">定义新部门</span><span class="sxs-lookup"><span data-stu-id="aace0-228">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="aace0-229">付薪周期和付薪期间</span><span class="sxs-lookup"><span data-stu-id="aace0-229">Pay cycles and pay periods</span></span>

<span data-ttu-id="aace0-230">付薪周期确定付薪的频率和工作人员获薪的具体天数。</span><span class="sxs-lookup"><span data-stu-id="aace0-230">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="aace0-231">例如，付薪周期可以是每月，并且可能在月末向员工付薪。</span><span class="sxs-lookup"><span data-stu-id="aace0-231">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="aace0-232">付薪周期也可以是每周，并且可能在付薪期间结束后的星期二向员工付薪。</span><span class="sxs-lookup"><span data-stu-id="aace0-232">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="aace0-233">为职位分配付薪周期是为了控制何时向所在职位的工作人员付薪。</span><span class="sxs-lookup"><span data-stu-id="aace0-233">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="aace0-234">创建付薪周期后，可以为每个周期生成付薪期间。</span><span class="sxs-lookup"><span data-stu-id="aace0-234">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="aace0-235">每个付薪期间包含一个基于您提供的信息的默认付薪日期。</span><span class="sxs-lookup"><span data-stu-id="aace0-235">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="aace0-236">但是，可以更改付薪期间中的默认付薪日期，以便应对异常，如付薪日期在假期中。</span><span class="sxs-lookup"><span data-stu-id="aace0-236">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="aace0-237">Dayforce 中使用以下信息：</span><span class="sxs-lookup"><span data-stu-id="aace0-237">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="aace0-238">付薪周期（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-238">Pay cycle (required)</span></span>
- <span data-ttu-id="aace0-239">付薪周期频率（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-239">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="aace0-240">期间开始日期（需要第一个付薪期间）</span><span class="sxs-lookup"><span data-stu-id="aace0-240">Period start date (first pay period required)</span></span>
- <span data-ttu-id="aace0-241">默认付薪日期（需要第一个付薪期间）</span><span class="sxs-lookup"><span data-stu-id="aace0-241">Default payment date (first pay period required)</span></span>

<span data-ttu-id="aace0-242">此信息与 Dayforce 集成为付薪组，并按各付薪周期的国家或地区分隔。</span><span class="sxs-lookup"><span data-stu-id="aace0-242">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="aace0-243">集成之前，必须至少生成一个付薪期间。</span><span class="sxs-lookup"><span data-stu-id="aace0-243">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="aace0-244">Dayforce 根据 Talent 中设置的第一个付薪期间的开始日期和默认付薪日期生成付薪组日历和付薪日期。</span><span class="sxs-lookup"><span data-stu-id="aace0-244">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="aace0-245">收入代码</span><span class="sxs-lookup"><span data-stu-id="aace0-245">Earning codes</span></span>

<span data-ttu-id="aace0-246">收入代码唯一标识工作人员获得的每种收入类型。</span><span class="sxs-lookup"><span data-stu-id="aace0-246">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="aace0-247">这些代码有多个与收入有关的参数，如会计规则、税法、报告要求和补偿费功能。</span><span class="sxs-lookup"><span data-stu-id="aace0-247">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="aace0-248">Dayforce 中使用以下信息：</span><span class="sxs-lookup"><span data-stu-id="aace0-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="aace0-249">收入代码（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-249">Earning Code (required)</span></span>
- <span data-ttu-id="aace0-250">说明</span><span class="sxs-lookup"><span data-stu-id="aace0-250">Description</span></span>
- <span data-ttu-id="aace0-251">度量单位</span><span class="sxs-lookup"><span data-stu-id="aace0-251">Unit of measure</span></span>
- <span data-ttu-id="aace0-252">生产</span><span class="sxs-lookup"><span data-stu-id="aace0-252">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="aace0-253">工作人员数据</span><span class="sxs-lookup"><span data-stu-id="aace0-253">Worker data</span></span>

<span data-ttu-id="aace0-254">工作人员的对您的人力资源和工资系统十分重要的不同类型的记录。</span><span class="sxs-lookup"><span data-stu-id="aace0-254">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="aace0-255">您输入的信息可用于跟踪工作人员和个人信息。</span><span class="sxs-lookup"><span data-stu-id="aace0-255">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="aace0-256">您可以维护工作人员的以下信息:</span><span class="sxs-lookup"><span data-stu-id="aace0-256">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="aace0-257">**基本** – 维护有关工作人员的基本信息，如联系人信息、人口统计的信息、标识信息、系列信息、状态、兵役迁移国外的信息和个人和紧急事件联系人。</span><span class="sxs-lookup"><span data-stu-id="aace0-257">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="aace0-258">**雇用** – 维护有关工作人员雇用情况的信息，例如公司或组织隶属关系、职位分配、开始日期和结束日期、工作的雇用资格、条款，退休金、假期和重定位信息。</span><span class="sxs-lookup"><span data-stu-id="aace0-258">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="aace0-259">**休假和缺勤** – 维护有关工作人员的缺勤的信息，例如工作日历、缺勤事务和缺勤设置。</span><span class="sxs-lookup"><span data-stu-id="aace0-259">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="aace0-260">**薪酬和工资单** – 维护有关工作人员的薪酬计划和工资信息的信息，例如计划登记、证书、性能、佣金、税务信息、报废和薪金扣缴。</span><span class="sxs-lookup"><span data-stu-id="aace0-260">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="aace0-261">输入工作人员信息时，请注意 Dayforce 中使用的以下数据和配置。</span><span class="sxs-lookup"><span data-stu-id="aace0-261">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="aace0-262">一般信息</span><span class="sxs-lookup"><span data-stu-id="aace0-262">General information</span></span>

- <span data-ttu-id="aace0-263">人员编号（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-263">Personnel number (required)</span></span>
- <span data-ttu-id="aace0-264">名字(必填)</span><span class="sxs-lookup"><span data-stu-id="aace0-264">First name (required)</span></span>
- <span data-ttu-id="aace0-265">姓氏(必填)</span><span class="sxs-lookup"><span data-stu-id="aace0-265">Last name (required)</span></span>
- <span data-ttu-id="aace0-266">中间名</span><span class="sxs-lookup"><span data-stu-id="aace0-266">Middle name</span></span>
- <span data-ttu-id="aace0-267">受聘日期</span><span class="sxs-lookup"><span data-stu-id="aace0-267">Seniority date</span></span>
- <span data-ttu-id="aace0-268">称作</span><span class="sxs-lookup"><span data-stu-id="aace0-268">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="aace0-269">个人信息</span><span class="sxs-lookup"><span data-stu-id="aace0-269">Personal information</span></span>

- <span data-ttu-id="aace0-270">婚姻状况（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-270">Marital status (required)</span></span>
- <span data-ttu-id="aace0-271">出生日期（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-271">Birth date (required)</span></span>
- <span data-ttu-id="aace0-272">性别（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-272">Gender (required)</span></span>
- <span data-ttu-id="aace0-273">残疾人士</span><span class="sxs-lookup"><span data-stu-id="aace0-273">Person with disabilities</span></span>
- <span data-ttu-id="aace0-274">国籍的国家地区（仅适用于墨西哥）</span><span class="sxs-lookup"><span data-stu-id="aace0-274">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="aace0-275">地址信息</span><span class="sxs-lookup"><span data-stu-id="aace0-275">Address information</span></span>

- <span data-ttu-id="aace0-276">主要（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-276">Primary (required)</span></span>
- <span data-ttu-id="aace0-277">国家/地区（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-277">Country/region (required)</span></span>
- <span data-ttu-id="aace0-278">邮政编码（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-278">Postal code (required)</span></span>
- <span data-ttu-id="aace0-279">街道编号（必填）（仅适用于墨西哥）</span><span class="sxs-lookup"><span data-stu-id="aace0-279">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="aace0-280">建筑物地址（仅适用于墨西哥）</span><span class="sxs-lookup"><span data-stu-id="aace0-280">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="aace0-281"> 市/县（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-281">City (required)</span></span>
- <span data-ttu-id="aace0-282">省/直辖市/自治区（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-282">State (required)</span></span>
- <span data-ttu-id="aace0-283">国家/地区（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-283">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="aace0-284">联系人信息</span><span class="sxs-lookup"><span data-stu-id="aace0-284">Contact information</span></span> 

- <span data-ttu-id="aace0-285">主要（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-285">Primary (required)</span></span>
- <span data-ttu-id="aace0-286">联系人号码（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-286">Contact number (required)</span></span>
- <span data-ttu-id="aace0-287">函授</span><span class="sxs-lookup"><span data-stu-id="aace0-287">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="aace0-288">工资信息和收入代码</span><span class="sxs-lookup"><span data-stu-id="aace0-288">Payroll information and earning codes</span></span>

<span data-ttu-id="aace0-289">可以按给定付薪频率为员工分配特定收入，而员工则可以具有首选付款方式。</span><span class="sxs-lookup"><span data-stu-id="aace0-289">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="aace0-290">Dayforce 中使用以下字段确保使用这些首选项和设置。</span><span class="sxs-lookup"><span data-stu-id="aace0-290">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="aace0-291">收入代码</span><span class="sxs-lookup"><span data-stu-id="aace0-291">Earning codes</span></span>

- <span data-ttu-id="aace0-292">职位（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-292">Position (required)</span></span>
- <span data-ttu-id="aace0-293">收入代码（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-293">Earning Code (required)</span></span>
- <span data-ttu-id="aace0-294">频率（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-294">Frequency (required)</span></span>
- <span data-ttu-id="aace0-295">金额（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-295">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="aace0-296">工资单信息</span><span class="sxs-lookup"><span data-stu-id="aace0-296">Payroll information</span></span>

- <span data-ttu-id="aace0-297">付款方式</span><span class="sxs-lookup"><span data-stu-id="aace0-297">Payment Method</span></span>
- <span data-ttu-id="aace0-298">经济区域（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-298">Economic Region (required)</span></span>
- <span data-ttu-id="aace0-299">员工福利 ID</span><span class="sxs-lookup"><span data-stu-id="aace0-299">Employee Benefits ID</span></span>
- <span data-ttu-id="aace0-300">国家/地区 ID 号（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-300">National ID Number (required)</span></span>
- <span data-ttu-id="aace0-301">兵役编号</span><span class="sxs-lookup"><span data-stu-id="aace0-301">Military Service Number</span></span>
- <span data-ttu-id="aace0-302">班次 ID（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-302">Shift ID (required)</span></span>
- <span data-ttu-id="aace0-303">税号（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-303">Tax Number (required)</span></span>
- <span data-ttu-id="aace0-304">工会 ID（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-304">Union ID (required)</span></span>
- <span data-ttu-id="aace0-305">工作日 ID（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-305">Work Day ID (required)</span></span>
- <span data-ttu-id="aace0-306">工作许可证编号</span><span class="sxs-lookup"><span data-stu-id="aace0-306">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="aace0-307">对于付款方式，墨西哥支持**现金**、**支票**（公司的实际支票）和**电子支付**。</span><span class="sxs-lookup"><span data-stu-id="aace0-307">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="aace0-308">如果不指定付款方式，则默认使用 **支票**。</span><span class="sxs-lookup"><span data-stu-id="aace0-308">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="aace0-309">雇用详细信息</span><span class="sxs-lookup"><span data-stu-id="aace0-309">Employment details</span></span>

<span data-ttu-id="aace0-310">在 Dayforce 中派生员工的入职、离职和重新入职状态时，雇用详细信息历史记录至关重要。</span><span class="sxs-lookup"><span data-stu-id="aace0-310">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="aace0-311">Dayforce 一次仅支持一条活动雇用记录。</span><span class="sxs-lookup"><span data-stu-id="aace0-311">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="aace0-312">雇用开始日期（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-312">Employment start date (required)</span></span>
- <span data-ttu-id="aace0-313">雇佣结束日期</span><span class="sxs-lookup"><span data-stu-id="aace0-313">Employment end date</span></span>
- <span data-ttu-id="aace0-314">入职日期</span><span class="sxs-lookup"><span data-stu-id="aace0-314">Start date</span></span>
- <span data-ttu-id="aace0-315">调整后的开始日期</span><span class="sxs-lookup"><span data-stu-id="aace0-315">Adjusted start date</span></span>
- <span data-ttu-id="aace0-316">离职日期（离职时必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-316">Termination date (required upon termination)</span></span>
- <span data-ttu-id="aace0-317">离职原因（离职时必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-317">Termination reason (required upon termination)</span></span>

<span data-ttu-id="aace0-318">员工的关键日期通过使用以下信息派生。</span><span class="sxs-lookup"><span data-stu-id="aace0-318">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="aace0-319">Talent</span><span class="sxs-lookup"><span data-stu-id="aace0-319">Talent</span></span>                | <span data-ttu-id="aace0-320">Dayforce</span><span class="sxs-lookup"><span data-stu-id="aace0-320">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aace0-321">最近雇用日期</span><span class="sxs-lookup"><span data-stu-id="aace0-321">Most recent hire date</span></span> | <span data-ttu-id="aace0-322">当前未离职雇用历史记录的雇用开始日期</span><span class="sxs-lookup"><span data-stu-id="aace0-322">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="aace0-323">终止日期</span><span class="sxs-lookup"><span data-stu-id="aace0-323">Termination date</span></span>      | <span data-ttu-id="aace0-324">当前未离职雇用历史记录的离职日期</span><span class="sxs-lookup"><span data-stu-id="aace0-324">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="aace0-325">入职日期</span><span class="sxs-lookup"><span data-stu-id="aace0-325">Start date</span></span>            | <span data-ttu-id="aace0-326">当前非活动雇用历史记录经过调整后的开始日期、开始日期或雇用开始时间。</span><span class="sxs-lookup"><span data-stu-id="aace0-326">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="aace0-327">原始雇用日期</span><span class="sxs-lookup"><span data-stu-id="aace0-327">Original hire date</span></span>    | <span data-ttu-id="aace0-328">最早雇用历史记录的雇用开始时间</span><span class="sxs-lookup"><span data-stu-id="aace0-328">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="aace0-329">薪酬</span><span class="sxs-lookup"><span data-stu-id="aace0-329">Compensation</span></span>

<span data-ttu-id="aace0-330">在整个雇用期间都必须为每个员工的主要职位关联一个固定的薪酬计划。</span><span class="sxs-lookup"><span data-stu-id="aace0-330">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="aace0-331">此期间在雇用员工的日期（或雇用开始日期）开始，持续到员工离职为止。</span><span class="sxs-lookup"><span data-stu-id="aace0-331">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="aace0-332">生效日期（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-332">Effective Date (required)</span></span>
- <span data-ttu-id="aace0-333">到期日期</span><span class="sxs-lookup"><span data-stu-id="aace0-333">Expiration date</span></span>
- <span data-ttu-id="aace0-334">付薪比率（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-334">Pay Rate (required)</span></span>
- <span data-ttu-id="aace0-335">付薪比率转换（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-335">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="aace0-336">年度等价金额（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-336">Annual equivalent (required)</span></span>
- <span data-ttu-id="aace0-337">小时等价金额（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-337">Hourly equivalent (required)</span></span>

<span data-ttu-id="aace0-338">如果小时员工有多个职位，则将主要职位的固定薪酬作为员工级基本比率/工资导入 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="aace0-338">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="aace0-339">对于非主要职位，小时收费比率保存到 Dayforce 中的相应位置。</span><span class="sxs-lookup"><span data-stu-id="aace0-339">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="aace0-340">如果固定员工有多个职位，则从所有活动职位派生累积小时费率和年工资，并用作员工级基本费率/工资。</span><span class="sxs-lookup"><span data-stu-id="aace0-340">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="aace0-341">标识号</span><span class="sxs-lookup"><span data-stu-id="aace0-341">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="aace0-342">社会安全标识符</span><span class="sxs-lookup"><span data-stu-id="aace0-342">Social Security identifier</span></span> 

<span data-ttu-id="aace0-343">每个员工必须有一个主要标识符。</span><span class="sxs-lookup"><span data-stu-id="aace0-343">Every employee must have one primary identifier.</span></span> <span data-ttu-id="aace0-344">此标识符的类型必须为 **SSN** 身份证明类型。</span><span class="sxs-lookup"><span data-stu-id="aace0-344">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="aace0-345">在 Dayforce 中，将自动派生为雇用时需要的员工社会安全标识符。</span><span class="sxs-lookup"><span data-stu-id="aace0-345">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="aace0-346">主要（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-346">Primary (required)</span></span>
- <span data-ttu-id="aace0-347">身份证明类型 =“SSN”</span><span class="sxs-lookup"><span data-stu-id="aace0-347">Identification Type = "SSN"</span></span>
- <span data-ttu-id="aace0-348">签发日期</span><span class="sxs-lookup"><span data-stu-id="aace0-348">Issued Date</span></span>
- <span data-ttu-id="aace0-349">到期日期</span><span class="sxs-lookup"><span data-stu-id="aace0-349">Expiration Date</span></span>

<span data-ttu-id="aace0-350">员工可以声明 **SSN** 身份证明类型的多个身份证明编号。</span><span class="sxs-lookup"><span data-stu-id="aace0-350">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="aace0-351">但是，只会将标记为**主要**的记录集成到 Dayforce，号码是有效还是已过期无关紧要。</span><span class="sxs-lookup"><span data-stu-id="aace0-351">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="aace0-352">银行帐户和付款</span><span class="sxs-lookup"><span data-stu-id="aace0-352">Bank accounts and disbursements</span></span>

<span data-ttu-id="aace0-353">必须为选择通过银行转账付薪的员工输入有效的银行帐户信息。</span><span class="sxs-lookup"><span data-stu-id="aace0-353">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="aace0-354">Talent</span><span class="sxs-lookup"><span data-stu-id="aace0-354">Talent</span></span>                         | <span data-ttu-id="aace0-355">Dayforce</span><span class="sxs-lookup"><span data-stu-id="aace0-355">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aace0-356">银行帐号（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-356">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="aace0-357">SWIFT 代码（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-357">SWIFT code (required)</span></span>          | <span data-ttu-id="aace0-358">在墨西哥处理工资单时使用的**银行 ID** 字段。</span><span class="sxs-lookup"><span data-stu-id="aace0-358">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="aace0-359">分行编号（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-359">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="aace0-360">银行帐户类型（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-360">Bank account type (required)</span></span>   | <span data-ttu-id="aace0-361">在墨西哥处理工资单时使用的**帐户类型**字段。</span><span class="sxs-lookup"><span data-stu-id="aace0-361">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="aace0-362">支持的值包括**支票**和**工资单**。</span><span class="sxs-lookup"><span data-stu-id="aace0-362">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="aace0-363">选择通过银行转帐付薪的员工必须提供一个链接，该链接是主要地址在墨西哥且与墨西哥银行的有效银行帐户关联的法人名下的余额帐户。</span><span class="sxs-lookup"><span data-stu-id="aace0-363">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="aace0-364">将忽略其他所有非余额帐户。</span><span class="sxs-lookup"><span data-stu-id="aace0-364">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="aace0-365">地址信息</span><span class="sxs-lookup"><span data-stu-id="aace0-365">Address information</span></span>

<span data-ttu-id="aace0-366">每个员工必须有一个主要职位。</span><span class="sxs-lookup"><span data-stu-id="aace0-366">Every employee must have one primary location.</span></span> <span data-ttu-id="aace0-367">在 Dayforce 中，此职位用于确定员工的主要纳税地址。</span><span class="sxs-lookup"><span data-stu-id="aace0-367">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="aace0-368">主要（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-368">Primary (required)</span></span>
- <span data-ttu-id="aace0-369">国家/地区（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-369">Country/region (required)</span></span>
- <span data-ttu-id="aace0-370">邮政编码（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-370">Zip/postal code (required)</span></span>
- <span data-ttu-id="aace0-371">街道（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-371">Street (required)</span></span>
- <span data-ttu-id="aace0-372">街道号（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-372">Street Number (required)</span></span>
- <span data-ttu-id="aace0-373">建筑物地址</span><span class="sxs-lookup"><span data-stu-id="aace0-373">Building Complement</span></span>
- <span data-ttu-id="aace0-374"> 市/县（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-374">City (required)</span></span>
- <span data-ttu-id="aace0-375">省/直辖市/自治区（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-375">State (required)</span></span>
- <span data-ttu-id="aace0-376">国家/地区（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-376">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="aace0-377">在美国和加拿大配置数据以生成工资单</span><span class="sxs-lookup"><span data-stu-id="aace0-377">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="aace0-378">如果要在美国和加拿大为员工生成付薪，必须配置以下元素：</span><span class="sxs-lookup"><span data-stu-id="aace0-378">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="aace0-379">需要职位的部门。</span><span class="sxs-lookup"><span data-stu-id="aace0-379">Departments are required on positions.</span></span>
- <span data-ttu-id="aace0-380">必须将成本中心设置为财务维度，并且成本中心必须为默认财务维度字符串的第一个元素。</span><span class="sxs-lookup"><span data-stu-id="aace0-380">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="aace0-381">工作类型</span><span class="sxs-lookup"><span data-stu-id="aace0-381">Job types</span></span>

<span data-ttu-id="aace0-382">工作类型用于将类似的工作分组为类别。</span><span class="sxs-lookup"><span data-stu-id="aace0-382">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="aace0-383">要在美国和加拿大处理工资单，需要工作类型。</span><span class="sxs-lookup"><span data-stu-id="aace0-383">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="aace0-384">例如，工作类型包括全职和兼职，或按工资付薪和按小时付薪。</span><span class="sxs-lookup"><span data-stu-id="aace0-384">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="aace0-385">作业类型作为付薪类型映射到 Dayforce，用于指示员工按小时还是按工资付薪。</span><span class="sxs-lookup"><span data-stu-id="aace0-385">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="aace0-386">需要以下作业类型和描述。</span><span class="sxs-lookup"><span data-stu-id="aace0-386">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="aace0-387">工作类型</span><span class="sxs-lookup"><span data-stu-id="aace0-387">Job type</span></span>   | <span data-ttu-id="aace0-388">说明</span><span class="sxs-lookup"><span data-stu-id="aace0-388">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="aace0-389">每小时</span><span class="sxs-lookup"><span data-stu-id="aace0-389">Hourly</span></span>     | <span data-ttu-id="aace0-390">每小时</span><span class="sxs-lookup"><span data-stu-id="aace0-390">Hourly</span></span>      |
| <span data-ttu-id="aace0-391">按工资</span><span class="sxs-lookup"><span data-stu-id="aace0-391">Salaried</span></span>   | <span data-ttu-id="aace0-392">按工资</span><span class="sxs-lookup"><span data-stu-id="aace0-392">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="aace0-393">职位类型</span><span class="sxs-lookup"><span data-stu-id="aace0-393">Position types</span></span> 

<span data-ttu-id="aace0-394">可使用职位类型描述职位是全职、兼职还是其他。</span><span class="sxs-lookup"><span data-stu-id="aace0-394">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="aace0-395">职位类型作为付薪类别映射到 Dayforce，用于指示员工是全职还是兼职。</span><span class="sxs-lookup"><span data-stu-id="aace0-395">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="aace0-396">需要以下职位类型和描述。</span><span class="sxs-lookup"><span data-stu-id="aace0-396">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="aace0-397">职位类型</span><span class="sxs-lookup"><span data-stu-id="aace0-397">Position type</span></span>   | <span data-ttu-id="aace0-398">说明</span><span class="sxs-lookup"><span data-stu-id="aace0-398">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="aace0-399">全职</span><span class="sxs-lookup"><span data-stu-id="aace0-399">Full-time</span></span>       | <span data-ttu-id="aace0-400">全职员工</span><span class="sxs-lookup"><span data-stu-id="aace0-400">Full time employee</span></span> |
| <span data-ttu-id="aace0-401">兼职</span><span class="sxs-lookup"><span data-stu-id="aace0-401">Part-time</span></span>       | <span data-ttu-id="aace0-402">兼职员工</span><span class="sxs-lookup"><span data-stu-id="aace0-402">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="aace0-403">原因代码</span><span class="sxs-lookup"><span data-stu-id="aace0-403">Reason codes</span></span>

<span data-ttu-id="aace0-404">原因代码提供有关员工状态的信息。</span><span class="sxs-lookup"><span data-stu-id="aace0-404">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="aace0-405">原因代码作为状态代码映射到 Dayforce，用于指示更改员工的职位或雇用状态的原因。</span><span class="sxs-lookup"><span data-stu-id="aace0-405">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="aace0-406">需要以下原因代码和描述。</span><span class="sxs-lookup"><span data-stu-id="aace0-406">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="aace0-407">原因代码</span><span class="sxs-lookup"><span data-stu-id="aace0-407">Reason code</span></span>    | <span data-ttu-id="aace0-408">说明</span><span class="sxs-lookup"><span data-stu-id="aace0-408">Description</span></span>      | <span data-ttu-id="aace0-409">适用的场景</span><span class="sxs-lookup"><span data-stu-id="aace0-409">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="aace0-410">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="aace0-410">RESIGNATION</span></span>    | <span data-ttu-id="aace0-411">辞职</span><span class="sxs-lookup"><span data-stu-id="aace0-411">Resignation</span></span>      | <span data-ttu-id="aace0-412">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="aace0-412">Terminate worker</span></span>     |
| <span data-ttu-id="aace0-413">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="aace0-413">TERMINATION</span></span>    | <span data-ttu-id="aace0-414">终止</span><span class="sxs-lookup"><span data-stu-id="aace0-414">Termination</span></span>      | <span data-ttu-id="aace0-415">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="aace0-415">Terminate worker</span></span>     |
| <span data-ttu-id="aace0-416">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="aace0-416">RETIREMENT</span></span>     | <span data-ttu-id="aace0-417">退休</span><span class="sxs-lookup"><span data-stu-id="aace0-417">Retirement</span></span>       | <span data-ttu-id="aace0-418">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="aace0-418">Terminate worker</span></span>     |
| <span data-ttu-id="aace0-419">OTHER</span><span class="sxs-lookup"><span data-stu-id="aace0-419">OTHER</span></span>          | <span data-ttu-id="aace0-420">其他原因</span><span class="sxs-lookup"><span data-stu-id="aace0-420">Other Reasons</span></span>    | <span data-ttu-id="aace0-421">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="aace0-421">Terminate worker</span></span>     |
| <span data-ttu-id="aace0-422">DEATH</span><span class="sxs-lookup"><span data-stu-id="aace0-422">DEATH</span></span>          | <span data-ttu-id="aace0-423">死亡</span><span class="sxs-lookup"><span data-stu-id="aace0-423">Death</span></span>            | <span data-ttu-id="aace0-424">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="aace0-424">Terminate worker</span></span>     |
| <span data-ttu-id="aace0-425">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="aace0-425">LEAVEOFABSENCE</span></span> | <span data-ttu-id="aace0-426">休假</span><span class="sxs-lookup"><span data-stu-id="aace0-426">Leave of Absence</span></span> | <span data-ttu-id="aace0-427">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="aace0-427">Terminate worker</span></span>     |
| <span data-ttu-id="aace0-428">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="aace0-428">CONTRACTEND</span></span>    | <span data-ttu-id="aace0-429">合同结束</span><span class="sxs-lookup"><span data-stu-id="aace0-429">End of Contract</span></span>  | <span data-ttu-id="aace0-430">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="aace0-430">Terminate worker</span></span>     |
| <span data-ttu-id="aace0-431">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="aace0-431">SALARYCHANGE</span></span>   | <span data-ttu-id="aace0-432">工资改变</span><span class="sxs-lookup"><span data-stu-id="aace0-432">Change of Salary</span></span> | <span data-ttu-id="aace0-433">薪酬</span><span class="sxs-lookup"><span data-stu-id="aace0-433">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="aace0-434">婚姻状况</span><span class="sxs-lookup"><span data-stu-id="aace0-434">Marital status</span></span>

<span data-ttu-id="aace0-435">婚姻状态值映射到 Dayforce，并在集成时根据需要转换为接受的值。</span><span class="sxs-lookup"><span data-stu-id="aace0-435">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="aace0-436">下表显示婚姻状态值如何映射到 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="aace0-436">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="aace0-437">Talent</span><span class="sxs-lookup"><span data-stu-id="aace0-437">Talent</span></span>                 | <span data-ttu-id="aace0-438">Dayforce</span><span class="sxs-lookup"><span data-stu-id="aace0-438">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="aace0-439">已婚</span><span class="sxs-lookup"><span data-stu-id="aace0-439">Married</span></span>                | <span data-ttu-id="aace0-440">已婚</span><span class="sxs-lookup"><span data-stu-id="aace0-440">Married</span></span>              |
| <span data-ttu-id="aace0-441">单一</span><span class="sxs-lookup"><span data-stu-id="aace0-441">Single</span></span>                 | <span data-ttu-id="aace0-442">单一</span><span class="sxs-lookup"><span data-stu-id="aace0-442">Single</span></span>               |
| <span data-ttu-id="aace0-443">丧偶</span><span class="sxs-lookup"><span data-stu-id="aace0-443">Widowed</span></span>                | <span data-ttu-id="aace0-444">丧偶</span><span class="sxs-lookup"><span data-stu-id="aace0-444">Widowed</span></span>              |
| <span data-ttu-id="aace0-445">离异</span><span class="sxs-lookup"><span data-stu-id="aace0-445">Divorced</span></span>               | <span data-ttu-id="aace0-446">离异</span><span class="sxs-lookup"><span data-stu-id="aace0-446">Divorced</span></span>             |
| <span data-ttu-id="aace0-447">注册伴侣关系</span><span class="sxs-lookup"><span data-stu-id="aace0-447">Registered Partnership</span></span> | <span data-ttu-id="aace0-448">民事结合关系</span><span class="sxs-lookup"><span data-stu-id="aace0-448">Domestic Partnership</span></span> |
| <span data-ttu-id="aace0-449">None</span><span class="sxs-lookup"><span data-stu-id="aace0-449">None</span></span>                   | <span data-ttu-id="aace0-450">None</span><span class="sxs-lookup"><span data-stu-id="aace0-450">None</span></span>                 |
| <span data-ttu-id="aace0-451">未婚同居</span><span class="sxs-lookup"><span data-stu-id="aace0-451">Cohabiting</span></span>             | <span data-ttu-id="aace0-452">未婚同居</span><span class="sxs-lookup"><span data-stu-id="aace0-452">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="aace0-453">性</span><span class="sxs-lookup"><span data-stu-id="aace0-453">Gender</span></span>

<span data-ttu-id="aace0-454">性别指派映射到 Dayforce，并在集成时根据需要转换为接受的值。</span><span class="sxs-lookup"><span data-stu-id="aace0-454">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="aace0-455">下表显示性别指派如何映射到 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="aace0-455">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="aace0-456">Talent</span><span class="sxs-lookup"><span data-stu-id="aace0-456">Talent</span></span>       | <span data-ttu-id="aace0-457">Dayforce</span><span class="sxs-lookup"><span data-stu-id="aace0-457">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="aace0-458">男</span><span class="sxs-lookup"><span data-stu-id="aace0-458">Male</span></span>         | <span data-ttu-id="aace0-459">男</span><span class="sxs-lookup"><span data-stu-id="aace0-459">Male</span></span>            |
| <span data-ttu-id="aace0-460">女</span><span class="sxs-lookup"><span data-stu-id="aace0-460">Female</span></span>       | <span data-ttu-id="aace0-461">女</span><span class="sxs-lookup"><span data-stu-id="aace0-461">Female</span></span>          |
| <span data-ttu-id="aace0-462">非特定</span><span class="sxs-lookup"><span data-stu-id="aace0-462">Non-specific</span></span> | <span data-ttu-id="aace0-463">*不支持*</span><span class="sxs-lookup"><span data-stu-id="aace0-463">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="aace0-464">收入代码</span><span class="sxs-lookup"><span data-stu-id="aace0-464">Earning codes</span></span>

<span data-ttu-id="aace0-465">收入代码唯一标识工作人员获得的每种收入类型。</span><span class="sxs-lookup"><span data-stu-id="aace0-465">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="aace0-466">这些代码有多个与收入有关的参数，如会计规则、税法、报告要求和补偿费功能。</span><span class="sxs-lookup"><span data-stu-id="aace0-466">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="aace0-467">如果使用不受支持的频率，默认将使用**每个付薪**频率进行计算。</span><span class="sxs-lookup"><span data-stu-id="aace0-467">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="aace0-468">支持的频率</span><span class="sxs-lookup"><span data-stu-id="aace0-468">Supported frequencies</span></span>

- <span data-ttu-id="aace0-469">所有</span><span class="sxs-lookup"><span data-stu-id="aace0-469">All</span></span>
- <span data-ttu-id="aace0-470">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="aace0-470">EVERYPAY</span></span>
- <span data-ttu-id="aace0-471">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="aace0-471">EACHPAYPERIOD</span></span>
- <span data-ttu-id="aace0-472">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="aace0-472">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="aace0-473">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="aace0-473">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="aace0-474">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="aace0-474">1OFMTH</span></span>
- <span data-ttu-id="aace0-475">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="aace0-475">LASTOFMTH</span></span>
- <span data-ttu-id="aace0-476">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="aace0-476">2OFMTH</span></span>
- <span data-ttu-id="aace0-477">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="aace0-477">3OFMTH</span></span>
- <span data-ttu-id="aace0-478">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="aace0-478">4OFMTH</span></span>
- <span data-ttu-id="aace0-479">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="aace0-479">5OFMTH</span></span>
- <span data-ttu-id="aace0-480">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="aace0-480">1N2OFMTH</span></span>
- <span data-ttu-id="aace0-481">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="aace0-481">3N4OFMTH</span></span>
- <span data-ttu-id="aace0-482">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="aace0-482">1N3OFMTH</span></span>
- <span data-ttu-id="aace0-483">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="aace0-483">1N4OFMTH</span></span>
- <span data-ttu-id="aace0-484">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="aace0-484">2N3OFMTH</span></span>
- <span data-ttu-id="aace0-485">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="aace0-485">2N4OFMTH</span></span>
- <span data-ttu-id="aace0-486">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="aace0-486">1N2N3OFMTH</span></span>
- <span data-ttu-id="aace0-487">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="aace0-487">1N2N4OFMTH</span></span>
- <span data-ttu-id="aace0-488">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="aace0-488">1N3N4OFMTH</span></span>
- <span data-ttu-id="aace0-489">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="aace0-489">2N3N4OFMTH</span></span>
- <span data-ttu-id="aace0-490">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="aace0-490">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="aace0-491">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="aace0-491">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="aace0-492">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="aace0-492">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="aace0-493">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="aace0-493">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="aace0-494">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="aace0-494">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="aace0-495">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="aace0-495">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="aace0-496">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="aace0-496">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="aace0-497">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="aace0-497">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="aace0-498">地址</span><span class="sxs-lookup"><span data-stu-id="aace0-498">Addresses</span></span>

<span data-ttu-id="aace0-499">特定国家或地区、省/直辖市/自治区和县/市（自治市）代码的标识需要 Dayforce 和国内/地区内提供商可识别的特定格式。</span><span class="sxs-lookup"><span data-stu-id="aace0-499">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="aace0-500">尽管县/市的格式可变，但是每个县/市必须与一个省/直辖市/自治区关联。</span><span class="sxs-lookup"><span data-stu-id="aace0-500">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="aace0-501">Talent</span><span class="sxs-lookup"><span data-stu-id="aace0-501">Talent</span></span>          | <span data-ttu-id="aace0-502">Dayforce</span><span class="sxs-lookup"><span data-stu-id="aace0-502">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="aace0-503">国家/地区</span><span class="sxs-lookup"><span data-stu-id="aace0-503">Country/Region</span></span>  | <span data-ttu-id="aace0-504">国家/地区代码</span><span class="sxs-lookup"><span data-stu-id="aace0-504">Country Code</span></span>          |
| <span data-ttu-id="aace0-505">邮政编码 </span><span class="sxs-lookup"><span data-stu-id="aace0-505">Zip/Postal Code</span></span> | <span data-ttu-id="aace0-506">邮政编码</span><span class="sxs-lookup"><span data-stu-id="aace0-506">Postal Code</span></span>           |
| <span data-ttu-id="aace0-507">状态</span><span class="sxs-lookup"><span data-stu-id="aace0-507">State</span></span>           | <span data-ttu-id="aace0-508">省/直辖市/自治区代码</span><span class="sxs-lookup"><span data-stu-id="aace0-508">State Code</span></span>            |
| <span data-ttu-id="aace0-509">城市</span><span class="sxs-lookup"><span data-stu-id="aace0-509">City</span></span>            | <span data-ttu-id="aace0-510">城市</span><span class="sxs-lookup"><span data-stu-id="aace0-510">City</span></span>                  |
| <span data-ttu-id="aace0-511">县</span><span class="sxs-lookup"><span data-stu-id="aace0-511">County</span></span>          | <span data-ttu-id="aace0-512">县（自治市）</span><span class="sxs-lookup"><span data-stu-id="aace0-512">County (Municipality)</span></span> |
| <span data-ttu-id="aace0-513">街道</span><span class="sxs-lookup"><span data-stu-id="aace0-513">Street</span></span>          | <span data-ttu-id="aace0-514">地址行 1</span><span class="sxs-lookup"><span data-stu-id="aace0-514">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="aace0-515">税区</span><span class="sxs-lookup"><span data-stu-id="aace0-515">Tax regions</span></span>

<span data-ttu-id="aace0-516">税区用于确定应在生成工资单期间应用的适当税费。</span><span class="sxs-lookup"><span data-stu-id="aace0-516">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="aace0-517">税区作为位置地址映射到 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="aace0-517">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="aace0-518">默认税区必须与工作人员的活动职位关联。</span><span class="sxs-lookup"><span data-stu-id="aace0-518">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="aace0-519">税区（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-519">Tax region (required)</span></span>
- <span data-ttu-id="aace0-520">国家/地区（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-520">Country/Region (required)</span></span>
- <span data-ttu-id="aace0-521">省/直辖市/自治区（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-521">State (required)</span></span>
- <span data-ttu-id="aace0-522">县</span><span class="sxs-lookup"><span data-stu-id="aace0-522">County</span></span> 
- <span data-ttu-id="aace0-523"> 市/县（必填）</span><span class="sxs-lookup"><span data-stu-id="aace0-523">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="aace0-524">在墨西哥配置数据以生成工资单</span><span class="sxs-lookup"><span data-stu-id="aace0-524">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="aace0-525">如果要在墨西哥为员工生成付薪，必须配置以下元素：</span><span class="sxs-lookup"><span data-stu-id="aace0-525">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="aace0-526">需要职位的部门。</span><span class="sxs-lookup"><span data-stu-id="aace0-526">Departments are required on positions.</span></span>
- <span data-ttu-id="aace0-527">必须将成本中心设置为财务维度，并且成本中心必须为默认财务维度字符串的第一个元素。</span><span class="sxs-lookup"><span data-stu-id="aace0-527">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="aace0-528">工作类型</span><span class="sxs-lookup"><span data-stu-id="aace0-528">Job types</span></span>

<span data-ttu-id="aace0-529">工作类型用于将类似的工作分组为类别。</span><span class="sxs-lookup"><span data-stu-id="aace0-529">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="aace0-530">在墨西哥需要工作类型才能处理工资单。</span><span class="sxs-lookup"><span data-stu-id="aace0-530">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="aace0-531">例如，工作类型包括全职和兼职，或按工资付薪和按小时付薪。</span><span class="sxs-lookup"><span data-stu-id="aace0-531">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="aace0-532">作业类型作为付薪类型映射到 Dayforce，用于指示员工按小时还是按工资付薪。</span><span class="sxs-lookup"><span data-stu-id="aace0-532">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="aace0-533">需要以下作业类型和描述。</span><span class="sxs-lookup"><span data-stu-id="aace0-533">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="aace0-534">工作类型</span><span class="sxs-lookup"><span data-stu-id="aace0-534">Job type</span></span>   | <span data-ttu-id="aace0-535">说明</span><span class="sxs-lookup"><span data-stu-id="aace0-535">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="aace0-536">每小时</span><span class="sxs-lookup"><span data-stu-id="aace0-536">Hourly</span></span>     | <span data-ttu-id="aace0-537">墨西哥按小时</span><span class="sxs-lookup"><span data-stu-id="aace0-537">MX Hourly</span></span>   |
| <span data-ttu-id="aace0-538">按工资</span><span class="sxs-lookup"><span data-stu-id="aace0-538">Salaried</span></span>   | <span data-ttu-id="aace0-539">墨西哥按工资</span><span class="sxs-lookup"><span data-stu-id="aace0-539">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="aace0-540">职位类型</span><span class="sxs-lookup"><span data-stu-id="aace0-540">Position types</span></span> 

<span data-ttu-id="aace0-541">可使用职位类型描述职位是全职、兼职还是其他。</span><span class="sxs-lookup"><span data-stu-id="aace0-541">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="aace0-542">职位类型作为付薪类别映射到 Dayforce，用于指示员工是全职还是兼职。</span><span class="sxs-lookup"><span data-stu-id="aace0-542">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="aace0-543">需要以下职位类型和描述。</span><span class="sxs-lookup"><span data-stu-id="aace0-543">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="aace0-544">职位类型</span><span class="sxs-lookup"><span data-stu-id="aace0-544">Position type</span></span>   | <span data-ttu-id="aace0-545">说明</span><span class="sxs-lookup"><span data-stu-id="aace0-545">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="aace0-546">全职</span><span class="sxs-lookup"><span data-stu-id="aace0-546">Full-time</span></span>       | <span data-ttu-id="aace0-547">全职员工</span><span class="sxs-lookup"><span data-stu-id="aace0-547">Full time employee</span></span> |
| <span data-ttu-id="aace0-548">兼职</span><span class="sxs-lookup"><span data-stu-id="aace0-548">Part-time</span></span>       | <span data-ttu-id="aace0-549">兼职员工</span><span class="sxs-lookup"><span data-stu-id="aace0-549">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="aace0-550">原因代码</span><span class="sxs-lookup"><span data-stu-id="aace0-550">Reason codes</span></span>

<span data-ttu-id="aace0-551">原因代码提供有关员工状态的信息。</span><span class="sxs-lookup"><span data-stu-id="aace0-551">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="aace0-552">原因代码作为状态代码映射到 Dayforce，用于指示更改员工的职位或雇用状态的原因。</span><span class="sxs-lookup"><span data-stu-id="aace0-552">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="aace0-553">需要以下原因代码和描述。</span><span class="sxs-lookup"><span data-stu-id="aace0-553">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="aace0-554">原因代码</span><span class="sxs-lookup"><span data-stu-id="aace0-554">Reason code</span></span>            | <span data-ttu-id="aace0-555">说明</span><span class="sxs-lookup"><span data-stu-id="aace0-555">Description</span></span>                    | <span data-ttu-id="aace0-556">适用的场景</span><span class="sxs-lookup"><span data-stu-id="aace0-556">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="aace0-557">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="aace0-557">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="aace0-558">首次付薪前离职</span><span class="sxs-lookup"><span data-stu-id="aace0-558">Departure before first payroll</span></span> | <span data-ttu-id="aace0-559">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="aace0-559">Terminate worker</span></span>     |
| <span data-ttu-id="aace0-560">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="aace0-560">RESIGNATION</span></span>            | <span data-ttu-id="aace0-561">辞职</span><span class="sxs-lookup"><span data-stu-id="aace0-561">Resignation</span></span>                    | <span data-ttu-id="aace0-562">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="aace0-562">Terminate worker</span></span>     |
| <span data-ttu-id="aace0-563">PENSION</span><span class="sxs-lookup"><span data-stu-id="aace0-563">PENSION</span></span>                | <span data-ttu-id="aace0-564">退休金</span><span class="sxs-lookup"><span data-stu-id="aace0-564">Pension</span></span>                        | <span data-ttu-id="aace0-565">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="aace0-565">Terminate worker</span></span>     |
| <span data-ttu-id="aace0-566">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="aace0-566">TERMINATION</span></span>            | <span data-ttu-id="aace0-567">终止</span><span class="sxs-lookup"><span data-stu-id="aace0-567">Termination</span></span>                    | <span data-ttu-id="aace0-568">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="aace0-568">Terminate worker</span></span>     |
| <span data-ttu-id="aace0-569">退休</span><span class="sxs-lookup"><span data-stu-id="aace0-569">RETIREMENT</span></span>             | <span data-ttu-id="aace0-570">退休</span><span class="sxs-lookup"><span data-stu-id="aace0-570">Retirement</span></span>                     | <span data-ttu-id="aace0-571">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="aace0-571">Terminate worker</span></span>     |
| <span data-ttu-id="aace0-572">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="aace0-572">ABSENTEE</span></span>               | <span data-ttu-id="aace0-573">缺勤者</span><span class="sxs-lookup"><span data-stu-id="aace0-573">Absentee</span></span>                       | <span data-ttu-id="aace0-574">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="aace0-574">Terminate worker</span></span>     |
| <span data-ttu-id="aace0-575">OTHER</span><span class="sxs-lookup"><span data-stu-id="aace0-575">OTHER</span></span>                  | <span data-ttu-id="aace0-576">其他原因</span><span class="sxs-lookup"><span data-stu-id="aace0-576">Other Reasons</span></span>                  | <span data-ttu-id="aace0-577">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="aace0-577">Terminate worker</span></span>     |
| <span data-ttu-id="aace0-578">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="aace0-578">CLOSURE</span></span>                | <span data-ttu-id="aace0-579">停业</span><span class="sxs-lookup"><span data-stu-id="aace0-579">Business Closure</span></span>               | <span data-ttu-id="aace0-580">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="aace0-580">Terminate worker</span></span>     |
| <span data-ttu-id="aace0-581">DEATH</span><span class="sxs-lookup"><span data-stu-id="aace0-581">DEATH</span></span>                  | <span data-ttu-id="aace0-582">死亡</span><span class="sxs-lookup"><span data-stu-id="aace0-582">Death</span></span>                          | <span data-ttu-id="aace0-583">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="aace0-583">Terminate worker</span></span>     |
| <span data-ttu-id="aace0-584">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="aace0-584">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="aace0-585">休假</span><span class="sxs-lookup"><span data-stu-id="aace0-585">Leave of Absence</span></span>               | <span data-ttu-id="aace0-586">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="aace0-586">Terminate worker</span></span>     |
| <span data-ttu-id="aace0-587">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="aace0-587">CONTRACTEND</span></span>            | <span data-ttu-id="aace0-588">合同结束</span><span class="sxs-lookup"><span data-stu-id="aace0-588">End of Contract</span></span>                | <span data-ttu-id="aace0-589">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="aace0-589">Terminate worker</span></span>     |
| <span data-ttu-id="aace0-590">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="aace0-590">SALARYCHANGE</span></span>           | <span data-ttu-id="aace0-591">工资改变</span><span class="sxs-lookup"><span data-stu-id="aace0-591">Change of Salary</span></span>               | <span data-ttu-id="aace0-592">薪酬</span><span class="sxs-lookup"><span data-stu-id="aace0-592">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="aace0-593">雇用条款</span><span class="sxs-lookup"><span data-stu-id="aace0-593">Terms of employment</span></span>

<span data-ttu-id="aace0-594">雇用条款用于创建雇用条款的类别。</span><span class="sxs-lookup"><span data-stu-id="aace0-594">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="aace0-595">这些条款作为雇用指标值映射到 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="aace0-595">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="aace0-596">需要以下雇用条款和描述。</span><span class="sxs-lookup"><span data-stu-id="aace0-596">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="aace0-597">雇用条款</span><span class="sxs-lookup"><span data-stu-id="aace0-597">Terms of employment</span></span>   | <span data-ttu-id="aace0-598">说明</span><span class="sxs-lookup"><span data-stu-id="aace0-598">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="aace0-599">常规</span><span class="sxs-lookup"><span data-stu-id="aace0-599">Regular</span></span>               | <span data-ttu-id="aace0-600">常规</span><span class="sxs-lookup"><span data-stu-id="aace0-600">Regular</span></span>     |
| <span data-ttu-id="aace0-601">直接</span><span class="sxs-lookup"><span data-stu-id="aace0-601">Direct</span></span>                | <span data-ttu-id="aace0-602">直接</span><span class="sxs-lookup"><span data-stu-id="aace0-602">Direct</span></span>      |
| <span data-ttu-id="aace0-603">实习</span><span class="sxs-lookup"><span data-stu-id="aace0-603">Internship</span></span>            | <span data-ttu-id="aace0-604">实习</span><span class="sxs-lookup"><span data-stu-id="aace0-604">Internship</span></span>  |
| <span data-ttu-id="aace0-605">永久</span><span class="sxs-lookup"><span data-stu-id="aace0-605">Permanent</span></span>             | <span data-ttu-id="aace0-606">永久</span><span class="sxs-lookup"><span data-stu-id="aace0-606">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="aace0-607">婚姻状况</span><span class="sxs-lookup"><span data-stu-id="aace0-607">Marital status</span></span>

<span data-ttu-id="aace0-608">婚姻状态值映射到 Dayforce，并在集成时根据需要转换为接受的值。</span><span class="sxs-lookup"><span data-stu-id="aace0-608">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="aace0-609">下表显示婚姻状态值如何映射到 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="aace0-609">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="aace0-610">Talent</span><span class="sxs-lookup"><span data-stu-id="aace0-610">Talent</span></span>                 | <span data-ttu-id="aace0-611">Dayforce</span><span class="sxs-lookup"><span data-stu-id="aace0-611">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="aace0-612">已婚</span><span class="sxs-lookup"><span data-stu-id="aace0-612">Married</span></span>                | <span data-ttu-id="aace0-613">已婚</span><span class="sxs-lookup"><span data-stu-id="aace0-613">Married</span></span>                   |
| <span data-ttu-id="aace0-614">单一</span><span class="sxs-lookup"><span data-stu-id="aace0-614">Single</span></span>                 | <span data-ttu-id="aace0-615">单一</span><span class="sxs-lookup"><span data-stu-id="aace0-615">Single</span></span>                    |
| <span data-ttu-id="aace0-616">丧偶</span><span class="sxs-lookup"><span data-stu-id="aace0-616">Widowed</span></span>                | <span data-ttu-id="aace0-617">丧偶</span><span class="sxs-lookup"><span data-stu-id="aace0-617">Widowed</span></span>                   |
| <span data-ttu-id="aace0-618">离异</span><span class="sxs-lookup"><span data-stu-id="aace0-618">Divorced</span></span>               | <span data-ttu-id="aace0-619">离异</span><span class="sxs-lookup"><span data-stu-id="aace0-619">Divorced</span></span>                  |
| <span data-ttu-id="aace0-620">注册伴侣关系</span><span class="sxs-lookup"><span data-stu-id="aace0-620">Registered Partnership</span></span> | <span data-ttu-id="aace0-621">民事结合关系</span><span class="sxs-lookup"><span data-stu-id="aace0-621">Domestic Partnership</span></span>      |
| <span data-ttu-id="aace0-622">None</span><span class="sxs-lookup"><span data-stu-id="aace0-622">None</span></span>                   | <span data-ttu-id="aace0-623">*墨西哥不支持*</span><span class="sxs-lookup"><span data-stu-id="aace0-623">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="aace0-624">未婚同居</span><span class="sxs-lookup"><span data-stu-id="aace0-624">Cohabiting</span></span>             | <span data-ttu-id="aace0-625">*墨西哥不支持*</span><span class="sxs-lookup"><span data-stu-id="aace0-625">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="aace0-626">性</span><span class="sxs-lookup"><span data-stu-id="aace0-626">Gender</span></span>

<span data-ttu-id="aace0-627">性别指派映射到 Dayforce，并在集成时根据需要转换为接受的值。</span><span class="sxs-lookup"><span data-stu-id="aace0-627">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="aace0-628">下表显示性别指派如何映射到 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="aace0-628">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="aace0-629">Talent</span><span class="sxs-lookup"><span data-stu-id="aace0-629">Talent</span></span>       | <span data-ttu-id="aace0-630">Dayforce</span><span class="sxs-lookup"><span data-stu-id="aace0-630">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="aace0-631">男</span><span class="sxs-lookup"><span data-stu-id="aace0-631">Male</span></span>         | <span data-ttu-id="aace0-632">男</span><span class="sxs-lookup"><span data-stu-id="aace0-632">Male</span></span>                      |
| <span data-ttu-id="aace0-633">女</span><span class="sxs-lookup"><span data-stu-id="aace0-633">Female</span></span>       | <span data-ttu-id="aace0-634">女</span><span class="sxs-lookup"><span data-stu-id="aace0-634">Female</span></span>                    |
| <span data-ttu-id="aace0-635">非特定</span><span class="sxs-lookup"><span data-stu-id="aace0-635">Non-specific</span></span> | <span data-ttu-id="aace0-636">*墨西哥不支持*</span><span class="sxs-lookup"><span data-stu-id="aace0-636">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="aace0-637">付款方式</span><span class="sxs-lookup"><span data-stu-id="aace0-637">Payment method</span></span>

<span data-ttu-id="aace0-638">付款方式为员工和公司提供描述如何向员工付款的方式。</span><span class="sxs-lookup"><span data-stu-id="aace0-638">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="aace0-639">付款方式映射到 Dayforce，并在集成时根据需要转换为接受的值。</span><span class="sxs-lookup"><span data-stu-id="aace0-639">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="aace0-640">下表显示付款方式如何映射到 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="aace0-640">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="aace0-641">Talent</span><span class="sxs-lookup"><span data-stu-id="aace0-641">Talent</span></span>             | <span data-ttu-id="aace0-642">Dayforce</span><span class="sxs-lookup"><span data-stu-id="aace0-642">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="aace0-643">现金</span><span class="sxs-lookup"><span data-stu-id="aace0-643">Cash</span></span>               | <span data-ttu-id="aace0-644">现金</span><span class="sxs-lookup"><span data-stu-id="aace0-644">Cash</span></span>                      |
| <span data-ttu-id="aace0-645">电子支付</span><span class="sxs-lookup"><span data-stu-id="aace0-645">Electronic Payment</span></span> | <span data-ttu-id="aace0-646">转移</span><span class="sxs-lookup"><span data-stu-id="aace0-646">Transfer</span></span>                  |
| <span data-ttu-id="aace0-647">检查</span><span class="sxs-lookup"><span data-stu-id="aace0-647">Check</span></span>              | <span data-ttu-id="aace0-648">支票</span><span class="sxs-lookup"><span data-stu-id="aace0-648">Cheque</span></span>                    |
| <span data-ttu-id="aace0-649">银行汇票</span><span class="sxs-lookup"><span data-stu-id="aace0-649">Bank Draft</span></span>         | <span data-ttu-id="aace0-650">*墨西哥不支持*</span><span class="sxs-lookup"><span data-stu-id="aace0-650">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="aace0-651">其他</span><span class="sxs-lookup"><span data-stu-id="aace0-651">Other</span></span>              | <span data-ttu-id="aace0-652">*墨西哥不支持*</span><span class="sxs-lookup"><span data-stu-id="aace0-652">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="aace0-653">银行帐户类型</span><span class="sxs-lookup"><span data-stu-id="aace0-653">Bank account type</span></span>

<span data-ttu-id="aace0-654">银行帐户类型用于对员工进行电子付款。</span><span class="sxs-lookup"><span data-stu-id="aace0-654">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="aace0-655">银行账户类型作为转帐信息映射到 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="aace0-655">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="aace0-656">集成时，银行帐户类型根据需要转换为接受的值。</span><span class="sxs-lookup"><span data-stu-id="aace0-656">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="aace0-657">Talent</span><span class="sxs-lookup"><span data-stu-id="aace0-657">Talent</span></span>            | <span data-ttu-id="aace0-658">Dayforce</span><span class="sxs-lookup"><span data-stu-id="aace0-658">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="aace0-659">支票帐户</span><span class="sxs-lookup"><span data-stu-id="aace0-659">Checking Account</span></span>  | <span data-ttu-id="aace0-660">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="aace0-660">CheckingAccount</span></span>           |
| <span data-ttu-id="aace0-661">工资单帐户</span><span class="sxs-lookup"><span data-stu-id="aace0-661">Payroll Account</span></span>   | <span data-ttu-id="aace0-662">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="aace0-662">PayrollAccount</span></span>            |
| <span data-ttu-id="aace0-663">储蓄帐户</span><span class="sxs-lookup"><span data-stu-id="aace0-663">Savings Account</span></span>   | <span data-ttu-id="aace0-664">*墨西哥不支持*</span><span class="sxs-lookup"><span data-stu-id="aace0-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="aace0-665">BankGirot 帐户</span><span class="sxs-lookup"><span data-stu-id="aace0-665">BankGirot account</span></span> | <span data-ttu-id="aace0-666">*墨西哥不支持*</span><span class="sxs-lookup"><span data-stu-id="aace0-666">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="aace0-667">PlusGirot 帐户</span><span class="sxs-lookup"><span data-stu-id="aace0-667">PlusGirot account</span></span> | <span data-ttu-id="aace0-668">*墨西哥不支持*</span><span class="sxs-lookup"><span data-stu-id="aace0-668">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="aace0-669">收入代码</span><span class="sxs-lookup"><span data-stu-id="aace0-669">Earning codes</span></span>

<span data-ttu-id="aace0-670">收入代码唯一标识工作人员获得的每种收入类型。</span><span class="sxs-lookup"><span data-stu-id="aace0-670">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="aace0-671">这些代码有多个与收入有关的参数，如会计规则、税法、报告要求和补偿费功能。</span><span class="sxs-lookup"><span data-stu-id="aace0-671">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="aace0-672">如果使用不受支持的频率，默认将使用**每个付薪**频率进行计算。</span><span class="sxs-lookup"><span data-stu-id="aace0-672">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="aace0-673">支持的频率</span><span class="sxs-lookup"><span data-stu-id="aace0-673">Supported frequencies</span></span>

- <span data-ttu-id="aace0-674">所有</span><span class="sxs-lookup"><span data-stu-id="aace0-674">All</span></span>
- <span data-ttu-id="aace0-675">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="aace0-675">EVERYPAY</span></span>
- <span data-ttu-id="aace0-676">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="aace0-676">EACHPAYPERIOD</span></span>
- <span data-ttu-id="aace0-677">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="aace0-677">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="aace0-678">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="aace0-678">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="aace0-679">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="aace0-679">1OFMTH</span></span>
- <span data-ttu-id="aace0-680">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="aace0-680">LASTOFMTH</span></span>
- <span data-ttu-id="aace0-681">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="aace0-681">2OFMTH</span></span>
- <span data-ttu-id="aace0-682">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="aace0-682">3OFMTH</span></span>
- <span data-ttu-id="aace0-683">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="aace0-683">4OFMTH</span></span>
- <span data-ttu-id="aace0-684">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="aace0-684">5OFMTH</span></span>
- <span data-ttu-id="aace0-685">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="aace0-685">1N2OFMTH</span></span>
- <span data-ttu-id="aace0-686">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="aace0-686">3N4OFMTH</span></span>
- <span data-ttu-id="aace0-687">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="aace0-687">1N3OFMTH</span></span>
- <span data-ttu-id="aace0-688">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="aace0-688">1N4OFMTH</span></span>
- <span data-ttu-id="aace0-689">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="aace0-689">2N3OFMTH</span></span>
- <span data-ttu-id="aace0-690">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="aace0-690">2N4OFMTH</span></span>
- <span data-ttu-id="aace0-691">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="aace0-691">1N2N3OFMTH</span></span>
- <span data-ttu-id="aace0-692">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="aace0-692">1N2N4OFMTH</span></span>
- <span data-ttu-id="aace0-693">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="aace0-693">1N3N4OFMTH</span></span>
- <span data-ttu-id="aace0-694">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="aace0-694">2N3N4OFMTH</span></span>
- <span data-ttu-id="aace0-695">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="aace0-695">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="aace0-696">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="aace0-696">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="aace0-697">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="aace0-697">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="aace0-698">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="aace0-698">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="aace0-699">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="aace0-699">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="aace0-700">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="aace0-700">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="aace0-701">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="aace0-701">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="aace0-702">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="aace0-702">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="aace0-703">地址</span><span class="sxs-lookup"><span data-stu-id="aace0-703">Addresses</span></span>

<span data-ttu-id="aace0-704">特定国家或地区、省/直辖市/自治区和县/市（自治市）代码的标识需要 Dayforce 和国内/地区内提供商可识别的特定格式。</span><span class="sxs-lookup"><span data-stu-id="aace0-704">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="aace0-705">尽管县/市的格式可变，但是每个县/市必须与一个省/直辖市/自治区关联。</span><span class="sxs-lookup"><span data-stu-id="aace0-705">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="aace0-706">Talent</span><span class="sxs-lookup"><span data-stu-id="aace0-706">Talent</span></span>              | <span data-ttu-id="aace0-707">Dayforce</span><span class="sxs-lookup"><span data-stu-id="aace0-707">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="aace0-708">国家/地区</span><span class="sxs-lookup"><span data-stu-id="aace0-708">Country/Region</span></span>      | <span data-ttu-id="aace0-709">国家/地区代码</span><span class="sxs-lookup"><span data-stu-id="aace0-709">Country Code</span></span>          |
| <span data-ttu-id="aace0-710">邮政编码 </span><span class="sxs-lookup"><span data-stu-id="aace0-710">Zip/Postal Code</span></span>     | <span data-ttu-id="aace0-711">邮政编码</span><span class="sxs-lookup"><span data-stu-id="aace0-711">Postal Code</span></span>           |
| <span data-ttu-id="aace0-712">状态</span><span class="sxs-lookup"><span data-stu-id="aace0-712">State</span></span>               | <span data-ttu-id="aace0-713">省/直辖市/自治区代码</span><span class="sxs-lookup"><span data-stu-id="aace0-713">State Code</span></span>            |
| <span data-ttu-id="aace0-714">城市</span><span class="sxs-lookup"><span data-stu-id="aace0-714">City</span></span>                | <span data-ttu-id="aace0-715">城市</span><span class="sxs-lookup"><span data-stu-id="aace0-715">City</span></span>                  |
| <span data-ttu-id="aace0-716">县</span><span class="sxs-lookup"><span data-stu-id="aace0-716">County</span></span>              | <span data-ttu-id="aace0-717">县（自治市）</span><span class="sxs-lookup"><span data-stu-id="aace0-717">County (Municipality)</span></span> |
| <span data-ttu-id="aace0-718">街道</span><span class="sxs-lookup"><span data-stu-id="aace0-718">Street</span></span>              | <span data-ttu-id="aace0-719">地址行 1</span><span class="sxs-lookup"><span data-stu-id="aace0-719">Address Line 1</span></span>        |
| <span data-ttu-id="aace0-720">街道编号</span><span class="sxs-lookup"><span data-stu-id="aace0-720">Street Number</span></span>       | <span data-ttu-id="aace0-721">地址行 2</span><span class="sxs-lookup"><span data-stu-id="aace0-721">Address Line 2</span></span>        |
| <span data-ttu-id="aace0-722">建筑物地址</span><span class="sxs-lookup"><span data-stu-id="aace0-722">Building Complement</span></span> | <span data-ttu-id="aace0-723">地址行 5</span><span class="sxs-lookup"><span data-stu-id="aace0-723">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="aace0-724">护照号</span><span class="sxs-lookup"><span data-stu-id="aace0-724">Passport number</span></span>

<span data-ttu-id="aace0-725">员工可以声明护照信息。</span><span class="sxs-lookup"><span data-stu-id="aace0-725">Employees can declare passport information.</span></span> <span data-ttu-id="aace0-726">此信息的身份证明类型为**护照**，并作为员工的墨西哥特定信息的一部分集成到 Dayforce 中。</span><span class="sxs-lookup"><span data-stu-id="aace0-726">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="aace0-727">身份证明类型 =“护照”</span><span class="sxs-lookup"><span data-stu-id="aace0-727">Identification Type = "Passport"</span></span>
- <span data-ttu-id="aace0-728">签发日期</span><span class="sxs-lookup"><span data-stu-id="aace0-728">Issued Date</span></span>
- <span data-ttu-id="aace0-729">到期日期</span><span class="sxs-lookup"><span data-stu-id="aace0-729">Expiration Date</span></span>

<span data-ttu-id="aace0-730">员工可以声明**护照**身份证明类型的多个身份证明编号。</span><span class="sxs-lookup"><span data-stu-id="aace0-730">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="aace0-731">但是，仅将当前有效的护照条目集成到 Dayforce 中。</span><span class="sxs-lookup"><span data-stu-id="aace0-731">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="aace0-732">如果所有护照条目均已过期，将把最近签发的护照集成到 Dayforce 中。</span><span class="sxs-lookup"><span data-stu-id="aace0-732">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>

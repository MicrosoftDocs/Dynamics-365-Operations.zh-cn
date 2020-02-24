---
title: 配置与 Dayforce 的集成
description: Microsoft Dynamics 365 Human Resources 与 Ceridian Dayforce 之间的集成依赖于本文中介绍的几个配置步骤。 必须先在 Human Resources 和 Dayforce 中配置集成，才能处理付薪。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 85e7274b0e9c130e5c3426fd1fff98410f93e49a
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008178"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="c7cc9-104">配置与 Dayforce 的集成</span><span class="sxs-lookup"><span data-stu-id="c7cc9-104">Configure integration with Dayforce</span></span>

<span data-ttu-id="c7cc9-105">Microsoft Dynamics 365 Human Resources 与 Ceridian Dayforce 之间的集成依赖于本文中介绍的几个配置步骤。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="c7cc9-106">必须先在 Human Resources 和 Dayforce 中配置集成，才能处理付薪。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="c7cc9-107">使用 Dayforce 之类的服务完成付薪时，必须在 Human Resources 中启用集成。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="c7cc9-108">此集成需要来自 Human Resources 的特定数据。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="c7cc9-109">因此，必须验证已按照支持集成的方式在 Human Resources 中配置了映射到 Dayforce 的数据。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="c7cc9-110">此集成使用下面的各种数据类别：</span><span class="sxs-lookup"><span data-stu-id="c7cc9-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="c7cc9-111">人力资源数据</span><span class="sxs-lookup"><span data-stu-id="c7cc9-111">Human resources data</span></span>
- <span data-ttu-id="c7cc9-112">薪酬数据</span><span class="sxs-lookup"><span data-stu-id="c7cc9-112">Compensation data</span></span>
- <span data-ttu-id="c7cc9-113">工资单数据，如付薪周期、付薪期间和收入代码</span><span class="sxs-lookup"><span data-stu-id="c7cc9-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="c7cc9-114">工作人员数据</span><span class="sxs-lookup"><span data-stu-id="c7cc9-114">Worker data</span></span>

<span data-ttu-id="c7cc9-115">本文介绍要启用集成必须执行的步骤。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="c7cc9-116">还介绍了集成所需的数据类型和配置详细信息。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="c7cc9-117">启用集成</span><span class="sxs-lookup"><span data-stu-id="c7cc9-117">Enable the integration</span></span>

<span data-ttu-id="c7cc9-118">在 Human Resources 中，必须开启集成并输入配置信息，才能连接到 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="c7cc9-119">如果要将生成的总帐交易记录导入 Microsoft Dynamics 365 Finance 中，还必须在 Finance 中设置 Microsoft Azure 存储帐户和输入 Azure Storage 连接字符串。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="c7cc9-120">要在 Human Resources 中开启集成，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="c7cc9-121">在**系统管理**页中，选择 **集成配置**。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="c7cc9-122">输入安全文件传输协议 (FTP) 终结点和安全 FTP 文件夹路径。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="c7cc9-123">输入将访问安全 FTP 终结点和文件夹路径的用户的用户名和密码。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="c7cc9-124">根据需要测试连接，然后将**启用工资单集成**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="c7cc9-125">开启集成后，将创建数据导出包和文件，并设置频率。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="c7cc9-126">可根据需要更改此频率。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="c7cc9-127">有关 Azure ML 存储帐户和 Azure 存储连接字符串的详细信息，请参阅以下 Azure ML 文章：</span><span class="sxs-lookup"><span data-stu-id="c7cc9-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="c7cc9-128">关于 Azure 存储帐户</span><span class="sxs-lookup"><span data-stu-id="c7cc9-128">About Azure storage accounts</span></span>](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="c7cc9-129">配置 Azure 存储连接字符串</span><span class="sxs-lookup"><span data-stu-id="c7cc9-129">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="c7cc9-130">启用工资单集成后的技术详细信息</span><span class="sxs-lookup"><span data-stu-id="c7cc9-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="c7cc9-131">开启工资单集成有两大效果：</span><span class="sxs-lookup"><span data-stu-id="c7cc9-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="c7cc9-132">创建一个名称为“工资单集成导出”的数据导出项目。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="c7cc9-133">此项目中包含工资单集成需要的实体和字段。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="c7cc9-134">若要检查此项目，请转到**系统管理**，选择**数据管理**磁贴，然后从项目列表打开数据项目。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="c7cc9-135">此批处理作业执行数据导出项目，加密生成的数据包，然后将数据包文件传输到**集成配置**屏幕上配置的 SFTP 终结点。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="c7cc9-136">将使用数据包的唯一密钥加密传输到 SFTP 终结点的数据包。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="c7cc9-137">此密钥位于只有 Ceridian 才能访问的 Azure 密钥保管库。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="c7cc9-138">不能解密和检查数据包内容。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="c7cc9-139">如果需要检查数据包的内容，需要手动导出“工资单集成导出”数据终结点，下载，然后打开。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="c7cc9-140">手动导出不会应用加密或传输包。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-140">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="c7cc9-141">配置数据</span><span class="sxs-lookup"><span data-stu-id="c7cc9-141">Configure your data</span></span> 

<span data-ttu-id="c7cc9-142">要处理工资单，必须在 Human Resources 中配置人力资源数据。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-142">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="c7cc9-143">必须设置组织数据（如工作和职位），以及福利和薪酬信息。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-143">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="c7cc9-144">这些信息提供生成员工付薪所需雇用、付薪和扣缴信息。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-144">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="c7cc9-145">人力资源数据</span><span class="sxs-lookup"><span data-stu-id="c7cc9-145">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="c7cc9-146">福利</span><span class="sxs-lookup"><span data-stu-id="c7cc9-146">Benefits</span></span> 

<span data-ttu-id="c7cc9-147">人力资源提供工具，用于设置和维护组织提供或为其工作人员处理的福利、扣缴和工作人员薪酬计划。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-147">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="c7cc9-148">创建福利时，请注意 Dayforce 中使用的以下数据和配置。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-148">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="c7cc9-149">福利计划</span><span class="sxs-lookup"><span data-stu-id="c7cc9-149">Benefit plans</span></span>

- <span data-ttu-id="c7cc9-150">计划（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-150">Plan (required)</span></span>
- <span data-ttu-id="c7cc9-151">类型（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-151">Type (required)</span></span>
- <span data-ttu-id="c7cc9-152">工资单影响（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-152">Payroll impact (required)</span></span>
- <span data-ttu-id="c7cc9-153">恢复欠款</span><span class="sxs-lookup"><span data-stu-id="c7cc9-153">Recover arrears</span></span>
- <span data-ttu-id="c7cc9-154">扣除方法</span><span class="sxs-lookup"><span data-stu-id="c7cc9-154">Deduction method</span></span>
- <span data-ttu-id="c7cc9-155">扣除优先级</span><span class="sxs-lookup"><span data-stu-id="c7cc9-155">Deduction priority</span></span>
- <span data-ttu-id="c7cc9-156">限制期</span><span class="sxs-lookup"><span data-stu-id="c7cc9-156">Limit period</span></span>
- <span data-ttu-id="c7cc9-157">限额</span><span class="sxs-lookup"><span data-stu-id="c7cc9-157">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="c7cc9-158">福利</span><span class="sxs-lookup"><span data-stu-id="c7cc9-158">Benefits</span></span>

- <span data-ttu-id="c7cc9-159">计划（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-159">Plan (required)</span></span>
- <span data-ttu-id="c7cc9-160">类型（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-160">Type (required)</span></span>
- <span data-ttu-id="c7cc9-161">选项（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-161">Option (required)</span></span>
- <span data-ttu-id="c7cc9-162">福利 ID（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-162">Benefit ID (required)</span></span>
- <span data-ttu-id="c7cc9-163">频率</span><span class="sxs-lookup"><span data-stu-id="c7cc9-163">Frequency</span></span>
- <span data-ttu-id="c7cc9-164">基础</span><span class="sxs-lookup"><span data-stu-id="c7cc9-164">Basis</span></span>
- <span data-ttu-id="c7cc9-165">金额或费率</span><span class="sxs-lookup"><span data-stu-id="c7cc9-165">Amount or rate</span></span>
- <span data-ttu-id="c7cc9-166">收入代码</span><span class="sxs-lookup"><span data-stu-id="c7cc9-166">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="c7cc9-167">支持的频率</span><span class="sxs-lookup"><span data-stu-id="c7cc9-167">Supported frequencies</span></span> 

- <span data-ttu-id="c7cc9-168">每周</span><span class="sxs-lookup"><span data-stu-id="c7cc9-168">Weekly</span></span>
- <span data-ttu-id="c7cc9-169">两周一次</span><span class="sxs-lookup"><span data-stu-id="c7cc9-169">Bi-weekly</span></span>
- <span data-ttu-id="c7cc9-170">每半月</span><span class="sxs-lookup"><span data-stu-id="c7cc9-170">Semi-monthly</span></span>
- <span data-ttu-id="c7cc9-171">每月</span><span class="sxs-lookup"><span data-stu-id="c7cc9-171">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="c7cc9-172">支持的库</span><span class="sxs-lookup"><span data-stu-id="c7cc9-172">Supported bases</span></span> 

- <span data-ttu-id="c7cc9-173">固定金额</span><span class="sxs-lookup"><span data-stu-id="c7cc9-173">Fixed amount</span></span>
- <span data-ttu-id="c7cc9-174">收入百分比</span><span class="sxs-lookup"><span data-stu-id="c7cc9-174">Percent of earnings</span></span>
- <span data-ttu-id="c7cc9-175">工作时数</span><span class="sxs-lookup"><span data-stu-id="c7cc9-175">Productive hours</span></span>

<span data-ttu-id="c7cc9-176">Dayforce 根据福利计划中定义的工资单影响创建以下扣缴。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-176">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="c7cc9-177">Human Resources 中的选择</span><span class="sxs-lookup"><span data-stu-id="c7cc9-177">Selection in Human Resources</span></span>        | <span data-ttu-id="c7cc9-178">Dayforce 中的结果</span><span class="sxs-lookup"><span data-stu-id="c7cc9-178">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="c7cc9-179">否</span><span class="sxs-lookup"><span data-stu-id="c7cc9-179">None</span></span>                       | <span data-ttu-id="c7cc9-180">不创建扣缴。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-180">No deduction is created.</span></span>                      |
| <span data-ttu-id="c7cc9-181">仅扣除</span><span class="sxs-lookup"><span data-stu-id="c7cc9-181">Deduction only</span></span>             | <span data-ttu-id="c7cc9-182">创建员工扣缴。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-182">An employee deduction is created.</span></span>             |
| <span data-ttu-id="c7cc9-183">仅缴纳</span><span class="sxs-lookup"><span data-stu-id="c7cc9-183">Contribution only</span></span>          | <span data-ttu-id="c7cc9-184">创建雇主扣缴。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-184">An employer deduction is created.</span></span>             |
| <span data-ttu-id="c7cc9-185">扣除和缴纳</span><span class="sxs-lookup"><span data-stu-id="c7cc9-185">Deduction and contribution</span></span> | <span data-ttu-id="c7cc9-186">创建员工扣缴和雇主扣缴。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-186">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="c7cc9-187">有关如何定义和管理福利计划的详细信息，请参阅以下文章：</span><span class="sxs-lookup"><span data-stu-id="c7cc9-187">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="c7cc9-188">交付员工福利计划</span><span class="sxs-lookup"><span data-stu-id="c7cc9-188">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="c7cc9-189">创建新福利</span><span class="sxs-lookup"><span data-stu-id="c7cc9-189">Create a new benefit</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="c7cc9-190">定义福利资格规则和策略</span><span class="sxs-lookup"><span data-stu-id="c7cc9-190">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="c7cc9-191">登记和删除工作人员的福利</span><span class="sxs-lookup"><span data-stu-id="c7cc9-191">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="c7cc9-192">薪酬</span><span class="sxs-lookup"><span data-stu-id="c7cc9-192">Compensation</span></span> 

<span data-ttu-id="c7cc9-193">薪酬管理用于控制基本工资和奖励的发放。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-193">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="c7cc9-194">员工的固定基本工资和业绩调薪是通过固定薪酬计划控制的。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-194">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="c7cc9-195">激励性的付款，例如额外津贴、绩效奖、股票期权和赠与以及一次性奖励，是通过可变薪酬计划控制的。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-195">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="c7cc9-196">Dayforce 使用薪酬信息计算员工的时薪或年薪。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-196">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="c7cc9-197">需要固定薪酬计划和付薪比率转换。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-197">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="c7cc9-198">必须将员工与固定薪酬计划关联。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-198">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="c7cc9-199">有关薪酬计划的详细信息，请参阅以下文章：</span><span class="sxs-lookup"><span data-stu-id="c7cc9-199">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="c7cc9-200">创建固定薪酬计划</span><span class="sxs-lookup"><span data-stu-id="c7cc9-200">Create fixed compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="c7cc9-201">创建可变薪酬计划</span><span class="sxs-lookup"><span data-stu-id="c7cc9-201">Create variable compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="c7cc9-202">制订薪水/薪酬结构和计划</span><span class="sxs-lookup"><span data-stu-id="c7cc9-202">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="c7cc9-203">薪酬流程</span><span class="sxs-lookup"><span data-stu-id="c7cc9-203">Process compensation</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="c7cc9-204">定义薪酬流程并计算结果</span><span class="sxs-lookup"><span data-stu-id="c7cc9-204">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="c7cc9-205">在固定薪酬计划中登记员工</span><span class="sxs-lookup"><span data-stu-id="c7cc9-205">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="c7cc9-206">在可变薪酬计划中登记员工</span><span class="sxs-lookup"><span data-stu-id="c7cc9-206">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="c7cc9-207">工作</span><span class="sxs-lookup"><span data-stu-id="c7cc9-207">Jobs</span></span> 

<span data-ttu-id="c7cc9-208">作业是执行作业的人员需要承担的任务和责任的集合。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-208">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="c7cc9-209">有关详细信息，请参阅以下文章：</span><span class="sxs-lookup"><span data-stu-id="c7cc9-209">For more information, see the following articles:</span></span>

- [<span data-ttu-id="c7cc9-210">设置作业组件</span><span class="sxs-lookup"><span data-stu-id="c7cc9-210">Setting up the components of a job</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="c7cc9-211">定义新工作</span><span class="sxs-lookup"><span data-stu-id="c7cc9-211">Define new jobs</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="c7cc9-212">职位</span><span class="sxs-lookup"><span data-stu-id="c7cc9-212">Positions</span></span>

<span data-ttu-id="c7cc9-213">位置是工作的单个实例。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-213">A position is an individual instance of a job.</span></span> <span data-ttu-id="c7cc9-214">例如，“销售经理（东部）”职位是与“销售经理”工作关联的职位。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-214">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="c7cc9-215">职位存在于部门中。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-215">A position exists in a department.</span></span> <span data-ttu-id="c7cc9-216">每个职位只能与一个工作人员关联。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-216">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="c7cc9-217">设置职位时，请注意以下数据和配置：</span><span class="sxs-lookup"><span data-stu-id="c7cc9-217">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="c7cc9-218">职位（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-218">Position (required)</span></span>
- <span data-ttu-id="c7cc9-219">描述（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-219">Description (required)</span></span>
- <span data-ttu-id="c7cc9-220">工作（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-220">Job (required)</span></span>
- <span data-ttu-id="c7cc9-221">部门（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-221">Department (required)</span></span>
- <span data-ttu-id="c7cc9-222">职位类型（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-222">Position type (required)</span></span>
- <span data-ttu-id="c7cc9-223">全职等价</span><span class="sxs-lookup"><span data-stu-id="c7cc9-223">Full-time equivalent</span></span>
- <span data-ttu-id="c7cc9-224">年度常规时间（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-224">Annual regular hours (required)</span></span>
- <span data-ttu-id="c7cc9-225">由法人支付（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-225">Paid by legal entity (required)</span></span>
- <span data-ttu-id="c7cc9-226">付薪周期（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-226">Pay cycle (required)</span></span>
- <span data-ttu-id="c7cc9-227">默认财务维度 – 成本中心（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-227">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="c7cc9-228">工作人员分配 – 工作人员、分配开始时间、分配结束时间、原因代码</span><span class="sxs-lookup"><span data-stu-id="c7cc9-228">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="c7cc9-229">如果同一个部门中多个职位与同一个工作关联，应在 Dayforce 中将这些职位合并为一个位置。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-229">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="c7cc9-230">有关详细信息，请参阅以下文章：</span><span class="sxs-lookup"><span data-stu-id="c7cc9-230">For more information, see the following articles:</span></span>

- [<span data-ttu-id="c7cc9-231">使用部门、工作和职位组织您的劳动力</span><span class="sxs-lookup"><span data-stu-id="c7cc9-231">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="c7cc9-232">设置职位</span><span class="sxs-lookup"><span data-stu-id="c7cc9-232">Set up positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="c7cc9-233">部门</span><span class="sxs-lookup"><span data-stu-id="c7cc9-233">Departments</span></span>

<span data-ttu-id="c7cc9-234">部门是一个运营单位，表示组织的类别或功能区域。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-234">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="c7cc9-235">部门负责组织的特定区域，例如，销售、会计或人力资源。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-235">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="c7cc9-236">您可以在功能区中使用要上报的部门。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-236">You can use departments to report on functional areas.</span></span> <span data-ttu-id="c7cc9-237">部门可能具有损益职责。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-237">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="c7cc9-238">有关详细信息，请参阅以下文章：</span><span class="sxs-lookup"><span data-stu-id="c7cc9-238">For more information, see the following articles:</span></span>

- [<span data-ttu-id="c7cc9-239">创建一个部门并将其与部门层次结构关联</span><span class="sxs-lookup"><span data-stu-id="c7cc9-239">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="c7cc9-240">定义新部门</span><span class="sxs-lookup"><span data-stu-id="c7cc9-240">Define new departments</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="c7cc9-241">付薪周期和付薪期间</span><span class="sxs-lookup"><span data-stu-id="c7cc9-241">Pay cycles and pay periods</span></span>

<span data-ttu-id="c7cc9-242">付薪周期确定付薪的频率和工作人员获薪的具体天数。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-242">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="c7cc9-243">例如，付薪周期可以是每月，并且可能在月末向员工付薪。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-243">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="c7cc9-244">付薪周期也可以是每周，并且可能在付薪期间结束后的星期二向员工付薪。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-244">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="c7cc9-245">为职位分配付薪周期是为了控制何时向所在职位的工作人员付薪。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-245">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="c7cc9-246">创建付薪周期后，可以为每个周期生成付薪期间。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-246">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="c7cc9-247">每个付薪期间包含一个基于您提供的信息的默认付薪日期。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-247">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="c7cc9-248">但是，可以更改付薪期间中的默认付薪日期，以便应对异常，如付薪日期在假期中。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-248">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="c7cc9-249">Dayforce 中使用以下信息：</span><span class="sxs-lookup"><span data-stu-id="c7cc9-249">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="c7cc9-250">付薪周期（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-250">Pay cycle (required)</span></span>
- <span data-ttu-id="c7cc9-251">付薪周期频率（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-251">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="c7cc9-252">期间开始日期（需要第一个付薪期间）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-252">Period start date (first pay period required)</span></span>
- <span data-ttu-id="c7cc9-253">默认付薪日期（需要第一个付薪期间）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-253">Default payment date (first pay period required)</span></span>

<span data-ttu-id="c7cc9-254">此信息与 Dayforce 集成为付薪组，并按各付薪周期的国家或地区分隔。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-254">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="c7cc9-255">集成之前，必须至少生成一个付薪期间。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-255">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="c7cc9-256">Dayforce 根据 Human Resources 中设置的第一个付款期间的开始日期和默认付款日期生成付款组日历和付款日期。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-256">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="c7cc9-257">收入代码</span><span class="sxs-lookup"><span data-stu-id="c7cc9-257">Earning codes</span></span>

<span data-ttu-id="c7cc9-258">收入代码唯一标识工作人员获得的每种收入类型。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-258">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="c7cc9-259">这些代码有多个与收入有关的参数，如会计规则、税法、报告要求和补偿费功能。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-259">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="c7cc9-260">Dayforce 中使用以下信息：</span><span class="sxs-lookup"><span data-stu-id="c7cc9-260">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="c7cc9-261">收入代码（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-261">Earning Code (required)</span></span>
- <span data-ttu-id="c7cc9-262">说明</span><span class="sxs-lookup"><span data-stu-id="c7cc9-262">Description</span></span>
- <span data-ttu-id="c7cc9-263">度量单位</span><span class="sxs-lookup"><span data-stu-id="c7cc9-263">Unit of measure</span></span>
- <span data-ttu-id="c7cc9-264">生产</span><span class="sxs-lookup"><span data-stu-id="c7cc9-264">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="c7cc9-265">工作人员数据</span><span class="sxs-lookup"><span data-stu-id="c7cc9-265">Worker data</span></span>

<span data-ttu-id="c7cc9-266">工作人员的对您的人力资源和工资系统十分重要的不同类型的记录。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-266">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="c7cc9-267">您输入的信息可用于跟踪工作人员和个人信息。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-267">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="c7cc9-268">您可以维护工作人员的以下信息:</span><span class="sxs-lookup"><span data-stu-id="c7cc9-268">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="c7cc9-269">**基本** – 维护有关工作人员的基本信息，如联系人信息、人口统计的信息、标识信息、系列信息、状态、兵役迁移国外的信息和个人和紧急事件联系人。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-269">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="c7cc9-270">**雇用** – 维护有关工作人员雇用情况的信息，例如公司或组织隶属关系、职位分配、开始日期和结束日期、工作的雇用资格、条款，退休金、假期和重定位信息。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-270">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="c7cc9-271">**休假和缺勤** – 维护有关工作人员的缺勤的信息，例如工作日历、缺勤事务和缺勤设置。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-271">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="c7cc9-272">**薪酬和工资单** – 维护有关工作人员的薪酬计划和工资信息的信息，例如计划登记、证书、性能、佣金、税务信息、报废和薪金扣缴。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-272">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="c7cc9-273">输入工作人员信息时，请注意 Dayforce 中使用的以下数据和配置。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-273">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="c7cc9-274">一般信息</span><span class="sxs-lookup"><span data-stu-id="c7cc9-274">General information</span></span>

- <span data-ttu-id="c7cc9-275">人员编号（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-275">Personnel number (required)</span></span>
- <span data-ttu-id="c7cc9-276">名字(必填)</span><span class="sxs-lookup"><span data-stu-id="c7cc9-276">First name (required)</span></span>
- <span data-ttu-id="c7cc9-277">姓氏(必填)</span><span class="sxs-lookup"><span data-stu-id="c7cc9-277">Last name (required)</span></span>
- <span data-ttu-id="c7cc9-278">中间名</span><span class="sxs-lookup"><span data-stu-id="c7cc9-278">Middle name</span></span>
- <span data-ttu-id="c7cc9-279">受聘日期</span><span class="sxs-lookup"><span data-stu-id="c7cc9-279">Seniority date</span></span>
- <span data-ttu-id="c7cc9-280">称作</span><span class="sxs-lookup"><span data-stu-id="c7cc9-280">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="c7cc9-281">个人信息</span><span class="sxs-lookup"><span data-stu-id="c7cc9-281">Personal information</span></span>

- <span data-ttu-id="c7cc9-282">婚姻状况（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-282">Marital status (required)</span></span>
- <span data-ttu-id="c7cc9-283">出生日期（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-283">Birth date (required)</span></span>
- <span data-ttu-id="c7cc9-284">性别（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-284">Gender (required)</span></span>
- <span data-ttu-id="c7cc9-285">残疾人士</span><span class="sxs-lookup"><span data-stu-id="c7cc9-285">Person with disabilities</span></span>
- <span data-ttu-id="c7cc9-286">国籍的国家地区（仅适用于墨西哥）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-286">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="c7cc9-287">地址信息</span><span class="sxs-lookup"><span data-stu-id="c7cc9-287">Address information</span></span>

- <span data-ttu-id="c7cc9-288">主要（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-288">Primary (required)</span></span>
- <span data-ttu-id="c7cc9-289">国家/地区（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-289">Country/region (required)</span></span>
- <span data-ttu-id="c7cc9-290">邮政编码（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-290">Postal code (required)</span></span>
- <span data-ttu-id="c7cc9-291">街道编号（必填）（仅适用于墨西哥）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-291">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="c7cc9-292">建筑物地址（仅适用于墨西哥）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-292">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="c7cc9-293"> 市/县（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-293">City (required)</span></span>
- <span data-ttu-id="c7cc9-294">省/直辖市/自治区（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-294">State (required)</span></span>
- <span data-ttu-id="c7cc9-295">国家/地区（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-295">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="c7cc9-296">联系人信息</span><span class="sxs-lookup"><span data-stu-id="c7cc9-296">Contact information</span></span> 

- <span data-ttu-id="c7cc9-297">主要（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-297">Primary (required)</span></span>
- <span data-ttu-id="c7cc9-298">联系人号码（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-298">Contact number (required)</span></span>
- <span data-ttu-id="c7cc9-299">函授</span><span class="sxs-lookup"><span data-stu-id="c7cc9-299">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="c7cc9-300">工资信息和收入代码</span><span class="sxs-lookup"><span data-stu-id="c7cc9-300">Payroll information and earning codes</span></span>

<span data-ttu-id="c7cc9-301">可以按给定付薪频率为员工分配特定收入，而员工则可以具有首选付款方式。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-301">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="c7cc9-302">Dayforce 中使用以下字段确保使用这些首选项和设置。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-302">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="c7cc9-303">收入代码</span><span class="sxs-lookup"><span data-stu-id="c7cc9-303">Earning codes</span></span>

- <span data-ttu-id="c7cc9-304">职位（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-304">Position (required)</span></span>
- <span data-ttu-id="c7cc9-305">收入代码（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-305">Earning Code (required)</span></span>
- <span data-ttu-id="c7cc9-306">频率（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-306">Frequency (required)</span></span>
- <span data-ttu-id="c7cc9-307">金额（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-307">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="c7cc9-308">工资单信息</span><span class="sxs-lookup"><span data-stu-id="c7cc9-308">Payroll information</span></span>

- <span data-ttu-id="c7cc9-309">付款方式</span><span class="sxs-lookup"><span data-stu-id="c7cc9-309">Payment Method</span></span>
- <span data-ttu-id="c7cc9-310">经济区域（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-310">Economic Region (required)</span></span>
- <span data-ttu-id="c7cc9-311">员工福利 ID</span><span class="sxs-lookup"><span data-stu-id="c7cc9-311">Employee Benefits ID</span></span>
- <span data-ttu-id="c7cc9-312">国家/地区 ID 号（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-312">National ID Number (required)</span></span>
- <span data-ttu-id="c7cc9-313">兵役编号</span><span class="sxs-lookup"><span data-stu-id="c7cc9-313">Military Service Number</span></span>
- <span data-ttu-id="c7cc9-314">班次 ID（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-314">Shift ID (required)</span></span>
- <span data-ttu-id="c7cc9-315">税号（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-315">Tax Number (required)</span></span>
- <span data-ttu-id="c7cc9-316">工会 ID（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-316">Union ID (required)</span></span>
- <span data-ttu-id="c7cc9-317">工作日 ID（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-317">Work Day ID (required)</span></span>
- <span data-ttu-id="c7cc9-318">工作许可证编号</span><span class="sxs-lookup"><span data-stu-id="c7cc9-318">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="c7cc9-319">对于付款方式，墨西哥支持**现金**、**支票**（公司的实际支票）和**电子支付**。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-319">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="c7cc9-320">如果不指定付款方式，则默认使用 **支票**。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-320">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="c7cc9-321">雇用详细信息</span><span class="sxs-lookup"><span data-stu-id="c7cc9-321">Employment details</span></span>

<span data-ttu-id="c7cc9-322">在 Dayforce 中派生员工的入职、离职和重新入职状态时，雇用详细信息历史记录至关重要。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-322">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="c7cc9-323">Dayforce 一次仅支持一条活动雇用记录。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-323">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="c7cc9-324">雇用开始日期（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-324">Employment start date (required)</span></span>
- <span data-ttu-id="c7cc9-325">雇佣结束日期</span><span class="sxs-lookup"><span data-stu-id="c7cc9-325">Employment end date</span></span>
- <span data-ttu-id="c7cc9-326">入职日期</span><span class="sxs-lookup"><span data-stu-id="c7cc9-326">Start date</span></span>
- <span data-ttu-id="c7cc9-327">调整后的开始日期</span><span class="sxs-lookup"><span data-stu-id="c7cc9-327">Adjusted start date</span></span>
- <span data-ttu-id="c7cc9-328">离职日期（离职时必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-328">Termination date (required upon termination)</span></span>
- <span data-ttu-id="c7cc9-329">离职原因（离职时必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-329">Termination reason (required upon termination)</span></span>

<span data-ttu-id="c7cc9-330">员工的关键日期通过使用以下信息派生。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-330">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="c7cc9-331">人力资源</span><span class="sxs-lookup"><span data-stu-id="c7cc9-331">Human Resources</span></span>                | <span data-ttu-id="c7cc9-332">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c7cc9-332">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7cc9-333">最近雇用日期</span><span class="sxs-lookup"><span data-stu-id="c7cc9-333">Most recent hire date</span></span> | <span data-ttu-id="c7cc9-334">当前未离职雇用历史记录的雇用开始日期</span><span class="sxs-lookup"><span data-stu-id="c7cc9-334">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="c7cc9-335">终止日期</span><span class="sxs-lookup"><span data-stu-id="c7cc9-335">Termination date</span></span>      | <span data-ttu-id="c7cc9-336">当前未离职雇用历史记录的离职日期</span><span class="sxs-lookup"><span data-stu-id="c7cc9-336">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="c7cc9-337">入职日期</span><span class="sxs-lookup"><span data-stu-id="c7cc9-337">Start date</span></span>            | <span data-ttu-id="c7cc9-338">当前非活动雇用历史记录经过调整后的开始日期、开始日期或雇用开始时间。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-338">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="c7cc9-339">原始雇用日期</span><span class="sxs-lookup"><span data-stu-id="c7cc9-339">Original hire date</span></span>    | <span data-ttu-id="c7cc9-340">最早雇用历史记录的雇用开始时间</span><span class="sxs-lookup"><span data-stu-id="c7cc9-340">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="c7cc9-341">薪酬</span><span class="sxs-lookup"><span data-stu-id="c7cc9-341">Compensation</span></span>

<span data-ttu-id="c7cc9-342">在整个雇用期间都必须为每个员工的主要职位关联一个固定的薪酬计划。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-342">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="c7cc9-343">此期间在雇用员工的日期（或雇用开始日期）开始，持续到员工离职为止。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-343">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="c7cc9-344">生效日期（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-344">Effective Date (required)</span></span>
- <span data-ttu-id="c7cc9-345">到期日期</span><span class="sxs-lookup"><span data-stu-id="c7cc9-345">Expiration date</span></span>
- <span data-ttu-id="c7cc9-346">付薪比率（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-346">Pay Rate (required)</span></span>
- <span data-ttu-id="c7cc9-347">付薪比率转换（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-347">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="c7cc9-348">年度等价金额（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-348">Annual equivalent (required)</span></span>
- <span data-ttu-id="c7cc9-349">小时等价金额（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-349">Hourly equivalent (required)</span></span>

<span data-ttu-id="c7cc9-350">如果小时员工有多个职位，则将主要职位的固定薪酬作为员工级基本比率/工资导入 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-350">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="c7cc9-351">对于非主要职位，小时收费比率保存到 Dayforce 中的相应位置。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-351">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="c7cc9-352">如果固定员工有多个职位，则从所有活动职位派生累积小时费率和年工资，并用作员工级基本费率/工资。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-352">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="c7cc9-353">标识号</span><span class="sxs-lookup"><span data-stu-id="c7cc9-353">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="c7cc9-354">社会安全标识符</span><span class="sxs-lookup"><span data-stu-id="c7cc9-354">Social Security identifier</span></span> 

<span data-ttu-id="c7cc9-355">每个员工必须有一个主要标识符。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-355">Every employee must have one primary identifier.</span></span> <span data-ttu-id="c7cc9-356">此标识符的类型必须为 **SSN** 身份证明类型。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-356">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="c7cc9-357">在 Dayforce 中，将自动派生为雇用时需要的员工社会安全标识符。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-357">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="c7cc9-358">主要（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-358">Primary (required)</span></span>
- <span data-ttu-id="c7cc9-359">身份证明类型 =“SSN”</span><span class="sxs-lookup"><span data-stu-id="c7cc9-359">Identification Type = "SSN"</span></span>
- <span data-ttu-id="c7cc9-360">签发日期</span><span class="sxs-lookup"><span data-stu-id="c7cc9-360">Issued Date</span></span>
- <span data-ttu-id="c7cc9-361">到期日期</span><span class="sxs-lookup"><span data-stu-id="c7cc9-361">Expiration Date</span></span>

<span data-ttu-id="c7cc9-362">员工可以声明 **SSN** 身份证明类型的多个身份证明编号。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-362">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="c7cc9-363">但是，只会将标记为**主要**的记录集成到 Dayforce，号码是有效还是已过期无关紧要。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-363">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="c7cc9-364">银行帐户和付款</span><span class="sxs-lookup"><span data-stu-id="c7cc9-364">Bank accounts and disbursements</span></span>

<span data-ttu-id="c7cc9-365">必须为选择通过银行转账付薪的员工输入有效的银行帐户信息。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-365">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="c7cc9-366">人力资源</span><span class="sxs-lookup"><span data-stu-id="c7cc9-366">Human Resources</span></span>                         | <span data-ttu-id="c7cc9-367">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c7cc9-367">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7cc9-368">银行帐号（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-368">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="c7cc9-369">SWIFT 代码（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-369">SWIFT code (required)</span></span>          | <span data-ttu-id="c7cc9-370">在墨西哥处理工资单时使用的**银行 ID** 字段。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-370">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="c7cc9-371">分行编号（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-371">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="c7cc9-372">银行帐户类型（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-372">Bank account type (required)</span></span>   | <span data-ttu-id="c7cc9-373">在墨西哥处理工资单时使用的**帐户类型**字段。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-373">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="c7cc9-374">支持的值包括**支票**和**工资单**。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-374">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="c7cc9-375">选择通过银行转帐付薪的员工必须提供一个链接，该链接是主要地址在墨西哥且与墨西哥银行的有效银行帐户关联的法人名下的余额帐户。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-375">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="c7cc9-376">将忽略其他所有非余额帐户。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-376">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="c7cc9-377">地址信息</span><span class="sxs-lookup"><span data-stu-id="c7cc9-377">Address information</span></span>

<span data-ttu-id="c7cc9-378">每个员工必须有一个主要职位。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-378">Every employee must have one primary location.</span></span> <span data-ttu-id="c7cc9-379">在 Dayforce 中，此职位用于确定员工的主要纳税地址。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-379">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="c7cc9-380">主要（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-380">Primary (required)</span></span>
- <span data-ttu-id="c7cc9-381">国家/地区（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-381">Country/region (required)</span></span>
- <span data-ttu-id="c7cc9-382">邮政编码（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-382">Zip/postal code (required)</span></span>
- <span data-ttu-id="c7cc9-383">街道（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-383">Street (required)</span></span>
- <span data-ttu-id="c7cc9-384">街道号（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-384">Street Number (required)</span></span>
- <span data-ttu-id="c7cc9-385">建筑物地址</span><span class="sxs-lookup"><span data-stu-id="c7cc9-385">Building Complement</span></span>
- <span data-ttu-id="c7cc9-386"> 市/县（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-386">City (required)</span></span>
- <span data-ttu-id="c7cc9-387">省/直辖市/自治区（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-387">State (required)</span></span>
- <span data-ttu-id="c7cc9-388">国家/地区（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-388">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="c7cc9-389">在美国和加拿大配置数据以生成工资单</span><span class="sxs-lookup"><span data-stu-id="c7cc9-389">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="c7cc9-390">如果要在美国和加拿大为员工生成付薪，必须配置以下元素：</span><span class="sxs-lookup"><span data-stu-id="c7cc9-390">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="c7cc9-391">需要职位的部门。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-391">Departments are required on positions.</span></span>
- <span data-ttu-id="c7cc9-392">必须将成本中心设置为财务维度，并且成本中心必须为默认财务维度字符串的第一个元素。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-392">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="c7cc9-393">可以配置 Human Resources，以便要求在“职位”中指定“部门”。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-393">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="c7cc9-394">方法是，转到**人力资源共享职位 > 职位 > 必填职位中的部门**。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-394">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="c7cc9-395">建议为集成实施此项设置。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-395">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="c7cc9-396">工作类型</span><span class="sxs-lookup"><span data-stu-id="c7cc9-396">Job types</span></span>

<span data-ttu-id="c7cc9-397">工作类型用于将类似的工作分组为类别。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-397">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="c7cc9-398">要在美国和加拿大处理工资单，需要工作类型。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-398">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="c7cc9-399">例如，工作类型包括全职和兼职，或按工资付薪和按小时付薪。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-399">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="c7cc9-400">作业类型作为付薪类型映射到 Dayforce，用于指示员工按小时还是按工资付薪。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-400">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="c7cc9-401">需要以下作业类型和描述。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-401">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="c7cc9-402">工作类型</span><span class="sxs-lookup"><span data-stu-id="c7cc9-402">Job type</span></span>   | <span data-ttu-id="c7cc9-403">说明</span><span class="sxs-lookup"><span data-stu-id="c7cc9-403">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="c7cc9-404">每小时</span><span class="sxs-lookup"><span data-stu-id="c7cc9-404">Hourly</span></span>     | <span data-ttu-id="c7cc9-405">每小时</span><span class="sxs-lookup"><span data-stu-id="c7cc9-405">Hourly</span></span>      |
| <span data-ttu-id="c7cc9-406">按工资</span><span class="sxs-lookup"><span data-stu-id="c7cc9-406">Salaried</span></span>   | <span data-ttu-id="c7cc9-407">按工资</span><span class="sxs-lookup"><span data-stu-id="c7cc9-407">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="c7cc9-408">职位类型</span><span class="sxs-lookup"><span data-stu-id="c7cc9-408">Position types</span></span> 

<span data-ttu-id="c7cc9-409">可使用职位类型描述职位是全职、兼职还是其他。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-409">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="c7cc9-410">职位类型作为付薪类别映射到 Dayforce，用于指示员工是全职还是兼职。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-410">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="c7cc9-411">需要以下职位类型和描述。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-411">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="c7cc9-412">职位类型</span><span class="sxs-lookup"><span data-stu-id="c7cc9-412">Position type</span></span>   | <span data-ttu-id="c7cc9-413">说明</span><span class="sxs-lookup"><span data-stu-id="c7cc9-413">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="c7cc9-414">全职</span><span class="sxs-lookup"><span data-stu-id="c7cc9-414">Full-time</span></span>       | <span data-ttu-id="c7cc9-415">全职员工</span><span class="sxs-lookup"><span data-stu-id="c7cc9-415">Full time employee</span></span> |
| <span data-ttu-id="c7cc9-416">兼职</span><span class="sxs-lookup"><span data-stu-id="c7cc9-416">Part-time</span></span>       | <span data-ttu-id="c7cc9-417">兼职员工</span><span class="sxs-lookup"><span data-stu-id="c7cc9-417">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="c7cc9-418">原因代码</span><span class="sxs-lookup"><span data-stu-id="c7cc9-418">Reason codes</span></span>

<span data-ttu-id="c7cc9-419">原因代码提供有关员工状态的信息。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-419">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="c7cc9-420">原因代码作为状态代码映射到 Dayforce，用于指示更改员工的职位或雇用状态的原因。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-420">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="c7cc9-421">需要以下原因代码和描述。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-421">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="c7cc9-422">原因代码</span><span class="sxs-lookup"><span data-stu-id="c7cc9-422">Reason code</span></span>    | <span data-ttu-id="c7cc9-423">说明</span><span class="sxs-lookup"><span data-stu-id="c7cc9-423">Description</span></span>      | <span data-ttu-id="c7cc9-424">适用的场景</span><span class="sxs-lookup"><span data-stu-id="c7cc9-424">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="c7cc9-425">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="c7cc9-425">RESIGNATION</span></span>    | <span data-ttu-id="c7cc9-426">辞职</span><span class="sxs-lookup"><span data-stu-id="c7cc9-426">Resignation</span></span>      | <span data-ttu-id="c7cc9-427">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="c7cc9-427">Terminate worker</span></span>     |
| <span data-ttu-id="c7cc9-428">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="c7cc9-428">TERMINATION</span></span>    | <span data-ttu-id="c7cc9-429">终止</span><span class="sxs-lookup"><span data-stu-id="c7cc9-429">Termination</span></span>      | <span data-ttu-id="c7cc9-430">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="c7cc9-430">Terminate worker</span></span>     |
| <span data-ttu-id="c7cc9-431">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="c7cc9-431">RETIREMENT</span></span>     | <span data-ttu-id="c7cc9-432">退休</span><span class="sxs-lookup"><span data-stu-id="c7cc9-432">Retirement</span></span>       | <span data-ttu-id="c7cc9-433">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="c7cc9-433">Terminate worker</span></span>     |
| <span data-ttu-id="c7cc9-434">OTHER</span><span class="sxs-lookup"><span data-stu-id="c7cc9-434">OTHER</span></span>          | <span data-ttu-id="c7cc9-435">其他原因</span><span class="sxs-lookup"><span data-stu-id="c7cc9-435">Other Reasons</span></span>    | <span data-ttu-id="c7cc9-436">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="c7cc9-436">Terminate worker</span></span>     |
| <span data-ttu-id="c7cc9-437">DEATH</span><span class="sxs-lookup"><span data-stu-id="c7cc9-437">DEATH</span></span>          | <span data-ttu-id="c7cc9-438">死亡</span><span class="sxs-lookup"><span data-stu-id="c7cc9-438">Death</span></span>            | <span data-ttu-id="c7cc9-439">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="c7cc9-439">Terminate worker</span></span>     |
| <span data-ttu-id="c7cc9-440">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="c7cc9-440">LEAVEOFABSENCE</span></span> | <span data-ttu-id="c7cc9-441">休假</span><span class="sxs-lookup"><span data-stu-id="c7cc9-441">Leave of Absence</span></span> | <span data-ttu-id="c7cc9-442">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="c7cc9-442">Terminate worker</span></span>     |
| <span data-ttu-id="c7cc9-443">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="c7cc9-443">CONTRACTEND</span></span>    | <span data-ttu-id="c7cc9-444">合同结束</span><span class="sxs-lookup"><span data-stu-id="c7cc9-444">End of Contract</span></span>  | <span data-ttu-id="c7cc9-445">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="c7cc9-445">Terminate worker</span></span>     |
| <span data-ttu-id="c7cc9-446">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="c7cc9-446">SALARYCHANGE</span></span>   | <span data-ttu-id="c7cc9-447">工资改变</span><span class="sxs-lookup"><span data-stu-id="c7cc9-447">Change of Salary</span></span> | <span data-ttu-id="c7cc9-448">薪酬</span><span class="sxs-lookup"><span data-stu-id="c7cc9-448">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="c7cc9-449">婚姻状况</span><span class="sxs-lookup"><span data-stu-id="c7cc9-449">Marital status</span></span>

<span data-ttu-id="c7cc9-450">婚姻状态值映射到 Dayforce，并在集成时根据需要转换为接受的值。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-450">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="c7cc9-451">下表显示婚姻状态值如何映射到 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-451">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="c7cc9-452">人力资源</span><span class="sxs-lookup"><span data-stu-id="c7cc9-452">Human Resources</span></span>                 | <span data-ttu-id="c7cc9-453">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c7cc9-453">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="c7cc9-454">已婚</span><span class="sxs-lookup"><span data-stu-id="c7cc9-454">Married</span></span>                | <span data-ttu-id="c7cc9-455">已婚</span><span class="sxs-lookup"><span data-stu-id="c7cc9-455">Married</span></span>              |
| <span data-ttu-id="c7cc9-456">单一</span><span class="sxs-lookup"><span data-stu-id="c7cc9-456">Single</span></span>                 | <span data-ttu-id="c7cc9-457">单一</span><span class="sxs-lookup"><span data-stu-id="c7cc9-457">Single</span></span>               |
| <span data-ttu-id="c7cc9-458">丧偶</span><span class="sxs-lookup"><span data-stu-id="c7cc9-458">Widowed</span></span>                | <span data-ttu-id="c7cc9-459">丧偶</span><span class="sxs-lookup"><span data-stu-id="c7cc9-459">Widowed</span></span>              |
| <span data-ttu-id="c7cc9-460">离婚</span><span class="sxs-lookup"><span data-stu-id="c7cc9-460">Divorced</span></span>               | <span data-ttu-id="c7cc9-461">离异</span><span class="sxs-lookup"><span data-stu-id="c7cc9-461">Divorced</span></span>             |
| <span data-ttu-id="c7cc9-462">注册伴侣关系</span><span class="sxs-lookup"><span data-stu-id="c7cc9-462">Registered Partnership</span></span> | <span data-ttu-id="c7cc9-463">民事结合关系</span><span class="sxs-lookup"><span data-stu-id="c7cc9-463">Domestic Partnership</span></span> |
| <span data-ttu-id="c7cc9-464">None</span><span class="sxs-lookup"><span data-stu-id="c7cc9-464">None</span></span>                   | <span data-ttu-id="c7cc9-465">None</span><span class="sxs-lookup"><span data-stu-id="c7cc9-465">None</span></span>                 |
| <span data-ttu-id="c7cc9-466">未婚同居</span><span class="sxs-lookup"><span data-stu-id="c7cc9-466">Cohabiting</span></span>             | <span data-ttu-id="c7cc9-467">未婚同居</span><span class="sxs-lookup"><span data-stu-id="c7cc9-467">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="c7cc9-468">性</span><span class="sxs-lookup"><span data-stu-id="c7cc9-468">Gender</span></span>

<span data-ttu-id="c7cc9-469">性别指派映射到 Dayforce，并在集成时根据需要转换为接受的值。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-469">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="c7cc9-470">下表显示性别指派如何映射到 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-470">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="c7cc9-471">人力资源</span><span class="sxs-lookup"><span data-stu-id="c7cc9-471">Human Resources</span></span>       | <span data-ttu-id="c7cc9-472">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c7cc9-472">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="c7cc9-473">男</span><span class="sxs-lookup"><span data-stu-id="c7cc9-473">Male</span></span>         | <span data-ttu-id="c7cc9-474">男</span><span class="sxs-lookup"><span data-stu-id="c7cc9-474">Male</span></span>            |
| <span data-ttu-id="c7cc9-475">女</span><span class="sxs-lookup"><span data-stu-id="c7cc9-475">Female</span></span>       | <span data-ttu-id="c7cc9-476">女</span><span class="sxs-lookup"><span data-stu-id="c7cc9-476">Female</span></span>          |
| <span data-ttu-id="c7cc9-477">非特定</span><span class="sxs-lookup"><span data-stu-id="c7cc9-477">Non-specific</span></span> | <span data-ttu-id="c7cc9-478">*不支持*</span><span class="sxs-lookup"><span data-stu-id="c7cc9-478">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="c7cc9-479">收入代码</span><span class="sxs-lookup"><span data-stu-id="c7cc9-479">Earning codes</span></span>

<span data-ttu-id="c7cc9-480">收入代码唯一标识工作人员获得的每种收入类型。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-480">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="c7cc9-481">这些代码有多个与收入有关的参数，如会计规则、税法、报告要求和补偿费功能。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-481">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="c7cc9-482">如果使用不受支持的频率，默认将使用**每个付薪**频率进行计算。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-482">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="c7cc9-483">支持的频率</span><span class="sxs-lookup"><span data-stu-id="c7cc9-483">Supported frequencies</span></span>

- <span data-ttu-id="c7cc9-484">所有</span><span class="sxs-lookup"><span data-stu-id="c7cc9-484">All</span></span>
- <span data-ttu-id="c7cc9-485">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="c7cc9-485">EVERYPAY</span></span>
- <span data-ttu-id="c7cc9-486">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="c7cc9-486">EACHPAYPERIOD</span></span>
- <span data-ttu-id="c7cc9-487">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="c7cc9-487">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="c7cc9-488">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="c7cc9-488">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="c7cc9-489">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7cc9-489">1OFMTH</span></span>
- <span data-ttu-id="c7cc9-490">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="c7cc9-490">LASTOFMTH</span></span>
- <span data-ttu-id="c7cc9-491">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7cc9-491">2OFMTH</span></span>
- <span data-ttu-id="c7cc9-492">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7cc9-492">3OFMTH</span></span>
- <span data-ttu-id="c7cc9-493">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7cc9-493">4OFMTH</span></span>
- <span data-ttu-id="c7cc9-494">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7cc9-494">5OFMTH</span></span>
- <span data-ttu-id="c7cc9-495">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7cc9-495">1N2OFMTH</span></span>
- <span data-ttu-id="c7cc9-496">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7cc9-496">3N4OFMTH</span></span>
- <span data-ttu-id="c7cc9-497">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7cc9-497">1N3OFMTH</span></span>
- <span data-ttu-id="c7cc9-498">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7cc9-498">1N4OFMTH</span></span>
- <span data-ttu-id="c7cc9-499">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7cc9-499">2N3OFMTH</span></span>
- <span data-ttu-id="c7cc9-500">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7cc9-500">2N4OFMTH</span></span>
- <span data-ttu-id="c7cc9-501">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7cc9-501">1N2N3OFMTH</span></span>
- <span data-ttu-id="c7cc9-502">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7cc9-502">1N2N4OFMTH</span></span>
- <span data-ttu-id="c7cc9-503">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7cc9-503">1N3N4OFMTH</span></span>
- <span data-ttu-id="c7cc9-504">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7cc9-504">2N3N4OFMTH</span></span>
- <span data-ttu-id="c7cc9-505">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7cc9-505">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="c7cc9-506">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="c7cc9-506">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="c7cc9-507">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="c7cc9-507">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="c7cc9-508">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="c7cc9-508">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="c7cc9-509">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="c7cc9-509">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="c7cc9-510">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="c7cc9-510">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="c7cc9-511">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="c7cc9-511">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="c7cc9-512">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="c7cc9-512">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="c7cc9-513">地址</span><span class="sxs-lookup"><span data-stu-id="c7cc9-513">Addresses</span></span>

<span data-ttu-id="c7cc9-514">特定国家或地区、省/直辖市/自治区和县/市（自治市）代码的标识需要 Dayforce 和国内/地区内提供商可识别的特定格式。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-514">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="c7cc9-515">尽管县/市的格式可变，但是每个县/市必须与一个省/直辖市/自治区关联。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-515">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="c7cc9-516">人力资源</span><span class="sxs-lookup"><span data-stu-id="c7cc9-516">Human Resources</span></span>          | <span data-ttu-id="c7cc9-517">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c7cc9-517">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="c7cc9-518">国家/地区</span><span class="sxs-lookup"><span data-stu-id="c7cc9-518">Country/Region</span></span>  | <span data-ttu-id="c7cc9-519">国家/地区代码</span><span class="sxs-lookup"><span data-stu-id="c7cc9-519">Country Code</span></span>          |
| <span data-ttu-id="c7cc9-520">邮政编码 </span><span class="sxs-lookup"><span data-stu-id="c7cc9-520">Zip/Postal Code</span></span> | <span data-ttu-id="c7cc9-521">邮政编码</span><span class="sxs-lookup"><span data-stu-id="c7cc9-521">Postal Code</span></span>           |
| <span data-ttu-id="c7cc9-522">状态</span><span class="sxs-lookup"><span data-stu-id="c7cc9-522">State</span></span>           | <span data-ttu-id="c7cc9-523">省/直辖市/自治区代码</span><span class="sxs-lookup"><span data-stu-id="c7cc9-523">State Code</span></span>            |
| <span data-ttu-id="c7cc9-524">城市</span><span class="sxs-lookup"><span data-stu-id="c7cc9-524">City</span></span>            | <span data-ttu-id="c7cc9-525">城市</span><span class="sxs-lookup"><span data-stu-id="c7cc9-525">City</span></span>                  |
| <span data-ttu-id="c7cc9-526">县</span><span class="sxs-lookup"><span data-stu-id="c7cc9-526">County</span></span>          | <span data-ttu-id="c7cc9-527">县（自治市）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-527">County (Municipality)</span></span> |
| <span data-ttu-id="c7cc9-528">街道</span><span class="sxs-lookup"><span data-stu-id="c7cc9-528">Street</span></span>          | <span data-ttu-id="c7cc9-529">地址行 1</span><span class="sxs-lookup"><span data-stu-id="c7cc9-529">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="c7cc9-530">税区</span><span class="sxs-lookup"><span data-stu-id="c7cc9-530">Tax regions</span></span>

<span data-ttu-id="c7cc9-531">税区用于确定应在生成工资单期间应用的适当税费。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-531">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="c7cc9-532">税区作为位置地址映射到 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-532">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="c7cc9-533">默认税区必须与工作人员的活动职位关联。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-533">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="c7cc9-534">税区（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-534">Tax region (required)</span></span>
- <span data-ttu-id="c7cc9-535">国家/地区（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-535">Country/Region (required)</span></span>
- <span data-ttu-id="c7cc9-536">省/直辖市/自治区（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-536">State (required)</span></span>
- <span data-ttu-id="c7cc9-537">县</span><span class="sxs-lookup"><span data-stu-id="c7cc9-537">County</span></span> 
- <span data-ttu-id="c7cc9-538"> 市/县（必填）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-538">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="c7cc9-539">在墨西哥配置数据以生成工资单</span><span class="sxs-lookup"><span data-stu-id="c7cc9-539">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="c7cc9-540">如果要在墨西哥为员工生成付薪，必须配置以下元素：</span><span class="sxs-lookup"><span data-stu-id="c7cc9-540">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="c7cc9-541">需要职位的部门。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-541">Departments are required on positions.</span></span>
- <span data-ttu-id="c7cc9-542">必须将成本中心设置为财务维度，并且成本中心必须为默认财务维度字符串的第一个元素。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-542">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="c7cc9-543">工作类型</span><span class="sxs-lookup"><span data-stu-id="c7cc9-543">Job types</span></span>

<span data-ttu-id="c7cc9-544">工作类型用于将类似的工作分组为类别。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-544">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="c7cc9-545">在墨西哥需要工作类型才能处理工资单。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-545">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="c7cc9-546">例如，工作类型包括全职和兼职，或按工资付薪和按小时付薪。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-546">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="c7cc9-547">作业类型作为付薪类型映射到 Dayforce，用于指示员工按小时还是按工资付薪。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-547">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="c7cc9-548">需要以下作业类型和描述。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-548">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="c7cc9-549">工作类型</span><span class="sxs-lookup"><span data-stu-id="c7cc9-549">Job type</span></span>   | <span data-ttu-id="c7cc9-550">说明</span><span class="sxs-lookup"><span data-stu-id="c7cc9-550">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="c7cc9-551">每小时</span><span class="sxs-lookup"><span data-stu-id="c7cc9-551">Hourly</span></span>     | <span data-ttu-id="c7cc9-552">墨西哥按小时</span><span class="sxs-lookup"><span data-stu-id="c7cc9-552">MX Hourly</span></span>   |
| <span data-ttu-id="c7cc9-553">按工资</span><span class="sxs-lookup"><span data-stu-id="c7cc9-553">Salaried</span></span>   | <span data-ttu-id="c7cc9-554">墨西哥按工资</span><span class="sxs-lookup"><span data-stu-id="c7cc9-554">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="c7cc9-555">职位类型</span><span class="sxs-lookup"><span data-stu-id="c7cc9-555">Position types</span></span> 

<span data-ttu-id="c7cc9-556">可使用职位类型描述职位是全职、兼职还是其他。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-556">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="c7cc9-557">职位类型作为付薪类别映射到 Dayforce，用于指示员工是全职还是兼职。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-557">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="c7cc9-558">需要以下职位类型和描述。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-558">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="c7cc9-559">职位类型</span><span class="sxs-lookup"><span data-stu-id="c7cc9-559">Position type</span></span>   | <span data-ttu-id="c7cc9-560">说明</span><span class="sxs-lookup"><span data-stu-id="c7cc9-560">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="c7cc9-561">全职</span><span class="sxs-lookup"><span data-stu-id="c7cc9-561">Full-time</span></span>       | <span data-ttu-id="c7cc9-562">全职员工</span><span class="sxs-lookup"><span data-stu-id="c7cc9-562">Full time employee</span></span> |
| <span data-ttu-id="c7cc9-563">兼职</span><span class="sxs-lookup"><span data-stu-id="c7cc9-563">Part-time</span></span>       | <span data-ttu-id="c7cc9-564">兼职员工</span><span class="sxs-lookup"><span data-stu-id="c7cc9-564">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="c7cc9-565">原因代码</span><span class="sxs-lookup"><span data-stu-id="c7cc9-565">Reason codes</span></span>

<span data-ttu-id="c7cc9-566">原因代码提供有关员工状态的信息。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-566">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="c7cc9-567">原因代码作为状态代码映射到 Dayforce，用于指示更改员工的职位或雇用状态的原因。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-567">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="c7cc9-568">需要以下原因代码和描述。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-568">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="c7cc9-569">原因代码</span><span class="sxs-lookup"><span data-stu-id="c7cc9-569">Reason code</span></span>            | <span data-ttu-id="c7cc9-570">说明</span><span class="sxs-lookup"><span data-stu-id="c7cc9-570">Description</span></span>                    | <span data-ttu-id="c7cc9-571">适用的场景</span><span class="sxs-lookup"><span data-stu-id="c7cc9-571">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="c7cc9-572">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="c7cc9-572">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="c7cc9-573">首次付薪前离职</span><span class="sxs-lookup"><span data-stu-id="c7cc9-573">Departure before first payroll</span></span> | <span data-ttu-id="c7cc9-574">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="c7cc9-574">Terminate worker</span></span>     |
| <span data-ttu-id="c7cc9-575">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="c7cc9-575">RESIGNATION</span></span>            | <span data-ttu-id="c7cc9-576">辞职</span><span class="sxs-lookup"><span data-stu-id="c7cc9-576">Resignation</span></span>                    | <span data-ttu-id="c7cc9-577">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="c7cc9-577">Terminate worker</span></span>     |
| <span data-ttu-id="c7cc9-578">PENSION</span><span class="sxs-lookup"><span data-stu-id="c7cc9-578">PENSION</span></span>                | <span data-ttu-id="c7cc9-579">退休金</span><span class="sxs-lookup"><span data-stu-id="c7cc9-579">Pension</span></span>                        | <span data-ttu-id="c7cc9-580">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="c7cc9-580">Terminate worker</span></span>     |
| <span data-ttu-id="c7cc9-581">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="c7cc9-581">TERMINATION</span></span>            | <span data-ttu-id="c7cc9-582">终止</span><span class="sxs-lookup"><span data-stu-id="c7cc9-582">Termination</span></span>                    | <span data-ttu-id="c7cc9-583">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="c7cc9-583">Terminate worker</span></span>     |
| <span data-ttu-id="c7cc9-584">退休</span><span class="sxs-lookup"><span data-stu-id="c7cc9-584">RETIREMENT</span></span>             | <span data-ttu-id="c7cc9-585">退休</span><span class="sxs-lookup"><span data-stu-id="c7cc9-585">Retirement</span></span>                     | <span data-ttu-id="c7cc9-586">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="c7cc9-586">Terminate worker</span></span>     |
| <span data-ttu-id="c7cc9-587">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="c7cc9-587">ABSENTEE</span></span>               | <span data-ttu-id="c7cc9-588">缺勤者</span><span class="sxs-lookup"><span data-stu-id="c7cc9-588">Absentee</span></span>                       | <span data-ttu-id="c7cc9-589">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="c7cc9-589">Terminate worker</span></span>     |
| <span data-ttu-id="c7cc9-590">OTHER</span><span class="sxs-lookup"><span data-stu-id="c7cc9-590">OTHER</span></span>                  | <span data-ttu-id="c7cc9-591">其他原因</span><span class="sxs-lookup"><span data-stu-id="c7cc9-591">Other Reasons</span></span>                  | <span data-ttu-id="c7cc9-592">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="c7cc9-592">Terminate worker</span></span>     |
| <span data-ttu-id="c7cc9-593">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="c7cc9-593">CLOSURE</span></span>                | <span data-ttu-id="c7cc9-594">停业</span><span class="sxs-lookup"><span data-stu-id="c7cc9-594">Business Closure</span></span>               | <span data-ttu-id="c7cc9-595">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="c7cc9-595">Terminate worker</span></span>     |
| <span data-ttu-id="c7cc9-596">DEATH</span><span class="sxs-lookup"><span data-stu-id="c7cc9-596">DEATH</span></span>                  | <span data-ttu-id="c7cc9-597">死亡</span><span class="sxs-lookup"><span data-stu-id="c7cc9-597">Death</span></span>                          | <span data-ttu-id="c7cc9-598">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="c7cc9-598">Terminate worker</span></span>     |
| <span data-ttu-id="c7cc9-599">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="c7cc9-599">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="c7cc9-600">休假</span><span class="sxs-lookup"><span data-stu-id="c7cc9-600">Leave of Absence</span></span>               | <span data-ttu-id="c7cc9-601">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="c7cc9-601">Terminate worker</span></span>     |
| <span data-ttu-id="c7cc9-602">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="c7cc9-602">CONTRACTEND</span></span>            | <span data-ttu-id="c7cc9-603">合同结束</span><span class="sxs-lookup"><span data-stu-id="c7cc9-603">End of Contract</span></span>                | <span data-ttu-id="c7cc9-604">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="c7cc9-604">Terminate worker</span></span>     |
| <span data-ttu-id="c7cc9-605">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="c7cc9-605">SALARYCHANGE</span></span>           | <span data-ttu-id="c7cc9-606">工资改变</span><span class="sxs-lookup"><span data-stu-id="c7cc9-606">Change of Salary</span></span>               | <span data-ttu-id="c7cc9-607">薪酬</span><span class="sxs-lookup"><span data-stu-id="c7cc9-607">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="c7cc9-608">雇用条款</span><span class="sxs-lookup"><span data-stu-id="c7cc9-608">Terms of employment</span></span>

<span data-ttu-id="c7cc9-609">雇用条款用于创建雇用条款的类别。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-609">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="c7cc9-610">这些条款作为雇用指标值映射到 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-610">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="c7cc9-611">需要以下雇用条款和描述。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-611">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="c7cc9-612">雇用条款</span><span class="sxs-lookup"><span data-stu-id="c7cc9-612">Terms of employment</span></span>   | <span data-ttu-id="c7cc9-613">说明</span><span class="sxs-lookup"><span data-stu-id="c7cc9-613">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="c7cc9-614">常规</span><span class="sxs-lookup"><span data-stu-id="c7cc9-614">Regular</span></span>               | <span data-ttu-id="c7cc9-615">常规</span><span class="sxs-lookup"><span data-stu-id="c7cc9-615">Regular</span></span>     |
| <span data-ttu-id="c7cc9-616">直接</span><span class="sxs-lookup"><span data-stu-id="c7cc9-616">Direct</span></span>                | <span data-ttu-id="c7cc9-617">直接</span><span class="sxs-lookup"><span data-stu-id="c7cc9-617">Direct</span></span>      |
| <span data-ttu-id="c7cc9-618">实习</span><span class="sxs-lookup"><span data-stu-id="c7cc9-618">Internship</span></span>            | <span data-ttu-id="c7cc9-619">实习</span><span class="sxs-lookup"><span data-stu-id="c7cc9-619">Internship</span></span>  |
| <span data-ttu-id="c7cc9-620">永久</span><span class="sxs-lookup"><span data-stu-id="c7cc9-620">Permanent</span></span>             | <span data-ttu-id="c7cc9-621">永久</span><span class="sxs-lookup"><span data-stu-id="c7cc9-621">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="c7cc9-622">婚姻状况</span><span class="sxs-lookup"><span data-stu-id="c7cc9-622">Marital status</span></span>

<span data-ttu-id="c7cc9-623">婚姻状态值映射到 Dayforce，并在集成时根据需要转换为接受的值。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-623">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="c7cc9-624">下表显示婚姻状态值如何映射到 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-624">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="c7cc9-625">人力资源</span><span class="sxs-lookup"><span data-stu-id="c7cc9-625">Human Resources</span></span>                 | <span data-ttu-id="c7cc9-626">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c7cc9-626">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="c7cc9-627">已婚</span><span class="sxs-lookup"><span data-stu-id="c7cc9-627">Married</span></span>                | <span data-ttu-id="c7cc9-628">已婚</span><span class="sxs-lookup"><span data-stu-id="c7cc9-628">Married</span></span>                   |
| <span data-ttu-id="c7cc9-629">单一</span><span class="sxs-lookup"><span data-stu-id="c7cc9-629">Single</span></span>                 | <span data-ttu-id="c7cc9-630">单一</span><span class="sxs-lookup"><span data-stu-id="c7cc9-630">Single</span></span>                    |
| <span data-ttu-id="c7cc9-631">丧偶</span><span class="sxs-lookup"><span data-stu-id="c7cc9-631">Widowed</span></span>                | <span data-ttu-id="c7cc9-632">丧偶</span><span class="sxs-lookup"><span data-stu-id="c7cc9-632">Widowed</span></span>                   |
| <span data-ttu-id="c7cc9-633">离婚</span><span class="sxs-lookup"><span data-stu-id="c7cc9-633">Divorced</span></span>               | <span data-ttu-id="c7cc9-634">离异</span><span class="sxs-lookup"><span data-stu-id="c7cc9-634">Divorced</span></span>                  |
| <span data-ttu-id="c7cc9-635">注册伴侣关系</span><span class="sxs-lookup"><span data-stu-id="c7cc9-635">Registered Partnership</span></span> | <span data-ttu-id="c7cc9-636">民事结合关系</span><span class="sxs-lookup"><span data-stu-id="c7cc9-636">Domestic Partnership</span></span>      |
| <span data-ttu-id="c7cc9-637">None</span><span class="sxs-lookup"><span data-stu-id="c7cc9-637">None</span></span>                   | <span data-ttu-id="c7cc9-638">*墨西哥不支持*</span><span class="sxs-lookup"><span data-stu-id="c7cc9-638">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="c7cc9-639">未婚同居</span><span class="sxs-lookup"><span data-stu-id="c7cc9-639">Cohabiting</span></span>             | <span data-ttu-id="c7cc9-640">*墨西哥不支持*</span><span class="sxs-lookup"><span data-stu-id="c7cc9-640">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="c7cc9-641">性</span><span class="sxs-lookup"><span data-stu-id="c7cc9-641">Gender</span></span>

<span data-ttu-id="c7cc9-642">性别指派映射到 Dayforce，并在集成时根据需要转换为接受的值。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-642">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="c7cc9-643">下表显示性别指派如何映射到 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-643">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="c7cc9-644">人力资源</span><span class="sxs-lookup"><span data-stu-id="c7cc9-644">Human Resources</span></span>       | <span data-ttu-id="c7cc9-645">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c7cc9-645">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="c7cc9-646">男</span><span class="sxs-lookup"><span data-stu-id="c7cc9-646">Male</span></span>         | <span data-ttu-id="c7cc9-647">男</span><span class="sxs-lookup"><span data-stu-id="c7cc9-647">Male</span></span>                      |
| <span data-ttu-id="c7cc9-648">女</span><span class="sxs-lookup"><span data-stu-id="c7cc9-648">Female</span></span>       | <span data-ttu-id="c7cc9-649">女</span><span class="sxs-lookup"><span data-stu-id="c7cc9-649">Female</span></span>                    |
| <span data-ttu-id="c7cc9-650">非特定</span><span class="sxs-lookup"><span data-stu-id="c7cc9-650">Non-specific</span></span> | <span data-ttu-id="c7cc9-651">*墨西哥不支持*</span><span class="sxs-lookup"><span data-stu-id="c7cc9-651">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="c7cc9-652">付款方式</span><span class="sxs-lookup"><span data-stu-id="c7cc9-652">Payment method</span></span>

<span data-ttu-id="c7cc9-653">付款方式为员工和公司提供描述如何向员工付款的方式。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-653">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="c7cc9-654">付款方式映射到 Dayforce，并在集成时根据需要转换为接受的值。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-654">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="c7cc9-655">下表显示付款方式如何映射到 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-655">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="c7cc9-656">人力资源</span><span class="sxs-lookup"><span data-stu-id="c7cc9-656">Human Resources</span></span>             | <span data-ttu-id="c7cc9-657">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c7cc9-657">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="c7cc9-658">现金</span><span class="sxs-lookup"><span data-stu-id="c7cc9-658">Cash</span></span>               | <span data-ttu-id="c7cc9-659">现金</span><span class="sxs-lookup"><span data-stu-id="c7cc9-659">Cash</span></span>                      |
| <span data-ttu-id="c7cc9-660">电子支付</span><span class="sxs-lookup"><span data-stu-id="c7cc9-660">Electronic Payment</span></span> | <span data-ttu-id="c7cc9-661">转账</span><span class="sxs-lookup"><span data-stu-id="c7cc9-661">Transfer</span></span>                  |
| <span data-ttu-id="c7cc9-662">检查</span><span class="sxs-lookup"><span data-stu-id="c7cc9-662">Check</span></span>              | <span data-ttu-id="c7cc9-663">支票</span><span class="sxs-lookup"><span data-stu-id="c7cc9-663">Cheque</span></span>                    |
| <span data-ttu-id="c7cc9-664">银行汇票</span><span class="sxs-lookup"><span data-stu-id="c7cc9-664">Bank Draft</span></span>         | <span data-ttu-id="c7cc9-665">*墨西哥不支持*</span><span class="sxs-lookup"><span data-stu-id="c7cc9-665">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="c7cc9-666">其他</span><span class="sxs-lookup"><span data-stu-id="c7cc9-666">Other</span></span>              | <span data-ttu-id="c7cc9-667">*墨西哥不支持*</span><span class="sxs-lookup"><span data-stu-id="c7cc9-667">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="c7cc9-668">银行帐户类型</span><span class="sxs-lookup"><span data-stu-id="c7cc9-668">Bank account type</span></span>

<span data-ttu-id="c7cc9-669">银行帐户类型用于对员工进行电子付款。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-669">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="c7cc9-670">银行账户类型作为转帐信息映射到 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-670">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="c7cc9-671">集成时，银行帐户类型根据需要转换为接受的值。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-671">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="c7cc9-672">人力资源</span><span class="sxs-lookup"><span data-stu-id="c7cc9-672">Human Resources</span></span>            | <span data-ttu-id="c7cc9-673">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c7cc9-673">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="c7cc9-674">支票帐户</span><span class="sxs-lookup"><span data-stu-id="c7cc9-674">Checking Account</span></span>  | <span data-ttu-id="c7cc9-675">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="c7cc9-675">CheckingAccount</span></span>           |
| <span data-ttu-id="c7cc9-676">工资单帐户</span><span class="sxs-lookup"><span data-stu-id="c7cc9-676">Payroll Account</span></span>   | <span data-ttu-id="c7cc9-677">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="c7cc9-677">PayrollAccount</span></span>            |
| <span data-ttu-id="c7cc9-678">储蓄帐户</span><span class="sxs-lookup"><span data-stu-id="c7cc9-678">Savings Account</span></span>   | <span data-ttu-id="c7cc9-679">*墨西哥不支持*</span><span class="sxs-lookup"><span data-stu-id="c7cc9-679">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="c7cc9-680">BankGirot 帐户</span><span class="sxs-lookup"><span data-stu-id="c7cc9-680">BankGirot account</span></span> | <span data-ttu-id="c7cc9-681">*墨西哥不支持*</span><span class="sxs-lookup"><span data-stu-id="c7cc9-681">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="c7cc9-682">PlusGirot 帐户</span><span class="sxs-lookup"><span data-stu-id="c7cc9-682">PlusGirot account</span></span> | <span data-ttu-id="c7cc9-683">*墨西哥不支持*</span><span class="sxs-lookup"><span data-stu-id="c7cc9-683">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="c7cc9-684">收入代码</span><span class="sxs-lookup"><span data-stu-id="c7cc9-684">Earning codes</span></span>

<span data-ttu-id="c7cc9-685">收入代码唯一标识工作人员获得的每种收入类型。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-685">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="c7cc9-686">这些代码有多个与收入有关的参数，如会计规则、税法、报告要求和补偿费功能。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-686">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="c7cc9-687">如果使用不受支持的频率，默认将使用**每个付薪**频率进行计算。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-687">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="c7cc9-688">支持的频率</span><span class="sxs-lookup"><span data-stu-id="c7cc9-688">Supported frequencies</span></span>

- <span data-ttu-id="c7cc9-689">所有</span><span class="sxs-lookup"><span data-stu-id="c7cc9-689">All</span></span>
- <span data-ttu-id="c7cc9-690">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="c7cc9-690">EVERYPAY</span></span>
- <span data-ttu-id="c7cc9-691">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="c7cc9-691">EACHPAYPERIOD</span></span>
- <span data-ttu-id="c7cc9-692">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="c7cc9-692">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="c7cc9-693">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="c7cc9-693">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="c7cc9-694">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7cc9-694">1OFMTH</span></span>
- <span data-ttu-id="c7cc9-695">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="c7cc9-695">LASTOFMTH</span></span>
- <span data-ttu-id="c7cc9-696">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7cc9-696">2OFMTH</span></span>
- <span data-ttu-id="c7cc9-697">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7cc9-697">3OFMTH</span></span>
- <span data-ttu-id="c7cc9-698">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7cc9-698">4OFMTH</span></span>
- <span data-ttu-id="c7cc9-699">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7cc9-699">5OFMTH</span></span>
- <span data-ttu-id="c7cc9-700">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7cc9-700">1N2OFMTH</span></span>
- <span data-ttu-id="c7cc9-701">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7cc9-701">3N4OFMTH</span></span>
- <span data-ttu-id="c7cc9-702">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7cc9-702">1N3OFMTH</span></span>
- <span data-ttu-id="c7cc9-703">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7cc9-703">1N4OFMTH</span></span>
- <span data-ttu-id="c7cc9-704">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7cc9-704">2N3OFMTH</span></span>
- <span data-ttu-id="c7cc9-705">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7cc9-705">2N4OFMTH</span></span>
- <span data-ttu-id="c7cc9-706">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7cc9-706">1N2N3OFMTH</span></span>
- <span data-ttu-id="c7cc9-707">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7cc9-707">1N2N4OFMTH</span></span>
- <span data-ttu-id="c7cc9-708">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7cc9-708">1N3N4OFMTH</span></span>
- <span data-ttu-id="c7cc9-709">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7cc9-709">2N3N4OFMTH</span></span>
- <span data-ttu-id="c7cc9-710">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7cc9-710">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="c7cc9-711">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="c7cc9-711">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="c7cc9-712">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="c7cc9-712">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="c7cc9-713">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="c7cc9-713">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="c7cc9-714">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="c7cc9-714">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="c7cc9-715">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="c7cc9-715">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="c7cc9-716">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="c7cc9-716">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="c7cc9-717">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="c7cc9-717">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="c7cc9-718">地址</span><span class="sxs-lookup"><span data-stu-id="c7cc9-718">Addresses</span></span>

<span data-ttu-id="c7cc9-719">特定国家或地区、省/直辖市/自治区和县/市（自治市）代码的标识需要 Dayforce 和国内/地区内提供商可识别的特定格式。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-719">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="c7cc9-720">尽管县/市的格式可变，但是每个县/市必须与一个省/直辖市/自治区关联。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-720">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="c7cc9-721">人力资源</span><span class="sxs-lookup"><span data-stu-id="c7cc9-721">Human Resources</span></span>              | <span data-ttu-id="c7cc9-722">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c7cc9-722">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="c7cc9-723">国家/地区</span><span class="sxs-lookup"><span data-stu-id="c7cc9-723">Country/Region</span></span>      | <span data-ttu-id="c7cc9-724">国家/地区代码</span><span class="sxs-lookup"><span data-stu-id="c7cc9-724">Country Code</span></span>          |
| <span data-ttu-id="c7cc9-725">邮政编码 </span><span class="sxs-lookup"><span data-stu-id="c7cc9-725">Zip/Postal Code</span></span>     | <span data-ttu-id="c7cc9-726">邮政编码</span><span class="sxs-lookup"><span data-stu-id="c7cc9-726">Postal Code</span></span>           |
| <span data-ttu-id="c7cc9-727">状态</span><span class="sxs-lookup"><span data-stu-id="c7cc9-727">State</span></span>               | <span data-ttu-id="c7cc9-728">省/直辖市/自治区代码</span><span class="sxs-lookup"><span data-stu-id="c7cc9-728">State Code</span></span>            |
| <span data-ttu-id="c7cc9-729">城市</span><span class="sxs-lookup"><span data-stu-id="c7cc9-729">City</span></span>                | <span data-ttu-id="c7cc9-730">城市</span><span class="sxs-lookup"><span data-stu-id="c7cc9-730">City</span></span>                  |
| <span data-ttu-id="c7cc9-731">县</span><span class="sxs-lookup"><span data-stu-id="c7cc9-731">County</span></span>              | <span data-ttu-id="c7cc9-732">县（自治市）</span><span class="sxs-lookup"><span data-stu-id="c7cc9-732">County (Municipality)</span></span> |
| <span data-ttu-id="c7cc9-733">街道</span><span class="sxs-lookup"><span data-stu-id="c7cc9-733">Street</span></span>              | <span data-ttu-id="c7cc9-734">地址行 1</span><span class="sxs-lookup"><span data-stu-id="c7cc9-734">Address Line 1</span></span>        |
| <span data-ttu-id="c7cc9-735">街道编号</span><span class="sxs-lookup"><span data-stu-id="c7cc9-735">Street Number</span></span>       | <span data-ttu-id="c7cc9-736">地址行 2</span><span class="sxs-lookup"><span data-stu-id="c7cc9-736">Address Line 2</span></span>        |
| <span data-ttu-id="c7cc9-737">建筑物地址</span><span class="sxs-lookup"><span data-stu-id="c7cc9-737">Building Complement</span></span> | <span data-ttu-id="c7cc9-738">地址行 5</span><span class="sxs-lookup"><span data-stu-id="c7cc9-738">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="c7cc9-739">护照号</span><span class="sxs-lookup"><span data-stu-id="c7cc9-739">Passport number</span></span>

<span data-ttu-id="c7cc9-740">员工可以声明护照信息。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-740">Employees can declare passport information.</span></span> <span data-ttu-id="c7cc9-741">此信息的身份证明类型为**护照**，并作为员工的墨西哥特定信息的一部分集成到 Dayforce 中。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-741">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="c7cc9-742">身份证明类型 =“护照”</span><span class="sxs-lookup"><span data-stu-id="c7cc9-742">Identification Type = "Passport"</span></span>
- <span data-ttu-id="c7cc9-743">签发日期</span><span class="sxs-lookup"><span data-stu-id="c7cc9-743">Issued Date</span></span>
- <span data-ttu-id="c7cc9-744">到期日期</span><span class="sxs-lookup"><span data-stu-id="c7cc9-744">Expiration Date</span></span>

<span data-ttu-id="c7cc9-745">员工可以声明**护照**身份证明类型的多个身份证明编号。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-745">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="c7cc9-746">但是，仅将当前有效的护照条目集成到 Dayforce 中。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-746">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="c7cc9-747">如果所有护照条目均已过期，将把最近签发的护照集成到 Dayforce 中。</span><span class="sxs-lookup"><span data-stu-id="c7cc9-747">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>


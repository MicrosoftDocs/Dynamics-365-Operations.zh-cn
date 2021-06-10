---
title: 配置与 Dayforce 的集成
description: Microsoft Dynamics 365 Human Resources 与 Ceridian Dayforce 之间的集成依赖于本文中介绍的几个配置步骤。 必须先在 Human Resources 和 Dayforce 中配置集成，才能处理付薪。
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PersonnelIntegrationConfiguration
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d150daa92fe79cf6620ce5ddf1a01f369c64053
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051489"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="88f7c-104">配置与 Dayforce 的集成</span><span class="sxs-lookup"><span data-stu-id="88f7c-104">Configure integration with Dayforce</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="88f7c-105">Microsoft Dynamics 365 Human Resources 与 Ceridian Dayforce 之间的集成依赖于本文中介绍的几个配置步骤。</span><span class="sxs-lookup"><span data-stu-id="88f7c-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="88f7c-106">必须先在 Human Resources 和 Dayforce 中配置集成，才能处理付薪。</span><span class="sxs-lookup"><span data-stu-id="88f7c-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="88f7c-107">使用 Dayforce 之类的服务完成付薪时，必须在 Human Resources 中启用集成。</span><span class="sxs-lookup"><span data-stu-id="88f7c-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="88f7c-108">此集成需要来自 Human Resources 的特定数据。</span><span class="sxs-lookup"><span data-stu-id="88f7c-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="88f7c-109">因此，必须验证已按照支持集成的方式在 Human Resources 中配置了映射到 Dayforce 的数据。</span><span class="sxs-lookup"><span data-stu-id="88f7c-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="88f7c-110">此集成使用下面的各种数据类别：</span><span class="sxs-lookup"><span data-stu-id="88f7c-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="88f7c-111">人力资源数据</span><span class="sxs-lookup"><span data-stu-id="88f7c-111">Human resources data</span></span>
- <span data-ttu-id="88f7c-112">薪酬数据</span><span class="sxs-lookup"><span data-stu-id="88f7c-112">Compensation data</span></span>
- <span data-ttu-id="88f7c-113">工资单数据，如付薪周期、付薪期间和收入代码</span><span class="sxs-lookup"><span data-stu-id="88f7c-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="88f7c-114">工作人员数据</span><span class="sxs-lookup"><span data-stu-id="88f7c-114">Worker data</span></span>

<span data-ttu-id="88f7c-115">本文介绍要启用集成必须执行的步骤。</span><span class="sxs-lookup"><span data-stu-id="88f7c-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="88f7c-116">还介绍了集成所需的数据类型和配置详细信息。</span><span class="sxs-lookup"><span data-stu-id="88f7c-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="88f7c-117">启用集成</span><span class="sxs-lookup"><span data-stu-id="88f7c-117">Enable the integration</span></span>

<span data-ttu-id="88f7c-118">在 Human Resources 中，必须开启集成并输入配置信息，才能连接到 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="88f7c-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="88f7c-119">如果要将生成的总帐交易记录导入 Microsoft Dynamics 365 Finance 中，还必须在 Finance 中设置 Microsoft Azure 存储帐户和输入 Azure Storage 连接字符串。</span><span class="sxs-lookup"><span data-stu-id="88f7c-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="88f7c-120">要在 Human Resources 中开启集成，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="88f7c-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="88f7c-121">在 **系统管理** 页中，选择 **集成配置**。</span><span class="sxs-lookup"><span data-stu-id="88f7c-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="88f7c-122">输入安全文件传输协议 (FTP) 终结点和安全 FTP 文件夹路径。</span><span class="sxs-lookup"><span data-stu-id="88f7c-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="88f7c-123">输入将访问安全 FTP 终结点和文件夹路径的用户的用户名和密码。</span><span class="sxs-lookup"><span data-stu-id="88f7c-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="88f7c-124">根据需要测试连接，然后将 **启用工资单集成** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="88f7c-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="88f7c-125">开启集成后，将创建数据导出包和文件，并设置频率。</span><span class="sxs-lookup"><span data-stu-id="88f7c-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="88f7c-126">可根据需要更改此频率。</span><span class="sxs-lookup"><span data-stu-id="88f7c-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="88f7c-127">有关 Azure ML 存储帐户和 Azure 存储连接字符串的详细信息，请参阅以下 Azure ML 文章：</span><span class="sxs-lookup"><span data-stu-id="88f7c-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="88f7c-128">关于 Azure 存储帐户</span><span class="sxs-lookup"><span data-stu-id="88f7c-128">About Azure storage accounts</span></span>](/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="88f7c-129">配置 Azure 存储连接字符串</span><span class="sxs-lookup"><span data-stu-id="88f7c-129">Configure Azure Storage connection strings</span></span>](/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="88f7c-130">启用工资单集成后的技术详细信息</span><span class="sxs-lookup"><span data-stu-id="88f7c-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="88f7c-131">开启工资单集成有两大效果：</span><span class="sxs-lookup"><span data-stu-id="88f7c-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="88f7c-132">创建一个名称为“工资单集成导出”的数据导出项目。</span><span class="sxs-lookup"><span data-stu-id="88f7c-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="88f7c-133">此项目中包含工资单集成需要的实体和字段。</span><span class="sxs-lookup"><span data-stu-id="88f7c-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="88f7c-134">若要检查此项目，请转到 **系统管理**，选择 **数据管理** 磁贴，然后从项目列表打开数据项目。</span><span class="sxs-lookup"><span data-stu-id="88f7c-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="88f7c-135">此批处理作业执行数据导出项目，加密生成的数据包，然后将数据包文件传输到 **集成配置** 屏幕上配置的 SFTP 终结点。</span><span class="sxs-lookup"><span data-stu-id="88f7c-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="88f7c-136">将使用数据包的唯一密钥加密传输到 SFTP 终结点的数据包。</span><span class="sxs-lookup"><span data-stu-id="88f7c-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="88f7c-137">此密钥位于只有 Ceridian 才能访问的 Azure 密钥保管库。</span><span class="sxs-lookup"><span data-stu-id="88f7c-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="88f7c-138">不能解密和检查数据包内容。</span><span class="sxs-lookup"><span data-stu-id="88f7c-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="88f7c-139">如果需要检查数据包的内容，需要手动导出“工资单集成导出”数据终结点，下载，然后打开。</span><span class="sxs-lookup"><span data-stu-id="88f7c-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="88f7c-140">手动导出不会应用加密或传输包。</span><span class="sxs-lookup"><span data-stu-id="88f7c-140">Manual export will not apply encryption or transfer the package.</span></span>
> <span data-ttu-id="88f7c-141">对于将集成文件从 Dynamics 365 Human Resources UAT 或沙盒环境发送到 Ceridian Dayforce 测试环境的实例，您可以使用以下密钥保管库 URL：https://payrollintegrationprod.vault.azure.net。</span><span class="sxs-lookup"><span data-stu-id="88f7c-141">For instances where the integration files are sent from a Dynamics 365 Human Resources UAT or Sandbox environment to a Ceridian Dayforce Test environment, you can use the following key vault URL: https://payrollintegrationprod.vault.azure.net.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="88f7c-142">配置数据</span><span class="sxs-lookup"><span data-stu-id="88f7c-142">Configure your data</span></span> 

<span data-ttu-id="88f7c-143">要处理工资单，必须在 Human Resources 中配置人力资源数据。</span><span class="sxs-lookup"><span data-stu-id="88f7c-143">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="88f7c-144">必须设置组织数据（如工作和职位），以及福利和薪酬信息。</span><span class="sxs-lookup"><span data-stu-id="88f7c-144">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="88f7c-145">这些信息提供生成员工付薪所需雇用、付薪和扣缴信息。</span><span class="sxs-lookup"><span data-stu-id="88f7c-145">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="88f7c-146">人力资源数据</span><span class="sxs-lookup"><span data-stu-id="88f7c-146">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="88f7c-147">福利</span><span class="sxs-lookup"><span data-stu-id="88f7c-147">Benefits</span></span> 

<span data-ttu-id="88f7c-148">人力资源提供工具，用于设置和维护组织提供或为其工作人员处理的福利、扣缴和工作人员薪酬计划。</span><span class="sxs-lookup"><span data-stu-id="88f7c-148">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="88f7c-149">创建福利时，请注意 Dayforce 中使用的以下数据和配置。</span><span class="sxs-lookup"><span data-stu-id="88f7c-149">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="88f7c-150">福利计划</span><span class="sxs-lookup"><span data-stu-id="88f7c-150">Benefit plans</span></span>

- <span data-ttu-id="88f7c-151">计划（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-151">Plan (required)</span></span>
- <span data-ttu-id="88f7c-152">类型（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-152">Type (required)</span></span>
- <span data-ttu-id="88f7c-153">工资单影响（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-153">Payroll impact (required)</span></span>
- <span data-ttu-id="88f7c-154">恢复欠款</span><span class="sxs-lookup"><span data-stu-id="88f7c-154">Recover arrears</span></span>
- <span data-ttu-id="88f7c-155">扣除方法</span><span class="sxs-lookup"><span data-stu-id="88f7c-155">Deduction method</span></span>
- <span data-ttu-id="88f7c-156">扣除优先级</span><span class="sxs-lookup"><span data-stu-id="88f7c-156">Deduction priority</span></span>
- <span data-ttu-id="88f7c-157">限制期</span><span class="sxs-lookup"><span data-stu-id="88f7c-157">Limit period</span></span>
- <span data-ttu-id="88f7c-158">限额</span><span class="sxs-lookup"><span data-stu-id="88f7c-158">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="88f7c-159">福利</span><span class="sxs-lookup"><span data-stu-id="88f7c-159">Benefits</span></span>

- <span data-ttu-id="88f7c-160">计划（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-160">Plan (required)</span></span>
- <span data-ttu-id="88f7c-161">类型（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-161">Type (required)</span></span>
- <span data-ttu-id="88f7c-162">选项（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-162">Option (required)</span></span>
- <span data-ttu-id="88f7c-163">福利 ID（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-163">Benefit ID (required)</span></span>
- <span data-ttu-id="88f7c-164">频率</span><span class="sxs-lookup"><span data-stu-id="88f7c-164">Frequency</span></span>
- <span data-ttu-id="88f7c-165">基础</span><span class="sxs-lookup"><span data-stu-id="88f7c-165">Basis</span></span>
- <span data-ttu-id="88f7c-166">金额或费率</span><span class="sxs-lookup"><span data-stu-id="88f7c-166">Amount or rate</span></span>
- <span data-ttu-id="88f7c-167">收入代码</span><span class="sxs-lookup"><span data-stu-id="88f7c-167">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="88f7c-168">支持的频率</span><span class="sxs-lookup"><span data-stu-id="88f7c-168">Supported frequencies</span></span> 

- <span data-ttu-id="88f7c-169">每周</span><span class="sxs-lookup"><span data-stu-id="88f7c-169">Weekly</span></span>
- <span data-ttu-id="88f7c-170">两周一次</span><span class="sxs-lookup"><span data-stu-id="88f7c-170">Bi-weekly</span></span>
- <span data-ttu-id="88f7c-171">每半月</span><span class="sxs-lookup"><span data-stu-id="88f7c-171">Semi-monthly</span></span>
- <span data-ttu-id="88f7c-172">每月</span><span class="sxs-lookup"><span data-stu-id="88f7c-172">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="88f7c-173">支持的库</span><span class="sxs-lookup"><span data-stu-id="88f7c-173">Supported bases</span></span> 

- <span data-ttu-id="88f7c-174">固定金额</span><span class="sxs-lookup"><span data-stu-id="88f7c-174">Fixed amount</span></span>
- <span data-ttu-id="88f7c-175">收入百分比</span><span class="sxs-lookup"><span data-stu-id="88f7c-175">Percent of earnings</span></span>
- <span data-ttu-id="88f7c-176">工作时数</span><span class="sxs-lookup"><span data-stu-id="88f7c-176">Productive hours</span></span>

<span data-ttu-id="88f7c-177">Dayforce 根据福利计划中定义的工资单影响创建以下扣缴。</span><span class="sxs-lookup"><span data-stu-id="88f7c-177">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="88f7c-178">Human Resources 中的选择</span><span class="sxs-lookup"><span data-stu-id="88f7c-178">Selection in Human Resources</span></span>        | <span data-ttu-id="88f7c-179">Dayforce 中的结果</span><span class="sxs-lookup"><span data-stu-id="88f7c-179">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="88f7c-180">否</span><span class="sxs-lookup"><span data-stu-id="88f7c-180">None</span></span>                       | <span data-ttu-id="88f7c-181">不创建扣缴。</span><span class="sxs-lookup"><span data-stu-id="88f7c-181">No deduction is created.</span></span>                      |
| <span data-ttu-id="88f7c-182">仅扣除</span><span class="sxs-lookup"><span data-stu-id="88f7c-182">Deduction only</span></span>             | <span data-ttu-id="88f7c-183">创建员工扣缴。</span><span class="sxs-lookup"><span data-stu-id="88f7c-183">An employee deduction is created.</span></span>             |
| <span data-ttu-id="88f7c-184">仅缴纳</span><span class="sxs-lookup"><span data-stu-id="88f7c-184">Contribution only</span></span>          | <span data-ttu-id="88f7c-185">创建雇主扣缴。</span><span class="sxs-lookup"><span data-stu-id="88f7c-185">An employer deduction is created.</span></span>             |
| <span data-ttu-id="88f7c-186">扣除和缴纳</span><span class="sxs-lookup"><span data-stu-id="88f7c-186">Deduction and contribution</span></span> | <span data-ttu-id="88f7c-187">创建员工扣缴和雇主扣缴。</span><span class="sxs-lookup"><span data-stu-id="88f7c-187">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="88f7c-188">有关如何定义和管理福利计划的详细信息，请参阅以下文章：</span><span class="sxs-lookup"><span data-stu-id="88f7c-188">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="88f7c-189">交付员工福利计划</span><span class="sxs-lookup"><span data-stu-id="88f7c-189">Deliver an employee benefits program</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="88f7c-190">创建新福利</span><span class="sxs-lookup"><span data-stu-id="88f7c-190">Create a new benefit</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="88f7c-191">定义福利资格规则和策略</span><span class="sxs-lookup"><span data-stu-id="88f7c-191">Define benefit eligibility rules and policies</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="88f7c-192">登记和删除工作人员的福利</span><span class="sxs-lookup"><span data-stu-id="88f7c-192">Enroll and remove benefits from workers</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="88f7c-193">薪酬</span><span class="sxs-lookup"><span data-stu-id="88f7c-193">Compensation</span></span> 

<span data-ttu-id="88f7c-194">薪酬管理用于控制基本工资和奖励的发放。</span><span class="sxs-lookup"><span data-stu-id="88f7c-194">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="88f7c-195">员工的固定基本工资和业绩调薪是通过固定薪酬计划控制的。</span><span class="sxs-lookup"><span data-stu-id="88f7c-195">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="88f7c-196">激励性的付款，例如额外津贴、绩效奖、股票期权和赠与以及一次性奖励，是通过可变薪酬计划控制的。</span><span class="sxs-lookup"><span data-stu-id="88f7c-196">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="88f7c-197">Dayforce 使用薪酬信息计算员工的时薪或年薪。</span><span class="sxs-lookup"><span data-stu-id="88f7c-197">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="88f7c-198">需要固定薪酬计划和付薪比率转换。</span><span class="sxs-lookup"><span data-stu-id="88f7c-198">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="88f7c-199">必须将员工与固定薪酬计划关联。</span><span class="sxs-lookup"><span data-stu-id="88f7c-199">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="88f7c-200">有关薪酬计划的详细信息，请参阅以下文章：</span><span class="sxs-lookup"><span data-stu-id="88f7c-200">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="88f7c-201">创建固定薪酬计划</span><span class="sxs-lookup"><span data-stu-id="88f7c-201">Create fixed compensation plans</span></span>](/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="88f7c-202">创建可变薪酬计划</span><span class="sxs-lookup"><span data-stu-id="88f7c-202">Create variable compensation plans</span></span>](/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="88f7c-203">制订薪水/薪酬结构和计划</span><span class="sxs-lookup"><span data-stu-id="88f7c-203">Develop salary/compensation structure and plans</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="88f7c-204">薪酬流程</span><span class="sxs-lookup"><span data-stu-id="88f7c-204">Process compensation</span></span>](/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="88f7c-205">定义薪酬流程并计算结果</span><span class="sxs-lookup"><span data-stu-id="88f7c-205">Define compensation process and calculate results</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="88f7c-206">在固定薪酬计划中登记员工</span><span class="sxs-lookup"><span data-stu-id="88f7c-206">Enroll an employee in a fixed compensation plan</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="88f7c-207">在可变薪酬计划中登记员工</span><span class="sxs-lookup"><span data-stu-id="88f7c-207">Enroll an employee in a variable compensation plan</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="88f7c-208">工作</span><span class="sxs-lookup"><span data-stu-id="88f7c-208">Jobs</span></span> 

<span data-ttu-id="88f7c-209">作业是执行作业的人员需要承担的任务和责任的集合。</span><span class="sxs-lookup"><span data-stu-id="88f7c-209">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="88f7c-210">有关详细信息，请参阅以下文章：</span><span class="sxs-lookup"><span data-stu-id="88f7c-210">For more information, see the following articles:</span></span>

- [<span data-ttu-id="88f7c-211">设置作业组件</span><span class="sxs-lookup"><span data-stu-id="88f7c-211">Setting up the components of a job</span></span>](/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="88f7c-212">定义新工作</span><span class="sxs-lookup"><span data-stu-id="88f7c-212">Define new jobs</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="88f7c-213">职位</span><span class="sxs-lookup"><span data-stu-id="88f7c-213">Positions</span></span>

<span data-ttu-id="88f7c-214">位置是工作的单个实例。</span><span class="sxs-lookup"><span data-stu-id="88f7c-214">A position is an individual instance of a job.</span></span> <span data-ttu-id="88f7c-215">例如，“销售经理（东部）”职位是与“销售经理”工作关联的职位。</span><span class="sxs-lookup"><span data-stu-id="88f7c-215">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="88f7c-216">职位存在于部门中。</span><span class="sxs-lookup"><span data-stu-id="88f7c-216">A position exists in a department.</span></span> <span data-ttu-id="88f7c-217">每个职位只能与一个工作人员关联。</span><span class="sxs-lookup"><span data-stu-id="88f7c-217">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="88f7c-218">设置职位时，请注意以下数据和配置：</span><span class="sxs-lookup"><span data-stu-id="88f7c-218">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="88f7c-219">职位（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-219">Position (required)</span></span>
- <span data-ttu-id="88f7c-220">描述（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-220">Description (required)</span></span>
- <span data-ttu-id="88f7c-221">工作（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-221">Job (required)</span></span>
- <span data-ttu-id="88f7c-222">部门（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-222">Department (required)</span></span>
- <span data-ttu-id="88f7c-223">职位类型（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-223">Position type (required)</span></span>
- <span data-ttu-id="88f7c-224">全职等价</span><span class="sxs-lookup"><span data-stu-id="88f7c-224">Full-time equivalent</span></span>
- <span data-ttu-id="88f7c-225">年度常规时间（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-225">Annual regular hours (required)</span></span>
- <span data-ttu-id="88f7c-226">由法人支付（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-226">Paid by legal entity (required)</span></span>
- <span data-ttu-id="88f7c-227">付薪周期（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-227">Pay cycle (required)</span></span>
- <span data-ttu-id="88f7c-228">默认财务维度 – 成本中心（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-228">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="88f7c-229">工作人员分配 – 工作人员、分配开始时间、分配结束时间、原因代码</span><span class="sxs-lookup"><span data-stu-id="88f7c-229">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="88f7c-230">如果同一个部门中多个职位与同一个工作关联，应在 Dayforce 中将这些职位合并为一个位置。</span><span class="sxs-lookup"><span data-stu-id="88f7c-230">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="88f7c-231">有关详细信息，请参阅以下文章：</span><span class="sxs-lookup"><span data-stu-id="88f7c-231">For more information, see the following articles:</span></span>

- [<span data-ttu-id="88f7c-232">使用部门、工作和职位组织您的劳动力</span><span class="sxs-lookup"><span data-stu-id="88f7c-232">Organize your workforce using departments, jobs, and positions</span></span>](/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="88f7c-233">设置职位</span><span class="sxs-lookup"><span data-stu-id="88f7c-233">Set up positions</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="88f7c-234">部门</span><span class="sxs-lookup"><span data-stu-id="88f7c-234">Departments</span></span>

<span data-ttu-id="88f7c-235">部门是一个运营单位，表示组织的类别或功能区域。</span><span class="sxs-lookup"><span data-stu-id="88f7c-235">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="88f7c-236">部门负责组织的特定区域，例如，销售、会计或人力资源。</span><span class="sxs-lookup"><span data-stu-id="88f7c-236">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="88f7c-237">您可以在功能区中使用要上报的部门。</span><span class="sxs-lookup"><span data-stu-id="88f7c-237">You can use departments to report on functional areas.</span></span> <span data-ttu-id="88f7c-238">部门可能具有损益职责。</span><span class="sxs-lookup"><span data-stu-id="88f7c-238">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="88f7c-239">有关详细信息，请参阅以下文章：</span><span class="sxs-lookup"><span data-stu-id="88f7c-239">For more information, see the following articles:</span></span>

- [<span data-ttu-id="88f7c-240">创建一个部门并将其与部门层次结构关联</span><span class="sxs-lookup"><span data-stu-id="88f7c-240">Create a department and associate it with the department hierarchy</span></span>](/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="88f7c-241">定义新部门</span><span class="sxs-lookup"><span data-stu-id="88f7c-241">Define new departments</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="88f7c-242">付薪周期和付薪期间</span><span class="sxs-lookup"><span data-stu-id="88f7c-242">Pay cycles and pay periods</span></span>

<span data-ttu-id="88f7c-243">付薪周期确定付薪的频率和工作人员获薪的具体天数。</span><span class="sxs-lookup"><span data-stu-id="88f7c-243">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="88f7c-244">例如，付薪周期可以是每月，并且可能在月末向员工付薪。</span><span class="sxs-lookup"><span data-stu-id="88f7c-244">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="88f7c-245">付薪周期也可以是每周，并且可能在付薪期间结束后的星期二向员工付薪。</span><span class="sxs-lookup"><span data-stu-id="88f7c-245">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="88f7c-246">为职位分配付薪周期是为了控制何时向所在职位的工作人员付薪。</span><span class="sxs-lookup"><span data-stu-id="88f7c-246">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="88f7c-247">创建付薪周期后，可以为每个周期生成付薪期间。</span><span class="sxs-lookup"><span data-stu-id="88f7c-247">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="88f7c-248">每个付薪期间包含一个基于您提供的信息的默认付薪日期。</span><span class="sxs-lookup"><span data-stu-id="88f7c-248">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="88f7c-249">但是，可以更改付薪期间中的默认付薪日期，以便应对异常，如付薪日期在假期中。</span><span class="sxs-lookup"><span data-stu-id="88f7c-249">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="88f7c-250">Dayforce 中使用以下信息：</span><span class="sxs-lookup"><span data-stu-id="88f7c-250">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="88f7c-251">付薪周期（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-251">Pay cycle (required)</span></span>
- <span data-ttu-id="88f7c-252">付薪周期频率（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-252">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="88f7c-253">期间开始日期（需要第一个付薪期间）</span><span class="sxs-lookup"><span data-stu-id="88f7c-253">Period start date (first pay period required)</span></span>
- <span data-ttu-id="88f7c-254">默认付薪日期（需要第一个付薪期间）</span><span class="sxs-lookup"><span data-stu-id="88f7c-254">Default payment date (first pay period required)</span></span>

<span data-ttu-id="88f7c-255">此信息与 Dayforce 集成为付薪组，并按各付薪周期的国家或地区分隔。</span><span class="sxs-lookup"><span data-stu-id="88f7c-255">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="88f7c-256">集成之前，必须至少生成一个付薪期间。</span><span class="sxs-lookup"><span data-stu-id="88f7c-256">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="88f7c-257">Dayforce 根据 Human Resources 中设置的第一个付款期间的开始日期和默认付款日期生成付款组日历和付款日期。</span><span class="sxs-lookup"><span data-stu-id="88f7c-257">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="88f7c-258">收入代码</span><span class="sxs-lookup"><span data-stu-id="88f7c-258">Earning codes</span></span>

<span data-ttu-id="88f7c-259">收入代码唯一标识工作人员获得的每种收入类型。</span><span class="sxs-lookup"><span data-stu-id="88f7c-259">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="88f7c-260">这些代码有多个与收入有关的参数，如会计规则、税法、报告要求和补偿费功能。</span><span class="sxs-lookup"><span data-stu-id="88f7c-260">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="88f7c-261">Dayforce 中使用以下信息：</span><span class="sxs-lookup"><span data-stu-id="88f7c-261">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="88f7c-262">收入代码（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-262">Earning Code (required)</span></span>
- <span data-ttu-id="88f7c-263">说明</span><span class="sxs-lookup"><span data-stu-id="88f7c-263">Description</span></span>
- <span data-ttu-id="88f7c-264">度量单位</span><span class="sxs-lookup"><span data-stu-id="88f7c-264">Unit of measure</span></span>
- <span data-ttu-id="88f7c-265">生产</span><span class="sxs-lookup"><span data-stu-id="88f7c-265">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="88f7c-266">工作人员数据</span><span class="sxs-lookup"><span data-stu-id="88f7c-266">Worker data</span></span>

<span data-ttu-id="88f7c-267">工作人员的对您的人力资源和工资系统十分重要的不同类型的记录。</span><span class="sxs-lookup"><span data-stu-id="88f7c-267">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="88f7c-268">您输入的信息可用于跟踪工作人员和个人信息。</span><span class="sxs-lookup"><span data-stu-id="88f7c-268">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="88f7c-269">您可以维护工作人员的以下信息:</span><span class="sxs-lookup"><span data-stu-id="88f7c-269">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="88f7c-270">**基本** – 维护有关工作人员的基本信息，如联系人信息、人口统计的信息、标识信息、系列信息、状态、兵役迁移国外的信息和个人和紧急事件联系人。</span><span class="sxs-lookup"><span data-stu-id="88f7c-270">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="88f7c-271">**雇用** – 维护有关工作人员雇用情况的信息，例如公司或组织隶属关系、职位分配、开始日期和结束日期、工作的雇用资格、条款，退休金、假期和重定位信息。</span><span class="sxs-lookup"><span data-stu-id="88f7c-271">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="88f7c-272">**休假和缺勤** – 维护有关工作人员的缺勤的信息，例如工作日历、缺勤事务和缺勤设置。</span><span class="sxs-lookup"><span data-stu-id="88f7c-272">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="88f7c-273">**薪酬和工资单** – 维护有关工作人员的薪酬计划和工资信息的信息，例如计划登记、证书、性能、佣金、税务信息、报废和薪金扣缴。</span><span class="sxs-lookup"><span data-stu-id="88f7c-273">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="88f7c-274">输入工作人员信息时，请注意 Dayforce 中使用的以下数据和配置。</span><span class="sxs-lookup"><span data-stu-id="88f7c-274">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="88f7c-275">一般信息</span><span class="sxs-lookup"><span data-stu-id="88f7c-275">General information</span></span>

- <span data-ttu-id="88f7c-276">人员编号（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-276">Personnel number (required)</span></span>
- <span data-ttu-id="88f7c-277">名字(必填)</span><span class="sxs-lookup"><span data-stu-id="88f7c-277">First name (required)</span></span>
- <span data-ttu-id="88f7c-278">姓氏(必填)</span><span class="sxs-lookup"><span data-stu-id="88f7c-278">Last name (required)</span></span>
- <span data-ttu-id="88f7c-279">中间名</span><span class="sxs-lookup"><span data-stu-id="88f7c-279">Middle name</span></span>
- <span data-ttu-id="88f7c-280">受聘日期</span><span class="sxs-lookup"><span data-stu-id="88f7c-280">Seniority date</span></span>
- <span data-ttu-id="88f7c-281">称作</span><span class="sxs-lookup"><span data-stu-id="88f7c-281">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="88f7c-282">个人信息</span><span class="sxs-lookup"><span data-stu-id="88f7c-282">Personal information</span></span>

- <span data-ttu-id="88f7c-283">婚姻状况（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-283">Marital status (required)</span></span>
- <span data-ttu-id="88f7c-284">出生日期（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-284">Birth date (required)</span></span>
- <span data-ttu-id="88f7c-285">性别（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-285">Gender (required)</span></span>
- <span data-ttu-id="88f7c-286">残疾人士</span><span class="sxs-lookup"><span data-stu-id="88f7c-286">Person with disabilities</span></span>
- <span data-ttu-id="88f7c-287">国籍的国家地区（仅适用于墨西哥）</span><span class="sxs-lookup"><span data-stu-id="88f7c-287">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="88f7c-288">地址信息</span><span class="sxs-lookup"><span data-stu-id="88f7c-288">Address information</span></span>

- <span data-ttu-id="88f7c-289">主要（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-289">Primary (required)</span></span>
- <span data-ttu-id="88f7c-290">国家/地区（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-290">Country/region (required)</span></span>
- <span data-ttu-id="88f7c-291">邮政编码（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-291">Postal code (required)</span></span>
- <span data-ttu-id="88f7c-292">街道编号（必填）（仅适用于墨西哥）</span><span class="sxs-lookup"><span data-stu-id="88f7c-292">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="88f7c-293">建筑物地址（仅适用于墨西哥）</span><span class="sxs-lookup"><span data-stu-id="88f7c-293">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="88f7c-294"> 市/县（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-294">City (required)</span></span>
- <span data-ttu-id="88f7c-295">省/直辖市/自治区（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-295">State (required)</span></span>
- <span data-ttu-id="88f7c-296">国家/地区（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-296">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="88f7c-297">联系人信息</span><span class="sxs-lookup"><span data-stu-id="88f7c-297">Contact information</span></span> 

- <span data-ttu-id="88f7c-298">主要（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-298">Primary (required)</span></span>
- <span data-ttu-id="88f7c-299">联系人号码（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-299">Contact number (required)</span></span>
- <span data-ttu-id="88f7c-300">函授</span><span class="sxs-lookup"><span data-stu-id="88f7c-300">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="88f7c-301">工资信息和收入代码</span><span class="sxs-lookup"><span data-stu-id="88f7c-301">Payroll information and earning codes</span></span>

<span data-ttu-id="88f7c-302">可以按给定付薪频率为员工分配特定收入，而员工则可以具有首选付款方式。</span><span class="sxs-lookup"><span data-stu-id="88f7c-302">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="88f7c-303">Dayforce 中使用以下字段确保使用这些首选项和设置。</span><span class="sxs-lookup"><span data-stu-id="88f7c-303">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="88f7c-304">收入代码</span><span class="sxs-lookup"><span data-stu-id="88f7c-304">Earning codes</span></span>

- <span data-ttu-id="88f7c-305">职位（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-305">Position (required)</span></span>
- <span data-ttu-id="88f7c-306">收入代码（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-306">Earning Code (required)</span></span>
- <span data-ttu-id="88f7c-307">频率（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-307">Frequency (required)</span></span>
- <span data-ttu-id="88f7c-308">金额（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-308">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="88f7c-309">工资单信息</span><span class="sxs-lookup"><span data-stu-id="88f7c-309">Payroll information</span></span>

- <span data-ttu-id="88f7c-310">付款方式</span><span class="sxs-lookup"><span data-stu-id="88f7c-310">Payment Method</span></span>
- <span data-ttu-id="88f7c-311">经济区域（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-311">Economic Region (required)</span></span>
- <span data-ttu-id="88f7c-312">员工福利 ID</span><span class="sxs-lookup"><span data-stu-id="88f7c-312">Employee Benefits ID</span></span>
- <span data-ttu-id="88f7c-313">国家/地区 ID 号（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-313">National ID Number (required)</span></span>
- <span data-ttu-id="88f7c-314">兵役编号</span><span class="sxs-lookup"><span data-stu-id="88f7c-314">Military Service Number</span></span>
- <span data-ttu-id="88f7c-315">班次 ID（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-315">Shift ID (required)</span></span>
- <span data-ttu-id="88f7c-316">税号（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-316">Tax Number (required)</span></span>
- <span data-ttu-id="88f7c-317">工会 ID（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-317">Union ID (required)</span></span>
- <span data-ttu-id="88f7c-318">工作日 ID（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-318">Work Day ID (required)</span></span>
- <span data-ttu-id="88f7c-319">工作许可证编号</span><span class="sxs-lookup"><span data-stu-id="88f7c-319">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="88f7c-320">对于付款方式，墨西哥支持 **现金**、**支票**（公司的实际支票）和 **电子支付**。</span><span class="sxs-lookup"><span data-stu-id="88f7c-320">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="88f7c-321">如果不指定付款方式，则默认使用 **支票**。</span><span class="sxs-lookup"><span data-stu-id="88f7c-321">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="88f7c-322">雇用详细信息</span><span class="sxs-lookup"><span data-stu-id="88f7c-322">Employment details</span></span>

<span data-ttu-id="88f7c-323">在 Dayforce 中派生员工的入职、离职和重新入职状态时，雇用详细信息历史记录至关重要。</span><span class="sxs-lookup"><span data-stu-id="88f7c-323">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="88f7c-324">Dayforce 一次仅支持一条活动雇用记录。</span><span class="sxs-lookup"><span data-stu-id="88f7c-324">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="88f7c-325">雇用开始日期（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-325">Employment start date (required)</span></span>
- <span data-ttu-id="88f7c-326">雇佣结束日期</span><span class="sxs-lookup"><span data-stu-id="88f7c-326">Employment end date</span></span>
- <span data-ttu-id="88f7c-327">入职日期</span><span class="sxs-lookup"><span data-stu-id="88f7c-327">Start date</span></span>
- <span data-ttu-id="88f7c-328">调整后的开始日期</span><span class="sxs-lookup"><span data-stu-id="88f7c-328">Adjusted start date</span></span>
- <span data-ttu-id="88f7c-329">离职日期（离职时必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-329">Termination date (required upon termination)</span></span>
- <span data-ttu-id="88f7c-330">离职原因（离职时必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-330">Termination reason (required upon termination)</span></span>

<span data-ttu-id="88f7c-331">员工的关键日期通过使用以下信息派生。</span><span class="sxs-lookup"><span data-stu-id="88f7c-331">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="88f7c-332">人力资源</span><span class="sxs-lookup"><span data-stu-id="88f7c-332">Human Resources</span></span>                | <span data-ttu-id="88f7c-333">Dayforce</span><span class="sxs-lookup"><span data-stu-id="88f7c-333">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88f7c-334">最近雇用日期</span><span class="sxs-lookup"><span data-stu-id="88f7c-334">Most recent hire date</span></span> | <span data-ttu-id="88f7c-335">当前未离职雇用历史记录的雇用开始日期</span><span class="sxs-lookup"><span data-stu-id="88f7c-335">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="88f7c-336">终止日期</span><span class="sxs-lookup"><span data-stu-id="88f7c-336">Termination date</span></span>      | <span data-ttu-id="88f7c-337">当前未离职雇用历史记录的离职日期</span><span class="sxs-lookup"><span data-stu-id="88f7c-337">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="88f7c-338">入职日期</span><span class="sxs-lookup"><span data-stu-id="88f7c-338">Start date</span></span>            | <span data-ttu-id="88f7c-339">当前非活动雇用历史记录经过调整后的开始日期、开始日期或雇用开始时间。</span><span class="sxs-lookup"><span data-stu-id="88f7c-339">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="88f7c-340">原始雇用日期</span><span class="sxs-lookup"><span data-stu-id="88f7c-340">Original hire date</span></span>    | <span data-ttu-id="88f7c-341">最早雇用历史记录的雇用开始时间</span><span class="sxs-lookup"><span data-stu-id="88f7c-341">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="88f7c-342">薪酬</span><span class="sxs-lookup"><span data-stu-id="88f7c-342">Compensation</span></span>

<span data-ttu-id="88f7c-343">在整个雇用期间都必须为每个员工的主要职位关联一个固定的薪酬计划。</span><span class="sxs-lookup"><span data-stu-id="88f7c-343">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="88f7c-344">此期间在雇用员工的日期（或雇用开始日期）开始，持续到员工离职为止。</span><span class="sxs-lookup"><span data-stu-id="88f7c-344">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="88f7c-345">生效日期（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-345">Effective Date (required)</span></span>
- <span data-ttu-id="88f7c-346">到期日期</span><span class="sxs-lookup"><span data-stu-id="88f7c-346">Expiration date</span></span>
- <span data-ttu-id="88f7c-347">付薪比率（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-347">Pay Rate (required)</span></span>
- <span data-ttu-id="88f7c-348">付薪比率转换（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-348">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="88f7c-349">年度等价金额（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-349">Annual equivalent (required)</span></span>
- <span data-ttu-id="88f7c-350">小时等价金额（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-350">Hourly equivalent (required)</span></span>

<span data-ttu-id="88f7c-351">如果小时员工有多个职位，则将主要职位的固定薪酬作为员工级基本比率/工资导入 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="88f7c-351">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="88f7c-352">对于非主要职位，小时收费比率保存到 Dayforce 中的相应位置。</span><span class="sxs-lookup"><span data-stu-id="88f7c-352">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="88f7c-353">如果固定员工有多个职位，则从所有活动职位派生累积小时费率和年工资，并用作员工级基本费率/工资。</span><span class="sxs-lookup"><span data-stu-id="88f7c-353">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="88f7c-354">标识号</span><span class="sxs-lookup"><span data-stu-id="88f7c-354">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="88f7c-355">社会安全标识符</span><span class="sxs-lookup"><span data-stu-id="88f7c-355">Social Security identifier</span></span> 

<span data-ttu-id="88f7c-356">每个员工必须有一个主要标识符。</span><span class="sxs-lookup"><span data-stu-id="88f7c-356">Every employee must have one primary identifier.</span></span> <span data-ttu-id="88f7c-357">此标识符的类型必须为 **SSN** 身份证明类型。</span><span class="sxs-lookup"><span data-stu-id="88f7c-357">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="88f7c-358">在 Dayforce 中，将自动派生为雇用时需要的员工社会安全标识符。</span><span class="sxs-lookup"><span data-stu-id="88f7c-358">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="88f7c-359">主要（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-359">Primary (required)</span></span>
- <span data-ttu-id="88f7c-360">身份证明类型 =“SSN”</span><span class="sxs-lookup"><span data-stu-id="88f7c-360">Identification Type = "SSN"</span></span>
- <span data-ttu-id="88f7c-361">签发日期</span><span class="sxs-lookup"><span data-stu-id="88f7c-361">Issued Date</span></span>
- <span data-ttu-id="88f7c-362">到期日期</span><span class="sxs-lookup"><span data-stu-id="88f7c-362">Expiration Date</span></span>

<span data-ttu-id="88f7c-363">员工可以声明 **SSN** 身份证明类型的多个身份证明编号。</span><span class="sxs-lookup"><span data-stu-id="88f7c-363">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="88f7c-364">但是，只会将标记为 **主要** 的记录集成到 Dayforce，号码是有效还是已过期无关紧要。</span><span class="sxs-lookup"><span data-stu-id="88f7c-364">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="88f7c-365">银行帐户和付款</span><span class="sxs-lookup"><span data-stu-id="88f7c-365">Bank accounts and disbursements</span></span>

<span data-ttu-id="88f7c-366">必须为选择通过银行转账付薪的员工输入有效的银行帐户信息。</span><span class="sxs-lookup"><span data-stu-id="88f7c-366">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="88f7c-367">人力资源</span><span class="sxs-lookup"><span data-stu-id="88f7c-367">Human Resources</span></span>                         | <span data-ttu-id="88f7c-368">Dayforce</span><span class="sxs-lookup"><span data-stu-id="88f7c-368">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88f7c-369">银行帐号（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-369">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="88f7c-370">SWIFT 代码（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-370">SWIFT code (required)</span></span>          | <span data-ttu-id="88f7c-371">在墨西哥处理工资单时使用的 **银行 ID** 字段。</span><span class="sxs-lookup"><span data-stu-id="88f7c-371">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="88f7c-372">分行编号（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-372">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="88f7c-373">银行帐户类型（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-373">Bank account type (required)</span></span>   | <span data-ttu-id="88f7c-374">在墨西哥处理工资单时使用的 **帐户类型** 字段。</span><span class="sxs-lookup"><span data-stu-id="88f7c-374">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="88f7c-375">支持的值包括 **支票** 和 **工资单**。</span><span class="sxs-lookup"><span data-stu-id="88f7c-375">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="88f7c-376">选择通过银行转帐付薪的员工必须提供一个链接，该链接是主要地址在墨西哥且与墨西哥银行的有效银行帐户关联的法人名下的余额帐户。</span><span class="sxs-lookup"><span data-stu-id="88f7c-376">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="88f7c-377">将忽略其他所有非余额帐户。</span><span class="sxs-lookup"><span data-stu-id="88f7c-377">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="88f7c-378">地址信息</span><span class="sxs-lookup"><span data-stu-id="88f7c-378">Address information</span></span>

<span data-ttu-id="88f7c-379">每个员工必须有一个主要职位。</span><span class="sxs-lookup"><span data-stu-id="88f7c-379">Every employee must have one primary location.</span></span> <span data-ttu-id="88f7c-380">在 Dayforce 中，此职位用于确定员工的主要纳税地址。</span><span class="sxs-lookup"><span data-stu-id="88f7c-380">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="88f7c-381">主要（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-381">Primary (required)</span></span>
- <span data-ttu-id="88f7c-382">国家/地区（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-382">Country/region (required)</span></span>
- <span data-ttu-id="88f7c-383">邮政编码（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-383">Zip/postal code (required)</span></span>
- <span data-ttu-id="88f7c-384">街道（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-384">Street (required)</span></span>
- <span data-ttu-id="88f7c-385">街道号（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-385">Street Number (required)</span></span>
- <span data-ttu-id="88f7c-386">建筑物地址</span><span class="sxs-lookup"><span data-stu-id="88f7c-386">Building Complement</span></span>
- <span data-ttu-id="88f7c-387"> 市/县（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-387">City (required)</span></span>
- <span data-ttu-id="88f7c-388">省/直辖市/自治区（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-388">State (required)</span></span>
- <span data-ttu-id="88f7c-389">国家/地区（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-389">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="88f7c-390">在美国和加拿大配置数据以生成工资单</span><span class="sxs-lookup"><span data-stu-id="88f7c-390">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="88f7c-391">如果要在美国和加拿大为员工生成付薪，必须配置以下元素：</span><span class="sxs-lookup"><span data-stu-id="88f7c-391">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="88f7c-392">需要职位的部门。</span><span class="sxs-lookup"><span data-stu-id="88f7c-392">Departments are required on positions.</span></span>
- <span data-ttu-id="88f7c-393">必须将成本中心设置为财务维度，并且成本中心必须为默认财务维度字符串的第一个元素。</span><span class="sxs-lookup"><span data-stu-id="88f7c-393">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="88f7c-394">可以配置 Human Resources，以便要求在“职位”中指定“部门”。</span><span class="sxs-lookup"><span data-stu-id="88f7c-394">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="88f7c-395">方法是，转到 **人力资源共享职位 > 职位 > 必填职位中的部门**。</span><span class="sxs-lookup"><span data-stu-id="88f7c-395">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="88f7c-396">建议为集成实施此项设置。</span><span class="sxs-lookup"><span data-stu-id="88f7c-396">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="88f7c-397">工作类型</span><span class="sxs-lookup"><span data-stu-id="88f7c-397">Job types</span></span>

<span data-ttu-id="88f7c-398">工作类型用于将类似的工作分组为类别。</span><span class="sxs-lookup"><span data-stu-id="88f7c-398">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="88f7c-399">要在美国和加拿大处理工资单，需要工作类型。</span><span class="sxs-lookup"><span data-stu-id="88f7c-399">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="88f7c-400">例如，工作类型包括全职和兼职，或按工资付薪和按小时付薪。</span><span class="sxs-lookup"><span data-stu-id="88f7c-400">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="88f7c-401">作业类型作为付薪类型映射到 Dayforce，用于指示员工按小时还是按工资付薪。</span><span class="sxs-lookup"><span data-stu-id="88f7c-401">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="88f7c-402">需要以下作业类型和描述。</span><span class="sxs-lookup"><span data-stu-id="88f7c-402">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="88f7c-403">工作类型</span><span class="sxs-lookup"><span data-stu-id="88f7c-403">Job type</span></span>   | <span data-ttu-id="88f7c-404">说明</span><span class="sxs-lookup"><span data-stu-id="88f7c-404">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="88f7c-405">每小时</span><span class="sxs-lookup"><span data-stu-id="88f7c-405">Hourly</span></span>     | <span data-ttu-id="88f7c-406">每小时</span><span class="sxs-lookup"><span data-stu-id="88f7c-406">Hourly</span></span>      |
| <span data-ttu-id="88f7c-407">按工资</span><span class="sxs-lookup"><span data-stu-id="88f7c-407">Salaried</span></span>   | <span data-ttu-id="88f7c-408">按工资</span><span class="sxs-lookup"><span data-stu-id="88f7c-408">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="88f7c-409">职位类型</span><span class="sxs-lookup"><span data-stu-id="88f7c-409">Position types</span></span> 

<span data-ttu-id="88f7c-410">可使用职位类型描述职位是全职、兼职还是其他。</span><span class="sxs-lookup"><span data-stu-id="88f7c-410">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="88f7c-411">职位类型作为付薪类别映射到 Dayforce，用于指示员工是全职还是兼职。</span><span class="sxs-lookup"><span data-stu-id="88f7c-411">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="88f7c-412">需要以下职位类型和描述。</span><span class="sxs-lookup"><span data-stu-id="88f7c-412">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="88f7c-413">职位类型</span><span class="sxs-lookup"><span data-stu-id="88f7c-413">Position type</span></span>   | <span data-ttu-id="88f7c-414">说明</span><span class="sxs-lookup"><span data-stu-id="88f7c-414">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="88f7c-415">全职</span><span class="sxs-lookup"><span data-stu-id="88f7c-415">Full-time</span></span>       | <span data-ttu-id="88f7c-416">全职员工</span><span class="sxs-lookup"><span data-stu-id="88f7c-416">Full time employee</span></span> |
| <span data-ttu-id="88f7c-417">兼职</span><span class="sxs-lookup"><span data-stu-id="88f7c-417">Part-time</span></span>       | <span data-ttu-id="88f7c-418">兼职员工</span><span class="sxs-lookup"><span data-stu-id="88f7c-418">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="88f7c-419">原因代码</span><span class="sxs-lookup"><span data-stu-id="88f7c-419">Reason codes</span></span>

<span data-ttu-id="88f7c-420">原因代码提供有关员工状态的信息。</span><span class="sxs-lookup"><span data-stu-id="88f7c-420">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="88f7c-421">原因代码作为状态代码映射到 Dayforce，用于指示更改员工的职位或雇用状态的原因。</span><span class="sxs-lookup"><span data-stu-id="88f7c-421">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="88f7c-422">需要以下原因代码和描述。</span><span class="sxs-lookup"><span data-stu-id="88f7c-422">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="88f7c-423">原因代码</span><span class="sxs-lookup"><span data-stu-id="88f7c-423">Reason code</span></span>    | <span data-ttu-id="88f7c-424">说明</span><span class="sxs-lookup"><span data-stu-id="88f7c-424">Description</span></span>      | <span data-ttu-id="88f7c-425">适用的场景</span><span class="sxs-lookup"><span data-stu-id="88f7c-425">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="88f7c-426">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="88f7c-426">RESIGNATION</span></span>    | <span data-ttu-id="88f7c-427">辞职</span><span class="sxs-lookup"><span data-stu-id="88f7c-427">Resignation</span></span>      | <span data-ttu-id="88f7c-428">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="88f7c-428">Terminate worker</span></span>     |
| <span data-ttu-id="88f7c-429">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="88f7c-429">TERMINATION</span></span>    | <span data-ttu-id="88f7c-430">终止</span><span class="sxs-lookup"><span data-stu-id="88f7c-430">Termination</span></span>      | <span data-ttu-id="88f7c-431">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="88f7c-431">Terminate worker</span></span>     |
| <span data-ttu-id="88f7c-432">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="88f7c-432">RETIREMENT</span></span>     | <span data-ttu-id="88f7c-433">退休</span><span class="sxs-lookup"><span data-stu-id="88f7c-433">Retirement</span></span>       | <span data-ttu-id="88f7c-434">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="88f7c-434">Terminate worker</span></span>     |
| <span data-ttu-id="88f7c-435">OTHER</span><span class="sxs-lookup"><span data-stu-id="88f7c-435">OTHER</span></span>          | <span data-ttu-id="88f7c-436">其他原因</span><span class="sxs-lookup"><span data-stu-id="88f7c-436">Other Reasons</span></span>    | <span data-ttu-id="88f7c-437">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="88f7c-437">Terminate worker</span></span>     |
| <span data-ttu-id="88f7c-438">DEATH</span><span class="sxs-lookup"><span data-stu-id="88f7c-438">DEATH</span></span>          | <span data-ttu-id="88f7c-439">死亡</span><span class="sxs-lookup"><span data-stu-id="88f7c-439">Death</span></span>            | <span data-ttu-id="88f7c-440">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="88f7c-440">Terminate worker</span></span>     |
| <span data-ttu-id="88f7c-441">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="88f7c-441">LEAVEOFABSENCE</span></span> | <span data-ttu-id="88f7c-442">休假</span><span class="sxs-lookup"><span data-stu-id="88f7c-442">Leave of Absence</span></span> | <span data-ttu-id="88f7c-443">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="88f7c-443">Terminate worker</span></span>     |
| <span data-ttu-id="88f7c-444">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="88f7c-444">CONTRACTEND</span></span>    | <span data-ttu-id="88f7c-445">合同结束</span><span class="sxs-lookup"><span data-stu-id="88f7c-445">End of Contract</span></span>  | <span data-ttu-id="88f7c-446">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="88f7c-446">Terminate worker</span></span>     |
| <span data-ttu-id="88f7c-447">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="88f7c-447">SALARYCHANGE</span></span>   | <span data-ttu-id="88f7c-448">工资改变</span><span class="sxs-lookup"><span data-stu-id="88f7c-448">Change of Salary</span></span> | <span data-ttu-id="88f7c-449">薪酬</span><span class="sxs-lookup"><span data-stu-id="88f7c-449">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="88f7c-450">婚姻状况</span><span class="sxs-lookup"><span data-stu-id="88f7c-450">Marital status</span></span>

<span data-ttu-id="88f7c-451">婚姻状态值映射到 Dayforce，并在集成时根据需要转换为接受的值。</span><span class="sxs-lookup"><span data-stu-id="88f7c-451">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="88f7c-452">下表显示婚姻状态值如何映射到 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="88f7c-452">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="88f7c-453">人力资源</span><span class="sxs-lookup"><span data-stu-id="88f7c-453">Human Resources</span></span>                 | <span data-ttu-id="88f7c-454">Dayforce</span><span class="sxs-lookup"><span data-stu-id="88f7c-454">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="88f7c-455">已婚</span><span class="sxs-lookup"><span data-stu-id="88f7c-455">Married</span></span>                | <span data-ttu-id="88f7c-456">已婚</span><span class="sxs-lookup"><span data-stu-id="88f7c-456">Married</span></span>              |
| <span data-ttu-id="88f7c-457">单一</span><span class="sxs-lookup"><span data-stu-id="88f7c-457">Single</span></span>                 | <span data-ttu-id="88f7c-458">单一</span><span class="sxs-lookup"><span data-stu-id="88f7c-458">Single</span></span>               |
| <span data-ttu-id="88f7c-459">丧偶</span><span class="sxs-lookup"><span data-stu-id="88f7c-459">Widowed</span></span>                | <span data-ttu-id="88f7c-460">丧偶</span><span class="sxs-lookup"><span data-stu-id="88f7c-460">Widowed</span></span>              |
| <span data-ttu-id="88f7c-461">离婚</span><span class="sxs-lookup"><span data-stu-id="88f7c-461">Divorced</span></span>               | <span data-ttu-id="88f7c-462">离异</span><span class="sxs-lookup"><span data-stu-id="88f7c-462">Divorced</span></span>             |
| <span data-ttu-id="88f7c-463">注册伴侣关系</span><span class="sxs-lookup"><span data-stu-id="88f7c-463">Registered Partnership</span></span> | <span data-ttu-id="88f7c-464">民事结合关系</span><span class="sxs-lookup"><span data-stu-id="88f7c-464">Domestic Partnership</span></span> |
| <span data-ttu-id="88f7c-465">None</span><span class="sxs-lookup"><span data-stu-id="88f7c-465">None</span></span>                   | <span data-ttu-id="88f7c-466">None</span><span class="sxs-lookup"><span data-stu-id="88f7c-466">None</span></span>                 |
| <span data-ttu-id="88f7c-467">未婚同居</span><span class="sxs-lookup"><span data-stu-id="88f7c-467">Cohabiting</span></span>             | <span data-ttu-id="88f7c-468">未婚同居</span><span class="sxs-lookup"><span data-stu-id="88f7c-468">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="88f7c-469">性</span><span class="sxs-lookup"><span data-stu-id="88f7c-469">Gender</span></span>

<span data-ttu-id="88f7c-470">性别指派映射到 Dayforce，并在集成时根据需要转换为接受的值。</span><span class="sxs-lookup"><span data-stu-id="88f7c-470">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="88f7c-471">下表显示性别指派如何映射到 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="88f7c-471">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="88f7c-472">人力资源</span><span class="sxs-lookup"><span data-stu-id="88f7c-472">Human Resources</span></span>       | <span data-ttu-id="88f7c-473">Dayforce</span><span class="sxs-lookup"><span data-stu-id="88f7c-473">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="88f7c-474">男</span><span class="sxs-lookup"><span data-stu-id="88f7c-474">Male</span></span>         | <span data-ttu-id="88f7c-475">男</span><span class="sxs-lookup"><span data-stu-id="88f7c-475">Male</span></span>            |
| <span data-ttu-id="88f7c-476">女</span><span class="sxs-lookup"><span data-stu-id="88f7c-476">Female</span></span>       | <span data-ttu-id="88f7c-477">女</span><span class="sxs-lookup"><span data-stu-id="88f7c-477">Female</span></span>          |
| <span data-ttu-id="88f7c-478">非特定</span><span class="sxs-lookup"><span data-stu-id="88f7c-478">Non-specific</span></span> | <span data-ttu-id="88f7c-479">*不支持*</span><span class="sxs-lookup"><span data-stu-id="88f7c-479">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="88f7c-480">收入代码</span><span class="sxs-lookup"><span data-stu-id="88f7c-480">Earning codes</span></span>

<span data-ttu-id="88f7c-481">收入代码唯一标识工作人员获得的每种收入类型。</span><span class="sxs-lookup"><span data-stu-id="88f7c-481">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="88f7c-482">这些代码有多个与收入有关的参数，如会计规则、税法、报告要求和补偿费功能。</span><span class="sxs-lookup"><span data-stu-id="88f7c-482">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="88f7c-483">如果使用不受支持的频率，默认将使用 **每个付薪** 频率进行计算。</span><span class="sxs-lookup"><span data-stu-id="88f7c-483">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="88f7c-484">支持的频率</span><span class="sxs-lookup"><span data-stu-id="88f7c-484">Supported frequencies</span></span>

- <span data-ttu-id="88f7c-485">所有</span><span class="sxs-lookup"><span data-stu-id="88f7c-485">All</span></span>
- <span data-ttu-id="88f7c-486">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="88f7c-486">EVERYPAY</span></span>
- <span data-ttu-id="88f7c-487">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="88f7c-487">EACHPAYPERIOD</span></span>
- <span data-ttu-id="88f7c-488">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="88f7c-488">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="88f7c-489">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="88f7c-489">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="88f7c-490">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="88f7c-490">1OFMTH</span></span>
- <span data-ttu-id="88f7c-491">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="88f7c-491">LASTOFMTH</span></span>
- <span data-ttu-id="88f7c-492">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="88f7c-492">2OFMTH</span></span>
- <span data-ttu-id="88f7c-493">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="88f7c-493">3OFMTH</span></span>
- <span data-ttu-id="88f7c-494">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="88f7c-494">4OFMTH</span></span>
- <span data-ttu-id="88f7c-495">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="88f7c-495">5OFMTH</span></span>
- <span data-ttu-id="88f7c-496">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="88f7c-496">1N2OFMTH</span></span>
- <span data-ttu-id="88f7c-497">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="88f7c-497">3N4OFMTH</span></span>
- <span data-ttu-id="88f7c-498">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="88f7c-498">1N3OFMTH</span></span>
- <span data-ttu-id="88f7c-499">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="88f7c-499">1N4OFMTH</span></span>
- <span data-ttu-id="88f7c-500">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="88f7c-500">2N3OFMTH</span></span>
- <span data-ttu-id="88f7c-501">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="88f7c-501">2N4OFMTH</span></span>
- <span data-ttu-id="88f7c-502">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="88f7c-502">1N2N3OFMTH</span></span>
- <span data-ttu-id="88f7c-503">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="88f7c-503">1N2N4OFMTH</span></span>
- <span data-ttu-id="88f7c-504">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="88f7c-504">1N3N4OFMTH</span></span>
- <span data-ttu-id="88f7c-505">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="88f7c-505">2N3N4OFMTH</span></span>
- <span data-ttu-id="88f7c-506">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="88f7c-506">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="88f7c-507">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="88f7c-507">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="88f7c-508">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="88f7c-508">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="88f7c-509">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="88f7c-509">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="88f7c-510">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="88f7c-510">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="88f7c-511">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="88f7c-511">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="88f7c-512">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="88f7c-512">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="88f7c-513">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="88f7c-513">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="88f7c-514">地址</span><span class="sxs-lookup"><span data-stu-id="88f7c-514">Addresses</span></span>

<span data-ttu-id="88f7c-515">特定国家或地区、省/直辖市/自治区和县/市（自治市）代码的标识需要 Dayforce 和国内/地区内提供商可识别的特定格式。</span><span class="sxs-lookup"><span data-stu-id="88f7c-515">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="88f7c-516">尽管县/市的格式可变，但是每个县/市必须与一个省/直辖市/自治区关联。</span><span class="sxs-lookup"><span data-stu-id="88f7c-516">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="88f7c-517">人力资源</span><span class="sxs-lookup"><span data-stu-id="88f7c-517">Human Resources</span></span>          | <span data-ttu-id="88f7c-518">Dayforce</span><span class="sxs-lookup"><span data-stu-id="88f7c-518">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="88f7c-519">国家/地区</span><span class="sxs-lookup"><span data-stu-id="88f7c-519">Country/Region</span></span>  | <span data-ttu-id="88f7c-520">国家/地区代码</span><span class="sxs-lookup"><span data-stu-id="88f7c-520">Country Code</span></span>          |
| <span data-ttu-id="88f7c-521">邮政编码 </span><span class="sxs-lookup"><span data-stu-id="88f7c-521">Zip/Postal Code</span></span> | <span data-ttu-id="88f7c-522">邮政编码</span><span class="sxs-lookup"><span data-stu-id="88f7c-522">Postal Code</span></span>           |
| <span data-ttu-id="88f7c-523">状态</span><span class="sxs-lookup"><span data-stu-id="88f7c-523">State</span></span>           | <span data-ttu-id="88f7c-524">省/直辖市/自治区代码</span><span class="sxs-lookup"><span data-stu-id="88f7c-524">State Code</span></span>            |
| <span data-ttu-id="88f7c-525">城市</span><span class="sxs-lookup"><span data-stu-id="88f7c-525">City</span></span>            | <span data-ttu-id="88f7c-526">城市</span><span class="sxs-lookup"><span data-stu-id="88f7c-526">City</span></span>                  |
| <span data-ttu-id="88f7c-527">县</span><span class="sxs-lookup"><span data-stu-id="88f7c-527">County</span></span>          | <span data-ttu-id="88f7c-528">县（自治市）</span><span class="sxs-lookup"><span data-stu-id="88f7c-528">County (Municipality)</span></span> |
| <span data-ttu-id="88f7c-529">街道</span><span class="sxs-lookup"><span data-stu-id="88f7c-529">Street</span></span>          | <span data-ttu-id="88f7c-530">地址行 1</span><span class="sxs-lookup"><span data-stu-id="88f7c-530">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="88f7c-531">税区</span><span class="sxs-lookup"><span data-stu-id="88f7c-531">Tax regions</span></span>

<span data-ttu-id="88f7c-532">税区用于确定应在生成工资单期间应用的适当税费。</span><span class="sxs-lookup"><span data-stu-id="88f7c-532">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="88f7c-533">税区作为位置地址映射到 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="88f7c-533">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="88f7c-534">默认税区必须与工作人员的活动职位关联。</span><span class="sxs-lookup"><span data-stu-id="88f7c-534">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="88f7c-535">税区（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-535">Tax region (required)</span></span>
- <span data-ttu-id="88f7c-536">国家/地区（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-536">Country/Region (required)</span></span>
- <span data-ttu-id="88f7c-537">省/直辖市/自治区（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-537">State (required)</span></span>
- <span data-ttu-id="88f7c-538">县</span><span class="sxs-lookup"><span data-stu-id="88f7c-538">County</span></span> 
- <span data-ttu-id="88f7c-539"> 市/县（必填）</span><span class="sxs-lookup"><span data-stu-id="88f7c-539">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="88f7c-540">在墨西哥配置数据以生成工资单</span><span class="sxs-lookup"><span data-stu-id="88f7c-540">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="88f7c-541">如果要在墨西哥为员工生成付薪，必须配置以下元素：</span><span class="sxs-lookup"><span data-stu-id="88f7c-541">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="88f7c-542">需要职位的部门。</span><span class="sxs-lookup"><span data-stu-id="88f7c-542">Departments are required on positions.</span></span>
- <span data-ttu-id="88f7c-543">必须将成本中心设置为财务维度，并且成本中心必须为默认财务维度字符串的第一个元素。</span><span class="sxs-lookup"><span data-stu-id="88f7c-543">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="88f7c-544">工作类型</span><span class="sxs-lookup"><span data-stu-id="88f7c-544">Job types</span></span>

<span data-ttu-id="88f7c-545">工作类型用于将类似的工作分组为类别。</span><span class="sxs-lookup"><span data-stu-id="88f7c-545">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="88f7c-546">在墨西哥需要工作类型才能处理工资单。</span><span class="sxs-lookup"><span data-stu-id="88f7c-546">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="88f7c-547">例如，工作类型包括全职和兼职，或按工资付薪和按小时付薪。</span><span class="sxs-lookup"><span data-stu-id="88f7c-547">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="88f7c-548">作业类型作为付薪类型映射到 Dayforce，用于指示员工按小时还是按工资付薪。</span><span class="sxs-lookup"><span data-stu-id="88f7c-548">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="88f7c-549">需要以下作业类型和描述。</span><span class="sxs-lookup"><span data-stu-id="88f7c-549">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="88f7c-550">工作类型</span><span class="sxs-lookup"><span data-stu-id="88f7c-550">Job type</span></span>   | <span data-ttu-id="88f7c-551">说明</span><span class="sxs-lookup"><span data-stu-id="88f7c-551">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="88f7c-552">每小时</span><span class="sxs-lookup"><span data-stu-id="88f7c-552">Hourly</span></span>     | <span data-ttu-id="88f7c-553">墨西哥按小时</span><span class="sxs-lookup"><span data-stu-id="88f7c-553">MX Hourly</span></span>   |
| <span data-ttu-id="88f7c-554">按工资</span><span class="sxs-lookup"><span data-stu-id="88f7c-554">Salaried</span></span>   | <span data-ttu-id="88f7c-555">墨西哥按工资</span><span class="sxs-lookup"><span data-stu-id="88f7c-555">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="88f7c-556">职位类型</span><span class="sxs-lookup"><span data-stu-id="88f7c-556">Position types</span></span> 

<span data-ttu-id="88f7c-557">可使用职位类型描述职位是全职、兼职还是其他。</span><span class="sxs-lookup"><span data-stu-id="88f7c-557">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="88f7c-558">职位类型作为付薪类别映射到 Dayforce，用于指示员工是全职还是兼职。</span><span class="sxs-lookup"><span data-stu-id="88f7c-558">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="88f7c-559">需要以下职位类型和描述。</span><span class="sxs-lookup"><span data-stu-id="88f7c-559">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="88f7c-560">职位类型</span><span class="sxs-lookup"><span data-stu-id="88f7c-560">Position type</span></span>   | <span data-ttu-id="88f7c-561">说明</span><span class="sxs-lookup"><span data-stu-id="88f7c-561">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="88f7c-562">全职</span><span class="sxs-lookup"><span data-stu-id="88f7c-562">Full-time</span></span>       | <span data-ttu-id="88f7c-563">全职员工</span><span class="sxs-lookup"><span data-stu-id="88f7c-563">Full time employee</span></span> |
| <span data-ttu-id="88f7c-564">兼职</span><span class="sxs-lookup"><span data-stu-id="88f7c-564">Part-time</span></span>       | <span data-ttu-id="88f7c-565">兼职员工</span><span class="sxs-lookup"><span data-stu-id="88f7c-565">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="88f7c-566">原因代码</span><span class="sxs-lookup"><span data-stu-id="88f7c-566">Reason codes</span></span>

<span data-ttu-id="88f7c-567">原因代码提供有关员工状态的信息。</span><span class="sxs-lookup"><span data-stu-id="88f7c-567">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="88f7c-568">原因代码作为状态代码映射到 Dayforce，用于指示更改员工的职位或雇用状态的原因。</span><span class="sxs-lookup"><span data-stu-id="88f7c-568">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="88f7c-569">需要以下原因代码和描述。</span><span class="sxs-lookup"><span data-stu-id="88f7c-569">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="88f7c-570">原因代码</span><span class="sxs-lookup"><span data-stu-id="88f7c-570">Reason code</span></span>            | <span data-ttu-id="88f7c-571">说明</span><span class="sxs-lookup"><span data-stu-id="88f7c-571">Description</span></span>                    | <span data-ttu-id="88f7c-572">适用的场景</span><span class="sxs-lookup"><span data-stu-id="88f7c-572">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="88f7c-573">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="88f7c-573">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="88f7c-574">首次付薪前离职</span><span class="sxs-lookup"><span data-stu-id="88f7c-574">Departure before first payroll</span></span> | <span data-ttu-id="88f7c-575">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="88f7c-575">Terminate worker</span></span>     |
| <span data-ttu-id="88f7c-576">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="88f7c-576">RESIGNATION</span></span>            | <span data-ttu-id="88f7c-577">辞职</span><span class="sxs-lookup"><span data-stu-id="88f7c-577">Resignation</span></span>                    | <span data-ttu-id="88f7c-578">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="88f7c-578">Terminate worker</span></span>     |
| <span data-ttu-id="88f7c-579">PENSION</span><span class="sxs-lookup"><span data-stu-id="88f7c-579">PENSION</span></span>                | <span data-ttu-id="88f7c-580">退休金</span><span class="sxs-lookup"><span data-stu-id="88f7c-580">Pension</span></span>                        | <span data-ttu-id="88f7c-581">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="88f7c-581">Terminate worker</span></span>     |
| <span data-ttu-id="88f7c-582">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="88f7c-582">TERMINATION</span></span>            | <span data-ttu-id="88f7c-583">终止</span><span class="sxs-lookup"><span data-stu-id="88f7c-583">Termination</span></span>                    | <span data-ttu-id="88f7c-584">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="88f7c-584">Terminate worker</span></span>     |
| <span data-ttu-id="88f7c-585">退休</span><span class="sxs-lookup"><span data-stu-id="88f7c-585">RETIREMENT</span></span>             | <span data-ttu-id="88f7c-586">退休</span><span class="sxs-lookup"><span data-stu-id="88f7c-586">Retirement</span></span>                     | <span data-ttu-id="88f7c-587">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="88f7c-587">Terminate worker</span></span>     |
| <span data-ttu-id="88f7c-588">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="88f7c-588">ABSENTEE</span></span>               | <span data-ttu-id="88f7c-589">缺勤者</span><span class="sxs-lookup"><span data-stu-id="88f7c-589">Absentee</span></span>                       | <span data-ttu-id="88f7c-590">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="88f7c-590">Terminate worker</span></span>     |
| <span data-ttu-id="88f7c-591">OTHER</span><span class="sxs-lookup"><span data-stu-id="88f7c-591">OTHER</span></span>                  | <span data-ttu-id="88f7c-592">其他原因</span><span class="sxs-lookup"><span data-stu-id="88f7c-592">Other Reasons</span></span>                  | <span data-ttu-id="88f7c-593">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="88f7c-593">Terminate worker</span></span>     |
| <span data-ttu-id="88f7c-594">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="88f7c-594">CLOSURE</span></span>                | <span data-ttu-id="88f7c-595">停业</span><span class="sxs-lookup"><span data-stu-id="88f7c-595">Business Closure</span></span>               | <span data-ttu-id="88f7c-596">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="88f7c-596">Terminate worker</span></span>     |
| <span data-ttu-id="88f7c-597">DEATH</span><span class="sxs-lookup"><span data-stu-id="88f7c-597">DEATH</span></span>                  | <span data-ttu-id="88f7c-598">死亡</span><span class="sxs-lookup"><span data-stu-id="88f7c-598">Death</span></span>                          | <span data-ttu-id="88f7c-599">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="88f7c-599">Terminate worker</span></span>     |
| <span data-ttu-id="88f7c-600">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="88f7c-600">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="88f7c-601">休假</span><span class="sxs-lookup"><span data-stu-id="88f7c-601">Leave of Absence</span></span>               | <span data-ttu-id="88f7c-602">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="88f7c-602">Terminate worker</span></span>     |
| <span data-ttu-id="88f7c-603">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="88f7c-603">CONTRACTEND</span></span>            | <span data-ttu-id="88f7c-604">合同结束</span><span class="sxs-lookup"><span data-stu-id="88f7c-604">End of Contract</span></span>                | <span data-ttu-id="88f7c-605">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="88f7c-605">Terminate worker</span></span>     |
| <span data-ttu-id="88f7c-606">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="88f7c-606">SALARYCHANGE</span></span>           | <span data-ttu-id="88f7c-607">工资改变</span><span class="sxs-lookup"><span data-stu-id="88f7c-607">Change of Salary</span></span>               | <span data-ttu-id="88f7c-608">薪酬</span><span class="sxs-lookup"><span data-stu-id="88f7c-608">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="88f7c-609">雇用条款</span><span class="sxs-lookup"><span data-stu-id="88f7c-609">Terms of employment</span></span>

<span data-ttu-id="88f7c-610">雇用条款用于创建雇用条款的类别。</span><span class="sxs-lookup"><span data-stu-id="88f7c-610">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="88f7c-611">这些条款作为雇用指标值映射到 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="88f7c-611">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="88f7c-612">需要以下雇用条款和描述。</span><span class="sxs-lookup"><span data-stu-id="88f7c-612">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="88f7c-613">雇用条款</span><span class="sxs-lookup"><span data-stu-id="88f7c-613">Terms of employment</span></span>   | <span data-ttu-id="88f7c-614">说明</span><span class="sxs-lookup"><span data-stu-id="88f7c-614">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="88f7c-615">常规</span><span class="sxs-lookup"><span data-stu-id="88f7c-615">Regular</span></span>               | <span data-ttu-id="88f7c-616">常规</span><span class="sxs-lookup"><span data-stu-id="88f7c-616">Regular</span></span>     |
| <span data-ttu-id="88f7c-617">直接</span><span class="sxs-lookup"><span data-stu-id="88f7c-617">Direct</span></span>                | <span data-ttu-id="88f7c-618">直接</span><span class="sxs-lookup"><span data-stu-id="88f7c-618">Direct</span></span>      |
| <span data-ttu-id="88f7c-619">实习</span><span class="sxs-lookup"><span data-stu-id="88f7c-619">Internship</span></span>            | <span data-ttu-id="88f7c-620">实习</span><span class="sxs-lookup"><span data-stu-id="88f7c-620">Internship</span></span>  |
| <span data-ttu-id="88f7c-621">永久</span><span class="sxs-lookup"><span data-stu-id="88f7c-621">Permanent</span></span>             | <span data-ttu-id="88f7c-622">永久</span><span class="sxs-lookup"><span data-stu-id="88f7c-622">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="88f7c-623">婚姻状况</span><span class="sxs-lookup"><span data-stu-id="88f7c-623">Marital status</span></span>

<span data-ttu-id="88f7c-624">婚姻状态值映射到 Dayforce，并在集成时根据需要转换为接受的值。</span><span class="sxs-lookup"><span data-stu-id="88f7c-624">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="88f7c-625">下表显示婚姻状态值如何映射到 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="88f7c-625">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="88f7c-626">人力资源</span><span class="sxs-lookup"><span data-stu-id="88f7c-626">Human Resources</span></span>                 | <span data-ttu-id="88f7c-627">Dayforce</span><span class="sxs-lookup"><span data-stu-id="88f7c-627">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="88f7c-628">已婚</span><span class="sxs-lookup"><span data-stu-id="88f7c-628">Married</span></span>                | <span data-ttu-id="88f7c-629">已婚</span><span class="sxs-lookup"><span data-stu-id="88f7c-629">Married</span></span>                   |
| <span data-ttu-id="88f7c-630">单一</span><span class="sxs-lookup"><span data-stu-id="88f7c-630">Single</span></span>                 | <span data-ttu-id="88f7c-631">单一</span><span class="sxs-lookup"><span data-stu-id="88f7c-631">Single</span></span>                    |
| <span data-ttu-id="88f7c-632">丧偶</span><span class="sxs-lookup"><span data-stu-id="88f7c-632">Widowed</span></span>                | <span data-ttu-id="88f7c-633">丧偶</span><span class="sxs-lookup"><span data-stu-id="88f7c-633">Widowed</span></span>                   |
| <span data-ttu-id="88f7c-634">离婚</span><span class="sxs-lookup"><span data-stu-id="88f7c-634">Divorced</span></span>               | <span data-ttu-id="88f7c-635">离异</span><span class="sxs-lookup"><span data-stu-id="88f7c-635">Divorced</span></span>                  |
| <span data-ttu-id="88f7c-636">注册伴侣关系</span><span class="sxs-lookup"><span data-stu-id="88f7c-636">Registered Partnership</span></span> | <span data-ttu-id="88f7c-637">民事结合关系</span><span class="sxs-lookup"><span data-stu-id="88f7c-637">Domestic Partnership</span></span>      |
| <span data-ttu-id="88f7c-638">None</span><span class="sxs-lookup"><span data-stu-id="88f7c-638">None</span></span>                   | <span data-ttu-id="88f7c-639">*墨西哥不支持*</span><span class="sxs-lookup"><span data-stu-id="88f7c-639">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="88f7c-640">未婚同居</span><span class="sxs-lookup"><span data-stu-id="88f7c-640">Cohabiting</span></span>             | <span data-ttu-id="88f7c-641">*墨西哥不支持*</span><span class="sxs-lookup"><span data-stu-id="88f7c-641">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="88f7c-642">性</span><span class="sxs-lookup"><span data-stu-id="88f7c-642">Gender</span></span>

<span data-ttu-id="88f7c-643">性别指派映射到 Dayforce，并在集成时根据需要转换为接受的值。</span><span class="sxs-lookup"><span data-stu-id="88f7c-643">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="88f7c-644">下表显示性别指派如何映射到 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="88f7c-644">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="88f7c-645">人力资源</span><span class="sxs-lookup"><span data-stu-id="88f7c-645">Human Resources</span></span>       | <span data-ttu-id="88f7c-646">Dayforce</span><span class="sxs-lookup"><span data-stu-id="88f7c-646">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="88f7c-647">男</span><span class="sxs-lookup"><span data-stu-id="88f7c-647">Male</span></span>         | <span data-ttu-id="88f7c-648">男</span><span class="sxs-lookup"><span data-stu-id="88f7c-648">Male</span></span>                      |
| <span data-ttu-id="88f7c-649">女</span><span class="sxs-lookup"><span data-stu-id="88f7c-649">Female</span></span>       | <span data-ttu-id="88f7c-650">女</span><span class="sxs-lookup"><span data-stu-id="88f7c-650">Female</span></span>                    |
| <span data-ttu-id="88f7c-651">非特定</span><span class="sxs-lookup"><span data-stu-id="88f7c-651">Non-specific</span></span> | <span data-ttu-id="88f7c-652">*墨西哥不支持*</span><span class="sxs-lookup"><span data-stu-id="88f7c-652">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="88f7c-653">付款方式</span><span class="sxs-lookup"><span data-stu-id="88f7c-653">Payment method</span></span>

<span data-ttu-id="88f7c-654">付款方式为员工和公司提供描述如何向员工付款的方式。</span><span class="sxs-lookup"><span data-stu-id="88f7c-654">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="88f7c-655">付款方式映射到 Dayforce，并在集成时根据需要转换为接受的值。</span><span class="sxs-lookup"><span data-stu-id="88f7c-655">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="88f7c-656">下表显示付款方式如何映射到 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="88f7c-656">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="88f7c-657">人力资源</span><span class="sxs-lookup"><span data-stu-id="88f7c-657">Human Resources</span></span>             | <span data-ttu-id="88f7c-658">Dayforce</span><span class="sxs-lookup"><span data-stu-id="88f7c-658">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="88f7c-659">现金</span><span class="sxs-lookup"><span data-stu-id="88f7c-659">Cash</span></span>               | <span data-ttu-id="88f7c-660">现金</span><span class="sxs-lookup"><span data-stu-id="88f7c-660">Cash</span></span>                      |
| <span data-ttu-id="88f7c-661">电子支付</span><span class="sxs-lookup"><span data-stu-id="88f7c-661">Electronic Payment</span></span> | <span data-ttu-id="88f7c-662">转账</span><span class="sxs-lookup"><span data-stu-id="88f7c-662">Transfer</span></span>                  |
| <span data-ttu-id="88f7c-663">检查</span><span class="sxs-lookup"><span data-stu-id="88f7c-663">Check</span></span>              | <span data-ttu-id="88f7c-664">支票</span><span class="sxs-lookup"><span data-stu-id="88f7c-664">Cheque</span></span>                    |
| <span data-ttu-id="88f7c-665">银行汇票</span><span class="sxs-lookup"><span data-stu-id="88f7c-665">Bank Draft</span></span>         | <span data-ttu-id="88f7c-666">*墨西哥不支持*</span><span class="sxs-lookup"><span data-stu-id="88f7c-666">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="88f7c-667">其他</span><span class="sxs-lookup"><span data-stu-id="88f7c-667">Other</span></span>              | <span data-ttu-id="88f7c-668">*墨西哥不支持*</span><span class="sxs-lookup"><span data-stu-id="88f7c-668">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="88f7c-669">银行帐户类型</span><span class="sxs-lookup"><span data-stu-id="88f7c-669">Bank account type</span></span>

<span data-ttu-id="88f7c-670">银行帐户类型用于对员工进行电子付款。</span><span class="sxs-lookup"><span data-stu-id="88f7c-670">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="88f7c-671">银行账户类型作为转帐信息映射到 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="88f7c-671">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="88f7c-672">集成时，银行帐户类型根据需要转换为接受的值。</span><span class="sxs-lookup"><span data-stu-id="88f7c-672">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="88f7c-673">人力资源</span><span class="sxs-lookup"><span data-stu-id="88f7c-673">Human Resources</span></span>            | <span data-ttu-id="88f7c-674">Dayforce</span><span class="sxs-lookup"><span data-stu-id="88f7c-674">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="88f7c-675">支票帐户</span><span class="sxs-lookup"><span data-stu-id="88f7c-675">Checking Account</span></span>  | <span data-ttu-id="88f7c-676">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="88f7c-676">CheckingAccount</span></span>           |
| <span data-ttu-id="88f7c-677">工资单帐户</span><span class="sxs-lookup"><span data-stu-id="88f7c-677">Payroll Account</span></span>   | <span data-ttu-id="88f7c-678">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="88f7c-678">PayrollAccount</span></span>            |
| <span data-ttu-id="88f7c-679">储蓄帐户</span><span class="sxs-lookup"><span data-stu-id="88f7c-679">Savings Account</span></span>   | <span data-ttu-id="88f7c-680">*墨西哥不支持*</span><span class="sxs-lookup"><span data-stu-id="88f7c-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="88f7c-681">BankGirot 帐户</span><span class="sxs-lookup"><span data-stu-id="88f7c-681">BankGirot account</span></span> | <span data-ttu-id="88f7c-682">*墨西哥不支持*</span><span class="sxs-lookup"><span data-stu-id="88f7c-682">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="88f7c-683">PlusGirot 帐户</span><span class="sxs-lookup"><span data-stu-id="88f7c-683">PlusGirot account</span></span> | <span data-ttu-id="88f7c-684">*墨西哥不支持*</span><span class="sxs-lookup"><span data-stu-id="88f7c-684">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="88f7c-685">收入代码</span><span class="sxs-lookup"><span data-stu-id="88f7c-685">Earning codes</span></span>

<span data-ttu-id="88f7c-686">收入代码唯一标识工作人员获得的每种收入类型。</span><span class="sxs-lookup"><span data-stu-id="88f7c-686">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="88f7c-687">这些代码有多个与收入有关的参数，如会计规则、税法、报告要求和补偿费功能。</span><span class="sxs-lookup"><span data-stu-id="88f7c-687">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="88f7c-688">如果使用不受支持的频率，默认将使用 **每个付薪** 频率进行计算。</span><span class="sxs-lookup"><span data-stu-id="88f7c-688">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="88f7c-689">支持的频率</span><span class="sxs-lookup"><span data-stu-id="88f7c-689">Supported frequencies</span></span>

- <span data-ttu-id="88f7c-690">所有</span><span class="sxs-lookup"><span data-stu-id="88f7c-690">All</span></span>
- <span data-ttu-id="88f7c-691">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="88f7c-691">EVERYPAY</span></span>
- <span data-ttu-id="88f7c-692">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="88f7c-692">EACHPAYPERIOD</span></span>
- <span data-ttu-id="88f7c-693">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="88f7c-693">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="88f7c-694">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="88f7c-694">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="88f7c-695">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="88f7c-695">1OFMTH</span></span>
- <span data-ttu-id="88f7c-696">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="88f7c-696">LASTOFMTH</span></span>
- <span data-ttu-id="88f7c-697">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="88f7c-697">2OFMTH</span></span>
- <span data-ttu-id="88f7c-698">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="88f7c-698">3OFMTH</span></span>
- <span data-ttu-id="88f7c-699">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="88f7c-699">4OFMTH</span></span>
- <span data-ttu-id="88f7c-700">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="88f7c-700">5OFMTH</span></span>
- <span data-ttu-id="88f7c-701">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="88f7c-701">1N2OFMTH</span></span>
- <span data-ttu-id="88f7c-702">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="88f7c-702">3N4OFMTH</span></span>
- <span data-ttu-id="88f7c-703">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="88f7c-703">1N3OFMTH</span></span>
- <span data-ttu-id="88f7c-704">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="88f7c-704">1N4OFMTH</span></span>
- <span data-ttu-id="88f7c-705">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="88f7c-705">2N3OFMTH</span></span>
- <span data-ttu-id="88f7c-706">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="88f7c-706">2N4OFMTH</span></span>
- <span data-ttu-id="88f7c-707">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="88f7c-707">1N2N3OFMTH</span></span>
- <span data-ttu-id="88f7c-708">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="88f7c-708">1N2N4OFMTH</span></span>
- <span data-ttu-id="88f7c-709">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="88f7c-709">1N3N4OFMTH</span></span>
- <span data-ttu-id="88f7c-710">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="88f7c-710">2N3N4OFMTH</span></span>
- <span data-ttu-id="88f7c-711">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="88f7c-711">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="88f7c-712">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="88f7c-712">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="88f7c-713">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="88f7c-713">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="88f7c-714">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="88f7c-714">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="88f7c-715">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="88f7c-715">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="88f7c-716">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="88f7c-716">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="88f7c-717">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="88f7c-717">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="88f7c-718">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="88f7c-718">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="88f7c-719">地址</span><span class="sxs-lookup"><span data-stu-id="88f7c-719">Addresses</span></span>

<span data-ttu-id="88f7c-720">特定国家或地区、省/直辖市/自治区和县/市（自治市）代码的标识需要 Dayforce 和国内/地区内提供商可识别的特定格式。</span><span class="sxs-lookup"><span data-stu-id="88f7c-720">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="88f7c-721">尽管县/市的格式可变，但是每个县/市必须与一个省/直辖市/自治区关联。</span><span class="sxs-lookup"><span data-stu-id="88f7c-721">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="88f7c-722">人力资源</span><span class="sxs-lookup"><span data-stu-id="88f7c-722">Human Resources</span></span>              | <span data-ttu-id="88f7c-723">Dayforce</span><span class="sxs-lookup"><span data-stu-id="88f7c-723">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="88f7c-724">国家/地区</span><span class="sxs-lookup"><span data-stu-id="88f7c-724">Country/Region</span></span>      | <span data-ttu-id="88f7c-725">国家/地区代码</span><span class="sxs-lookup"><span data-stu-id="88f7c-725">Country Code</span></span>          |
| <span data-ttu-id="88f7c-726">邮政编码 </span><span class="sxs-lookup"><span data-stu-id="88f7c-726">Zip/Postal Code</span></span>     | <span data-ttu-id="88f7c-727">邮政编码</span><span class="sxs-lookup"><span data-stu-id="88f7c-727">Postal Code</span></span>           |
| <span data-ttu-id="88f7c-728">状态</span><span class="sxs-lookup"><span data-stu-id="88f7c-728">State</span></span>               | <span data-ttu-id="88f7c-729">省/直辖市/自治区代码</span><span class="sxs-lookup"><span data-stu-id="88f7c-729">State Code</span></span>            |
| <span data-ttu-id="88f7c-730">城市</span><span class="sxs-lookup"><span data-stu-id="88f7c-730">City</span></span>                | <span data-ttu-id="88f7c-731">城市</span><span class="sxs-lookup"><span data-stu-id="88f7c-731">City</span></span>                  |
| <span data-ttu-id="88f7c-732">县</span><span class="sxs-lookup"><span data-stu-id="88f7c-732">County</span></span>              | <span data-ttu-id="88f7c-733">县（自治市）</span><span class="sxs-lookup"><span data-stu-id="88f7c-733">County (Municipality)</span></span> |
| <span data-ttu-id="88f7c-734">街道</span><span class="sxs-lookup"><span data-stu-id="88f7c-734">Street</span></span>              | <span data-ttu-id="88f7c-735">地址行 1</span><span class="sxs-lookup"><span data-stu-id="88f7c-735">Address Line 1</span></span>        |
| <span data-ttu-id="88f7c-736">街道编号</span><span class="sxs-lookup"><span data-stu-id="88f7c-736">Street Number</span></span>       | <span data-ttu-id="88f7c-737">地址行 2</span><span class="sxs-lookup"><span data-stu-id="88f7c-737">Address Line 2</span></span>        |
| <span data-ttu-id="88f7c-738">建筑物地址</span><span class="sxs-lookup"><span data-stu-id="88f7c-738">Building Complement</span></span> | <span data-ttu-id="88f7c-739">地址行 5</span><span class="sxs-lookup"><span data-stu-id="88f7c-739">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="88f7c-740">护照号</span><span class="sxs-lookup"><span data-stu-id="88f7c-740">Passport number</span></span>

<span data-ttu-id="88f7c-741">员工可以声明护照信息。</span><span class="sxs-lookup"><span data-stu-id="88f7c-741">Employees can declare passport information.</span></span> <span data-ttu-id="88f7c-742">此信息的身份证明类型为 **护照**，并作为员工的墨西哥特定信息的一部分集成到 Dayforce 中。</span><span class="sxs-lookup"><span data-stu-id="88f7c-742">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="88f7c-743">身份证明类型 =“护照”</span><span class="sxs-lookup"><span data-stu-id="88f7c-743">Identification Type = "Passport"</span></span>
- <span data-ttu-id="88f7c-744">签发日期</span><span class="sxs-lookup"><span data-stu-id="88f7c-744">Issued Date</span></span>
- <span data-ttu-id="88f7c-745">到期日期</span><span class="sxs-lookup"><span data-stu-id="88f7c-745">Expiration Date</span></span>

<span data-ttu-id="88f7c-746">员工可以声明 **护照** 身份证明类型的多个身份证明编号。</span><span class="sxs-lookup"><span data-stu-id="88f7c-746">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="88f7c-747">但是，仅将当前有效的护照条目集成到 Dayforce 中。</span><span class="sxs-lookup"><span data-stu-id="88f7c-747">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="88f7c-748">如果所有护照条目均已过期，将把最近签发的护照集成到 Dayforce 中。</span><span class="sxs-lookup"><span data-stu-id="88f7c-748">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
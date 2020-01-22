---
title: 配置 Talent 与 Dayforce 之间的工资单集成
description: 本主题说明如何配置 Microsoft Dynamics 365 Talent 与 Ceridian Dayforce 之间的集成，以便处理付薪。
author: andreabichsel
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 075b2bdfa08bb190f66b6d60074e1263feedcf70
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898519"
---
# <a name="configure-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="c7d8b-103">配置 Talent 和 Dayforce 之间的工资单集成</span><span class="sxs-lookup"><span data-stu-id="c7d8b-103">Configure payroll integration between Talent and Dayforce</span></span>

<span data-ttu-id="c7d8b-104">Microsoft Dynamics 365 Talent 与 Ceridian Dayforce 之间的集成依赖于本主题中介绍的几个配置步骤。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-104">The integration between Microsoft Dynamics 365 Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="c7d8b-105">必须先在 Talent 和 Dayforce 中配置集成，才能处理付薪。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="c7d8b-106">使用 Dayforce 之类服务完成付薪时，必须在 Talent 中启用集成。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="c7d8b-107">此集成需要来自 Talent 的特定数据。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="c7d8b-108">因此，必须验证已按照支持集成的方式在 Talent 中配置了映射到 Dayforce 的数据。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="c7d8b-109">此集成使用下面的各种数据类别：</span><span class="sxs-lookup"><span data-stu-id="c7d8b-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="c7d8b-110">人力资源数据</span><span class="sxs-lookup"><span data-stu-id="c7d8b-110">Human resources data</span></span>
- <span data-ttu-id="c7d8b-111">薪酬数据</span><span class="sxs-lookup"><span data-stu-id="c7d8b-111">Compensation data</span></span>
- <span data-ttu-id="c7d8b-112">工资单数据，如付薪周期、付薪期间和收入代码</span><span class="sxs-lookup"><span data-stu-id="c7d8b-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="c7d8b-113">工作人员数据</span><span class="sxs-lookup"><span data-stu-id="c7d8b-113">Worker data</span></span>

<span data-ttu-id="c7d8b-114">此主题介绍要启用集成必须执行的步骤。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="c7d8b-115">还介绍了集成所需的数据类型和配置详细信息。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="c7d8b-116">启用集成</span><span class="sxs-lookup"><span data-stu-id="c7d8b-116">Enable the integration</span></span>

<span data-ttu-id="c7d8b-117">在 Talent 中，必须开启集成并输入配置信息，才能连接到 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="c7d8b-118">如果要将生成的总帐交易记录导入 Microsoft Dynamics 365 Finance 中，还必须在 Finance 中设置 Microsoft Azure 存储帐户和输入 Azure Storage 连接字符串。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="c7d8b-119">要在 Talent 中开启集成，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="c7d8b-120">在**系统管理**页中，选择 **集成配置**。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="c7d8b-121">输入安全文件传输协议 (FTP) 终结点和安全 FTP 文件夹路径。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="c7d8b-122">输入将访问安全 FTP 终结点和文件夹路径的用户的用户名和密码。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="c7d8b-123">根据需要测试连接，然后将**启用工资单集成**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="c7d8b-124">开启集成后，将创建数据导出包和文件，并设置频率。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="c7d8b-125">可根据需要更改此频率。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="c7d8b-126">有关 Azure ML 存储帐户和 Azure 存储连接字符串的详细信息，请参阅以下 Azure ML 主题：</span><span class="sxs-lookup"><span data-stu-id="c7d8b-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="c7d8b-127">关于 Azure 存储帐户</span><span class="sxs-lookup"><span data-stu-id="c7d8b-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="c7d8b-128">配置 Azure 存储连接字符串</span><span class="sxs-lookup"><span data-stu-id="c7d8b-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="c7d8b-129">启用工资单集成后的技术详细信息</span><span class="sxs-lookup"><span data-stu-id="c7d8b-129">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="c7d8b-130">开启工资单集成有两大效果：</span><span class="sxs-lookup"><span data-stu-id="c7d8b-130">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="c7d8b-131">创建一个名称为“工资单集成导出”的数据导出项目。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-131">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="c7d8b-132">此项目中包含工资单集成需要的实体和字段。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-132">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="c7d8b-133">若要检查此项目，请转到**系统管理**，选择**数据管理**磁贴，然后从项目列表打开数据项目。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-133">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="c7d8b-134">此批处理作业执行数据导出项目，加密生成的数据包，然后将数据包文件传输到**集成配置**屏幕上配置的 SFTP 终结点。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-134">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="c7d8b-135">将使用数据包的唯一密钥加密传输到 SFTP 终结点的数据包。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-135">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="c7d8b-136">此密钥位于只有 Ceridian 才能访问的 Azure 密钥保管库。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-136">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="c7d8b-137">不能解密和检查数据包内容。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-137">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="c7d8b-138">如果需要检查数据包的内容，需要手动导出“工资单集成导出”数据终结点，下载，然后打开。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-138">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="c7d8b-139">手动导出不会应用加密或传输包。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-139">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="c7d8b-140">配置数据</span><span class="sxs-lookup"><span data-stu-id="c7d8b-140">Configure your data</span></span> 

<span data-ttu-id="c7d8b-141">要处理工资单，必须在 Talent 中配置人力资源数据。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-141">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="c7d8b-142">必须设置组织数据（如工作和职位），以及福利和薪酬信息。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-142">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="c7d8b-143">这些信息提供生成员工付薪所需雇用、付薪和扣缴信息。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-143">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="c7d8b-144">人力资源数据</span><span class="sxs-lookup"><span data-stu-id="c7d8b-144">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="c7d8b-145">福利</span><span class="sxs-lookup"><span data-stu-id="c7d8b-145">Benefits</span></span> 

<span data-ttu-id="c7d8b-146">人力资源提供工具，用于设置和维护组织提供或为其工作人员处理的福利、扣缴和工作人员薪酬计划。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-146">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="c7d8b-147">创建福利时，请注意 Dayforce 中使用的以下数据和配置。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-147">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="c7d8b-148">福利计划</span><span class="sxs-lookup"><span data-stu-id="c7d8b-148">Benefit plans</span></span>

- <span data-ttu-id="c7d8b-149">计划（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-149">Plan (required)</span></span>
- <span data-ttu-id="c7d8b-150">类型（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-150">Type (required)</span></span>
- <span data-ttu-id="c7d8b-151">工资单影响（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-151">Payroll impact (required)</span></span>
- <span data-ttu-id="c7d8b-152">恢复欠款</span><span class="sxs-lookup"><span data-stu-id="c7d8b-152">Recover arrears</span></span>
- <span data-ttu-id="c7d8b-153">扣除方法</span><span class="sxs-lookup"><span data-stu-id="c7d8b-153">Deduction method</span></span>
- <span data-ttu-id="c7d8b-154">扣除优先级</span><span class="sxs-lookup"><span data-stu-id="c7d8b-154">Deduction priority</span></span>
- <span data-ttu-id="c7d8b-155">限制期</span><span class="sxs-lookup"><span data-stu-id="c7d8b-155">Limit period</span></span>
- <span data-ttu-id="c7d8b-156">限额</span><span class="sxs-lookup"><span data-stu-id="c7d8b-156">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="c7d8b-157">福利</span><span class="sxs-lookup"><span data-stu-id="c7d8b-157">Benefits</span></span>

- <span data-ttu-id="c7d8b-158">计划（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-158">Plan (required)</span></span>
- <span data-ttu-id="c7d8b-159">类型（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-159">Type (required)</span></span>
- <span data-ttu-id="c7d8b-160">选项（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-160">Option (required)</span></span>
- <span data-ttu-id="c7d8b-161">福利 ID（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-161">Benefit ID (required)</span></span>
- <span data-ttu-id="c7d8b-162">频率</span><span class="sxs-lookup"><span data-stu-id="c7d8b-162">Frequency</span></span>
- <span data-ttu-id="c7d8b-163">基础</span><span class="sxs-lookup"><span data-stu-id="c7d8b-163">Basis</span></span>
- <span data-ttu-id="c7d8b-164">金额或费率</span><span class="sxs-lookup"><span data-stu-id="c7d8b-164">Amount or rate</span></span>
- <span data-ttu-id="c7d8b-165">收入代码</span><span class="sxs-lookup"><span data-stu-id="c7d8b-165">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="c7d8b-166">支持的频率</span><span class="sxs-lookup"><span data-stu-id="c7d8b-166">Supported frequencies</span></span> 

- <span data-ttu-id="c7d8b-167">每周</span><span class="sxs-lookup"><span data-stu-id="c7d8b-167">Weekly</span></span>
- <span data-ttu-id="c7d8b-168">两周一次</span><span class="sxs-lookup"><span data-stu-id="c7d8b-168">Bi-weekly</span></span>
- <span data-ttu-id="c7d8b-169">每半月</span><span class="sxs-lookup"><span data-stu-id="c7d8b-169">Semi-monthly</span></span>
- <span data-ttu-id="c7d8b-170">每月</span><span class="sxs-lookup"><span data-stu-id="c7d8b-170">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="c7d8b-171">支持的库</span><span class="sxs-lookup"><span data-stu-id="c7d8b-171">Supported bases</span></span> 

- <span data-ttu-id="c7d8b-172">固定金额</span><span class="sxs-lookup"><span data-stu-id="c7d8b-172">Fixed amount</span></span>
- <span data-ttu-id="c7d8b-173">收入百分比</span><span class="sxs-lookup"><span data-stu-id="c7d8b-173">Percent of earnings</span></span>
- <span data-ttu-id="c7d8b-174">工作时数</span><span class="sxs-lookup"><span data-stu-id="c7d8b-174">Productive hours</span></span>

<span data-ttu-id="c7d8b-175">Dayforce 根据福利计划中定义的工资单影响创建以下扣缴。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-175">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="c7d8b-176">Talent 中的选择</span><span class="sxs-lookup"><span data-stu-id="c7d8b-176">Selection in Talent</span></span>        | <span data-ttu-id="c7d8b-177">Dayforce 中的结果</span><span class="sxs-lookup"><span data-stu-id="c7d8b-177">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="c7d8b-178">None</span><span class="sxs-lookup"><span data-stu-id="c7d8b-178">None</span></span>                       | <span data-ttu-id="c7d8b-179">不创建扣缴。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-179">No deduction is created.</span></span>                      |
| <span data-ttu-id="c7d8b-180">仅扣除</span><span class="sxs-lookup"><span data-stu-id="c7d8b-180">Deduction only</span></span>             | <span data-ttu-id="c7d8b-181">创建员工扣缴。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-181">An employee deduction is created.</span></span>             |
| <span data-ttu-id="c7d8b-182">仅缴纳</span><span class="sxs-lookup"><span data-stu-id="c7d8b-182">Contribution only</span></span>          | <span data-ttu-id="c7d8b-183">创建雇主扣缴。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-183">An employer deduction is created.</span></span>             |
| <span data-ttu-id="c7d8b-184">扣除和缴纳</span><span class="sxs-lookup"><span data-stu-id="c7d8b-184">Deduction and contribution</span></span> | <span data-ttu-id="c7d8b-185">创建员工扣缴和雇主扣缴。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-185">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="c7d8b-186">有关如何定义和管理福利计划的详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="c7d8b-186">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="c7d8b-187">交付员工福利计划</span><span class="sxs-lookup"><span data-stu-id="c7d8b-187">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="c7d8b-188">创建新福利</span><span class="sxs-lookup"><span data-stu-id="c7d8b-188">Create a new benefit</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="c7d8b-189">定义福利资格规则和策略</span><span class="sxs-lookup"><span data-stu-id="c7d8b-189">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="c7d8b-190">登记和删除工作人员的福利</span><span class="sxs-lookup"><span data-stu-id="c7d8b-190">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="c7d8b-191">薪酬</span><span class="sxs-lookup"><span data-stu-id="c7d8b-191">Compensation</span></span> 

<span data-ttu-id="c7d8b-192">薪酬管理用于控制基本工资和奖励的发放。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-192">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="c7d8b-193">员工的固定基本工资和业绩调薪是通过固定薪酬计划控制的。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-193">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="c7d8b-194">激励性的付款，例如额外津贴、绩效奖、股票期权和赠与以及一次性奖励，是通过可变薪酬计划控制的。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-194">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="c7d8b-195">Dayforce 使用薪酬信息计算员工的时薪或年薪。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-195">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="c7d8b-196">需要固定薪酬计划和付薪比率转换。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-196">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="c7d8b-197">必须将员工与固定薪酬计划关联。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-197">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="c7d8b-198">有关薪酬计划的详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="c7d8b-198">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="c7d8b-199">创建固定薪酬计划</span><span class="sxs-lookup"><span data-stu-id="c7d8b-199">Create fixed compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="c7d8b-200">创建可变薪酬计划</span><span class="sxs-lookup"><span data-stu-id="c7d8b-200">Create variable compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="c7d8b-201">制订薪水/薪酬结构和计划</span><span class="sxs-lookup"><span data-stu-id="c7d8b-201">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="c7d8b-202">薪酬流程</span><span class="sxs-lookup"><span data-stu-id="c7d8b-202">Process compensation</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="c7d8b-203">定义薪酬流程并计算结果</span><span class="sxs-lookup"><span data-stu-id="c7d8b-203">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="c7d8b-204">在固定薪酬计划中登记员工</span><span class="sxs-lookup"><span data-stu-id="c7d8b-204">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="c7d8b-205">在可变薪酬计划中登记员工</span><span class="sxs-lookup"><span data-stu-id="c7d8b-205">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="c7d8b-206">工作</span><span class="sxs-lookup"><span data-stu-id="c7d8b-206">Jobs</span></span> 

<span data-ttu-id="c7d8b-207">作业是执行作业的人员需要承担的任务和责任的集合。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-207">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="c7d8b-208">有关详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="c7d8b-208">For more information, see the following topics:</span></span>

- [<span data-ttu-id="c7d8b-209">设置作业组件</span><span class="sxs-lookup"><span data-stu-id="c7d8b-209">Setting up the components of a job</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="c7d8b-210">定义新工作</span><span class="sxs-lookup"><span data-stu-id="c7d8b-210">Define new jobs</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="c7d8b-211">职位</span><span class="sxs-lookup"><span data-stu-id="c7d8b-211">Positions</span></span>

<span data-ttu-id="c7d8b-212">位置是工作的单个实例。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-212">A position is an individual instance of a job.</span></span> <span data-ttu-id="c7d8b-213">例如，“销售经理（东部）”职位是与“销售经理”工作关联的职位。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-213">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="c7d8b-214">职位存在于部门中。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-214">A position exists in a department.</span></span> <span data-ttu-id="c7d8b-215">每个职位只能与一个工作人员关联。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-215">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="c7d8b-216">设置职位时，请注意以下数据和配置：</span><span class="sxs-lookup"><span data-stu-id="c7d8b-216">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="c7d8b-217">职位（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-217">Position (required)</span></span>
- <span data-ttu-id="c7d8b-218">描述（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-218">Description (required)</span></span>
- <span data-ttu-id="c7d8b-219">工作（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-219">Job (required)</span></span>
- <span data-ttu-id="c7d8b-220">部门（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-220">Department (required)</span></span>
- <span data-ttu-id="c7d8b-221">职位类型（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-221">Position type (required)</span></span>
- <span data-ttu-id="c7d8b-222">全职等价</span><span class="sxs-lookup"><span data-stu-id="c7d8b-222">Full-time equivalent</span></span>
- <span data-ttu-id="c7d8b-223">年度常规时间（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-223">Annual regular hours (required)</span></span>
- <span data-ttu-id="c7d8b-224">由法人支付（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-224">Paid by legal entity (required)</span></span>
- <span data-ttu-id="c7d8b-225">付薪周期（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-225">Pay cycle (required)</span></span>
- <span data-ttu-id="c7d8b-226">默认财务维度 – 成本中心（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-226">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="c7d8b-227">工作人员分配 – 工作人员、分配开始时间、分配结束时间、原因代码</span><span class="sxs-lookup"><span data-stu-id="c7d8b-227">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="c7d8b-228">如果同一个部门中多个职位与同一个工作关联，应在 Dayforce 中将这些职位合并为一个位置。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-228">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="c7d8b-229">有关详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="c7d8b-229">For more information, see the following topics:</span></span>

- [<span data-ttu-id="c7d8b-230">使用部门、工作和职位组织您的劳动力</span><span class="sxs-lookup"><span data-stu-id="c7d8b-230">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="c7d8b-231">设置职位</span><span class="sxs-lookup"><span data-stu-id="c7d8b-231">Set up positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="c7d8b-232">部门</span><span class="sxs-lookup"><span data-stu-id="c7d8b-232">Departments</span></span>

<span data-ttu-id="c7d8b-233">部门是一个运营单位，表示组织的类别或功能区域。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-233">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="c7d8b-234">部门负责组织的特定区域，例如，销售、会计或人力资源。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-234">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="c7d8b-235">您可以在功能区中使用要上报的部门。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-235">You can use departments to report on functional areas.</span></span> <span data-ttu-id="c7d8b-236">部门可能具有损益职责。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-236">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="c7d8b-237">有关详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="c7d8b-237">For more information, see the following topics:</span></span>

- [<span data-ttu-id="c7d8b-238">创建一个部门并将其与部门层次结构关联</span><span class="sxs-lookup"><span data-stu-id="c7d8b-238">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="c7d8b-239">定义新部门</span><span class="sxs-lookup"><span data-stu-id="c7d8b-239">Define new departments</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="c7d8b-240">付薪周期和付薪期间</span><span class="sxs-lookup"><span data-stu-id="c7d8b-240">Pay cycles and pay periods</span></span>

<span data-ttu-id="c7d8b-241">付薪周期确定付薪的频率和工作人员获薪的具体天数。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-241">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="c7d8b-242">例如，付薪周期可以是每月，并且可能在月末向员工付薪。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-242">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="c7d8b-243">付薪周期也可以是每周，并且可能在付薪期间结束后的星期二向员工付薪。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-243">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="c7d8b-244">为职位分配付薪周期是为了控制何时向所在职位的工作人员付薪。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-244">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="c7d8b-245">创建付薪周期后，可以为每个周期生成付薪期间。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-245">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="c7d8b-246">每个付薪期间包含一个基于您提供的信息的默认付薪日期。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-246">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="c7d8b-247">但是，可以更改付薪期间中的默认付薪日期，以便应对异常，如付薪日期在假期中。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-247">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="c7d8b-248">Dayforce 中使用以下信息：</span><span class="sxs-lookup"><span data-stu-id="c7d8b-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="c7d8b-249">付薪周期（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-249">Pay cycle (required)</span></span>
- <span data-ttu-id="c7d8b-250">付薪周期频率（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-250">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="c7d8b-251">期间开始日期（需要第一个付薪期间）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-251">Period start date (first pay period required)</span></span>
- <span data-ttu-id="c7d8b-252">默认付薪日期（需要第一个付薪期间）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-252">Default payment date (first pay period required)</span></span>

<span data-ttu-id="c7d8b-253">此信息与 Dayforce 集成为付薪组，并按各付薪周期的国家或地区分隔。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-253">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="c7d8b-254">集成之前，必须至少生成一个付薪期间。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-254">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="c7d8b-255">Dayforce 根据 Talent 中设置的第一个付薪期间的开始日期和默认付薪日期生成付薪组日历和付薪日期。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-255">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="c7d8b-256">收入代码</span><span class="sxs-lookup"><span data-stu-id="c7d8b-256">Earning codes</span></span>

<span data-ttu-id="c7d8b-257">收入代码唯一标识工作人员获得的每种收入类型。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-257">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="c7d8b-258">这些代码有多个与收入有关的参数，如会计规则、税法、报告要求和补偿费功能。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-258">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="c7d8b-259">Dayforce 中使用以下信息：</span><span class="sxs-lookup"><span data-stu-id="c7d8b-259">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="c7d8b-260">收入代码（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-260">Earning Code (required)</span></span>
- <span data-ttu-id="c7d8b-261">说明</span><span class="sxs-lookup"><span data-stu-id="c7d8b-261">Description</span></span>
- <span data-ttu-id="c7d8b-262">度量单位</span><span class="sxs-lookup"><span data-stu-id="c7d8b-262">Unit of measure</span></span>
- <span data-ttu-id="c7d8b-263">生产</span><span class="sxs-lookup"><span data-stu-id="c7d8b-263">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="c7d8b-264">工作人员数据</span><span class="sxs-lookup"><span data-stu-id="c7d8b-264">Worker data</span></span>

<span data-ttu-id="c7d8b-265">工作人员的对您的人力资源和工资系统十分重要的不同类型的记录。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-265">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="c7d8b-266">您输入的信息可用于跟踪工作人员和个人信息。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-266">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="c7d8b-267">您可以维护工作人员的以下信息:</span><span class="sxs-lookup"><span data-stu-id="c7d8b-267">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="c7d8b-268">**基本** – 维护有关工作人员的基本信息，如联系人信息、人口统计的信息、标识信息、系列信息、状态、兵役迁移国外的信息和个人和紧急事件联系人。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-268">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="c7d8b-269">**雇用** – 维护有关工作人员雇用情况的信息，例如公司或组织隶属关系、职位分配、开始日期和结束日期、工作的雇用资格、条款，退休金、假期和重定位信息。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-269">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="c7d8b-270">**休假和缺勤** – 维护有关工作人员的缺勤的信息，例如工作日历、缺勤事务和缺勤设置。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-270">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="c7d8b-271">**薪酬和工资单** – 维护有关工作人员的薪酬计划和工资信息的信息，例如计划登记、证书、性能、佣金、税务信息、报废和薪金扣缴。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-271">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="c7d8b-272">输入工作人员信息时，请注意 Dayforce 中使用的以下数据和配置。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-272">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="c7d8b-273">一般信息</span><span class="sxs-lookup"><span data-stu-id="c7d8b-273">General information</span></span>

- <span data-ttu-id="c7d8b-274">人员编号（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-274">Personnel number (required)</span></span>
- <span data-ttu-id="c7d8b-275">名字(必填)</span><span class="sxs-lookup"><span data-stu-id="c7d8b-275">First name (required)</span></span>
- <span data-ttu-id="c7d8b-276">姓氏(必填)</span><span class="sxs-lookup"><span data-stu-id="c7d8b-276">Last name (required)</span></span>
- <span data-ttu-id="c7d8b-277">中间名</span><span class="sxs-lookup"><span data-stu-id="c7d8b-277">Middle name</span></span>
- <span data-ttu-id="c7d8b-278">受聘日期</span><span class="sxs-lookup"><span data-stu-id="c7d8b-278">Seniority date</span></span>
- <span data-ttu-id="c7d8b-279">称作</span><span class="sxs-lookup"><span data-stu-id="c7d8b-279">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="c7d8b-280">个人信息</span><span class="sxs-lookup"><span data-stu-id="c7d8b-280">Personal information</span></span>

- <span data-ttu-id="c7d8b-281">婚姻状况（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-281">Marital status (required)</span></span>
- <span data-ttu-id="c7d8b-282">出生日期（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-282">Birth date (required)</span></span>
- <span data-ttu-id="c7d8b-283">性别（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-283">Gender (required)</span></span>
- <span data-ttu-id="c7d8b-284">残疾人士</span><span class="sxs-lookup"><span data-stu-id="c7d8b-284">Person with disabilities</span></span>
- <span data-ttu-id="c7d8b-285">国籍的国家地区（仅适用于墨西哥）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-285">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="c7d8b-286">地址信息</span><span class="sxs-lookup"><span data-stu-id="c7d8b-286">Address information</span></span>

- <span data-ttu-id="c7d8b-287">主要（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-287">Primary (required)</span></span>
- <span data-ttu-id="c7d8b-288">国家/地区（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-288">Country/region (required)</span></span>
- <span data-ttu-id="c7d8b-289">邮政编码（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-289">Postal code (required)</span></span>
- <span data-ttu-id="c7d8b-290">街道编号（必填）（仅适用于墨西哥）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-290">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="c7d8b-291">建筑物地址（仅适用于墨西哥）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-291">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="c7d8b-292"> 市/县（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-292">City (required)</span></span>
- <span data-ttu-id="c7d8b-293">省/直辖市/自治区（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-293">State (required)</span></span>
- <span data-ttu-id="c7d8b-294">国家/地区（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-294">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="c7d8b-295">联系人信息</span><span class="sxs-lookup"><span data-stu-id="c7d8b-295">Contact information</span></span> 

- <span data-ttu-id="c7d8b-296">主要（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-296">Primary (required)</span></span>
- <span data-ttu-id="c7d8b-297">联系人号码（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-297">Contact number (required)</span></span>
- <span data-ttu-id="c7d8b-298">函授</span><span class="sxs-lookup"><span data-stu-id="c7d8b-298">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="c7d8b-299">工资信息和收入代码</span><span class="sxs-lookup"><span data-stu-id="c7d8b-299">Payroll information and earning codes</span></span>

<span data-ttu-id="c7d8b-300">可以按给定付薪频率为员工分配特定收入，而员工则可以具有首选付款方式。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-300">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="c7d8b-301">Dayforce 中使用以下字段确保使用这些首选项和设置。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-301">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="c7d8b-302">收入代码</span><span class="sxs-lookup"><span data-stu-id="c7d8b-302">Earning codes</span></span>

- <span data-ttu-id="c7d8b-303">职位（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-303">Position (required)</span></span>
- <span data-ttu-id="c7d8b-304">收入代码（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-304">Earning Code (required)</span></span>
- <span data-ttu-id="c7d8b-305">频率（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-305">Frequency (required)</span></span>
- <span data-ttu-id="c7d8b-306">金额（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-306">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="c7d8b-307">工资单信息</span><span class="sxs-lookup"><span data-stu-id="c7d8b-307">Payroll information</span></span>

- <span data-ttu-id="c7d8b-308">付款方式</span><span class="sxs-lookup"><span data-stu-id="c7d8b-308">Payment Method</span></span>
- <span data-ttu-id="c7d8b-309">经济区域（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-309">Economic Region (required)</span></span>
- <span data-ttu-id="c7d8b-310">员工福利 ID</span><span class="sxs-lookup"><span data-stu-id="c7d8b-310">Employee Benefits ID</span></span>
- <span data-ttu-id="c7d8b-311">国家/地区 ID 号（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-311">National ID Number (required)</span></span>
- <span data-ttu-id="c7d8b-312">兵役编号</span><span class="sxs-lookup"><span data-stu-id="c7d8b-312">Military Service Number</span></span>
- <span data-ttu-id="c7d8b-313">班次 ID（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-313">Shift ID (required)</span></span>
- <span data-ttu-id="c7d8b-314">税号（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-314">Tax Number (required)</span></span>
- <span data-ttu-id="c7d8b-315">工会 ID（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-315">Union ID (required)</span></span>
- <span data-ttu-id="c7d8b-316">工作日 ID（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-316">Work Day ID (required)</span></span>
- <span data-ttu-id="c7d8b-317">工作许可证编号</span><span class="sxs-lookup"><span data-stu-id="c7d8b-317">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="c7d8b-318">对于付款方式，墨西哥支持**现金**、**支票**（公司的实际支票）和**电子支付**。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-318">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="c7d8b-319">如果不指定付款方式，则默认使用 **支票**。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-319">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="c7d8b-320">雇用详细信息</span><span class="sxs-lookup"><span data-stu-id="c7d8b-320">Employment details</span></span>

<span data-ttu-id="c7d8b-321">在 Dayforce 中派生员工的入职、离职和重新入职状态时，雇用详细信息历史记录至关重要。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-321">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="c7d8b-322">Dayforce 一次仅支持一条活动雇用记录。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-322">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="c7d8b-323">雇用开始日期（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-323">Employment start date (required)</span></span>
- <span data-ttu-id="c7d8b-324">雇佣结束日期</span><span class="sxs-lookup"><span data-stu-id="c7d8b-324">Employment end date</span></span>
- <span data-ttu-id="c7d8b-325">入职日期</span><span class="sxs-lookup"><span data-stu-id="c7d8b-325">Start date</span></span>
- <span data-ttu-id="c7d8b-326">调整后的开始日期</span><span class="sxs-lookup"><span data-stu-id="c7d8b-326">Adjusted start date</span></span>
- <span data-ttu-id="c7d8b-327">离职日期（离职时必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-327">Termination date (required upon termination)</span></span>
- <span data-ttu-id="c7d8b-328">离职原因（离职时必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-328">Termination reason (required upon termination)</span></span>

<span data-ttu-id="c7d8b-329">员工的关键日期通过使用以下信息派生。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-329">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="c7d8b-330">Talent</span><span class="sxs-lookup"><span data-stu-id="c7d8b-330">Talent</span></span>                | <span data-ttu-id="c7d8b-331">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c7d8b-331">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7d8b-332">最近雇用日期</span><span class="sxs-lookup"><span data-stu-id="c7d8b-332">Most recent hire date</span></span> | <span data-ttu-id="c7d8b-333">当前未离职雇用历史记录的雇用开始日期</span><span class="sxs-lookup"><span data-stu-id="c7d8b-333">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="c7d8b-334">终止日期</span><span class="sxs-lookup"><span data-stu-id="c7d8b-334">Termination date</span></span>      | <span data-ttu-id="c7d8b-335">当前未离职雇用历史记录的离职日期</span><span class="sxs-lookup"><span data-stu-id="c7d8b-335">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="c7d8b-336">入职日期</span><span class="sxs-lookup"><span data-stu-id="c7d8b-336">Start date</span></span>            | <span data-ttu-id="c7d8b-337">当前非活动雇用历史记录经过调整后的开始日期、开始日期或雇用开始时间。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-337">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="c7d8b-338">原始雇用日期</span><span class="sxs-lookup"><span data-stu-id="c7d8b-338">Original hire date</span></span>    | <span data-ttu-id="c7d8b-339">最早雇用历史记录的雇用开始时间</span><span class="sxs-lookup"><span data-stu-id="c7d8b-339">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="c7d8b-340">薪酬</span><span class="sxs-lookup"><span data-stu-id="c7d8b-340">Compensation</span></span>

<span data-ttu-id="c7d8b-341">在整个雇用期间都必须为每个员工的主要职位关联一个固定的薪酬计划。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-341">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="c7d8b-342">此期间在雇用员工的日期（或雇用开始日期）开始，持续到员工离职为止。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-342">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="c7d8b-343">生效日期（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-343">Effective Date (required)</span></span>
- <span data-ttu-id="c7d8b-344">到期日期</span><span class="sxs-lookup"><span data-stu-id="c7d8b-344">Expiration date</span></span>
- <span data-ttu-id="c7d8b-345">付薪比率（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-345">Pay Rate (required)</span></span>
- <span data-ttu-id="c7d8b-346">付薪比率转换（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-346">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="c7d8b-347">年度等价金额（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-347">Annual equivalent (required)</span></span>
- <span data-ttu-id="c7d8b-348">小时等价金额（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-348">Hourly equivalent (required)</span></span>

<span data-ttu-id="c7d8b-349">如果小时员工有多个职位，则将主要职位的固定薪酬作为员工级基本比率/工资导入 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-349">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="c7d8b-350">对于非主要职位，小时收费比率保存到 Dayforce 中的相应位置。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-350">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="c7d8b-351">如果固定员工有多个职位，则从所有活动职位派生累积小时费率和年工资，并用作员工级基本费率/工资。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-351">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="c7d8b-352">标识号</span><span class="sxs-lookup"><span data-stu-id="c7d8b-352">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="c7d8b-353">社会安全标识符</span><span class="sxs-lookup"><span data-stu-id="c7d8b-353">Social Security identifier</span></span> 

<span data-ttu-id="c7d8b-354">每个员工必须有一个主要标识符。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-354">Every employee must have one primary identifier.</span></span> <span data-ttu-id="c7d8b-355">此标识符的类型必须为 **SSN** 身份证明类型。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-355">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="c7d8b-356">在 Dayforce 中，将自动派生为雇用时需要的员工社会安全标识符。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-356">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="c7d8b-357">主要（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-357">Primary (required)</span></span>
- <span data-ttu-id="c7d8b-358">身份证明类型 =“SSN”</span><span class="sxs-lookup"><span data-stu-id="c7d8b-358">Identification Type = "SSN"</span></span>
- <span data-ttu-id="c7d8b-359">签发日期</span><span class="sxs-lookup"><span data-stu-id="c7d8b-359">Issued Date</span></span>
- <span data-ttu-id="c7d8b-360">到期日期</span><span class="sxs-lookup"><span data-stu-id="c7d8b-360">Expiration Date</span></span>

<span data-ttu-id="c7d8b-361">员工可以声明 **SSN** 身份证明类型的多个身份证明编号。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-361">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="c7d8b-362">但是，只会将标记为**主要**的记录集成到 Dayforce，号码是有效还是已过期无关紧要。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-362">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="c7d8b-363">银行帐户和付款</span><span class="sxs-lookup"><span data-stu-id="c7d8b-363">Bank accounts and disbursements</span></span>

<span data-ttu-id="c7d8b-364">必须为选择通过银行转账付薪的员工输入有效的银行帐户信息。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-364">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="c7d8b-365">Talent</span><span class="sxs-lookup"><span data-stu-id="c7d8b-365">Talent</span></span>                         | <span data-ttu-id="c7d8b-366">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c7d8b-366">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7d8b-367">银行帐号（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-367">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="c7d8b-368">SWIFT 代码（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-368">SWIFT code (required)</span></span>          | <span data-ttu-id="c7d8b-369">在墨西哥处理工资单时使用的**银行 ID** 字段。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-369">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="c7d8b-370">分行编号（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-370">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="c7d8b-371">银行帐户类型（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-371">Bank account type (required)</span></span>   | <span data-ttu-id="c7d8b-372">在墨西哥处理工资单时使用的**帐户类型**字段。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-372">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="c7d8b-373">支持的值包括**支票**和**工资单**。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-373">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="c7d8b-374">选择通过银行转帐付薪的员工必须提供一个链接，该链接是主要地址在墨西哥且与墨西哥银行的有效银行帐户关联的法人名下的余额帐户。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-374">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="c7d8b-375">将忽略其他所有非余额帐户。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-375">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="c7d8b-376">地址信息</span><span class="sxs-lookup"><span data-stu-id="c7d8b-376">Address information</span></span>

<span data-ttu-id="c7d8b-377">每个员工必须有一个主要职位。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-377">Every employee must have one primary location.</span></span> <span data-ttu-id="c7d8b-378">在 Dayforce 中，此职位用于确定员工的主要纳税地址。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-378">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="c7d8b-379">主要（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-379">Primary (required)</span></span>
- <span data-ttu-id="c7d8b-380">国家/地区（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-380">Country/region (required)</span></span>
- <span data-ttu-id="c7d8b-381">邮政编码（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-381">Zip/postal code (required)</span></span>
- <span data-ttu-id="c7d8b-382">街道（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-382">Street (required)</span></span>
- <span data-ttu-id="c7d8b-383">街道号（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-383">Street Number (required)</span></span>
- <span data-ttu-id="c7d8b-384">建筑物地址</span><span class="sxs-lookup"><span data-stu-id="c7d8b-384">Building Complement</span></span>
- <span data-ttu-id="c7d8b-385"> 市/县（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-385">City (required)</span></span>
- <span data-ttu-id="c7d8b-386">省/直辖市/自治区（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-386">State (required)</span></span>
- <span data-ttu-id="c7d8b-387">国家/地区（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-387">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="c7d8b-388">在美国和加拿大配置数据以生成工资单</span><span class="sxs-lookup"><span data-stu-id="c7d8b-388">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="c7d8b-389">如果要在美国和加拿大为员工生成付薪，必须配置以下元素：</span><span class="sxs-lookup"><span data-stu-id="c7d8b-389">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="c7d8b-390">需要职位的部门。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-390">Departments are required on positions.</span></span>
- <span data-ttu-id="c7d8b-391">必须将成本中心设置为财务维度，并且成本中心必须为默认财务维度字符串的第一个元素。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-391">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="c7d8b-392">可以配置 Talent，以便要求在“职位”中指定“部门”。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-392">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="c7d8b-393">方法是，转到**人力资源共享职位 > 职位 > 必填职位中的部门**。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-393">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="c7d8b-394">建议为集成实施此项设置。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-394">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="c7d8b-395">工作类型</span><span class="sxs-lookup"><span data-stu-id="c7d8b-395">Job types</span></span>

<span data-ttu-id="c7d8b-396">工作类型用于将类似的工作分组为类别。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-396">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="c7d8b-397">要在美国和加拿大处理工资单，需要工作类型。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-397">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="c7d8b-398">例如，工作类型包括全职和兼职，或按工资付薪和按小时付薪。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-398">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="c7d8b-399">作业类型作为付薪类型映射到 Dayforce，用于指示员工按小时还是按工资付薪。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-399">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="c7d8b-400">需要以下作业类型和描述。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-400">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="c7d8b-401">工作类型</span><span class="sxs-lookup"><span data-stu-id="c7d8b-401">Job type</span></span>   | <span data-ttu-id="c7d8b-402">说明</span><span class="sxs-lookup"><span data-stu-id="c7d8b-402">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="c7d8b-403">每小时</span><span class="sxs-lookup"><span data-stu-id="c7d8b-403">Hourly</span></span>     | <span data-ttu-id="c7d8b-404">每小时</span><span class="sxs-lookup"><span data-stu-id="c7d8b-404">Hourly</span></span>      |
| <span data-ttu-id="c7d8b-405">按工资</span><span class="sxs-lookup"><span data-stu-id="c7d8b-405">Salaried</span></span>   | <span data-ttu-id="c7d8b-406">按工资</span><span class="sxs-lookup"><span data-stu-id="c7d8b-406">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="c7d8b-407">职位类型</span><span class="sxs-lookup"><span data-stu-id="c7d8b-407">Position types</span></span> 

<span data-ttu-id="c7d8b-408">可使用职位类型描述职位是全职、兼职还是其他。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-408">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="c7d8b-409">职位类型作为付薪类别映射到 Dayforce，用于指示员工是全职还是兼职。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-409">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="c7d8b-410">需要以下职位类型和描述。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-410">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="c7d8b-411">职位类型</span><span class="sxs-lookup"><span data-stu-id="c7d8b-411">Position type</span></span>   | <span data-ttu-id="c7d8b-412">说明</span><span class="sxs-lookup"><span data-stu-id="c7d8b-412">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="c7d8b-413">全职</span><span class="sxs-lookup"><span data-stu-id="c7d8b-413">Full-time</span></span>       | <span data-ttu-id="c7d8b-414">全职员工</span><span class="sxs-lookup"><span data-stu-id="c7d8b-414">Full time employee</span></span> |
| <span data-ttu-id="c7d8b-415">兼职</span><span class="sxs-lookup"><span data-stu-id="c7d8b-415">Part-time</span></span>       | <span data-ttu-id="c7d8b-416">兼职员工</span><span class="sxs-lookup"><span data-stu-id="c7d8b-416">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="c7d8b-417">原因代码</span><span class="sxs-lookup"><span data-stu-id="c7d8b-417">Reason codes</span></span>

<span data-ttu-id="c7d8b-418">原因代码提供有关员工状态的信息。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-418">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="c7d8b-419">原因代码作为状态代码映射到 Dayforce，用于指示更改员工的职位或雇用状态的原因。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-419">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="c7d8b-420">需要以下原因代码和描述。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-420">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="c7d8b-421">原因代码</span><span class="sxs-lookup"><span data-stu-id="c7d8b-421">Reason code</span></span>    | <span data-ttu-id="c7d8b-422">说明</span><span class="sxs-lookup"><span data-stu-id="c7d8b-422">Description</span></span>      | <span data-ttu-id="c7d8b-423">适用的场景</span><span class="sxs-lookup"><span data-stu-id="c7d8b-423">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="c7d8b-424">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="c7d8b-424">RESIGNATION</span></span>    | <span data-ttu-id="c7d8b-425">辞职</span><span class="sxs-lookup"><span data-stu-id="c7d8b-425">Resignation</span></span>      | <span data-ttu-id="c7d8b-426">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="c7d8b-426">Terminate worker</span></span>     |
| <span data-ttu-id="c7d8b-427">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="c7d8b-427">TERMINATION</span></span>    | <span data-ttu-id="c7d8b-428">终止</span><span class="sxs-lookup"><span data-stu-id="c7d8b-428">Termination</span></span>      | <span data-ttu-id="c7d8b-429">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="c7d8b-429">Terminate worker</span></span>     |
| <span data-ttu-id="c7d8b-430">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="c7d8b-430">RETIREMENT</span></span>     | <span data-ttu-id="c7d8b-431">退休</span><span class="sxs-lookup"><span data-stu-id="c7d8b-431">Retirement</span></span>       | <span data-ttu-id="c7d8b-432">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="c7d8b-432">Terminate worker</span></span>     |
| <span data-ttu-id="c7d8b-433">OTHER</span><span class="sxs-lookup"><span data-stu-id="c7d8b-433">OTHER</span></span>          | <span data-ttu-id="c7d8b-434">其他原因</span><span class="sxs-lookup"><span data-stu-id="c7d8b-434">Other Reasons</span></span>    | <span data-ttu-id="c7d8b-435">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="c7d8b-435">Terminate worker</span></span>     |
| <span data-ttu-id="c7d8b-436">DEATH</span><span class="sxs-lookup"><span data-stu-id="c7d8b-436">DEATH</span></span>          | <span data-ttu-id="c7d8b-437">死亡</span><span class="sxs-lookup"><span data-stu-id="c7d8b-437">Death</span></span>            | <span data-ttu-id="c7d8b-438">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="c7d8b-438">Terminate worker</span></span>     |
| <span data-ttu-id="c7d8b-439">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="c7d8b-439">LEAVEOFABSENCE</span></span> | <span data-ttu-id="c7d8b-440">休假</span><span class="sxs-lookup"><span data-stu-id="c7d8b-440">Leave of Absence</span></span> | <span data-ttu-id="c7d8b-441">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="c7d8b-441">Terminate worker</span></span>     |
| <span data-ttu-id="c7d8b-442">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="c7d8b-442">CONTRACTEND</span></span>    | <span data-ttu-id="c7d8b-443">合同结束</span><span class="sxs-lookup"><span data-stu-id="c7d8b-443">End of Contract</span></span>  | <span data-ttu-id="c7d8b-444">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="c7d8b-444">Terminate worker</span></span>     |
| <span data-ttu-id="c7d8b-445">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="c7d8b-445">SALARYCHANGE</span></span>   | <span data-ttu-id="c7d8b-446">工资改变</span><span class="sxs-lookup"><span data-stu-id="c7d8b-446">Change of Salary</span></span> | <span data-ttu-id="c7d8b-447">薪酬</span><span class="sxs-lookup"><span data-stu-id="c7d8b-447">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="c7d8b-448">婚姻状况</span><span class="sxs-lookup"><span data-stu-id="c7d8b-448">Marital status</span></span>

<span data-ttu-id="c7d8b-449">婚姻状态值映射到 Dayforce，并在集成时根据需要转换为接受的值。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-449">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="c7d8b-450">下表显示婚姻状态值如何映射到 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-450">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="c7d8b-451">Talent</span><span class="sxs-lookup"><span data-stu-id="c7d8b-451">Talent</span></span>                 | <span data-ttu-id="c7d8b-452">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c7d8b-452">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="c7d8b-453">已婚</span><span class="sxs-lookup"><span data-stu-id="c7d8b-453">Married</span></span>                | <span data-ttu-id="c7d8b-454">已婚</span><span class="sxs-lookup"><span data-stu-id="c7d8b-454">Married</span></span>              |
| <span data-ttu-id="c7d8b-455">单一</span><span class="sxs-lookup"><span data-stu-id="c7d8b-455">Single</span></span>                 | <span data-ttu-id="c7d8b-456">单一</span><span class="sxs-lookup"><span data-stu-id="c7d8b-456">Single</span></span>               |
| <span data-ttu-id="c7d8b-457">丧偶</span><span class="sxs-lookup"><span data-stu-id="c7d8b-457">Widowed</span></span>                | <span data-ttu-id="c7d8b-458">丧偶</span><span class="sxs-lookup"><span data-stu-id="c7d8b-458">Widowed</span></span>              |
| <span data-ttu-id="c7d8b-459">离异</span><span class="sxs-lookup"><span data-stu-id="c7d8b-459">Divorced</span></span>               | <span data-ttu-id="c7d8b-460">离异</span><span class="sxs-lookup"><span data-stu-id="c7d8b-460">Divorced</span></span>             |
| <span data-ttu-id="c7d8b-461">注册伴侣关系</span><span class="sxs-lookup"><span data-stu-id="c7d8b-461">Registered Partnership</span></span> | <span data-ttu-id="c7d8b-462">民事结合关系</span><span class="sxs-lookup"><span data-stu-id="c7d8b-462">Domestic Partnership</span></span> |
| <span data-ttu-id="c7d8b-463">None</span><span class="sxs-lookup"><span data-stu-id="c7d8b-463">None</span></span>                   | <span data-ttu-id="c7d8b-464">None</span><span class="sxs-lookup"><span data-stu-id="c7d8b-464">None</span></span>                 |
| <span data-ttu-id="c7d8b-465">未婚同居</span><span class="sxs-lookup"><span data-stu-id="c7d8b-465">Cohabiting</span></span>             | <span data-ttu-id="c7d8b-466">未婚同居</span><span class="sxs-lookup"><span data-stu-id="c7d8b-466">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="c7d8b-467">性</span><span class="sxs-lookup"><span data-stu-id="c7d8b-467">Gender</span></span>

<span data-ttu-id="c7d8b-468">性别指派映射到 Dayforce，并在集成时根据需要转换为接受的值。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-468">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="c7d8b-469">下表显示性别指派如何映射到 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-469">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="c7d8b-470">Talent</span><span class="sxs-lookup"><span data-stu-id="c7d8b-470">Talent</span></span>       | <span data-ttu-id="c7d8b-471">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c7d8b-471">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="c7d8b-472">男</span><span class="sxs-lookup"><span data-stu-id="c7d8b-472">Male</span></span>         | <span data-ttu-id="c7d8b-473">男</span><span class="sxs-lookup"><span data-stu-id="c7d8b-473">Male</span></span>            |
| <span data-ttu-id="c7d8b-474">女</span><span class="sxs-lookup"><span data-stu-id="c7d8b-474">Female</span></span>       | <span data-ttu-id="c7d8b-475">女</span><span class="sxs-lookup"><span data-stu-id="c7d8b-475">Female</span></span>          |
| <span data-ttu-id="c7d8b-476">非特定</span><span class="sxs-lookup"><span data-stu-id="c7d8b-476">Non-specific</span></span> | <span data-ttu-id="c7d8b-477">*不支持*</span><span class="sxs-lookup"><span data-stu-id="c7d8b-477">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="c7d8b-478">收入代码</span><span class="sxs-lookup"><span data-stu-id="c7d8b-478">Earning codes</span></span>

<span data-ttu-id="c7d8b-479">收入代码唯一标识工作人员获得的每种收入类型。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-479">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="c7d8b-480">这些代码有多个与收入有关的参数，如会计规则、税法、报告要求和补偿费功能。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-480">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="c7d8b-481">如果使用不受支持的频率，默认将使用**每个付薪**频率进行计算。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-481">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="c7d8b-482">支持的频率</span><span class="sxs-lookup"><span data-stu-id="c7d8b-482">Supported frequencies</span></span>

- <span data-ttu-id="c7d8b-483">所有</span><span class="sxs-lookup"><span data-stu-id="c7d8b-483">All</span></span>
- <span data-ttu-id="c7d8b-484">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="c7d8b-484">EVERYPAY</span></span>
- <span data-ttu-id="c7d8b-485">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="c7d8b-485">EACHPAYPERIOD</span></span>
- <span data-ttu-id="c7d8b-486">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="c7d8b-486">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="c7d8b-487">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="c7d8b-487">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="c7d8b-488">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7d8b-488">1OFMTH</span></span>
- <span data-ttu-id="c7d8b-489">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="c7d8b-489">LASTOFMTH</span></span>
- <span data-ttu-id="c7d8b-490">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7d8b-490">2OFMTH</span></span>
- <span data-ttu-id="c7d8b-491">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7d8b-491">3OFMTH</span></span>
- <span data-ttu-id="c7d8b-492">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7d8b-492">4OFMTH</span></span>
- <span data-ttu-id="c7d8b-493">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7d8b-493">5OFMTH</span></span>
- <span data-ttu-id="c7d8b-494">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7d8b-494">1N2OFMTH</span></span>
- <span data-ttu-id="c7d8b-495">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7d8b-495">3N4OFMTH</span></span>
- <span data-ttu-id="c7d8b-496">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7d8b-496">1N3OFMTH</span></span>
- <span data-ttu-id="c7d8b-497">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7d8b-497">1N4OFMTH</span></span>
- <span data-ttu-id="c7d8b-498">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7d8b-498">2N3OFMTH</span></span>
- <span data-ttu-id="c7d8b-499">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7d8b-499">2N4OFMTH</span></span>
- <span data-ttu-id="c7d8b-500">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7d8b-500">1N2N3OFMTH</span></span>
- <span data-ttu-id="c7d8b-501">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7d8b-501">1N2N4OFMTH</span></span>
- <span data-ttu-id="c7d8b-502">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7d8b-502">1N3N4OFMTH</span></span>
- <span data-ttu-id="c7d8b-503">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7d8b-503">2N3N4OFMTH</span></span>
- <span data-ttu-id="c7d8b-504">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7d8b-504">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="c7d8b-505">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="c7d8b-505">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="c7d8b-506">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="c7d8b-506">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="c7d8b-507">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="c7d8b-507">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="c7d8b-508">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="c7d8b-508">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="c7d8b-509">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="c7d8b-509">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="c7d8b-510">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="c7d8b-510">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="c7d8b-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="c7d8b-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="c7d8b-512">地址</span><span class="sxs-lookup"><span data-stu-id="c7d8b-512">Addresses</span></span>

<span data-ttu-id="c7d8b-513">特定国家或地区、省/直辖市/自治区和县/市（自治市）代码的标识需要 Dayforce 和国内/地区内提供商可识别的特定格式。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-513">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="c7d8b-514">尽管县/市的格式可变，但是每个县/市必须与一个省/直辖市/自治区关联。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-514">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="c7d8b-515">Talent</span><span class="sxs-lookup"><span data-stu-id="c7d8b-515">Talent</span></span>          | <span data-ttu-id="c7d8b-516">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c7d8b-516">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="c7d8b-517">国家/地区</span><span class="sxs-lookup"><span data-stu-id="c7d8b-517">Country/Region</span></span>  | <span data-ttu-id="c7d8b-518">国家/地区代码</span><span class="sxs-lookup"><span data-stu-id="c7d8b-518">Country Code</span></span>          |
| <span data-ttu-id="c7d8b-519">邮政编码 </span><span class="sxs-lookup"><span data-stu-id="c7d8b-519">Zip/Postal Code</span></span> | <span data-ttu-id="c7d8b-520">邮政编码</span><span class="sxs-lookup"><span data-stu-id="c7d8b-520">Postal Code</span></span>           |
| <span data-ttu-id="c7d8b-521">状态</span><span class="sxs-lookup"><span data-stu-id="c7d8b-521">State</span></span>           | <span data-ttu-id="c7d8b-522">省/直辖市/自治区代码</span><span class="sxs-lookup"><span data-stu-id="c7d8b-522">State Code</span></span>            |
| <span data-ttu-id="c7d8b-523">城市</span><span class="sxs-lookup"><span data-stu-id="c7d8b-523">City</span></span>            | <span data-ttu-id="c7d8b-524">城市</span><span class="sxs-lookup"><span data-stu-id="c7d8b-524">City</span></span>                  |
| <span data-ttu-id="c7d8b-525">县</span><span class="sxs-lookup"><span data-stu-id="c7d8b-525">County</span></span>          | <span data-ttu-id="c7d8b-526">县（自治市）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-526">County (Municipality)</span></span> |
| <span data-ttu-id="c7d8b-527">街道</span><span class="sxs-lookup"><span data-stu-id="c7d8b-527">Street</span></span>          | <span data-ttu-id="c7d8b-528">地址行 1</span><span class="sxs-lookup"><span data-stu-id="c7d8b-528">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="c7d8b-529">税区</span><span class="sxs-lookup"><span data-stu-id="c7d8b-529">Tax regions</span></span>

<span data-ttu-id="c7d8b-530">税区用于确定应在生成工资单期间应用的适当税费。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-530">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="c7d8b-531">税区作为位置地址映射到 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-531">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="c7d8b-532">默认税区必须与工作人员的活动职位关联。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-532">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="c7d8b-533">税区（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-533">Tax region (required)</span></span>
- <span data-ttu-id="c7d8b-534">国家/地区（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-534">Country/Region (required)</span></span>
- <span data-ttu-id="c7d8b-535">省/直辖市/自治区（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-535">State (required)</span></span>
- <span data-ttu-id="c7d8b-536">县</span><span class="sxs-lookup"><span data-stu-id="c7d8b-536">County</span></span> 
- <span data-ttu-id="c7d8b-537"> 市/县（必填）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-537">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="c7d8b-538">在墨西哥配置数据以生成工资单</span><span class="sxs-lookup"><span data-stu-id="c7d8b-538">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="c7d8b-539">如果要在墨西哥为员工生成付薪，必须配置以下元素：</span><span class="sxs-lookup"><span data-stu-id="c7d8b-539">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="c7d8b-540">需要职位的部门。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-540">Departments are required on positions.</span></span>
- <span data-ttu-id="c7d8b-541">必须将成本中心设置为财务维度，并且成本中心必须为默认财务维度字符串的第一个元素。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-541">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="c7d8b-542">工作类型</span><span class="sxs-lookup"><span data-stu-id="c7d8b-542">Job types</span></span>

<span data-ttu-id="c7d8b-543">工作类型用于将类似的工作分组为类别。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-543">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="c7d8b-544">在墨西哥需要工作类型才能处理工资单。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-544">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="c7d8b-545">例如，工作类型包括全职和兼职，或按工资付薪和按小时付薪。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-545">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="c7d8b-546">作业类型作为付薪类型映射到 Dayforce，用于指示员工按小时还是按工资付薪。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-546">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="c7d8b-547">需要以下作业类型和描述。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-547">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="c7d8b-548">工作类型</span><span class="sxs-lookup"><span data-stu-id="c7d8b-548">Job type</span></span>   | <span data-ttu-id="c7d8b-549">说明</span><span class="sxs-lookup"><span data-stu-id="c7d8b-549">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="c7d8b-550">每小时</span><span class="sxs-lookup"><span data-stu-id="c7d8b-550">Hourly</span></span>     | <span data-ttu-id="c7d8b-551">墨西哥按小时</span><span class="sxs-lookup"><span data-stu-id="c7d8b-551">MX Hourly</span></span>   |
| <span data-ttu-id="c7d8b-552">按工资</span><span class="sxs-lookup"><span data-stu-id="c7d8b-552">Salaried</span></span>   | <span data-ttu-id="c7d8b-553">墨西哥按工资</span><span class="sxs-lookup"><span data-stu-id="c7d8b-553">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="c7d8b-554">职位类型</span><span class="sxs-lookup"><span data-stu-id="c7d8b-554">Position types</span></span> 

<span data-ttu-id="c7d8b-555">可使用职位类型描述职位是全职、兼职还是其他。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-555">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="c7d8b-556">职位类型作为付薪类别映射到 Dayforce，用于指示员工是全职还是兼职。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-556">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="c7d8b-557">需要以下职位类型和描述。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-557">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="c7d8b-558">职位类型</span><span class="sxs-lookup"><span data-stu-id="c7d8b-558">Position type</span></span>   | <span data-ttu-id="c7d8b-559">说明</span><span class="sxs-lookup"><span data-stu-id="c7d8b-559">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="c7d8b-560">全职</span><span class="sxs-lookup"><span data-stu-id="c7d8b-560">Full-time</span></span>       | <span data-ttu-id="c7d8b-561">全职员工</span><span class="sxs-lookup"><span data-stu-id="c7d8b-561">Full time employee</span></span> |
| <span data-ttu-id="c7d8b-562">兼职</span><span class="sxs-lookup"><span data-stu-id="c7d8b-562">Part-time</span></span>       | <span data-ttu-id="c7d8b-563">兼职员工</span><span class="sxs-lookup"><span data-stu-id="c7d8b-563">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="c7d8b-564">原因代码</span><span class="sxs-lookup"><span data-stu-id="c7d8b-564">Reason codes</span></span>

<span data-ttu-id="c7d8b-565">原因代码提供有关员工状态的信息。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-565">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="c7d8b-566">原因代码作为状态代码映射到 Dayforce，用于指示更改员工的职位或雇用状态的原因。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-566">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="c7d8b-567">需要以下原因代码和描述。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-567">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="c7d8b-568">原因代码</span><span class="sxs-lookup"><span data-stu-id="c7d8b-568">Reason code</span></span>            | <span data-ttu-id="c7d8b-569">说明</span><span class="sxs-lookup"><span data-stu-id="c7d8b-569">Description</span></span>                    | <span data-ttu-id="c7d8b-570">适用的场景</span><span class="sxs-lookup"><span data-stu-id="c7d8b-570">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="c7d8b-571">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="c7d8b-571">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="c7d8b-572">首次付薪前离职</span><span class="sxs-lookup"><span data-stu-id="c7d8b-572">Departure before first payroll</span></span> | <span data-ttu-id="c7d8b-573">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="c7d8b-573">Terminate worker</span></span>     |
| <span data-ttu-id="c7d8b-574">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="c7d8b-574">RESIGNATION</span></span>            | <span data-ttu-id="c7d8b-575">辞职</span><span class="sxs-lookup"><span data-stu-id="c7d8b-575">Resignation</span></span>                    | <span data-ttu-id="c7d8b-576">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="c7d8b-576">Terminate worker</span></span>     |
| <span data-ttu-id="c7d8b-577">PENSION</span><span class="sxs-lookup"><span data-stu-id="c7d8b-577">PENSION</span></span>                | <span data-ttu-id="c7d8b-578">退休金</span><span class="sxs-lookup"><span data-stu-id="c7d8b-578">Pension</span></span>                        | <span data-ttu-id="c7d8b-579">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="c7d8b-579">Terminate worker</span></span>     |
| <span data-ttu-id="c7d8b-580">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="c7d8b-580">TERMINATION</span></span>            | <span data-ttu-id="c7d8b-581">终止</span><span class="sxs-lookup"><span data-stu-id="c7d8b-581">Termination</span></span>                    | <span data-ttu-id="c7d8b-582">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="c7d8b-582">Terminate worker</span></span>     |
| <span data-ttu-id="c7d8b-583">退休</span><span class="sxs-lookup"><span data-stu-id="c7d8b-583">RETIREMENT</span></span>             | <span data-ttu-id="c7d8b-584">退休</span><span class="sxs-lookup"><span data-stu-id="c7d8b-584">Retirement</span></span>                     | <span data-ttu-id="c7d8b-585">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="c7d8b-585">Terminate worker</span></span>     |
| <span data-ttu-id="c7d8b-586">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="c7d8b-586">ABSENTEE</span></span>               | <span data-ttu-id="c7d8b-587">缺勤者</span><span class="sxs-lookup"><span data-stu-id="c7d8b-587">Absentee</span></span>                       | <span data-ttu-id="c7d8b-588">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="c7d8b-588">Terminate worker</span></span>     |
| <span data-ttu-id="c7d8b-589">OTHER</span><span class="sxs-lookup"><span data-stu-id="c7d8b-589">OTHER</span></span>                  | <span data-ttu-id="c7d8b-590">其他原因</span><span class="sxs-lookup"><span data-stu-id="c7d8b-590">Other Reasons</span></span>                  | <span data-ttu-id="c7d8b-591">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="c7d8b-591">Terminate worker</span></span>     |
| <span data-ttu-id="c7d8b-592">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="c7d8b-592">CLOSURE</span></span>                | <span data-ttu-id="c7d8b-593">停业</span><span class="sxs-lookup"><span data-stu-id="c7d8b-593">Business Closure</span></span>               | <span data-ttu-id="c7d8b-594">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="c7d8b-594">Terminate worker</span></span>     |
| <span data-ttu-id="c7d8b-595">DEATH</span><span class="sxs-lookup"><span data-stu-id="c7d8b-595">DEATH</span></span>                  | <span data-ttu-id="c7d8b-596">死亡</span><span class="sxs-lookup"><span data-stu-id="c7d8b-596">Death</span></span>                          | <span data-ttu-id="c7d8b-597">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="c7d8b-597">Terminate worker</span></span>     |
| <span data-ttu-id="c7d8b-598">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="c7d8b-598">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="c7d8b-599">休假</span><span class="sxs-lookup"><span data-stu-id="c7d8b-599">Leave of Absence</span></span>               | <span data-ttu-id="c7d8b-600">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="c7d8b-600">Terminate worker</span></span>     |
| <span data-ttu-id="c7d8b-601">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="c7d8b-601">CONTRACTEND</span></span>            | <span data-ttu-id="c7d8b-602">合同结束</span><span class="sxs-lookup"><span data-stu-id="c7d8b-602">End of Contract</span></span>                | <span data-ttu-id="c7d8b-603">解雇工作人员</span><span class="sxs-lookup"><span data-stu-id="c7d8b-603">Terminate worker</span></span>     |
| <span data-ttu-id="c7d8b-604">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="c7d8b-604">SALARYCHANGE</span></span>           | <span data-ttu-id="c7d8b-605">工资改变</span><span class="sxs-lookup"><span data-stu-id="c7d8b-605">Change of Salary</span></span>               | <span data-ttu-id="c7d8b-606">薪酬</span><span class="sxs-lookup"><span data-stu-id="c7d8b-606">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="c7d8b-607">雇用条款</span><span class="sxs-lookup"><span data-stu-id="c7d8b-607">Terms of employment</span></span>

<span data-ttu-id="c7d8b-608">雇用条款用于创建雇用条款的类别。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-608">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="c7d8b-609">这些条款作为雇用指标值映射到 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-609">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="c7d8b-610">需要以下雇用条款和描述。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-610">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="c7d8b-611">雇用条款</span><span class="sxs-lookup"><span data-stu-id="c7d8b-611">Terms of employment</span></span>   | <span data-ttu-id="c7d8b-612">说明</span><span class="sxs-lookup"><span data-stu-id="c7d8b-612">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="c7d8b-613">常规</span><span class="sxs-lookup"><span data-stu-id="c7d8b-613">Regular</span></span>               | <span data-ttu-id="c7d8b-614">常规</span><span class="sxs-lookup"><span data-stu-id="c7d8b-614">Regular</span></span>     |
| <span data-ttu-id="c7d8b-615">直接</span><span class="sxs-lookup"><span data-stu-id="c7d8b-615">Direct</span></span>                | <span data-ttu-id="c7d8b-616">直接</span><span class="sxs-lookup"><span data-stu-id="c7d8b-616">Direct</span></span>      |
| <span data-ttu-id="c7d8b-617">实习</span><span class="sxs-lookup"><span data-stu-id="c7d8b-617">Internship</span></span>            | <span data-ttu-id="c7d8b-618">实习</span><span class="sxs-lookup"><span data-stu-id="c7d8b-618">Internship</span></span>  |
| <span data-ttu-id="c7d8b-619">永久</span><span class="sxs-lookup"><span data-stu-id="c7d8b-619">Permanent</span></span>             | <span data-ttu-id="c7d8b-620">永久</span><span class="sxs-lookup"><span data-stu-id="c7d8b-620">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="c7d8b-621">婚姻状况</span><span class="sxs-lookup"><span data-stu-id="c7d8b-621">Marital status</span></span>

<span data-ttu-id="c7d8b-622">婚姻状态值映射到 Dayforce，并在集成时根据需要转换为接受的值。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-622">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="c7d8b-623">下表显示婚姻状态值如何映射到 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-623">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="c7d8b-624">Talent</span><span class="sxs-lookup"><span data-stu-id="c7d8b-624">Talent</span></span>                 | <span data-ttu-id="c7d8b-625">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c7d8b-625">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="c7d8b-626">已婚</span><span class="sxs-lookup"><span data-stu-id="c7d8b-626">Married</span></span>                | <span data-ttu-id="c7d8b-627">已婚</span><span class="sxs-lookup"><span data-stu-id="c7d8b-627">Married</span></span>                   |
| <span data-ttu-id="c7d8b-628">单一</span><span class="sxs-lookup"><span data-stu-id="c7d8b-628">Single</span></span>                 | <span data-ttu-id="c7d8b-629">单一</span><span class="sxs-lookup"><span data-stu-id="c7d8b-629">Single</span></span>                    |
| <span data-ttu-id="c7d8b-630">丧偶</span><span class="sxs-lookup"><span data-stu-id="c7d8b-630">Widowed</span></span>                | <span data-ttu-id="c7d8b-631">丧偶</span><span class="sxs-lookup"><span data-stu-id="c7d8b-631">Widowed</span></span>                   |
| <span data-ttu-id="c7d8b-632">离异</span><span class="sxs-lookup"><span data-stu-id="c7d8b-632">Divorced</span></span>               | <span data-ttu-id="c7d8b-633">离异</span><span class="sxs-lookup"><span data-stu-id="c7d8b-633">Divorced</span></span>                  |
| <span data-ttu-id="c7d8b-634">注册伴侣关系</span><span class="sxs-lookup"><span data-stu-id="c7d8b-634">Registered Partnership</span></span> | <span data-ttu-id="c7d8b-635">民事结合关系</span><span class="sxs-lookup"><span data-stu-id="c7d8b-635">Domestic Partnership</span></span>      |
| <span data-ttu-id="c7d8b-636">None</span><span class="sxs-lookup"><span data-stu-id="c7d8b-636">None</span></span>                   | <span data-ttu-id="c7d8b-637">*墨西哥不支持*</span><span class="sxs-lookup"><span data-stu-id="c7d8b-637">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="c7d8b-638">未婚同居</span><span class="sxs-lookup"><span data-stu-id="c7d8b-638">Cohabiting</span></span>             | <span data-ttu-id="c7d8b-639">*墨西哥不支持*</span><span class="sxs-lookup"><span data-stu-id="c7d8b-639">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="c7d8b-640">性</span><span class="sxs-lookup"><span data-stu-id="c7d8b-640">Gender</span></span>

<span data-ttu-id="c7d8b-641">性别指派映射到 Dayforce，并在集成时根据需要转换为接受的值。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-641">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="c7d8b-642">下表显示性别指派如何映射到 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-642">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="c7d8b-643">Talent</span><span class="sxs-lookup"><span data-stu-id="c7d8b-643">Talent</span></span>       | <span data-ttu-id="c7d8b-644">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c7d8b-644">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="c7d8b-645">男</span><span class="sxs-lookup"><span data-stu-id="c7d8b-645">Male</span></span>         | <span data-ttu-id="c7d8b-646">男</span><span class="sxs-lookup"><span data-stu-id="c7d8b-646">Male</span></span>                      |
| <span data-ttu-id="c7d8b-647">女</span><span class="sxs-lookup"><span data-stu-id="c7d8b-647">Female</span></span>       | <span data-ttu-id="c7d8b-648">女</span><span class="sxs-lookup"><span data-stu-id="c7d8b-648">Female</span></span>                    |
| <span data-ttu-id="c7d8b-649">非特定</span><span class="sxs-lookup"><span data-stu-id="c7d8b-649">Non-specific</span></span> | <span data-ttu-id="c7d8b-650">*墨西哥不支持*</span><span class="sxs-lookup"><span data-stu-id="c7d8b-650">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="c7d8b-651">付款方式</span><span class="sxs-lookup"><span data-stu-id="c7d8b-651">Payment method</span></span>

<span data-ttu-id="c7d8b-652">付款方式为员工和公司提供描述如何向员工付款的方式。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-652">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="c7d8b-653">付款方式映射到 Dayforce，并在集成时根据需要转换为接受的值。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-653">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="c7d8b-654">下表显示付款方式如何映射到 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-654">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="c7d8b-655">Talent</span><span class="sxs-lookup"><span data-stu-id="c7d8b-655">Talent</span></span>             | <span data-ttu-id="c7d8b-656">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c7d8b-656">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="c7d8b-657">现金</span><span class="sxs-lookup"><span data-stu-id="c7d8b-657">Cash</span></span>               | <span data-ttu-id="c7d8b-658">现金</span><span class="sxs-lookup"><span data-stu-id="c7d8b-658">Cash</span></span>                      |
| <span data-ttu-id="c7d8b-659">电子支付</span><span class="sxs-lookup"><span data-stu-id="c7d8b-659">Electronic Payment</span></span> | <span data-ttu-id="c7d8b-660">转移</span><span class="sxs-lookup"><span data-stu-id="c7d8b-660">Transfer</span></span>                  |
| <span data-ttu-id="c7d8b-661">检查</span><span class="sxs-lookup"><span data-stu-id="c7d8b-661">Check</span></span>              | <span data-ttu-id="c7d8b-662">支票</span><span class="sxs-lookup"><span data-stu-id="c7d8b-662">Cheque</span></span>                    |
| <span data-ttu-id="c7d8b-663">银行汇票</span><span class="sxs-lookup"><span data-stu-id="c7d8b-663">Bank Draft</span></span>         | <span data-ttu-id="c7d8b-664">*墨西哥不支持*</span><span class="sxs-lookup"><span data-stu-id="c7d8b-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="c7d8b-665">其他</span><span class="sxs-lookup"><span data-stu-id="c7d8b-665">Other</span></span>              | <span data-ttu-id="c7d8b-666">*墨西哥不支持*</span><span class="sxs-lookup"><span data-stu-id="c7d8b-666">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="c7d8b-667">银行帐户类型</span><span class="sxs-lookup"><span data-stu-id="c7d8b-667">Bank account type</span></span>

<span data-ttu-id="c7d8b-668">银行帐户类型用于对员工进行电子付款。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-668">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="c7d8b-669">银行账户类型作为转帐信息映射到 Dayforce。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-669">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="c7d8b-670">集成时，银行帐户类型根据需要转换为接受的值。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-670">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="c7d8b-671">Talent</span><span class="sxs-lookup"><span data-stu-id="c7d8b-671">Talent</span></span>            | <span data-ttu-id="c7d8b-672">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c7d8b-672">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="c7d8b-673">支票帐户</span><span class="sxs-lookup"><span data-stu-id="c7d8b-673">Checking Account</span></span>  | <span data-ttu-id="c7d8b-674">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="c7d8b-674">CheckingAccount</span></span>           |
| <span data-ttu-id="c7d8b-675">工资单帐户</span><span class="sxs-lookup"><span data-stu-id="c7d8b-675">Payroll Account</span></span>   | <span data-ttu-id="c7d8b-676">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="c7d8b-676">PayrollAccount</span></span>            |
| <span data-ttu-id="c7d8b-677">储蓄帐户</span><span class="sxs-lookup"><span data-stu-id="c7d8b-677">Savings Account</span></span>   | <span data-ttu-id="c7d8b-678">*墨西哥不支持*</span><span class="sxs-lookup"><span data-stu-id="c7d8b-678">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="c7d8b-679">BankGirot 帐户</span><span class="sxs-lookup"><span data-stu-id="c7d8b-679">BankGirot account</span></span> | <span data-ttu-id="c7d8b-680">*墨西哥不支持*</span><span class="sxs-lookup"><span data-stu-id="c7d8b-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="c7d8b-681">PlusGirot 帐户</span><span class="sxs-lookup"><span data-stu-id="c7d8b-681">PlusGirot account</span></span> | <span data-ttu-id="c7d8b-682">*墨西哥不支持*</span><span class="sxs-lookup"><span data-stu-id="c7d8b-682">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="c7d8b-683">收入代码</span><span class="sxs-lookup"><span data-stu-id="c7d8b-683">Earning codes</span></span>

<span data-ttu-id="c7d8b-684">收入代码唯一标识工作人员获得的每种收入类型。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-684">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="c7d8b-685">这些代码有多个与收入有关的参数，如会计规则、税法、报告要求和补偿费功能。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-685">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="c7d8b-686">如果使用不受支持的频率，默认将使用**每个付薪**频率进行计算。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-686">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="c7d8b-687">支持的频率</span><span class="sxs-lookup"><span data-stu-id="c7d8b-687">Supported frequencies</span></span>

- <span data-ttu-id="c7d8b-688">所有</span><span class="sxs-lookup"><span data-stu-id="c7d8b-688">All</span></span>
- <span data-ttu-id="c7d8b-689">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="c7d8b-689">EVERYPAY</span></span>
- <span data-ttu-id="c7d8b-690">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="c7d8b-690">EACHPAYPERIOD</span></span>
- <span data-ttu-id="c7d8b-691">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="c7d8b-691">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="c7d8b-692">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="c7d8b-692">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="c7d8b-693">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7d8b-693">1OFMTH</span></span>
- <span data-ttu-id="c7d8b-694">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="c7d8b-694">LASTOFMTH</span></span>
- <span data-ttu-id="c7d8b-695">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7d8b-695">2OFMTH</span></span>
- <span data-ttu-id="c7d8b-696">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7d8b-696">3OFMTH</span></span>
- <span data-ttu-id="c7d8b-697">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7d8b-697">4OFMTH</span></span>
- <span data-ttu-id="c7d8b-698">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7d8b-698">5OFMTH</span></span>
- <span data-ttu-id="c7d8b-699">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7d8b-699">1N2OFMTH</span></span>
- <span data-ttu-id="c7d8b-700">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7d8b-700">3N4OFMTH</span></span>
- <span data-ttu-id="c7d8b-701">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7d8b-701">1N3OFMTH</span></span>
- <span data-ttu-id="c7d8b-702">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7d8b-702">1N4OFMTH</span></span>
- <span data-ttu-id="c7d8b-703">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7d8b-703">2N3OFMTH</span></span>
- <span data-ttu-id="c7d8b-704">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7d8b-704">2N4OFMTH</span></span>
- <span data-ttu-id="c7d8b-705">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7d8b-705">1N2N3OFMTH</span></span>
- <span data-ttu-id="c7d8b-706">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7d8b-706">1N2N4OFMTH</span></span>
- <span data-ttu-id="c7d8b-707">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7d8b-707">1N3N4OFMTH</span></span>
- <span data-ttu-id="c7d8b-708">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7d8b-708">2N3N4OFMTH</span></span>
- <span data-ttu-id="c7d8b-709">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c7d8b-709">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="c7d8b-710">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="c7d8b-710">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="c7d8b-711">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="c7d8b-711">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="c7d8b-712">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="c7d8b-712">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="c7d8b-713">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="c7d8b-713">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="c7d8b-714">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="c7d8b-714">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="c7d8b-715">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="c7d8b-715">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="c7d8b-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="c7d8b-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="c7d8b-717">地址</span><span class="sxs-lookup"><span data-stu-id="c7d8b-717">Addresses</span></span>

<span data-ttu-id="c7d8b-718">特定国家或地区、省/直辖市/自治区和县/市（自治市）代码的标识需要 Dayforce 和国内/地区内提供商可识别的特定格式。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-718">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="c7d8b-719">尽管县/市的格式可变，但是每个县/市必须与一个省/直辖市/自治区关联。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-719">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="c7d8b-720">Talent</span><span class="sxs-lookup"><span data-stu-id="c7d8b-720">Talent</span></span>              | <span data-ttu-id="c7d8b-721">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c7d8b-721">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="c7d8b-722">国家/地区</span><span class="sxs-lookup"><span data-stu-id="c7d8b-722">Country/Region</span></span>      | <span data-ttu-id="c7d8b-723">国家/地区代码</span><span class="sxs-lookup"><span data-stu-id="c7d8b-723">Country Code</span></span>          |
| <span data-ttu-id="c7d8b-724">邮政编码 </span><span class="sxs-lookup"><span data-stu-id="c7d8b-724">Zip/Postal Code</span></span>     | <span data-ttu-id="c7d8b-725">邮政编码</span><span class="sxs-lookup"><span data-stu-id="c7d8b-725">Postal Code</span></span>           |
| <span data-ttu-id="c7d8b-726">状态</span><span class="sxs-lookup"><span data-stu-id="c7d8b-726">State</span></span>               | <span data-ttu-id="c7d8b-727">省/直辖市/自治区代码</span><span class="sxs-lookup"><span data-stu-id="c7d8b-727">State Code</span></span>            |
| <span data-ttu-id="c7d8b-728">城市</span><span class="sxs-lookup"><span data-stu-id="c7d8b-728">City</span></span>                | <span data-ttu-id="c7d8b-729">城市</span><span class="sxs-lookup"><span data-stu-id="c7d8b-729">City</span></span>                  |
| <span data-ttu-id="c7d8b-730">县</span><span class="sxs-lookup"><span data-stu-id="c7d8b-730">County</span></span>              | <span data-ttu-id="c7d8b-731">县（自治市）</span><span class="sxs-lookup"><span data-stu-id="c7d8b-731">County (Municipality)</span></span> |
| <span data-ttu-id="c7d8b-732">街道</span><span class="sxs-lookup"><span data-stu-id="c7d8b-732">Street</span></span>              | <span data-ttu-id="c7d8b-733">地址行 1</span><span class="sxs-lookup"><span data-stu-id="c7d8b-733">Address Line 1</span></span>        |
| <span data-ttu-id="c7d8b-734">街道编号</span><span class="sxs-lookup"><span data-stu-id="c7d8b-734">Street Number</span></span>       | <span data-ttu-id="c7d8b-735">地址行 2</span><span class="sxs-lookup"><span data-stu-id="c7d8b-735">Address Line 2</span></span>        |
| <span data-ttu-id="c7d8b-736">建筑物地址</span><span class="sxs-lookup"><span data-stu-id="c7d8b-736">Building Complement</span></span> | <span data-ttu-id="c7d8b-737">地址行 5</span><span class="sxs-lookup"><span data-stu-id="c7d8b-737">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="c7d8b-738">护照号</span><span class="sxs-lookup"><span data-stu-id="c7d8b-738">Passport number</span></span>

<span data-ttu-id="c7d8b-739">员工可以声明护照信息。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-739">Employees can declare passport information.</span></span> <span data-ttu-id="c7d8b-740">此信息的身份证明类型为**护照**，并作为员工的墨西哥特定信息的一部分集成到 Dayforce 中。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-740">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="c7d8b-741">身份证明类型 =“护照”</span><span class="sxs-lookup"><span data-stu-id="c7d8b-741">Identification Type = "Passport"</span></span>
- <span data-ttu-id="c7d8b-742">签发日期</span><span class="sxs-lookup"><span data-stu-id="c7d8b-742">Issued Date</span></span>
- <span data-ttu-id="c7d8b-743">到期日期</span><span class="sxs-lookup"><span data-stu-id="c7d8b-743">Expiration Date</span></span>

<span data-ttu-id="c7d8b-744">员工可以声明**护照**身份证明类型的多个身份证明编号。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-744">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="c7d8b-745">但是，仅将当前有效的护照条目集成到 Dayforce 中。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-745">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="c7d8b-746">如果所有护照条目均已过期，将把最近签发的护照集成到 Dayforce 中。</span><span class="sxs-lookup"><span data-stu-id="c7d8b-746">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>

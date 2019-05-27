---
title: 配置 Talent 与 Dayforce 之间的工资单集成
description: 本主题说明如何配置 Microsoft Dynamics 365 for Talent 与 Ceridian Dayforce 之间的集成，以便处理付薪。
author: andreabichsel
manager: AnnBe
ms.date: 03/26/2019
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
ms.openlocfilehash: 9a88bf61dbb12520b555ceb7363b1c646d95386e
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517386"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a>配置 Talent 和 Dayforce 之间的工资单集成

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 for Talent 与 Ceridian Dayforce 之间的集成依赖于本主题中介绍的几个配置步骤。 必须先在 Talent 和 Dayforce 中配置集成，才能处理付薪。

使用 Dayforce 之类服务完成付薪时，必须在 Talent 中启用集成。 此集成需要来自 Talent 的特定数据。 因此，必须验证已按照支持集成的方式在 Talent 中配置了映射到 Dayforce 的数据。 此集成使用下面的各种数据类别：

- 人力资源数据
- 薪酬数据
- 工资单数据，如付薪周期、付薪期间和收入代码
- 工作人员数据

此主题介绍要启用集成必须执行的步骤。 还介绍了集成所需的数据类型和配置详细信息。

## <a name="enable-the-integration"></a>启用集成

在 Talent 中，必须开启集成并输入配置信息，才能连接到 Dayforce。 如果要将生成的的总帐交易记录导入 Microsoft Dynamics 365 for Finance and Operations 中，还必须在 Finance and Operations 只不过设置 Microsoft Azure 存储帐户和输入 Azure Storage 连接字符串。

要在 Talent 中开启集成，请执行以下步骤。

1. 在**系统管理**页中，选择 **集成配置**。
2. 输入安全文件传输协议 (FTP) 终结点和安全 FTP 文件夹路径。
3. 输入将访问安全 FTP 终结点和文件夹路径的用户的用户名和密码。
4. 根据需要测试连接，然后将**启用工资单集成**选项设置为**是**。

开启集成后，将创建数据导出包和文件，并设置频率。 可根据需要更改此频率。

有关 Azure ML 存储帐户和 Azure 存储连接字符串的详细信息，请参阅以下 Azure ML 主题：

- [关于 Azure 存储帐户](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [配置 Azure 存储连接字符串](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a>配置数据 

要处理工资单，必须在 Talent 中配置人力资源数据。 必须设置组织数据（如工作和职位），以及福利和薪酬信息。 这些信息提供生成员工付薪所需雇用、付薪和扣缴信息。

### <a name="human-resource-data"></a>人力资源数据

#### <a name="benefits"></a>福利 

人力资源提供工具，用于设置和维护组织提供或为其工作人员处理的福利、扣缴和工作人员薪酬计划。

创建福利时，请注意 Dayforce 中使用的以下数据和配置。

##### <a name="benefit-plans"></a>福利计划

- 计划（必填）
- 类型（必填）
- 工资单影响（必填）
- 恢复欠款
- 扣除方法
- 扣除优先级
- 限制期
- 限额

##### <a name="benefits"></a>福利

- 计划（必填）
- 类型（必填）
- 选项（必填）
- 福利 ID（必填）
- 频率
- 基础
- 金额或费率
- 收入代码

##### <a name="supported-frequencies"></a>支持的频率 

- 每周
- 两周一次
- 每半月
- 每月

##### <a name="supported-bases"></a>支持的库 

- 固定金额
- 收入百分比
- 工作时数

Dayforce 根据福利计划中定义的工资单影响创建以下扣缴。

| Talent 中的选择        | Dayforce 中的结果                            |
|----------------------------|-----------------------------------------------|
| None                       | 不创建扣缴。                      |
| 仅扣除             | 创建员工扣缴。             |
| 仅缴纳          | 创建雇主扣缴。             |
| 扣除和缴纳 | 创建员工扣缴和雇主扣缴。 |

有关如何定义和管理福利计划的详细信息，请参阅以下主题：

- [交付员工福利计划](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [创建新福利](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [定义福利资格规则和策略](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [登记和删除工作人员的福利](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a>薪酬 

薪酬管理用于控制基本工资和奖励的发放。 员工的固定基本工资和业绩调薪是通过固定薪酬计划控制的。 激励性的付款，例如额外津贴、绩效奖、股票期权和赠与以及一次性奖励，是通过可变薪酬计划控制的。

Dayforce 使用薪酬信息计算员工的时薪或年薪。 需要固定薪酬计划和付薪比率转换。 必须将员工与固定薪酬计划关联。

有关薪酬计划的详细信息，请参阅以下主题：

- [创建固定薪酬计划](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [创建可变薪酬计划](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [制订薪水/薪酬结构和计划](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [薪酬流程](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [定义薪酬流程并计算结果](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [在固定薪酬计划中登记员工](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [在可变薪酬计划中登记员工](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a>工作 

作业是执行作业的人员需要承担的任务和责任的集合。 有关详细信息，请参阅以下主题：

- [设置作业组件](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [定义新工作](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a>职位

位置是工作的单个实例。 例如，“销售经理（东部）”职位是与“销售经理”工作关联的职位。 职位存在于部门中。 每个职位只能与一个工作人员关联。

设置职位时，请注意以下数据和配置：

- 职位（必填）
- 描述（必填）
- 工作（必填）
- 部门（必填）
- 职位类型（必填）
- 全职等价
- 年度常规时间（必填）
- 由法人支付（必填）
- 付薪周期（必填）
- 默认财务维度 – 成本中心（必填）
- 工作人员分配 – 工作人员、分配开始时间、分配结束时间、原因代码

如果同一个部门中多个职位与同一个工作关联，应在 Dayforce 中将这些职位合并为一个位置。

有关详细信息，请参阅以下主题：

- [使用部门、工作和职位组织您的劳动力](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [设置职位](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a>部门

部门是一个运营单位，表示组织的类别或功能区域。 部门负责组织的特定区域，例如，销售、会计或人力资源。 您可以在功能区中使用要上报的部门。 部门可能具有损益职责。

有关详细信息，请参阅以下主题：

- [创建一个部门并将其与部门层次结构关联](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [定义新部门](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a>付薪周期和付薪期间

付薪周期确定付薪的频率和工作人员获薪的具体天数。 例如，付薪周期可以是每月，并且可能在月末向员工付薪。 付薪周期也可以是每周，并且可能在付薪期间结束后的星期二向员工付薪。 为职位分配付薪周期是为了控制何时向所在职位的工作人员付薪。

创建付薪周期后，可以为每个周期生成付薪期间。 每个付薪期间包含一个基于您提供的信息的默认付薪日期。 但是，可以更改付薪期间中的默认付薪日期，以便应对异常，如付薪日期在假期中。

Dayforce 中使用以下信息：

- 付薪周期（必填）
- 付薪周期频率（必填）
- 期间开始日期（需要第一个付薪期间）
- 默认付薪日期（需要第一个付薪期间）

此信息与 Dayforce 集成为付薪组，并按各付薪周期的国家或地区分隔。 集成之前，必须至少生成一个付薪期间。 Dayforce 根据 Talent 中设置的第一个付薪期间的开始日期和默认付薪日期生成付薪组日历和付薪日期。

#### <a name="earning-codes"></a>收入代码

收入代码唯一标识工作人员获得的每种收入类型。 这些代码有多个与收入有关的参数，如会计规则、税法、报告要求和补偿费功能。

Dayforce 中使用以下信息：

- 收入代码（必填）
- 说明
- 度量单位
- 生产

### <a name="worker-data"></a>工作人员数据

工作人员的对您的人力资源和工资系统十分重要的不同类型的记录。 您输入的信息可用于跟踪工作人员和个人信息。

您可以维护工作人员的以下信息:

- **基本** – 维护有关工作人员的基本信息，如联系人信息、人口统计的信息、标识信息、系列信息、状态、兵役迁移国外的信息和个人和紧急事件联系人。
- **雇用** – 维护有关工作人员雇用情况的信息，例如公司或组织隶属关系、职位分配、开始日期和结束日期、工作的雇用资格、条款，退休金、假期和重定位信息。
- **休假和缺勤** – 维护有关工作人员的缺勤的信息，例如工作日历、缺勤事务和缺勤设置。
- **薪酬和工资单** – 维护有关工作人员的薪酬计划和工资信息的信息，例如计划登记、证书、性能、佣金、税务信息、报废和薪金扣缴。

输入工作人员信息时，请注意 Dayforce 中使用的以下数据和配置。

#### <a name="general-information"></a>一般信息

- 人员编号（必填）
- 名字(必填)
- 姓氏(必填)
- 中间名
- 受聘日期
- 称作

#### <a name="personal-information"></a>个人信息

- 婚姻状况（必填）
- 出生日期（必填）
- 性别（必填）
- 残疾人士
- 国籍的国家地区（仅适用于墨西哥）

#### <a name="address-information"></a>地址信息

- 主要（必填）
- 国家/地区（必填）
- 邮政编码（必填）
- 街道编号（必填）（仅适用于墨西哥）
- 建筑物地址（仅适用于墨西哥）
-  市/县（必填）
- 省/直辖市/自治区（必填）
- 国家/地区（必填）

#### <a name="contact-information"></a>联系人信息 

- 主要（必填）
- 联系人号码（必填）
- 函授

#### <a name="payroll-information-and-earning-codes"></a>工资信息和收入代码

可以按给定付薪频率为员工分配特定收入，而员工则可以具有首选付款方式。 Dayforce 中使用以下字段确保使用这些首选项和设置。

##### <a name="earning-codes"></a>收入代码

- 职位（必填）
- 收入代码（必填）
- 频率（必填）
- 金额（必填）

##### <a name="payroll-information"></a>工资单信息

- 付款方式
- 经济区域（必填）
- 员工福利 ID
- 国家/地区 ID 号（必填）
- 兵役编号
- 班次 ID（必填）
- 税号（必填）
- 工会 ID（必填）
- 工作日 ID（必填）
- 工作许可证编号

> [!NOTE]
> 对于付款方式，墨西哥支持**现金**、**支票**（公司的实际支票）和**电子支付**。 如果不指定付款方式，则默认使用 **支票**。

#### <a name="employment-details"></a>雇用详细信息

在 Dayforce 中派生员工的入职、离职和重新入职状态时，雇用详细信息历史记录至关重要。 Dayforce 一次仅支持一条活动雇用记录。

- 雇用开始日期（必填）
- 雇佣结束日期
- 入职日期
- 调整后的开始日期
- 离职日期（离职时必填）
- 离职原因（离职时必填）

员工的关键日期通过使用以下信息派生。

| Talent                | Dayforce                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| 最近雇用日期 | 当前未离职雇用历史记录的雇用开始日期                                 |
| 终止日期      | 当前未离职雇用历史记录的离职日期                                 |
| 入职日期            | 当前非活动雇用历史记录经过调整后的开始日期、开始日期或雇用开始时间。 |
| 原始雇用日期    | 最早雇用历史记录的雇用开始时间                                               |

#### <a name="compensation"></a>薪酬

在整个雇用期间都必须为每个员工的主要职位关联一个固定的薪酬计划。 此期间在雇用员工的日期（或雇用开始日期）开始，持续到员工离职为止。

- 生效日期（必填）
- 到期日期
- 付薪比率（必填）
- 付薪比率转换（必填）
- 年度等价金额（必填）
- 小时等价金额（必填）

如果小时员工有多个职位，则将主要职位的固定薪酬作为员工级基本比率/工资导入 Dayforce。 对于非主要职位，小时收费比率保存到 Dayforce 中的相应位置。

如果固定员工有多个职位，则从所有活动职位派生累积小时费率和年工资，并用作员工级基本费率/工资。

#### <a name="identification-numbers"></a>标识号

##### <a name="social-security-identifier"></a>社会安全标识符 

每个员工必须有一个主要标识符。 此标识符的类型必须为 **SSN** 身份证明类型。 在 Dayforce 中，将自动派生为雇用时需要的员工社会安全标识符。

- 主要（必填）
- 身份证明类型 =“SSN”
- 签发日期
- 到期日期

员工可以声明 **SSN** 身份证明类型的多个身份证明编号。 但是，只会将标记为**主要**的记录集成到 Dayforce，号码是有效还是已过期无关紧要。

#### <a name="bank-accounts-and-disbursements"></a>银行帐户和付款

必须为选择通过银行转账付薪的员工输入有效的银行帐户信息。

| Talent                         | Dayforce                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| 银行帐号（必填） |                                                                                                             |
| SWIFT 代码（必填）          | 在墨西哥处理工资单时使用的**银行 ID** 字段。                                                             |
| 分行编号（必填）       |                                                                                                             |
| 银行帐户类型（必填）   | 在墨西哥处理工资单时使用的**帐户类型**字段。 支持的值包括**支票**和**工资单**。 |

> [!NOTE]
> 选择通过银行转帐付薪的员工必须提供一个链接，该链接是主要地址在墨西哥且与墨西哥银行的有效银行帐户关联的法人名下的余额帐户。 将忽略其他所有非余额帐户。

#### <a name="address-information"></a>地址信息

每个员工必须有一个主要职位。 在 Dayforce 中，此职位用于确定员工的主要纳税地址。

- 主要（必填）
- 国家/地区（必填）
- 邮政编码（必填）
- 街道（必填）
- 街道号（必填）
- 建筑物地址
-  市/县（必填）
- 省/直辖市/自治区（必填）
- 国家/地区（必填）

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a>在美国和加拿大配置数据以生成工资单

如果要在美国和加拿大为员工生成付薪，必须配置以下元素：

- 需要职位的部门。
- 必须将成本中心设置为财务维度，并且成本中心必须为默认财务维度字符串的第一个元素。

> [!NOTE] 
> 可以配置 Talent，以便要求在“职位”中指定“部门”。 方法是，转到**人力资源共享职位 > 职位 > 必填职位中的部门**。 建议为集成实施此项设置。

### <a name="job-types"></a>工作类型

工作类型用于将类似的工作分组为类别。 要在美国和加拿大处理工资单，需要工作类型。 例如，工作类型包括全职和兼职，或按工资付薪和按小时付薪。 作业类型作为付薪类型映射到 Dayforce，用于指示员工按小时还是按工资付薪。

需要以下作业类型和描述。

| 工作类型   | 说明 |
|------------|-------------|
| 每小时     | 每小时      |
| 按工资   | 按工资    |

### <a name="position-types"></a>职位类型 

可使用职位类型描述职位是全职、兼职还是其他。 职位类型作为付薪类别映射到 Dayforce，用于指示员工是全职还是兼职。

需要以下职位类型和描述。

| 职位类型   | 说明        |
|-----------------|--------------------|
| 全职       | 全职员工 |
| 兼职       | 兼职员工 |

### <a name="reason-codes"></a>原因代码

原因代码提供有关员工状态的信息。 原因代码作为状态代码映射到 Dayforce，用于指示更改员工的职位或雇用状态的原因。

需要以下原因代码和描述。

| 原因代码    | 说明      | 适用的场景 |
|----------------|------------------|----------------------|
| RESIGNATION    | 辞职      | 解雇工作人员     |
| TERMINATION    | 终止      | 解雇工作人员     |
| RETIREMENT     | 退休       | 解雇工作人员     |
| OTHER          | 其他原因    | 解雇工作人员     |
| DEATH          | 死亡            | 解雇工作人员     |
| LEAVEOFABSENCE | 休假 | 解雇工作人员     |
| CONTRACTEND    | 合同结束  | 解雇工作人员     |
| SALARYCHANGE   | 工资改变 | 薪酬         |

### <a name="marital-status"></a>婚姻状况

婚姻状态值映射到 Dayforce，并在集成时根据需要转换为接受的值。

下表显示婚姻状态值如何映射到 Dayforce。

| Talent                 | Dayforce             |
|------------------------|----------------------|
| 已婚                | 已婚              |
| 单一                 | 单一               |
| 丧偶                | 丧偶              |
| 离异               | 离异             |
| 注册伴侣关系 | 民事结合关系 |
| None                   | None                 |
| 未婚同居             | 未婚同居           |

### <a name="gender"></a>性

性别指派映射到 Dayforce，并在集成时根据需要转换为接受的值。

下表显示性别指派如何映射到 Dayforce。

| Talent       | Dayforce        |
|--------------|-----------------|
| 男         | 男            |
| 女       | 女          |
| 非特定 | *不支持* |

### <a name="earning-codes"></a>收入代码

收入代码唯一标识工作人员获得的每种收入类型。 这些代码有多个与收入有关的参数，如会计规则、税法、报告要求和补偿费功能。 如果使用不受支持的频率，默认将使用**每个付薪**频率进行计算。

#### <a name="supported-frequencies"></a>支持的频率

- 所有
- EVERYPAY
- EACHPAYPERIOD
- EVRYOTHRPAYODD
- EVRYOTHRPAYEVN
- 1OFMTH
- LASTOFMTH
- 2OFMTH
- 3OFMTH
- 4OFMTH
- 5OFMTH
- 1N2OFMTH
- 3N4OFMTH
- 1N3OFMTH
- 1N4OFMTH
- 2N3OFMTH
- 2N4OFMTH
- 1N2N3OFMTH
- 1N2N4OFMTH
- 1N3N4OFMTH
- 2N3N4OFMTH
- 1N2N3N4OFMTH - 1N2N3N4OFMTH
- 2N3N4N5OFMth - 2N3N4N5OFMth
- 1OFQTR - 1OFQTR
- LASTOFQTR – LASTOFQTR
- LASTMTHOFQTR – LASTMTHOFQTR
- 1OFYEAR - 1OFYEAR
- LASTOFYEAR – LASTOFYEAR
- NOVNDECOFYEAR - NOVNDECOFYEAR

### <a name="addresses"></a>地址

特定国家或地区、省/直辖市/自治区和县/市（自治市）代码的标识需要 Dayforce 和国内/地区内提供商可识别的特定格式。 尽管县/市的格式可变，但是每个县/市必须与一个省/直辖市/自治区关联。

| Talent          | Dayforce              |
|-----------------|-----------------------|
| 国家/地区  | 国家/地区代码          |
| 邮政编码  | 邮政编码           |
| 状态           | 省/直辖市/自治区代码            |
| 城市            | 城市                  |
| 县          | 县（自治市） |
| 街道          | 地址行 1        |

### <a name="tax-regions"></a>税区

税区用于确定应在生成工资单期间应用的适当税费。 税区作为位置地址映射到 Dayforce。 默认税区必须与工作人员的活动职位关联。 

- 税区（必填）
- 国家/地区（必填）
- 省/直辖市/自治区（必填）
- 县 
-  市/县（必填）

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a>在墨西哥配置数据以生成工资单

如果要在墨西哥为员工生成付薪，必须配置以下元素：

- 需要职位的部门。
- 必须将成本中心设置为财务维度，并且成本中心必须为默认财务维度字符串的第一个元素。

### <a name="job-types"></a>工作类型

工作类型用于将类似的工作分组为类别。 在墨西哥需要工作类型才能处理工资单。 例如，工作类型包括全职和兼职，或按工资付薪和按小时付薪。 作业类型作为付薪类型映射到 Dayforce，用于指示员工按小时还是按工资付薪。

需要以下作业类型和描述。

| 工作类型   | 说明 |
|------------|-------------|
| 每小时     | 墨西哥按小时   |
| 按工资   | 墨西哥按工资 |

### <a name="position-types"></a>职位类型 

可使用职位类型描述职位是全职、兼职还是其他。 职位类型作为付薪类别映射到 Dayforce，用于指示员工是全职还是兼职。

需要以下职位类型和描述。

| 职位类型   | 说明        |
|-----------------|--------------------|
| 全职       | 全职员工 |
| 兼职       | 兼职员工 |

### <a name="reason-codes"></a>原因代码

原因代码提供有关员工状态的信息。 原因代码作为状态代码映射到 Dayforce，用于指示更改员工的职位或雇用状态的原因。

需要以下原因代码和描述。

| 原因代码            | 说明                    | 适用的场景 |
|------------------------|--------------------------------|----------------------|
| DEPARTUREBEFOREPAYMENT | 首次付薪前离职 | 解雇工作人员     |
| RESIGNATION            | 辞职                    | 解雇工作人员     |
| PENSION                | 退休金                        | 解雇工作人员     |
| TERMINATION            | 终止                    | 解雇工作人员     |
| 退休             | 退休                     | 解雇工作人员     |
| ABSENTEE               | 缺勤者                       | 解雇工作人员     |
| OTHER                  | 其他原因                  | 解雇工作人员     |
| CLOSURE                | 停业               | 解雇工作人员     |
| DEATH                  | 死亡                          | 解雇工作人员     |
| LEAVEOFABSENCE         | 休假               | 解雇工作人员     |
| CONTRACTEND            | 合同结束                | 解雇工作人员     |
| SALARYCHANGE           | 工资改变               | 薪酬         |

### <a name="terms-of-employment"></a>雇用条款

雇用条款用于创建雇用条款的类别。 这些条款作为雇用指标值映射到 Dayforce。

需要以下雇用条款和描述。

| 雇用条款   | 说明 |
|-----------------------|-------------|
| 常规               | 常规     |
| 直接                | 直接      |
| 实习            | 实习  |
| 永久             | 永久   |

### <a name="marital-status"></a>婚姻状况

婚姻状态值映射到 Dayforce，并在集成时根据需要转换为接受的值。

下表显示婚姻状态值如何映射到 Dayforce。

| Talent                 | Dayforce                  |
|------------------------|---------------------------|
| 已婚                | 已婚                   |
| 单一                 | 单一                    |
| 丧偶                | 丧偶                   |
| 离异               | 离异                  |
| 注册伴侣关系 | 民事结合关系      |
| None                   | *墨西哥不支持* |
| 未婚同居             | *墨西哥不支持* |

### <a name="gender"></a>性

性别指派映射到 Dayforce，并在集成时根据需要转换为接受的值。

下表显示性别指派如何映射到 Dayforce。

| Talent       | Dayforce                  |
|--------------|---------------------------|
| 男         | 男                      |
| 女       | 女                    |
| 非特定 | *墨西哥不支持* |

### <a name="payment-method"></a>付款方式

付款方式为员工和公司提供描述如何向员工付款的方式。 付款方式映射到 Dayforce，并在集成时根据需要转换为接受的值。

下表显示付款方式如何映射到 Dayforce。

| Talent             | Dayforce                  |
|--------------------|---------------------------|
| 现金               | 现金                      |
| 电子支付 | 转移                  |
| 检查              | 支票                    |
| 银行汇票         | *墨西哥不支持* |
| 其他              | *墨西哥不支持* |

### <a name="bank-account-type"></a>银行帐户类型

银行帐户类型用于对员工进行电子付款。 银行账户类型作为转帐信息映射到 Dayforce。 集成时，银行帐户类型根据需要转换为接受的值。

| Talent            | Dayforce                  |
|-------------------|---------------------------|
| 支票帐户  | CheckingAccount           |
| 工资单帐户   | PayrollAccount            |
| 储蓄帐户   | *墨西哥不支持* |
| BankGirot 帐户 | *墨西哥不支持* |
| PlusGirot 帐户 | *墨西哥不支持* |

### <a name="earning-codes"></a>收入代码

收入代码唯一标识工作人员获得的每种收入类型。 这些代码有多个与收入有关的参数，如会计规则、税法、报告要求和补偿费功能。 如果使用不受支持的频率，默认将使用**每个付薪**频率进行计算。

#### <a name="supported-frequencies"></a>支持的频率

- 所有
- EVERYPAY
- EACHPAYPERIOD
- EVRYOTHRPAYODD
- EVRYOTHRPAYEVN
- 1OFMTH
- LASTOFMTH
- 2OFMTH
- 3OFMTH
- 4OFMTH
- 5OFMTH
- 1N2OFMTH
- 3N4OFMTH
- 1N3OFMTH
- 1N4OFMTH
- 2N3OFMTH
- 2N4OFMTH
- 1N2N3OFMTH
- 1N2N4OFMTH
- 1N3N4OFMTH
- 2N3N4OFMTH
- 1N2N3N4OFMTH - 1N2N3N4OFMTH
- 2N3N4N5OFMth - 2N3N4N5OFMth
- 1OFQTR - 1OFQTR
- LASTOFQTR – LASTOFQTR
- LASTMTHOFQTR – LASTMTHOFQTR
- 1OFYEAR - 1OFYEAR
- LASTOFYEAR – LASTOFYEAR
- NOVNDECOFYEAR - NOVNDECOFYEAR

### <a name="addresses"></a>地址

特定国家或地区、省/直辖市/自治区和县/市（自治市）代码的标识需要 Dayforce 和国内/地区内提供商可识别的特定格式。 尽管县/市的格式可变，但是每个县/市必须与一个省/直辖市/自治区关联。

| Talent              | Dayforce              |
|---------------------|-----------------------|
| 国家/地区      | 国家/地区代码          |
| 邮政编码      | 邮政编码           |
| 状态               | 省/直辖市/自治区代码            |
| 城市                | 城市                  |
| 县              | 县（自治市） |
| 街道              | 地址行 1        |
| 街道编号       | 地址行 2        |
| 建筑物地址 | 地址行 5        |

### <a name="passport-number"></a>护照号

员工可以声明护照信息。 此信息的身份证明类型为**护照**，并作为员工的墨西哥特定信息的一部分集成到 Dayforce 中。

- 身份证明类型 =“护照”
- 签发日期
- 到期日期

员工可以声明**护照**身份证明类型的多个身份证明编号。 但是，仅将当前有效的护照条目集成到 Dayforce 中。 如果所有护照条目均已过期，将把最近签发的护照集成到 Dayforce 中。

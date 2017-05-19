---
title: "登记 ID"
description: "本主题提供有关设置和使用登记 ID 的信息。"
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DirPartTaxRegistrationSearch, LogisticsPostalAddress, TaxRegistrationLegislationTypes, TaxRegistrationType
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 264824
ms.assetid: e86f0a35-be58-4ef5-b5ab-bcfc495eaa13
ms.search.region: Global
ms.author: vlru
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 712eb9ec22f4eea4a969a7bd23b7d3728b35772e
ms.contentlocale: zh-cn
ms.lasthandoff: 04/25/2017


---

# <a name="registration-ids"></a>登记 ID

[!include[banner](../includes/banner.md)]


本主题提供有关设置和使用登记 ID 的信息。

大多数国家和地区对记录登记编号或 ID 有不同的法规和要求。 本主题提供欧洲不同国家/地区各方支持的登记类型的所需设置和处理概览。 对于支持与不同政府提供的登记编号有关的各种国家/地区特定的功能，所有国家/地区都有自己的要求。 例如，登记编号包括社会安全号 (SSN)、税务识别号码 (TIN) 和欧洲 VAT 标识 (EU VAT ID)。 此功能为所有需要满足某些欧洲国家国家特定的要求的所有区域中的国家/地区提供统一的框架。 以下章节介绍用于设置和处理登记 ID 的整体信息流。

## <a name="registration-type-creation"></a>创建登记类型
在您可以输入登记 ID，必须为每个当事方设置登记编号的不同类型的登记类型。 转至**组织管理** &gt; **全球通讯簿** &gt; **登记类型** &gt; **登记类型**页面，以便为不同国家/地区的供应商、客户、工作人员和法人创建和管理登记类型。

|字段                 |说明      |
|------------------------------|----------------------------|                                                                           
| 姓名                | 登记类型的名称。 |                                                                           
| 说明         | 登记类型的描述。 |
| 国家/地区      | 国家/地区的唯一标识符。|
| 税务主管机构       | 与登记类型关联的税务主管机构。|
| 限制为       | 应用于登记类型的限制类型：无、人员、组织。|
| 格式              | 登记类型的验证格式。|
| 可进行更新      | 定义登记类型的登记编号在输入后是否可更新。|
| 唯一              | 定义登记类型的登记编号是否唯一。 |
| 国家/地区的主要地址 | 如果一个当事方与特定国家/地区的一个或多个地址关联，并且登记 ID 对所有这些地址都有效，则必须将一个地址指定为这个国家/地区的主地址。 只能将一个 ID 登记为主地址。 定义是否只能为国家/地区地址的主地址输入登记编号。 |

## <a name="assign-a-registration-type-to-a-registration-category"></a>为登记类别指定登记类型
登记类别是为了出于税务、海关和其他目的在特定国家/地区批准的国家/地区登记标识符。 此类别定义不同报表中特定注册 ID（包括校验位等）和包含登录 ID 的验证规则。 使用页面**组织管理** &gt; **全球通讯簿** &gt; **登记类型** &gt; **登记类别**为支持的登记类别分配特定国家/地区的登记类型。

| 字段            | 说明|
|-----------------------|----------------|
| 登记类型     | 特定国家/地区的登记类型。|
| 限制为         | 应用于登记类型的限制类型：无、人员、组织。|
| 登记类别 | 批准在这个国家/地区中使用的唯一登录标识符。 下面是 AX7.1 类别中支持的完整列表。 |

## <a name="enter-registration-ids-for-global-address-book-records"></a>输入全球通讯簿记录的登录 ID
Microsoft Dynamics 365 for Operations 中的全球通讯簿 (GAB) 包含客户、供应商、联系人、业务关系和法人的统一地址格式。 有关详细信息，请参阅[全球通讯簿概览](/dynamics365/operations/organization-administration/overview-global-address-book)。 存储在全球通讯簿中的当事方记录可能包含一个或多个地址记录。 这些地址用于多种目的，例如记帐或交运。 可以为客户、供应商、工作人员和法人的地址信息设置登记 ID。 找到要为其输入登记 ID 的当事方（法人、供应商、客户、工作人员）记录，然后在与当事方、法人、供应商、客户、工作人员有关的窗体上单击**登记 ID** 打开**管理地址**页面。 在**税务登记**选项卡上，单击**添加**，然后输入有关登记 ID 的以下信息。

|字段                |说明                                                |
|---------------------|-----------------------------------------------------------|
| 登记类型   | 选定国家/地区的登记类型。     |
| 登记编号 | 当事方登记 ID。                                |
| 说明         | 登记编号的描述。               |
| 部分             | 有关登记编号的更多信息。 |
| 签发机构      | 颁发登记编号的主管机构。        |
| 签发日期         | 登记编号的颁发日期。              |
| 生效           | 登记编号的生效日期。           |
| 到期          | 登记编号的到期日期。          |

> [!NOTE]
> 可以从与 VAT ID 有关的登记 ID 选择并为当事方输入法人、供应商和客户的免税编号。

## <a name="search-for-records-by-registration-id"></a>按登记 ID 搜索记录
可从与当事方、法人、供应商、客户和工作人员有关的窗体中基于登记 ID 搜索当事方记录。 单击**登记 ID 搜索**打开**登记 ID 搜索条件**页面。 指定搜索条件并单击**查找**。 系统将显示全球通讯簿中选择的记录和关联的当事方记录类型。

## <a name="supported-registration-categories"></a>支持的登记类别
下表列出了 Dynamics 365 for Operations 中支持的登记类型。 如果您熟悉登记 ID 的 Microsoft Dynamics AX 2012 字段，此表还将这些字段映射到 Dynamics 365 for Operations 登记类别。

| Dynamics 365 for Operations Registration 类别         |国家/地区  | Dynamics AX 2012 术语/字段|
|---------------------------------------------------------------|---------------------|---------------------------------|
| 增值税 ID                                                        | 所有欧盟 (EU) 国家/地区|  免税编号（AX2012 R3 中的立法类型 TAX ID）|
| 企业 ID (COID)                                          | 比利时 捷克共和国 爱沙尼亚 匈亚利 拉脱维亚 立陶宛 波兰 瑞士 | 企业编号 (EnterpriseNumber) 登记编号 (RegNum\_W) 登记编号 (RegNum\_W) 登记编号 (RegNum\_W) 登记编号 (RegNum\_W) 企业代码 (EnterpriseCode) 登记编号 (RegNum\_W) UID（AX2012 R3 中的立法类型 UID） |
| 分支 ID                                                     | 比利时            | 分公司编号 (BranchNumber)|
| Spisová značka（登记编号、颁发机构、部门） | 捷克共和国     | 插页编号 (CommercialRegisterInsetNumber) 保留在商业登记簿中 (CommercialRegister) 商业登记簿的部分 (CommercialRegisterSection)|
| 海关客户 ID                                           | 芬兰 | 海关客户编号 (CustomsCustomerNumber\_FI)|
| INN                                                           | 俄罗斯联邦| INN（AX2012 R3 中的立法类型 INN）|
| RRC                                                           | 俄罗斯联邦| RRC（AX2012 R3 中的立法类型 RRC）|
| OKDP                                                          | 俄罗斯联邦| OKDP（AX2012 R3 中的立法类型 OKDP）|
| OKPO                                                          | 俄罗斯联邦| OKPO（AX2012 R3 中的立法类型 OKPO）|
| RCOAD                                                         | 俄罗斯联邦| RCOAD（AX2012 R3 中的立法类型 RCOAD）|
| OGRN                                                          | 俄罗斯联邦| OGRN（AX2012 R3 中的立法类型 OGRN） |
| SNILS                                                         | 俄罗斯联邦| SNILS（AX2012 R3 中的立法类型 SNILS）|
| CIFTS                                                         | 俄罗斯联邦| CIFTS（AX2012 R3 中的立法类型 CIFTS）|

有关登记 ID 处理的详细信息（包括必须满足的先决条件），请参阅 Lifecycle Services (LCS) 中 VAT ID 的以下任务录制：

-   设置增值税 ID
-   供应商的 VAT ID 登记
-    使用增值税 ID 搜索当事方






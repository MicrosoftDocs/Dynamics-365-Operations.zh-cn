---
title: "登记 ID"
description: "此主题提供有关设置和使用收银机 ID 的信息。"
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
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 32cd09975861083b8940368ed53ae16e89bcd748
ms.lasthandoff: 03/31/2017


---

# <a name="registration-ids"></a>登记 ID

此主题提供有关设置和使用收银机 ID 的信息。

许多国家/地区和地区有不同的规则和要求。记录登记编号或 ID。 此主题。当事方提供必需设置和流程概览支持不同类型的登记的欧洲国家/地区/地区。 所有国家/地区有其支持不同国家/地区特定功能的需求与不同的状态 Office 提供的登记编号。 登记编号，包括社会保险号 (SSN)，纳税标识号 (TIN)) 和增值欧洲税收标识 (增值税欧盟 ID) 的示例。 此功能。所有国家/地区提供统一的框架将在考虑到某些欧洲国家/地区的国家/地区特定要求的所有区域。 以下各节介绍为设置和处理登记的 ID 使用的完整信息流。

## <a name="registration-type-creation"></a>创建登记类型
在您可以输入登记 ID，必须先设置收银机编号不同登记类型{{支配：subject_to}}为要求逆向每个当事方。 **转到组织管理** &gt; **全球通讯簿** &gt; **登记类型** &gt; ** **登记类型创建和管理供应商、客户、工作人员和法人的登记类型的页面处于不同的国家/地区。

|字段                 |说明      |
|------------------------------|----------------------------|                                                                           
| 姓名                | 登记类型的名称。 |                                                                           
| 说明         | 登记类型的描述。 |
| 国家/地区      | 国家/地区的唯一标识符。|
| 税务主管机构       | 与登记类型的税务主管机构。|
| 限制为       | 应用于登记类型的税限制类型："无，负责人，组织。|
| 格式              | 登记验证类型的格式。|
| 可进行更新      | 定义，则登记类型的登记编号可以更新，然后输入该密钥后。|
| 唯一              | 则登记类型的登记编号都是唯一的，定义的时间。 |
| 国家/地区的主要地址 | 如果当事方特别是与一个或多个地址国家/地区，和 ID 地址所有这些登记为有效，您必须指定一主要用于地址为该国家/地区。 只能登记一个 ID 根据是主工序。 如果登记编号，可以仅对主输入国家/地区的地址，定义的时间。 |

## <a name="assign-a-registration-type-to-a-registration-category"></a>登记分配登记类别类型。
类别是登记国家/地区。特别是使用国家/地区的标识符审核登记税、自定义和其他目的。 此类别定义特定登记 ID (包括校验位等) 和登记包括 ID 验证规则在不同的报告。 **使用页面组织管理** &gt; **全球通讯簿** &gt; **登记类型** &gt; **类别**登记分配特定国家/地区类型登记到登记支持的类别。

| 字段            | 说明|
|-----------------------|----------------|
| 登记类型     | 登记类型特别是国家/地区。|
| 限制为         | 这限制适用于税登记类型："无，负责人，组织。|
| 登记类别 | 用于审核登记唯一标识符的国家/地区。 完整列表支持在 AX7.1 类别。 |

## <a name="enter-registration-ids-for-global-address-book-records"></a>为全球通讯簿记录的登记 ID
全球通讯簿 (GAB) 在工序 (GAB) 的 Microsoft Dynamics 中包含供应商、客户、联系人、业务关系和法人的合并的地址信息。 有关详细信息，请参阅"概览 [] (全球通讯簿/dynamics365/operations/organization 全局 administration/overview 地址帐簿)。 在全球通讯簿中的方记录可能包含一个或多个地址记录。 这些地址用于多种目的，例如记帐或交运。 您可以设置地址信息的登记 ID 客户、供应商、员工和法人的。 查找当事方 (法人，供应商，则客户，工作人员) 记录要输入登记 ID，然后单击窗体上登记** ** ID 关联集会，法律实体，供应商，则客户，请打开**管理地址**页面的工人。 **在税登记** "选项卡上，单击"添加** **，并输入有关登记的 ID 以下信息。

|字段                |说明                                                |
|---------------------|-----------------------------------------------------------|
| 登记类型   | 登记类型中所选国家/地区。     |
| 登记编号 | 该当事方登记 ID。                                |
| 说明         | 登记编号的描述。               |
| 部分             | 有关登记编号的其他信息。 |
| 签发机构      | 颁发登记编号的主管机构。        |
| 签发日期         | 登记编号的发货日期。              |
| 生效           | 登记编号的生效日期。           |
| 到期          | 登记编号的到期日期。          |

> [!NOTE]
> 法律实体，供应商，则客户免税编号可以从为该方与增值税和 ID 输入选择登记的 ID。

## <a name="search-for-records-by-registration-id"></a>搜索登记的记录 ID。
基于登记的记录 ID 的当事方搜索可用的法人，关联的窗体集会、供应商、客户和工作人员。 **打开**登记 ID 搜索条件**页面**单击搜索登记的 ID。 指定搜索条件后依次单击** **查找。 系统将查看从全球通讯簿的所选记录和与当事方记录的类型。

## <a name="supported-registration-categories"></a>支持的登记类别
下表列出了支持 365 Dynamics 中的登记类型的操作。 如果您熟悉 Microsoft Dynamics AX 2012 为登记，此表 ID 字段还这些表字段。工序登记类别的 Dynamics 365。

| 登记工序类别的 Dynamics 365         |国家/地区  | 条款/字段 Dynamics AX 2012|
|---------------------------------------------------------------|---------------------|---------------------------------|
| 增值税 ID                                                        | 欧盟 (EU) 的所有国家/地区|  免税编号 (在 AX2012 R3 的法定税收 ID 类型)|
| 企业 ID (COID)                                          | 捷克比利时爱沙尼亚匈牙利拉脱维亚立陶宛波兰瑞士 | 企业编号 (EnterpriseNumber 登记编号) (RegNum\_) W 登记编号 (RegNum\_) W 登记编号 (RegNum\_) W 登记编号 (RegNum\_企业 W) 代码 (EnterpriseCode 登记编号) (RegNum\_W) (UID 在 AX2012 R3 的法定 UID 类型) |
| 分支 ID                                                     | 比利时            | 分公司编号 (BranchNumber)|
| Spisová (登记编号，značka 颁发机构，部分中) | 捷克共和国     | 插页编号) (CommercialRegisterInsetNumber 了在剩余商业登记 (CommercialRegisterSection) 的商业登记 (CommercialRegister) 件|
| 海关客户 ID                                           | 芬兰 | 自定义客户编号 (CustomsCustomerNumber\_FI)|
| 客栈                                                           | 俄罗斯联邦| (客栈 AX2012 R3 的法律客栈类型)|
| RRC                                                           | 俄罗斯联邦| RRC (在 AX2012 R3 的法定 RRC 类型)|
| OKDP                                                          | 俄罗斯联邦| OKDP (在 AX2012 R3 的法定 OKDP 类型)|
| OKPO                                                          | 俄罗斯联邦| OKPO (在 AX2012 R3 的法定 OKPO 类型)|
| RCOAD                                                         | 俄罗斯联邦| RCOAD (在 AX2012 R3 的法定 RCOAD 类型)|
| OGRN                                                          | 俄罗斯联邦| OGRN (在 AX2012 R3 的法定 OGRN 类型) |
| SNILS                                                         | 俄罗斯联邦| SNILS (在 AX2012 R3 的法定 SNILS 类型)|
| CIFTS                                                         | 俄罗斯联邦| CIFTS (在 AX2012 R3 的法定 CIFTS 类型)|

有关处理，包括必需的必备登记 ID 的详细信息，为税收 ID 投入使用的增值 Lifecycle Services (LCS) 参阅以下任务记录：

-   设置增值税 ID
-   增值税登记供应商的 ID。
-    使用增值税 ID 搜索当事方




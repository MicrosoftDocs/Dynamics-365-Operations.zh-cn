---
title: 配置生活事件类型
description: Microsoft Dynamics 365 Human Resources 使用生命事件类型来定义对更新员工福利登记有效的事件。
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
ms.openlocfilehash: 8b1d911fcd86b91b96edb1bdf42316c9097ea8bc
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092629"
---
# <a name="configure-life-event-types"></a>配置生活事件类型

[!include [banner](includes/preview-feature.md)]

Microsoft Dynamics 365 Human Resources 使用生命事件类型来定义对更新员工福利登记有效的事件。 例如，结婚或生子。 每个生命事件类型 ID 只能与一个生命事件类型相关联。 例如，如果您创建与生命事件类型“员工地址更改”相关联的名为“地址更改”的生命事件 ID，您将无法创建另一个标注为“员工地址更改”的 ID 并将其与生命事件类型“员工地址更改”相关联。 

创建生命事件类型后，需要将它们与计划类型相关联。 有关详细信息，请参阅[创建计划类型](hr-benefits-setup-plan-types.md)。

   > [!NOTE]
   > 创建生命事件时，需要将其与计划类型相关联。 有关详细信息，请参阅[创建计划类型](hr-benefits-setup-life-event-types.md)。

## <a name="create-a-life-event-type"></a>创建生命事件类型

1. 在**福利管理**工作区中，在**设置**下，选择**生命事件类型**。

2. 选择**新建**。

3. 为以下字段指定值：

   | 字段 | 说明 |
   | --- | --- |
   | 生命事件类型 ID | 生命事件类型的唯一标识符。 |
   | 说明 | 生命事件类型的描述。 |
   | 生命事件类型 | 促进更新员工福利登记的催化剂。 有关生命事件的列表，请参阅下面的[生命事件](hr-benefits-setup-payment-frequencies.md?life-events)。 |

4. 选择**保存**。

## <a name="view-attached-plans"></a>查看附加的计划

您可以查看附加到所选生命事件类型的计划的列表。 生命事件将附加到计划类型，计划类型将与计划相关联。 

1. 在**福利管理**工作区中，在**设置**下，选择**生命事件类型**。

2. 选择**操作**。

3. 选择**附加的计划**。

## <a name="life-events"></a>生命事件

创建生命事件类型时，可以从以下生命事件中进行选择：

| 生命事件 | 场所 | 触发器 |
| --- | --- | --- |
| 婚姻状况更改 | 工作人员 > 个人资料 > 个人信息 > 婚姻状况| 婚姻状况的更改 |
| 就业状况更改 | <ul><li>工作人员 > 雇用</li><li>雇用历史记录页面</li></ul> | 就业状况的更改 |
| 员工地址更改 | <ul><li>工作人员 > 个人资料 > 地址 </li><li>工作人员 > 个人信息 > 个人联系人 > 地址</li></ul> 已经添加、编辑或删除的地址 |
| 依赖方更改 | <ul><li>工作人员 > 个人资料 > 个人信息 > 个人联系人 > 添加或删除依赖方</li><li>员工自助服务</li></ul> | 已添加或删除的依赖方。 个人联系人关系必须是子女、配偶、家庭伴侣或前配偶。 更新**生效日期**日期将触发生命事件。 如果您不更新该日期，将不会触发生命事件。 |
| 出生或收养(依赖方) | <ul><li>工作人员 > 个人资料 > 个人信息 > 个人联系人 > 依赖方详细信息</li><li>员工自助服务</li></ul> | **收养日期**字段已填充。 子女的出生日期是必填项。 |
| 覆盖范围缺失(配偶/家庭伴侣) | 工作人员 > 个人资料 > 个人信息 > 个人联系人 > 依赖方详细信息 > 覆盖范围缺失 | 为个人联系人选择的**覆盖范围缺失**，以及**生效日期** |
| 国内合作伙伴雇用变动 | 工作人员 > 个人资料 > 个人信息 > 个人联系人 > 依赖方详细信息 > 已雇用。 | <ul><li>依赖方详细信息已创建，**个人联系人已雇用**框 = 是</li><li>**个人联系人已雇用**框已更改（是或否）</li></ul> |
| 休假(配偶/家庭伴侣) | 工作人员 > 个人资料 > 个人信息 > 个人联系人 > 依赖方详细信息 > 休假 | <ul><li>依赖方详细信息已创建，**EhrLOAEffectiveDate** 已填充</li><li>**personPrivateDetails.EhrIsLOA** 已更改（是或否）</li><li>**personPrivateDetails.EhrLOAEffectiveDate** 已更改</li></ul> |
| 覆盖范围(职位)更改 | <ul><li>工作人员 > 职位分配 > 工作人员职位分配</li><li>职位 > 职位</li></ul> | <ul><li>对工作人员职位分配记录中的职位的更改</li><li>职位中工作人员分配的更改</li></ul> |
| 覆盖范围(薪金)更改 | 工作人员 > 薪酬 > 固定计划 | 更改薪酬时，年度福利薪金将自动重新计算 |
| 医疗保险(员工/依赖方) | 工作人员 > 个人资料 > 个人信息 > 个人联系人 > 依赖方详细信息 > 医疗保险生效日期 | 当个人联系人输入生效日期时，不会自动触发。 |
| 法院裁定的支持 | 工作人员 > 个人资料 > 个人信息 > 个人联系人 > 依赖方 > 法院裁定的支持（QMSCO/QDRO 和生效日期 | 不触发任何自动更新。 不影响资格；记录生命事件。 |
| 死亡 | 工作人员 > 个人资料 > 个人信息 > 死亡日期 | 死亡日期已输入 |
| 保险证明 | <ul><li>工作人员 > 工作人员 > 版本 > 雇用历史记录 > 日期管理器 > 福利详细信息</li><li> 工作人员 > 雇用 > 福利详细信息 > 验证日期</li></ul> | <ul><li>工作人员输入验证日期</li><li>工作人员将 EvidenceOfInsurability 字段设置为**是**</li></ul> |
| 受益人 | 工作人员 > 个人资料 > 个人信息 > 个人联系人 | 个人联系人已添加，**受益人**框和**生效日期**已填充。 个人联系人必须为 **Child**、**Spouse**、**DomesticPartner**、**Sibling**、**FamilyContact**、**OtherContact**、**Parent**、**BeneficiaryEstate**、**BeneficiaryOrg** 或 **BeneficiaryTrust** 类型。 |
| 员工医疗保险 | 工作人员 > 工作人员 > 版本 > 雇用历史记录 > 日期管理器 > 福利详细信息 | <ul><li>**EhrMedicareEligibilityDate** 已更改</li><li>**MedicareEligibile** 设置为**是**</li></ul> |
| 生日 | 工作人员 > 个人资料 > 个人信息 > 个人联系人 > 依赖方详细信息 > 出生日期 | 出生日期已添加或更新（不是在生命事件更改处理之后）。 示例：如果子女的**个人联系人资格选项**在“设置 > 福利 > 个人联系人资格选项”中设置为“年龄：26”，并且 HR 人员在依赖方年满 26 岁后的任何一天运行生命事件更改处理，则会出现一条消息，提醒他们依赖方不再符合覆盖范围的条件。 |
| 工作人员资格更改（不特定于美国） | <ul><li>工作人员 > 雇用</li><li>工作人员 > 工作人员 > 版本 > 雇用历史记录</li></ul> | <ul><li>员工类型、雇用类别或五个用户可定义的资格字段更改</li><li>**HcmEmploymentDetail.EhrEmploymentType** 更改（仅为*已更改*的雇用详细信息记录进行了处理，未为*新*雇用记录处理，例如重新雇用和终止雇用）</li></ul> |
| 新资格覆盖（不特定于美国） | 人力资源(高级) > 福利 > 计划 > 福利 >资格规则覆盖 | 使用生命事件处理 | EhrBenefitEligibilityRuleOverride.ValidFrom |
| 资格规则覆盖更改（不特定于美国） | 人力资源(高级) > 福利 > 计划 > 福利 >资格规则覆盖 | 使用生命事件处理（仅捕获对资格规则覆盖上的 **ValidFrom** 和 **ValidTo** 字段的更改） |
| 资格规则覆盖到期（不特定于美国） | 人力资源(高级) > 福利 > 计划 > 福利 >资格规则覆盖 | 使用生命事件更改处理。 例如，如果您将计划的资格规则覆盖的到期日期编辑为今天下午 5:00、下午 5:00 以后的任何时间或之后的几天，然后运行生命事件更改处理，则会出现一条消息，显示资格规则覆盖已过期。 |
| 新福利计划（不特定于美国） | 人力资源(高级) > 福利 > 计划 > 新 | <ul><li>资格选项已添加到当前计划</li><li>附加了资格选项的新计划已添加</li></ul></br></br>HR 人员应在这种情况下运行生命事件资格处理。 |
| 资格规则更改（不特定于美国） | 人力资源(高级) > 福利 > 规则/选项 > 资格规则 | 使用生命事件资格处理。 记录了 **EhrBenefitEligibilityRule** 记录何时更改了以下值：**UseEmplCategory**、**UseEmplStatus** 或 **UseEmplType**。 仅更新已更改的规则或资格条件已存在的生效事件交易。 |

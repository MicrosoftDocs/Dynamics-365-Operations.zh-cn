---
title: 定义福利资格规则和策略
description: 本主题介绍如何创建福利资格规则和政策并将规则分配给福利。
author: twheeloc
ms.date: 08/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 4781a00ae63bb2d27df0610a1886cc43e52798f9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861180"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a>定义福利资格规则和策略


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本文介绍如何创建福利资格规则和政策并将规则分配给福利。  

## <a name="create-benefit-eligibility-policy-rule-type"></a>创建福利资格政策规则类型

1. 转到 **人力资源 > 福利 > 资格 > 福利资格政策规则类型**。
2. 选择 **新建**。
3. 在 **规则名称** 字段中，输入一个值。
4. 在 **描述** 字段中，输入一个值。
5. 在 **查询名称** 字段中，选择下拉按钮打开查找。
6. 在列表中，选择所选择行中的链接。
7. 选择 **保存**。
8. 关闭该页面。

## <a name="benefit-eligibility-policy"></a>福利资格策略

1. 转到 **人力资源 > 福利 > 资格 > 福利资格政策**。
2. 选择一个现有的福利政策。
3. 在列表中，选择所选择行中的链接。
4. 切换 **政策组织** 部分的扩展。 您可以添加或删除您想要加入政策内的所有组织。
5. 展开或折叠 **策略规则** 部分。
6. 在列表中，查找并选择以前创建的政策规则。
7. 选择 **创建策略规则**。
8. 在 **生效日期** 字段中，输入您希望政策开始生效的日期。
    * 如果您希望这些更改生效，则设置有效截止日期，以允许您以后对政策规则作出更改，而无需返回到政策。  
9. 如果需要，在 **添加条件** 字段中添加 where 子句。
    * 例如，如果您希望规则仅适用于销售经理，您可以创建 where 子句进行规定：Where 职位描述等于销售经理。 您可以在规则中一起添加多个 where 语句。  
10. 选择 **确定**。
11. 关闭该页面。

## <a name="assign-rule-to-benefit"></a>分配福利规则

1. 转到 **人力资源 > 福利 > 福利**。
2. 在列表中，找到并选择所需记录。
3. 在列表中，选择所选择行中的链接。
4. 展开或折叠 **资格规则** 部分。
5. 选择 **编辑**。
6. 在 **资格** 字段中，选择规则。
7. 在 **规则类型** 中，查找并选择以前创建的规则。
9. 在列表中，选择所选择行中的链接。
10. 选择 **保存**。
11. 关闭窗体。



[!INCLUDE[footer-include](../includes/footer-banner.md)]

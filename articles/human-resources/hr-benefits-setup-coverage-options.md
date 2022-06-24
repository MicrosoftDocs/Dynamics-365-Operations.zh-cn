---
title: 创建覆盖范围选项
description: 本文介绍 Microsoft Dynamics 365 Human Resources 中的覆盖范围选项，这些选项供参与者在福利计划或项目中进行选择。
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8569cabf72871396b9935a14a5637e5e645705fb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848214"
---
# <a name="create-coverage-options"></a>创建覆盖范围选项


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

覆盖范围选项确定谁应该被范围，或者保险计划中有多少可用覆盖范围。 例如，对于医疗计划，您可能有 **仅员工** 选项、**员工 + 1** 选项和 **家庭** 选项。 对于人寿保险，您可以提供 **1 x 薪水** 或 **2 x 薪水** 覆盖范围。

定义福利覆盖选项后，您可以重复使用它们。 可以将一个选项与一个或多个计划关联。

> [!IMPORTANT]
> 定义覆盖范围选项后，将选项附加到福利计划类型中。 然后计划类型将与福利计划或项目关联。 与计划类型相关联的覆盖范围选项可用于创建的类型的所有计划。

## <a name="create-coverage-options"></a>创建覆盖范围选项
1. 在 **福利管理** 工作区中，在 **设置** 下，选择 **覆盖范围选项**。

2. 选择 **新建**。

3. 为以下字段指定值：

   | 字段 | 说明 |
   | --- | --- |
   | **覆盖范围选项** | 唯一的覆盖范围选项名称。 |
   | **说明** | 覆盖范围选项的描述。 |
   | **覆盖范围代码** | 覆盖范围代码为每个合格的已覆盖人员类型分配最小和最大金额。 覆盖范围代码指示某计划类型覆盖哪些人员以及允许的覆盖范围金额。 您可以用美元金额或百分比表示覆盖范围金额。 例如:<ul><li>**Emp+1** – 要取得资格，员工必须选择一个依赖方（如果选择了多个，将不再具有资格）。</li><li>**Emp+家庭** – 要取得资格，员工必须至少选择两个依赖方。</li></ul> |
   | **最大数** | 最大依赖方数。 |
   | **状态** | 覆盖范围选项的状态。 如果覆盖范围选项的状态设置为 **无效**，则不能在计划类型上选择该覆盖范围选项。 |
   | **百分比** | 百分比金额。 仅当在“覆盖范围代码”字段中选择了“% x 薪金”时，此字段才有效。 |
   | **除数** | 选择覆盖范围代码 % x 薪金时要在计算中使用的除数。 |
   | **最小百分比** | 选择百分比覆盖范围代码时的最小百分比。 |
   | **最大百分比** | 选择百分比覆盖范围代码时的最大百分比。 |

4. 在 **个人联系人资格选项** 下，将合适的个人联系人资格选项附加到每个覆盖范围选项中。

5. 在 **自助服务** 下，为以下字段指定值：

   | 字段 | 说明 |
   | --- | --- |
   | **允许员工缴纳金额** | 指定是否允许员工在选择福利时在福利自助服务中修改缴纳金额。 如果选中此复选框，系统将根据员工在福利自助服务中输入的缴纳金额来计算福利计划参数。 |
   | **允许员工覆盖范围金额** | 指定是否允许员工在选择福利时在福利自助服务中修改覆盖范围金额。 如果选中此复选框，系统将根据员工在福利自助服务中输入的覆盖范围金额来计算福利计划参数。 |

6. 选择 **保存**。 


[!INCLUDE[footer-include](../includes/footer-banner.md)]

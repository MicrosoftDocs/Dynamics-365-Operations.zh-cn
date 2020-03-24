---
title: 创建覆盖范围选项
description: Microsoft Dynamics 365 Human Resources 中的覆盖范围选项是供参与者在福利计划或项目中选择的覆盖范围级别，例如医疗计划的“仅限员工”，或人寿保险计划的“2x 薪金”。
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
ms.openlocfilehash: 0af2b6ae0853b4c7f64c4d4f04299c87089d622b
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092698"
---
# <a name="create-coverage-options"></a>创建覆盖范围选项

[!include [banner](includes/preview-feature.md)]

Microsoft Dynamics 365 Human Resources 中的覆盖范围选项是供参与者在福利计划或项目中选择的覆盖范围级别，例如医疗计划的“仅限员工”，或人寿保险计划的“2x 薪金”。 定义后，覆盖范围选项可以重复使用，您可以将一个选项与一个或多个计划相关联。

定义覆盖范围选项后，将覆盖范围选项附加到福利计划类型中。 然后计划类型将与福利计划或项目关联。 与计划类型相关联的覆盖范围选项可用于使用该计划类型创建的所有计划。 

1. 在**福利管理**工作区中，在**设置**下，选择**覆盖范围选项**。

2. 选择**新建**。

3. 为以下字段指定值：

   | 字段 | 说明 |
   | --- | --- |
   | **覆盖范围选项** | 唯一的覆盖范围选项名称。 |
   | **说明** | 覆盖范围选项的描述。 |
   | **覆盖范围代码** | 覆盖范围代码为每个合格的已覆盖人员类型分配最小和最大金额。 覆盖范围代码指示某计划类型覆盖哪些人员以及允许的覆盖范围金额。 您可以用美元金额或百分比表示覆盖范围金额。 例如:</br></br>- **Emp+1** – 要取得资格，员工必须选择一个依赖方（如果选择了多个，将不再具有资格）。</br></br>- **Emp+家庭** – 要取得资格，员工必须至少选择两个依赖方。 |
   | **最大数** | 最大依赖方数。 |
   | **状态** | 覆盖范围选项的状态。 如果覆盖范围选项的状态设置为“无效”，则不能在计划类型上选择该覆盖范围选项。 |
   | **百分比** | 百分比金额。 仅当在“覆盖范围代码”字段中选择了“% x 薪金”时，此字段才有效。 |
   | **除数** | 选择覆盖范围代码 % x 薪金时要在计算中使用的除数。 |
   | **最小百分比** | 选择百分比覆盖范围代码时的最小百分比。 |
   | **最大百分比** | 选择百分比覆盖范围代码时的最大百分比。 |

4. 在**个人联系人资格选项**下，将合适的个人联系人资格选项附加到每个覆盖范围选项中。

5. 在**自助服务**下，为以下字段指定值：

   | 字段 | 说明 |
   | --- | --- |
   | **允许员工缴纳金额** | 指定是否允许员工在选择福利时在福利自助服务上修改缴纳金额。 如果选中此复选框，系统将根据员工在福利自助服务中输入的缴纳金额来计算福利计划参数。 |
   | **允许员工覆盖范围金额** | 指定是否允许员工在选择福利时在福利自助服务上修改覆盖范围金额。 如果选中此复选框，系统将根据员工在福利自助服务中输入的覆盖范围金额来计算福利计划参数。 |

6. 选择**保存**。 

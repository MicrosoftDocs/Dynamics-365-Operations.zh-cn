---
title: 创建工作时间日历
description: 在 Dynamics 365 Human Resources 中定义工作时间日历、假日和非工作时间。
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2bedbe65f146c4159c2a809de8f683815fd4a01f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417438"
---
# <a name="create-a-working-time-calendar"></a>创建工作时间日历

Dynamics 365 Human Resources 中的工作时间日历显示员工在您的组织中工作的天数和时数。 当员工提交休息时间请求时，他们不必担心假日和歇业的影响。

要简化休息时间请求，请为您的组织配置以下项目：

- 工作时间日历
- 假日和歇业
- 非工作时间

您可以在设置工作时间日历时添加最后两个项目。 您还可以单独配置或更新它们。

## <a name="set-up-a-working-time-calendar"></a>设置工作日历

设置至少一个工作时间日历，以显示您的工作天数和时数。 如果您在多个国家和地区设有分点，您可能需要为每个区域设置工作时间日历。

1. 在 **组织管理** 页面上，选择 **日历**。

2. 选择 **新建**，然后为日历输入名称和说明。

3. 在 **生成选项** 下，为您的组织选择工作日，然后输入工作时间。 
   - 要添加假日和歇业，请选择 **假日和歇业** 旁边的 **添加** 按钮。
   - 要添加非工作时间（例如午餐或工间休息），请选择 **非工作时间** 下的 **添加** 并输入名称和时间范围。

4. 在 **天数** 下，选择 **生成** 以生成日历中包含的天数。 为日历输入日期范围，然后选择 **生成日**。

5. 要添加工作计划，在 **工作计划** 下，选择 **添加**，然后输入每个工作计划的时间。

## <a name="configure-holidays-and-closures"></a>配置假日和歇业

您可以从工作时间日历单独添加或更改假日和歇业。

1. 在 **组织管理** 页面上，选择 **假日和歇业**。

2. 选择 **新建**，然后为假日和歇业输入名称和日期。

## <a name="configure-non-work-time"></a>配置非工作时间

您可以从工作时间日历单独添加或更改非工作时间。

1. 在 **组织管理** 页面上，选择 **非工作时间**。

2. 选择 **新建**，然后为非工作时间输入名称和时间范围。

如果已启用“休假和缺勤银行假日更正”预览功能，Human Resources 将使用假日和歇业日期来确定要为日历中登记的员工调整的天数。

## <a name="see-also"></a>请参阅

- [休假和缺勤概览](hr-leave-and-absence-overview.md)
- [配置休假和缺勤类型](hr-leave-and-absence-types.md)

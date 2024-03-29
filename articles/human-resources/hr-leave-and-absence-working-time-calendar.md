---
title: 创建工作时间日历
description: 在 Dynamics 365 Human Resources 中定义工作时间日历、假日和非工作时间。
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dac3ad583be9e4cbd6eacbc6d228819bd298628b
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2022
ms.locfileid: "9323535"
---
# <a name="create-a-working-time-calendar"></a>创建工作时间日历


[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]

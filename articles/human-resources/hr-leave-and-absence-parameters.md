---
title: 配置休假和缺勤参数
description: 在 Dynamics 365 Human Resources 中定义休假和缺勤的人力资源参数。
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
ms.openlocfilehash: 2acb8502ebcab122a0a1ff21e9f5e23931026327
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008205"
---
# <a name="configure-leave-and-absence-parameters"></a>配置休假和缺勤参数

在您在 Dynamics 365 Human Resources 中设置休假和缺勤计划之前，最好先验证所有相关的人力资源参数的设置，包括：

- 休假请求的编号规则
- 家庭医疗休假法 (FMLA) 设置
- 休假和缺勤请求的员工自助服务设置
- 休假和缺勤参数

## <a name="view-and-change-human-resources-parameters"></a>查看和更改人力资源参数

1. 在**休假和缺勤**页面，选择**链接**选项卡。

2. 在**设置**下，选择**人力资源参数**。

3. 在**编号规则**选项卡上，验证**休假请求 ID** 的**编号规则代码**并根据需要进行更改。 此设置确定用于向休假请求自动分配 ID 的顺序。

4. 在 **FMLA** 选项卡上，验证 FMLA 设置并根据需要进行更改。

5. 在**员工自助服务**选项卡上，指示经理是否可以代表员工输入休假和缺勤请求。

6. 在**休假和缺勤**选项卡上，验证设置并根据需要进行更改。

7. 选择**保存**。

## <a name="configure-calendar-parameters"></a>配置日历参数

如果启用了休假和缺勤日历预览功能，您需要配置其他参数。 

[!include [banner](includes/preview-feature-leave-absence.md)]

> [!NOTE]
> 对于 2020 年 2 月 3 日的预览版本，仅启用了**等待处理的休假请求**。

1. 在**休假和缺勤**页面，选择**链接**选项卡。

2. 在**设置**下，选择**人力资源参数**。

3. 在**日历**选项卡上，根据需要更改日历设置。

4. 选择**保存**。

## <a name="see-also"></a>请参阅

- [休假和缺勤概览](hr-leave-and-absence-overview.md)

---
title: 工资单集成参数
description: 本文介绍了 Dynamics 365 Human Resources 工资单集成参数。
author: marcelbf
ms.date: 06/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-17
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7d784909fc8c5fa05557566b62b19802cd2acece
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896088"
---
# <a name="payroll-integration-parameters"></a>工资单集成参数


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

在使用 Dynamics 365 Human Resources 工资单集成之前，必须如本文中所述设置参数。

## <a name="enable-payroll-address"></a>启用工资单地址

为了能够使用工资单地址，必须在工资单集成选项卡上从[共享参数窗体](hr-setup-shared-parameters.md)中启用它。

## <a name="define-the-identification-type"></a>定义标识类型

若要在[工资单员工实体](hr-admin-integration-payroll-api-payroll-employee.md)中公开标识类型，必须为每个公司[配置人力资源参数](hr-setup-shared-parameters.md)。

1. 在 **薪酬管理** 工作区中，在链接下，选择 **人力资源参数**。 
2. 在 **工资单集成** 选项卡商，指定以下字段的值。

| 字段 | 说明 |
| --- | --- |
| 在处理工资单时使用标识类型 | 选择此选项后，所选类型 ID 将显示在工资单员工实体中。 |
| 标识类型 | 要在 [工资单员工实体](hr-admin-integration-payroll-api-payroll-employee.md)的 **mshr_payrollemployeeentityid** 字段中公开的标识类型。 |

## <a name="see-also"></a>请参阅

[工资单集成 API 简介](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

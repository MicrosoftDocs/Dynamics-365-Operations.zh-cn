---
title: 其他货位区域
description: 本主题概述已向 Microsoft Dynamics 365 Supply Chain Management 添加的新货位区域。
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationBuild
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: c0bed8c95760b3dee350048c5f824f974b784f26
ms.sourcegitcommit: 7b7cc93c0f78c6bfc7a3ea66a74a29ba0f218553
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/04/2020
ms.locfileid: "3658326"
---
# <a name="additional-location-zones"></a>其他货位区域

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management 中新增了三个区域字段。 仓库经理可将其用于定义更多仓库组织或布局。 可以手动或通过使用**货位设置**向导设置新区域字段。 可以在任何使用“货位”表的查询或筛选中使用这些字段。

无需进行更多设置即可使用区域字段。

## <a name="turn-on-the-additional-location-zone-feature"></a>开启“其他货位区域”功能

*其他货位区域*功能只有在系统中开启之后才能使用。 管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能（如果需要）。 在**功能管理**工作区中，此功能按照下面的方式列出：

- **模块**：*仓库管理*
- **功能名称**：*其他货位区域*

## <a name="use-location-zones"></a>使用货位区域

1. 转到**仓库管理 \> 设置 \> 仓库 \> 货位设置向导**。
2. 设置以下值：

    - 在**仓库**字段中，选择 _62_。
    - 在**区域 ID** 字段中，选择 _FLOOR_。
    - 在**其他区域 1** 字段中，选择 _PICKZONE1_。
    - 在**其他区域 2** 字段中，选择 _WEBSHOP1_。
    - 在**货位模板 ID** 字段中，选择 _FLOOR_。

3. 选择**场地**行。
4. 在**起始编号**字段中，输入 _1_。 在**结束编号**字段中，输入 _3_。
5. 选择**通道**行。
6. 在**起始编号**字段中，输入 _1_。 在**结束编号**字段中，输入 _5_。
7. 选择**创建**。
8. 将收到消息，说明已添加了新货位。 选择**显示消息**按钮查看消息。
9. 转到**仓库管理 \> 设置 \> 仓库 \> 货位**。 将在列表中显示新货位，并且可使用所有区域字段（即，现有区域字段和新的其他区域字段）。

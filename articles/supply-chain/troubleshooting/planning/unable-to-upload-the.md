---
title: 导入需求预测记录时，无法更新预测的单位成本
description: 当您使用数据实体导入需求预测记录时，现有记录的成本价不会更新，以与导入的数据匹配。
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c8ea8322a6c7bafe2dfcaaee3e9989f753c85e2a
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026307"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a>导入需求预测记录时，无法更新预测的单位成本

知识库编号：4614109

## <a name="symptoms"></a>故障特征

当您使用数据实体导入需求预测记录时，现有记录的 **预测单位成本** 值不会更新，以与导入的数据匹配。

## <a name="cause"></a>原因

**预测单位成本** 是一个只读字段。 此值基于产品单位成本，不能直接通过导入设置。

## <a name="resolution"></a>解决方法

由于此字段是只读字段，因此您无法导入此字段的值。 此值将根据现有业务逻辑计算得出。

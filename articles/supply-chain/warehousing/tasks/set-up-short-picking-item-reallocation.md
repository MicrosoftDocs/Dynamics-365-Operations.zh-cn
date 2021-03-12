---
title: 设置领料短缺的物料重新分配
description: 此主题显示如何启用仓库工作人员，以便在为其指示的货位的库存不足时，快速找到备用货位。
author: ShylaThompson
manager: tfehr
ms.date: 06/29/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker, WHSLocationWithWorkException
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab8baf846d65e6fefe9ca575b5af5a2dbceac666
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976880"
---
# <a name="set-up-short-picking-item-reallocation"></a>设置领料短缺的物料重新分配

[!include [banner](../../includes/banner.md)]

此过程显示如何启用仓库工作人员，以便在为其指示的货位的库存不足时，快速找到备用货位。 

重新分配过程由 **工作异常** 控制，由仓库 **工作人员** 使用。

可以使用自动和/或手动重新分配流程：

- 自动重新分配 - 货位指令用于确定另一个货位是否提供这些货物。 如果可以，将更新工作，并将仓库用户定向到备用货位。
- 手动重新分配 - 允许仓库用户在拥有未预留货物数量的一个或多个货位中进行选择。 
- 自动加手动 - 如果系统无法执行自动重新分配，并且有货位具有未预留数量，将提示用户选择货位。

## <a name="set-up-work-exceptions"></a>设置工作异常
可以使用不同物料重新分配策略定义多个工作异常，以便让仓库工作人员可以根据处理的装运需求选择一个。

创建此过程时使用的是 USMF 演示数据格式。

1. 在 **导航窗格** 中，转到 **仓库管理 > 设置 > 工作 > 工作异常**。
2. 单击 **新建** 
3. 在 **工作异常代码** 字段中，键入一个值。 这将是此异常的标题。 例如，“手动领料短缺”。
4. 在 **描述** 字段中，键入一个值。 这将是此异常的使用情况简短说明。 例如，“领料短缺 - 物料不可用”。
5. 在 **异常类型** 字段中，选择 **领料短缺**。
6. 选中 **调整库存** 复选框。 如果选中，领料短缺货位自动将库存调整为 0。
7. 在 **默认调整类型代码** 字段中，输入或选择一个值。 例如，在 USMF 中，可以选择 **删除 Res Adj Out**。每个调整类型代码中包含四个特征：名称、说明、库存日记帐名称和 **删除预留**。 如果启用了 **删除预留**，将删除领料短缺行的预留。  
8. 在 **物料重新分配** 字段中，选择一个值，如“手动”。 如果选择“手动”或“自动和手动”，需要启用仓库工作人员才能使用手动重新分配。

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a>设置工作人员以使用物料手动重新分配

创建此过程时使用的是 USMF 演示数据格式。

1. 关闭该页面。
2. 在 **导航窗格** 中，转到 **仓库管理 > 设置 > 工作人员**。
3. 单击 **编辑**。
4. 在列表中，选择工作人员。 例如，Julia Funderburk。
5. 展开 **用户** 快速选项卡。
6. 在列表中选择一个 **用户 ID**。 例如，24。
7. 展开 **工作** 快速选项卡。
8. 在 **允许手动重新分配物料** 字段中选择 **是**。

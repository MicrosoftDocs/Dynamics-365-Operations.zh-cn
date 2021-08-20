---
title: 工作订单类型
description: 本主题介绍资产管理中的工作订单类型。
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderType
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d77effbfe329a449318d6942918245917f22cdc23defadcb5e85f02c6c786f6d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6754720"
---
# <a name="work-order-types"></a>工作订单类型

[!include [banner](../../includes/banner.md)]

 

工作订单类型用于为工作订单归类。 例如，您可能有与预防性维护或修复性维护有关的工作订单。

工作订单类型定义与工作订单生命周期模型之间的隶属关系。 工作订单生命周期模型定义可为工作订单设置的工作订单生命周期状态。 （工作订单生命周期状态示例包括 **已创建**、**进行中** 和 **已完成**。）

有关工作订单生命周期状态和项目阶段的详细信息，请参阅[工作订单生命周期状态](work-order-lifecycle-states.md)。

1. 选择 **资产管理** \> **设置** \> **工作订单** \> **工作订单类型**。
2. 选择 **新建** 以创建新的工作订单类型。
3. 在 **工作订单类型** 字段中，输入工作订单类型的 ID。
4. 在 **名称** 字段中输入名称。
5. 在 **工作订单生命周期模型** 字段中选择生命周期模型。
5. 如果应该将与此类型的工作订单关联的所有工作订单作业安排给同一位维护工人，请将 **一位维护工人** 选择为 **是**。
6. 根据需要在 **成本类型** 字段中选择 **纠正**、**预防性** 或 **投资**。 一个工作订单的所有工作订单作业具有相同的成本类型。
7. 在 **必需** 部分中，将相关选项设置为 **是**，以便指定向此类型的工作订单添加哪些与故障有关或与维护停机时间有关的信息。

    > [!NOTE]
    > **必需** 部分中的选项与 **工作订单生命周期状态** 页（**资产管理** \> **设置** \> **工作订单** \> **生命周期状态**）的 **验证** 快速选项卡上的选项有关。

8. 选择 **保存**。

![工作订单类型。](media/16-setup-for-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
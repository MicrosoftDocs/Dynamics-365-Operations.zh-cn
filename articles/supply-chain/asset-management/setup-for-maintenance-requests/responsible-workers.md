---
title: 负责的维护工人
description: 本主题说明如何在资产管理中设置负责的维护工人。
author: josaw1
manager: tfehr
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b5f83474e56c996a40bdbdf7d3a7c8d495429c6
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208930"
---
# <a name="responsible-maintenance-workers"></a>负责的维护工人

[!include [banner](../../includes/banner.md)]

 

可以将负责的维护工人与资产类型、资产、功能位置、维护作业类型类别、维护作业类型、维护作业类型变体和贸易关联。 可以在工作订单和维护请求中使用，以指示与应负责工作订单的维护工人有关的偏好。 （但是，这些维护工人不必是安排来履行工作订单的同一位工人。）此功能为可选功能。 例如，可用于为特定工作类型或工作领域选择负责的工人或工人组。

工作订单生命周期或维护请求生命周期期间，可以更改或更新负责的维护工人。 例如，可以将此更改或更新与维护请求生命周期状态或工作订单生命周期状态的更改关联。

安排工作订单期间，*不*使用**负责的维护工人**页上的设置。

> [!NOTE]
> 在资产管理中，也可以设置安排工作订单期间可以分配给工人的*首选*维护工人。

设置负责的维护工人之前，必须设置应该可供选择的工人和维护工人组。 有关如何设置工人和维护工人组的信息，请参阅[维护工人和工人组](../setup-for-objects/workers-and-worker-groups.md)。

## <a name="set-up-responsible-maintenance-workers"></a>设置负责的维护工人

1. 选择**资产管理** \> **设置** \> **工人** \> **负责的维护工人**。
2. 选择**新建**创建记录。
3. 首先创建默认负责的维护工人或负责的维护工人组设置，可在其中仅设置**负责的维护工人组**字段和/或**负责的工人**字段。 将其余字段保留为空。 如果在安排工作订单期间没有其他更具体的组合与工作订单的内容匹配，将使用这个默认设置。

    > [!NOTE]
    > 创建维护请求期间，**所有维护请求**页中有负责的维护工人或负责的维护工人组可供选择时，资产管理将浏览所有负责的维护工人记录以检查可能的匹配项。 始终先检查最具体的组合。 换句话说，资产管理首先会检查**贸易**字段的匹配项。 如果未找到匹配项，将检查**维护作业类型变体**字段的匹配项。 如果未找到匹配项，将检查**维护作业类型**字段的匹配项，以此类推。 您可以在页面的布局中看到，此行为意味着，为了查找最具体的组合，资产管理将从右到左检查每个记录以查找匹配项（依次检查**贸易**、**维护作业类型变体**、**维护作业类型**、**维护作业类型类别**、**功能位置**、**资产**，最后检查**资产类型**）。 如果未找到匹配项，将使用这七个字段中无可供选择的内容的默认记录。

下图显示**负责的维护工人**页的示例。

![负责维护工人页面](media/08-setup-for-requests.png)

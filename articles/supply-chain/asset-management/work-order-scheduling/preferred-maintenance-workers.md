---
title: 设置首选维护工作人员
description: 本文说明如何在资产管理中设置首选维护工人。
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkerPreferred
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 72f545b952e72412fc05239ed90e2cbbf2c11437
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846233"
---
# <a name="set-up-preferred-maintenance-workers"></a>设置首选维护工人

[!include [banner](../../includes/banner.md)]

在工作订单计划期间，您可以优先选择要分配哪个维护工人或工作人员组来完成工作订单。 此功能为可选功能，但是可帮助您根据工人技能和能力选择最有资格完成作业的维护工人。 将仅安排在安排时可用的维护工人。 如果安排期间某项首选维护工人设置与工作订单匹配，但是将该维护工人分配给了其他作业，将把工作订单安排给另一位可用维护工人。

在设置首选维护工人之前，必须首先设置维护工人和工作人员组。 有关如何设置维护工人和工作人员组的描述，请参阅[维护工人和工作人员组](../setup-for-objects/workers-and-worker-groups.md)。

## <a name="set-up-preferred-workers"></a>设置首选工人

可以将首选维护工人或工作人员组关联到以下一项或多项：

- 贸易  
- 维护作业类型变型  
- 维护作业类型  
- 维护作业类型类别  
- asset / 资产  
- 资产类型  

为同一条记录选择的越多，设置越具体。

1. 单击 **资产管理** > **设置** > **工人** > **首选维护工人**。

2. 单击 **新建** 创建一条新记录。

3. 首先创建一个“默认”维护工人或工作人员组。 这意味着仅在 **首选维护工人组** 字段或 **首选维护工人** 字段中进行选择。 下面屏幕截图中的示例显示，第一个记录中选择了“请求”来充当 **首选维护工人组**。

    > [!NOTE]
    > 如果在安排工作订单期间没有其他更具体的组合与工作订单的内容匹配，将使用默认设置。

4. 重复步骤 2 以创建新的记录。 进行所需选择，具体取决于首选工人或工人组的详细程度。 

    *示例：* 下面屏幕截图中的第六个记录内，选择了维护工人 Shawn Richardson 来充当首选工人。 安排包含资产“CH-BP1-03-02”和维护作业类型“设施评估”的工作订单时，如果他当时有空，将自动选择他。

    > [!NOTE]
    > 通常当在安排工作订单期间选择了首选维护工人时，资产将在所有 **首选维护工人** 记录中查找可能的匹配项，始终首先查找最具体的组合。 如果未找到匹配项，将使用在 **首选维护工人组** 字段或 **首选维护工人** 字段中进行了选择的“默认”记录。

![图 1.](media/02-work-order-scheduling.png)

也可以设置在创建维护请求或工作订单时可选择的 *负责* 维护工人。 如果需要，可在 **所有工作订单** 和 **所有维护请求** 中编辑所选内容。 有关详细信息，请参阅[负责维护工人](../setup-for-maintenance-requests/responsible-workers.md)。

安排工作订单期间，可以计算分数来确定哪些工人应完成与工作订单关联的作业（这些分数在 **资产管理参数** > **工作订单计划编制** 链接中设置）。 如果在安排工作订单期间两位或更多首选维护工人或负责的维护工人得到的分数相同，则随机选择一位工人。 否则，始终选择为其分配的分数最高的工人来完成工作订单。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
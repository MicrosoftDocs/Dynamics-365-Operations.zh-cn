---
title: 维护请求
description: 本主题概述资产管理中如何管理维护请求。
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 56d4abee451e6e22b9b9cc2fd36a13648202e7df
ms.sourcegitcommit: 871b76f8808a48d282f151144829323258ffc912
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/02/2019
ms.locfileid: "1847428"
---
# <a name="maintenance-requests"></a>维护请求

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

维护请求是为了在尚未创建工作订单的情况下通知经理或规划员需要执行维护或维修作业时，创建的注释或声明。 如果认为维护请求的内容有效，可以根据维护请求创建工作订单。

可以在资产管理中为任何资产创建维护请求。 可以根据公司使用维护请求的方式创建各种类型的维护请求。 下面举了一些示例加以说明：

- 维护请求
- 注释
- 更正或增强
- 投资
- 仓库维修（如果要接收来自其他位置的资产，以便执行维修或维护作业，在作业完成后退还资产，则使用此类型。）

## <a name="view-maintenance-requests"></a>查看维护请求

若要查看维护请求，请选择**资产管理** \> **常用** \> **维护请求** \> **所有维护请求**、**有效维护请求**或**我的功能位置维护请求**。 每个列表页显示与维护请求有关的部分信息。

![图 1](media/01-manage-maintenance-requests.png)

> [!NOTE]
> 使用**我的功能位置维护请求**列表页查看维护请求的列表，这些维护请求中包含您作为工人关联的功能位置或在此类功能位置安装的资产。 （有关如何为维护工人设置功能位置的信息，请参阅[维护工人和工人组](../setup-for-objects/workers-and-worker-groups.md)。）
> 
> 尽管客户帐户信息在资产服务管理（外部维护）中可用，但却在资产管理（内部维护）中不可用。

要打开记录的详细信息视图，请在**所有维护请求**列表页的网格视图中，选择**维护请求**列中的链接。

![图 2](media/02-manage-maintenance-requests.png)

操作窗格上的按钮排列在选项卡上。 下表简述与资产管理有关的按钮。

| 按钮名称                      | 说明 |
|----------------------------------|-------------|
| 编辑​​                             | 编辑所选维护请求。 |
| 新                              | 创建新的维护请求。 |
| 删除                           | 删除所选维护请求。 |
| 工作订单池                  | 将所选维护请求连接到工作订单池。 |
| 工作订单                       | 基于所选维护请求创建工作订单。 |
| 资产故障                      | 单击**资产故障**，可在其中为所选维护请求创建故障登记。 |
| 工作订单                      | 显示与所选维护请求相连的所有工作订单的列表。 |
| 更新维护请求状态 | 更新维护请求的状态。 |
| 生命周期状态日志              | 查看日志，其中显示所选维护请求的生命周期状态。 |
| 维护请求详细信息      | 打印报告，其中显示所选维护请求的详细信息。 |
| 发送出借资产                  | 选择应该用于临时替换所选维护请求中选择的资产的出借资产。 |
| 退还出借资产                | 将出借资产登记为已退回。 |


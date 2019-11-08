---
title: 创建维护请求
description: 本主题说明如何在资产管理中创建维护请求。
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
ms.openlocfilehash: 7fc9ec2f6a9a8a11d824e4b5c13d5aa173541454
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571913"
---
# <a name="create-maintenance-requests"></a>创建维护请求

[!include [banner](../../includes/banner.md)]

 

如果维护工人或生产工人发现需要维修设备，但是不能立即开展维修作业，可以使用维护请求。

**示例：** 一位维护工人正在进行维修，这时她发现必须维修同一位置的另一个资产。 但是，这位工人没有时间，或没有维修作业所需备件。 因此，她为该资产创建了维护请求，并输入了简短的问题说明。

Active maintenance requests section of the Related information pane on the right side of the **所有资产**或**有效资产**页面（**资产管理** \> **常用** \> **资产** \> **所有资产**或**有效资产**）右侧**相关信息**窗格的**有效维护请求**部分中显示与所选资产关联的有效维护请求。

1. 选择**资产管理** \> **常用** \> **维护请求** \> **所有维护请求**或**有效维护请求**。
2. 选择**新建**。
3. 在**创建请求**对话框的**维护请求类型**字段中，选择维护请求的类型。 将推荐默认类型。
4. 在**描述**字段中，输入用于简要描述维护请求的名称或标题。
5. 在**功能位置**和**资产**字段中，根据需要设置功能位置或资产，或功能位置和资产的组合。 创建维护请求时可以不选择资产，以后可以向该维护请求添加资产。 如果已登录的维护工人与该资产的关联资源有关，将自动设置**资产**字段。

    如果已经为所选资产关联了维护请求，将在**创建请求**对话框顶部显示消息栏，告知您现有维护请求的 ID。 消息栏该告知您该资产是否涵盖在某个保修协议内。

6. 在**服务级别**字段中，选择服务级别，用于指示请求的紧急程度。
7. 如果在步骤 5 中选择了资产，可使用**故障特征**、**故障区域**和**故障类型**字段创建故障登记。
8. 如果维护请求导致了维护停机时间，请输入停机时间的开始日期和时间。

    将把**启动人**字段自动设置为您的名称。

10. 将把**实际开始时间**字段自动设置为当前日期和时间。 但是，您可以根据需要更改此值。
11. 在**注释**字段中，输入所需的其他任何注释。
12. 选择**确定**。

![创建维护请求](media/03-manage-maintenance-requests.png)

## <a name="subsequent-processing-of-maintenance-requests"></a>维护请求的后续处理

创建维护请求之后，将其转化为工作订单之前，应该更新有关该维护请求的各种信息。 通常由规划员或其他管理员工完成此任务。

- 在**所有维护请求**或**有效维护请求**页，选择要处理的请求，然后选择**编辑**。

在详细信息视图中，可以更新各种信息。 下面举了一些示例加以说明：

- 选择并验证资产。 如果必须在以后选择其他资产，可以将**已验证资产**选项设置为**否**。
- 选择负责的维护工人组和/或负责的维护工人。 有关所需设置的详细信息，请参阅[负责的维护工人](../setup-for-maintenance-requests/responsible-workers.md)。
- 选择维护作业类型，并且如果此信息相关，则选择关联的维护作业变体和作业交易。
- 在**纬度**和**经度**字段中输入地理坐标。 将把向维护请求添加的所有坐标自动传输给关联的工作订单。 

![更新维护请求](media/04-manage-maintenance-requests.png)

> [!NOTE]
> 如果在创建维护请求时选择资产，则可向该资产添加一个故障。 创建维护请求之后，可以根据需要添加更多故障。 若要添加故障，请选择**所有维护请求**页中的**资产故障**。

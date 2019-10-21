---
title: 创建批处理作业
description: 批处理作业是提交到某一应用程序对象服务器 (AOS) 实例以供自动处理的一组任务。
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 27541c84a40fe9b7e7705162e06167ad4f7e4ed9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191377"
---
# <a name="create-a-batch-job"></a>创建批处理作业

[!include [task guide banner](../../includes/task-guide-banner.md)]

批处理作业是提交到某一应用程序对象服务器 (AOS) 实例以供自动处理的一组任务。 通过使用创建了该作业的用户的安全凭据来运行批处理作业。 使用以下过程来创建批处理作业。 创建此程序的演示数据公司是 USMF。


## <a name="create-the-batch-job"></a>创建批处理作业
1. 转到**导航窗格 > 模块 > 系统管理 > 查询 > 批处理作业**。
2. 单击**新建**。
3. 在**作业描述**字段中，键入一个值。
4. 在**计划开始日期/时间**字段中，输入日期和时间。
5. 单击**保存**。

## <a name="create-a-recurrence"></a>创建重复执行
1. 在操作窗格上，单击**批处理作业**。
2. 单击**重复执行**。 使用这些选项输入一个重复执行的范围和模式。  
3. 单击 **确定**。

## <a name="add-alerts"></a>添加预警
1. 在操作窗格上，单击**批处理作业**。
2. 单击**预警**。 指示批处理作业结束，出错或取消时是否希望发送预警消息。 然后指定是否要将预警显示为弹出消息。   
3. 单击 **确定**。

## <a name="adjust-batch-job-status"></a>调整批处理作业状态
1. 转到**系统管理 > 查询 > 批处理作业**。
2. 选择相应批处理作业。
3. 在操作窗格上，单击**批处理作业 > 功能 > 更改状态**。
4. 选择相应的状态：
    - **预扣**：将批处理作业设置为**预扣**，使其从批处理作业调度程序中扣除。 等同*停止*。
    - **等待**：将批处理作业设置为**等待**，使其等待批处理作业调度程序选取。 等同*执行*。
5. 单击 **确定**。

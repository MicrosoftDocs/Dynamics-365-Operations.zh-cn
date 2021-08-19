---
title: 波次不符合清理条件
description: 波次不符合清理条件
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWaveTable_WHSWaveProcessingDataCleanup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 99d76b6a90045be7630785769b11e43abaf4b789b1c4a134050b6ee396c71199
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778498"
---
# <a name="wave-isnt-eligible-for-cleanup"></a>波次不符合清理条件

错误代码：WaveNotEligibleForCleanup

## <a name="symptoms"></a>故障特征

系统将显示以下错误消息：

> 波次 %1 不符合清除条件。

波次数据无法清理。  

## <a name="cause"></a>原因

当前正在处理波次，如以下情况之一所示：

- **波次状态** 字段设置为 *正在执行*。
- 当您在操作窗格的 **波次** 选项卡上的 **波次** 组中选择 **批处理作业** 时，**状态** 字段未设置为 *已结束*、*错误* 或 *已取消*。 因此，批处理作业当前正在运行。

## <a name="resolution"></a>解决方法

在操作窗格上，在 **波次** 选项卡上，在 **波次** 组中，选择 **批处理作业**，然后执行以下步骤之一：

- 如果 **状态** 字段设置为 *正在执行*：在操作窗格上，在 **批处理作业** 选项卡上，在 **批处理作业** 组中，选择 **查看任务**。 您可以刷新 **批处理任务** 页来跟踪进度。
- 如果 **状态** 字段未设置为 *正在执行*：在操作窗格上，在 **批处理作业** 选项卡上，在 **功能** 组中，选择 **更改状态**。 在 **选择新状态** 字段中，选择 *正在等待*。 然后选择 **确定**。

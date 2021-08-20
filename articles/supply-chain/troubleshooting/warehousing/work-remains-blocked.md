---
title: 工作仍然处于锁定状态
description: 工作仍然处于锁定状态
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTableListPage_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 898390c78bb26fb8a44f77a10ad27a00720f7d1a3396cec5fff10e9d6b93364d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768562"
---
# <a name="work-remains-blocked"></a>工作仍然处于锁定状态

错误代码：WHSWorkBlockingExecutingWaveReason_ErrorMessage

## <a name="symptoms"></a>故障特征

系统将显示以下错误消息：

> 工作 %1 仍然受阻，因为相关波次 %2 的状态为 %3。

## <a name="cause"></a>原因

工作当前正在波次上处理，无法解锁，如以下情况之一所示：

- 在 **锁定原因** 选项卡上，一或多行的 **工作锁定原因** 字段设置为 *处理波次*。
- 当您在操作窗格的 **相关信息** 选项卡上的 **相关信息** 组中选择 **波次** 时，**波次状态** 字段将设置为 *正在处理*。

## <a name="resolution"></a>解决方法

在操作窗格的 **相关信息** 选项卡上的 **相关信息** 组中，选择 **波次**。 然后，在 **波次** 页上，在操作窗格上的 **波次** 选项卡上，在 **波次** 组中，选择 **清理波次数据**。

## <a name="workaround"></a>解决方法

如果上述步骤不能解决问题，您可以按照以下步骤取消工作。

1. 转到 **仓库管理 \> 定期任务 \> 清理 \> 取消工作**。
1. 在 **工作 ID** 字段中，指定您要取消的当前的 **工作状态** 值为 *打开*、*进行中*、*已取消*、*已合并* 或 *已关闭* 的工作的 ID。
1. 选择 **确定**。
1. 选择 **是** 确认要取消该工作。

有关详细信息，请参阅[取消要进行异常处理的仓库工作](../../warehousing/cancel-warehouse-work.md)。

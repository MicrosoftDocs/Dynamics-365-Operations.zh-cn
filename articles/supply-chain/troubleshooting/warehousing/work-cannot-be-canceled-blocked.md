---
title: 工作已被锁定，无法取消
description: 工作已被锁定，无法取消
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a7ab4c7263947767164702fb7dd6da7573175253
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924271"
---
# <a name="work-cant-be-canceled-because-its-blocked"></a>工作已被锁定，无法取消

错误代码：WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage

## <a name="symptoms"></a>故障特征

系统将显示以下错误消息：

> 工作 %1 无法取消，因为它由原因类型 %2 锁定。 必须先解锁该工作，然后才能取消。

## <a name="cause"></a>原因

工作已被锁定，无法取消。

在 **工作** 页上的 **常规** 选项卡上，**已锁定** 选项设置为 *是*。 此设置指示工作已被锁定。 **锁定原因** 选项卡显示为何工作被锁定。

## <a name="resolution"></a>解决方法

要解锁工作，选择 **锁定原因** 选项卡，然后按照下列步骤之一操作：

- 如果 **工作锁定原因** 字段设置为 *未定义原因*：在操作窗格的 **工作** 选项卡上，在 **工作** 组中，选择 **解锁工作**。
- 如果 **工作锁定原因** 字段设置为 *处理波次*：在操作窗格的 **相关信息** 选项卡上，在 **相关信息** 组中，选择 **波次**。 然后，在 **波次** 页上，在操作窗格上的 **波次** 选项卡上，在 **波次** 组中，选择 **清理波次数据**。

## <a name="workaround"></a>解决方法

如果上述步骤不能解决问题，您可以按照以下步骤取消工作。

1. 转到 **仓库管理 \> 定期任务 \> 清理 \> 取消工作**。
1. 在 **工作 ID** 字段中，指定您要取消的当前的 **工作状态** 值为 *打开*、*进行中*、*已取消*、*已合并* 或 *已关闭* 的工作的 ID。
1. 选择 **确定**。
1. 选择 **是** 确认要取消该工作。

有关详细信息，请参阅[取消要进行异常处理的仓库工作](../../warehousing/cancel-warehouse-work.md)。

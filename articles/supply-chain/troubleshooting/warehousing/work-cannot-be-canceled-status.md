---
title: 工作由于其状态无法取消
description: 工作由于其状态无法取消
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f983501b490c5516525b4d5904603ed62e8799f9e6124e5672b36a12804ecb0a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755970"
---
# <a name="work-cant-be-canceled-because-of-its-status"></a>工作由于其状态无法取消

错误代码：WAX2190

## <a name="symptoms"></a>故障特征

系统将显示以下错误消息：

> 无法取消工作 %1，因为其状态为 %2。

## <a name="cause"></a>原因

工作无法在当前状态下取消。

工作标头或工作行没有预期的 **工作状态** 值。 工作标头上的 **工作状态** 字段未设置为 *打开* 或 *进行中*。

## <a name="resolution"></a>解决方法

要取消工作，请按照下列步骤操作。

1. 转到 **仓库管理 \> 定期任务 \> 清理 \> 取消工作**。
1. 在 **工作 ID** 字段中，指定要取消的工作的 ID。
1. 选择 **确定**。
1. 选择 **是** 确认要取消该工作。

有关详细信息，请参阅[取消要进行异常处理的仓库工作](../../warehousing/cancel-warehouse-work.md)。

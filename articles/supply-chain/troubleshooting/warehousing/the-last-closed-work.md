---
title: 最后关闭的工作行必须为“放置”
description: 最后关闭的工作行必须为“放置”
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
ms.openlocfilehash: 221c64c89d0e8addbf44acab8e7561e5f3a27239
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474740"
---
# <a name="the-last-closed-work-line-must-be-a-put"></a>最后关闭的工作行必须为“放置”

错误代码：WAX1285

## <a name="symptoms"></a>故障特征

系统将显示以下错误消息：

> 最后关闭的工作行必须为“放置”。

## <a name="cause"></a>原因

工作无法在当前状态下取消。

在最后一个工作行上，**工作状态** 字段设置为 *已关闭*，但 **工作类型** 字段未设置为 *放置*。

## <a name="resolution"></a>解决方法

要取消工作，请按照下列步骤操作。

1. 转到 **仓库管理 \> 定期任务 \> 清理 \> 取消工作**。
1. 在 **工作 ID** 字段中，指定要取消的工作的 ID。
1. 选择 **确定**。
1. 选择 **是** 确认要取消该工作。

有关详细信息，请参阅[取消要进行异常处理的仓库工作](../../warehousing/cancel-warehouse-work.md)。

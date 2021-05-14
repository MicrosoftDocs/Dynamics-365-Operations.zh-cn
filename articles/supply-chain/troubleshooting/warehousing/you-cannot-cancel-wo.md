---
title: 您无法取消用户正在进行的工作
description: 您无法取消用户正在进行的工作
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
ms.openlocfilehash: e5f6912cfb1d5be8e46b7989856af99f8a611c11
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924393"
---
# <a name="you-cant-cancel-work-that-is-on-a-user"></a>您无法取消用户正在进行的工作

错误代码：WAX708

## <a name="symptoms"></a>故障特征

系统将显示以下错误消息：

> 无法取消用户正在进行的工作。

## <a name="cause"></a>原因

工作已被用户锁定，无法取消。 要确认这一点，打开工作 ID，然后打开 **常规** 选项卡。如果工作被锁定，**工作状态** 字段将设置为 *进行中*，**锁定者** 字段将设置为用户 ID。

## <a name="resolution"></a>解决方法

要取消工作，请按照下列步骤操作。

1. 转到 **仓库管理 \> 定期任务 \> 清理 \> 取消工作**。
1. 在 **工作 ID** 字段中，指定要取消的工作的 ID。
1. 选择 **确定**。
1. 选择 **是** 确认要取消该工作。

有关详细信息，请参阅[取消要进行异常处理的仓库工作](../../warehousing/cancel-warehouse-work.md)。

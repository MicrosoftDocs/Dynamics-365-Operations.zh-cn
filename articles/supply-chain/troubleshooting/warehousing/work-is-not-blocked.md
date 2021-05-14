---
title: 工作未锁定
description: 工作未锁定
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d64ab282972e46e8857581b59e5705dd15667328
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924196"
---
# <a name="work-isnt-blocked"></a>工作未锁定

错误代码：WHSUnblockNotBlockedWorkErrorMessage

## <a name="symptoms"></a>故障特征

系统将显示以下错误消息：

> 未锁定 ID 为 %1 的工作。

## <a name="cause"></a>原因

波次上的 **锁定波次** 选项设置为 *否*。 工作无法解锁，因为其当前未被锁定。

## <a name="resolution"></a>解决方法

 仅 **锁定波次** 选项设置为 *是* 的工作可以解锁。

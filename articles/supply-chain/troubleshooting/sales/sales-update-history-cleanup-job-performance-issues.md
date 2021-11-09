---
title: 销售更新历史记录清理作业失败或存在性能问题
description: 如果存在大量的销售更新数据，则销售历史记录清理批处理作业可能会失败或花费很长时间。
author: myvakalo
ms.date: 10/05/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 4f04dc204c705b40ed25fadc75118feaef4d6b6e
ms.sourcegitcommit: 42bd701179e664947b6eafcd1804c83a5e64abcb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2021
ms.locfileid: "7641447"
---
# <a name="sales-update-history-cleanup-job-fails-or-has-performance-issues"></a>销售更新历史记录清理作业失败或存在性能问题

## <a name="symptoms"></a>故障特征

**销售更新历史记录清理** 批处理作业失败或存在性能问题。  

## <a name="cause"></a>原因

当您的系统包含大量销售更新时，可能会发生这种情况，这可能会导致大量的销售更新数据。 清理作业尝试在一个交易中清理所有这些数据。 因此，该作业可能需要很长的运行时间，甚至可能会失败。

## <a name="resolution"></a>解决方法

新版本的 **销售更新历史记录清理** 批处理作业适用于 Supply Chain Management 版本 10.0.19 及更高版本。 默认情况下未启用此功能。 有关其工作方式以及如何在功能管理中启用它的详细信息，请参阅[销售历史记录清理性能改进](../../sales-marketing/sales-update-history-cleanup-performance-improvements.md)。

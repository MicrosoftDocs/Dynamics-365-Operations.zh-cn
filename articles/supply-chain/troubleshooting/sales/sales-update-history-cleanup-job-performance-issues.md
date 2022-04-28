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
ms.openlocfilehash: 124fb90ecafd4f4cccbd8a8bb443694c95365732
ms.sourcegitcommit: 197e6ddee84522fd587c6e4ee4f9089101e301c2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2022
ms.locfileid: "8570301"
---
# <a name="sales-update-history-cleanup-job-fails-or-has-performance-issues"></a>销售更新历史记录清理作业失败或存在性能问题

## <a name="symptoms"></a>故障特征

**销售更新历史记录清理** 批处理作业失败或存在性能问题。  

## <a name="cause"></a>原因

当您的系统包含大量销售更新时，可能会发生这种情况，这可能会导致大量的销售更新数据。 清理作业尝试在一个交易中清理所有这些数据。 因此，该作业可能需要很长的运行时间，甚至可能会失败。

## <a name="resolution"></a>解决方法

新版本的 **销售更新历史记录清理** 批处理作业适用于 Supply Chain Management 版本 10.0.19 及更高版本。 此功能默认情况下不打开。 有关其工作方式以及如何在功能管理中启用它的详细信息，请参阅[计划销售历史记录数据清理](../../sales-marketing/sales-update-history-cleanup-performance-improvements.md)。


---
title: 选择新批次 ID 时，批处理号被清除
description: 在查看领料单日记帐行时，如果在“批次 ID”字段中选择新值，“批处理号”字段中的值将被清除。
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: datra
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 71977a04adb066a8b51c9bf7b8c5a4e752ca902e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026288"
---
# <a name="batch-number-is-cleared-when-a-new-lot-id-is-selected"></a>选择新批次 ID 时，批处理号被清除

知识库编号：4613107

## <a name="symptoms"></a>故障特征

在查看领料单日记帐行时，如果在 **批次 ID** 字段中选择新值，**批处理号** 字段中的值将被清除。

## <a name="resolution"></a>解决方法

此系统行为是有意设计的。 如果更改批次 ID，将更改物料上下文。 因此，批处理号将重置。

要将批处理号与批次 ID 关联，必须首先设置批次 ID。

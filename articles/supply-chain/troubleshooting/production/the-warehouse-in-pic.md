---
title: 领料单日记帐中的仓库在物料清单行上未更新。
description: 领料单日记帐中的仓库在物料清单 (BOM) 行上未更新。
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5d24c0b8538f3894fd1d2a3edb3a6ed8633c9609
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026294"
---
# <a name="the-warehouse-in-the-picking-list-journal-isnt-updated-on-a-bom-line"></a>领料单日记帐中的仓库在物料清单行上未更新

知识库编号：4614848

## <a name="symptoms"></a>故障特征

领料单日记帐中的仓库在物料清单 (BOM) 行上未更新。

## <a name="resolution"></a>解决方法

此系统行为是有意设计的。 如果创建的领料单日记帐行具有对生产物料清单行的引用（通过批次 ID），当生产领料单日记帐行上的仓库维度之后更改时，生产物料清单行上的仓库不会更新。

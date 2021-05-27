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
# <a name="the-warehouse-in-the-picking-list-journal-isnt-updated-on-a-bom-line"></a><span data-ttu-id="f2af2-103">领料单日记帐中的仓库在物料清单行上未更新</span><span class="sxs-lookup"><span data-stu-id="f2af2-103">The warehouse in the picking list journal isn't updated on a BOM line</span></span>

<span data-ttu-id="f2af2-104">知识库编号：4614848</span><span class="sxs-lookup"><span data-stu-id="f2af2-104">KB number: 4614848</span></span>

## <a name="symptoms"></a><span data-ttu-id="f2af2-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="f2af2-105">Symptoms</span></span>

<span data-ttu-id="f2af2-106">领料单日记帐中的仓库在物料清单 (BOM) 行上未更新。</span><span class="sxs-lookup"><span data-stu-id="f2af2-106">The warehouse in the picking list journal isn't updated on a bill of materials (BOM) line.</span></span>

## <a name="resolution"></a><span data-ttu-id="f2af2-107">解决方法</span><span class="sxs-lookup"><span data-stu-id="f2af2-107">Resolution</span></span>

<span data-ttu-id="f2af2-108">此系统行为是有意设计的。</span><span class="sxs-lookup"><span data-stu-id="f2af2-108">The system is behaving as designed.</span></span> <span data-ttu-id="f2af2-109">如果创建的领料单日记帐行具有对生产物料清单行的引用（通过批次 ID），当生产领料单日记帐行上的仓库维度之后更改时，生产物料清单行上的仓库不会更新。</span><span class="sxs-lookup"><span data-stu-id="f2af2-109">If a picking list journal line is created that has a reference (via the lot ID) to a production BOM line, the warehouse on the production BOM line won't be updated if the warehouse dimension on the production picking list journal line is changed later.</span></span>

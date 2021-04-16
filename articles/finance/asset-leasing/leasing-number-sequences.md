---
title: 分配编号规则
description: 本主题说明如何为租赁 ID 创建编号规则。 它还说明了如何创建在索引重估过程中使用的唯一 ID。
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a0b5d622df1e5dcdf7f1322328bce7e185f8edb8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819810"
---
# <a name="assign-number-sequences"></a><span data-ttu-id="08462-104">分配编号规则</span><span class="sxs-lookup"><span data-stu-id="08462-104">Assign number sequences</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="08462-105">本主题说明如何为租赁 ID 创建编号规则。</span><span class="sxs-lookup"><span data-stu-id="08462-105">This topic explains how to create number sequences for lease IDs.</span></span> <span data-ttu-id="08462-106">它还说明了如何创建在索引重估过程中使用的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="08462-106">It also explains how to create unique IDs that are used in the index revaluation process.</span></span>

1. <span data-ttu-id="08462-107">转到 **资产租赁 \> 设置 \> 资产租赁参数**。</span><span class="sxs-lookup"><span data-stu-id="08462-107">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="08462-108">选择 **编号规则** 侧选项卡。</span><span class="sxs-lookup"><span data-stu-id="08462-108">Select the **Number sequences** side tab.</span></span>
3. <span data-ttu-id="08462-109">在侧边栏中选择 **编号规则**。</span><span class="sxs-lookup"><span data-stu-id="08462-109">Select **Number sequences** in the side bar.</span></span>
4. <span data-ttu-id="08462-110">为 **租赁 ID** 引用选择编号规则。</span><span class="sxs-lookup"><span data-stu-id="08462-110">Select the number sequence for the **Lease ID** reference.</span></span> <span data-ttu-id="08462-111">该编号规则将用于为每个租赁生成唯一的标识符。</span><span class="sxs-lookup"><span data-stu-id="08462-111">This number sequence will be used to generate the unique identifier for each lease.</span></span>
5. <span data-ttu-id="08462-112">为 **流程 ID** 引用选择编号规则。</span><span class="sxs-lookup"><span data-stu-id="08462-112">Select the number sequence for the **Process ID** reference.</span></span> <span data-ttu-id="08462-113">该编号规则将用于为每个索引重估过程生成唯一的标识符。</span><span class="sxs-lookup"><span data-stu-id="08462-113">This number sequence will be used to generate the unique identifier for each index revaluation process.</span></span>
6. <span data-ttu-id="08462-114">为 **终止方案 ID** 引用选择编号规则。</span><span class="sxs-lookup"><span data-stu-id="08462-114">Select the number sequence for the **Termination Proposal ID** reference.</span></span> <span data-ttu-id="08462-115">该编号规则将用于为每个终止方案生成唯一的标识符。</span><span class="sxs-lookup"><span data-stu-id="08462-115">This number sequence will be used to generate the unique identifier for each termination proposal.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
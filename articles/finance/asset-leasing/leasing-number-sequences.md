---
title: 分配编号规则
description: 本主题说明如何为租赁 ID 创建编号规则。 它还说明了如何创建在索引重估过程中使用的唯一 ID。
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 331542811b2ba9399185478b6d25d1a57fce3a05
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881076"
---
# <a name="assign-number-sequences"></a><span data-ttu-id="29690-104">分配编号规则</span><span class="sxs-lookup"><span data-stu-id="29690-104">Assign number sequences</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="29690-105">本主题说明如何为租赁 ID 创建编号规则。</span><span class="sxs-lookup"><span data-stu-id="29690-105">This topic explains how to create number sequences for lease IDs.</span></span> <span data-ttu-id="29690-106">它还说明了如何创建在索引重估过程中使用的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="29690-106">It also explains how to create unique IDs that are used in the index revaluation process.</span></span>

1. <span data-ttu-id="29690-107">转到 **资产租赁 \> 设置 \> 资产租赁参数**。</span><span class="sxs-lookup"><span data-stu-id="29690-107">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="29690-108">选择 **编号规则** 侧选项卡。</span><span class="sxs-lookup"><span data-stu-id="29690-108">Select the **Number sequences** side tab.</span></span>
3. <span data-ttu-id="29690-109">在侧边栏中选择 **编号规则**。</span><span class="sxs-lookup"><span data-stu-id="29690-109">Select **Number sequences** in the side bar.</span></span>
4. <span data-ttu-id="29690-110">为 **租赁 ID** 引用选择编号规则。</span><span class="sxs-lookup"><span data-stu-id="29690-110">Select the number sequence for the **Lease ID** reference.</span></span> <span data-ttu-id="29690-111">该编号规则将用于为每个租赁生成唯一的标识符。</span><span class="sxs-lookup"><span data-stu-id="29690-111">This number sequence will be used to generate the unique identifier for each lease.</span></span>
5. <span data-ttu-id="29690-112">为 **流程 ID** 引用选择编号规则。</span><span class="sxs-lookup"><span data-stu-id="29690-112">Select the number sequence for the **Process ID** reference.</span></span> <span data-ttu-id="29690-113">该编号规则将用于为每个索引重估过程生成唯一的标识符。</span><span class="sxs-lookup"><span data-stu-id="29690-113">This number sequence will be used to generate the unique identifier for each index revaluation process.</span></span>
6. <span data-ttu-id="29690-114">为 **终止方案 ID** 引用选择编号规则。</span><span class="sxs-lookup"><span data-stu-id="29690-114">Select the number sequence for the **Termination Proposal ID** reference.</span></span> <span data-ttu-id="29690-115">该编号规则将用于为每个终止方案生成唯一的标识符。</span><span class="sxs-lookup"><span data-stu-id="29690-115">This number sequence will be used to generate the unique identifier for each termination proposal.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

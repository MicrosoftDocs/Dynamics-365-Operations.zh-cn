---
title: 审核计划订单
description: 此主题介绍计划优化中支持的计划订单的审核。
author: ChristianRytt
manager: tfehr
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: b7975088be898ccecceb1f7be009cecff107f6e6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4422971"
---
# <a name="approve-planned-orders"></a><span data-ttu-id="7f936-103">审核计划订单</span><span class="sxs-lookup"><span data-stu-id="7f936-103">Approve planned orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7f936-104">此主题介绍如何在计划优化中更新计划订单的状态。</span><span class="sxs-lookup"><span data-stu-id="7f936-104">This topic provides information about how to update the status of planned orders in Planning Optimization.</span></span>

<span data-ttu-id="7f936-105">请注意，审核计划订单为最终从计划订单创建确定订单过程中的可选步骤。</span><span class="sxs-lookup"><span data-stu-id="7f936-105">Note that approval of planned orders is an optional step, on the way to create a firmed order from a planned order.</span></span> <span data-ttu-id="7f936-106">建议批准修改后的计划订单，否则将忽略编辑，并替换为下一个运行计划。</span><span class="sxs-lookup"><span data-stu-id="7f936-106">It is recommended to approve modified planned orders, otherwise the edits will be ignored and overwritten by the next planning run.</span></span>

![计划订单流](media/approved-planned-orders-1.png)

<span data-ttu-id="7f936-108">**状态** 字段可帮助您使用以下值来确定进度：</span><span class="sxs-lookup"><span data-stu-id="7f936-108">The **Status** field helps you tack your progress using the following values:</span></span>

- <span data-ttu-id="7f936-109">**未处理：** 当主计划生成计划订单时，该计划订单状态为 *未处理*。</span><span class="sxs-lookup"><span data-stu-id="7f936-109">**Unprocessed:** When master planning generates planned orders, the planned orders have a status of *Unprocessed*.</span></span> <span data-ttu-id="7f936-110">此状态的计划订单将在下一次计划运行期间删除。</span><span class="sxs-lookup"><span data-stu-id="7f936-110">Planned orders with this status will be deleted during the next planning run.</span></span>
- <span data-ttu-id="7f936-111">**已完成：** 如果您决定不确认计划订单，可以将状态更改为 *已完成* 以表示您已完成对该计划订单的评估。</span><span class="sxs-lookup"><span data-stu-id="7f936-111">**Completed:** If you decide not to firm a planned order, you can change the status to *Completed* to indicate that you completed evaluating this planned order.</span></span> <span data-ttu-id="7f936-112">请注意，系统同等对待 *未处理* 和 *已完成* 状态。</span><span class="sxs-lookup"><span data-stu-id="7f936-112">Note that a status of *Unprocessed* and *Completed* are treated the same by the system.</span></span>
- <span data-ttu-id="7f936-113">**已批准：** 如果要保留编辑或计划确定计划订单，请将状态更改为 *已批准*。</span><span class="sxs-lookup"><span data-stu-id="7f936-113">**Approved:** If you want to keep edits or are planning to firm a planned order, change the status to *Approved*.</span></span> <span data-ttu-id="7f936-114">主计划将状态为 *已批准* 的计划订单视为已确定和预期供应，所以不会在随后的主计划运行期间修改或删除这些订单。</span><span class="sxs-lookup"><span data-stu-id="7f936-114">Planned orders with *Approved* status are considered as fixed and expected supply by master planning, so they are not modified or deleted during later master planning runs.</span></span> <span data-ttu-id="7f936-115">为此，计划逻辑会在主计划期间将 *已审核* 的计划订单从旧计划版本复制到新计划版本。</span><span class="sxs-lookup"><span data-stu-id="7f936-115">To achieve this, the planning logic copies the *Approved* planned orders from the old plan version to the new plan version during master planning.</span></span> <span data-ttu-id="7f936-116">请注意，*已批准* 的计划订单在特定主计划内仅视为供应。</span><span class="sxs-lookup"><span data-stu-id="7f936-116">Note that *Approved* planned orders are only considered supply within the specific master plan.</span></span>

<span data-ttu-id="7f936-117">您可以从 **主计划** 工作区、**计划订单** 列表或 **计划生产订单**、**计划采购订单** 和 **计划转移** 列表中管理计划订单。</span><span class="sxs-lookup"><span data-stu-id="7f936-117">You can manage planned orders from the  **Master planning**  workspace, the  **Planned order**  list, or the  **Planned production orders**,  **Planned purchase orders**, and  **Planned transfer**  lists.</span></span>

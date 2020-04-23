---
title: 工作订单类型
description: 本主题介绍资产管理中的工作订单类型。
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 375b18a4bd37ddadecee03a01b3b2125f5cc8d0a
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215416"
---
# <a name="work-order-types"></a><span data-ttu-id="598f1-103">工作订单类型</span><span class="sxs-lookup"><span data-stu-id="598f1-103">Work order types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="598f1-104">工作订单类型用于为工作订单归类。</span><span class="sxs-lookup"><span data-stu-id="598f1-104">Work order types are used to categorize work orders.</span></span> <span data-ttu-id="598f1-105">例如，您可能有与预防性维护或修复性维护有关的工作订单。</span><span class="sxs-lookup"><span data-stu-id="598f1-105">For example, you might have work orders that are related to preventive maintenance or corrective maintenance.</span></span>

<span data-ttu-id="598f1-106">工作订单类型定义与工作订单生命周期模型之间的隶属关系。</span><span class="sxs-lookup"><span data-stu-id="598f1-106">A work order type defines an affiliation with a work order lifecycle model.</span></span> <span data-ttu-id="598f1-107">工作订单生命周期模型定义可为工作订单设置的工作订单生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="598f1-107">A work order lifecycle model defines the work order lifecycle states that can be set on a work order.</span></span> <span data-ttu-id="598f1-108">（工作订单生命周期状态示例包括**已创建**、**进行中**和**已完成**。）</span><span class="sxs-lookup"><span data-stu-id="598f1-108">(Examples of work order lifecycle states include **Created**, **In Process**, and **Finished**.)</span></span>

<span data-ttu-id="598f1-109">有关工作订单生命周期状态和项目阶段的详细信息，请参阅[工作订单生命周期状态](work-order-lifecycle-states.md)。</span><span class="sxs-lookup"><span data-stu-id="598f1-109">For more information about work order lifecycle states and project stages, see [Work order lifecycle states](work-order-lifecycle-states.md).</span></span>

1. <span data-ttu-id="598f1-110">选择**资产管理** \> **设置** \> **工作订单** \> **工作订单类型**。</span><span class="sxs-lookup"><span data-stu-id="598f1-110">Select **Asset management** \> **Setup** \> **Work orders** \> **Work order types**.</span></span>
2. <span data-ttu-id="598f1-111">选择**新建**以创建新的工作订单类型。</span><span class="sxs-lookup"><span data-stu-id="598f1-111">Select **New** to create a work order type.</span></span>
3. <span data-ttu-id="598f1-112">在**工作订单类型**字段中，输入工作订单类型的 ID。</span><span class="sxs-lookup"><span data-stu-id="598f1-112">In the **Work order type** field, enter an ID for the work order type.</span></span>
4. <span data-ttu-id="598f1-113">在**名称**字段中输入名称。</span><span class="sxs-lookup"><span data-stu-id="598f1-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="598f1-114">在**工作订单生命周期模型**字段中选择生命周期模型。</span><span class="sxs-lookup"><span data-stu-id="598f1-114">In the **Work order lifecycle model** field, select a lifecycle model.</span></span>
5. <span data-ttu-id="598f1-115">如果应该将与此类型的工作订单关联的所有工作订单作业安排给同一位维护工人，请将**一位维护工人**选择为**是**。</span><span class="sxs-lookup"><span data-stu-id="598f1-115">Set the **One maintenance worker** option to **Yes** if all work order jobs that are related to a work order of this type should be scheduled to the same maintenance worker.</span></span>
6. <span data-ttu-id="598f1-116">根据需要在**成本类型**字段中选择**纠正**、**预防性**或**投资**。</span><span class="sxs-lookup"><span data-stu-id="598f1-116">In the **Cost type** field, select **Corrective**, **Preventive**, or **Investment**, as appropriate.</span></span> <span data-ttu-id="598f1-117">一个工作订单的所有工作订单作业具有相同的成本类型。</span><span class="sxs-lookup"><span data-stu-id="598f1-117">All work order jobs on a work order must have the same cost type.</span></span>
7. <span data-ttu-id="598f1-118">在**必需**部分中，将相关选项设置为**是**，以便指定向此类型的工作订单添加哪些与故障有关或与维护停机时间有关的信息。</span><span class="sxs-lookup"><span data-stu-id="598f1-118">In the **Mandatory** section, set the relevant options to **Yes** to specify which fault-related or maintenance downtime–related information is added to a work order of this type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="598f1-119">**必需**部分中的选项与**工作订单生命周期状态**页（**资产管理** \> **设置** \> **工作订单** \> **生命周期状态**）的**验证**快速选项卡上的选项有关。</span><span class="sxs-lookup"><span data-stu-id="598f1-119">The options in the **Mandatory** section are related to the options on the **Validate** FastTab of the **Work order lifecycle states** page (**Asset management** \> **Setup** \> **Work orders** \> **Lifecycle states**).</span></span>

8. <span data-ttu-id="598f1-120">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="598f1-120">Select **Save**.</span></span>

![工作订单类型](media/16-setup-for-work-orders.png)

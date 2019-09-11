---
title: 已计划执行
description: 本主题介绍资产管理中的已计划执行。
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8d9c8afc139c96e32efb3161d35fde685b8abcc5
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874662"
---
# <a name="scheduled-execution"></a><span data-ttu-id="996e9-103">已计划执行</span><span class="sxs-lookup"><span data-stu-id="996e9-103">Scheduled execution</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="996e9-104">可使用工作订单服务级别设置已计划执行。</span><span class="sxs-lookup"><span data-stu-id="996e9-104">You can use work order service levels to set up scheduled execution.</span></span> <span data-ttu-id="996e9-105">（有关工作订单服务级别的详细信息，请参阅[服务级别和描述](service-level-and-description.md)。）已计划执行可以在为维护工人计划工作时提高灵活性，因为可以为应完成工作订单的期间设置更详细或更通用的要求。</span><span class="sxs-lookup"><span data-stu-id="996e9-105">(For more information about work order service levels, see [Service level and description](service-level-and-description.md).) Scheduled execution provides flexibility in work planning for maintenance workers, because you can set up more detailed or less detailed requirements for the interval that a work order should be completed during.</span></span> <span data-ttu-id="996e9-106">例如，可能可以让一个生产设施中完成作业的速度比预计快的维护工人继续处理附近另一个安排在本周，但不一定当天执行的作业。</span><span class="sxs-lookup"><span data-stu-id="996e9-106">For example, a maintenance worker who completes a job faster than expected in a production facility might be able to move on to another nearby job that was planned for the current week but not necessarily for the current day.</span></span> <span data-ttu-id="996e9-107">这种方法可以优化工人规划和作业完成。</span><span class="sxs-lookup"><span data-stu-id="996e9-107">This approach allows for optimization of worker planning and job completion.</span></span>

<span data-ttu-id="996e9-108">已计划执行的设置与工人有关，可以通用，也可以具体。</span><span class="sxs-lookup"><span data-stu-id="996e9-108">Scheduled execution setup, which is related to work orders, can be generic or specific.</span></span> <span data-ttu-id="996e9-109">可以设置不限制到具体工作订单类型、资产类型等的通用行。</span><span class="sxs-lookup"><span data-stu-id="996e9-109">You can set up generic lines that aren't limited to specific work order types, asset types, and so on.</span></span> <span data-ttu-id="996e9-110">也可以创建应用于具体工作订单类型、资产类型、维护作业类型等的已计划执行行。</span><span class="sxs-lookup"><span data-stu-id="996e9-110">Alternatively, you can create scheduled execution lines that apply to a specific work order type, asset type, maintenance job type, and so on.</span></span>

1. <span data-ttu-id="996e9-111">选择**资产管理** \> **设置** \> **工作订单** \> **已计划执行**。</span><span class="sxs-lookup"><span data-stu-id="996e9-111">Select **Asset management** \> **Setup** \> **Work orders** \> **Scheduled execution**.</span></span>
2. <span data-ttu-id="996e9-112">选择**新建**以创建已计划执行行。</span><span class="sxs-lookup"><span data-stu-id="996e9-112">Select **New** to create a scheduled execution line.</span></span>
3. <span data-ttu-id="996e9-113">在**功能位置**、**工作订单类型**、**资产类型**、**制造商**、**型号**、**维护作业类型类别**、**维护作业类型**、**维护作业变型**和**工种**字段中，根据需要选择值。</span><span class="sxs-lookup"><span data-stu-id="996e9-113">In the **Functional location**, **Work order type**, **Asset type**, **Manufacturer**, **Model**, **Maintenance job type category**, **Maintenance job type**, **Maintenance job type variant**, and **Trade** fields, select values as you require.</span></span>
4. <span data-ttu-id="996e9-114">在**服务级别**字段中，选择一个工作订单服务级别。</span><span class="sxs-lookup"><span data-stu-id="996e9-114">In the **Service level** field, select a work order service level.</span></span> <span data-ttu-id="996e9-115">如果让此字段保留为空，则创建的是最通用的已计划执行类型。</span><span class="sxs-lookup"><span data-stu-id="996e9-115">If you leave this field blank, you make the most generic type of scheduled execution line.</span></span> <span data-ttu-id="996e9-116">有关通用行的示例，请参阅下图中的第一个记录。</span><span class="sxs-lookup"><span data-stu-id="996e9-116">For an example of a generic line, see the first record in the illustration that follows.</span></span> <span data-ttu-id="996e9-117">该行启用未为其安排具体日期和时间的工作订单服务级别的所有工作订单。</span><span class="sxs-lookup"><span data-stu-id="996e9-117">That line enables all work orders that have no work order service level to be scheduled for a specific date and time.</span></span>
5. <span data-ttu-id="996e9-118">在**已计划执行**字段中，输入时间间隔。</span><span class="sxs-lookup"><span data-stu-id="996e9-118">In the **Scheduled execution** field, select the time interval.</span></span>
6. <span data-ttu-id="996e9-119">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="996e9-119">Select **Save**.</span></span>

![图 1](media/20-setup-for-work-orders.png)

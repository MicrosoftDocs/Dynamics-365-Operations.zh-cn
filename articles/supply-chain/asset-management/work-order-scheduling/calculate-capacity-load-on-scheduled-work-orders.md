---
title: 对计划的工作订单计算产能负荷
description: 本主题介绍如何在资产管理中对计划的工作订单计算产能负荷。
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 09e0fc17a288a278b7b1feaba8c7b73425aa2d52
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808152"
---
# <a name="calculate-capacity-load-on-scheduled-work-orders"></a><span data-ttu-id="52596-103">对计划的工作订单计算产能负荷</span><span class="sxs-lookup"><span data-stu-id="52596-103">Calculate capacity load on scheduled work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="52596-104">可以对计划的工作订单计算产能负荷，以便获取资源在特定期间的工作负荷。</span><span class="sxs-lookup"><span data-stu-id="52596-104">You can calculate capacity load on scheduled work orders to get an overview of the work load on resources for a specific period.</span></span> <span data-ttu-id="52596-105">可以对以下资源进行计算：维护工人、工人组、工具和资产。</span><span class="sxs-lookup"><span data-stu-id="52596-105">Calculations can be made for the following resources: Maintenance workers, worker groups, tools, and assets.</span></span>

1. <span data-ttu-id="52596-106">单击 **资产管理** > **查询** > **计划** > **产能负荷**。</span><span class="sxs-lookup"><span data-stu-id="52596-106">Click **Asset management** > **Inquiries** > **Schedule** > **Capacity load**.</span></span>

2. <span data-ttu-id="52596-107">在 **计算产能负荷** 对话框 > **显示** 字段中，选择要计算的负荷类型：**产能**、**预留** 或 **余额**。</span><span class="sxs-lookup"><span data-stu-id="52596-107">In the **Calculate capacity load** dialog > **Show** field, select which load type you want to calculate: **Capacity**, **Reserved**, or **Remainder**.</span></span>

3. <span data-ttu-id="52596-108">如果不希望显示包含零的结果，请在 **忽略零** 切换按钮上选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="52596-108">Select **Yes** on the **Skip zero** toggle button if you do not want to show results containing zero.</span></span>

4. <span data-ttu-id="52596-109">通过在相关切换按钮上选择 **是**，选择要为其计算产能负荷的资源类型：**工人**、**维护工人组**、**工具** 和 **资产**。</span><span class="sxs-lookup"><span data-stu-id="52596-109">Select the resource types for which you want to calculate capacity load by selecting **Yes** on the relevant toggle buttons: **Worker**, **Maintenance worker group**, **Tool**, and **Asset**.</span></span>

5. <span data-ttu-id="52596-110">在 **开始日期** 字段中选择计算的开始日期。</span><span class="sxs-lookup"><span data-stu-id="52596-110">Select the start date for the calculation in the **From date** field.</span></span>

6. <span data-ttu-id="52596-111">在 **间隔类型** 字段中，选择计算的间隔：**天**、**周**、**月** 或 **季度**。</span><span class="sxs-lookup"><span data-stu-id="52596-111">In the **Interval type** field, select the interval for the calculation: **Day**, **Week**, **Month**, or **Quarter**.</span></span>

7. <span data-ttu-id="52596-112">在 **期间频率** 字段中，插入要计算的间隔的数量。</span><span class="sxs-lookup"><span data-stu-id="52596-112">In the **Period frequency** field, insert the number of intervals you want to calculate.</span></span> <span data-ttu-id="52596-113">例如，如果选择的间隔类型为 **天**，并且在此字段中输入数字“5”，将从开始日期之后五天进行计算。</span><span class="sxs-lookup"><span data-stu-id="52596-113">For example, if you have selected **Day** as the interval type, and you enter the number "5" in this field, a calculation of five days from the start date will be made.</span></span>

8. <span data-ttu-id="52596-114">单击 **确定** 开始计算。</span><span class="sxs-lookup"><span data-stu-id="52596-114">Click **OK** to start the calculation.</span></span>

<span data-ttu-id="52596-115">下图显示的计算结果涵盖三天的负荷类型 **预留**。</span><span class="sxs-lookup"><span data-stu-id="52596-115">The figure below shows the result of a calculation covering three weeks for the load type **Reserved**.</span></span>

![图 1](media/08-work-order-scheduling.png)

[!NOTE]
<span data-ttu-id="52596-117">如果为计算选择 **产能** 或 **余额**，并且在所选期间没有为资源进行预留，将显示相同的结果。</span><span class="sxs-lookup"><span data-stu-id="52596-117">If you select the load types **Capacity** or **Remainder** for your calculation, the same result will be displayed if no reservations have been made for the resources in the selected period.</span></span>

<span data-ttu-id="52596-118">有关如何对维护安排行，而不是计划的工作订单计算产能负荷的信息，请参阅[计算产能负荷](../capacity-planning/calculate-capacity-load.md)。</span><span class="sxs-lookup"><span data-stu-id="52596-118">For information about how to calculate capacity load on maintenance schedule lines and not scheduled work orders, refer to [Calculate capacity load](../capacity-planning/calculate-capacity-load.md).</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
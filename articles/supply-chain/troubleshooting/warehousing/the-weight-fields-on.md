---
title: 负荷行上的重量字段与负荷上的重量字段不匹配
description: 负荷行上的重量字段与负荷上的重量字段不匹配
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSShipmentDetails_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 639b82a9d46b74f179d6904d2c3b8e7dfb813b58
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924343"
---
# <a name="the-weight-fields-on-load-lines-dont-match-the-weight-fields-on-the-load"></a><span data-ttu-id="2f242-103">负荷行上的重量字段与负荷上的重量字段不匹配</span><span class="sxs-lookup"><span data-stu-id="2f242-103">The weight fields on load lines don't match the weight fields on the load</span></span>

<span data-ttu-id="2f242-104">错误代码：WHSLoadWeightOnLinesDoNotMatchLoadWarning</span><span class="sxs-lookup"><span data-stu-id="2f242-104">Error codes: WHSLoadWeightOnLinesDoNotMatchLoadWarning</span></span>

## <a name="symptoms"></a><span data-ttu-id="2f242-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="2f242-105">Symptoms</span></span>

<span data-ttu-id="2f242-106">系统将显示以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="2f242-106">The system shows the following error message:</span></span>

> <span data-ttu-id="2f242-107">负荷行上的重量字段与负荷 %1 上的重量字段不匹配。</span><span class="sxs-lookup"><span data-stu-id="2f242-107">The weight fields on load lines do not match the weight fields on load %1.</span></span> <span data-ttu-id="2f242-108">请运行仓库负荷重量一致性检查来重新计算重量字段。</span><span class="sxs-lookup"><span data-stu-id="2f242-108">Run the Warehouse load weight consistency check to recalculate the weight fields.</span></span>

## <a name="cause"></a><span data-ttu-id="2f242-109">原因</span><span class="sxs-lookup"><span data-stu-id="2f242-109">Cause</span></span>

<span data-ttu-id="2f242-110">**净重** 和 **皮重** 字段在负荷行上设置为 *0*（零）。</span><span class="sxs-lookup"><span data-stu-id="2f242-110">The **Net weight** and **Tara weight** fields are set to *0* (zero) on the load line.</span></span> <span data-ttu-id="2f242-111">但是，产品的重量度量的重量字段未设置为 *0*。</span><span class="sxs-lookup"><span data-stu-id="2f242-111">However, the weight fields aren't set to *0* for the weight measurements on the product.</span></span> <span data-ttu-id="2f242-112">如果未在负荷行上设置重量字段，对负荷行上的数量进行任何更正都可能导致负荷上的重量计算不正确。</span><span class="sxs-lookup"><span data-stu-id="2f242-112">When weight fields aren't set on the load line, any corrections of the quantity on the load line might cause incorrect weight calculation on the load.</span></span> <span data-ttu-id="2f242-113">如果自创建负荷行以来更改了产品上的重量，可能会发生此问题。</span><span class="sxs-lookup"><span data-stu-id="2f242-113">This issue might occur if the weights on the product have been changed since the load line was created.</span></span>

## <a name="resolution"></a><span data-ttu-id="2f242-114">解决方法</span><span class="sxs-lookup"><span data-stu-id="2f242-114">Resolution</span></span>

<span data-ttu-id="2f242-115">默认情况下，创建负荷行时，将在负荷行上输入来自产品的重量字段。</span><span class="sxs-lookup"><span data-stu-id="2f242-115">By default, when a load line is created, the weight fields from the product are entered on it.</span></span> <span data-ttu-id="2f242-116">如果重量为零，可以使用 *仓库负荷重量一致性检查* 功能重新进行计算。</span><span class="sxs-lookup"><span data-stu-id="2f242-116">If the weight is zero, you can recalculate it by using the *Warehouse load weight consistency check* functionality.</span></span>

1. <span data-ttu-id="2f242-117">转到 **系统管理 \> 定期任务 \> 数据库 \> 一致性检查**。</span><span class="sxs-lookup"><span data-stu-id="2f242-117">Go to **System administration \> Periodic tasks \> Database \> Consistency check**.</span></span>
1. <span data-ttu-id="2f242-118">在 **一致性检查** 对话框中，将 **模块** 字段设置为 *仓库管理*。</span><span class="sxs-lookup"><span data-stu-id="2f242-118">In the **Consistency check** dialog box, set the **Module** field to *Warehouse management*.</span></span>
1. <span data-ttu-id="2f242-119">将 **检查/修复** 字段设置为 *修复错误*。</span><span class="sxs-lookup"><span data-stu-id="2f242-119">Set the **Check/Fix** field to *Fix error*.</span></span>
1. <span data-ttu-id="2f242-120">在复选框列表中，选中 **仓库负荷重量一致性检查** 复选框，并确保仅突出显示此复选框的行。</span><span class="sxs-lookup"><span data-stu-id="2f242-120">In the checkbox list, select the **Warehouse load weight consistency check** checkbox, and make sure that only the row for this checkbox is highlighted.</span></span>
1. <span data-ttu-id="2f242-121">在复选框列表的顶部，选择省略号按钮 (**...**)，然后选择菜单上的 **对话**。</span><span class="sxs-lookup"><span data-stu-id="2f242-121">At the top of the checkbox list, select the ellipsis button (**...**), and then select **Dialog** on the menu.</span></span>
1. <span data-ttu-id="2f242-122">在 **仓库负荷重量一致性检查** 对话框中，设置以下字段来指定应运行一致性检查的条件：</span><span class="sxs-lookup"><span data-stu-id="2f242-122">In the **Warehouse load weight consistency check** dialog box, set the following fields to specify the criteria that the consistency check should run for:</span></span>

    - <span data-ttu-id="2f242-123">**负荷 ID：** 指定负荷 ID。</span><span class="sxs-lookup"><span data-stu-id="2f242-123">**Load ID:** Specify a load ID.</span></span> <span data-ttu-id="2f242-124">保留为空白将检查所有负荷 ID。</span><span class="sxs-lookup"><span data-stu-id="2f242-124">Leave this blank to check all load IDs.</span></span>
    - <span data-ttu-id="2f242-125">**物料编号：** 指定物料编号。</span><span class="sxs-lookup"><span data-stu-id="2f242-125">**Item number:** Specify an item number.</span></span> <span data-ttu-id="2f242-126">保留为空白将检查所有物料。</span><span class="sxs-lookup"><span data-stu-id="2f242-126">Leave this blank to check all items.</span></span>
    - <span data-ttu-id="2f242-127">**始终重新计算负荷上的重量：** 将此选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="2f242-127">**Always recalculate weight on loads:** Set this option to *Yes*.</span></span>
    - <span data-ttu-id="2f242-128">**允许覆盖负荷行上的重量：** 将此选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="2f242-128">**Allow overwrite of weight on load lines:** Set this option to *Yes*.</span></span>

1. <span data-ttu-id="2f242-129">选择 **确定** 关闭 **仓库负荷重量一致性检查** 对话框。</span><span class="sxs-lookup"><span data-stu-id="2f242-129">Select **OK** to close the **Warehouse load weight consistency check** dialog box.</span></span>
1. <span data-ttu-id="2f242-130">选择省略号按钮，然后在菜单上选择 **执行**。</span><span class="sxs-lookup"><span data-stu-id="2f242-130">Select the ellipsis button, and then select **Execute** on the menu.</span></span>

<span data-ttu-id="2f242-131">将根据您指定的条件重新计算重量。</span><span class="sxs-lookup"><span data-stu-id="2f242-131">The weight is recalculated based on the criteria that you specified.</span></span> <span data-ttu-id="2f242-132">选择 **消息详细信息** 链接可以查看一致性检查的结果。</span><span class="sxs-lookup"><span data-stu-id="2f242-132">Select the **Message details** link to view the result of the consistency check.</span></span>

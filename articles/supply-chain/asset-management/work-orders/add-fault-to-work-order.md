---
title: 将故障添加到工作订单
description: 此主题介绍如何在资产管理中向工作订单添加故障登记。
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
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
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2b58cc31578d7bb102c6b5aa8b4ce2d6cfe8c893
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626193"
---
# <a name="add-fault-to-work-order"></a><span data-ttu-id="f9f86-103">将故障添加到工作订单</span><span class="sxs-lookup"><span data-stu-id="f9f86-103">Add fault to work order</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="f9f86-104">可以向工作订单添加故障设计器中设置的故障。</span><span class="sxs-lookup"><span data-stu-id="f9f86-104">You can add faults that were set up in the fault designer to a work order.</span></span> <span data-ttu-id="f9f86-105">必须将一个或多个故障记录连接到在工作订单中选择的资产所使用的资产类型。</span><span class="sxs-lookup"><span data-stu-id="f9f86-105">One or more fault records must be connected to the asset types that are used for the asset that is selected in the work order.</span></span> <span data-ttu-id="f9f86-106">有关设置的详细信息，请参阅[故障管理](../setup-for-work-orders/fault-management.md)。</span><span class="sxs-lookup"><span data-stu-id="f9f86-106">For more information about the setup, see [Fault management](../setup-for-work-orders/fault-management.md).</span></span>

1. <span data-ttu-id="f9f86-107">选择**资产管理** > **常用** > **工作订单** > **所有工作订单**或**有效工作订单**。</span><span class="sxs-lookup"><span data-stu-id="f9f86-107">Select **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="f9f86-108">选择要创建故障登记的工作订单，然后，在操作窗格中，在**工作订单**选项卡上，在**资产**组中，选择**资产故障**。</span><span class="sxs-lookup"><span data-stu-id="f9f86-108">Select the work order to make a fault registration on, and then, on the Action Pane, on the **Work order** tab, in the **Asset** group, select **Asset fault**.</span></span>

3. <span data-ttu-id="f9f86-109">在**特征**快速选项卡中，选择**添加行**。</span><span class="sxs-lookup"><span data-stu-id="f9f86-109">On the **Symptoms** FastTab, select **Add line**.</span></span> <span data-ttu-id="f9f86-110">将在**故障**字段中自动输入一个连续故障编号。</span><span class="sxs-lookup"><span data-stu-id="f9f86-110">A sequential fault number is automatically entered in the **Fault** field.</span></span>

4. <span data-ttu-id="f9f86-111">在**故障特征**字段中，选择相关特征。</span><span class="sxs-lookup"><span data-stu-id="f9f86-111">In the **Fault symptom** field, select the relevant symptom.</span></span>

5. <span data-ttu-id="f9f86-112">在**故障区域**和**故障类型**字段中，选择适当的值。</span><span class="sxs-lookup"><span data-stu-id="f9f86-112">In the **Fault area** and **Fault type** fields, select the appropriate values.</span></span>

6. <span data-ttu-id="f9f86-113">将在**故障日期**字段中自动插入当前日期。</span><span class="sxs-lookup"><span data-stu-id="f9f86-113">In the **Fault date** field, the current date is automatically inserted.</span></span> <span data-ttu-id="f9f86-114">您可以根据需要选择其他日期。</span><span class="sxs-lookup"><span data-stu-id="f9f86-114">You can select a different date as you require.</span></span>

7. <span data-ttu-id="f9f86-115">在**所选故障特征的成因**快速选项卡上，添加一行来描述问题成因。</span><span class="sxs-lookup"><span data-stu-id="f9f86-115">On the **Causes for selected symptom** FastTab, add a line to describe the cause of the issue.</span></span>

8. <span data-ttu-id="f9f86-116">在**所选故障特征的成因**快速选项卡上，添加一行来描述问题的可行解决方案。</span><span class="sxs-lookup"><span data-stu-id="f9f86-116">On the **Remedies for selected symptom** FastTab, add a line to describe a possible solution to the issue.</span></span>

9. <span data-ttu-id="f9f86-117">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="f9f86-117">Select **Save**.</span></span>

<span data-ttu-id="f9f86-118">下图显示了故障登记的示例。</span><span class="sxs-lookup"><span data-stu-id="f9f86-118">The illustration below shows an example of a fault registration.</span></span>

![图 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a><span data-ttu-id="f9f86-120">查看资产故障</span><span class="sxs-lookup"><span data-stu-id="f9f86-120">View asset faults</span></span>

<span data-ttu-id="f9f86-121">在**资产故障**列表中，可概览为资产登记的所有故障。</span><span class="sxs-lookup"><span data-stu-id="f9f86-121">In the **Asset faults** list, you can get an overview of all faults registered on assets.</span></span>

<span data-ttu-id="f9f86-122">在**资产故障**列表页上，可概览已为资产登记的所有故障。</span><span class="sxs-lookup"><span data-stu-id="f9f86-122">On the **Asset faults** list page, you can get an overview of all faults that have been registered on assets.</span></span> <span data-ttu-id="f9f86-123">要打开此页面，请选择**资产管理** > **查询** > **资产故障** > **资产故障**。</span><span class="sxs-lookup"><span data-stu-id="f9f86-123">To open the page, select **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span>


## <a name="print-asset-fault-report"></a><span data-ttu-id="f9f86-124">打印资产故障报告</span><span class="sxs-lookup"><span data-stu-id="f9f86-124">Print asset fault report</span></span>

<span data-ttu-id="f9f86-125">可从**所有资产**列表页打印资产故障报告，其中显示所有故障登记和故障统计信息的图形概览。</span><span class="sxs-lookup"><span data-stu-id="f9f86-125">From the **All assets** list page, you can print an asset fault report that shows all fault registrations and a graphical overview of fault statistics.</span></span>

1. <span data-ttu-id="f9f86-126">选择**资产管理** > **常用** > **资产** > **所有资产**。</span><span class="sxs-lookup"><span data-stu-id="f9f86-126">Select **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="f9f86-127">选择要为其打印故障报告的资产。</span><span class="sxs-lookup"><span data-stu-id="f9f86-127">Select the asset to print a fault report for.</span></span>

3. <span data-ttu-id="f9f86-128">在“操作”窗格中，在**常规**选项卡上，在**报告**组中，选择**资产故障**。</span><span class="sxs-lookup"><span data-stu-id="f9f86-128">On the Action Pane, on the **General** tab, in the **Reports** group, select **Asset fault**.</span></span>

4. <span data-ttu-id="f9f86-129">输入具体期间，或选择故障类型。</span><span class="sxs-lookup"><span data-stu-id="f9f86-129">Enter a specific period, or select a fault type.</span></span>

5. <span data-ttu-id="f9f86-130">选择**确定**打印报告。</span><span class="sxs-lookup"><span data-stu-id="f9f86-130">Select **OK** to print the report.</span></span>

>[!NOTE]
><span data-ttu-id="f9f86-131">要打印多个资产或资产类型的故障报告，请选择**资产管理** > **报告** > **资产** > **资产故障**。</span><span class="sxs-lookup"><span data-stu-id="f9f86-131">To print a fault report for several assets or asset types, select **Asset management** > **Reports** > **Assets** > **Asset fault**.</span></span>


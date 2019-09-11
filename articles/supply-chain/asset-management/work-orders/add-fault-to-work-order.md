---
title: 将故障添加到工作订单
description: 此主题介绍如何在资产管理中向工作订单添加故障登记。
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7c86973ca44d9113d14e180e27cc51343da5d2c0
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875530"
---
# <a name="add-fault-to-work-order"></a><span data-ttu-id="a0f31-103">将故障添加到工作订单</span><span class="sxs-lookup"><span data-stu-id="a0f31-103">Add fault to work order</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="a0f31-104">可以向工作订单添加故障设计器中设置的故障。</span><span class="sxs-lookup"><span data-stu-id="a0f31-104">You can add faults set up in the fault designer to a work order.</span></span> <span data-ttu-id="a0f31-105">工作订单中选择的资产必须包含与一个或多个故障记录连接的资产类型。</span><span class="sxs-lookup"><span data-stu-id="a0f31-105">The asset selected in the work order must contain asset types that have one or more fault records connected to it.</span></span> <span data-ttu-id="a0f31-106">有关设置的详细信息，请参阅[故障管理](../setup-for-work-orders/fault-management.md)部分。</span><span class="sxs-lookup"><span data-stu-id="a0f31-106">Read more about setup in the [Fault management](../setup-for-work-orders/fault-management.md) section.</span></span>

1. <span data-ttu-id="a0f31-107">单击**资产管理** > **常用** > **工作订单** > **所有工作订单**或**有效工作订单**。</span><span class="sxs-lookup"><span data-stu-id="a0f31-107">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="a0f31-108">在列表中，选择要为其创建故障登记的工作订单，然后单击**资产故障**。</span><span class="sxs-lookup"><span data-stu-id="a0f31-108">In the list, select the work order on which you want to make a fault registration and click **Asset fault**.</span></span>

3. <span data-ttu-id="a0f31-109">在**特征**快速选项卡中，单击**添加行**。</span><span class="sxs-lookup"><span data-stu-id="a0f31-109">On the **Symptoms** FastTab, click **Add line**.</span></span> <span data-ttu-id="a0f31-110">将在**故障**字段中自动插入一个连续故障编号。</span><span class="sxs-lookup"><span data-stu-id="a0f31-110">A sequential fault number is automatically inserted in the **Fault** field.</span></span>

4. <span data-ttu-id="a0f31-111">在**故障特征**字段中选择相关特征。</span><span class="sxs-lookup"><span data-stu-id="a0f31-111">Select the relevant symptom in the **Fault symptom** field.</span></span>

5. <span data-ttu-id="a0f31-112">选择**故障区域**和**故障类型**。</span><span class="sxs-lookup"><span data-stu-id="a0f31-112">Select **Fault area** and **Fault type**.</span></span>

6. <span data-ttu-id="a0f31-113">将在**故障日期**字段中自动插入当前日期。</span><span class="sxs-lookup"><span data-stu-id="a0f31-113">In the **Fault date** field, the current date is automatically inserted.</span></span> <span data-ttu-id="a0f31-114">如有必要，可以选择其他日期。</span><span class="sxs-lookup"><span data-stu-id="a0f31-114">You can select another date, if necessary.</span></span>

7. <span data-ttu-id="a0f31-115">在**所选故障特征的成因**快速选项卡上，添加一行，用于描述问题成因。</span><span class="sxs-lookup"><span data-stu-id="a0f31-115">On the **Causes for selected symptom** FastTab, add a line describing the cause of the problem.</span></span>

8. <span data-ttu-id="a0f31-116">在**所选故障特征的成因**快速选项卡上，添加一行，用于描述问题的可行解决方案。</span><span class="sxs-lookup"><span data-stu-id="a0f31-116">On the **Remedies for selected symptom** FastTab, add a line describing a possible solution to the problem.</span></span>

9. <span data-ttu-id="a0f31-117">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="a0f31-117">Click **Save**.</span></span>

![图 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a><span data-ttu-id="a0f31-119">查看资产故障</span><span class="sxs-lookup"><span data-stu-id="a0f31-119">View asset faults</span></span>

<span data-ttu-id="a0f31-120">在**资产故障**列表中，可概览为资产登记的所有故障。</span><span class="sxs-lookup"><span data-stu-id="a0f31-120">In the **Asset faults** list, you can get an overview of all faults registered on assets.</span></span>

<span data-ttu-id="a0f31-121">单击**资产管理** > **查询** > **资产故障** > **资产故障**打开列表。</span><span class="sxs-lookup"><span data-stu-id="a0f31-121">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults** to open the list.</span></span>


## <a name="print-asset-fault-report"></a><span data-ttu-id="a0f31-122">打印资产故障报告</span><span class="sxs-lookup"><span data-stu-id="a0f31-122">Print asset fault report</span></span>

<span data-ttu-id="a0f31-123">可从**所有资产**列表页打印资产故障报告，其中显示所有故障登记，以及故障统计信息的图形概览。</span><span class="sxs-lookup"><span data-stu-id="a0f31-123">From the **All assets** list page, you can print an asset fault report displaying all fault registrations as well as a graphic overview of fault statistics.</span></span>

1. <span data-ttu-id="a0f31-124">单击**资产管理** > **常用** > **资产** > **所有资产**。</span><span class="sxs-lookup"><span data-stu-id="a0f31-124">Click **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="a0f31-125">在**资产**列表中，选择要打印其故障报告的资产。</span><span class="sxs-lookup"><span data-stu-id="a0f31-125">In the **Assets** list, select the asset for which you want to print a fault report.</span></span>

3. <span data-ttu-id="a0f31-126">在**常规**选项卡 > **报告**部分中，单击**资产故障**。</span><span class="sxs-lookup"><span data-stu-id="a0f31-126">On the **General** tab > **Reports section**, click **Asset fault**.</span></span>

4. <span data-ttu-id="a0f31-127">插入具体期间，或选择故障类型。</span><span class="sxs-lookup"><span data-stu-id="a0f31-127">Insert a specific period, or select a fault type.</span></span>

5. <span data-ttu-id="a0f31-128">单击**确定**打印报表。</span><span class="sxs-lookup"><span data-stu-id="a0f31-128">Click **OK** to print the report.</span></span>

>[!NOTE]
><span data-ttu-id="a0f31-129">也可以通过单击**资产管理** > **报告** > **资产** > **资产故障**来打印多个资产或资产类型的故障报告。</span><span class="sxs-lookup"><span data-stu-id="a0f31-129">You can also print a fault report for several assets or asset types by clicking **Asset management** > **Reports** > **Assets** > **Asset fault**.</span></span>


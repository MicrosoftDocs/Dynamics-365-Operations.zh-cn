---
title: 自动创建服务订单
description: 您可以为某个服务协议或若干服务协议创建服务订单。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9bcb9611fd5e59cbfafbc8419a421ad0905e8b9f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001441"
---
# <a name="create-service-orders-automatically"></a><span data-ttu-id="93e40-103">自动创建服务订单</span><span class="sxs-lookup"><span data-stu-id="93e40-103">Create service orders automatically</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="93e40-104">您可以为某个服务协议或若干服务协议创建服务订单。</span><span class="sxs-lookup"><span data-stu-id="93e40-104">You can create service orders for one service agreement or for several service agreements.</span></span> <span data-ttu-id="93e40-105">在创建服务订单时，可以在 **服务订单** 窗体中查看您的服务订单。</span><span class="sxs-lookup"><span data-stu-id="93e40-105">When they are created, you can view your service orders in the **Service orders** form.</span></span>

<span data-ttu-id="93e40-106">只能为有效期间的服务协议创建服务订单。</span><span class="sxs-lookup"><span data-stu-id="93e40-106">Service orders are created only for the valid period of the service agreement.</span></span> <span data-ttu-id="93e40-107">如果您在 **创建服务订单** 窗体中指定的间隔在服务协议的开始日期间或在服务协议的结束日期后，则只能为属于该服务协议日期内的时间间隔部分创建服务订单。</span><span class="sxs-lookup"><span data-stu-id="93e40-107">If the interval that you specify in the **Create service orders** form is before the starting date or after the ending date of the service agreement, service orders are created only for the part of the interval that is within the service agreement dates.</span></span>

<span data-ttu-id="93e40-108">当您手动或自动从服务协议行创建服务订单时，该服务订单必须在该行的开始和结束日期定义的时间间隔内，除非您不指定该行的结束日期。</span><span class="sxs-lookup"><span data-stu-id="93e40-108">When you create service orders manually or automatically from the service agreement line, the service order must be in the time interval that is defined by the starting and ending dates for the line, unless you do not specify an ending date on the line.</span></span>

## <a name="create-service-orders-automatically-for-a-service-agreement"></a><span data-ttu-id="93e40-109">为服务协议自动创建服务订单</span><span class="sxs-lookup"><span data-stu-id="93e40-109">Create service orders automatically for a service agreement</span></span>

1.  <span data-ttu-id="93e40-110">单击 **服务管理** \> **常用** \> **服务协议** \> **服务协议**。</span><span class="sxs-lookup"><span data-stu-id="93e40-110">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="93e40-111">选择某一服务协议。</span><span class="sxs-lookup"><span data-stu-id="93e40-111">Select a service agreement.</span></span>

3.  <span data-ttu-id="93e40-112">单击 **交货** 选项卡，然后单击 **计划服务订单**。</span><span class="sxs-lookup"><span data-stu-id="93e40-112">Click the **Deliver** tab, and then click **Planned service orders**.</span></span>

4.  <span data-ttu-id="93e40-113">在 **开始日期** 字段和 **结束日期** 字段中指定日期，以便定义服务期间。</span><span class="sxs-lookup"><span data-stu-id="93e40-113">Specify dates in the **From date** and **To date** fields to define the service period.</span></span>

5.  <span data-ttu-id="93e40-114">选中 **显示消息日志** 复选框，以便显示创建的服务订单列表。</span><span class="sxs-lookup"><span data-stu-id="93e40-114">Select the **Show Infolog** check box to display a list of the service orders that are created.</span></span>

6.  <span data-ttu-id="93e40-115">在 **包括交易记录类型** 字段组中选择交易记录类型。</span><span class="sxs-lookup"><span data-stu-id="93e40-115">Select transaction types in the **Include transaction types** field group.</span></span> <span data-ttu-id="93e40-116">交易记录类型表示在服务协议中创建的行，并且根据在服务协议行上指定的服务间隔，您选择的每个交易记录类型都将生成若干服务订单。</span><span class="sxs-lookup"><span data-stu-id="93e40-116">The transaction types represent the lines that are created in the service agreement, and each transaction type that you select generates several service orders, depending on the service interval that is specified on the service agreement line.</span></span>

7.  <span data-ttu-id="93e40-117">若要创建在一系列连续服务订单内缺少的所有服务订单，请选中 **连续** 复选框。</span><span class="sxs-lookup"><span data-stu-id="93e40-117">To create any service orders that are missing from continuous series of service orders, select the **Continuous** check box.</span></span>

8.  <span data-ttu-id="93e40-118">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="93e40-118">Click **OK**.</span></span>

## <a name="create-service-orders-automatically-for-several-service-agreements"></a><span data-ttu-id="93e40-119">为若干服务协议自动创建服务订单</span><span class="sxs-lookup"><span data-stu-id="93e40-119">Create service orders automatically for several service agreements</span></span>

1.  <span data-ttu-id="93e40-120">单击 **服务管理** \> **定期** \> **服务订单** \> **创建服务订单**。</span><span class="sxs-lookup"><span data-stu-id="93e40-120">Click **Service management** \> **Periodic** \> **Service orders** \> **Create service orders**.</span></span>

2.  <span data-ttu-id="93e40-121">单击 **选择** 以做出选择，添加或移除要用于创建服务订单的条件。</span><span class="sxs-lookup"><span data-stu-id="93e40-121">Click **Select** to make selections to add or remove criteria to use to create service orders.</span></span>

3.  <span data-ttu-id="93e40-122">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="93e40-122">Click **OK**.</span></span>

## <a name="see-also"></a><span data-ttu-id="93e40-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="93e40-123">See also</span></span>

[<span data-ttu-id="93e40-124">服务订单</span><span class="sxs-lookup"><span data-stu-id="93e40-124">Service orders</span></span>](service-orders.md)

[<span data-ttu-id="93e40-125">自动创建服务订单</span><span class="sxs-lookup"><span data-stu-id="93e40-125">Automatically create service orders</span></span>](auto-create-service-orders.md)

  



---
title: "取消服务订单"
description: "您可以取消某一服务订单或从服务订单本身中取消服务订单行，或者您可以通过运行定期作业来取消多个服务订单。"
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 1495fa139ea2c3cb7f2450b402126822f5549f60
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---

# <a name="cancel-service-orders"></a><span data-ttu-id="2bbf0-103">取消服务订单</span><span class="sxs-lookup"><span data-stu-id="2bbf0-103">Cancel service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="2bbf0-104">您可以取消某一服务订单或从服务订单本身中取消服务订单行，或者您可以通过运行定期作业来取消多个服务订单。</span><span class="sxs-lookup"><span data-stu-id="2bbf0-104">You can cancel a service order or service order line from the service order itself, or you can cancel multiple service orders by running a periodic job.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2bbf0-105">在以下情况下不能取消服务订单：服务订单的阶段不允许取消，服务订单具有物料需求，或者服务订单已过帐。</span><span class="sxs-lookup"><span data-stu-id="2bbf0-105">Service orders cannot be canceled if the stage of the service order does not allow cancelation, if the service order has item requirements, or if the service order has already been posted.</span></span></P>


## <a name="cancel-a-service-order-in-the-service-orders-form"></a><span data-ttu-id="2bbf0-106">在“服务订单”窗体中取消服务订单</span><span class="sxs-lookup"><span data-stu-id="2bbf0-106">Cancel a service order in the Service orders form</span></span>

1.  <span data-ttu-id="2bbf0-107">单击**服务管理** \> **通用** \> **服务订单** \> **服务订单**。</span><span class="sxs-lookup"><span data-stu-id="2bbf0-107">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="2bbf0-108">选择服务订单，然后在操作窗格上单击**取消订单**。</span><span class="sxs-lookup"><span data-stu-id="2bbf0-108">Select the service order, and on the Action Pane, click **Cancel order**.</span></span>

## <a name="cancel-a-service-order-line"></a><span data-ttu-id="2bbf0-109">取消服务订单行</span><span class="sxs-lookup"><span data-stu-id="2bbf0-109">Cancel a service order line</span></span>

1.  <span data-ttu-id="2bbf0-110">单击**服务管理** \> **通用** \> **服务订单** \> **服务订单**。</span><span class="sxs-lookup"><span data-stu-id="2bbf0-110">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="2bbf0-111">双击包含要取消的服务订单。</span><span class="sxs-lookup"><span data-stu-id="2bbf0-111">Double-click the service order that contains the line you want to cancel.</span></span>

2.  <span data-ttu-id="2bbf0-112">选择您想取消的服务订单行，然后单击**取消订单行**以将该行的状态更改为 **已取消**。</span><span class="sxs-lookup"><span data-stu-id="2bbf0-112">Select the service order line that you want to cancel, and then click **Cancel order line** to change the status of the line to **Canceled**.</span></span>


> [!TIP]
> <P><span data-ttu-id="2bbf0-113">若要冲销服务订单行的取消并将状态更改回为<STRONG>已创建</STRONG> ，请单击<STRONG>撤消取消</STRONG>。</span><span class="sxs-lookup"><span data-stu-id="2bbf0-113">To reverse the cancellation of a service order line and change the status back to <STRONG>Created</STRONG>, click <STRONG>Revoke cancel</STRONG>.</span></span></P>


## <a name="cancel-multiple-service-orders"></a><span data-ttu-id="2bbf0-114">取消多个服务订单</span><span class="sxs-lookup"><span data-stu-id="2bbf0-114">Cancel multiple service orders</span></span>

1.  <span data-ttu-id="2bbf0-115">单击**服务管理** \> **定期** \> **服务订单** \> **取消服务订单**。</span><span class="sxs-lookup"><span data-stu-id="2bbf0-115">Click **Service management** \> **Periodic** \> **Service orders** \> **Cancel service orders**.</span></span>

2.  <span data-ttu-id="2bbf0-116">单击**选择**按钮。</span><span class="sxs-lookup"><span data-stu-id="2bbf0-116">Click the **Select** button.</span></span>

3.  <span data-ttu-id="2bbf0-117">在**查询**窗体的**条件**列中，选择您想要取消的服务订单。</span><span class="sxs-lookup"><span data-stu-id="2bbf0-117">In the **Inquiry** form, in the **Criteria** column, select the service orders that you want to cancel.</span></span>

4.  <span data-ttu-id="2bbf0-118">单击**确定**关闭**查询**窗体。</span><span class="sxs-lookup"><span data-stu-id="2bbf0-118">Click **OK** to close the **Inquiry** form.</span></span>

5.  <span data-ttu-id="2bbf0-119">选中**显示信息日志**复选框，以便生成列举已取消服务订单的信息日志。</span><span class="sxs-lookup"><span data-stu-id="2bbf0-119">Select the **Show Infolog** check box to generate an Infolog that lists the canceled service orders.</span></span>

6.  <span data-ttu-id="2bbf0-120">如果您想要撤消某一服务订单的**已取消**状态，则选中**撤消取消**复选框。</span><span class="sxs-lookup"><span data-stu-id="2bbf0-120">Select the **Revoke cancel** check box if you want to reverse the **Canceled** status of a service order.</span></span>

7.  <span data-ttu-id="2bbf0-121">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="2bbf0-121">Click **OK**.</span></span>

<span data-ttu-id="2bbf0-122">取消已选服务订单，或它们的进度状态**已取消**已冲销为**进行中**。</span><span class="sxs-lookup"><span data-stu-id="2bbf0-122">The selected service orders are either canceled or their progress status of **Canceled** has been reversed to **In process**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2bbf0-123">如果您选中了<STRONG>撤消取消</STRONG>复选框，将冲销进度状态为<STRONG>已取消</STRONG>的服务订单，而不会取消进度状态为<STRONG>进行中</STRONG>的服务订单。</span><span class="sxs-lookup"><span data-stu-id="2bbf0-123">If you select the <STRONG>Revoke cancel</STRONG> check box, service orders with a progress status of <STRONG>Canceled</STRONG> are reversed and service orders with a progress status of <STRONG>In process</STRONG> are not canceled.</span></span></P>


  




---
title: 手动创建服务订单
description: 您可以通过使用服务协议或通过使用**服务订单**窗体，手动创建服务订单。
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9fbcdaa50a8f13247c13c1885cdb4ab7f5f39a47
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "310913"
---
# <a name="create-service-orders-manually"></a><span data-ttu-id="0c990-103">手动创建服务订单</span><span class="sxs-lookup"><span data-stu-id="0c990-103">Create service orders manually</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="0c990-104">您可以通过使用服务协议或通过使用**服务订单**窗体，手动创建服务订单。</span><span class="sxs-lookup"><span data-stu-id="0c990-104">You can create service orders manually by using a service agreement or by using the **Service orders** form.</span></span> <span data-ttu-id="0c990-105">您还可以从项目创建服务订单。</span><span class="sxs-lookup"><span data-stu-id="0c990-105">You can also create a service order from a project.</span></span>

> [!TIP]
> <P><span data-ttu-id="0c990-106">您可以使用自动执行流程创建服务订单。</span><span class="sxs-lookup"><span data-stu-id="0c990-106">You can use automated processes to create service orders.</span></span> 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a><span data-ttu-id="0c990-107">手动从服务协议创建服务订单</span><span class="sxs-lookup"><span data-stu-id="0c990-107">Create a service order manually from a service agreement</span></span>

1.  <span data-ttu-id="0c990-108">单击**服务管理** \> **常用** \> **服务协议** \> **服务协议**。</span><span class="sxs-lookup"><span data-stu-id="0c990-108">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="0c990-109">选择某一服务协议，或者创建新的服务协议。</span><span class="sxs-lookup"><span data-stu-id="0c990-109">Select a service agreement or create a new service agreement.</span></span>

3.  <span data-ttu-id="0c990-110">单击**交货**选项卡，然后在**创建**组中单击**计划服务订单**打开**创建服务订单**窗体。</span><span class="sxs-lookup"><span data-stu-id="0c990-110">Click the **Deliver** tab and in the **Create** group click **Planned service orders** to open the **Create service orders** form.</span></span>

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a><span data-ttu-id="0c990-111">在服务订单窗体中手动创建服务订单</span><span class="sxs-lookup"><span data-stu-id="0c990-111">Create a service order manually in the Service orders form</span></span>

1.  <span data-ttu-id="0c990-112">单击**服务管理** \> **通用** \> **服务订单** \> **服务订单**。</span><span class="sxs-lookup"><span data-stu-id="0c990-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="0c990-113">按 Ctrl+N 创建新的服务订单。</span><span class="sxs-lookup"><span data-stu-id="0c990-113">Press Ctrl+N to create a new service order.</span></span>

3.  <span data-ttu-id="0c990-114">为服务订单创建服务订单行。</span><span class="sxs-lookup"><span data-stu-id="0c990-114">Create service order lines for the service order.</span></span>

> [!NOTE]
> <P><span data-ttu-id="0c990-115">如果在<STRONG>服务管理参数</STRONG>窗体中选中了<STRONG>允许，但没有服务协议</STRONG>复选框，则您可以从服务订单行过帐交易记录，而无需将服务订单附加到服务协议。</span><span class="sxs-lookup"><span data-stu-id="0c990-115">If the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form is selected, you can post the transactions from the service order lines without attaching the service order to a service agreement.</span></span> <span data-ttu-id="0c990-116">如果取消选中该复选框，则您必须将手动创建的服务订单附加到项目，然后才能过帐服务订单行。</span><span class="sxs-lookup"><span data-stu-id="0c990-116">If the check box is cleared, you must attach the manually created service order to a project before posting the service order lines.</span></span></P>

## <a name="create-a-service-order-from-a-project"></a><span data-ttu-id="0c990-117">从一个项目创建服务订单</span><span class="sxs-lookup"><span data-stu-id="0c990-117">Create a service order from a project</span></span>

1.  <span data-ttu-id="0c990-118">单击**项目管理与核算** \> **通用** \> **项目** \> **所有项目**。</span><span class="sxs-lookup"><span data-stu-id="0c990-118">Click **Project management and accounting** \> **Common** \> **Projects** \> **All projects**.</span></span>

2.  <span data-ttu-id="0c990-119">在**项目**窗体中的**操作窗格**上，单击**管理**选项卡 \> **服务** \> **服务订单**。</span><span class="sxs-lookup"><span data-stu-id="0c990-119">In the **Projects** form, on the **Action pane**, click the **Manage** tab \> click **Service** \> **Service orders**.</span></span>

3.  <span data-ttu-id="0c990-120">按照前面的过程执行，以便在**服务订单**窗体中手动创建某一服务订单。</span><span class="sxs-lookup"><span data-stu-id="0c990-120">Follow the previous procedure to create a service order manually in the **Service orders** form.</span></span> <span data-ttu-id="0c990-121">**项目 ID** 字段显示项目参考。</span><span class="sxs-lookup"><span data-stu-id="0c990-121">The **Project ID** field displays the project reference.</span></span>

> [!NOTE]
> <P><span data-ttu-id="0c990-122">如果在<STRONG>服务管理参数</STRONG>窗体中选中了<STRONG>允许，但没有服务协议</STRONG>复选框，则您可以从服务订单行过帐交易记录，而无需将服务订单附加到服务协议。</span><span class="sxs-lookup"><span data-stu-id="0c990-122">If the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form is selected, you can post the transactions from the service order lines without attaching the service order to a service agreement.</span></span> <span data-ttu-id="0c990-123">如果取消选中该复选框，则您必须将手动创建的服务订单附加到项目，然后才能过帐服务订单行。</span><span class="sxs-lookup"><span data-stu-id="0c990-123">If the check box is cleared, you must attach the manually created service order to a project before posting the service order lines.</span></span></P>

## <a name="create-a-service-order-from-the-sales-order-form"></a><span data-ttu-id="0c990-124">从销售订单窗体创建一个服务订单</span><span class="sxs-lookup"><span data-stu-id="0c990-124">Create a service order from the Sales order form</span></span>

<span data-ttu-id="0c990-125">可使用**基于销售订单创建新的服务订单**向导从**服务订单**窗体创建服务订单。</span><span class="sxs-lookup"><span data-stu-id="0c990-125">You can create a service order from the **Sales orders** form by using the **Create a new service order based on the sales order** wizard.</span></span>

1.  <span data-ttu-id="0c990-126">单击**销售和市场营销** \> **通用** \> **销售订单** \> **所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="0c990-126">Click **Sales and marketing** \> **Common** \> **Sales orders** \> **All sales orders**.</span></span>

2.  <span data-ttu-id="0c990-127">打开相关销售订单。</span><span class="sxs-lookup"><span data-stu-id="0c990-127">Open the relevant sales order.</span></span>

3.  <span data-ttu-id="0c990-128">在**销售订单**选项卡上，单击**服务订单**启动**基于销售订单创建新的服务订单**向导。</span><span class="sxs-lookup"><span data-stu-id="0c990-128">On the **Sales order** tab, click **Service order** to start the **Create a new service order based on the sales order** wizard.</span></span>

4.  <span data-ttu-id="0c990-129">单击**下一步 \>**，然后在**选择服务订单关联的协议**页上完成以下步骤：</span><span class="sxs-lookup"><span data-stu-id="0c990-129">Click **Next \>**, and then complete the following steps on the **Select agreement for service order** page:</span></span>
    
      - <span data-ttu-id="0c990-130">使用**服务协议**字段可以选择新的服务订单应与之关联的服务协议。</span><span class="sxs-lookup"><span data-stu-id="0c990-130">Use the **Service agreement** field to select the service agreement with which the new service order should be associated.</span></span>
    
      - <span data-ttu-id="0c990-131">可选：使用**项目 ID** 字段可以将此服务订单与特定项目相关联。</span><span class="sxs-lookup"><span data-stu-id="0c990-131">Optional: Use the **Project ID** field to associate this service order with a particular project.</span></span>

5.  <span data-ttu-id="0c990-132">单击**下一步 \>**，然后在**创建服务订单**页上完成以下步骤：</span><span class="sxs-lookup"><span data-stu-id="0c990-132">Click **Next \>**, and then complete the following steps on the **Create service order** page:</span></span>
    
      - <span data-ttu-id="0c990-133">在**首选服务时间**字段中输入服务电话要开始的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="0c990-133">Enter a date and time for the service call to begin in the **Preferred service time** field.</span></span>
    
      - <span data-ttu-id="0c990-134">可选：修改**说明**字段中的文本。</span><span class="sxs-lookup"><span data-stu-id="0c990-134">Optional: Modify the text in the **Description** field.</span></span> <span data-ttu-id="0c990-135">默认情况下，此字段包含您在前一页上选择的服务协议的描述。</span><span class="sxs-lookup"><span data-stu-id="0c990-135">By default, this field contains the description of the service agreement that you selected on the previous page.</span></span>
    
      - <span data-ttu-id="0c990-136">在**负责人**字段中，选择负责该协议的员工的 ID；并且如果您知道，输入该服务电话的客户首选技术人员的 ID。</span><span class="sxs-lookup"><span data-stu-id="0c990-136">In the **Responsible** field, select the ID of the employee who is responsible for the agreement, and if you know what it is, enter the ID of the customer's preferred technician for the service call.</span></span>
    
      - <span data-ttu-id="0c990-137">在**联系人 ID** 字段，选择客户公司中应针对此服务订单与之联系的人员。</span><span class="sxs-lookup"><span data-stu-id="0c990-137">In the **Contact ID** field, select the person in the customer's company who should be contacted regarding this service order.</span></span>

6.  <span data-ttu-id="0c990-138">单击**下一步\>**，然后单击**完成**。</span><span class="sxs-lookup"><span data-stu-id="0c990-138">Click **Next \>**, and then click **Finish**.</span></span>


## <a name="see-also"></a><span data-ttu-id="0c990-139">请参阅</span><span class="sxs-lookup"><span data-stu-id="0c990-139">See also</span></span>

[<span data-ttu-id="0c990-140">服务订单</span><span class="sxs-lookup"><span data-stu-id="0c990-140">Service orders</span></span>](service-orders.md)

[<span data-ttu-id="0c990-141">自动创建服务订单</span><span class="sxs-lookup"><span data-stu-id="0c990-141">Create service orders automatically</span></span>](create-service-orders-automatically.md)

<span data-ttu-id="0c990-142">[创建服务订单（类窗体）](https://technet.microsoft.com/en-us/library/aa553901\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="0c990-142">[Create service orders (class form)](https://technet.microsoft.com/en-us/library/aa553901\(v=ax.60\))</span></span> 


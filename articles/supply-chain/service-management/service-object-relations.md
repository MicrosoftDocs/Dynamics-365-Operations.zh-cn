---
title: 服务对象关系
description: 您可以在服务对象和服务协议或服务订单之间创建服务对象关系。
author: ShylaThompson
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectRelation
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 03047b3eccf3c90d4cf7426ddaec83f10dbea1b0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "314363"
---
# <a name="service-object-relations"></a><span data-ttu-id="91f85-103">服务对象关系</span><span class="sxs-lookup"><span data-stu-id="91f85-103">Service object relations</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="91f85-104">您可以在服务对象和服务协议或服务订单之间创建服务对象关系。</span><span class="sxs-lookup"><span data-stu-id="91f85-104">You can create service object relations between a service object and a service agreement or service order.</span></span> <span data-ttu-id="91f85-105">在您创建某一关系时，将服务对象附加到服务协议或服务订单。</span><span class="sxs-lookup"><span data-stu-id="91f85-105">When you create a relation, you attach the service object to the service agreement or service order.</span></span>

<span data-ttu-id="91f85-106">在创建该关系后，您可以将服务对象附加到服务协议或服务订单上的任何行。</span><span class="sxs-lookup"><span data-stu-id="91f85-106">After the relation is created, you can attach the service object to any lines on the service agreement or service order.</span></span>

## <a name="template-boms"></a><span data-ttu-id="91f85-107">物料清单模板</span><span class="sxs-lookup"><span data-stu-id="91f85-107">Template BOMs</span></span>

<span data-ttu-id="91f85-108">您还可为对象关系指定物料清单模板。</span><span class="sxs-lookup"><span data-stu-id="91f85-108">You can also specify a template BOM for the object relation.</span></span> <span data-ttu-id="91f85-109">物料清单模板是您对其执行服务的对象的物料清单。</span><span class="sxs-lookup"><span data-stu-id="91f85-109">The template BOM is a bill of materials for the object on which you perform service.</span></span> <span data-ttu-id="91f85-110">如果您在执行服务的过程中更换了服务对象的某一组件部分，则可以通过使用“服务对象”窗体在服务物料清单中登记此更改。</span><span class="sxs-lookup"><span data-stu-id="91f85-110">If you replace a component part of the service object during a service visit, you can register this change in the service BOM by using the Service objects form.</span></span>

## <a name="example"></a><span data-ttu-id="91f85-111">示例</span><span class="sxs-lookup"><span data-stu-id="91f85-111">Example</span></span>

<span data-ttu-id="91f85-112">您针对在客户站点为两台电梯提供的服务创建了一个服务协议。</span><span class="sxs-lookup"><span data-stu-id="91f85-112">You create a service agreement for servicing two elevators at a customer site.</span></span>
<span data-ttu-id="91f85-113">该服务协议的 ID 标识符为 SAL-001。</span><span class="sxs-lookup"><span data-stu-id="91f85-113">The service agreement has the identifier ID SAL-001.</span></span>

<span data-ttu-id="91f85-114">这两台电梯在“服务对象”窗体中分别作为 EL-S/1000 对象和 EL-L/1000 对象设置。</span><span class="sxs-lookup"><span data-stu-id="91f85-114">The elevators are set up in the Service objects form as objects, EL-S/1000 and EL-L/1000.</span></span>

<span data-ttu-id="91f85-115">您将这两个服务对象（EL-S/1000 和 EL-L/1000）附加到该服务协议。</span><span class="sxs-lookup"><span data-stu-id="91f85-115">You attach the service objects, EL-S/1000 and EL-L/1000, to the service agreement.</span></span>

<span data-ttu-id="91f85-116">您想要在物料清单中登记服务对象的更改，因为您更换了该对象的组件部分；因此，您将某一服务物料清单附加到该服务对象关系，如下表中所述。</span><span class="sxs-lookup"><span data-stu-id="91f85-116">You want to register changes in the BOM for the service object as you replace component parts of the object, so you attach a service BOM to the service object relation, as described in the following table.</span></span>

| <span data-ttu-id="91f85-117">服务对象</span><span class="sxs-lookup"><span data-stu-id="91f85-117">Service object</span></span> | <span data-ttu-id="91f85-118">关系 – 服务协议</span><span class="sxs-lookup"><span data-stu-id="91f85-118">Relation – Service agreement</span></span> | <span data-ttu-id="91f85-119">服务物料清单</span><span class="sxs-lookup"><span data-stu-id="91f85-119">Service BOM</span></span>   |
|----------------|------------------------------|---------------|
| <span data-ttu-id="91f85-120">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="91f85-120">EL-S/1000</span></span>      | <span data-ttu-id="91f85-121">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="91f85-121">ID SAL-001</span></span>                   | <span data-ttu-id="91f85-122">BOM-EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="91f85-122">BOM-EL-S/1000</span></span> |
| <span data-ttu-id="91f85-123">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="91f85-123">EL-L/1000</span></span>      | <span data-ttu-id="91f85-124">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="91f85-124">ID SAL-001</span></span>                   | <span data-ttu-id="91f85-125">BOM-EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="91f85-125">BOM-EL-L/1000</span></span> |

<span data-ttu-id="91f85-126">因为存在该协议的服务对象关系，所以您现在可以创建服务协议行，行中具有下表中显示的这些对象。</span><span class="sxs-lookup"><span data-stu-id="91f85-126">Because there are service object relations for the agreement, you can now create service agreement lines with these objects, as shown in the following table.</span></span>

| <span data-ttu-id="91f85-127">交易记录类型</span><span class="sxs-lookup"><span data-stu-id="91f85-127">Transaction type</span></span> | <span data-ttu-id="91f85-128">类别</span><span class="sxs-lookup"><span data-stu-id="91f85-128">Category</span></span>           | <span data-ttu-id="91f85-129">服务对象</span><span class="sxs-lookup"><span data-stu-id="91f85-129">Service object</span></span> |
|------------------|--------------------|----------------|
| <span data-ttu-id="91f85-130">工时</span><span class="sxs-lookup"><span data-stu-id="91f85-130">Hour</span></span>             | <span data-ttu-id="91f85-131">检查</span><span class="sxs-lookup"><span data-stu-id="91f85-131">Inspection</span></span>         | <span data-ttu-id="91f85-132">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="91f85-132">EL-S/1000</span></span>      |
| <span data-ttu-id="91f85-133">工时</span><span class="sxs-lookup"><span data-stu-id="91f85-133">Hour</span></span>             | <span data-ttu-id="91f85-134">变速箱清洁</span><span class="sxs-lookup"><span data-stu-id="91f85-134">Gear box cleaning</span></span>  | <span data-ttu-id="91f85-135">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="91f85-135">EL-S/1000</span></span>      |
| <span data-ttu-id="91f85-136">物料</span><span class="sxs-lookup"><span data-stu-id="91f85-136">Item</span></span>             | <span data-ttu-id="91f85-137">清洁材料</span><span class="sxs-lookup"><span data-stu-id="91f85-137">Cleaning materials</span></span> | <span data-ttu-id="91f85-138">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="91f85-138">EL-S/1000</span></span>      |
| <span data-ttu-id="91f85-139">工时</span><span class="sxs-lookup"><span data-stu-id="91f85-139">Hour</span></span>             | <span data-ttu-id="91f85-140">检查</span><span class="sxs-lookup"><span data-stu-id="91f85-140">Inspection</span></span>         | <span data-ttu-id="91f85-141">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="91f85-141">EL-L/1000</span></span>      |
| <span data-ttu-id="91f85-142">工时</span><span class="sxs-lookup"><span data-stu-id="91f85-142">Hour</span></span>             | <span data-ttu-id="91f85-143">变速箱清洁</span><span class="sxs-lookup"><span data-stu-id="91f85-143">Gearbox cleaning</span></span>   | <span data-ttu-id="91f85-144">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="91f85-144">EL-L/1000</span></span>      |
| <span data-ttu-id="91f85-145">物料</span><span class="sxs-lookup"><span data-stu-id="91f85-145">Item</span></span>             | <span data-ttu-id="91f85-146">清洁材料</span><span class="sxs-lookup"><span data-stu-id="91f85-146">Cleaning materials</span></span> | <span data-ttu-id="91f85-147">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="91f85-147">EL-L/1000</span></span>      |

<span data-ttu-id="91f85-148">在登门服务期间，您必须更换电梯 EL-S/1000 的变速箱。</span><span class="sxs-lookup"><span data-stu-id="91f85-148">On a service visit, you have to replace the gearbox for elevator EL-S/1000.</span></span> <span data-ttu-id="91f85-149">为了更换该对象的零部件，您可以通过使用为当前服务协议设置的服务对象关系访问物料清单设计器。</span><span class="sxs-lookup"><span data-stu-id="91f85-149">To replace a component part of the object, you can access the BOM Designer by using the service object relation that you set up for the current service agreement.</span></span>

<span data-ttu-id="91f85-150">通过使用服务对象关系访问物料清单设计器</span><span class="sxs-lookup"><span data-stu-id="91f85-150">Access the BOM Designer by using a service object relation</span></span>

1. <span data-ttu-id="91f85-151">服务协议</span><span class="sxs-lookup"><span data-stu-id="91f85-151">Service agreements</span></span>
2. <span data-ttu-id="91f85-152">双击某个服务协议，或单击“服务协议”以创建一个服务协议。</span><span class="sxs-lookup"><span data-stu-id="91f85-152">Double-click a service agreement, or click Service agreement to create a service agreement.</span></span>
3. <span data-ttu-id="91f85-153">单击“设置”选项卡。</span><span class="sxs-lookup"><span data-stu-id="91f85-153">Click the Setup tab.</span></span>
4. <span data-ttu-id="91f85-154">若要将某一物料清单模板附加到该服务协议，请单击“服务对象”。</span><span class="sxs-lookup"><span data-stu-id="91f85-154">Click Service objects to attach a template BOM to the service agreement.</span></span>
5. <span data-ttu-id="91f85-155">在“服务对象”窗体中，单击“设计器”打开“设计器”窗体以修改模板“物料清单”。</span><span class="sxs-lookup"><span data-stu-id="91f85-155">In the Service objects form, click Designer to open the Designer form to modify the template BOM.</span></span>

## <a name="automatically-created-service-orders"></a><span data-ttu-id="91f85-156">自动创建了服务订单</span><span class="sxs-lookup"><span data-stu-id="91f85-156">Automatically created service orders</span></span>

<span data-ttu-id="91f85-157">如果为某一服务协议自动创建服务订单，则该协议中的服务对象关系也处于已创建的服务订单中。</span><span class="sxs-lookup"><span data-stu-id="91f85-157">If you automatically create service orders for a service agreement, the service object relations in the agreement are also created in the service orders.</span></span>


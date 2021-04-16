---
title: 故障管理
description: 本主题介绍资产管理中的故障管理。
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetFaultArea, EntAssetFaultDesigner, EntAssetFaultCopyFromObjectType, EntAssetFaultRemedy, EntAssetObjectFaultRelationRequestInfoPart, EntAssetObjectFaultRelationWorkOrderInfoPart, EntAssetFaultCreateCombinations, EntAssetObjectFaultSymptom, EntAssetObjectFaultSymptomListPage, EntAssetFaultType, EntAssetFaultSymptom, EntAssetFaultCause
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c87bfa057fd2808551674f2acb9d654ad47e9a42
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825654"
---
# <a name="fault-management"></a><span data-ttu-id="85654-103">故障管理</span><span class="sxs-lookup"><span data-stu-id="85654-103">Fault management</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="85654-104">在资产管理中，可使用故障设计器为资产故障设置故障特征、故障区域和故障类型。</span><span class="sxs-lookup"><span data-stu-id="85654-104">In Asset Management, you can use the fault designer to set up fault symptoms, fault areas, and fault types on asset types.</span></span> <span data-ttu-id="85654-105">这样就可以管理为资产检测到的故障。</span><span class="sxs-lookup"><span data-stu-id="85654-105">In this way, you can manage faults that are detected on assets.</span></span> <span data-ttu-id="85654-106">此外，还可以为工作订单登记故障成因和有关解决故障的建议。</span><span class="sxs-lookup"><span data-stu-id="85654-106">Additionally, fault causes and suggestions for fixing faults can be registered on a work order.</span></span>

<span data-ttu-id="85654-107">故障登记和管理流程包含以下步骤。</span><span class="sxs-lookup"><span data-stu-id="85654-107">The process for fault registration and management consists of these steps.</span></span>

1. <span data-ttu-id="85654-108">创建资产类型可能出现的故障特征、故障区域和故障类型的列表。</span><span class="sxs-lookup"><span data-stu-id="85654-108">Create a list of fault symptoms, fault areas, and fault types that might occur on your asset types.</span></span>
2. <span data-ttu-id="85654-109">在故障设计器中，设置特征、故障区域和故障类型。</span><span class="sxs-lookup"><span data-stu-id="85654-109">In the fault designer, set up symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="85654-110">下面这些示例可帮助您理解故障特征、故障区域和故障类型之间的区别。</span><span class="sxs-lookup"><span data-stu-id="85654-110">Here are some examples to help you understand the difference between fault symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="85654-111">**故障特征：**</span><span class="sxs-lookup"><span data-stu-id="85654-111">**Fault symptoms:**</span></span>

- <span data-ttu-id="85654-112">电压不平衡s</span><span class="sxs-lookup"><span data-stu-id="85654-112">Unbalanced voltages</span></span>
- <span data-ttu-id="85654-113">短路</span><span class="sxs-lookup"><span data-stu-id="85654-113">Short circuit</span></span>
- <span data-ttu-id="85654-114">噪声</span><span class="sxs-lookup"><span data-stu-id="85654-114">Noise</span></span>
- <span data-ttu-id="85654-115">泄漏</span><span class="sxs-lookup"><span data-stu-id="85654-115">Leak</span></span>
- <span data-ttu-id="85654-116">振动</span><span class="sxs-lookup"><span data-stu-id="85654-116">Vibrations</span></span>

<span data-ttu-id="85654-117">**故障区域：**</span><span class="sxs-lookup"><span data-stu-id="85654-117">**Fault areas:**</span></span>

- <span data-ttu-id="85654-118">电</span><span class="sxs-lookup"><span data-stu-id="85654-118">Electrical</span></span>
- <span data-ttu-id="85654-119">机械</span><span class="sxs-lookup"><span data-stu-id="85654-119">Mechanical</span></span>
- <span data-ttu-id="85654-120">水力</span><span class="sxs-lookup"><span data-stu-id="85654-120">Hydraulic</span></span>
- <span data-ttu-id="85654-121">气动</span><span class="sxs-lookup"><span data-stu-id="85654-121">Pneumatic</span></span>

<span data-ttu-id="85654-122">**故障类型：**</span><span class="sxs-lookup"><span data-stu-id="85654-122">**Fault types:**</span></span>

- <span data-ttu-id="85654-123">主定子绕组故障</span><span class="sxs-lookup"><span data-stu-id="85654-123">Faulty main stator winding</span></span>
- <span data-ttu-id="85654-124">二级管故障</span><span class="sxs-lookup"><span data-stu-id="85654-124">Faulty diode</span></span>
- <span data-ttu-id="85654-125">绕组脏</span><span class="sxs-lookup"><span data-stu-id="85654-125">Dirty windings</span></span>
- <span data-ttu-id="85654-126">发电机有缺陷</span><span class="sxs-lookup"><span data-stu-id="85654-126">Defective generator</span></span>
- <span data-ttu-id="85654-127">传感器有缺陷</span><span class="sxs-lookup"><span data-stu-id="85654-127">Defective sensor</span></span>

## <a name="create-fault-symptoms"></a><span data-ttu-id="85654-128">创建故障特征</span><span class="sxs-lookup"><span data-stu-id="85654-128">Create fault symptoms</span></span>

<span data-ttu-id="85654-129">执行以下步骤创建可在故障设计器中使用的特征的列表。</span><span class="sxs-lookup"><span data-stu-id="85654-129">Follow these steps to create a list of symptoms that can be used in the fault designer.</span></span>

1. <span data-ttu-id="85654-130">选择 **资产管理** \> **设置** \> **故障** \> **故障特征**。</span><span class="sxs-lookup"><span data-stu-id="85654-130">Select **Asset management** \> **Setup** \> **Fault** \> **Fault symptoms**.</span></span>
2. <span data-ttu-id="85654-131">选择 **新建** 创建记录。</span><span class="sxs-lookup"><span data-stu-id="85654-131">Select **New** to create a record.</span></span>
3. <span data-ttu-id="85654-132">在 **故障特征** 字段中，输入故障特征的名称。</span><span class="sxs-lookup"><span data-stu-id="85654-132">In the **Fault symptom** field, enter a name for the fault symptom.</span></span>
4. <span data-ttu-id="85654-133">在 **描述** 字段中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="85654-133">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="85654-134">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="85654-134">Select **Save**.</span></span>

## <a name="create-fault-areas"></a><span data-ttu-id="85654-135">创建故障区域</span><span class="sxs-lookup"><span data-stu-id="85654-135">Create fault areas</span></span>

<span data-ttu-id="85654-136">执行以下步骤创建可在故障设计器中使用的区域或位置的列表。</span><span class="sxs-lookup"><span data-stu-id="85654-136">Follow these steps to create a list of areas or locations that can be used in the fault designer.</span></span>

1. <span data-ttu-id="85654-137">选择 **资产管理** \> **设置** \> **故障** \> **故障区域**。</span><span class="sxs-lookup"><span data-stu-id="85654-137">Select **Asset management** \> **Setup** \> **Fault** \> **Fault areas**.</span></span>
2. <span data-ttu-id="85654-138">选择 **新建** 创建记录。</span><span class="sxs-lookup"><span data-stu-id="85654-138">Select **New** to create a record.</span></span>
3. <span data-ttu-id="85654-139">在 **故障区域** 字段中，输入故障区域的名称。</span><span class="sxs-lookup"><span data-stu-id="85654-139">In the **Fault area** field, enter a name for the fault area.</span></span>
4. <span data-ttu-id="85654-140">在 **描述** 字段中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="85654-140">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="85654-141">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="85654-141">Select **Save**.</span></span>

## <a name="create-fault-types"></a><span data-ttu-id="85654-142">创建故障类型</span><span class="sxs-lookup"><span data-stu-id="85654-142">Create fault types</span></span>

<span data-ttu-id="85654-143">执行以下步骤创建可在故障设计器中使用的故障类型的列表。</span><span class="sxs-lookup"><span data-stu-id="85654-143">Follow these steps to create a list of fault types that can be used in the fault designer.</span></span>

1. <span data-ttu-id="85654-144">选择 **资产管理** \> **设置** \> **故障** \> **故障类型**。</span><span class="sxs-lookup"><span data-stu-id="85654-144">Select **Asset management** \> **Setup** \> **Fault** \> **Fault types**.</span></span>
2. <span data-ttu-id="85654-145">选择 **新建** 创建记录。</span><span class="sxs-lookup"><span data-stu-id="85654-145">Select **New** to create a record.</span></span>
3. <span data-ttu-id="85654-146">在 **故障类型** 字段中，输入故障类型的名称。</span><span class="sxs-lookup"><span data-stu-id="85654-146">In the **Fault type** field, enter a name for the fault type.</span></span>
4. <span data-ttu-id="85654-147">在 **描述** 字段中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="85654-147">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="85654-148">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="85654-148">Select **Save**.</span></span>

## <a name="set-up-the-fault-designer"></a><span data-ttu-id="85654-149">设置故障设计器</span><span class="sxs-lookup"><span data-stu-id="85654-149">Set up the fault designer</span></span>

<span data-ttu-id="85654-150">可以在故障设计器中为资产类型设置故障数据。</span><span class="sxs-lookup"><span data-stu-id="85654-150">In the fault designer, you set up fault data on asset types.</span></span>

1. <span data-ttu-id="85654-151">选择 **资产管理** \> **设置** \> **故障** \> **故障设计器**。</span><span class="sxs-lookup"><span data-stu-id="85654-151">Select **Asset management** \> **Setup** \> **Fault** \> **Fault designer**.</span></span>
2. <span data-ttu-id="85654-152">在左窗格中，选择要为其设置故障记录的资产的类型。</span><span class="sxs-lookup"><span data-stu-id="85654-152">In the left pane, select the type of asset to set up a fault record for.</span></span>
3. <span data-ttu-id="85654-153">在 **故障特征** 快速选项卡上，选择 **添加行**，然后在 **故障特征** 字段中选择故障特征。</span><span class="sxs-lookup"><span data-stu-id="85654-153">On the **Fault symptom** FastTab, select **Add line**, and then, in the **Fault symptom** field, select a fault symptom.</span></span>
4. <span data-ttu-id="85654-154">在 **故障区域** 快速选项卡上，选择 **添加行**，然后在 **故障区域** 字段中选择故障区域。</span><span class="sxs-lookup"><span data-stu-id="85654-154">On the **Fault area** FastTab, select **Add line**, and then, in the **Fault area** field select a fault area.</span></span>
5. <span data-ttu-id="85654-155">在 **故障类型** 快速选项卡上，选择 **添加行**，然后在 **故障类型** 字段中选择故障类型。</span><span class="sxs-lookup"><span data-stu-id="85654-155">On the **Fault type** FastTab, select **Add line**, and then, in the **Fault type** field, select a fault type.</span></span>
6. <span data-ttu-id="85654-156">若要快速创建所选资产类型的所有现有故障特征、区域和类型的组合，请选择 **创建故障组合**。</span><span class="sxs-lookup"><span data-stu-id="85654-156">To quickly create combinations of all existing fault symptoms, areas, and types for the selected asset type, select **Create fault combinations**.</span></span> <span data-ttu-id="85654-157">如果已经添加了大量故障特征、区域和类型，此功能非常有用。</span><span class="sxs-lookup"><span data-stu-id="85654-157">This function is useful if you've added many fault symptoms, areas, and types.</span></span> <span data-ttu-id="85654-158">相比手动创建新行，删除与资产类型无关的任何组合更容易。</span><span class="sxs-lookup"><span data-stu-id="85654-158">It's easier to delete the lines for any combinations that aren't relevant to the asset type than to create new lines manually.</span></span>

    > [!NOTE]
    > <span data-ttu-id="85654-159">若要将故障特征、区域和类型的设置从一个资产类型复制到所选资产类型，请选择 **从资产类型复制**。</span><span class="sxs-lookup"><span data-stu-id="85654-159">To copy the setup of fault symptoms, areas, and types from one asset type to the selected asset type, select **Copy from asset type**.</span></span>

7. <span data-ttu-id="85654-160">选择 **保存** 以保存您的更改。</span><span class="sxs-lookup"><span data-stu-id="85654-160">Select **Save** to save your changes.</span></span>

![故障设计器页面](media/21-setup-for-work-orders.png)

## <a name="create-fault-causes"></a><span data-ttu-id="85654-162">创建故障成因</span><span class="sxs-lookup"><span data-stu-id="85654-162">Create fault causes</span></span>

<span data-ttu-id="85654-163">执行以下步骤，以便创建可添加到工作订单或维护请求的已知故障成因的列表。</span><span class="sxs-lookup"><span data-stu-id="85654-163">Follow these steps to create a list of known fault causes that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="85654-164">选择 **资产管理** \> **设置** \> **故障** \> **故障成因**。</span><span class="sxs-lookup"><span data-stu-id="85654-164">Select **Asset management** \> **Setup** \> **Fault** \> **Fault causes**.</span></span>
2. <span data-ttu-id="85654-165">选择 **新建** 创建记录。</span><span class="sxs-lookup"><span data-stu-id="85654-165">Select **New** to create a record.</span></span>
3. <span data-ttu-id="85654-166">在 **故障成因** 字段中，输入故障成因的名称。</span><span class="sxs-lookup"><span data-stu-id="85654-166">In the **Fault cause** field, enter a name for the fault cause.</span></span>
4. <span data-ttu-id="85654-167">在 **描述** 字段中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="85654-167">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="85654-168">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="85654-168">Select **Save**.</span></span>

## <a name="create-fault-remedies"></a><span data-ttu-id="85654-169">创建故障补救措施</span><span class="sxs-lookup"><span data-stu-id="85654-169">Create fault remedies</span></span>

<span data-ttu-id="85654-170">执行以下步骤，以便创建可添加到工作订单或维护请求的补救措施和修复建议的列表。</span><span class="sxs-lookup"><span data-stu-id="85654-170">Follow these steps to create a list of suggestions for remedy and repair that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="85654-171">选择 **资产管理** \> **设置** \> **故障** \> **故障补救措施**。</span><span class="sxs-lookup"><span data-stu-id="85654-171">Select **Asset management** \> **Setup** \> **Fault** \> **Fault remedies**.</span></span>
2. <span data-ttu-id="85654-172">选择 **新建** 创建记录。</span><span class="sxs-lookup"><span data-stu-id="85654-172">Select **New** to create a record.</span></span>
3. <span data-ttu-id="85654-173">在 **故障补救措施** 字段中，输入故障补救措施的名称。</span><span class="sxs-lookup"><span data-stu-id="85654-173">In the **Fault remedy** field, enter a name for the fault remedy.</span></span>
4. <span data-ttu-id="85654-174">在 **描述** 字段中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="85654-174">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="85654-175">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="85654-175">Select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="85654-176">可根据需要更改故障特征、区域、类型、成因和补救措施的名称。</span><span class="sxs-lookup"><span data-stu-id="85654-176">You can change the names of your fault symptoms, areas, types, causes, and remedies as you require.</span></span> <span data-ttu-id="85654-177">将在关联的故障登记中自动体现名称的变化。</span><span class="sxs-lookup"><span data-stu-id="85654-177">The name changes are automatically reflected in the related fault registrations.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
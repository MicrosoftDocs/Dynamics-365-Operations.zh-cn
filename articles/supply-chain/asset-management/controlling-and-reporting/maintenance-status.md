---
title: 维护状态
description: 本主题说明如何在资产管理中计算维护状态。
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetStatusCalculate, EntAssetStatus
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0f65bfc7b5ef9651853a12bab2ed83dbb8562ba6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253726"
---
# <a name="maintenance-status"></a><span data-ttu-id="8ab85-103">维护状态</span><span class="sxs-lookup"><span data-stu-id="8ab85-103">Maintenance status</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="8ab85-104">在资产管理中，您可以针对新的、有效的和已完成的维护请求、工作订单和维护停机时间活动，在特定期间进行概览计算。</span><span class="sxs-lookup"><span data-stu-id="8ab85-104">In Asset Management, you can make an overview calculation for a specific period for new, active, and completed maintenance requests, work orders, and maintenance downtime activities.</span></span> <span data-ttu-id="8ab85-105">也可以查看同一期间的已完成条件评估数量。</span><span class="sxs-lookup"><span data-stu-id="8ab85-105">You can also see the number of completed condition assessments for the same period.</span></span> <span data-ttu-id="8ab85-106">可使用此计算获取传入的和已完成的维护请求和工作订单的工作负载的概览。</span><span class="sxs-lookup"><span data-stu-id="8ab85-106">Use this calculation to get an overview of workload for incoming and completed maintenance requests and work orders.</span></span>

## <a name="make-a-maintenance-status-calculation"></a><span data-ttu-id="8ab85-107">创建维护状态计算</span><span class="sxs-lookup"><span data-stu-id="8ab85-107">Make a maintenance status calculation</span></span>

1. <span data-ttu-id="8ab85-108">单击 **资产管理** > **查询** > **维护状态**。</span><span class="sxs-lookup"><span data-stu-id="8ab85-108">Click **Asset management** > **Inquiries** > **Maintenance status**.</span></span>

2. <span data-ttu-id="8ab85-109">在 **计算状态** 对话框的 **开始日期** 和 **结束日期** 字段中选择要进行计算的时间范围。</span><span class="sxs-lookup"><span data-stu-id="8ab85-109">In the **Calculate status** dialog, select the time range that you want to make the calculation in the **From date** and **To date** fields.</span></span>

3. <span data-ttu-id="8ab85-110">可使用 **级别** 字段指示要与功能位置有关的维护行的详细程度。</span><span class="sxs-lookup"><span data-stu-id="8ab85-110">You can use the **Level** field to indicate how detailed you want the maintenance lines to be regarding functional locations.</span></span> 

  <span data-ttu-id="8ab85-111">例如，如果在字段中插入数字“1”，并且采用了多级别功能位置结构，则将在最上级别显示某个功能位置的所有维护安排行，因此，可以从较低级别的功能位置叠加行中的状态。</span><span class="sxs-lookup"><span data-stu-id="8ab85-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance lines for a functional location will be shown on the top level, and therefore the status on a line may be added up from functional locations located at a lower level.</span></span> 
  
  <span data-ttu-id="8ab85-112">如果在 **级别** 字段中插入数字“0”，将看到详细结果，其中显示其关联的所有功能位置级别的所有维护行。</span><span class="sxs-lookup"><span data-stu-id="8ab85-112">If you insert the number "0" in the **Level** field, you see a detailed result showing all maintenance lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="8ab85-113">单击 **确定** 开始计算。</span><span class="sxs-lookup"><span data-stu-id="8ab85-113">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="8ab85-114">单击 **分组依据** 按钮显示所需的计算详细程度。</span><span class="sxs-lookup"><span data-stu-id="8ab85-114">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="8ab85-115">将突出显示所选 **分组依据** 按钮。</span><span class="sxs-lookup"><span data-stu-id="8ab85-115">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="8ab85-116">单击按钮将其激活或停用。</span><span class="sxs-lookup"><span data-stu-id="8ab85-116">Click on a button to activate or deactivate it.</span></span>

6. <span data-ttu-id="8ab85-117">每次通过激活或停用 **分组依据** 按钮或通过为新期间创建计算来进行更改时，都应该单击 **更新** 按钮以更新计算。</span><span class="sxs-lookup"><span data-stu-id="8ab85-117">Remember to click the **Update** button to update the calculation each time you make changes by activating or deactivating **Group by** buttons, or by making a calculation for a new period.</span></span>

7. <span data-ttu-id="8ab85-118">如果要创建新的维护状态计算，请单击 **状态**。</span><span class="sxs-lookup"><span data-stu-id="8ab85-118">Click **Status** if you want to create a new maintenance status calculation.</span></span>

>[!NOTE]
><span data-ttu-id="8ab85-119">**维护状态** 中显示的结果仅包括具有实际开始日期和时间的维护请求和工作订单。</span><span class="sxs-lookup"><span data-stu-id="8ab85-119">The results shown in **Maintenance status** only include maintenance requests and work orders that have an actual start date and time.</span></span> <span data-ttu-id="8ab85-120">结束日期和时间可以为空。</span><span class="sxs-lookup"><span data-stu-id="8ab85-120">End date and time may be blank.</span></span>

## <a name="example-1"></a><span data-ttu-id="8ab85-121">示例 1</span><span class="sxs-lookup"><span data-stu-id="8ab85-121">Example 1</span></span>

<span data-ttu-id="8ab85-122">在下面的屏幕截图中，已激活 **年** 和 **月** 按钮。</span><span class="sxs-lookup"><span data-stu-id="8ab85-122">In the screenshot below, the **Year** and **Month** buttons have been activated.</span></span> <span data-ttu-id="8ab85-123">选择这些 **分组依据** 选项后，您将获取基于与维护请求和工作订单关联的月工作负载和吞吐量的一般概览。</span><span class="sxs-lookup"><span data-stu-id="8ab85-123">With these **Group by** options selected, you get a general overview on a monthly basis of workload and throughput related to maintenance requests and work orders.</span></span> 

![月工作负载示例](media/13-controlling-and-reporting.png)

## <a name="example-2"></a><span data-ttu-id="8ab85-125">示例 2</span><span class="sxs-lookup"><span data-stu-id="8ab85-125">Example 2</span></span>

<span data-ttu-id="8ab85-126">在下面的屏幕截图中，已添加了有关功能位置的信息。</span><span class="sxs-lookup"><span data-stu-id="8ab85-126">In the screenshot below, information about functional locations has been added.</span></span> <span data-ttu-id="8ab85-127">请注意，可以比较多个功能位置（可以是地理位置、工厂或工作区域）的工作负载和吞吐量。</span><span class="sxs-lookup"><span data-stu-id="8ab85-127">Now it is possible to compare workload and throughput across functional locations, which may represent geographical locations, factories, or work areas.</span></span> 

![包含功能位置的月工作负载示例](media/14-controlling-and-reporting.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
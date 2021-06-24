---
title: 指南：手动修改需求预测
description: 本主题介绍了如何修改物料的预测
author: ChristianRytt
ms.date: 08/12/2019
ms.topic: business-process
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e12ccf90b9971379e8931bd48d6243a855bb795
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/10/2021
ms.locfileid: "6224002"
---
# <a name="guide-modify-a-demand-forecast-manually"></a><span data-ttu-id="0f075-103">指南：手动修改需求预测</span><span class="sxs-lookup"><span data-stu-id="0f075-103">Guide: Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0f075-104">此过程显示如何修改物料预测。</span><span class="sxs-lookup"><span data-stu-id="0f075-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="0f075-105">此程序是专为生产规划员设计的。</span><span class="sxs-lookup"><span data-stu-id="0f075-105">This procedure is intended for the production planner.</span></span>

## <a name="modify-the-forecast-for-a-selected-item"></a><span data-ttu-id="0f075-106">修改选定物料的预测</span><span class="sxs-lookup"><span data-stu-id="0f075-106">Modify the forecast for a selected item</span></span>

<span data-ttu-id="0f075-107">若要修改选定物料的预测：</span><span class="sxs-lookup"><span data-stu-id="0f075-107">To modify the forecast for a selected item:</span></span>

1. <span data-ttu-id="0f075-108">转到 **模块 \> 产品信息管理 \> 产品 \> 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="0f075-108">Go to **Modules \> Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="0f075-109">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="0f075-109">In the list, find and select the desired record.</span></span> <span data-ttu-id="0f075-110">选择要更改预测的物料。</span><span class="sxs-lookup"><span data-stu-id="0f075-110">Select the item for which you want to modify the forecast.</span></span>
1. <span data-ttu-id="0f075-111">在操作窗格上，打开 **计划** 选项卡并选择 **需求预测**。</span><span class="sxs-lookup"><span data-stu-id="0f075-111">On the Action Pane, open the **Plan** tab and select **Demand forecast**.</span></span>
1. <span data-ttu-id="0f075-112">在列表中，选择一行。</span><span class="sxs-lookup"><span data-stu-id="0f075-112">In the list, select a row.</span></span> <span data-ttu-id="0f075-113">如果没有预测行，通过在操作窗格上选择 **新建** 来创建新行。</span><span class="sxs-lookup"><span data-stu-id="0f075-113">If there are no forecast lines, create a new line by selecting **New** on the Action Pane.</span></span>  
1. <span data-ttu-id="0f075-114">在 **销售数量** 字段中，输入一个正数。</span><span class="sxs-lookup"><span data-stu-id="0f075-114">In the **Sales quantity** field, enter a positive number.</span></span> <span data-ttu-id="0f075-115">此数字代表该物料的预测数量。</span><span class="sxs-lookup"><span data-stu-id="0f075-115">This number represents the forecasted quantity for the item.</span></span> <span data-ttu-id="0f075-116">如果输入负数，将显示错误。</span><span class="sxs-lookup"><span data-stu-id="0f075-116">An error will be shown if you enter a negative number.</span></span>
1. <span data-ttu-id="0f075-117">根据需要填写其他字段。</span><span class="sxs-lookup"><span data-stu-id="0f075-117">Fill out the other fields as needed.</span></span>
1. <span data-ttu-id="0f075-118">在操作窗格上选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="0f075-118">Select **Save** on the Action Pane.</span></span>

## <a name="modify-the-forecast-for-one-or-more-items-with-microsoft-excel"></a><span data-ttu-id="0f075-119">使用 Microsoft Excel 修改一个或多个物料的预测</span><span class="sxs-lookup"><span data-stu-id="0f075-119">Modify the forecast for one or more items with Microsoft Excel</span></span>

<span data-ttu-id="0f075-120">若要使用 Microsoft Excel 修改一个或多个物料的预测：</span><span class="sxs-lookup"><span data-stu-id="0f075-120">To modify the forecast for one or more items with Microsoft Excel:</span></span>

1. <span data-ttu-id="0f075-121">执行以下选项之一：</span><span class="sxs-lookup"><span data-stu-id="0f075-121">Do one of the following:</span></span>
    - <span data-ttu-id="0f075-122">针对上一部分中所述的任何物料（无论是哪一个）打开 **需求预测** 页面。</span><span class="sxs-lookup"><span data-stu-id="0f075-122">Open the **Demand forecast** page for any item (it doesn't matter which one) as described in the previous section.</span></span>
    - <span data-ttu-id="0f075-123">转到 **主计划 \> 预测 \> 手动预测条目 \> 需求预测行**。</span><span class="sxs-lookup"><span data-stu-id="0f075-123">Go to **Master planning \> Forecasting \> Manual forecast entry \> Demand forecast lines**.</span></span>
1. <span data-ttu-id="0f075-124">在操作窗格上，选择 **在 Microsoft Office 中打开 \> 需求预测条目**。</span><span class="sxs-lookup"><span data-stu-id="0f075-124">On the Action Pane, select **Open in Microsoft Office \> Demand forecast entries**.</span></span>
1. <span data-ttu-id="0f075-125">选择下载位置，保存，然后在 Excel 中打开下载的文件。</span><span class="sxs-lookup"><span data-stu-id="0f075-125">Select a download location, save, and then open the downloaded file in Excel.</span></span>
1. <span data-ttu-id="0f075-126">如果看到警告，请选择 **启用编辑**。</span><span class="sxs-lookup"><span data-stu-id="0f075-126">If you see a warning, choose to **Enable editing**.</span></span>
1. <span data-ttu-id="0f075-127">在 Excel 中，使用 Microsoft Dynamics 任务窗格登录到 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="0f075-127">In Excel, sign in to Supply Chain Management using the Microsoft Dynamics task pane.</span></span> <span data-ttu-id="0f075-128">您必须使用启用的 **我保持登录状态** 选项登录，并且必须信任数据连接应用。</span><span class="sxs-lookup"><span data-stu-id="0f075-128">You must sign in with the **Keep me signed in** option enabled and you must trust the data connection app.</span></span>
1. <span data-ttu-id="0f075-129">Excel 电子表格现在显示您的公司的所有当前需求预测行。</span><span class="sxs-lookup"><span data-stu-id="0f075-129">The Excel spreadsheet now shows all the current demand forecast lines for your company.</span></span>  <span data-ttu-id="0f075-130">根据需要添加、删除和编辑需求预测行。</span><span class="sxs-lookup"><span data-stu-id="0f075-130">Add, delete, and edit demand forecast lines as needed.</span></span>
1. <span data-ttu-id="0f075-131">在 Microsoft Dynamics 任务窗格上选择 **发布** 以将您的更改上传回 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="0f075-131">Select **Publish** on the Microsoft Dynamics task pane to upload your changes back to Supply Chain Management.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

---
title: 手动修改需求预测
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
ms.openlocfilehash: 5da1d5b1fbd91964e695a704681b1c9ee513a2f1
ms.sourcegitcommit: 4016c223a985c46e33f9941bf91ba5e1583e1cfd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889016"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="27323-103">手动修改需求预测</span><span class="sxs-lookup"><span data-stu-id="27323-103">Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="27323-104">此过程显示如何修改物料预测。</span><span class="sxs-lookup"><span data-stu-id="27323-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="27323-105">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="27323-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="27323-106">此程序是专为生产规划员设计的。</span><span class="sxs-lookup"><span data-stu-id="27323-106">This procedure is intended for the production planner.</span></span>

## <a name="modify-the-forecast-for-a-selected-item"></a><span data-ttu-id="27323-107">修改选定物料的预测</span><span class="sxs-lookup"><span data-stu-id="27323-107">Modify the forecast for a selected item</span></span>

<span data-ttu-id="27323-108">若要修改选定物料的预测：</span><span class="sxs-lookup"><span data-stu-id="27323-108">To modify the forecast for a selected item:</span></span>

1. <span data-ttu-id="27323-109">转到 **模块 \> 产品信息管理 \> 产品 \> 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="27323-109">Go to **Modules \> Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="27323-110">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="27323-110">In the list, find and select the desired record.</span></span> <span data-ttu-id="27323-111">选择要更改预测的物料。</span><span class="sxs-lookup"><span data-stu-id="27323-111">Select the item for which you want to modify the forecast.</span></span>
1. <span data-ttu-id="27323-112">在操作窗格上，打开 **计划** 选项卡并选择 **需求预测**。</span><span class="sxs-lookup"><span data-stu-id="27323-112">On the Action Pane, open the **Plan** tab and select **Demand forecast**.</span></span>
1. <span data-ttu-id="27323-113">在列表中，选择一行。</span><span class="sxs-lookup"><span data-stu-id="27323-113">In the list, select a row.</span></span> <span data-ttu-id="27323-114">如果没有预测行，通过在操作窗格上选择 **新建** 来创建新行。</span><span class="sxs-lookup"><span data-stu-id="27323-114">If there are no forecast lines, create a new line by selecting **New** on the Action Pane.</span></span>  
1. <span data-ttu-id="27323-115">在 **销售数量** 字段中，输入一个正数。</span><span class="sxs-lookup"><span data-stu-id="27323-115">In the **Sales quantity** field, enter a positive number.</span></span> <span data-ttu-id="27323-116">此数字代表该物料的预测数量。</span><span class="sxs-lookup"><span data-stu-id="27323-116">This number represents the forecasted quantity for the item.</span></span> <span data-ttu-id="27323-117">如果输入负数，将显示错误。</span><span class="sxs-lookup"><span data-stu-id="27323-117">An error will be shown if you enter a negative number.</span></span>
1. <span data-ttu-id="27323-118">根据需要填写其他字段。</span><span class="sxs-lookup"><span data-stu-id="27323-118">Fill out the other fields as needed.</span></span>
1. <span data-ttu-id="27323-119">在操作窗格上选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="27323-119">Select **Save** on the Action Pane.</span></span>

## <a name="modify-the-forecast-for-one-or-more-items-microsoft-excel"></a><span data-ttu-id="27323-120">修改 Microsoft Excel 中一个或多个物料的预测</span><span class="sxs-lookup"><span data-stu-id="27323-120">Modify the forecast for one or more items Microsoft Excel</span></span>

<span data-ttu-id="27323-121">若要修改 Microsoft Excel 中一个或多个物料的预测：</span><span class="sxs-lookup"><span data-stu-id="27323-121">To modify the forecast for one or more items Microsoft Excel:</span></span>

1. <span data-ttu-id="27323-122">执行以下选项之一：</span><span class="sxs-lookup"><span data-stu-id="27323-122">Do one of the following:</span></span>
    - <span data-ttu-id="27323-123">针对上一部分中所述的任何物料（无论是哪一个）打开 **需求预测** 页面。</span><span class="sxs-lookup"><span data-stu-id="27323-123">Open the **Demand forecast** page for any item (it doesn't matter which one) as described in the previous section.</span></span>
    - <span data-ttu-id="27323-124">转到 **主计划 \> 预测 \> 手动预测条目 \> 需求预测行**。</span><span class="sxs-lookup"><span data-stu-id="27323-124">Go to **Master planning \> Forecasting \> Manual forecast entry \> Demand forecast lines**.</span></span>
1. <span data-ttu-id="27323-125">在操作窗格上，选择 **在 Microsoft Office 中打开 \> 需求预测条目**。</span><span class="sxs-lookup"><span data-stu-id="27323-125">On the Action Pane, select **Open in Microsoft Office \> Demand forecast entries**.</span></span>
1. <span data-ttu-id="27323-126">选择下载位置，保存，然后在 Excel 中打开下载的文件。</span><span class="sxs-lookup"><span data-stu-id="27323-126">Select a download location, save, and then open the downloaded file in Excel.</span></span>
1. <span data-ttu-id="27323-127">如果看到警告，请选择 **启用编辑**。</span><span class="sxs-lookup"><span data-stu-id="27323-127">If you see a warning, choose to **Enable editing**.</span></span>
1. <span data-ttu-id="27323-128">在 Excel 中，使用 Microsoft Dynamics 任务窗格登录到 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="27323-128">In Excel, sign in to Supply Chain Management using the Microsoft Dynamics task pane.</span></span> <span data-ttu-id="27323-129">您必须使用启用的 **我保持登录状态** 选项登录，并且必须信任数据连接应用。</span><span class="sxs-lookup"><span data-stu-id="27323-129">You must sign in with the **Keep me signed in** option enabled and you must trust the data connection app.</span></span>
1. <span data-ttu-id="27323-130">Excel 电子表格现在显示您的公司的所有当前需求预测行。</span><span class="sxs-lookup"><span data-stu-id="27323-130">The Excel spreadsheet now shows all the current demand forecast lines for your company.</span></span>  <span data-ttu-id="27323-131">根据需要添加、删除和编辑需求预测行。</span><span class="sxs-lookup"><span data-stu-id="27323-131">Add, delete, and edit demand forecast lines as needed.</span></span>
1. <span data-ttu-id="27323-132">在 Microsoft Dynamics 任务窗格上选择 **发布** 以将您的更改上传回 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="27323-132">Select **Publish** on the Microsoft Dynamics task pane to upload your changes back to Supply Chain Management.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

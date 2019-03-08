---
title: 转移固定资产
description: 此任务指南将一个固定资产帐簿的财务信息从一个财务维度转移到一个新的财务维度集。
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb8a5b94d9a0bb510daa2a698524e0c380597991
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "357189"
---
# <a name="transfer-a-fixed-asset"></a><span data-ttu-id="9b841-103">转移固定资产</span><span class="sxs-lookup"><span data-stu-id="9b841-103">Transfer a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9b841-104">此任务指南将一个固定资产帐簿的财务信息从一个财务维度转移到一个新的财务维度集。</span><span class="sxs-lookup"><span data-stu-id="9b841-104">This task guide will transfer the financial information for a fixed asset book from one financial dimension set to a new financial dimension set.</span></span>  <span data-ttu-id="9b841-105">它为 USMF 法人实体使用会计角色和演示数据。</span><span class="sxs-lookup"><span data-stu-id="9b841-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="9b841-106">转到“固定资产”>“固定资产”>“固定资产”。</span><span class="sxs-lookup"><span data-stu-id="9b841-106">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="9b841-107">在列表中，查找并选择要转移的固定资产。</span><span class="sxs-lookup"><span data-stu-id="9b841-107">In the list, find and select the fixed asset to transfer.</span></span>
3. <span data-ttu-id="9b841-108">在“操作”窗格上，单击“固定资产”。</span><span class="sxs-lookup"><span data-stu-id="9b841-108">On the Action Pane, click Fixed asset.</span></span>
4. <span data-ttu-id="9b841-109">单击“转移固定资产”。</span><span class="sxs-lookup"><span data-stu-id="9b841-109">Click Transfer fixed assets.</span></span>
5. <span data-ttu-id="9b841-110">在“转移日期”字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="9b841-110">In the Transfer date field, enter a date.</span></span>
6. <span data-ttu-id="9b841-111">输入注释以对转移进行描述。</span><span class="sxs-lookup"><span data-stu-id="9b841-111">Enter comments to describe the transfer.</span></span>
    * <span data-ttu-id="9b841-112">此列表显示固定资产所有帐簿。</span><span class="sxs-lookup"><span data-stu-id="9b841-112">This list shows all books for the fixed asset.</span></span>  
7. <span data-ttu-id="9b841-113">标记要转移到新财务维度集的帐簿。</span><span class="sxs-lookup"><span data-stu-id="9b841-113">Mark the books you want to transfer to a new financial dimension set.</span></span>
    * <span data-ttu-id="9b841-114">此列表显示所选帐簿的现有财务维度值。</span><span class="sxs-lookup"><span data-stu-id="9b841-114">This list shows the existing financial dimension values for the selected book.</span></span>  
    * <span data-ttu-id="9b841-115">选择要为所选固定资产帐簿更新的财务维度。</span><span class="sxs-lookup"><span data-stu-id="9b841-115">Select the financial dimension you want to update for the selected fixed asset book.</span></span>  
8. <span data-ttu-id="9b841-116">在“财务维度”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="9b841-116">In the Financial dimension field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="9b841-117">根据需要设置其他财务维度值。</span><span class="sxs-lookup"><span data-stu-id="9b841-117">Set other financial dimension values as appropriate.</span></span>  
    * <span data-ttu-id="9b841-118">当交易发生时，无论是否输入值，所有财务维度值都会更改。</span><span class="sxs-lookup"><span data-stu-id="9b841-118">All financial dimension values change when a transfer occurs, whether a value has been entered or left blank.</span></span> <span data-ttu-id="9b841-119">例如，如果您为 BusinessUnit 输入了值，而将 CostCenter 和财务维度留为空白。</span><span class="sxs-lookup"><span data-stu-id="9b841-119">For example, if you entered a value for the BusinessUnit and left the CostCenter and Department financial dimensions blank.</span></span> <span data-ttu-id="9b841-120">如果您的科目结构允许将 CostCenter 和部门值留为空白，交易发生后，每个价值模型中的 BusinessUnit 都会有新值，而 CostCenter 和部门则仍为空值。</span><span class="sxs-lookup"><span data-stu-id="9b841-120">If your account structure allows blank values for CostCenter and Department, the transfer would result in each value model having the new value for BusinessUnit and a blank value for CostCenter and Department.</span></span>  
9. <span data-ttu-id="9b841-121">单击“更新”。</span><span class="sxs-lookup"><span data-stu-id="9b841-121">Click Update.</span></span>
    * <span data-ttu-id="9b841-122">您可以在完成交易前预览所做更改。</span><span class="sxs-lookup"><span data-stu-id="9b841-122">You have the opportunity to preview the changes before finalizing the transfer.</span></span>  
    * <span data-ttu-id="9b841-123">在转移固定资产帐簿之前查看结果。</span><span class="sxs-lookup"><span data-stu-id="9b841-123">Review results before transferring the fixed asset books.</span></span>  
10. <span data-ttu-id="9b841-124">单击“转移”。</span><span class="sxs-lookup"><span data-stu-id="9b841-124">Click Transfer.</span></span>


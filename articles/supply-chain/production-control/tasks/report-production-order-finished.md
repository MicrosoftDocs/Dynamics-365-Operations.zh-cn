---
title: 将生产订单报告为已完工入库
description: 该过程显示如何报告生产订单为完工入库。
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmReportFinished, ProdJournalTransProd
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: def39fa86103bc69d1c88dde8d0660945c1de82e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210540"
---
# <a name="report-a-production-order-as-finished"></a><span data-ttu-id="e94da-103">将生产订单报告为已完工入库</span><span class="sxs-lookup"><span data-stu-id="e94da-103">Report a production order as finished</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e94da-104">该过程显示如何报告生产订单为完工入库。</span><span class="sxs-lookup"><span data-stu-id="e94da-104">This procedure shows how to report a production order as finished.</span></span> <span data-ttu-id="e94da-105">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="e94da-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="e94da-106">这是解释生产订单周期的七个过程中的第六个过程。</span><span class="sxs-lookup"><span data-stu-id="e94da-106">This is the sixth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="report-a-production-order-as-finished"></a><span data-ttu-id="e94da-107">将生产订单报告为已完工入库</span><span class="sxs-lookup"><span data-stu-id="e94da-107">Report a production order as finished</span></span>
1. <span data-ttu-id="e94da-108">转到“生产控制”>“生产订单”>“全部生产订单”。</span><span class="sxs-lookup"><span data-stu-id="e94da-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="e94da-109">选择具有“已开始”状态的一个生产订单。</span><span class="sxs-lookup"><span data-stu-id="e94da-109">Select a production order that has the Started status.</span></span>  
2. <span data-ttu-id="e94da-110">在操作窗格上单击“生产订单”。</span><span class="sxs-lookup"><span data-stu-id="e94da-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="e94da-111">单击“完工入库”。</span><span class="sxs-lookup"><span data-stu-id="e94da-111">Click Report as finished.</span></span>
    * <span data-ttu-id="e94da-112">在此页，您可以确认报告为已完工的成品的数量。</span><span class="sxs-lookup"><span data-stu-id="e94da-112">On this page, you can confirm the quantity of the finished product to be reported as finished.</span></span>  
4. <span data-ttu-id="e94da-113">单击“常规”选项卡。</span><span class="sxs-lookup"><span data-stu-id="e94da-113">Click the General tab.</span></span>
5. <span data-ttu-id="e94da-114">设置“良品数量”为“18”。</span><span class="sxs-lookup"><span data-stu-id="e94da-114">Set Good quantity to '18'.</span></span>
6. <span data-ttu-id="e94da-115">设置“残次数量”为“2”。</span><span class="sxs-lookup"><span data-stu-id="e94da-115">Set Error quantity to '2'.</span></span>
7. <span data-ttu-id="e94da-116">在“残次原因”字段中，选择“物料“。</span><span class="sxs-lookup"><span data-stu-id="e94da-116">In the Error cause field, select 'Material'.</span></span>
8. <span data-ttu-id="e94da-117">选择或取消选择“结束作业”复选框。</span><span class="sxs-lookup"><span data-stu-id="e94da-117">Select or clear the End job check box.</span></span>
9. <span data-ttu-id="e94da-118">选择或取消选择“接受残次”复选框。</span><span class="sxs-lookup"><span data-stu-id="e94da-118">Select or clear the Accept error check box.</span></span>
10. <span data-ttu-id="e94da-119">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="e94da-119">Click OK.</span></span>

## <a name="verify-the-report-as-finished-journal"></a><span data-ttu-id="e94da-120">核实完工入库的日记帐</span><span class="sxs-lookup"><span data-stu-id="e94da-120">Verify the Report as finished journal</span></span>
1. <span data-ttu-id="e94da-121">在操作窗格上，单击“查看”。</span><span class="sxs-lookup"><span data-stu-id="e94da-121">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="e94da-122">单击“完工入库”。</span><span class="sxs-lookup"><span data-stu-id="e94da-122">Click Reported as finished.</span></span>
3. <span data-ttu-id="e94da-123">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="e94da-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="e94da-124">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="e94da-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e94da-125">过帐“完工入库日记帐”。</span><span class="sxs-lookup"><span data-stu-id="e94da-125">The Report as finished journal is posted.</span></span> <span data-ttu-id="e94da-126">如果您想要对日记帐作调整，您可以在可进行更改的位置手动创建新日记帐。</span><span class="sxs-lookup"><span data-stu-id="e94da-126">If you want to make adjustments to the journal, you can manually create  a new journal where you can make changes.</span></span>  


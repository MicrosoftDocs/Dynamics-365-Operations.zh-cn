---
title: 建议固定资产购置
description: 本主题介绍如何使用固定资产日记帐中的购置方案购置固定资产。
author: saraschi2
manager: AnnBe
ms.date: 07/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0997af638c141661afb677e2407a90a883168aed
ms.sourcegitcommit: a8201e0b9033c2afc2b1702b0337facaf7ad4b92
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2020
ms.locfileid: "3628877"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="c9841-103">建议固定资产购置</span><span class="sxs-lookup"><span data-stu-id="c9841-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c9841-104">本主题介绍如何使用固定资产日记帐中的购置方案购置固定资产。</span><span class="sxs-lookup"><span data-stu-id="c9841-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="c9841-105">它为 USMF 法人实体使用会计角色和演示数据。</span><span class="sxs-lookup"><span data-stu-id="c9841-105">It uses the accountant role and demo data for the USMF legal entity.</span></span> <span data-ttu-id="c9841-106">要通过固定资产建议日记帐获取固定资产，必须首先创建固定资产记录，然后在资产帐簿中定义购置价格。</span><span class="sxs-lookup"><span data-stu-id="c9841-106">To acquire a fixed asset through a fixed asset proposal journal, you must first create the fixed asset record, and then define the acquisition price in the asset book.</span></span>

1. <span data-ttu-id="c9841-107">在导航窗格中，转到**模块 > 固定资产 > 日记帐条目 > 固定资产日记帐**。</span><span class="sxs-lookup"><span data-stu-id="c9841-107">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="c9841-108">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="c9841-108">Select **New**.</span></span>
3. <span data-ttu-id="c9841-109">在**名称**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="c9841-109">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="c9841-110">在操作窗格中，选择**行**。</span><span class="sxs-lookup"><span data-stu-id="c9841-110">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="c9841-111">选择**方案**。</span><span class="sxs-lookup"><span data-stu-id="c9841-111">Select **Proposals**.</span></span>
6. <span data-ttu-id="c9841-112">选择**购置方案**。</span><span class="sxs-lookup"><span data-stu-id="c9841-112">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="c9841-113">选择**筛选器**。</span><span class="sxs-lookup"><span data-stu-id="c9841-113">Select **Filter**.</span></span> <span data-ttu-id="c9841-114">选择**重置**以清除先前值。</span><span class="sxs-lookup"><span data-stu-id="c9841-114">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="c9841-115">选择**固定资产编号**行。</span><span class="sxs-lookup"><span data-stu-id="c9841-115">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="c9841-116">在**标准**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="c9841-116">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="c9841-117">为您想要以此方案购置的固定资产设置其他条件。</span><span class="sxs-lookup"><span data-stu-id="c9841-117">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="c9841-118">选择**确定**两次退出窗格。</span><span class="sxs-lookup"><span data-stu-id="c9841-118">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="c9841-119">验证已创建的交易记录行。</span><span class="sxs-lookup"><span data-stu-id="c9841-119">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="c9841-120">只有在帐簿中设置了购置日期和购置价格的固定资产才会包含在购置方案中。</span><span class="sxs-lookup"><span data-stu-id="c9841-120">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="c9841-121">在页面上，选择**帐簿**选项卡。</span><span class="sxs-lookup"><span data-stu-id="c9841-121">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="c9841-122">选择**过帐**。</span><span class="sxs-lookup"><span data-stu-id="c9841-122">Select **Post**.</span></span>

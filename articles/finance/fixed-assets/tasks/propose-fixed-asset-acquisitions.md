---
title: 建议固定资产购置
description: 本主题介绍如何使用固定资产日记帐中的购置方案购置固定资产。
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
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
ms.openlocfilehash: e08177aad2db2438c2d5d4ddd294c1056b88167c
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142723"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="74c1d-103">建议固定资产购置</span><span class="sxs-lookup"><span data-stu-id="74c1d-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="74c1d-104">本主题介绍如何使用固定资产日记帐中的购置方案购置固定资产。</span><span class="sxs-lookup"><span data-stu-id="74c1d-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="74c1d-105">它为 USMF 法人实体使用会计角色和演示数据。</span><span class="sxs-lookup"><span data-stu-id="74c1d-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="74c1d-106">在导航窗格中，转到**模块 > 固定资产 > 日记帐条目 > 固定资产日记帐**。</span><span class="sxs-lookup"><span data-stu-id="74c1d-106">In the Navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="74c1d-107">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="74c1d-107">Select **New**.</span></span>
3. <span data-ttu-id="74c1d-108">在**名称**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="74c1d-108">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="74c1d-109">在操作窗格中，选择**行**。</span><span class="sxs-lookup"><span data-stu-id="74c1d-109">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="74c1d-110">选择**方案**。</span><span class="sxs-lookup"><span data-stu-id="74c1d-110">Select **Proposals**.</span></span>
6. <span data-ttu-id="74c1d-111">选择**购置方案**。</span><span class="sxs-lookup"><span data-stu-id="74c1d-111">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="74c1d-112">选择**筛选器**。</span><span class="sxs-lookup"><span data-stu-id="74c1d-112">Select **Filter**.</span></span> <span data-ttu-id="74c1d-113">选择**重置**以清除先前值。</span><span class="sxs-lookup"><span data-stu-id="74c1d-113">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="74c1d-114">选择**固定资产编号**行。</span><span class="sxs-lookup"><span data-stu-id="74c1d-114">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="74c1d-115">在**标准**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="74c1d-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="74c1d-116">为您想要以此方案购置的固定资产设置其他条件。</span><span class="sxs-lookup"><span data-stu-id="74c1d-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="74c1d-117">选择**确定**两次退出窗格。</span><span class="sxs-lookup"><span data-stu-id="74c1d-117">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="74c1d-118">验证已创建的交易记录行。</span><span class="sxs-lookup"><span data-stu-id="74c1d-118">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="74c1d-119">只有在帐簿中设置了购置日期和购置价格的固定资产才会包含在购置方案中。</span><span class="sxs-lookup"><span data-stu-id="74c1d-119">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="74c1d-120">在页面上，选择**帐簿**选项卡。</span><span class="sxs-lookup"><span data-stu-id="74c1d-120">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="74c1d-121">选择**过帐**。</span><span class="sxs-lookup"><span data-stu-id="74c1d-121">Select **Post**.</span></span>


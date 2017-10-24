---
title: "合并科目组和其他合并科目"
description: "此主题提供有关合并科目组和其他合并科目的信息，并说明其在 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中的使用方法。"
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: eb69b8def1d0a4fc296ccf44490af6c70591cb7b
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a><span data-ttu-id="82dbf-103">合并科目组和其他合并科目</span><span class="sxs-lookup"><span data-stu-id="82dbf-103">Consolidation account groups and additional consolidation accounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="82dbf-104">此主题提供有关合并科目组和其他合并科目的信息，并说明其在 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中的使用方法。</span><span class="sxs-lookup"><span data-stu-id="82dbf-104">This topic provides information about consolidation account groups and additional consolidation accounts, and explains how they are used in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

<a name="consolidation-account-groups"></a><span data-ttu-id="82dbf-105">合并帐户组</span><span class="sxs-lookup"><span data-stu-id="82dbf-105">Consolidation account groups</span></span>
----------------------------

<span data-ttu-id="82dbf-106">可通过合并科目组创建要用于合并数据的科目组。</span><span class="sxs-lookup"><span data-stu-id="82dbf-106">Consolidation account groups let you create groups of the accounts that you want to use to consolidate data.</span></span> <span data-ttu-id="82dbf-107">通常，合并科目组表示政府规定的会计科目表，或将科目映射到公司总部定义的组。</span><span class="sxs-lookup"><span data-stu-id="82dbf-107">Most often, a consolidation account group represents a government-mandated chart of accounts or maps accounts to a group that is defined by the company's headquarters.</span></span> <span data-ttu-id="82dbf-108">可以在**合并**模块的**设置**区域中找到合并科目组。</span><span class="sxs-lookup"><span data-stu-id="82dbf-108">You can find consolidation account groups in the **Setup** area of the **Consolidations** module.</span></span> <span data-ttu-id="82dbf-109">添加新组时，请为科目组输入唯一标识和名称。</span><span class="sxs-lookup"><span data-stu-id="82dbf-109">When you add a new group, you enter a unique identifier for the account group and a name.</span></span>

## <a name="additional-consolidation-accounts"></a><span data-ttu-id="82dbf-110">其他合并帐户</span><span class="sxs-lookup"><span data-stu-id="82dbf-110">Additional consolidation accounts</span></span>
<span data-ttu-id="82dbf-111">可通过其他合并科目将现有会计科目表中的科目分配给合并科目组。</span><span class="sxs-lookup"><span data-stu-id="82dbf-111">Additional consolidation accounts let you assign an account from an existing chart of accounts to a consolidation account group.</span></span> <span data-ttu-id="82dbf-112">然后可以指定合并科目值和名称。</span><span class="sxs-lookup"><span data-stu-id="82dbf-112">You can then specify a consolidation account value and name.</span></span> 

<span data-ttu-id="82dbf-113">可以在**合并**模块的**设置**区域中找到其他合并科目。</span><span class="sxs-lookup"><span data-stu-id="82dbf-113">You can find additional consolidation accounts in the **Setup** area of the **Consolidations** module.</span></span> <span data-ttu-id="82dbf-114">在创建新的合并科目时，至少必须指定以下信息：</span><span class="sxs-lookup"><span data-stu-id="82dbf-114">When you create a new consolidation account, you must specify the following information:</span></span>

-   <span data-ttu-id="82dbf-115">**主科目** – 此字段是查询，用于显示基于您在页面中选择的会计科目表的所有主科目。</span><span class="sxs-lookup"><span data-stu-id="82dbf-115">**Main account** – This field is a lookup that shows all the main accounts that are based on the chart of accounts that you selected on the page.</span></span> <span data-ttu-id="82dbf-116">在您选择科目时，将在**主科目名称**字段中自动输入名称。</span><span class="sxs-lookup"><span data-stu-id="82dbf-116">When you select an account, the name is automatically entered in the **Main account name** field.</span></span>
-   <span data-ttu-id="82dbf-117">**合并科目组** – 此字段用于指定要将科目分配给的组。</span><span class="sxs-lookup"><span data-stu-id="82dbf-117">**Consolidation account group** – Use this field to specify the group to assign the account to.</span></span> <span data-ttu-id="82dbf-118">如果以两种不同方式合并，则必须将同一个科目添加到所有四个合并科目组。</span><span class="sxs-lookup"><span data-stu-id="82dbf-118">If you consolidate in two different ways, you must add the same account to all four consolidation account groups.</span></span>
-   <span data-ttu-id="82dbf-119">**合并科目** – 输入合并科目的值。</span><span class="sxs-lookup"><span data-stu-id="82dbf-119">**Consolidation account** – Enter the value of the consolidation account.</span></span> <span data-ttu-id="82dbf-120">此值可以不是会计科目表中的科目。</span><span class="sxs-lookup"><span data-stu-id="82dbf-120">This value doesn't have to be an account from a chart of accounts.</span></span> <span data-ttu-id="82dbf-121">它可以是您需要的任何值。</span><span class="sxs-lookup"><span data-stu-id="82dbf-121">It can be any value that you require.</span></span>
-   <span data-ttu-id="82dbf-122">**合并科目名称** – 输入您希望在查询和报表中显示的科目名称。</span><span class="sxs-lookup"><span data-stu-id="82dbf-122">**Consolidation account name** – Enter the name of account as you want it to appear on inquiries and reports.</span></span>
-   <span data-ttu-id="82dbf-123">**SAT 级别** – 此字段用于向墨西哥税务部门报告帐户对账单。</span><span class="sxs-lookup"><span data-stu-id="82dbf-123">**SAT level** – This field is used to report account statements to the Mexican tax authorities.</span></span> 

<span data-ttu-id="82dbf-124">创建合并科目组和其他合并科目完毕后，可以在“在线合并流程”中选择该组。</span><span class="sxs-lookup"><span data-stu-id="82dbf-124">When you've finished creating your consolidation account groups and additional consolidation accounts, you can select the group in the Consolidate online process.</span></span>


<span data-ttu-id="82dbf-125">有关详细信息，请参阅[创建合并组和其他合并帐户](../general-ledger/tasks/create-consolidation-groups.md)。</span><span class="sxs-lookup"><span data-stu-id="82dbf-125">For more information, see [Create consolidation groups and additional consolidation accounts](../general-ledger/tasks/create-consolidation-groups.md).</span></span> 




---
title: 创建日记帐高级规则
description: 该过程介绍创建日记帐高级规则的步骤。
author: aprilolson
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalControl, CompanyLookup, LedgerJournalPostControl
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cd753d521dc4ad4c1e46bf51d9c1e4aa0ba02721
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832794"
---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="63efb-103">创建日记帐高级规则</span><span class="sxs-lookup"><span data-stu-id="63efb-103">Create advanced rules for journals</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="63efb-104">该过程介绍创建日记帐高级规则的步骤。</span><span class="sxs-lookup"><span data-stu-id="63efb-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="63efb-105">这包括设置日记帐控制和用户过帐限制。</span><span class="sxs-lookup"><span data-stu-id="63efb-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="63efb-106">此过程使用演示数据公司 USMF。</span><span class="sxs-lookup"><span data-stu-id="63efb-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="63efb-107">设置日记帐控制</span><span class="sxs-lookup"><span data-stu-id="63efb-107">Set up journal control</span></span>
1. <span data-ttu-id="63efb-108">在 **导航窗格** 中，转到 **模块 > 总帐 > 日记帐设置 > 日记帐名称**。</span><span class="sxs-lookup"><span data-stu-id="63efb-108">In the **Navigation pane**, go to **Modules > General ledger > Journal setup > Journal names**.</span></span>
2. <span data-ttu-id="63efb-109">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="63efb-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="63efb-110">在 **操作窗格** 中，单击 **日记帐控制**。</span><span class="sxs-lookup"><span data-stu-id="63efb-110">On the **Action pane**, click **Journal control**.</span></span>
4. <span data-ttu-id="63efb-111">在 **哪些科目类型可以过帐** 快速选项卡上，单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="63efb-111">In the **Which account types can be posted** fastTab, click **Add**.</span></span>
5. <span data-ttu-id="63efb-112">在 **公司帐户** 字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="63efb-112">In the **Company accounts** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="63efb-113">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="63efb-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="63efb-114">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="63efb-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="63efb-115">在 **对于此日记帐，哪些段落值是有效的** 快速选项卡上，单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="63efb-115">In the **Which segment values are valid for this journal** fastTab, click **Add**.</span></span>
9. <span data-ttu-id="63efb-116">在 **科目结构** 字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="63efb-116">In the **Account structure** field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="63efb-117">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="63efb-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="63efb-118">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="63efb-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="63efb-119">在 **分部** 字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="63efb-119">In the **Segment** field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="63efb-120">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="63efb-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="63efb-121">在 **起始值** 字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="63efb-121">In the **From value** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="63efb-122">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="63efb-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="63efb-123">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="63efb-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="63efb-124">在 **目标值** 字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="63efb-124">In the **To value** field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="63efb-125">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="63efb-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="63efb-126">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="63efb-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="63efb-127">设置过帐限制</span><span class="sxs-lookup"><span data-stu-id="63efb-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="63efb-128">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="63efb-128">Close the page.</span></span>
2. <span data-ttu-id="63efb-129">单击 **过帐限制**。</span><span class="sxs-lookup"><span data-stu-id="63efb-129">Click **Posting restrictions**.</span></span>
3. <span data-ttu-id="63efb-130">在 **如何设置过帐限制** 字段中，选择“按用户组”。</span><span class="sxs-lookup"><span data-stu-id="63efb-130">In the **How do you want to set up posting restrictions** field, select 'By user group'.</span></span>
4. <span data-ttu-id="63efb-131">在树形图中，单击“您允许该日记帐过帐的组”。</span><span class="sxs-lookup"><span data-stu-id="63efb-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="63efb-132">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="63efb-132">Click **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
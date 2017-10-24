---
title: "在工作流中配置有条件决策"
description: "使用以下过程配置有条件决策的属性。"
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e9d5c8add546cad0446e863f64cac8f9cb603cbb
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="configure-a-conditional-decision-in-a-workflow"></a><span data-ttu-id="cb45b-103">在工作流中配置有条件决策</span><span class="sxs-lookup"><span data-stu-id="cb45b-103">Configure a conditional decision in a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="cb45b-104">使用以下过程配置有条件决策的属性。</span><span class="sxs-lookup"><span data-stu-id="cb45b-104">Use the following procedure to configure the properties of a conditional decision.</span></span>

<span data-ttu-id="cb45b-105">有条件决策是工作流划分为两个分支处的点。</span><span class="sxs-lookup"><span data-stu-id="cb45b-105">A conditional decision is a point at which a workflow divides into two branches.</span></span> <span data-ttu-id="cb45b-106">要配置有条件决策，在工作流编辑器中，右键单击“有条件决策”，然后单击“**属性**”以打开“**属性**”窗体。</span><span class="sxs-lookup"><span data-stu-id="cb45b-106">To configure a conditional decision, in the workflow editor, right-click the conditional decision, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-a-decision"></a><span data-ttu-id="cb45b-107">为决策命名</span><span class="sxs-lookup"><span data-stu-id="cb45b-107">Name a decision</span></span>
<span data-ttu-id="cb45b-108">按照以下步骤为有条件决策输入名称。</span><span class="sxs-lookup"><span data-stu-id="cb45b-108">Follow these steps to enter a name for a conditional decision.</span></span>
1.  <span data-ttu-id="cb45b-109">在左侧窗格中，单击**基本设置**。</span><span class="sxs-lookup"><span data-stu-id="cb45b-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="cb45b-110">在“**名称**”字段中，为有条件决策输入唯一名称。</span><span class="sxs-lookup"><span data-stu-id="cb45b-110">In the **Name** field, enter a unique name for the conditional decision.</span></span>

## <a name="set-conditions"></a><span data-ttu-id="cb45b-111">设置条件</span><span class="sxs-lookup"><span data-stu-id="cb45b-111">Set conditions</span></span>
<span data-ttu-id="cb45b-112">系统确定使用的分支，方法是评估提交的文档以确定其是否符合特定条件。</span><span class="sxs-lookup"><span data-stu-id="cb45b-112">The system determines which branch is used by evaluating the submitted document to determine whether it meets specific conditions.</span></span>
1.  <span data-ttu-id="cb45b-113">在左侧窗格中，单击**基本设置**。</span><span class="sxs-lookup"><span data-stu-id="cb45b-113">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="cb45b-114">单击“**添加条件**”。</span><span class="sxs-lookup"><span data-stu-id="cb45b-114">Click **Add condition**.</span></span>
3.  <span data-ttu-id="cb45b-115">输入条件。</span><span class="sxs-lookup"><span data-stu-id="cb45b-115">Enter a condition.</span></span>
4.  <span data-ttu-id="cb45b-116">如果需要，输入其他条件。</span><span class="sxs-lookup"><span data-stu-id="cb45b-116">Enter additional conditions, if they are required.</span></span>
5.  <span data-ttu-id="cb45b-117">要验证输入的条件是否正确配置，请完成以下步骤：</span><span class="sxs-lookup"><span data-stu-id="cb45b-117">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>
    1.  <span data-ttu-id="cb45b-118">单击“**测试**”以打开“**测试工作流条件**”窗体。</span><span class="sxs-lookup"><span data-stu-id="cb45b-118">Click **Test** to open the **Test workflow condition** form.</span></span>
    2.  <span data-ttu-id="cb45b-119">在该窗体的“**验证条件**”区域中选择某个记录。</span><span class="sxs-lookup"><span data-stu-id="cb45b-119">Select a record in the **Validate condition** area of the form.</span></span>
    3.  <span data-ttu-id="cb45b-120">单击“**测试**”。</span><span class="sxs-lookup"><span data-stu-id="cb45b-120">Click **Test**.</span></span> <span data-ttu-id="cb45b-121">系统对该记录进行评估，判断其是否符合您定义的条件。</span><span class="sxs-lookup"><span data-stu-id="cb45b-121">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4.  <span data-ttu-id="cb45b-122">单击“**确定**”或“**取消**”返回到“**属性**”窗体。</span><span class="sxs-lookup"><span data-stu-id="cb45b-122">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>







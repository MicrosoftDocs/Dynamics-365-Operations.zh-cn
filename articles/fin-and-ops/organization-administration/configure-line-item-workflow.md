---
title: "配置行项工作流"
description: "本主题说明如何配置行项工作流元素。"
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 658829ccb79d0b2b4f627a45647ba6076e4384b0
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---

# <a name="configure-a-line-item-workflow"></a><span data-ttu-id="422fd-103">配置行项工作流</span><span class="sxs-lookup"><span data-stu-id="422fd-103">Configure a line-item workflow</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="422fd-104">本主题说明如何配置行项工作流元素。</span><span class="sxs-lookup"><span data-stu-id="422fd-104">This topic explains how to configure a line-item workflow element.</span></span>

<span data-ttu-id="422fd-105">要配置行项工作流元素，在工作流编辑器中，右键单击该元素，然后单击“**属性**”以打开“**属性**”页。</span><span class="sxs-lookup"><span data-stu-id="422fd-105">To configure a line-item workflow element, in the workflow editor, right-click the element, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="422fd-106">然后使用以下过程配置行项工作流元素的属性。</span><span class="sxs-lookup"><span data-stu-id="422fd-106">Then use the following procedures to configure the properties of the line-item workflow element.</span></span>

## <a name="name-the-line-item-workflow-element"></a><span data-ttu-id="422fd-107">对行项工作流元素命名。</span><span class="sxs-lookup"><span data-stu-id="422fd-107">Name the line-item workflow element</span></span>
<span data-ttu-id="422fd-108">按照以下步骤为行项工作流元素输入一个名称。</span><span class="sxs-lookup"><span data-stu-id="422fd-108">Follow these steps to enter a name for the line-item workflow element.</span></span>

1.  <span data-ttu-id="422fd-109">在左侧窗格中，单击**基本设置**。</span><span class="sxs-lookup"><span data-stu-id="422fd-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="422fd-110">在“**名称**”字段中，为行项工作流元素输入唯一名称。</span><span class="sxs-lookup"><span data-stu-id="422fd-110">In the **Name** field, enter a unique name for the line-item workflow element.</span></span>

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a><span data-ttu-id="422fd-111">指定是否使用相同工作流处理所有行项</span><span class="sxs-lookup"><span data-stu-id="422fd-111">Specify whether the same workflow is used to process all line items</span></span>
<span data-ttu-id="422fd-112">按照以下步骤指定是否使用相同的工作流处理在文档中的所有行项。</span><span class="sxs-lookup"><span data-stu-id="422fd-112">Follow these steps to specify whether the same workflow is used to process all the line items on a document.</span></span>

1.  <span data-ttu-id="422fd-113">在左侧窗格中，单击**基本设置**。</span><span class="sxs-lookup"><span data-stu-id="422fd-113">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="422fd-114">如果相同的工作流处理单据上的所有行项，则单击“**为所有行项调用一个单一工作流**”。</span><span class="sxs-lookup"><span data-stu-id="422fd-114">If the same workflow should process all the line items on a document, click **Invoke a single workflow for all line-items**.</span></span> <span data-ttu-id="422fd-115">然后，选择用于处理行项的工作流。</span><span class="sxs-lookup"><span data-stu-id="422fd-115">Then select the workflow to use to process the line items.</span></span>
3.  <span data-ttu-id="422fd-116">如果特定工作流应处理满足一组特定条件的行项，则单击“**为每个行项调用一个工作流**”。</span><span class="sxs-lookup"><span data-stu-id="422fd-116">If a specific workflow should process line items that meet a specific set of conditions, click **Invoke a workflow for each line-item**.</span></span> <span data-ttu-id="422fd-117">然后按照以下步骤定义一组条件：</span><span class="sxs-lookup"><span data-stu-id="422fd-117">Then follow these steps to define the set of conditions:</span></span>
    1.  <span data-ttu-id="422fd-118">单击“**添加**”。</span><span class="sxs-lookup"><span data-stu-id="422fd-118">Click **Add**.</span></span>
    2.  <span data-ttu-id="422fd-119">选择表中的条件。</span><span class="sxs-lookup"><span data-stu-id="422fd-119">Select the condition in the table.</span></span>
    3.  <span data-ttu-id="422fd-120">在“**条件名称**”选项卡上，输入您定义的一组条件的名称。</span><span class="sxs-lookup"><span data-stu-id="422fd-120">On the **Condition name** tab, enter a name for the set of conditions that you're defining.</span></span>
    4.  <span data-ttu-id="422fd-121">单击“**添加条件**”输入条件。</span><span class="sxs-lookup"><span data-stu-id="422fd-121">Click **Add condition** to enter a condition.</span></span>
    5.  <span data-ttu-id="422fd-122">输入需要的任何其他条件。</span><span class="sxs-lookup"><span data-stu-id="422fd-122">Enter any additional conditions that are required.</span></span>
    6.  <span data-ttu-id="422fd-123">要验证输入的该组条件是否配置正确，请单击“**测试**”。</span><span class="sxs-lookup"><span data-stu-id="422fd-123">To verify that the set of conditions that you entered is configured correctly, click **Test**.</span></span> <span data-ttu-id="422fd-124">在“**测试工作流条件**”页面，在“**验证条件**”区域，选择一条记录，然后单击“**测试**”。</span><span class="sxs-lookup"><span data-stu-id="422fd-124">On the **Test workflow condition** page, in the **Validate condition** area, select a record, and then click **Test**.</span></span> <span data-ttu-id="422fd-125">系统对该记录进行评估，判断其是否符合您定义的条件。</span><span class="sxs-lookup"><span data-stu-id="422fd-125">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span> <span data-ttu-id="422fd-126">单击**确定**或**取消**返回到**属性**页面。</span><span class="sxs-lookup"><span data-stu-id="422fd-126">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

    <span data-ttu-id="422fd-127">在“**工作流**”选项卡，选择处理满足您定义的一组条件的行项时要使用的工作流。</span><span class="sxs-lookup"><span data-stu-id="422fd-127">On the **Workflow** tab, select the workflow select the workflow to use to process line items that meet the set of conditions that you defined.</span></span>






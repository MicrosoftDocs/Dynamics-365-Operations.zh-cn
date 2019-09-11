---
title: 维护安排成本
description: 本主题介绍资产管理中的维护安排成本。
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 71b958839a914d90a86a0dcd16a09285ca6dcfa4
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875515"
---
# <a name="maintenance-schedule-cost"></a><span data-ttu-id="934b0-103">维护安排成本</span><span class="sxs-lookup"><span data-stu-id="934b0-103">Maintenance schedule cost</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="934b0-104">在资产管理中，可计算维护安排行的预算成本。</span><span class="sxs-lookup"><span data-stu-id="934b0-104">In Asset Management, you can calculate budget costs on maintenance schedule lines.</span></span> <span data-ttu-id="934b0-105">如果要获取预计成本（如与为下一年计划的预防性维护作业有关的成本）的概览，这非常有用。</span><span class="sxs-lookup"><span data-stu-id="934b0-105">This is useful if you want to get an overview of expected costs, for example, costs relating to planned preventive maintenance jobs for the next year.</span></span> <span data-ttu-id="934b0-106">此类计算基于类型为“维护计划”和“维护阶段”与“维护请求”的现有维护安排行。</span><span class="sxs-lookup"><span data-stu-id="934b0-106">The calculations are based on existing maintenance schedule lines of type "Maintenance plans" and "Maintenance rounds" and "Maintenance requests".</span></span>

1. <span data-ttu-id="934b0-107">单击**资产管理** > **查询** > **资产** > **维护安排成本**。</span><span class="sxs-lookup"><span data-stu-id="934b0-107">Click **Asset management** > **Inquiries** > **Assets** > **Maintenance schedule cost**.</span></span>

2. <span data-ttu-id="934b0-108">如果要查看按财务维度分组的成本，可在**维护安排成本**对话框中选择**财务维度集**。</span><span class="sxs-lookup"><span data-stu-id="934b0-108">In the **Maintenance schedule cost** dialog, you can select a **Financial dimension set** if you want to see costs grouped in financial dimensions.</span></span>

>[!NOTE]
><span data-ttu-id="934b0-109">财务维度集在**总帐** > **会计科目表** > **维度** > **财务维度集**中设置。</span><span class="sxs-lookup"><span data-stu-id="934b0-109">Financial dimension sets are set up in **General ledger** > **Chart of accounts** > **Dimensions** > **Financial dimension sets**.</span></span>

3. <span data-ttu-id="934b0-110">可使用**级别**字段指示要与功能位置有关的维护安排行的详细程度。</span><span class="sxs-lookup"><span data-stu-id="934b0-110">You can use the **Level** field to indicate how detailed you want the maintenance schedule lines to be regarding functional locations.</span></span> <span data-ttu-id="934b0-111">例如，如果在字段中插入数字“1”，并且采用了多级别功能位置结构，则将在最上级别显示某个功能位置的所有维护安排行，因此，可以从较低级别的功能位置叠加行中的工时。</span><span class="sxs-lookup"><span data-stu-id="934b0-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="934b0-112">如果在**级别**字段中插入数字“0”，将看到详细结果，其中显示其关联的所有功能位置级别的所有维护安排行。</span><span class="sxs-lookup"><span data-stu-id="934b0-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="934b0-113">如果要对特定资产进行计算，请单击**要包括的记录**快速选项卡上的**筛选**，然后选择相关资产。</span><span class="sxs-lookup"><span data-stu-id="934b0-113">If you want to make a calculation for specific assets, click **Filter** on the **Records to include** FastTab, and select the relevant assets.</span></span> <span data-ttu-id="934b0-114">如果需要，也可以为成本计算指定**预计的开始日期**，或为成本计算选择其他**状态**</span><span class="sxs-lookup"><span data-stu-id="934b0-114">If required, you can also specify an **Expected start** date for the cost calculation or select a different **Status** for the cost calculation</span></span>

5. <span data-ttu-id="934b0-115">单击**确定**开始计算成本。</span><span class="sxs-lookup"><span data-stu-id="934b0-115">Click **OK** to start the cost calculation.</span></span>

6. <span data-ttu-id="934b0-116">在**维护安排成本**选项卡上 > **分组依据**操作窗格组中，单击相关按钮显示所需成本计算详细程度。</span><span class="sxs-lookup"><span data-stu-id="934b0-116">On the **Maintenance schedule cost** tab > in the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the cost calculation.</span></span> <span data-ttu-id="934b0-117">将以蓝色突出显示所选操作窗格组按钮。</span><span class="sxs-lookup"><span data-stu-id="934b0-117">The selected action pane group buttons are highlighted in blue color.</span></span> <span data-ttu-id="934b0-118">单击按钮将其激活或停用。</span><span class="sxs-lookup"><span data-stu-id="934b0-118">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="934b0-119">如果要进行新的成本计算，请单击**计算成本**按钮。</span><span class="sxs-lookup"><span data-stu-id="934b0-119">Click the **Calculate cost** button if you want to make a new cost calculation.</span></span>


![图 1](media/17-preventive-maintenance.png)


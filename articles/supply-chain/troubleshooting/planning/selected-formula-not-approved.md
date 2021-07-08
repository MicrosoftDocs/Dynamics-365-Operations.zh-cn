---
title: 未为批次订单审核选择的配方编号
description: 当您尝试确认计划订单时，将收到一条错误消息，指示未为批次订单审核选择的配方编号。
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4f993c92ca0a2f8f79e4b0e0eda43904529163f8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294016"
---
# <a name="selected-formula-number-isnt-approved-for-a-batch-order"></a><span data-ttu-id="6a79a-103">未为批次订单审核选择的配方编号</span><span class="sxs-lookup"><span data-stu-id="6a79a-103">Selected formula number isn't approved for a batch order</span></span>

<span data-ttu-id="6a79a-104">错误代码：PRO2614</span><span class="sxs-lookup"><span data-stu-id="6a79a-104">Error code: PRO2614</span></span>

## <a name="symptoms"></a><span data-ttu-id="6a79a-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="6a79a-105">Symptoms</span></span>

<span data-ttu-id="6a79a-106">当您尝试确认计划订单时，将收到以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="6a79a-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="6a79a-107">未为批次订单审批选择的配方编号。</span><span class="sxs-lookup"><span data-stu-id="6a79a-107">The selected formula number is not approved for a batch order.</span></span>

## <a name="cause"></a><span data-ttu-id="6a79a-108">原因</span><span class="sxs-lookup"><span data-stu-id="6a79a-108">Cause</span></span>

<span data-ttu-id="6a79a-109">系统验证确认操作以确保审核的配方可用于活动物料。</span><span class="sxs-lookup"><span data-stu-id="6a79a-109">The system validates the firming operation to make sure that an approved formula is available for the active item.</span></span> <span data-ttu-id="6a79a-110">您可能必须审核该配方。</span><span class="sxs-lookup"><span data-stu-id="6a79a-110">You must probably approve the formula.</span></span>

## <a name="resolution"></a><span data-ttu-id="6a79a-111">解决方法</span><span class="sxs-lookup"><span data-stu-id="6a79a-111">Resolution</span></span>

<span data-ttu-id="6a79a-112">若要审核配方，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="6a79a-112">To approve a formula, follow these steps.</span></span>

1. <span data-ttu-id="6a79a-113">转到 **产品信息管理 \> 物料清单和配方 \> 配方**。</span><span class="sxs-lookup"><span data-stu-id="6a79a-113">Go to **Product information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="6a79a-114">选择相关配方。</span><span class="sxs-lookup"><span data-stu-id="6a79a-114">Select the relevant formula.</span></span>
1. <span data-ttu-id="6a79a-115">在操作窗格上的 **配方** 选项卡上，在 **维护** 组中，选择 **审核配方**。</span><span class="sxs-lookup"><span data-stu-id="6a79a-115">On the Action Pane, on the **Formula** tab, in the **Maintain** group, select **Approve formula**.</span></span>
1. <span data-ttu-id="6a79a-116">在 **审核物料清单或配方** 对话框中，选择审批者，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="6a79a-116">In the **Approve BOM or formula** dialog box, select an approver, and then select **OK**.</span></span>

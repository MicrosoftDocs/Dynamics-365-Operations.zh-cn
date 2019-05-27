---
title: 服务订单阶段
description: 通过定义服务订单的阶段并将其分配给工作人员，您可以通过服务组织中的不同人员所执行的任务来控制服务订单的流程。
author: ShylaThompson
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAStageTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3b924be95c7e60598879e4d0cfd03193fe888dd7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569697"
---
# <a name="service-order-stages"></a><span data-ttu-id="2f2c5-103">服务订单阶段</span><span class="sxs-lookup"><span data-stu-id="2f2c5-103">Service order stages</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="2f2c5-104">您可以设置服务订单的阶段来定义必须完成的任务、完成的订单以及负责完成它们的工作人员。</span><span class="sxs-lookup"><span data-stu-id="2f2c5-104">You can set up stages for a service order to define the tasks that must be completed, the order in which they are completed, and the workers who are responsible for completing them.</span></span> <span data-ttu-id="2f2c5-105">通过定义服务订单的阶段并将其分配给工作人员，您可以通过服务组织中的不同人员所执行的任务来控制服务订单的流程。</span><span class="sxs-lookup"><span data-stu-id="2f2c5-105">By defining the stages for a service order and assigning them to workers, you can control the flow of a service order through the tasks that various people perform in the service organization.</span></span> <span data-ttu-id="2f2c5-106">阶段序列中必须包含一个初始阶段。</span><span class="sxs-lookup"><span data-stu-id="2f2c5-106">The sequence of stages must include an initial stage.</span></span>

<span data-ttu-id="2f2c5-107">还可以定义每个阶段中所允许的操作。</span><span class="sxs-lookup"><span data-stu-id="2f2c5-107">You can also define the actions that are permitted at each stage.</span></span> <span data-ttu-id="2f2c5-108">例如，如果清除所有阶段（最后阶段除外）的**过帐**复选框，您可以防止过帐尚未经过完整阶段序列处理的任何服务订单。</span><span class="sxs-lookup"><span data-stu-id="2f2c5-108">For example, if you clear the **Post** check box for all stages except the final stage, you prevent any service orders from being posted before the service orders are processed through the complete sequence of stages.</span></span>

## <a name="branching-in-service-order-stages"></a><span data-ttu-id="2f2c5-109">服务订单阶段中的分支</span><span class="sxs-lookup"><span data-stu-id="2f2c5-109">Branching in service order stages</span></span>

<span data-ttu-id="2f2c5-110">在您设置服务阶段时，可以创建多个选项或分支，以便下一个服务阶段从中进行选择。</span><span class="sxs-lookup"><span data-stu-id="2f2c5-110">When you set up a service stage, you can create multiple options, or branches, to select from for the next service stage.</span></span> <span data-ttu-id="2f2c5-111">在完成初始阶段后，您可以从所有创建可用的分支中进行选择。</span><span class="sxs-lookup"><span data-stu-id="2f2c5-111">All the branches that you create are available to select from when the initial stage is completed.</span></span> <span data-ttu-id="2f2c5-112">例如，您设置**计划**作为初始阶段。</span><span class="sxs-lookup"><span data-stu-id="2f2c5-112">For example, you set up **Planning** as an initial stage.</span></span> <span data-ttu-id="2f2c5-113">创建名为**进行中**和**取消**的两个阶段，然后选择**计划**作为它们的父阶段。</span><span class="sxs-lookup"><span data-stu-id="2f2c5-113">You create two stages named **In process** and **Cancel**, and then select **Planning** as the parent for them.</span></span> <span data-ttu-id="2f2c5-114">将**计划**阶段分配到销售订单。</span><span class="sxs-lookup"><span data-stu-id="2f2c5-114">You assign the **Planning** stage to sales order.</span></span> <span data-ttu-id="2f2c5-115">在完成销售订单的计划阶段后，如果销售订单准备工作，您可以选择**进行中**阶段，或者如果取消了销售订单，则可以选择**取消**阶段。</span><span class="sxs-lookup"><span data-stu-id="2f2c5-115">When the planning stage for the sales order is completed, you can select the **In process** stage if the sales order is ready to work on, or you can select the **Cancel** stage if the sales order is canceled.</span></span>

## <a name="see-also"></a><span data-ttu-id="2f2c5-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="2f2c5-116">See also</span></span>

[<span data-ttu-id="2f2c5-117">设置服务订单阶段</span><span class="sxs-lookup"><span data-stu-id="2f2c5-117">Set up service order stages</span></span>](set-up-service-order-stages.md)

[<span data-ttu-id="2f2c5-118">更改服务订单阶段</span><span class="sxs-lookup"><span data-stu-id="2f2c5-118">Change the service order stage</span></span>](change-service-order-stage.md)

  



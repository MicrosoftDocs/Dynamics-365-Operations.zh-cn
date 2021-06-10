---
title: 配置未来的生命事件
description: 您可以在 Dynamics 365 Human Resources 中计划未来的生命事件。
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitFutureLifeEvents, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d52e91e7b050027485b3536f40f6ad80afd90de8
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056724"
---
# <a name="configure-future-life-events"></a><span data-ttu-id="ab6d2-103">配置未来的生命事件</span><span class="sxs-lookup"><span data-stu-id="ab6d2-103">Configure future life events</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ab6d2-104">您可以在 Dynamics 365 Human Resources 中计划未来的生命事件。</span><span class="sxs-lookup"><span data-stu-id="ab6d2-104">You can schedule future life events in Dynamics 365 Human Resources.</span></span>

1. <span data-ttu-id="ab6d2-105">在 **福利管理** 工作区中，在 **设置** 下，选择 **未来生命事件**。</span><span class="sxs-lookup"><span data-stu-id="ab6d2-105">In the **Benefits management** workspace, under **Setup**, select **Future life events**.</span></span>

2. <span data-ttu-id="ab6d2-106">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="ab6d2-106">Select **New**.</span></span>

3. <span data-ttu-id="ab6d2-107">为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="ab6d2-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="ab6d2-108">字段</span><span class="sxs-lookup"><span data-stu-id="ab6d2-108">Field</span></span> | <span data-ttu-id="ab6d2-109">说明</span><span class="sxs-lookup"><span data-stu-id="ab6d2-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="ab6d2-110">生命事件日期</span><span class="sxs-lookup"><span data-stu-id="ab6d2-110">Life event date</span></span> | <span data-ttu-id="ab6d2-111">系统将处理在登记期间直到该日期为止的所有事件。</span><span class="sxs-lookup"><span data-stu-id="ab6d2-111">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="ab6d2-112">已记录生命事件</span><span class="sxs-lookup"><span data-stu-id="ab6d2-112">Life event logged</span></span> | <span data-ttu-id="ab6d2-113">记录生命事件的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="ab6d2-113">Date and time when the life event is logged.</span></span> |
   | <span data-ttu-id="ab6d2-114">日志类型</span><span class="sxs-lookup"><span data-stu-id="ab6d2-114">Log type</span></span> | <span data-ttu-id="ab6d2-115">显示操作是否为以下操作之一：</span><span class="sxs-lookup"><span data-stu-id="ab6d2-115">Shows whether the action is one of the following:</span></span></br></br><span data-ttu-id="ab6d2-116">- **更新** – 对跟踪生命事件的现有记录进行更改</span><span class="sxs-lookup"><span data-stu-id="ab6d2-116">- **Update** – a change to an existing record that is tracking life events</span></span></br></br><span data-ttu-id="ab6d2-117">- **插入** – 创建新的生命事件记录</span><span class="sxs-lookup"><span data-stu-id="ab6d2-117">- **Insert** – the creation of a new life event record</span></span> |
   | <span data-ttu-id="ab6d2-118">生命事件类型 ID</span><span class="sxs-lookup"><span data-stu-id="ab6d2-118">Life event type ID</span></span> | <span data-ttu-id="ab6d2-119">生命事件类型的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="ab6d2-119">The life event type unique identifier.</span></span> |
   | <span data-ttu-id="ab6d2-120">生命事件类型</span><span class="sxs-lookup"><span data-stu-id="ab6d2-120">Life event type</span></span> | <span data-ttu-id="ab6d2-121">促进更新员工福利登记的催化剂。</span><span class="sxs-lookup"><span data-stu-id="ab6d2-121">A catalyst to updating an employee’s benefits enrollment.</span></span> <span data-ttu-id="ab6d2-122">有关更多详细信息，请参阅“生命事件触发器”一节。</span><span class="sxs-lookup"><span data-stu-id="ab6d2-122">For more details, see the Life event triggers section.</span></span> |
   | <span data-ttu-id="ab6d2-123">状态</span><span class="sxs-lookup"><span data-stu-id="ab6d2-123">Status</span></span> | <span data-ttu-id="ab6d2-124">生命事件是否已处理。</span><span class="sxs-lookup"><span data-stu-id="ab6d2-124">Whether the life event has been processed or not.</span></span> |
   | <span data-ttu-id="ab6d2-125">扁平</span><span class="sxs-lookup"><span data-stu-id="ab6d2-125">Line</span></span> | <span data-ttu-id="ab6d2-126">未来生命事件的行号。</span><span class="sxs-lookup"><span data-stu-id="ab6d2-126">The line number of the future life event.</span></span> |

4. <span data-ttu-id="ab6d2-127">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="ab6d2-127">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
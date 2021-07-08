---
title: 计划生产订单必须在确认之前进行计划
description: 当您尝试确认计划订单时，将收到一条错误消息，指示订单必须在确认之前进行计划。
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
ms.openlocfilehash: a360cb3cbd26e1bc1ebb1baf1a6a4d8282c28c5c
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294024"
---
# <a name="planned-production-order-must-be-scheduled-before-it-can-be-firmed"></a><span data-ttu-id="24b11-103">计划生产订单必须在确认之前进行计划</span><span class="sxs-lookup"><span data-stu-id="24b11-103">Planned production order must be scheduled before it can be firmed</span></span>

<span data-ttu-id="24b11-104">错误代码：SYS309802</span><span class="sxs-lookup"><span data-stu-id="24b11-104">Error code: SYS309802</span></span>

## <a name="symptoms"></a><span data-ttu-id="24b11-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="24b11-105">Symptoms</span></span>

<span data-ttu-id="24b11-106">当您尝试确认计划订单时，将收到以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="24b11-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="24b11-107">确认计划生产订单之前，必须对其进行计划。</span><span class="sxs-lookup"><span data-stu-id="24b11-107">The planned production order must be scheduled before it can be firmed.</span></span>

## <a name="cause"></a><span data-ttu-id="24b11-108">原因</span><span class="sxs-lookup"><span data-stu-id="24b11-108">Cause</span></span>

<span data-ttu-id="24b11-109">计划的开始和结束日期不能为空。</span><span class="sxs-lookup"><span data-stu-id="24b11-109">The scheduled start and end dates can't be blank.</span></span>

## <a name="resolution"></a><span data-ttu-id="24b11-110">解决方法</span><span class="sxs-lookup"><span data-stu-id="24b11-110">Resolution</span></span>

<span data-ttu-id="24b11-111">若要为计划订单指定开始和结束日期，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="24b11-111">To specify start and end dates for the planned order, follow these steps.</span></span>

1. <span data-ttu-id="24b11-112">转到 **主计划 \> 主计划 \> 计划订单**。</span><span class="sxs-lookup"><span data-stu-id="24b11-112">Go to **Master planning \> Master planning \> Planned orders**.</span></span>
1. <span data-ttu-id="24b11-113">打开相关计划订单。</span><span class="sxs-lookup"><span data-stu-id="24b11-113">Open the relevant planned order.</span></span>
1. <span data-ttu-id="24b11-114">在 **常规** 快速选项卡上的 **计划** 部分中，在 **开始日期** 和 **结束日期** 字段中指定日期。</span><span class="sxs-lookup"><span data-stu-id="24b11-114">On the **General** FastTab, in the **Scheduled** section, specify dates in the **Start date** and **End date** fields.</span></span>

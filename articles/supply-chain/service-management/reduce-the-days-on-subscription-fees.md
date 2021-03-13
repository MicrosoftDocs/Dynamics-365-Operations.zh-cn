---
title: 缩减预订费用天数
description: 若要缩减现有预订费用的天数，可以创建一个新的交易记录，从中您删除不应继续作为预订费用间隔的一部分的时段。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae2486d08e89c06d76ab9945ccce25c5e97f1500
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010549"
---
# <a name="reduce-the-days-on-subscription-fees"></a><span data-ttu-id="450aa-103">缩减预订费用天数</span><span class="sxs-lookup"><span data-stu-id="450aa-103">Reduce the days on subscription fees</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="450aa-104">若要缩减现有预订费用的天数，可以创建一个新的交易记录，从中您删除不应继续作为预订费用间隔的一部分的时段。</span><span class="sxs-lookup"><span data-stu-id="450aa-104">To reduce the number of days of an existing subscription fee, you can create a new transaction in which you remove the period of time that should no longer be part of the subscription fee interval.</span></span>

## <a name="reduce-the-days-on-a-subscription-fee"></a><span data-ttu-id="450aa-105">缩减预订费用天数</span><span class="sxs-lookup"><span data-stu-id="450aa-105">Reduce the days on a subscription fee</span></span>

1.  <span data-ttu-id="450aa-106">单击 **服务管理** \> **常用** \> **服务预订** \> **所有服务预订**。</span><span class="sxs-lookup"><span data-stu-id="450aa-106">Click **Service management** \> **Common** \> **Service subscriptions** \> **All service subscriptions**.</span></span> <span data-ttu-id="450aa-107">选择服务预定，并在“操作窗格”中单击 **预订费用**。</span><span class="sxs-lookup"><span data-stu-id="450aa-107">Select the service subscription, and on the Action Pane, click **Subscription fees**</span></span>

2.  <span data-ttu-id="450aa-108">在 **预订类型** 字段中，选择 **缩减天数**。</span><span class="sxs-lookup"><span data-stu-id="450aa-108">In the **Subscription type** field, select **Reduction days**.</span></span>

3.  <span data-ttu-id="450aa-109">用 **开始日期** 和 **结束日期** 字段来定义要从预订费用期间删除的预订费用的日期间隔，然后单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="450aa-109">Use the **From date** field and the **To date** fields to define the date interval of the subscription fee that you want to remove from the subscription fee period, and then click **OK**.</span></span>

<span data-ttu-id="450aa-110">若要查看已创建的交易记录，请在 **预订** 窗体中，单击 **费用交易记录**。</span><span class="sxs-lookup"><span data-stu-id="450aa-110">To view the transaction that was created, in the **Subscription** form, click **Fee transactions**.</span></span>

## <a name="example"></a><span data-ttu-id="450aa-111">示例</span><span class="sxs-lookup"><span data-stu-id="450aa-111">Example</span></span>

<span data-ttu-id="450aa-112">如果某一预订交易记录期间是从 1 月 1 日到 1 月 31 日，并且您想要将该期间缩减 10 天，则创建一个缩减期间是从 1 月 1 日到 1 月 10 日的新交易记录。</span><span class="sxs-lookup"><span data-stu-id="450aa-112">If a subscription transaction period runs from January 1 to January 31, and you want to reduce the period by 10 days, create a new transaction in which the reduction period is January 1 to January 10.</span></span> <span data-ttu-id="450aa-113">（该缩减期间还可以是从 1 月 5 日到 1 月 15 日或其他任何为期十天的期间）。</span><span class="sxs-lookup"><span data-stu-id="450aa-113">(The reduction period could also be January 5 to January 15, or any other ten day period).</span></span>

<span data-ttu-id="450aa-114">此外，如果该缩减期间的 **开始日期** 是 1 月 21 日（31 减 10），则您可以将 **结束日期** 设置为 1 月 31 日之后的任何日期，并且 10 天仍将从费用交易记录期间中删除。</span><span class="sxs-lookup"><span data-stu-id="450aa-114">Also, if the **From date** on the reduction period is January 21 (31 minus 10), you could set the **To date** to any date after January 31, and 10 days will still be removed from the fee transaction period.</span></span>

## <a name="see-also"></a><span data-ttu-id="450aa-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="450aa-115">See also</span></span>

[<span data-ttu-id="450aa-116">缩减天数示例</span><span class="sxs-lookup"><span data-stu-id="450aa-116">Reduction days example</span></span>](reduction-days-example.md)

  



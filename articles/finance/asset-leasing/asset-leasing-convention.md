---
title: 资产租赁惯例
description: 文主题介绍租赁资产的惯例。
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 67c4d2b7162cf6bda2eedfecef43ff0b216e6e6c
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881800"
---
# <a name="asset-leasing-conventions"></a><span data-ttu-id="95e23-103">资产租赁惯例</span><span class="sxs-lookup"><span data-stu-id="95e23-103">Asset leasing conventions</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="95e23-104">文主题介绍租赁资产的惯例。</span><span class="sxs-lookup"><span data-stu-id="95e23-104">This topic describes conventions for leased assets.</span></span> <span data-ttu-id="95e23-105">租赁惯例用于确定租赁帐簿的开始日期。</span><span class="sxs-lookup"><span data-stu-id="95e23-105">Leasing conventions are used to determine the commencement date of a lease book.</span></span> <span data-ttu-id="95e23-106">如果租赁惯例设置为 **否**，开始日期与租赁的开始日期相同（即 **租赁开始日期** 字段的值）。</span><span class="sxs-lookup"><span data-stu-id="95e23-106">If the leasing convention is set to **None**, the commencement date is the same as the start date for the lease (that is, the value of the **Lease start date** field).</span></span> <span data-ttu-id="95e23-107">如果租赁惯例设置为 **整月**，开始日期则是租赁开始日期所在月份的第一天。</span><span class="sxs-lookup"><span data-stu-id="95e23-107">If the leasing convention is set to **Full month**, the commencement date is the first day of the month that the lease's start date falls in.</span></span>

<span data-ttu-id="95e23-108">开始日期确定负债摊销和资产折旧计划的期间的开始日期。</span><span class="sxs-lookup"><span data-stu-id="95e23-108">The commencement date determines the start date of the period for the liability amortization and asset depreciation schedules.</span></span> <span data-ttu-id="95e23-109">利息支出和折旧支出在相应计划的期间结束日期过帐。</span><span class="sxs-lookup"><span data-stu-id="95e23-109">Interest expenses and depreciation expenses are posted on the period end date of the corresponding schedules.</span></span> <span data-ttu-id="95e23-110">初始确认和调整日记帐条目在开始日期过帐。</span><span class="sxs-lookup"><span data-stu-id="95e23-110">The initial recognition and adjustment journal entry are posted on the commencement date.</span></span>

> [!NOTE]
> <span data-ttu-id="95e23-111">租赁惯例功能必须通过“功能管理”打开。</span><span class="sxs-lookup"><span data-stu-id="95e23-111">The feature for leasing conventions must be turned on through Feature Management.</span></span> <span data-ttu-id="95e23-112">在 **功能管理** 工作区中，找到并选择名为 **资产租赁的租赁惯例** 功能，然后选择 **立即启用**。</span><span class="sxs-lookup"><span data-stu-id="95e23-112">In the **Feature management** workspace, find and select the feature that is named **Leasing convention for asset leasing** feature, and then select **Enable now**.</span></span>

<span data-ttu-id="95e23-113">租赁惯例将被分配到租赁资产帐簿的设置。</span><span class="sxs-lookup"><span data-stu-id="95e23-113">Leasing conventions are assigned to the setup for a lease asset book.</span></span>

<span data-ttu-id="95e23-114">要查看或分配租赁惯例，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="95e23-114">To view or assign the leasing convention, follow these steps.</span></span>

1. <span data-ttu-id="95e23-115">转到 **资产租赁 \> 设置 \> 租赁帐簿**。</span><span class="sxs-lookup"><span data-stu-id="95e23-115">Go to **Asset leasing \> Setup \> Lease books**.</span></span>
2. <span data-ttu-id="95e23-116">在 **租赁惯例** 字段中，选择以下值之一。</span><span class="sxs-lookup"><span data-stu-id="95e23-116">In the **Leasing convention** field, select one of the following values.</span></span>

    | <span data-ttu-id="95e23-117">租赁惯例</span><span class="sxs-lookup"><span data-stu-id="95e23-117">Leasing convention</span></span> | <span data-ttu-id="95e23-118">说明</span><span class="sxs-lookup"><span data-stu-id="95e23-118">Description</span></span> |
    |--------------------|-------------|
    | <span data-ttu-id="95e23-119">None</span><span class="sxs-lookup"><span data-stu-id="95e23-119">None</span></span>               | <span data-ttu-id="95e23-120">负债摊销和资产折旧计划从租赁的开始日期开始，因为开始日期等于租赁的开始日期。</span><span class="sxs-lookup"><span data-stu-id="95e23-120">The liability amortization and asset depreciation schedules start on the lease's start date, because the commencement date equals the lease's start date.</span></span> <span data-ttu-id="95e23-121">结束日期是一个月后。</span><span class="sxs-lookup"><span data-stu-id="95e23-121">The end date is one month later.</span></span> <span data-ttu-id="95e23-122">此租赁惯例不保证利息会在每个月的最后一天过帐。</span><span class="sxs-lookup"><span data-stu-id="95e23-122">This leasing convention doesn't guarantee that the interest will be posted on the last day of each month.</span></span> |
    | <span data-ttu-id="95e23-123">全月</span><span class="sxs-lookup"><span data-stu-id="95e23-123">Full month</span></span>         | <span data-ttu-id="95e23-124">对于开始日期在当月任何时间发生的租赁，负债摊销和资产折旧计划在该月的第一天开始计入费用。</span><span class="sxs-lookup"><span data-stu-id="95e23-124">For leases that have a start date that occurs at any time during the month, the liability amortization and asset depreciation schedules start to accrue expenses on the first day of that month.</span></span> <span data-ttu-id="95e23-125">此租赁惯例可确保在每个整月的最后一天计算利息。</span><span class="sxs-lookup"><span data-stu-id="95e23-125">This leasing convention ensures that interest is accrued on the last day of each month for the whole month.</span></span> |

3. <span data-ttu-id="95e23-126">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="95e23-126">Select **Save**.</span></span>

<span data-ttu-id="95e23-127">租赁创建后，将根据为租赁输入的开始日期和为帐簿指定的租赁惯例自动输入每个帐簿的开始日期。</span><span class="sxs-lookup"><span data-stu-id="95e23-127">When a lease is created, the commencement date of each book is automatically entered based on the start date that is entered for the lease and the leasing convention that is specified for the book.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

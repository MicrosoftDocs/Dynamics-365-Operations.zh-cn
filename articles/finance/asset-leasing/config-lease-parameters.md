---
title: 配置租赁参数（预览）
description: 本主题描述资产租赁的配置设置，例如安全信息和记帐设置。
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 77caf751f9baf4abef534bac97e226484df7acf7
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881268"
---
# <a name="configure-lease-parameters"></a><span data-ttu-id="4b84c-103">配置租赁参数</span><span class="sxs-lookup"><span data-stu-id="4b84c-103">Configure lease parameters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4b84c-104">几个配置设置会影响资产租赁的行为。</span><span class="sxs-lookup"><span data-stu-id="4b84c-104">Several configuration settings affect how Asset leasing behaves.</span></span> <span data-ttu-id="4b84c-105">这些设置包括日记帐名称、常规参数和过帐模板设置。</span><span class="sxs-lookup"><span data-stu-id="4b84c-105">These settings include journal names, general parameters, and posting profile settings.</span></span>

1. <span data-ttu-id="4b84c-106">转到 **资产租赁 \> 设置 \> 资产租赁参数**。</span><span class="sxs-lookup"><span data-stu-id="4b84c-106">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="4b84c-107">在 **选择** 选项卡中，选择 **常规** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="4b84c-107">On the **Leases** tab, select the **General** FastTab.</span></span>

    <span data-ttu-id="4b84c-108">**允许手动覆盖分类** 参数决定在确认付款计划之前是否可以覆盖租赁分类。</span><span class="sxs-lookup"><span data-stu-id="4b84c-108">The **Allow manual classification override** parameter determines whether the lease classification can be overridden before the payment schedule is confirmed.</span></span>

    <span data-ttu-id="4b84c-109">**跨实体批处理** 参数确定您是否可以从当前法人过帐到其他法人。</span><span class="sxs-lookup"><span data-stu-id="4b84c-109">The **Cross-entity batch** parameter determines whether you can post to other legal entities from the current legal entity.</span></span> <span data-ttu-id="4b84c-110">如果已开启此参数，则可以为您有权访问的法人体创建日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="4b84c-110">If this parameter is turned on, you can create journal entries for the legal entities that you have access to.</span></span>

3. <span data-ttu-id="4b84c-111">将 **允许删除已确认的租赁** 选项设置为 **是** 以允许删除已确认付款计划的租赁。</span><span class="sxs-lookup"><span data-stu-id="4b84c-111">Set the **Allow delete of confirmed leases** option to **Yes** to allow leases that have confirmed payment schedules to be deleted.</span></span> <span data-ttu-id="4b84c-112">不能删除与已过帐或未过帐交易关联的租赁，无论此选项的设置如何。</span><span class="sxs-lookup"><span data-stu-id="4b84c-112">Leases can't be deleted if posted or unposted transactions are associated with them, regardless of the setting of this option.</span></span> <span data-ttu-id="4b84c-113">删除租赁记录后，不能恢复。</span><span class="sxs-lookup"><span data-stu-id="4b84c-113">You can't restore a lease record after it's deleted.</span></span> <span data-ttu-id="4b84c-114">如果您手动或通过数据实体上载了已删除租赁的任何记录，则上载的信息将被视为新信息，而不是对现有租赁的更新。</span><span class="sxs-lookup"><span data-stu-id="4b84c-114">If you upload any records for a deleted lease, either manually or through data entities, the uploaded information is treated as new, not as an update to an existing lease.</span></span>

    <span data-ttu-id="4b84c-115">如果将此选项设置为 **是**，而帐簿的转换类型为 **累积采纳选项 A 或 B**，系统将把 **增量借贷利率** 字段的值设置为 **帐簿设置** 页上的 **转换期增量借贷利率** 字段的值。</span><span class="sxs-lookup"><span data-stu-id="4b84c-115">If you set this option to **Yes**, and the transition type of the book is **Cumulative Catchup Option A or B**, the system sets the **Incremental borrowing rate** field to the value of the **Incremental borrowing rate at transition** field on the **Book setup** page.</span></span> <span data-ttu-id="4b84c-116">如果此选项设置为 **否**，则将总租赁费率设置为 **帐簿详细信息** 页上的 **增量借贷利率** 字段的值，而不论帐簿的转换类型为何。</span><span class="sxs-lookup"><span data-stu-id="4b84c-116">If this option is set to **No**, the rate on the head lease is set to the value of the **Incremental borrowing rate** field on the **Book details** page, regardless of the transition type of the book.</span></span>

4. <span data-ttu-id="4b84c-117">将 **允许对已结帐簿版本进行折旧冲销** 选项设置为 **是**，以允许冲销折旧费用交易。</span><span class="sxs-lookup"><span data-stu-id="4b84c-117">Set the **Allow depreciation reversals on closed book version** option to **Yes** to allow depreciation expense transactions to be reversed.</span></span> <span data-ttu-id="4b84c-118">即使帐簿版本已结，也可以冲销费用交易。</span><span class="sxs-lookup"><span data-stu-id="4b84c-118">Expense transactions can be reversed even when the book version is closed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4b84c-119">我们建议您将此选项保持设置为 **否**。</span><span class="sxs-lookup"><span data-stu-id="4b84c-119">We recommend that you keep this option set to **No**.</span></span> <span data-ttu-id="4b84c-120">此选项的设置用作验证和控制，以防止已结帐簿版本意外折旧。</span><span class="sxs-lookup"><span data-stu-id="4b84c-120">The setting of this option is used as a validation and control to prevent a closed book version from being accidently depreciated.</span></span> <span data-ttu-id="4b84c-121">通过将选项设置为 **否**，您可以帮助保持帐面净值和未来折旧计算的准确性。</span><span class="sxs-lookup"><span data-stu-id="4b84c-121">By keeping the option set to **No**, you help keep the net book value and future depreciation calculations accurate.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

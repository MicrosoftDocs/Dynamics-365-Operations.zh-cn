---
title: 现金管理改进
description: 本主题介绍适用于 Dynamics 365 Commerce 的 POS 中的现金管理改进。
author: anpurush
manager: AnnBe
ms.date: 05/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-21
ms.dyn365.ops.version: ''
ms.openlocfilehash: 86cdd70919926243bbf2cb5cc2f26690accdac80
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993670"
---
# <a name="cash-management-improvements"></a><span data-ttu-id="0ab4b-103">现金管理改进</span><span class="sxs-lookup"><span data-stu-id="0ab4b-103">Cash management improvements</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="0ab4b-104">现金管理是一个面向实体商店零售商的关键功能。</span><span class="sxs-lookup"><span data-stu-id="0ab4b-104">Cash management is a key function for retailers in physical stores.</span></span> <span data-ttu-id="0ab4b-105">零售商希望为自己的商店安装系统来对现金及其在商店中不同收银机和出纳之间的变动进行完全跟踪和会计问责。</span><span class="sxs-lookup"><span data-stu-id="0ab4b-105">Retailers want their stores to have systems that can help them provide complete traceability and accountability of cash and its movement across the different registers and cashiers in a store.</span></span> <span data-ttu-id="0ab4b-106">必须可以对帐任何差额和确定会计责任。</span><span class="sxs-lookup"><span data-stu-id="0ab4b-106">They must be able to reconcile any differences and determine accountability.</span></span>


<span data-ttu-id="0ab4b-107">Microsoft Dynamics 365 Commerce 的销售点 (POS) 应用程序中包含现金管理功能。</span><span class="sxs-lookup"><span data-stu-id="0ab4b-107">Microsoft Dynamics 365 Commerce has cash management capabilities in its point of sale (POS) application.</span></span> <span data-ttu-id="0ab4b-108">但是，在低于 10.0.3 的 Retail 版本中，现金管理功能不够强大，无法完全跟踪商店中的现金变动。</span><span class="sxs-lookup"><span data-stu-id="0ab4b-108">However, in versions of Retail that are earlier than version 10.0.3, cash management functionality isn't robust enough to provide complete traceability of cash movements in stores.</span></span> <span data-ttu-id="0ab4b-109">尽管零售商可以对帐商店的现金，如果存在现金差异，就不能准确判断会计责任。</span><span class="sxs-lookup"><span data-stu-id="0ab4b-109">Although retailers can reconcile the cash for a store, they can't precisely determine accountability in the event of a cash discrepancy.</span></span>


<span data-ttu-id="0ab4b-110">在 Retail 版本 10.0.3 及更高版本中，零售商可以跟踪对现金的处理。</span><span class="sxs-lookup"><span data-stu-id="0ab4b-110">In Retail version 10.0.3 and later, retailers will gain traceability for cash handling.</span></span> <span data-ttu-id="0ab4b-111">进行此项跟踪期间，零售商可以定义金库，开展双方现金交易记录，以及对帐现金管理交易记录。</span><span class="sxs-lookup"><span data-stu-id="0ab4b-111">As part of this traceability, retailers will be able to define safes, make two-sided cash transactions, and reconcile cash management transactions.</span></span>

## <a name="set-up-traceability-and-define-safes"></a><span data-ttu-id="0ab4b-112">设置可跟踪性和定义金库</span><span class="sxs-lookup"><span data-stu-id="0ab4b-112">Set up traceability and define safes</span></span>

<span data-ttu-id="0ab4b-113">若要设置新的现金管理功能，请执行下列步骤为商店配置功能配置文件。</span><span class="sxs-lookup"><span data-stu-id="0ab4b-113">To set up the new cash management functionality, follow these steps to configure the functionality profile for stores.</span></span>

1. <span data-ttu-id="0ab4b-114">转到 **Retail 和 Commerce \> 渠道设置 \> POS 设置 \> POS 配置文件 \> 功能配置文件**，然后选择与您要改进以实现现金管理功能的商店关联的功能配置文件。</span><span class="sxs-lookup"><span data-stu-id="0ab4b-114">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Functionality profiles**, and select a functionality profile that is linked to the stores where you want to make the improvements for cash management available.</span></span>
2. <span data-ttu-id="0ab4b-115">在功能配置文件的 **功能** 快速选项卡上的 **高级现金管理** 下，将 **启用现金跟踪** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="0ab4b-115">On the **Functions** FastTab of the functionality profile, under **Advanced cash management**, set the **Enable cash traceability** option to **Yes**.</span></span>
3. <span data-ttu-id="0ab4b-116">若要设置金库，请转至 **Retail 和 Commerce \> 渠道 \> 商店 \> 所有商店**，然后选择商店。</span><span class="sxs-lookup"><span data-stu-id="0ab4b-116">To set up safes, go to **Retail and Commerce \> Channels \> Stores \> All stores**, and select a store.</span></span>
4. <span data-ttu-id="0ab4b-117">在 **商店** 页操作窗格中 **设置** 选项卡的 **设置** 组中，选择 **金库**。</span><span class="sxs-lookup"><span data-stu-id="0ab4b-117">On the **Stores** page, on the Action Pane, on the **Set up** tab, in the **Set up** group, select **Safes**.</span></span> <span data-ttu-id="0ab4b-118">可使用此选项为商店定义和维护多个金库。</span><span class="sxs-lookup"><span data-stu-id="0ab4b-118">By using this option, you can define and maintain multiple safes for a store.</span></span>
4. <span data-ttu-id="0ab4b-119">必须先运行 **1070 渠道配置** 配送计划作业以将这些配置同步到渠道数据库，才能使用此功能。</span><span class="sxs-lookup"><span data-stu-id="0ab4b-119">Before the functionality can be used, you must run the **1070 Channel configuration** distribution schedule job to sync these configurations to the channel database.</span></span>

## <a name="additional-cash-management-changes"></a><span data-ttu-id="0ab4b-120">其他现金管理更改</span><span class="sxs-lookup"><span data-stu-id="0ab4b-120">Additional cash management changes</span></span>

<span data-ttu-id="0ab4b-121">在 Retail 版本 10.0.3 及更高版本中，还提供了下列与现金交易记录有关的功能：</span><span class="sxs-lookup"><span data-stu-id="0ab4b-121">In Retail version 10.0.3 and later, the following capabilities that are related to cash transactions are also provided:</span></span>

- <span data-ttu-id="0ab4b-122">用户在收到“声明初始金额”提示时必须输入现金来源。</span><span class="sxs-lookup"><span data-stu-id="0ab4b-122">A user who is prompted to "declare start amount" must enter the source of cash.</span></span> <span data-ttu-id="0ab4b-123">用户可以搜索商店中定义的可用金库，并选择正在取出现金的金库，以便将其放到收银机中。</span><span class="sxs-lookup"><span data-stu-id="0ab4b-123">The user can search for the available safes that are defined in the store and select the safe that the cash is being taken out of so that it can be put into the register.</span></span>
- <span data-ttu-id="0ab4b-124">将提示执行“取钱”操作的用户在未结“浮动条目”交易记录列表中选择此操作针对的交易记录。</span><span class="sxs-lookup"><span data-stu-id="0ab4b-124">A user who does a "tender removal" operation is prompted to select, in a list of open "float entry" transactions, the transaction that the operation is being done against.</span></span> <span data-ttu-id="0ab4b-125">如果系统中不存在相应浮动条目，用户可以创建无链接的取钱交易记录。</span><span class="sxs-lookup"><span data-stu-id="0ab4b-125">If the corresponding float entry doesn't exist in the system, the user can create a non-linked tender removal transaction.</span></span>
- <span data-ttu-id="0ab4b-126">“浮点条目”操作将提示用户在未结“取钱”交易记录列表中选择浮动条目此操作针对的交易记录。</span><span class="sxs-lookup"><span data-stu-id="0ab4b-126">A "float entry" operation prompts a user to select, in a list of open "tender removal" transactions, the transaction that the float entry operation is being done against.</span></span> <span data-ttu-id="0ab4b-127">如果系统中不存在相应取钱，用户可以创建无链接的浮动条目交易记录。</span><span class="sxs-lookup"><span data-stu-id="0ab4b-127">If the corresponding tender removal doesn't exist in the system, the user can create a non-linked float entry transaction.</span></span>
- <span data-ttu-id="0ab4b-128">将提示进行“金库投箱”的用户选择现金投入的金库。</span><span class="sxs-lookup"><span data-stu-id="0ab4b-128">A user who makes a "safe drop" is prompted to select the safe where the cash is being dropped.</span></span>
- <span data-ttu-id="0ab4b-129">对于商店中定义的金库，用户可以管理清点起始金额、执行浮动条目、取钱和进行银行投箱之类操作。</span><span class="sxs-lookup"><span data-stu-id="0ab4b-129">For safes that are defined in a store, users can manage operations such as declaring the start amount, doing a float entry, doing a tender removal, and making a bank drop.</span></span>
- <span data-ttu-id="0ab4b-130">对于拥有相应用户权限的用户，“管理班次”操作将显示活动、已暂停和直接结束的班次的现金余额。</span><span class="sxs-lookup"><span data-stu-id="0ab4b-130">For users who have the appropriate user privileges, "manage shifts" operations show the cash balances of active, suspended, and blind closed shifts.</span></span>
- <span data-ttu-id="0ab4b-131">若要为一个班次或多个班次的现金交易记录对帐，请选择要对帐的班次，然后选择 **对帐**。</span><span class="sxs-lookup"><span data-stu-id="0ab4b-131">To reconcile the cash transactions within a shift or across shifts, select the shift to reconcile, and then select **Reconcile**.</span></span> <span data-ttu-id="0ab4b-132">打开的视图中将通过单独的选项卡显示已对帐交易记录和未对帐交易记录的列表。</span><span class="sxs-lookup"><span data-stu-id="0ab4b-132">The view that is opened shows the list of reconciled and unreconciled transactions on separate tabs.</span></span> <span data-ttu-id="0ab4b-133">用户可在此视图中选择未对帐的交易记录并为其对帐，或选择以前对帐过的交易记录并取消对帐。</span><span class="sxs-lookup"><span data-stu-id="0ab4b-133">From this view, users can either select unreconciled transactions and reconcile them, or select previously reconciled transactions and unreconcile them.</span></span>
- <span data-ttu-id="0ab4b-134">对帐期间，如果所选交易记录不平衡，用户必须输入不平衡对帐的原因说明。</span><span class="sxs-lookup"><span data-stu-id="0ab4b-134">During reconciliation, if the selected transaction doesn't balance, the user must enter a description of the reason for the unbalanced reconciliation.</span></span> <span data-ttu-id="0ab4b-135">用户可以选择一个交易记录并为其对帐，同时添加所需的相关原因说明。</span><span class="sxs-lookup"><span data-stu-id="0ab4b-135">Users can select a single transaction and reconcile it with the relevant reason description as they require.</span></span>
- <span data-ttu-id="0ab4b-136">用户继续为交易记录继续对帐和取消对帐，直到班次结束。</span><span class="sxs-lookup"><span data-stu-id="0ab4b-136">Users can continue to reconcile and unreconcile transactions until the shift is closed.</span></span> <span data-ttu-id="0ab4b-137">班次结束后，不能对交易记录进行取消对帐。</span><span class="sxs-lookup"><span data-stu-id="0ab4b-137">After a shift is closed, the transactions can't be unreconciled.</span></span>
- <span data-ttu-id="0ab4b-138">当用户选择结束班次时，Commerce 将验证班次中是否没有未对帐的现金管理交易记录。</span><span class="sxs-lookup"><span data-stu-id="0ab4b-138">When a user chooses to close a shift, Commerce validates that there are no unreconciled cash management transactions in the shift.</span></span> <span data-ttu-id="0ab4b-139">如果有未对帐的交易记录，用户就不能结束班次。</span><span class="sxs-lookup"><span data-stu-id="0ab4b-139">Users can't close a shift if there are unreconciled transactions.</span></span>

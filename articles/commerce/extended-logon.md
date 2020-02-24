---
title: 设置 MPOS 和 Cloud POS 的扩展登录功能
description: 此介绍介绍设置 Cloud POS 和 Retail Modern POS (MPOS) 扩展登录的选项。
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 79878e2ffbf219f77f378997c277ced8bb41598c
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021780"
---
# <a name="set-up-extended-logon-functionality-for-mpos-and-cloud-pos"></a><span data-ttu-id="4f7e0-103">为 MPOS 和 Cloud MPOS 设置扩展登录功能</span><span class="sxs-lookup"><span data-stu-id="4f7e0-103">Set up extended logon functionality for MPOS and Cloud POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4f7e0-104">此介绍介绍设置 Cloud POS 和 Retail Modern POS (MPOS) 扩展登录的选项。</span><span class="sxs-lookup"><span data-stu-id="4f7e0-104">This topic covers your options for setting up extended logon for Cloud POS and Retail Modern POS (MPOS).</span></span>

## <a name="setting-up-extended-logon"></a><span data-ttu-id="4f7e0-105">设置扩展登录</span><span class="sxs-lookup"><span data-stu-id="4f7e0-105">Setting up extended logon</span></span>

<span data-ttu-id="4f7e0-106">您可以在 **Retail 和 Commerce** &gt; **渠道设置** &gt; **POS 设置** &gt; **POS 配置文件** &gt; **功能配置文件**找到条码掩码的设置。</span><span class="sxs-lookup"><span data-stu-id="4f7e0-106">You can find the setup for bar code masks at **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Functionality profiles**.</span></span> <span data-ttu-id="4f7e0-107">**功能**快速选项卡包括与扩展登录有关的以下选项。</span><span class="sxs-lookup"><span data-stu-id="4f7e0-107">The **Functions** FastTab includes the following options that are related to extended logon.</span></span>

### <a name="staff-bar-code-logon"></a><span data-ttu-id="4f7e0-108">职员条码登录</span><span class="sxs-lookup"><span data-stu-id="4f7e0-108">Staff bar code logon</span></span>

<span data-ttu-id="4f7e0-109">在**职员条码登录**选项启用时，将扩展登录分配到销售点 (POS) 凭据的工作人员可以使用条码登录。</span><span class="sxs-lookup"><span data-stu-id="4f7e0-109">When the **Staff bar code logon** option is enabled, workers who have an extended logon assigned to their point of sale (POS) credentials can log on by using a bar code.</span></span>

### <a name="staff-bar-code-logon-requires-password"></a><span data-ttu-id="4f7e0-110">职员条码登录需要密码</span><span class="sxs-lookup"><span data-stu-id="4f7e0-110">Staff bar code logon requires password</span></span>

<span data-ttu-id="4f7e0-111">在**职员条码登录需要密码**选项启用时，职员条码登录只选择分配给存在的扩展登录的工作人员。</span><span class="sxs-lookup"><span data-stu-id="4f7e0-111">When the **Staff bar code logon requires password** option is enabled, the staff bar code logon selects only the worker who is assigned to the extended logon that is presented.</span></span> <span data-ttu-id="4f7e0-112">在此选项启用时，工作人员仍必须输入密码。</span><span class="sxs-lookup"><span data-stu-id="4f7e0-112">Workers must still enter their password when this option is enabled.</span></span>

### <a name="staff-card-logon"></a><span data-ttu-id="4f7e0-113">职员卡登录</span><span class="sxs-lookup"><span data-stu-id="4f7e0-113">Staff card logon</span></span>

<span data-ttu-id="4f7e0-114">在**职员卡登录**选项启用时，将扩展登录分配到 POS 凭据的工作人员可以使用磁条登录。</span><span class="sxs-lookup"><span data-stu-id="4f7e0-114">When the **Staff card logon** option is enabled, workers who have an extended logon assigned to their POS credentials can log on by using a magnetic stripe.</span></span>

### <a name="staff-card-logon-requires-password"></a><span data-ttu-id="4f7e0-115">职员卡登录需要密码</span><span class="sxs-lookup"><span data-stu-id="4f7e0-115">Staff card logon requires password</span></span>

<span data-ttu-id="4f7e0-116">在**职员卡登录需要密码**选项启用时，职员卡码登录只选择分配给存在的扩展登录的工作人员。</span><span class="sxs-lookup"><span data-stu-id="4f7e0-116">When the **Staff card logon requires password** option is enabled, the staff card logon selects only the worker who is assigned to the extended logon that is presented.</span></span> <span data-ttu-id="4f7e0-117">在此选项启用时，工作人员仍必须输入密码。</span><span class="sxs-lookup"><span data-stu-id="4f7e0-117">Workers must still enter their password when this option is enabled.</span></span>

## <a name="assigning-an-extended-logon"></a><span data-ttu-id="4f7e0-118">分配扩展登录</span><span class="sxs-lookup"><span data-stu-id="4f7e0-118">Assigning an extended logon</span></span>

<span data-ttu-id="4f7e0-119">默认情况下，只有经理可以将扩展登录分配给工作人员。</span><span class="sxs-lookup"><span data-stu-id="4f7e0-119">By default, only managers can assign extended logon to workers.</span></span> <span data-ttu-id="4f7e0-120">要分配扩展登录，转到 POS 中的**扩展登录**。</span><span class="sxs-lookup"><span data-stu-id="4f7e0-120">To assign extended logon, go to **Extended log on** in POS.</span></span> <span data-ttu-id="4f7e0-121">然后通过在搜索字段中输入他或她的操作员 ID 搜索工作人员。</span><span class="sxs-lookup"><span data-stu-id="4f7e0-121">Then search for a worker by entering his or her operator ID in the search field.</span></span> <span data-ttu-id="4f7e0-122">选择工作人员，然后单击**分配**。</span><span class="sxs-lookup"><span data-stu-id="4f7e0-122">Select the worker, and then click **Assign**.</span></span> <span data-ttu-id="4f7e0-123">在下一个页面，刷卡或扫描扩展登录以分配给工作人员。</span><span class="sxs-lookup"><span data-stu-id="4f7e0-123">On the next page, swipe or scan the extended logon to assign to the worker.</span></span> <span data-ttu-id="4f7e0-124">如果成功读取刷卡或扫描，**确定**按钮将可用。</span><span class="sxs-lookup"><span data-stu-id="4f7e0-124">If the swipe or scan is successfully read, the **OK** button becomes available.</span></span> <span data-ttu-id="4f7e0-125">单击**确定**为该工作人员保存扩展登录。</span><span class="sxs-lookup"><span data-stu-id="4f7e0-125">Click **OK** to save the extended logon for that worker.</span></span>

## <a name="deleting-an-extended-logon"></a><span data-ttu-id="4f7e0-126">删除扩展登录</span><span class="sxs-lookup"><span data-stu-id="4f7e0-126">Deleting an extended logon</span></span>

<span data-ttu-id="4f7e0-127">若要删除分配给工作人员的扩展登录，使用**扩展登录**操作搜索工作人员。</span><span class="sxs-lookup"><span data-stu-id="4f7e0-127">To delete the extended logon that is assigned to a worker, search for the worker by using the **Extended log on** operation.</span></span> <span data-ttu-id="4f7e0-128">选择工作人员，然后单击**取消分配**。</span><span class="sxs-lookup"><span data-stu-id="4f7e0-128">Select the worker, and then click **Unassign**.</span></span> <span data-ttu-id="4f7e0-129">与该工作人员关联的所有扩展登录凭据将被删除。</span><span class="sxs-lookup"><span data-stu-id="4f7e0-129">All extended logon credentials that are associated with that worker are removed.</span></span>

## <a name="extending-extended-logon"></a><span data-ttu-id="4f7e0-130">扩展扩展登录</span><span class="sxs-lookup"><span data-stu-id="4f7e0-130">Extending extended logon</span></span>

<span data-ttu-id="4f7e0-131">登录服务可扩展以支持其他扩展登录设备，例如掌上扫描仪。</span><span class="sxs-lookup"><span data-stu-id="4f7e0-131">The logon service can be extended to support additional extended logon devices, such as palm scanners.</span></span> <span data-ttu-id="4f7e0-132">有关详细信息，请参阅 POS 可扩展性文档。</span><span class="sxs-lookup"><span data-stu-id="4f7e0-132">For more information, see the POS extensibility documentation.</span></span>

## <a name="using-extended-logon"></a><span data-ttu-id="4f7e0-133">使用扩展登录</span><span class="sxs-lookup"><span data-stu-id="4f7e0-133">Using extended logon</span></span>

<span data-ttu-id="4f7e0-134">在配置扩展登录时，并且工作人员已被分配了条码或磁条，在 POS 登录页显示时，工作人员必须刷或扫描他或她的卡。</span><span class="sxs-lookup"><span data-stu-id="4f7e0-134">When extended logon is configured, and a worker has been assigned a bar code or magnetic stripe, the worker just has to swipe or scan his or her card while the POS logon page is displayed.</span></span> <span data-ttu-id="4f7e0-135">如果还需要密码才能继续登录，系统将提示工作人员输入他或她的密码。</span><span class="sxs-lookup"><span data-stu-id="4f7e0-135">If a password is also required before logon can proceed, the worker is prompted to enter his or her password.</span></span>

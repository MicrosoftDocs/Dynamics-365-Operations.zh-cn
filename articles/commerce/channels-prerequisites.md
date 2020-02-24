---
title: 渠道设置先决条件
description: 此主题概述 Microsoft Dynamics 365 Commerce 中的渠道设置先决条件。
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b861d90f1333c8f6e61a83602ed74e30b65f3dc1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002281"
---
# <a name="channel-setup-prerequisites"></a><span data-ttu-id="ab3f6-103">渠道设置先决条件</span><span class="sxs-lookup"><span data-stu-id="ab3f6-103">Channel setup prerequisites</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ab3f6-104">此主题概述 Microsoft Dynamics 365 Commerce 中的渠道设置先决条件。</span><span class="sxs-lookup"><span data-stu-id="ab3f6-104">This topic presents an overview of channel setup prerequisites in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ab3f6-105">概览</span><span class="sxs-lookup"><span data-stu-id="ab3f6-105">Overview</span></span>

<span data-ttu-id="ab3f6-106">在可以创建 Dynamics 365 Commerce 通道之前，必须完成几个先决条件任务。</span><span class="sxs-lookup"><span data-stu-id="ab3f6-106">Before a Dynamics 365 Commerce channel can be created, several prerequisite tasks must be completed.</span></span> <span data-ttu-id="ab3f6-107">以下先决条件任务列表按渠道类型进行组织。</span><span class="sxs-lookup"><span data-stu-id="ab3f6-107">The following lists of prerequisite tasks are organized by channel type.</span></span>

> [!NOTE]
> <span data-ttu-id="ab3f6-108">一些文档仍在编写中，链接将随着新内容的发布而更新。</span><span class="sxs-lookup"><span data-stu-id="ab3f6-108">Some documentation is still being written, and links will be updated as new content is published.</span></span>

## <a name="initialization"></a><span data-ttu-id="ab3f6-109">初始化</span><span class="sxs-lookup"><span data-stu-id="ab3f6-109">Initialization</span></span>

- [<span data-ttu-id="ab3f6-110">初始化种子数据</span><span class="sxs-lookup"><span data-stu-id="ab3f6-110">Initialize seed data</span></span>](../retail/enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a><span data-ttu-id="ab3f6-111">所有渠道类型所需的全局先决条件</span><span class="sxs-lookup"><span data-stu-id="ab3f6-111">Global prerequisities required for all channel types</span></span>

- [<span data-ttu-id="ab3f6-112">定义和配置法人结构</span><span class="sxs-lookup"><span data-stu-id="ab3f6-112">Define and configure your legal entity structure</span></span>](channels-legal-entities.md) 
- [<span data-ttu-id="ab3f6-113">配置组织层次结构</span><span class="sxs-lookup"><span data-stu-id="ab3f6-113">Configure your organizational hierarchy</span></span>](channels-org-hierarchies.md)
- [<span data-ttu-id="ab3f6-114">设置仓库</span><span class="sxs-lookup"><span data-stu-id="ab3f6-114">Set up a warehouse</span></span>](channels-setup-warehouse.md)
- [<span data-ttu-id="ab3f6-115">配置销售税</span><span class="sxs-lookup"><span data-stu-id="ab3f6-115">Configure sales tax</span></span>](https://docs.microsoft.com/en-us/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="ab3f6-116">设置电子邮件通知配置文件</span><span class="sxs-lookup"><span data-stu-id="ab3f6-116">Set up an email notification profile</span></span>](email-notification-profiles.md)
- [<span data-ttu-id="ab3f6-117">设置编号规则</span><span class="sxs-lookup"><span data-stu-id="ab3f6-117">Set up number sequences</span></span>](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="ab3f6-118">设置默认客户和通讯簿</span><span class="sxs-lookup"><span data-stu-id="ab3f6-118">Set up a default customer and address book</span></span>](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a><span data-ttu-id="ab3f6-119">零售渠道先决条件</span><span class="sxs-lookup"><span data-stu-id="ab3f6-119">Retail channel prerequisites</span></span>

- [<span data-ttu-id="ab3f6-120">信息代码和信息代码组</span><span class="sxs-lookup"><span data-stu-id="ab3f6-120">Info codes and info code groups</span></span>](https://docs.microsoft.com/en-us/dynamics365/retail/info-codes-retail?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="ab3f6-121">设置零售功能配置文件</span><span class="sxs-lookup"><span data-stu-id="ab3f6-121">Set up a retail functionality profile</span></span>](retail-functionality-profile.md)
- [<span data-ttu-id="ab3f6-122">设置员工通讯簿</span><span class="sxs-lookup"><span data-stu-id="ab3f6-122">Set up an employee address book</span></span>](new-address-book.md)
- [<span data-ttu-id="ab3f6-123">设置屏幕布局</span><span class="sxs-lookup"><span data-stu-id="ab3f6-123">Set up a screen layout</span></span>](https://docs.microsoft.com/en-us/dynamics365/retail/pos-screen-layouts?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="ab3f6-124">设置硬件工作站</span><span class="sxs-lookup"><span data-stu-id="ab3f6-124">Set up a hardware station</span></span>](https://docs.microsoft.com/en-us/dynamics365/retail/retail-hardware-station-configuration-installation?toc=/dynamics365/commerce/toc.json)

## <a name="call-center-channel-prerequisites"></a><span data-ttu-id="ab3f6-125">呼叫中心渠道先决条件</span><span class="sxs-lookup"><span data-stu-id="ab3f6-125">Call Center channel prerequisites</span></span>

- <span data-ttu-id="ab3f6-126">呼叫中心参数</span><span class="sxs-lookup"><span data-stu-id="ab3f6-126">Call center parameters</span></span>
- <span data-ttu-id="ab3f6-127">呼叫中心退款方式</span><span class="sxs-lookup"><span data-stu-id="ab3f6-127">Call center refund methods</span></span>
- <span data-ttu-id="ab3f6-128">租赁类型</span><span class="sxs-lookup"><span data-stu-id="ab3f6-128">Rental types</span></span>
- <span data-ttu-id="ab3f6-129">付款服务</span><span class="sxs-lookup"><span data-stu-id="ab3f6-129">Payment services</span></span>
- <span data-ttu-id="ab3f6-130">订单保留代码</span><span class="sxs-lookup"><span data-stu-id="ab3f6-130">Order hold codes</span></span>

## <a name="online-channel-prerequisites"></a><span data-ttu-id="ab3f6-131">在线渠道先决条件</span><span class="sxs-lookup"><span data-stu-id="ab3f6-131">Online channel prerequisites</span></span>

- [<span data-ttu-id="ab3f6-132">创建在线功能配置文件</span><span class="sxs-lookup"><span data-stu-id="ab3f6-132">Create an online functionality profile</span></span>](online-functionality-profile.md)

## <a name="additional-resources"></a><span data-ttu-id="ab3f6-133">其他资源</span><span class="sxs-lookup"><span data-stu-id="ab3f6-133">Additional resources</span></span>

[<span data-ttu-id="ab3f6-134">渠道概览</span><span class="sxs-lookup"><span data-stu-id="ab3f6-134">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="ab3f6-135">组织和组织层次结构概览</span><span class="sxs-lookup"><span data-stu-id="ab3f6-135">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="ab3f6-136">设置组织层次结构</span><span class="sxs-lookup"><span data-stu-id="ab3f6-136">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="ab3f6-137">创建法人</span><span class="sxs-lookup"><span data-stu-id="ab3f6-137">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="ab3f6-138">设置零售渠道</span><span class="sxs-lookup"><span data-stu-id="ab3f6-138">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="ab3f6-139">设置在线渠道</span><span class="sxs-lookup"><span data-stu-id="ab3f6-139">Set up an online channel</span></span>](channel-setup-online.md)

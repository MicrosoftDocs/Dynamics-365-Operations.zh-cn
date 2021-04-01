---
title: 仓库工作疑难解答
description: 此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中处理仓库工作时可能遇到的常见问题。
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: b1814f7b23efda2cabdb7bfc7bea4de6e3d6ec2f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237051"
---
# <a name="troubleshoot-warehouse-work"></a><span data-ttu-id="7df89-103">仓库工作疑难解答</span><span class="sxs-lookup"><span data-stu-id="7df89-103">Troubleshoot warehouse work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7df89-104">此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中处理仓库工作时可能遇到的常见问题。</span><span class="sxs-lookup"><span data-stu-id="7df89-104">This topic describes how to fix common issues that you might encounter while you work with warehouse work in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-cant-move-license-plates-that-have-serial-number-items-when-blank-issue-and-blank-receipt-are-allowed-on-the-tracking-dimension-group"></a><span data-ttu-id="7df89-105">当跟踪维度组中允许空发货和空收货时，我无法移动具有序列号项的牌照。</span><span class="sxs-lookup"><span data-stu-id="7df89-105">I can't move license plates that have serial number items when blank issue and blank receipt are allowed on the tracking dimension group.</span></span>

### <a name="issue-description"></a><span data-ttu-id="7df89-106">问题描述</span><span class="sxs-lookup"><span data-stu-id="7df89-106">Issue description</span></span>

<span data-ttu-id="7df89-107">如果序列号在跟踪维度组上有 *允许空发货* 和 *允许空收货* 设置，并且同一个位置有多个牌照，其中一些有序列号，另一些则没有，这种情况下您无法使用 **移动** 菜单项移动牌照。</span><span class="sxs-lookup"><span data-stu-id="7df89-107">You can't move a license plate by using a **Movement** menu item if the serial number has settings of *Blank issue allowed* and *Blank receipt allowed* on the tracking dimension group, and if there are multiple license plates in the same location, some of which have serial numbers and some of which don't have them.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7df89-108">解决问题</span><span class="sxs-lookup"><span data-stu-id="7df89-108">Issue resolution</span></span>

<span data-ttu-id="7df89-109">此问题将通过 [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687) 中部署的更改修复。</span><span class="sxs-lookup"><span data-stu-id="7df89-109">This issue will be fixed by changes that are deployed in [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687).</span></span> <span data-ttu-id="7df89-110">当允许空收货和空发货时，这些更改将使 **序列号** 字段变为可选。</span><span class="sxs-lookup"><span data-stu-id="7df89-110">Those changes will make the **Serial number** field optional when blank receipt and blank issue are allowed.</span></span>

## <a name="i-receive-the-following-error-message-in-the-warehouse-app-when-i-process-movements-the-inventory-owner-1-is-not-allowed-in-this-process"></a><span data-ttu-id="7df89-111">处理移动时，我在仓库应用中收到以下错误消息：“此流程不允许库存所有者 %1。”</span><span class="sxs-lookup"><span data-stu-id="7df89-111">I receive the following error message in the warehouse app when I process movements: "The inventory owner %1 is not allowed in this process."</span></span>

### <a name="issue-description"></a><span data-ttu-id="7df89-112">问题描述</span><span class="sxs-lookup"><span data-stu-id="7df89-112">Issue description</span></span>

<span data-ttu-id="7df89-113">当使用仓库应用进行移动时，缺少 **所有者** 跟踪维度。</span><span class="sxs-lookup"><span data-stu-id="7df89-113">The **Owner** tracking dimension is missing when the warehouse app is used to make movements.</span></span> <span data-ttu-id="7df89-114">Supply Chain Management 客户端中的常规库存转移日记帐好像可以按预期工作，但只能在填充了 **所有者** 维度时过帐。</span><span class="sxs-lookup"><span data-stu-id="7df89-114">A regular inventory transfer journal from the Supply Chain Management client appears to work as intended and can be posted only if the **Owner** dimension is filled in.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7df89-115">解决问题</span><span class="sxs-lookup"><span data-stu-id="7df89-115">Issue resolution</span></span>

<span data-ttu-id="7df89-116">Microsoft 已评估此问题，确定了这是一项功能限制。</span><span class="sxs-lookup"><span data-stu-id="7df89-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="7df89-117">当前，仓库管理流程仅支持法人所有的库存。</span><span class="sxs-lookup"><span data-stu-id="7df89-117">Currently, warehouse management processes support only inventory that is owned by the legal entity.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
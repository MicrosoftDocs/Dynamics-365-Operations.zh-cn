---
title: 通过安全角色访问专用地址
description: 本文说明如何解决客户无法访问专用地址的问题。
author: andreabichsel
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2edcef338f0ff8fcf231d4314fc972284397d000
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053315"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="3cff8-103">通过安全角色访问专用地址</span><span class="sxs-lookup"><span data-stu-id="3cff8-103">Access to private addresses by security role</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3cff8-104">**发货**</span><span class="sxs-lookup"><span data-stu-id="3cff8-104">**Issue**</span></span>

<span data-ttu-id="3cff8-105">在客户复制安全角色并以该新角色登录后，该客户无法看到标记为专用的地址。</span><span class="sxs-lookup"><span data-stu-id="3cff8-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="3cff8-106">**分辨率**</span><span class="sxs-lookup"><span data-stu-id="3cff8-106">**Resolution**</span></span>

<span data-ttu-id="3cff8-107">为了解决此问题，客户必须对复制的安全角色执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="3cff8-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="3cff8-108">转到 **组织管理 \> 全球通讯簿 \> 全球通讯簿参数**。</span><span class="sxs-lookup"><span data-stu-id="3cff8-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="3cff8-109">在 **专用位置安全** 选项卡上，将新安全角色从 **可用角色** 列表移到 **选定角色** 列表。</span><span class="sxs-lookup"><span data-stu-id="3cff8-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="3cff8-110">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="3cff8-110">Select **Save**.</span></span>

![全球通讯簿参数页面](media/GAD-parameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
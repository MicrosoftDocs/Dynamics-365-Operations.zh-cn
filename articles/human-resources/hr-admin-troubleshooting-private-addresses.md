---
title: 通过安全角色访问专用地址
description: 本文说明如何解决客户无法访问专用地址的问题。
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: facfd17f007b2c9e6f068d0ec4c5ce45b85a1b78
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008246"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="cbdf2-103">通过安全角色访问专用地址</span><span class="sxs-lookup"><span data-stu-id="cbdf2-103">Access to private addresses by security role</span></span>

<span data-ttu-id="cbdf2-104">**发货**</span><span class="sxs-lookup"><span data-stu-id="cbdf2-104">**Issue**</span></span>

<span data-ttu-id="cbdf2-105">在客户复制安全角色并以该新角色登录后，该客户无法看到标记为专用的地址。</span><span class="sxs-lookup"><span data-stu-id="cbdf2-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="cbdf2-106">**分辨率**</span><span class="sxs-lookup"><span data-stu-id="cbdf2-106">**Resolution**</span></span>

<span data-ttu-id="cbdf2-107">为了解决此问题，客户必须对复制的安全角色执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="cbdf2-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="cbdf2-108">转到**组织管理 \> 全球通讯簿 \> 全球通讯簿参数**。</span><span class="sxs-lookup"><span data-stu-id="cbdf2-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="cbdf2-109">在**专用位置安全**选项卡上，将新安全角色从**可用角色**列表移到**选定角色**列表。</span><span class="sxs-lookup"><span data-stu-id="cbdf2-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="cbdf2-110">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="cbdf2-110">Select **Save**.</span></span>

![全球通讯簿参数页面](media/GAD-parameters.png)
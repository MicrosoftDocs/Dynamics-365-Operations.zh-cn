---
title: 通过安全角色访问专用地址
description: 本主题说明如何解决客户无法访问专用地址的问题。
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: f8aaa33e5fda404b48548f9a57977dd0ccd53dc1
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517422"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="d7bbf-103">通过安全角色访问专用地址</span><span class="sxs-lookup"><span data-stu-id="d7bbf-103">Access to private addresses by security role</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d7bbf-104">**发货**</span><span class="sxs-lookup"><span data-stu-id="d7bbf-104">**Issue**</span></span>

<span data-ttu-id="d7bbf-105">在客户复制安全角色并以该新角色登录后，该客户无法看到标记为专用的地址。</span><span class="sxs-lookup"><span data-stu-id="d7bbf-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="d7bbf-106">**分辨率**</span><span class="sxs-lookup"><span data-stu-id="d7bbf-106">**Resolution**</span></span>

<span data-ttu-id="d7bbf-107">为了解决此问题，客户必须对复制的安全角色执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="d7bbf-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="d7bbf-108">转到**组织管理 \> 全球通讯簿 \> 全球通讯簿参数**。</span><span class="sxs-lookup"><span data-stu-id="d7bbf-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="d7bbf-109">在**专用位置安全**选项卡上，将新安全角色从**可用角色**列表移到**选定角色**列表。</span><span class="sxs-lookup"><span data-stu-id="d7bbf-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="d7bbf-110">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="d7bbf-110">Select **Save**.</span></span>

![全球通讯簿参数页面](media/GAD-parameters.png)

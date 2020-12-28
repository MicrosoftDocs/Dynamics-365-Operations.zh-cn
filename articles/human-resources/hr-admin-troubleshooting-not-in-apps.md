---
title: Human Resources 未出现在 Microsoft Dynamics 365 应用中
description: 本文说明如果客户在 Microsoft Dynamics 365 应用之间看不到 Microsoft Dynamics 365 Human Resources 应用该做什么。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cbf47b4673e1c97965bba7728e5669b7639c4d56
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417436"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a><span data-ttu-id="e1b30-103">Human Resources 未出现在 Microsoft Dynamics 365 应用中</span><span class="sxs-lookup"><span data-stu-id="e1b30-103">Human Resources doesn't appear in Microsoft Dynamics 365 apps</span></span>

<span data-ttu-id="e1b30-104">**发货**</span><span class="sxs-lookup"><span data-stu-id="e1b30-104">**Issue**</span></span>

<span data-ttu-id="e1b30-105">客户在 Microsoft Dynamics 365 应用之间看不到 Dynamics 365 Human Resources。</span><span class="sxs-lookup"><span data-stu-id="e1b30-105">The customer doesn't see Dynamics 365 Human Resources among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="e1b30-106">**解决方法**</span><span class="sxs-lookup"><span data-stu-id="e1b30-106">**Resolution**</span></span>

<span data-ttu-id="e1b30-107">用户必须在 Microsoft Power Apps 中被添加到环境的环境制造者角色。</span><span class="sxs-lookup"><span data-stu-id="e1b30-107">The user must be added to the Environment Maker role for the environment in Microsoft Power Apps.</span></span>

1. <span data-ttu-id="e1b30-108">具有 Power Apps 计划 2 许可证的管理员用户必须打开 [Power Apps 管理门户](https://preview.admin.powerapps.com/)。</span><span class="sxs-lookup"><span data-stu-id="e1b30-108">The admin user who has a Power Apps Plan 2 license must open the [Power Apps Admin portal](https://preview.admin.powerapps.com/).</span></span>

2. <span data-ttu-id="e1b30-109">选择 **环境**，然后为 Human Resources 选择正确的环境。</span><span class="sxs-lookup"><span data-stu-id="e1b30-109">Select **Environments**, and select the correct environment for Human Resources.</span></span>

3. <span data-ttu-id="e1b30-110">在 **安全** 选项卡上，在 **环境角色** 选项卡上，选择 **环境制造者**。</span><span class="sxs-lookup"><span data-stu-id="e1b30-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![环境角色选项卡](media/environment-roles.png)

4. <span data-ttu-id="e1b30-112">在 **用户** 选项卡上，添加用户或您的组织。</span><span class="sxs-lookup"><span data-stu-id="e1b30-112">On the **Users** tab, add the user or your organization.</span></span>

    ![用户选项卡](media/environment-maker.png)

5. <span data-ttu-id="e1b30-114">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="e1b30-114">Select **Save**.</span></span>

6. <span data-ttu-id="e1b30-115">用户现在必须登录到 [Microsoft Dynamics 365](https://home.dynamics.com/)。</span><span class="sxs-lookup"><span data-stu-id="e1b30-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>

7. <span data-ttu-id="e1b30-116">选择 **同步** 更新用户应用。</span><span class="sxs-lookup"><span data-stu-id="e1b30-116">Select **Sync** to update the user apps.</span></span>

    ![同步按钮](media/get-more.png)

    <span data-ttu-id="e1b30-118">在完成同步后，Human Resources 将显示在主页上。</span><span class="sxs-lookup"><span data-stu-id="e1b30-118">After synchronization is completed, Human Resources will appear on the home page.</span></span>

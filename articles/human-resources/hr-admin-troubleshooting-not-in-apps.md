---
title: Human Resources 未出现在 Microsoft Dynamics 365 应用中
description: 本文说明如果客户在 Microsoft Dynamics 365 应用之间看不到 Microsoft Dynamics 365 Human Resources 应用该做什么。
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: 9be1c2b862a01d6f14ad98dbcb01e061649c6af0
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463976"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a><span data-ttu-id="a80f8-103">Human Resources 未出现在 Microsoft Dynamics 365 应用中</span><span class="sxs-lookup"><span data-stu-id="a80f8-103">Human Resources doesn't appear in Microsoft Dynamics 365 apps</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="a80f8-104">**发货**</span><span class="sxs-lookup"><span data-stu-id="a80f8-104">**Issue**</span></span>

<span data-ttu-id="a80f8-105">客户在 Microsoft Dynamics 365 应用之间看不到 Dynamics 365 Human Resources。</span><span class="sxs-lookup"><span data-stu-id="a80f8-105">The customer doesn't see Dynamics 365 Human Resources among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="a80f8-106">**解决方法**</span><span class="sxs-lookup"><span data-stu-id="a80f8-106">**Resolution**</span></span>

<span data-ttu-id="a80f8-107">用户必须在 Microsoft Power Apps 中被添加到环境的环境制造者角色。</span><span class="sxs-lookup"><span data-stu-id="a80f8-107">The user must be added to the Environment Maker role for the environment in Microsoft Power Apps.</span></span>

1. <span data-ttu-id="a80f8-108">具有 Power Apps 计划 2 许可证的管理员用户必须打开 [Power Apps 管理门户](https://preview.admin.powerapps.com/)。</span><span class="sxs-lookup"><span data-stu-id="a80f8-108">The admin user who has a Power Apps Plan 2 license must open the [Power Apps Admin portal](https://preview.admin.powerapps.com/).</span></span>

2. <span data-ttu-id="a80f8-109">选择 **环境**，然后为 Human Resources 选择正确的环境。</span><span class="sxs-lookup"><span data-stu-id="a80f8-109">Select **Environments**, and select the correct environment for Human Resources.</span></span>

3. <span data-ttu-id="a80f8-110">在 **安全** 选项卡上，在 **环境角色** 选项卡上，选择 **环境制造者**。</span><span class="sxs-lookup"><span data-stu-id="a80f8-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![环境角色选项卡](media/environment-roles.png)

4. <span data-ttu-id="a80f8-112">在 **用户** 选项卡上，添加用户或您的组织。</span><span class="sxs-lookup"><span data-stu-id="a80f8-112">On the **Users** tab, add the user or your organization.</span></span>

    ![用户选项卡](media/environment-maker.png)

5. <span data-ttu-id="a80f8-114">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="a80f8-114">Select **Save**.</span></span>

6. <span data-ttu-id="a80f8-115">用户现在必须登录到 [Microsoft Dynamics 365](https://home.dynamics.com/)。</span><span class="sxs-lookup"><span data-stu-id="a80f8-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>

7. <span data-ttu-id="a80f8-116">选择 **同步** 更新用户应用。</span><span class="sxs-lookup"><span data-stu-id="a80f8-116">Select **Sync** to update the user apps.</span></span>

    ![同步按钮](media/get-more.png)

    <span data-ttu-id="a80f8-118">在完成同步后，Human Resources 将显示在主页上。</span><span class="sxs-lookup"><span data-stu-id="a80f8-118">After synchronization is completed, Human Resources will appear on the home page.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
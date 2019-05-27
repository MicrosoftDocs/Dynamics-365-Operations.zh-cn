---
title: Talent 未在 Microsoft Dynamics 365 应用 (Common Data Service 1.0) 中显示
description: 本主题说明如果客户在 Microsoft Dynamics 365 应用之间看不到 Microsoft Dynamics 365 for Talent 应用该做什么。
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
ms.openlocfilehash: ad5add2b572ccb6bff175806b965f63b53986152
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517473"
---
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-common-data-service-10"></a><span data-ttu-id="d9d50-103">Talent 未在 Microsoft Dynamics 365 应用 (Common Data Service 1.0) 中显示</span><span class="sxs-lookup"><span data-stu-id="d9d50-103">Talent doesn't appear among the Microsoft Dynamics 365 apps (Common Data Service 1.0)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d9d50-104">**发货**</span><span class="sxs-lookup"><span data-stu-id="d9d50-104">**Issue**</span></span>

<span data-ttu-id="d9d50-105">客户在 Microsoft Dynamics 365 应用之间看不到 Dynamics 365 for Talent 应用。</span><span class="sxs-lookup"><span data-stu-id="d9d50-105">The customer doesn't see the Microsoft Dynamics 365 for Talent app among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="d9d50-106">**分辨率**</span><span class="sxs-lookup"><span data-stu-id="d9d50-106">**Resolution**</span></span>

<span data-ttu-id="d9d50-107">用户必须在 Microsoft PowerApps 中被添加到环境的环境制造者角色。</span><span class="sxs-lookup"><span data-stu-id="d9d50-107">The user must be added to the Environment Maker role for the environment in Microsoft PowerApps.</span></span>

1. <span data-ttu-id="d9d50-108">具有 PowerApps 计划 2 许可证的管理员用户必须打开 [PowerApps 管理门户](https://preview.admin.powerapps.com/)。</span><span class="sxs-lookup"><span data-stu-id="d9d50-108">The admin user who has a PowerApps Plan 2 license must open the [PowerApps Admin portal](https://preview.admin.powerapps.com/).</span></span>
2. <span data-ttu-id="d9d50-109">选择**环境**，然后为 Talent 选择正确的环境。</span><span class="sxs-lookup"><span data-stu-id="d9d50-109">Select **Environments**, and select the correct environment for Talent.</span></span>
3. <span data-ttu-id="d9d50-110">在**安全**选项卡上，在**环境角色**选项卡上，选择**环境制造者**。</span><span class="sxs-lookup"><span data-stu-id="d9d50-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![环境角色选项卡](media/environment-roles.png)

4. <span data-ttu-id="d9d50-112">在**用户**选项卡上，添加用户或您的组织。</span><span class="sxs-lookup"><span data-stu-id="d9d50-112">On the **Users** tab, add the user or your organization.</span></span>

    ![用户选项卡](media/environment-maker.png)

5. <span data-ttu-id="d9d50-114">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="d9d50-114">Select **Save**.</span></span>
6. <span data-ttu-id="d9d50-115">用户现在必须登录到 [Microsoft Dynamics 365](https://home.dynamics.com/)。</span><span class="sxs-lookup"><span data-stu-id="d9d50-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>
7. <span data-ttu-id="d9d50-116">选择**同步**更新用户应用。</span><span class="sxs-lookup"><span data-stu-id="d9d50-116">Select **Sync** to update the user apps.</span></span>

    ![同步按钮](media/get-more.png)

    <span data-ttu-id="d9d50-118">在完成同步后，Talent 将显示在主页上。</span><span class="sxs-lookup"><span data-stu-id="d9d50-118">After synchronization is completed, Talent will appear on the home page.</span></span>

---
title: 在 Dynamics 365 - Core HR 中嵌入 PowerApps 应用程序
description: 此主题介绍如何解决 PowerApps 菜单项从系统管理模块中消失的问题。
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
ms.openlocfilehash: b510c10ebfcf4939eb2e1297972d27aa1812ae5a
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550995"
---
# <a name="embed-powerapps-apps-in-dynamics-365---core-hr"></a><span data-ttu-id="faddf-103">在 Dynamics 365 - Core HR 中嵌入 PowerApps 应用程序</span><span class="sxs-lookup"><span data-stu-id="faddf-103">Embed PowerApps apps in Dynamics 365 - Core HR</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="faddf-104">**发货**</span><span class="sxs-lookup"><span data-stu-id="faddf-104">**Issue**</span></span>

<span data-ttu-id="faddf-105">**PowerApps** 菜单项从**系统管理**模块中消失。</span><span class="sxs-lookup"><span data-stu-id="faddf-105">The **PowerApps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="faddf-106">**原因**</span><span class="sxs-lookup"><span data-stu-id="faddf-106">**Cause**</span></span>

<span data-ttu-id="faddf-107">用户界面 (UI) 设计已更改，Microsoft PowerApps 现在包含在标准个性化模型中。</span><span class="sxs-lookup"><span data-stu-id="faddf-107">The user interface (UI) design has been changed, and Microsoft PowerApps is now included in the standard personalization model.</span></span>

<span data-ttu-id="faddf-108">**解决方法**</span><span class="sxs-lookup"><span data-stu-id="faddf-108">**Resolution**</span></span>

<span data-ttu-id="faddf-109">PowerApps 应用程序的嵌入方式已更改。</span><span class="sxs-lookup"><span data-stu-id="faddf-109">The way that PowerApps apps are embedded has been changed.</span></span> <span data-ttu-id="faddf-110">PowerApps 应用程序现在通过个性化模型添加。</span><span class="sxs-lookup"><span data-stu-id="faddf-110">PowerApps apps are now added through the personalization model.</span></span> <span data-ttu-id="faddf-111">您可以将 PowerApps 应用程序添加到 Microsoft Dynamics 365 Talent 中的几乎所有页面。</span><span class="sxs-lookup"><span data-stu-id="faddf-111">You can add PowerApps apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="faddf-112">有关如何在 Talent 中嵌入 PowerApps 应用程序的信息，请参阅[嵌入 PowerApps 应用程序](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps)。</span><span class="sxs-lookup"><span data-stu-id="faddf-112">For information about how to embed PowerApps apps in Talent, see [Embed PowerApps apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="faddf-113">在更改前嵌入了应用程序的任何 PowerApps 客户应该已经升级到了新模型。</span><span class="sxs-lookup"><span data-stu-id="faddf-113">Any PowerApps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="faddf-114">**PowerApps** 按钮在 Talent 中几乎每个页面的右上角。</span><span class="sxs-lookup"><span data-stu-id="faddf-114">The **PowerApps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="faddf-115">您可以使用此按钮插入 PowerApps 应用程序。</span><span class="sxs-lookup"><span data-stu-id="faddf-115">You can use this button to insert a PowerApps app.</span></span>

<span data-ttu-id="faddf-116">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="faddf-116">Here is an example.</span></span>

1. <span data-ttu-id="faddf-117">转到**人事管理 \> 链接 \> 工作人员 \> 员工**。</span><span class="sxs-lookup"><span data-stu-id="faddf-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="faddf-118">选择 **PowerApps** 按钮，然后选择**插入 PowerApp**。</span><span class="sxs-lookup"><span data-stu-id="faddf-118">Select the **PowerApps** button, and then select **Insert a PowerApp**.</span></span>

    ![PowerApps 按钮](media/png.png)

3. <span data-ttu-id="faddf-120">填写**插入 PowerApp** 对话框中的字段。</span><span class="sxs-lookup"><span data-stu-id="faddf-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![插入 PowerApp 对话框](media/insert-powerapp.png)

<span data-ttu-id="faddf-122">或者，执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="faddf-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="faddf-123">在页面的操作窗格上，在**选项**选项卡上，在**个性化**组中，选择**个性化设置此窗体**。</span><span class="sxs-lookup"><span data-stu-id="faddf-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![在“选项”选项卡上个性化设置组](media/options.png)

    <span data-ttu-id="faddf-125">个性化设置工具栏将显示。</span><span class="sxs-lookup"><span data-stu-id="faddf-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="faddf-126">在工具栏上，选择**插入 \> PowerApp**。</span><span class="sxs-lookup"><span data-stu-id="faddf-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![使用个性化设置工具栏插入 PowerApps 应用程序](media/powerapp-bar.png)

---
title: "Core HR 中的嵌入 PowerApps 应用"
description: "此主题介绍如何解决 PowerApps 菜单项从系统管理模块中消失的问题。"
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 197b553f0b202ee29ad42274e2c0e03446ec782c
ms.contentlocale: zh-cn
ms.lasthandoff: 12/04/2018

---

# <a name="embed-powerapps-apps-in-core-hr"></a><span data-ttu-id="b8345-103">Core HR 中的嵌入 PowerApps 应用</span><span class="sxs-lookup"><span data-stu-id="b8345-103">Embed PowerApps apps in Core HR</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b8345-104">**发货**</span><span class="sxs-lookup"><span data-stu-id="b8345-104">**Issue**</span></span>

<span data-ttu-id="b8345-105">**PowerApps** 菜单项从**系统管理**模块中消失。</span><span class="sxs-lookup"><span data-stu-id="b8345-105">The **PowerApps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="b8345-106">**原因**</span><span class="sxs-lookup"><span data-stu-id="b8345-106">**Cause**</span></span>

<span data-ttu-id="b8345-107">用户界面 (UI) 设计已更改，Microsoft PowerApps 现在包含在标准个性化模型中。</span><span class="sxs-lookup"><span data-stu-id="b8345-107">The user interface (UI) design has been changed, and Microsoft PowerApps is now included in the standard personalization model.</span></span>

<span data-ttu-id="b8345-108">**分辨率**</span><span class="sxs-lookup"><span data-stu-id="b8345-108">**Resolution**</span></span>

<span data-ttu-id="b8345-109">PowerApps 应用的嵌入方式已更改。</span><span class="sxs-lookup"><span data-stu-id="b8345-109">The way that PowerApps apps are embedded has been changed.</span></span> <span data-ttu-id="b8345-110">PowerApps 应用现在通过个性化模型添加。</span><span class="sxs-lookup"><span data-stu-id="b8345-110">PowerApps apps are now added through the personalization model.</span></span> <span data-ttu-id="b8345-111">您可以将 PowerApps 应用添加到 Microsoft Dynamics 365 for Talent 中的几乎所有页面。</span><span class="sxs-lookup"><span data-stu-id="b8345-111">You can add PowerApps apps to almost all pages in Microsoft Dynamics 365 for Talent.</span></span>

<span data-ttu-id="b8345-112">有关如何在 Talent 中嵌入 PowerApps 应用的信息，请参阅[嵌入 PowerApps 应用](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps)。</span><span class="sxs-lookup"><span data-stu-id="b8345-112">For information about how to embed PowerApps apps in Talent, see [Embed PowerApps apps](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="b8345-113">在更改前嵌入了应用的任何 PowerApps 客户应该已经升级到了新模型。</span><span class="sxs-lookup"><span data-stu-id="b8345-113">Any PowerApps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="b8345-114">**PowerApps** 按钮在 Talent 中几乎每个页面的右上角。</span><span class="sxs-lookup"><span data-stu-id="b8345-114">The **PowerApps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="b8345-115">您可以使用此按钮插入 PowerApps 应用。</span><span class="sxs-lookup"><span data-stu-id="b8345-115">You can use this button to insert a PowerApps app.</span></span>

<span data-ttu-id="b8345-116">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="b8345-116">Here is an example.</span></span>

1. <span data-ttu-id="b8345-117">转到**人事管理 \> 链接 \> 工作人员 \> 员工**。</span><span class="sxs-lookup"><span data-stu-id="b8345-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="b8345-118">选择 **PowerApps** 按钮，然后选择**插入 PowerApp**。</span><span class="sxs-lookup"><span data-stu-id="b8345-118">Select the **PowerApps** button, and then select **Insert a PowerApp**.</span></span>

    ![PowerApps 按钮](media/png.png)

3. <span data-ttu-id="b8345-120">填写**插入 PowerApp** 对话框中的字段。</span><span class="sxs-lookup"><span data-stu-id="b8345-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![插入 PowerApp 对话框](media/insert-powerapp.png)

<span data-ttu-id="b8345-122">或者，执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="b8345-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="b8345-123">在页面的操作窗格上，在**选项**选项卡上，在**个性化**组中，选择**个性化设置此窗体**。</span><span class="sxs-lookup"><span data-stu-id="b8345-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![在“选项”选项卡上个性化设置组](media/options.png)

    <span data-ttu-id="b8345-125">个性化设置工具栏将显示。</span><span class="sxs-lookup"><span data-stu-id="b8345-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="b8345-126">在工具栏上，选择**插入 \> PowerApp**。</span><span class="sxs-lookup"><span data-stu-id="b8345-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![使用个性化设置工具栏插入 PowerApps 应用](media/powerapp-bar.png)


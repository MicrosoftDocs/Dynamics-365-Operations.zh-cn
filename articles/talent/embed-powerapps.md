---
title: 在 Dynamics 365 - Core HR 中嵌入 Power Apps 应用程序
description: 此主题介绍如何解决 Microsoft Power Apps 菜单项从系统管理模块中消失的问题。
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
ms.openlocfilehash: b1dd1756be349d85af8e6d7159623a2a95e75526
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898704"
---
# <a name="embed-power-apps-apps-in-dynamics-365---core-hr"></a><span data-ttu-id="10158-103">在 Dynamics 365 - Core HR 中嵌入 Power Apps 应用程序</span><span class="sxs-lookup"><span data-stu-id="10158-103">Embed Power Apps apps in Dynamics 365 - Core HR</span></span>

<span data-ttu-id="10158-104">**发货**</span><span class="sxs-lookup"><span data-stu-id="10158-104">**Issue**</span></span>

<span data-ttu-id="10158-105">**Power Apps** 菜单项从**系统管理**模块中消失。</span><span class="sxs-lookup"><span data-stu-id="10158-105">The **Power Apps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="10158-106">**原因**</span><span class="sxs-lookup"><span data-stu-id="10158-106">**Cause**</span></span>

<span data-ttu-id="10158-107">用户界面 (UI) 设计已更改，Microsoft Power Apps 现在包含在标准个性化模型中。</span><span class="sxs-lookup"><span data-stu-id="10158-107">The user interface (UI) design has been changed, and Microsoft Power Apps is now included in the standard personalization model.</span></span>

<span data-ttu-id="10158-108">**解决方法**</span><span class="sxs-lookup"><span data-stu-id="10158-108">**Resolution**</span></span>

<span data-ttu-id="10158-109">Power Apps 的嵌入方式已更改。</span><span class="sxs-lookup"><span data-stu-id="10158-109">The way that Power Apps are embedded has been changed.</span></span> <span data-ttu-id="10158-110">Power Apps 现在通过个性化模型添加。</span><span class="sxs-lookup"><span data-stu-id="10158-110">Power Apps are now added through the personalization model.</span></span> <span data-ttu-id="10158-111">您可以将 Power Apps 添加到 Microsoft Dynamics 365 Talent 中的几乎所有页面。</span><span class="sxs-lookup"><span data-stu-id="10158-111">You can add Power Apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="10158-112">有关如何在 Talent 中嵌入 Power Apps 的信息，请参阅[嵌入 Microsoft Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps)。</span><span class="sxs-lookup"><span data-stu-id="10158-112">For information about how to embed Power Apps in Talent, see [Embed Microsoft Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="10158-113">在更改前嵌入了应用程序的任何 Power Apps 客户应该已经升级到了新模型。</span><span class="sxs-lookup"><span data-stu-id="10158-113">Any Power Apps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="10158-114">**Power Apps** 按钮在 Talent 中几乎每个页面的右上角。</span><span class="sxs-lookup"><span data-stu-id="10158-114">The **Power Apps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="10158-115">您可以使用此按钮插入 Power Apps。</span><span class="sxs-lookup"><span data-stu-id="10158-115">You can use this button to insert Power Apps.</span></span>

<span data-ttu-id="10158-116">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="10158-116">Here is an example.</span></span>

1. <span data-ttu-id="10158-117">转到**人事管理 \> 链接 \> 工作人员 \> 员工**。</span><span class="sxs-lookup"><span data-stu-id="10158-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="10158-118">选择 **Power Apps** 按钮，然后选择**插入 PowerApp**。</span><span class="sxs-lookup"><span data-stu-id="10158-118">Select the **Power Apps** button, and then select **Insert a PowerApp**.</span></span>

    ![Power Apps 按钮](media/png.png)

3. <span data-ttu-id="10158-120">填写**插入 PowerApp** 对话框中的字段。</span><span class="sxs-lookup"><span data-stu-id="10158-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![插入 PowerApp 对话框](media/insert-powerapp.png)

<span data-ttu-id="10158-122">或者，执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="10158-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="10158-123">在页面的操作窗格上，在**选项**选项卡上，在**个性化**组中，选择**个性化设置此窗体**。</span><span class="sxs-lookup"><span data-stu-id="10158-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![在“选项”选项卡上个性化设置组](media/options.png)

    <span data-ttu-id="10158-125">个性化设置工具栏将显示。</span><span class="sxs-lookup"><span data-stu-id="10158-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="10158-126">在工具栏上，选择**插入 \> PowerApp**。</span><span class="sxs-lookup"><span data-stu-id="10158-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![使用个性化设置工具栏插入 Power Apps 应用程序](media/powerapp-bar.png)

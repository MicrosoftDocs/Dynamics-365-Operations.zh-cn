---
title: 使用“在新窗口中打开”功能并排显示页面
description: 本文说明如何并排显示页面。
author: aneesmsft
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ba583c2c9bcaaf106af75f8ac41f79bebc2c363
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748385"
---
# <a name="show-pages-side-by-side-using-the-open-in-new-window-feature"></a><span data-ttu-id="33bba-103">使用“在新窗口中打开”功能并排显示页面</span><span class="sxs-lookup"><span data-stu-id="33bba-103">Show pages side-by-side using the Open in new window feature</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="33bba-104">本文说明如何并排显示页面。</span><span class="sxs-lookup"><span data-stu-id="33bba-104">This article explains how to display pages side by side.</span></span>

<span data-ttu-id="33bba-105">您可能需要并行查看多个页面以快速完成任务。</span><span class="sxs-lookup"><span data-stu-id="33bba-105">You may want to view multiple pages side by side to complete tasks quickly.</span></span> <span data-ttu-id="33bba-106">例如，您可能希望在多个日记帐中验证或输入行。</span><span class="sxs-lookup"><span data-stu-id="33bba-106">As an example, you might want to validate or enter lines in more than one journal.</span></span> <span data-ttu-id="33bba-107">若要在多个日记帐中验证或输入，通常必须在显示日记帐列表的页面与显示给定日记帐行的页面之间来回切换。</span><span class="sxs-lookup"><span data-stu-id="33bba-107">Typically, to validate or enter lines in more than one journal, you would have to go back and forth between the page that displays a list of journals, and the page that displays lines for a given journal.</span></span> <span data-ttu-id="33bba-108">但是，利用 **在新窗口中打开** 功能，您可以并行显示这些页面，以便快速执行任务。</span><span class="sxs-lookup"><span data-stu-id="33bba-108">However, the **Open in new window** feature enables you to display these pages side-by-side so that you can perform your tasks quickly.</span></span>

<span data-ttu-id="33bba-109">继续上面提到的示例，在查看行时，您可以单击 **在新窗口中打开** 图标。</span><span class="sxs-lookup"><span data-stu-id="33bba-109">Continuing with the example mentioned above, when viewing the lines, you can click the **Open in new window** icon.</span></span>

<span data-ttu-id="33bba-110">[![单击“在新窗口中打开”图标。](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)</span><span class="sxs-lookup"><span data-stu-id="33bba-110">[![Click the Open in new window icon.](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)</span></span>

<span data-ttu-id="33bba-111">单击 **在新窗口中打开** 图标将在新的弹出浏览器中打开行页面，然后将历史记录中的原始浏览器导航回显示了日记帐列表的页面。</span><span class="sxs-lookup"><span data-stu-id="33bba-111">Clicking the **Open in new window** icon opens the lines page in a new, pop-up browser, and then navigates the original browser back in history to the page that displayed the list of journals.</span></span> <span data-ttu-id="33bba-112">然后，您可以并行显示这两个页面。</span><span class="sxs-lookup"><span data-stu-id="33bba-112">You can then display both pages side by side.</span></span> <span data-ttu-id="33bba-113">查看完日记帐后，可以在日记帐列表页面上更改所选日记帐，而且弹出窗口中的行页面将自动显示新选定日记帐的行。</span><span class="sxs-lookup"><span data-stu-id="33bba-113">After viewing a journal, you can change the selected journal on the journal list page, and the lines page in the pop-up window will automatically display the lines of the newly selected journal.</span></span>

<span data-ttu-id="33bba-114">[![您可以并排显示页面。](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)</span><span class="sxs-lookup"><span data-stu-id="33bba-114">[![You can display pages side-by-side.](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)</span></span>

<span data-ttu-id="33bba-115">由于返回这些页面的数据之间存在的关系，将会发生动态链接和刷新。</span><span class="sxs-lookup"><span data-stu-id="33bba-115">The dynamic linking and refreshing happens due to the relations that exist between the data that is backing these pages.</span></span> <span data-ttu-id="33bba-116">如果系统未意识到数据之间的关系，则弹出窗口将不会自动刷新以响应它源自的窗口中的更改。</span><span class="sxs-lookup"><span data-stu-id="33bba-116">If the system is not aware of the relation between the data, the pop-up window will not refresh automatically in response to a change in the window it originated from.</span></span>

<span data-ttu-id="33bba-117">某些页面具有多个视图，如网格视图、标题视图和详细信息视图。</span><span class="sxs-lookup"><span data-stu-id="33bba-117">Some pages have multiple views such as the Grid view, Header view, and Details view.</span></span> <span data-ttu-id="33bba-118">**在新窗口中打开** 图标会导致整个页面在新的浏览器窗口中打开。</span><span class="sxs-lookup"><span data-stu-id="33bba-118">The **Open in new window** icon causes the entire page to open in the new browser window.</span></span> <span data-ttu-id="33bba-119">因此，您无法使用 **在新窗口中打开** 功能并行保留同一页面的视图。</span><span class="sxs-lookup"><span data-stu-id="33bba-119">Therefore, you cannot keep two views of the same page side by side using the **Open in new window** feature.</span></span> <span data-ttu-id="33bba-120">几乎所有此类页面都有一个导航列表，可用来在记录之间切换并实现类似体验。</span><span class="sxs-lookup"><span data-stu-id="33bba-120">Almost all such pages have a navigation list that you can use to switch between records and achieve a similar experience.</span></span>

<span data-ttu-id="33bba-121">在使用 **在新窗口中打开** 功能之前，您应先将浏览器的弹出阻止程序配置为允许来自站点的 URL 的弹出窗口。</span><span class="sxs-lookup"><span data-stu-id="33bba-121">Before using the **Open in new window** feature, you should configure your browser's pop-up blocker to allow pop-ups from the URL of the site.</span></span> <span data-ttu-id="33bba-122">例如，您可允许来自“\*.dynamics.com”的弹出窗口。</span><span class="sxs-lookup"><span data-stu-id="33bba-122">As an example, you could allow pop-ups from "\*.dynamics.com".</span></span>

<span data-ttu-id="33bba-123">**在新窗口中打开** 功能仅在窗口中已打开多个页面时适用。</span><span class="sxs-lookup"><span data-stu-id="33bba-123">The **Open in new window** feature is only available when there is more than one page open in the window.</span></span> <span data-ttu-id="33bba-124">此外，弹出窗口将在未打开多个页面时（即您关闭该窗口中的最后一个页面时）自动关闭。</span><span class="sxs-lookup"><span data-stu-id="33bba-124">Also, the pop-up window automatically closes when there are no more pages open (that is, when you close the last page in that window).</span></span> <span data-ttu-id="33bba-125">系统还在您导航到该应用程序中的其他区域时关闭打开的页面。</span><span class="sxs-lookup"><span data-stu-id="33bba-125">The system also closes open pages when you navigate to a different area in the application.</span></span> <span data-ttu-id="33bba-126">因此，如果您打开弹出窗口并导航到该应用程序中的其他区域，则弹出窗口将自动关闭，因为系统已将这些窗口中的页面关闭。</span><span class="sxs-lookup"><span data-stu-id="33bba-126">Therefore, if you have pop-up windows open and navigate to a different area in the application, the pop-up windows close automatically because the system closed the pages in those windows.</span></span>

<span data-ttu-id="33bba-127">弹出窗口中的顶部栏显示有关页面已在其中打开且只读的公司的信息。</span><span class="sxs-lookup"><span data-stu-id="33bba-127">The top bar in the pop-up windows displays information about the company the page was opened in and is read-only.</span></span> <span data-ttu-id="33bba-128">弹出窗口还依赖主浏览器窗口。</span><span class="sxs-lookup"><span data-stu-id="33bba-128">The pop-up windows also rely on the main browser window.</span></span> <span data-ttu-id="33bba-129">如果关闭或刷新主窗口，则所有打开的弹出窗口将变为只读。</span><span class="sxs-lookup"><span data-stu-id="33bba-129">If the main window is closed or refreshed, all open pop-up windows will become read only.</span></span> <span data-ttu-id="33bba-130">如果出现这种情况，您仍可查看这些窗口中的信息，但将无法与其进行交互。</span><span class="sxs-lookup"><span data-stu-id="33bba-130">If this situation occurs, you can still view the information in these windows, but you will not be able to interact with it.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: 文档状态和生命周期
description: 此主题介绍 Microsoft Dynamics 365 Commerce 中的页面元素的各种文档状态。
author: phinneyridge
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a34d10edbf84ac1814afdc7107727aea68a303e0
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770427"
---
# <a name="document-states-and-lifecycle"></a><span data-ttu-id="bf0fd-103">文档状态和生命周期</span><span class="sxs-lookup"><span data-stu-id="bf0fd-103">Document states and lifecycle</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="bf0fd-104">此主题介绍 Microsoft Dynamics 365 Commerce 中的页面元素的各种文档状态。</span><span class="sxs-lookup"><span data-stu-id="bf0fd-104">This topic covers the various document states of page elements in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="document-state-descriptions"></a><span data-ttu-id="bf0fd-105">文档状态描述</span><span class="sxs-lookup"><span data-stu-id="bf0fd-105">Document state descriptions</span></span>

<span data-ttu-id="bf0fd-106">[页面元素](page-elements-overview.md)主题列出了内容管理系统 (CMS) 中的各种文档类型。</span><span class="sxs-lookup"><span data-stu-id="bf0fd-106">The [Page elements](page-elements-overview.md) topic lists various documents types in the content management system (CMS).</span></span> <span data-ttu-id="bf0fd-107">在创作工具中，这些文档类型可以具有多种状态。</span><span class="sxs-lookup"><span data-stu-id="bf0fd-107">These document types can have several states in the authoring tool.</span></span> <span data-ttu-id="bf0fd-108">文档状态可帮助避免数据冲突和实施版本控制。</span><span class="sxs-lookup"><span data-stu-id="bf0fd-108">The document states help prevent data conflicts and enforce version control.</span></span> <span data-ttu-id="bf0fd-109">它们决定谁可以更改文档，何时可以更改文档，以及其他人何时可查看更改。</span><span class="sxs-lookup"><span data-stu-id="bf0fd-109">They determine who can change the documents, when the documents can be changed, and when changes can be viewed by other people.</span></span>

<span data-ttu-id="bf0fd-110">下表显示 Commerce 中的页面元素可以的文档状态。</span><span class="sxs-lookup"><span data-stu-id="bf0fd-110">The following table shows the possible document states of page elements in Commerce.</span></span>

| <span data-ttu-id="bf0fd-111">单据状态</span><span class="sxs-lookup"><span data-stu-id="bf0fd-111">Document state</span></span> | <span data-ttu-id="bf0fd-112">说明</span><span class="sxs-lookup"><span data-stu-id="bf0fd-112">Description</span></span> |
|---|---|
| <span data-ttu-id="bf0fd-113">已签出</span><span class="sxs-lookup"><span data-stu-id="bf0fd-113">Checked out</span></span> | <span data-ttu-id="bf0fd-114">CMS 项签出给您后，不能被其他已经过身份验证的系统用户编辑。</span><span class="sxs-lookup"><span data-stu-id="bf0fd-114">When a CMS item is checked out to you, it can't be edited by any other authenticated system users.</span></span> <span data-ttu-id="bf0fd-115">您对项进行的所有更改只能对您显示。</span><span class="sxs-lookup"><span data-stu-id="bf0fd-115">Any changes that you make to the item are visible only to you.</span></span> |
| <span data-ttu-id="bf0fd-116">已签入</span><span class="sxs-lookup"><span data-stu-id="bf0fd-116">Checked in</span></span> | <span data-ttu-id="bf0fd-117">CMS 项签入后，所有更改对其他已经过身份验证的系统用户显示，然后，这些用户可以签出和编辑该项。</span><span class="sxs-lookup"><span data-stu-id="bf0fd-117">When a CMS item is checked in, all changes are visible to other authenticated system users, and those users can then check out the item and edit it.</span></span> <span data-ttu-id="bf0fd-118">每次签入在项的历史记录中创建一个文档版本记录。</span><span class="sxs-lookup"><span data-stu-id="bf0fd-118">Each check-in creates a document version record in the item's history.</span></span> |
| <span data-ttu-id="bf0fd-119">已发布</span><span class="sxs-lookup"><span data-stu-id="bf0fd-119">Published</span></span> | <span data-ttu-id="bf0fd-120">CMS 项发布后，将推送到您的活动站点，并且在 Internet 中可被未经身份验证的外部用户发现。</span><span class="sxs-lookup"><span data-stu-id="bf0fd-120">When a CMS item is published, it's pushed to your live site and becomes discoverable on the internet by non-authenticated external users.</span></span> <span data-ttu-id="bf0fd-121">只能发布已签入的项。</span><span class="sxs-lookup"><span data-stu-id="bf0fd-121">Items can be published only if they have been checked in.</span></span> |
| <span data-ttu-id="bf0fd-122">已保存</span><span class="sxs-lookup"><span data-stu-id="bf0fd-122">Saved</span></span> | <span data-ttu-id="bf0fd-123">可以将对已签出 CMS 项进行的更改保存到 CMS，之后才能签入或发布。</span><span class="sxs-lookup"><span data-stu-id="bf0fd-123">Changes that have been made to a checked-out CMS item can be saved to the CMS before the item is checked in or published.</span></span> <span data-ttu-id="bf0fd-124">签入项之前，保存的这些更改不对其他已身份验证的系统用户显示。</span><span class="sxs-lookup"><span data-stu-id="bf0fd-124">These saved changes aren't visible to other authenticated system users until the item is checked in.</span></span> <span data-ttu-id="bf0fd-125">发布项之前，不对外部用户显示。</span><span class="sxs-lookup"><span data-stu-id="bf0fd-125">They aren't visible to external users until the item is published.</span></span> |
| <span data-ttu-id="bf0fd-126">放弃签出</span><span class="sxs-lookup"><span data-stu-id="bf0fd-126">Discarded check out</span></span> | <span data-ttu-id="bf0fd-127">如果放弃已签出的 CMS 项，将删除保存的所有更改，而项将还原为最近签入的版本。</span><span class="sxs-lookup"><span data-stu-id="bf0fd-127">When a checked-out CMS item is discarded, all saved changes are deleted, and the item reverts to the version that was most recently checked in.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="bf0fd-128">其他资源</span><span class="sxs-lookup"><span data-stu-id="bf0fd-128">Additional resources</span></span>

[<span data-ttu-id="bf0fd-129">添加内容的方法</span><span class="sxs-lookup"><span data-stu-id="bf0fd-129">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="bf0fd-130">页面模型词汇表</span><span class="sxs-lookup"><span data-stu-id="bf0fd-130">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="bf0fd-131">使用模块</span><span class="sxs-lookup"><span data-stu-id="bf0fd-131">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="bf0fd-132">使用片段</span><span class="sxs-lookup"><span data-stu-id="bf0fd-132">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="bf0fd-133">模板和布局概览</span><span class="sxs-lookup"><span data-stu-id="bf0fd-133">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="bf0fd-134">自定义站点导航</span><span class="sxs-lookup"><span data-stu-id="bf0fd-134">Customize site navigation</span></span>](customize-site-navigation.md)

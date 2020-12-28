---
title: 文档状态和生命周期
description: 此主题介绍 Microsoft Dynamics 365 Commerce 中的页面元素的各种文档状态。
author: phinneyridge
manager: annbe
ms.date: 10/09/2020
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
ms.openlocfilehash: 8aad7ef8425e46182c669686710dfc178abc418f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410491"
---
# <a name="document-states-and-lifecycle"></a><span data-ttu-id="d3c9d-103">文档状态和生命周期</span><span class="sxs-lookup"><span data-stu-id="d3c9d-103">Document states and lifecycle</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d3c9d-104">此主题介绍 Microsoft Dynamics 365 Commerce 中的页面元素的各种文档状态。</span><span class="sxs-lookup"><span data-stu-id="d3c9d-104">This topic covers the various document states of page elements in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="document-state-descriptions"></a><span data-ttu-id="d3c9d-105">文档状态描述</span><span class="sxs-lookup"><span data-stu-id="d3c9d-105">Document state descriptions</span></span>

<span data-ttu-id="d3c9d-106">[页面元素](page-elements-overview.md)主题列出了内容管理系统 (CMS) 中的各种文档类型。</span><span class="sxs-lookup"><span data-stu-id="d3c9d-106">The [Page elements](page-elements-overview.md) topic lists various documents types in the content management system (CMS).</span></span> <span data-ttu-id="d3c9d-107">在创作工具中，这些文档类型可以具有多种状态。</span><span class="sxs-lookup"><span data-stu-id="d3c9d-107">These document types can have several states in the authoring tool.</span></span> <span data-ttu-id="d3c9d-108">文档状态可帮助避免数据冲突和实施版本控制。</span><span class="sxs-lookup"><span data-stu-id="d3c9d-108">The document states help prevent data conflicts and enforce version control.</span></span> <span data-ttu-id="d3c9d-109">它们决定谁可以更改文档，何时可以更改文档，以及其他人何时可查看更改。</span><span class="sxs-lookup"><span data-stu-id="d3c9d-109">They determine who can change the documents, when the documents can be changed, and when changes can be viewed by other people.</span></span>

<span data-ttu-id="d3c9d-110">下表显示 Commerce 中的页面元素可以的文档状态。</span><span class="sxs-lookup"><span data-stu-id="d3c9d-110">The following table shows the possible document states of page elements in Commerce.</span></span>

| <span data-ttu-id="d3c9d-111">单据状态</span><span class="sxs-lookup"><span data-stu-id="d3c9d-111">Document state</span></span>      | <span data-ttu-id="d3c9d-112">站点构建器操作</span><span class="sxs-lookup"><span data-stu-id="d3c9d-112">Site builder action</span></span>        | <span data-ttu-id="d3c9d-113">说明</span><span class="sxs-lookup"><span data-stu-id="d3c9d-113">Description</span></span>                                                  |
| ------------------- | -------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="d3c9d-114">已结账</span><span class="sxs-lookup"><span data-stu-id="d3c9d-114">Checked out</span></span>         | <span data-ttu-id="d3c9d-115">选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="d3c9d-115">Select **Edit**.</span></span>           | <span data-ttu-id="d3c9d-116">将把适用的文档签出给您。</span><span class="sxs-lookup"><span data-stu-id="d3c9d-116">The applicable document is checked out to you.</span></span> <span data-ttu-id="d3c9d-117">当文档处于此状态时，其他经过身份验证的系统用户不能更改此文档，而您对此文档进行的任何更改都仅对您可见。</span><span class="sxs-lookup"><span data-stu-id="d3c9d-117">While a document is in this state, it can't be changed by other authenticated system users, and any changes that you make to the document are visible only to you.</span></span> |
| <span data-ttu-id="d3c9d-118">已保存</span><span class="sxs-lookup"><span data-stu-id="d3c9d-118">Saved</span></span>               | <span data-ttu-id="d3c9d-119">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="d3c9d-119">Select **Save**.</span></span>           | <span data-ttu-id="d3c9d-120">将把已对签出文档进行的更改保存到数据库，但是尚未签入或发布该文档。</span><span class="sxs-lookup"><span data-stu-id="d3c9d-120">Changes that have been made to a checked-out document are saved to the database, but the document isn't yet checked in or published.</span></span> <span data-ttu-id="d3c9d-121">作者选择 **完成编辑** 之前，保存的更改不对其他已身份验证的系统用户显示。</span><span class="sxs-lookup"><span data-stu-id="d3c9d-121">The saved changes aren't visible to other authenticated system users until the author selects **Finish editing**.</span></span> <span data-ttu-id="d3c9d-122">发布项之前，不对外部用户显示。</span><span class="sxs-lookup"><span data-stu-id="d3c9d-122">They aren't visible to external users until the item is published.</span></span> |
| <span data-ttu-id="d3c9d-123">放弃签出</span><span class="sxs-lookup"><span data-stu-id="d3c9d-123">Discarded check out</span></span> | <span data-ttu-id="d3c9d-124">选择 **放弃编辑**。</span><span class="sxs-lookup"><span data-stu-id="d3c9d-124">Select **Discard edits**.</span></span>  | <span data-ttu-id="d3c9d-125">将放弃对签出文档进行的所有更改，而项目将恢复为签出前的最后一个版本。</span><span class="sxs-lookup"><span data-stu-id="d3c9d-125">All changes to the checked-out document are discarded, and the item reverts to the last version that was checked in.</span></span> |
| <span data-ttu-id="d3c9d-126">已签入</span><span class="sxs-lookup"><span data-stu-id="d3c9d-126">Checked in</span></span>          | <span data-ttu-id="d3c9d-127">选择 **完成编辑**。</span><span class="sxs-lookup"><span data-stu-id="d3c9d-127">Select **Finish editing**.</span></span> | <span data-ttu-id="d3c9d-128">将签入编辑的文档。</span><span class="sxs-lookup"><span data-stu-id="d3c9d-128">The edited document is checked in.</span></span> <span data-ttu-id="d3c9d-129">所有更改对其他已身份验证系统用户可见，并且这些用户可编辑此文档。</span><span class="sxs-lookup"><span data-stu-id="d3c9d-129">All changes are visible to other authenticated system users, and those users can then edit the document.</span></span> <span data-ttu-id="d3c9d-130">每次签入在项的历史记录中创建一个文档版本记录。</span><span class="sxs-lookup"><span data-stu-id="d3c9d-130">Each check-in creates a document version record in the item's history.</span></span> |
| <span data-ttu-id="d3c9d-131">已发布</span><span class="sxs-lookup"><span data-stu-id="d3c9d-131">Published</span></span>           | <span data-ttu-id="d3c9d-132">选择 **发布**。</span><span class="sxs-lookup"><span data-stu-id="d3c9d-132">Select **Publish**.</span></span>        | <span data-ttu-id="d3c9d-133">将发布文档，并且更改将发布给您的实时站点，并可被外部用户发现。</span><span class="sxs-lookup"><span data-stu-id="d3c9d-133">The document is published, and the changes are pushed to your live site and become discoverable by external users.</span></span> <span data-ttu-id="d3c9d-134">项只有在先通过选择 **完成编辑** 签入后才能发布。</span><span class="sxs-lookup"><span data-stu-id="d3c9d-134">Items can be published only if they have first been checked in by selecting **Finish editing**.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="d3c9d-135">其他资源</span><span class="sxs-lookup"><span data-stu-id="d3c9d-135">Additional resources</span></span>

[<span data-ttu-id="d3c9d-136">添加内容的方法</span><span class="sxs-lookup"><span data-stu-id="d3c9d-136">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="d3c9d-137">页面模型词汇表</span><span class="sxs-lookup"><span data-stu-id="d3c9d-137">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="d3c9d-138">使用发布组</span><span class="sxs-lookup"><span data-stu-id="d3c9d-138">Work with publish groups</span></span>](publish-groups.md)

[<span data-ttu-id="d3c9d-139">启用和使用跨渠道共享</span><span class="sxs-lookup"><span data-stu-id="d3c9d-139">Enable and use cross-channel sharing</span></span>](cross-channel-sharing.md)

[<span data-ttu-id="d3c9d-140">使用模块</span><span class="sxs-lookup"><span data-stu-id="d3c9d-140">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="d3c9d-141">使用片段</span><span class="sxs-lookup"><span data-stu-id="d3c9d-141">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="d3c9d-142">模板和布局概览</span><span class="sxs-lookup"><span data-stu-id="d3c9d-142">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="d3c9d-143">自定义站点导航</span><span class="sxs-lookup"><span data-stu-id="d3c9d-143">Customize site navigation</span></span>](customize-site-navigation.md)

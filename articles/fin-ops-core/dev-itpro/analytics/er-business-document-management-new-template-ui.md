---
title: 业务文档管理中的新文档用户界面
description: 本主题提供有关如何在电子报告 (ER) 框架的业务文档管理功能中使用新文档用户界面 (UI) 的信息。
author: v-anamir
manager: AnnBe
ms.date: 05/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4acde9703c721ab7c20d1603299a10dda91b23c4
ms.sourcegitcommit: b8f8ccab2cd9d848e5ecd71caaf0a63237e2236b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2020
ms.locfileid: "2957055"
---
# <a name="new-document-user-interface-in-business-document-management"></a><span data-ttu-id="16b84-103">业务文档管理中的新文档用户界面</span><span class="sxs-lookup"><span data-stu-id="16b84-103">New document user interface in Business document management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="16b84-104">业务文档管理使业务用户可以使用 Microsoft Office 365 服务或相应的 Microsoft Office 桌面应用程序来编辑业务文档模板。</span><span class="sxs-lookup"><span data-stu-id="16b84-104">Business document management lets business users edit business document templates by using a Microsoft Office 365 service or the appropriate Microsoft Office desktop application.</span></span> <span data-ttu-id="16b84-105">编辑可能包括设计更改或新部署，或者用户可能会添加占位符以包含其他数据，而不必更改源代码。</span><span class="sxs-lookup"><span data-stu-id="16b84-105">Edits might include design changes or new deployments, or users might add placeholders to include additional data without having to change the source code.</span></span> <span data-ttu-id="16b84-106">有关如何使用业务文档管理的更多信息，请参见[业务文档管理概述](er-business-document-management.md)。</span><span class="sxs-lookup"><span data-stu-id="16b84-106">For more information about how to work with Business document management, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="16b84-107">新的文档用户界面 (UI) 更清晰，使用起来更舒适。</span><span class="sxs-lookup"><span data-stu-id="16b84-107">The new document user interface (UI) is clearer and more comfortable to use.</span></span> <span data-ttu-id="16b84-108">**业务文档**区域仅显示当前提供商可用的模板。</span><span class="sxs-lookup"><span data-stu-id="16b84-108">The **Business document** area shows only the templates that are available for the current provider.</span></span>

<span data-ttu-id="16b84-109">利用**新建文件**按钮，用户能够以其他提供商提供的电子报告 (ER) 格式配置创建和编辑模板。</span><span class="sxs-lookup"><span data-stu-id="16b84-109">The **New document** button lets users create and edit a template in an Electronic reporting (ER) format configuration that is provided by another provider.</span></span> <span data-ttu-id="16b84-110">在本主题的示例中，提供者是 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="16b84-110">In the example in this topic, the provider is Microsoft.</span></span>

## <a name="make-the-new-document-ui-in-business-document-management-available"></a><span data-ttu-id="16b84-111">使业务文档管理中的新文档 UI 可用</span><span class="sxs-lookup"><span data-stu-id="16b84-111">Make the new document UI in Business document management available</span></span>

<span data-ttu-id="16b84-112">要开始使用业务文档管理中的新文档 UI，必须打开**功能管理**工作区中的**类似于 Office 的业务文档管理 UI 体验**功能。</span><span class="sxs-lookup"><span data-stu-id="16b84-112">To start to use the new document UI in Business document management, you must turn on the **Office-like UI experience for Business document management** feature in the **Feature management** workspace.</span></span>

<span data-ttu-id="16b84-113">请按照以下步骤为所有法人启用此功能。</span><span class="sxs-lookup"><span data-stu-id="16b84-113">Follow these steps to turn on this feature for all legal entities.</span></span>

1. <span data-ttu-id="16b84-114">在**功能管理**工作区中的**新建**选项卡上，选择列表中的**类似于 Office 的业务文档管理 UI 体验**功能。</span><span class="sxs-lookup"><span data-stu-id="16b84-114">In the **Feature management** workspace, on the **New** tab, select the **Office-like UI experience for Business document management** feature in the list.</span></span>
2. <span data-ttu-id="16b84-115">选择**立即启用**以打开所选功能。</span><span class="sxs-lookup"><span data-stu-id="16b84-115">Select **Enable now** to turn on the selected feature.</span></span>
3. <span data-ttu-id="16b84-116">刷新页面以访问新功能。</span><span class="sxs-lookup"><span data-stu-id="16b84-116">Refresh the page to access the new feature.</span></span>

### <a name="edit-templates-that-are-owned-by-other-providers"></a><span data-ttu-id="16b84-117">编辑其他提供商拥有的模板</span><span class="sxs-lookup"><span data-stu-id="16b84-117">Edit templates that are owned by other providers</span></span>

1. <span data-ttu-id="16b84-118">在**业务文档管理**工作区中，选择**新建文档**。</span><span class="sxs-lookup"><span data-stu-id="16b84-118">In the **Business document management** workspace, select **New document**.</span></span>

    ![业务文档管理工作区](./media/BDM_overview_new_template1.png)

2. <span data-ttu-id="16b84-120">在此对话框中，选择要用作模板的文档，然后选择**创建文档**。</span><span class="sxs-lookup"><span data-stu-id="16b84-120">In the dialog box, select the document to use as a template, and then select **Create document**.</span></span>

    ![业务文档对话框](./media/BDM_overview_new_template2.png)

3. <span data-ttu-id="16b84-122">在此新对话框内的**标题**字段中，根据需要更改标题。</span><span class="sxs-lookup"><span data-stu-id="16b84-122">In the new dialog box, in the **Title** field, change the title as you require.</span></span> <span data-ttu-id="16b84-123">标题文本用于命名自动创建的新 ER 格式配置。</span><span class="sxs-lookup"><span data-stu-id="16b84-123">The title text is used to name the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="16b84-124">此配置 (**Customer FTI report (GER) Copy**) 的草稿版本将包含编辑的模板，并且将用于为当前用户运行此 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="16b84-124">The draft version of this configuration (**Customer FTI report (GER) Copy**) will contain the edited template and will be used to run this ER format for the current user.</span></span> <span data-ttu-id="16b84-125">将使用来自基本 ER 格式配置的原始模板为每个其他用户运行此 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="16b84-125">The original template from the base ER format configuration will be used to run this ER format for every other user.</span></span>
4. <span data-ttu-id="16b84-126">在**名称**字段中，更改将自动创建的可编辑模板第一个修订的名称。</span><span class="sxs-lookup"><span data-stu-id="16b84-126">In the **Name** field, change the name of the first revision of the editable template that will be automatically created.</span></span>
5. <span data-ttu-id="16b84-127">在**注释**字段中，更新有关将自动创建的可编辑模板的修订注解。</span><span class="sxs-lookup"><span data-stu-id="16b84-127">In the **Comment** field, update the remarks for the revision of the editable template that will be automatically created.</span></span>
6. <span data-ttu-id="16b84-128">选择**确定**以确认开始执行编辑流程。</span><span class="sxs-lookup"><span data-stu-id="16b84-128">Select **OK** to confirm the start of the editing process.</span></span>

    ![文档创建对话框](./media/BDM_overview_new_template3.png)

<span data-ttu-id="16b84-130">**新建文件**按钮用于以其他提供商提供的 ER 格式配置创建和编辑模板。</span><span class="sxs-lookup"><span data-stu-id="16b84-130">The **New document** button is used to create and edit a template in an ER format configuration that is provided by another provider.</span></span> <span data-ttu-id="16b84-131">在本示例中，提供商是 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="16b84-131">In this example, the provider is Microsoft.</span></span> <span data-ttu-id="16b84-132">当您选择**新建文档**时，您可以查看当前提供商和其他提供商拥有的所有模板。</span><span class="sxs-lookup"><span data-stu-id="16b84-132">When you select **New document**, you can view all the templates that are owned by current and other providers.</span></span> <span data-ttu-id="16b84-133">选择模板后，将打开它进行编辑。</span><span class="sxs-lookup"><span data-stu-id="16b84-133">After you select the template, it's opened for editing.</span></span> <span data-ttu-id="16b84-134">然后将把编辑后的模板存储在自动生成的新 ER 格式配置中。</span><span class="sxs-lookup"><span data-stu-id="16b84-134">The edited template will then be stored in a new ER format configuration that is automatically generated.</span></span>

<span data-ttu-id="16b84-135">有关更多信息，请参见[业务文档管理概述](er-business-document-management.md)。</span><span class="sxs-lookup"><span data-stu-id="16b84-135">For more information, see [Business document management overview](er-business-document-management.md).</span></span>

---
title: 在税务配置中添加数据字段
description: 本主题说明如何通过添加数据字段自定义税务配置。
author: kailiang
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 197a2d1605dd39188841aba02a71d228c7138c54
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921181"
---
# <a name="add-data-fields-in-tax-configurations"></a><span data-ttu-id="d7766-103">在税务配置中添加数据字段</span><span class="sxs-lookup"><span data-stu-id="d7766-103">Add data fields in tax configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d7766-104">本主题说明如何通过使用[在税务集成中添加的数据字段](tax-service-add-data-fields-tax-integration-by-extension.md)自定义税务配置。</span><span class="sxs-lookup"><span data-stu-id="d7766-104">This topic explains how to customize tax configurations by using [data fields that are added in the tax integration](tax-service-add-data-fields-tax-integration-by-extension.md).</span></span>

## <a name="customize-the-tax-data-model"></a><span data-ttu-id="d7766-105">自定义税务数据模型</span><span class="sxs-lookup"><span data-stu-id="d7766-105">Customize the tax data model</span></span>

1. <span data-ttu-id="d7766-106">在 Microsoft Dynamics 365 Finance 中，转到 **电子报告** \> **税务配置**。</span><span class="sxs-lookup"><span data-stu-id="d7766-106">In Microsoft Dynamics 365 Finance, go to **Electronic Reporting** \> **Tax configurations**.</span></span>
2. <span data-ttu-id="d7766-107">在配置树中，选择 **税务数据模型 - 欧洲**。</span><span class="sxs-lookup"><span data-stu-id="d7766-107">In the configuration tree, select **Tax Data Model - Europe**.</span></span> <span data-ttu-id="d7766-108">然后，在操作窗格上，选择 **创建配置**。</span><span class="sxs-lookup"><span data-stu-id="d7766-108">Then, on the Action Pane, select **Create configuration**.</span></span>
3. <span data-ttu-id="d7766-109">在下拉对话框中，选择 **派生自名称的应纳税单据模型：税务数据模型 -- 欧洲，Microsoft** 选项，输入新税务数据模型的名称，然后选择 **创建配置**。</span><span class="sxs-lookup"><span data-stu-id="d7766-109">In the drop-down dialog box, select the **Taxable document model derived from Name: Tax Data Model -- Europe, Microsoft** option, enter a name for the new tax data model, and then select **Create configuration**.</span></span>
4. <span data-ttu-id="d7766-110">选择您刚创建的税务数据模型，然后在操作窗格上，选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="d7766-110">Select the tax data model that you just created, and then, on the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="d7766-111">展开数据模型树，选择 **行**，然后选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="d7766-111">Expand the data model tree, select **Lines**, and then select **New**.</span></span>
6. <span data-ttu-id="d7766-112">在 **创建节点** 对话框中，输入名称，指定物料类型，然后选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="d7766-112">In the **Create node** dialog box, enter a name, specify the item type, and then select **Add**.</span></span>
7. <span data-ttu-id="d7766-113">添加任何必需的列。</span><span class="sxs-lookup"><span data-stu-id="d7766-113">Add any required columns.</span></span>
8. <span data-ttu-id="d7766-114">在操作窗格上，选择 **保存**，然后选择 **完成**。</span><span class="sxs-lookup"><span data-stu-id="d7766-114">On the Action Pane, select **Save**, and then select **Complete**.</span></span>
9. <span data-ttu-id="d7766-115">关闭页面，然后查看税务数据模型的已完成版本。</span><span class="sxs-lookup"><span data-stu-id="d7766-115">Close the page, and view the completed version of your tax data model.</span></span>

## <a name="customize-the-tax-configuration"></a><span data-ttu-id="d7766-116">自定义税务配置</span><span class="sxs-lookup"><span data-stu-id="d7766-116">Customize the tax configuration</span></span>

1. <span data-ttu-id="d7766-117">在 Finance 中，转到 **电子报告** \> **税务配置**。</span><span class="sxs-lookup"><span data-stu-id="d7766-117">In Finance, go to **Electronic reporting** \> **Tax configurations**.</span></span>
2. <span data-ttu-id="d7766-118">在配置树中，选择 **税务配置 -- 欧洲**。</span><span class="sxs-lookup"><span data-stu-id="d7766-118">In the configuration tree, select **Tax Configuration -- Europe**.</span></span> <span data-ttu-id="d7766-119">然后，在操作窗格上，选择 **创建配置**。</span><span class="sxs-lookup"><span data-stu-id="d7766-119">Then, on the Action Pane, select **Create configuration**.</span></span>
3. <span data-ttu-id="d7766-120">在下拉对话框中，选择 **派生自名称的税务服务配置：税务配置 -- 欧洲，Microsoft** 选项，输入新税务配置的名称，然后选择 **创建配置**。</span><span class="sxs-lookup"><span data-stu-id="d7766-120">In the drop-down dialog box, select the **Tax service configuration derived from Name: Tax Configuration -- Europe, Microsoft** option, enter a name for the new tax configuration, and then select **Create configuration**.</span></span>
4. <span data-ttu-id="d7766-121">选择您刚创建的税务配置，然后在操作窗格上，选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="d7766-121">Select the tax configuration that you just created, and then, on the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="d7766-122">在 **属性** 部分中，在 **数据模型** 字段中，选择您之前创建的自定义税务数据模型。</span><span class="sxs-lookup"><span data-stu-id="d7766-122">In the **Properties** section, in the **Data model** field, select the customized tax data model that you created earlier.</span></span>
6. <span data-ttu-id="d7766-123">在 **数据模型版本** 字段中，选择税务数据模型的已完成版本。</span><span class="sxs-lookup"><span data-stu-id="d7766-123">In the **Data model version** field, select the completed version of the tax data model.</span></span>
7. <span data-ttu-id="d7766-124">选择 **添加**，然后添加所需的税务措施。</span><span class="sxs-lookup"><span data-stu-id="d7766-124">Select **Add**, and add the required tax measures.</span></span>
8. <span data-ttu-id="d7766-125">在操作窗格上，选择 **保存**，然后选择 **完成**。</span><span class="sxs-lookup"><span data-stu-id="d7766-125">On the Action Pane, select **Save**, and then select **Complete**.</span></span>
9. <span data-ttu-id="d7766-126">关闭页面，然后查看税务配置的已完成版本。</span><span class="sxs-lookup"><span data-stu-id="d7766-126">Close page, and view the completed version of your tax configuration.</span></span>

## <a name="implement-tax-features-in-the-customized-tax-configuration"></a><span data-ttu-id="d7766-127">在自定义税务配置中实施税务功能</span><span class="sxs-lookup"><span data-stu-id="d7766-127">Implement tax features in the customized tax configuration</span></span>

1. <span data-ttu-id="d7766-128">在 Regulatory Configuration Service (RCS) 中，转到 **全球化功能** \> **税务**。</span><span class="sxs-lookup"><span data-stu-id="d7766-128">In Regulatory Configuration Service (RCS), go to **Globalization Features** \> **Tax**.</span></span>
2. <span data-ttu-id="d7766-129">选择 **添加**，输入有关新功能的信息，然后选择 **创建功能**。</span><span class="sxs-lookup"><span data-stu-id="d7766-129">Select **Add**, enter information about the new feature, and then select **Create feature**.</span></span>
3. <span data-ttu-id="d7766-130">在 **版本** 选项卡上，选择功能，然后选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="d7766-130">On the **Versions** tab, select the feature, and then select **Edit**.</span></span>
4. <span data-ttu-id="d7766-131">在 **常规** 选项卡上，在 **配置版本** 字段中，选择自定义税务配置和版本。</span><span class="sxs-lookup"><span data-stu-id="d7766-131">On the **General** tab, in the **Configuration version** field, select the customized tax configuration and version.</span></span>
5. <span data-ttu-id="d7766-132">在 **管理列** 对话框中，选择要包含在自定义税务措施中的标题和行列，然后选择向右箭头按钮将其添加到 **所选列** 列表中。</span><span class="sxs-lookup"><span data-stu-id="d7766-132">In the **Manage columns** dialog box, select the header and line columns that you want to include in your customized tax measure, and then select the right arrow button to add them to the **Selected columns** list.</span></span>

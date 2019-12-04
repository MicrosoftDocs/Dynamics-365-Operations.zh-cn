---
title: 通过使用相连应用程序访问应用程序元数据
description: 本主题中的步骤介绍 Regulatory Configuration Service (RCS) 用户如何在 Finance and Operations 中通过使用元数据设计新的电子申报 (ER) 模型映射。
author: NickSelin
manager: AnnBe
ms.date: 06/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5020b523ca5d76d36f7436a8f43e8629c029e3e8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769870"
---
# <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="99de8-103">通过使用相连应用程序访问应用程序元数据</span><span class="sxs-lookup"><span data-stu-id="99de8-103">Access application metadata by using connected applications</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="99de8-104">以下步骤介绍系统管理员或电子报表开发人员角色的 Regulatory Configuration Service (RCS) 用户如何使用 Finance and Operations 中的元数据设计新的电子报表 (ER) 模型映射。</span><span class="sxs-lookup"><span data-stu-id="99de8-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using metadata in Finance and Operations.</span></span> <span data-ttu-id="99de8-105">将使用与 RCS 相连的应用程序联机访问应用程序元数据。</span><span class="sxs-lookup"><span data-stu-id="99de8-105">Application metadata will be accessed online by using the RCS connected application.</span></span> <span data-ttu-id="99de8-106">将配置示例 ER 模型映射以访问外贸交易。</span><span class="sxs-lookup"><span data-stu-id="99de8-106">Sample ER model mapping will be configured to access foreign trade transactions.</span></span> <span data-ttu-id="99de8-107">为了完成这些步骤，在 RCS 中，您必须首先完成[创建配置提供程序并标记为当前运行的](er-configuration-provider-mark-it-active-2016-11.md)主题中的步骤。</span><span class="sxs-lookup"><span data-stu-id="99de8-107">To complete these steps, in RCS you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="99de8-108">如果已完成了[使用 ER 配置访问应用程序元数据](access-application-metadata-er-configuration.md)主题中的步骤，请转至[电子申报示例页](https://go.microsoft.com/fwlink/?linkid=862266)下载并保存以下 ER 配置：Foreign trade metadata.xml、Foreign trade model.xml、Foreign trade mapping.xml，然后完成此过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="99de8-108">If you have not completed the steps in the topic, [Access application metadata by using ER configuration](access-application-metadata-er-configuration.md), go to the [Electronic reporting examples page](https://go.microsoft.com/fwlink/?linkid=862266) to download and save the following ER configurations: Foreign trade metadata.xml; Foreign trade model.xml; Foreign trade mapping.xml, and then complete the steps in the procedure.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="99de8-109">先决条件</span><span class="sxs-lookup"><span data-stu-id="99de8-109">Prerequisites</span></span>
1. <span data-ttu-id="99de8-110">转到**所有工作区** > **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="99de8-110">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="99de8-111">确保示例公司 Litware 公司的配置提供程序可用且标记为**有效**。</span><span class="sxs-lookup"><span data-stu-id="99de8-111">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="99de8-112">如果没有看到此配置提供程序，请首先完成[创建配置提供程序并标记为当前运行的](er-configuration-provider-mark-it-active-2016-11.md)这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="99de8-112">If you don’t see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="get-required-er-configurations"></a><span data-ttu-id="99de8-113">获取所需的 ER 配置</span><span class="sxs-lookup"><span data-stu-id="99de8-113">Get required ER configurations</span></span>
1. <span data-ttu-id="99de8-114">单击**申报配置**。</span><span class="sxs-lookup"><span data-stu-id="99de8-114">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="99de8-115">如果已经完成了[使用 ER 配置访问应用程序元数据](access-application-metadata-er-configuration.md)过程中的步骤，则当前 RCS 实例中已经拥有了所有必需的 ER 配置（外贸元数据、模型和映射配置）。</span><span class="sxs-lookup"><span data-stu-id="99de8-115">If you already completed the steps in the [Access application metadata by using ER configuration](access-application-metadata-er-configuration.md) procedure, you already have all necessary ER configurations (foreign trade metadata, model and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="99de8-116">您可以跳过此子任务的所有其余步骤。</span><span class="sxs-lookup"><span data-stu-id="99de8-116">You can skip all the remaining steps of this sub-task.</span></span> 
3. <span data-ttu-id="99de8-117">单击**交换**。</span><span class="sxs-lookup"><span data-stu-id="99de8-117">Click **Exchange**.</span></span> 
4. <span data-ttu-id="99de8-118">单击**从 XML 文件加载**。</span><span class="sxs-lookup"><span data-stu-id="99de8-118">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="99de8-119">单击**浏览**并选择 **Foreign trade metadata.xml** 文件。</span><span class="sxs-lookup"><span data-stu-id="99de8-119">Click **Browse** and select the **Foreign trade metadata.xml** file.</span></span> 
6. <span data-ttu-id="99de8-120">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="99de8-120">Click **OK**.</span></span> 
7. <span data-ttu-id="99de8-121">单击**交换**。</span><span class="sxs-lookup"><span data-stu-id="99de8-121">Click **Exchange**.</span></span> 
8. <span data-ttu-id="99de8-122">单击**从 XML 文件加载**。</span><span class="sxs-lookup"><span data-stu-id="99de8-122">Click **Load from XML file**.</span></span> 
9. <span data-ttu-id="99de8-123">单击**浏览**并选择 **Foreign trade model.xml** 文件。</span><span class="sxs-lookup"><span data-stu-id="99de8-123">Click **Browse** and select the **Foreign trade model.xml** file.</span></span> 
10. <span data-ttu-id="99de8-124">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="99de8-124">Click **OK**.</span></span> 
11. <span data-ttu-id="99de8-125">单击**交换**。</span><span class="sxs-lookup"><span data-stu-id="99de8-125">Click **Exchange**.</span></span> 
12. <span data-ttu-id="99de8-126">单击**从 XML 文件加载**。</span><span class="sxs-lookup"><span data-stu-id="99de8-126">Click **Load from XML file**.</span></span> 
13. <span data-ttu-id="99de8-127">单击**浏览**并选择 **Foreign trade mapping.xml** 文件。</span><span class="sxs-lookup"><span data-stu-id="99de8-127">Click **Browse** and select the **Foreign trade mapping.xml** file.</span></span> 
14. <span data-ttu-id="99de8-128">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="99de8-128">Click **OK**.</span></span> 

## <a name="register-a-connected-application"></a><span data-ttu-id="99de8-129">注册连接的应用程序</span><span class="sxs-lookup"><span data-stu-id="99de8-129">Register a connected application</span></span>
1. <span data-ttu-id="99de8-130">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="99de8-130">Close the page.</span></span> 
2. <span data-ttu-id="99de8-131">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="99de8-131">Close the page.</span></span> 
3. <span data-ttu-id="99de8-132">转到**所有工作区** > **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="99de8-132">Go to **All workspaces** > **Electronic reporting**.</span></span> 
4. <span data-ttu-id="99de8-133">单击**相连应用程序**。</span><span class="sxs-lookup"><span data-stu-id="99de8-133">Click **Connected applications**.</span></span> 
5. <span data-ttu-id="99de8-134">确保配置的应用程序基于 Azura 且可供当前 RCS 用户访问。</span><span class="sxs-lookup"><span data-stu-id="99de8-134">Make sure that the configured application is Azura based and accessible for the current RCS user.</span></span> <span data-ttu-id="99de8-135">还要求当前 RCS 用户可访问所选应用程序，并且已注册为此应用程序的用户，从而使其有权访问应用程序的元数据。</span><span class="sxs-lookup"><span data-stu-id="99de8-135">It is also required that the current RCS user has access to the selected application and has been registered as a user of this application playing a role giving him privileges to access application’s metadata.</span></span> 
6. <span data-ttu-id="99de8-136">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="99de8-136">Click **New**.</span></span> 
7. <span data-ttu-id="99de8-137">在**名称**字段中，键入“MyConnectedApp”。</span><span class="sxs-lookup"><span data-stu-id="99de8-137">In the **Name** field, type 'MyConnectedApp'.</span></span> 
8. <span data-ttu-id="99de8-138">在**应用程序**字段中，键入“https:// mycompany.operations.dynamics.com”。</span><span class="sxs-lookup"><span data-stu-id="99de8-138">In the **Application** field, type 'https:// mycompany.operations.dynamics.com'.</span></span> 
9. <span data-ttu-id="99de8-139">在**租户**字段中，键入“mycompany.onmicrosoft.com”。</span><span class="sxs-lookup"><span data-stu-id="99de8-139">In the **Tenant** field, type ‘mycompany.onmicrosoft.com’.</span></span> 
10. <span data-ttu-id="99de8-140">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="99de8-140">Click **Save**.</span></span> 
11. <span data-ttu-id="99de8-141">检查与配置的应用程序之间的连接时，请在**连接到远程应用程序**页中，单击**单击此处连接到所选远程应用程序**链接。</span><span class="sxs-lookup"><span data-stu-id="99de8-141">When you check connection to configured application, on the **Connect to remote application** page click **Click here to connect to selected remote application** link.</span></span> 
12. <span data-ttu-id="99de8-142">单击**检查连接**。</span><span class="sxs-lookup"><span data-stu-id="99de8-142">Click **Check connection**.</span></span> 
13. <span data-ttu-id="99de8-143">单击**关闭**。</span><span class="sxs-lookup"><span data-stu-id="99de8-143">Click **Close**.</span></span> 
14. <span data-ttu-id="99de8-144">连接验证成功完成后，将在当前网格中更新所配置应用程序的版本和租户详细信息。</span><span class="sxs-lookup"><span data-stu-id="99de8-144">When the connection validation succeeded, version and tenant details will be updated for the configured application in the current grid.</span></span> 

## <a name="review-existing-model-mapping-configuration"></a><span data-ttu-id="99de8-145">检查现有模型映射配置</span><span class="sxs-lookup"><span data-stu-id="99de8-145">Review existing model mapping configuration</span></span>
1. <span data-ttu-id="99de8-146">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="99de8-146">Close the page.</span></span> 
2. <span data-ttu-id="99de8-147">单击**申报配置**。</span><span class="sxs-lookup"><span data-stu-id="99de8-147">Click **Reporting configurations**.</span></span> 
3. <span data-ttu-id="99de8-148">在树中，展开**外贸模型**。</span><span class="sxs-lookup"><span data-stu-id="99de8-148">In the tree, expand **Foreign trade model**.</span></span> 
4. <span data-ttu-id="99de8-149">在树中，选择**外贸模型\外贸映射**。</span><span class="sxs-lookup"><span data-stu-id="99de8-149">In the tree, select **Foreign trade model\Foreign trade mapping**.</span></span> 
5. <span data-ttu-id="99de8-150">展开**先决条件**部分。</span><span class="sxs-lookup"><span data-stu-id="99de8-150">Expand the **Prerequisites** section.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="99de8-151">此映射当前引用元数据配置。</span><span class="sxs-lookup"><span data-stu-id="99de8-151">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="99de8-152">设计此模型映射时，将提供来自此配置的应用程序元数据。</span><span class="sxs-lookup"><span data-stu-id="99de8-152">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

6. <span data-ttu-id="99de8-153">单击**设计器**。</span><span class="sxs-lookup"><span data-stu-id="99de8-153">Click **Designer**.</span></span> 
7. <span data-ttu-id="99de8-154">单击**设计器**。</span><span class="sxs-lookup"><span data-stu-id="99de8-154">Click **Designer**.</span></span> 
8. <span data-ttu-id="99de8-155">在树中，选择 **Dynamics 365 for Operations\表记录**。</span><span class="sxs-lookup"><span data-stu-id="99de8-155">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
9. <span data-ttu-id="99de8-156">单击**添加根**。</span><span class="sxs-lookup"><span data-stu-id="99de8-156">Click **Add root**.</span></span> 
10. <span data-ttu-id="99de8-157">在**表格**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="99de8-157">In the **Table** field, enter or select a value.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="99de8-158">此映射当前引用元数据配置。</span><span class="sxs-lookup"><span data-stu-id="99de8-158">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="99de8-159">设计此模型映射时，将提供来自此配置的应用程序元数据。</span><span class="sxs-lookup"><span data-stu-id="99de8-159">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

11. <span data-ttu-id="99de8-160">单击**取消**。</span><span class="sxs-lookup"><span data-stu-id="99de8-160">Click **Cancel**.</span></span> 
12. <span data-ttu-id="99de8-161">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="99de8-161">Close the page.</span></span> 
13. <span data-ttu-id="99de8-162">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="99de8-162">Close the page.</span></span> 

## <a name="assign-connected-application-to-model-mapping"></a><span data-ttu-id="99de8-163">将相连应用程序分配给模型映射</span><span class="sxs-lookup"><span data-stu-id="99de8-163">Assign connected application to model mapping</span></span> 
1. <span data-ttu-id="99de8-164">单击**编辑**。</span><span class="sxs-lookup"><span data-stu-id="99de8-164">Click **Edit**.</span></span> 
2. <span data-ttu-id="99de8-165">选择 **MyConnectedApp** 应用程序。</span><span class="sxs-lookup"><span data-stu-id="99de8-165">Select **MyConnectedApp** application.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="99de8-166">目前此映射引用所选相连应用程序的元数据。</span><span class="sxs-lookup"><span data-stu-id="99de8-166">Currently, this mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="99de8-167">当同一个映射同时引用元数据配置和相连应用程序时，将使用相连应用程序的元数据。</span><span class="sxs-lookup"><span data-stu-id="99de8-167">When the same mapping refers to metadata configuration and connected application at the same time, metadata of the connected application will be used.</span></span> 

3. <span data-ttu-id="99de8-168">单击**设计器**。</span><span class="sxs-lookup"><span data-stu-id="99de8-168">Click **Designer**.</span></span> 
4. <span data-ttu-id="99de8-169">单击**设计器**。</span><span class="sxs-lookup"><span data-stu-id="99de8-169">Click **Designer**.</span></span> 
5. <span data-ttu-id="99de8-170">在树中，选择 **Dynamics 365 for Operations\表记录**。</span><span class="sxs-lookup"><span data-stu-id="99de8-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
6. <span data-ttu-id="99de8-171">单击**添加根**。</span><span class="sxs-lookup"><span data-stu-id="99de8-171">Click **Add root**.</span></span> 
7. <span data-ttu-id="99de8-172">在**表格**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="99de8-172">In the **Table** field, enter or select a value.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="99de8-173">现在提供了两个以上的应用程序表，因为此映射使用已经为其分配的相连应用程序的所有元数据。</span><span class="sxs-lookup"><span data-stu-id="99de8-173">More than two application tables were offered now as this mapping uses all the metadata of the connected application that has been assigned for it.</span></span> 

8. <span data-ttu-id="99de8-174">单击**取消**。</span><span class="sxs-lookup"><span data-stu-id="99de8-174">Click **Cancel**.</span></span> 
9. <span data-ttu-id="99de8-175">单击**验证**。</span><span class="sxs-lookup"><span data-stu-id="99de8-175">Click **Validate**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="99de8-176">我们已使用已为此映射分配的相连应用程序的元数据详细信息成功绑定了带有介绍的数据源项的数据模型的元素。</span><span class="sxs-lookup"><span data-stu-id="99de8-176">We successfully bound elements of data model with items of data sources that are described by using details of metadata of the connected application that has been assigned for this mapping.</span></span> 

10. <span data-ttu-id="99de8-177">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="99de8-177">Close the page.</span></span> 
11. <span data-ttu-id="99de8-178">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="99de8-178">Close the page.</span></span> 

<span data-ttu-id="99de8-179">如果需要使用另一个版本应用程序的元数据评估此模型映射，请再注册一个相连应用程序，将其分配给此模型映射，然后使用新元数据再次验证。</span><span class="sxs-lookup"><span data-stu-id="99de8-179">When you need to evaluate this model mapping by using metadata of a different version application, register another connected application, assign it to this model mapping and validate it against new metadata.</span></span>

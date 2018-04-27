---
title: "使用 Power BI Embedded 将分析添加到工作区"
description: "本主题说明如何在工作区的“分析”选项卡上嵌入 Power BI 报表。"
author: tjvass
manager: AnnBe
ms.date: 06/21/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: robinr
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d8cd3a6b3cbfa1219f0ebcf9d4d2132197167220
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---

# <a name="add-analytics-to-workspaces-by-using-power-bi-embedded"></a><span data-ttu-id="8992a-103">使用 Power BI Embedded 将分析添加到工作区</span><span class="sxs-lookup"><span data-stu-id="8992a-103">Add analytics to workspaces by using Power BI Embedded</span></span>

[!INCLUDE [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="8992a-104">此功能在 Dynamics 365 for Finance and Operations（版本 7.2 及更高版本）上受支持。</span><span class="sxs-lookup"><span data-stu-id="8992a-104">This feature is supported in Dynamics 365 for Finance and Operations (version 7.2 and later).</span></span>

## <a name="introduction"></a><span data-ttu-id="8992a-105">简介</span><span class="sxs-lookup"><span data-stu-id="8992a-105">Introduction</span></span>
<span data-ttu-id="8992a-106">本主题说明如何在工作区的**分析**选项卡上嵌入 Microsoft Power BI 报表。</span><span class="sxs-lookup"><span data-stu-id="8992a-106">This topic shows how to embed a Microsoft Power BI report on the **Analytics** tab of a workspace.</span></span> <span data-ttu-id="8992a-107">对于此处提供的示例，我们将“车队管理”应用程序中的**预订管理**工作区扩展到在**分析**选项卡上嵌入分析工作区。</span><span class="sxs-lookup"><span data-stu-id="8992a-107">For the example that is given here, we will extend the **Reservation management** workspace in the Fleet Management application to embed an analytical workspace on an **Analytics** tab.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8992a-108">必备项</span><span class="sxs-lookup"><span data-stu-id="8992a-108">Prerequisites</span></span>
+ <span data-ttu-id="8992a-109">对运行平台更新 8 或更高版本的开发人员环境的访问权限。</span><span class="sxs-lookup"><span data-stu-id="8992a-109">Access to a developer environment that runs Platform update 8 or later.</span></span>
+ <span data-ttu-id="8992a-110">使用 Microsoft Power BI 桌面创建的分析报表（.pbix 文件），且具有从实体商店数据库采购的数据模型。</span><span class="sxs-lookup"><span data-stu-id="8992a-110">An analytical report (.pbix file) that was created by using Microsoft Power BI Desktop, and that has a data model that is sourced from the Entity store database.</span></span>

## <a name="overview"></a><span data-ttu-id="8992a-111">概览</span><span class="sxs-lookup"><span data-stu-id="8992a-111">Overview</span></span>
<span data-ttu-id="8992a-112">无论你是扩展现有的应用程序工作区，还是引入你自己创建新的工作区，都可以使用嵌入的分析视图来提供对你的业务数据的具有见解和交互的视图。</span><span class="sxs-lookup"><span data-stu-id="8992a-112">Whether you extend an existing application workspace or introduce a new workspace of your own, you can use embedded analytical views to deliver insightful and interactive views of your business data.</span></span> <span data-ttu-id="8992a-113">添加分析工作区选项卡的流程具有四个步骤。</span><span class="sxs-lookup"><span data-stu-id="8992a-113">The process for adding an analytical workspace tab has four steps.</span></span>

1. <span data-ttu-id="8992a-114">将 .pbix 文件添加为 Dynamics 365 资源。</span><span class="sxs-lookup"><span data-stu-id="8992a-114">Add a .pbix file as a Dynamics 365 resource.</span></span>
2. <span data-ttu-id="8992a-115">定义分析工作区选项卡。</span><span class="sxs-lookup"><span data-stu-id="8992a-115">Define an analytical workspace tab.</span></span>
3. <span data-ttu-id="8992a-116">在工作区选项卡上嵌入 .pbix 资源。</span><span class="sxs-lookup"><span data-stu-id="8992a-116">Embed the .pbix resource on the workspace tab.</span></span>
4. <span data-ttu-id="8992a-117">可选：添加扩展以自定义视图。</span><span class="sxs-lookup"><span data-stu-id="8992a-117">Optional: Add extensions to customize the view.</span></span>

> [!NOTE]
> <span data-ttu-id="8992a-118">有关如何创建分析报表的详细信息，请参阅 [Power BI 桌面入门](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/)。</span><span class="sxs-lookup"><span data-stu-id="8992a-118">For more information about how to create analytical reports, see [Getting started with Power BI Desktop](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/).</span></span> <span data-ttu-id="8992a-119">此页是提供帮助你创建出色的分析报告解决方案的见解的出色来源。</span><span class="sxs-lookup"><span data-stu-id="8992a-119">This page is a great source for insights that can help you create compelling analytical reporting solutions.</span></span>

## <a name="add-a-pbix-file-as-a-resource"></a><span data-ttu-id="8992a-120">将 .pbix 文件添加为资源。</span><span class="sxs-lookup"><span data-stu-id="8992a-120">Add a .pbix file as a resource</span></span>
<span data-ttu-id="8992a-121">在开始之前，你必须创建或获得在工作区中将嵌入的 Power BI 报表。</span><span class="sxs-lookup"><span data-stu-id="8992a-121">Before you begin, you must create or obtain the Power BI report that you will embed in the workspace.</span></span> <span data-ttu-id="8992a-122">有关如何创建分析报表的详细信息，请参阅 [Power BI 桌面入门](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/)。</span><span class="sxs-lookup"><span data-stu-id="8992a-122">For more information about how to create analytical reports, see [Getting started with Power BI Desktop](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/).</span></span>

<span data-ttu-id="8992a-123">执行以下步骤以将 .pbix 文件添加为 Visual Studio 项目。</span><span class="sxs-lookup"><span data-stu-id="8992a-123">Follow these steps to add a .pbix file as a Visual Studio project artifact.</span></span>

1. <span data-ttu-id="8992a-124">在相应的模型中创建新项目。</span><span class="sxs-lookup"><span data-stu-id="8992a-124">Create a new project in the appropriate model.</span></span>
2. <span data-ttu-id="8992a-125">在“解决方案资源管理器”中，选择项目，右键单击，然后选择**添加** > **新物料**。</span><span class="sxs-lookup"><span data-stu-id="8992a-125">In Solution Explorer, select the project, right-click, and then select **Add** > **New Item**.</span></span>
3. <span data-ttu-id="8992a-126">在**添加新物料**对话框中，在 **Operations 项目**下，选择**资源**模板。</span><span class="sxs-lookup"><span data-stu-id="8992a-126">In the **Add New Item** dialog box, under **Operations Artifacts**, select the **Resource** template.</span></span>
4. <span data-ttu-id="8992a-127">输入将用于在 X++ 元数据中引用报表的名称，然后单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="8992a-127">Enter a name that will be used to reference the report in X++ metadata, and then click **Add**.</span></span>

    ![“添加新物料”对话框](media/analytical-workspace-add.png)

5. <span data-ttu-id="8992a-129">查找包含分析报表的定义的 .pbix 文件，然后单击**打开**。</span><span class="sxs-lookup"><span data-stu-id="8992a-129">Find the .pbix file that contains the definition of the analytical report, and then click **Open**.</span></span>

    ![选择“资源”文件对话框](media/analytical-workspace-select-resource.png)

<span data-ttu-id="8992a-131">既然你已将 .pbix 文件添加为 Dynamics 365 资源，你现在可以在工作区中嵌入报表并使用菜单项添加直接链接。</span><span class="sxs-lookup"><span data-stu-id="8992a-131">Now that you've added the .pbix file as a Dynamics 365 resource, you can embed the reports in workspaces and add direct links by using menu items.</span></span>

## <a name="add-a-tab-control-to-an-application-workspace"></a><span data-ttu-id="8992a-132">将选项卡控件添加到应用程序工作区</span><span class="sxs-lookup"><span data-stu-id="8992a-132">Add a tab control to an application workspace</span></span>
<span data-ttu-id="8992a-133">在此示例中，我们将通过将**分析**选项卡添加到 **FMClerkWorkspace** 窗体的定义中的方式扩展车队管理模型中的**预订管理**工作区。</span><span class="sxs-lookup"><span data-stu-id="8992a-133">In this example, we will extend the **Reservation management** workspace in the Fleet Management model by adding the **Analytics** tab to the definition of the **FMClerkWorkspace** form.</span></span>

<span data-ttu-id="8992a-134">下图显示 **FMClerkWorkspace** 窗体在 Microsoft Visual Studio 中的设计器中的外观。</span><span class="sxs-lookup"><span data-stu-id="8992a-134">The following illustration shows what the **FMClerkWorkspace** form looks like in the designer in Microsoft Visual Studio.</span></span>

![进行更改前的 FMClerkWorkspace 窗体](media/analytical-workspace-definition-before.png)

<span data-ttu-id="8992a-136">执行以下步骤扩展**预订管理**工作区中的窗体定义。</span><span class="sxs-lookup"><span data-stu-id="8992a-136">Follow these steps to extend the form definition for the **Reservation management** workspace.</span></span>

1. <span data-ttu-id="8992a-137">打开设计器窗体以扩展设计定义。</span><span class="sxs-lookup"><span data-stu-id="8992a-137">Open the form designer to extend the design definition.</span></span>
2. <span data-ttu-id="8992a-138">在设计定义中，请选择标记为**设计|模式：工作区运营**的顶部元素。</span><span class="sxs-lookup"><span data-stu-id="8992a-138">In the design definition, select the top element that is labeled **Design | Pattern: Workspace Operational**.</span></span>
3. <span data-ttu-id="8992a-139">右键单击，然后选择**新** > **选项卡**以添加命名为 **FormTabControl1** 的新控件。</span><span class="sxs-lookup"><span data-stu-id="8992a-139">Right-click, and then select **New** > **Tab** to add a new control that is named **FormTabControl1**.</span></span>
4. <span data-ttu-id="8992a-140">在窗体设计器中，选择 **FormTabControl1**。</span><span class="sxs-lookup"><span data-stu-id="8992a-140">In the form designer, select **FormTabControl1**.</span></span>
5. <span data-ttu-id="8992a-141">右键单击，然后选择**新选项卡页**以添加新的选项卡页。</span><span class="sxs-lookup"><span data-stu-id="8992a-141">Right-click, and then select **New Tab Page** to add a new tab page.</span></span>
6. <span data-ttu-id="8992a-142">将选项卡页重命名为有意义的名称，例如**工作区**。</span><span class="sxs-lookup"><span data-stu-id="8992a-142">Rename the tab page to something meaningful, such as **Workspace**.</span></span>
7. <span data-ttu-id="8992a-143">在窗体设计器中，选择 **FormTabControl1**。</span><span class="sxs-lookup"><span data-stu-id="8992a-143">In the form designer, select **FormTabControl1**.</span></span>
8. <span data-ttu-id="8992a-144">右键单击，然后选择**新选项卡页**。</span><span class="sxs-lookup"><span data-stu-id="8992a-144">Right-click, and then select **New Tab Page**.</span></span>
9. <span data-ttu-id="8992a-145">将选项卡页重命名为有意义的名称，例如**分析**。</span><span class="sxs-lookup"><span data-stu-id="8992a-145">Rename the tab page to something meaningful, such as **Analytics**.</span></span>
10. <span data-ttu-id="8992a-146">在窗体设计器，选择**分析（选项卡页）**。</span><span class="sxs-lookup"><span data-stu-id="8992a-146">In the form designer, select **Analytics (Tab Page)**.</span></span>
11. <span data-ttu-id="8992a-147">将**标题**属性设置为**分析**。</span><span class="sxs-lookup"><span data-stu-id="8992a-147">Set the **Caption** property to **Analytics**.</span></span>
12. <span data-ttu-id="8992a-148">右键单击控件，然后选择**新** > **组**以添加新的窗体组控件。</span><span class="sxs-lookup"><span data-stu-id="8992a-148">Right-click the control, and then select **New** > **Group** to add a new form group control.</span></span>
13. <span data-ttu-id="8992a-149">将窗体组重命名为有意义的名称，例如 **powerBIReportGroup**。</span><span class="sxs-lookup"><span data-stu-id="8992a-149">Rename the form group to something meaningful, such as **powerBIReportGroup**.</span></span>
14. <span data-ttu-id="8992a-150">在窗体设计器中，选择 **PanoramaBody（选项卡）**，然后将控件拖动到**工作区**选项卡上。</span><span class="sxs-lookup"><span data-stu-id="8992a-150">In the form designer, select **PanoramaBody (Tab)**, and then drag the control onto the **Workspace** tab.</span></span>
15. <span data-ttu-id="8992a-151">在设计定义中，请选择标记为**设计|模式：工作区运营**的顶部元素。</span><span class="sxs-lookup"><span data-stu-id="8992a-151">In the design definition, select the top element that is labeled **Design | Pattern: Workspace Operational**.</span></span>
16. <span data-ttu-id="8992a-152">右键单击，然后选择**删除模式**。</span><span class="sxs-lookup"><span data-stu-id="8992a-152">Right-click, and then select **Remove pattern**.</span></span>
17. <span data-ttu-id="8992a-153">再次右键单击，然后选择**添加模式** > **工作区选项卡式**。</span><span class="sxs-lookup"><span data-stu-id="8992a-153">Right-click again, and then select **Add pattern** > **Workspace Tabbed**.</span></span>
18. <span data-ttu-id="8992a-154">执行内部版本以验证你的更改。</span><span class="sxs-lookup"><span data-stu-id="8992a-154">Perform a build to verify your changes.</span></span>

<span data-ttu-id="8992a-155">下图显示设计在应用这些更改后的外观。</span><span class="sxs-lookup"><span data-stu-id="8992a-155">The following illustration shows what the design looks like after these changes are applied.</span></span>

![进行更改后的 FMClerkWorkspace](media/analytical-workspace-definition-after.png)

<span data-ttu-id="8992a-157">既然你已添加了将用于嵌入工作区报表的窗体控件，你现在必须定义父控件的大小，使之适应布局。</span><span class="sxs-lookup"><span data-stu-id="8992a-157">Now that you've added the form controls that will be used to embed the workspace report, you must define the size of the parent control so that it accommodates the layout.</span></span> <span data-ttu-id="8992a-158">默认情况下，**筛选器窗格**页和**选项卡**页将在报表上显示。</span><span class="sxs-lookup"><span data-stu-id="8992a-158">By default, both the **Filters Pane** page and the **Tab** page will be visible on the report.</span></span> <span data-ttu-id="8992a-159">但是，你可以根据报表的目标使用者相应地更改这些控件的可见性。</span><span class="sxs-lookup"><span data-stu-id="8992a-159">However, you can change the visibility of these controls as appropriate for the target consumer of the report.</span></span>

> [!NOTE]
> <span data-ttu-id="8992a-160">对于嵌入的工作区，为了获得一致性，我们建议你使用扩展以同时隐藏**筛选器窗格**和**选项卡**页。</span><span class="sxs-lookup"><span data-stu-id="8992a-160">For embedded workspaces, we recommend that you use extensions to hide both the **Filters Pane** and **Tab** pages, for consistency.</span></span>

<span data-ttu-id="8992a-161">你现在已完成了扩展应用程序窗体定义的任务。</span><span class="sxs-lookup"><span data-stu-id="8992a-161">You've now completed the task of extending the application form definition.</span></span> <span data-ttu-id="8992a-162">有关如何使用扩展执行自定义的详细信息，请参阅[自定义：覆盖和扩展](../extensibility/customization-overlayering-extensions.md)。</span><span class="sxs-lookup"><span data-stu-id="8992a-162">For more information about how to use extensions to do customizations, see  [Customization: Overlayering and extensions](../extensibility/customization-overlayering-extensions.md).</span></span>

## <a name="add-x-business-logic-to-embed-a-viewer-control"></a><span data-ttu-id="8992a-163">添加 X++ 业务逻辑以嵌入查看器控件</span><span class="sxs-lookup"><span data-stu-id="8992a-163">Add X++ business logic to embed a viewer control</span></span>
<span data-ttu-id="8992a-164">按照下面的步骤添加初始化在**预订管理**工作区中嵌入的报表查看器控件的业务逻辑。</span><span class="sxs-lookup"><span data-stu-id="8992a-164">Follow these steps to add business logic that initializes the report viewer control that is embedded in the **Reservation management** workspace.</span></span>

1. <span data-ttu-id="8992a-165">打开 **FMClerkWorkspace** 窗体设计器以扩展设计定义。</span><span class="sxs-lookup"><span data-stu-id="8992a-165">Open the **FMClerkWorkspace** form designer to extend the design definition.</span></span>
2. <span data-ttu-id="8992a-166">按 F7 访问代码定义后的代码。</span><span class="sxs-lookup"><span data-stu-id="8992a-166">Press F7 to access the code behind the code definition.</span></span>
3. <span data-ttu-id="8992a-167">添加以下 X++ 代码。</span><span class="sxs-lookup"><span data-stu-id="8992a-167">Add the following X++ code.</span></span>

    ```
    [Form] 
    public class FMClerkWorkspace extends FormRun
    {
        private boolean initReportControl = true;     
        protected void initAnalyticalReport()
        {
            if (!initReportControl)
            {
                return;
            }
            // Note: secure entry point into the Workspace's Analytics report
            if (Global::hasMenuItemAccess(menuItemDisplayStr(FMClerkWorkspace), MenuItemType::Display))
            {
                FMPBIWorkspaceController controller = new FMPBIWorkspaceController();
                PBIReportHelper::initializeReportControl('FMPBIWorkspaces', powerBIReportGroup);
            }
            initReportControl = false;
    }
        /// <summary>
        /// Initializes the form.
        /// </summary>
        public void init()
        {
            super();
            this.initAnalyticalReport();
        }
    }
    ```

4. <span data-ttu-id="8992a-168">执行内部版本以验证你的更改。</span><span class="sxs-lookup"><span data-stu-id="8992a-168">Perform a build to verify your changes.</span></span>

<span data-ttu-id="8992a-169">现在你已完成添加业务逻辑以初始化嵌入的报表查看器控件的任务。</span><span class="sxs-lookup"><span data-stu-id="8992a-169">You've now completed the task of adding business logic to initialize the embedded report viewer control.</span></span> <span data-ttu-id="8992a-170">下图显示工作区在应用这些更改后的外观。</span><span class="sxs-lookup"><span data-stu-id="8992a-170">The following illustration shows what the workspace looks like after these changes are applied.</span></span>

![在工作区嵌入的报表](media/analytical-workspace-final.png)

> [!NOTE]
> <span data-ttu-id="8992a-172">你可以使用页标题下方的工作区选项卡访问现有的操作视图。</span><span class="sxs-lookup"><span data-stu-id="8992a-172">You can access the existing operational view by using the workspace tabs below the page title.</span></span>

## <a name="reference"></a><span data-ttu-id="8992a-173">参考</span><span class="sxs-lookup"><span data-stu-id="8992a-173">Reference</span></span>

### <a name="pbireporthelperinitializereportcontrol-method"></a><span data-ttu-id="8992a-174">PBIReportHelper.initializeReportControl 方法</span><span class="sxs-lookup"><span data-stu-id="8992a-174">PBIReportHelper.initializeReportControl method</span></span>
<span data-ttu-id="8992a-175">本节提供有关用于在窗体组控件中嵌入 Power BI 报表（.pbix 资源）的帮助程序类的信息。</span><span class="sxs-lookup"><span data-stu-id="8992a-175">This section provides information about the helper class that is used to embed a Power BI report (.pbix resource) in a form group control.</span></span>

#### <a name="syntax"></a><span data-ttu-id="8992a-176">语法</span><span class="sxs-lookup"><span data-stu-id="8992a-176">Syntax</span></span>
```
public static void initializeReportControl(
     str                 _resourceName,
     FormGroupControl    _formGroupControl,
     str                 _defaultPageName = '',
     boolean             _showFilterPane = false,
     boolean             _showNavPane = false,
     List                _defaultFilters = new List(Types::Class))
```

#### <a name="parameters"></a><span data-ttu-id="8992a-177">参数设置</span><span class="sxs-lookup"><span data-stu-id="8992a-177">Parameters</span></span>

|       <span data-ttu-id="8992a-178">姓名</span><span class="sxs-lookup"><span data-stu-id="8992a-178">Name</span></span>       |                                                              <span data-ttu-id="8992a-179">说明</span><span class="sxs-lookup"><span data-stu-id="8992a-179">Description</span></span>                                                               |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="8992a-180">resourceName</span><span class="sxs-lookup"><span data-stu-id="8992a-180">resourceName</span></span>   |                                                    <span data-ttu-id="8992a-181">.pbix 资源的名称。</span><span class="sxs-lookup"><span data-stu-id="8992a-181">The name of the .pbix resource.</span></span>                                                     |
| <span data-ttu-id="8992a-182">formGroupControl</span><span class="sxs-lookup"><span data-stu-id="8992a-182">formGroupControl</span></span> |                                    <span data-ttu-id="8992a-183">要应用 Power BI 报表控件的窗体组控件。</span><span class="sxs-lookup"><span data-stu-id="8992a-183">The form group control to apply the Power BI report control to.</span></span>                                     |
| <span data-ttu-id="8992a-184">defaultPageName</span><span class="sxs-lookup"><span data-stu-id="8992a-184">defaultPageName</span></span>  |                                                         <span data-ttu-id="8992a-185">默认页名称。</span><span class="sxs-lookup"><span data-stu-id="8992a-185">The default page name.</span></span>                                                         |
|  <span data-ttu-id="8992a-186">showFilterPane</span><span class="sxs-lookup"><span data-stu-id="8992a-186">showFilterPane</span></span>  |   <span data-ttu-id="8992a-187">指示是否应显示 (<strong>true</strong>) 或隐藏 (<strong>false</strong>) 筛选器窗格的布尔值。</span><span class="sxs-lookup"><span data-stu-id="8992a-187">A Boolean value that indicates whether the filter pane should be shown (<strong>true</strong>) or hidden (<strong>false</strong>).</span></span>   |
|   <span data-ttu-id="8992a-188">showNavPane</span><span class="sxs-lookup"><span data-stu-id="8992a-188">showNavPane</span></span>    | <span data-ttu-id="8992a-189">指示是否应显示 (<strong>true</strong>) 或隐藏 (<strong>false</strong>) 导航窗格的布尔值。</span><span class="sxs-lookup"><span data-stu-id="8992a-189">A Boolean value that indicates whether the navigation pane should be shown (<strong>true</strong>) or hidden (<strong>false</strong>).</span></span> |
|  <span data-ttu-id="8992a-190">defaultFilters</span><span class="sxs-lookup"><span data-stu-id="8992a-190">defaultFilters</span></span>  |                                              <span data-ttu-id="8992a-191">Power BI 报表的默认筛选器。</span><span class="sxs-lookup"><span data-stu-id="8992a-191">The default filters for the Power BI report.</span></span>                                              |



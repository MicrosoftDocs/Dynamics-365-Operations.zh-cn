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

# <a name="add-analytics-to-workspaces-by-using-power-bi-embedded"></a>使用 Power BI Embedded 将分析添加到工作区

[!INCLUDE [banner](../includes/banner.md)]

> [!NOTE]
> 此功能在 Dynamics 365 for Finance and Operations（版本 7.2 及更高版本）上受支持。

## <a name="introduction"></a>简介
本主题说明如何在工作区的**分析**选项卡上嵌入 Microsoft Power BI 报表。 对于此处提供的示例，我们将“车队管理”应用程序中的**预订管理**工作区扩展到在**分析**选项卡上嵌入分析工作区。

## <a name="prerequisites"></a>必备项
+ 对运行平台更新 8 或更高版本的开发人员环境的访问权限。
+ 使用 Microsoft Power BI 桌面创建的分析报表（.pbix 文件），且具有从实体商店数据库采购的数据模型。

## <a name="overview"></a>概览
无论你是扩展现有的应用程序工作区，还是引入你自己创建新的工作区，都可以使用嵌入的分析视图来提供对你的业务数据的具有见解和交互的视图。 添加分析工作区选项卡的流程具有四个步骤。

1. 将 .pbix 文件添加为 Dynamics 365 资源。
2. 定义分析工作区选项卡。
3. 在工作区选项卡上嵌入 .pbix 资源。
4. 可选：添加扩展以自定义视图。

> [!NOTE]
> 有关如何创建分析报表的详细信息，请参阅 [Power BI 桌面入门](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/)。 此页是提供帮助你创建出色的分析报告解决方案的见解的出色来源。

## <a name="add-a-pbix-file-as-a-resource"></a>将 .pbix 文件添加为资源。
在开始之前，你必须创建或获得在工作区中将嵌入的 Power BI 报表。 有关如何创建分析报表的详细信息，请参阅 [Power BI 桌面入门](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/)。

执行以下步骤以将 .pbix 文件添加为 Visual Studio 项目。

1. 在相应的模型中创建新项目。
2. 在“解决方案资源管理器”中，选择项目，右键单击，然后选择**添加** > **新物料**。
3. 在**添加新物料**对话框中，在 **Operations 项目**下，选择**资源**模板。
4. 输入将用于在 X++ 元数据中引用报表的名称，然后单击**添加**。

    ![“添加新物料”对话框](media/analytical-workspace-add.png)

5. 查找包含分析报表的定义的 .pbix 文件，然后单击**打开**。

    ![选择“资源”文件对话框](media/analytical-workspace-select-resource.png)

既然你已将 .pbix 文件添加为 Dynamics 365 资源，你现在可以在工作区中嵌入报表并使用菜单项添加直接链接。

## <a name="add-a-tab-control-to-an-application-workspace"></a>将选项卡控件添加到应用程序工作区
在此示例中，我们将通过将**分析**选项卡添加到 **FMClerkWorkspace** 窗体的定义中的方式扩展车队管理模型中的**预订管理**工作区。

下图显示 **FMClerkWorkspace** 窗体在 Microsoft Visual Studio 中的设计器中的外观。

![进行更改前的 FMClerkWorkspace 窗体](media/analytical-workspace-definition-before.png)

执行以下步骤扩展**预订管理**工作区中的窗体定义。

1. 打开设计器窗体以扩展设计定义。
2. 在设计定义中，请选择标记为**设计|模式：工作区运营**的顶部元素。
3. 右键单击，然后选择**新** > **选项卡**以添加命名为 **FormTabControl1** 的新控件。
4. 在窗体设计器中，选择 **FormTabControl1**。
5. 右键单击，然后选择**新选项卡页**以添加新的选项卡页。
6. 将选项卡页重命名为有意义的名称，例如**工作区**。
7. 在窗体设计器中，选择 **FormTabControl1**。
8. 右键单击，然后选择**新选项卡页**。
9. 将选项卡页重命名为有意义的名称，例如**分析**。
10. 在窗体设计器，选择**分析（选项卡页）**。
11. 将**标题**属性设置为**分析**。
12. 右键单击控件，然后选择**新** > **组**以添加新的窗体组控件。
13. 将窗体组重命名为有意义的名称，例如 **powerBIReportGroup**。
14. 在窗体设计器中，选择 **PanoramaBody（选项卡）**，然后将控件拖动到**工作区**选项卡上。
15. 在设计定义中，请选择标记为**设计|模式：工作区运营**的顶部元素。
16. 右键单击，然后选择**删除模式**。
17. 再次右键单击，然后选择**添加模式** > **工作区选项卡式**。
18. 执行内部版本以验证你的更改。

下图显示设计在应用这些更改后的外观。

![进行更改后的 FMClerkWorkspace](media/analytical-workspace-definition-after.png)

既然你已添加了将用于嵌入工作区报表的窗体控件，你现在必须定义父控件的大小，使之适应布局。 默认情况下，**筛选器窗格**页和**选项卡**页将在报表上显示。 但是，你可以根据报表的目标使用者相应地更改这些控件的可见性。

> [!NOTE]
> 对于嵌入的工作区，为了获得一致性，我们建议你使用扩展以同时隐藏**筛选器窗格**和**选项卡**页。

你现在已完成了扩展应用程序窗体定义的任务。 有关如何使用扩展执行自定义的详细信息，请参阅[自定义：覆盖和扩展](../extensibility/customization-overlayering-extensions.md)。

## <a name="add-x-business-logic-to-embed-a-viewer-control"></a>添加 X++ 业务逻辑以嵌入查看器控件
按照下面的步骤添加初始化在**预订管理**工作区中嵌入的报表查看器控件的业务逻辑。

1. 打开 **FMClerkWorkspace** 窗体设计器以扩展设计定义。
2. 按 F7 访问代码定义后的代码。
3. 添加以下 X++ 代码。

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

4. 执行内部版本以验证你的更改。

现在你已完成添加业务逻辑以初始化嵌入的报表查看器控件的任务。 下图显示工作区在应用这些更改后的外观。

![在工作区嵌入的报表](media/analytical-workspace-final.png)

> [!NOTE]
> 你可以使用页标题下方的工作区选项卡访问现有的操作视图。

## <a name="reference"></a>参考

### <a name="pbireporthelperinitializereportcontrol-method"></a>PBIReportHelper.initializeReportControl 方法
本节提供有关用于在窗体组控件中嵌入 Power BI 报表（.pbix 资源）的帮助程序类的信息。

#### <a name="syntax"></a>语法
```
public static void initializeReportControl(
     str                 _resourceName,
     FormGroupControl    _formGroupControl,
     str                 _defaultPageName = '',
     boolean             _showFilterPane = false,
     boolean             _showNavPane = false,
     List                _defaultFilters = new List(Types::Class))
```

#### <a name="parameters"></a>参数设置

|       姓名       |                                                              说明                                                               |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------|
|   resourceName   |                                                    .pbix 资源的名称。                                                     |
| formGroupControl |                                    要应用 Power BI 报表控件的窗体组控件。                                     |
| defaultPageName  |                                                         默认页名称。                                                         |
|  showFilterPane  |   指示是否应显示 (<strong>true</strong>) 或隐藏 (<strong>false</strong>) 筛选器窗格的布尔值。   |
|   showNavPane    | 指示是否应显示 (<strong>true</strong>) 或隐藏 (<strong>false</strong>) 导航窗格的布尔值。 |
|  defaultFilters  |                                              Power BI 报表的默认筛选器。                                              |



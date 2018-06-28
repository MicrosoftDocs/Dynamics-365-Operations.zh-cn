---
title: "嵌入 PowerApps"
description: "此主题描述如何将 PowerApps 嵌入到 Finance and Operations 客户端以细分该产品的功能。"
author: jasongre
manager: AnnBe
ms.date: 06/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 07224faabcf2b183d4c8da0ba4588c33ec140d03
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---

# <a name="embed-powerapps"></a>嵌入 PowerApps

[!include [banner](../includes/banner.md)]

在平台更新 14 中，Microsoft Dynamics 365 for Finance and Operations 支持与 Microsoft PowerApps 集成，这是一项面向为移动设备、平板电脑和 Web 构建自定义企业应用、而无需编写代码的开发人员和非技术用户的服务。 由您、您的组织或者更广泛的生态系统开发的 PowerApps 反之可以嵌入到 Finance and Operations 客户端以细分产品的功能。 例如，您可以构建 PowerApp 来使用从其他系统检索的信息补充 Finance and Operations。 

若要了解有关嵌入 PowerApp 的详细信息，请观看视频短片[如何在 Dynamics 365 for Finance and Operations 中嵌入 PowerApp](https://www.youtube.com/watch?v=x3qyA1bH-NY)。

## <a name="adding-an-embedded-powerapp-to-a-page"></a>将嵌入的 PowerApp 添加到页面
### <a name="overview"></a>概览
在将 PowerApp 嵌入到 Finance and Operations 客户端之前，您首先需要使用所需的视觉对象和/或功能找到或构建 PowerApp。 我们在这里不介绍构建 PowerApp 的详细流程。 如果您是 PowerApps 的新用户，[PowerApps 简介](https://docs.microsoft.com/en-us/powerapps/getting-started)主题是一个好的起始点。

当您准备嵌入特定 PowerApp 时，您可以选择以下两种方式之一在页面上访问 PowerApp，选择更适合您的场景的路线。 第一种方法是通过已添加到标准操作窗格的 PowerApps 按钮。 使用此机制添加的 PowerApps 在 PowerApps 菜单按钮内将显示为菜单项。 一旦选中，这些菜单项中的每一项都将打开包含嵌入的 PowerApp 的侧窗格。 或者，您可以选择直接在页面上将 PowerApp 显示为新选项卡、快速选项卡、边栏选项卡，或者显示为工作区的新部分。 

在 Finance and Operations 中配置嵌入的 PowerApp 时，您可以选择您希望将其作为输入发送到 PowerApp 的单个字段。 这允许 PowerApp 基于您在 Finance and Operations 中正在查看的数据作出响应。  

### <a name="details"></a>明细
以下说明显示如何将 PowerApp 嵌入到 Finance and Operations Web 客户端。  

1. 转到您希望嵌入 PowerApp 的页面。 这与包含需要作为输入传送到 PowerApp 的任何数据的页面是同一页。  
2. 打开**插入 PowerApp** 窗格：
   - 单击**选项**，然后选择**个性化设置此窗体**。 在**插入**菜单下，选择 **PowerApp**。 最后，选择要添加 PowerApp 的区域。 如果要在 PowerApp 菜单按钮下嵌入 PowerApps，选择操作窗格。 如果要将 PowerApp 直接嵌入到页面上，选择相应的选项卡、快速选项卡、边栏选项卡或部分（如果您处于工作区）。   
   - 如果将使用 PowerApps 菜单按钮访问 PowerApp，您可以单击标准操作窗格中的 **PowerApps** 菜单按钮，然后选择**插入 PowerApp**。  
3. 配置嵌入的 PowerApp：
   - **名称**字段指示为要包含嵌入的 PowerApp 的按钮或选项卡显示的文本。 通常，您可能要在此字段中重复 PowerApp 的名称。  
   - **应用 ID** 是您要嵌入的 PowerApp 的 GUID。 若要检索此值，在 [web.powerapps.com](https://web.powerapps.com) 上找到 PowerApp，然后在**详细信息**下找到**应用 ID** 字段。  
   - 对于 **PowerApp 的输入数据**，您可以有选择性地选择包含您要作为输入传送到 PowerApp 的数据的字段。 请参阅本主题后面名为[构建利用 Finance and Operations 的数据的 PowerApp](#building-a-powerapp-that-leverages-data-sent-from-finance-and-operations) 部分，了解有关 PowerApp 如何访问发送自 Finance and Operations 的数据的详细信息。  
   - 选择与您嵌入的 PowerApp 类型匹配的**应用程序大小**。 为针对移动设备构建的 PowerApps 选择**窄**，为平板电脑构建的 PowerApps 选择**宽**。 这将确保为嵌入的 PowerApp 分配足够的空间量。
   - **法人**快速选项卡提供选择 PowerApp 可用于哪些法人的功能。 默认显示所有法人中的 PowerApp。  
4. 在确认配置正确后，请单击**插入**在页面上嵌入 PowerApp。 系统将提示您刷新浏览器以查看嵌入的 PowerApp。 

## <a name="sharing-an-embedded-powerapp"></a>共享嵌入的 PowerApp
在页面上嵌入 PowerApp 并确认它能够正确处理从页面传递的所有数据上下文后，您可能希望与系统中的其他用户共享此嵌入的 PowerApp。 可使用本产品的个性化功能以两种不同的方法达到此目的：

- 建议的方案是通过系统管理员，因为系统管理员可以将个性化设置推送给所有用户或一小部分用户。 

- 也可以导出页面的个性化设置，将其发送给一位或多位用户，然后请这些用户分别导入那些更改。 可使用个性化工具栏上的管理选项导出和导入个性化设置。

有关产品中的个性化功能以及如何使用的更多详细信息，请参阅[打造个性化的用户体验](personalize-user-experience.md)。

## <a name="building-a-powerapp-that-leverages-data-sent-from-finance-and-operations"></a>构建利用发送自 Finance and Operations 的数据的 PowerApp
构建将嵌入到 Finance and Operations 的 PowerApp 的一个重要部分是使用 Finance and Operations 的输入数据。 在 PowerApp 内，该输入数据可以使用 Param("EntityId") 变量访问。  

例如，在 PowerApp 的 OnStart 功能中，可以将 Finance and Operations 的输入数据设置为类似这样的一个变量：

If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, "")); 

## <a name="viewing-an-embedded-powerapp"></a>查看嵌入的 PowerApp
若要查看 Finance and Operations 中页面上的嵌入 PowerApp，只需转到包含嵌入的 PowerApp 的页面。 回忆一下，PowerApps 可以通过标准操作窗格的 PowerApps 按钮访问，或可以在页面上直接显示为新的选项卡、快速选项卡，或在工作区显示为新部分。 当用户首次尝试在页面上加载 PowerApp 时，系统将提示他或她登录到 PowerApps 以确保用户有使用 PowerApp 的相应权限。   

## <a name="editing-an-embedded-powerapp"></a>编辑嵌入的 PowerApp
在 PowerApp 嵌入到页面后，可能需要对该 PowerApp 的配置作一些更改。 例如，可能您要修改与嵌入的 PowerApp 或创建的新版本 PowerApp 关联的标签，并且您需要更新应用 ID 以指示最新的 PowerApp。 

执行以下步骤来编辑嵌入的 PowerApp 的配置：
1. 转到**编辑 PowerApp** 窗格。 
   - 如果嵌入的 PowerApp 通过 PowerApps 菜单按钮访问，右键单击 PowerApps 菜单按钮并选择**个性化**。 选择您想要从**选择 PowerApp** 下拉菜单配置的 PowerApp。  
   - 如果嵌入的 PowerApp 直接出现在页面上，选择**选项**，然后选择**个性化设置此窗体**。 使用**选择**工具，单击嵌入的 PowerApp。  
2. 对 PowerApps 配置进行需要的修改，然后单击**保存**。  

## <a name="removing-an-embedded-powerapp"></a>删除嵌入的 PowerApp
在 PowerApp 嵌入到页面上后，如果需要，有两种方法可以删除它： 

- 使用此主题前面[编辑嵌入的 PowerApp](#editing-an-embedded-powerapp) 部分的说明转到**编辑 PowerApp** 窗格。 确认窗格显示您要删除的嵌入 PowerApp 的信息，然后单击**删除**按钮。 

- 由于嵌入的 PowerApp 保存为个性化数据，清除页面的个性化也将删除该页面上所有嵌入的 PowerApps。 请注意，清除页面的个性化是永久的，并且无法撤消。 若要删除您的页面上的个性化设置，选择**选项**，然后单击**个性化设置此窗体**。 在**管理**菜单下，选择**清除**按钮。 刷新您的浏览器后，将删除此页之前的所有个性化设置。 请参阅[打造个性化的用户体验](personalize-user-experience.md)了解有关如何使用个性化设置优化页面的更多信息。  

## <a name="appendix"></a>附录 
### <a name="developer-control-over-where-a-powerapp-can-be-embedded"></a>开发人员控制 PowerApp 可以嵌入的位置
默认情况下，用户可以在任何页面嵌入 PowerApps，在 PowerApps 菜单按钮下，或直接在页面上作为选项卡、快速选项卡、边栏选项卡，或作为工作区的新部分。 但是，如果需要，开发人员还可以将此功能配置为只允许在特定页面上嵌入 PowerApps，方法如下： 

- **isPowerAppPersonalizationEnabled** - 如果此方法为特定页面返回 false，那么 PowerApps 菜单按钮不显示，并且用户不能将 PowerApps 嵌入到此页的任何位置，包括作为选项卡。 

- **isPowerAppTabPersonalizationEnabled** - 如果此方法为特定页返回 false，那么用户不能直接在页面上作为选项卡、快速选项卡或全景部分嵌入 PowerApps。 如果允许在页面上嵌入，用户仍可以通过 PowerApps 菜单按钮嵌入 PowerApps。  

以下示例显示需要通过这两种方法来配置 PowerApps 可以嵌入的位置的新类。  

```
[ExtensionOf(classStr(FormRunConfigurationPowerAppsConfiguration))]

public final class ClassTest_Extension
{

    public static boolean isPowerAppPresonalizationEnabled(str pageName)
    {
        var result = next isPowerAppPresonalizationEnabled(pageName);
        return true;
    }

    public static boolean isPowerAppTabPresonalizationEnabled(str pageName)   
    {
        var result = next isPowerAppTabPresonalizationEnabled(pageName);
        return true;
    }
    ```

}



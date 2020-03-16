---
title: 嵌入 Power Apps
description: 此主题描述如何将 Power Apps 嵌入到客户端以细分该产品的功能。
author: jasongre
manager: AnnBe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: 90422a34499dab7302ad7722cf84d40e1815991c
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042934"
---
# <a name="embed-microsoft-power-apps"></a>嵌入 Microsoft Power Apps

[!include [banner](../includes/banner.md)]

Finance and Operations 支持与 Microsoft Power Apps 集成，这项服务供开发人员和非技术用户为移动设备、平板电脑和 Web 构建自定义企业应用，而无需编写代码。 以生，由您、您的组织或者更广泛的生态系统开发的 Power Apps 可以嵌入到 Finance and Operations 应用程序以细分产品的功能。 例如，您可以利用 Power Apps 构建应用以使用从其他系统检索的信息补充 Finance and Operations 应用。

若要了解有关嵌入 Power Apps 的详细信息，请观看视频短片[如何嵌入 Power Apps](https://www.youtube.com/watch?v=x3qyA1bH-NY)。

## <a name="adding-an-embedded-app-from-power-apps-to-a-page"></a>将 Power Apps 中的嵌入应用添加到页面中

### <a name="overview"></a>概览

在将 Power Apps 中的应用嵌入到客户端之前，您首先需要使用所需的视觉对象和/或功能找到或构建应用。 我们在这里将不介绍构建应用的详细流程。 如果您是 Power Apps 的新用户，[Power Apps 简介](https://docs.microsoft.com/powerapps/getting-started)主题是一个好的起始点。

当您准备嵌入特定应用时，您可以选择以下两种方式之一在页面上访问应用，选择更适合您的场景的路线。 第一种方法是通过已添加到标准操作窗格的 Power Apps 按钮。 使用此机制添加的应用在 Power Apps 菜单按钮内将显示为菜单项。 一旦选中，这些菜单项中的每一项都将打开包含嵌入的应用的侧窗格。 或者，您可以选择直接在页面上将应用嵌入为新选项卡、快速选项卡、边栏选项卡，或者显示为工作区的新部分。

配置嵌入的应用时，您可以选择您希望将其作为上下文发送到应用的单个字段。 这允许应用基于您正在查看的数据作出响应。

### <a name="details"></a>明细

以下说明显示如何将 Power Apps 中的应用嵌入到 Web 客户端。

1. 转到您希望嵌入应用的页面。 这与包含需要作为输入传送到应用的任何数据的页面是同一页。
2. 打开**从 Power Apps 中添加应用**窗格：

    - 单击**选项**，然后选择**个性化设置此页面**。 在**插入**菜单下，选择 **Power Apps**。 最后，选择要添加应用的区域。 如果要在 Power Apps 菜单按钮下嵌入应用，选择操作窗格。 如果要将应用直接嵌入到页面上，选择相应的选项卡、快速选项卡、边栏选项卡或部分（如果您处于工作区）。
    - 如果将使用 Power Apps 菜单按钮访问应用，您可以单击标准操作窗格中的 **Power Apps** 菜单按钮，然后选择**添加应用**。

3. 配置嵌入的应用：

    - **名称**字段指示为将包含嵌入的应用的按钮或选项卡显示的文本。 通常，您可能要在此字段中重复应用的名称。
    - **应用 ID** 是您要嵌入的应用的 GUID。 若要检索此值，在 [web.powerapps.com](https://web.powerapps.com) 上找到应用，然后在**详细信息**下找到**应用 ID** 字段。
    - 对于**应用的输入上下文**，您可以有选择性地选择包含您要作为输入传送到应用的数据的字段。 请参阅本主题后面名为[构建利用从 Finance and Operations 应用发送的数据的应用](#building-an-app-that-leverages-data-sent-from-finance-and-operations-apps)部分，了解有关应用如何访问发送自 Finance and Operations 应用的数据的详细信息。
    - 选择与您嵌入的应用类型匹配的**应用程序大小**。 为针对移动设备构建的应用选择**窄**，为平板电脑构建的应用选择**宽**。 这将确保为嵌入的应用分配足够的空间量。
    - **法人**快速选项卡提供选择应用可用于哪些法人的功能。 默认让所有法人都能访问应用。 此选项仅在[保存的视图](saved-views.md)功能已禁用时才可用。 

4. 在确认配置正确后，请单击**插入**在页面上嵌入 Power App。 系统将提示您刷新浏览器以查看嵌入的应用。

## <a name="sharing-an-embedded-app"></a>共享嵌入的应用

在页面上嵌入应用并确认它能够正确处理从页面传递的所有数据上下文后，您可能希望与系统中的其他用户共享此应用。 可使用本产品的个性化功能以两种不同的方法达到此目的：

- 建议的方案是通过系统管理员，因为系统管理员可以将个性化设置推送给所有用户或一小部分用户。
- 也可以导出页面的个性化设置，将其发送给一位或多位用户，然后请这些用户分别导入那些更改。 个性化工具栏具有允许您导出和导入个性化的操作。

有关产品中的个性化功能以及如何使用的更多详细信息，请参阅[打造个性化的用户体验](personalize-user-experience.md)。

## <a name="building-an-app-that-leverages-data-sent-from-finance-and-operations-apps"></a>构建一个利用从 Finance and Operations 应用中发送的数据的应用

从将嵌入到 Finance and Operations 应用中的 Power Apps 中构建应用的重要部分将使用该应用程序中的输入数据。 根据 Power Apps 开发经验，可以使用 Param("EntityId") 变量访问从 Finance and Operations 应用传递的输入数据。

例如，在应用的 OnStart 功能中，可以将 Finance and Operations 应用的输入数据设置为类似这样的一个变量：

```powerapps
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-app"></a>查看应用

若要查看 Finance and Operations 应用中页面上的嵌入应用，只需转到包含嵌入的应用的页面。 回忆一下，应用可以通过标准操作窗格的 Power Apps 按钮访问，或可以在页面上直接显示为新的选项卡、快速选项卡，或在工作区显示为新部分。 当用户首次尝试在页面上加载应用时，系统将提示他或她登录到以确保用户有使用应用的相应权限。

## <a name="editing-an-embedded-app"></a>编辑嵌入的应用

在应用嵌入到页面后，可能需要对该应用的配置作一些更改。 例如，可能您要修改与嵌入的应用关联的标签，或者已创建新版本应用并且您需要更新应用 ID 以指向最新应用。

执行以下步骤来编辑嵌入的应用的配置：

1. 转到**编辑应用**窗格。

    - 如果嵌入的应用通过 Power Apps 菜单按钮访问，右键单击 Power Apps 菜单按钮并选择**个性化**。 选择您想要从**选择应用**下拉菜单配置的应用。
    - 如果嵌入的应用直接出现在页面上，选择**选项**，然后选择**个性化设置此页面**。 使用**选择**工具，单击嵌入的应用。

2. 对应用配置进行需要的修改，然后单击**保存**。

## <a name="removing-an-app"></a>移除应用

在应用嵌入到页面上后，如果需要，有两种方法可以删除它：

- 使用此主题前面[编辑嵌入的应用](#editing-an-embedded-app)部分中的说明转到**编辑应用**窗格。 确认窗格显示您要删除的嵌入应用的信息，然后单击**删除**按钮。
- 由于嵌入的应用保存为个性化数据，清除页面的个性化也将删除该页面上所有嵌入的应用。 请注意，清除页面的个性化是永久的，并且无法撤消。 若要删除您的页面上的个性化设置，依次选择**选项**、**个性化设置此页面**和**清除**。 刷新您的浏览器后，将删除此页之前的所有个性化设置。 请参阅[打造个性化的用户体验](personalize-user-experience.md)了解有关如何使用个性化设置优化页面的更多信息。

## <a name="appendix"></a>附录

### <a name="developer-control-over-where-an-app-can-be-embedded"></a>开发人员控制应用可以嵌入的位置

默认情况下，用户可以在任何页面嵌入应用，要么嵌入在 Power Apps 菜单按钮下，要么作为选项卡、快速选项卡、边栏选项卡或工作区新部分直接嵌入在页面上。 但是，如果需要，开发人员还可以将此功能配置为只允许在特定页面上嵌入应用，方法如下：

- **isPowerAppPersonalizationEnabled** – 如果此方法为特定页面返回 false，那么 Power Apps 菜单按钮不显示，并且用户不能将应用嵌入到此页的任何位置，包括作为选项卡。
- **isPowerAppTabPersonalizationEnabled** – 如果此方法为特定页返回 false，那么用户不能直接在页面上作为选项卡、快速选项卡或全景部分嵌入应用。 如果允许在页面上嵌入，用户仍可以通过 Power Apps 菜单按钮嵌入应用。

以下示例显示需要通过这两种方法来配置应用可以嵌入的位置的新类。

```powerapps
[ExtensionOf(classStr(FormRunConfigurationPowerAppsConfiguration))]

public final class ClassTest_Extension
{
    public static boolean isPowerAppPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppPersonalizationEnabled(pageName);
        return result;
    }
    
    public static boolean isPowerAppTabPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppTabPersonalizationEnabled(pageName);
        return result;
    }
}
```

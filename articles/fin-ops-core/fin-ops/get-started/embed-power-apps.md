---
title: 从 Power Apps 嵌入画布应用
description: 此主题说明如何将 Microsoft Power Apps 中的画布应用嵌入到客户端以细分该产品的功能。
author: jasongre
ms.date: 08/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: 37ef6101a5a69e9c820347dd6f61c987467d40b3
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344521"
---
# <a name="embed-canvas-apps-from-power-apps"></a>从 Power Apps 嵌入画布应用

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Microsoft Power Apps 是一项服务，让开发人员和非技术用户无需编写代码即可为移动设备、平板电脑和 Web 构建自定义业务应用。 Finance and Operations 应用支持与 Power Apps 集成。 您、您的组织或更广泛的生态系统开发的画布应用可以嵌入到 Finance and Operations 应用中来细分产品的功能。 例如，您可以利用 Power Apps 构建画布应用以使用从其他系统检索的信息补充 Finance and Operations 应用。

若要了解有关嵌入画布应用的详细信息，请观看视频短片[如何嵌入画布应用](https://www.youtube.com/watch?v=x3qyA1bH-NY)。

## <a name="adding-an-embedded-canvas-app-from-power-apps-to-a-page"></a>将 Power Apps 中的嵌入画布应用添加到页面中

将画布应用从 Power Apps 嵌入到客户端之前，必须找到或构建具有所需视觉效果或功能的应用。 本主题不包括对构建应用的流程的详细描述。 如果您不熟悉 Power Apps，请参阅 [Power Apps 文档](/powerapps/)。

有三种方法可以将画布应用嵌入到 Finance and Operations 应用中。 您可以使用最适合您的方案的方法。 

- 将画布应用嵌入页面标准操作窗格上的 **Power Apps** 按钮中。 您以这种方式添加的应用在 **Power Apps** 菜单按钮上显示为项，应用会在侧窗格中打开。 
- 将画布应用作为新的选项卡页面（数据透视选项卡、快速选项卡、边栏选项卡或工作区部分）直接嵌入到现有页面。
- 从仪表板为画布应用创建新的整页体验。

配置嵌入的画布应用时，您可以选择您希望将其作为上下文发送到应用的单个字段。 此步骤使应用可以根据您当前正在查看的数据作出响应。

> [!NOTE]
> 您无法使用此机制来嵌入模型驱动应用。

### <a name="embedding-a-canvas-app-on-an-existing-page"></a>在现有页面上嵌入画布应用

以下过程显示了如何将画布应用嵌入到 Power Apps 中的现有页面上。

1. 转到您要嵌入画布应用的页面。 此页面将包含必须作为输入传递到应用的任何数据。
2. 打开 **从 Power Apps 中添加应用** 窗格：

    - 如果应用将直接嵌入到页面上，请选择 **选项** \> **个性化此页面** \> **更多**，然后按照以下步骤之一进行操作：

        - 如果启用了 **完整页面应用** 功能，请选择 **添加页面**，然后选择要在其中添加应用的区域。 若要将应用嵌入到 **Power Apps** 菜单按钮中，请选择操作窗格。 若要将应用直接嵌入到页面上，请选择相应的选项卡、快速选项卡、边栏选项卡或部分（如果您处于工作区中）。 然后，在 **添加应用** 窗格中，选择 **Power Apps**。
        - 如果禁用了 **完整页面应用** 功能，请选择 **从 Power Apps 中添加页面**，然后选择要在其中添加应用的区域。 若要将应用嵌入到 **Power Apps** 菜单按钮中，请选择操作窗格。 若要将应用直接嵌入到页面上，请选择相应的选项卡、快速选项卡、边栏选项卡或部分（如果您处于工作区中）。

    - 如果将使用 **Power Apps** 菜单按钮访问应用，您可以选择标准操作窗格中的 **Power Apps** 菜单按钮，然后选择 **添加应用**。

3. 配置嵌入的应用。 有关详细信息，请参阅本主题后面的[配置画布应用](#configuring-a-canvas-app)一节。
4. 确认配置正确后，选择 **插入**。

    - 如果已关闭 **已保存视图** 功能，则会提示您刷新浏览器以查看嵌入式应用。
    - 如果打开了 **已保存视图** 功能，则必须保存该视图才能保留更改。

### <a name="embedding-a-canvas-app-as-a-full-page-experience-from-the-dashboard"></a>从仪表板将画布应用嵌入为整页体验

如果应用与现有页面无关，或者如果您只想在 Finance and Operations 应用中将应用显示为全页面体验，您可能希望从仪表板嵌入画布应用。

> [!NOTE]
> 若要使此功能可用，您必须在功能管理中启用 **整页应用** 功能。 

1. 打开仪表板。
2. 选择并按住（或右键单击）页面，选择 **个性化**，然后选择 **添加页面**。
3. 在 **添加页面** 窗格中，选择 **Power Apps**。
4. 配置嵌入的应用。 有关详细信息，请参阅本主题后面的[配置画布应用](#configuring-a-canvas-app)一节。
5. 选择 **保存** 将应用作为新磁贴添加到仪表板。
6. 选择仪表板上的新磁贴，确认画布应用按预期显示。

### <a name="configuring-a-canvas-app"></a>配置画布应用

嵌入画布应用时，必须设置以下参数：

- **名称** – 输入应为包含嵌入式应用的按钮或选项卡显示的文本。 通常，您可能要在此字段中重复应用的名称。
- **应用 ID** - 指定要嵌入的画布应用的全局唯一标识符 (GUID)。 若要检索此值，在 [make.powerapps.com](https://make.powerapps.com) 上找到应用，然后在 **详细信息** 下查找 **应用 ID** 字段。
- **应用的输入上下文** - 您可以有选择性地选择包含您要作为输入传送到应用的数据的字段。 有关应用如何访问发送自 Finance and Operations 应用的数据的信息，请参阅本主题后面的[构建利用从 Finance and Operations 应用发送的数据的应用](#building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps)一节。

    从版本 10.0.19 开始，当前法人还将作为上下文通过 **cmp** URL 参数传递到画布应用。 在目标画布应用使用该信息之前，此行为不会影响该应用。

- **应用程序大小** - 选择您要嵌入的应用的类型。 为针对移动设备构建的应用选择 **窄**，或者为针对平板电脑构建的应用选择 **宽**。 此参数将确保为嵌入的应用分配足够的空间量。
- **法人** - 您可以选择该应用应该适用于的法人。 默认情况下，该应用适用于所有法人。 仅当您直接嵌入现有页面并且禁用了 **[已保存视图](saved-views.md)** 功能时，此选项才可用。

## <a name="sharing-an-embedded-app"></a>共享嵌入的应用

在将画布应用嵌入页面并确认此应用能够正常使用后，您可能希望与系统中的其他用户共享此应用。 要共享嵌入的画布应用，请按照下列步骤操作。

1. 与适当的用户[共享 Power Apps 中的画布应用](/powerapps/maker/canvas-apps/share-app)，以便他们可以直接在 Power Apps 中访问此应用。
2. 与所需用户共享与嵌入式应用关联的个性化设置。 您可以使用以下两种方法之一：

    - **发布视图（建议）：** 如果打开了 **[已保存视图](saved-views.md)** 功能，建议的首选方法是创建包含嵌入式画布应用的视图，然后将该视图发布给所需的用户。 此方法可以确保具有发布视图所针对的安全角色的所有用户都会在页面上看到画布应用。

        您还可以从仪表板发布已嵌入为整页体验的画布应用。 在仪表板上，选择并按住（或右键单击）与应用关联的磁贴，选择 **个性化**，然后选择 **发布页面**。 系统显示了与 *发布视图* 体验相似的体验，您可以选择要发布到的安全角色。 在更新 10.0.21 或更高版本中，如果打开了 **改进了对已保存视图的法人支持** 功能，您还可以将应用发布到所需的法人。

    - 如果关闭了 **已保存视图** 功能，则系统管理员可以通过 **个性化设置** 页面为合适的用户组提供包括画布应用的个性化设置。 或者，您可以导出页面的个性化设置，然后将其发送给一个或多个用户。 这些用户中的每一个都可以导入个性化设置。 个性化工具栏具有让您可以导出和导入个性化设置的按钮。

> [!NOTE]
> 如果画布应用已与外部用户共享，这些用户将不能在 Finance and Operations 应用内使用嵌入的应用。 不过，他们可以直接在 Power Apps 内访问该应用。 外部用户包括来宾和不属于在其中部署了 Finance and Operations 应用的 Microsoft 365 Azure Directory 目录的用户。

有关产品中的个性化功能以及如何使用的更多详细信息，请参阅[打造个性化的用户体验](personalize-user-experience.md)。

## <a name="building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps"></a>构建使用从 Finance and Operations 应用发送的数据的画布应用

当您构建将嵌入到 Finance and Operations 应用中的画布应用时，此流程的一个重要部分是使用来自该 Finance and Operations 应用的输入数据。 根据 Power Apps 开发经验，可以使用 **Param("EntityId")** 变量访问从 Finance and Operations 应用传递的输入数据。 此外，从版本 10.0.19 开始，当前法人还将通过 **Param("cmp")** 变量传递到画布应用。 

例如，在应用的 OnStart 功能中，可以将 Finance and Operations 应用的输入数据设置为类似这样的一个变量：

``` Power Apps
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));

If(!IsBlank(Param("cmp")), Set(FinOpsLegalEntity, Param("cmp")), Set(FinOpsLegalEntity, ""));
```

## <a name="viewing-a-canvas-app"></a>查看画布应用

若要查看 Finance and Operations 应用中页面上的嵌入画布应用，只需转到包含嵌入的应用的页面。 请记住，可以使用标准操作窗格上的 **Power Apps** 按钮来访问应用。 或者，它们可以作为新选项卡、快速选项卡或边栏选项卡或作为工作区中的新部分直接显示在页面上。 当用户首次尝试在页面上加载应用时，将提示他们登录。 此步骤可确保用户具有使用该应用的适当权限。

## <a name="editing-an-embedded-app"></a>编辑嵌入的应用

在应用嵌入到页面后，可能需要对该应用的配置作一些更改。 例如，可能您要修改与嵌入的应用关联的标签，或者已创建新版本应用并且您需要更新应用 ID 以指向最新应用。

执行以下步骤来编辑嵌入的应用的配置：

1. 转到 **编辑应用** 窗格。

    - 如果嵌入的应用通过 Power Apps 菜单按钮访问，请选择并按住（或右键单击）Power Apps 菜单按钮并选择 **个性化**。 选择您想要从 **选择应用** 下拉菜单配置的应用。
    - 如果嵌入的应用直接出现在页面上，选择 **选项**，然后选择 **个性化设置此页面**。 使用 **选择** 工具，单击嵌入的应用。
    - 如果从仪表板中添加了嵌入式应用，请打开仪表板，选择并按住（或右键单击）与画布应用关联的磁贴，选择 **个性化**，然后选择 **编辑页面**。

2. 对应用配置进行需要的修改，然后单击 **保存**。

## <a name="removing-an-app"></a>移除应用

在应用嵌入到页面上后，如果需要，有一些方法可以删除它：

- 使用此主题前面 [编辑嵌入的应用](#editing-an-embedded-app)部分中的说明转到 **编辑应用** 窗格。 确认窗格显示您要删除的嵌入应用的信息，然后单击 **删除** 按钮。
- 如果从仪表板中添加了嵌入式应用，请打开仪表板，选择并按住（或右键单击）与画布应用关联的磁贴，选择 **个性化**，然后选择 **删除页面**。 
- 由于嵌入的应用保存为个性化数据，清除页面的个性化也将删除该页面上所有嵌入的应用。 请注意，清除页面的个性化是永久的，并且无法撤消。 若要删除您的页面上的个性化设置，依次选择 **选项**、**个性化设置此页面** 和 **清除**。 刷新您的浏览器后，将删除此页之前的所有个性化设置。 请参阅[打造个性化的用户体验](personalize-user-experience.md)了解有关如何使用个性化设置优化页面的更多信息。

## <a name="appendix"></a>附录

### <a name="developer-modeling-a-canvas-app-on-a-form"></a>[开发人员] 在窗体上为画布应用建模

本主题着重介绍通过个性化嵌入画布应用，开发人员还可以选择使用 Visual Studio 开发体验将画布应用添加到窗体中。 要使用此方法，只需将 PowerAppsHostControl 添加到窗体中。 控件上可用的元数据属性提供与个性化体验相同的功能。

### <a name="developer-specifying-where-an-app-can-be-embedded"></a>[开发人员]指定应用可以嵌入的位置

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

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

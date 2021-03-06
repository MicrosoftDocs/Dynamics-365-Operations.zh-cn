---
title: 功能管理概览
description: 本主题介绍功能管理功能及其用法。
author: ChrisGarty
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: IT Pro, Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: 2164c07d1a179a0aa15611b742084d872f41bbfc
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270805"
---
# <a name="feature-management-overview"></a>功能管理概览

[!include [banner](../../includes/banner.md)]

每个版本中都会增加和更新功能。 功能管理体验提供一个工作区，可在其中查看各版本已交付的功能的列表。 默认情况下，新功能处于关闭状态。 可使用该工作区开启这些功能并查看其文档。

## <a name="the-feature-management-workspace"></a>功能管理工作区

可通过在仪表板中选择相应磁贴打开 **功能管理** 工作区。 将看到一个页面，其中显示功能管理体验支持的所有版本的功能列表。 Microsoft 将不断增强功能管理体验，使其包含更多功能以帮助您管理功能。

功能列表中包含以下信息：

- **功能名称** – 已添加的功能的说明。
- **启用状态** – 一个符号指示功能已开启（选中符号），未开启（空白），已计划开启（时钟），已强制开启（锁），开启前需要注意（警告），或不能启用 (X)。 显示的设置用于所有法人。 请注意，功能即使已开启，仍然受安全性控制。 因此，功能仅对根据安全角色具有其访问权的用户可用。 还仅在用户可访问的法人中可用。
- **启用日期** – 功能的开启或计划开启日期。
- **功能添加日期** – 功能添加到您的环境时的日期。 此日期是您在月度版本周期内更新环境时自动输入的。
- **模块** – 新功能影响的模块。

选择功能时，功能列表右侧的详细信息窗格内会显示更多信息。 可以在窗格顶部看到功能名称、功能的添加日期、功能影响的模块，以及 **了解更多** 链接。 选择此链接可查看功能的文档。 如果文档不可用，将回到临时页。 详细信息窗格中还包含 **注释** 字段，可在其中添加您自己有关功能的注释。

**功能管理** 工作区中有多个选项卡，每个选项卡都会显示功能列表。

- **新增** - 此选项卡显示上次月度更新以来增加的所有功能。 如果跳过任何月度更新，选项卡将显示上次更新以后增加的所有新功能。 最新的功能在列表顶部显示。 页面顶部的磁贴中还会显示新功能的总数。
- **未启用** – 此选项卡显示尚未开启的所有功能。 最新的功能在列表顶部显示。 页面顶部的磁贴中还会显示尚未开启的新功能的总数。
- **已计划** - 此选项卡显示所有已计划在将来开启的功能。 计划的日期最早的功能在列表顶部显示。 页面顶部的磁贴中还会显示计划新功能的总数。
- **所有** – 此选项卡显示所有功能。 最新的功能在列表顶部显示。

## <a name="turn-on-a-feature"></a>开启一项功能

如果尚未开启某个功能，详细信息窗格中将显示 **立即启用** 按钮。 可使用此按钮开启该功能。

- 选择要开启的功能，然后在详细信息窗格中选择 **立即启用**。 将开启此功能。

某些功能在开启后不能关闭。 如果尝试开启的功能不可关闭，您将收到警告。 此时可选择 **取消** 以取消操作并让功能保持关闭状态。 但是，如果选择 **启用** 以开启功能，以后不能关闭该功能。

开启某些功能之前，这些功能会显示一条消息，为您提供更多信息。 这些功能带有黄色警告符号。 应仔细阅读这些额外信息，以便更好地理解启用这些功能的后果。 但是，仍然可以选择 **启用** 以开启功能。

某些功能会显示一条消息，说明执行操作后才能启用这些功能。 这些功能带有红色 X 符号。 启用这些功能之前，必须按照说明中的介绍执行操作。 例如，如果禁用配置键之前不能使用某些功能，则必须先禁用配置键，然后返回功能管理以启用功能。

开启一项功能后，详细信息窗格的 **了解更多** 链接下将显示一条消息。 此消息说明已开启该功能或指示计划开启此功能的将来日期。 只要在功能列表中选择该功能，此消息都会显示。

**已计划** 选项卡中将显示计划在将来开启的功能。批处理流程将根据系统日期表示的时区在指定的日期开启这些功能。

## <a name="reschedule-a-feature"></a>重新计划功能

如果某个功能已计划在将来开启，详细信息窗格中将显示 **计划** 按钮。 可使用此按钮将 **启用日期** 值更改为其他日期。

1. 选择重新计划的已计划功能，然后在详细信息窗格中选择 **计划**。
2. 在显示的对话框中的 **启用日期** 字段中，指定应开启功能的新日期。
3. 选择 **启用** 以重新计划该功能，或选择 **禁用** 以取消计划。

## <a name="turn-off-a-feature"></a>关闭一项功能

如果已开启某个功能，详细信息窗格中将显示 **禁用** 按钮。 可使用此按钮关闭该功能。 如果功能在开启后不可关闭，则 **禁用** 按钮不可用。

- 选择要关闭的功能，然后在详细信息窗格中选择 **禁用**。 将关闭此功能，并清除 **启用日期** 字段。

关闭一项功能后，详细信息窗格的 **了解更多** 链接下将显示一条消息。 此消息说明尚未开启此功能。 只要在功能列表中选择该功能，此消息都会显示。 **未启用** 选项卡中将显示尚未开启的功能。

## <a name="features-that-must-be-turned-on"></a>必须开启的功能

有时会交付某个在您执行更新时必须自动开启的关键功能。 将在 **启用日期** 字段中指定的日期自动开启这些功能。 对于这些功能，详细信息窗格的 **了解更多** 链接下将显示一条消息。 此消息说明已开启该功能或指示将开启此功能的将来日期。 只要在功能列表中选择该功能，此消息都会显示。

## <a name="enable-all-features"></a>启用所有功能

默认情况下，将关闭向您的环境添加的所有功能。 可以通过选择 **全部启用** 按钮启用所有功能。 

如果选择 **全部启用**，将显示一个选项，需要在该处提供以下信息：
- 确认后才能启用的所有功能的列表。 如果要启用列表中的功能，请对 **启用需要确认的功能** 按钮选择 **是**。
- 将显示不能启用的所有功能的列表。 将不启用这些功能。

将启用可启用的所有功能。 如果已经安排在将来启用某项功能，此项安排不会改变。 

## <a name="turn-on-all-features-automatically"></a>自动开启所有功能

默认情况下，将关闭向您的环境添加的所有功能，除非是必需功能。 但是，如果要自动开启所有新功能，可使用工作区磁贴下方的下拉列表更改添加新功能时显示的内容。

- 选择 `Enable new features automatically`，以在向您的环境添加新功能时，自动开启所有新功能。
- 选择 `Do not enable new features automatically`，以在向您的环境添加新功能时，默认关闭所有新功能。


自动启用所有功能时，将启用在您单击 **全部启用** 按钮时要启用的所有功能。 不会启用需要确认的功能或执行操作后才能启用的功能。

## <a name="check-for-updates"></a>检查更新

每次更新后，将向您的环境添加功能。 但是，可通过单击 **检查更新** 按钮手动检查更新。 将把更新后已添加到系统的所有功能添加到功能列表。 例如，如果在发布后启用了一项外部测试版功能，则您可检查更新，并将把此功能添加到列表。

## <a name="assigning-roles"></a>分配角色

**功能管理** 工作区可以由系统管理员打开，也可以由分配有功能管理员或功能查看者角色的用户打开。 创建这两种角色是为了支持功能管理体验。 功能管理员角色的用户可打开或关闭任何功能。 他们还可以更新功能的 **注释** 字段。 功能查看者角色的用户只能查看 **功能管理** 工作区。 不能打开或关闭功能。

功能管理员角色和功能查看者角色不能覆盖用户的现有安全性。 他们只能控制用户是否可以开启和关闭功能。 不能提供功能本身的访问权限。

## <a name="features-that-use-configuration-keys"></a>使用配置键的功能

如果某个功能使用配置键，但是未开启此配置键，**功能管理** 工作区的可用功能列表中将不显示该功能。 开启该配置键之后，必须通过使用 **检查更新** 菜单项更新功能列表。 然后将在功能列表中显示该功能。

如果关闭配置键，将从功能列表中删除此功能。

## <a name="data-entities"></a>数据实体

可通过名称为 **功能管理** 的数据实体从一个环境中导出功能管理设置，然后将其导入另一个环境中。 此实体仅更新现有功能。 此实体中的业务逻辑还有助于保证导入完成时应用在 **功能管理** 工作区中使用的相同规则。 例如，不能通过在导入期间删除日期来覆盖必需功能设置。

以下示例介绍使用 **功能管理** 实体导入数据时所发生的情况。

- 如果将 **启用** 字段的值更改为 **是**，将开启此功能，并将 **启用日期** 字段设置为当前日期。
- 如果将 **启用** 字段的值更改为 **否** 或让 **启用日期** 保留为空，将关闭此功能，并清除 **启用日期** 字段。 不能关闭必需功能或开启后不能关闭的功能。
- 如果将 **启用日期** 字段的值更改为将来的日期，将为功能安排该日期。
- 如果将 **启用** 字段的值更改为 **是**，并将 **启用日期** 字段的值更改为将来的日期，将为此功能安排该日期。 
- 如果将 **启用** 字段的值更改为 **否**，但是仍然将 **启用日期** 字段的值更改为将来的日期，将为此功能安排该日期。
- 如果开启某项功能，并添加设置为将来日期的 **启用日期** 字段，该功能将保持开启状态。 若要重新计划该功能，必须将 **启用** 字段更改为 **否**。

## <a name="feature-management-and-flighting"></a>功能管理和外部测试

可通过功能管理控制每个版本中交付的功能。 Microsoft 团队可通过外部测试将功能发布给一小部分客户，这样测试和验证这些功能时不会影响全体客户。 功能管理不会控制任何功能的外部测试。

## <a name="new-features-are-optional-for-12-months"></a>新功能在 12 个月内可选

新的非关键功能在安装后 12 个月内可选。 这样就为您和您的组织留出了时间来提前计划何时使用功能并针对日常操作进行测试。 有关预览版的详细信息，请参阅 [One Version 服务更新常见问题](../one-version.md#what-about-new-features)。

## <a name="using-feature-management-to-turn-on-isv-features-or-custom-features"></a>使用功能管理开启 ISV 功能或自定义功能

功能管理现在不支持来自独立软件供应商 (ISV) 的功能和自定义功能。 但是，Microsoft 将增加更多功能以增强功能管理。 完成这些增强之后，Microsoft 将向所有功能提供功能管理，并提供有关如何更新功能以使用功能管理的说明。

## <a name="frequently-asked-questions-faq"></a>常见问题 (FAQ)

### <a name="when-are-features-added-removed-or-changed"></a>何时添加、删除或更改功能？ 
功能通过代码更改来添加、删除和更改。 需要更新环境来接收这些更改。

### <a name="does-a-feature-become-mandatory-automatically"></a>功能会自动变成强制功能吗？ 
不会，功能变为强制不是自动操作。 产品团队需要进行代码更改。

### <a name="when-do-features-become-mandatory"></a>功能何时会成为强制功能？ 
政策是所有新功能都有 12 个月的选择使用期间，在您启用功能之前不需要任何更改管理。 产品团队可以在该期限结束后选择是否将某项功能设为强制功能。 

### <a name="why-isnt-there-a-specific-mandatory-enabled-date"></a>为什么没有特定的“强制启用日期”？ 
更新发布时间是可变的，环境更新时间是可变的，客户可以选择跳过某些更新。 因此，难以确定具体日期。 

### <a name="wheres-the-documentation-for-features-that-are-mandatory"></a>设为强制的功能的文档在哪里？ 
此文档来自每个 Dynamics 365 应用程序团队。 通常，[客户端功能状态的更新](/dynamics365-release-plan/2021wave1/finance-operations/finance-operations-crossapp-capabilities/updates-client-feature-states)或[已删除或弃用的功能](../../../dev-itpro/migration-upgrade/deprecated-features.md)中将涉及这些功能。 

### <a name="is-there-an-in-product-notification-or-signal-that-a-feature-is-going-to-be-mandatory-enabled"></a>是否有产品内通知或信号指示将强制启用某项功能？ 
目前不存在有关设为强制功能的通知机制。

### <a name="do-features-ever-get-enabled-without-the-customer-knowing-about-it"></a>功能是否会在客户不知情的情况下被启用？ 
是，如果功能不具有功能性影响，它们可能被默认启用。

### <a name="what-is-feature-flighting-and-how-does-it-relate-to-feature-management"></a>什么是功能外部测试？它与功能管理有何关系？ 
功能外部测试是 Microsoft 控制的实时“开/关”开关。 它们与“功能管理”提供的客户控制是分开的。 
- 个人预览功能在进行外部测试之前不会在“功能管理”中列出。 在生产中，客户需要同意成为特殊计划的一部分，才能进行外部测试。
- 除非已关闭外部测试，否则“公开预览”和“已发布”（公开发布）功能将在“功能管理”中列出。 如果发现关键问题并且通常是每个客户的操作，关闭功能的外部测试是产品团队的最后一种选择。

### <a name="do-features-ever-get-flighted-off-without-the-customer-knowing-about-it"></a>功能是否会在客户不知情的情况下关闭外部测试？ 
是，如果某项功能影响没有功能性影响的环境的运行，则可能默认启用它们。

### <a name="how-can-feature-enablement-be-checked-in-code"></a>如何在代码中检查功能启用？
使用 **FeatureStateProvider** 类上的 **isFeatureEnabled** 方法，向其传递功能类的一个实例。 示例: 

```xpp
if (FeatureStateProvider::isFeatureEnabled(BatchContentionPreventionFeature::instance()))
```

### <a name="how-can-feature-enablement-be-checked-in-metadata"></a>如何在元数据中检查功能启用？
**FeatureClass** 属性可用于指示某些元数据与功能相关联。 应该使用用于功能的类名，例如 **BatchContentionPreventionFeature**。 此元数据仅在该功能中可见。 **FeatureClass** 属性在菜单、菜单项、枚举值和表/视图字段上可用。

### <a name="what-is-a-feature-class"></a>什么是功能类？
功能管理中的功能将定义为 *功能类*。 功能类将 **实现 IFeatureMetadata** 并使用功能类属性，以向功能管理工作区标识自身。 有许多可用的功能类示例，可用于使用 **FeatureStateProvider** API 在代码中以及使用 **FeatureClass** 属性在元数据中检查功能启用。 示例: 

```xpp
[ExportAttribute(identifierStr(Microsoft.Dynamics.ApplicationPlatform.FeatureExposure.IFeatureMetadata))]
internal final class BankCurrencyRevalGlobalEnableFeature implements IFeatureMetadata
```

### <a name="what-is-the-ifeaturelifecycle-implemented-by-some-feature-classes"></a>一些功能类实现的 IFeatureLifecycle 是什么？
IFeatureLifecycle 是 Microsoft 内部的一种机制，用于指示功能生命周期阶段。 功能可以是：
- `PrivatePreview` - 需要外部测试版可见。
- `PublicPreview` - 默认显示，但具有该功能处于预览状态的警告。
- `Released` - 已完全发布。



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

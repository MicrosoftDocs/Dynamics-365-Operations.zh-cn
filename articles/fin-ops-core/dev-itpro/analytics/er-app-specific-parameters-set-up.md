---
title: 为每个法人设置 ER 格式的参数
description: 本主题说明如何为每个法人设置电子报告 (ER) 格式的参数。
author: NickSelin
ms.date: 03/25/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: f72ce72e9cbd268efc6ab09dbec7009794d69613
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/27/2022
ms.locfileid: "8644490"
---
# <a name="set-up-the-parameters-of-an-er-format-per-legal-entity"></a>为每个法人设置 ER 格式的参数

[!include[banner](../includes/banner.md)]

## <a name="prerequisites"></a>先决条件

要完成这些步骤，您必须首先完成[配置 ER 格式以使用每个法人指定的参数](er-app-specific-parameters-configure-format.md)中的步骤。

若要完成本主题中的示例，您必须具有以下角色之一的 Microsoft Dynamics 365 Finance 访问权限：

- 电子报告开发人员
- 电子报告功能顾问
- 系统管理员

## <a name="import-er-configurations"></a>导入 ER 配置
要导入 ER 配置，请执行以下步骤： 

1. 登录您的环境。
2. 在默认仪表板中，选择 **电子申报**。
3. 选择 **申报配置**。
4. 在完成[配置 ER 格式以使用每个法人指定的参数](er-app-specific-parameters-configure-format.md)主题中的步骤时，在 Finance 的当前实例中，导入您从 Regulatory Configuration Services (RCS) 导出的配置。 对于每个[电子报告 (ER)](general-electronic-reporting.md) 配置，请按照以下顺序执行以下步骤：数据模型、模型映射和格式。

    1. 选择 **交易 \> 从 XML 文件加载**。
    2. 选择 **浏览** 以 XML 格式选择所需 ER 配置的文件。
    3. 选择 **确定**。

    下图显示了完成后必须具有的配置。

    ![ER 配置页面。](./media/GER-AppSpecParms-ImportedConfigurations.PNG)

## <a name="set-up-parameters-for-the-demf-company"></a>为 DEMF 公司设置参数

您可以使用 ER 框架为 ER 格式设置特定于应用程序的参数。

1. 选择 **DEMF** 法人。
2. 在配置树中，选择 **用于了解如何查找 LE 数据的格式** 格式。
3. 在操作窗格的 **配置** 选项卡的 **应用程序特定参数** 组中，选择 **设置**。

    ![设置参数的特定于 ER 应用程序的参数页。](./media/GER-AppSpecParms-LookupForm.PNG)

    在 **应用程序特定参数** 页面上，您可以为 **用于了解如何查找 LE 数据的格式** 格式的 **选择器** 数据源配置规则。

    如果基本 ER 格式将包含多个 **查找** 类型的数据源，则必须先在 **查找** 快速选项卡上选择所需的数据源，然后才能开始为数据源配置规则集。

    对于每个数据源，您可以为所选 ER 格式的每个版本配置单独的规则。

    在基本 ER 格式的选定版本中可用的所有查找数据源的全部规则构成了 ER 格式的特定于应用程序的参数。

4. 选择 ER 格式的版本 **1.1.1**。
5. 在 **条件** 快速选项卡上，选择 **添加**。
6. 在新记录的 **代码** 字段中，选择下拉箭头以打开查找。

    查找显示可供选择的税码列表。 此列表由在基本 ER 格式中配置的 **Model.Data.Tax** 数据源返回。 由于此数据源包含 **名称** 字段，因此每个税码的名称将显示在查找中。

    ![ER 应用程序特定参数页面上的代码字段查找。](./media/GER-AppSpecParms-LookupForm-CodeFldPicker.PNG)

7. 选择 **VAT19** 税码。
8. 在新记录的 **查找结果** 字段中，选择下拉箭头以打开查找。 查找显示 TaxationLevel 格式枚举的值列表供选择。

    请注意，如果您选择德语作为用来登录的用户的首选语言，则查找中值的标签将以德语显示，前提是它们已在基本 ER 格式中进行翻译。 此外，如果查找数据源的标签已翻译，该标签将以用户的首选语言显示在 **查找** 选项卡上。

    ![ER 应用程序特定参数页上翻译为德语的查找字段。](./media/GER-AppSpecParms-LookupForm-LookupFldPicker.PNG)

9. 选择 **正常税收** 值。

    通过添加此记录，您可以定义以下规则：当请求 **选择器** 查找数据源，并且将 **VAT19** 税码作为参数传递时，**正常税收** 将返回为请求的征税级别。

10. 选择 **添加**，然后按照以下步骤操作：

    1. 在 **代码** 字段中，选择 **InVAT19** 税码。
    2. 在 **查找结果** 字段中，选择 **正常税收** 值。

11. 选择 **添加**，然后按照以下步骤操作：

    1. 在 **代码** 字段中，选择 **VAT7** 税码。
    2. 在 **查找结果** 字段中，选择 **减税** 值。

12. 选择 **添加**，然后按照以下步骤操作：

    1. 在 **代码** 字段中，选择 **InVAT7** 税码。
    2. 在 **查找结果** 字段中，选择 **减税** 值。

13. 选择 **添加**，然后按照以下步骤操作：

    1. 在 **代码** 字段中，选择 **THIRD** 税码。
    2. 在 **查找结果** 字段中，选择 **免税** 值。

14. 选择 **添加**，然后按照以下步骤操作：

    1. 在 **代码** 字段中，选择 **InVAT0** 税码。
    2. 在 **查找结果** 字段中，选择 **免税** 值。

15. 选择 **添加**，然后按照以下步骤操作：

    1. 在 **代码** 字段中，选择 **\*非空\*** 选项。
    2. 在 **查找结果** 字段中，选择 **其他** 值。

    通过添加最后这个记录，您可以定义以下规则：当作为参数传递的税码不满足任何先前的规则时，查找数据源将返回 **其他** 作为请求的征税级别。

    ![在 ER 应用程序特定参数页面上添加的最后一个记录。](./media/GER-AppSpecParms-LookupForm-RulesSet.PNG)

16. 在 **状态** 字段中，选择 **已完成**。

    当您运行状态为 **已完成** 或 **共享** 的 ER 格式版本时，这组规则必须处于 **已完成** 状态。 否则，当运行 **选择器** 查找数据源时，如果尝试从此组规则加载数据，则基本 ER 格式的执行将被中断。

    当您运行状态为 **草稿** 的 ER 格式版本时，基本 ER 格式可以访问这组规则，不管其状态如何。

17. 选择 **保存**。
18. 关闭 **应用程序特定参数** 页面。

## <a name="run-the-er-format-in-the-demf-company"></a>在 DEMF 公司中运行 ER 格式
要在 DEMF 公司中运行 ER 格式，请执行以下步骤： 

1. 在配置树中，选择 **用于了解如何查找 LE 数据的格式** 格式。
2. 在操作窗格上，选择 **运行**。
3. 在显示的对话框中，选择 **确定**。
4. 下载生成的报表并将其存储在本地。

    在生成的报表中，注意 **InVAT7** 税码的汇总已进入 **减税** 级别，**VAT19** 和 **InVA19** 税码的汇总已进入 **正常** 级别。 此行为由依赖于法人的一组规则中的配置确定。

5. 转到 **税金 \> 间接税 \> 销售税 \> 销售税代码**。
6. 选择 **InVAT7** 税码。
7. 在操作窗格的 **销售税代码** 选项卡上的 **查询** 组中，选择 **已过帐的销售税** 以查看有关每个税码的税金值和所应用税率的信息。

    ![已过帐的销售税页面。](./media/GER-AppSpecParms-Statement.PNG)

8. 关闭 **已过帐的销售税** 页。

## <a name="set-up-parameters-for-the-usmf-company"></a>为 USMF 公司设置参数
要设置 USMF 公司的参数，请完成以下步骤： 

1. 选择 **USMF** 法人。
2. 转到 **组织管理 \> 电子申报 \> 配置**。
3. 在配置树中，展开 **用于了解参数化调用的数据模型** 项，展开 **用于了解参数化调用的格式** 项，然后选择 **用于了解如何查找 LE 数据的格式** 格式。
4. 在操作窗格的 **配置** 选项卡的 **应用程序特定参数** 组中，选择 **设置**。
5. 选择所选 ER 格式的版本 **1.1.1**。
6. 在 **条件** 快速选项卡上，选择 **添加**。
7. 在新记录的 **代码** 字段中，选择下拉箭头以打开查找。

    现在，查找将显示 **USMF** 公司税务的税码列表供选择。

    ![USMF 公司税务的税码。](./media/GER-AppSpecParms-LookupForm-CodeFldPicker2.PNG)

8. 选择 **EXEMPT** 税码。
9. 在新记录的 **查找结果** 字段中，选择 **免税** 值。
10. 选择 **添加**。
11. 在新记录的 **代码** 字段中，选择 **\*非空\*** 选项。
12. 在新记录的 **查找结果** 字段中，选择 **正常税收** 值。
13. 在 **状态** 字段中，选择 **已完成**。
14. 选择 **保存**。

    ![ER 应用程序特定参数页面。](./media/GER-AppSpecParms-LookupForm-RulesSet2.PNG)

15. 关闭 **应用程序特定参数** 页面。

## <a name="run-the-er-format-in-the-usmf-company"></a>在 USMF 公司中运行 ER 格式
要在 USMF 公司中运行 ER 格式，请完成以下步骤：

1. 在配置树中，选择 **用于了解如何查找 LE 数据的格式** 格式。
2. 在操作窗格上，选择 **运行**。
3. 在显示的对话框中，选择 **确定**。
4. 下载生成的报表并将其存储在本地。

    在生成的报表中，注意您现在已将相同的 ER 格式重复用于其他法人，但未对 ER 格式进行任何调整。

## <a name="reuse-legal-entitydependent-parameters"></a>重用依赖于法人的参数

### <a name="duplicate-existing-parameters"></a>复制现有参数

#### <a name="export-parameters"></a>导出参数
要导出参数，请完成以下步骤：

1. 转到 **组织管理 \> 工作区 \> 电子申报**。
2. 选择 **申报配置**。
3. 在配置树中，选择 **用于了解如何查找 LE 数据的格式** 格式。
4. 在操作窗格的 **配置** 选项卡的 **应用程序特定参数** 组中，选择 **设置**。
5. 选择 ER 格式的版本 **1.1.1**。
6. 在操作窗格上，选择 **导出**。
7. 下载生成的文件并将其存储在本地。

    现在，配置的一组特定于应用程序的参数已导出为 XML 文件。

#### <a name="import-parameters"></a>导入参数
要导入参数，请完成以下步骤：

1. 选择 ER 格式的版本 **1.1.2**。
2. 在操作窗格上，选择 **导入**。
3. 选择 **是** 以确认您要为此格式版本覆盖现有的特定于应用程序的参数。
4. 选择 **浏览** 查找包含导出的版本 **1.1.1** 的应用程序特定参数的文件。
5. 选择 **确定**。

    ER 格式的版本 **1.1.2** 现在具有与您最初为版本 **1.1.1** 版本配置的应用程序特定参数相同的参数。

##### <a name="applicability-considerations"></a>适用性注意事项

ER 格式的特定于应用程序的参数依赖于法人。 要重用为另一个法人中的一个法人配置的应用程序特定参数，必须在登录第一个法人时将其导出。 然后在登录另一个法人后将其导入。

您还可以使用此导出-导入方法将最初在一个 Finance 实例中配置的与 ER 格式相关的特定于应用程序的参数转移到另一个 Finance 实例。

如果您为 ER 格式的一个版本配置特定于应用程序的参数，然后将相同格式的更高版本导入当前 Finance 实例，现有的特定于应用程序的参数将不会应用于导入的版本，除非您使用 **使用先前版本的 ER 格式中的应用程序特定参数** 功能。 有关详细信息，请参阅本主题后面的[重用现有参数](#reuse-existing-parameters)一节。

当选择要导入的文件时，该文件中特定于应用程序的参数的结构将与为导入选择的 ER 格式中的 **查找** 类型的相应数据源的结构进行比较。 默认情况下，仅当每个特定于应用程序的参数的结构与为导入选择的 ER 格式的相应数据源的结构匹配时，才完成导入。 如果结构不匹配，一条警告消息会通知您无法完成导入。 如果您强制导入，将清除所选 ER 格式的现有的特定于应用程序的参数，您必须从头开始进行设置。


从 Finance 版本 10.0.24 开始，您可以通过启用 **功能管理** 工作区的 **导入时对齐电子报告应用程序特定的参数** 功能来更改默认行为，避免收到警告消息。 启用此功能后，如果您导入的应用程序特定参数的结构与为导入选择的目标 ER 格式的相应数据源的结构不同，导入将在以下情况下成功：

- 通过向 **查找** 类型的任何现有数据源添加新条件列，目标 ER 格式的结构已更改。 导入完成后，应用程序特定参数已更新。 在所有导入的应用程序特定参数记录中，每个添加的条件列中的值都使用该列的[数据类型](er-formula-supported-data-types-primitive.md)的默认值进行了初始化。
- 通过从 **查找** 类型的任何现有数据源中删除某些条件列，目标 ER 格式的结构已更改。 导入完成后，应用程序特定参数已更新。 在应用程序特定参数的所有导入的记录中，每个已删除的条件列中的值都被删除。
- 通过添加 **查找** 类型的新数据，目标 ER 格式的结构已更改。 导入完成后，添加的查找将追加到特定于应用程序的参数。
- 通过删除某些 **查找** 类型的现有数据源，目标 ER 格式的结构已更改。 导入完成后，与从目标 ER 格式中删除的 **查找** 类型的数据源相关的所有项目都被从导入的应用程序特定参数中删除。

导入完成后，除了刚刚描述的更改之外，导入的应用程序特定参数的状态更改为 **进行中**。 警告消息通知您，必须手动编辑自动调整后的应用程序特定参数。

#### <a name="replicate-parameters"></a>复制参数

从 Finance 版本 10.0.27 开始，您可以将您在一个公司配置的参数同时复制到其他公司。

要复制参数，请完成以下步骤。

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 选择 **申报配置**。
3. 在配置树中，选择 **用于了解如何查找 LE 数据的格式** 格式。
4. 在操作窗格的 **配置** 选项卡的 **应用程序特定参数** 组中，选择 **设置**。
5. 选择 ER 格式的版本 **1.1.1**。
6. 在操作窗格上，选择 **复制**。
7. 在 **复制** 对话框中，在 **公司** 选项卡上，选择要将参数复制到的公司。

    > [!NOTE]
    > 目标公司的列表仅提供给分配了安全[角色](../sysadmin/role-based-security.md#security-roles)的用户，该角色被配置为授予对所有组织的访问权限。

8. 选择 **确定**。

    > [!NOTE]
    > 如果某些目标公司包含先前为选定版本的 ER 格式配置的参数，确认对话框会通知您。 选择 **是** 可通过从当前公司复制参数来覆盖这些参数。

    配置的应用程序特定参数集现在会复制到选定的公司。

### <a name="reuse-existing-parameters"></a>重用现有参数

从 Finance 版本 10.0.23 开始，当您运行相同格式的更高版本时，您可以重用为一个版本的 ER 格式配置的特定于应用程序的参数。 要重用现有参数，请在 **功能管理** 工作区中启用 **使用先前版本的 ER 格式中的应用程序特定参数** 功能。 启用此功能并运行一个正在尝试读取特定于应用程序的参数的 ER 格式版本时，ER 将尝试查找已为此格式的运行版本配置的应用程序特定参数。 如果它们不可用，ER 将尝试为最接近的较低版本格式查找它们。

> [!NOTE]
> 您只能在当前法人的范围中重用特定于应用程序的参数。
>
> 当您运行的更高版本的 ER 格式尝试重用已为相同格式的较低版本配置的特定于应用程序的参数时，如果更高格式版本中至少有一个 **查找** 类型的数据源的结构更改，运行时将显示错误。

## <a name="relationship-between-application-specific-parameters-and-an-er-format"></a>特定于应用程序的参数和 ER 格式之间的关系

ER 格式与其特定于应用程序的参数之间的关系由 ER 格式不依赖于实例的唯一标识代码建立。 因此，当您从 Finance 中删除 ER 格式时，为 ER 格式配置的特定于应用程序的参数将保留在 Finance 的当前实例中。 在将基本 ER 格式重新导入到此 Finance 实例时，可以访问它们。

## <a name="access-application-specific-parameters-by-using-the-er-framework"></a>通过使用 ER 框架访问特定于应用程序的参数

在前面的示例中，您已经通过使用 ER 框架访问了 ER 格式的特定于应用程序的参数。 这种方法不允许您限制对特定 ER 格式的应用程序特定参数的访问。 如果您必须应用此类限制，请按照下列步骤操作。 

1. 重用现有的 **ERSolutionAppSpecificParametersDesigner** 菜单项，或实现自己的 **ERSolutionAppSpecificParametersDesigner** 菜单项。

    ![ERSolutionAppSpecificParametersDesigner 的菜单项显示内容。](./media/GER-AppSpecParms-LookupForm-Access1.PNG)

2. 按以下步骤之一：

    1. 创建一个新的菜单项按钮，并将其 **数据源** 属性设置为 **ERSolutionTable**，通过此方式将其链接到 **ERSolutionTable** 表中的相应记录。

        ![新菜单项设置的显示内容。](./media/GER-AppSpecParms-LookupForm-Access2.PNG)

    2. 创建一个简单的按钮，并覆盖 **单击** 方法，如以下示例所示。

        通过使用此方法，您可以指定唯一的解决方案 ID（通过 **GUID** 值定义），以允许仅访问特定 ER 格式的应用程序特定参数以及从其派生的后代副本。
        
        ```xpp
        public void clicked()
            {
                super();

                ERSolutionTable solutionTableRecord = ERSolutionTable::findByGUID(str2Guid('ADACCB2F-EFD1-4C90-877D-7E1E5D1AEE92'));

                Args args = new Args();
                args.record(solutionTableRecord);
                args.caller(this);

                new MenuFunction(menuItemDisplayStr(ERSolutionAppSpecificParametersDesigner), MenuItemType::Display)
                    .run(args);
            }
        ```

## <a name="additional-resources"></a>其他资源

[电子报告中的配方设计器](general-electronic-reporting-formula-designer.md)

[配置 ER 格式以使用每个法人指定的参数](er-app-specific-parameters-configure-format.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

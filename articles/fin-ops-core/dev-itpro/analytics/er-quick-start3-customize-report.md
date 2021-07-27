---
title: 自定义电子报告配置以生成电子单据
description: 本主题介绍了如何自定义 Microsoft 提供的电子报告 (ER) 配置，它们用于生成自定义电子单据。
author: NickSelin
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom:
- "220314"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b2b22d6e18974ed600dae6501ec103a49876d2db
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/06/2021
ms.locfileid: "6345904"
---
# <a name="customize-electronic-reporting-configurations-to-generate-an-electronic-document"></a>自定义电子报告配置以生成电子单据

[!include[banner](../includes/banner.md)]

通过[电子报告 (ER) 框架](general-electronic-reporting.md)，您可以将 Microsoft 提供的 ER [配置](general-electronic-reporting.md#Configuration)上传到 Microsoft Dynamics 365 Finance 实例。 通过此方式，Microsoft 提供的配置可以用作 ER 解决方案，用于生成电子客户发票（电子发票）。 您可以使用此 ER 解决方案配置您的自定义 ER 解决方案，以访问您的自定义数据库字段并生成符合您的特定要求的电子发票，而无需编辑源代码。

## <a name="overview"></a>概览

对于本主题中的示例，您必须指定联邦纳税标识代码作为您开具电子发票的每个客户的新自定义属性。 因此，必须通过在生成的每个电子发票中添加一个必须用税码填充的新物料来自定义当前使用的发票的结构。

本主题中的过程介绍了系统管理员、电子报告开发人员或电子报告功能顾问角色的用户如何在 Finance 实例中执行以下任务：

- [配置开始使用 ER 框架所需的最低限度的 ER 参数](#ConfigureER)。
- [导入提供用于生成电子发票的标准 ER 配置的初始版本](#ImportERConfigurations1)。
- [配置应收帐款参数以开始使用标准 ER 配置](#ConfigureAR1)。
- [配置法人参数以向客户开具发票](#ConfigureLE)。
- [准备用于开具电子发票的客户记录](#ConfigureCustomer1)。
- [使用标准 ER 配置添加、过帐和发送客户发票](#ProcessInvoice1)。
- [添加自定义数据库字段以管理客户的联邦纳税标识代码](#AddCustomField)。
- [刷新 ER 元数据以启用 ER 模型映射设计器的数据库更改](#RefreshERMetadata)。
- [设计自定义 ER 配置以生成包含新税码的电子发票](#DesignCustomERConfigurations)。
- [配置应收帐款参数以开始使用自定义 ER 配置](#ConfigureAR2)。
- [更新用于开具电子发票的客户记录](#ConfigureCustomer2)。
- [使用自定义 ER 配置添加、过帐和发送客户发票](#ProcessInvoice2)。
- [导入提供用于生成电子发票的标准 ER 配置的新版本](#ImportERConfigurations2)。
- [在您的自定义 ER 配置中采用对标准 ER 配置的新版本所做的更改](#RebaseCustomERConfigurations)。
- [使用自定义 ER 配置的新版本添加、过帐和发送客户发票](#ProcessInvoice3)。

所有这些过程都可以在 **DEMF** 公司中完成。

## <a name="configure-the-er-framework"></a><a name="ConfigureER"></a>配置 ER 框架

作为电子报告功能顾问或电子报告开发人员角色的用户，您必须配置最低限度的 ER 参数。 然后，您可以开始使用 ER 框架设计用于生成电子发票的 ER 解决方案的标准配置的自定义版本。

### <a name="configure-er-parameters"></a>配置 ER 参数

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **本地化配置** 页面的 **相关链接** 部分中，选择 **电子申报参数**。
3. 在 **电子申报参数** 页上，在 **常规** 选项卡上，将 **启用设计模式** 选项设置为 **是**。
4. 在 **附件** 选项卡上，在 **配置** 字段中，选择 **文件**。
5. 在 **作业存档**、**临时**、**基准** 和 **其他** 字段中，选择 **文件** 类型。

有关 ER 参数的详细信息，请参阅[配置 ER 框架](electronic-reporting-er-configure-parameters.md)。

### <a name="activate-an-er-configuration-provider"></a>激活 ER 配置提供程序

将把添加的每个 ER 配置标记为由 ER 配置提供程序负责。 在 **电子申报** 工作区中激活的 ER 配置提供程序用于此目的。 因此，必须先在 **电子申报** 工作区中激活 ER 配置提供程序，才能开始添加或编辑 ER 配置。

> [!NOTE]
> 只有 ER 配置的负责人才能对其进行编辑。 因此，必须先在 **电子申报** 工作区中激活相应 ER 配置提供程序，才能编辑 ER 配置。

#### <a name="review-the-list-of-er-configuration-providers"></a>查看 ER 配置提供程序列表

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **本地化配置** 页面的 **相关链接** 部分中，选择 **配置提供程序**。
3. 在 **配置提供程序表** 页面中，每条提供程序记录都有唯一名称和 URL。 查看此页面的内容。 如果已有 **Litware, Inc.** (`https://www.litware.com`) 的记录，请跳过下一过程，即[添加新 ER 配置提供程序](#AddProvider)。

#### <a name="add-a-new-er-configuration-provider"></a><a id="AddProvider"></a>添加新 ER 配置提供程序

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **本地化配置** 页面的 **相关链接** 部分中，选择 **配置提供程序**。
3. 在 **配置提供程序** 页面上，选择 **新建**。
4. 在 **名称** 字段中，输入 **Litware, Inc.**
5. 在 **Internet 地址** 字段中，输入 `https://www.litware.com`。
6. 选择 **保存**。

#### <a name="activate-an-er-configuration-provider"></a>激活 ER 配置提供程序

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **本地化配置** 页面的 **配置提供程序** 部分中，选择 **Litware, Inc.** 磁贴，然后选择 **设置有效**。

有关 ER 配置提供程序的详细信息，请参阅[创建配置提供程序并将其标记为有效](tasks/er-configuration-provider-mark-it-active-2016-11.md)。

## <a name="import-the-initial-versions-of-standard-er-configurations"></a><a name="ImportERConfigurations1"></a>导入标准 ER 配置的初始版本

若要向当前 Finance 实例添加标准 ER 配置，必须从为该实例配置的 ER [存储库](general-electronic-reporting.md#Repository)中导入这些配置。

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **本地化配置** 页面的 **配置提供程序** 部分中，选择 **Microsoft** 磁贴，然后选择 **存储库** 查看 Microsoft 提供程序的存储库列表。
3. 在 **配置存储库** 页，选择 **全球** 类型的存储库，然后选择 **打开**。 如果提示您进行授权以连接到 Regulatory Configuration Service，请按照授权说明进行操作。
4. 在 **配置存储库** 页面上，在左侧窗格的配置树中，选择 **Peppol 销售发票** 格式配置。
5. 在 **版本** 快速选项卡中，选择版本 **11.2.2**。
6. 选择 **导入** 以从全局存储库中下载所选版本。

![配置存储库页面。](./media/er-quick-start3-import-solution1.png)

> [!TIP]
> 如果在访问[全球存储库](er-download-configurations-global-repo.md)时遇到问题，可改为从 Microsoft Dynamics Lifecycle Services (LCS)[ 下载配置](download-electronic-reporting-configuration-lcs.md)。

### <a name="review-the-imported-er-configurations"></a>查看导入的 ER 配置

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **本地化配置** 页面的 **配置** 部分中，选择 **报告配置** 磁贴。
3. 在 **配置** 页面上，展开 **配置组件** 快速选项卡。
4. 在左侧窗格的配置树中，展开 **发票模型**，然后展开 **UBL 销售发票**。

请注意，除了所选的 **Peppol 销售发票** ER 格式，还导入了其他必需的 ER 配置。 因为将向全局存储库和 LCS 不断发布 ER 配置的新版本以使相应的解决方案符合新要求，因此导入了所需的[数据模型](general-electronic-reporting.md#data-model-and-model-mapping-components)配置及其[模型映射](general-electronic-reporting.md#data-model-and-model-mapping-components)配置的最新版本。

![配置页面。](./media/er-quick-start3-imported-solution1a.png)

若要在之前已导入 **Peppol 销售发票** ER 格式的版本 **11.2.2**（例如 2019 年 8 月 7 日）的情况下模拟 ER 配置在当前 Finance 实例中的状态，请按照以下步骤操作。

- 在“操作”窗格上，选择 **删除** 以删除 2019 年 8 月 7 日之后发布的所有 ER 配置。 必须仅保留 **发票模型**、**发票模型映射**（最初命名为 **客户发票模型映射**）、**UBL 销售发票** 和 **Peppol 销售发票** 配置。
- 对于其余的 ER 配置，请在 **版本** 快速选项卡上，选择 **删除** 以删除 2019 年 8 月 7 日之后发布的 ER 配置的所有版本。

然后，验证配置树中是否有以下 ER 配置：

- **发票模型** ER 数据模型配置（最初命名为 **客户发票模型**）：

    - 版本 11 包含[数据模型](general-electronic-reporting.md#data-model-and-model-mapping-components) ER 组件的版本 10，用于表示开票业务域的数据结构。 此 ER 配置已导入，作为选择导入的 **Peppol 销售发票** ER 格式的上级。
    - 版本 50 包含数据模型 ER 组件的版本 31。 此 ER 配置已导入，作为 **发票模型映射** ER 模型映射配置的 2019 年 8 月 7 日版本的上级。

    ![“配置”页面上的发票模型 ER 数据模型配置。](./media/er-quick-start3-imported-solution1b1.png)

    > [!TIP]
    > 如果看不到该数据模型的版本 50，请打开全局存储库，然后导入 **发票模型映射** ER 配置的版本 50.19。

- **发票模型映射** ER 模型映射配置（最初命名为 **客户发票模型映射**）：

    - 版本 50.19 已导入，作为 **发票模型** ER 数据模型配置的版本 50 的最新实现。 它包含两个[模型映射](general-electronic-reporting.md#data-model-and-model-mapping-components) ER 组件，用于描述在运行时如何使用应用程序数据填充数据模型。

    ![“配置”页面上的发票模型映射 ER 模型映射配置。](./media/er-quick-start3-imported-solution1b2.png)

    > [!TIP]
    > 如果看不到该模型映射的版本 50.19，请打开全局存储库，然后导入 **发票模型映射** ER 配置的版本 50.19。

- **UBL 销售发票** ER 格式配置：

    - 版本 11.2 包含[格式](general-electronic-reporting.md#FormatComponentOutbound)和格式映射 ER 组件。 格式组件指定报表布局。 格式映射组件包含模型数据源，并指定如何在运行时使用此数据源填充报告布局。 该 ER 格式配置为生成通用商业语言 (UBL) 格式的电子发票。 它已导入，作为选择导入的 **Peppol 销售发票** ER 格式的父级。

- **Peppol 销售发票** ER 格式配置：

    - 版本 11.2.2 包含格式和格式映射 ER 组件，它们配置为生成泛欧洲 Public Procurement OnLine (PEPPOL) 格式的电子发票。

    ![“配置”页面上的 Peppol 销售发票 ER 格式配置。](./media/er-quick-start3-imported-solution1b3.png)

## <a name="configure-the-accounts-receivable-parameters"></a><a name="ConfigureAR1"></a>配置应收帐款参数

1. 转到 **应收帐款** \> **设置** \> **应收帐款参数**。
2. 在 **电子单据** 选项卡上，在 **电子报告** 快速选项卡上，在 **销售和普通发票** 字段中，选择 **Peppol 销售发票**。
3. 选择 **保存**。

![应收帐款参数页面上的电子文档选项卡。](./media/er-quick-start3-configure-ar1.png)

## <a name="configure-the-legal-entity-parameters"></a><a name="ConfigureLE"></a>配置法人参数

1. 转到 **组织管理** \> **组织** \> **法人**。
2. 对于所选的 **DEMF** 公司，在 **银行帐户信息** 快速选项卡上，在 **银行代号** 字段中，输入 **1234**。
3. 选择 **保存**。
4. 关闭 **法人** 页面。

## <a name="prepare-a-customer-record"></a><a name="ConfigureCustomer1"></a>准备客户记录

1. 转到 **应收帐款** \> **客户** \> **所有客户**。
2. 在 **所有客户** 页面上，选择 **DE-014** 客户帐户链接。

### <a name="add-a-customer-contact"></a>添加客户联系人

1. 转到 **应收帐款** \> **客户** \> **所有客户**。
2. 在“操作”窗格的 **客户** 选项卡上，在 **帐户** 组中，选择 **联系人**。
3. 选择 **添加联系人**。
4. 在 **联系人** 页面的 **名字** 字段中，打开查找，选择 **Adam Carter**，然后选择 **选择** 以关闭查找。
5. 选择 **保存**。
6. 关闭 **联系人** 页面。

### <a name="define-a-primary-contact"></a>定义主要联系人

1. 转到 **应收帐款** \> **客户** \> **所有客户**。
2. 在 **销售人口统计数据** 快速选项卡上，在 **主要联系人** 字段中，选择 **Adam Carter**。

### <a name="set-the-e-invoicing-option"></a>设置电子开票选项

1. 转到 **应收帐款** \> **客户** \> **所有客户**。
2. 在 **发票和交货** 快速选项卡上，将 **电子发票** 选项设置为 **是**。
3. 选择 **保存**。
4. 关闭 **所有客户** 页面。

## <a name="process-a-customer-invoice-by-using-the-standard-er-configurations"></a><a name="ProcessInvoice1"></a>使用标准 ER 配置处理客户发票

现在，您可以使用导入的标准 ER 配置以电子方式将普通发票发送给客户。

### <a name="add-a-new-invoice"></a>添加新发票

1. 转至 **应收帐款** \> **发票** \> **所有普通发票**。
2. 在 **普通发票** 页面上，选择 **新建**。
3. 在 **普通发票标题** 快速选项卡上，在 **客户帐户** 字段中，选择 **DE-014**。
4. 在 **发票行** 快速选项卡上，自动添加发票行。 在此行上，设置以下字段：

    - 在 **描述** 字段中，输入 **Notebook**。
    - 在 **主帐户** 字段中，选择 **401100**。
    - 在 **单位价格** 字段中，输入 **1000**。

5. 选择 **保存**。

![普通发票页面。](./media/er-quick-start3-add-invoice.png)

有关详细信息，请参阅[创建普通发票](../../../finance/accounts-receivable/create-free-text-invoice-new.md)。

### <a name="post-a-new-invoice"></a>过帐新发票

1. 转至 **应收帐款** \> **发票** \> **所有普通发票**。
2. 在 **普通发票** 页面上，在“操作”窗格上，选择 **过帐**。
3. 在 **过帐普通发票** 对话框中，选择 **确定**。

![普通发票详细信息页面。](./media/er-quick-start3-post-invoice.png)

### <a name="send-a-posted-invoice"></a>发送一个已过帐发票

1. 转至 **应收帐款** \> **发票** \> **所有普通发票**。
2. 在 **普通发票** 页面上，在“操作”窗格的 **单据** 组中，选择 **发送** \> **原始**。

    ![原始发票的预览。](./media/er-quick-start3-send-invoice.png)

3. 关闭 **普通发票** 页面。

### <a name="analyze-a-generated-e-invoice"></a>分析生成的电子发票

1. 转到 **组织管理** \> **电子报告** \> **电子报告作业**。
2. 在 **电子报告作业** 页面上，选择具有任务描述 **发送电子发票 XML** 的初始记录。
3. 选择 **显示文件** 以访问生成的文件列表。

    ![电子报告作业页面。](./media/er-quick-start3-jobs-list.png)

4. 选择 **打开** 以下载生成的电子发票 XML 文件。
5. 分析电子发票 XML 文件。 请注意，客户税架构当前由 **schemeID** 和 **schemeAgencyID** XML 属性表示。 另请注意，**cbc:CustomizationID** XML 元素当前包含以下文本：`urn:www.cenbii.eu:transaction:biicoretrdm010:ver1.0:# urn:www.peppol.eu:bis:peppol5a:ver1.0`。

    ![生成的电子发票 XML 文件的预览。](./media/er-quick-start3-e-invoice1.png)

## <a name="add-a-custom-database-field"></a><a name="AddCustomField"></a>添加自定义数据库字段

您可以使用[自定义字段](../../fin-ops/get-started/user-defined-fields.md)功能在当前的 Finance 实例中执行以下自定义：

- 通过添加为每个客户存储联邦纳税标识代码的新自定义数据库字段来自定义数据库结构。
- 通过添加可用于在新自定义数据库字段中输入税码值的新数据输入字段来自定义 **客户** 页面。

请按照以下步骤进行自定义。

1. 转到 **应收帐款** \> **客户** \> **所有客户**。
2. 在 **所有客户** 页面上，选择 **DE-014** 客户帐户链接。
3. 在 **常规** 快速选项卡上，右键单击 **语言** 字段下的任何空白区域，然后选择 **个性化：UpperGroup**。

    将突出显示 **常规** 快速选项卡的内容并将显示 **个性化** 菜单。

4. 在 **个性化** 菜单上，选择 **添加字段**。
5. 在 **添加列** 对话框中，选择 **创建新字段**。
6. 在 **创建新字段** 对话框中，在 **表单名称** 字段中，选择 **客户**。
7. 在 **名称前缀** 字段中，输入 **FederalTaxID**。

    > [!NOTE]
    > 整个字段名称已自动定义为 **FederalTaxID\_Custom**。

8. 在 **标签** 字段中，输入 **税号标识**。
9. 在 **类型** 字段中，选择 **文本**。
10. 在 **长度** 字段中，输入 **20**。
11. 选择 **保存**。
12. 在显示的消息框中，选择 **是** 以确认您要为 **客户** 表创建新的 **FederalTaxID** 字段输入。
13. 选择 **插入** 以 <a name="insert_custom_field"></a>向当前页面添加 **FederalTaxID\_Custom** 字段。

    ![所有客户页面。](./media/er-quick-start3-create-new-field.gif)

14. 关闭 **所有客户** 页面。

## <a name="refresh-the-er-metadata"></a><a name="RefreshERMetadata"></a>刷新 ER 元数据

您必须刷新 ER 元数据，才能使添加的自定义字段在 ER 模型映射设计器中[可见](electronic-reporting-er-configure-parameters.md#frequently-asked-questions)。

1. 转到 **组织管理** \> **电子报告** \> **重建表格引用**。
2. 在 **更新数据模型** 对话框中，选择 **确定**。

## <a name="design-the-custom-er-configurations"></a><a name="DesignCustomERConfigurations"></a>设计自定义 ER 配置

您可以使用 Microsoft 提供的 ER 配置来设计自定义 ER 配置，以便它们生成包含新税码的电子发票。

### <a name="customize-the-data-model-configuration"></a>自定义数据模型配置

作为电子报告功能顾问角色的用户，您可以设计自定义 ER 数据模型。

#### <a name="add-a-custom-data-model-configuration"></a>添加自定义数据模型配置

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页面上，在左侧窗格的配置树中，选择 **客户发票模型**。
3. 在操作窗格中选择 **创建配置**。
4. 在下拉对话框的 **新建** 字段中，选择 **从名称派生：客户发票模型，Microsoft** 以表示您的新自定义 ER 数据模型配置应基于 ER 数据模型配置。
5. 在 **名称** 字段中，输入 **发票模型 (Litware)**。
6. 选择 **创建配置** 以添加新 ER 配置。

现在，您可以使用 ER 数据模型设计器在 **草稿**[状态](general-electronic-reporting.md#component-versioning)下编辑 **发票模型 (Litware)** ER 配置的版本 50.1。

![“配置”页面上的 ER 配置的版本 50.1。](./media/er-quick-start3-added-custom-model.png)

#### <a name="configure-a-custom-data-model"></a>配置自定义数据模型

您必须通过添加新字段以提供联邦纳税标识码的值来修改自定义数据模型。 对于每种将使用此数据模型作为数据源的 ER 格式，此代码都是客户数据的一部分。

1. 在 **配置** 页面上，在左侧窗格的配置树中，选择 **发票模型 (Litware)**。
2. 在 **版本** 快速选项卡上，在 **草稿** 状态下选择所选 ER 数据模型配置的版本 **50.1**。
3. 在“操作”窗格上，为所选配置版本选择 **设计器**。
4. 在 **数据模型设计器** 页面的数据模型树中，选择 **客户信息（客户）**。
5. 选择 **新建**。
6. 在下拉对话框中，在 **作为以下项的新节点** 字段中，接受默认值 **活动节点的子节点**。
7. 在 **名称** 字段中，输入 **FederalTaxID\_Litware**。
8. 在 **物料类型** 字段中，接受默认值 **字符串**。
9. 选择 **添加**，然后选择 **保存**。

    ![数据模型设计器页面。](./media/er-quick-start3-add-data-model-field.png)

    > [!NOTE]
    > **标签** 和 **描述** 字段描述了新字段的目的。 您可以用多种语言填写这些字段。 有关详细信息，请参阅[在电子报告中设计多语言报告](er-design-multilingual-reports.md)。

10. 关闭 **数据模型设计器** 页。

#### <a name="complete-a-custom-data-model-configuration"></a>完成自定义数据模型配置

您必须[完成](general-electronic-reporting.md#component-versioning)自定义 ER 数据模型配置的版本 50.1 的工作以使其可用，以便可以添加其他自定义 ER 配置。

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页面上，在左侧窗格的配置树中，展开 **发票模型**，然后选择 **发票模型 (Litware)**。
3. 在 **版本** 快速选项卡上，选择 **更改状态** \> **完成**，然后选择 **确定**。

版本 50.1 的状态将从 **草稿** 更改为 **已完成**，并且该版本变为只读。 添加了一个新的可编辑版本 50.2，其状态为 **草稿**。 您可以使用此版本在自定义 ER 数据模型配置中进行进一步更改。

![在“配置”页面上完成的版本 50.1。](./media/er-quick-start3-completed-custom-model1.png)

### <a name="customize-the-model-mapping-configuration"></a>自定义模型映射配置

作为电子报告开发人员角色的用户，您可以设计自定义 ER 模型映射。

#### <a name="add-a-custom-model-mapping-configuration"></a>添加自定义模型映射配置

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页面上，在左侧窗格的配置树中，展开 **客户发票模型**，然后选择 **客户发票模型映射**。
3. 在操作窗格中选择 **创建配置**。
4. 在下拉对话框的 **新建** 字段中，选择 **从名称派生：客户发票模型映射，Microsoft** 以表示您的新自定义 ER 模型映射配置应基于 ER 模型映射配置。
5. 在 **名称** 字段中，输入 **发票模型映射 (Litware)**。
6. 在 **目标模型** 字段中，选择 **发票模型 (Litware)**。

    > [!IMPORTANT]
    > 此步骤非常重要。 如果忽略该步骤，将无法在配置的模型映射中使用自定义数据模型。

7. 选择 **创建配置** 以添加新 ER 配置。

![在“配置”页面上添加自定义模型映射配置。](./media/er-quick-start3-adding-custom-mapping.png)

#### <a name="configure-a-custom-model-mapping"></a>配置自定义模型映射

您必须修改自定义模型映射并指定应该如何在运行时使用应用程序数据填充自定义数据模型的自定义 **FederalTaxID\_Litware** 字段。

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页面上，在左侧窗格的配置树中，展开 **客户发票模型** \> **客户发票模型映射**，然后选择 **发票模型映射 (Litware)**。
3. 在操作窗格上，选择 **设计器**。
4. 在 **模型到数据源映射** 页面上，选择 **客户发票** 映射。

    ![模型到数据源映射页面。](./media/er-quick-start3-select-customer-mapping.png)

5. 选择 **设计器**。
6. 在 **模型映射设计器** 页面上，在 **数据源** 窗格中，展开表示 **CustInvoiceJour** 应用程序表的 **CustInvoiceJour** 数据源。
7. 在 **CustInvoiceJour** 下，展开 **关系** 以查看 **CustInvoiceJour** 表的多对一 (N:1) 类型的关系列表。
8. 在 **CustInvoiceJour** \> **关系** 下，展开 **客户 (CustTable)** 以访问 **客户 (CustTable)** 表的字段和关系。
9. 选择 [之前](#insert_custom_field)实现的 **FederalTaxID\_Custom** 数据源字段。
10. 在 **数据模型** 窗格中，展开 **客户信息（客户）**，然后选择 **FederalTaxID\_Litware** 数据模型字段。
11. 选择 **绑定**。

    ![模型映射设计器页面。](./media/er-quick-start3-customize-model-mapping.gif)

12. 选择 **保存**。
13. 关闭 **模型映射设计器** 页。
14. 关闭 **模型到数据源映射** 页。

#### <a name="complete-a-custom-model-mapping-configuration"></a>完成自定义模型映射配置

您必须[完成](general-electronic-reporting.md#component-versioning)自定义 ER 模型映射配置的版本 50.19.1 的工作以使其可供使用。

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页面上，在左侧窗格的配置树中，展开 **客户发票模型** \> **客户发票模型映射**，然后选择 **发票模型映射 (Litware)**。
3. 在 **版本** 快速选项卡上，选择 **更改状态** \> **完成**，然后选择 **确定**。

版本 50.19.1 的状态将从 **草稿** 更改为 **已完成**，并且该版本变为只读。 添加了一个新的可编辑版本 50.19.2，其状态为 **草稿**。 您可以使用此版本在自定义 ER 模型映射配置中进行进一步更改。

![在“配置”页面上完成的版本 50.19.1。](./media/er-quick-start3-completed-custom-mapping1.png)

> [!NOTE]
> 支持的配置[生命周期](general-electronic-reporting-manage-configuration-lifecycle.md)不包含数据库更改的生命周期。 如果您从当前 Finance 实例中导出 **发票模型映射 (Litware)** 配置的版本 50.19.1，并尝试将其导入在 **CustTable** 表中不包含自定义 **FederalTaxID\_Custom** 字段的另一个实例，将发生异常。 该异常指出导入的 ER 配置与目标 Finance 实例的元数据不兼容。

### <a name="customize-the-format-configuration"></a>自定义格式配置

作为电子报告功能顾问角色的用户，您可以设计自定义 ER 格式。

#### <a name="add-a-custom-format-configuration"></a>添加自定义格式配置

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页面上，在左侧窗格的配置树中，展开 **客户发票模型** \> **UBL 销售发票**，然后选择 **Peppol 销售发票**。
3. 在操作窗格中选择 **创建配置**。
4. 在下拉对话框的 **新建** 字段中，选择 **从名称派生：Peppol 销售发票，Microsoft** 以表示您的自定义 ER 格式配置应基于 ER 格式配置。
5. 在 **名称** 字段中，输入 **Peppol 销售发票 (Litware)**。
6. 在 **数据模型** 字段中，选择 **发票模型 (Litware)** 以使用自定义数据模型和模型映射组件。

    > [!NOTE]
    > 此步骤非常重要。 如果忽略该步骤，将无法在配置的格式中使用自定义数据模型。

7. 在 **数据模型** 字段中，选择 **InvoiceCustomer** 根定义。
8. 选择 **创建配置** 以添加新 ER 配置。

![在“配置”页面上添加自定义格式配置。](./media/er-quick-start3-adding-custom-format.png)

现在，您可以使用 ER Operations 设计器在 **草稿**[状态](general-electronic-reporting.md#component-versioning)下编辑 **Peppol 销售发票 (Litware)** ER 配置的版本 11.2.2.1。

![“配置”页面上的 ER 配置的版本 11.2.2.1。](./media/er-quick-start3-added-custom-format.png)

#### <a name="configure-a-custom-format"></a>配置自定义格式

您必须通过添加新格式元素以填写已开票客户的联邦纳税标识代码的值来修改自定义格式。

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页面上，在左侧窗格的配置树中，展开 **客户发票模型** \> **UBL 销售发票** \> **Peppol 销售发票**，然后选择 **Peppol 销售发票 (Litware)**。
3. 在操作窗格上，选择 **设计器**。
4. 在格式树中，展开 **XMLHeader** \> **发票** \> **cac:AccountingCustomerParty** \> **cac:Party** \> **cac:PartyTaxScheme** \> **cac:TaxScheme**，然后选择 **cbc:ID**。
5. 选择 **添加**，然后选择 **XML** \> **属性**。
6. 在 **组件属性** 对话框的 **名称** 字段中，输入 **FederalTaxID**。
7. 选择 **确定** 以添加新的格式元素，从而在生成的 XML 文件中创建新的 **FederalTaxID** XML 属性。
8. 在格式树中，在 **XMLHeader** \> **发票** \> **cac:AccountingCustomerParty** \> **cac:Party** \> **cac:PartyTaxScheme** \> **cac:TaxScheme** \> **cbc:ID** 下，选择 **FederalTaxID**。
9. 选择 **上移**。

![格式设计器页面上的新格式元素。](./media/er-quick-start3-customized-format.png)

#### <a name="configure-a-custom-format-mapping"></a>配置自定义格式映射

1. 在 **格式设计器** 页面的 **映射** 选项卡上，展开 **模型** 类型的 **发票** 数据源。
2. 在 **发票** 下，展开 **客户信息（客户）**，然后选择 **FederalTaxID\_Litware**。
3. 选择 **绑定**。

    ![“格式设计器”页面。](./media/er-quick-start3-customized-format-mapping.png)

4. 选择 **模型** 类型的 **发票** 数据源，然后选择 **编辑**。
5. 在 **版本** 字段中，选择自定义数据模型的版本 **1**，然后选择 **确定**。
6. 选择 **保存**。
7. 关闭 **格式设计器** 页。

#### <a name="complete-a-custom-format-configuration"></a>完成自定义格式配置

您必须[完成](general-electronic-reporting.md#component-versioning)自定义 ER 格式配置的版本 11.2.2.1 的工作以使其可供使用。

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页面上，在左侧窗格的配置树中，展开 **客户发票模型** \> **UBL 销售发票** \> **Peppol 销售发票**，然后选择 **Peppol 销售发票 (Litware)**。
3. 在 **版本** 快速选项卡上，选择 **更改状态** \> **完成**，然后选择 **确定**。

版本 11.2.2.1 的状态将从 **草稿** 更改为 **已完成**，并且该版本变为只读。 添加了一个新的可编辑版本 11.2.2.2，其状态为 **草稿**。 您可以使用此版本在自定义 ER 格式配置中进行进一步更改。

![在“配置”页面上完成的版本 11.2.2.1。](./media/er-quick-start3-completed-custom-format1.png)

## <a name="configure-the-accounts-receivable-parameters-to-start-to-use-custom-er-configurations"></a><a name="ConfigureAR2"></a>配置应收帐款参数以开始使用自定义 ER 配置

1. 转到 **应收帐款** \> **设置** \> **应收帐款参数**。
2. 在 **电子单据** 选项卡上，在 **电子报告** 快速选项卡上，在 **销售和普通发票** 字段中，选择 **Peppol 销售发票 (Litware)**。
3. 选择 **保存**。

![应收帐款参数页面、电子文档选项卡、电子报告快速选项卡。](./media/er-quick-start3-configure-ar2.png)

## <a name="update-a-customer-record-by-adding-a-federal-tax-identification-code"></a><a name="ConfigureCustomer2"></a>通过添加联邦纳税标识代码来更新客户记录

1. 转到 **应收帐款** \> **客户** \> **所有客户**。
2. 在 **所有客户** 页面上，选择 **DE-014** 客户帐户链接。
3. 在 **常规** 快速选项卡上，在 **税号标识** 字段中，输入 **LITWARE-6789**。
4. 选择 **保存**。

    ![DE-014 客户详细信息页面。](./media/er-quick-start3-added-tax-id-value.png)

5. 关闭 **所有客户** 页面。

## <a name="process-a-customer-invoice-by-using-custom-er-configurations"></a><a name="ProcessInvoice2"></a>使用自定义 ER 配置处理客户发票

### <a name="select-and-send-a-posted-invoice"></a>选择并发送已过帐发票

1. 转至 **应收帐款** \> **发票** \> **所有普通发票**。
2. 在 **普通发票** 页面上，选择您之前添加和过帐的发票。
3. 在“操作”窗格上，在 **单据** 组中，选择 **发送** \> **原始**。
4. 关闭 **普通发票** 页面。

### <a name="analyze-a-generated-e-invoice"></a>分析生成的电子发票

1. 转到 **组织管理** \> **电子报告** \> **电子报告作业**。
2. 在 **电子报告作业** 页面上，选择具有任务描述 **发送电子发票 XML** 的最新记录。
3. 选择 **显示文件** 以访问生成的文件列表。
4. 选择 **打开** 以下载生成的电子发票 XML 文件。
5. 分析电子发票 XML 文件。 请注意，根据您的自定义，除了 **schemeID** 和 **schemeAgencyID** XML 属性，客户税架构还包括自定义 **FederalTaxID** XML 属性。 此新 XML 属性的值由为已开票客户输入的 **LITWARE-6789** 税号标识指定。

    ![具有您的自定义的已生成电子发票 XML 文件的预览。](./media/er-quick-start3-e-invoice2.png)

## <a name="import-the-latest-versions-of-standard-er-configurations"></a><a name="ImportERConfigurations2"></a>导入标准 ER 配置的最新版本

若要使一组标准 ER 配置在 Finance 实例中保持[最新](general-electronic-reporting-manage-configuration-lifecycle.md)，只要它们在为该实例配置的 ER [存储库](general-electronic-reporting.md#Repository)中可用，就必须导入它们的新版本。

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **本地化配置** 页面的 **配置提供程序** 部分中，选择 **Microsoft** 磁贴，然后选择 **存储库** 查看 Microsoft 提供程序的存储库列表。
3. 在 **配置存储库** 页，选择 **全球** 类型的存储库，然后选择 **打开**。 如果提示您进行授权以连接到 Regulatory Configuration Service，请按照授权说明进行操作。
4. 在 **配置存储库** 页面上，在左侧窗格的配置树中，选择 **Peppol 销售发票** 格式配置。
5. 在 **版本** 快速选项卡上，选择所选 ER 格式配置的版本 **32.6.7**，该版本已发布以支持 PEPPOL BIS 3 格式的客户电子发票。 有关详细信息，请参阅 [KB4490320](https://support.microsoft.com/help/4490320/an-update-for-european-union-to-support-export-of-customers-electronic)。
6. 选择 **导入** 将所选版本从全局存储库下载到当前 Finance 实例。

![在配置存储库页面上选择的版本 32.6.7。](./media/er-quick-start3-import-solution2.png)

有关如何自动执行此过程的信息，请参阅[导入 ER 配置的更新版本](er-download-updated-versions-global-repo.md)。

### <a name="review-the-imported-er-configurations"></a>查看导入的 ER 配置

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **本地化配置** 页面的 **配置** 部分中，选择 **报告配置** 磁贴。
3. 展开 **配置组件** 快速选项卡。
4. 在左侧窗格的配置树中，展开 **发票模型**。 请注意，在导入的 ER 数据模型配置之一中，**客户发票模型** 的名称已更改为 **发票模型**。
5. 在左侧窗格的配置树中，展开 **发票模型映射**。 请注意，在导入的 ER 模型映射配置之一中，**客户发票模型映射** 的名称已更改为 **发票模型映射**。
6. 展开 **UBL 销售发票** \> **Peppol 销售发票**。

请注意，除了所选的 **Peppol 销售发票** ER 格式，还导入了其他必需的 ER 配置的最新版本。 因为将向全局存储库和 LCS 不断发布 ER 配置的新版本以使相应的 ER 解决方案符合新要求，因此导入了所需的数据模型配置及其模型映射配置的最新版本。

请确保最终配置树中有以下 ER 配置：

- **发票模型** ER 数据模型配置：

    - 版本 206（或更高版本）包含数据模型 ER 组件的版本 24（或更高版本），用于表示开票业务域的数据结构。 此 ER 配置已导入，作为可用的最新 **发票模型映射** ER 模型映射配置的上级。

    ![“配置”页面上的版本 206。](./media/er-quick-start3-imported-solution2b1.png)

- **发票模型映射** ER 模型映射配置：

    - 版本 206.132（或更高版本）已导入，作为 **发票模型** ER 数据模型配置的版本 206 的最新实现。 它包含若干模型映射 ER 组件，用于描述在运行时如何使用应用程序数据填充数据模型。

    ![“配置”页面上的版本 206.132。](./media/er-quick-start3-imported-solution2b2.png)

- **UBL 销售发票** ER 格式配置：

    - 版本 32.6 包含格式和格式映射 ER 组件。 格式组件指定报表布局。 格式映射组件包含模型数据源，并指定如何在运行时使用此数据源填充报告布局。 该 ER 格式配置为生成 UBL 格式的电子发票。 它已导入，作为选择导入的 **Peppol 销售发票** ER 格式的父级。

- **Peppol 销售发票** ER 格式配置：

    - 版本 32.6.7 包含格式和格式映射 ER 组件，它们配置为生成 PEPPOL 格式的电子发票。

    ![“配置”页面上的版本 32.6.7。](./media/er-quick-start3-imported-solution2b3.png)

## <a name="adopt-the-changes-to-the-new-standard-er-configurations-in-your-custom-er-configurations"></a><a name="RebaseCustomERConfigurations"></a>在您的自定义 ER 配置中采用对新标准 ER 配置所做的更改

### <a name="adopt-your-custom-er-data-model"></a>采用您的自定义 ER 数据模型

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页面上，在左侧窗格的配置树中，展开 **发票模型**，然后选择 **发票模型 (Litware)**。
3. 在 **版本** 快速选项卡上，对于所选数据模型配置的草稿版本 **50.2**，选择 **重定基本版本**。
4. 在 **目标版本** 字段中，确认基本 ER 数据模型配置的版本 **206** 的选择，然后选择 **确定**。

    自定义 ER 数据模型配置的草稿版本从 **50.2** 重新编号为 **206.2**，以表示它现在包含您的自定义，该自定义已与基本 ER 数据模型配置的最新版本 (206) 中的更改合并。

    > [!NOTE]
    > 重定操作可逆。 若要取消此重定基本版本，请在 **版本** 快速选项卡上选择 **发票模型 (Litware)** 模型的版本 **50.1**，然后选择 **获取此版本**。 将版本 206.2 重新编号回 **50.2**，草稿版本 50.2 的内容将与版本 50.1 的内容匹配。

5. 在 **版本** 快速选项卡上，选择 **更改状态** \> **完成**，然后选择 **确定**。

版本 206.2 的状态将从 **草稿** 更改为 **已完成**，并且该版本变为只读。 添加了一个新的可编辑版本 206.3，其状态为 **草稿**。 您可以使用此版本在自定义 ER 数据模型配置中进行进一步更改。

![在“配置”页面上完成的版本 206.2。](./media/er-quick-start3-completed-custom-model2.png)

### <a name="adopt-your-custom-er-model-mapping"></a>采用您的自定义 ER 模型映射

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页面上，在左侧窗格的配置树中，展开 **发票模型** \> **发票模型映射**，然后选择 **发票模型映射 (Litware)**。
3. 在 **版本** 快速选项卡上，对于所选模型映射配置的草稿版本 **50.19.2**，选择 **重定基本版本**。
4. 在 **目标版本** 字段中，确认基本 ER 模型映射配置的版本 **206.132** 的选择，然后选择 **确定**。

    自定义 ER 模型映射配置的草稿版本从 **50.19.2** 重新编号为 **206.132.2**，以表示它现在包含您的自定义，该自定义已与基本 ER 模型映射配置的最新版本 (206.132) 中的更改合并。

    请注意，发现了一些重定基本版本冲突。 现在，您必须手动解决这些冲突。

    ![“配置”页面上的重定基本版本冲突消息。](./media/er-quick-start3-rebase-conflicts-model-mapping1.png)

5. 在“操作”窗格上，选择 **设计器**，然后在映射列表中，选择 **客户发票**。
6. 对于每个重定基本版本冲突，选择 **保留自定义值**，因为您必须为提及的每个组件保留自定义数据模型的版本号。

    ![模型映射设计器页面上的重定基本版本冲突。](./media/er-quick-start3-rebase-conflicts-model-mapping2.png)

7. 选择 **保存**，然后关闭 **模型映射设计器** 页面。
8. 在映射列表中，选择 **项目发票**。
9. 对于每个重定基本版本冲突，选择 **保留自定义值**，因为您必须为提及的每个组件保留自定义数据模型的版本号。
10. 选择 **保存**，然后关闭 **模型映射** 页面。

    > [!NOTE]
    > 重定操作可逆。 若要取消此重定基本版本，请在 **版本** 快速选项卡上选择 **发票模型映射 (Litware)** 模型映射的版本 **50.19.1**，然后选择 **获取此版本**。 将版本 206.132.2 重新编号回 **50.19.2**，草稿版本 50.19.2 的内容将与版本 50.19.1 的内容匹配。

11. 在 **版本** 快速选项卡上，选择 **更改状态** \> **完成**，然后选择 **确定**。

版本 206.132.2 的状态将从 **草稿** 更改为 **已完成**，并且该版本变为只读。 添加了一个新的可编辑版本 206.132.3，其状态为 **草稿**。 您可以使用此版本在自定义 ER 模型映射配置中进行进一步更改。

![在“配置”页面上完成的版本 206.132.2。](./media/er-quick-start3-completed-custom-mapping2.png)

### <a name="adopt-your-custom-er-format"></a>采用您的自定义 ER 格式

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页面上，在左侧窗格的配置树中，展开 **发票模型** \> **UBL 销售发票** \> **Peppol 销售发票**，然后选择 **Peppol 销售发票 (Litware)**。
3. 在 **版本** 快速选项卡上，对于所选格式配置的草稿版本 **11.2.2.2**，选择 **重定基本版本**。
4. 在 **目标** 版本字段中，确认基本 ER 格式配置的版本 **32.6.7** 的选择，然后选择 **确定**。

    自定义 ER 格式配置的草稿版本从 **11.2.2.2** 重新编号为 **32.6.7.2**，以表示它现在包含您的自定义，该自定义已与基本 ER 格式配置的最新版本 (32.6.7) 中的更改合并。

    请注意，发现了一些重定基本版本冲突。 现在，您必须手动解决这些冲突。

5. 在操作窗格上，选择 **设计器**。
6. 对于每个重定基本版本冲突，选择 **保留自定义值**，因为您必须为提及的每个组件保留自定义数据模型的版本号。
7. 选择 **保存**。
8. 在 **映射** 选项卡上，选择 **模型** 类型的 **发票** 数据源，然后选择 **编辑**。
9. 在 **版本** 字段中，选择自定义数据模型的版本 **2**，然后选择 **确定**。
10. 选择 **保存**。

    > [!NOTE]
    > 重定操作可逆。 若要取消此重定基本版本，请在 **版本** 快速选项卡上选择 **Peppol 销售发票 (Litware)** 格式的版本 **11.2.2.1**，然后选择 **获取此版本**。 将版本 32.6.7.2 重新编号回 **11.2.2.2**，草稿版本 11.2.2.2 的内容将与版本 11.2.2.1 的内容匹配。

11. 关闭 **格式设计器** 页。
12. 在 **版本** 快速选项卡上，选择 **更改状态** \> **完成**，然后选择 **确定**。

版本 32.6.7.2 的状态将从 **草稿** 更改为 **已完成**，并且该版本变为只读。 添加了一个新的可编辑版本 32.6.7.3，其状态为 **草稿**。 您可以使用此版本在自定义 ER 格式配置中进行进一步更改。

![在“配置”页面上完成的版本 32.6.7.2。](./media/er-quick-start3-completed-custom-format2.png)

## <a name="process-a-customer-invoice-by-using-new-versions-of-the-custom-er-configurations"></a><a name="ProcessInvoice3"></a>使用自定义 ER 配置的新版本处理客户发票

### <a name="select-and-send-a-posted-invoice"></a>选择并发送已过帐发票

1. 转至 **应收帐款** \> **发票** \> **所有普通发票**。
2. 在 **普通发票** 页面上，选择您之前添加和过帐的发票。
3. 在“操作”窗格上，在 **单据** 组中，选择 **发送** \> **原始**。

    > [!NOTE] 
    > 因为您现在有两个版本的 **Peppol 销售发票 (Litware)** ER 格式配置，并且两个版本都没有[生效日期](general-electronic-reporting.md#component-date-effectivity)值，因此使用最新版本生成电子发票。

4. 关闭 **普通发票** 页面。

### <a name="analyze-a-generated-e-invoice"></a>分析生成的电子发票

1. 转到 **组织管理** \> **电子报告** \> **电子报告作业**。
2. 在 **电子报告作业** 页面上，选择具有任务描述 **发送电子发票 XML** 的最新记录。
3. 选择 **显示文件** 以访问生成的文件列表。
4. 选择 **打开** 以下载生成的电子发票 XML 文件。
5. 分析电子发票 XML 文件。 请注意，根据您的自定义，除了 **schemeID** 和 **schemeAgencyID** XML 属性，客户税架构仍然包含自定义 **FederalTaxID** XML 属性。 另外，因为基本 **UBL 销售发票** 格式的新版本中的更改已与您的自定义合并，因此 **cbc:CustomizationID** XML 元素的文本已从 `urn:www.cenbii.eu:transaction:biicoretrdm010:ver1.0:# urn:www.peppol.eu:bis:peppol5a:ver1.0` 更改为 `urn:cen.eu:en16931:2017#compliant#urn:fdc:peppol.eu:2017:poacc:billing:3.0`。

    ![具有自定义的已生成电子发票 XML 文件的预览。](./media/er-quick-start3-e-invoice3.png)

## <a name="additional-resources"></a>其他资源

- [电子申报概览](general-electronic-reporting.md)
- [从 Lifecycle Services 下载 ER 配置](download-electronic-reporting-configuration-lcs.md)
- [从 Configuration Service 的全局存储库下载 ER 配置](er-download-configurations-global-repo.md)
- [创建普通账单](../../../finance/accounts-receivable/create-free-text-invoice-new.md)
- [创建并使用自定义字段](../../fin-ops/get-started/user-defined-fields.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
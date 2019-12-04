---
title: 业务文档管理概览
description: 本主题介绍有关如何使用 ER 框架的业务文档管理功能的信息。
author: NickSelin
manager: AnnBe
ms.date: 08/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERSecurityAccessEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0a2fa6a7f6efef05862a3727a80122c22d591487
ms.sourcegitcommit: 4162d9ef4239c9d4e5297b8aaa903dd54f9cafc3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2019
ms.locfileid: "2824512"
---
# <a name="business-document-management-overview"></a>业务文档管理概览

业务用户使用[电子申报 (ER) 概述](general-electronic-reporting.md)根据各个国家/地区的法律要求配置传出文档的格式。 用户也可以定义数据流，以便指定在生成的文档中放置哪些数据。 ER 框架使用预定义的模板生成 Microsoft Office 格式（Excel 工作簿或 Word 文档）格式的传出文档。 将根据生成所需文档时配置的数据流使用必需数据填充模板。 可以在 ER 解决方案中发布配置的每种格式，以便生成特定传出文档。 这通过 ER 格式配置表示，其中可包含可用于生成不同传出文档的模板。 业务用户可使用此框架管理所需业务文档。

**业务文档管理**建立在 ER 框架的基础上，可供业务用户使用 Microsoft Office 365 服务或相应 Microsoft Office 桌面应用程序编辑业务文档模板。 对此类文档的编辑包括在不执行源代码更改和不进行新部署的情况下，更改业务文档设计和为更多数据添加占位符。 若要更新业务文档模板，无需了解 ER 框架。

> [!NOTE]
> 请注意，可通过业务文档管理修改用于生成订单、发票等之类业务文档的模板。修改模板和发布模板新版本之后，此版本用于生成必需的业务文档。 业务文档管理不可用于修改已生成的业务文档。

## <a name="supported-deployments"></a>支持的部署

现在，只能针对云部署实施业务文档管理功能。 如果此功能对您的本地部署至关重要，请通过在[灵感](https://experience.dynamics.com/ideas/)站点提供反馈来告知我们。

## <a name="supported-microsoft-office-applications"></a>支持的 Microsoft Office 应用程序

若要使用业务文档管理和 Microsoft Office 桌面应用程序以 Excel 或 Word 格式编辑文档，则必须安装 Microsoft Office 2010 或更高版本。 这在云和本地部署中受支持。

## <a name="business-document-availability"></a>业务文档可用性

公共预览版中支持采用基于 Excel 的模板的以下报告：

**应收帐款**（2019 年 8 月）

- 销售预付款发票
- 销售订单装箱单

**应付帐款**（2019 年 8 月）

- 采购预付款发票
- 采购订单
- 采购订单装箱单

将支持更多报告。 将单独发送有关更多报告的特殊通知。 

[Word 和 Excel 中的可配置业务文档报告](https://docs.microsoft.com/en-us/dynamics365-release-plan/2019wave2/dynamics365-finance-operations/configurable-business-documents-reporting-word-excel-pdf#feature-details)中提供了为 2019 年 10 月发行版规划的所有报告的完整列表。 若要了解有关此功能的详细信息，请完成本主题中的示例。

## <a name="configure-er-parameters"></a>配置 ER 参数

因为业务文档管理建立在 ER 框架的基础上，所以必须配置 ER 参数，才能开始使用业务文档管理。 为此，需要按照[配置电子报告 (ER) 框架](electronic-reporting-er-configure-parameters.md)中的说明设置 ER 参数。 还需要按照[创建配置提供商并将其标记为有效](tasks/er-configuration-provider-mark-it-active-2016-11.md)中的说明添加新的配置提供商。

![ER 工作区](./media/BDM-Overview-ERSetting.png)

## <a name="import-er-solutions"></a>导入 ER 解决方案

在此过程的示例中使用了示例 ER 配置。 您必须将包含业务文档模板的 ER 配置导入到 Dynamics 365 Finance 的当前实例中，模板可以使用业务文档管理进行编辑。 下载以下文件，然后存储在本地，以完成此过程。

**示例 ER 客户开票解决方案**

| **文件**                                  | **内容**                                |
|-------------------------------------------|--------------------------------------------|
| Customer invoicing model.version.2.xml    | [ER 数据模型配置](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Customer FTI report (GER).version.2.3.xml | [普通发票 ER 格式配置](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

**示例 ER 付款检查解决方案**

| **文件**                                  | **内容**                                |
|-------------------------------------------|--------------------------------------------|
| Model for cheques.version.10.xml          | [ER 数据模型配置](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Cheques printing format.version.10.9.xml  | [付款支票 ER 格式配置](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

**示例 ER 外贸解决方案**

| **文件**                                  | **内容**                                |
|-------------------------------------------|--------------------------------------------|
| Intrastat model.version.1.xml             | [ER 数据模型配置](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Intrastat report.version.1.9.xml          | [内部统计控制报表 ER 格式配置](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

使用以下过程导入每个文件。 导入相应 ER *格式*配置之前，导入上表中每个 ER 解决方案的 ER *数据模型*配置。

1. 打开**组织管理** \> **电子申报** \> **配置**页面。
2. 在页面顶部，选择**交易**。
3. 选择**从 XML 文件加载**。
4. 选择**浏览**以加载所需的 XML 文件。
5. 选择**确定**以确认导入配置。

![ER 配置页](./media/BDM-Overview-ERSolutions.png)


或者，您可以从 Microsoft Dynamics Lifecycle Service (LCS) 导入正式发布的 ER 格式配置。 例如，要完成此过程，您可以导入**普通发票(Excel)** ER 格式配置的最新版本。 相应的 ER 数据模型和 ER 模型映射配置将自动导入。

![LCS 共享资产库内容页面](./media/BDM-Overview-SharedAssetLibrary.png)

有关导入 ER 配置的详细信息，请参阅[管理 ER 配置生命周期](general-electronic-reporting-manage-configuration-lifecycle.md)。


## <a name="enable-business-document-management"></a>启用业务文档管理

若要启动业务文档管理，需要打开**功能管理**工作区，并启用**业务文档管理**功能。

使用以下过程为所有法人启用业务文档管理。

1. 打开**功能管理**工作区。
2. 在**新建**选项卡上，选择列表中的**业务文档管理**功能。
3. 选择**立即启用**以打开所选功能。
4. 刷新页面以访问新功能。

>[!NOTE]
> 另外，您需要启用**类似于 Office 的业务文档管理 UI 体验**，以使用新的业务文档管理界面

![“功能管理”工作区](./media/BDM-Overview-FMEnabling.png)

有关激活新功能的详细信息，请参阅[功能管理概述](../../fin-ops/get-started/feature-management/feature-management-overview.md)。

## <a name="configure-parameters"></a>配置参数

使用以下部分中的信息为业务文档管理设置基本参数。

### <a name="prerequisites-for-parameter-setup"></a>参数设置的先决条件
必须先在文档管理框架中设置必需的文档类型，才能设置业务文档管理。 此文档类型用于指定 Office 格式（Excel 和 Word）文档的临时存储，用作 ER 报表的模板。 可使用 Office 桌面应用程序编辑临时存储模板。

对于此文档类型，必须选择以下属性值。

| **属性名称**  | **属性值**   |
|---------------------|-----------------------|
| 分类               | 附加文件           |
| 组合               | 文件                  |
| 场所            | SharePoint            |

有关如何设置必需文档管理参数和文档类型的信息，请参阅[配置文档管理](../../fin-ops/organization-administration/configure-document-management.md)。

![设置文档管理文档类型](./media/BDM-Overview-DMSetting.png)

### <a name="set-up-parameters"></a>设置参数

可在**业务文档参数**页设置基本业务文档管理参数。 只有特定用户才可以访问此页。 这包括：

- 已为其分配了**系统管理员**角色的用户。
- 已为其分配了为执行**维护业务文档管理参数**（AOT 名称为 **ERBDMaintainParameters**）职责而配置的任何角色的用户。

使用以下过程为所有法人设置基本参数。

1. 以具有**业务文档参数**页面访问权限的用户的身份登录。
2. 转到**组织管理** \> **电子申报** \> **业务文档管理** \> **业务文档参数**。
3.  在**业务文档参数**页**附件**选项卡的 **SharePoint 文档类型**字段中，定义应该用于在使用 Office 桌面应用程序编辑 Office 格式的模板时，临时存储此类模板的文档类型。 

> [!NOTE]
> 此参数仅支持使用 SharePoint 位置配置的文档类型。

![设置业务文档管理参数](./media/BDM-Overview-BDMSetting.png)

所选文档类型特定于公司，将在当用户在为其配置了所选文档类型的公司中使用业务文档管理时使用。 当用户在另一家公司使用业务文档管理时，如果尚未为此公司配置文档类型，将使用选择的同一个文档类型。 如果已配置了文档类型，则使用此文档类型，而不是在 **SharePoint 文档类型**字段中选择的文档类型。

## <a name="configure-access-permissions"></a>配置访问权限

默认情况下，在未启用业务文档管理权限的访问时，每位可访问业务文档管理工作区的用户都可以看到所有可用 ER 解决方案模板。 业务文档管理工作区将仅显示 ER 格式配置中的模板和带有**业务文档类型**标记的模板。

![ER 配置页](./media/BDM-Overview-ERFormatTags.png)

可通过配置访问权限来限制业务文档管理工作区中的可用模板的列表。 这在以下情况下可能非常重要：使用不同模板为不同业务域（功能区）生成业务文档，并且要允许特定用户访问要在业务文档管理工作区中进行编辑的不同模板。

可在**配置权限的配置器**中设置业务文档管理访问权限。 只有以下用户才可以访问此页：

- 已为其分配了**系统管理员**角色的用户。
- 已为其分配了为执行**配置权限以访问要编辑的业务文档模板**（AOT 名称为 **ERBDTemplatesSecurity**）职责而配置的其他任何角色的用户。

使用以下过程为所有法人设置业务文档管理访问权限。

1. 以具有**访问权限配置器**页面访问权限的用户的身份登录。
2. 转到**组织管理** \> **电子申报** \> **业务文档管理** \> **管理访问权限**。

    请注意有关当前未启用业务文档管理访问权限的使用的通知。

    ![“业务文档管理访问权限配置器”页面](./media/BDM-Overview-TemplatesAccess1.png)

    通过此设置，已为其分配了为执行**管理业务文档模板**（AOT 名称为 **ERBDManageTemplates**）职责而配置的任何安全角色的每位用户都可以打开业务文档管理工作区，并可编辑所有可用模板。

    下图显示业务文档管理工作区中为其分配了**应收帐款员**角色的用户的可用模板。 通过使用当前访问权限设置，用户可从不同功能区（包括开票、法规报告和付款）编辑业务文档模板。

    ![业务文档管理工作区页](./media/BDM-Overview-TemplatesForAlice1.png)

3. 在**访问权限配置器**页，选择**访问权限设置**。
4. 在**用于编辑模板的访问权限的设置**对话框中，启用**应用已配置的访问权限**选项。
5. 选择**确定**以确认已启用业务文档管理访问权限。

    ![“配置业务文档管理访问权限”页面](./media/BDM-Overview-TemplatesAccess2.png)

6. 选择**添加**以输入必须要为其配置用于访问业务文档管理模板的权限的新业务角色。
7. 在**安全角色**对话框中，选择**应收帐款员**角色，然后选择**确定**以确认选择的角色。
8. 在**每个配置标记的访问权限**选项卡上，选择**新建**。
9. 在**标记类型**字段中，选择**功能区**，然后在 **ID** 字段中选择**开票**。
10. 选择**保存**以存储为所选角色配置的访问权限。

    当前设置意味着对于为其分配了**应收帐款员**角色且正在执行**管理业务文档模板**（AOT 名称为 **ERBDManageTemplates**）职责的任何用户，可在业务文档管理工作区中编辑**功能区**标记值为**开票**的 ER 格式配置模板。

11. 从当前页右侧切换**相关信息**窗格。 **相关信息**窗格显示如何应用配置的访问权限，包括为其分配了**应收帐款员**角色的用户可使用哪些 ER 配置模板。

    ![“配置业务文档管理访问权限”页面](./media/BDM-Overview-TemplatesAccess3.png)

12. 在**每个配置的访问权限**选项卡上，选择**添加**选项。
13. 在**选择配置**对话框中，标记**内部统计报表** ER 格式配置。
14. 选择**确定**以确认所选配置的条目，然后选择**保存**以存储为所选角色配置的访问权限。

当前设置意味着对于为其分配了**应收帐款员**角色且正在执行**管理业务文档模板**（AOT 名称为 **ERBDManageTemplates**）职责的任何用户，可在业务文档管理工作区中编辑以下模板：

- **功能区**标记的值为**开票**的模板。
- 来自**每个配置的访问权限**选项卡上列出的 ER 格式配置的模板（此示例中，为来自**法定申报**域的**内部统计报表**格式配置的模板）。

![“配置业务文档管理访问权限”页面](./media/BDM-Overview-TemplatesAccess4.png)

下图显示业务文档管理工作区向为其分配了**应收帐款员**角色的用户提供的模板。 采用当前业务文档管理访问权限设置的用户可编辑**开票**域和**内部统计报表** ER 格式配置中的业务文档模板。 **应收帐款员**角色不可访问**付款**域中的模板。

![业务文档管理工作区页](./media/BDM-Overview-TemplatesForAlice2.png)

> [!NOTE]
> **每个配置的访问权限**规则通过使用 ER 格式配置的唯一标识 ID 来存储。 这意味着如果删除引用这些规则的 ER 配置，不会删除这些规则。 将删除的配置导入回此实例时，这些规则将再次引用这些配置。 再次导入删除的配置之后，无需再次设置规则。

## <a name="use-business-document-management-to-edit-templates"></a>使用业务文档管理编辑模板

业务用户可在业务文档管理工作区中访问要编辑的业务文档模板。 只有以下用户可访问业务文档管理工作区：

- 已为其分配了**系统管理员**角色的用户。
- 已为其分配了为执行**管理业务文档模板**（AOT 名称为 **ERBDManageTemplates**）职责而配置的任何角色的用户。

在业务文档管理工作区中使用以下过程编辑普通发票模板。 完成此过程之前，必须先完成本主题中前文的所有过程。

1. 以具有业务文档管理工作区访问权限的用户的身份登录。
2. 打开业务文档管理工作区。

![业务文档管理工作区页](./media/BDM-Overview-EditingTemplate1.png)

**模板**选项卡中提供所选模板的内容。 选择**详细信息**选项卡以查看所选模板的详细信息，以及此模板所在 ER 格式配置的详细信息。 请注意，所有模板的状态均为**已发布**，并且其**修订**列中不包含任何详细信息。 这表示当前未在编辑这些模板。

### <a name="initiate-editing-templates-owned-by-your-configuration-provider"></a>开始编辑配置提供商负责的模板

1. 在业务文档管理工作区中，选择列表中的 **Cheques printing format** 模板。
2. 选择**详细信息**选项卡。

![业务文档管理工作区页](./media/BDM-Overview-EditingTemplate2.png)

将为所选模板提供**编辑模板**选项。 有效 ER 配置提供商（此示例中为 **Litware, Inc.**）负责的 ER 格式配置中的模板始终可使用此选项。 如果选择了**编辑模板**，则可编辑基础 ER 格式配置草稿版本中的现有模板。

### <a name="initiate-editing-templates-owned-by-other-providers"></a>开始编辑其他提供商负责的模板

1. 在业务文档管理工作区中，选择**新建文档**。

![业务文档管理工作区页](./media/BDM_overview_new_template1.png)

2. 选择您要用作模板的文档。

![业务文档管理工作区页](./media/BDM_overview_new_template2.png)

3. 单击**创建文档**
4. 如果需要，在**标题**字段中更改可编辑模板的标题。 将把此文本用于命名自动创建的 ER 格式配置。 请注意，将自动标记此配置 (**Customer FTI report (GER) Copy**) 的草稿版本（其中将包含编辑后的模板），以便为当前用户运行此 ER 格式。 同时，将使用来自基本 ER 格式配置的未经修改原始模板为其他任何用户运行此 ER 格式。
5. 在**名称**字段中，更改将自动创建的可编辑模板第一个修订的名称。
6. 在**注释**字段中，更改自动创建的可编辑模板修订的注解。
7. 选择**确定**以确认开始执行编辑流程

![业务文档管理工作区页](./media/BDM_overview_new_template3.png)

另一个提供商（此示例中为 Microsoft）提供的 ER 格式配置中的模板始终可使用**新建文档**选项。 当您单击**新建文档**时，您会看到当前提供商和其他提供商拥有的所有模板。 选择模板后，将打开它进行编辑。 然后将把编辑后的模板存储在自动生成的新 ER 格式配置中。

### <a name="start-editing-a-template"></a>开始编辑模板

1. 从所选模板选择**编辑文档**。
2. 在**名称**字段中，更改将自动创建的可编辑模板第一个修订的名称。
3. 在**注释**字段中，更改自动创建的可编辑模板修订的注解。

    ![业务文档管理工作区页](./media/BDM_overview_new_template4.png)

5. 选择**确定**以确认开始执行编辑流程。

将打开 **BDM 模板编辑器**页。 可通过使用 Office 365 在线编辑所选模板。

![业务文档管理工作区页](./media/BDM-Overview-EditingLayout1.png)

### <a name="edit-a-template-in-office-365"></a>在 Office 365 中编辑模板

通过使用 Office 365 的功能修改模板。 例如，在 Office Online 中，将模板标题中的字段提示的字体从**常规**更改为**加粗**。 将自动存储为 ER 框架配置的主模板存储（默认情况下为 Azure blob 存储）中存储的可编辑模板的这些更改。

![业务文档管理模板编辑器页面](./media/BDM-Overview-EditingLayout2.png)

### <a name="edit-a-template-in-the-office-desktop-application"></a>在 Office 桌面应用程序中编辑模板

1. 选择**在桌面应用程序中打开**选项，以便使用 Office 桌面应用程序的功能（此示例中为 Excel）修改模板。 将把可编辑模板从永久存储复制到业务文档管理参数中配置为 SharePoint 文件夹的临时存储。
2. 确认要在 Office 桌面的 Excel 应用程序中从临时文件存储打开模板。

    ![业务文档管理工作区页](./media/BDM-Overview-EditingLayout3.png)

3. 修改模板。 例如，通过将颜色从**黑色**更改为**蓝色**，更改模板标题中的字段提示的字体。

    ![业务文档管理模板编辑器页面](./media/BDM-Overview-EditingLayout4.png)

4. 在 Excel 桌面应用程序中选择**保存**以将模板更改存储到临时存储中。

    ![业务文档管理模板编辑器页面](./media/BDM-Overview-EditingLayout5.png)

5. 关闭 Excel 桌面应用程序。
6. 选择**同步已存储副本**将临时模板存储同步到永久模板存储。

> [!NOTE]
> 临时文件存储中的可编辑模板副本将仅保留在当前模板编辑会话中。 通过关闭 **BDM 模板编辑器**页完成会话时，将删除此副本。 如果调整了临时文件存储中的模板，但是未选择**同步已存储副本**，则在尝试关闭 **BDM 模板编辑器**页时，将有一条消息询问您是否要存储引入的更改。 如果要将对模板的更改保存到永久文件存储，请选择**是**。

### <a name="validate-a-template"></a>验证模板

1. 在 **BDM 模板编辑器**页中，选择**检查问题**以针对基础 ER 格式配置验证修改后的模板。 按照建议（如果有）让模板与基本 ER 格式配置中的格式结构一致。
2. 选择**显示格式**以查看基本 ER 格式配置中必须与可编辑模板一致的当前格式结构。 
3. 选择**隐藏格式**以关闭窗格。

    ![BDM 模板编辑器页面](./media/BDM-Overview-EditingTemplate6.png)

4. 关闭 **BDM 模板编辑器**页。

将在**模板**选项卡上显示更新后的模板。请注意，现在，编辑后的模板的状态为**草稿**，并且当前修订不再为空。 这意味着此模板的编辑过程已开始。

![业务文档管理工作区页](./media/BDM-Overview-EditingTemplate5.png)

### <a name="test-the-modified-template"></a>测试修改后的模板 

1. 在应用程序中，切换到公司 **USMF**。
2. 转至**应收帐款** \> **发票** \> **所有普通发票**。
3. 选择 **FTI-00000002** 发票，然后选择**打印管理**。
4. 选择**模块 - 应收帐款** \> **文档** \> **普通发票** \> **原始凭证**级别以指定要处理的发票范围。
5. 在**报表格式**字段中，为指定的文档级别选择 **Customer FTI report (GER) Copy** ER 格式。

    ![打印管理设置页](./media/BDM-Overview-TestRun1.png)

6. 按 **Escape** 关闭当前页。
7. 选择**打印**，然后单击**已选择**。
8. 下载文档，然后使用 Excel 桌面应用程序打开。

![普通发票页面](./media/BDM-Overview-TestRun2.png)

修改后的模板将用于为所选物料生成普通发票报表。 若要分析为模板进行的更改对此报表造成了哪些影响，可以在一个应用程序会话中修改模板之后，立即在另一个应用程序会话中运行此报表。

### <a name="create-an-alternative-template-revision"></a>创建备用模板修订

1. 打开 **BDM 模板编辑器**页，然后选择 **Customer FTI report (GER) Copy** 模板。
2. 在**修订**选项卡上，选择**新建**。
3. 如果需要，在**名称**字段中，更改第二个修订的名称，并以当前第一个有效修订为基础。
4. 如果需要，在**注释**字段中，更改自动创建的可编辑模板修订的注解。

    ![业务文档管理工作区页](./media/BDM-Overview-AddRevision.png)

    您创建了永久模板存储中已存储的模板的新修订。 现在可以继续编辑当前选择为活动的第二个修订的模板。

5. 选择第一个修订，然后选择**设置有效**。 任何时候如果要返回为模板的另一个修订，可选择此修订为有效。
6. 选择第二个修订，然后选择**删除**。
7. 选择**确定**以确认您要删除所选修订。 可删除任何不再需要的非有效修订。

### <a name="delete-a-modified-template"></a>删除修改后的模板

1. 在 **BDM 模板编辑器**页中，选择**模板**选项卡。
2. 选择**删除**。
3. 如果选择**确定**以确认删除，将删除采用修改后模板的 **Customer FTI report (GER) Copy** ER 格式。 选择**取消**以浏览其他选项。

### <a name="revoke-changes-of-template"></a>撤消对模板的更改

编辑当前有效提供程序负责的 ER 格式中的模板时，将为您提供用于撤消对模板的更改的选项。

![业务文档管理工作区页](./media/BDM-Overview-RevokeChanges.png)

1. 在 **BDM 模板编辑器**页中，选择**模板**选项卡。
2. 选择**撤消**。
3. 如果选择**确定**以撤消对模板的更改，将把修改后的模板替换为原始模板，并删除所有更改。 撤消对模板的更改之后，可以删除模板。 选择**取消**以浏览其他选项。

### <a name="publish-a-modified-template"></a>发布修改后的模板
1. 在 **BDM 模板编辑器**页中的**模板**选项卡上，选择**发布**。
2. 如果选择**确定**以确认发布，将把包含修改后的模板的派生 **Customer FTI report (GER) Copy** ER 格式的草稿版本标记为已完成。 其他用户将可使用修改后的模板。 此 ER 格式的完成版本将仅保留模板的最后一个有效版本。 将删除其他修订。 选择**取消**以浏览其他选项。

## <a name="frequently-asked-questions"></a>常见问题

#### <a name="i-selected-edit-document-but-instead-of-opening-the-bdm-template-editor-page-in-finance-and-operations-i-have-been-sent-to-the-office-365-web-page"></a>我选择了**编辑文档**，但是结果不是在 Finance and Operations 中打开 **BDM 模板编辑器**页，而是转到了 Office 365 网页。
这是 Office 365 重定向的已知问题。 首次登录 Office 365 时会出现此情况。 若要解决此问题，请选择浏览器的**后退**按钮返回。

#### <a name="i-understand-how-to-edit-a-template-by-using-office-365-in-the-first-application-session-and-how-to-use-the-template-in-the-second-application-session-adjusting-the-template-to-see-how-my-changes-affect-the-generated-business-document-can-i-do-this-using-the-office-desktop-application"></a>我知道如何在第一个应用程序会话中通过使用 Office 365 编辑模板，以及如何在第二个应用程序会话中使用模板，并调整模板来查看我的更改对生成的业务文档有何影响。 我可以使用 Office 桌面应用程序执行此操作吗？
是的，可以。 在第一个应用程序会话中，选择**在桌面应用程序中打开**。 将把您的模板存储到临时文件存储中，并在 Office 桌面应用程序中打开。 接下来，完成以下步骤在生成的业务文档中预览模板更改：

1. 通过使用 Office 桌面应用程序在模板中进行更改。
2. 在 Office 桌面应用程序中选择**保存**。
3. 在第一个应用程序会话的 **BDM 模板编辑器**页中，选择**同步已存储副本**。
4. 在第二个应用程序会话中执行此模板 ER 格式。

#### <a name="i-get-the-error-value-cannot-be-null-parameter-name-externalid-when-i-select-open-in-desktop-app-how-do-i-work-around-this"></a>我在执行以下操作时，发生了“值不能为空。 参数名称：externalId”错误：选择**在桌面应用程序中打开**。 应该如何解决这个问题？ 
您当前登录的应用程序实例所在 Azure AD 域很可能不是用于部署此实例的 Azure AD 域。 因为 SharePoint 服务（用于存储模板来使其可通过使用 Office 桌面应用程序进行编辑）属于相同域，所以我们无权访问 SharePoint 服务。 若要解决此问题，请使用具有正确 Azure AD 域的用户的凭据登录当前实例。

## <a name="additional-resources"></a>其他资源

[电子申报 (ER) 概览](general-electronic-reporting.md)

[ER 设计以 OPENXML 格式生成报表的配置（2016 年 11 月）](tasks/er-design-reports-openxml-2016-11.md)

[设计 ER 配置以生成 Word 格式的报表](tasks/er-design-configuration-word-2016-11.md)

[使用 ER 在您生成的文档中嵌入图像和形状](electronic-reporting-embed-images-shapes.md)

[配置电子申报 (ER) 以便将数据导入 Power BI](general-electronic-reporting-report-configuration-get-data-powerbi.md)
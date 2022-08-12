---
title: 管理电子报告 (ER) 配置生命周期
description: 本文介绍如何管理 Dynamics 365 Finance 的电子报告 (ER) 配置的生命周期。
author: NickSelin
ms.date: 07/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d6a64908a167c09089a95f1d3faa825dcc63f064
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/01/2022
ms.locfileid: "9109073"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a>管理电子报告 (ER) 配置生命周期

[!include [banner](../includes/banner.md)]

本文介绍如何管理 Dynamics 365 Finance 的电子报告 (ER) 配置的生命周期。

## <a name="overview"></a>概述

电子申报 (ER) 是一个引擎，可支持法律要求的和国家/地区特定的电子文档。 一般来说，ER 假设执行一个电子文档的以下任务的能力。 有关详细信息，请参阅[电子申报 (ER) 概览](general-electronic-reporting.md)。

- 设计电子文件的模板：

    - 标识可在此文档中提供的所需数据源：

        - 基础数据（如数据表、数据实体和类）。
        - 处理特定的属性（如执行日期和时间，以及时区）。
        - 用户输入参数（在运行时由最终用户指定）。

    - 定义所需文档的元素及其拓扑结构以指定最终文档格式。
    - 配置从所选数据源到定义的文档元素的所需数据流（通过绑定到文档格式组件的数据源）并指定流程控制逻辑。

- 将一个模板变为可用，以便可以在其他实例中使用：

    - 将创建的文档模板转换为 ER 配置，并且将当前应用程序实例中的配置导出为可以存储在本地或 Lifecycle Services (LCS) 中的 XML 包。
    - 将 ER 配置转换为应用程序文档模板。
    - 将存储在本地或 LCS 中的 XML 包导入到当前实例。

- 自定义电子文档模板：

    - 从 LCS 将模板作为 ER 配置导入到当前实例。
    - 设计自定义版本的 ER 配置，并保留对其基础版本的引用。

- 将模板与特定业务流程集成，以使它在应用程序中可用：

    - 通过在流程相关参数中引用该配置来配置设置以便应用程序开始使用 ER 配置。 例如，引用特定应付帐款付款方式中的 ER 配置以生成用于处理发票的电子付款消息。

- 使用特定的业务流程中的模板：

    - 在特定的业务流程中运行 ER 配置。 例如，要在选择了引用 ER 配置的付款方式时生成用于处理发票的电子付款消息。

## <a name="concepts"></a>概念
以下角色和相关活动与 ER 配置生命周期相关。

| 角色                                       | 活动                                                      | 说明 |
|--------------------------------------------|-----------------------------------------------------------------|-------------|
| 电子申报功能顾问 | 创建和管理 ER 组件（模型和格式）。           | 设计 ER 域特定数据模型、设计电子文档的所需模板并将它们进行相应绑定的业务人员。 |
| 电子申报开发人员             | 创建和管理数据模型映射。                          | 选择所需的 Finance 数据源并将它们绑定到 ER 域特定数据模型的专业人员。 |
| 会计主管                      | 配置引用 ER 项目的流程相关设置。 | 例如，允许 ER 配置设置用于特定应付帐款付款方式来生成用于处理发票的电子付款消息的 **会计主管** 角色。 |
| 应付帐款付款员            | 使用特定业务流程中的 ER 项目。                | 例如，允许基于为特定付款方式配置的 ER 格式为处理发票生成电子付款消息的 **应付帐款付款员**。 |

## <a name="er-configuration-development-lifecycle"></a>ER 配置开发生命周期
出于以下与 ER 相关的原因，我们建议您在开发环境中将 ER 配置设计为单独的财务和运营实例：

- 担当 **电子申报开发人员** 角色或 **电子申报功能顾问** 角色的用户可编辑配置，并运行配置以进行测试。 此情况可能会导致调用类和表的方法，可能对业务数据和实例的性能产生负面影响。
- 在调用作为 ER 配置的 ER 数据源的类和表的方法时，不受入口点和记录的公司内容的限制。 因此，担当 **电子申报开发人员** 角色或 **电子申报功能顾问** 角色的用户可访问业务敏感数据。

在开发环境中设计的 ER 配置可[上传](#data-persistence-consideration)到测试环境以进行配置评估（适当的流程集成、结果的正确性、性能）和质量保证（例如角色驱动的访问权限的正确性和职责划分）。 启用 ER 配置交换的功能可以用于此目的。 已审核的 ER 配置可上传到 LCS 以与服务订阅者共享，它们也可[导入](#data-persistence-consideration)到生产环境以供内部使用。

![ER 配置生命周期。](./media/ger-configuration-lifecycle.png)

## <a name="data-persistence-consideration"></a>数据持久性注意事项

您可以将 ER [配置](general-electronic-reporting.md#Configuration)的不同[版本](general-electronic-reporting.md#component-versioning)单独[导入](tasks/er-import-configuration-lifecycle-services.md)到您的 Finance 实例。 导入新版本的 ER 配置时，系统将控制此配置的草稿版本的内容：

- 当导入的版本低于当前 Finance 实例中此配置的最高版本时，此配置的草稿版本内容将保持不变。
- 当导入的版本高于当前 Finance 实例中此配置的任何其他版本时，导入版本的内容将复制到此配置的草稿版本，以使您可以继续编辑最后完成的版本。

如果此配置由当前已激活的配置 [提供商](general-electronic-reporting.md#Provider)负责，您可以在 **配置** 页面的 **版本** 快速选项卡上看到此配置的草稿版本（**组织管理** > **电子报告** > **配置**）。 您可以选择配置的草稿版本，然后通过使用相关的 ER 设计器[修改](er-quick-start2-customize-report.md#ConfigureDerivedFormat)其内容。 在编辑 ER 配置的草稿版本后，其内容不再与当前 Finance 实例中此配置的最高版本的内容相匹配。 若要防止更改丢失，系统将显示一个错误，即由于此配置的版本高于当前 Finance 实例中此配置的最高版本，因此导入无法继续。 当发生这种情况时，例如，对于格式配置 **X**，将显示 **格式“X”版本未完成** 错误。

若要撤消在草稿版本中引入的更改，请在 **版本** 快速选项卡上选择 Finance 中 ER 配置的已完成或已共享最高版本，然后选择 **获取此版本** 选项。 所选版本的内容将复制到草稿版本。

## <a name="applicability-consideration"></a>适用性注意事项

当您设计新版本的 ER 配置时，您可以定义其对其他软件组件的[依赖关系](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md)。 此步骤被视为控制从 ER 存储库或外部 XML 文件下载此配置的版本和进一步使用此版本的先决条件。 当您尝试导入 ER 配置的新版本时，系统使用配置的先决条件控制是否可以导入该版本。

在某些情况下，您可能要求系统在您导入新版本的 ER 配置时忽略配置的先决条件。 要使系统在导入期间忽略先决条件，请按照以下步骤操作。

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页操作窗格中 **配置** 选项卡的 **高级设置** 组中，选择 **用户参数**。
3. 将 **导入期间跳过产品更新和版本先决条件检查** 设置为 **是**。

    > [!NOTE]
    > 此参数特定于用户并且特定于公司。

## <a name="additional-resources"></a>其他资源

[电子报告 (ER) 概览](general-electronic-reporting.md)

[定义其他组件上的电子报告配置的依赖关系](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]


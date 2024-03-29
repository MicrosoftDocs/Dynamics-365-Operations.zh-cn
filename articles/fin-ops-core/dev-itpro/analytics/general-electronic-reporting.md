---
title: 电子报告 (ER) 概览
description: 本文概括介绍了电子报告工具。 介绍作为解决方案一部分的关键概念、支持的场景和格式。
author: kfend
ms.date: 11/02/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58941,  ""intro-internal
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.form: ERWorkspace
ms.openlocfilehash: e94846dd565abb6de2c1f07532d285e28307e9a2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269682"
---
# <a name="electronic-reporting-er-overview"></a>电子报告 (ER) 概览

[!include [banner](../includes/banner.md)]

本文概括介绍了电子报告 (ER) 工具。 内容包含有关重要概念、ER 支持的方案以及作为解决方案的一部分进行设计和发布的格式列表的信息。

ER 是一种可配置的工具，可帮助您创建和维护监管电子报告和付款。 它基于以下三个概念：

- 配置而不是编码：

    - 配置可以由业务用户完成，不需要开发人员。
    - 数据模型使用业务术语定义。
    - 可视化编辑器用于创建 ER 配置的所有组件。
    - 用于数据转换的语言类似于 Microsoft Excel 中使用的语言。

- 多个 Dynamics 365 Finance 版本使用一个配置：

    - 管理使用业务术语定义的一个特定于域的数据模型。
    - 在依赖于版本的数据模型映射中隔离应用程序版本详细信息。
    - 根据数据模型，为当前版本的多个发布版本维护一个格式配置。

- 轻松升级或自动升级：

    - 支持 ER 配置的版本控制。
    - Microsoft Dynamics Lifecycle Services (LCS) 资产库可用作 ER 配置的存储库，用于版本交换。
    - 基于原始 ER 配置的本地化可以作为子版本引入。
    - 提供 ER 配置树作为帮助控制版本依赖项的工具。
    - 记录本地化或增量配置的差异以启用自动升级到原始 ER 配置的新版本。
    - 可以轻松手动解决在本地化版本自动升级过程中发现的冲突。

ER 允许您定义电子格式结构，然后描述应如何使用数据和算法填充结构。 您可以使用类似于 Excel 语言的公式语言进行数据转换。 为了使数据库到格式的映射更易于管理、可重用且独立于格式更改，引入了中间数据模型概念。 此概念使实现详细信息能够从格式映射中隐藏，并使单个数据模型能够重复用于多个格式映射。

您可以根据各个国家和地区的法律要求，使用 ER 配置传入和传出电子文档的格式。 ER 可以在电子文档的生命周期中管理这些格式。 例如，您可以采用新的法规要求，并可以使用所需格式生成业务文档以与政府机构、银行和其他当事方通过电子方式交换信息。

ER 引擎主要面向企业用户，而不是开发人员。 因为配置格式，而不是代码，创建和调整电子文档格式的流程更快、更方便。

ER 目前支持 TEXT、XML、JSON、PDF、Microsoft Word、Microsoft Excel 和 OPENXML 工作表格式。

## <a name="capabilities"></a>功能

ER 引擎具有以下功能：

- 它表示不同域中的电子申报的单一共享工具，并替换超过 20 个用于执行某种财务和运营电子申报的不同引擎。
- 它让报表的格式与当前实施隔离。 换句话说，该格式适用于不同版本。
- 它支持创建基于原始格式的自定义格式。 它还包括当原始格式发生更改时自动升级自定义格式的功能，因为引入了本地化/自定义要求。
- 它成为支持电子申报中的本地化要求的主要标准工具，针对 Microsoft 以及 Microsoft 合作伙伴。
- 它支持通过 Microsoft Dynamics Lifecycle Services (LCS) 为合作伙伴和客户分配格式的功能。

## <a name="key-concepts"></a>重要概念

### <a name="main-data-flow"></a>主数据流

[![ER 主数据流。](./media/ger-main-data-flow.jpg)](./media/ger-main-data-flow.jpg)

### <a name="component"></a>组分

ER 支持以下组件类型：

- 数据模型
- 模型映射
- 格式
- 元数据

有关详细信息，请参阅[电子报告组件](er-overview-components.md)。

### <a name="configuration"></a><a name="Configuration"></a>配置

ER 配置是特定 ER 组件的包装。 该组件可以是数据模型组件或组件格式。 配置可包括不同版本的 ER 组件。 每个配置被标记为由特定配置提供商所有。 当配置的所有者已选为应用程序内 ER 设置中的有效提供商时，配置的组件的 **草稿** 版本可进行编辑。

每个模型配置包含数据模型组件。 新的格式配置可以衍生自特定的数据模型配置。 在配置数中，创建的格式配置将作为原始数据模型配置的子配置显示。

创建的格式配置包含格式组件。 原始模型配置的数据模型组件将作为默认数据源自动插入到子格式配置的格式组件。

将对应用程序公司共享 ER 配置。

### <a name="provider"></a><a name="Provider"></a>提供程序

ER 提供商是用于指示每个 ER 配置的作者（所有者）的当事方的标识符。 ER 可以管理配置提供商的列表。 作为财务和运营解决方案的一部分为电子单据发布的格式配置被标记为由配置提供商 **Microsoft** 所有。

要了解如何登记新的 ER 提供商，可播放任务指南，**ER 创建配置提供商并将其标记为有效**（**7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677)** 业务流程的一部分）。

### <a name="repository"></a><a name="Repository"></a>知识库

ER 存储库中会存储 ER 配置。 目前支持以下 ER 存储库类型： 

- LCS 共享库
- LCS 项目
- 文件系统
- RCS
- Operations 资源
- 全局知识库

**LCS 共享库** 存储库提供对 Lifecycle Services (LCS) 中共享资产库内的配置列表的访问。 只能为 Microsoft 提供程序注册这种类型的 ER 存储库。 可将最新版本的 ER 配置从 LCS 共享资产库导入到当前实例中。

**LCS 项目** 存储库允许您访问在存储库登记时选择的特定 LCS 项目（LCS 项目资产库）的配置列表。 ER 让你可以从当前实例将共享配置上载到特定 **LCS 项目** 存储库。 您还可以从 **LCS 项目** 存储库将配置导入到当前的财务和运营应用实例。

**文件系统** 存储库提供对作为 XML 文件位于承载 AOS 服务的计算机的本地文件系统的特定文件夹的配置列表的访问。 所需文件夹在存储库登记阶段选择。 您可以从 **文件系统** 存储库将配置导入到当前实例。 

请注意，存储库类型在以下环境中可访问：

- 为开发目的部署的云托管环境（包含所含套件的测试模型）
- 本地部署的环境（本地）

有关详细信息，请参阅[导入电子申报 (ER) 配置](./electronic-reporting-import-ger-configurations.md)。

**RCS** 存储库允许您访问在存储库登记阶段选择的 [Configuration service (RCS)](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration) 的特定实例的配置列表。 ER 让您可以将完成的或共享的配置从所选的 RCS 实例导入到当前实例并用于电子申报。

有关详细信息，请参阅[从 RCS 导入电子申报 (ER) 配置](./rcs-download-configurations.md)。

一个 **全局知识库** 存储库提供对[配置服务](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration)中全局知识库中的配置列表的访问。 只能为 Microsoft 提供程序注册这种类型的 ER 存储库。 可将最新版本的 ER 配置从全局知识库导入到当前实例中。

有关详细信息，请参阅[从配置服务的全局知识库导入电子申报 (ER) 配置](./er-download-configurations-global-repo.md)。

**运营资源** 存储库允许您访问由 Microsoft 最初作为 EER 配置提供商发布的作为应用程序解决方案的一部分的配置的列表。 这些配置可以导入到当前实例，并且可以用于电子申报或播放示例任务指南。 它们还可以用于其他本地化和自定义。 请注意，必须使用相应的 ER 存储库从 LCS 共享资产库导入 Microsoft ER 配置提供的最新版本。

可分别为当前实例的每个配置提供商登记所需的 **LCS 项目**、**文件系统** 和 **监管配置服务 (RCS)** 存储库。 每个存储库可专门针对一个特定配置提供商。

## <a name="supported-scenarios"></a>支持的方案

### <a name="building-a-data-model"></a>构建数据模型

ER 提供了一个模型设计器，可以用于为特定业务域构建数据模型。 所有特定于域的业务实体以及这些实体之间的关系可在数据模型以层次结构的形式呈现。 

若要详细了解此方案，播放 **ER 设计域特定数据模型** 任务指南（**7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677)** 业务流程的一部分）以。

### <a name="translating-data-model-content"></a>翻译数据模型内容

数据模型内容（标签和描述）可以翻译成应用程序支持的其他语言。 您可能因为以下原因想要翻译数据模型内容︰

- 在设计时，使内容对于说外语且将使用数据模型进行格式组件的数据映射的格式设计人员更容易理解。
- 在运行时，通过呈现提示让内容更加用户友好并帮助运行时参数，另外还使用当前登录的用户偏好的语言配置验证消息（错误和警告）。

### <a name="configuring-data-model-mappings-for-outgoing-documents"></a>配置传出文档的数据模型映射

ER 提供模型映射设计器，可让用户将他们所设计的数据模型映射到特定应用程序数据源。 基于映射，数据将在运行时从所选数据源导入到数据模型。 然后使用数据模型作为生成传出电子文档的 ER 格式的抽象数据源。 

若要详细了解此方案，播放 **ER 定义模型映射并选择数据源** 和 **ER 将数据模型映射到所选数据源** 任务指南（**7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677)** 业务流程的一部分）。

### <a name="configuring-data-model-mappings-for-incoming-documents"></a>配置传入文档的数据模型映射

ER 提供模型映射设计器，可让用户将他们所设计的数据模型映射到特定的目的地。 例如，数据模型可以映射到可更新数据组件（表、数据实体和视图）。 基于映射，使用数据模型的数据在运行时更新。 作为 ER 格式的抽象存储，使用从传入电子文档导入的数据填充数据模型。 

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>将设计的模型组件存储为模型配置

ER 能够将设计的数据模型（与关联的数据映射一起）存储为当前实例的模型配置。 下图显示这种类型的数据模型配置（付款模型配置）的示例。

若要详细了解此方案，播放 **ER 将数据模型映射到所选数据源** 任务指南（**7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677)** 业务流程的一部分）以。

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>构建使用数据模型作为基础的格式

ER 支持格式设计器，您可以通过选择模型组件作为基础来使用此设计器构建电子单据的格式。 同一 ER 格式设计器让您可以将创建的格式作为数据源映射到所选域的数据模型映射。 

若要详细了解此方案，播放 **ER 设计域特定格式** 任务指南（**7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677)** 业务流程的一部分）以。

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>构建配置以生成使用 OPENXML 工作表格式的电子单据

ER 格式设计器可以用于构建使用 OPENXML 工作表格式的电子单据。 

若要详细了解此方案，播放 **ER 创建 OPENXML 格式的报表配置** 任务指南（**7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677)** 业务流程的一部分）以。 作为导入模板的任务指南的一部分，使用 [付款报表模板 (SampleVendPaymWsReport.xlsx)](https://download.microsoft.com/download/3/f/0/3f0658b2-042c-43cf-a776-0f4c7f7cfe4e/SampleVendPaymWsReport.xlsx) Excel 文件作为模板。

### <a name="building-a-configuration-to-generate-electronic-documents-in-a-word-document-format"></a>构建配置以生成使用 Word 文档格式的电子单据

ER 格式设计器可以用于构建使用 Word 文档格式的电子单据。 下图显示这种格式类型的示例。 请注意，此格式重复使用最初为生成 OPENXML 格式的报表输出而设计的现有 ER 配置。

若要详细了解此方案，播放 ER 设计用于生成 Microsoft WORD 格式的报表的配置任务指南（7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677) 业务流程的一部分）。 作为导入模板的任务指南步骤的一部分，使用以下 Word 文件作为 ER 格式的模板：

- [付款报表模板 (SampleVendPaymDocReport.docx)](https://download.microsoft.com/download/0/d/e/0de5a87c-95fc-4dfa-958f-285cb28b5b2b/SampleVendPaymDocReport.docx)
- [付款报表绑定模板 (SampleVendPaymDocReportBounded.docx)](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded.docx)

### <a name="building-a-configuration-to-import-data-from-incoming-electronic-documents"></a>生成配置以从传入的电子文档导入数据

ER 格式设计器可用于描述为 XML 或文本格式的数据导入计划的电子文档。 设计的格式用于分析传入的文档。 ER 格式映射设计器可用于定义设计格式的元素到数据模型的绑定。 

若要详细了解此方案，播放创建从外部文件导入数据所需配置任务指南（7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677) 业务流程的一部分）。 使用以下文件播放本指南：

- [ER 数据模型配置 (1099model.xml)](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml)
- [ER 格式配置 (1099format.xml)](https://download.microsoft.com/download/e/8/7/e87154b0-b53f-431f-8e1e-0b7f7c9805a9/1099format.xml)
- [XML 格式的传入文档示例 (1099entries.xml)](https://download.microsoft.com/download/4/0/3/403a4958-df24-476a-b8b0-6843a9fa7f89/1099entries.xml)
- [管理传入文档数据的工作簿的示例 (1099entries.xlsx)](https://download.microsoft.com/download/6/0/0/6001abab-a331-48db-a939-41851fb0f5d0/1099entries.xlsx)

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>在格式配置中存储设计的格式组件

ER 能够将设计的格式（与已配置的数据映射一起）存储为当前实例的格式配置。 上面的插图显示了这种格式配置的一个示例（**BACS（英国）**，这是 **付款模型** 配置的子配置）。 若要详细了解此方案，播放 **ER 设计域特定格式** 任务指南（**7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677)** 业务流程的一部分）以。

### <a name="configuring-finance-to-start-to-use-a-created-format-internally"></a>配置 Finance 以开始在内部使用创建的格式

可以配置此应用程序以开始将创建的格式用于电子报表生成。 对创建的格式配置的引用应在特定域的设置中定义。 例如，若要开始在 BACS 格式中使用 ER 格式配置进行电子供应商付款，格式配置应在特定付款方式中引用。

若要详细了解此方案，播放 **ER 使用格式为付款生成电子单据** 任务指南（**7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677)** 业务流程的一部分）。

## <a name="handling-er-components"></a>处理 ER 组件

### <a name="publishing-an-er-component-in-lcs-to-offer-it-externally-localization"></a>在 LCS 中发布 ER 组件以在外部提供该组件（本地化）

创建的组件（模型或格式）的所有者能够使用 ER 将已完成版本的组件发布到 LCS。 需要当前 ER 配置提供商的 **LCS 项目** 类型的存储库。 当已完成版本的组件的状态从 **已完成** 更改为 **共享** 时，此版本将在 LCS 中发布。 当某个组件已发布到 LCS 时，此组件的所有者将成为支持此组件的服务的提供商。 例如，如果此格式组件可生成法律要求的电子单据（例如，根据本地化方案），将假设此格式与法律更改保持一致，且提供商将发布新的组件版本，无论是否必须满足新出现的法律要求。 若要详细了解此方案，播放 **ER 上载配置到 Lifecycle Services** 任务指南（**7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677)** 业务流程的一部分）以。

### <a name="importing-an-er-component-from-lcs-to-use-it-internally"></a>从 LCS 导入 ER 组件以在内部使用该组件

ER 可以将 ER 组件从 LCS 导入到当前实例。 对此，需要 **LCS 项目** 类型的存储库。 当 ER 组件已从 LCS 导入到当前实例后，此实例的所有者将变成由导入的组件的所有者（作者）提供的服务的使用者。 例如，如果格式组件可从此应用程序生成特定于某些国家/地区的格式（本地化方案）的特定电子单据，将假设服务使用者能够获取此格式的任何更新以使其符合法律要求。 若要详细了解此方案，播放 **ER 从 Lifecycle Services 导入配置** 任务指南（**7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677)** 业务流程的一部分）以。

### <a name="building-a-format-selecting-another-format-as-a-base-customization"></a>构建选择其他格式作为基础的格式（自定义）

ER 可让您通过从 LCS 导入的当前组件版本（基本）创建（派生）新组件。 例如，用户想派生一种新的格式以履行某些特殊电子单据要求（如额外字段或广泛描述）来支持自定义方案。 若要详细了解此方案，播放 **ER 通过采用新基础版本的格式来升级格式** 任务指南（**7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677)** 业务流程的一部分）。

### <a name="upgrading-a-format-selecting-a-new-version-of-base-format-rebase"></a>升级选择新版本的基础格式（重定基）的格式

ER 支持在当前草稿版的派生组件中自动采用最新版本的基础组件的更改的功能。 此流程称为 *重定基本值*。 例如，新的法规性更改（将在从 LCS 导入的最新版的格式组件中引入）可自动合并到电子单据此格式的自定义版本中。 任何不能自动合并的更改视为冲突。 这些冲突将在相应组件的设计器工具中呈现以进行手动解决。 若要详细了解此方案，播放 **ER 通过采用该格式的新基础版本来升级格式** 任务指南（**7.5.5.3 获取/开发更改的 IT 服务/解决方案组件 (10683)** 业务流程的一部分）。

## <a name="list-of-er-configurations-that-have-been-released-in-finance"></a><a name="list-of-configurations"></a>Finance 中已发布的 ER 配置列表

Finance 的 ER 配置列表会不断更新。 打开[全局存储库](er-download-configurations-global-repo.md)查看当前支持的 ER 配置列表。 在 **停用详细信息** 快速选项卡上，您可以查看有关已停用或不再维护的配置的信息。 

![配置存储库页面上的全局存储库的内容。](./media/er-overview-03.gif)

## <a name="additional-resources"></a>其他资源

- [电子报告组件](er-overview-components.md)
- [创建电子报告 (ER) 配置](electronic-reporting-configuration.md)
- [管理电子申报 (ER) 配置生命周期](general-electronic-reporting-manage-configuration-lifecycle.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]


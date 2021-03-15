---
title: 电子申报 (ER) 概览
description: 此主题概要介绍了电子报告工具。 介绍作为解决方案一部分的关键概念、支持的场景和格式。
author: NickSelin
manager: AnnBe
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33d399c6a9051097d3ea0c7990a37302395d9c77
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093918"
---
# <a name="electronic-reporting-er-overview"></a>电子报告 (ER) 概览

[!include [banner](../includes/banner.md)]

此主题概要介绍了电子申报 (ER) 工具。 内容包含有关重要概念、ER 支持的方案以及作为解决方案的一部分进行设计和发布的格式列表的信息。

ER 是一种工具，你可以使用它根据不同国家/地区的法律要求配置传入和传出电子文档的格式。 ER 可以在电子文档的生命周期中管理这些格式。 例如，您可以采用新的法规要求，并可以使用所需格式生成业务文档以与政府机构、银行和其他当事方通过电子方式交换信息。

ER 引擎主要面向企业用户，而不是开发人员。 因为配置格式，而不是代码，创建和调整电子文档格式的流程更快、更方便。

ER 目前支持 TEXT、XML、Microsoft Word 文档和 OPENXML 工作表格式。 但是，扩展接口提供更多支持的格式。

## <a name="capabilities"></a>功能

ER 引擎具有以下功能：

- 它表示不同域中的电子申报的单一共享工具，并替换超过 20 个用于执行某种 Finance and Operations 电子申报的不同引擎。
- 它让报表的格式与当前实施隔离。 换句话说，该格式适用于不同版本。
- 它支持创建基于原始格式的自定义格式。 它还包括当原始格式发生更改时自动升级自定义格式的功能，因为引入了本地化/自定义要求。
- 它成为支持电子申报中的本地化要求的主要标准工具，针对 Microsoft 以及 Microsoft 合作伙伴。
- 它支持通过 Microsoft Dynamics Lifecycle Services (LCS) 为合作伙伴和客户分配格式的功能。

## <a name="key-concepts"></a>重要概念

### <a name="components"></a>组件

ER 支持两种组件类型：**数据模型** 和 **格式**。

#### <a name="data-model-and-model-mapping-components"></a>数据模型和模型映射组件

数据模型组件是数据结构的抽象表现形式。 它用于描述一个特定的业务域领域，而且具有足够的详细信息满足该域的报告要求。 数据模型组件由以下部分组成︰

- <a name="DataModelComponent"></a>以一组特定于域的业务实体表示的数据模型以及这些实体之间的关系的分层式定义。
- <a name="ModelMappingComponent"></a>将选定的应用程序数据源关联到在运行时指定的数据模型的各个元素模型映射，业务数据的数据流和规则对数据模型组件的填充。

数据模型的业务实体表示为容器（记录）。 业务实体属性表示为数据项（字段）。 每个数据项具有一个唯一的名称、标签、描述和值。 每个数据项的值可以设计，以便它被识别为字符串、整数、实数、日期、枚举、布尔值，等等。 此外，它可以是另一条记录或记录列表。

单个数据模型组件可以包含特定域的业务实体的若干层次结构。 它还可以包含在运行时间支持特定报告的数据流的模型映射。 层次结构通过已被选择为模型映射的根的单一记录区分。 例如，付款域区域的数据模型可支持以下映射：

- 公司 \> 供应商 \> AP 域的付款交易记录
- 客户 \> 公司 \> AP 域的付款交易记录

请注意，业务实体（如公司和付款交易记录）是一次性设计而成。 然后不同的映射重用它们。

支持传出电子文档的模型映射具有以下功能：

- 它可以使用不同的数据类型作为数据模型的数据源。 例如，它可以使用表、数据实体、方法或枚举。
- 当某些数据必须在运行时指定时，它支持用户输入可定义为数据模型数据源的参数。
- 它支持将数据转换到所需的组。 它还能让您对数据进行筛选、排序和汇总，并且还追加通过与 Microsoft Excel 公式类似的公式设计的逻辑计算字段。 有关详细信息，请参阅[电子申报 (ER) 中的公式设计器](general-electronic-reporting-formula-designer.md)。

支持传入电子文档的模型映射具有以下功能：

- 它可以使用不同的可更新数据元素作为目标。 这些数据元素包括表、数据实体和视图。 这些数据可以使用来自传入电子文档的数据进行更新。 可以在单个模型映射中使用多个目标。
- 当某些数据必须在运行时指定时，它支持用户输入可定义为数据模型数据源的参数。

为每个业务域设计了一个数据模型组件，业务域将用作报告的统一数据源，用于将报告与数据源的物理实施隔离。 它表示提高了报告格式的初始设计和后续维护的效率的窗体中特定于域的业务概念和功能。

#### <a name="format-components-for-outgoing-electronic-documents"></a><a name="FormatComponentOutbound"></a>传出电子文档的格式组件

格式组件是在运行时生成的报告输出的方案。 方案由下列元素组成︰

- 定义在运行时生成的传出电子文档的结构和内容的格式。
- 数据源，形式为一组用户输入参数和使用所选模型映射的特定于域的数据模型。
- 一个格式映射，形式为具有某个格式的单独元素的格式数据源的一组绑定，该格式在运行时指定格式输出生成的数据流和规则。
- 一个格式验证，形式为在运行时根据运行上下文控制报表生成的一组可配置规则。 例如，可能存在规则在选定供应商的特定属性（例如银行帐号）缺失时停止供应商付款的输出生成并引发异常。

格式组件支持以下函数︰

- 使用不同格式（例如文本、XML、Microsoft Word 文档或工作表）作为单个文件创建报告输出。
- 单独创建多个文件，并将这些文件压缩为 zip 文件。

格式组件能让您附加可在报告输出中使用的特定文件：

- 包含可用作使用 OPENXML 工作表格式输出的模板的工作表的 Excel 工作簿
- 包含可用作 Microsoft Word 文档格式的输出模板的文档的 Word 文件
- 其他文件可合并到格式的输出中以坐为预定义文件

下图显示这些格式的数据流情况。

[![传出格式组件的数据流](./media/ER-overview-02.png)](./media/ER-overview-02.png)

要运行单个 ER 格式配置和生成传出电子文档，您必须确定格式配置的映射。

#### <a name="format-components-for-incoming-electronic-documents"></a><a name="FormatComponentInbound"></a>传入电子文档的格式组件

格式组件是在运行时导入的传入文档的方案。 方案由下列元素组成︰

- 定义包含在运行时导入的数据的传入电子文档的结构和内容的格式。 格式组件用于分析不同格式（例如文本和 XML）的传入文档。
- 将各个格式元素绑定到特定于域的数据模型元素的格式映射。 在运行时，数据模型中的元素指定数据流和从传入文档导入数据的规则，然后将数据存储到数据模型中。
- 一个格式验证，形式为在运行时根据运行上下文控制数据导入的一组可配置规则。 例如，可能存在规则在特定供应商的属性缺失（例如供应商标识代码）时阻止导入具有供应商付款的银行对账单的数据并引发异常。

下图显示这些格式的数据流情况。

[![传入格式组件的数据流](./media/ER-overview-03.png)](./media/ER-overview-03.png)

要运行单个 ER 格式配置以从传入电子文档导入数据，您必须确定格式配置的预期映射，以及模型映射的集成点。 您可以使用不同的格式为不同类型的传入文档同时使用相同的模型映射和目标。

#### <a name="component-versioning"></a>组件版本控制

ER 组件支持版本控制。 提供了以下工作流以便在 ER 组件中管理更改：

1. 最初创建的版本被标记为 **草稿** 版本。 此版本可进行编辑，并可用于测试运行。
2. **草稿** 版本可以转换为 **已完成** 版本。 此版本可在本地报告流程中使用。
3. **已完成** 版本可以转换为 **共享** 版本。 此版本在 LCS 上发布，并可在全球报告流程中使用。
4. **共享** 版本可以转换为 **已终止** 版本。 然后可以删除此版本。

状态为 **已完成** 或 **共享** 的版本可用于其他数据交换。 可以对具有这些状态的组件执行以下操作：

- 该组件可以以 XML 格式序列化并导出为 XML 格式的文件。
- 组件可以从 XML 文件重新序列化并作为 ER 组件的新版本导入到应用程序中。

#### <a name="component-date-effectivity"></a>组件日期有效性

ER 组件版本是有时限的。 可以设置 ER 组件的 **生效** 日期以指定此组件开始对报告流程生效的日期。 应用程序会话日期用于定义组件是否对执行有效。 当多个版本在特定日期生效时，最新版本将用于报告流程。

#### <a name="component-access"></a>组件访问权限

对 ER 格式组件的访问权限取决于 ISO 国家/地区代码的设置。 当所选格式配置的版本的这一设置为空时，可以在运行时从任何公司访问格式组件。 当此设置包含 ISO 国家/地区代码时，格式组件只能从为格式组件 ISO 国家/地区代码之一定义了主要地址的公司访问。

不同版本的数据格式组件可以有不同的 ISO 国家/地区代码设置。

#### <a name="configuration"></a><a name="Configuration"></a>配置

ER 配置是特定 ER 组件的包装。 该组件可以是数据模型组件或组件格式。 配置可包括不同版本的 ER 组件。 每个配置被标记为由特定配置提供商所有。 当配置的所有者已选为应用程序内 ER 设置中的有效提供商时，配置的组件的 **草稿** 版本可进行编辑。

每个模型配置包含数据模型组件。 新的格式配置可以衍生自特定的数据模型配置。 在配置数中，创建的格式配置将作为原始数据模型配置的子配置显示。

创建的格式配置包含格式组件。 原始模型配置的数据模型组件将作为默认数据源自动插入到子格式配置的格式组件。

将对应用程序公司共享 ER 配置。

#### <a name="provider"></a><a name="Provider"></a>提供程序

ER 提供商是用于指示每个 ER 配置的作者（所有者）的当事方的标识符。 ER 可以管理配置提供商的列表。 作为 Finance and Operations 解决方案的一部分为电子单据发布的格式配置被标记为由配置提供商 **Microsoft** 所有。

要了解如何登记新的 ER 提供商，可播放任务指南，**ER 创建配置提供商并将其标记为有效**（**7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677)** 业务流程的一部分）。

#### <a name="repository"></a><a name="Repository"></a>知识库

ER 存储库中会存储 ER 配置。 目前支持以下 ER 存储库类型： 

- LCS 共享库
- LCS 项目
- 文件系统
- RCS
- Operations 资源
- 全局知识库

**LCS 共享库** 存储库提供对 Lifecycle Services (LCS) 中共享资产库内的配置列表的访问。 只能为 Microsoft 提供程序注册这种类型的 ER 存储库。 可将最新版本的 ER 配置从 LCS 共享资产库导入到当前实例中。

**LCS 项目** 存储库允许您访问在存储库登记时选择的特定 LCS 项目（LCS 项目资产库）的配置列表。 ER 让你可以从当前实例将共享配置上载到特定 **LCS 项目** 存储库。 您还可以从 **LCS 项目** 存储库将配置导入到您的 Finance and Operations 应用的当前实例。

**文件系统** 存储库提供对作为 xml 文件位于承载 AOS 服务的计算机的本地文件系统的特定文件夹的配置列表的访问。 所需文件夹在存储库登记阶段选择。 您可以从 **文件系统** 存储库将配置导入到当前实例。 

请注意，存储库类型在以下环境中可访问：

- 为开发目的部署的云托管环境（包含所含套件的测试模型）
- 本地部署的环境（本地）

有关详细信息，请参阅[导入电子申报 (ER) 配置](./electronic-reporting-import-ger-configurations.md)。

**RCS** 存储库允许您访问在存储库登记阶段选择的 [Configuration service (RCS)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration) 的特定实例的配置列表。 ER 让您可以将完成的或共享的配置从所选的 RCS 实例导入到当前实例并用于电子申报。

有关详细信息，请参阅[从 RCS 导入电子申报 (ER) 配置](./rcs-download-configurations.md)。

一个 **全局知识库** 存储库提供对[配置服务](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration)中全局知识库中的配置列表的访问。 只能为 Microsoft 提供程序注册这种类型的 ER 存储库。 可将最新版本的 ER 配置从全局知识库导入到当前实例中。

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

若要详细了解此方案，播放 **ER 创建 OPENXML 格式的报表配置** 任务指南（**7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677)** 业务流程的一部分）以。 作为导入模板的任务指南的一部分，使用 [付款报表模板 (SampleVendPaymWsReport.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202) Excel 文件作为模板。

### <a name="building-a-configuration-to-generate-electronic-documents-in-a-word-document-format"></a>构建配置以生成使用 Word 文档格式的电子单据

ER 格式设计器可以用于构建使用 Word 文档格式的电子单据。 下图显示这种格式类型的示例。 请注意，此格式重复使用最初为生成 OPENXML 格式的报表输出而设计的现有 ER 配置。

若要详细了解此方案，播放 ER 设计用于生成 Microsoft WORD 格式的报表的配置任务指南（7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677) 业务流程的一部分）。 作为导入模板的任务指南步骤的一部分，使用以下 Word 文件作为 ER 格式的模板：

- [付款报表模板 (SampleVendPaymDocReport.docx)](https://go.microsoft.com/fwlink/?linkid=845202)
- [付款报表绑定模板 (SampleVendPaymDocReportBounded.docx)](https://go.microsoft.com/fwlink/?linkid=845202)

### <a name="building-a-configuration-to-import-data-from-incoming-electronic-documents"></a>生成配置以从传入的电子文档导入数据

ER 格式设计器可用于描述为 XML 或文本格式的数据导入计划的电子文档。 设计的格式用于分析传入的文档。 ER 格式映射设计器可用于定义设计格式的元素到数据模型的绑定。 

若要详细了解此方案，播放创建从外部文件导入数据所需配置任务指南（7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677) 业务流程的一部分）。 使用以下文件播放本指南：

- [ER 数据模型配置 (1099model.xml)](https://go.microsoft.com/fwlink/?linkid=845202)
- [ER 格式配置 (1099format.xml)](https://go.microsoft.com/fwlink/?linkid=845202)
- [XML 格式的传入文档示例 (1099entries.xml)](https://go.microsoft.com/fwlink/?linkid=845202)
- [管理传入文档数据的工作簿的示例 (1099entries.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202)

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

![配置存储库页上的全局存储库的内容](./media/er-overview-03.gif)

## <a name="additional-resources"></a>其他资源

- [创建电子报告 (ER) 配置](electronic-reporting-configuration.md)
- [管理电子申报 (ER) 配置生命周期](general-electronic-reporting-manage-configuration-lifecycle.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
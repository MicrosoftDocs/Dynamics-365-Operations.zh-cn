---
title: "电子申报概览"
description: "本文概要介绍了电子申报 (ER) 工具。 内容包含有关重要概念、ER 支持的方案以及作为解决方案的一部分进行设计和发布的格式列表的信息。"
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: caa9f4c73f4c6b5b7637b5b012bd9ed3b7dd6392
ms.contentlocale: zh-cn
ms.lasthandoff: 05/25/2017


---

# <a name="electronic-reporting-overview"></a>电子申报概览

[!include[banner](../includes/banner.md)]


本文概要介绍了电子申报 (ER) 工具。 内容包含有关重要概念、ER 支持的方案以及作为解决方案的一部分进行设计和发布的格式列表的信息。

电子申报 (ER) 是一种工具，您可以使用它根据不同国家/地区的法律要求配置电子文档的格式。 ER 可以在电子文档的生命周期中管理这些格式。 例如，您可以采用新的法规要求，并可以使用所需格式生成业务文档以与政府机构、银行和其他当事方通过电子方式交换信息。 ER 引擎主要面向企业用户，而不是开发人员。 因为配置格式，而不是代码，创建和调整电子文档格式的流程更快、更方便。 ER 目前支持 TEXT、XML 和 OPENXML 工作表格式。 但是，扩展接口提供更多支持的格式。

## <a name="capabilities"></a>功能
ER 引擎具有以下功能：

-   它表示不同域中的电子申报的单一通用工具，并替换超过 20 个用于执行某种 Microsoft Dynamics 365 for Operations 电子申报的不同引擎。
-   它让报表的格式与当前 Dynamics 365 for Operations 实施隔离。 （换句话说，该格式适用于 Dynamics 365 for Operations 的不同版本。）
-   它支持创建基于原始格式的自定义格式。 它包括当原始格式发生更改时自动升级自定义格式的功能（因为引入了本地化/自定义要求）。
-   它成为支持电子申报中的本地化要求的主要标准工具，针对 Microsoft 以及 Microsoft 合作伙伴。
-   它支持通过 Microsoft Dynamics Lifecycle Services (LCS) 为合作伙伴和客户分配格式的功能。

## <a name="concepts"></a>概念
### <a name="components"></a>组件

ER 支持两种组件类型：**数据模型**和**格式**。

#### <a name="data-model-components"></a>数据模型组件

数据模型组件是数据结构的抽象表示方式，用于描述带有足以满足此域的报告要求的详述的特定业务域区域。 数据模型组件由以下部分组成︰

-   以一组特定于域的业务实体表示的数据模型以及这些实体之间的关系的分层式定义。
-   将选定的 Dynamics 365 for Operations 数据源关联到在运行时指定的数据模型的各个元素模型映射，业务数据的数据流和规则对数据模型组件的填充。

数据模型的业务实体表示为容器（记录）。 业务实体属性表示为数据项（字段）。 每个数据项具有唯一的名称、标签、描述和值。 每个数据项的值可以设计，以便它被识别为字符串、整数、实数、日期、枚举类型、布尔值，等等。 此外，它可以是另一条记录或记录列表。 单个数据模型组件可包含特定于域的业务实体的几个层次结构，以及在运行时支持特定于某个报表的数据流的模型映射。 层次结构通过已被选择为模型映射的根的单一记录区分。 例如，付款域区域的数据模型可支持以下映射：

-   公司 -&gt; 供应商 -&gt; AP 域的付款交易记录
-   客户 -&gt; 公司 -&gt; AP 域的付款交易记录

请注意，业务实体（如公司和付款交易记录）设计一次。 然后不同的映射重用它们。 模型映射具有以下功能︰

-   它可以使用不同的 Dynamics 365 for Operations 数据类型作为数据模型的数据源。 例如，它可以使用表、数据实体、方法或枚举。
-   当某些数据必须在运行时指定时，它支持用户输入可定义为数据模型数据源的参数。
-   它支持将 Dynamics 365 for Operations 数据转换为所需的组，筛选、排序和汇总数据，并且还追加通过 Microsoft Excel 类似公式设计逻辑计算字段（有关更多详细信息，请参阅[电子申报中的公式设计器](general-electronic-reporting-formula-designer.md)）。

[![类似于 Excel 的公式编辑器](./media/pic-formula-1024x615.png)](./media/pic-formula.png) 为每个业务域设计了一个模型组件，业务域将用作报告的统一数据源，用于将报告与 Dynamics 365 for Operations 数据源的物理实施隔离，表示提高了报告格式的初始设计和后续维护的效率的窗体中特定于域的业务概念和功能。

#### <a name="format-components"></a>格式组件

格式组件是在运行时生成的报告输出的方案。 方案由下列元素组成︰

-   定义在运行时生成的电子申报单据的结构和内容的格式
-   数据源，形式为一组用户输入参数和使用所选模型映射的特定于域的数据模型
-   一个格式映射，形式为具有在运行时指定的各个格式元素的格式数据源的一组绑定，格式输出生成的数据流和规则
-   格式验证，形式为在运行时根据运行上下文控制报表生成的一组可配置规则（例如，停止供应商付款输出生成，并在缺少所选供应商的特定属性(如银行帐号)时引发异常的规则）。

格式组件支持以下函数︰

-   使用不同格式作为单个文件创建报告输出︰文本、XML 或工作表
-   单独创建多个文件，并将这些文件压缩为 zip 文件

格式组件提供附加可在报告输出中使用的特定文件的功能：

-   包含可用作使用 OPENXML 工作表格式输出的模板的工作表的 Excel 工作簿
-   其他文件可合并到格式的输出中以坐为预定义文件

#### <a name="component-versioning"></a>组件版本控制

ER 组件支持版本控制。 提供了以下工作流以便在 ER 组件中管理更改：

-   最初创建的版本被标记为**草稿**版本。 此版本可进行编辑，并可用于测试运行。
-   **草稿**版本可以转换为**已完成**版本。 此版本可在本地报告流程中使用。
-   **已完成**版本可以转换为**共享**版本。 此版本在 LCS 上发布，并可在全球报告流程中使用。
-   **共享**版本可以转换为**已终止**版本。 然后可以删除此版本。

状态为 **已完成** 或**共享**的版本可用于其他数据交换。 处于这些状态的组件可以对其执行这些操作︰

-   他们可以以 XML 格式序列化并从 Dynamics 365 for Operations 导出为 XML 格式的文件。
-   它们可以从 XML 文件重新序列化并作为 ER 组件的新版本导入 Dynamics 365 for Operations。

#### <a name="component-date-effectivity"></a>组件日期有效性

ER 组件版本是有时限的。 可为 ER 组件定义**生效**日期以指定此组件变得对报告流程有效的日期。 Dynamics 365 for Operations 会话日期用于定义组件是否对执行有效。 当多个版本在特定日期生效时，最新版本将用于报告流程。

#### <a name="component-access"></a>组件访问权限

对 ER 格式组件的访问权限取决于 ISO 国家/地区代码的设置。 当所选格式配置的版本的这一设置为空时，可以在运行时从任何 Dynamics 365 for Operations 公司访问格式组件。 当此设置包含 ISO 国家/地区代码时，格式组件只能从为格式组件 ISO 国家/地区代码之一定义了主要地址的 Dynamics 365 for Operations 公司访问。 不同版本的数据格式组件可以有不同的 ISO 国家/地区代码设置。

#### <a name="configuration"></a>配置

ER 配置是特定 ER 组件的包装，**数据模型**或**格式**。 配置可包括不同版本的特定 ER 组件。 每个配置被标记为由特定配置提供商所有。 当配置的所有者已选为 Dynamics 365 for Operations ER 设置中的有效提供商时，配置的组件的**草稿**版本可进行编辑。 每个模型配置包含**数据模型**组件。 新的格式配置源自特定的数据模型配置。 创建的格式配置将作为原始数据模型配置的子配置呈现在配置结构树中。 创建的格式配置包含**格式**组件。 原始模型配置的**数据模型**组件将作为默认数据源自动插入到子格式配置的**格式**组件。 将对 Dynamics 365 for Operations 公司共享 ER 配置。

#### <a name="provider"></a>提供程序

ER 提供商是用于指示每个 ER 配置的作者（所有者）的当事方的标识符。 ER 可以管理配置提供商的列表。 作为 Dynamics 365 for Operations 解决方案的一部分为电子单据发布的格式配置被标记为由配置提供商 **Microsoft** 所有。

#### <a name="repository"></a>知识库

ER 存储库中会存储 ER 配置。 目前支持以下 ER 存储库类型：**Operations 资源**和 **LCS 项目**。 **Operations 资源** 存储库允许您访问作为 Dynamics 365 for Operations 解决方案的一部分发布（由 Microsoft 作为 GER 配置提供商）的配置的列表。 这些配置可以导入到当前的 Dynamics 365 for Operations 实例，并且可以用于电子申报。 它们还可以用于其他本地化/自定义。 **LCS 项目**存储库允许您访问在存储库登记阶段选择的特定 LCS 项目（LCS 项目资产库）的配置列表。 ER 让您可以从当前 Dynamics 365 for Operations 实例将共享配置上载到特定 **LCS 项目**存储库的功能。 您还可以从特定 **LCS 项目**存储库将配置导入到当前的 Dynamics 365 for Operations 实例。 可分别为当前 Dynamics 365 for Operations 实例的每个配置提供商登记所需的 **LCS 项目**存储库。 每个存储库可专门针对一个特定配置提供商。

## <a name="supported-scenarios"></a>支持的方案
### <a name="building-a-data-model"></a>构建数据模型

ER 提供了一个模型设计器，可以用于为特定业务域构建数据模型。 所有特定于域的业务实体以及这些实体之间的关系可在数据模型以层次结构的形式呈现。 下图显示这种类型的数据模型（付款域数据模型）的示例。 [![数据模型的示例](./media/pic-data-model-1024x550.png)](./media/pic-data-model.png) 若要详细了解此方案，播放 **ER 设计域特定数据模型**任务指南（**7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677)**业务流程的一部分）以。

### <a name="translating-data-model-content"></a>翻译数据模型内容

数据模型内容（标签和描述）可以翻译成 Dynamics 365 for Operations 支持的其他语言。 您可能因为以下原因想要翻译数据模型内容︰

-   在设计时，使内容对于说外语且将使用数据模型进行格式组件的数据映射的格式设计人员更容易理解
-   运行时，通过呈现提示让内容更加用户友好并帮助运行时参数，另外还使用当前登录的 Dynamics 365 for Operations 偏好的语言配置验证消息（错误和警告）

下面的插图显示示例数据模型内容如何从英语翻译为日文。 [![英语数据模型内容](./media/pic-translate-en-1024x495.png)](./media/pic-translate-en.png) [![翻译成日语的数据模型内容](./media/pic-translate-ja-1024x495.png)](./media/pic-translate-ja.png)

### <a name="configuring-data-model-mappings"></a>配置数据模型映射

ER 提供模型映射设计器，可让用户将他们所设计的数据模型映射到特定 Dynamics 365 for Operations 数据源。 下图显示此类型的数据模型映射的示例（付款域数据模型的 **SEPA 贷方转帐**模型映射）。 [![数据模型映射的示例](./media/pic-model-mapping-1024x551.png)](./media/pic-model-mapping.png) 若要详细了解此方案，播放 **ER 定义模型映射并选择数据源**和 **ER 将数据模型映射到所选数据源**任务指南（**7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677)** 业务流程的一部分）。

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>将设计的模型组件存储为模型配置

ER 能够将设计的数据模型（与关联的数据映射一起）存储为当前 Dynamics 365 for Operations 实例的模型配置。 下图显示这种类型的数据模型配置（付款模型配置）的示例。 [![数据模型配置的示例](./media/pic-model-configuration-1024x585.png)](./media/pic-model-configuration.png) 若要详细了解此方案，播放 **ER 将数据模型映射到所选数据源**任务指南（**7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677)**业务流程的一部分）。

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>构建使用数据模型作为基础的格式

ER 支持格式设计器，您可以通过选择模型组件作为基础来使用此设计器构建特定电子单据的格式。 同一 ER 格式设计器让您可以将创建的格式作为数据源映射到所选域的数据模型映射。 下面的插图显示了这种格式的示例（支持英国 **BACS** 付款格式的格式配置）。 [![使用数据模型作为基础的格式示例](./media/pic-format-1024x690.png)](./media/pic-format.png) 若要详细了解此方案，播放 **ER 设计域特定格式**任务指南（**7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677)**业务流程的一部分）以。

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>构建配置以生成使用 OPENXML 工作表格式的电子单据

ER 格式设计器可以用于构建使用 OPENXML 工作表格式的特定电子单据。 下图显示这种格式类型的示例（生成包含所选付款日记帐的 OPENXML 工作表的格式配置）︰[![Pic-ER-format-Excel](./media/pic-er-format-excel.jpg)](./media/pic-er-format-excel.jpg)若要详细了解此方案，播放 <**ER 创建 OPENXML 格式的报表配置**任务指南（**7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677)** 业务流程的一部分）。 使用引用以下 Excel 文件作为设计 ER 格式的模板来完成此任务指南的格式模板导入的步骤︰[付款报表模板 (SampleVendPaymWsReport.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202)

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>在格式配置中存储设计的格式组件

ER 能够将设计的格式（与已配置的数据映射一起）存储为当前 Dynamics 365 for Operations 实例的格式配置。 上面的插图显示了这种格式配置的一个示例（**BACS（英国）**，这是**付款模型**配置的子配置）。 若要详细了解此方案，播放 **ER 设计域特定格式**任务指南（**7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677)** 业务流程的一部分）以。

### <a name="configuring-dynamics-365-for-operations-to-start-to-use-a-created-format-internally"></a>配置 Dynamics 365 for Operations 以开始在内部使用创建的格式

可以配置 Dynamics 365 for Operations 以开始将创建的格式用于电子报表生成。 对创建的格式配置的引用应在特定域的设置中定义。 例如，若要开始在 BACS 格式中使用 ER 格式配置进行电子供应商付款，格式配置应在特定付款方式中引用，如下面的插图所示： 

[![BACS（英国）格式配置](media/ger-bacs-uk-format-configuration.png) 

[![在付款方式中引用 BACS（英国）格式](media/ger-bacs-uk-format-method.png) 

若要详细了解此方案，播放 **ER 使用格式为付款生成电子单据**任务指南（**7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677)** 业务流程的一部分）。

## <a name="handling-er-components"></a>处理 ER 组件
### <a name="publishing-an-er-component-in-lcs-to-offer-it-externally-localization"></a>在 LCS 中发布 ER 组件以在外部提供该组件（本地化）

创建的组件（模型或格式）的所有者能够使用 ER 将已完成版本的组件发布到 LCS。 需要当前 ER 配置提供商的 **LCS 项目**类型的存储库。 当已完成版本的组件的状态从**“已完成”**更改为**“共享”**时，此版本将在 LCS 中发布。 当某个组件已发布到 LCS 时，此组件的所有者将成为支持此组件的服务的提供商。 例如，如果此格式组件可生成法律要求的电子单据（例如，根据本地化方案），将假设此格式与法律更改保持一致，且提供商将发布新的组件版本，无论是否必须满足新出现的法律要求。 若要详细了解此方案，播放 **ER 上载配置到 Lifecycle Services** 任务指南（**7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677)** 业务流程的一部分）以。

### <a name="importing-an-er-component-from-lcs-to-use-it-internally"></a>从 LCS 导入 ER 组件以在内部使用该组件

ER 可以将 ER 组件从 LCS 导入到当前 Dynamics 365 for Operations 实例。 对此，需要 **LCS 项目**类型的存储库。 当 ER 组件已从 LCS 导入到当前 Dynamics 365 for Operations 实例后，此实例的所有者将变成由导入的组件的所有者（作者）提供的服务的使用者。 例如，如果格式组件可从 Dynamics 365 for Operations 生成特定于某些国家/地区的格式（本地化方案）的特定电子单据，将假设服务使用者能够获取此格式的任何更新以使其符合法律要求。 若要详细了解此方案，播放 **ER 从 Lifecycle Services 导入配置**任务指南（**7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677)** 业务流程的一部分）以。

### <a name="building-a-format-selecting-another-format-as-a-base-customization"></a>构建选择其他格式作为基础的格式（自定义）

ER 可让您通过从 LCS 导入的当前组件版本（基本）创建（派生）新组件。 例如，用户想派生一种新的格式以履行某些特殊电子单据要求（如额外字段或广泛描述）来支持自定义方案。 若要详细了解此方案，播放 **ER 通过采用新基础版本的格式来升级格式**任务指南（**7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677)** 业务流程的一部分）。

### <a name="upgrading-a-format-selecting-a-new-version-of-base-format-rebase"></a>升级选择新版本的基础格式（重定基）的格式

ER 支持在当前草稿版的派生组件中自动采用最新版本的基础组件的更改的功能。 此流程称为*重定基本值*。 例如，新的法规性更改（将在从 LCS 导入的最新版的格式组件中引入）可自动合并到电子单据此格式的自定义版本中。 任何不能自动合并的更改视为冲突。 这些冲突将在相应组件的设计器工具中呈现以进行手动解决。 若要详细了解此方案，播放 **ER 通过采用新基础版本的格式来升级格式**任务指南（**7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677)** 业务流程的一部分）。

## <a name="list-of-er-configurations-that-are-delivered-in-the-dynamics-365-for-operations-solution"></a>在 Dynamics 365 for Operations 解决方案中交付的 ER 配置列表
| 特定于域的数据模型配置︰标题 | 域                | 数据模型依赖格式配置︰标题 | 说明                                                        |
|--------------------------------------------------|-----------------------|---------------------------------------------------|--------------------------------------------------------------------|
| 审计文件模型                                 | 财务审计       |                                                   |                                                                    |
|                                                  |                       | 审计文件 (NL)                                   | 荷兰审计文件格式                                  |
| BAS 模型                                        | 纳税申报         |                                                   |                                                                    |
|                                                  |                       | BAS（澳大利亚）                                          | 澳大利亚的 BAS 格式                                           |
| Construction industry scheme 模型               | 纳税申报         |                                                   |                                                                    |
|                                                  |                       | CIS 每月报表（英国）                           | 英国的 CIS 每月报表格式                   |
| 催款单模型                          | 电子开票  |                                                   |                                                                    |
|                                                  |                       | OIOUBL 催款单（丹麦）                     | 丹麦的 OIOUBL 催款单格式                        |
| 电子分类科目模型（墨西哥）          | 纳税申报         |                                                   |                                                                    |
|                                                  |                       | 辅助分类帐 XML（墨西哥）                         | 墨西哥帐户报表格式的辅助分类帐交易记录 |
|                                                  |                       | 会计科目表 XML（墨西哥）                         | 墨西哥会计科目表格式                          |
|                                                  |                       | 日记帐 XML（墨西哥）                                 | 墨西哥的日记帐交易记录报表格式                      |
|                                                  |                       | 试算平衡表 XML（墨西哥）                            | 墨西哥试算平衡表报表格式                             |
| Elster 模型                                     | 纳税申报         |                                                   |                                                                    |
|                                                  |                       | Elster（德国）                                       | 德国 Elster 格式                                          |
| 欧盟销售清单模型                              | 贸易报告       |                                                   |                                                                    |
|                                                  |                       | 欧盟销售清单（德国）                                | 德国欧盟销售清单 TXT 格式                               |
|                                                  |                       | 欧盟销售清单（丹麦）                                | 丹麦欧盟销售清单 TXT 格式                               |
|                                                  |                       | 欧盟销售清单（法国）                                | 法国欧盟销售清单 XML 格式                                |
|                                                  |                       | 欧盟销售清单（荷兰）                                | 荷兰欧盟销售清单 XML 格式                           |
|                                                  |                       | 欧盟销售清单 TXT（英国）                            | 英国欧盟销售清单 TXT 格式                    |
|                                                  |                       | 欧盟销售清单 XML（英国）                            | 英国欧盟销售清单 XML 格式                    |
|                                                  |                       | 按列的欧盟销售清单报表                   | 按列的欧盟销售清单报表                                    |
|                                                  |                       | 按行的欧盟销售清单报表                      | 按行的欧盟销售清单报表                                       |
| FEC 核算模型（法国）                        | 纳税申报         |                                                   |                                                                    |
|                                                  |                       | FEC 会计数据 XML（法国）                      | 法国 FEC 会计数据导出 XML 格式                   |
| 德国审计文件                                | 财务审计       |                                                   |                                                                    |
|                                                  |                       | 德国审计文件输出                          | 德国和奥地利审计文件输出                          |
| 内部统计模型                                  | 贸易报告       |                                                   |                                                                    |
|                                                  |                       | 内部统计（德国）                                    | 德国内部统计格式                                       |
|                                                  |                       | 内部统计（丹麦）                                    | 丹麦内部统计格式                                       |
|                                                  |                       | 内部统计 INTRACOM（法国）                           | 法国内部统计 INTRACOM 格式                               |
|                                                  |                       | 内部统计 SAISUNIC（法国）                           | 法国内部统计 SAISUNIC 格式                               |
|                                                  |                       | 内部统计（荷兰）                                    | 荷兰内部统计格式                               |
|                                                  |                       | 内部统计（英国）                                    | 英国内部统计格式                            |
|                                                  |                       | 内部统计报表                                  | 内部统计 Excel 控制报表                                     |
| 客户发票模型                           | 电子开票  |                                                   |                                                                    |
|                                                  |                       | OIOUBL 项目贷方通知单（丹麦）                   | 丹麦的 OIOUBL 项目贷方通知单格式                      |
|                                                  |                       | OIOUBL 项目发票（丹麦）                       | 丹麦 OIOUBL 项目发票格式                          |
|                                                  |                       | OIOUBL 销售贷方通知单（丹麦）                     | 丹麦的 OIOUBL 销售贷方通知单格式                        |
|                                                  |                       | OIOUBL 销售发票（丹麦）                         | 丹麦的 OIOUBL 销售发票格式                            |
| OB 申报模型                             | 纳税申报         |                                                   |                                                                    |
|                                                  |                       | OB 申报（荷兰）                               | 荷兰的 OB 申报格式                          |
| 付款模型                                    | 付款              |                                                   |                                                                    |
|                                                  |                       | Betalingsservice（丹麦）                             | 丹麦的 Betalingsservice 付款格式                        |
|                                                  |                       | 汇票汇款（法国）                  | 法国的汇票汇款格式                      |
|                                                  |                       | BTL91（荷兰）                                        | 荷兰 BTL91 供应商付款格式                    |
|                                                  |                       | CFONB Prelevements（法国）                           | 法国的 CFONB 直接借记付款格式                       |
|                                                  |                       | CFONB Virements（法国）                              | 法国的 CFONB 国内供应商付款格式                    |
|                                                  |                       | Nordea 供应商（丹麦）                                | 丹麦 Nordea corporate netbank 供应商付款格式         |
|                                                  |                       | ANZ 直接贷记服务（澳大利亚）                    | 澳大利亚的 ANZ 直接贷记服务格式                 |
|                                                  |                       | CBA 直接贷记服务（澳大利亚）                    | 澳大利亚的 CBA 直接贷记服务格式                 |
|                                                  |                       | NAB 直接贷记服务（澳大利亚）                    | 澳大利亚的 NAB 直接贷记服务格式                 |
|                                                  |                       | STG 直接贷记服务（澳大利亚）                    | 澳大利亚的 STG 直接贷记服务格式                 |
|                                                  |                       | WBC 直接输入系统（澳大利亚）                      | 澳大利亚的 WBC 直接输入系统格式                   |
|                                                  |                       | DirectLink（新西兰）                                   | 新西兰的 DirectLink 格式                              |
|                                                  |                       | JBA 付款文件（日期）                             | 日本 JBA 付款格式                                       |
|                                                  |                       | ISO20022 贷方转帐                          | 欧洲 SEPA 贷方转帐格式                             |
|                                                  |                       | ISO20022 贷方转帐（法国）                     | 法国 SEPA 贷方转帐格式                             |
|                                                  |                       | ISO20022 贷方转帐（德国）                     | 德国 SEPA 贷方转帐格式                            |
|                                                  |                       | ISO20022 贷方转帐（荷兰）                     | 荷兰 SEPA 贷方转帐格式                    |
|                                                  |                       | ISO20022 直接借记                             | 欧洲 SEPA 直接借记格式                                |
|                                                  |                       | ISO20022 直接借记（法国）                        | 法国 SEPA 直接借记格式                                |
|                                                  |                       | ISO20022 直接借记（德国）                        | 德国 SEPA 直接借记格式                               |
|                                                  |                       | ISO20022 直接借记（荷兰）                        | 荷兰 SEPA 直接借记格式                       |
|                                                  |                       | BACS（英国）                                         | 英国的 BACS 供应商付款格式                  |
| 冲销费用                                   | 纳税申报         |                                                   |                                                                    |
|                                                  |                       | 冲销费用销售清单                         | 冲销费用销售清单格式                                   |
| 荷兰 XBRL 集成模式                     | XBRL 报表        |                                                   |                                                                    |
|                                                  |                       | Semansys XBRL（荷兰）                                | 荷兰 Semansys XBRL 导出格式                    |
| GAF 模型（马来西亚）                                   | 财务审计       |                                                   |                                                                    |
|                                                  |                       | GAF 文件（马来西亚）                                     | 马来西亚的 GAF 格式                                         |
| 供应商帐龄分析表（中国）                         | 供应商数据分析 |                                                   |                                                                    |
|                                                  |                       | 供应商帐龄分析表格式（中国）                   | 中国供应商帐龄分析表格式                               |
| 供应商发票申报模型                 | 供应商数据分析 |                                                   |                                                                    |
|                                                  |                       | 供应商发票申报（冰岛）                   | 冰岛的供应商发票申报格式                      |
|                                                  |                       | 供应商发票申报报表（冰岛）            | 冰岛的供应商发票申报报表                      |



<a name="see-also"></a>请参阅
--------

[本地化要求 – 创建电子申报配置](electronic-reporting-configuration.md)

[管理电子申报配置生命周期](general-electronic-reporting-manage-configuration-lifecycle.md)





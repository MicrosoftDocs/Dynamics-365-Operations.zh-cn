---
title: 与 Finance 集成的常见问题
description: 本主题说明在 Human Resources 和 Finance 集成中要同步哪些数据。
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 308e2a538666522edf4a76be13b93c82c3f3a774
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071102"
---
# <a name="integration-with-finance-faq"></a>与 Finance 集成的常见问题


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



此主题回答有关在 Dynamics 365 Human Resources 与 Dynamics 365 Finance 集成时同步的数据的常见问题。

## <a name="can-i-edit-the-dynamics-365-talent-application-user-in-power-apps"></a>是否可以在 Power Apps 中编辑 Dynamics 365 Talent 申请用户？

编号 如果您编辑 Human Resources 应用程序用户，Human Resources 和 Dataverse 之间的集成可能会失败。 下表显示 Talent 申请用户的默认设置。

| 全名 | 申请 ID | Azure AD 对象 ID | 申请 ID URI |
| --- | --- | --- | --- |
| Dynamics 365 for Talent | f9be0c49-aa22-4ec6-911a-c5da515226ff | 27fd8129-4b3c-43f7-b1bf-47495d3a049b | f9be0c49-aa22-4ec6-911a-c5da515226ff |

![Talent 申请用户的默认设置。](media/DynamicsApplicationUser.png)

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a>所有数据均同步还是只是一些数据实体？

将同步一部分数据。 有关所有实体的列表，请参阅[与 Dynamics 365 Finance 的集成](hr-admin-integration-finance.md)。

## <a name="why-dont-i-see-any-data-synced-to-dataverse"></a>为什么我看不到任何数据同步到 Dataverse？

默认情况下，Dataverse 集成在不包含提供的演示数据的新环境中处于关闭状态。 默认情况下，在包含演示数据的新环境中将其打开，并且在设置环境后即开始数据同步。 环境准备好可以同步数据后，可以打开集成。 有关详细信息，请参阅[配置 Dataverse 集成](hr-admin-integration-common-data-service.md)。

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a>我可以不使用模板创建新映射吗？

模板是起点。 您可以创建自己的模板，但在创建集成项目时始终需要模板。 有关数据集成器 (DI)、模板和项目的详细信息，请参阅[将数据集成到 Microsoft Dataverse](/powerapps/administrator/data-integrator)。

## <a name="can-i-map-financial-dimensions-to-transfer-between-human-resources-and-finance"></a>我可以映射在 Human Resources 和 Finance 之间转移的财务维度吗？

Financial dimensions 当前不在 Dataverse 中，因此不是默认模板的一部分。 此实体已计划，但当前未确定发布时间。

对于位于 Finance 但不存在于 Human Resources 中的数据，请使用 Human Resources 中的 **配置链接** 将两个系统链接在一起。

![映射财务维度。](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a>在某些情况下，当我导入员工时，他们在 Finance 中成为空闲工作人员。 为什么？

如果员工在 Human Resources 中没有活动雇用详细信息记录，您可能收到此错误。 若要解决此问题，请转到 **人员管理 \> 员工 \> 雇佣历史记录 \> 日期管理器**，验证是否有活动雇用详细信息记录。

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a>如果我选择仅映射一部分字段，对非映射字段所做的更改是否会触发同步？

数据同步按照执行计划进行。 集成将在记录中的任意字段更改时提取该记录，不论字段是否是集成映射的一部分。

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a>我如何仅发送有效工作人员的更改而不发送已离职的记录？

使用“高级查询”，您可以在将数据传递到目标前筛选并改造源数据。

![可用工作人员高级查询。](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a>我可以指定将特定实体的哪些字段发送到 Finance 吗？

字段可以在集成任务中添加或删除。 并非 Dataverse 表上存在的所有数据字段都从 Human Resources 填充。
附加数据可以通过 Power Apps 填充。

![在集成任务中添加或删除字段。](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-human-resources-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a>我将集成设置为批处理作业，但 Human Resources 失去了与目标系统的连接。 我如何将同一组更改发送到目标系统？

异常处理不需要特殊设置。 数据集成器将自动捕获和报告在源和目标发生的错误，并允许手动重试。 但是，它不允许手动数据更正。 如果需要更新数据，这应在源或目标发生。

## <a name="can-i-set-up-bi-directional-integration"></a>我可以设置双向集成吗？

否，集成现在是单向的（Human Resources 到财务和运营）。 不过，提供了默认模板将数据从 Human Resources 发送到 Finance。

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a>我在集成时可以允许删除记录吗？

否，数据集成器不会捕获已删除的数据传输记录。 目前仅包括数据创建和更新 (UPSERT)。

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a>我可以重新运行出错的执行吗？ 如果可以，是发送完整文件还是仅更改部分？

数据集成器的首次运行始终是完整运行。 后续运行基于更改跟踪。 在错误运行执行时，它会提取运行作用域内的记录并发出 Dataverse 中的最近更改。

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a>当我保存项目时，发生错误：“项目存在映射错误”。 我该做什么？

检查您的集成密钥的设置，对设置进行任何所需的更改，然后刷新项目中的实体。

在使用默认模板时，集成密钥将自动导入。 在新任务添加到现有模板时，可能发生此问题。

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a>如果我有 N 个工作人员有雇用关系的法人，我是否需要为每个法人创建映射？

是，对于 Finance 中的每个法人，您需要在数据集成中有单独的集成项目。

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a>我需要转移不是 Microsoft 提供的默认模板一部分的数据。 我可以这样做吗？

可以，字段可以在现有模板中添加或删除。 模板可以修改成包括其他 Dataverse 表中的其他数据。 实体必须在 Dataverse 中才能够包含在模板中。 

## <a name="i-just-created-new-finance-and-human-resources-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a>我只是创建了新的 Finance 和 Human Resources 环境，但发生错误“数据值违反了完整性约束”。 为什么？

此错误的原因可能包括：

- 数据转移导致源 (Dataverse) 发生了重复的记录提取。

- 数据转移在 Finance and Operations 中必填的字段中包含空值。 验证 Dataverse 中的数据以及是否满足 Finance and Operations 的要求。

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a>如果存在执行错误，并且员工 ID 未同步，我如何找到具有失败员工记录的历史作业？

数据集成器将在 Finance 中创建多个项目。 数据集成器任务与 Finance 项目之间的关系是一对一。

跟踪 Finance 中数据集成器执行历史记录的时间并查找索引 -1 项目。 如果任务编号在数据集成器中是 9，索引在 Finance 中则是 8。

1. 从数据集成器捕获任务索引（在本示例中是“9”）。

    ![从数据集成器捕获任务索引。](media/CaptureTaskIndex.png)

2. 跟踪项目的执行时间。

    ![跟踪项目的执行时间。](media/CaptureTimeOfExecution.png)

3. 在 Finance 中，识别索引 - 1。 在此示例中，后缀为“8”的项目和索引“0”项目的执行时间与步骤 2 中的执行时间匹配。

    ![标识索引。](media/IdentifyIndex.png)

## <a name="after-integrating-human-resources-and-finance-i-dont-see-my-human-resources-data-in-finance-what-do-i-do"></a>集成 Human Resources 和 Finance 之后，我在 Finance 中看不到我的 Human Resources 数据。 我该做什么？

与 Finance 的集成是一个两步流程。 首先，验证 Human Resources 数据在 Dataverse 中已更新并可用。 这是一个接近实时的同步，可以在 Power Apps 中通过查看数据表中的数据验证。

![Dataverse 中的数据。](media/DataInCDS.png)

如果数据未按预期出现在 Dataverse 中，请验证集成中是否支持该实体。 若要在 Dataverse 中包括附加数据，需要 Microsoft 一端进行更改。

如果实体受支持，且数据在 Dataverse 中可用，请验证映射在数据集成器中是正确的。 如果集成器映射看起来正常，则验证数据管理作业是否成功运行。 错误可能在执行批处理作业时发生。 有关数据管理的详细信息，请参阅[数据管理](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json)。

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a>我在将员工地址导入 Finance 之后，这些地址不正确。 我应该怎么做？

**位置 ID** 的编号规则在 Human Resources 和 Finance 中使用相同模式。 编号规则在两端都需要是唯一的，以便在将数据从 Dataverse 集成到 Finance and Operations 时没有地址冲突。

在实施 Human Resources 时，请验证编号规则在 Human Resources 和 Finance 中不同。 验证数据可以在两个系统中维护的情况的所有编号规则是不同的。

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a>当创建连接集时，我无法在“连接”下拉列表中看到连接。 我该做什么？

请确保在创建连接时，您选择的是 Dynamics 365 Finance 和 Dataverse。

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a>当同步雇佣时，发生错误“CompanyInfo_FK 不存在”或“未在相关表‘雇佣’中找到字段‘雇佣结束日期’中的值‘12/31/2154 11:59:59 pm’”。我应该怎么做？

确保您在映射到正确的法人。 法人同步不是默认模板的一部分，因此，Human Resources 和 Dataverse 中存在的每个法人也会出现在 Finance 中。 此外，还请确保您为关联的连接集选择了正确的法人。

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a>在设置我的项目后，Finance 的字段映射似乎是空的。 我应该怎么做？

通过转到 **数据管理 \> 框架参数 \> 实体设置 \> 刷新实体列表** 刷新 Finance 中的数据实体。 这应需要两三分钟完成，然后您应该看到这些映射。 在已创建新项目时，将发生此问题。

![缺少字段映射。](media/MissingFieldMapping.png)

## <a name="additional-resources"></a>其他资源

- 数据集成器 (DI)： 

  - [将数据集成到 Microsoft Dataverse](/powerapps/administrator/data-integrator)

  - [数据集成器错误管理和故障排除](/powerapps/administrator/data-integrator-error-management)

  - [响应 Power Apps、Microsoft Power Automate 和 Dataverse 中系统生成日志的 DSR 请求](/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- 数据管理：

  - [数据管理](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

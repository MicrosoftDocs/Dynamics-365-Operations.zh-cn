---
title: "将 Dynamics AX 2012 更新至 Dynamics 365 for Finance and Operations Enterprise Edition"
description: "此主题描述当前运行 Microsoft Dynamics AX 2012 的客户可以用来将其数据和代码移动到 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 的流程。"
author: tariqbell
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations Platform
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 8
ms.translationtype: Human Translation
ms.sourcegitcommit: 6816e3820ab77c71bbf9bde4a068375448331671
ms.openlocfilehash: 13507fcf9c0d626709aeb4e00a8632411204c20f
ms.contentlocale: zh-cn
ms.lasthandoff: 06/15/2017

---

# <a name="upgrade-microsoft-dynamics-ax-2012-to-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition"></a>将 Microsoft Dynamics AX 2012 更新至 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition

[!include[banner](../includes/banner.md)]

在平台更新 8，Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中，提供当前运行 Microsoft Dynamics AX 2012 的客户可以用来将其数据和代码移动到 Finance and Operations 的升级路径。 升级过程在以下元素上生成：

- 帮助您从 AX 2012 提供现有自定义应用程序代码的工具。
- 可用来提供数据库的数据升级过程。 因此，您可以升级您的完整历史记录。

## <a name="overview"></a>概览

整个升级过程可以可视化为三个总体阶段：分析、执行和验证。

下图显示端对端升级过程以及我们视为各阶段一部分的活动。 

![升级过程](./media/upgrade-process.png)

## <a name="analyze"></a>分析

分析阶段中的活动帮助您估计升级所需的工作。 它们还帮助您准备项目计划。 这些活动可以在购买 Finance and Operations 前完成。 它们将提供关于您需要的工作和资源的数据点，从而帮助您做出明确的采购决策。

### <a name="sign-up-for-a-public-preview-in-lcs"></a>在 LCS 中注册公开预览

要在购买 Finance and Operations 前执行分析活动，您可以注册公开预览。 公开预览可以让您部署您自己的 Finance and Operations 环境。 它还允许您访问 Microsoft Dynamics Lifecycle Services (LCS) 中用于评估您的 AX 2012 环境和您的现有自定义代码的工具。

如果您的 AX 2012 具有现有 LCS 项目，您仍必须注册一个额外的新项目以评估 Finance and Operations。

有关如何为客户获取公开预览的信息，请转到 https://mbs.microsoft.com/customersource/global/AX/news-events/news/Microsoft_Dynamics_AX_Public_Preview。

有关如何为合作伙伴获取公开预览的信息，请转到 https://mbs.microsoft.com/partnersource/global/news-events/news/Microsoft_Dynamics_AX_Public_Preview。

请注意，此公开预览与 [30 天试用](https://aka.ms/D365OperationTrials) 不同。 三十天试用提供已部署的 Finance and Operations 实例，可用来探索和评估应用。 但是，分析活动要求完整的 LCS 体验和工具。

### <a name="select-the-upgrade-methodology"></a>选择升级方法
在您的新 LCS 项目中，将项目方法设置为**将 AX 2012 升级到 Dynamics 365 for Operations**。 此方法专门适用于正在升级的 AX 2012 客户。 它详细描述了三个阶段，并提供关于此流程的所有支持文档的链接。

![升级方法(./media/methodology.png)
 
### <a name="run-the-upgrade-analyzer"></a>运行升级分析器
升级分析器工具针对您的 AX 2012 环境运行，并标识您在准备 AX 2012 环境时应执行的任务，这有助于让升级体验更加流畅和节约成本：

- **数据清除** - 此流程帮助您识别您可以移除的数据，同时不会导致功能的丧失。 此工具标识您通过运行清除流程可以减少的不同数据类型。 对于每种数据类型，给出了关于清除的影响的解释。 您可以决定是否运行清除流程。 您的 Finance and Operations 订阅的部分成本基于数据库的大小。 因此，通过减少大小，您可以减少该部分订阅成本，同时还有助于减少升级实施流程所需的时间。 更小的数据库有助于保障更快的升级速度。
- **SQL 配置** - 此过程审核 SQL 配置和建议优化。 通过确保 SQL 的优化执行，此过程有助于减少升级实施过程所需的时间。
- **弃用的功能** - 此过程标识您当前使用的功能，但在 Finance and Operations 中不可用。 因此，此过程有助于您今早发现功能差异。 它还提供替代方案建议。

此外，作为此步骤的一部分，您必须在 AX 2012 环境中安装 KBXXXXXXX。 此修补程序提供预升级核对清单。 在 AX 2012 环境中，您可以使用此核对清单输入升级过程所需的数据。 例如，在一个预升级核对清单任务中，您为每个当前 AX 2012 用户提供 Microsoft Azure Active Directory (Azure AD) 登录信息，以便每个用户能够登录到 Finance and Operations。

此步骤的输出成为您的 AX 2012 系统管理员的升级项目计划中的工作流。

有关详细信息，请参阅 [分析：使用升级分析器计划迁移工作](upgrade-analyzer-tool.md)。

### <a name="run-the-code-upgrade-estimation-tools"></a>运行代码升级估计工具
此步骤从 AX 2012 提取您的代码，将其转换为新格式，并提供开发人员必须稍后解决的冲突的相关反馈。 此步骤构成您的代码升级成本估计的基础。

要完成此步骤，您必须将您的代码从 AX 2012 导出为模型库导出，并将其上载到 LCS 代码升级工具。 代码升级工具将生成您的代码的升级版本以及关于您必须解决的剩余冲突的报告。 您的开发人员可查看升级代码和报告以确定升级您的代码库所需的工作。

此步骤的输出表示您的 Microsoft Dynamics AX 开发人员的升级项目计划中的工作流。

有关详细信息，请参阅 [分析：估计升级代码所需的工作](analyze-code-upgrade.md)。

### <a name="deploy-a-demo-environment"></a>部署演示环境
演示环境是包含演示数据（不是您自己的数据）和标准代码（不是自定义项）的默认环境。 我们建议您部署演示环境以评估新功能和执行在 AX 2012 中使用但可能在 Finance and Operations 中已经更改的标准流程的基本填补差距分析。 您可以在 Azure 中部署这些演示环境或将它们下载为在您自己的硬件上运行的虚拟机 (VM)。 如果在 Azure 中部署，您必须提供您的 Azure 订阅，因为您仍在使用公开预览项目，且尚未购买 Finance and Operations 订阅。

此步骤的输出表示您的功能用户或业务用户的升级项目计划中的工作流。

有关详细信息，请参阅 [分析：部署沙盒环境](analysis-sandbox.md)

### <a name="create-a-project-plan"></a>创建项目计划
升级方法中提供了项目计划的模板。 在此步骤中，来自分析阶段前面步骤的输出用于填充升级项目的项目计划。 项目计划还将包含所有测试详细信息：数据升级测试、转换测试、功能测试传递迭代以及关于这些任务的不同资源分配的详细信息。

在此阶段，项目计划提供一个数据点，它可以帮助您了解升级到 Finance and Operations 将需要的时间和成本。

## <a name="execute"></a>执行
在执行阶段，您执行在分析阶段计划的任务。 要进入执行阶段，您必须购买 Finance and Operations，还必须具有可以进行升级的可用资源。

### <a name="switch-to-the-lcs-implementation-project"></a>切换到 LCS 实施项目
您用于分析阶段的公开预览项目已实现其目的。 您现在可以丢弃它。 对于剩下的步骤，您仅需要在分析阶段的最后一步创建的项目计划。

购买 Finance and Operations 订阅时，您将收到关于任何注册新 LCS 项目的详细信息。 该项目被称为实施项目，并且将成为您的订阅的新的永久性 LCS 项目，只要您拥有该订阅。 此项目与公开预览计划的不同之处在于它由 Microsoft 管理。 因此，此项目具有以下特征：

- 项目中的所有环境在 Azure 中托管。
- 与项目关联的 Azure 订阅由 Microsoft 管理。 因此，不对 Azure 成本单独计费。 该成本涵盖在您的 Finance and Operations 订阅中。
- 项目中的生产环境由 Microsoft 维护。 因此，代码部署、升级和基础结构维护直接由 Microsoft 运行，而不是由您的员工运行。 

### <a name="perform-the-ax-2012-preparation-tasks"></a>执行 AX 2012 准备任务
完成升级分析器工具已发现且在您的升级项目计划中记录的任务。 您的 Microsoft Dynamics AX 系统管理员和数据库管理员 (DBA) 必须完成这些任务。

[将 AX 2012 中的数据升级到 Dynamics 365 for Operations – AX 2012 中的预升级核对清单](prepare-data-upgrade.md)

### <a name="perform-code-upgrade"></a>执行代码升级
完成在分析阶段的代码升级估计步骤期间计划的任务。 您的开发人员必须运行这些任务。

从此时起，AX 2012 中的代码更改应被锁定。 AX 2012 中应仅允许紧急代码更改。 如果做出更改，必须手动将其导入到新的代码库。

### <a name="develop-new-code"></a>开发新代码
完成在分析阶段的“部署演示环境”步骤期间执行的填补差距分析的任务。 这些任务将可能是功能任务的组合，这些功能任务定义与使用的新功能相关的自定义项的配置和开发任务。

### <a name="data-upgrade-development-environment"></a>数据升级（开发环境）
完成代码升级任务后，您可以首次将您的 AX 2012 数据库升级到 Finance and Operations。 第一次升级发生在开发环境中，因此您可以更加轻松地纠正或调试在此阶段发现的任何问题。 在开发环境中，可立即调试问题，调整代码，并且可以在几分钟后再次运行升级。 更大的沙盒环境不提供此敏捷性，至少需要几个小时调试和纠正问题、更新代码、部署更新的代码和再次运行升级。

下图显示了此流程。 只需备份 AX 2012 数据库，将其上载到 Azure，还原到 Finance and Operations 环境，然后运行数据升级。

![开发环境中的数据升级](./media/data-upgrade-dev.png)
 
数据升级通过特殊类型的可部署包完成。 相同机制用于将一个环境中的新 Finance and Operations 代码部署到另一个环境。

用于在此流程期间转换数据库中的数据的基础框架大部分与基于运行 **ReleaseUpdatexxx** 类的 X++ 批作业的 AX 2012 中的升级框架相同。

有关详细信息，请参阅 [在开发环境中将 AX 2012 的数据升级到 Dynamics 365 for Operations](data-upgrade-2012.md)。

### <a name="data-upgrade-sandbox-environments"></a>数据升级（沙盒环境）
在开发环境中完成数据升级后，可以在沙盒环境中运行相同流程。 沙盒环境是业务用户和功能团队成员可以在其中通过使用升级后的 AX 2012 数据和代码测试业务流程的环境。

下图显示在沙盒环境中运行数据升级的流程。 此处的不同之处在于使用的是 bacpac 工具，而不是传统的 SQL 备份。 在 Microsoft SQL Server 和 Azure SQL 数据库之间进行转换要求使用此工具。 这是一个标准 SQL 工具，并非特定于 Finance and Operations。

![沙盒环境中的数据升级](./media/data-upgrade-sandbox.png)

有关详细信息，请参阅 [在沙盒环境中将 AX 2012 的数据升级到 Dynamics 365 for Operations](upgrade-data-sandbox.md)。
 
## <a name="validate"></a>复核
当您进入验证阶段后，您将具有包含升级的自定义代码和升级的数据的可用环境。 此阶段描述验证和测试升级后的环境是否如期工作的流程。 它还描述实施准备流程。

### <a name="perform-cutover-testing-and-create-a-cutover-plan"></a>执行转换测试和创建转换计划
术语_转换_在此处用于描述将新系统上线的最终流程。 此流程包括在关闭 AX 2012 后和打开 Finance and Operations 前发生的任务。 

测试的目的是实践转换流程。 此方法有助于保证参与实际转换到实施的每个人都将获得一个平稳的体验。

有两个主要工作流：

- **技术工作流** –此工作流是运行数据升级的流程。 您的公司将对允许的停机时间量执行限制。 在此停机时间期间，AX 2012 和 Finance and Operations 都不可用。 技术工作流可能必须对其数据升级过程进行性能优化以满足企业的停机时间限制。 
- **功能工作流** - 在数据升级后，需要在 Finance and Operations 环境中执行若干配置任务。 必须记录和量化所有这些任务，并对它们分配资源，因为它们必须与企业停机时间限制内的技术任务匹配在一起。

有关详细信息，请参阅 
- [验证：直接转换测试](upgrade-cutover-testing.md)
- [验证：应用验证流程](app-validation-process.md)

### <a name="functional-test-pass"></a>功能测试传递
对所有业务流程完成一个完整的功能测试传递。 此测试传递将对涉及 Finance and Operations 的所有业务流程进行广泛的重新测试。 这些业务流程包括从 AX 2012 提取的旧流程和涉及在 Finance and Operations 中第一次使用的新功能的新流程。 

根据代码质量，问题补救和重新测试可能要求若干功能测试传递迭代。 问题解决后，请务必重新测试涉及的所有流程，以帮助保证下游或上游流程不受变更的影响。

有关详细信息，请参阅 [验证：功能测试](upgrade-functional-validation.md)。

### <a name="pre-go-live-checklist"></a>预实施核对清单
预实施核对清单是一个推荐的过程，可以帮助减少最终转换到实施期间发生错误的几率。 在实施到期的前一周，停止 AX 2012 中（即在\<模块\>\设置下）的配置更改。 此配置更改限制仅仅是程序性的。 Microsoft Dynamics AX 系统管理员仅同意此时将此类型的更改暂停。

我们还建议您锁定 Finance and Operations 代码库中的代码更改。 不允许任何进一步的更改，除非这些更改已经过评估，并且已表明不会阻止实施。  

配置限制和代码锁定就绪后，应在转换前最后一次运行数据升级。 通过此方法可以确保一切仍按预期工作。 

有关详细信息，请参阅 [验证：准备实施](upgrade-go-live-prep.md)。



### <a name="supported-upgrade-paths"></a>支持的升级路径
从 2017 年 6 月起，支持从 Microsoft Dynamics AX 2012 R3 升级到 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 版本 0617。 支持 AX 2012 R3 的所有累计更新 (CU)。

目前不支持 Microsoft Dynamics AX 2012 R2 和 Microsoft Dynamics AX 2012 RTM。 在 2017 年的晚些时候将增加支持。

仅支持升级到 Finance and Operations 的云部署版本。 不支持升级到本地版本。 将在 2017 年的晚些时候增加升级到本地版本的支持。


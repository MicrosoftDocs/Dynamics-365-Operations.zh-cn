---
title: Dynamics 365 Human Resources 客户迁移到财务和运营基础结构
description: 本文介绍 Microsoft Dynamics 365 Human Resources 的客户向财务和运营基础结构的迁移。
author: twheeloc
ms.date: 10/25/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4df9a68ea0128378224bf77bd66423fd2e13fa55
ms.sourcegitcommit: e5b290bac7e8f468167caa1a5607aac6eac9aaea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/11/2022
ms.locfileid: "9760354"
---
# <a name="dynamics-365-human-resources-customer-migration"></a>Dynamics 365 Human Resources 客户迁移

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

客户迁移是客户数据库到财务和运营基础结构的“直接迁移”（移动）。 在客户迁移中使用了自动迁移工具。 结果是生成了使用客户的 Human Resources 数据库的新财务和运营环境。

## <a name="prerequisites"></a>先决条件

### <a name="user-access-and-permissions"></a>用户访问和权限

- Microsoft Dynamics Lifecycle Services 用户应具有 **组织管理员** 角色。
- 用户应能够[创建 Azure DevOps 项目](/azure/devops/organizations/projects/create-project)或使用现有的 Azure DevOps 项目。
- 用户应该有权[创建 Azure DevOps 个人访问安全令牌](/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate)，或者应该有一个可以使用的令牌。

### <a name="dataverse-environment-backup-sandbox"></a>Dataverse 环境备份（沙盒）

 - 可选但推荐：使用 Human Resources 生产环境的副本刷新现有的 Human Resources 沙盒环境。
 - 使用 Power Platform 管理中心创建新的 Dataverse 环境。
 - 将链接到独立 Human Resources 应用的现有 Dataverse 环境复制到您在上一步中创建的环境中。

> [!NOTE]
> 添加数据库时，确保将 **启用 Dynamics 365 应用** 选项设置为 **是**。 有关详细信息，请参阅[准备 Power Platform 环境](hr-cust-migration.md#prepare-a-power-platform-environment)

### <a name="dataverse-capacity"></a>Dataverse 容量

1. 使用 Power Platform 管理中心中的 **摘要** 页面验证 [Dataverse 存储](/power-platform/admin/finance-operations-storage-capacity)是否有足够的可用容量存储环境副本。
2. 如果没有足够的可用容量，使用[释放存储空间指南](/power-platform/admin/free-storage-space)来减少总体消耗。 客户还可以[增加额外的存储容量](/power-platform/admin/add-storage)。

## <a name="customer-migration-process"></a>客户迁移流程

### <a name="create-a-lifecycle-services-project-for-human-resources-migration"></a>为 Human Resources 迁移创建 Lifecycle Services 项目

第一步是在 Lifecycle Services 中创建一个新的财务和运营实施项目。 客户将有一个现有的 Human Resources Lifecycle Services 项目。 现有的 Human Resources 环境将被迁移到新的财务和运营实施项目中。

要创建新项目，请按以下步骤进行操作。

1. 以全局管理员或指定的服务帐户用户身份登录 Lifecycle Services。
2. 在 Lifecycle Services 主页上，选择 **创建/新建 (+)**。
3. 选择财务和运营应用作为产品。
4. 在 **项目用途** 字段中，选择 **实施**。
5. 输入项目名称和描述。
6. 在 **项目自定义类型** 字段中，选择 **Microsoft Dynamics 365 Human Resources 迁移**。
7. 选中复选框同意条款和条件。
8. 选择 **创建**。

创建新的 Lifecycle Services 项目后，按照以下步骤进行设置和配置。

1. 选择 **项目加入** 完成项目加入。 有关详细信息，请参阅[项目入门](../fin-ops-core/dev-itpro/lifecycle-services/project-onboarding.md)。

    - 选择与当前环境相同的区域。 此选择不会影响迁移。
    - 对于旧系统，选择 **其他**。

2. 完成项目设置。 作为此步骤的一部分，您应该配置 SharePoint Online 库、Azure DevOps 和 Azure 连接（如果需要）。 有关详细信息，请参阅 [Lifecycle Services (LCS) 用户指南](../dev-itpro/lifecycle-services/lcs-user-guide.md)。

> [!NOTE]
> 客户可以使用现有的 Azure DevOps 项目和关联的个人访问安全令牌。 如果使用现有项目，与该项目相关的配置将自动可用，并可以检查其准确度。

### <a name="migrate-a-human-resources-sandbox-environment"></a>迁移 Human Resources 沙盒环境

#### <a name="prepare-to-migrate-the-sandbox-environment"></a>准备迁移沙盒环境

创建新的 Lifecycle Services 项目并完成项目加入过程后，您就可以迁移您的第一个环境了。 在开始此过程之前，我们建议您刷新要从独立基础结构上的生产环境迁移的沙盒环境。

#### <a name="prepare-a-power-platform-environment"></a>准备 Power Platform 环境

> [!NOTE]
> 此步骤仅适用于沙盒环境迁移。 当您迁移生产环境时，附加到生产环境的现有 Power Platform 管理中心环境将继续运行。 添加数据库时，确保将 **启用 Dynamics 365 应用** 按钮设置为 **是**。 

- 在 Power Platform 管理中心，[创建一个带有数据库的环境](/power-platform/admin/create-environment#create-an-environment-with-a-database)来用于沙盒迁移，或选择现有环境。
- [复制环境](/power-platform/admin/copy-environment)刷新用于映射的 Power Platform 环境。

#### <a name="migrate-the-sandbox-environment"></a>迁移沙盒环境

1. 以全局管理员或指定的服务帐户用户身份登录 Lifecycle Services。

    > [!NOTE]
    > 我们建议您使用命名的用户帐户。 登录用户应在独立的 Human Resources Lifecycle Services 项目中具有 **项目负责人** 或 **环境管理员** 安全角色。

2. 打开新创建的 Human Resources 迁移项目。
3. 查看并完成迁移方法和项目加入的相应阶段。
4. 在项目仪表板上的 **默认: 标准接受度测试** 窗格中，选择 **迁移 HR**。
5. 在 **选择要迁移的环境** 窗格中，选择适当的 Lifecycle Services 项目和原始 Human Resources 环境（从源独立 Human Resources 应用程序）。
6. 启用 **映射到新 Power Platform 环境**，选择相应的 Power Platform 环境。 然后选择 **下一步**。
7. 完成 **部署设置（财务和运营 – 沙盒）** 向导，确认详细信息和客户签核，然后选择 **部署**。

环境状态将显示进度。 状态将从 **正在加载** 变为 **正在部署**，然后变为 **已部署**。

> [!NOTE]
> 在完成实施项目准备核对清单之前，生产窗格不可用。 有关详细信息，请参阅[准备实施](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md)。

#### <a name="considerations-and-assumptions"></a>考虑因素和假设

租户上的 Lifecycle Services 项目中存在 Human Resources 沙盒环境，具有以下特征：

- Human Resources 沙盒环境未链接到现有的合并环境。 对于给定的 Human Resources 环境，一次只能进行一项迁移。
- 一次允许的沙盒环境数量取决于 Human Resources 许可。 如果为租户购买了足够的许可，其他沙盒环境将在项目的 **环境** 窗格中列出。
- 必须迁移到相同类型的环境。 换句话说，只能进行沙盒到沙盒或生产到生产的迁移。

    > [!NOTE]
    > 确定生产或沙盒状态时，仅考虑 Human Resources 环境类型。 如果环境分类错误（即生产环境被标记为沙盒环境，或沙盒环境被标记为生产环境），请联系客户支持。

- 如果迁移不成功，将显示失败错误消息，**删除** 按钮将可用。 使用此按钮可删除失败的迁移。 然后，您可以重新迁移环境。

#### <a name="validate-the-sandbox-migration"></a>验证沙盒迁移

沙盒迁移过程成功完成后，创建详细的测试计划来验证和签核所有业务流程。

在开始测试之前，请验证以下详细信息：

- 确认可通过生成的 URL 访问迁移的环境。
- 确认用户可以访问迁移的沙盒。
- 确认与迁移的沙盒环境关联的 Dataverse 环境可以访问。
- 抽查不同数据，确认最新的数据可用。
- 完成关键的验证业务流程。
- 确认您的安全策略适用。
- 确认批处理作业按预期触发。

您没有对迁移的沙盒的远程桌面访问权限。 您可以使用自助服务功能和工具对您的第 2+ 层沙盒环境执行以下操作：

- 访问 [Azure SQL 数据库](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-the-azure-sql-database)。
- 访问[日志文件](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-log-files)。
- 使用[性能监视器工具](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#use-perfmon-tools)。
- [打开/关闭维护模式](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-self-service-logs)。
- 重新启动[服务](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#restart-services)。
- 配置 [Regression Suite Automation Tool](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#configure-the-regression-suite-automation-tool)。

有关详细信息，请参阅[自助服务部署常见问题](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md)。

### <a name="migrate-a-human-resources-production-environment"></a>迁移 Human Resources 生产环境

完成迁移和验证沙盒环境后，按照以下步骤迁移生产环境。

#### <a name="prerequisites"></a>先决条件

- 应完成订阅估算器。
- 应完成实施[准备评估](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md)。

#### <a name="migrate-the-production-environment"></a>迁移生产环境

1. 以全局管理员或指定的服务帐户用户身份登录 Lifecycle Services。

    > [!NOTE]
    > 我们建议您使用命名的用户帐户。 登录用户应在 Lifecycle Services 项目中具有 **项目负责人** 或 **环境管理员** 安全角色。

2. 打开新的 Human Resources 迁移项目。
3. 查看并完成迁移方法和项目加入的相应阶段。
4. 在项目仪表板上的 **生产** 窗格中，选择 **迁移 HR**。
5. 在 **选择要迁移的环境** 窗格中，选择适当的 Lifecycle Services 项目和原始 Human Resources 环境（从源独立 Human Resources 应用程序）。 然后选择 **下一步**。
6. 完成 **部署设置（财务和运营 – 沙盒）** 向导，确认详细信息和客户签核，然后选择 **部署**。

环境状态将显示部署进度。 状态将从 **正在加载** 变为 **正在部署**，然后变为 **已部署**。

#### <a name="post-migration-considerations"></a>迁移后注意事项

- 对您的环境应用最新的[质量更新](/fin-ops-core/fin-ops/get-started/quality-updates)。
- 如果您使用的是[虚拟表](hr-admin-integration-common-data-service-virtual-entities.md)，重新配置终结点。
- 重新配置双写入集成。 评估必须启用哪些实体。
- 考虑使用虚拟表代替双写入进行集成。

#### <a name="dual-write-integration"></a>双写入集成

##### <a name="set-up-microsoft-power-platform-dual-write-integration"></a>设置 Microsoft Power Platform 双写入集成

1. 转到 Power Platform 管理中心，在左侧导航中选择 **环境**。
2. 选择之前复制/刷新的环境，确认状态为 **就绪**。
3. 转到 Lifecycle Services，确认迁移项目的状态为 **已部署**.
4. 在迁移的环境下，选择 **完整详细信息** 查看其他详细信息，并[设置双写入应用程序](../fin-ops-core/dev-itpro/data-entities/dual-write/lcs-setup.md#set-up-dual-write-for-new-or-existing-dataverse-environments)。
5. 在 **双写入应用程序配置** 窗格中，选中复选框以同意在数据库之间映射和同步数据，然后选择 **配置**。
6. 当消息框通知您双写入配置成功时，选择 **确定**。
7. 您可以在详细信息中监视配置的进度。
8. 配置完成后，选择 **链接到 Power Platform 环境** 同步可用的数据实体。
9. 当状态指示环境已成功链接时，转到 Power Platform 管理中心查看和选择相应的数据实体。
10. 在左侧窗格中，选择 **Dynamics 365 应用 \> 资源**。
11. 确认双写入 Human Resources 应用的状态为 **已启用**。
12. 选择双写入 Human Resources 应用，然后选择 **安装**。
13. 在 **安装双写入 Dynamics 365 Human Resources 应用** 窗格中，选择相应的环境来安装包。
14. 选择复选框以同意服务条款，然后选择 **安装**。
15. 在 Dynamics 365 应用环境中，在进行安装时，状态将为 **正在安装**。 安装完成时，将更新为 **已安装**。

##### <a name="review-and-apply-a-dual-write-solution"></a>查看并应用双写入解决方案

1. 在新的财务和运营环境中，转到 **数据管理 \> 双写入**。
2. 选择 **应用解决方案**。
3. 在窗格中，选择 **动态已安装解决方案**、**双写入应用程序核心实体映射** 和 **Dynamics 365 Human Resources 映射**。 然后选择 **应用**。 一条消息将确认正在应用解决方案。 成功应用解决方案后，将显示所有可用的表映射。
4. 查看可用的表映射，使用双写入选择和运行集成。
5. 首次为表映射运行双写入集成时，选中 **初始同步** 复选框。 如果有来自源 Human Resources 环境的现有集成，在运行表映射集成时，不必选中 **初始同步** 复选框。

#### <a name="recommended-practices"></a>推荐做法

本节概述从独立基础结构迁移到财务和运营基础结构的建议。

- 我们强烈建议您与 Microsoft Dynamics 合作伙伴合作，在 Human Resources 环境迁移方面获得帮助。
- 计划适当的时间在沙盒迁移环境上进行完整的用户接受度测试 (UAT)。
- 计划并记录将集成迁移到迁移环境的详细步骤。
- 创建详细的核对清单来概括迁移的转换过程。
- 为您的业务计划迁移过程中的适当停机时长。
- 我们强烈建议获得 FastTrack 资格的客户让 FastTrack 解决方案架构师加入，以在监管迁移过程方面获得帮助。
- 我们强烈建议您在进行第一次迁移之前刷新独立基础结构中的沙盒环境。 此刷新应包括连接到您计划迁移到的沙盒环境的 Dataverse 环境。
- 我们强烈建议您在部署、迁移和创建 Lifecycle Services 项目时使用服务帐户。
- 计划在最新的正式发布 (GA) 版本上升级沙盒环境以进行 UAT 验证。 有关详细信息，请参阅[注意事项](hr-infrastructure-merge.md#considerations)。

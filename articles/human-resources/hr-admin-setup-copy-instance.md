---
title: 复制实例
description: 您可以使用 Microsoft Dynamics Lifecycle Services (LCS) 将 Microsoft Dynamics 365 Human Resources 数据库复制到沙盒环境。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bb363369994d99f358be0c23cdaf1dbc80b644e5
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092284"
---
# <a name="copy-an-instance"></a>复制实例

您可以使用 Microsoft Dynamics Lifecycle Services (LCS) 将 Microsoft Dynamics 365 Human Resources 数据库复制到沙盒环境。 如果您有另一个沙盒环境，还可以将数据库从该环境复制到目标沙盒环境。

要复制实例，您需要确保：

- 您要覆盖的 Human Resources 实例必须是沙盒环境。

- 您要从中复制或向其复制的环境必须位于同一区域。 不能跨区域复制。

- 您必须是目标环境中的管理员，这样您才能在复制实例后登录环境。

- 复制 Human Resources 数据库时，不复制 Microsoft PowerApps 环境中包含的元素（应用或数据）。 有关如何在 PowerApps 环境中复制元素的信息，请参阅[复制环境](https://docs.microsoft.com/power-platform/admin/copy-environment)。 您要覆盖的 PowerApps 环境必须是沙盒环境。 您必须是全局租户管理员才能将 PowerApps 生产环境更改为沙盒环境。 有关更改 PowerApps 环境的详细信息，请参阅[切换实例](https://docs.microsoft.com/dynamics365/admin/switch-instance)。

## <a name="effects-of-copying-a-human-resources-database"></a>复制 Human Resources 数据库的影响

复制 Human Resources 数据库时，会发生以下事件：

- 复制过程将擦除目标环境中的现有数据库。 复制过程完成后，您将无法恢复现有数据库。

- 在复制过程完成之前，目标环境将不可用。

- Microsoft Azure Blob 存储中的文档不会从一个环境复制到另一个环境。 因此，附加的所有文档和模板都不会被复制，并将保留在源环境中。

- 除管理员用户和其他内部服务用户帐户之外的所有用户将不可用。 因此，在允许其他用户返回到系统之前，管理员用户可以删除或打乱数据。

- 管理员用户必须进行必要的配置更改，例如将集成终结点重新连接到特定服务或 URL。

## <a name="copy-the-human-resources-database"></a>复制 Human Resources 数据库

要完成此任务，您首先要复制一个实例，然后登录到 Microsoft Power Platform 管理中心以复制 PowerApps 环境。

> [!WARNING]
> 复制实例时，目标实例中的数据库将被擦除。 在此过程中，目标实例不可用。

1. 登录到 LCS，然后选择包含要复制的实例的 LCS 项目。

2. 在您的 LCS 项目中，选择 **Human Resources 应用管理**磁贴。

3. 选择要复制的实例，然后选择**复制**。

4. 在**复制实例**任务窗格中，选择要覆盖的实例，然后选择**复制**。 等待**复制状态**字段的值更新为**已完成**。

   ![[选择要覆盖的实例](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. 选择 **Power Platform**，然后登录到 Microsoft Power Platform 管理中心。

   ![[选择 Power Platform](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. 选择要复制的 PowerApps 环境，然后选择**复制**。

7. 复制过程完成后，登录到目标实例，然后启用 Common Data Service 集成。 有关详细信息和说明，请参阅[配置 Common Data Service 集成](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration)。

## <a name="data-elements-and-statuses"></a>数据元素和状态

复制 Human Resources 实例时，不会复制以下数据元素：

- **LogisticsElectronicAddress** 表中的电子邮件地址

- **BatchJobHistory**、**BatchHistory** 和 **BatchConstraintHistory** 表中的批处理作业历史记录

- **SysEmailSMTPPassword** 表中的简单邮件传输协议 (SMTP) 密码

- **SysEmailParameters** 表中的 SMTP 中继服务器

- **PrintMgmtSettings** 和 **PrintMgmtDocInstance** 表中的“打印管理”设置

- **SysServerConfig**、**SysServerSessions**、**SysCorpNetPrinters**、**SysClientSessions**、**BatchServerConfig** 和 **BatchServerGroup** 表中的特定于环境的记录

- DocuValue 表中的文档附件。 这些附件包括在源环境中被覆盖的所有 Microsoft Office 模板

- **PersonnelIntegrationConfiguration** 表中的连接字符串

这些元素中的某些元素是特定于环境的，因此不会被复制。 示例包括 **BatchServerConfig** 和 **SysCorpNetPrinters** 记录。 其他元素由于支持票证的数量，不会被复制。 例如，可能由于在用户接受测试（沙盒）环境中仍启用 SMTP 而发送了重复的电子邮件，可能由于仍启用了批处理作业而发送了无效的集成消息，或者可能在管理员可以执行刷新后清理操作之前启用了用户。

此外，复制实例时，以下状态也会更改：

- 除管理员以外的所有用户均设置为**已禁用**。

- 除某些系统作业外，所有批处理作业均设置为**预扣**。

## <a name="environment-admin"></a>环境管理员

目标沙盒环境中的所有用户（包括管理员）都将被替换为源环境的用户。 复制实例之前，请确保您是目标环境中的管理员。 如果不是，则复制完成后您将无法登录到目标沙盒环境。

目标沙盒环境中的所有非管理员用户均会被禁用，以防止在沙盒环境中进行不必要的登录。 管理员可以根据需要重新启用用户。

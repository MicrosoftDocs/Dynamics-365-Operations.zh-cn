---
title: 删除实例
description: 本文介绍如何删除 Microsoft Dynamics 365 Human Resources 的 Test Drive 或生产环境。
author: twheeloc
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0ce676c93e133cc04ad9c49417ed2ca0d6791e93
ms.sourcegitcommit: 1401d66b6b64c590ca1f8f339d622e922920cf15
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/20/2022
ms.locfileid: "9178463"
---
# <a name="remove-an-instance"></a>删除实例

_**适用于：** 独立基础结构中的 Human Resources_ 

> [!NOTE]
> 从 2022 年 7 月开始，无法在独立的 Human Resources 基础结构中预配新的 Human Resources 环境，因此无法在其中创建新的 Microsoft Dynamics Lifecycle Services (LCS) 项目。 客户可以在财务和运营基础结构上部署 Human Resources 环境。 有关详细信息，请参阅[在财务和运营基础结构中预配 Human Resources](/hr-admin-setup-provision-fo.md)。

> [!IMPORTANT]
> 财务和运营应用基础结构支持删除环境。 有关如何删除环境的更多信息，请参阅[删除环境](../fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure.md#delete-an-environment)。

本文介绍如何删除 Microsoft Dynamics 365 Human Resources 的测试驱动器或生产环境。

## <a name="remove-a-test-drive-environment"></a>删除测试驱动器环境

Human Resources 测试驱动器设置了 60 天的到期策略。 不过，测试驱动器环境的所有者可以选择通过完成以下步骤来提前结束试用。 

1. 导航到 [Power Apps 管理中心](https://admin.businessplatform.microsoft.com/)。
2. 选择 **环境**。
3. 选择测试驱动器环境，其命名模式类似于这样：TestDrive - alias@domain
4. 选择 **删除** 并确认决定。 

现有的测试驱动器环境将被删除。 在删除后，您可以注册新的测试驱动器环境。 

## <a name="remove-a-production-environment"></a>删除生产环境

本文假设您已通过云解决方案提供商 (CSP) 或企业体系结构 (EA) 协议购买了 Human Resources。 

因为单个 Human Resources 环境包含在单个 Power Apps 环境中，因此在删除环境时需要考虑两个选项： 
- **删除整个 Power Apps 环境。** 当创建 Power Apps 环境的目的是为了预配 Human Resources，且您刚刚开始实施或您没有任何既定的集成时，这是首选选项。  
- **仅删除 Human Resources。** 当存在建立的 Power Apps 环境，并使用 Microsoft Power Apps 和 Power Automate 中使用的数据填充了此环境时，适用此选项。


> [!Important]
> 在删除 Power Apps 环境之前，请确保其未在 Human Resources 范围外用于数据集成。 另请注意，不能删除默认的 Power Apps 环境。 

若要删除整个 Power Apps 环境，包括 Human Resources 以及关联的应用和流：

1. 导航到 [Power Apps 管理中心](https://admin.businessplatform.microsoft.com/)。
2. 选择 **环境**。
3. 选择要删除的环境。
4. 选择 **删除** 并确认决定。 
5. 等待直到删除完成。
6. 使用您用于订阅 Human Resources 的帐户登录到 [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS)。 
7. 选择包含环境的 Human Resources 项目。 
8. 在您的 LCS 项目中，选择 **Human Resources 应用管理** 磁贴。 
9. 选择要删除的实例。 
10. 选择 **删除实例** 并确认您的决定。  

若要从现有的 Power Apps 环境中删除 Human Resources 环境，请完成以下步骤。 请注意，在直接在 LCS 中支持此功能前，暂时需要 Human Resources DevOps 团队的支持及联系。

1. 联系支持以发起删除请求。
2. 支持团队将向 Human Resources DevOps 团队发起删除请求。 
3. 在收到环境已删除的消息后继续操作。
4. 使用您用于订阅 Human Resources 的帐户登录到 LCS。 
5. 选择包含环境的 Human Resources 项目。 
6. 在您的 LCS 项目中，选择 **Human Resources 应用管理** 磁贴。 
7. 选择要删除的实例，其应标记有部署状态 **已删除**。
8. 选择 **删除实例** 并确认您的决定。 

## <a name="recover-a-soft-deleted-environment"></a>恢复软删除的环境

如果删除与 Human Resources 环境连接的 Power Apps 环境，LCS 中 Human Resources 环境的状态将为 **已软删除**。 在这种情况下，用户无法连接到 Human Resources。

要恢复环境：

1. 按照[恢复 Power Apps 环境](/power-platform/admin/recover-environment)中的说明操作。

2. 与客户支持联系恢复 Human Resources 环境。 有关详细信息，请参阅[获取支持](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md)。

> [!Warning]
> Power Apps 环境在删除后仅保存 7 天。 您必须在 7 天之内恢复环境。


[!INCLUDE[footer-include](../includes/footer-banner.md)]

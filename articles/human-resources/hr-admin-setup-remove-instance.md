---
title: 删除实例
description: ''
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
ms.openlocfilehash: 5c5f875ad9361c31af4fbe863488b881cdd97a6e
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008175"
---
# <a name="remove-an-instance"></a>删除实例

此文将指导您如何删除 Microsoft Dynamics 365 Human Resources 的测试驱动器或生产环境。

## <a name="remove-a-test-drive-environment"></a>删除测试驱动器环境

Human Resources 测试驱动器设置了 60 天的到期策略。 不过，测试驱动器环境的所有者可以选择通过完成以下步骤来提前结束试用。 

1. 导航到 [Power Apps 管理中心](https://admin.businessplatform.microsoft.com/)。
2. 选择**环境**。
3. 选择测试驱动器环境，其命名模式类似于这样：TestDrive - alias@domain
4. 选择**删除**并确认决定。 

现有的测试驱动器环境将被删除。 在删除后，您可以注册新的测试驱动器环境。 

## <a name="remove-a-production-environment"></a>删除生产环境

本文假设您已通过云解决方案提供商 (CSP) 或企业体系结构 (EA) 协议购买了 Human Resources。 

因为单个 Human Resources 环境包含在单个 Power Apps 环境中，有两个选项可以考虑。 第一个选项是要删除整个 Power Apps 环境；第二个选项是仅删除 Human Resources。 当您创建 Power Apps 环境的目的明确是为了预配 Human Resources，且您刚刚开始实施或您没有任何既定的集成，这时首选第一个选项。 当您已建立了 Power Apps 环境并使用 Power Apps 和 Power Automate 中利用的富数据填充时，适用第二个选项。

> [!Important]
> 在删除 Power Apps 环境之前，请确保其未在 Human Resources 范围外用于富数据集成。 另请注意，不能删除默认的 Power Apps 环境。 

若要删除整个 Power Apps 环境，包括 Human Resources 以及关联的应用和流：

1. 导航到 [Power Apps 管理中心](https://admin.businessplatform.microsoft.com/)。
2. 选择**环境**。
3. 选择要删除的环境。
4. 选择**删除**并确认决定。 
5. 等待直到删除完成。
6. 使用您用于订阅 Human Resources 的帐户登录到 [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS)。 
7. 选择包含环境的 Human Resources 项目。 
8. 在您的 LCS 项目中，选择 **Human Resources 应用管理**磁贴。 
9. 选择要删除的实例。 
10. 选择**删除实例**并确认您的决定。  

若要从现有的 Power Apps 环境中删除 Human Resources 环境，请完成以下步骤。 请注意，在直接在 LCS 中支持此功能前，暂时需要 Human Resources DevOps 团队的支持及联系。

1. 联系支持以发起删除请求。
2. 支持团队将向 Human Resources DevOps 团队发起删除请求。 
3. 在收到环境已删除的消息后继续操作。
4.  使用您用于订阅 Human Resources 的帐户登录到 LCS。 
5. 选择包含环境的 Human Resources 项目。 
6. 在您的 LCS 项目中，选择 **Human Resources 应用管理**磁贴。 
7. 选择要删除的实例，其应标记有部署状态**失败**。
8. 选择**删除实例**并确认您的决定。 

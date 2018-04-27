---
title: "删除 Talent 环境"
description: "此主题将指导您如何删除 Microsoft Dynamics 365 for Talent 的测试驱动器或生产环境。"
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d1870c84d4d5e7402bae44d192ce7587c2f67fe7
ms.openlocfilehash: 0e7748b079b1cd5c069917d46e05cd281ea6aa01
ms.contentlocale: zh-cn
ms.lasthandoff: 04/05/2018

---
# <a name="remove-a-talent-environment"></a>删除 Talent 环境

此主题将指导您如何删除 Microsoft Dynamics 365 for Talent 的测试驱动器或生产环境。

## <a name="removing-a-test-drive-environment"></a>删除测试驱动器环境

Talent 测试驱动器设置了 60 天的到期策略。 不过，测试驱动器环境的所有者可以选择通过完成以下步骤来提前结束试用。 

1. 导航到 [PowerApps 管理中心](https://admin.businessplatform.microsoft.com/)。
2. 选择**环境**。
3. 选择测试驱动器环境，其命名模式类似于这样：TestDrive - alias@domain
4. 选择**删除**并确认决定。 

现有的测试驱动器环境将被删除。 在删除后，您可以注册新的测试驱动器环境。 

## <a name="removing-a-production-environment"></a>删除生产环境

此主题假设您已通过云解决方案提供商 (CSP) 或企业体系结构 (EA) 协议购买了 Talent。 

因为单个 Talent 环境“包含”在单个 PowerApps 环境中，有两个选项可以考虑。 第一个选项是要删除整个 PowerApps 环境；第二个选项是仅删除 Talent。 当您创建 PowerApps 环境的目的明确是为了配置 Talent，且您刚刚开始实施或您没有任何既定的集成，这时首选第一个选项。 当您已建立了 PowerApps 环境并使用 PowerApps 和 Flows 中利用的富数据填充时，适用第二个选项。

> [!Important]
> 在删除 PowerApps 环境之前，请确保其未在 Talent 范围外用于富数据集成。 另请注意，不能删除默认的 PowerApps 环境。 

若要删除整个 PowerApps 环境，包括 Talent 以及关联的应用和流：

1. 导航到 [PowerApps 管理中心](https://admin.businessplatform.microsoft.com/)。
2. 选择**环境**。
3. 选择要删除的环境。
4. 选择**删除**并确认决定。 
5. 等待直到删除完成。
6. 使用您用于订阅 Talent 的帐户登录到 [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS)。 
7. 选择包含环境的 Talent 项目。 
8. 在您的 LCS 项目中，选择 **Talent 应用管理**磁贴。 
9. 选择要删除的实例。 
10. 选择**删除实例**并确认您的决定。  

若要从现有的 PowerApps 环境中删除 Talent 环境，请完成以下步骤。 请注意，在直接在 LCS 中支持此功能前，暂时需要 Talent DevOps 团队的支持及联系。

1. 联系支持以发起删除请求。
2. 支持团队将向 Talent DevOps 团队发起删除请求。 
3. 在收到环境已删除的消息后继续操作。
4.  使用您用于订阅 Talent 的帐户登录到 LCS。 
5. 选择包含环境的 Talent 项目。 
6. 在您的 LCS 项目中，选择 **Talent 应用管理**磁贴。 
7. 选择要删除的实例，其应标记有部署状态**失败**。
8. 选择**删除实例**并确认您的决定。 



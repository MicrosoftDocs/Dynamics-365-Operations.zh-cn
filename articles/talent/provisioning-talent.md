---
title: "配置 Talent"
description: "此主题将指导您如何为 Microsoft Dynamics 365 for Talent 配置新环境。"
author: rschloma
manager: AnnBe
ms.date: 09/27/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: 6fb41a8c1ff4ce95bab5b169256955f244e66071
ms.contentlocale: zh-cn
ms.lasthandoff: 11/01/2018

---
# <a name="provision-talent"></a>配置 Talent

[!include [banner](includes/banner.md)]

此主题将指导您如何为 Microsoft Dynamics 365 for Talent 配置新生产环境。 此主题假设您已通过云解决方案提供商 (CSP) 或企业体系结构 (EA) 协议购买了 Talent。 如果您有已包括 Talent 服务计划的现有 Microsoft Dynamics 365 许可证，但无法完成本主题中的步骤，请联系支持人员。

若要开始，全局管理员应登录到 [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) 并创建新的 Talent 项目。 除非许可问题妨碍了您配置 Talent，否则不需要从支持人员或 Dynamics Service 工程 (DSE) 代表处获得帮助。

## <a name="create-an-lcs-project"></a>创建 LCS 项目
若要使用 LCS 来管理您的 Talent 环境，您必须先创建 LCS 项目。

1. 使用您用于订阅 Talent 的帐户登录到 [LCS](https://lcs.dynamics.com/Logon/Index)。
2. 选择加号 (**+**) 创建项目。
3. 选择 **Microsoft Dynamics 365 for Talent** 作为产品名称和产品版本。
4. 选择 **Dynamics 365 for Talent** 方法。
5. 选择**创建**。

有关如何开始 Talent 的信息，请参阅在新项目中创建的 **Talent** 方法。 在您完成创建项目后，请完成以下过程来设置您的 Talent 环境。

## <a name="provision-a-talent-project"></a>配置 Talent 项目
在创建 LCS 项目之后，您可以将 Talent 配置到环境中。

1. 在您的 LCS 项目中，选择 **Talent 应用管理**磁贴。
2. Talent 始终配置到 Microsoft PowerApps 环境，以支持 PowerApps 集成和可扩展性。 在继续之前，请阅读本主题的“选择 PowerApps 环境”部分。 如果您没有 PowerApps 环境，在 LCS 中选择“管理环境”或导航到 PowerApps 管理员中心。 然后按照步骤[创建 PowerApps 环境](https://docs.microsoft.com/en-us/powerapps/administrator/create-environment)。

    > [!NOTE]
    > 若要查看现有的环境或创建新环境，必须为配置 Talent 的租户管理员分配 PowerApps P2 许可证。 如果您的组织没有 PowerApps P2 许可证，则可以从 CSP 或从 [PowerApps 定价页面](https://powerapps.microsoft.com/en-us/pricing/)获取一个。

4. 选择**添加**，然后选择要为 Talent 配置的环境。
5. 如果希望环境中包含 Talent 测试驱动器体验中使用的相同演示数据集，请选择“包括演示数据”选项。  这对长期演示或培训环境有益，但切勿用于生产环境。  请注意，初始部署后就必须选择此选项，因为以后不能更新现有部署。
6. 选择**是**同意条款并开始部署。

    您的新环境将出现在左侧导航窗格的环境列表中。 不过，在部署状态更新为**已部署**前，您无法开始使用此环境。 此过程通常需要几分钟。 如果配置过程失败，您必须与支持人员联系。

7. 选择**登录 Talent** 来使用您的新环境。

> [!NOTE]
> 如果您尚未验证最终要求，您可以在项目中部署 Talent 的测试实例。 您可以随后使用此实例来测试您的解决方案，直到验证完成。 如果您使用新环境进行测试，那么您必须重复此过程来创建一个生产环境。

> [!NOTE]
> 由于 Talent 预订中仅允许两个 LCS 环境，所以也可以考虑利用免费的 60 天的 [Talent 试用环境](https://dynamics.microsoft.com/en-us/talent/overview/)。 尽管试用环境归其请求用户所有，仍然可以通过 Core HR 的系统管理体验邀请其他用户。 试用环境中包含可用于以安全方式探索该程序的虚拟数据。 不应将其用作生产环境。 请注意，如果试用环境在 60 天后到期，其中的所有数据都将被删除且不可恢复。 现有环境过期后，可以注册新试用环境。

## <a name="select-a-powerapps-environment"></a>选择 PowerApps 环境

通过 Talent 与 PowerApps 环境之间的集成，可使用 PowerApps 工具集成和扩展 Talent 数据的使用。 了解 PowerApps 环境的用途不仅有助于您构建扩展 Talent 的应用，还可以帮助您在配置 Talent 时选择正确的环境。 有关 PowerApps 环境的信息，包括环境范围、环境访问和创建与选择环境，请参阅[介绍 PowerApps 环境](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/)。 

在确定部署 Talent 的目标 PowerApps 环境时请使用以下指南： 
1. 在 LCS 中，选择“管理环境”，或直接导航到“PowerApps 管理员中心”，您可以在那里查看现有的环境和创建新的环境。
2. 单个 Talent 环境映射到单个 PowerApps 环境。
3. PowerApps 环境“包含”Talent 应用程序，以及相应的 PowerApps、流和 CDS 应用程序。 如果 PowerApps 环境被删除，其中的应用也会被删除。 在设置人才环境时，可以设置“试用”或“生产”。 根据环境使用方式选择环境类型。 
4. 应该考虑数据集成和测试策略，例如：沙盒、UAT、生产。 因此，建议您考虑对您的部署的各种影响，因为以后不容易更改将哪个 Talent 环境映射到 PowerApps 环境。
5. 以下 PowerApps 环境不能用于 Talent，将从 LCS 内的选择列表中筛除：
 
   **默认 PowerApps 环境**虽然每个租户均自动配置为默认的 PowerApps 环境，但我们不建议在 Talent 中使用它们，因为所有租户用户均有权访问 PowerApps 环境，有可能会在使用 PowerApps 或流集成进行测试和探索时意外损坏生产数据。
   
   <strong>测试驱动器环境</strong>具有类似“TestDrive – alias@domain”这样的名称的环境创建后有 60 天的到期期间，此时间过后，会导致您的环境自动删除。
   
   **不支持的地区**Talent 当前仅在以下地区受支持：美国、欧洲或澳大利亚。
  
6. 一旦您确定了要使用的正确环境，则没有要采取的特定行动。 继续配置流程。 
 
## <a name="grant-access-to-the-environment"></a>授予对环境的访问
默认情况下，创建环境的全局管理员可以访问环境。 但是，必须为更多应用程序用户明确授予访问权限。 要授予访问权限，请在 Core HR 环境中[添加用户](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users)并[为其分配相应角色](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles)。 部署了 Talent 的全局管理员还必须启动 Attract 和 Onboard 应用程序以完成初始化和允许其他租户用户访问。  在此之前，其他用户不能访问 Attract 和 Onboard 应用程序，并且将发生访问冲突错误。



---
title: "配置 Microsoft Dynamics 365 for Talent"
description: "此主题将指导您如何为 Microsoft Dynamics 365 for Talent 配置新环境。"
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
ms.sourcegitcommit: 8b59ea6a2ac8c1c4e5df6e251fa3390639ff3f30
ms.openlocfilehash: e6266ef5890b5caaf33db76eeccfc8a7a6888a11
ms.contentlocale: zh-cn
ms.lasthandoff: 03/01/2018

---
# <a name="provision-microsoft-dynamics-365-for-talent"></a>配置 Microsoft Dynamics 365 for Talent

[!include[banner](includes/banner.md)]

[!include[banner](includes/banner.md)]

此主题将指导您如何为 Microsoft Dynamics 365 for Talent 配置新生产环境。 此主题假设您已通过云解决方案提供商 (CSP) 或企业体系结构 (EA) 协议购买了 Talent。 如果您有已包括 Talent 服务计划的现有 Microsoft Dynamics 365 许可证，但无法完成本主题中的步骤，请联系支持人员。

若要开始，全局管理员应登录到 [Microsoft Dynamics Lifecycle Services](http://lcs.dynamics.com) (LCS) 并创建新的 Talent 项目。 除非许可问题妨碍了您配置 Talent，否则不需要从支持人员或 Dynamics Service 工程 (DSE) 代表处获得帮助。

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
2. Talent 始终配置到 Microsoft PowerApps 环境，以支持 PowerApps 集成和可扩展性。 如果您还没有 PowerApps 环境，在继续前请先执行本主题“创建新的 PowerApps 环境（如果需要）”部分中的步骤。

    > [!NOTE]
    > 若要查看现有的环境或创建新环境，必须为配置 Talent 的租户管理员分配 PowerApps P2 许可证。 如果您的组织没有 PowerApps P2 许可证，则可以从 CSP 或从 [PowerApps 定价页面](https://powerapps.microsoft.com/en-us/pricing/)获取一个。

3. 选择**添加**，然后选择要为 Talent 配置的环境。
4. 选择**是**同意条款并开始部署。

    您的新环境将出现在左侧导航窗格的环境列表中。 不过，在部署状态更新为**已部署**前，您无法开始使用此环境。 此过程通常需要几分钟。 如果配置过程失败，您必须与支持人员联系。

6. 选择**登录 Talent** 来使用您的新环境。

> [!NOTE]
> 如果您尚未验证最终要求，您可以在项目中部署 Talent 的测试实例。 您可以随后使用此实例来测试您的解决方案，直到验证完成。 如果您使用新环境进行测试，那么您必须重复此过程来创建一个生产环境。

> [!NOTE]
> 通过 LCS 设置的 Talent 环境不包含为人力资源 (HR) 任务配置的演示数据或特定于 Talent 的演示数据。 如果需要包含演示数据的环境，建议您注册 60 天的免费 [Talent 试用环境](https://dynamics.microsoft.com/en-us/talent/overview/)。 尽管试用环境归其请求用户所有，仍然可以通过 Core HR 的系统管理体验邀请其他用户。 试用环境中包含可用于以安全方式探索该程序的虚拟数据。 不应将其用作生产环境。 请注意，如果试用环境在 60 天后到期，其中的所有数据都将被删除且不可恢复。 现有环境过期后，可以注册新试用环境。

## <a name="create-a-new-powerapps-environment-if-required"></a>创建新的 PowerApps 环境（如果需要）
通过 Talent 与 PowerApps 环境之间的集成，可使用 PowerApps 工具集成和扩展 Talent 数据的使用。 了解 PowerApps 环境的用途有助于构建应用以满足对扩展 Talent 的需要。 有关 PowerApps 环境的信息，包括环境范围、环境访问和创建与选择环境，请参阅[介绍 PowerApps 环境](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/)。 由于默认 PowerApps 环境中将自动设置每个租户，所以该环境可能不是最适合用于您的 Talent 部署的环境。 此步骤中应考虑数据集成和测试策略，所以建议您注意可能对您的部署的影响，因为某些决定以后不容易更改。 

尽管默认 PowerApps 环境中将自动设置每个租户，但是该环境可能不是最适合您的 Talent 部署的环境。 此步骤应考虑数据集成和测试策略。 因此，建议您考虑对您的部署的各种影响，因为以后不容易更改 PowerApps 环境。

1. 在 LCS 中选择**管理环境**。 您会被带到 [PowerApps 管理员中心](https://preview.admin.powerapps.com/environments)，从中您可以查看现有的环境并创建新环境。
2. 选择**新建环境**。
3. 为环境输入唯一名称，然后选择要部署的位置。

    > [!NOTE]
    > Talent 不是在所有地区都可用。 因此，在您为环境选择位置之前，请务必检查可用性。

4. 在询问您是否要创建数据库时，请选择**创建数据库**来创建必须承载Talent 数据的一部分的 Common Data Service (CDS) 数据库。 通过创建数据库，您还可以将 PowerApps 应用程序与 Talent 集成。
5. 您将被询问要用于数据库的访问级别。 我们建议您选择**限制访问**，因为此选项通过使用 PowerApps 应用程序阻止 Talent 用户直接访问敏感数据。
6. 创建的 CDS 数据库中包含演示数据，而演示数据会将非活动员工和虚构地址及其他信息添加到您的生产环境中。 若要删除演示数据，在您完成创建 CDS 数据库后执行以下步骤：

    > [!IMPORTANT]
    > 如果您以前已创建了 CDS 数据库并在其中输入了您公司的任何生产数据，以下步骤将删除所选数据库中的**所有**数据，甚至您公司的生产数据。

    1. 登录 [PowerApps](https://preview.web.powerapps.com/home)。
    2. 在右上方的下拉列表中，选择您在步骤 2 中创建的环境。
    3. 在左侧的导航窗格中，展开 **Common Data Service**，然后选择**实体**。
    4. 在页面的右侧，请选择椭圆形 (**…**) 按钮，然后选择**清除所有数据**。
    5. 选择**删除数据**以确认您要删除该数据。 此操作默认情况下将删除 CDS 中包括的所有演示数据。 它还会删除在所选数据库中输入的任何其他数据。

您现在可以使用您的新环境了。

## <a name="grant-access-to-the-environment"></a>授予对环境的访问
默认情况下，创建环境的全局管理员可以访问环境。 但是，必须为更多应用程序用户明确授予访问权限。 要授予访问权限，请在 Core HR 环境中[添加用户](../dev-itpro/sysadmin/tasks/create-new-users.md)并[为其分配相应角色](../dev-itpro/sysadmin/tasks/assign-users-security-roles.md)。 还必须将这些用户添加到 PowerApps 环境，以便他们可以访问 Attract 和 Onboard 应用程序。 下面概述此过程。 如果需要帮助才能完成这些步骤，请参阅博客文章[介绍 PowerApps 管理中心](https://powerapps.microsoft.com/en-us/blog/introducing-admin-center-for-powerapps/)。

应由部署 Talent 环境的全局管理员完成此过程。

1. 打开 [PowerApps 管理中心](https://preview.admin.powerapps.com/environments)。
2. 选择相应环境。
3. 在**安全性**选项卡中，将所需用户添加到**环境制造者**角色。

请注意，将用户手动添加到 PowerApps 环境这一最后步骤是暂时的。 在 Core HR 中添加用户时，将最终自动完成此步骤。


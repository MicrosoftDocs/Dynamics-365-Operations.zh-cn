---
title: 预配 Human Resources
description: 此主题介绍为 Microsoft Dynamics 365 Human Resources 配置新生产环境的流程。
author: twheeloc
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 766e807ee9061f52b692cf3436ba393b334e67c4
ms.sourcegitcommit: 7a2001e4d01b252f5231d94b50945fd31562b2bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/15/2021
ms.locfileid: "7488075"
---
# <a name="provision-human-resources"></a>预配 Human Resources

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

此主题介绍为 Microsoft Dynamics 365 Human Resources 配置新生产环境的流程。 

## <a name="prerequisites"></a>先决条件

必须先满足以下先决条件，才能预配新的生产环境：

- 您已通过云解决方案提供商 (CSP) 或企业体系结构 (EA) 协议购买了 Human Resources。 如果您有已包括 Human Resources 服务计划的现有 Microsoft Dynamics 365 许可证，但无法完成本主题中的步骤，请联系支持人员。

- 全局管理员已登录到 [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) 并创建新的 Human Resources 项目。 

## <a name="provision-a-human-resources-trial-environment"></a>预配 Human Resources 试用环境

在预配您的第一个沙盒或生产环境之前，可能需要预配 [Human Resources 试用环境](https://go.microsoft.com/fwlink/p/?LinkId=2115962)来验证 Human Resources 功能。 试用环境中包含可用于以安全方式探索该程序的虚拟数据。 尽管试用环境归其请求用户所有，仍然可以通过 Human Resources 的系统管理体验邀请其他用户。 

试用环境为尚未访问 Human Resources 环境的个人提供评估人力资源功能的能力。 如果您在预配试用环境并且经过身份验证的用户已经有权访问一个或多个现有 Human Resources 环境，该用户将被重定向到现有环境或环境列表。

不应将试用环境用作生产环境。 它们仅限于 60 天的试用期。 当试用期到期时，该环境以及其中的所有数据都将删除且不可恢复。 该环境无法转换为沙盒或生产环境。 现有环境过期后，可以注册新试用环境。

在创建 Human Resources 试用环境时，还将在租户上创建 Power Apps 试用环境并链接到 Human Resources 环境。 Power Apps 环境的名称为“TestDrive”，其试用期与 Human Resources 环境相同。

> [!NOTE]
> 如果经过身份验证的用户无权创建 Power Apps 试用环境，则设置 Human Resources 试用环境将失败 。 该用户必须属于可在 Power Platform 管理中心中创建试用环境的用户组。 有关详细信息，请参阅[控制谁可以在 Power Platform 管理中心中创建和管理环境](//power-platform/admin/control-environment-creation)。

## <a name="plan-human-resources-environments"></a>计划 Human Resources 环境

在创建第一个 Human Resources 环境之前，您应该仔细计划项目的环境需求。 Human Resources 的基本订阅包括两个环境：生产环境和沙盒环境。 根据项目的复杂性，您可能需要购买其他沙盒环境来支持项目活动。 

其他环境的注意事项：

- **数据迁移**：您可能需要考虑额外增加一个环境来用于数据迁移活动，以允许将沙盒环境用于整个项目的测试。 多增加一个环境，当测试和配置活动在不同环境中同时进行时，可以让数据迁移活动继续进行。
- **集成**：您可能需要考虑额外增加一个环境来用于配置和测试集成。 这可能包括本地集成，如 Ceridian Dayforce LinkedIn Talent Hub 集成，或自定义集成，如工资单、申请人跟踪系统或福利系统和提供商。
- **培训**：您可能需要一个单独的环境，并在环境中配置一组培训数据来对员工进行新系统使用方面的培训。 
- **多阶段项目**：您可能需要一个额外的环境来支持项目初始投入使用后计划的项目阶段内的配置、数据迁移、测试或其他活动。

 > [!IMPORTANT]
 > 在您考虑您的环境时，我们建议您执行以下操作：
 > - 在整个项目中使用生产环境作为 GOLD 配置环境。 这很重要，因为您不能将沙盒环境复制到生产环境。 因此，投入使用时，您的 GOLD 环境就是您的生产环境，您将在此环境中完成直接转换活动。</br></br>
 > - 在投入使用之前使用沙盒或其他环境执行模拟转换。 您可以通过将具有 GOLD 配置的生产环境刷新到沙盒环境来实现此目的。</br></br>
 > - 保留一份详细的直接转换清单，其中包括在执行转换期间将最终数据迁移到生产环境所需的每个数据包。</br></br>
 > - 在整个项目中使用沙盒环境作为 TEST 环境。 如果您需要其他环境，您的组织可以购买，但需要支付额外的费用。</br></br>

## <a name="create-an-lcs-project"></a>创建 LCS 项目

若要使用 LCS 来管理您的 Human Resources 环境，您必须先创建 LCS 项目。

1. 使用您用于订阅 Human Resources 的帐户登录到 [LCS](https://lcs.dynamics.com/Logon/Index)。

   > [!NOTE]
   > 要确保成功预配，必须将用于预配 Human Resources 环境的帐户分配给与 Human Resources 环境关联的 Power Apps 环境中的 **系统管理员** 或 **系统定制员** 角色。 有关在 Power Platform 中为用户分配安全角色的详细信息，请参阅[为资源配置用户安全性](/power-platform/admin/database-security)。

2. 选择加号 (**+**) 创建项目。

3. 选择 **Microsoft Dynamics 365 Human Resources** 作为产品名称和产品版本。

4. 选择 **Dynamics 365 Human Resources** 方法。

5. 选择 **创建**。

有关如何开始 Human Resources 的信息，请参阅在新项目中创建的 **Human Resources** 方法。 在您完成创建项目后，请完成以下过程来设置您的 Human Resources 环境。

## <a name="provision-a-human-resources-project"></a>预配 Human Resources 项目

在创建 LCS 项目之后，您可以将 Human Resources 预配到环境中。

1. 在您的 LCS 项目中，选择 **Human Resources 应用管理** 磁贴。

2. 指示此环境是 Human Resources 的沙盒实例还是生产实例。 沙盒实例中可能提供提前预览功能以便提前反馈和测试。
   
    > [!NOTE]
    > Human Resources 实例类型一旦设置就无法更改。 在继续之前，请验证是否选择了正确的实例类型。</br></br>
    > Human Resources 实例类型独立于 Microsoft Power Apps 环境的实例类型，后者是您在 Power Apps 管理中心中设置的。
    
3. 如果希望环境中包含 Human Resources 试用环境中使用的相同演示数据集，请选择 **包括演示数据** 选项。 演示数据对长期演示或培训环境有益，但切勿用于生产环境。 您必须在初始部署之后立即选择此选项。 不能在以后更新现有部署。

4. Human Resources 始终预配到 Microsoft Power Apps 环境，以支持 Power Apps 集成和可扩展性。 在继续之前，请阅读本文的“选择 Power Apps 环境”部分。 如果您没有 Power Apps 环境，在 LCS 中选择“管理环境”或导航到 Power Apps 管理员中心。 然后按照步骤[创建 Power Apps 环境](/powerapps/administrator/create-environment)。

5. 选择要预配 Human Resources 的环境。

6. 选择 **是** 同意条款并开始部署。

   您的新环境将出现在左侧导航窗格的环境列表中。 不过，在部署状态更新为 **已部署** 前，您无法开始使用此环境。 此过程通常需要几分钟。 如果配置过程失败，您必须与支持人员联系。

7. 选择 **登录 Human Resources** 来使用您的新环境。

    > [!NOTE]
    > 如果您尚未验证最终要求，您可以在项目中部署 Human Resources 的测试实例。 您可以随后使用此实例来测试您的解决方案，直到验证完成。 如果您使用新环境进行测试，那么您必须重复此过程来创建一个生产环境。

## <a name="select-a-power-apps-environment"></a>选择 Power Apps 环境

您可以使用 Power Apps 工具集成和扩展 Human Resources 数据的使用。 有关 Power Apps 环境的信息，包括环境范围、环境访问和创建与选择环境，请参阅[介绍 Power Apps 环境](https://powerapps.microsoft.com/blog/powerapps-environments/)。 

在确定部署 Human Resources 的目标 Power Apps 环境时请使用以下指南： 

1. 在 LCS 中选择 **管理环境**。 您也可以直接转到 Power Apps 管理中心，从中您可以查看现有的环境并创建新环境。

2. 单个 Human Resources 环境映射到单个 Power Apps 环境。

3. Power Apps 环境包含 Human Resources，以及相应的 Power Apps、Power Automate 和 Dataverse 应用程序。 如果 Power Apps 环境被删除，其中的应用也会被删除。 在预配 Human Resources 环境时，可以预配 **试用** 或 **生产** 环境。 根据环境使用方式选择环境类型。 

4. 应该考虑数据集成和测试策略，如沙盒、UAT 或生产。 请认真考虑对您的部署的影响，因为更改将哪个 Human Resources 环境映射到 Power Apps 环境并非易事。

5. 不能将以下 Power Apps 环境用于 Human Resources。 它们是在 LCS 中从选择列表中筛选出的：
 
    - **默认 Power Apps 环境** - 虽然会自动为每个租户预配默认的 Power Apps 环境，但我们不建议将其用于 Human Resources。 所有租户用户都可以访问 Power Apps 环境，因此在通过 Power Apps 或 Power Automate 集成进行测试和探索时可能会无意间破坏生产数据。
   
    - **试用环境** - 这些环境在创建时具有到期日期。 到期后，您的环境及其中包含的任何 Human Resources 实例都将自动删除。
   
    - **不支持的地理区域** - 环境必须位于受支持的地理区域。 有关详细信息，请参阅[支持的地理区域](hr-admin-setup-provision.md#supported-geographies)。

6. 只有为环境选择了 **启用 Dynamics 365 应用** 选项，才能使用将 Human Resources 数据与 Power Apps 环境集成的双重写入功能。 有关双重写入的详细信息，请参阅[双重写入主页](../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)。

    > [!NOTE]
    > 在创建 Power Apps 环境时，必须选择 **启用 Dynamics 365 应用** 选项。 如果在预配时未选择此选项，您将无法使用双重写入在 Dynamics 365 Human Resources 和 Power Apps 环境之间集成数据，或在环境中安装 Dynamics 365 应用，如 Dynamics 365 Sales 和 Field Service。 此选项不可逆。 有关详细信息，请参阅 Power Platform 文档站点上的[创建新环境时的一些重要注意事项](//power-platform/admin/create-environment#some-important-considerations-when-creating-a-new-environment)。

7. 确定了要使用的正确环境之后，可以继续进行配置流程。 

### <a name="supported-geographies"></a>支持的地理区域

Human Resources 目前支持以下地理区域：

- 美国
- 欧洲
- 英国
- 澳大利亚
- 加拿大
- 亚洲 

创建 Human Resources 环境时，您将选择要与 Human Resources 环境关联的 Power Apps 环境。 然后，该 Human Resources 环境将在与所选 Power Apps 环境相同的 Azure 地理区域预配。 您可以在创建将与 Human Resources 环境关联的 Power Apps 环境时选择地理区域，从而选择 Human Resources 环境和数据库的实际位置。

您可以选择在其中预配了环境的 Azure *地理区域*，但不能选择特定的 Azure *区域*。 自动化将确定创建环境的地理区域内的特定区域，以优化负载均衡和性能。 您可以在有关 [Azure 地理区域](https://azure.microsoft.com/global-infrastructure/geographies)的文档中找到有关 Azure 地理区域和区域的信息。

Human Resources 环境的数据始终会包含在创建该环境的 Azure 地理区域中。 但是，不会总包含在同一个 Azure 区域。 出于灾难恢复目的，数据将被复制到地理区域内的主要 Azure 区域和二级故障转移区域。

 > [!NOTE]
 > 不支持将 Human Resources 环境从一个 Azure 区域迁移到另一个区域。

## <a name="grant-access-to-the-environment"></a>授予对环境的访问

默认情况下，创建环境的全局管理员可以访问环境。 您必须为更多应用程序用户明确授予访问权限。 您必须在 Human Resources 环境中添加用户并为其分配相应角色。 有关详细信息，请参阅[创建新用户](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users)和[向安全角色分配用户](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles)。 


[!INCLUDE[footer-include](../includes/footer-banner.md)]

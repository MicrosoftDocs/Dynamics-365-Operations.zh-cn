---
title: 设置 Human Resources
description: 本文将指导您如何为 Microsoft Dynamics 365 Human Resources 预配新生产环境。
author: andreabichsel
manager: AnnBe
ms.date: 04/23/2020
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
ms.openlocfilehash: 88a0be50a9b861190e7ce9b3f56bb4e583b791d1
ms.sourcegitcommit: 33685a5cc37081a189279e917def7f122d3beaef
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/24/2020
ms.locfileid: "3285481"
---
# <a name="provision-human-resources"></a>设置 Human Resources

本文将指导您如何为 Microsoft Dynamics 365 Human Resources 预配新生产环境。 本文假设您已通过云解决方案提供商 (CSP) 或企业体系结构 (EA) 协议购买了 Human Resources。 如果您有已包括 Human Resources 服务计划的现有 Microsoft Dynamics 365 许可证，但无法完成本文中的步骤，请联系支持人员。

若要开始，全局管理员应登录到 [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) 并创建新的 Human Resources 项目。 除非许可问题妨碍了您预配 Human Resources，否则不需要从支持人员或 Dynamics Service 工程 (DSE) 代表处获得帮助。

## <a name="create-an-lcs-project"></a>创建 LCS 项目

若要使用 LCS 来管理您的 Human Resources 环境，您必须先创建 LCS 项目。

1. 使用您用于订阅 Human Resources 的帐户登录到 [LCS](https://lcs.dynamics.com/Logon/Index)。

2. 选择加号 (**+**) 创建项目。

3. 选择 **Microsoft Dynamics 365 Human Resources** 作为产品名称和产品版本。

4. 选择 **Dynamics 365 Human Resources** 方法。

5. 选择**创建**。

有关如何开始 Human Resources 的信息，请参阅在新项目中创建的 **Human Resources** 方法。 在您完成创建项目后，请完成以下过程来设置您的 Human Resources 环境。

## <a name="provision-a-human-resources-project"></a>预配 Human Resources 项目

在创建 LCS 项目之后，您可以将 Human Resources 预配到环境中。

1. 在您的 LCS 项目中，选择 **Human Resources 应用管理**磁贴。

2. 指示此环境是 Human Resources 的沙盒实例还是生产实例。 沙盒实例中可能提供提前预览功能以便提前反馈和测试。
   
    > [!NOTE]
    > Human Resources 实例类型一旦设置就无法更改。 在继续之前，请验证是否选择了正确的实例类型。</br></br>
    > Human Resources 实例类型独立于 Microsoft Power Apps 环境的实例类型，后者是您在 Power Apps 管理中心中设置的。
    
3. 如果希望环境中包含 Human Resources 测试驱动器体验中使用的相同演示数据集，请选择**包括演示数据**选项。 演示数据对长期演示或培训环境有益，但切勿用于生产环境。 您必须在初始部署之后立即选择此选项。 不能在以后更新现有部署。

4. Human Resources 始终预配到 Microsoft Power Apps 环境，以支持 Power Apps 集成和可扩展性。 在继续之前，请阅读本文的“选择 Power Apps 环境”部分。 如果您没有 Power Apps 环境，在 LCS 中选择“管理环境”或导航到 Power Apps 管理员中心。 然后按照步骤[创建 Power Apps 环境](https://docs.microsoft.com/powerapps/administrator/create-environment)。

5. 选择要预配 Human Resources 的环境。

6. 选择**是**同意条款并开始部署。

   您的新环境将出现在左侧导航窗格的环境列表中。 不过，在部署状态更新为**已部署**前，您无法开始使用此环境。 此过程通常需要几分钟。 如果配置过程失败，您必须与支持人员联系。

7. 选择**登录 Human Resources** 来使用您的新环境。

    > [!NOTE]
    > 如果您尚未验证最终要求，您可以在项目中部署 Human Resources 的测试实例。 您可以随后使用此实例来测试您的解决方案，直到验证完成。 如果您使用新环境进行测试，那么您必须重复此过程来创建一个生产环境。

    > 您可以考虑使用 60 天免费的 [Human Resources 试用环境](https://go.microsoft.com/fwlink/p/?LinkId=2115962)。 尽管试用环境归其请求用户所有，仍然可以通过 Human Resources 的系统管理体验邀请其他用户。 试用环境中包含可用于以安全方式探索该程序的虚拟数据。 不应将其用作生产环境。 请注意，如果试用环境在 60 天后到期，其中的所有数据都将被删除且不可恢复。 现有环境过期后，可以注册新试用环境。

## <a name="select-a-power-apps-environment"></a>选择 Power Apps 环境

您可以使用 Power Apps 工具集成和扩展 Human Resources 数据的使用。 有关 Power Apps 环境的信息，包括环境范围、环境访问和创建与选择环境，请参阅[介绍 Power Apps 环境](https://powerapps.microsoft.com/blog/powerapps-environments/)。 

在确定部署 Human Resources 的目标 Power Apps 环境时请使用以下指南： 

1. 在 LCS 中选择**管理环境**。 您也可以直接转到 Power Apps 管理中心，从中您可以查看现有的环境并创建新环境。

2. 单个 Human Resources 环境映射到单个 Power Apps 环境。

3. Power Apps 环境包含 Human Resources，以及相应的 Power Apps、Power Automate 和 Common Data Service 应用程序。 如果 Power Apps 环境被删除，其中的应用也会被删除。 在预配 Human Resources 环境时，可以预配**试用**或**生产**环境。 根据环境使用方式选择环境类型。 

4. 应该考虑数据集成和测试策略，如沙盒、UAT 或生产。 请认真考虑对您的部署的影响，因为更改将哪个 Human Resources 环境映射到 Power Apps 环境并非易事。

5. 您不能将以下 Power Apps 环境用于 Human Resources。 它们是在 LCS 中从选择列表中筛选出的：
 
    - **默认 Power Apps 环境** - 虽然会自动为每个租户预配默认的 Power Apps 环境，但我们不建议将其用于 Human Resources。 所有租户用户都可以访问 Power Apps 环境，因此在通过 Power Apps 或 Power Automate 集成进行测试和探索时可能会无意间破坏生产数据。
   
    - **试用环境** - 这些环境在创建时具有到期日期。 到期后，您的环境及其中包含的任何 Human Resources 实例都将自动删除。
   
    - **不受支持的地区** - 目前仅在以下地区支持 Human Resources：美国、欧洲、英国、澳大利亚、加拿大和亚洲。

    > [!NOTE]
    > Human Resources 环境在预配 Power Apps 环境的同一区域中预配。 不支持将 Human Resources 环境迁移到另一个区域。

6. 确定了要使用的正确环境之后，可以继续进行配置流程。 
 
## <a name="grant-access-to-the-environment"></a>授予对环境的访问

默认情况下，创建环境的全局管理员可以访问环境。 您必须为更多应用程序用户明确授予访问权限。 您必须在 Human Resources 环境中添加用户并为其分配相应角色。 部署了 Human Resources 的全局管理员还必须启动 Attract 和 Onboard 以完成初始化和允许其他租户用户访问。 在此之前，其他用户不能访问 Attract 和 Onboard，并且将发生访问冲突错误。 有关详细信息，请参阅[创建新用户](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users)和[向安全角色分配用户](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles)。 

---
title: 制造和仓库管理工作负荷的 Cloud Scale Unit 和 Edge Scale Unit
description: 本主题提供有关制造和仓库管理工作负荷的 Cloud Scale Unit 和 Edge Scale Unit 的信息。
author: cabeln
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: dbe5833d4c9d8038fcebf1d9d446af757c834e42a2f77f10c7eb7268e738ed28
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6780666"
---
# <a name="cloud-and-edge-scale-units-for-manufacturing-and-warehouse-management-workloads"></a>用于制造和仓库管理工作负载的云和边缘缩放单元

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> 根据管理服务使用的条款向您提供 Microsoft Dynamics 365 Supply Chain Management 的缩放单元功能。 有关详细信息，请参阅 [Microsoft Dynamics 法律信息](https://go.microsoft.com/fwlink/?LinkID=290927)。
>
> 当启用 Cloud Scale Unit 和 Edge Scale Unit 时，系统将要求您确认了解与 Cloud Scale Unit 和 Edge Scale Unit 的配置和处理相关的某些数据可能存储在位于美国的数据中心中。 若要了解有关 Cloud Scale Unit 和 Edge Scale Unit 的数据处理的详细信息，请参阅本主题后面的[缩放单元管理期间的数据处理](#data-processing-management)部分。

## <a name="core-value-proposition-for-scale-units"></a>缩放单元的核心价值主张

从事制造和分销业务的公司必须能够不中断且大规模地全天候运行关键业务流程。 通过 Cloud Scale Unit 和 Edge Scale Unit，公司能够不中断地运行重要的任务关键型制造和仓库流程，即使偶尔遇到网络连接或延迟问题也是如此。

通过 Cloud Scale Unit 和 Edge Scale Unit，可在不同的环境中分配车间和仓库执行工作负荷。 此功能可以帮助提高性能，防止服务中断并最大化运行时间。 通过 Supply Chain Management 订阅的以下加载项提供缩放单元：

- Dynamics 365 Supply Chain Management 的 Cloud Scale Unit 加载项（*2021 年 4 月推出*）
- Dynamics 365 Supply Chain Management 的 Edge Scale Unit 加载项（*即将推出*）

将通过增量增强不断发布工作负荷功能。

## <a name="scale-units-and-dedicated-workloads"></a>缩放单元和专用工作负荷

缩放单元通过添加专用的处理容量来扩展您的集中 Supply Chain Management 中心环境。 缩放单元可在 Cloud 中运行。 或者，它们可在您的本地机构的 Edge 上本地运行。

:::image type="content" source="./media/cloud_edge-HeroDiagram.png" alt-text="具有缩放单元的 Dynamics 365。":::

缩放单元为已分配的工作负荷提供弹性、可靠性和规模。 Edge Scale Unit 可以临时从云中心环境中断开连接，工作人员可以继续在 Edge 上的已分配工作负荷中工作。

*工作负荷* 是一组定义的业务功能，可以进行分解并委派给缩放单元。 尽管已发布仓库管理的工作负荷，但制造执行的工作负荷仍处于预览状态。

您可以使用[缩放单元管理器门户](https://sum.dynamics.com)为选定工作负荷配置中心环境和 Cloud Scale Unit。 您还可以针对每个缩放单元分配多个工作负荷。 有关当前版本中 Cloud Scale Unit 的先决条件和限制的信息，请参阅本主题后面的 [Cloud Scale Unit 的先决条件和限制](#cloud-scale-unit-prerequisites)部分。

### <a name="dedicated-warehouse-management-workload-capabilities-in-a-scale-unit"></a>缩放单元中的专用仓库管理工作负荷功能

仓库管理工作负荷是缩放单元的第一个分发的工作负荷，并且已正式发布。

对于仓库管理，缩放单元提供以下功能：

- 系统可以处理销售订单和需求补货的选定波次方法。
- 仓库工作人员可以使用仓库管理移动应用运行销售和需求补货仓库工作。
- 仓库工作人员可以使用仓库管理移动应用查询现有库存。
- 仓库工作人员可以使用仓库管理移动应用创建和运行库存移动。
- 仓库工作人员可以使用仓库管理移动应用登记采购订单并进行储存。

有关详细信息，请参阅 [Cloud Scale Unit 和 Edge Scale Unit 的仓库管理工作负荷](cloud-edge-workload-warehousing.md)。

### <a name="dedicated-manufacturing-execution-workload-capabilities-in-a-scale-unit"></a>缩放单元中的专用制造执行工作负荷功能

制造工作负荷的第一个版本当前处于预览状态，将提供以下功能：

- 机器操作员和车间主管可以访问操作生产计划。
- 机器操作员可以通过运行离散和流程制造作业来使计划保持最新状态。
- 车间主管可以调整操作计划。
- 工作人员可以访问在 Edge 中上下班打卡的考勤管理，以确保正确计算工作人员工资。

有关详细信息，请参阅 [Cloud Scale Unit 和 Edge Scale Unit 的制造执行工作负荷](cloud-edge-workload-manufacturing.md)。

## <a name="considerations-before-you-enable-the-distributed-hybrid-topology-for-supply-chain-management"></a>为 Supply Chain Management 启用分布式混合拓扑之前的注意事项

通过启用分布式混合拓扑，您可以转换 Supply Chain Management 云环境，使其充当一个中心。 您还可以在 Cloud 中或在 Edge 上关联配置为缩放单元的其他环境。

### <a name="prerequisites-and-limitations-for-cloud-scale-units"></a><a name="cloud-scale-unit-prerequisites"></a>Cloud Scale Unit 的先决条件和限制

在缩放单元的当前版本中，某些功能尚不可用，但随着时间的推移可能会添加到增量版本中。

#### <a name="you-must-be-a-licensed-customer-of-supply-chain-management"></a>您必须是 Supply Chain Management 的许可客户

若要加入到分布式拓扑，您必须具有 Supply Chain Management 的许可证。 您的现有云环境将成为混合拓扑中的中心。 您可以将沙盒环境和生产环境声明为中心环境，并且可以根据所获取的加载项添加缩放单元。

#### <a name="your-existing-project-must-be-administered-via-the-global-commercial-version-of-lcs"></a>您的现有项目必须通过 LCS 的全球商业版本进行管理

您的现有 Microsoft Dynamics Lifecyle Services (LCS) 项目必须满足以下版本要求：

- 该项目必须通过 [lcs.dynamics.com](https://lcs.dynamics.com) 上 LCS 的全球商业版本进行管理。
- LCS 的本地版本（例如 [eu.lcs.dynamics.com](https://eu.lcs.dynamics.com) 和 [fr.lcs.dynamics.com](https://fr.lcs.dynamics.com)）不受支持。
- LCS 的 Governmental Cloud 版本不受支持。
- LCS 的 Mooncake 版本不受支持。

#### <a name="your-current-production-environment-must-be-of-the-self-service-type-in-lcs"></a>您的当前生产环境必须是 LCS 中的自助服务类型

您的当前生产环境必须标记有 LCS 中的 **自助服务** 类型。 此类型指示已转换您的 LCS 项目的租户，因此它支持 Azure Service Fabric 托管模型。

> [!IMPORTANT]
> 作为服务架构 (IaaS) 运行的环境类型不受支持。 这些环境通常标记有 LCS 中的 **Microsoft 托管** 类型。 如果您拥有此类型的环境，请与您的 Microsoft 联系人合作以了解迁移到 **自助服务** 类型的时间线。

Microsoft 正在将 Supply Chain Management 的所有云环境从 IaaS 模型转换到在 Service Fabric 中托管的拓扑。 此迁移可以提供更好的可扩展性，并且有助于简化服务管理。 因此，可以更快实现部署和维护操作。 同样，服务组件将迁移到微服务的概念，服务托管模型将从虚拟机 (VM) 模型[转换](/virtualization/windowscontainers/about/containers-vs-vm)到轻型容器化体系结构。

最终，相同的基于 Service Fabric 的容器化服务基础架构将同时为服务的 Cloud 和 Edge 实例提供支持，而不管实例是 Cloud 中的中心，还是 Cloud 中或 Edge 上的缩放单元。

您必须先将项目租户转换到 Service Fabric 托管的模型，然后才能加入到支持缩放单元的混合拓扑。 此外，必须转换将充当中心的任何环境。

> [!TIP]
> 若要查询您的 LCS 项目租户的状态，请在 [LCS](https://lcs.dynamics.com/) 中查找环境的类型，或者与您的合作伙伴或 Microsoft 联系人联系。

#### <a name="local-business-data-on-premises-environments-arent-supported-as-hubs-for-scale-units"></a>不支持将本地业务数据（本地）环境用作缩放单元的中心

本地环境不能用作缩放单元的中心。 中心环境必须始终由云托管。

#### <a name="scale-unit-management-capabilities-are-limited"></a>缩放单元管理功能受限制

可以帮助移动工作负荷的管理功能受限制。 某些管理操作在自助服务方式中不受支持，您必须通过合作伙伴或 Microsoft 联系人请求支持。 示例包括缩放单元之间的某些工作负荷移动和灾难情况下的临时特别移动。

#### <a name="metrics-and-measurements-arent-yet-available"></a>指标和度量尚不可用

可帮助您为缩放单元选择最佳应用程序的指标和度量尚不可用。 与您的 Microsoft 联系人或实施合作伙伴合作，选择最有利的应用程序。

### <a name="data-processing-during-management-of-scale-units"></a><a name="data-processing-management"></a>缩放单元管理期间的数据处理

当您使 Dynamics 365 环境针对 Cloud Scale Unit 和 Edge Scale Unit 支持分布式混合拓扑时，某些管理服务将仅在美国托管，就像 LCS 一样。 此行为会影响[缩放单元管理器门户](https://sum.dynamics.com)使用的某些管理和配置信息的传输和存储。 下面举了一些示例加以说明：

- 您的租户名称和 ID
- 您的 LCS 项目 ID
- 用于登录的管理员和项目所有者电子邮件地址
- 中心的环境 ID 和缩放单元
- 工作负荷配置，包括法人和设施的名称和实际地址，以便您的拓扑可以显示在地理地图上
- 收集的指标（例如延迟和吞吐量），将显示在地图分析页面上，以帮助您选择最有用的缩放单元

根据 Microsoft 数据保留策略，将删除传输到美国数据中心并存储在其中的数据。 Microsoft 非常注重您的隐私。 若要了解详细信息，请阅读我们的[隐私声明](https://go.microsoft.com/fwlink/?LinkId=521839)。

## <a name="onboarding-in-two-stages"></a>加入分为两个阶段

加入到分布式混合拓扑的流程具有两个阶段。 在第一个阶段中，您必须验证自定义以确保它们可在具有缩放单元的分布式拓扑中工作。 沙盒和生产环境仅在第二阶段中移动。

### <a name="stage-1-evaluate-customizations-in-one-box-development-environments"></a>阶段 1：在单盒开发环境中评估自定义

在开始加入沙盒或生产环境之前，建议您在开发设置中探索缩放单元，例如单盒环境（也称为第 1 层环境），以便您可以验证流程、自定义和解决方案。 在此阶段中，数据和自定义将应用到单盒环境。 一个环境用作中心，另一个环境用作缩放单元。 此设置提供识别和修复问题的最佳方法。 最新的提前访问 (PEAP) 版本也可以用于完成此阶段。

对于阶段 1，应使用[单盒开发环境的缩放单元部署工具](https://github.com/microsoft/SCMScaleUnitDevTools)。 这些工具使您可以在一个或两个单独的单盒环境中配置中心和缩放单元。 这些工具作为二进制版本提供，并在 GitHub 上以源代码的形式提供。 研究项目 wiki，其中包括描述如何使用工具的[分步使用指南](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide)。

### <a name="stage-2-acquire-add-ins-and-deploy-in-your-sandbox-and-production-environments"></a>阶段 2：获取加载项，并在沙盒和生产环境中进行部署

若要将沙盒或生产环境之一加入到新拓扑，您必须获取一个或多个 Cloud Scale Unit（以及将来的 Edge Scale Unit）的加载项。 加载项将在 [LCS](https://lcs.dynamics.com/) 中授予相应的项目和环境插槽，以便可以部署缩放单元环境。

> [!NOTE]
> 缩放单元加载项不与有限数量的用户耦合，但可以根据管理员分配的角色供现有订阅中的任何用户使用。

在多个库存单位 (SKU) 和定价选项中提供缩放单元。 因此，您可以选择最能满足您计划的每月交易量和性能要求的选项。

入门级 SKU 称为 *基本*，性能更高的 SKU 称为 *标准*。 每个 SKU 都预先加载有特定数量的每月交易。 但是，您可以通过为每个 SKU 添加超额加载项来增加每月交易预算。

:::image type="content" source="media/SKUs-highlevel.png" alt-text="Cloud Scale Unit 的加载项。":::

> [!TIP]
> 若要确定最能满足您的需求的规模，请与您的合作伙伴和 Microsoft 合作，以了解所需的每月交易规模。

购买每个缩放单元加载项后，您不仅可以获取每月交易量，还有权使用 LCS 中特定数量的环境插槽。 对于每个 Cloud Scale Unit 加载项，您都有权使用一个新生产槽和一个新沙盒槽。 在加入流程期间，将添加具有这些插槽的新 LCS 项目。 插槽的使用权受到限制，因此必须将插槽用作具有云中心的缩放单元。

超额加载项不能赋予您使用新环境的权限。

如果要获取更多沙盒环境，您可以购买额外的常规沙盒槽。 然后，Microsoft 可以帮助您启用这些插槽作为混合拓扑的沙盒缩放单元。

## <a name="onboard-to-the-distributed-hybrid-topology-for-supply-chain-management"></a>加入到 Supply Chain Management 的分布式混合拓扑

### <a name="select-your-lcs-project-tenant-and-the-detailed-onboarding-process"></a>选择您的 LCS 项目租户和详细的加入流程

完成计划如何加入到 Supply Chain Management 的分布式混合拓扑后，您将使用[缩放单元管理器门户](https://aka.ms/SCMSUM)开始加入流程。 在门户中，选择 **Dynamics 365 租户** 选项卡。此选项卡显示您的帐户所属的租户列表，以及您在哪个租户中是 LCS 项目的所有者或环境管理员。

如果您要查找的租户不在列表中，请转到 [LCS](https://lcs.dynamics.com/v2)，并确保您是该租户的 LCS 项目的环境管理员或项目所有者。 仅授权选定租户中的 Azure Active Directory (Azure AD) 帐户完成注册体验。

> [!NOTE]
> 将更改应用到 LCS 后，租户列表最多可能需要 30 分钟才能反映更改。

对于每个租户，列表都会显示加入状态。

:::image type="content" source="media/cloud_edge-EnableHybrid1.png" alt-text="Dynamics 365 租户选项卡上的租户列表。":::

选择 **单击此处开始** 以请求加入 LCS 租户。 您必须接受这些条款。 您还必须提供公司电子邮件地址，Microsoft 可以通过该地址发送与加入流程相关的通信。

:::image type="content" source="media/cloud_edge-EnableHybrid2.png" alt-text="租户的注册提交。":::

Microsoft 将审查您的请求，并通过向您在注册窗体中提供的地址发送电子邮件来通知有关后续步骤的信息。 Microsoft 将与您紧密合作，为您的业务场景在混合拓扑中启用缩放单元。

完成加入后，您可以使用端口配置缩放单元和工作负荷。

### <a name="manage-cloud-scale-units-and-workloads-by-using-the-scale-unit-manager-portal"></a><a name="scale-unit-manager-portal"></a>使用缩放单元管理器门户管理 Cloud Scale Unit 和工作负荷

转到[缩放单元管理器门户](https://aka.ms/SCMSUM)，然后使用您的租户帐户登录。 在 **配置缩放单元** 页面上，如果尚未列出中心环境，则可以添加一个。 然后，可以选择要使用缩放单元和工作负荷配置的中心。

:::image type="content" source="media/cloud_edge-Manage.png" alt-text="缩放单元和工作负荷管理体验。":::

若要添加一个或多个在订阅中可用的缩放单元，请选择 **添加缩放单元**。

在 **已定义工作负荷** 选项卡上，使用 **创建工作负荷** 按钮将仓库管理工作负荷添加到您的缩放单元之一。 对于每个工作负荷，您必须指定工作负荷将负责的流程的上下文。 对于仓库管理工作负荷，上下文是特定站点和法人中的特定仓库。

:::image type="content" source="media/cloud_edge-DefineWorkload.png" alt-text="工作负荷创建。":::

> [!TIP]
> 随着时间的推移，将向缩放单元管理器体验添加增量增强，以帮助简化生命周期管理操作。 当前版本的特定功能记录在加入手册中，该手册适用于正在加入到 Supply Chain Management 的分布式混合拓扑。 <!-- KFM: Add a link to the handbook when it is published -->

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

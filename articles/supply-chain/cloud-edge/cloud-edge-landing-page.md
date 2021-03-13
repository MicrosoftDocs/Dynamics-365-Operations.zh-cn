---
title: 制造和仓库管理工作负荷的 Cloud Scale Unit 和 Edge Scale Unit
description: 本主题提供有关制造和仓库管理工作负荷的 Cloud Scale Unit 和 Edge Scale Unit 的信息。
author: cabeln
manager: ''
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 28301cdfb86d00ea6f04e996fe7fb1485e83b2d4
ms.sourcegitcommit: 289e9183d908825f4c8dcf85d9affd4119238d0c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104956"
---
# <a name="cloud-and-edge-scale-units-for-manufacturing-and-warehouse-management-workloads"></a>制造和仓库管理工作负荷的 Cloud Scale Unit 和 Edge Scale Unit

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

通过 Cloud Scale Unit 和 Edge Scale Unit，可在不同的环境中分配车间和仓库执行工作负荷。 此功能可以帮助提高性能，防止服务中断并最大化运行时间。 它通过以下加载项提供：

- Dynamics 365 Supply Chain Management 的 Cloud Scale Unit 加载项
- Dynamics 365 Supply Chain Management 的 Edge Scale Unit 加载项

从事制造和分销业务的公司必须能够不中断且大规模地全天候运行关键业务流程。 通过 Cloud Scale Unit 和 Edge Scale Unit，公司能够不中断地运行重要的任务关键型制造和仓库流程，即使偶尔遇到网络连接或延迟问题也是如此。

## <a name="public-preview-information"></a>公开预览版信息

预览版提供一个环境用作 Dynamics 365 Supply Chain Management 环境的基于云的中心，还提供一个环境用作 Cloud Scale Unit。

<!-- You will also be able to use Local Business Data (LBD) to configure an on-premises environment as an edge scale unit for the hub you received as part of the preview program.-->

### <a name="preview-availability"></a>预览版可用性

Cloud Scale Unit 和 Edge Scale Unit 的预览版在 2020 年 10 月提供给 Supply Chain Management 的现有客户。

若要访问在 [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/v2) 环境中部署的 10 月预览版本 10.0.15/平台更新 39，您必须成为 Supply Chain Management 的预览版提前访问计划（称为 PEAP）的一部分。 如果您已经是更广泛的 [Dynamics Insider Program](https://experience.dynamics.com/insider) 的成员，则可以加入 PEAP。 只需选择名为“Finance & Operations：预览版提前访问计划 (PEAP)”的特定计划。

> [!IMPORTANT]
> Supply Chain Management 的缩放单元功能仅在您同意 [Finance and Operations 的 Cloud + Edge 预览版条款](https://Aka.ms/SCMCnETerms)时才可用。

### <a name="data-processing-for-the-preview"></a>预览版的数据处理

在公开预览版期间，某些管理服务将仅在美国托管。 但是，在该功能公开发布后，这些管理服务将在 Supply Chain Management 支持的所有地区提供。 这会影响缩放单元管理器使用的管理信息的传输和存储，包括：

- 您的租户名称和 ID
- 您的 LCS 项目 ID
- 用于登录的管理员电子邮件
- 中心的环境 ID 和缩放单元
- 工作负荷配置
- 收集的指标（例如延迟和吞吐量），显示在地图分析页面上

关闭预览环境后，将删除传输到美国数据中心和存储在其中的数据。

### <a name="sign-up-for-the-preview"></a>注册预览

若要注册 Supply Chain Management 的 Cloud 和 Edge 预览版，您的组织必须已经有一个实际的 Supply Chain Management 云环境。

缩放单元功能当前在公开预览版中。 在注册时，您必须在特定租户上使用用户帐户。 对于该租户中的活动 Dynamics 365 LCS 项目，您还必须是 LCS 中的项目所有者或环境管理员。

在注册预览版时，您将选择一个租户并执行注册步骤。 一旦 Microsoft 可以分配预览版容量，我们将向您发送一封电子邮件，其中包含相应 LCS 项目的两个环境（中心和缩放单元）的预配详细信息和促销（促销）代码。 然后，您能够将两个环境部署为第 2 层沙盒环境。 这些环境将在促销代码创建之日起的 60 天内有效。 在完成下一段描述的步骤之前，您不应使用这两个环境。

在与 Microsoft 确认已使用促销代码部署两个环境后，其中一个环境将配置为用作中心，另一个环境将配置为用作缩放单元。 然后，您可以使用[缩放单元管理器门户](https://aka.ms/SCMSUM)配置缩放单元并部署选定的仓库管理和制造工作负荷。

预览环境将在 60 天后自动删除。 但是，如果它们看起来没有在使用，则可能会更快删除。 在删除预览环境后，您可以注册并排队等待新的预览版部署。

若要注册预览版，请转到[缩放单元管理器门户](https://aka.ms/SCMSUM)。

### <a name="limitations-that-apply-during-the-preview-period"></a>预览版期间适用的限制

> [!IMPORTANT]
> 对于此功能的预览版计划的初始阶段，Microsoft 仅支持具有 Cloud Scale Unit 的中心，而不支持具有 Edge Scale Unit 的中心。 Edge Scale Unit 在本地安装，并预计在计划的下一阶段可用。

由于 Cloud Scale Unit 和 Edge Scale Unit 是预览功能，因此与它们相关的服务目前仅在有限的国家和地区可用。 通过启用 Cloud Scale Unit 和 Edge Scale Unit，您确认了解与 Cloud Scale Unit 和 Edge Scale Unit 的配置和处理相关的某些数据可能存储在位于美国的数据中心中。 通过启用 Cloud Scale Unit 和 Edge Scale Unit，您还同意 [Finance and Operations 的 Cloud + Edge 预览版条款](https://Aka.ms/SCMCnETerms)。 若要了解有关 Cloud Scale Unit 和 Edge Scale Unit 的详细信息，请参阅[文档](https://aka.ms/scmcne)。

Microsoft 非常注重您的隐私。 若要了解详细信息，请阅读我们的[隐私声明](https://aka.ms/privacy)。

> [!IMPORTANT]
> 当在缩放单元上使用工作负荷时，公开预览版中不完全支持某些业务功能。 有关功能工作负荷的详细信息，请参阅本主题后面的部分。

## <a name="scale-units-and-dedicated-workloads"></a>缩放单元和专用工作负荷

:::image type="content" source="./media/cloud_edge-HeroDiagram.png" alt-text="具有缩放单元的 Dynamics 365":::

缩放单元通过添加专用的处理容量来扩展您的集中 Supply Chain Management 中心环境。 缩放单元可在 Cloud 中运行。 或者，它们可在您的本地机构的 Edge 上运行。 缩放单元可以从中心环境临时断开连接。 在它们连接后，缩放单元将收到运行已分配工作负荷的专用处理所需的所有信息。

:::image type="content" source="media/cloud_edge-previewoptions.png" alt-text="公开预览版中的缩放单元选项":::

对于公开预览版，您可以使用缩放单元管理器门户在 Cloud Scale Unit 上配置具有选定工作负荷的中心环境。 有权访问本地业务数据 (LBD) 本地环境的预览版参与者还可以将 LBD 环境配置为 Edge Scale Unit。

工作负荷是一组定义的业务功能，可以进行分解并委派给缩放单元。 当前，预览版具有两种类型的工作负荷：

- 制造执行
- 仓库管理

您可以为每个缩放单元分配其中一种工作负荷。 

### <a name="dedicated-manufacturing-execution-workload-capabilities-in-a-scale-unit"></a>缩放单元中的专用制造执行工作负荷功能

对于制造执行，Cloud Scale Unit 和 Edge Scale Unit 提供以下功能，即使 Edge 单元未连接到 Cloud：

- 机器操作员和车间主管可以访问操作生产计划。
- 机器操作员可以通过运行离散和流程制造作业来使计划保持最新状态。
- 车间主管可以调整操作计划。
- 工作人员可以访问在 Edge 中上下班打卡的考勤管理，以确保正确计算工作人员工资。

有关详细信息，请参阅[制造缩放单元工作负荷详细信息](cloud-edge-workload-manufacturing.md)。

### <a name="dedicated-warehouse-management-workload-capabilities-in-a-scale-unit"></a>缩放单元中的专用仓库管理工作负荷功能

对于仓库管理，Cloud Scale Unit 和 Edge Scale Unit 提供以下功能，即使 Edge 单元未连接到 Cloud：

- 对销售订单和需求补货启用选定波次方法的处理。
- 仓库工作人员可以使用仓库应用运行销售和需求补货仓库工作。
- 仓库工作人员可以使用仓库应用查询现有库存。
- 仓库工作人员可以使用仓库应用创建和运行库存变动。
- 仓库工作人员可以使用仓库应用登记采购订单并进行储存。

有关详细信息，请参阅[仓库缩放单元工作负荷详细信息](cloud-edge-workload-warehousing.md)。

## <a name="onboard-scale-units-for-your-supply-chain-management-environment"></a>Supply Chain Management 环境的 Onboard Scale Unit

### <a name="deploy-the-preview-for-cloud-and-edge-scale-units"></a>部署 Cloud Scale Unit 和 Edge Scale Unit 的预览版

下图显示了 Cloud Scale Unit 的公开预览版的注册和预配流。

:::image type="content" source="media/cloud_edge-previewsignup.png" alt-text="预览版注册步骤":::

### <a name="select-your-lcs-project-tenant-and-the-detailed-preview-process"></a>选择您的 LCS 项目租户和详细的预览版流程

在公开预览版中，[缩放单元管理器门户](https://aka.ms/SCMSUM)显示您的帐户所属的租户列表，以及您在哪个租户中是 LCS 项目的所有者或环境管理员。

如果您要查找的租户不在此列表中，请转到 [LCS](https://lcs.dynamics.com/v2)，并确保您是该租户的 LCS 项目的环境管理员或项目所有者。 请注意，仅授权选定租户中的 Azure Active Directory (Azure AD) 帐户完成注册体验。

> [!NOTE]
> 将更改应用到 LCS 后，租户列表最多可能需要 30 分钟才能反映更改。

对于每个租户，列表都会显示注册状态。

:::image type="content" source="media/cloud_edge-Signup1.png" alt-text="租户的注册选项":::

选择 **单击此处注册** 链接注册您的 LCS 租户以参与预览版。 您必须接受这些条款。 您还必须提供公司电子邮件地址，Microsoft 可以通过该地址发送与预览版注册流程相关的通信。

:::image type="content" source="media/cloud_edge-Signup2.png" alt-text="租户的注册提交":::

Microsoft 将审查您的请求，并通过向您在注册表单上提供的地址发送电子邮件来通知有关后续步骤的信息。

在获得预览版计划的访问权限后，您将收到 LCS 项目的两个促销代码。 现在，您可以使用这些促销代码在 LCS 中部署两个环境。 这些环境必须使用 PEAP 版本 10.0.15 或更高版本。 应用完促销代码后，通知 Microsoft（按照指示），以便我们可以为预览功能启用环境。 完成此配置步骤后，Microsoft 会通知您。

现在，您可以开始在预览环境中配置缩放单元和工作负荷。

> [!IMPORTANT]
> 配置 Cloud Scale Unit 时，您可以[在缩放单元管理器门户中执行所有必需步骤](#scale-unit-manager-portal)。
<!-- 
> If want to use edge scale units with your preview deployment, you must do all scale unit configuration in the user interface on the hub as described in [Configure the hub environment for use with edge scale units](cloud-edge-edge-scale-units-lbd.md#configure-the-hub-environment). You can't use Scale Unit Manager portal if you include an edge scale unit. -->

### <a name="manage-cloud-scale-units-and-workloads-by-using-the-scale-unit-manager-portal"></a><a name="scale-unit-manager-portal"></a>使用缩放单元管理器门户管理 Cloud Scale Unit 和工作负荷

转到[缩放单元管理器门户](https://aka.ms/SCMSUM)，然后使用您的租户帐户登录。 在 **配置缩放单元** 页面上，如果尚未列出中心环境，则可以添加一个。 然后，可以选择要使用缩放单元和工作负荷配置的中心。

:::image type="content" source="media/cloud_edge-Manage.png" alt-text="缩放单元和工作负荷管理体验":::

若要添加一个或多个在拓扑中可用的缩放单元，请选择 **添加缩放单元**。 在预览版中，您应该看到从作为预览版计划一部分收到的一个促销代码中部署的 Cloud Scale Unit。

<!--  [!IMPORTANT]
> In the public preview, the Scale Unit Manager portal shows the cloud scale unit that you received as part of the preview program. Any edge scale unit that you created based on an LBD configuration can't be managed in the Scale Unit Manager portal yet. For configuration details, see [Deploy custom edge scale units on custom hardware using LBD](cloud-edge-edge-scale-units-lbd.md) -->

在 **已定义工作负荷** 选项卡上，使用 **创建工作负荷** 按钮将仓库管理或制造执行工作负荷添加到您的缩放单元之一。 对于每个工作负荷，您必须指定工作负荷将负责的流程的上下文。 对于仓库管理工作负荷，上下文是特定站点和法人中的特定仓库。 对于制造执行工作负荷，上下文是法人中的特定站点。

:::image type="content" source="media/cloud_edge-DefineWorkload.png" alt-text="工作负荷创建":::

> [!IMPORTANT]
> 预览版中的缩放单元管理器门户不支持在分配后从缩放单元中删除工作负荷或从中心取消分配缩放单元。 如果必须删除分配，请与您的预览版计划管理的联系人联系。

<!-- ### Create an edge scale unit using your custom on-premises hardware appliance

In the public preview, you can create on-premises edge scale units on your custom hardware using the LBD environments. For details, see [Deploy custom edge scale units on custom hardware using LBD](cloud-edge-edge-scale-units-lbd.md). -->

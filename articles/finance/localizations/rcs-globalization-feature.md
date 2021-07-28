---
title: Regulatory Configuration Services (RCS) - 全球化功能
description: 此主题介绍如何使用 Microsoft Regulatory Configuration Services (RCS) 和全局知识库创建和使用全球化功能。
author: JaneA07
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, RCSWorkspace, e-Invoicing service
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: 7faa9a3cf6a29d8ed126cfcb0e2902b2016d03ff
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/06/2021
ms.locfileid: "6358138"
---
# <a name="regulatory-configuration-services-rcs---globalization-features"></a>Regulatory Configuration Services (RCS) - 全球化功能

[!include [banner](../includes/banner.md)]

您可以使用 Microsoft Regulatory Configuration Services (RCS) 创建可以在全球化服务（如电子开票服务）中使用的全球化功能。 RCS 使您可以执行以下任务：

- 定义相关的功能组件。
- 通过功能状态管理功能生命周期。
- 使功能可用于定义的环境。
- 与其他组织共享功能。

以下过程说明 RCS 中的用户如何添加全球化功能和相关组件、更新功能的状态，以及提供功能以可以在全球化服务中使用它。

在完成这些过程之前，您必须完成与以下任务相关的步骤：

- 访问 RCS 实例。
- 创建和激活配置提供程序。 有关详细信息，请参阅[创建配置提供程序并将其标记为有效](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md)。

在您的 Finance and Operations 应用实例中，按照以下步骤操作。

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 如果没有为公司预配 RCS 环境，请选择 **Regulatory services – 配置**，然后按照说明预配一个。

> [!NOTE]
> 如果已经为公司预配了 RCS 环境，请通过选择登录选项使用页面 URL 访问该环境。

## <a name="turn-on-the-globalization-features"></a>开启全球化功能

1. 在您的 RCS 实例中，选择 **功能管理** 磁贴。
2. 在 **功能管理** 工作区，在列表中选择 **全球化功能**，然后选择 **立即启用**。

    ![“功能管理”中的“全球化功能”。](./media/RCS_GlobalF_1%20Feature%20mgmt.JPG)

## <a name="globalization-features"></a>全球化功能

要使用全球化功能，必须首先从全局知识库导入它并为此功能创建一个您自己的版本。 有两种添加全球化功能的方法：

- 添加基于已发布或共享的现有功能的派生功能。
- 添加您从头开始创建的新功能。

## <a name="access-globalization-features"></a>访问全球化功能

1. 如本主题前面所述，确保在“功能管理”中启用了 **全球化功能** 功能。
2. 打开新的 **全球化功能** 工作区，然后在 **功能** 下，选择 **电子开票** 磁贴。

    ![全局功能工作区。](./media/RCS_GlobalF_2%20Feature%20wrkspace.JPG)

    **电子开票功能** 页面将打开。

    ![电子开票功能页面。](./media/RCS_GlobalF_3%20Feature%20form.JPG)

## <a name="add-a-derived-globalization-feature"></a>添加派生的全球化功能

您可以通过从已发布或共享的现有功能派生全球化功能来添加新的全球化功能。

1. 选择 **导入** 打开 **从全局知识库导入功能** 页面。

    ![“从全局存储库导入功能”页面。](./media/RCS_GlobalF_4%20Feature%20import%20form%20GR.JPG)

2. 选择 **同步** 获取最新功能。

    同步的列表包含由于 Microsoft 已发布或由于另一个配置提供程序已与您共享而可用的功能。

    ![同步的功能列表。](./media/RCS_GlobalF_5%20Feature%20GR%20sync.JPG)

3. 在此列表中，选择要导入的功能，然后选择 **导入**。 成功导入所选功能后，您会收到一条消息。

    ![导入成功消息。](./media/RCS_GlobalF_6%20Feature%20GR%20import%20success.JPG)

4. 选择 **添加**，然后在下拉对话框中选择 **基于现有版本** 选项。
5. 为功能输入名称和描述。
6. 在可用功能列表中，选择功能的基本版本，然后选择 **创建功能**。

    ![添加派生功能。](./media/RCS_GlobalF_7%20Feature%20create%20derived.JPG)

    您添加的功能将创建，状态为 **草稿**。

    ![具有“草稿”状态的派生功能。](./media/RCS_GlobalF_8%20Feature%20draft%20create.JPG)

7. 查看功能组件确定是否需要更新：

    - 如果需要自定义电子报告 (ER) 格式及其与功能版本的格式映射的绑定，请查看配置。
    - 如果需要针对功能版本自定义 **操作** 选项卡、**适用性规则** 选项卡或 **变量** 选项卡，请查看设置。

8. 在 **版本** 选项卡上，选择 **生效开始** 日期，如果 **描述** 字段为空，请输入描述。
9. 选择 **更改状态** 完成功能。 完整的功能可以为特定环境提供，以便可以在全球化服务中使用它们，也可以将其发布到全局知识库。

> [!NOTE]
> **功能版本状态** 值为 **已发布** 的功能可以与外部组织共享。

## <a name="add-a-new-globalization-feature"></a>添加新的全球化功能

您可以通过从头开始创建来添加新的全球化功能。

1. 在 **从全局知识库导入功能** 页面上，选择 **添加**，然后在下拉对话框中选择 **新功能** 选项。
2. 为功能输入名称和描述。
3. 选择 **创建功能**。

    ![添加新功能。](./media/RCS_GlobalF_9%20Feature%20create%20new.JPG)

4. 在 **版本** 选项卡上，选择 **生效开始** 日期，然后选择 **更改状态** 完成功能。 完整的功能可以为特定环境提供，以便可以在全球化服务中使用它们，也可以将其发布到全局知识库。

> [!NOTE]
> **功能版本状态** 值为 **已发布** 的功能可以与外部组织共享。

## <a name="feature-component-overview"></a>功能组件概览

全球化功能包含多个组件：

- **版本** – 此组件支持功能生命周期管理，并允许用户管理功能的不同版本的状态。
- **配置** – 此组件使用户可以管理、查看和编辑相关的电子报告格式和格式映射。
- **设置** – 此组件使全球化服务（如电子开票服务）的用户可以管理相关功能版本的设置。 因此，它支持通信和响应规则的灵活构造。
- **环境** – 此组件使全球化服务（如电子开票服务）的用户可以管理使用功能版本设置的环境，并可以向将有权访问该环境的用户授予授权。
- **组织** – 此组件使用户可以与外部组织共享功能。

## <a name="configuring-feature-components"></a>配置功能组件

### <a name="version-and-status"></a>版本和状态

版本用于管理全球化功能生命周期。

状态可以在 **版本** 选项卡上的 **状态** 字段中更改。以下状态可用：

- **草稿** – 功能仅在此状态下可以编辑。
- **完成** – 功能及所有相关组件已结束（完成），无法进行编辑。
- **已发布** – 功能及所有相关组件已发布到全局存储库。
- **已共享** – 功能及所有相关组件已与外部组织共享。
- **已启用** – 功能及所有相关组件已启用，可以在全球化服务（如电子开票服务）中使用。

> [!NOTE]
> 功能必须在其中某些状态中顺序移动。 因此，可能并非每个状态在每个生命周期阶段都可用。

### <a name="configurations"></a>配置

以下操作可用于配置：

- **查看** – 查看不需要任何更新的基础功能配置。
- **编辑** – 创建所选配置的草稿版本，以便您可以在格式设计器中编辑格式或格式映射。
- **删除** – 从功能中删除所选配置。
- **重定基本版本** – 重新设定功能的基本版本。 有关详细信息，请参阅本主题后面的[重新设定派生的全球化功能的基本版本](#rebase)一节。

### <a name="setups"></a>设置

以下操作可用于功能设置：

- **添加** – 创建新的功能设置。 此功能设置可以从现有功能设置派生，也可以从头创建。
- **删除** – 删除所选的功能设置。
- **查看** – 查看不需要任何更改的基础功能设置。
- **编辑** – 创建、删除或修改功能设置的三个主要组件的属性：

    - 操作及其参数
    - 适用性规则
    - 变量

![功能版本设置页面。](./media/RCS_GlobalF_10%20Feature%20set%20up.JPG)

### <a name="environments"></a>环境

以下操作可用于环境：

- **启用** – 为所选的功能版本，选择已发布的环境，并选择它应该可用的 **生效开始** 日期。 有关详细信息，请参阅本主题后面的[为启用配置环境](#configureenvironment)一节。
- **取消** – 删除用于功能设置的环境。

### <a name="organizations"></a>组织

请按照以下步骤与外部组织共享全球化功能。

1. 在 **电子开票功能** 页面，选择功能和要共享的功能版本。
2. 在 **组织** 选项卡上，选择 **共享**，然后在下拉对话框中输入组织的域名。
3. 选择 **共享**。

    ![与组织共享功能。](./media/RCS_GlobalF_20%20Feature%20orgn_share%20with.JPG)

功能将与所选组织共享，并在全局知识库中提供给该组织。 从那里，功能可以导入到组织的 RCS 或 Dynamics 365 Finance 实例以使它可以使用。

## <a name="rebase-derived-globalization-features"></a><a name="rebase"></a>重新设定派生的全球化功能的基本版本

您可以将派生的全球化功能重新设定为新的或更新的基本功能版本。 这样，基本版本中发生的更改可以自动更新。 更新的基本功能版本由原始配置提供程序创建，然后发布或共享。

![更新的基本功能版本。](./media/RCS_GlobalF_12%20Feature%20new%20version.JPG)

例如，如果要重新设定所创建功能的派生版本的基本版本，请首先通过从全局知识库导入该功能的最新版本来获取最新版本。

1. 在 **电子开票功能** 页面，选择 **导入**。
2. 选择 **同步** 获取最新功能。
3. 在功能列表中，选择要导入的功能，然后选择 **导入**。

    ![导入功能的最新版本。](./media/RCS_GlobalF_13%20Feature%20new%20version%20import.JPG)

4. 在功能列表中，选择要重定基本版本的功能。
5. 在 **版本** 选项卡上，选择 **新建** 创建草稿版本。

    ![新的草稿版本已创建。](./media/RCS_GlobalF_14%20Feature%20new%20base%20version.JPG)

6. 选择 **重定基本版本**。
7. 在 **重定基本版本** 对话框中，选择要重定的最新的功能版本。

    ![“重定基本版本”对话框。](./media/RCS_GlobalF_15%20Feature%20rebase%20version.JPG)

8. 选择 **确定**。
9. 查看功能组件，并进行所需的更改。
10. 选择 **更改状态** 完成已重定基本版本的功能。 重定基本版本完成后，您可以执行其他操作。 例如，您可以发布功能并在全球化服务中提供它供其他用户使用。

    ![功能状态更新为“已完成”。](./media/RCS_GlobalF_16%20Feature%20rebase%20version%20complete.JPG)

## <a name="configure-environments-for-globalization-features"></a><a name="configureenvironment"></a>配置全球化功能的环境

全球化服务的用户可以通过管理环境来设置全球化功能，并向将有权访问环境的其他用户授予授权。

1. 在 **全球化功能** 工作区，在 **环境** 下，选择 **电子开票** 磁贴。

    ![全球化功能工作区。](./media/RCS_GlobalF_17%20Feature%20environment.JPG)

2. 选择 **密钥保管库参数**，然后选择 **新建** 创建一个 Azure Key Vault 密钥。
3. 为密钥保管库输入名称和描述，然后在 **密钥保管库 URI** 字段中，输入用于标识 Azure 中的密钥保管库资源的 URL。
4. 在 **证书** 快速选项卡上，选择 **添加** 以添加证书，并为每个证书输入名称和描述。

    ![证书已添加。](./media/RCS_GlobalF_18%20Feature%20envn%20key%20vault%20parameter.JPG)

5. 选择 **新建** 创建新环境。
6. 输入名称、描述和存储所需的共享访问签名令牌密钥。
7. 在 **用户** 快速选项卡上，选择 **新** 添加将有权访问此环境的用户。
8. 输入用户的用户 ID 和电子邮件地址。
9. 重复执行步骤 7 和 8 添加更多用户。
10. 选择 **发布** 发布环境。

    ![已发布的环境。](./media/RCS_GlobalF_19%20Feature%20envn%20publishing.JPG)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: 配置 Invoice capture 解决方案
description: 本文介绍如何配置 Invoice capture 解决方案。
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: e297dafc930368f14f2e68213ce4153ba792ef4d
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691131"
---
# <a name="configure-the-invoice-capture-solution"></a>配置 Invoice capture 解决方案

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

安装 Invoice capture 解决方案后，您必须配置环境。 此过程包括以下基本步骤。

1. **必需：** 从 Microsoft Dynamics 365 Finance 同步法人。 此步骤用于在 Microsoft Power Platform 中设置组织结构。
2. **必需：** 为发票图像导入配置渠道。 此解决方案支持以下渠道：

    - Office 365 Outlook（默认）
    - Outlook.com
    - OneDrive
    - SharePoint

3. **可选：** 为光学字符识别 (OCR) 服务定义其他配置组。
4. **可选：** 为法人、供应商帐户、项目和采购类型定义映射规则。

本文重点介绍此过程的两个必需步骤。 有关配置组的更多信息，请参阅 [Invoice capture 解决方案配置组](invoice-capture-config-group.md)。 有关映射规则的更多信息，请参阅 [Invoice capture 解决方案映射规则](invoice-capture-mapping-rules.md)。

## <a name="manage-legal-entities"></a>管理法人

Finance 将法人定义为通过向法律机关登记而确定的组织。 业务活动在不同的法人中执行和记录。 在 Microsoft Power Platform 中，业务单位、安全角色和用户以符合基于角色的安全模型的方式链接在一起。

业务单位与安全角色一起用于控制数据访问。 用户只能看到他们完成工作所需的信息。 Invoice capture 解决方案提供了一个配置空间，您可以在其中从 Finance 中的现有法人加载基本信息，并可以管理手动创建的实体。 法人在供应商发票和安全控制中使用。

法人已创建并在列表视图中显示时，将自动创建具有相同名称的默认业务单位。 团队将被授予 **AP 职员** 安全角色。 导入法人时，会导入 Finance 中的基本主数据。 不存在的项目将由法人识别，并将它们添加到 Invoice capture 解决方案中。 默认配置组将分配给新法人。

### <a name="sync-legal-entities"></a>同步法人

您无法直接创建法人。 但是，可以从 Finance 同步法人。 要同步法人，请按照以下步骤操作。

1. 转到 **设置 \> 系统设置 \> 管理法人**。
2. 选择 **同步法人**，然后在确认对话框中选择 **确定**。

同步完成后，将显示新法人的数量。 新法人会显示在列表视图中。 默认配置组将分配给新法人。

## <a name="configure-invoice-import-channels"></a>配置发票导入渠道

供应商通过不同格式（纸质或图像）从不同渠道（电子邮件、文件工作区或发票门户）发送发票。 Invoice capture 解决方案可以处理不同的渠道和格式。 支持以下类型：

- Office 365 Outlook
- Outlook.com
- SharePoint
- OneDrive

当为特定帐户创建渠道时，将构建具有预定义模板的自动流来监视收件箱或空间内的传入电子邮件或文件。 具有有效发票的任何文件都会被识别出来并被发送到发票区域，等待应付帐款 (AP) 职员进行处理。 附件应为 PDF 或图像格式。 发票可以根据渠道配置加载到 Invoice capture 解决方案中。

### <a name="create-a-channel"></a>创建渠道

如果您已导入其他解决方案包（Dynamics 365 Invoice capture – 安装工具），Office 365 Outlook 的默认连接已经可以使用。 如果您想为不同的电子邮件帐户或其他渠道类型创建更多连接，请参阅[为渠道创建更多连接](invoice-capture-advanced-settings.md#create-additional-connections-for-channels)。

要创建渠道，请执行以下步骤。

1. 转到 **设置 \> 系统设置 \> 配置渠道**。
2. 选择 **新建**。
3. 设置以下字段：

    - 渠道名称
    - Description
    - 类型
    - 连接

只有符合以下条件的电子邮件或文件才可以被导入解决方案。

| 类型               | 配置  | 更多信息… |
|--------------------|----------------|------------------|
| Office 365 Outlook | 文件夹         | 电子邮件文件夹必须在根目录下。 默认使用“收件箱”文件夹。 不支持子文件夹。 |
|                    | 主题筛选器 | （可选）应包含在主题中的子字符串。 |
|                    | 来源           | （可选）发件人的电子邮件地址。 如果您要指定多个地址，使用分号 (;) 作为分隔符。 |
| SharePoint         | 站点地址   | 站点地址的 URL。 |
|                    | 文件夹         | 站点地址中的文件夹。 |

### <a name="activate-the-channel"></a>激活渠道

保存流时，字段会显示渠道的状态和创建时间。 最初，**状态** 字段将设置为 **停用**。 **状态描述** 字段表示渠道已初始化并准备好激活。

要激活渠道，选择 **激活**。 **状态** 和 **状态描述** 字段将更新。

如果不需要某个渠道，您可以将其停用。 要停用渠道，选择 **停用**。 **状态** 和 **状态描述** 字段将更新。

### <a name="manage-flows-in-flow-management"></a>在流管理中管理流

您可以在 **配置渠道** 页面或流管理中查看渠道。

要查看更多详细信息，转到 **管理系统 \> 默认解决方案 \> 云端流**，然后选择目标流。 显示的详细信息包括链接的连接、负责人和运行历史记录。

要同步状态，选择 **检查** 确认渠道的状态与流的状态匹配。

某些异常处理案例将显示在 **状态描述** 字段中：

- **缺少 Dataverse 连接** – 当前用户未创建任何 **Microsoft Dataverse** 连接引用（至少应创建一个）。
- **未找到** – 链接到渠道的流已在流管理中删除。 应再次保存渠道以创建新渠道。
- **已在流管理中停用** – 流已在流管理中停用，渠道的状态与流的状态不同。
- **已在流管理中激活** – 流已在流管理中激活，渠道的状态与流的状态不同。
- **发生意外错误** – 用户必须确认站点是“通信站点”，并且文件夹是“文档库”。

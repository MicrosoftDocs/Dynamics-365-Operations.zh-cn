---
title: Invoice capture 解决方案配置组
description: 本文提供有关 Invoice capture 解决方案中配置组的一般信息。
author: sunfzam
ms.date: 09/28/2022
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
ms.openlocfilehash: cfe5ae35b4f87a350d944b30a49251081766ad27
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691141"
---
# <a name="invoice-capture-solution-configuration-groups"></a>Invoice capture 解决方案配置组

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

用户可以使用配置组管理发票字段列表和法人的手动审核设置。 用户可以为组中的不同法人设置发票配置。 同一个配置组中的所有法人使用相同的发票字段和手动审核设置。

## <a name="manage-configuration-groups"></a>管理配置组

要使用此应用管理配置组，转到 **设置**，然后选择 **系统设置 \> 定义配置组组件**。

在 **定义配置组** 页面，主选项卡显示已定义的配置组列表。 另外还会显示默认配置组。 对于每个配置组，可以执行以下操作：

- **复制配置组** – 您可以通过复制现有组来创建新配置组。 除了 **组名称** 和 **组描述** 之外，新组所有字段的值均与原始组相同。 复制配置组后，选择 **确定**。
- **删除配置组** – 要删除配置组，选择它，然后选择 **删除**。

    > [!NOTE]
    > 默认配置组无法删除。

- **编辑配置组的 ID** – 要编辑配置组的 ID，选择 **组 ID** 字段，然后更新值。 组 ID 不应包含空格或特殊字符，且不应超过 20 个字符。

    > [!NOTE]
    > **组 ID** 字段的值只能更新一次。

- **编辑配置组的描述** – 要编辑配置组的描述，选择 **描述** 字段，然后更新值。
- **更改手动审核设置** – 用户可以决定是否必须手动审核发票。 要更改手动审核设置，选择 **需要手动审核** 选项。 选项如下：

    - **始终手动审核** – 如果配置组中的发票始终需要手动审核，选择此选项。
    - **针对错误和警告** – 如果包含错误消息或警告消息的发票需要手动审核，选择此选项。
    - **针对错误** – 如果包含错误消息的发票需要手动审核，选择此选项。

- **更改置信度分数设置** – 置信度分数是 Invoice capture 解决方案提供的元数据，用于报告已确认发票数据的准确度。 分数越高，确认的数据可能越准确。 此配置允许用户根据置信度分数定义何时需要手动审核。 用户可以更改发票的置信度分数阈值。 要更新置信度分数设置，选择 **置信度分数** 字段，然后更新值。

    置信度分数有两种警报类型：

    - **警告** – 置信度分数超过警告阈值的发票字段被视为正确。 警告阈值必须大于错误阈值且小于 100。
    - **错误** – 置信度分数在错误阈值以下的发票字段被视为失败。 错误消息将显示给用户。 错误阈值必须大于 0（零）且小于错误阈值。 将为置信度分数在警告阈值和错误阈值之间的发票字段显示警告消息。

- **管理发票字段** – 用户可以管理并排查看器中显示的发票字段列表。 在 **发票字段管理** 选项卡上，选择齿轮符号，选择要添加的发票字段，然后选择 **保存**。 所选字段将被添加到列表。 要从列表中删除发票字段，在该字段上选择 **删除**。

### <a name="manage-file-filters-optional"></a>管理文件筛选器（可选）

管理文件筛选器允许用户为传入的发票文件定义其他筛选器。 不符合筛选条件的文件会被接收，并显示在 **已接收文件** 列表中，但它们会显示文件验证错误。 此行为不同于渠道中定义的筛选器的行为。 对于那些筛选器，不会接收不符合条件的文件。 用户可以查看传入文件并决定每个文件是否为无效发票，他们可以废弃该文件，或手动包含该文件，用于在捕获的发票中进行识别和包含在捕获的发票中。

安装 Invoice capture 解决方案时，会定义默认文件筛选器。 此文件筛选器是全局性的。 如果您需要不同的筛选器设置，可以更新默认筛选器。 如果字段是必填项，选择 **必需**。 

### <a name="accepted-file-size"></a>接受的文件大小

您可以选择接受的文件大小。

> [!NOTE]
> 不支持超过 20,480 千字节 (KB) 的文件。

### <a name="supported-file-types"></a>支持的文件类型

当前支持以下文件类型：

- PDF
- PNG
- JPG
- JPEG
- TIF
- TIFF

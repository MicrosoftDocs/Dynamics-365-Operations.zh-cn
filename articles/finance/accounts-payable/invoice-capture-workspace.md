---
title: Invoice capture 解决方案工作区
description: 本文提供有关 Invoice capture 解决方案工作区的信息。
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
ms.openlocfilehash: 4f3af7abf94542437be6132344d6bb7ffaf33d07
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691136"
---
# <a name="invoice-capture-solution-workspace"></a>Invoice capture 解决方案工作区

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="side-by-side-viewer-for-the-invoice-capture-solution"></a>Invoice capture 解决方案的并排查看器

将发票输入系统通常是一个耗时且容易出错的过程，因为职员必须在多个附件文件和窗口之间导航来收集正确的信息。 并排文档查看器可以让流程更加简单、高效和准确，从而帮助改善您处理发票时的体验。

并排文档查看器允许用户在同一窗口中并排打开原始文档和发票。 发票页面会填充来自原始发票文档的信息。 此查看器在发票页面字段和原始发票文档之间建立连接。 查看器还可以帮助用户查找发票页面上存在的所有错误。

### <a name="open-the-side-by-side-viewer"></a>打开并排查看器

在 Microsoft Dynamics 365 Finance 中，您可以从摘要页面的列表或发票列表页打开并排查看器。 您还可以通过双击记录或选择发票编号来打开它。

### <a name="using-the-side-by-side-viewer"></a>使用并排查看器

#### <a name="manually-review-an-invoice"></a>手动审核发票

由于有错误或警告，已导入的发票文档可能需要手动审核。 在并排查看器中，文档标题将显示状态 **已导入**，当前版本将为 **原始版本**。

要开始审核发票，选择 **开始审核**。 所有字段都将变为可编辑。 **状态** 字段将更新为 **正在审核**，**当前版本** 字段将更新为 **修改版本**。

#### <a name="view-and-work-with-messages"></a>查看和处理消息

用户应从消息窗格开始审核过程。 错误消息以红色 X 表示，警告消息以三角形表示，信息性消息以圆圈表示。 根据配置组设置的阈值，与置信度分数相关的消息可以分类为警告或错误。 有关详细信息，请参阅 [Invoice capture 解决方案配置组](invoice-capture-config-group.md)。

可以从消息窗格、发票标题或发票行忽略警告和错误消息。 忽略消息后，它不再显示为错误或警告，发票也不会出现验证失败。

- 要从消息窗格忽略消息，选择 **忽略**。 要重置已忽略的消息，再次选择 **忽略**。 然后消息类型将从错误或警告更改为信息。
- 要从发票标题或发票行忽略消息，在字段上选择 **忽略**。 消息符号将消失。 但是，如果从消息窗格重置消息，它会重新出现。

对于与发票标题字段相关的消息，当您在消息窗格中选择该消息时，光标将移到标题部分的相应字段。

#### <a name="proofread-and-edit-fields"></a>校对和编辑字段

如果字段的值是通过光学字符识别 (OCR) 从原始发票读取的，该字段上会出现一个符号。 如果您选择符号，文档查看器会放大并突出显示读取字段值的位置，以帮助您验证发票数据。

要将文档查看器重置为其原始放大倍率，请执行以下步骤之一：

- 选择您之前选择的相同符号。
- 选择文档查看器右上角的按钮。

根据需要编辑字段。 当光标离开字段时，编辑会自动保存。 字段右侧的符号表示该字段已手动更新。 页面刷新时，该符号将被删除。

#### <a name="check-an-invoice-to-get-up-to-date-messages"></a>检查发票以获取最新消息

当您编辑字段时，字段值会更新，但不会生成新的验证消息。 要获取最新的验证消息，选择 **检查**。 消息窗格、发票标题和发票行中的消息将更新。

#### <a name="complete-the-review"></a>完成审核

要完成审核，选择 **完成审核**。 发票已验证。 如果发现任何错误，文档状态将保持 **正在审核** 状态，并会显示一个消息栏。 消息窗格以及发票标题和行中的所有消息都会自动更新，以提供有关验证失败原因的信息。

修复所有锁定错误后，即可完成审核。 文档状态将更新为 **已审核**，字段无法再进行编辑。 您可以通过再次选择 **开始审核** 来重新开始审核。

#### <a name="generate-a-pending-vendor-invoice-in-finance"></a>在 Finance 中生成待处理的供应商发票

要将发票文档发送到连接的 Finance 环境，选择 **生成**。 如果发票生成失败，消息栏中会显示一条错误消息。

#### <a name="void-an-invoice"></a>将发票作废

要将发票作废，选择 **作废**。 作废的发票无法进行审核，也不会显示在 **发票需要手动审核** 列表中。

### <a name="validation-logic"></a>验证逻辑

并排查看器中的一些关键字段在发票暂存数据中不存在，但在 Finance 中生成待处理发票时需要这些字段。 这些字段派生自 Finance 中的当前发票暂存数据和主数据的组合。

必须派生的字段有 **法人**、**供应商帐户** 和 **物料编号**。 字段必须按以下顺序派生。 如果字段的派生失败，流程将停止。

1. **法人** – 法人将首先派生。 如果找到法人的活动映射规则，将根据公司名称和公司地址派生法人。
2. **供应商帐户** – 接下来，根据活动映射规则以及派生的法人与供应商的名称和供应商地址的组合来派生供应商帐户。
3. **物料编号** – 最后，根据以下三类信息从暂存派生物料名称：

    - 配置的映射规则
    - 派生的法人
    - 派生的供应商帐户

要运行验证，在并排查看器中选择 **检查**。 当前，验证执行以下检查：

- **强制检查** – 此检查验证并排查看器的必填字段。 用户可以在 **配置设置** 页面选择哪些字段必须是必填字段。
- **置信度分数** – 用户可以设置置信度分数的警告阈值和错误阈值。 此检查的重点是 OCR 中低于这些阈值的置信度分数。 将根据验证结果显示错误或警告消息。
- **法人** – 此检查验证法人是否在 Finance 中。 如果法人不在 Finance 环境中，验证将失败。

当第一次使用并排查看器时，在用户选择 **检查** 时，将运行派生和验证流程。 如果发票准确，当用户选择 **完成审核** 时，将运行验证流程。 当用户选择 **生成供应商发票** 时，也会运行此流程。

派生流程发生在验证流程之前，所有警告或错误都来自验证流程。 警告和错误将在 Finance 中记录。

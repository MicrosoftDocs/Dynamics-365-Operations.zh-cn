---
title: 配置工作流中的审核流程
description: 使用以下过程配置审核流程的属性。
author: ChrisGarty
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99a4e131b2afa65152d8e9d41b8405895d997250
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070794"
---
# <a name="configure-approval-processes-in-a-workflow"></a>配置工作流中的审核流程

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

使用以下过程配置审核流程的属性。

要配置审核流程，在“工作流”编辑器中，右键单击审核元素，然后单击 **属性** 以打开 **属性** 窗体。

## <a name="name-the-approval-process"></a>为审核流程命名

按照以下步骤为审核流程输入名称。

1. 在左侧窗格中，单击 **基本设置**。
2. 在 **名称** 字段中，为该审核流程输入唯一名称。

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a>指定系统何时对文档采取操作

如果满足特定条件，可将系统配置为自动对对文档采取操作。 例如，系统可审核总金额小于 100 美元的支出报表。 按照以下步骤指定系统何时对文档采取操作。

1. 在左窗格中，单击 **自动操作**。
2. 选中 **启用自动操作** 复选框。
3. 单击 **添加条件**。
4. 输入条件。
5. 按需输入附加条件。
6. 要验证输入的条件是否正确配置，请完成以下步骤：

    1. 单击 **测试** 以打开 **测试工作流条件** 窗体。
    2. 在该窗体的 **验证条件** 区域中选择某个记录。
    3. 单击 **测试**。 系统对该记录进行评估，判断其是否符合您定义的条件。
    4. 单击 **确定** 或 **取消** 返回到 **属性** 窗体。

7. 在 **自动完成操作** 列表中选择系统应对文档采取的操作。

## <a name="specify-when-notifications-are-sent"></a>指定发送通知的时间

您可以在审核、拒绝、委托、呈报或更改文档后向相关人员发送通知。 按照以下步骤指定发送通知的时间以通知发送给哪些人员。

1. 在左窗格中，单击 **通知**。
2. 选中要对其发送通知的事件旁边的复选框：

    - **委托**- 将文档分配给其他用户进行审核时。
    - **呈报**- 分配的用户未在分配的时间内对文档采取操作时。
    - **审核**- 已审核文档时。
    - **拒绝**- 拒绝文档时。
    - **请求更改**- 分配的用户请求对提交的文档进行更改时。

3. 为您在第 2 步中选择的事件选择行。
4. 单击 **通知文本** 选项卡。
5. 在文本框中，输入通知的文本。
6. 要对文本进行个性化设置，可以插入占位符，向用户显示时，该占位符由相应的数据替换。 按照以下步骤插入占位符：

    1. 在消息文本中，单击应出现占位符的位置。
    2. 单击 **插入占位符**。
    3. 在显示的列表中，选择要插入的占位符。
    4. 单击 **插入**。

7. 要添加通知的翻译，请单击 **翻译**。 在显示在窗体中，执行以下步骤：

    1. 单击 **添加**。
    2. 在显示的列表，选择您要输入的文本的语言。
    3. 在 **已翻译的文本** 文本框中输入文本。
    4. 要对文本进行个性化设置，插入占位符。
    5. 单击 **关闭**。

8. 单击 **接收人** 选项卡。
9. 指定通知发送给哪些人员。 选择下表中的选项之一，然后按照该选项的其他步骤转到第 10 步。

    <table>
    <thead>
    <tr>
    <th>选项</th>
    <th>通知收件人。</th>
    <th>附加步骤</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><strong>参与者</strong></td>
    <td>分配到特定组或角色的用户</td>
    <td>
    <ol>
    <li>在选择<strong>参与者</strong>后，单击<strong>基于角色</strong>选项卡。</li>
    <li>在<strong>参与者类型</strong>列表中，选择向其发送通知的组或角色类型。</li>
    <li>在<strong>参与者</strong>列表中，选择向其发送通知的组或角色。</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><strong>工作流用户</strong></td>
    <td>参与当前工作流的用户</td>
    <td>
    <ol>
    <li>在选择<strong>工作流用户</strong>后，单击<strong>工作流用户</strong>选项卡。</li>
    <li>在<strong>工作流用户</strong>列表中，选择参与工作流的用户。</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><strong>用户</strong></td>
    <td>特定用户</td>
    <td>
    <ol>
    <li>在选择<strong>用户</strong>后，单击<strong>用户</strong>选项卡。</li>
    <li>选择向其发送通知的用户，然后将这些用户移动到<strong>所选用户</strong>列表中。</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

10. 对您在第 2 步中选择的每个事件重复 第 3 步到第 9 步。

## <a name="specify-a-final-approver"></a>指定最终审核人。

您可以为以下情况指定最终批准者：批准者是提交文档以供批准的人，并且正在使用“不允许提交者批准”。 按照以下步骤指定最终审核人。

1. 在工作流编辑器中，右键单击审核元素，然后选择 **属性** 以打开 **属性** 窗体。
2. 在左侧窗格中，单击 **高级设置**。
3. 选中 **使用最终审核人** 复选框。
4. 从列表中选择要作为最终审核人的用户。

## <a name="set-a-time-limit"></a>设置时间限制

如果必须在特定时间内完成审核流程，请执行以下步骤。

> [!NOTE]
> 在这些步骤中选择的选项将覆盖您在每个审核步骤的 **分配** 和 **呈报** 区域选择的选项。

1. 在左侧窗格中，单击 **高级设置**。
2. 选中 **为工作流元素** **设置时间限制** 复选框。
3. 在 **持续时间** 字段中，指定必须在何时完成审核流程。 选择以下选项之一：

    - **小时** – 输入必须在几小时内完成审核流程。 然后选择您的组织使用的日历，并输入有关您的组织的工作周的信息。
    - **天** – 输入必须在几天内完成审核流程。 然后选择您的组织使用的日历，并输入有关您的组织的工作周的信息。
    - **周** – 输入必须在几周内完成审核流程。
    - **月** – 选择必须在哪一周和哪一日前完成审核流程。 例如，您可能希望在当月第三周的周五之前完成审核流程。
    - **年** – 选择必须在哪一月、哪一周和哪一日前完成审核流程。 例如，您可能希望在十二月的第三周的周五之前完成审核流程。

4. 如果超出时间限制，系统将对文档采取操作。 在 **操作** 列表中选择系统应采取的操作。

## <a name="specify-which-actions-are-available-to-the-user"></a>指定用户可以采取的操作

将单据分配给用户进行审核后，该用户必须对该单据采取行动。 按照以下步骤指定要对用户提交的文档采取什么操作。

1. 在左侧窗格中，单击 **高级设置**。
2. 如果用户可批准文档，请选中 **审核** 复选框。
3. 如果用户可拒绝文档，请选中 **拒绝** 复选框。
4. 用户可以请求对文档进行更改时选中 **请求更改** 复选框。
5. 如果用户可以将文档分配给其他用户进行审核，请选中 **委托** 复选框。

> [!NOTE]
> **从企业门户中的工作列表启用操作** 复选框已被弃用。

## <a name="configure-the-approval-steps"></a>配置审核步骤

审核流程包括多个审核步骤。 完成以下过程以将步骤添加到审核流程并配置这些步骤。

1. 在工作流编辑器中，双击审核流程。 工作流编辑器显示审核流程的步骤。
2. 要添加审核步骤，请将步骤从 **工作流元素** 区域拖到画布。
3. 要配置审核步骤，请参阅[配置工作流中的审核步骤](configure-approval-step-workflow.md)。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: "配置工作流中的自动化任务"
description: "本主题说明如何配置自动化任务的属性。"
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192061
ms.assetid: c0aceb57-b5e6-4ef3-91e7-89a21c9f048a
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 047abbf297b3514c7f97d2baa6c0f5cab6696cde
ms.contentlocale: zh-cn
ms.lasthandoff: 08/08/2018

---

# <a name="configure-automated-tasks-in-a-workflow"></a>配置工作流中的自动化任务

[!include [banner](../includes/banner.md)]

本主题说明如何配置自动化任务的属性。

要配置自动化任务，在工作流编辑器中，右键单击任务，然后单击**属性**打开**属性**页面。 然后使用以下过程配置自动化任务的属性。

## <a name="name-the-task"></a>为任务命名

按照以下为自动化任务输入名称。

1. 在左侧窗格中，单击**基本设置**。
2. 在**名称**字段中，为该任务输入唯一名称。

## <a name="specify-when-notifications-are-sent"></a>指定发送通知的时间

已允许或取消自动化任务时，您可以向人员发送通知。 按照以下步骤指定发送通知的时间以通知发送给哪些人员。

1. 在左窗格中，单击**通知**。
2. 选中要对其发送通知的事件旁边的复选框：

    - **执行**– 在运行任务时发送通知。
    - **已取消**– 在取消任务时发送通知。

3. 为您在第 2 步中选择的事件选择行。
4. 在**通知文本**选项卡上，在文本框中输入通知的文本。
5. 要对通知进行个性化设置，可以插入占位符。 向用户显示通知时，占位符由适当的数据代替。 按照以下步骤插入占位符：

    1. 在文本框中，单击应该出现占位符的位置。
    2. 单击**插入占位符**。
    3. 在出现的列表中，选择要插入的占位符。
    4. 单击**插入**。

6. 若要添加通知的翻译，请执行以下步骤：

    1. 单击**翻译**。
    2. 在出现的页面上，单击**添加**。
    3. 在出现的列表中，选择您输入文本使用的语言。
    4. 在**已翻译的文本**字段中，输入文本。
    5. 如果要对文本进行个性化设置，可以如步骤 5 所述插入占位符。
    6. 单击**关闭**。

7. 在**接收人**选项卡上，指定向谁发送通知。 选择下表中的选项之一，然后按照该选项的其他步骤转到第 8 步。

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
    <td>参与者</td>
    <td>分配到特定组或角色的用户</td>
    <td>
    <ol>
    <li>在您选择<strong>参与者</strong>后，在选项卡<strong>基于角色</strong>上，在<strong>参与者类型</strong>列表中，选择要向其发送通知的组或角色的类型。</li>
    <li>在<strong>参与者</strong>列表中，选择向其发送通知的组或角色。</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>工作流用户</td>
    <td>参与当前工作流的用户</td>
    <td>
    <ul>
    <li>在您选择<strong>工作流用户</strong>后，在选项卡<strong>工作流用户</strong>上，在<strong>工作流用户</strong>列表中，选择参与工作流的用户。</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>用户</td>
    <td>特定的 Microsoft Dynamics 365 for Finance and Operations 用户</td>
    <td>
    <ol>
    <li>在选择<strong>用户</strong>后，单击<strong>用户</strong>选项卡。</li>
    <li><strong>可用用户</strong>列表包含所有 Finance and Operations 用户。 选择向其发送通知的用户，然后将这些用户移动到<strong>所选用户</strong>列表中。</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. 对您在第 2 步中选择的每个事件重复 第 3 步到第 7 步。


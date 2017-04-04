---
title: "配置应用在仓库的应用字段名称"
description: "此主题描述如何定义并配置仓库字段名称和应用优先级 Dynamics 中 365 操作。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: ce8f6d6f7090995bc44db1ba0103a7d6c0416620
ms.lasthandoff: 03/31/2017


---

# <a name="configure-app-field-names-in-warehousing-app"></a>配置应用在仓库的应用字段名称

此主题描述如何定义并配置仓库字段名称和应用优先级 Dynamics 中 365 操作。 

**注释：**此主题适用于在仓库管理"中的功能。 在不适用于库存管理"中的功能。 工序的 Dynamics 365 -仓库是您可以使用仓库执行任务的应用程序。 您可以定义和配置用于应用的字段名称，以及配置字段名称应分配的优先级。 本主题说明如何定义和配置应用这些仓库字段名称，和优先级，以及如何在 Dynamics 365。工序-仓库。 有关如何配置到 Dynamics 365 的连接的详细信息的工序的仓库-仓库，请参阅本指南 [则安装和配置操作的 Dynamics 365 -安装 Configuration app.md] (仓库)。

<a name="configure-warehouse-app-field-names"></a>配置应用仓库字段名称
===================================

如果某工序所使用 Dynamics 365 -在您的仓库移动设备时，可以配置如何在您的设备上应显示数据的元**应用仓库字段名称**页。 在 Dynamics 中 365 的新公司中的工序，选择**创建的设置默认**生成用于仓库移动设备工作流的所有字段名称，则分配一首选的输入模式和输入类型。它们。 在您生成了所有字段名称后，您可以选择以下输入选项。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>选项</th>
<th>说明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>首选输入类型</td>
<td>此选项定义是否应为所选字段名称显示用于扫描或手动输入一字段输入域。 如果条码用于字段，则使用此功能非常有用。根据部分字段。 <strong>注意：</strong> 对于用于首选的输入模式的字段名称，如果 <strong>扫描</strong>条码不可读取或损坏，设置到，可以手动输入信息。</td>
</tr>
<tr class="even">
<td>输入类型</td>
<td>此选项定义应为所选字段名称使用的输入类型。 四个可用选项：
<ul>
<li><strong>选择</strong>包含 - -选择从选项的列表。 此选项使用的字段名称不可编辑。</li>
<li><strong>日期</strong>为指定的日期 - -将字段名称显示具有一个标签的日期格式。 -在输入日期的格式所帮助仓库工人查看。 此选项使用的字段名称不可编辑。</li>
<li><strong>Alpha</strong>- -，如果选中，将在应用设备键盘时使用，则手动输入信息。 键盘体验可以更改要使用的设备。</li>
<li><strong>数字</strong>仅使用数字输入的字段的名称 - -上，您可以选中此选项显示具有输入域的自定义{{而数字键盘不是：instead_of}}设备键盘。</li>
</ul></td>
</tr>
</tbody>
</table>

<a name="configure-warehouse-app-field-priority"></a>配置应用仓库字段优先级
======================================

**请在应用仓库字段**优先级"页面中，您可以为不同地方字段名称的优先级。组 这样便可以在决定主要任务页应显示哪些信息使用应用时，仓库，此时工作人员执行任务。 如果单击**创建的设置默认**默认组，优先级组生成。 创建多个组。根据需要优先级可能的，但是，仅三个优先级。组任务页将显示。 在工序的 Dynamics 365 发送元数据对应用，则分配每个字段相对优先级物料组，其优先级，并且应用将显示在对任务的页面的元数据包含前三个优先级组。 溢出的元数据的其余上辅助详细信息页将显示。 下表显示五个优先级组的示例。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>优先级组</th>
<th>已分配字段</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> 优先级为 10</td>
<td><ul>
<li>项目</li>
<li>数量</li>
<li>度量单位</li>
</ul></td>
</tr>
<tr class="even">
<td> 优先级为 20</td>
<td><ul>
<li>群集职位</li>
<li>群集</li>
</ul></td>
</tr>
<tr class="odd">
<td> 优先级为 30</td>
<td><ul>
<li>物料描述</li>
</ul></td>
</tr>
<tr class="even">
<td> 优先级为 40</td>
<td><ul>
<li>配置</li>
<li>颜色</li>
<li>尺寸</li>
<li>样式</li>
</ul></td>
</tr>
<tr class="odd">
<td> 优先级为 50</td>
<td><ul>
<li>库位</li>
<li>牌照</li>
</ul></td>
</tr>
</tbody>
</table>

例如，工作人员，在仓库上执行的任务，移动设备，如果应用中显示数据的元包括以下字段：

-   项目
-   数量
-   度量单位
-   物料描述
-   尺寸和位置

应用基于仓库字段优先级设置在上述表中，行上 3 信息以下任务页将显示：

-   第 1 行：物料数量，度量单位，
-   第 2 行：物料描述
-   第 3 行：大小

剩余的元数据，例如，位置，任务页上详细信息"页面上，将不显示，而是将显示。 若要了解和查看用户界面的示例，请参阅过帐博客 [过帐工序的 Dynamics 365 -仓库] (https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/)。

<a name="see-also"></a>请参阅
--------

[则安装和配置操作的 Microsoft Dynamics 365 –安装配置仓库] (仓库 app.md)



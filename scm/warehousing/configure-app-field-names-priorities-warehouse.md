---
title: "配置 Warehousing 应用程序中的应用程序字段名"
description: "此主题介绍如何在 Dynamics 365 for Operations 中定义和配置仓库应用程序字段名和优先级。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: edcbf8a0921e0eb08d0f970e681c9d098b354c0b
ms.contentlocale: zh-cn
ms.lasthandoff: 05/25/2017


---

# <a name="configure-app-field-names-in-warehousing-app"></a>配置 Warehousing 应用程序中的应用程序字段名

[!include[banner](../includes/banner.md)]


此主题介绍如何在 Dynamics 365 for Operations 中定义和配置仓库应用程序字段名和优先级。 

**注意：**本主题适用于仓库管理中的功能。 它不适用于库存管理中的功能。 Dynamics 365 for Operations - Warehousing 是可用于执行仓库任务的应用程序。 可定义和配置此应用程序中使用的字段名，以及配置应该为字段名分配的优先级。 此主题说明如何在 Dynamics 365 for Operations - Warehousing 中定义、配置和使用这些仓库应用程序字段名和优先级。 有关如何配置与 Dynamics 365 for Operations - Warehousing 之间的连接的详细信息，请参阅教程[安装和配置 Dynamics 365 for Operations - Warehousing](install-configure-warehousing-app.md)。

<a name="configure-warehouse-app-field-names"></a>配置仓库应用程序字段名
===================================

在移动设备上使用 Dynamics 365 for Operations - Warehousing 时，可在**仓库应用字段名**页面中配置应如何在设备上显示元数据。 在 Dynamics 365 for Operations 中的新公司中，选择**创建默认设置**以生成将在仓库移动设备工作流中使用的所有字段名，然后为其分配首选输入模式和输入类型。 生成所有字段名之后，可以选择以下输入选项。

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
<td>此选项定义应如何为所选字段名显示扫描字段或手动输入的输入字段。 这对根据条码是否用于字段来区分字段十分有用。 <strong>注释：</strong>对于首选输入模式设置为<strong>扫描</strong>的字段名，如果条码不可识别或已损坏，则可手动输入信息。</td>
</tr>
<tr class="even">
<td>输入类型</td>
<td>此选项定义应对所选字段名使用哪种输入类型。 有四个选项：
<ul>
<li><strong>选择</strong> - 包含可供选择的选项的列表。 使用此选项选择的字段名不可编辑。</li>
<li><strong>日期</strong> - 指定为日期的字段名将显示带标签的日期格式。 这将帮助仓库工作人员了解要使用哪种格式输入日期。 使用此选项选择的字段名不可编辑。</li>
<li><strong>字母</strong> - 如果选择此选项，在应用程序中手动输入信息时，将使用设备键盘。 可根据所用设备更改键盘体验。</li>
<li><strong>数字</strong> - 对于仅使用数字输入的字段名，可选择此选项以显示带输入字段的自定义数字键盘，而不是设备键盘。</li>
</ul></td>
</tr>
</tbody>
</table>

<a name="configure-warehouse-app-field-priority"></a>配置仓库应用字段优先级
======================================

在**仓库应用字段优先级**页面中，可将字段名放入不同优先级组。 这样就可以定义当仓库工作人员使用此应用程序执行任务时，应在主任务页面中显示哪些信息。 如果单击**创建默认设置**，将生成一组默认优先级组。 可以根据需要创建任意数量的优先级组，但是任务页面中将仅显示三个优先级组。 当 Dynamics 365 for Operations 向该应用程序发送元数据时，将根据每个字段的优先级组为字段分配一个相对优先级，并且该应用程序将在任务页面中显示元数据中包含的前三个优先级组。 将在第二详细信息页面中显示其余过剩元数据。 下表显示五个优先级组的示例。

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
<td> 优先级 10</td>
<td><ul>
<li>项目</li>
<li>数量</li>
<li>度量单位</li>
</ul></td>
</tr>
<tr class="even">
<td> 优先级 20</td>
<td><ul>
<li>群集职位</li>
<li>群集</li>
</ul></td>
</tr>
<tr class="odd">
<td> 优先级 30</td>
<td><ul>
<li>物料描述</li>
</ul></td>
</tr>
<tr class="even">
<td> 优先级 40</td>
<td><ul>
<li>配置</li>
<li>颜色</li>
<li>尺寸</li>
<li>样式</li>
</ul></td>
</tr>
<tr class="odd">
<td> 优先级 50</td>
<td><ul>
<li>库位</li>
<li>牌照</li>
</ul></td>
</tr>
</tbody>
</table>

例如，当仓库工作人员在移动设备上执行任务时，如果应用程序中将显示的元数据包含以下字段：

-   项目
-   数量
-   度量单位
-   物料描述
-   尺寸和位置

将根据上表中设置的仓库应用程序字段优先级，在任务页面中显示以下 3 行信息：

-   第 1 行：物料、数量、度量单位
-   第 2 行：物料描述
-   第 3 行：尺寸

其余元数据（如位置）将不在任务页面中显示，但是将在详细信息页面中显示。 若要详细了解和查看用户界面的示例，请参阅博客文章[介绍 Dynamics 365 for Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/)。

<a name="see-also"></a>请参阅
--------

[安装和配置 Microsoft Dynamics 365 for Operations – Warehousing](install-configure-warehousing-app.md)





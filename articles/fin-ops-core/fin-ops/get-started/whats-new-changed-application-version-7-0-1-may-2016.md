---
title: Dynamics AX 应用程序版本 7.0.1（2016 年 5 月）的新增功能和更改内容
description: 本文介绍了 Microsoft Dynamics AX 应用程序版本 7.0.1 中的新功能和更改的功能。 本版于 2016 年 5 月发布，版本号为 7.0.1265.23014。
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 91213
ms.assetid: f0bbc78f-87fc-40e9-b46a-6655893f69be
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 1dd76150dd1519adf2c453db8e874d6db32b5906
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693134"
---
# <a name="whats-new-or-changed-in-dynamics-ax-application-version-701-may-2016"></a>Dynamics AX 应用程序版本 7.0.1（2016 年 5 月）的新增功能和更改内容

[!include [banner](../includes/banner.md)]

本文介绍了 Microsoft Dynamics AX 应用程序版本 7.0.1 中的新功能和更改的功能。 本版于 2016 年 5 月发布，版本号为 7.0.1265.23014。

## <a name="electronic-reporting-er"></a>电子申报 (ER)

| 您能怎么做？ | 为什么如此重要 |
|------------------|------------------------|
| 为设计电子申报 (ER) 报表配置运行时对话框，以便用户可以选择他们想要的财务维度。 | 在运行时，在运行 ER 报表的对话框中，用户可以选择多个财务维度。 所选财务维度的详细信息将显示在生成的电子文档中。 |
| 在设计 ER 报表时通过与所需数据源的单个映射配置对多个财务维度的访问。 | 相同的 ER 报表配置可用于生成显示交易数据以及财务维度详细信息的电子文档，否认用户选择的或为当前法人或实例配置的财务维度的数量是多少。 |
| 配置 ER 报表，以在动态生成的使用 OPENXML 工作表格式创建的电子单据的列中输入数据。 | ER 报表可以通过水平复制列在生成的 OPENXML 工作表中输入数据。 因此，可以重用相同的 ER 报表配置来生成具有不同的动态生成的列数的电子文档。 |
| 配置 ER 目标以使格式的输出结果定向到特定目标︰文件、电子邮件或存档（Microsoft SharePoint 文件夹或 Microsoft Azure Storage）。 | 以前，当您运行 ER 配置时，一个消息框出现，需要用户执行操作来保存或打开文件。 现在，您可以为每个格式配置和每个输出组件（文件夹或文件）分别预配置目标。 具有相应的访问权限的用户还可以在运行时修改目标设置。 |

## <a name="pos--microsoft-dynamics-ax-retail"></a>POS – Microsoft Dynamics AX Retail

| 您能怎么做？ | 为什么如此重要 |
|------------------|------------------------|
| 使用 Google Chrome 浏览器。 | 零售商现在可以从 Chrome 浏览器启动 Cloud POS，并可以体验 Microsoft Edge 和 Cloud POS 的 Internet Explorer 版本中提供的所有功能。 |

## <a name="financial-reporting"></a>财务报告

| 您能怎么做？ | 为什么如此重要 |
|------------------|------------------------|
| 重新构建财务报告数据市场。 | 当在环境之间移动 Dynamics AX 数据库或对该环境进行其他入侵性更改时，可能必须重建财务报告数据库。 现提供 Windows PowerShell 脚本为您重建数据库。 |
| 您可以不再选择无效的报表设计器选项。 | Management reporter 的市场内版本中使用的几个报表设计器选项不适用于此版本的 Dynamics AX。 这些选项与财务报表设计、输出和链接相关。 这些选项已被从财务报表设计器从删除来防止用户错误。 |

## <a name="financial-management"></a>财务管理

| 您能怎么做？ | 为什么如此重要 |
|------------------|------------------------|
| 生成应付帐款付款的付款确认文件。 | 可以生成付款确认文件以帮助防止支票欺诈。 |

## <a name="warehouse-and-production"></a>仓库和生产

<table>
<thead>
<tr>
<th>您能怎么做？</th>
<th>为什么如此重要</th>
</tr>
</thead>
<tbody>
<tr>
<td>定义控制在特定位置创建一组产品的工作的仓库工作策略。</td>
<td>仓库流程有时不包括工作。 通过使用新仓库工作策略，您可以阻止创建原材料领料工作，并在特定位置放置一组产品的成品。</td>
</tr>
<tr>
<td>指定生产输出位置不是牌照控制。</td>
<td>现在您可以指定产品输出位置不是牌照控制。 例如，当上游生产订单在充当下游生产订单的生产输入位置的某个位置直接将物料报告为完工入库时，此功能很有用。</td>
</tr>
<tr>
<td>支持包含具有同一物料的不同产品维度的物料的物料清单。</td>
<td>当在生产环境中使用一个或多个产品维度时，可能遇到希望根据同一物料的不同变型生产物料的情况。 有关详细信息，请参阅<a href="https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/">此博客</a>。</td>
</tr>
<tr>
<td>在物料清单的第一个级别具有循环结构的生产订单从材料资源规划的物料清单级别计算中排除。</td>
<td>不能为在物料清单层次结构中导致循环的生产订单的产品变型分配正确的物料清单级别。</td>
</tr>
<tr>
<td>为材料资源规划和成本计算计算单独的物料清单级别︰
<ul>
<li>对于材料资源规划，在新 <strong>ReqItemLevel</strong> 表中计算物料清单级别。 在计算中，已结束的生产订单将被忽略。</li>
<li>对于生产成本计算，在 <strong>InventTable</strong> 中计算物料清单级别。 在计算中，已结束的生产订单将被包括在内。</li>
</ul>
</td>
<td>
<ul>
<li>在运行材料资源规划时，例如，主计划的计划和增加，仅需要重新计算用于材料资源计划的物料清单级别。 换句话说，不需要计算用于生产成本计算的物料清单级别。</li>
<li>在运行成本计算操作时，例如，库存结转，仅用于生产成本计算的物料清单级别需要重新计算。</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>其他资源

[Finance and Operations 主页中的新增功能或更改](whats-new-changed.md)

[新的或更新任务指南（2016 年 5 月）](new-updated-task-guides-available-may-2016.md)

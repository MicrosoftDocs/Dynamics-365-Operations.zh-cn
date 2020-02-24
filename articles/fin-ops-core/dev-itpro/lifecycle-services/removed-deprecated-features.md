---
title: Lifecycle Services (LCS) 中已移除或弃用的功能
description: 本主题介绍已经从 Microsoft Dynamics Lifecycle Services (LCS) 移除或计划移除的功能。
author: AngelMarshall
manager: AnnBe
ms.date: 02/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 96ecd040ef8661765c0a3861d8e07fee3c241161
ms.sourcegitcommit: fb7d0efd97754f1ae0b5aa765d0eeb3f57b8078f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2020
ms.locfileid: "3027972"
---
# <a name="removed-or-deprecated-features-in-lifecycle-services-lcs"></a>Lifecycle Services (LCS) 中已移除或弃用的功能

[!include[banner](../includes/banner.md)]

本主题介绍已从 Microsoft Dynamics Lifecycle Services (LCS) 移除或弃用的功能。

- *已移除*的功能在服务中不再可用。
- *已弃用*的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。

提供此列表是为了让您可以在制定自己的计划时考虑这些功能的移除和弃用。

## <a name="october-2019-announcements"></a>2019 年 10 月公告

### <a name="flowchart-diagrams-in-business-process-modeler"></a>业务流程建模器中的流程图图表

<table>
<tbody>
<tr>
<td><strong>弃用/移除的原因</strong></td>
<td>我们正在弃用业务流程建模器 (BPM) 中的流程图图表组件，因为旧版设计导致使用率较低。</td>
</tr>
<tr>
<td><strong>被另一个功能取代？</strong></td>
<td>否</td>
</tr>
<tr>
<td><strong>影响的区域</strong></td>
<td>业务流程建模器</td>
</tr>
<tr>
<td><strong>状态</strong></td>
<td>已弃用：BPM 中的流程图图表组件预计将于 2020 年移除。 以下功能将被移除：
<ul>
<li>现有流程图将无法查看或编辑。 与流程图活动关联的形状属性也将不再可用，因为整个<strong>流程图</strong>选项卡将被移除。 这些流程图既包括自动生成的默认流程图，也包括基于这些默认流程图修改的自定义流程图。</li>
<li>旧版适应/差距分析功能将不再可用。 因此，不会再自动创建差距列表或提供导出。
<p><strong>注意：</strong>此功能先前已被弃用，已由 Microsoft Azure DevOps 集成取代。</p>
</li>
<li>将不再提供流程图的版本历史记录。</li>
</ul>
</td>
</tr>
</tbody>
</table>

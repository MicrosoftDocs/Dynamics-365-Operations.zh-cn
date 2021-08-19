---
title: 成本对象控制器的访问权限
description: 此主题提供关于成本对象控制员访问权限的信息。
author: AndersGirke
ms.date: 06/24/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c30a7c2765647aad17a475ba8705b8e688d166593adf242fcd15d90e49334189
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733021"
---
# <a name="access-rights-for-cost-object-controllers"></a>成本对象控制器的访问权限

[!include [banner](../includes/banner.md)]

**成本控制** 工作区是经理可以查看其成本对象的性能的一个中心点。 此工作区使经理可以使用成本核算数据，即使他们不是成本会计员。 出于安全原因，应仅允许经理查看与他们负责的具体成本对象有关的成本核算数据。

成本核算中有四个唯一角色。

| 角色名称               | 许可证      |
|-------------------------|--------------|
| 成本会计经理 | 活动     |
| 成本核算师         | Operations   |
| 成本核算师   | Operations   |
| 成本对象控制器  | 团队成员 |

此主题说明如何向经理分配 **成本对象控制员** 角色。

将 **成本对象控制员** 角色分配到经理后，经理可执行以下任务：

- 访问 **成本控制** 工作区（在客户端中）。

    - 钻取并获得支持钻取体验的页面的查看权限。

- 访问 **成本控制** 工作区（在移动应用程序中）。

> [!NOTE]
> **成本对象控制员** 角色不控制用户可以访问和查看其数据的成本对象。 行级别安全通过维度层次结构和访问列表层次结构提供。

## <a name="grant-access-rights"></a>授予访问权限
以下示例显示维度层次结构的样式。

**维度层次结构明细**

| 维度层次结构名称 | 维度    | 维度层次结构类型名称      | 访问列表层次结构 |
|--------------------------|--------------|------------------------------------|-----------------------|
| 组织             | 成本中心 | 维度分类层次结构 | **是**               |

您可以使用层次结构设计器中的 **用户** 快速选项卡在各节点上插入一个或多个用户 ID。

|             节点                 | 用户            | 起始维度成员     |   截止维度成员   |
|-----------------------------------|------------------|---------------------------|-------------------------|
| 组织                      | 本杰明，克莱尔 |                           |                         |
| &nbsp;&nbsp;管理                 | 四月            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;财务   | 艾丽西亚           | CC002                     | CC003                   |
|                                   |                  | CC007                     | CC007                   |
| &nbsp;&nbsp;&nbsp;&nbsp;HR        | 尔尼            | CC001                     | CC001                   |
| &nbsp;&nbsp;生产            | 大卫            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;包装 | 爱伦            | CC005                     | CC005                   |
| &nbsp;&nbsp;&nbsp;&nbsp;程序集  | 克里斯            | CC006                     | CC006                   |

> [!NOTE]
> 成本会计员应分配到该层次结构的顶层，以便他们可以查看成本核算中的所有条目。

应用访问列表层次结构及其安全设置前，**成本核算参数** 页 **常规** 选项卡上的 **为成本对象维度成员启用视图访问** 选项必须设置为 **是**（**成本核算** > **设置** > **参数**）。

访问列表层次结构的设置用于控制在以下区域显示的数据：

- **成本控制** 工作区（在客户端中）：

    - 用于钻取的页面上的数据

- **成本控制** 工作区（在移动应用程序中）：

    - 卡内余额

- Microsoft Power BI：

    - Power BI 可视化项中显示的数据
    - 在 Dynamics 365 Finance 客户端中嵌入的数据 Power BI 可视化项

> [!IMPORTANT]
> - 在访问列表层次结构可能会影响 Power BI 中的数据前，Power BI 中的访问列表层次结构和行级别安全性必须配对。 有关详细信息，请参阅 [设置成本核算内容包的安全性](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)。
> - 此主题说明使用 **成本控制** 工作区前必须具备的先决条件。

其他资源

- [成本控制工作区](cost-control-workspace.md)
- [维度层次结构](dimension-hierarchy.md)
- [设置成本核算内容包的安全性](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

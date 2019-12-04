---
title: 组织和组织层次结构概览
description: 组织是共同工作以执行业务流程的群体。 组织层次结构表示构成您的公司的组织之间的关系。
author: sericks007
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMHierarchyManager, OMOperatingUnit,
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 17291
ms.assetid: 76b7ca45-93d4-45cc-b191-66ee63afa1fd
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8c28c9e8c2573bcd82434f88daa8f9cadc946209
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812378"
---
# <a name="organizations-and-organizational-hierarchies-overview"></a>组织和组织层次结构概览

[!include [banner](../includes/banner.md)]

组织是共同工作以执行业务流程的群体。 组织层次结构表示构成您的公司的组织之间的关系。

## <a name="organizations"></a>组织

您可以定义以下类型的内部组织：法人、运营单位和团队。

所有内部组织都为**聚会**实体的类型。 因此，这些组织使用通讯簿功能储存地址和联系信息。 当事人（可以是人员或组织）可以属于一个或多个通讯簿。

### <a name="legal-entities"></a>法人

法人是具有已登记的或法律允许的法律结构的组织。 法人可以输入到法律合同，并需要准备报告它们的业绩的报表。

公司是法人的一种类型。 现在，公司只能是您能创建的这类法人，每个法人与公司 ID 相关联。 因为程序中的某些功能区域在它们的数据模型中使用了公司 ID 或 DataAreaId，所以此关联存在。 在这些功能区域中，公司用作了数据安全性的边界。 用户只能访问他们当前登录到的公司的数据。

### <a name="operating-units"></a>运营单位

运营单位是用来拆分企业中的经济资源和运营流程的控件的组织。 运营单位中的人有义务最大化对稀有资源的使用、改进流程和记录他们的业绩。

运营单位的类型包括成本中心、业务单位、价值流、部门以及零售渠道。 下表提供了有关每个类型的运营单位的详细信息。

| 运营单位类型 | 描述 | 用途 |
|---------------------|-------------|---------|
| 成本中心         | 经理对预算的和实际支出负问责性的工序运营单位。 | 用于跨法人的业务流程的管理和运营控制。 |
| 业务单位       | 创建来满足战略业务目标的一个半自主运营单位。 | 用于基于组织单独服务的法人的工厂或产品行的财务报表。 |
| 价值流        | 控制一个或多个生产流的工序单位。 | 通常在控制产品或服务要求提供给客户的活动和流的精益制造中。 |
| 部门          | 表示执行销售或记账等特定任务的组织的类别或功能部分的运营单位。 | 用于申报功能区域。 某部分可能具有损益责任，而且可能是由一组成本中心构成的。 |
| 零售渠道      | 应用单位表示传统实体店、在线商店或联机市场。 | 用于法人内或跨法人的一个或多个商店的管理和运营控制。 |

### <a name="teams"></a>团队

团队是一个组织，该组织的成员共享公共责任、利益或目标。 团队不能用于组织层次结构。

## <a name="organizational-hierarchies"></a>组织的层次结构

设置组织的层次结构以查看和申报来自不同视角的业务。 例如，您可以针对纳税、法律或法定申报设置法人的层次结构。 设置基于运营单位的层次结构以报告不是法律要求但用于内部控制的财务信息。 例如，您可以创建一个采购层次结构以控制采购策略、规则和义务流程。

每个层次结构都将分配用途。 层次结构用途确定可以包括在层次结构中的组织的类型。 该用途还决定着哪些应用程序方案能够在该层次结构中使用。

层次结构中的组织可以共享参数、策略和交易记录。 组织可以继承或覆盖其父级组织的参数。 但是，产品和地址簿等共享的主数据适用于整个组织，但是不能被单个组织覆盖。 创建组织和层次结构要求详细计划。 有关详细信息，请参阅[计划组织层次结构](plan-organizational-hierarchy.md)。

---
title: Dataverse 中的组织层次结构
description: 本文介绍财务和运营应用与 Dataverse 之间的组织数据集成。
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 48533dd104f62080d0ebd47389a4a829c772db13
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289037"
---
# <a name="organization-hierarchy-in-dataverse"></a>Dataverse 中的组织层次结构

[!include [banner](../../includes/banner.md)]



因为 Dynamics 365 Finance 是财务系统，所以 *组织* 是核心概念，并且系统设置从确认组织层次结构开始。 然后可以在组织级别，还可以在组织层次结构中的任何级别跟踪企业的财务。

尽管 Dataverse 没有组织层次结构这个概念，但是的确有一些松散的概念，如总销售收入。 在 Dataverse 集成中，组织层次结构数据结构添加到了 Dataverse。

## <a name="data-flow"></a>数据流

包含财务和运营应用和 Dataverse 的业务生态系统将继续采用组织层次结构。 这种组织层次结构基于财务和运营应用，并在 Dataverse 中显示以实现参考和扩展性目的。 下图显示在 Dataverse 中显示为从财务和运营应用到 Dataverse 的单向数据流的组织层次结构信息。

![体系结构图像。](media/dual-write-data-flow.png)

组织层次结构表映射可用于从财务和运营应用到 Dataverse 的单向数据同步。

## <a name="templates"></a>模板

组织是共同工作以执行业务流程的群体。 组织层次结构表示构成您的公司的组织之间的关系。 您可以定义以下类型的内部组织：法人、运营单位和团队。 如下表所示，创建了一组表映射以同步法人、运营单位和相关的组织层次结构信息。

财务和运营应用 | 客户互动应用     | Description
-----------------------|--------------------------------|---
[法人](mapping-reference.md#102) | cdm_companies | 
[法人](mapping-reference.md#142) | msdyn_internalorganizations |
[运营单位](mapping-reference.md#143) | msdyn_internalorganizations |
[组织层次结构 - 已发布](mapping-reference.md#139) | msdyn_internalorganizationhierarchies | 此模板提供组织层次结构已发布表的单向同步。
[组织层次结构目的](mapping-reference.md#140) | msdyn_internalorganizationhierarchypurposes | 此模板提供组织层次结构目的表的单向同步。
[组织层次结构类型](mapping-reference.md#141) | msdyn_internalorganizationhierarchytypes | 此模板提供组织层次结构类型表的单向同步。

## <a name="internal-organization"></a>内部组织

Dataverse 中的内部组织信息来自两个表：**运营单位** 和 **法人**。

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]


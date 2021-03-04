---
title: Dataverse 中的组织层次结构
description: 本主题介绍 Finance and Operations 应用与 Dataverse 之间的组织数据集成。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: e2b652f11db62eb58ffc2ec2fc4322149e7d45d1
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680064"
---
# <a name="organization-hierarchy-in-dataverse"></a>Dataverse 中的组织层次结构

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

因为 Dynamics 365 Finance 是财务系统，所以 *组织* 是核心概念，并且系统设置从确认组织层次结构开始。 然后可以在组织级别，还可以在组织层次结构中的任何级别跟踪企业的财务。

尽管 Dataverse 没有组织层次结构这个概念，但是的确有一些松散的概念，如总销售收入。 在 Dataverse 集成中，组织层次结构数据结构添加到了 Dataverse。

## <a name="data-flow"></a>数据流

包含 Finance and Operations 应用和 Dataverse 的业务生态系统将继续采用组织层次结构。 这种组织层次结构基于 Finance and Operations 应用，并在 Dataverse 中显示以实现参考和扩展性目的。 下图显示在 Dataverse 中显示为从 Finance and Operations 应用到 Dataverse 的单向数据流的组织层次结构信息。

![体系结构图像](media/dual-write-data-flow.png)

组织层次结构表映射可用于从 Finance and Operations 应用到 Dataverse 的单向数据同步。

## <a name="templates"></a>模板

产品信息包含与产品及其定义有关的所有信息，例如产品维度或跟踪维度和存储维度。 如下表所示，将创建表映射的集合以同步产品和相关信息。

Finance and Operations 应用 | 其他 Dynamics 365 应用 | 说明
-----------------------|--------------------------------|---
组织层次结构目的 | msdyn_internalorganizationhierarchypurposes | 此模板提供组织层次结构目的实体的单向同步。
组织层次结构类型 | msdyn_internalorganizationhierarchytypes | 此模板提供组织层次结构类型实体的单向同步。
组织层次结构 - 已发布 | msdyn_internalorganizationhierarchies | 此模板提供组织层次结构已发布实体的单向同步。
运营单位 | msdyn_internalorganizations |
法人 | msdyn_internalorganizations |
法人 | cdm_companies | 提供法人实体（公司）信息的双向同步。

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a>内部组织

Dataverse 中的内部组织信息来自两个表：**运营单位** 和 **法人**。

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
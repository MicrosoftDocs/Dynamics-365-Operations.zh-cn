---
title: Common Data Service 中的组织层次结构
description: 本主题介绍 Finance and Operations 应用与 Common Data Service 之间的组织数据集成。
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 9a12ab249129dce24cdca5e29d737fa9f68c0eac
ms.sourcegitcommit: 6e0909e95f38b7487a4b7f68cc62b723f8b59bd4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572441"
---
# <a name="organization-hierarchy-in-common-data-service"></a>Common Data Service 中的组织层次结构

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

因为 Dynamics 365 Finance 是财务系统，所以*组织*是核心概念，并且系统设置从确认组织层次结构开始。 然后可以在组织级别，还可以在组织层次结构中的任何级别跟踪企业的财务。

尽管 Common Data Service 没有组织层次结构这个概念，但是的确有一些松散的概念，如总销售收入。 在 Common Data Service 集成中，组织层次结构数据结构添加到了 Common Data Service。

## <a name="data-flow"></a>数据流

包含 Finance and Operations 应用和 Common Data Service 的业务生态系统将继续采用组织层次结构。 这种组织层次结构基于 Finance and Operations 应用，并在 Common Data Service 中显示以实现参考和扩展性目的。 下图显示在 Common Data Service 中显示为从 Finance and Operations 应用到 Common Data Service 的单向数据流的组织层次结构信息。

![体系结构图像](media/dual-write-data-flow.png)

## <a name="templates"></a>模板

组织层次结构实体映射可用于从 Finance and Operations 应用到 Common Data Service 的单向数据同步。

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a>内部组织层次结构目的

此模板提供组织层次结构目的实体从 Finance and Operations 到其他 Dynamics 365 应用的单向同步。

<!-- ![architecture image](media/dual-write-purpose.png) -->

源字段 | 映射类型 | 目标字段
---|---|---
HIERARCHYTYPE | \> | msdyn\_hierarchypurposetypename
HIERARCHYTYPE | \> | msdyn\_hierarchytype.msdyn\_name
HIERARCHYPURPOSE | \>\> | msdyn\_hierarchypurpose
IMMUTABLE | \>\> | msdyn\_immutable
SETASDEFAULT | \>\> | msdyn\_setasdefault

## <a name="internal-organization-hierarchy-type"></a>内部组织层次结构类型

此模板提供组织层次结构类型实体从 Finance and Operations 到其他 Dynamics 365 应用的单向同步。

<!-- ![architecture image](media/dual-write-type.png) -->

源字段 | 映射类型 | 目标字段
---|---|---
名称 | \> | msdyn\_name

## <a name="internal-organization-hierarchy"></a>内部组织层次结构

此模板提供组织层次结构已发布实体从 Finance and Operations 到其他 Dynamics 365 应用的单向同步。

<!-- ![architecture image](media/dual-write-organization.png) -->

源字段 | 映射类型 | 目标字段
---|---|---
VALIDTO | \> | msdyn\_validto
VALIDFROM | \> | msdyn\_validfrom
HIERARCHYTYPE | \> | msdyn\_hierarchytypename
PARENTORGANIZATIONPARTYNUMBER | \> | msdyn\_parentpartyid
CHILDORGANIZATIONPARTYNUMBER | \> | msdyn\_childpartyid
HIERARCHYTYPE | \> | msdyn\_hierarchytypeid.msdyn\_name
CHILDORGANIZATIONPARTYNUMBER | \> | msdyn\_childid.msdyn\_partynumber
PARENTORGANIZATIONPARTYNUMBER | \> | msdyn\_parentid.msdyn\_partynumber

## <a name="internal-organization"></a>内部组织

Common Data Service 中的内部组织信息来自两个实体：**运营单位**和**法人**。

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a>运营单位

源字段 | 映射类型 | 目标字段
---|---|---
LANGUAGEID | \> | msdyn\_languageid
NAMEALIAS | \> | msdyn\_namealias
名称 | \> | msdyn\_name
PARTYNUMBER | \> | msdyn\_partynumber
OPERATINGUNITTYPE | \>\> | msdyn\_type

### <a name="legal-entity"></a>法人

源字段 | 映射类型 | 目标字段
---|---|---
NAMEALIAS | \> | msdyn\_namealias
LANGUAGEID | \> | msdyn\_languageid
名称 | \> | msdyn\_name
PARTYNUMBER | \> | msdyn\_partynumber
无 | \>\> | msdyn\_type
LEGALENTITYID | \> | msdyn\_companycode

## <a name="company"></a>公司

提供 Finance and Operations 与其他 Dynamics 365 应用之间法人（公司）信息的双向同步。

<!-- ![architecture image](media/dual-write-company.png) -->

源字段 | 映射类型 | 目标字段
---|---|---
名称 | = | cdm\_name
LEGALENTITYID | = | cdm\_companycode

---
title: "将项目合同和项目直接从 Project Service Automation 同步到 Finance and Operations"
description: "本主题介绍用于将项目合同和项目直接从 Project Service Automation 同步到 Microsoft Dynamics 365 for Finance and Operations 的模板和基础任务。"
author: KimANelson
manager: AnnBe
ms.date: 10/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: 0889bc233674cb80dd056ac77edb5c936c6633a7
ms.contentlocale: zh-cn
ms.lasthandoff: 11/01/2018

---

# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a>将项目合同和项目直接从 Project Service Automation 同步到 Finance and Operations

[!include[banner](../includes/banner.md)]

本主题介绍用于将项目合同和项目直接从 Project Service Automation 同步到 Microsoft Dynamics 365 for Finance and Operations 的模板和基础任务。

> [!NOTE] 
> 如果您正在使用 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.300，您必须安装 KB 4074835。

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Project Service Automation 到 Finance and Operations 的数据传输

> [!NOTE]
> 应先熟悉 Microsoft Dynamics 365 Data integration 功能，才能使用 Project Service Automation 到 Finance and Operations 集成解决方案。

Project Service Automation 到 Finance and Operations 集成解决方案使用数据集成功能在 Project Service Automation 和 Finance and Operations 的实例之间同步数据。 可通过数据集成功能提供的集成模板将有关项目合同、项目、项目合同行和项目合同行里程碑的数据从 Project Service Automation 传输到 Finance and Operations。

下图显示 Project Service Automation 与 Finance and Operations 之间中如何同步数据。

[![Project Service Automation 与 Finance and Operations 集成的数据传输](./media/ProjectsAndContractsFlow.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>模板和任务

若要访问可用模板，请在 Microsoft PowerApps 管理员中心中选择**项目**，然后在右上角中选择**新建项目**以选择公共模板。

以下模板和基础任务用于将项目合同和项目从 Project Service Automation 同步到 Finance and Operations：

- **数据集成中的模板名称：** 项目和合同（PSA 到 Fin and Ops）
- **项目中的任务名称：**

    - 项目合同（PSA 到 Fin and Ops）
    - 项目（PSA 到 Fin and Ops）
    - 项目合同行（PSA 到 Fin and Ops）
    - 项目合同行里程碑（PSA 到 Fin and Ops）

必须先同步科目，才能同步项目合同和项目。

## <a name="entity-set"></a>实体集

| Project Service Automation       | Finance and Operations                                 |
|----------------------------------|--------------------------------------------------------|
| 订单                           | 项目合同集成实体                |
| 项目                         | 项目的集成实体                         |
| 订单行                      | 项目合同行集成实体           |
| 项目合同行里程碑。 | 项目合同行里程碑集成实体 |

## <a name="entity-flow"></a>实体流

项目合同在 Project Service Automation 中管理，并同步到 Finance and Operations 中充当项目合同。 在集成模板中，可在 Finance and Operations 中为项目合同设置集成源。

时间和物料项目和固定价格项目在 Project Service Automation 中管理，并同步到 Finance and Operations 中充当项目。 在模板集成时，可在 Finance and Operations 中为项目设置集成源。

项目合同行在 Project Service Automation 中管理，并同步到 Finance and Operations 中充当项目合同计费规则。 如果交付方法与默认项目类型不同，同步将更新合同行项目和项目组的项目类型。

项目合同行里程碑在 Project Service Automation 中管理，并同步到 Finance and Operations 中充当项目合同计费规则里程碑。

## <a name="project-service-automation-to-finance-and-operations-integration-solution"></a>Project Service Automation 到 Finance and Operations 集成解决方案

**项目合同**页上有**项目合同 ID** 字段。 该字段由一个自然唯一密钥组成以支持集成。

新建项目合同时，如果**项目合同 ID**值不存在，则使用编号规则自动生成。 该值由 **ORD** 以及依次紧跟在后面的一个递增编号规则和一个由六个字符组成的后缀构成。 下面是一个示例：**ORD-01022-Z4M9Q0**。

**项目编号**字段在**项目**页提供。 该字段由一个自然唯一密钥组成以支持集成。

新建项目时，如果**项目编号**值不存在，则使用编号规则自动生成。 该值由 **PRJ** 以及依次紧跟在后面的一个递增编号规则和一个由六个字符组成的后缀构成。 下面是一个示例：**PRJ-01049-CCNID0**。

应用 Project Service Automation 到 Finance and Operations 集成解决方案时，<TO DO: link in the top level document link where we will be adding the instructions for applying the PSA solution>升级脚本将在 Project Service Automation 为现有项目合同设置**项目合同 ID**字段，为现有项目设置**项目编号**字段。

## <a name="prerequisites-and-mapping-setup"></a>先决条件和映射设置

- 必须先同步科目，才能同步项目合同和项目。
- 在连接集中，向 **msdyn\_name \[Name\]** 添加 **msdyn\_organizationalunits** 的集成密钥字段映射。 可能首先需要向连接集添加一个项目。 有关详细信息，请参阅[将数据集成到 Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator)。
- 在连接集中，向 **msdynce\_projectnumber \[Project Number\]** 添加 **msdyn\_projects** 的集成密钥字段映射。 可能首先需要向连接集添加一个项目。 有关详细信息，请参阅[将数据集成到 Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator)。
- 可将项目合同和项目的 **SourceDataID** 更新为其他值，也可以将其从映射中移除。 默认模板值为 **Project Service Automation**。
- 必须更新 **PaymentTerms** 映射，才能在 Finance and Operations 中体现有效的付款期限。 也可以从项目任务中移除映射。 默认值映射具有演示数据的默认值。 下表显示 Project Service Automation 中的值。

    | 值 | 说明   |
    |-------|---------------|
    | 1     | Net 30        |
    | 2     | 2%10，Net 30 |
    | 3     | Net 45        |
    | 4     | Net 60        |

## <a name="power-query"></a>Power Query

如果满足以下条件，则必须使用 Microsoft Power Query for Excel：

- 您在 Microsoft Dynamics 365 for Sales 中有销售订单。
- 您在 Project Service Automation 中有多个组织单位，并且这些组织单位将映射到 Finance and Operations 中的多个法人。

如果必须使用 Power Query，请遵守以下准则：

- 项目和合同（PSA 到 Fin and Ops）模板有一个默认筛选器，其中仅包含类型为**工作项 (msdyn\_ordertype = 192350001)** 的销售订单。 此筛选器有助于确保不在 Finance and Operations 中为销售订单创建项目合同。 如果创建自己的模板，则必须添加这个筛选器。
- 创建的 Power Query 筛选器必须仅包含应同步到集成连接集的法人的合同组织。 例如，应将您的包含合同组织单位 Contoso US 的项目合同同步到 USSI 法人，但您的包含合同组织单位 Contoso Global 的项目合同则应同步到 USMF 法人。 如果不向任务映射添加此筛选器，则将把所有项目合同同步到为连接集定义的法人，而不考虑合同组织单位。

## <a name="template-mapping-in-data-integration"></a>数据集成中的模板映射

> [!NOTE] 
> 项目合同的默认映射中不包含 **CustomerReference**、**AddressCity**、**AddressCountryRegionID**、**AddressDescription**、**AddressLine1**、**AddressLine2**、**AddressState** 和 **AddressZipCode** 字段。 如果需要为项目合同同步此数据，可添加这些映射。
>
> 项目的默认映射中不包含 **Description**、**ParentID**、**ProjectGroup**、**ProjectManagerPersonnelNumber** 和 **ProjectType** 字段。 如果需要为项目同步此数据，可添加这些映射。

下图显示了数据集成中的模板任务映射的示例。 此映射显示将从 Project Service Automation 同步到 Finance and Operations 的字段信息。

[![模板映射](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![模板映射](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![模板映射](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![模板映射](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)


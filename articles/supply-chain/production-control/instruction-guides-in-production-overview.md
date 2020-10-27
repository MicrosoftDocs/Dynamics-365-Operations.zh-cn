---
title: 为生产中的工作人员提供混合现实指南
description: 本主题说明了如何将 Microsoft Dynamics 365 Supply Chain Management 中的生产管理模块与 Dynamics 365 Guides 集成。
author: cabeln
manager: tfehr
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkGuidesManufacturing
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: cabeln
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: d8c2da17d4e3df37c55844f0aad00f883725f741
ms.sourcegitcommit: c55fecae96b4bb27bc313ba10a97eddb9c91350a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989260"
---
# <a name="provide-mixed-reality-guides-for-workers-in-production"></a>为生产中的工作人员提供混合现实指南

生产流程中的工作人员将从在其工作范围内在适当时间提供的相关说明中受益。 *说明*适用于多个工作领域，包括：装配、服务、工序、认证和安全。 在所有这些核心业务功能中，持续进行的培训说明可以帮助员工实现更多目标，更好地进行工作。

## <a name="introduction"></a>简介

您可以通过不同的方式提供说明。 随附开箱即用的 [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/) 的一个有效系统。

Dynamics 365 Guides 可以帮助您的员工通过实践进行学习。 您可以通过分步说明来定义标准化流程，这些分步说明将指导您的员工使用他们所需的工具和零件，并向员工展示如何在实际工作中使用这些工具。

您可以将 Guides 附加到生产控制的各个方面，包括：

- [资源](#resources)
- [资源组](#resource-groups)
- [已发布产品](#released-products)
- [配方](#formulas)
- [配方版本](#formula-versions)
- [物料清单 (BOM)](#bom)
- [物料清单版本](#bom-versions)
- [运输路径](#routes)
- [工艺路线版本](#route-versions)
- [工艺路线工序关系](#route-operation-relations)

> [!NOTE]
> 您也可以将 Guides 与资产管理附加在一起。 有关该选项的详细信息，请参阅[将 Dynamics 365 Supply Chain Management（资产管理）与 Dynamics 365 Guides 集成](../asset-management/asset-management-guides-integration.md)。

当一线工作人员通过 Supply Chain Management 在车间中选择作业时，工作人员可以在作业卡上看到[相关指南](#logic)。 当工作人员选择一个特定指南时，该指南的 QR 码将显示在屏幕上。 然后，工作人员使用他们的 HoloLens 扫描 QR 码，这会启动 Guides 并显示所需的说明。

以下小节介绍了一些选定方案，在这些方案中，各个行业的公司都可以看到使用 Guides 显示制造说明时的最大价值。

### <a name="assembly"></a>程序集

![在装配任务中使用指南](media/instruction-guides-hero-assembly.png "在服务任务中使用指南")

装配操作说明向工作人员介绍了他们所需的工具和零件，以及如何在实际工作中使用它们。

例如，生产经理可以为[生产工艺路线](routes-operations.md)、[工序关系](routes-operations.md#operation-relations)或[物料清单](bill-of-material-bom.md)创建和分配指南。 工作人员将在车间中找到有关相应操作经验的相关说明。

### <a name="service"></a>服务

![在服务任务中使用指南](media/instruction-guides-hero-service.png "在服务任务中使用指南")

在作业现场为技术人员提供指导说明，从而无需计划其他访问。

例如，服务经理可以向完成质量评估例程的特定[产品](../../commerce/product.md)分配指南。

### <a name="quality"></a>质量

![在质量保证任务中使用指南](media/instruction-guides-hero-quality.png "在质量保证任务中使用指南")

推出新流程并通过将员工的知识变成可重复的工具来确保提高一致性。

例如，质量保证经理可以向完成质量评估例程的[产品](../../commerce/product.md)分配指南。

### <a name="certifications"></a>认证

![在与认证相关的任务中使用指南](media/instruction-guides-hero-certification.png "在与认证相关的任务中使用指南")

通过快速确定谁需要帮助以及哪里需要帮助，确保每个员工都符合高标准。

### <a name="safety"></a>安全

![在工作安全说明中使用指南](media/instruction-guides-hero-safety.png "在工作安全说明中使用指南")

提供在尝试进入物理环境之前以虚拟方式完成危险过程的说明。 通过混合现实方法，工作人员可以通过虚拟方式体验危险过程。

生产经理可以通过向[产品物料](../../commerce/product.md)、[工艺路线](routes-operations.md)和[工序](routes-operations.md#operation-relations)分配说明来提供有关危险物料处理的专门处理说明或专门处理过程。

## <a name="get-started-with-instructions-and-guides"></a>开始使用说明和 Guides

为了在生产过程中启用说明，Supply Chain Management 提供了与 Dynamics 365 Guides 的开箱即用集成。 需要 Guides 的许可和安装的应用程序实例，才能为生产资产和工作构建、维护和分配混合现实说明。

### <a name="prerequisites"></a>先决条件

若要使用此功能，您的系统必须包括以下内容：

- Dynamics 365 Supply Chain Management 版本 10.0.15 或更高版本
- Supply Chain Management 应用的[双写入](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write)。
- [Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) 版本 400.0.1.48 或更高版本

### <a name="turn-on-the-feature"></a>开启功能

若要使该功能在您的系统上可用，必须启用其 Configuration Key。 您只需要执行一次。 为此，管理员必须执行以下操作：

1. 将您的系统置于维护模式下，如[维护模式](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)中所述。
1. 转到**系统管理 \> 设置 \> 许可证配置**。
1. 展开**混合现实**部分，然后选择**混合现实指南**复选框。
1. 展开**生产管理**部分，然后选择**生产说明**复选框。
1. 关闭维护模式，如[维护模式](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)中所述。
  
## <a name="configure-how-guides-appear-on-the-shop-floor"></a>配置指南在车间中的显示方式

若要配置指南在车间中的显示方式，请转到**混合现实 \> Dynamics 365 Guides \> 配置指南集成**。

![为制造配置指南集成](media/instruction-guides-configure-integration.png "为制造配置指南集成")

设置以下字段：

- **CDS 环境子域** - 此字段应该已显示一个值。 此字段保留创建指南的 Common Data Service 环境的子域。 子域是 URL 的第一部分，通常以您的组织命名。 例如，如果您的 Common Data Service URL 是“contoso.crm4.dynamics.com”，您应该在此处输入 *contoso*。 此值用于构成指南的地址，并将编码为 QR 码。
- **QR 码大小** - 设置呈现的 QR 码的大小。 我们建议选择一个将填充大部分显示屏幕而不是超过显示屏幕的大小。 通常，*15* 是一个适合的值。
- **QR 码错误纠正级别** - 设置 QR 码的粒度。 更高的粒度可以帮助提高代码的可靠性，但是您的 **QR 码大小**必须足够大以支持所选纠正级别所需的详细级别。


> [!TIP]
> - 对于您的显示器过大的 QR 码大小将花费更长时间呈现，将其缩小以适应您的显示器。 这些没有好处。
> - QR 码太小可能会削弱 HoloLens 在某些环境中正确读取代码的能力。
> - 我们建议您测试为 HoloLens 用户显示 QR 码的每台设备的设置。 选择在车间环境中提供足够的可读性的设置。  

## <a name="get-an-overview-of-all-guide-assignments"></a>获取所有指南分配的概述

使用**所有指南**页面以查看组织中所有可用指南的列表以及生产流程和资源的所有分配。 若要打开它，请转到**混合现实 \> 指南 \> 所有指南**。 顶部的列表显示了所有可用指南，您可以在此处使用该字段筛选列表。 底部的列表显示了所有指南分配，并提供了用于管理它们的工具栏。

![管理指南](media/instruction-guides-allguides.png "管理指南")

以下部分描述了可以将指南分配到的对象类型。 每个分配的指南都提供了将自动附加到各个生产作业的说明，这些说明将在车间中提供。

## <a name="associate-a-guide-to-a-resource"></a><a name="resources"></a>将指南关联到资源

将指南添加到[资源](operations-resources.md)以在相关的生产作业中提供指南。

### <a name="typical-scenario-using-resources"></a>使用资源的典型方案

例如，您可以将具有常规机器安全性或处理说明的指南附加到机器类型的资源。 然后，该指南将适用于在机器上执行的每个作业。

### <a name="add-a-guide-to-a-resource"></a>将指南添加到资源

若要将指南添加到资源：

1. 转到**生产控制 \> 设置 \> 资源 \> 资源**。
1. 在列表窗格中，选择要为其分配指南的资源。
1. 展开**关联的指南**快速选项卡。
1. 从**关联的指南**工具栏中选择**添加**。 新行将添加到网格中。
1. 对于新行，请使用**名称**列中的下拉列表选择要分配的指南。 如果您有大量指南，可以筛选列表以查找所需的指南。
    ![管理指南](media/instruction-guides-allguides.png "管理指南")

## <a name="associate-a-guide-to-a-resource-group"></a><a name="resource-groups"></a>将指南关联到资源组

如果您使用资源组管理机器、生产线或工作单元的组，您可以向[资源组](tasks/define-discrete-manufacturing-resource-group.md)添加指南。

### <a name="typical-scenarios-using-resource-groups"></a>使用资源组的典型方案

**示例 1：** 您已经为同一型号的多台机器定义了一个资源组。 不是将机器型号的相关处理说明指南分配给每个相关资源，而是将该指南分配给反映该机器型号的资源组。

**示例 2：** 您已经为包含不同机器的工作单元定义了一个资源组，并且拥有提供有关如何维护工作单元的一般说明的指南。 该指南适用于此工作单元中的任何生产活动。

### <a name="add-a-guide-to-a-resource-group"></a>将指南添加到资源组

若要将指南添加到资源组：

1. 转到**生产控制 \> 设置 \> 资源 \> 资源组**。
1. 在列表窗格中，选择要为其分配指南的资源组。
1. 展开**关联的指南**快速选项卡。
1. 从**关联的指南**工具栏中选择**添加**。 新行将添加到网格中。
1. 对于新行，请使用**名称**列中的下拉列表选择要分配的指南。 如果您有大量指南，可以筛选列表以查找所需的指南。
    ![将指南添加到资源组](media/instruction-guides-resourcegroup.png "将指南添加到资源组")

## <a name="associate-a-guide-to-a-released-product"></a><a name="released-products"></a>将指南关联到已发布产品

您可以将指南添加到任何[已发布产品](../pim/tasks/create-released-product-single-company.md)。

### <a name="typical-scenario-using-released-products"></a>使用已发布产品的典型方案

产品级指南可帮助车间工作人员获得与运营或处理特定分已发布产品或物料相关的说明。

### <a name="add-a-guide-to-a-released-product"></a>将指南添加到已发布产品

若要将指南添加到已发布产品：

1. 转到**生产信息管理 \> 产品 \> 已发布产品**。
1. 打开要为其分配指南的产品。
1. 在“操作”窗格上，打开**工程师**选项卡，然后从**查看**组中，选择**关联的指南**。
1. 将针对选定产品打开**关联的指南**页面。
1. 在“操作”窗格上，选择**添加**以向网格添加一个新行。 
1. 对于新行，请使用**名称**列中的下拉列表选择要分配的指南。
    ![将指南添加到已发布产品](media/instruction-guides-ReleasedProduct-AddGuides.png "将指南添加到已发布产品")

## <a name="associate-a-guide-to-a-formula"></a><a name="formulas"></a>将指南关联到配方

您可以将指南添加到任何[配方](bill-of-material-bom.md#formulas-co-products-and-by-products)。

### <a name="typical-scenario-using-formulas"></a>使用配方的典型方案
  
配方级指南为车间工作人员提供与配方或基本配方相关的指导处理说明。 指南也可以分配到配方的版本。

> [!NOTE]
> 您可以根据工艺路线、工艺路线版本或工艺路线工序关系的配方分配与生产流程相关的指南。  

> 指南当前无法附加到单独的配方行。

### <a name="add-a-guide-to-a-formula"></a>将指南添加到配方

若要将指南添加到配方：

1. 转到**生产信息管理 \> 物料清单和配方 \> 配方**。
1. 打开要为其分配指南的配方。
1. 打开顶部快速选项卡上方的**标题**选项卡。
1. 展开**关联的指南**快速选项卡。
1. 从**关联的指南**工具栏中选择**添加**。 新行将添加到网格中。
1. 对于新行，请使用**名称**列中的下拉列表选择要分配的指南。
    ![将指南添加到配方](media/instruction-guides-Formula.png "将指南添加到配方")

## <a name="associate-a-guide-to-a-formula-version"></a><a name="formula-versions"></a>将指南关联到配方版本

您可以将指南添加到任何[配方版本](bill-of-material-bom.md#bom-and-formula-versions)。

### <a name="typical-scenario-using-formula-versions"></a>使用配方版本的典型方案

附加到单独配方版本的指南为车间工作人员提供了演示该版本配方的说明。

> [!TIP]
> 您可以根据工艺路线、工艺路线版本或工艺路线工序关系的此配方版本分配与生产流程相关的指南。  

> [!NOTE]
> 指南当前无法附加到单独的配方行。

### <a name="add-a-guide-to-a-formula-version"></a>将指南添加到配方版本

若要将指南添加到配方版本：

1. 转到**生产信息管理 \> 物料清单和配方 \> 配方**。
1. 打开包含要为其分配指南的版本的配方。
1. 打开顶部快速选项卡上方的**标题**选项卡。
1. 在**配方版本**快速选项卡上，选择要为其分配指南的版本。
1. 在**配方版本**工具栏上，选择**关联的指南**。
    ![打开与所选配方版本关联的指南](media/instruction-guides-FormulaVersion.png "打开与所选配方版本关联的指南")
1. 将针对配方版本打开**关联的指南**页面。
1. 在“操作”窗格上，选择**添加**以向网格添加一个新行。 
1. 对于新行，请使用**名称**列中的下拉列表选择要分配的指南。
    ![将指南添加到配方版本](media/instruction-guides-FormulaVersionAddGuide.png "将指南添加到配方版本")

## <a name="associate-a-guide-to-a-bill-of-materials"></a><a name="bom"></a>将指南关联到物料清单

您可以将指南添加到任何[物料清单](bill-of-material-bom.md) (BOM)。

### <a name="typical-scenario-using-bills-of-materials"></a>使用物料清单的典型方案

附加到物料清单的指南为车间工作人员提供了解释如何通过物料清单准备和处理物料的说明。 指南也可以分配到物料清单的版本。

> [!NOTE]
> 指南当前无法附加到单独的物料清单行。

### <a name="add-a-guide-to-a-bill-of-materials"></a>将指南添加到物料清单

若要将指南添加到物料清单：

1. 转到**生产信息管理 \> 物料清单和配方 \> 物料清单**。
1. 打开要为其分配指南的物料清单。
1. 打开顶部快速选项卡上方的**标题**选项卡。
1. 展开**关联的指南**快速选项卡。
1. 从**关联的指南**工具栏中选择**添加**。 新行将添加到网格中。
1. 对于新行，请使用**名称**列中的下拉列表选择要分配的指南。
    ![将指南添加到物料清单](media/instruction-guides-BOM.png "将指南添加到物料清单")

## <a name="associate-a-guide-to-a-bill-of-materials-version"></a><a name="bom-versions"></a>将指南关联到物料清单版本

您可以将指南添加到任何[物料清单版本](bill-of-material-bom.md#bom-and-formula-versions)。

### <a name="typical-scenario-using-bill-of-materials-versions"></a>使用物料清单版本的典型方案

附加到单独物料清单版本的指南为车间工作人员提供解释了如何为不同于通用物料清单或其他版本的物料清单版本准备和处理物料的说明。

> [!NOTE]
> 指南当前无法附加到单独的物料清单行。

### <a name="add-a-guide-to-a-bill-of-materials-version"></a>将指南添加到物料清单版本

若要将指南添加到物料清单版本：

1. 转到**生产信息管理 \> 物料清单和配方 \> 物料清单**。
1. 打开包含要为其分配指南的版本的物料清单。
1. 打开顶部快速选项卡上方的**标题**选项卡。
1. 在**物料清单版本**快速选项卡上，选择要为其分配指南的版本。
1. 在**物料清单版本**工具栏上，选择**关联的指南**。
    ![打开与所选物料清单版本关联的指南](media/instruction-guides-BOMVersion.png "打开与所选物料清单版本关联的指南")
1. 将针对物料清单版本打开**关联的指南**页面。
1. 在“操作”窗格上，选择**添加**以向网格添加一个新行。
1. 对于新行，请使用**名称**列中的下拉列表选择要分配的指南。
    ![将指南添加到物料清单版本](media/instruction-guides-BOMVersionAddGuide.png "将指南添加到物料清单版本")

## <a name="associate-a-guide-to-a-route"></a><a name="routes"></a>将指南关联到工艺路线

您可以将指南添加到任何[工艺路线](routes-operations.md)。

### <a name="typical-scenario-using-routes"></a>使用工艺路线的典型方案

工艺路线通常用于指定应如何基于物料清单或物料清单版本以及一组资源或资源组来生产特定的已发布产品。

将指南分配到工艺路线，以为各个生产流程提供分步说明。

### <a name="add-a-guide-to-a-route"></a>将指南添加到工艺路线

若要将指南添加到工艺路线：

1. 转到**生产控制 \> 所有工艺路线**。
1. 打开要为其分配指南的工艺路线。
1. 展开**关联的指南**快速选项卡。
1. 从**关联的指南**工具栏中选择**添加**。 新行将添加到网格中。
1. 对于新行，请使用**名称**列中的下拉列表选择要分配的指南。
    ![将指南添加到工艺路线](media/instruction-guides-Route.png "将指南添加到工艺路线")

## <a name="associate-a-guide-to-a-route-version"></a><a name="route-versions"></a>将指南关联到工艺路线版本

您可以将指南添加到任何[工艺路线版本](routes-operations.md#route-versions)。

### <a name="typical-scenario-using-route-versions"></a>使用工艺路线版本的典型方案

工艺路线版本通常用于根据现有工艺路线指定生产流程的变体。 您可以为每个工艺路线版本分配不同的指南。

### <a name="add-a-guide-to-a-route-version"></a>将指南添加到工艺路线版本

若要将指南添加到工艺路线版本：

1. 转到**生产控制 \> 所有工艺路线**。
1. 打开要为其分配指南的工艺路线。
1. 在**版本**快速选项卡上，选择要为其分配指南的版本。
1. 在**版本**工具栏上，选择**关联的指南**。
    ![打开与所选工艺路线版本关联的指南](media/instruction-guides-RouteVersion.png "打开与所选工艺路线版本关联的指南")
1. 将针对物料清单版本打开**关联的指南**页面。
1. 在“操作”窗格上，选择**添加**以向网格添加一个新行。
1. 对于新行，请使用**名称**列中的下拉列表选择要分配的指南。
    ![将指南添加到工艺路线版本](media/instruction-guides-RouteVersionAddGuide.png "将指南添加到工艺路线版本")

## <a name="associate-a-guide-to-a-route-operation-relation"></a><a name="route-operation-relations"></a>将指南关联到工艺路线工序关系

您可以将指南添加到任何[工艺路线工序关系](routes-operations.md#operation-relations)。

### <a name="typical-scenario-using-route-operation-relations"></a>使用工艺路线工序关系的典型场景

工序关系是向产品流程及其相关工序添加指南的最具体方法。 您可以为工艺路线中的每个工序指定指导，并针对为工艺路线指定的任何类型的关系环境（例如，特定物料、配置等）指定不同的指南。 您还可以指定该指南适用于工序中的哪些阶段（例如设置、排队、处理或运输）。

> [!NOTE]
> 如果为一个工艺路线的多个工序关系指定指南，则在这些指南中，只有最具体的关系中的指南才会显示在生成作业的车间中。

### <a name="add-a-guide-to-a-route-operation-relation"></a>将指南添加到工艺路线工序关系

若要将指南添加到工艺路线工序关系：

1. 转到**生产控制 \> 所有工艺路线**。
1. 打开要为其分配指南的工艺路线。
1. 在“操作”窗格上，打开**工艺路线**选项卡，然后从**维护**组中，选择**工艺路线详细信息**。
1. 将针对所选工艺路线打开**工艺路线详细信息**页面。
1. 在顶部网格中，选择要为其提供指南的工序。
1. 在底部网格中，选择一个特定的关系（或通用**所有**关系）。
    ![选择一个工序，然后选择一个关系](media/instruction-guides-RouteOperationRelation.png "选择一个工序，然后选择一个关系")
1. 在底部网格的上方，打开**关联的指南**选项卡。![关联的指南选项卡](media/instruction-guides-RouteOperationRelation-AddGuide.png "关联的指南选项卡")
1. 在底部网格的顶部，从工具栏中选择**添加**以向网格添加一个新行。
1. 对于新行，请使用**名称**列中的下拉列表选择要分配的指南。 在该行的其余部分，为每个环境选择相应的复选框，其中所选指南应该可用。

> [!NOTE]
> 您可以为每个工序的每个阶段添加一个或多个指南。

## <a name="select-guides-from-the-shop-floor-execution-interface"></a>从车间执行界面中选择指南

当工作人员在车间执行界面上打开作业列表时，Supply Chain Management 将为显示的作业找到相关的指南。 使用**指南**按钮以查看相关的指南。

![车间执行界面中的指南按钮](media/instruction-guides-Shopfloor1.png "车间执行界面中的指南按钮")

然后设定 HoloLens，通过浏览 QR 码并激活相应的指南来访问相应的指南。

![用于使用 HoloLens 访问指南的 QR 码](media/instruction-guides-Shopfloor2.png "用于使用 HoloLens 访问指南的 QR 码")

## <a name="resolving-the-logic-for-selecting-guides"></a><a name="logic"></a>解析用于选择指南的逻辑

您可以将指南添加到以下生产数据：

- [资源](#resources)
- [资源组](#resource-groups)
- [已发布产品](#released-products)
- [配方](#formulas)
- [配方版本](#formula-versions)
- [物料清单 (BOM)](#bom)
- [物料清单版本](#bom-versions)
- [运输路径](#routes)
- [工艺路线版本](#route-versions)
- [工艺路线工序关系](#route-operation-relations)

当 Supply Chain Management 为车间生成作业时，它将从这些来源收集相关的指南。 请注意以下重要的规则。

- 如果将物料清单版本或配方版本附加到工艺路线或生产订单，则附加到此版本的任何指南以及附加到该版本的父级物料清单或配方的指南都将显示在作业上。
- 如果将工艺路线版本附加到生产订单，则附加到此版本的任何指南以及附加到该版本的父级工艺路线的指南都将显示在作业上。
- 如果定义多个包括*所有*关系的工艺路线工艺关系并向其分配指南，则仅为该作业显示最具体关系中的指南。  

![解析相关指南的图表](media/instruction-guides-Resolve.png "解析相关指南的图表")

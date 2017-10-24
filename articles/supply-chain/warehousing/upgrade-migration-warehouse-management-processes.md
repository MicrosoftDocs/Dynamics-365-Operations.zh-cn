---
title: "将产品和仓库管理从 AX 2012 迁移到 Finance and Operations"
description: "此主题提供产品和仓库管理迁移选项的概览。"
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocationWHSProcessEnablement, WHSLocationProfile, InventTableStorageDimensionGroupChange, InventUpdateBlockedItem, WHSParameters, WHSReservationHierarchy, WHSUOMSeqGroupTable
audience: Application User
ms.reviewer: bis
ms.search.scope: AX 7.0.0, Operations, UnifiedOperations
ms.custom: 1714054
ms.assetid: 79a1a3b9-3a36-4162-8839-ec39b5e26602
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 9f618e61cd1cfb7e2abbbc0c9a00b5a06792b4bc
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="migrate-products-and-warehouse-management-from-ax-2012-to-finance-and-operations"></a>将产品和仓库管理从 AX 2012 迁移到 Finance and Operations

本主题提供关于 Microsoft Dynamics 365 for Finance and Operations Enterprise 版中的产品和仓库管理迁移选项的概览。

<a name="introduction"></a>简介
------------

在升级到 Finance and Operations 期间，如果产品所关联的存储维度组的设置与 Finance and Operations 中对存储维度组设置的要求不匹配，则该产品被锁定。 但是，在升级后，您可以使用**更改物料的存储维度组**流程中的一组迁移选项取消锁定在升级期间被锁定的产品。 之后可以处理这些产品的交易记录。 您的一些物料可能已经与其站点、仓库和库位库存维度处于活动状态且被物理跟踪的存储维度组关联。 在这种情况下，您可以使用**更改物料的存储维度组**流程允许这些物料在仓库管理流程中使用。 如果您要为现有物料使用仓库管理功能，此功能十分有用。

## <a name="upgrading-to-finance-and-operations-when-ax-2012-r3-wmsii-is-used"></a>使用 AX 2012 R3 WMSII 时，升级到 Finance and Operations
Finance and Operations 不再支持来自 Microsoft Dynamics AX 2012 的旧 **WMSII** 模块。 相反，您可以使用新的**仓库管理**模块。 在以前的版本中，可能为财务库存选择库位和托盘 ID 库存维度。 但是，作为升级流程的一部分，不可以再为财务库存启用托盘 ID 库存维度。 所有与使用托盘 ID 库存维度的存储维度组关联的产品将被锁定且不会被处理。

### <a name="enabling-items-in-finance-and-operations"></a>在 Finance and Operations 中启用物料

在 Finance and Operations 中，作为仓库管理流程一部分使用的物料必须与选择了**使用仓库管理流程**参数的存储维度组相关联。 选择此设置后，站点、仓库、库存状态、库位和牌照库存维度变为活动状态。 您可以仅为已经与库位库存维度处于活动状态的存储维度组关联的物料更改此类型的存储维度组。

### <a name="items-that-are-blocked-for-inventory-updates"></a>已针对库存更新锁定的物料

要查看在升级期间已锁定且无法处理的已发布产品的列表，请单击**库存管理** &gt; **设置** &gt; **库存** &gt; **针对库存更新锁定的物料**。

### <a name="reapplying-blocked-products"></a>重新应用锁定的产品

要取消锁定在升级期间已锁定的产品，必须为该产品选择新的存储维度组。 请注意，即使存在未结的库存交易记录，您也可以更改存储维度组。 要使用在升级期间已锁定的物料，您有两个选项：

-   将物料的存储维度组更改为仅使用站点、仓库和库位库存维度的存储维度组。 进行此更改后，不再使用托盘 ID 库存维度。
-   将物料的存储维度组更改为使用仓库管理流程的存储维度组。 进行此更改后，现在开始使用牌照库存维度。

### <a name="migration-processes"></a>迁移流程

在 Finance and Operations 中，物料跟踪是仓库管理流程的一部分。 对于这些流程，所有仓库及其库位必须与库位模板相关联。 从概念上讲，如果您要使用仓库管理流程，必须处理两个流程：

-   必须启用现有仓库以使用仓库管理流程。
-   现有的已发布的产品必须与使用仓库管理流程的新的存储维度组相关联。

如果源存储维度组使用托盘 ID 库存维度，使用托盘 ID 库位维度的现有库存的库位必须与选择了**使用牌照跟踪**参数的库位模板相关联。 如果不应启用现有仓库以使用仓库管理流程，您可以将现有库存的存储维度组更改为仅处理站点、仓库和库位库存维度的组。

### <a name="using-the-warehouse-management-processes"></a>使用仓库管理流程

在您可以使用**仓库管理**模块中的已发布产品前，产品必须使用选择了**使用仓库管理流程**参数的存储维度组。

#### <a name="enable-warehouses-to-use-warehouse-management-processes"></a>启用仓库以使用仓库管理流程

1.  创建至少一个新的库位模板。
2.  单击**仓库管理** &gt; **设置** &gt;**启用仓库管理流程** &gt;**启用仓库设置**。
3.  在**启用仓库设置**页，添加应启用的仓库。 您可以直接在页面上或使用 Microsoft Office 集成完成此步骤。
4.  将库位模板分配到所有库位。 您可以直接从页面使用 Microsoft Office 集成轻松地完成此步骤。 您可以在 [数据管理](../../dev-itpro/data-entities/data-entities.md) 中导出和导入数据或使用数据实体处理。
5.  验证更改。 作为验证过程的一部分，发生不同的数据完整性验证。 作为更大的升级流程的一部分，可能必须在源实现上调整发生的发货。 在这种情况下，需要附加数据升级。
6.  处理更改。

#### <a name="change-the-storage-dimension-group-for-items-so-that-it-uses-warehouse-management-processes"></a>更改物料的存储维度组，以便其使用仓库管理流程

1.  创建新的**库存状态**值，并将它分配为**仓库管理参数**设置中的**默认库存状态 ID**值。
2.  创建选择了**使用仓库管理流程**参数的新的存储维度组。
3.  在**预留层次结构**页，根据物料的存储和跟踪维度组定义新的预留层次结构。
4.  创建一个或多个单位序列组且序列组至少包括与用于物料的库存单位相同的单位。
5.  单击**仓库管理** &gt; **设置** &gt;**启用仓库管理流程** &gt;**更改物料的存储维度组**。
6.  在**更改物料的存储维度组**页，添加物料编号、存储维度组和单位序列组。 您可以直接在页面上、使用 Microsoft Office 集成或使用 [数据管理](../../dev-itpro/data-entities/data-entities.md) 中的数据实体流程完成此步骤。
7.  验证更改。 作为验证过程的一部分，发生不同的数据完整性验证。 作为更大的升级流程的一部分，可能必须在源实现上调整发生的发货。 在这种情况下，需要附加数据升级。
8.  处理更改。 更新所有库存维度可能需要一段时间。 您可以使用批处理作业任务监控进度。




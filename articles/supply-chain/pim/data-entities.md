---
title: 产品数据实体
description: 本主题提供有关可用于导入和导出产品数据的不同实体的信息。
author: cvocph
manager: tfehr
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: kamaybac
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2019-12-1
ms.openlocfilehash: e05d5febdd57a25d796fb3d085390758f5e7ceca
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007758"
---
# <a name="product-data-entities"></a>产品数据实体

[!include [banner](../includes/banner.md)]

要导入和导出产品数据，必须使用数据实体。 下表提供有关产品相关数据实体的详细信息，并介绍每个实体的用途。

| 实体 | 应用程序对象树 (AOT) 名称（类型） | 说明 |
|--------|-------------------------------------------|-------|
| 产品 V2 | `EcoResProductV2Entity` | 此实体用于导入和导出共享产品 - 独特产品和基础产品。 允许更新。 不支持基于集的 SQL 操作。 已启用开放数据协议 (OData)。 |
| 已发布产品 V2 | `EcoResReleasedProductV2Entity` | 此实体用于导入和导出已发布产品 - 独特产品和基础产品。 允许更新。 要求已经创建了共享产品。 导入新发布的产品时，将进行共享产品发布。 另外还有一些单独的实体可用于导入和导出已发布的基础产品和已发布的独特产品变型。 此实体不支持基于集的 SQL 操作或删除操作。 已启用 OData。 |
| 已发布产品创建 V2 | `EcoResReleasedProductCreationV2Entity` | 此实体用于一步导入共享产品和已发布产品。 尽管它支持导出，但不建议用于此目的，因为此实体的用途是产品创建。 不支持更新。 支持一组有限的字段（在产品创建对话框中可用的字段）。 不支持基于集的 SQL 操作。 不是通过 OData 公开。 |
| 产品变型 | `EcoResProductVariantEntity` | 此实体用于导入和导出共享产品变型。 允许更新。 要求已经创建了维度值。 集成密钥是基础产品加产品维度。 此实体不支持基于集的 SQL 操作。 已启用 OData。 支持删除操作。 不能通过添加新产品维度来扩展。 |
| 按产品编号标识分类的产品变型 | `EcoResProductNumberIdentifiedProductVariantEntity` | 此实体用于导入和导出共享产品变型。 允许更新。 要求已经创建了维度值。 集成密钥是产品编号（而 **产品变型** 实体的集成密钥是基础产品加产品维度）。 |
| 已发布的产品变型 | `EcoResReleasedProductVariantEntity` | 此实体用于导入和导出已发布产品变型。 允许更新。 要求已经创建了共享产品变型。 导入新发布的产品变型时，将进行共享产品变型发布。 此实体不支持基于集的 SQL 操作。 已启用 OData。 尽管它支持删除操作，但是由于当前平台中的错误，当前使用该操作会导致数据损坏。 此实体不能通过添加新产品维度来扩展。 |
| 按产品编号标识分类的已发放产品变型 | `EcoResProductNumberIdentifiedReleasedProductVariantEntity` | 此实体类似于 **已发布产品变型** 实体，但是集成密钥是产品编号，而不是基础产品加产品维度。 可以通过添加新产品维度来扩展。 |
| 适售的已发布产品 | `EcoResSellableReleasedProductEntity` | 此实体仅用于导出适售产品。 适售产品是具有为用于销售订单而需要具备的信息的产品。 相同的规则适用于使用 **已发布产品** 页上的 **验证** 功能对产品进行验证时。 |
| 已发布独特产品 V2 | `EcoResDistinctProductV2Entity` | 此实体用于导出独特产品。 独特产品可以是产品、子类型产品和产品变型。 |
| 已发布基础产品 V2 | `EcoResProductMasterV2Entity` | 此实体用于导入和导出基础产品。 未启用数据管理。 |
| 物料 - 条码 | `EcoResProductBarcodeEntityV3` | 此实体用于导出产品和条码。 此实体不允许更改追踪、更新或删除。 若要在条码上使用更改跟踪、更新或删除，请使用 **物料 - 条码关联** 实体。 |
| 物料 - 条码关联 | `EcoResProductBarcodeAssociationEntity` | 此实体用于导出产品和条码。 它允许更改跟踪、更新和删除。 若要使用实体，必须在 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中启用 *物料 - 条码改进* 功能。 其实体键为 `AssociationID`，这将在条码和产品之间创建关联。 若要添加对此键的支持，在打开该功能时，将针对现有物料条码数据填充表 `InventitemBarcodeAssociation`。 使用批处理作业填充该表，如果您的条码表具有大量记录，则可能会花费大量时间来运行批处理作业。 因此，我们建议您计划在适合您的业务计划的时间启用该功能（并因此运行批处理作业）。 |
| 产品生命周期状态 | `EcoResProductLifecycleSateEntity` | 此实体用于导入和导出可以分配给产品的不同产品生命周期状态。 |

> [!NOTE]
> 仅当已创建共享产品时，您才能使用 **已发布产品 V2** 数据实体将产品导入系统。 否则，要将产品导入系统，必须使用 **产品创建** 数据实体。

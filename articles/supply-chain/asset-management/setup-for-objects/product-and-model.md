---
title: 资产制造商和模型
description: 本主题介绍如何在资产管理中设置资产制造商和相关模型。
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetProductLookup, EntAssetModelLookup, EntAssetProduct
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae2dfcebcbab77cba1795a8b559a3a4244abd00e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4422903"
---
# <a name="asset-manufacturers-and-models"></a>资产制造商和模型

[!include [banner](../../includes/banner.md)]

 

本主题介绍如何在资产管理中设置资产制造商和相关模型。 可以将模型与资产类型关联。

## <a name="set-up-product-model-relations"></a>设置产品-模型关系

1. 选择 **资产管理** \> **设置** \> **资产** \> **制造商和模型**。
2. 选择 **新建** 以创建新产品。
3. 在 **制造商** 字段中，输入资产制造商的名称。
4. 在 **描述** 字段中，输入描述。
5. 在 **模型** 快速选项卡上，选择 **添加** 创建应该与资产制造商关联的资产模型。
6. 在 **模型** 字段中，输入资产模型的名称。
7. 在 **描述** 字段中，输入描述。
8. 在 **资产类型** 字段中，选择制造商模型应关联的资产类型。

    > [!NOTE]
    > 也可以在 **资产类型** 查找中为资产类型、制造商和模型设置关系。 有关详细信息，请参阅[资产类型](../setup-for-objects/object-types.md)。

    **详细信息** 快速选项卡中的 **模型** 字段显示为所选资产制造商设置的资产模型数量。 **资产** 字段显示使用所选制造商的资产的数量。
    
    **资产** 字段显示使用所选制造商模型的对象的数量。

> [!NOTE]
> 资产类型可以没有资产制造商模型关系，可以与一个资产制造商模型关联，也可以与多个资产制造商模型关联。 如果一个资产类型与至少一个制造商模型关联，则只能在其中可设置资产类型、制造商和模型组合的“资产管理”页面中选择在 **制造商模型** 查找中设置的组合。 这些页面包括 **所有资产**、**资产服务级别**、**作业类型默认值** 和 **维护预算行**。 如果某些资产类型不与任何制造商模型关联，则页面中仅显示这些资产类型，以及也不与资产类型关联的制造商模型。

## <a name="select-a-manufacturer-and-model-on-an-object"></a>为对象选择制造商和模型

1. 选择 **资产管理** \> **常用** \> **资产** \> **所有资产**。
2. 在 **资产** 列中，选择资产的链接。 将显示 **详细信息** 页。
3. 选择 **编辑**。
4. 在 **常规** 快速选项卡上的 **制造商** 和 **模型** 字段中选择值。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
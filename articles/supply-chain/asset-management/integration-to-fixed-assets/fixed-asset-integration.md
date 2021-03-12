---
title: 将资产管理与固定资产进行集成
description: 本主题说明如何集成资产管理和固定资产模块，以便可以将固定资产与维护资产关联起来。
author: kamaybac
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 879950b9aeb345fcd59dfe73d3963a44607c7ac2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994221"
---
# <a name="integrate-asset-management-with-fixed-assets"></a>将资产管理与固定资产进行集成

[!include [banner](../../includes/banner.md)]

通过集成 **资产管理** 和 **固定资产** 模块，您可以将固定资产与维护资产关联起来。 然后，固定资产用户可以从新的或现有固定资产创建维护资产，资产管理用户可以将维护资产与现有的固定资产相关联。 此功能还使固定资产用户可以轻松查看从工作订单过帐的相关维护资产的成本。

> [!NOTE]
> 在本主题中，*维护资产* 指 **资产管理** 模块中的资产，*固定资产* 指 **固定资产** 模块中的资产。

## <a name="set-a-default-location-for-new-maintenance-assets-that-are-created-from-fixed-assets-optional"></a>为从固定资产创建的新维护资产设置默认位置（可选）

通过此可选配置，您可以为从固定资产创建的新维护资产设置默认功能位置。 如果您已经完全完成此配置，通常只需配置这一次即可。

若要完成此配置，请执行以下步骤。

1. 转到 **资产管理 \> 设置 \> 资产管理参数**。
1. 在 **固定资产** 选项卡的 **功能位置** 字段中，选择默认位置。
1. 在操作窗格上，选择 **保存**。

## <a name="work-with-integrated-maintenance-assets-and-fixed-assets"></a>处理集成的维护资产和固定资产

本节提供了一系列过程，这些过程显示可以用来处理集成的资产管理和固定资产功能的各种方式。

### <a name="associate-an-existing-maintenance-asset-with-a-fixed-asset"></a>将现有维护资产与固定资产相关联

要将现有维护资产与固定资产相关联，请按照以下步骤操作。

1. 转到 **资产管理 \> 资产 \> 所有资产**（或 **有效资产**）。
1. 选择一个资产。
1. 在 **固定资产** 快速选项卡上，在 **固定资产编号** 字段中，选择一个现有的固定资产。
1. 在操作窗格上，选择 **保存**。

### <a name="view-the-fixed-asset-that-is-associated-with-a-selected-maintenance-asset"></a>查看与选定维护资产关联的固定资产

要查看与选定维护资产关联的固定资产，请按照以下步骤操作。

1. 转到 **资产管理 \> 资产 \> 所有资产**（或 **有效资产**）。
1. 选择一个资产。
1. 在 **固定资产** 快速选项卡上，在 **固定资产编号** 字段中，选择链接。

    所选资产的 **固定资产** 页面将打开。 （通常，此页面位于 **固定资产 \> 固定资产 \> 固定资产**。）

### <a name="view-the-maintenance-asset-that-is-associated-with-a-selected-fixed-asset"></a>查看与选定固定资产关联的维护资产

要查看与选定固定资产关联的维护资产，请按照以下步骤操作。

1. 转到 **固定资产 \> 固定资产 \> 固定资产**。
1. 选择一个资产。
1. 在操作窗格上，在 **资产管理** 选项卡的 **视图** 组中，选择 **维护资产**。

    与所选固定资产关联的资产的 **维护资产** 页面将打开。 （通常，此页面位于 **资产管理 \> 资产 \> 所有资产**。）

### <a name="view-maintenance-costs-that-are-associated-with-a-fixed-asset"></a>查看与固定资产相关联的维护成本

可以过帐维护资产的资产管理工作订单，每个工作订单通常都有成本。 当固定资产与维护资产相关联时，您可以直接从固定资产查看相关成本。

要查看与固定资产关联的维护成本，请按照以下步骤操作。

1. 转到 **固定资产 \> 固定资产 \> 固定资产**。
1. 选择一个资产。
1. 在操作窗格上，在 **资产管理** 选项卡的 **视图** 组中，选择 **维护成本**。

    **维护成本** 页面将打开，显示相关成本。

### <a name="create-a-new-maintenance-asset-for-an-existing-fixed-asset"></a><a name="new-maintenance-from-fixed"></a>为现有固定资产创建新维护资产

要为现有固定资产创建新维护资产，请按照以下步骤操作。

1. 转到 **固定资产 \> 固定资产 \> 固定资产**。
1. 选择一个资产。
1. 在操作窗格上，在 **资产管理** 选项卡的 **新建** 组中，选择 **创建维护资产**。 （如果此选项不可用，说明维护资产可能已经与所选固定资产关联。）
1. 按照[创建资产](../objects/create-an-object.md)中所述完成资产创建。

### <a name="create-a-new-fixed-asset-and-add-a-new-maintenance-asset-for-it"></a>创建新固定资产并为其添加新维护资产

要创建新固定资产并为其添加新维护资产，请按照以下步骤操作。

1. 转到 **固定资产 \> 固定资产 \> 固定资产**。
1. 在操作窗格上，选择 **新建**。
1. 按照[创建固定资产](../../../finance/fixed-assets/tasks/create-fixed-asset.md)中所述完成固定资产的创建。
1. 在操作窗格上，在 **资产管理** 选项卡的 **新建** 组中，选择 **创建维护资产**。
1. 按照[创建资产](../objects/create-an-object.md)中所述完成资产创建。

### <a name="remove-the-association-between-two-assets"></a>删除两个资产之间的关联

在某些情况下，您可能必须解除维护资产与其固定资产的关联。 例如，如果您想要从固定资产[创建新维护资产](#new-maintenance-from-fixed)，您必须先删除所有现有关联。

要删除维护资产和固定资产之间的现有关联，请按照以下步骤操作。

1. 转到 **资产管理 \> 资产 \> 所有资产**（或 **有效资产**）。
1. 查找并打开固定资产。
1. 在 **固定资产** 快速选项卡上，清除 **功能位置** 字段中的值。
1. 在操作窗格上，选择 **保存**。

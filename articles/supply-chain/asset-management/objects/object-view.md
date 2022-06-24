---
title: 资产视图
description: 本文介绍资产管理中的资产视图。
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectTree, EntAssetFunctionalLocationTree
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a416dbea0bab8f6a506ae5cfbfc4feeae8edfe29
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882712"
---
# <a name="asset-view"></a>资产视图

[!include [banner](../../includes/banner.md)]

 

本文介绍资产管理中的资产视图。 **资产视图** 页以树视图显示有效资产和功能位置。 因此，您可以轻松获取资产与功能位置之间的关系的概览。 此外，还可以查看有关功能位置、资产和相关物料清单 (BOM) 的详细信息。 还可以快速获取与资产有关的有效维护请求和工作订单的概览。

1. 选择 **资产管理** \> **常用** \> **资产** \> **资产视图**。
2. 若要更改页面上显示的视图，请在 **视图** 字段中选择一个新值。

    > [!NOTE]
    > 打开 **资产视图** 页时显示的默认视图取决于 **资产管理参数** 页（**资产管理** \> **设置** \> **资产管理参数**）**资产** 选项卡上 **视图** 字段中选择的值。

页面右侧的快速选项卡显示所选视图的详细信息。

树视图上方显示的痕迹显示树视图中当前选择的内容。 此痕迹使用以下格式：

功能位置 ID/功能位置 ID（如果有多个功能位置）\> 资产 ID/资产 ID（如果有多个资产）- 物料编号。

如果已经在树视图中选择了一个资产，则可选择 **有效请求** 或 **有效工作订单** 查看与资产有关的维护请求或工作订单。 也可以选择 **打开** \> **功能位置**、**资产** 或 **资产 BOM** 以打开相关视图。

可在其中选择资产的任何资产查找中也提供可在 **视图** 字段中选择的 **资产功能位置** 选项。 例如，**资产视图** 选项卡上将显示树视图，可在其中[创建资产](../objects/create-an-object.md)，创建维护请求或创建工作订单。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
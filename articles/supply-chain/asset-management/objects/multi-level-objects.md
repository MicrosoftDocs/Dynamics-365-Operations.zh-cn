---
title: 多级资产
description: 本主题介绍如何创建和删除多级资产。
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fd4da57c3849095909226db53c23b3c25301acdc
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021314"
---
# <a name="multi-level-assets"></a>多级资产

[!include [banner](../../includes/banner.md)]

 

本主题介绍如何创建和删除多级资产。 可以按分层树结构创建资产和关联的子资产。 这样就可以显示资产之间的关系和依赖关系。 可以将维护作业与树结构的所有级别关联。 也可以为单个级别创建统计信息，或作为所有子资产级别的总和创建。

在 **所有资产** 列表页（**资产管理** \> **常用** \> **资产** \> **所有资产**）上，**资产** 列按分层顺序列出资产。 **父级** 列显示关联的父级。 此外，如果已经创建了资产和子资产，则 **相关信息** 窗格中的 **资产树** 部分以树结构的形式显示资产。

有关如何创建资产的详细信息，请参阅[创建资产](../objects/create-an-object.md)。 若要创建子资产，请在 **常规** 快速选项卡上 **父级** 字段中选择父资产。

## <a name="copy-an-asset-or-asset-structure"></a>复制资产或资产结构

如果公司有多个相似资产结构，可使用资产管理中的复制功能快速创建它们。

1. 选择 **资产管理** \> **常用** \> **资产** \> **所有资产**。
2. 在 **所有资产** 列表页，选择要复制的资产。 例如，如果要复制整个资产结构（包括子资产），请选择父资产。
3. 选择 **复制资产**。 在 **复制自** 部分中，**资产** 字段设置为您在列表页选择的资产。
4. 在 **复制到** 部分的 **资产** 字段中，输入新资产的名称。
5. 如果要创建的资产应该是现有资产结构的一部分，请在 **父资产** 部分的 **资产** 字段中选择一个父 ID。
6. 选择 **确定**。 将在 **所有资产** 列表页显示新资产结构。 将把与复制的资产关联的所有资产属性、维护计划和维护阶段转移到新资产或资产结构。

复制资产结构时，新结构中的子资产与复制的子资产同名。 复制过程完成后，可轻松更改资产的名称和其他设置。 在 **所有资产** 列表页选择资产，然后选择 **编辑** 按钮。

> [!NOTE]
> 复制资产或资产结构时，将把新资产的生命周期状态重置为您为资产定义的初始生命周期状态。 将把功能位置重置为默认功能位置。

## <a name="delete-an-asset-or-asset-structure"></a>删除资产或资产结构

如果资产有关联的子资产，则仅当没有为这些资产中的任何一个登记维护请求、工作订单作业、故障登记或条件评估时，才能删除该资产。

1. 在 **所有资产** 列表页，选择要删除的资产。
2. 选择 **删除**。

> [!NOTE]
> 如果不能通过此过程删除资产，另一种处理删除的方法是为此目的设置资产生命周期状态。 例如，可在 **资产生命周期状态** 页设置 **已报废** 或 **已删除** 生命周期状态。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
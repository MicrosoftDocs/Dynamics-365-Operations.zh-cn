---
title: 资产关键性类型
description: 本主题介绍资产管理中的资产关键性类型。
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetCriticality, EntAssetObjectCriticality
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9edf55c22375a66fda04ae7ff76d7a0a191140e5ffb3a377b9ac1a7ba604a8d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776912"
---
# <a name="asset-criticality-types"></a>资产关键性类型

[!include [banner](../../includes/banner.md)]

 

本主题介绍资产管理中的资产关键性类型。 资产关键性与资产关联，并转移到工作订单。 不能在工作订单中更改。 资产关键性用于在计划工作订单时计算工作订单关键性。 换句话说，用于计算资产的维护作业对公司中的生产计划和生产效率的影响程度。 有关与计算工作订单排产的等级评分关联的设置的详细信息，请参阅[资产管理参数](../setup-for-objects/enterprise-asset-management-parameters.md)。

若要设置关键性，首先创建资产设置中应该使用的关键性类型。 然后设置资产关键性。

## <a name="set-up-criticality-types"></a>设置关键性类型

1. 选择 **资产管理** \> **设置** \> **资产** \> **关键性类型**。
2. 选择 **新建** 创建记录。
3. 在 **关键性** 字段中，输入用于表示关键性的数字。
4. 在 **名称** 字段中，输入关键性类型的名称。
5. 在 **系数** 字段中，输入一个系数。 此系数在计算工作订单排产时用于确定应使用的关键性记录。 （始终使用系数最大的记录。）如果创建的关键性行具有相同的关键性值（如下图所示），则此设置相关。

    ![关键性类型页面。](media/23-setup-for-objects.png)

## <a name="set-up-asset-criticalities"></a>设置资产关键性

1. 选择 **资产管理** \> **设置** \> **资产关键性**。
2. 选择 **新建** 创建记录。
3. 根据所需的资产关键性详细信息级别，在 **功能位置**、**资产类型**、**制造商**、**模型**、**资产**、**作业类型类别**、**作业类型**、**作业类型变体** 和 **作业要求** 字段中进行相关选择。

    > [!NOTE]
    > 选择资产关键性之后，资产管理将检查所有资产关键性记录以查找可能的匹配项。 始终先检查最具体的组合。 换句话说，资产管理首先检查 **作业要求**。 如果未找到匹配项，将检查 **作业类型变体**。 如果未找到匹配项，将检查 **作业类型变体**，依此类推。 如页面布局中显示，此行为表示为了找到最具体的组合，资产管理从右到左检查每个记录以查找匹配项。 如果未找到匹配项，将使用无可供选择的内容的"默认"记录。

4. 在 **关键性** 字段中，选择在上一个过程中创建的一个关键性值。

### <a name="notes-about-criticality-setup"></a>有关关键性设置的说明

- 如果在此设置中更改已在工作订单中使用过的资产关键性，将不会相应更新工作订单中的关键性。
- 只要在工作订单中添加或删除工作订单行，都将重新计算该工作订单中的关键性。
- 如果一个工作订单中包含多个工作订单作业，则始终在工作订单中使用根据 **关键性类型** 页上的 **系数** 字段的最高关键性。
- 资产关键性通常会随时间改变。 购买新设备，补货等可能会影响关键性。 请考虑定期（如每年或每隔一年一次）重新评估资产关键性，以确保关键性定义与当前生产设置匹配。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
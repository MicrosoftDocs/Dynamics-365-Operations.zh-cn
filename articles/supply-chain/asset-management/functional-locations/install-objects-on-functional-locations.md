---
title: 在功能位置安装资产
description: 本主题介绍如何在资产管理中在功能位置安装资产。
author: josaw1
manager: tfehr
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationObjectChange, EntAssetFunctionalLocationObjectInstall, EntAssetFunctionalLocationObject
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ea67e2392d8e25a2a5f3cb7e1ff5032322f2c48
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022022"
---
# <a name="install-assets-on-functional-locations"></a>在功能位置安装资产

[!include [banner](../../includes/banner.md)]

 

创建功能位置结构之后，下一步是在相关功能位置安装资产。 本主题介绍如何在资产管理中在这些功能位置安装资产。 有关如何创建资产的详细信息，请参阅[资产简介](../objects/introduction-to-objects.md)。

如果已创建了资产结构，则必须将整个资产结构安装到功能位置。 因此，只能在功能位置选择父资产（即无父资产的顶级资产）。 还会将所有相关子资产安装到功能位置。 在功能位置安装资产时，可能会将功能位置的财务维度自动传输到这些资产，具体取决于为功能位置选择的功能位置类型的设置。 有关如何设置功能位置类型的详细信息，请参阅[功能位置类型](../setup-for-functional-locations/functional-location-types.md)。

> [!NOTE]
> 可以为用于功能位置的功能位置类型设置资产类型。 在此情况下，在功能位置安装资产时，该功能位置可安装的资产的列表中将仅显示具有相同资产类型的父资产。

在功能位置安装资产之后，可以根据需要替换父资产或资产结构。 就像在安装资产时一样，只能选择替换父资产。 也将替换所有相关子资产。 


## <a name="install-an-asset-structure-on-a-functional-location"></a>在功能位置安装资产结构

1. 选择 **资产管理** \> **常用** \> **功能位置** \> **所有功能位置** 或 **有效功能位置**。
2. 选择要安装资产的功能位置。
3. 选择 **安装资产**。

    **属性** 部分显示对为功能位置选择的功能位置类型设置的资产属性要求的列表。 这些属性仅供参考。 系统不会针对为要安装的资产设置的资产属性验证属性。 在 **资产** 字段中选择资产之后，必须执行此项验证。

4. 在 **资产** 字段中，选择要安装的父资产。 安装中将自动包含所有相关子资产。

    资产列表右侧的 **资产属性** 部分显示与所选资产有关的资产属性。

5. 在 **生效** 字段中，选择资产安装的生效日期和时间。 该日期和时间之后，将把资产和相关子资产的成本与功能位置关联。

    > [!NOTE]
    > 将把为资产设置的资产属性添加到 **属性** 部分。 例如，**重量** 属性要求已同时添加为资产和功能位置的要求。 如果资产与功能位置具有相同类型的属性要求，则将在 **值** 字段中输入资产的属性要求值。 因此，可针对为功能位置设置的属性要求验证资产值。 将使用选中标记来标记为功能位置设置的属性要求。

6. 选择 **确定**。

    > [!NOTE]
    > 若要通过将资产安装到新功能位置来更改该资产的安装，请执行此过程的步骤 1 到 6。 如果资产安装到新功能位置，将从上一个功能位置自动卸载该资产。 **不会** 将资产安装到新功能位置之前为该资产创建的所有有效维护请求或工作订单自动传输到新功能位置。 如果资产仍然需要这些维护请求和工作订单，必须在将资产安装到新位置之后重新创建它们。

7. 若要查看功能位置安装的所有资产的列表（包括子资产），请在 **所有功能位置** 页选择该功能位置，然后选择 **资产**。
8. 若要查看与功能位置安装的资产关联的有效维护请求、有效工作订单或故障登记的列表，请在 **所有功能位置** 页选择该功能位置，然后选择 **请求**、**工作订单** 或 **故障**。

> [!NOTE]
> 如果更改了与资产有关的数据，也会在安装该资产的功能位置自动更新这些数据。 此项自动更新与对维护请求、工作订单、资产故障登记、维护停机时间登记和资产度量登记的更改有关。

## <a name="automatically-create-one-asset-on-a-functional-location"></a>在功能位置自动创建一个资产

可设置功能位置阶段和功能位置类型，以便处理功能位置 *一个* 资产的自动创建。 该资产获取的 ID 和名称与功能位置的相同。 处理对大型静态资产（如建筑物）的维护时，此功能可能非常有用。

必须有以下设置数据，才能在功能位置自动创建资产。

- 创建功能位置类型以处理资产的自动创建。 在 **资产类型** 字段中，选择资产类型。 有关详细信息，请参阅[功能位置类型](../setup-for-functional-locations/functional-location-types.md)。
- 创建功能位置生命周期状态以处理资产的自动创建。 将 **创建资产** 选项设置为 **是**。 有关详细信息，请参阅[功能位置生命周期状态](../setup-for-functional-locations/functional-location-stages.md)。

有设置数据之后，即可创建资产。

1. 在 **所有功能位置** 页中，确保要自动创建资产的功能位置使用您为此目的创建的功能位置类型。
2. 在列表中选择功能位置。
3. 选择 **更新功能位置状态**，然后选择为此目的创建的生命周期状态。 现在将在该功能位置自动安装一个资产。 该资产与功能位置同名。

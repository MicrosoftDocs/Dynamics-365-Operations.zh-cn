---
title: 功能位置生命周期状态
description: 本主题介绍如何在资产管理中设置功能位置状态和生命周期模型。
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationLifecycleModel, EntAssetFunctionalLocationLifecycleState
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f119e68319b901b052fa4aa659260f386f44bcf
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021259"
---
# <a name="functional-location-lifecycle-states"></a>功能位置生命周期状态

[!include [banner](../../includes/banner.md)]

 

本主题介绍如何在资产管理中设置功能位置生命周期状态和生命周期模型。 功能位置生命周期状态定义功能位置可以经历的状态，如已创建、有效和已结束。 无论功能位置处于哪种生命周期状态，您都可以在 **所有功能位置** 列表页中查看所有功能位置。 可以更改功能位置的状态，方法是在 **所有功能位置** 列表页中选择功能位置，然后选择 **更新功能位置状态**。

## <a name="set-up-functional-location-lifecycle-states"></a>设置功能位置生命周期状态

1. 选择 **资产管理** > **设置** > **功能位置** > **生命周期状态**。
2. 选择 **新建** 创建新的功能位置状态。
3. 在 **生命周期状态** 字段中插入状态 ID，在 **名称** 字段中插入功能位置状态的名称。 在 **生命周期模型** 字段中，可查看使用该功能位置状态的功能位置生命周期模型的数量。
4. 如果在此状态时功能位置应有效，请在 **常规** 快速选项卡的 **有效** 切换按钮上选择“是”。
5. 如果应该可以在此状态时自动创建与功能位置同名的资产并安装到这个功能位置，请在 **创建资产** 切换按钮上选择“是”。  
>[!NOTE]
>此切换按钮与 **功能位置类型** 窗体（**资产管理** > **设置** > **功能位置** > **功能位置类型**）中 **常规** 快速选项卡上的 **资产类型** 字段关联。
6. 如果应该可以在此状态更改功能位置的名称，请在 **重命名位置** 切换按钮上选择“是”。
7. 如果应该可以在此状态向功能位置添加新的子位置，请在 **新建子位置** 切换按钮上选择“是”。
8. 如果应该可以在此状态在功能位置安装资产，请在 **安装资产** 切换按钮上选择“是”。
9. 如果应该可以在此状态删除功能位置，请在 **删除功能位置** 切换按钮上选择“是”。
10. 如果希望在此状态自动更新在功能位置安装的所有支持的资产生命周期状态，请在 **生命周期状态** 字段中选择资产状态。 示例：如果关闭一个功能位置，然后将该功能位置的生命周期状态设置为“已结束”，您可能希望将在该功能位置安装的资产的生命周期状态更改为“未在使用中”。


>[!NOTE]
>功能位置生命周期状态、生命周期模型和类型与工作订单生命周期状态、工作订单生命周期模型和工作订单类型的关联方法和使用方法相同。 

## <a name="set-up-functional-location-lifecycle-models"></a>设置功能位置生命周期模型

创建功能位置所需生命周期状态之后，可将这些状态拆分为组。 目的是创建可用于不同类型功能位置的生命周期模型流。 至少应创建一个标准功能位置生命周期模型。

1. 选择 **资产管理** > **设置** > **功能位置** > **生命周期模型**。
2. 选择 **新建** 以创建新的生命周期模型。
3. 在 **生命周期模型** 字段中插入生命周期模型 ID，在 **名称** 字段中插入生命周期模型的名称。 在 **功能位置类型** 和 **生命周期状态** 字段中，可查看使用该生命周期模型的功能位置类型数量和生命周期模型中选择的状态数量。
4. 在 **生命周期状态** 快速选项卡上，选择模型中应包含的状态。 方法是单击 **其余生命周期状态** 部分中的状态，然后单击 ![前进箭头](media/02-setup-for-functional-locations.png) 按钮。
5. 如果要为模型选择所有可用状态，请单击![选择所有可用阶段](media/03-setup-for-functional-locations.png)按钮。 将把所有状态移到 **所选生命周期状态** 部分。
6. 如果要从模型删除所选状态，请在 **所选生命周期状态** 部分中选择状态，然后单击 ![后退箭头](media/04-setup-for-functional-locations.png) 按钮。
7. 要定义哪些生命周期状态可采用所选状态，选择 **生命周期状态更新**。

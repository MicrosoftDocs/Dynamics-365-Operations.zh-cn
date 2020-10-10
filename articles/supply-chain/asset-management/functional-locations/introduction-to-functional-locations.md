---
title: 功能位置简介
description: 本主题概述资产管理中的功能位置。
author: josaw1
manager: tfehr
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationEditSubLocations, EntAssetFunctionalLocationLookup, EntAssetFunctionalLocationRename, EntAssetFunctionalLocation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80ea318d750f1ef18f270fa246ab54ecb63aa790
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888820"
---
# <a name="introduction-to-functional-locations"></a>功能位置简介

[!include [banner](../../includes/banner.md)]

 

本主题概述资产管理中的功能位置。 功能位置是技术结构中的元素，如系统中的功能单元。 功能位置以层次结构的方式创建，可以在其中安装资产。 公司中的功能位置设置取决于公司的要求。

下面是一些如何使用功能位置的示例：

- **功能** – 功能位置面向用户，用于管理具有相似行为的资产。
- **流程相关** – 功能位置面向工作流。
- **空间** – 功能位置表示地理位置或地点。

每个功能位置在资产管理中独立管理。 下面是功能位置的一些有用的功能：

- 设置功能位置规范。
- 设置资产规范要求。
- 为预防性和反应性维护设置维护顺序
- 管理安装的资产。
- 跟踪有效请求和与所安装资产关联的工作订单。
- 跟踪为资产登记的故障。
- 跟踪与功能位置关联的资产在指定时间的维护成本。

功能位置可用于跟踪与请求、工作订单、故障登记、条件评估、生产停止登记和资产计数器登记有关的资产。

> [!NOTE]
> 即使资产在其生命周期内安装在多个功能位置，成本也可以与每个位置关联。 换句话说，资产成本始终与指定时间安装资产的功能位置关联。

功能位置**不**具备灵活性。 因此，设置功能位置层次结构之后，不能在其中移动位置。 

创建功能位置层次结构之后，下一步是在其中安装资产。 有关详细信息，请参阅[在功能位置安装资产](../functional-locations/install-objects-on-functional-locations.md)。

## <a name="all-functional-locations"></a>所有功能位置

选择**资产管理** \> **常用** \> **功能位置** \> **所有功能位置**以打开**所有功能位置**列表页。 此页显示所有功能位置和与每个功能位置有关的信息。 若要仅查看有效功能位置，请选择**有效功能位置**。 若要仅查看在您作为工人关联到的功能位置，请选择**我的有效功能位置**。 （此项关联在**工人**页设置。 有关详细信息，请参阅[维护工人和工人组](../setup-for-objects/workers-and-worker-groups.md)。）

在**所有功能位置**列表页中的**功能位置**列选择链接可查看所选记录的详细信息。 若要编辑功能位置，请选择**编辑**按钮。 这个详细信息视图显示与位置有关的详细信息。 右侧有一个**相关信息**窗格。 此窗格显示功能位置层次结构。 可展开和折叠**相关信息**窗格。

操作窗格上的按钮排列在选项卡上。 下表简述与资产管理有关的按钮。

| 按钮名称                         | 说明                                                                                                                                  |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 编辑​​                                | 在页面的编辑模式和查看模式之间切换。                                                                                         |
| 新                                 | 创建新的功能位置。                                                                                                            |
| 删除                              | 删除所选功能位置。                                                                                                     |
| 重命名                              | 重命名所选功能位置。                                                                                                     |
| 复制功能位置结构  | 复制功能位置层次结构。                                                                                                      |
| 安装资产                       | 在功能位置安装资产，包括子资产。                                                                        |
| 替换资产                       | 将资产层次结构替换为功能位置中的另一个资产层次结构。                                                         |
| 成本控制                        | 打开**功能位置成本控制**页，可在其中计算所选功能位置的成本。                |
| 工时控制                        | 打开**功能位置工时控制**页，可在其中计算所选功能位置的成本。                |
| 资产                              | 打开**所有资产**页，可在其中查看与所选功能位置关联的资产的列表。                      |
| 请求                            | 打开**有效请求**页，可在其中查看与所选功能位置关联的请求的列表。               |
| 工作订单                         | 打开**有效工作订单**页，可在其中查看与所选功能位置关联的工作订单的列表。         |
| 故障                              | 打开**资产故障**页，可在其中查看与所选功能位置关联的资产故障登记的列表。 |
| 更新功能位置状态    | 更新所选功能位置的阶段。                                                                                        |
| 生命周期状态日志                 | 查看日志，其中显示所选功能位置的阶段。                                                                        |

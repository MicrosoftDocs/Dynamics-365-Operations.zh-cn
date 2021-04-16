---
title: 条件评估
description: 本主题介绍如何在资产管理中为资产创建条件评估模板和登记。
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectCondition, EntAssetConditionTemplate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 082a2bfd8818e511095e9ab2dcc22de59eb98d31
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808416"
---
# <a name="condition-assessment"></a>条件评估

[!include [banner](../../includes/banner.md)]

 

本主题介绍如何在资产管理中为资产创建条件评估模板和登记。 条件评估定期执行，主要目的是为资产创建和维护条件数据。 从预防性维护角度来看，监视当前条件和剩余寿命之类关键信息至关重要。 此外，如果定期执行评估，就可以监控和比较工厂内的机器条件。

条件评估可用于度量和监控设备的各种条件。 示例：可以度量机器的振动。 在资产管理中为各种设备登记了振动度量之后，可以搜索最近登记的评估和查看振动度量。

条件评估是为资产创建的。 请在执行条件评估过程之前为资产类型设置条件评估模板。 之所以为条件评估使用模板，是为了避免相似资产的条件数据变更。 在资产管理中设置和使用条件评估的顺序为：首先设置所需条件评估模板。 接下来在 **资产类型** 窗体中将模板与资产类型关联。 最后可以在 **资产** 窗体中为资产创建条件评估模板登记。

## <a name="create-a-condition-assessment-template"></a>创建条件评估模板

1. 选择 **资产管理** > **设置** > **资产类型** > **条件评估**。
2. 选择 **新建** 以创建新模板。
3. 在 **模板** 字段中插入模板的 ID。
4. 在 **名称** 字段中插入模板的名称。
5. 在 **条件评估行** 快速选项卡上，添加条件评估所需行，包括选择相应条件类型和度量单位。
6. 在 **资产类型** 快速选项卡上，添加应该使用条件评估模板的资产类型。
7. 在屏幕顶部 **详细信息** 组中的 **行** 和 **资产类型** 字段中，可以看到与所选条件评估模板关联的评估行和评估类型的数量。


## <a name="create-condition-assessment-registration-on-an-asset"></a>为资产创建条件评估登记

1. 选择 **资产管理** > **常用** > **资产** > **所有资产**。
2. 在列表中，选择要为其创建条件评估登记的资产。
3. 在 **常规** 选项卡上，单击 **条件评估**。
4. 单击 **新建** 创建新的登记。
5. 在 **日期** 字段中选择条件评估的日期。
6. 在 **工人** 字段中选择执行评估登记的工人的姓名。
7. 在 **行** 字段中，可以查看为条件评估设置的评估行数量。
8. 在 **模板** 字段中选择条件评估的模板。 将在 **名称** 字段中自动插入模板的名称，在 **条件评估行** 快速选项卡上插入关联的登记行。
9. 可在 **注释** 快速选项卡上插入与所选条件评估有关的注释。
10. 在 **值** 字段中插入每个条件评估行的度量数据。
11. 可在 **条件评估行** 快速选项卡 > **注释** 字段中插入与所选登记行有关的注释。 如果添加有关行的注释，将自动选中 **注释** 复选框。

为资产创建条件评估登记之后，可以打印条件评估报告。

>[!NOTE]
>也可以为工作订单登记条件评估（**资产管理** > **常用** > **工作订单** > **所有工作订单** > **条件评估** 按钮）。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
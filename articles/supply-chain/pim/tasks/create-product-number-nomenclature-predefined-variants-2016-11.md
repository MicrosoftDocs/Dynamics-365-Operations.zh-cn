---
title: 为预定义的产品变型创建产品编号命名法
description: 本主题介绍如何为预定义的产品变型设置产品编号命名法，以及如何将其分配给适当的产品维度组。
author: ShylaThompson
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6871765a450295a3f308ec7e706f1b126071585f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4422994"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a>为预定义的产品变型创建产品编号命名法

[!include [banner](../../includes/banner.md)]

本主题介绍如何为预定义的产品变型设置产品编号命名法，以及如何将其分配给适当的产品维度组。 创建此程序的演示数据公司是 USMF。 将为“颜色和大小”产品维度组分配新产品编号命名法。 此任务通常由产品设计师完成。


## <a name="create-a-product-number-nomenclature"></a>创建产品编号命名法
1. 选择 **产品变型定义**。
2. 选择 **产品命名法**。
3. 选择 **新建**。
4. 在 **名称** 字段中，输入可帮助识别目标产品维度组的命名法名称，如 `ColorSize`。
5. 在 **描述** 字段中，键入一个值。
6. 选择 **添加**。
7. 选择 **基础产品** 编号。
8. 选择 **添加**。
9. 选择 **文本常量**。
10. 在 **文本** 字段中，键入一个值。
11. 选择 **添加**。
12. 选择 **颜色**。
13. 选择 **添加**。
14. 选择 **文本常量**。
15. 在 **文本** 字段中，键入一个值。
16. 选择 **添加**。
17. 选择 **大小**。
18. 关闭该页面。

## <a name="assign-the-nomenclature-to-a-product-master"></a>为基础产品分配命名法
1. 选择 **产品维度组**。
2. 选择 **SizeCol 产品维度组**。
3. 选择 **编辑**。
4. 在 **使用命名法** 字段中选择 **是**。
5. 在 **产品变型编号命名法** 字段中，输入或选择一个值。
6. 关闭该页面。


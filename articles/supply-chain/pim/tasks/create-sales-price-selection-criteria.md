---
title: 创建销售价选择条件
description: 此过程显示如何为基于属性的销售价模型创建销售价选择条件。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 69d22c3321beaa2667ee20bff00acd746714b993
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920523"
---
# <a name="create-sales-price-selection-criteria"></a>创建销售价选择条件

[!include [banner](../../includes/banner.md)]

此过程显示如何为基于属性的销售价模型创建销售价选择条件。 此过程要求至少有一个销售价模型可用。 此示例使用 USMF 演示数据公司中的扬声器解决方案销售价模型的价格模型。 通常，产品经理使用此过程。

## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>为现有销售价模型添加新条件

1. 转到 **产品信息管理 \> 产品 \> 产品配置模型**。
1. 在此列表中，选择扬声器解决方案产品模型的行，但是不选择模型名称的链接。
1. 在操作窗格上，选择 **模型**。
1. 选择 **价格模型条件**。
1. 选择 **新建**。
1. 在 **名称** 字段中，键入“客户组 10”。
    * 价格模型条件的名称用于帮助识别基础选择条件。  
1. 在 **价格模型** 字段中，输入或选择一个值。
1. 在 **订单类型** 字段中选择 *销售订单*。
    * 订单类型确定将可用于选择查询的数据库字段。  
1. 在 **生效日期** 字段中输入日期。
1. 在 **到期日期** 字段中输入日期。
1. 选择 **保存**。

## <a name="create-the-query-for-the-selection-criteria"></a>为选择条件创建查询

1. 选择 **编辑**。
2. 在 **表** 字段中，选择 *客户*。
3. 在 **字段** 字段中，选择 *客户组*。
    * 在此示例中，我们为选择条件使用特定客户组。  
4. 在 **条件** 字段中，选择 *客户组 10*。
5. 选择 **确定**。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
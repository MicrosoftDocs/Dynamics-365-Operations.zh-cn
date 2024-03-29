---
title: 创建销售价选择条件
description: 此过程显示如何为基于属性的销售价模型创建销售价选择条件。
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ed7083f289948033782f74dd9ed1b3c2d2a73aea
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568439"
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
---
title: 创建基于维度的基础产品的物料清单
description: 对于此过程，您应该已经以八个记录的这个顺序完成之前的 4 个指南。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 696cb96c6e934eaa44bfe6f51347df4541e5648f75f1ce07139787a1b235d69d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6715763"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a>创建基于维度的基础产品的物料清单

[!include [banner](../../includes/banner.md)]

对于此过程，您应该已经以八个记录的这个顺序完成之前的 4 个指南。 前 4 个记录设置完成此过程需要的数据。 创建此程序的演示数据公司是 USMF。 此任务通常由产品设计器处理。

## <a name="select-the-product"></a>选择产品

1. 转到 **产品信息管理 \> 产品 \> 已发布产品**。
1. 在列表中，标记所选的行。
    * 使用您以此顺序在第一个任务指南中创建的基于维度的配置技术查找发布的基础产品。  
1. 在操作窗格上，选择 **工程师**。
1. 选择 **物料清单版本**。

## <a name="create-new-bom-and-bom-version"></a>创建新的物料清单和物料清单版本

1. 选择 **新建**。
1. 选择 **物料清单和物料清单版本**。
1. 在 **名称** 字段中，键入一个值。
    * 设置站点  
    * 在此过程中，我们不设置物料清单的特定站点。  
1. 选择 **确定**。
1. 选择 **新建**。
    * 在此过程中，我们将添加四行到物料清单。 两行表示电缆选项，两行表示机柜选项。  
1. 在列表中，标记所选的行。
1. 在 **物料编号** 字段中，输入或选择一个值。
    * 选择物料编号 A0001，HDMI 6' 电缆。  
1. 在 **配置组** 字段中，输入或选择一个值。
    * 选择以此顺序在指南 4 中创建的电缆配置组。  
1. 选择 **新建**。
    * 选择物料编号 A0002，HDMI 12' 电缆。  
1. 在列表中，标记所选的行。
1. 在 **物料编号** 字段中，输入或选择一个值。
1. 在 **配置组** 字段中，输入或选择一个值。
    * 再次选择电缆配置组。  
1. 选择 **新建**。
1. 在列表中，标记所选的行。
1. 在 **物料编号** 字段中，输入或选择一个值。
    * 选择物料编号 D0002 机柜。  
1. 在 **配置组** 字段中，输入或选择一个值。
    * 选择此物料清单行的机柜配置组。  
1. 选择 **新建**。
1. 在列表中，标记所选的行。
1. 在 **物料编号** 字段中，输入或选择一个值。
    * 选择物料编号 M0007 StandardCabinet 作为最后的物料清单行。  
1. 在 **配置组** 字段中，输入或选择一个值。
    * 选择最后物料清单行的机柜配置组。  

## <a name="approve-and-activate"></a>审核并启用

1. 关闭该页面。
1. 选择 **审核**。
1. 在 **审核人** 字段中，输入或选择一个值。
1. 在 **是否还要审核该物料清单?** 字段中选择 *是*。
1. 选择 **确定**。
1. 选择 **激活**。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
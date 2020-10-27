---
title: 创建基于维度的基础产品的物料清单
description: 对于此过程，您应该已经以八个记录的这个顺序完成之前的 4 个指南。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e7961cfb4ad0e20c49d327d83f56c08811598ac1
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986279"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a>创建基于维度的基础产品的物料清单

[!include [banner](../../includes/banner.md)]

对于此过程，您应该已经以八个记录的这个顺序完成之前的 4 个指南。 前 4 个记录设置完成此过程需要的数据。 创建此程序的演示数据公司是 USMF。 此任务通常由产品设计器处理。


## <a name="select-the-product"></a>选择产品
1. 单击“已发布产品的维护”。
2. 单击“已发布产品”。
3. 在列表中，标记所选的行。
    * 使用您以此顺序在第一个任务指南中创建的基于维度的配置技术查找发布的基础产品。  
4. 在“操作”窗格上，单击“设计”。
5. 单击“物料清单版本”。

## <a name="create-new-bom-and-bom-version"></a>创建新的物料清单和物料清单版本
1. 单击“新建”。
2. 单击“物料清单”和“物料清单版本”。
3. 在“名称”字段中，键入一个值。
    * 设置站点  
    * 在此过程中，我们不设置物料清单的特定站点。  
4. 单击“确定”。
5. 单击“新建”。
    * 在此过程中，我们将添加四行到物料清单。 两行表示电缆选项，两行表示机柜选项。  
6. 在列表中，标记所选的行。
7. 在“物料编号”字段中，输入或选择一个值。
    * 选择物料编号 A0001，HDMI 6' 电缆。  
8. 在“配置组”字段中，输入或选择一个值。
    * 选择以此顺序在指南 4 中创建的电缆配置组。  
9. 单击“新建”。
    * 选择物料编号 A0002，HDMI 12' 电缆。  
10. 在列表中，标记所选的行。
11. 在“物料编号”字段中，输入或选择一个值。
12. 在“配置组”字段中，输入或选择一个值。
    * 再次选择电缆配置组。  
13. 单击“新建”。
14. 在列表中，标记所选的行。
15. 在“物料编号”字段中，输入或选择一个值。
    * 选择物料编号 D0002 机柜。  
16. 在“配置组”字段中，输入或选择一个值。
    * 选择此物料清单行的机柜配置组。  
17. 单击“新建”。
18. 在列表中，标记所选的行。
19. 在“物料编号”字段中，输入或选择一个值。
    * 选择物料编号 M0007 StandardCabinet 作为最后的物料清单行。  
20. 在“配置组”字段中，输入或选择一个值。
    * 选择最后物料清单行的机柜配置组。  

## <a name="approve-and-activate"></a>审核并启用
1. 关闭该页面。
2. 单击“审核”。
3. 在“已审核”字段中，输入或选择一个值。
4. 在“是否还要审核该物料清单？”字段中选择“是”。
5. 单击“确定”。
6. 单击“启用”。


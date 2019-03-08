---
title: 维护产品配置模型的物料清单
description: 运行该过程要求有现有的产品配置模型。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 457aa5720919d8455a3099b200980bb36f60577f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "342377"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a>维护产品配置模型的物料清单

[!include [task guide banner](../../includes/task-guide-banner.md)]

运行该过程要求有现有的产品配置模型。 该过程使用演示公司 USMF 的“高端扬声器模型”创建。


## <a name="add-a-bom-line"></a>添加物料清单行
1. 单击“产品变型模型定义”。
2. 单击“产品配置模型”。
3. 在列表中，找到并选择所需记录。
    * 为该过程选择“高端扬声器”。  
4. 在列表中，单击所选行中的链接。
5. 展开“物料清单行”部分。
6. 单击“添加”。
7. 在“名称”字段中，键入一个值。
8. 在“描述”字段中，键入一个值。
9. 单击“保存”。

## <a name="add-bom-line-details"></a>添加物料清单行详细信息
1. 单击“物料清单行详细信息”。
2. 在“物料编号”字段中，输入或选择一个值。
    * 例如，可以选择物料 M0055。  
    * 对于每个物料清单行属性，您可以选择是否带固定值或映射到属性中。  
3. 选择“设置”复选框。
4. 在“计算”字段中选择“是”。
    * 设置“计算”属性为“是”，确保物料清单行包括在成本计算中。  
5. 单击“设置”选项卡。
6. 选择“设置”复选框。
7. 在“数量”字段中，输入一个数字。
    * 数量字段确定物料清单中包含的物料数。 这可能为属性映射的明显候选项。  
8. 单击“维度”选项卡。
    * 核实产品维度是否有效，因此必须有分配的值或属性。  
9. 单击“确定”。


---
title: 维护产品配置模型的物料清单
description: 运行该过程要求有现有的产品配置模型。
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd78b06f10d0c9b1df57dacdd824b06ebe414b3b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577280"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a>维护产品配置模型的物料清单

[!include [banner](../../includes/banner.md)]

运行该过程要求有现有的产品配置模型。 该过程使用演示公司 USMF 的“高端扬声器模型”创建。

## <a name="add-a-bom-line"></a>添加物料清单行

1. 转到 **产品信息管理 \> 产品 \> 产品配置模型**。
1. 在列表中，找到并选择所需记录。
    * 为该过程选择“高端扬声器”。  
1. 在列表中，选择所选择行中的链接。
1. 展开 **物料清单行** 部分。
1. 选择 **添加**。
1. 在 **名称** 字段中，键入一个值。
1. 在 **描述** 字段中，键入一个值。
1. 选择 **保存**。

## <a name="add-bom-line-details"></a>添加物料清单行详细信息

1. 选择 **物料清单行详细信息**。
2. 在 **物料编号** 字段中，输入或选择一个值。
    * 例如，可以选择物料 M0055。  
    * 对于每个物料清单行属性，您可以选择是否带固定值或映射到属性中。  
3. 选择 **设置** 复选框。
4. 在 **计算** 字段中选择 *是*。
    * 将 **计算** 属性设置为 *是*，确保物料清单行包括在成本计算中。  
5. 选择 **设置** 选项卡。
6. 选择 **设置** 复选框。
7. 在 **数量** 字段中，输入一个数字。
    * 数量字段确定物料清单中包含的物料数。 这可能为属性映射的明显候选项。  
8. 选择 **维度** 选项卡。
    * 核实产品维度是否有效，因此必须有分配的值或属性。  
9. 选择 **确定**。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
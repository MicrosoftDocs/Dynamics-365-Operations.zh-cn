---
title: 设置集装化
description: 本主题描述如何在“仓库管理”中自动进行装载集装化。
author: ShylaThompson
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable, WHSContainerizatonHistory, WHSContainerPackingPolicyChange, WHSManifestShipmentContainers, WHSAllowedContainerTypeGroup, WHSPostMethod, WHSContainerCreateDialog, WHSContainerCloseDiag, WHSContainer
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1f961dc379ceeeae9bbceec1baaa9b9be21316f3
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4423329"
---
# <a name="set-up-containerization"></a>设置集装化

[!include [banner](../../includes/banner.md)]

本主题描述如何在“仓库管理”中自动进行装载集装化。 自动执行集装化在处理波次，且工作行可以分解为适合集装箱的数量时，创建集装箱和用于装运的领料工作。 这有助于仓库工作人员将物料直接拣选到选择的集装箱内。 与手动包装流程对比，创建集装箱、分配物料和封闭集装箱等任务由系统自动执行。 此过程使用 USMF 演示公司，并由仓库经理执行。


## <a name="set-up-a-wave-template"></a>设置波次模板
1. 在导航窗格中，转到 **模块 > 仓库管理 > 设置 > 波次 > 波次模板**。
2. 选择 **新建**。
3. 在 **波次模板名称** 字段中，键入一个值。
4. 在 **波次模板描述** 字段中，键入一个值。
5. 在 **站点** 字段中，输入或选择一个值。
6. 在 **仓库** 字段中，输入或选择一个值。
7. 展开 **方法** 部分。 **已选定方法** 窗格列出了所选波模板类型的方法。 波次模板必须包括集装化方法。  
8. 在 **波次步骤代码** 字段中，键入一个值。 键入添加方法的一个波次步骤代码，可以是任意代码。 可以多次添加方法，并分配不同的波次步骤代码。 为此，在 **波次流程方法** 页上选择 **对此方法可重复**。  
9. 选择 **保存**。
10. 关闭该页面。

## <a name="set-up-a-container-type"></a>设置集装箱类型
1. 在导航窗格中，转到 **模块 > 仓库管理 > 设置 > 集装箱 > 集装箱类型**。 您可以在 **集装箱类型** 页定义您的集装箱。 您可以配置集装箱的物理维度，包括皮重、最大重量、最大体积、长度、宽度和高度。 在此示例中，我们有三种不同的箱尺寸。  
2. 选择 **新建**。
3. 在 **集装箱类型代码** 字段中，键入一个值。
4. 在 **皮重** 字段中，输入一个数字。
5. 在 **最大重量** 字段中，输入一个数字。
6. 在 **体积** 字段中，输入一个数字。
7. 在 **长度** 字段中，输入一个数字。
8. 在 **宽度** 字段中输入数字。
9. 在 **高度** 字段中输入数字。
10. 在 **描述** 字段中，键入一个值。
11. 选择 **保存**。
13. 再重复执行步骤 2-11 两次，以便创建总计三个集装箱类型。
14. 关闭该页面。

## <a name="set-up-a-container-group"></a>设置集装箱组
1. 在导航窗格中，转到 **模块 > 仓库管理 > 设置 > 集装箱 > 集装箱组**。
2. 在操作窗格上，选择 **新建**。 可以设置集装箱类型的逻辑组。 对于每个组，可以指定集装箱包装和集装箱填充百分比的序列。物料的尺寸维度用于决定其在集装箱中是否合适。 使用最接近物料尺寸维度的集装箱。 如果在组中有多个集装箱类型，我们建议您按尺寸排列顺序，因此最大的集装箱在序列中排第一，编号为 1，最小的集装箱排最后。    
3. 在 **集装箱组 ID** 字段中，键入您之前创建的值。
4. 在 **描述** 字段中，键入一个值。
5. 对前面创建的所有三个集装箱类型重复执行步骤 2-4。
6. 选择 **保存**。
7. 关闭该页面。

## <a name="set-up-a-container-build-template"></a>设置集装箱生成模板
1. 在导航窗格中，转到 **模块 > 仓库管理 > 设置 > 集装箱 > 集装箱生成模板**。
2. 选择 **新建**。 集装箱生成模板基于执行的集装化流程。 每个集装箱生成模板定义波次模板将使用的一个集装化流程。 **编辑查询** 选项允许您定义将处理所选模板的条件。 例如，您可能想要只运行特定客户、产品或者仓库的集装化，或您可以添加相应查询范围到该模板。 **波次步骤代码** 字段是集装箱生成模板如何与波次模板中的步骤关联。 在执行波次时，它确定哪些集装箱生成模板用于启用集装化。 “基本查询类型”字段确定包装内容和筛选器查询的基础。 
3. 在 **集装箱模板 ID** 字段中，键入一个值。
4. 在 **集装箱组 ID** 字段中，输入或选择一个值。
5. 在 **波次步骤代码** 字段中，键入一个值。
6. 选中 **允许拆分领料** 复选框。
7. 选择 **保存**。
8. 选择 **集装箱混合约束**。 混合逻辑分隔符允许您为集装箱内的包装分配行设置规则。 例如，如果您添加 **物料编号字段**，物料分配给集装箱，在存在新的物料编号时将创建新集装箱。 这将阻止工作人员在同一个集装箱中包装两个不同客户的分配行。  
9. 选择 **新建**。
10. 在 **表** 字段中，选择一个选项。
11. 在 **字段选择** 字段中，输入或选择一个值。
12. 选择 **确定**。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: 设置登记已接收物料的移动设备菜单项
description: 本文重点介绍设置移动设备菜单项。
author: Mirzaab
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFMenu, WHSRFDefaultData
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b59a78ef98215bec7610fe17ed56e6fc287004c0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882306"
---
# <a name="set-up-a-mobile-device-menu-item-to-register-received-items"></a>设置登记已接收物料的移动设备菜单项

[!include [banner](../../includes/banner.md)]

本文重点介绍设置移动设备菜单项。 此菜单项用于通过采购订单采购的物料的登记和接收。 

您可以使用演示数据公司 USMF 运行此指南。 该过程专门面向仓库经理。


## <a name="create-a-mobile-device-menu-item"></a>创建移动设备菜单项
1. 在导航窗格中，转到 **模块 > 仓库管理 > 设置 > 移动设备 > 移动设备菜单项**。
2. 选择 **新建**。
3. 在 **菜单项名称** 字段中，键入一个值。 这是移动设备菜单项的唯一标识符。 例如，您可以键入 `My PO registration`。  
4. 在 **标题** 字段中，键入一个值。 这是标题，将向移动设备用户显示。 例如，您可以键入 `PO registration`。  
5. 在 **模式** 字段中，选择 **工作**。 登记采购订单的现有接收量会创建将物料从接收区移到库存的工作。 在登记物料前不会创建工作。 因此，将 **使用现有工作** 选项的设置留为 **否**。
6. 在 **常规** 部分的 **工作创建流程** 字段中，选择 **接收的采购订单物料**。
    - 现有采购订单行必须具有唯一标识符才能在仓库中登记。 在此场景中，移动设备将登记采购订单号和物料编号，并且这将允许系统识别采购订单行。 将会创建入库工作，并且另一工作人员可承担该工作。  您选择的工作创建方法确定哪些字段会出现在 **常规** 快速选项卡上。  
    - 如果您选择 **使用默认数据** 选项，**默认数据** 按钮将会启用。 您可以在这里选择字段从而显示工作人员在日常工作中通常需要的数据，以在移动设备上显示这些值。  
    - **牌照分组** 参数与分配给接收物料的单位序列组同样有效。 您可以指定是否应将少于或多于一个托盘的收据分组到一个牌照中，或划分为适用于每个单位的单独牌照。  
    - 如果您选择 **生成牌照** 选项卡，将根据编号规则选项生成唯一牌照号。  
    - 您可以选择创建工作时使用的模板。 例如，如果您登记了采购订单中的某个物料，那么会基于工作模板生成入库工作。 如果您没有选择工作模板，则系统将基于与模板相关的查询条件分配模板。  
    - 如果处置代码在移动设备上显示，工作人员可评估物料的状态和质量，并选择相应代码。 处置代码规则决定了物料是否可用于其他仓库流程。 规则还决定哪个库位指令用于已创建的工作。   
    - 如果您选择 **批处置代码** 选项，工作人员可评估批次的状态和质量，并选择相应处置代码。 批处置代码设置的规则决定了该批次是否可用于其他仓库流程。  
    - 如果您选择 **打印标签** 选项，在接收物料时会自动打印牌照标签。  
7. 选择 **保存**。
8. 关闭该页面。

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>添加菜单项到一个移动设备菜单
1. 在导航窗格中，转到 **模块 > 仓库管理 > 设置 > 移动设备 > 移动设备菜单**。
2. 使用 **快速筛选** 来筛选值为 `inbound` 的 **名称** 字段。
3. 选择 **编辑**。
4. 在可用菜单和物料树形图中，选择您先前创建的菜单项。
5. 选择向右箭头。
6. 选择 **保存**。
7. 关闭该页面。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
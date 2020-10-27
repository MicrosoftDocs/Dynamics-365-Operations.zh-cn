---
title: 设置用于完成采购订单类型工作的移动设备菜单项
description: 此主题演示如何设置“移动设备”菜单项。
author: ShylaThompson
manager: tfehr
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFAutoConfirm, WHSRFMenu
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 86ccc39cb243354db337a5747701e9731c5ad775
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986918"
---
# <a name="set-up-a-mobile-device-menu-item-for-completing-work-of-type-purchase-order"></a>设置用于完成采购订单类型工作的移动设备菜单项

[!include [banner](../../includes/banner.md)]

此主题演示如何设置“移动设备”菜单项。 在此示例中，此菜单项用于执行采购订单类型的工作。 与此菜单项关联的工作类决定哪项工作有效。 您可以使用演示数据公司 USMF 运行此指南。 此过程通常由仓库经理执行。


## <a name="create-a-mobile-device-menu-item"></a>创建移动设备菜单项
1. 通过在搜索栏中进行输入，转到**移动设备菜单项**。
2. 选择**新建**。
3. 在**菜单项名称**字段中，键入一个值。 输入唯一值。 例如，您可以键入 `POMove`。 请记住此值，您稍后需要用到。  
4. 在**标题**字段中，键入一个值。 这是标题，将在移动设备上显示。 例如，您可以键入 `PO Move`。  
5. 在**模式**字段中，选择**工作**。
6. 在**使用现有工作**字段中选择**是**。
    - 该移动设备菜单项用于执行现有的工作。 因此必须将此值设置为**是**。  
    - **显示库存状态**字段确定是否向移动设备上的仓库工作人员显示现有库存的库存状态。  
7. 在**主管**字段中，选择**系统分组**。 在**主管**字段中进行了选择时，将在该页中的**常规**部分显示更多字段。 显示的字段取决于您选择的内容。 如果您选择**系统分组**，将添加两个新字段。 这些在下文中说明。  
8. 在**系统分组**字段中，选择 **WorkPoolId**。 当仓库工作人员打开该菜单项时，将要求他们扫描工作池 ID。 具有此工作池 ID 的所有工作订单以及具有添加到此菜单项的工作类之一的未结工作订单行将被推送到用户。  
9. 在**系统分组标签**字段中，键入一个值。 这是将显示给移动设备用户的文本。 例如，您可以键入 **Work pool**。  
10. 在**放置时覆盖牌照**字段中选择**是**。 当物料放置在牌照控制位置时，此选项允许仓库工作人员覆盖目标牌照。  
11. 在**入库组**字段中选择**是**。
    - 如果工作订单上的所有“放置”行都共享同一位置，则用户将收到一个用于所有行组合的“放置”指令。 
    - 审计模板 ID：工作审计模板允许您指定菜单项的工作流程应该被中断，以便可以执行其他操作。 例如，如果一个菜单项适用于入站工作，则审计模板可能要求工作人员检查温度。 审核模板中说明了流程被中断的点，例如，工作起始或结束点，或者状态改变时的点。  
12. 展开**工作类**部分。
13. 选择**新建**。
14. 在**工作类 ID** 字段中，键入 `Purchase`。 工作池限制该菜单项可以用于的工作。 在这种情况下，其将用于具有采购工作类 ID 的未结工作订单行。  
15. 选择**保存**。

## <a name="set-up-work-confirmation"></a>设置工作确认
1. 选择**工作确认设置**。
2. 在**工作类型**字段中，选择**领料**。
3. 选中**自动确认**复选框。 工作类型为“领料”的工作指令将会自动确认。 此指令不会向用户显示。  
4. 选择**新建**。
5. 在**工作类型**字段中，选择“放置”。
6. 选中**库位确认**复选框。 当放置物料时，仓库工作人员可能需要执行位置确认扫描。  
7. 选择**保存**。

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>添加菜单项到一个移动设备菜单
1. 通过在搜索栏中进行输入，转到**移动设备**菜单。
2. 选择**编辑**。
3. 使用“快速筛选器”以查找记录。 例如，在**名称**字段中筛选值**入站**。 您需要查找用于入站菜单项的菜单。 在 USMF 中，这称为**入站**。  
4. 在树形图中，选择**一个值**。
5. 选择向右箭头。
6. 选择**保存**。
7. 关闭该页面。

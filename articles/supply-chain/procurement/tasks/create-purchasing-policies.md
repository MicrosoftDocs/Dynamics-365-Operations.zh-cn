---
title: 创建采购策略
description: 此过程演示如何创建与您的采购业务流程一致的采购政策。
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicyParameters, SysPolicy, RequisitionPurposeRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3bd4d6f8625c91f2190e994f04cbec4548272f04
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557817"
---
# <a name="create-purchasing-policies"></a>创建采购策略

[!include [task guide banner](../../includes/task-guide-banner.md)]

此过程演示如何创建与您的采购业务流程一致的采购政策。 在您可以创建采购政策之前，必须设置采购政策参数。 可以创建、修改和废弃采购政策，但不能删除采购政策。 此过程通常由采购经理完成。 您可以使用演示数据公司 USMF，也可使用您自己的数据运行该过程。


## <a name="set-up-policy-parameters"></a>设置政策参数
1. 转到“采购政策”。
2. 单击“参数”。
    * 政策优先级规则适用于组织中的不同级别。 显示的组织单元取决于组织的层次结构，以及已经为层次结构中的哪些级别分配了采购内部控制用途。 例如，您的组织可能有法人、成本中心、地区和部门，但是可能其中只有一部分有采购内部控制的层次结构用途。 默认情况下，类型为“公司”的组织可用。  
3. 单击“政策规则类型参数”选项卡。
4. 在树中，选择“采购政策\采购申请控制规则”。
    * 您以策略级别为策略解决方法定义优先级顺序。 但是，对于某些策略类型，您可以为单独的策略规则的类型覆盖优先级顺序。 例如，您可以将采购政策的优先级顺序定义为：成本中心、部门、公司。 对于目录策略规则，您可能希望优先级顺序为：部门、成本中心、公司。 可以为目录策略规则更改优先顺序。 工作人员创建申请时，显示的目录由与该工作人员的部门，随后是与其成本中心，再然后是与其公司关联的政策决定。  
    * 如果列出了多个组织级别，可使用上下箭头设置采购申请控制规则的优先级顺序。  
5. 关闭该页面。

## <a name="create-a-new-policy"></a>创建新策略
1. 单击“新建”。
2. 在“名称”字段中，键入一个值。
3. 在“描述”字段中，键入一个值。
    * 单个采购政策仅可应用于一个组织层次结构。 例如，您可以有一个层次结构称为“地理”，一个称为“部门”，这两个层次结构分别有不同的采购政策。  
    * 选择政策应适用于的组织。  
4. 单击箭头添加所选组织。
    * 可以重复执行此过程添加更多组织。  

## <a name="add-a-policy-rule"></a>添加政策规则
1. 在“政策规则类型”列表中，选择“申请用途规则”。
    * 您将创建一个规则，该规则把默认申请用途设置为类型“消耗量”，但是允许改为选择“补货”类型。  
2. 单击“创建政策规则”。
3. 选择“允许手动覆盖改”字段中的“是”。
4. 单击“关闭”。
    * 现在可为采购政策设置其他政策规则。   请注意，政策规则类型不能有在一个采购政策内同时有效的重叠规则。  
5. 关闭该页面。
6. 关闭该页面。


---
title: 创建和分配高级规则结构
description: 本主题介绍如何创建高级规则结构并分配给科目结构。
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cb18b96d6d7db84262f8fcfadb15afa80e2fa3d8
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145115"
---
# <a name="create-and-assign-advanced-rule-structures"></a>创建和分配高级规则结构

[!include [banner](../../includes/banner.md)]

本主题介绍如何创建高级规则结构并分配给科目结构。 此指南使用演示公司 USMF。

## <a name="create-an-advanced-rule-structure"></a>创建高级规则结构
1. 转到**导航窗格 > 模块 > 总帐 > 会计科目表 > 结构 > 高级规则结构**。
2. 选择**新建**，以打开对话框。
3. 在**高级规则结构**字段中，输入用于描述规则结构的名称。
4. 选择**确定**。
5. 选择**添加段落**。
6. 在“分部”列表中，选择财务维度。 例如，**商店**。  
7. 选择**添加段落**。
8. 选择**激活**。

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a>应用高级规则结构到科目结构中
1. 转到**导航窗格 > 模块 > 总帐 > 会计科目表 > 结构 > 配置科目结构**。
2. 在列表中，找到并选择您想应用高级规则的科目结构。
3. 选择**编辑**。 您还可以选择**高级规则**，将会提示您将科目结构设置为**草稿模式**。  
4. 选择**高级规则**。
5. 选择**新建**，以打开对话框。
6. 在**高级规则**字段中，键入一个值。
7. 在**名称**字段中，键入一个值。
8. 选择**创建**。
9. 选择**添加新条件**。
10. 在**目标位置**字段中，选择主科目或财务维度。
11. 在**运算符**字段中，选择一个选项，例如**介于**和**包含**。
12. 在**值**字段中，键入一个值。
13. 在**范围**字段中，键入一个值。
14. 选择**添加**以打开下拉对话框。
15. 在列表中，找到满足您输入的条件时使用的高级规则结构。
16. 选择**添加**。
17. 关闭该页面。
18. 选择**激活**。


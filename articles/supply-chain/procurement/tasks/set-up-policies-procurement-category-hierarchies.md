---
title: 设置采购类别层次结构的策略
description: 使用此过程设置类别中订购产品的规则。
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicy, ProcCategoryAccessPolicyRule, ProcCategoryPolicyRule, EcoResCategorySingleLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1fdf357466de12bd0188fc43cd266c67af762c7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569906"
---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a>设置采购类别层次结构的策略

[!include [task guide banner](../../includes/task-guide-banner.md)]

使用此过程设置类别中订购产品的规则。 规则是为具体采购政策定义的。 类别访问策略规则控制员工在创建申请时有权访问的采购类别。 在创建申请时，应采用的采购政策和类别访问规则由员工所属法人和运营单位确定。 您可以在演示数据公司 USMF 中使用此过程。 此任务通常由采购经理完成。


## <a name="find-the-procurement-policy"></a>查找采购政策
1. 转到“采购”>“设置”>“策略”>“采购策略”。
2. 单击“采购政策 USMF”政策中的链接。
    * 这是您将为其添加规则的政策。 该政策必须是有效政策。  

## <a name="create-a-category-access-rule"></a>创建类别访问规则
1. 选择“类别访问政策规则”。
    * 如果“创建政策规则”按钮灰显，这是因为“类别访问”已经有一个有效政策规则。 检查“生效日期”和“到期日期”字段以确定到底是哪个，将其选中，然后单击“废弃政策规则”。 如果“创建政策规则”按钮可用，则不需要执行任何操作。  
2. 单击“创建政策规则”。
3. 在“有效日期”字段中输入日期和时间。
    * 时间不得与已处于有效状态的其他规则重合。  
    * 选择将应用此规则的类别。 记下此规则的类别，以后会用到。 当您选择类别时，其父类别也会添加到选定的类别列表中。  
    * 如果要将规则应用于所选类别的所有子类别，请选中“包括子类别”复选框。  
4. 单击“添加”。
    * 如果将“包括父规则”选项设置为“是”，并且尚未为子类别定义任何政策规则，还将把为父类别定义的政策规则分配给其子类别。  
5. 单击“确定”。

## <a name="create-a-category-policy-rule"></a>创建类别策略规则
1. 选择“类别政策规则”。
    * 如果“创建政策规则”按钮灰显，请选择有效政策规则，然后单击“废弃政策规则”。  
2. 单击“创建政策规则”。
3. 在“有效日期”字段中输入日期和时间。
4. 单击“添加”。
5. 选择用于“类别访问规则”的同一个类别。
6. 在“供应商选择”字段中，选择一个选项。
    * 选择一个规则来控制创建申请时可以为类别选择哪种供应商。  
7. 单击“关闭”。
    * 您已定义的政策规则针对类型为“消耗量”的申请。 如果要为类型为“补货”的申请定义政策，请为该政策规则类型创建名称为“补货类别访问政策规则”的规则。  


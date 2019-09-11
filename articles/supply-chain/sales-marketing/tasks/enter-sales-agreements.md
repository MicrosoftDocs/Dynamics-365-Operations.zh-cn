---
title: 输入销售协议
description: 此主题介绍如何向您的客户创建承诺：在超限时间采购议定数量的产品将获得特定的销售折扣的销售协议。
author: omulvad
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7699f426c102b4ae2610db0851ddd127e514b652
ms.sourcegitcommit: 6545bef4584d72dd7789f2d3935cf00ac8f489b0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/13/2019
ms.locfileid: "1871021"
---
# <a name="enter-sales-agreements"></a>输入销售协议

[!include [task guide banner](../../includes/task-guide-banner.md)]

此主题介绍如何向您的客户创建承诺：在超限时间采购议定数量的产品将获得特定的销售折扣的销售协议。 您可以使用 USMF 公司演示数据，也可使用您自己的数据运行该过程。


## <a name="set-up-sales-agreement-header"></a>设置销售协议标题
1. 在导航窗格中，转到**模块 > 销售和营销 > 销售协议 > 销售协议**。
2. 选择**新建**。
3. 在**客户帐户**字段中，从下拉菜单选择所需记录。
4. 在**销售协议分类**字段中，从下拉菜单选择所需记录。
5. 展开**常规**部分。
6. 在**默认承诺**字段中，选择**产品价值承诺**。 承诺类型是您必须在协议中分配的用于定义如何执行协议合同的一个强制性条件。 四种预定义类型可以设置客户的承诺目标，表示为数量或值。 数量承诺类型仅适用于特定的产品，但是基于值的类型适用于特定和非特定的产品销售。  
7. 在**到期日期**字段中，将日期设置为您想要协议终止的将来的日期。
8. 选择**确定**。

## <a name="set-up-product-value-commitment-lines"></a>设置产品值承诺行
1. 选择**添加行**。
2. 在**物料编号**字段中，从下拉菜单选择所需记录。 为协议所选择的承诺类型会影响您可以为协议行输入信息的种类。 例如，对于基于值的协议，必须为客户承诺购买您的货物的金额指定总净额（使用协定币种）。 在此示例中，由于您在为某一客户创建的购买特定值的产品的协议，所以该行上的**数量**和**单位**字段不可用。   
3. 在**净额**字段中，输入客户承诺要购买产品的金额。
4. 在**折扣百分比**字段，输入与该协议相关的应用于客户销售订单行的百分值。
5. 展开**行详细信息**部分。
6. 在**执行最大**字段中，选择**是**。
    - 选择**执行最大**意味着使用承诺的特价、折扣和/或付款期限的所有销售订单行的总金额不能超过该承诺所指定的金额。  
    - 最小和最大发放金额指定了使用所选协议的每个销售订单的销售值的范围。   
7. 展开**销售协议标题**部分。 除非协议的状态设置为**有效**，否则销售订单不能与协议关联，因而不能参与协议的履行。 在此阶段，您可以手动更改状态。 但是，当您确认客户的协议时，状态通常将更改。  
8. 在操作窗格上选择**销售协议**。
9. 选择**确认**。 请确保将**标记协议为有效**选项设置为**是**。  
10. 在**打印报表**字段中选择**是**。
11. 选择**确定**。
12. 关闭该页面。 此协议现在已生效。 您可以将客户订单链接到协议，来抵消承诺目标。  


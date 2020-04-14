---
title: 履行销售协议
description: 此过程向您显示如何通过将销售订单与销售协议关联来履行销售协议。
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreement, SalesAgreementGenerateReleaseOrder, SalesTableListPage, SalesTable, AgreementLine, SalesCreateOrder,  SalesEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7e32decdd13cb578c1ac026f25a56b37ff7231a9
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146460"
---
# <a name="fulfill-sales-agreements"></a>履行销售协议

[!include [banner](../../includes/banner.md)]

此过程向您显示如何通过将销售订单与销售协议关联来履行销售协议。 您可以使用 USMF 公司演示数据，也可使用您自己的数据运行该过程。 在开始本指南前，请确保您具有有效的类型为“产品价值承诺”的销售协议。 或者，您可以运行名为“创建销售协议”的任务指南。  




## <a name="release-a-sales-order-from-the-agreement"></a>发布协议的销售订单
1. 转到“销售和市场”>“销售协议”>“销售协议”。
2. 在列表中，打开您要发布该订单的协议。
3. 在“操作窗格”上单击“销售协议”。
4. 单击“发布订单”。
    * 如“创建发布订单”页顶部的文本所指出的，销售订单行所需的详细信息根据协议是否根据数量或价值而有变化。  
    * 此指南的协议属于“产品价值承诺”类型。 这是本页的“行”部分为空白的原因。 如果承诺是基于数量，则行信息需从协议中复制。  
5. 单击“创建”。
    * 消息通知您，已创建销售订单。 由于订单不包含任何行，您必须添加订单行详细信息，以完成下达流程。   
6. 关闭该页面。
7. 关闭该页面。
8. 转至“销售和营销”>“销售订单”>“所有销售订单”。
9. 在列表中，查找并打开在前一任务中发布的订单。
10. 单击“添加行”。
11. 在“物料编号”字段中，单击下拉按钮以打开查找。
12. 在“物料编号”字段中，键入或选择在相关销售协议中指定的物料。
13. 在“数量”字段中，输入一个数字。
    * 确保您输入的数量带来的“净额”低于相关销售协议的值。  
    * 请注意，由于销售订单与协议关联，协商的折扣百分比适用于该订单行。  
14. 单击“更新行”。
15. 单击“已附加”。
    * “附加的协议”页显示 ID 以及协议期间，此为行发布时间。  
16. 关闭该页面。
17. 在操作窗格上，单击“常规”。
18. 单击“附加销售协议”。
19. 展开“行明细”部分。
20. 单击“履行”选项卡。
    * “履行”选型卡显示与此承诺相关的销售订单行及其履行状态和尚未发布的金额和数量的汇总。   
21. 关闭该页面。
22. 关闭该页面。
23. 关闭该页面。

## <a name="apply-sales-agreement-in-the-order-process"></a>将销售协议应用于订购过程
1. 转至“销售和营销”>“销售订单”>“所有销售订单”。
2. 单击“新建”。
3. 在“客户帐户”字段中，单击下拉按钮以打开查找。
4. 在列表中，查找并选择销售协议所指定的客户。
5. 在列表中，单击所选行中的链接。
6. 展开“常规”部分。
7. 在“销售协议 ID”字段中，单击下拉按钮以打开查找。
8. 在列表中，单击所选行中的链接。
9. 单击“是”。
10. 单击“确定”。
11. 在列表中，标记所选的行。
12. 在“物料编号”字段中，单击下拉按钮以打开查找。
13. 在“物料编号”字段中，键入或选择在相关销售协议中指定的物料。
14. 在列表中，单击所选行中的链接。
15. 单击“保存”。
16. 在操作窗格中，单击“领料和装箱”。
17. 单击“将装箱单过帐”。
18. 展开“参数”部分。
19. 在“过帐”字段中选择“是”。
20. 单击“确定”。
21. 单击“确定”。
22. 在操作窗格上，单击“常规”。
23. 单击“附加销售协议”。
24. 单击“履行”选项卡。


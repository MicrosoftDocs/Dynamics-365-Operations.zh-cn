--- 
title: "设置销售税结算期间"
description: "销售税结算期间含有有关需要申报和缴纳的销售税的期间间隔的信息。"
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: ab7d3a00a327f42a9f70c954d9b64a360a7f9163
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-sales-tax-settlement-periods"></a>设置销售税结算期间

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

销售税结算期间含有有关需要申报和缴纳的销售税的期间间隔的信息。 结算流程可在结算期间或特定日期间隔内运行。 所有与结算期间相关的税务代码将进行结算。 根据相关销售税主管机构的设置，应交税金过帐到供应商或总帐科目。



本任务使用 USMF 公司进行演示。



1. 转到“纳税”>“间接税”>“销售税”>“销售税结算期间”。
2. 单击“新建”。
3. 在“结算期间”字段中，输入一个值。
4. 在“描述”字段中，键入一个值。
5. 在“主管机构”字段中，选择接收为结算期间创建的报表和付款的销售税主管机构。
6. 在列表中，找到并选择所需记录。
7. 在列表中，单击所选行中的链接。
8. 在“付款”字段中，单击下拉按钮以打开查找。
    * 相关销售税主管机构可以设置为供应商，销售税结算将创建开放式供应商发票。 付款期限定义开放式供应商发票的到期日期。  
9. 在列表中，找到并选择所需记录。
10. 在列表中，单击所选行中的链接。
11. 为结算期间间隔选择类型。
12. 输入每一期间的期间间隔单位数。 例如，1 个季度有 3 个月。
13. 选择或清除销售税清算复选框上的“使用批处理”。
    * 结算期的结算流程可在后台将交易记录作为批处理作业。 这是对在期间间隔内的大量涉税交易记录的建议。  
14. 展开“期间间隔”选项卡。
15. 单击“添加”。
16. 在列表中，标记所选的行。
17. 在“开始日期”字段中输入日期。
18. 在“结束日期”字段中输入日期。
19. 单击“新建期间间隔”。
    * 一旦输入第一个期间间隔，可自动创建新期间。 您可以返回和根据需要添加新期间间隔。  
20. 关闭该页面。



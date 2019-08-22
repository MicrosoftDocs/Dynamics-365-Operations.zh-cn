---
title: 设置销售税结算期间
description: 销售税结算期间含有有关需要申报和缴纳的销售税的期间间隔的信息。
author: twheeloc
manager: AnnBe
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8304d9e8997a5d31740ee1203aa4bf0603014056
ms.sourcegitcommit: d0fa8d0140fa81029527edb317623c1a7737c593
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2019
ms.locfileid: "1862980"
---
# <a name="set-up-sales-tax-settlement-periods"></a>设置销售税结算期间

[!include [task guide banner](../../includes/task-guide-banner.md)]

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
    > [!NOTE]
    > 奥地利、比利时、西班牙、意大利、日本和荷兰现在不支持。
14. 选择或清除“防止生成抵消税交易记录”复选框。
    * 默认情况下，系统在结算过程中生成抵消税交易记录，如果在某期间间隔内存在大量税交易记录，这可能造成性能问题。 选择此复选框以防止生成抵消税交易记录。
15. 展开“期间间隔”选项卡。
16. 单击“添加”。
17. 在列表中，标记所选的行。
18. 在“开始日期”字段中输入日期。
19. 在“结束日期”字段中输入日期。
20. 单击“新建期间间隔”。
    * 一旦输入第一个期间间隔，可自动创建新期间。 您可以返回和根据需要添加新期间间隔。  
21. 关闭该页面。


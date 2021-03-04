---
title: 启用考勤管理的工资流程
description: 此程序说明如何根据工时与出勤率来生成工资。
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgPayTable, JmgPayRate, JmgPayAgreementTable, JmgPayAgreementLine, HcmWorker
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5805cc31bf9c7c2231defab63dc9a1e67f82622a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4422964"
---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a>启用考勤管理的工资流程

[!include [banner](../../includes/banner.md)]

此程序说明如何根据工时与出勤率来生成工资。 创建此程序的演示数据公司是 USMF。


## <a name="create-a-pay-type-with-a-related-pay-rate"></a>创建一个具有相关付薪比率的支付类型
1. “工时与出勤率”>“设置”>“工资单”>“支付类型”
2. 单击“新建”。
3. 在“支付类型”字段中，键入一个值。
4. 在“描述”字段中，键入一个值。
5. 单击“保存”。
6. 单击“利率”。
    * 利率支付的类型根据具体的时间间隔设置，个人利率是为员工创建的。 通常没有必要根据工时与出勤率创建支付利率类型。 此信息可能已存于劳资管理系统，用于生成工资。  
7. 单击“新建”。
8. 在列表中，标记所选的行。
9. 在“利率”字段中，输入一个数字。
10. 单击“保存”。

## <a name="create-a-pay-agreement"></a>创建付薪协议
1. 关闭该页面。
2. 关闭该页面。
3. 转到“支付协议”。
    * “工时与出勤率”>“设置”>“付薪协议”  
4. 单击“新建”。
5. 在“支付协议”字段中，键入一个值。
6. 在“描述”字段中，键入一个值。
7. 单击“保存”。
8. 单击“协议”。
9. 单击“新建”。
10. 在列表中，标记所选的行。
11. 在“档案类型”字段中，输入或选择一个值。
12. 在“支付类型”字段中，输入或选择一个值。

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a>设置时间登记工作员工的支付协议
1. 关闭该页面。
2. 关闭该页面。
3. 转到“时间登记工作员工”。
    * “工时与出勤率”>“设置”>“时间登记工作人员”  
4. 在列表中，单击所选行中的链接。
5. 单击“雇用”选项卡。
6. 展开“时间登记”部分。
7. 单击“编辑”。
8. 在“支付协议”字段中，输入或选择一个值。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
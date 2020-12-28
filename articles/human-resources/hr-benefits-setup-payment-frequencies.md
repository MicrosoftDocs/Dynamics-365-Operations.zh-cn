---
title: 设置付款频率
description: Microsoft Dynamics 365 Human Resources 使用付款频率来计算年度福利薪金，确定员工在每个付款期间支付的福利金金额，以及提供商的付款频率。
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a5d562b64a161891bf34b0dfa94fbf68325e21b5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417483"
---
# <a name="set-up-payment-frequencies"></a>设置付款频率

Microsoft Dynamics 365 Human Resources 使用付款频率来计算年度福利薪金，确定员工在每个付款期间支付的福利金金额，以及提供商的付款频率。

福利付款频率使用换算系数转换每月、每半月、每两周、每周和每天付款频率之间的福利付款期间。 这使公司可以定义福利计划中付款频率之间的相关性。

换算系数字段标识从付款频率到标准付款期间的换算系数，允许系统在付款频率之间进行计算。 换算系数金额还确定员工按每个支付频率应该支付的福利金金额。

1. 在 **福利管理** 工作区中，在 **设置** 下，选择 **付款频率**。

2. 选择 **新建**。

3. 为以下字段指定值：

   | 字段 | 说明 |
   | --- | --- |
   | **付款频率** | 唯一的付款频率名称。 |
   | **说明** | 付款频率的描述。 |
   | **期间余额** | 与福利提供商和员工付款频率最匹配的合适的期间。 期间列表包含标准付款期间。 |
   | **付薪期间数** | 代表福利提供商或员工的支付频率的支付期间数。 此数字将用于计算员工的年度福利薪金金额。 |
   | **年度换算系数** | 付款频率的年度换算系数。 例如，每月支付频率的年度换算系数为： </br></br>（12 次每月付款/1 年）= 12 |
   | **每半年换算系数** | 付款频率的半年换算系数。 例如，每月支付频率的半年换算系数为： </br></br>（12 次每月付款/一年 2 次）= 6 |
   | **季度换算系数** | 付款频率的季度换算系数。 例如，每月支付频率的季度换算系数为： </br></br>（12 次每月付款/4 个季度）= 3 |
   | **每月换算系数** | 付款频率的每月换算系数。 例如，每月支付频率的每月换算系数为： </br></br>（12 次每月付款/12 个月）= 1 |
   | **每半月换算系数** | 付款频率的每半月换算系数。 例如，每月支付频率的每半月换算系数为： </br></br>(12 次每月付款/ 24(每月 2 次))= 0.5 | 
   | **每两周换算系数** | 付款频率的年度换算系数。 例如，每月支付频率的年度换算系数为： </br></br>（12 次每月付款/26 周）= 0.461538 |
   | **每周换算系数** | 付款频率的年度换算系数。 例如，每月支付频率的年度换算系数为： </br></br>（12 次每月付款/52 周）= 0.230769 |
   | **每日换算系数** | 付款频率的年度换算系数。 例如，每月支付频率的年度换算系数为： </br></br>（12 次每月付款/365 天）= 0.032877 |
   | **每小时换算系数** | 付款频率的年度换算系数。 例如，每月支付频率的年度换算系数为： </br></br>（12 次每月付款/2080 小时）= 0.005769

4. 选择 **保存**。 

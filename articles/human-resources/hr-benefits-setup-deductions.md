---
title: 配置扣缴
description: 在 Microsoft Dynamics 365 Human Resources 中使用扣缴确定从员工的工资中扣除每种福利的多少（如果有）。
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 46a37aebf99751d16952d3d7c07c538713377a67
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324864"
---
# <a name="configure-deductions"></a>配置扣缴


在 Microsoft Dynamics 365 Human Resources 中使用扣缴确定从员工的工资中扣除每种福利的多少（如果有）。 扣缴是有有效日期的，因此您可以保留扣缴信息的历史记录。 

1. 在 **福利管理** 工作区中，在 **设置** 下，选择 **扣缴**。

2. 选择 **新建**。

3. 为以下字段指定值：

   | 字段 | 说明 |
   | --- | --- |
   | **扣除额** | 用于标识福利扣缴的唯一 ID。 |
   | **说明** | 扣缴的描述。 |
   | **生效** | 开始日期。 默认值为当前系统日期。 |
   | **到期** | 结束日期。 默认值为 12/31/2154，表示永不。 |
   | **标题** | 在处理工资单的福利时，该扣缴针对扣缴中员工部分所使用的工资系统中的标题代码。 这在您使用第三方工资单提供程序时会用到。 |
   | **员工工资扣缴引用** | 在处理工资单的福利时，该扣缴针对扣缴中员工部分所使用的工资系统中的代码。 |
   | **金额标题** | 在处理工资单的福利时，该扣缴金额针对扣缴中员工部分所使用的工资系统中的标题代码。 这通常在您使用第三方工资单提供程序时会用到。 |
   | **可以删除** | 指定从 Dynamics 365 Finance 导出的值是否可以让该值在工资系统中删除。 |
   | **已配对的列** | 指定是否将已配对的相邻列中的标题和扣缴金额导出到工资系统。 |
   | **更改生效日期** | 福利扣缴更改的生效日期。 在此日期，只要您运行 **扣缴更改更新** 处理，福利扣缴都将改变，并更新与此扣缴相关联的所有福利计划。 |
   | **已完成扣缴更改** | 在扣缴更新更改处理完成福利扣缴更改后，将自动选中 **已完成扣缴更改** 复选框。 |
   
4. 要跟踪并维护对福利比率设置的更改，请选择 **操作**，然后选择 **维护版本**。

5. 选择 **保存**。 


[!INCLUDE[footer-include](../includes/footer-banner.md)]


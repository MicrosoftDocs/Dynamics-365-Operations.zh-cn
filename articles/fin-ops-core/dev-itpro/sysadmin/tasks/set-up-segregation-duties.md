---
title: 设置职责划分
description: 您可以设置规则，以分离必须由不同用户执行的任务。
author: peakerbl
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 57c7c436c91ab11404cac3ea056b028023a0617a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688165"
---
# <a name="set-up-segregation-of-duties"></a>设置职责划分

[!include [banner](../../includes/banner.md)]

您可以设置规则，以分离必须由不同用户执行的任务。 此概念被称作职责划分。 例如，您可能不希望由同一人确认收到货物和处理向供应商付款的事宜。 职责划分有助于您减少欺骗风险，并且它还有助于您检测错误或违规。 您还可以使用职责划分来执行内部控制策略。 完成以下过程以创建规则。 您必须是系统管理员，才能完成该过程。 用于创建该过程的演示数据公司是 DAT。 

1. 转到 **导航窗格 > 模块 > 系统管理 > 安全 > 职责划分 > 职责划分规则**。
2. 单击 **新建**。
3. 在 **名称** 字段中，为规则输入一个值。
4. 在 **第一个职责** 字段中，单击下拉按钮以打开查找。
5. 在列表中，找到并选择所需记录。 选择由规则控制的第一个职责。
6. 在 **第二个职责** 字段中，单击下拉按钮以打开查找。 
7. 在列表中，找到并选择所需记录。 选择由规则控制的第二个职责。
10. 在 **严重性** 字段中，选择一个选项。 选择在同一用户或角色同时履行两个职责时发生风险的严重性。  
11. 在 **安全风险** 字段中，键入一个值。 输入安全风险的描述。  
12. 在 **安全降低** 字段中，键入一个值。 输入您为减少安全风险而采取的行动的描述。 例如，您可以通过更详细地审查流程，通过进行阅读管理审查，或者通过与其他部门共享资源，减少风险。     
13. 单击 **保存**。



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
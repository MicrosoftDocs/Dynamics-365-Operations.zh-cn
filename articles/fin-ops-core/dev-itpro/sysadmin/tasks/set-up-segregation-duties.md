---
title: 设置职责划分
description: 您可以设置规则，以分离必须由不同用户执行的任务。
author: peakerbl
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1c1521d6bbbe12964fef0942fcc4943f12a4360a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562489"
---
# <a name="set-up-segregation-of-duties"></a>设置职责划分

[!include [banner](../../includes/banner.md)]

您可以设置规则，以分离必须由不同用户执行的任务。 此概念被称作职责划分。 例如，您可能不希望由同一人确认收到货物和处理向供应商付款的事宜。 职责划分有助于您减少欺骗风险，并且它还有助于您检测错误或违规。 您还可以使用职责划分来执行内部控制策略。 完成以下过程以创建规则。 您必须是系统管理员，才能完成该过程。

1. 转到 **系统管理** > **安全** > **职责划分** > **职责划分规则**。
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

> [!IMPORTANT] 
> 创建规则时，不会验证是否符合职责划分规则。 您可以创建一个为现有角色创建冲突的规则。 现有用户角色分配也可能与新规则冲突。 创建或修改规则后，您必须验证合规性。 有关详细信息，请参阅[确定和解决职责划分冲突](identify-resolve-conflicts-segregation-duties.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
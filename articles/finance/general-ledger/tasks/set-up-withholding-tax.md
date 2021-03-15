---
title: 设置预缴税金
description: 本主题说明如何设置预缴税金。
author: twheeloc
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxWithholdTable, TaxWithholdData, TaxWithholdGroup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45ae7d6bb04dbf06b9b05d9f5610895fced650b0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994432"
---
# <a name="set-up-withholding-tax"></a>设置预缴税金

[!include [banner](../../includes/banner.md)]

本主题说明如何设置预缴税金。 *预缴税金* 是针对供应商的一种不创建增值税交易记录的税金。 对供应商付款计算的预缴税金是一种负债。 因此，在过帐预缴税金时，只有资产负债表科目或负债科目是有效科目。 此任务指南演示如何设置预缴税金。

1. 转到 **导航窗格 > 模块 > 纳税 > 间接税 > 预缴税金 > 预缴税金代码**。
2. 选择 **新建**。
3. 在 **预缴税金代码** 字段中，输入一个值。
4. 在 **预缴税金名称** 字段中，输入预缴税金代码的名称。
5. 在 **主科目** 字段中，选择将预缴应交税金过帐的主科目。
6. 选择 **保存**。
7. 选择 **数值**，然后在列表中标记所需记录。
8. 在 **数值** 字段中，输入用于计算预缴税金的百分比。
9. 选择 **保存**。
10. 关闭该页面。
11. 选择 **保存**。
12. 关闭该页面。
13. 转到 **导航窗格 > 模块 > 纳税 > 间接税 > 预缴税金 > 预缴税金组**。
14. 选择 **新建**。
15. 在 **预缴税金组** 字段中，输入预缴税金组的标识。
16. 在 **描述** 字段中，输入预缴税金组的名称。
17. 在 **预缴税金代码** 字段中，选择预缴税金代码。
18. 选择 **保存**。
19. 关闭该页面。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
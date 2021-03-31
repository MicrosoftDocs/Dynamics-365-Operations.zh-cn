---
title: 设置销售税组和物料销售税组
description: 此任务记录向您介绍销售税和物料销售税组的设置。
author: twheeloc
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxGroup,  TaxItemGroup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e97766be1207fb66b38f25b1e423fb21cec9e726
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222159"
---
# <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a>设置销售税组和物料销售税组

[!include [banner](../../includes/banner.md)]

此任务记录向您介绍销售税和物料销售税组的设置。 增值税组是附加到客户和供应商的增值税代码组。 它们也附加到了交易记录的会计科目，这些会计科目没有过帐到某个特定的供应商或客户。  物料销售税组是附到产品等资源中的销售税代码组。  应用到特定交易记录的增值税由该交易记录的增值税组及增值税（物料）组中包括的增值税代码决定。  仅当为必须及时或记录增值税的每个交易记录选择了增值税组合物料增值税组，才能计算增值税。  

1. 转到 **导航窗格 > 模块 > 纳税 > 间接税 > 销售税 > 销售税组**。
2. 单击 **新建**。
3. 在 **销售税组** 字段中，输入一个值。
4. 在 **描述** 字段中，键入一个值。
5. 切换 **设置** 部分的扩展。
6. 单击 **添加**。
7. 在列表中，标记所选的行。
8. 在 **销售税代码** 字段中，单击下拉按钮以打开查找。
9. 在列表中，单击所选行中的链接。
10. 单击 **保存**。
11. 关闭该页面。
12. 转到 **报税 > 间接税 > 销售税 > 物料销售税组**。
13. 单击 **新建**。
14. 在 **物料销售税组** 字段中，输入一个值。
15. 在 **描述** 字段中，键入一个值。
16. 单击 **添加**。
17. 在列表中，标记所选的行。
18. 在 **销售税代码** 字段中，单击下拉按钮以打开查找。
19. 在列表中，单击所选行中的链接。
20. 单击 **保存**。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
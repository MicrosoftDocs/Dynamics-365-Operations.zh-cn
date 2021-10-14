---
title: 设置销售税代码
description: 本主题说明如何在 Dynamics 365 Finance 中设置销售税代码。
author: twheeloc
ms.date: 09/27/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2539d701dda4ef5e1484d095b2d86d1f68a0dc98
ms.sourcegitcommit: 86f0574363fb869482ef73ff294f345f81d17c5b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7562094"
---
# <a name="set-up-sales-tax-codes"></a>设置销售税代码

[!include [banner](../../includes/banner.md)]

本主题说明如何设置销售税代码。 为法人实体必须计算、征收和向销售税主管机构缴纳的所有间接税或关税创建销售税代码。

此任务使用 USMF 公司演示。

1. 转到 **导航窗格 > 纳税 > 间接税 > 销售税 > 销售税代码**。
2. 选择 **新建**。
3. 在 **销售税代码** 字段中，输入一个值。
4. 在 **名称** 字段中，键入一个值。
5. 通过打开下拉列表选择某一 **结算期间**，以指定需要在哪一期间间隔内必须向哪一销售税主管机构申报和缴纳。
6. 选择 **分类帐过帐组**，以指定将销售税过帐到总帐的主科目。
7. 展开 **计算** 快速选项卡。 其中包含多个字段，可控制销售税金额计算方式。 根据需要填写这些字段。  
8. 在界面顶部的 **操作窗格** 上，选择 **销售税代码**。
9. 选择 **值**。
10. 在 **值** 列中输入此税代码的值。

    在 **计算** 快速选项卡上的 **来源** 字段中，如果选择 **单位金额**，将用该数值乘以该交易记录数量以计算销售税金额。  如果税码不是基于单位税，则该值为在用于该税码的来源上，用以计算销售税金额的百分比。     

11. 选择 **保存**。
12. 关闭该页面。
13. 选择 **保存**。

从 Microsoft Dynamics 365 Finance 版本 10.0.22 开始，如果您正在使用 [税务服务](../../localizations/global-tax-calcuation-service-overview.md)，并且在 **功能管理** 工作区中启用了 [**支持多个增值税登记编号**](../../localizations/emea-multiple-vat-registration-numbers.md)功能 ，则您可以使用 **税务类型** 字段来指定税码的类型。 提供以下值：

- 标准增值税
- 减少增值税
- 增值税 0%
- 消费税
- 其他

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

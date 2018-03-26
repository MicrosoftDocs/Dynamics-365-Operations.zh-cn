---
title: "零售报表"
description: "本主题描述如何创建报表和过帐。"
author: ashishmsft
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: df9c62a2-6f13-4a08-bdca-07d041172c1b
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: ddceadb797af98f85670df72a335b2714fe2f01e
ms.contentlocale: zh-cn
ms.lasthandoff: 03/07/2018

---

# <a name="retail-statements"></a>零售报表

[!include[banner](includes/banner.md)]

在 Microsoft Dynamics 365 for Retail 中，报表过帐流程用于说明在云销售点 (POS) 或现代 POS (MPOS) 中发生的交易记录。 报表过帐流程使用配送计划将一组 POS 交易记录导入到总部 (HQ) 客户端。 在**零售参数**和**商店**页定义的参数用于选择导入到单个报表的交易记录。  

下图显示了报表过帐流程。 在此流程中，通过使用零售调度将 POS 中记录的交易记录传输给客户端。 在客户端接收交易记录后，你可以为商店创建、计算和过帐交易记录报表。 

[![报表过帐流程](./media/retail-statements.png)](./media/retail-statements.png)

## <a name="creating-and-posting-statements"></a>创建和过帐报表
您可以手动创建报表或通过使用该批处理您可以设置全天定期运行。 在这两种情况下，使用以下步骤来创建和过帐报表。

###  <a name="create-the-statement"></a>创建报表
此步骤标识手动创建商店报表。 如果您配置批处理，您可以基于您定义的计划自动创建所有商店的报表。 

### <a name="calculate-the-statement"></a>计算报表
在此步骤中，基于在**零售参数**和**商店**页为每个商店定义的标准来选择交易记录行。 在这些页面中，你定义条件并指定如何计算交易记录。 在你计算报表之前，若要查看包含在报表中的交易记录列表，请使用**交易记录**页。 

报表计算使用来自收银机的钱币清点作为盘点金额。 或者，您可以手动输入该盘点金额。 报表显示交易记录的销售额和所有支付方式中实际盘点金额之间的差额。 只要此差额小于为商店定义的最大过帐差额就将报表过帐。 

> [!NOTE]
> 报表计算流程使用全局编号规则。

在计算报表时，计算包括以下任务：

- 对于所选日期范围，标记以前报表计算中不包括的交易记录。 
- 计算在所选交易记录中支付的总金额。 结果将显示在报表行内，根据报表方法：

  - 如果报表方法是**总计**，则在所选交易记录中为每种付款方式都创建一行。 
  - 如果报表方法是**职员**，则在所选职员成员执行的交易记录中为每种付款方式都创建一行。 
  - 如果报表方法是 **POS 终端**，则在所选收银机执行的交易记录中为每种付款方式都创建一行。 
  - 如果报表方法是**班次**，则在班次期间执行的交易记录中为每种付款方式都创建一行。

如果在**商店**页选中**按报表拆分方法**复选框，则基于在**报表方法**字段中选择的值创建单独的报表。

如果你的商店营业时间延长到午夜之后，你可以基于工作日结束时间（而不是日历日结束时间）配置报表过帐。 

在**商店**页，在**报表/结算**快速选项卡上，在**工作日结束时**字段中，输入工作日报表中包括的必须纪录的最后一次交易记录的时间。 选择**按工作日过帐**复选框以将相同工作日中的交易记录过帐。 当将报表过帐时，在相同工作日内记录的交易记录可以包括在相同销售订单中，即使有些交易记录发生在午夜前，而其他交易记录发生在午夜后。 

#### <a name="example-post-a-statement-for-a-business-day-that-extends-over-two-calendar-days"></a>示例：对于扩展为两个日历日的一个工作日的过帐报表 

商店的营业时间是上午 8:00 至凌晨 3:00，并且在商店配置中选择**按工作日过帐**复选框。 在 5 月 31 日，商店记录上午 8:00 至午夜之间的交易记录。 商店还记录 6 月 1 日凌晨 12:01 至凌晨 3:00 之间的交易记录。 

当商店在工作日结束过帐报表时，生成包括上午 8:00 至次日凌晨 3:00 之间记录的所有交易记录的销售订单，即便是这些交易记录发生在 5 月 31 日和 6 月 1 日两天。 

如果同一商店清除**按工作日过帐**复选框，那么当商店在工作日结束过帐报表时将生成单独的销售订单。 一个销售订单包括在 5 月 31 日上午 8:00 至午夜之间的营业时间记录的交易记录，并且第二个销售订单包括在 6 月 1 日凌晨 12:01 至凌晨 3:00 之间的营业时间记录的交易记录。
 
> [!NOTE]
> 在创建报表前，您在报表期间应关闭班次。 

### <a name="post-the-statement"></a>将报表过帐
在您过帐报表时，将针对报表中的零售销售创建销售订单和发票。

- 对于分配给商店的默认客户，将付现自运的销售聚合到一个销售订单和发票上。 
- 在 Microsoft Dynamics 365 for Retail POS 中将客户添加到交易记录中的零售销售生成单独的销售订单和发票，每个针对一个独有客户。 

付款日志在报表中自动为付款创建，并且库存，为 POS 商店更新。


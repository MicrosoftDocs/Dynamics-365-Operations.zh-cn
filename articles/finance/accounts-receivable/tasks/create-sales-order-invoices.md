---
title: 创建销售订单账单
description: 本文介绍如何给销售订单开票，包括合并发票以及成批处理。
author: ShivamPandey-msft
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ceda837cae563dab68969cb9f05de113079d4495
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910249"
---
# <a name="create-sales-order-invoices"></a>创建销售订单账单

[!include [banner](../../includes/banner.md)]

本文介绍如何给销售订单开票，包括合并发票以及成批处理。 该程序适用于 USMF 演示公司。


## <a name="create-an-invoice-from-a-sales-order"></a>为一个销售订单创建一张发票
1. 转到 **导航窗格 > 模块 > 应收帐款 > 订单 > 已装运但未开票的销售订单**。
2. 从列表中选择一个销售订单。 
3. 在 **操作窗格** 上，单击 **发票 > 生成 > 发票**。 请注意此销售订单具有多个相关的装箱单。 它将只显示单词 *多个*，不会显示装箱单编号。  
4. 展开 **参数** 部分。
    - 若要过帐发票，请设定为“是”。 也可以关闭过帐功能只打印发票。 但是您还可以通过创建形式发票代替发票，效果一样。  
    - 此选项用于批处理作业。 运行批处理作业，查询将会运行。
5. 在 **打印** 字段中，选择“以后”。
6. 为 **打印发票** 选择 **是**。 “打印管理”可打印多个发票副本并通过电子邮件以 PDF 文档的形式发送发票。  
7. 在 **打印费用** 字段中，选择“汇总”。
8. 在 **检查信用额度** 字段中，选择“余额”。
9. 单击 **取消**。

## <a name="combine-orders-into-a-single-invoice"></a>合并订单为一张发票
1. 转到 **导航窗格 > 模块 > 应收帐款 > 订单 > 所有销售订单**。
2. 选定一个拥有多个发票的客户。
3. 选择来自同一客户的多个未结销售订单。
4. 在 **操作窗格** 上，单击 **发票 > 生成 > 发票**。
5. 展开 **参数** 部分。
6. 在 **数量** 字段中，选择“全部”。 请注意在概述部分列出的两张发票。 现在将两张合并为一张发票。  
7. 在 **汇总更新** 字段中，选择“发票帐目”。
8. 单击 **整理** 合并这两个销售订单为一张发票。 两个销售订单现在合并为一张发票。   
9. 单击 **取消**。
10. 单击 **是**。

## <a name="post-invoices-in-a-batch"></a>成批过帐发票
1. 转至 **导航窗格 > 模块 > 应收帐款 > 发票 > 批处理开票 > 发票**。
2. 单击 **选择**。
3. 单击 **确定**。
4. 单击 **批处理**。
5. 在 **批处理** 中选择 **是**。
6. 单击 **重复执行**。
7. 选择 **天**。
8. 单击 **确定**。
9. 单击 **确定**。
10. 单击 **取消**。
11. 单击 **是**。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

---
title: 购买交易记录中的预缴税金
description: 对于有预缴税金的供应商，您可以在 **所有供应商** 页上分配默认的 **预缴税金组**。
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 06997e2d6b47d867e014a7d493d91015c78a5e04
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060704"
---
# <a name="withholding-tax-in-purchase-transactions"></a>购买交易记录中的预缴税金

对于有预缴税金的供应商，您可以在 **所有供应商** 页上分配默认的 **预缴税金组**。

1. 转到 **导航窗格 > 模块 > 应付帐款 > 供应商 > 所有供应商**。

2. 单击相应的供应商帐户，单击 **编辑**。

3. 在 **发票和交货** 选项卡中，将 **计算预缴税金** 字段设置为 **是**。

   > [!NOTE] 
   > 如果未在数据中为此供应商打开 **计算预缴税金**，将不会计算预缴税金。

4. 在 **预缴税金组** 中选择一个预缴税金组。

5. 单击 **保存**。

对于有预缴税金的产品/服务，您可以在 **已发布产品** 中分配默认的 **物料预缴税金组**。

1. 转到 **导航窗格 > 模块 > 产品信息管理 > 产品 > 已发放产品**。

2. 单击相应的物料编号，单击 **编辑**。

3. 在 **采购** 选项卡中，单击 **计算预缴税金**。

   > [!NOTE] 
   > 如果在 **已发布产品** 页上的 **采购** 选项卡中未将此产品的 **计算预缴税金** 设置为 **是**，将不计算预缴税金。

4. 在 **物料预缴税金组** 列表中选择一个物料预缴税金组。

5. 单击 **保存**。

预缴税金组和物料预缴税金组可以在页面中分配： 

- **采购订单**
- **供应商账单**
- **账单日记帐**

创建 **采购订单** 和/或 **待定供应商发票页** 时，默认的预缴税金组和物料预缴税金组将被带入行中。 对于 **供应商发票日记帐**，您可以打开 **计算预缴税金**，然后在日记帐中的 **常规** 选项卡中选择 **物料预缴税金组**。

临时预缴税金金额可在 **采购订单** 页上 **总计** 选项卡的 **调整后预缴税金** 字段中找到。

![采购订单中包含预缴税金](media/withholding-tax-adjusted.png)

预缴税金根据 **供应商付款日记帐** 计算。 您可以在 **结算交易** 页上的 **预缴税金** 选项卡中手动调整适用的预缴税金代码以及实际的预缴税金金额。

![可以在“结算交易”页上手动调整预缴](media/withholding-tax-vendor-payment-tab.png)

所得的预缴税金金额将从供应商付款中扣除，并过帐到相关凭证中的 **预缴税金科目**。

![显示相关凭证的预缴税金科目](media/withholding-tax-adjusted.png)

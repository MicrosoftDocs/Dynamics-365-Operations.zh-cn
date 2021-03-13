---
title: 销售交易记录中的预缴税金
description: 本主题列出了避免为选定客户计算预缴税金的步骤。 对于在向您的付款中指定预缴税金的客户，您可以分配默认的预缴税金组。
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
ms.openlocfilehash: c50f6df1c63c91107da65f463934565f786d6ccd
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060706"
---
# <a name="withholding-tax-in-sales-transactions"></a>销售交易记录中的预缴税金

本主题列出了避免为选定客户计算预缴税金的步骤。 对于在向您的付款中指定预缴税金的客户，您可以在 **客户** 页分配默认的 **预缴税金组**。 

1. 转到 **导航窗格 > 模块 > 应收帐款 > 客户 > 所有客户**。

2. 单击相应的客户帐户，单击 **编辑**。

3. 在 **发票和交货** 选项卡中，将 **计算预缴税金** 字段设置为 **是**。

   > [!NOTE] 
   > 如果未在主数据中为此客户打开 **计算预缴税金**，将不会计算预缴税金。

4. 在 **预缴税金组** 中选择一个预缴税金组。

5. 单击 **保存**。

对于有预缴税金的产品/服务，您可以在 **已发布产品** 中分配默认的 **物料预缴税金组**。

1. 转到 **导航窗格 > 模块 > 产品信息管理 > 产品 > 已发放产品**。

2. 单击相应的物料编号，单击 **编辑**。

3. 在 **销售** 选项卡中，单击 **计算预缴税金**。

   > [!NOTE] 
   > 如果在 **已发布产品** 页上的 **销售** 选项卡中未将此产品的 **计算预缴税金** 设置为 **是**，将不计算预缴税金。

4. 在 **物料预缴税金组** 列表中选择一个物料预缴税金组。

5. 单击 **保存**。

预缴税金组和物料预缴税金组可以使用 **销售订单** 页分配。 

创建新的销售订单时，默认预缴税金组和物料预缴税金组将用作销售订单行上的默认条目。

预缴税金使用 **客户付款日记帐** 计算和过帐。 您可以在 **结算交易** 页上的 **预缴税金** 选项卡中手动调整适用的预缴税金代码以及实际的预缴税金金额。

计算出的预缴税金金额将从客户付款中扣除，并过帐到相关凭证中的 **预缴税金冲销** 科目。

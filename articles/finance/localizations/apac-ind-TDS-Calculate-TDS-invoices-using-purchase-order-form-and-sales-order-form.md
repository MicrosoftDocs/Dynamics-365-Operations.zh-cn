---
title: 使用采购订单窗体和销售订单窗体计算 TDS 发票
description: 本主题列出了用于计算各种类型的发票的从源扣缴税款 (TDS) 的步骤。
author: kailiang
ms.date: 02/12/2021
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
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: d0e6cce8f7a90cd1624e64023a1b51fd02d12152f874e13ce2e5d22af16fe173
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782835"
---
# <a name="calculate-tds-invoices-using-purchase-order-form-and-sales-order-form"></a>使用采购订单窗体和销售订单窗体计算 TDS 发票

[!include [banner](../includes/banner.md)]

本主题列出了使用 **采购订单**、**采购日记帐**、**总订单** 和 **销售订单** 页面计算各种类型的发票的从源扣缴税款 (TDS) 的步骤。

1. 使用列出的页面创建采购订单、采购日记帐、采购总订单或销售订单。 输入所需的详细信息。

2. 选择 **设置** 选项卡以查看供应商或客户的评估对象的性质。 此信息在 **预缴税金组** 字段组下的 **评估对象的性质** 字段中列出。

3. 在 **TDS 组** 字段中，查看或修改为供应商或客户定义的默认 TDS 组。

   > [!NOTE]
   > 在 **TDS 组** 字段中选择 TDS 组时，**TCS 组** 字段不可用。 如果为 **所有供应商** 或 **所有客户** 页面上的供应商或客户选中 **计算预缴税金** 复选框，将仅计算 TDS。  

4. 在 **行** 选项卡上创建明细项，然后输入所需的详细信息。

5. 选择 **设置** 选项卡（行级别）以查看或更改在标头级别定义的 TDS 组。 TDS 组显示在位于 **预缴税金组** 字段组下的 **TDS 组** 字段中。

6. 选择 **税务信息** 选项卡，然后选择为此字段中显示的公司名称设置的备用地址。 公司名称显示在位于 **公司信息** 字段组下的 **名称** 字段中。 

   选定公司名称的 TAN 显示在 **预缴税金** 字段组下的 **税务帐号** (**TAN**) 字段中。 

7. 选择 **预缴税金** 以打开 **临时预缴税金交易** 页面。 查看 **临时预缴税金交易** 页面上方的窗格上的以下字段。

   - **预缴税金总金额** - 为 TDS 组的交易计算的总 TDS。

   - **值** - 用于计算交易的 TDS 的总百分比。 总百分比基于为附加到 TDS 组的 TDS 税码定义的公式。

   - **调整后预缴税金总金额** - TDS 组中所有税码的调整后 TDS 总金额。

   - **TDS** - 如果选择，TDS 组将附加到交易。

**临时预缴税金交易** 页面上的 **概述**、**常规** 和 **调整** 选项卡上的字段为附加到 TDS 组的每个 TDS 税码显示计算的 TDS 金额和调整的 TDS 金额详细信息。

8. 选择 **阈值** 以打开 **阈值** 页面。 在此页面上查看为附加到特定 TDS 税码的 TDS 税种组分定义的阈值限制。

9. 选择 **公式设计器** 以打开 **公式设计器** 页面。 在此页面上查看为特定 TDS 税码定义的公式。 

10. 过帐发票。 根据采购发票计算的 TDS 金额将过帐到应付帐款，根据销售发票计算的 TDS 金额将过帐到为 TDS 组中每个 TDS 税码定义的应收帐款。 TDS 税码的应付帐款或应收帐款在 **预缴税金代码** 页面上定义。

11. 选择 **查询** 按钮 **> 发票 > 过帐的预缴税金** 按钮以打开 **预缴税金交易** 页面。 您可以在 **值** 字段中查看用于计算交易的 TDS 的总百分比。

**预缴税金交易** 页面上的 **概述**、**常规** 和 **金额** 选项卡上的字段显示为交易计算的 TDS 的信息。 查看附加到 TDS 组的每个 TDS 税码的 TDS 计算信息。

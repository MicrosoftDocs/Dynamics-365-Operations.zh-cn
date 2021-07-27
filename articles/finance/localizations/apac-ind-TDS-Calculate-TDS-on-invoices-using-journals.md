---
title: 使用日记帐计算发票的 TDS
description: 本主题列出了使用日记帐计算从源扣缴税款 (TDS) 的步骤。
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
ms.openlocfilehash: bc1a8570e60e2b17f27c3e63c5ff847b3cb7a2dd
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/06/2021
ms.locfileid: "6358450"
---
# <a name="calculate-tds-on-invoices-using-journals"></a>使用日记帐计算发票的 TDS

[!include [banner](../includes/banner.md)]

本主题列出了使用日记帐计算从源扣缴税款 (TDS) 的步骤。

首先，打开 **普通日记帐** 页面（**总帐 > 日记帐条目 > 总帐**）。

[![普通日记帐。](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)

1. 使用表中列出的日记帐表单创建日记帐行。 选择帐户类型和抵销帐户类型，然后输入交易金额。 

   > [!NOTE]
   > 在 **发票审核日记帐** 页面上，选择 **查找凭证**，然后选择要计算 TDS 的发票。 查看在 **发票登记簿** 页面或 **查找凭证** 页面中创建的发票。  

2. 在 **日记帐凭证** 页面的 **常规** 选项卡上，在 **TDS 组** 字段中查看或修改为供应商或客户定义的默认 TDS 组。 在日记帐行上计算的 TDS 金额基于为在 **TDS 组** 字段中列出的 TDS 税码定义的公式。 

   > [!NOTE]
   > 当在 **TDS 组** 字段中选择 TDS 组时，**预缴税金组** 字段和 **TCS 组** 字段变得不可用。 **预缴税金组** 字段仅在 **普通日记帐** 页面上可用。 如果为 **所有供应商** 或 **所有客户** 页面上的供应商或客户选中 **计算预缴税金** 复选框，将仅计算 TDS。   

3. 选择 **税务信息** 选项卡。根据需要选择为此字段中的公司设置的公司备用地址。 您可以在位于 **公司信息** 字段组下的 **名称** 字段中查看公司名称。 

4. 在位于 **预缴税金** 字段组下的 **评估对象的性质** 字段中查看供应商或客户的评估对象类别的性质。 在 **税务帐号** (**TAN**) 字段中，查看显示的选定公司名称的 TAN。  

5. 在 **预缴税金** 菜单中选择 **预缴税金** 以打开 **临时预缴税金交易** 页面。 以下字段显示在 **临时预缴税金交易** 页面上方的窗格上。

   - **预缴税金总金额** - 为 TDS 组的交易计算的总 TDS。

   - **值** - 用于计算交易的 TDS 的总百分比。 总百分比基于为附加到 TDS 组的 TDS 税码定义的公式。

   - **调整后预缴税金总金额** - TDS 组中所有税码的调整后 TDS 总金额。

   - **TDS** - 如果选择，TDS 组将附加到交易。

  **临时预缴税金交易** 页面上的 **概述**、**常规** 和 **调整** 选项卡上的字段为附加到 TDS 组的每个 TDS 税码显示计算的 TDS 金额和调整的 TDS 金额详细信息。

6. 选择 **阈值** 以打开 **阈值** 页面。 在此页面上查看为附加到特定 TDS 税码的 TDS 税种组分定义的阈值限制和异常阈值限制。

   选择 **公式设计器** 以打开 **公式设计器** 窗体。 在此页面中查看为特定 TDS 税码定义的公式。 关闭 **公式设计器** 和 **临时预缴税金交易** 页面以返回到 **日记帐凭证** 页面。

8. 输入其他所需的详细信息。 验证和过帐日记帐。 根据采购发票计算的 TDS 金额将过帐到应付帐款。 根据销售发票计算的 TDS 金额将过帐到为 TDS 组中每个 TDS 税码定义的应收帐款。 TDS 税码的应付帐款或应收帐款在 **预缴税金代码** 页面上定义。

9. 选择 **过帐的预缴税金** 以打开 **预缴税金交易** 页面。 在 **值** 字段中，显示用于计算交易的 TDS 的总百分比。

   预缴税金交易页面中的 **概述**、**常规** 和 **金额** 选项卡上的字段为附加到 TDS 组的每个 TDS 税码显示计算的 TDS 金额和调整的 TDS 金额详细信息。

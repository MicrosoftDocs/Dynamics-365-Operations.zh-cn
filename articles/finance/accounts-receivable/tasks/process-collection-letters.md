---
title: 处理催款单
description: 该主题说明如何创建、打印并过帐收款单。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 4e9f53215643d0ed431f075891798b7837cedfe9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220147"
---
# <a name="process-collection-letters"></a>处理催款单

[!include [banner](../../includes/banner.md)]

该主题说明如何创建、打印并过帐收款单。 此任务使用 USMF 公司演示。

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a>在该过帐上设置收款单的排序
1. 转到 **导航窗格 > 模块 > 信用和收款 > 设置 > 客户过帐模板**。
2. 单击 **编辑**。
3. 从下拉列表中选择收款单排序。 如果不希望使用该过帐模板生成交易收款单，则该字段保留空白。  
4. 展开 **表限制** 选项卡可以更改处理收款单的方式。 如果此字段设置为 **是**，则将在此过帐模板创建收款单。  

## <a name="create-collection-letters"></a>创建催款单
1. 转到 **导航窗格 > 模块 > 信用与收款 > 收款单 > 创建收款单**。
2. 选择收款单的交易类型。 此计算包含这些类型的所有开放交易。  
3. 在 **催款单** 字段中，选择一个选项。
4. 在 **催款单日期** 字段中，输入催款单的日期。
5. 如果将 **使用过帐模板** 更改为 **选择**，则请选择一个过帐模板。 具有两个过帐模板选项：   

   - **帐户** – 使用分配给每个利息单的客户帐户的过帐模板。   
   - **选择** – 使用在 **过帐模板** 字段中选择的过帐模板。  

6. 扩展 **要包括的记录** 部分。
7. 选择 **筛选器**。
8. 在 **条件** 字段中，输入“客户 ID”。 例如，输入 'US-001'。
9. 选择 **确定**。
10. 选择 **确定**。

## <a name="print-collection-letters"></a>打印收款单
1. 转到 **导航窗格 > 模块 > 信用与收款 > 催款单 > 审核和处理催款单**。
2. 在 **状态** 字段中，选择 **创建**。
3. 在 **打印** 字段中，选择 **不打印**。
4. 选择 **打印**。
5. 选择 **催款单**。
6. 在 **参数** 部分中，输入过帐的截止日期。
7. 展开 **要包括的记录** 部分，然后输入催款单的详细信息。
8. 选择 **确定** 以打印催款单。
9. 过帐收款单。

    1. 选择 **过帐**。
    1. 输入该收款单的过帐日期
    1. 扩展 **要包括的记录** 部分。
    1. 选择 **确定**。
    1. 在 **状态** 字段中，选择 **已过帐**。
    1. 在 **打印** 字段中，选择一个选项。

## <a name="control-collection-letters-at-the-customer-level"></a>在客户级别控制催款单
如果在交易记录级别设置催款单，则可以根据交易帐龄为一个客户生成多张催款单。 如果交易在不同催款单序列中显示，将为客户的每组逾期交易生成单独的催款单。 因此，可能会发生如下情况：一位客户可能会收到一张针对逾期 60 天的交易的催款单，以及另一张针对逾期 90 天的交易的催款单。 

每张催款单还与一个催款单代码关联。 催款单代码与单个交易关联，用于确定何时应该为每个交易生成下一张催款单。 例如，如果一个交易预期超过 30 天，则催款单代码确定交易预期 60 天且尚未支付时，发送下一张催款单。 

也可以在客户级别设置催款单。 在此情况下，将跟踪每个交易的催款单代码，但催款单处理将基于为客户存储的单个催款单级别。 单个催款单将包含对于客户已逾期的所有交易记录。 由于宽限天数现在在客户级别跟踪，下一个催款单将在序列中下一个催款单经过的宽限天数后发送，即使交易记录在上一个催款单发送之后变为逾期。 此选项可帮助减少您必须向每个客户发送的催款单数量。

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a>将客户设置为在客户级别控制催款单
1.  转到 **导航窗格 > 模块 > 信用和收款 > 设置 > 应收帐款参数**，然后选择 **收款** 选项卡。 
2.  将 **依据以下条件创建催款单** 值更改为 **客户**。 
3.  转到 **导航窗格 > 模块 > 信用与收款 > 催款单 > 审核和处理催款单**。 将只为客户生成一个催款单，其中包含所有逾期的交易记录。

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a>忽略计算催款单代码时的付款及贷项通知单
如果您在将包含在催款单中的交易记录中包含付款及贷项通知单，您可能有将触发催款单的付款或贷项通知单。 您可以通过更改 **忽略计算催款单代码时的付款及贷项通知单** 参数来控制付款及贷项通知单如何控制催款单代码。 

若要忽略计算催款单代码时的付款及贷项通知单，请执行以下操作。

1. 转到 **导航窗格 > 模块 > 信用和收款 > 设置 > 应收帐款参数**，然后单击 **收款** 选项卡。 
2. 将 **忽略计算催款单代码时的付款及贷项通知单** 的值更改为 **是**。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
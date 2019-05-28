---
title: 处理催款单
description: 该过程说明如何创建、打印并过帐收款单。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/04/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 8a3f74d2891c050294e089eae14ba2386449d7c9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549621"
---
# <a name="process-collection-letters"></a>处理催款单

[!include [banner](../../includes/banner.md)]

该过程说明如何创建、打印并过帐收款单。 本任务使用 USMF 公司进行演示。

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a>在该过帐上设置收款单的排序
1. 转到**信用和收款 > 设置 >客户过账模板**。
2. 单击**编辑**。
3. 从下拉列表中选择收款单排序。 如果不希望使用该过帐模板生成交易收款单，则该字段保留空白。  
4. 展开该表格的限制选项卡可以更改处理收款单的方式。 如果此字段设置为**是**，则将在此过帐模板创建收款单。  

## <a name="create-collection-letters"></a>创建催款单
1. 转到**信用与收款 > 收款单 > 创建收款单**。
2. 选择收款单的交易类型。 此计算包含这些类型的所有开放交易。  
2. 在**催款单**字段中，选择一个选项。
3. 输入该收款单的日期。
4. 如果将**使用过帐模板**更改为**选择**，则请选择一个过帐模板。 具有两个过帐模板选项：   
   - **帐户** – 使用分配给每个利息单的客户帐户的过帐模板。   
   - **选择** – 使用在**过帐模板**字段中选择的过帐模板。  
5. 扩展**要包括的记录**部分。
6. 单击**筛选器**。
7. 在**条件**字段中，输入“客户 ID”。 例如，输入 'US-001'。
8. 单击**确定**。
9. 单击**确定**。

## <a name="print-collection-letters"></a>打印收款单
1. 转到**信用和收款 > 收款单 > 查看并处理收款单**。
2. 在**状态**字段中，选择**创建**。
3. 在**打印**字段中，选择**不打印**。
4. 单击**打印**。
5. 单击**注解收款单**。
6. 扩展**要包括的记录**部分。
7. 输入过帐的截止日期。
8. 单击**确定**以打印收款单。
9. 过帐收款单。
   1. 单击**过帐**。
   2. 输入该收款单的过帐日期
   3. 扩展**要包括的记录**部分。
   4. 单击**确定**。
   5. 在**状态**字段中，选择**已过帐**。
   6. 在**打印**字段中，选择一个选项。

## <a name="control-collection-letters-at-the-customer-level"></a>在客户级别控制催款单
您还可以在客户级别设置催款单，以便跟踪每个交易记录的催款单代码，但催款单处理将基于为客户存储的单个催款单级别。 单个催款单将包含对于客户已逾期的所有交易记录。 由于宽限天数现在在客户级别跟踪，下一个催款单将在序列中下一个催款单经过的宽限天数后发送，即使交易记录在上一个催款单发送之后变为逾期。 此选项将减少您按客户发送的催款单数量。 

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a>将客户设置为在客户级别控制催款单
1.  转到**信用和收款 > 设置 > 应收帐款参数**并单击**收款**选项卡。 
2.  将**依据以下条件创建催款单**值更改为**客户**。 
3.  转到**信用和收款 > 收款单 > 查看并处理收款单**。 将只为客户生成一个催款单，其中包含所有逾期的交易记录。

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a>忽略计算催款单代码时的付款及贷项通知单
如果您在将包含在催款单中的交易记录中包含付款及贷项通知单，您可能有将触发催款单的付款或贷项通知单。 您可以通过更改**忽略计算催款单代码时的付款及贷项通知单**参数来控制付款及贷项通知单如何控制催款单代码。 

若要忽略计算催款单代码时的付款及贷项通知单，请执行以下操作。
1. 转到**信用和收款 > 设置 > 应收帐款参数**并单击**收款**选项卡。 
2. 将**忽略计算催款单代码时的付款及贷项通知单**的值更改为**是**。

---
title: 处理利息
description: 此过程将向您展示如何创建、打印和过帐利息单。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 093fbd23f9fcaf62db9988a98a94b8cebf582768
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140137"
---
# <a name="process-interest"></a>处理利息

[!include [banner](../../includes/banner.md)]

此过程将向您展示如何创建、打印和过帐利息单。 此任务使用 USMF 公司演示。


## <a name="set-up-interest-on-the-posting-profile"></a>在过帐模板设置利息。
1. 在**导航窗格**中，转到**模块 > 信用和收款 > 设置 > 客户过帐模板**。
2. 单击**编辑**。
3. 在**设置**快速选项卡的**利息代码**字段中，从下拉列表选择一个利息代码。 如果您不希望使用此过帐模板计算交易利息，则将此字段留空。 **表单限制**快速选项卡可允许您更改处理利息的方法。 如果此字段设置为“是”，则根据此过帐模板计算利息。  

## <a name="calculate-interest"></a>计算利息
1. 在**导航窗格**中，转到**模块 > 信用和收款 > 利息 > 创建利息单**。
2. 您必须为您将要计算的利息选择交易记录类型。 此计算包含这些类型的所有开放交易。  
3. 如果将**利息**设置为“是”，您将在利息单中计算利息。 您也许想要在包括这些交易之前，管理利息单中计算利息的法律。  
4. 在**开始日期**字段中，输入将计算的利息的开始日期。 如果您并未设定**开始日期**，则所有未过帐的利息单将会被取消，利息将从交易记录日期开始重新计算。
5. 在**结束日期**字段中，输入将计算的利息的结束日期。
6. 在**使用的过帐模板来自**字段中，选择一个选项。 过帐模板选项有三个：
    - 帐户 – 使用分配给每个利息单的客户帐户的过帐模板。 
    - 选择 – 使用在“过帐模板”字段中选择的过帐模板。
    - 交易记录 –使用来自为每张利息单计算出利息的交易记录的单独过帐模板。 未分配过帐模板的交易记录将使用“应收账款参数单”的“分类帐”和“销售税”所指定的过帐模板。  
7. 扩展**要包括的记录**快速选项卡。
8. 单击**筛选器**。
9. 在**条件**字段中，输入“客户 ID”。 例如，输入 'US-001'。
6. 单击 **确定**。
7. 单击 **确定**。

## <a name="print-interest-notes"></a>打印利息单
1. 在**导航窗格**中，转到**模块 > 信用和收款 > 利息 > 审核和处理利息单**。
2. 在**状态**字段中，选择“创建”。
3. 在**打印**字段中，选择“不打印”。
4. 单击**打印**。
5. 扩展**要包括的记录**快速选项卡。
6. 单击 **确定**。
7. 关闭该页面。

## <a name="post-the-interest-note"></a>过帐利息单
1. 选择准备过帐的利息单（状态为“已创建”）。
2. 单击**过帐**。
3. 输入利息单的过帐日期。 选择“是”可以为每张利息单创建一个总帐交易记录。 如果未选择“是”，应付给客户的所有利息单上的利息将累加起来，作为一笔交易记录过帐到总帐中。  
4. 扩展**要包括的记录**快速选项卡。
5. 单击 **确定**。
6. 在**状态**字段中，选择“已过帐”。


---
title: 处理利息
description: 此过程将向您展示如何创建、打印和过帐利息单。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5652a38684061914f895d7f8b82999c9840fd63
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "359144"
---
# <a name="process-interest"></a>处理利息

[!include [task guide banner](../../includes/task-guide-banner.md)]

此过程将向您展示如何创建、打印和过帐利息单。 本任务使用 USMF 公司进行演示。


## <a name="set-up-interest-on-the-posting-profile"></a>在过帐模板设置利息。
1. 转到“信用征收”>“设置”>“客户过帐模板”。
2. 单击“编辑”。
    * 从下拉列表中选择利息代码。 如果您不希望使用此过帐模板计算交易利息，则将此字段留空。  
    * “表单限制”选项卡可允许您更改处理利息的方法。 如果此字段设置为“是”，则根据此过帐模板计算利息。  

## <a name="calculate-interest"></a>计算利息
1. 转到“信用征收”>“利息”>“创建利息单”。
    * 您必须为您将要计算的利息选择交易记录类型。 此计算包含这些类型的所有开放交易。  
    * 如果您选择“利息”，您将在利息单中计算利息。 您也许想要在包括这些交易之前，管理利息单中计算利息的法律。  
    * 利息为此该日期开始计算到“结束日期”。 如果您并未设定“开始日期“，则所有未过帐的利息单将会被取消，利息将从交易记录日期开始重新计算。  
2. 输入利息单的日期。
    * 具有三个过帐模板选项：帐户 – 使用分配给客户帐户每张利息单的过帐模板。   选择 – 使用在“过帐模板”字段中选择的过帐模板。   交易记录 –使用来自为每张利息单计算出利息的交易记录的单独过帐模板。 未分配过帐模板的交易记录将使用“应收账款参数单”的“分类帐”和“销售税”所指定的过帐模板。  
    * 如果您将“使用过帐模板”更改为“选择”，则在此选择一个过帐模板。  
3. 展开或折叠包含部分的“记录”。
4. 单击“筛选器”。
5. 在“条件”字段中，输入“客户 ID”。 例如，输入 'US-001'。
6. 单击“确定”。
7. 单击“确定”。

## <a name="print-interest-notes"></a>打印利息单
1. 转到“信用征收”>“利息”>“审查和处理利息单”。
2. 在“状态”字段中，选择“创建”。
3. 在“打印”字段中，选择“不打印”。
4. 单击“打印”。
5. 展开或折叠包含部分的“记录”。
6. 单击“确定”。
7. 关闭该页面。

## <a name="post-the-interest-note"></a>过帐利息单
1. 选择准备过帐的利息单（状态为“已创建”）。
2. 单击“过帐”。
3. 输入利息单的过帐日期。
    * 选择“是”可以为每张利息单创建一个总帐交易记录。     如果未选择“是”，应付给客户的所有利息单上的利息将累加起来，作为一笔交易记录过帐到总帐中。  
4. 展开或折叠包含部分的“记录”。
5. 单击“确定”。
6. 在“状态”字段中，选择“已过帐”。


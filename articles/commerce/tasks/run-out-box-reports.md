---
title: 生成和运行现成报表
description: 可使用此任务指南运行不同工作区中总部的现成报表和“商业”中的“查询和销售“报表。
author: ashishmsft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailCategoryAndProductWorkspace, RetailOrgHierarchyTreeLookup, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5f9931a39e4ca2141ed5b43086226c7fcc7cbd7c
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021716"
---
# <a name="generate-and-run-out-of-box-reports"></a>生成和运行现成报表

[!include[task guide banner](../includes/task-guide-banner.md)]

可使用此任务指南运行不同工作区中总部的现成报表和“商业”中的“查询和销售“报表。

创建此记录时使用的演示数据公司为 USRT。 此录制专门面向系统管理员角色。

## <a name="launch-reports-from-workspaces"></a>启动工作区中的报表
1. 转至“Retail 和 Commerce”>“产品和类别”>“类别和产品管理”。
2. 单击此箭头可展开或折叠“报表”部分。
3. 单击“排名靠前的产品报表”。
4. 在“开始日期”字段中输入日期。
5. 在“结束日期”字段中输入日期。
6. 在“渠道”字段中，单击下拉按钮以打开查找。
7. 在树结构中，请选择“Contoso Retail\Contoso Retail USA\中心\休斯顿”。
    * 这会显示“商业报告”目的的默认组织层次结构。   转至“组织管理”>“组织”>“组织层次结构目的”，选择“商业报告”，然后在“已分配层次结构”下，选中“默认”列已选中的层次结构名称。 作为演示数据的一部分（用于此任务录制），您会注意到，“商店(按地区)”是报告目的的默认组织层次结构。     
8. 单击“确定”。
9. 在“视图”字段中，选择一个选项。
10. 在“依据”字段中，选择一个选项。
11. 单击“确定”。

## <a name="launch-reports-from-the-inquiries-and-sales-reports"></a>从查询和销售报表中启动报表
1. 转至“Retail 和 Commerce”>“查询和报表”>“销售报表”>“类别销售报表”。
2. 在“开始日期”字段中输入日期。
3. 在“结束日期”字段中输入日期。
4. 在“渠道”字段中，单击下拉按钮以打开查找。
5. 在树结构中，请选择“Contoso Retail\Contoso Retail USA\西部\西雅图”。
    * 这会显示“商业报告”目的的默认组织层次结构。 转至“组织管理”>“组织”>“组织层次结构目的”，选择“商业报告”，然后在“已分配层次结构”下，选中“默认”列已选中的层次结构名称。 作为演示数据的一部分（用于此任务录制），您会注意到，“商店(按地区)”是报告目的的默认组织层次结构。     
6. 单击“确定”。
7. 单击“确定”。

## <a name="export-an-hq-reports"></a>导出 HQ 报表
1. 转至“Retail 和 Commerce”>“查询和报表”>“销售报表”>“组织销售报表”。
2. 在“开始日期”字段中输入日期。
3. 在“结束日期”字段中输入日期。
4. 单击“确定”。
5. 单击“导出”。
6. 单击 PDF。


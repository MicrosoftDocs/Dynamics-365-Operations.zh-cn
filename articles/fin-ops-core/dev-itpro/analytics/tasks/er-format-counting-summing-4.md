---
title: ER 配置格式以执行盘点和合计（第 4 部分 - 运行格式）
description: 本主题介绍如何配置电子报告格式以基于已经生成的文本输出的数据执行盘点和合计。 （第 4 部分）
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, IntrastatParameters, Intrastat, InventItemIdLookupSimple, IntrastatCommodityLookup, ERFormatMappingRunLogTable, DocuView
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5576229e8b81824dff6d0b38b8ab5483e04ade8
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092939"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4---run-format"></a>ER 配置格式以执行盘点和合计（第 4 部分 - 运行格式）

[!include [banner](../../includes/banner.md)]

以下步骤介绍指定为系统管理或电子申报开发人员角色的用户如何配置电子申报 (ER) 格式，以便基于已生成的文本输出的数据执行盘点和合计。 这些步骤可以在 DEMF 公司执行。

为了完成这些步骤，您必须首先完成“ER 配置格式以执行盘点和合计（第 3 部分：使用计算创建输出）”这一过程中的步骤。

此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a>为生成内部统计报表测试此配置
1. 转到“组织管理”>“工作区”>“电子申报”。
2. 单击“申报配置”。
3. 在树中，展开“内部统计模型”。
4. 在树中，展开“内部统计模型\内部统计 (DE)”。
5. 在树中，选择“内部统计模型\内部统计 (DE)\带盘点和合计的内部统计 (DE)”。
6. 在操作窗格上，单击“配置”。
7. 单击“用户参数”。
8. 在“运行设置”字段中选择“是”。
9. 单击“确定”。
10. 单击“编辑”。
11. 在“运行草稿”字段中选择“是”。
12. 单击“保存”。
13. 转到缴税>设置 >外贸>外贸参数。
14. 展开“电子报表”部分。
15. 选择“带盘点和合计的内部统计 (DE)”配置。
16. 选择“带盘点和合计的内部统计 (DE)”配置。
17. 单击“保存”。
18. 关闭该页面。
19. 转到“纳税”>“申报”>“外贸”>“内部统计”。
20. 单击“输出”。
21. 单击“报表”。
    * 运行内部统计报表生成过程。  
22. 在“开始日期”字段中，将日期设置为“2000-01-01”。
    * 为报表期间定期开始和结束日期，其中包含窗体交易中的现有日期。  
23. 在“结束日期”字段中，将日期设置为“2022-12-31”。
    * 为报表期间定期开始和结束日期，其中包含窗体交易中的现有日期。  
24. 在“方向”字段中，选择“到货”。
25. 在“生成文档”字段中选择“是”。
26. 单击“确定”。
    * 查看创建的输出，该输出的结尾包含汇总行。  
27. 单击“新建”。
28. 在列表中，标记所选的行。
29. 在“方向”字段中，选择“发货”。
30. 在“物料编号”字段中，输入或选择一个值。
31. 在“商品”字段中，输入或选择一个值。
32. 将“重量”设置为“10”。
33. 将“发票金额”设置为“10000”。
34. 将“统计金额”设置为“10000”。
35. 单击“输出”。
36. 单击“报表”。
37. 在“方向”字段中，选择“发货”。
38. 单击“确定”。
    * 查看创建的输出，该输出的结尾包含汇总行。 请注意，已经在与首次运行的比较中更改了它。  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a>以调试模式运行此配置以查看收集的盘点和合计数据
1. 转到“组织管理”>“电子申报”>“配置”。
2. 在树中，展开“内部统计模型”。
3. 在树中，展开“内部统计模型\内部统计 (DE)”。
4. 在树中，选择“内部统计模型\内部统计 (DE)\带盘点和合计的内部统计 (DE)”。
5. 在操作窗格上，单击“配置”。
6. 单击“用户参数”。
7. 在“在调试模式下运行”字段中选择“是”。
8. 单击“确定”。
9. 关闭该页面。
10. 转到“纳税”>“申报”>“外贸”>“内部统计”。
11. 单击“输出”。
12. 单击“报表”。
13. 单击“确定”。
14. 关闭该页面。
15. 转到“组织管理”>“电子申报”>“配置”。
16. 在树中，展开“内部统计模型”。
17. 在树中，展开“内部统计模型\内部统计 (DE)”。
18. 在树中，选择“内部统计模型\内部统计 (DE)\带盘点和合计的内部统计 (DE)”。
19. 单击“调试日志”。
    * 请注意，已经为所选配置的执行过程创建了调试日志记录。  
20. 单击“附加”。
21. 单击“打开”。
    * 查看创建的 XML 文件，其中包含执行所选配置期间收集的盘点和合计详细信息。  


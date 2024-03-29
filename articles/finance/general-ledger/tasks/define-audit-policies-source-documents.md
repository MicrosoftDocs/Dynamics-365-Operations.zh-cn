---
title: 定义原始单据的审计策略
description: 本文介绍如何设置和运行审计政策规则。
author: panolte
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b8aa106cd5a5596f6b9a6663390e03ebc3f91a7b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872519"
---
# <a name="define-audit-policies-for-source-documents"></a>定义原始单据的审计策略

[!include [banner](../../includes/banner.md)]

本文介绍如何设置和运行审计政策规则。 本例使用含酒店费用类型的费用报表。 该程序适用于 USMF 演示公司。 审计角色包含执行这些任务的正确权限。

1. 在导航窗格中，转到 **模块 > 审计工作台 > 设置 > 策略规则类型**。
2. 选择 **新建**。
3. 在 **规则名称** 字段中，输入一个值。
4. 在 **描述** 字段中，键入一个值。
5. 在 **查询名称** 字段中，选择 **支出报表行**
6. 在 **查询类型** 字段中，选择 **汇总**
7. 在 **法人** 字段中，选择 **法人**
8. 在 **文档日期引用** 字段中，选择 **已修改的日期和时间**
9. 选择 **保存**。
10. 在导航窗格中，转到 **模块 > 审计工作台 > 设置 > 审计策略**。
11. 选择 **新建**。
12. 在 **名称** 字段中，键入一个值。
13. 展开 **策略组织** 部分。
14. 在树结构中，选择 **美国 Contoso 娱乐系统**，然后选择 **添加**。
15. 在树结构中，选择 **美国 Contoso 咨询**，然后选择 **添加**。
16. 在树结构中，选择 **美国 Contoso 零售**，然后选择 **添加**。
17. 展开 **策略组织** 部分。
18. 展开 **策略规则** 部分。
19. 在列表中，查找并选择以前创建的政策规则。
20. 选择 **创建策略规则**。
21. 在 **生效日期** 字段中，输入日期和时间。
22. 选择 **筛选器**。
23. 在列表中，选择 **支出类别** 行，然后将详细信息设置为 **酒店**。
24. 在 **标准** 字段中，输入或选择一个值。
25. 选择 **汇总** 选项卡。
26. 选择 **添加**。
27. 在列表中，选择 **交易金额** 的字段值。
28. 在 **字段** 字段中，输入或选择一个值。
29. 在 **汇总功能** 字段中，选择 **合计**。
30. 选择 **分组依据** 选项卡。
31. 选择 **添加**。
32. 在列表中，选择 **员工** 值。
33. 选择 **添加**。
34. 在列表中，选择 **支出类别** 的值。
35. 在 **字段** 字段中，输入或选择一个值。
36. 选择 **具有** 选项卡。
37. 选择 **添加**。
38. 选择 **交易金额**。
39. 在 **字段** 字段中，输入或选择一个值。
40. 在 **汇总功能** 字段中，选择 **合计**。
41. 在 **标准** 字段中，输入 `>2000`。
42. 选择 **确定**。
43. 选择 **测试**。
44. 在 **文档选择开始日期** 字段，输入日期和时间。
45. 在 **文档选择结束日期** 字段，输入日期和时间。
46. 选择 **运行测试**。
47. 在操作窗格上，选择 **审计策略**。
48. 选择 **其他选项**。
49. 在 **开始日期** 字段中，输入日期和时间。
50. 在 **结束日期** 字段中，输入日期和时间。
51. 选择 **批处理**。
52. 展开 **后台运行** 部分。
53. 在 **批处理** 字段中选择 **是**。
54. 选择 **确定**。
55. 在导航窗格中，转到 **模块 > 审计工作台 > 设置 > 审计案例**。
56. 在列表中，找到并选择所需记录。
57. 展开 **关联** 部分。
58. 在列表中，找到并选择所需记录。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

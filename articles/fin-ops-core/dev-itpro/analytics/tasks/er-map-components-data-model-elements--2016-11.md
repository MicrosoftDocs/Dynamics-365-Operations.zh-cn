---
title: ER 将创建的格式的组件映射到数据模型元素（2016 年 11 月）
description: 本文介绍如何将数据模型元素映射到所创建的电子报告 (ER) 配置的组件。
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner
ms.openlocfilehash: d1dee2a26edd5a2162bb8c5cebaf014825f4e5a2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290205"
---
# <a name="er-map-components-of-the-created-format-to-data-model-elements-november-2016"></a>ER 将创建的格式的组件映射到数据模型元素（2016 年 11 月）

[!include [banner](../../includes/banner.md)]

以下过程显示属于系统管理员或电子报表开发人员的用户如何将数据模型元素映射到创建的电子申报 (ER) 配置的组件，该配置用于定义付款业务域的电子单据格式。 后面将使用此格式生成用于处理付款的电子单据。 在此示例中，您将创建示例公司“Litware 公司”的格式配置。 这些步骤适用于所有公司，因为所有公司共享 ER 配置。 为了完成这些步骤，您首先必须完成任务指南“创建格式配置”中的步骤。


## <a name="select-a-format-configuration"></a>选择格式配置
1. 转到“组织管理”>“工作区”>“电子申报”。
2. 单击“申报配置”。
3. 在树结构中，展开“付款（简化模型）”。
4. 在树结构中，选择“付款（简化模型）\BACS（英国虚构）”。
5. 单击“设计器”。

## <a name="map-format-components-to-data-model-elements"></a>映射格式部分到数据模型元素
1. 单击”展开/折叠“。
2. 单击“映射”选项卡。
3. 在树结构中，展开“模型”。
4. 在树结构中，选择“Xml\消息\处理日期\日期时间”。
5. 在树结构中，选择“模型\处理日期时间”。
6. 单击“绑定”。
7. 在树结构中，选择“Xml\消息\消息 ID\字符串”。
8. 在树结构中，选择“模型\消息标识”。
9. 单击“绑定”。
10. 在树结构中，展开“模型\付款”。
11. 在树结构中，选择“Xml\消息\付款\项\金额\字符串”。
12. 在树结构中，选择“模型\付款\指示金额”。
13. 单击“绑定”。
14. 在树结构中，选择“Xml\消息\付款\项\交易日期\日期时间”。
15. 在树结构中，选择“模型\付款\交易日期”。
16. 单击“绑定”。
17. 在树结构中，选择“Xml\消息\付款\项\描述\字符串”。
18. 在树结构中，选择“模型\付款\描述”。
19. 单击“绑定”。
20. 在树结构中，选择“Xml\消息\付款\项\货币\字符串”。
21. 在树结构中，选择“模型\付款\货币”。
22. 单击“绑定”。
23. 在树结构中，选择“Xml\消息\付款\项\ID”。
24. 在树结构中，选择“模型\付款\End2EndID”。
25. 单击“绑定”。
26. 在树结构中，展开“模型\付款\贷方”。
27. 在树结构中，展开“模型\付款\贷方\金额”。
28. 在树结构中，展开“模型\付款\贷方\代理”。
29. 在树结构中，选择“Xml\消息\付款\项\供应商\名称\字符串”。
30. 在树结构中，展开“模型\付款\贷方\名称”。
31. 单击“绑定”。
32. 在树结构中，选择“Xml\消息\付款\项\供应商\银行\银行代号\字符串”。
33. 在树结构中，选择“模型\付款\贷方\代理\银行代号”。
34. 单击“绑定”。
35. 在树结构中，选择“Xml\消息\付款\项\供应商\银行\帐号\字符串”。
36. 在树结构中，选择“模型\付款\贷方\帐户\编号”。
37. 单击“绑定”。
38. 在树结构中，选择“Xml\消息\付款\项\付款人\名称\字符串”。
39. 在树结构中，展开“模型\付款\借方”。
40. 在树结构中，展开“模型\付款\借方\金额”。
41. 在树结构中，展开“模型\付款\借方\代理”。
42. 在树结构中，展开“模型\付款\借方\名称”。
43. 单击“绑定”。
44. 在树结构中，选择“Xml\消息\付款\项\付款人\银行\银行代号\字符串”。
45. 在树结构中，选择“模型\付款\借方\代理\银行代号”。
46. 单击“绑定”。
47. 在树结构中，选择“Xml\消息\付款\项\付款人\银行\帐号\字符串”。
48. 在树结构中，选择“模型\付款\借方\帐户\编号”。
49. 单击“绑定”。
50. 在树结构中，选择“Xml\消息\付款\项”。
51. 在树结构中，选择“模型\付款”。
52. 单击“绑定”。
53. 单击“保存”。

## <a name="validate-format-mapping"></a>验证格式映射
1. 单击“验证”。
    * 验证新映射以确保所有绑定正常。  
2. 关闭该页面。

## <a name="change-status-of-the-current-version-of-format-configuration"></a>更改格式配置的当前版本状态
在下一步骤中，您将把格式配置的状态从“草稿”更改为“已完成”，以使其可用于生成付款单据。  
1. 单击“更改状态”。
2. 单击“完成”。
3. 在“描述”字段中，键入一个值。
    * 例如，“版本 1”。  
4. 单击“确定”。
5. 选择当前配置的已完成版本。
    * 请注意配置保存为已完成版本 1.1：即基于数据模型的第 1 版本的格式的第 1 版本。  

## <a name="define-effective-date-for-completed-version-of-format"></a>定义已完成格式版本的生效日期
每个格式版本可配置为从特定日期开始可供使用。 当多个格式版本在特定日期有效时，将选择使用最新格式（根据版本号）。 此会话日期值将用于选择相应的版本。  

## <a name="restrict-access-to-created-format-from-companies"></a>限制公司对创建的格式的访问
1. 展开“ISO 国家/地区代码”部分。
    * 每种格式访问可通过识别格式适用的特定国家/地区来设定限制。 如果特定格式的国家/地区列表为空，此格式可供所有公司使用。 在该国家/地区列表中插入某些 ISO 国家/地区代码时，此格式仅可以在其主要地址位于该国家/地区中的公司中使用。  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

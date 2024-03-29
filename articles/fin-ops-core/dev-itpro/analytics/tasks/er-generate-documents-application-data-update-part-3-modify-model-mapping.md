---
title: 修改模型和映射以生成包含应用程序数据的单据
description: 本文介绍如何设计报告配置以生成电子文档与更新应用程序数据。 （第 2 部分 - 生成文档）。
author: kfend
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8e94a78b9ee9821b65430b2fed179fd9f15617c1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290505"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a>修改模型和映射以生成包含应用程序数据的单据

[!include [banner](../../includes/banner.md)]

若要完成此过程中的步骤，首先必须完成“ER 使用应用程序数据更新生成单据（第 2 部分：生成单据）”这一过程。 

此过程中的步骤介绍如何设计电子申报 (ER) 配置以生成电子单据和更新应用程序数据。 在此过程中，您将修改 ER 配置以开始将其用于生成电子单据和更新应用程序数据。 此过程是为向其分配了系统管理员角色或电子申报开发人员角色的用户创建的。 可使用 DEMF 数据集完成这些步骤。


## <a name="modify-data-model"></a>修改数据模型
1. 转到“组织管理”>“电子申报”>“配置”。
2. 在树中，选择“内部统计(模型)”。
    * 您将扩展数据模型的使用方式。 除了将其用作源以生成内部统计报表，数据模型还将用于收集有关内部统计报告流程的详细信息。 然后将把此详细信息用于更新应用程序数据。   
3. 单击“设计器”。
4. 单击“新建”，以打开对话框。
5. 在“作为以下项的新节点”字段中，输入“模型根”。
6. 在“名称”字段中，键入“用于应用程序数据更新”。
    * 对于应用程序数据更新  
7. 单击“添加”。
8. 在树中，选择“用于应用程序数据更新”。
    * 将添加这个新根项以指定将来自内部统计报表（用作数据源）的数据移到应用程序表（更新目标）的数据流。 必须为获取过帐到传出单据的数据和为从用于更新应用程序数据的单据获取数据使用不同的根项。   
9. 单击“新建”，以打开对话框。
10. 在“名称”字段中，键入“存档标题”。
    * 存档标题  
11. 在“物料类型”字段中，选择“记录列表”。
12. 单击“添加”。
    * 因为您将为生成的每个内部统计报表创建一个记录，所以必须为其创建一个新项。  
13. 单击“新建”，以打开对话框。
14. 在“名称”字段中，键入“文件名”。
    * 文件名  
15. 在“物料类型”字段中，选择“字符串”。
16. 单击“添加”。
17. 单击“新建”，以打开对话框。
18. 在“名称”字段中，键入“行数”。
    * 行数  
19. 在“物料类型”字段中，选择“整数”。
20. 单击“添加”。
    * 添加此项以表示当前报告流程期间报告的内部统计交易记录数量。  
21. 单击“新建”，以打开对话框。
22. 在“名称”字段中，键入“存档行”。
    * 存档行  
23. 在“物料类型”字段中，选择“记录列表”。
24. 单击“添加”。
    * 添加此项以表示当前报告流程期间报告的内部统计交易记录列表。  
25. 单击“新建”，以打开对话框。
26. 在“名称”字段中，键入“金额”。
    * 本币金额  
27. 在“物料类型”字段中，选择“实时”。
28. 单击“添加”。
29. 单击“新建”，以打开对话框。
30. 在“名称”字段中，键入“商品记录标识”。
    * 商品记录标识  
31. 在“物料类型”字段中，选择“Int64”。
32. 单击“添加”。
33. 单击“新建”，以打开对话框。
34. 在“名称”字段中，键入“物料编号”。
    * 物料编号  
35. 在“物料类型”字段中，选择“字符串”。
36. 单击“添加”。
37. 单击“保存”。
38. 关闭该页面。

## <a name="modify-model-mapping"></a>修改模型映射
1. 在树中，展开“内部统计(模型)”。
2. 在树中，选择“内部统计(模型)\内部统计(映射)”。
    * 修改现有模型映射，以便开始讲起用于应用程序数据更新和存档内部统计报告详细信息。  
3. 单击“设计器”。
4. 单击“新建”。
5. 在“名称”字段中，键入“更新存档”。
    * 更新存档  
6. 在“方向”字段中，选择“截止目标”。
7. 单击“保存”。
    * 这个新映射指定将来自数据模型的数据（内部统计报告详细信息）移到应用程序表（更新目标）的数据流。 请注意，必须使用不同模型的根项来为报告流程从应用程序获取数据，然后将来自数据模型的数据用于应用程序数据更新。   
8. 单击“设计器”。
9. 在树结构中，选择“数据模型\数据模型”。
    * 添加所需数据源。 这是其中包含必须存档的所报告内部统计交易记录详细信息的数据模型。  
10. 单击“添加根”。
11. 在“名称”字段中，键入“模型”。
    * 模型  
12. 在“定义”字段中，输入或选择值“用于应用程序数据更新”。
    * 对于应用程序数据更新  
13. 单击“确定”。
14. 在树中，展开“模型”。
15. 在树结构中，选择“功能\计算字段”。
16. 在树中，选择“模型\存档标题”。
17. 单击“添加”。
    * 因为需要为存档枚举所报告内部统计交易记录，所以必须添加相应的数据源。  
18. 在“名称”字段中，键入“枚举行”。
    * 枚举行  
19. 单击“编辑公式”。
20. 在树中，选择“列表\ENUMERATE”。
21. 单击“添加”功能。
22. 在树结构中，展开“模型”。
23. 在树中，展开“模型\存档标题”。
24. 在树中，选择“模型\存档标题\存档行”。
25. 单击“添加数据源”。
26. 在“公式”字段中，输入“ENUMERATE(model.'Archive header'.'Archive lines')”。
    * ENUMERATE(model.'Archive header'.'Archive lines')  
27. 单击“保存”。
28. 关闭该页面。
29. 单击“确定”。
30. 单击”添加目标“。
    * 将应用程序表添加为需要更新以存档所报告内部统计交易记录详细信息的必需目标。  
31. 在“名称”字段中，键入“存档”。
    * 存档  
32. 在“表名”字段中，键入“IntrastatArchiveGeneral”。
    * IntrastatArchiveGeneral  
    * 保留记录操作“插入”，以便在存档各内部统计报告流程详细信息期间添加记录。  
33. 在“记录信息日志”字段中选择“是”。
    * 选择“是”以获取有关应用程序数据更新问题的信息。  
34. 在“跳过记录操作验证”字段中选择“是”。
    * 选择“是”以禁止有关空“内部统计存档标识”字段的验证错误。 这将在添加记录后，基于“外贸参数”窗体中为此表配置的序号完成。  
35. 单击“确定”。
    * 绑定所添加数据源（基于所选根项过滤后的模型）的元素和来自所添加目标的元素。  
36. 在树中，展开“存档”。
37. 在树中，展开“存档\<关系”。
38. 在树结构中，展开“存档\<关系\IntrastatArchiveDetail”。
39. 在树中，选择“存档\<关系\IntrastatArchiveDetail\Amount(AmountMST)”。
40. 在树中，展开“模型\存档标题\枚举行”。
41. 在树中，展开“模型\存档标题\枚举行\值”。
42. 在树中，选择“模型\存档标题\枚举行\值\金额”。
43. 单击“绑定”。
44. 在树中，选择“存档\<关系\IntrastatArchiveDetail\Commodity(IntrastatCommodity)”。
45. 在树中，选择“模型\存档标题\枚举行\值\商品记录标识”。
46. 单击“绑定”。
47. 在树中，选择“存档\<关系\IntrastatArchiveDetail\物料编号(ItemId)”。
48. 在树中，选择“模型\存档标题\枚举行\值\物料编号”。
49. 单击“绑定”。
50. 在树中，选择“存档\<关系\IntrastatArchiveDetail\行号(LineNumber)”。
51. 在树中，选择“模型\存档标题\枚举行\编号”。
52. 单击“绑定”。
53. 在树中，选择“存档\<关系\IntrastatArchiveDetail”。
54. 在树中，选择“模型\存档标题\枚举行”。
55. 单击“绑定”。
56. 在树中，选择“存档\文件名(FileName)”。
57. 在树中，选择“模型\存档标题\文件名”。
58. 单击“绑定”。
59. 在树中，选择“存档\行数(NumberOfLines)“。
60. 在树中，选择“模型\存档标题\行数”。
61. 单击“绑定”。
62. 在树中，选择“存档”。
63. 在树中，选择“模型\存档标题”。
64. 单击“绑定”。
65. 单击“保存”。
66. 关闭该页面。
67. 关闭该页面。



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

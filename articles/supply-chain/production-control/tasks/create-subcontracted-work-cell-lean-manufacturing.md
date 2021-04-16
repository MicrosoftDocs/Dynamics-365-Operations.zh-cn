---
title: 创建 lean manufacturing 的转包工作单元
description: 若要为 lean manufacturing 的转包工作建模，必须创建与提供该工作的供应商关联的工作单元。
author: cvocph
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0dc1e28202c42502cbec0f0066863d24d4396c88
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828890"
---
# <a name="create-a-subcontracted-work-cell-for-lean-manufacturing"></a>创建 lean manufacturing 的转包工作单元

[!include [banner](../../includes/banner.md)]

若要为 lean manufacturing 的转包工作建模，必须创建与提供该工作的供应商关联的工作单元。 转包工作单元通过关联供应商类型的资源链接到供应商。 如果在 USMF 演示公司播放此录制，可以选择供应商帐户 ID 1002 和站点 1。


## <a name="create-a-vendor-resource"></a>创建供应商资源
1. 转到“资源”。
2. 单击“新建”。
3. 在“资源”字段中，输入一个值。
4. 在“描述”字段中，键入一个值。
5. 在“类型”字段中选择“供应商”。
6. 在“供应商”字段中，单击下拉按钮以打开查找。

## <a name="create-the-resource-group"></a>创建资源组
1. 转到“资源组”。
2. 单击“新建”。
3. 在“资源组”字段中，键入一个值。
4. 在“描述”字段中，键入一个值。
5. 在“位置”字段中，单击下拉按钮打开查询。
    * 选择应将工作单元分配给的站点。 理论上，站点可以表示由供应商运营的一个站点。 但是在大多数情况下，转包资源仅分配给订购转包工作的站点。 请注意，转包工作单元的输入和输出仓库必须在同一个站点。  
6. 在“站点”字段中，输入一个值。
7. @SysTaskRecorder:_RequestClose
8. 选中或清除“工作单元”复选框。
9. 在“输入仓库”字段中，单击下拉按钮以打开查找。
    * 选择用于为供应商管理的工作单元暂存材料的仓库和库位。 许多情况下，通过为每个供应商使用一个单独的仓库和每个工作单元使用一个库位，为仓库和库位建模。  
10. 在“输入位置”字段中，单击下拉按钮以打开查找。
11. 在“输出仓库”字段中，单击下拉按钮以打开查找。
    * 定义过帐工作单元的转包活动时过帐材料的仓库和库位。 如果供应商报告看板作业，仓库和库位可以在供应商站点。 仓库和库位也可以在与生产流下一步关联的收货库位。  
12. 在“输出位置”字段中，单击下拉按钮以打开查找。
13. 展开或折叠“日历”部分。
14. 单击“添加”。
15. 在“日历”字段中，单击下拉按钮以打开查找。
    * 将工作单元的工作时间日历与资源组关联。 对于关键资源，我们建议您定义用于表示工作单元或供应商站点的确切工作时间和相关产能的特定日历。  
16. 展开或折叠“资源”部分。
17. 单击“添加”。
    * 转包资源组必须有供应商类型的关联资源，用于将资源组链接到供应商帐户。  
18. 在“资源”字段中，单击下拉按钮以打开查找。
    * 选择或收入您在先前的子任务中创建的供应商资源。  
19. 展开或折叠“工作单元产能”部分。
20. 单击“添加”。
    * 必须为工作单元定义产能。 在此示例中，我们创建的吞吐量产能为每个标准工作日 100 件。  
21. 在“生产流模型”字段中，单击下拉按钮以打开查找。
22. 在“产能期间”字段中，选择一个选项。
23. 在“平均吞吐量”字段中，输入一个数字。
24. 在“单位”字段中，单击下拉按钮以打开查找。
25. ResolveChanges 单位。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
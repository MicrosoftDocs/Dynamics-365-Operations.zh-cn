---
title: "设置管理的先决条件"
description: "使用此过程可以启用未达标管理流程。"
author: perlynne
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: e8f7ec305316b5290019ec28deed1cae382e93b3
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-prerequisites-for-management"></a>设置管理的先决条件

[!include[task guide banner](../../includes/task-guide-banner.md)]

使用此过程可以启用未达标管理流程。 未达标描述存在质量问题的过程或物料，有关的描述性信息将包括问题的来源和类型。 此过程使用演示数据公司 USMF。 此过程通常由质量经理执行。


## <a name="enable-quality-management-processes-within-the-company"></a>在公司内启用质量管理流程
1. 转到“库存管理”>“设置”>“库存和仓库管理参数”。
2. 单击“质量管理”选项卡。
3. 在“使用质量管理”字段中，选择“是”。
    * 选择此参数以启用公司的质量管理流程。  
4. 在“小时工资率”字段中，输入一个数字。
    * 使用“小时工资率”字段用本币输入人工小时工资率。 小时工资率用于计算与未达标相关的工序的成本。 小时工资率和计算的成本为未达标提供了参考信息，并且它们不与其他功能交互。  
5. 单击“报表设置”。
    * 此页面允许您定义将在不同类型的质量管理报表上使用的质量报表注释类型。  
6. 关闭该页面。
7. 关闭该页面。

## <a name="enable-user-for-nonconformance-processing"></a>支持用户进行未达标处理
1. 转到“系统管理”>“用户”>“用户”。
    * 若要处理未达标的审核，审核或拒绝未达标的用户必须有在用户页分配的“名称”值。 若要使用文档注释，用户还必须具有在用户选项内启用的“文档处理”。  
2. 使用“快速筛选器”以查找记录。 例如，在“姓名”字段中筛选值 'Ricardo'。
    * 使用筛选器查找将审核或拒绝未达标记录的用户。  
3. 在列表中，单击所选行中的链接。
    * 若要处理未达标的审核，确保审核或拒绝未达标的用户具有在用户页分配的“名称”值。  
4. 单击“用户选项”。
5. 单击“首选项”选项卡。
6. 在“启用文档处理”字段中选择“是”。
    * 若要使用文档注释，用户还必须具有在用户选项内启用的“文档处理”。  
7. 关闭该页面。
8. 关闭该页面。
9. 关闭该页面。

## <a name="define-diagnostic-types-for-nonconformance-processing"></a>定义未达标处理的诊断类型
1. 转到“库存管理”>“设置”>“质量管理”>“诊断类型”。
    * 使用诊断类型页定义诊断操作的分类。 更正标识应对已审核的未达标采取的诊断操作类型、应该执行更改的用户，以及请求和计划的完成日期。  
2. 单击“新建”。
3. 在“诊断”字段中，键入一个值。
4. 在“描述”字段中，键入一个值。
5. 关闭该页面。

## <a name="define-quality-charges-for-nonconformance-processing"></a>定义未达标处理的质量费用
1. 转到“库存管理“>”设置“>”质量管理“>”质量费用”。
    * 使用质量费用页定义将在未达标相关工序中使用的费用的分类。  
2. 单击“新建”。
3. 在“费用代码”字段中，输入一个值。
4. 在“描述”字段中，键入一个值。
5. 关闭该页面。

## <a name="define-the-operations-for-nonconformance-processing"></a>定义未达标处理的工序
1. 转到“库存管理”>“设置”>“质量管理”>“工序”。
    * 使用工序页定义可以对已审核的未达标执行的工作的分类。 在将工序与未达标关联时，您可以定义有关执行该工序所需的关联物料、工时和杂项费用的信息。 这些信息为计算执行该工序所需的预估成本奠定了基础。  
2. 单击“新建”。
3. 在“工序”字段中，键入一个值。
4. 在“描述”字段中，键入一个值。
5. 关闭该页面。

## <a name="define-problem-types-for-nonconformance-processing"></a>定义未达标处理的问题类型
1. 转到“库存管理”>“设置”>“质量管理”>“问题类型”。
    * 使用问题类型页定义各类未达标类型遇到的质量问题分类。 未达标类型包括内部、客户、供应商、服务请求、生产和联产品生产。 一个问题类型可与多个未达标类型关联。  
2. 单击“新建”。
3. 在“问题类型”字段中，键入一个值。
4. 在“描述”字段中，键入一个值。
5. 单击“未达标类型”。
    * 使用未达标类型页来授权一个或多个未达标类型的问题类型的使用。 例如，有关缺陷代码的问题类型可适用于所有未达标类型，而有关客户投诉的问题类型只能适用于客户和服务请求未达标类型。  
6. 单击“新建”。
7. 在列表中，标记所选的行。
8. 在“未达标类型”字段中，选择一个选项。
9. 关闭该页面。
10. 关闭该页面。

## <a name="define-quarantine-zones-for-nonconformance-processing"></a>定义未达标处理的检验区域
1. 转到“库存管理“>”设置“>”质量管理“>”检验区域”。
2. 单击“新建”。
3. 在“检验区域”字段中，键入一个值。
4. 在“描述”字段中，键入一个值。
5. 关闭该页面。


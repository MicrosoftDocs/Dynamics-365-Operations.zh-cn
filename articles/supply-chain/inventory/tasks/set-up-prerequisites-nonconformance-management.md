---
title: 设置不符合项管理的先决条件
description: 使用此主题可以启用未达标管理流程。
author: perlynne
manager: tfehr
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, SysUserManagement, SysUserSetup, InventTestDiagnosticType, InventTestMiscCharges, InventTestOperation, InventProblemType, InventProblemTypeSetup, InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 80a7ae2249179c561d03f7b729ebb942ba856046
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4961495"
---
# <a name="set-up-prerequisites-for-nonconformance-management"></a>设置不符合项管理的先决条件

[!include [banner](../../includes/banner.md)]

使用此主题可以启用未达标管理流程。 未达标描述存在质量问题的过程或物料，有关的描述性信息将包括问题的来源和类型。 此过程使用演示数据公司 USMF。 此过程通常由质量经理执行。


## <a name="enable-quality-management-processes-within-the-company"></a>在公司内启用质量管理流程
1. 在导航窗格中，转到 **模块 > 库存管理 > 设置 > 库存和仓库管理参数**。
2. 选择 **质量管理** 选项卡。
3. 在 **使用质量管理** 字段中选择 **是** 以便为公司启用质量管理流程。
4. 在 **小时工资率** 字段中用本币输入一个数字。 小时工资率用于计算与未达标相关的工序的成本。 小时工资率和计算的成本为未达标提供了参考信息，并且它们不与其他功能交互。  
5. 萱蕚 **报表设置** 以定义将在不同类型的质量管理报表上使用的质量报表注释类型。

## <a name="enable-user-for-nonconformance-processing"></a>支持用户进行未达标处理
1. 在导航窗格中，转到 **模块 > 系统管理 > 用户 > 用户**。 
2. 使用快速筛选器查找将审核或拒绝未达标记录的用户。 例如，使用值 `Ricardo` 在 **名称** 字段中进行筛选。 若要处理未达标的审核，审核或拒绝未达标的用户必须有在 **用户** 页分配的“名称”值。 若要使用文档注释，用户还必须具有在用户选项内启用的“文档处理”。  
3. 标记所需记录的行。
4. 选择 **用户选项**。
5. 选择 **首选项** 选项卡。
6. 在 **启用文档处理** 字段中选择 **是**。

## <a name="define-diagnostic-types-for-nonconformance-processing"></a>定义未达标处理的诊断类型
1. 在导航窗格中，转到 **模块 > 库存管理 > 设置 > 质量管理 > 诊断类型**。 使用 **诊断类型** 页定义诊断操作的分类。 更正标识应对已审核的未达标采取的诊断操作类型、应该执行更改的用户，以及请求和计划的完成日期。  
2. 选择 **新建**。
3. 在 **诊断** 字段中，键入一个值。
4. 在 **描述** 字段中，键入一个值。

## <a name="define-quality-charges-for-nonconformance-processing"></a>定义未达标处理的质量费用
1. 在导航窗格中，转到 **模块 > 库存管理 > 设置 > 质量管理 > 质量费用**。 使用 **质量费用** 页定义将在未达标相关工序中使用的费用的分类。  
2. 选择 **新建**。
3. 在 **费用代码** 字段中，输入一个值。
4. 在 **描述** 字段中，键入一个值。

## <a name="define-the-operations-for-nonconformance-processing"></a>定义未达标处理的工序
1. 在导航窗格中，转到 **模块 > 库存管理 > 设置 > 质量管理 > 工序**。 使用 **工序** 页定义可以对已审核的未达标执行的工作的分类。 在将工序与未达标关联时，您可以定义有关执行该工序所需的关联物料、工时和杂项费用的信息。 这些信息为计算执行该工序所需的预估成本奠定了基础。  
2. 选择 **新建**。
3. 在 **工序** 字段中，键入一个值。
4. 在 **描述** 字段中，键入一个值。

## <a name="define-problem-types-for-nonconformance-processing"></a>定义未达标处理的问题类型
1. 在导航窗格中，转到 **模块 > 库存管理 > 设置 > 质量管理 > 问题类型**。 使用 **问题类型** 页定义各类未达标类型遇到的质量问题分类。 未达标类型包括 **内部**、**客户**、**供应商**、**服务请求**、**生产** 和 **联产品生产**。 一个问题类型可与多个未达标类型关联。  
2. 选择 **新建**。
3. 在 **问题类型** 字段中，键入一个值。
4. 在 **描述** 字段中，键入一个值。
5. 选择 **不符合项类型**。 使用 **不符合项类型** 页来授权一个或多个不符合项类型的问题类型的使用。 例如，有关缺陷代码的问题类型可适用于所有未达标类型，而有关客户投诉的问题类型只能适用于客户和服务请求未达标类型。  
6. 选择 **新建**。
7. 在新行的 **不符合项类型** 字段中，选择一个选项。

## <a name="define-quarantine-zones-for-nonconformance-processing"></a>定义未达标处理的检验区域
1. 在导航窗格中，转到 **模块 > 库存管理 > 设置 > 质量管理 > 检验区域**。
2. 选择 **新建**。
3. 在 **检验区域** 字段中，键入一个值。
4. 在 **描述** 字段中，键入一个值。
5. 关闭该页面。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
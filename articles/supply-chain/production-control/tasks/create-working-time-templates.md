---
title: 创建工作时间模板
description: 工作时间模板定义一周内的工作时间，可用于生成一段时期的工作时间。
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed1981b7c1427c902f237f0aa95f63e89bc345ab
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920920"
---
# <a name="create-working-time-templates"></a>创建工作时间模板

[!include [banner](../../includes/banner.md)]

工作时间模板定义一周内的工作时间，可用于生成一段时期的工作时间。 该过程说明如何使用对工作时间间隔进行分类的工作时间计划属性定义工作时间模板。 您可以使用演示数据公司 USMF 或您自己的数据浏览此程序。

1. 转到 **工作区 > 资源生命周期管理**。
1. 选择 **工作时间模板**。

## <a name="create-working-time-template"></a>创建工作时间模板

1. 选择 **新建**。
1. 在 **工作时间模板** 字段中，键入一个值。
1. 在 **名称** 字段中，键入一个值。
1. 展开 **星期一** 部分。
1. 选择 **添加**。
1. 在 **开始** 字段中，输入一个时间。
    * 指定上午开始工作的时间。  
1. 在 **结束** 字段中，输入一个时间。
    * 指定工作人员的午餐时间。  
1. 选择 **添加**。
1. 在 **开始** 字段中，输入一个时间。
    * 指定午餐后重新开始工作的时间。  
1. 在 **结束** 字段中，输入一个时间。
    * 指定工作日结束的时间。  

## <a name="replicate-working-times-to-all-week-days"></a>复制工作时间到所有工作日

1. 选择 **复制日**。
    * 复制星期一的工作时间定义到星期二。  
1. 选择 **确定**。
1. 选择 **复制日**。
    * 复制星期一的工作时间定义到星期三。  
1. 在 **结束工作日** 字段中，选择一个选项。
1. 选择 **确定**。
1. 选择 **复制日**。
    * 复制星期一的工作时间定义到星期四。  
1. 在 **结束工作日** 字段中，选择一个选项。
1. 选择 **确定**。
1. 选择 **复制日**。
    * 复制星期一的工作时间定义到星期五。  
1. 在 **结束工作日** 字段中，选择一个选项。
1. 选择 **确定**。

## <a name="define-time-slots-for-special-operations"></a>定义特殊操作的时隙

1. 展开 **星期五** 部分。
1. 在列表中，找到并选择所需记录。
1. 在 **属性** 字段中，输入或选择一个值。
1. 在列表中，找到并选择所需记录。
1. 在 **属性** 字段中，输入或选择一个值。

## <a name="mark-weekend-days-as-closed-for-pickup"></a>标记周末为装货关闭的时间

1. 展开 **星期六** 部分。
1. 在 **停止装货** 字段中选择 *是*。
1. 展开 **星期日** 部分。
1. 在 **停止装货** 字段中选择 *是*。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: "不符合项管理"
description: "本文介绍使用未达标所需的基本设置。 如果要使用质检订单还需要其他设置。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 28951
ms.assetid: a62d4ba8-eebc-4b14-b587-630be7298522
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4aebabfc6160393e5c817cd07af835d3b1268c2e
ms.contentlocale: zh-cn
ms.lasthandoff: 05/25/2017


---

# <a name="nonconformance-management"></a>不符合项管理

[!include[banner](../includes/banner.md)]


本文介绍使用未达标所需的基本设置。 如果要使用质检订单还需要其他设置。 

要启用未达标管理，请执行以下步骤：

1.  定义与未达标有关的库存和仓库管理参数：
    -   将**使用质量管理**选项设置为**是**。
    -   在**小时工资率**字段中用本币输入人工小时工资率。 小时工资率用于计算与未达标相关的工序的成本。 小时工资率和计算的成本为未达标提供了参考信息。 它们不与其他功能交互。
    -   使用**报表设置**页上的**质量管理**选项卡定义要打印的单据类型。 您可以打印未达标报表，未达标标记或更正报表。 您可以定义多个记录在报表上打印不同的文档类型，或打印内部和外部注释。 您可能发现使用**单据类型**页为未达标并且更正的唯一单据类型来定义唯一的文档类型很有帮助。 例如，要通过未达标的唯一单据类型，输入与未达标有关的注释。 在这种情况下，请在报表选项中确定唯一单据类型。
    -   启用未达标和更正参考的编号规则。

2.  支持用户审核未达标。 使用**用户**页的**姓名**字段向必须审核未达标的每个用户分配员工。 系统将使用更改未达标的状态以跟踪未达标历史记录的员工。 除非用户被分配员工标识符，否则他们无法审核未达标。
3.  定义将分配给未达标的问题类型。 使用**问题类型**页定义各类未达标类型遇到的质量问题分类。 您可以设置以下未达标类型：**内部**、**客户**、**供应商**、**服务请求**、**生产**和**联产品生产**。 使用**未达标类型**页来授权用于一个或多个未达标类型的问题类型。 例如，关于缺陷代码的问题类型可能适用于所有未达标类型，而有关客户投诉的问题类型可能只适用于**客户**和**服务请求**未达标类型。
4.  定义检验区域，提供有关应处理的有缺陷物料的准则。 使用**检验区域**页定义可以分配给未达标的区域。 打印的未达标标记将显示分配的检验区域和有关使用的信息，以提供有关如何处理有缺陷物料的指导。 这些区域可以与库存库位或运营资源对应。
5.  定义将分配给更正的诊断类型。 使用**诊断类型**页定义诊断操作的分类。 更正指定应对已审核的未达标采取的诊断操作类型以及应该执行操作的用户。 它还指定请求的完成日期和计划的完成日期。
6.  定义将分配给未达标的相关工序。 使用**工序**页定义可以对已审核的未达标执行的工作的分类。 向未达标分配相关工序时，可以提供详细信息，如有关执行该工序所需的关联物料、工时和杂项费用的信息。 此信息用于计算工序的估计成本。 这些详细信息和预估成本用于参考。 针对质量的相关工序不同于可以为生产工艺路线定义的工序。


<a name="see-also"></a>请参阅
--------

[创建和处理未达标（任务指南）](https://ax.help.dynamics.com/en/wiki/create-and-process-a-nonconformance/)

[质量管理流程](quality-management-processes.md)

[设置不符合项管理的先决条件（任务指南）](https://ax.help.dynamics.com/en/wiki/set-up-prequisites-for-nonconformance-management/)





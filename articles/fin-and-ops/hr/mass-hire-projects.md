---
title: "大批雇用项目"
description: "大型雇用项目允许人力资源专员创建多个职位，并且高效地为这些职位雇用工作人员。"
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HRMMassHireProject
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 7481
ms.assetid: 5f5eb271-76eb-4305-bd1c-5d171dafccc9
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 0904db82b006f874594881afdb5d568afff575eb
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="mass-hire-projects"></a>大批雇用项目

[!include[banner](../includes/banner.md)]


大型雇用项目允许人力资源专员创建多个职位，并且高效地为这些职位雇用工作人员。

<a name="overview"></a>概览
--------

当您一次雇用多个工作人员时，使用大批雇用项目，例如在您满足季节性需求而大量雇用员工时。 创建成批雇用项目便十分有用，因为您可以同时创建职位记录、工作人员记录和职位的工作人员分配。 在您创建大批雇用项目的位置时，您可以指定以下信息：
-   要创建的职位数
-   将为这些职位雇用人员的工作类型
-   部门和作业与这些职位关联
-   职位的全职等效值

## <a name="example"></a>示例
在夏季，您通常雇用 15-20 个兼职大学生在您公司填充可用实习。 本年度，您想要雇用 5 个会计、5 个订单处理人员和 5 个出纳。 而不是单独创建每个位置记录和工作人员记录，您创建一个称为“SummerInterns”的大批雇用项目。 项目的开始日期和结束日期与您为大批雇用项目创建的职位的职位持续时间的开始日期和结束日期关联。 

在**大批雇用项目**页上，选择“SummerInterns”项目然后单击**打开项目**。 在打开大批雇用项目中，单击**创建职位**并输入有关会计位置的信息。 您可以指示应使用同一信息为每个职位创建的五种会计职位，然后单击“确定”。 对订单处理人员和出纳职位重复此过程。 

在为实习职位选择要雇用的学员后，您可以在**职位详细信息**中为您雇用学生所从事的职位输入每个学生的信息。 在输入所有职位详细信息后，请选择“大批雇用项目”页的职位，然后单击**雇用**。 将为每个职位创建职位记录，然后将创建某一工作人员记录并将其分配到您雇用的每个人员的正确职位。

## <a name="mass-hire-project-statuses"></a>成批雇用项目状态
大批雇用项目可以具有以下状态。
-   创建时间
-   未完成
-   已结束

在**大批雇用项目**页，单击**打开项目**或**关闭项目**以更改大批雇用项目的状态。 下表描述了针对项目状态可以对不同的项目进行的操作。

<table>
<thead>
<tr class="header">
<th>状态</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>创建时间</td>
<td>您可以创建和修改信息，但不能为项目创建职位。 这是新项目的默认状态。</td>
</tr>
<tr class="even">
<td>未完成</td>
<td>您可以修改项目详细信息，为大批雇用项目创建职位，并为该职位雇用人员。 这是有效项目的状态。</td>
</tr>
<tr class="odd">
<td>已结束</td>
<td>您无法将这些职位添加到该项目。 若要将这些职位添加到大批雇用项目，请再次打开该项目。 这是已完成项目的状态。
<div class="alert">
<table>
<thead>
<tr class="header">
<th><strong>注意</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>在关闭大批雇用项目之前，项目中所有职位的状态必须是“已创建”或“已关闭”。</td>
</tr>
</tbody>
</table>
</div></td>
</tr>
</tbody>
</table>

 







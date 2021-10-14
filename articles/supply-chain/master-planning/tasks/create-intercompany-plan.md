---
title: 创建内部公司计划
description: 此过程显示如何创建内部公司计划。
author: ChristianRytt
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ef1484e6925427454f819a5effdc911f762b48b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578264"
---
# <a name="create-an-intercompany-plan"></a>创建内部公司计划

[!include [banner](../../includes/banner.md)]

此过程显示如何创建内部公司计划。 创建此程序的演示数据公司是 USMF。

## <a name="set-up-an-intercompany-planning-group"></a>设置内部公司计划组

1. 在 **导航窗格** 中，转到 **模块 > 主计划 > 设置 > 内部公司计划组**。
2. 使用“快速筛选器”以查找记录。 例如，使用值“10”在“名称”字段中进行筛选。
3. 在列表中，标记所选的行。
4. 选择 **删除**。 必须执行此步骤，才能缩短运行的内部公司计划。   内部公司计划将从最低计划序列开始在运行计划组中的所有公司运行主计划。  
5. 选择 **是**。
6. 关闭该页面。

## <a name="create-an-intercompany-master-plan"></a>创建内部公司主计划

1. 在 **导航窗格** 中，转到 **模块 > 主计划 > 工作区 > 主计划**。
2. 选择 **内部公司主计划**。  
3. 在 **内部公司计划组** 字段中，选择下拉按钮以打开查找。
4. 在列表中，选择所选择行中的链接。 选择内部公司计划组 10。  
5. 在 **内部公司计划迭代数** 中，输入“2”。 内部公司计划组 10 有两个成员。 若要将延迟从源公司 (USMF) 传播到客户公司 (DEMF)，需要在两个公司内两次运行内部公司。 第一个迭代将传播需求，并在源公司 (USMF) 中识别延迟。 第二个迭代将把延迟从 USMF 传播到 DEMF。  
6. 在 **第一个迭代** 字段中，选择“重新生成”。
7. 在 **后面的迭代** 字段中，选择“重新生成”。
8. 在 **线程数** 字段中，输入一个数字。 这表示用于计划的并行线程数。  
9. 选择 **确定**。

## <a name="view-the-result-of-the-plan"></a>查看计划的结果

1. 在 **计划** 字段中，选择下拉按钮以打开查找。
2. 在列表中，选择所选择行中的链接。 选择 StaticPlan 的链接。 您需要是 USMF 公司的。  
3. 选择 **计划订单**。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
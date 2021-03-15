---
title: 下达生产订单
description: 此程序显示了如何发放生产订单。
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmRelease, SrsReportViewerForm, ProdSetupRelease
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 82a8316014d28f1c31343a2e54038fc93623cd70
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966247"
---
# <a name="release-a-production-order"></a>下达生产订单

[!include [banner](../../includes/banner.md)]

此程序显示了如何发放生产订单。 创建此程序的演示数据公司是 USMF。 这是解释生产订单周期七个程序中的第四个程序。

1. 转到“生产控制”>“生产订单”>“全部生产订单”。
    * 在网格中，选择具有“已计划”状态的生产订单。  
2. 在“操作窗格”中，单击“生产订单”。
3. 单击“发放”。
    * 在此页面，您可以确认发放选择的范围的生产订单。 如果您想要添加订单，单击“选择”。  
    * 发放步骤指示何时向生产车间发放生产订单，以便车间操作员可以报告生产作业的进度。 可以发放包含有关处理作业的相关信息的生产文件。 对于为仓库流程设置的物料，会生成原材料领料的仓库工作。  
4. 单击“常规”选项卡。
    * 选择应打印的生产报表。 作业卡报表打印每个已计划作业的页面并要求生产订单按照作业水平进行计划。 报表包含计划开始和结束时间、要生产的数量以及用于处理作业的资源的相关信息。 工艺路线作业报表收集同一页面的相同信息，但是并不会打印每个作业的页面。 工艺卡报表仅显示操作，而不显示作业。 因此，此报表并不要求作业计划，而当生产订单按操作等级计划时可以使用它。  
5. 单击“打印工艺卡”复选框。
6. 单击“确定”。
7. 关闭该页面。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
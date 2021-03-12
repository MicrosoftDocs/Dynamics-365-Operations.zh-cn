---
title: 配置和运行作业以过帐报表
description: 此程序会逐步演示如何配置和运行某一重复批处理作业，以过帐选定商店或商店组的报表。
author: josaw1
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bed4cfb4875231d11ad76e4403c7995519d56e73
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003670"
---
# <a name="configure-and-run-job-to-post-statements"></a>配置和运行作业以过帐报表

[!include [banner](../includes/banner.md)]

此程序会逐步演示如何配置和运行某一重复批处理作业，以过帐选定商店或商店组的报表。 此程序使用 USRT 演示数据公司。

1. 转至“所有工作区”> > 商店财务。
2. 单击“成批过帐对帐单”。
    * 选择一个组织层次结构，然后在组织节点树结构中，选择一个商店或节点。 如果您想要为一组商店创建批处理作业，选择一个节点。  
    * 单击箭头以添加您的选择。  
3. 单击“在后台运行”选项卡。![在后台运行](../dev-itpro/media/runbackground.png "在后台运行") 
4. 选中或取消选中“批处理”复选框。
![批处理](../dev-itpro/media/batchprocessing.png "批处理和重复执行") 
5. 单击“再循环”。
6. 在“开始日期”字段中，输入一个日期。
7. 在“开始时间”字段中，输入时间。
    * 选择您是否想要在特定运行数量或特定日期之后结束重复，或从不结束重复。 然后选择不同选项，以定义您希望作业的运行频率是什么。  
8. 单击“确定”。
9. 单击“确定”。


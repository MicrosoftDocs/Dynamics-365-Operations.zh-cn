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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f89203850b302b769b22920fa5c42d2b0b877684
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410518"
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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
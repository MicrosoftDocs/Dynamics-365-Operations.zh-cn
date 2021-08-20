---
title: 配置和运行作业以计算报表
description: 此程序会逐步演示如何配置和运行重复批处理作业，以创建和计算选定商店或商店组的报表。
author: josaw1
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ecbc35cabced37a51ecedcd3f37bff2f23c093e184607b0c4d57ae9e70ae2c75
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751511"
---
# <a name="configure-and-run-job-to-calculate-statements"></a>配置和运行作业以计算报表

[!include [banner](../includes/banner.md)]

此程序会逐步演示如何配置和运行重复批处理作业，以创建和计算选定商店或商店组的报表。 此程序使用 USRT 演示数据公司。

1. 转至“所有工作区”>“商店财务”。
2. 单击“计算报表”。
    * 如果您想要为一组商店创建批处理作业，选择一个特定商店或一个节点。  
    * 单击箭头以添加您的选择。  
3. 单击“后台运行”选项卡。
4. 在“批处理”之下，选择“是”。
5. 单击“再循环”。
6. 在“开始日期”字段中，输入一个日期。
7. 在“开始时间”字段中，输入时间。
8. 选择“无结束日期”选项。
9. 在“PatternUnit”字段中，输入“天数”。
10. 在“每”字段中，输入一个数字。
11. 单击“确定”。
12. 单击“确定”。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
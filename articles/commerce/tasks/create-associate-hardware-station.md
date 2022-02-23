---
title: 创建和关联硬件工作站
description: 此程序会逐步演示如何创建新的硬件工作站。
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailHardwareStation, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: adbd5ef1cafe778cf897aafb05c77fca89be3e20
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964912"
---
# <a name="create-and-associate-a-hardware-station"></a>创建和关联硬件工作站

[!include [banner](../includes/banner.md)]

此程序会逐步演示如何创建新的硬件工作站。 新硬件配置文件将被创建和用于添加新的硬件工作站到预定义的商店（渠道）。 此程序使用 USRT 演示数据公司。

1. 转至“商业要素”>“渠道”> > > >”硬件工作站配置文件“。
2. 单击“新建”。
3. 在“硬件工作站 ID”字段中，输入“TestHWProfile”。
4. 在“名称”字段中，键入一个值。
5. 在“端口编号”字段中，输入一个数字。
6. 在“硬件配置文件”字段中，单击下拉按钮以打开查找。
7. 在列表中，找到并选择所需记录。
8. 在列表中，单击所选行中的链接。
9. 在“包装名称”字段中，单击下拉按钮以打开查找。
10. 在列表中，单击所选行中的链接。
    * 这是随新环境提供的标准包装。 版本号可能有所不同。  
11. 单击“保存”。
12. 关闭该页面。
13. 转至“Retail 和 Commerce”>“渠道”>“所有商店”。
14. 在列表中，选择行 17。
    * 如果您正使用 USRT 演示数据公司，则是休斯敦商店。  
15. 在列表中，单击所选行中的链接。
16. 切换“硬件工作站”部分的扩展项。
17. 单击“添加”。
18. 在列表中，标记所选的行。
19. 在“配置文件 ID”字段中，单击下拉按钮以打开查找。
20. 在列表中，找到并选择所需记录。
    * 这必须是前面步骤中创建的新硬件工作站配置文件。  
21. 在列表中，单击所选行中的链接。
22. 在“主机名称”字段中，输入一个值。
23. 在“EFT 终端 ID”字段中，输入一个值。
24. 单击“保存”。


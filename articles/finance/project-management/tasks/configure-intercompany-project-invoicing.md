---
title: 配置内部公司项目开票
description: 此主题显示如何设置贵组织内部两个公司之间的项目开票。
author: KimANelson
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 31dbae2d37aefe1841fe85cb6caf185c78596e55
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144271"
---
# <a name="configure-intercompany-project-invoicing"></a>配置内部公司项目开票

[!include [banner](../../includes/banner.md)]

此主题显示如何设置贵组织内部两个公司之间的项目开票。 此任务使用 USSI 数据集。

1. 在导航窗格中，转到**模块 > 应付帐款 > 供应商 > 所有供应商**。
2. 在**所有供应商**列表中，找到并选择所需记录。
3. 在操作窗格上，选择**常规**。
4. 选择**内部公司**。
5. 将**有效**设置为**是**以启用内部公司贸易。
6. 在**客户公司**字段中，输入或选择一个值。
7. 在**我的帐户**字段中，输入或选择一个值。
8. 选择**保存**。
9. 关闭页面将返回到主页。
10. 在导航窗格中，转到**模块 > 项目管理和核算 > 设置 > 项目管理与核算参数**。
11. 选择**内部公司**选项卡。
12. 将滑块移到**是**以启用公司间资源计划编制和工时单。
13. 在列表中，标记所选的行。
14. 选择**新建**。
15. 在**借人方法人**字段中，输入或选择一个值。
16. 选中**应计收入**复选框。
17. 在**默认工时单类别**字段中，输入或选择一个值。
18. 在**默认费用类别**字段中，输入或选择一个值。
19. 选择**保存**。
20. 关闭该页面。
21. 在导航窗格中，转到**模块 > 项目管理与核算 > 设置 > 过帐 > 分类帐过帐设置**。
22. 在**会计科目类型**字段中，选择一个选项。
23. 选择**新建**。
24. 在新行的**主科目**字段中，指定所需值。
25. 选择**保存**。
26. 关闭该页面。
27. 在导航窗格中，转到**模块 > 项目管理与核算 > 设置 > 价格 > 转让价格**。
28. 选择**新建**。
29. 在**生效日期**字段中，输入日期。
30. 在**借人方法人**字段中，输入或选择一个值。
31. 在**转让价格模型**字段中，选择一个选项。
32. 在**定价**字段中输入数字。
33. 选择**保存**。


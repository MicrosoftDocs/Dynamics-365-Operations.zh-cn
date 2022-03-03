---
title: 订阅计费概述
description: 本主题介绍 Microsoft Dynamics 365 Finance 中的订阅计费。
author: JodiChristiansen
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustVendExternalItem
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-02-09
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: b94ac36e49d55ad42909877d77903cd40cb22cbe
ms.sourcegitcommit: 6102f70d4595d01b90afe5b23dfd8ec2ea030653
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/16/2022
ms.locfileid: "8182673"
---
# <a name="subscription-billing-overview"></a>订阅计费概述

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

订阅计费使组织能够通过计费计划管理订阅收入商机和定期计费。 复杂的定价和计费模型以及收入分配将变得很容易管理，将在行级别进行计费和确认。 多元素收入分配使收入分配符合国际会计准则（国际财务报告准则 15 \[IFRS 15\]）和美国公认会计准则 (US GAAP) 的标准（会计准则编纂专题 606 \[ASC 606\]）。

此解决方案具有三个可独立使用的模块。 或者，可以同时使用所有三个模块。

- **定期合同计费** – 此模块支持定期计费和价格管理，以提供对定价和计费参数、合同续签和合并发票的控制。
- **收入和支出延期** – 此模块通过管理收入和支持实时了解每月定期收入，消除了手动流程和对外部系统的依赖。
- **多元素收入分配** – 此模块通过处理多个物料的定价和收入分配来帮助实现收入合规。

订阅计费通过 **功能管理** 启用。 但是，它不能与 **收入确认** 功能一起使用。 因此，您必须先禁用该功能，然后才能启用订阅计费。

1. 在 **功能管理** 工作区的 **全部** 选项卡上，在筛选器中输入 **收入确认**，然后选择功能名称作为筛选器。
2. 选择 **收入确认** 功能，然后选择 **禁用** 按钮。
3. 在 **功能名称** 筛选器中，输入 **订阅计费**，然后选择模块筛选器。
4. 选择 **订阅计费** 功能，然后选择 **启用**。
5. 从上一个列表中选择三个模块之一，然后选择 **启用**。 对其他两个模块中的每个模块重复此步骤。

    > [!IMPORTANT]
    > 必须先启用 **订阅计费** 功能，然后才能启用这三个模块中的任何一个。

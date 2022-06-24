---
title: 设置物料到达概览配置文件
description: 本文重点介绍到货概览配置文件的设置。
author: yufeihuang
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8517710f5d0be1859f86449152712d950281769a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871998"
---
# <a name="set-up-an-item-arrival-overview-profile"></a>设置物料到达概览配置文件

[!include [banner](../../includes/banner.md)]

本文重点介绍到货概览配置文件的设置。 到货概览配置文件是用户打开到货概览页面时将应用的规则的集合。 您可以在演示数据公司 USMF 中使用此过程。 此过程通常由验收员完成。

1. 在导航窗格中，转到 **模块 > 库存管理 > 设置 > 配送 > 到货概览配置文件**。
2. 选择 **新建**。 由于您几乎总是操作相同仓库的整车卸货，您应创建到货概览资料，以简化收到物料的登记流程。  
3. 在 **到货概览配置文件名称** 字段中，键入一个值。
4. 在 **显示行** 字段中，选择一个选项。 选择要针对收货显示的行：  

    - **全部** - 显示所有行，而不考虑状态。   
    - **在进行中** – 显示进度为“完成”或“部分”的收货的行。 这意味着，对于每个行，已在到达日记帐中登记全部数量或部分数量。   
    - **未完成** – 显示进度为“无”或“部分”的收货的行。 这意味着，对于每个行，没有在到达日记帐中登记数量或仅登记部分数量。  

5. 展开或收起 **到货选项** 部分。
6. 在 **提前天数** 字段中，键入一个值。 这设置了筛选器，以显示预期在接下来几天内（取决于您设置的数字）收到的收据行。  
7. 在 **延迟天数** 字段中，键入一个值。 这设置了筛选器，以显示在今天之前的几天内收到的收据行。  
8. 在 **仓库** 字段中，键入一个值。 一个或多个仓库筛选器。  
9. 在 **交货方式** 字段中，选择一个值。 它可设置一个筛选器以仅显示带此“交货方式”的收据行。  
10. 在 **名称** 字段中选择 WHS。
11. 在 **仓库** 字段中，选择仓库 24。 这是默认仓库，将用于使用此模板的已登记的收据行。  
12. 在 **库位** 字段中，选择 **Baydoor**。 这是默认位置，将用于使用此模板的已登记的收据行。  
13. 展开或折叠 **到货查询详细信息** 部分。
14. 在 **限制到站点** 字段中，选择站点 2。 它可设置一个筛选器以仅显示带此站点的收据行。  
15. 将 **采购订单** 选项设置为 **是**。 从采购订单选择收据行。  
16. 将 **转移单** 选项设置为 **是**。 从转移订单选择收据行。  
17. 选择 **保存**。
18. 关闭该页面。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

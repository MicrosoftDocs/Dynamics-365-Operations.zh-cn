---
title: "按中国站点过帐主库存科目"
description: "此主题提供有关按中国的站点过帐库存主科目过帐的信息。"
author: ShylaThompson
manager: AnnBe
ms.date: 03/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventPostingParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 262754
ms.assetid: f8e0b34d-006a-4baf-86ae-60625ba4b442
ms.search.region: China (PRC)
ms.author: leguo
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 554c350961baed8be8f37854dd1b095d4342ae0e
ms.openlocfilehash: 40199425ced4953ce875afc4f6d0015d2ff85199
ms.contentlocale: zh-cn
ms.lasthandoff: 03/21/2018

---

# <a name="post-inventory-main-accounts-by-site-for-china"></a>按中国站点过帐主库存科目

[!INCLUDE [banner](../includes/banner.md)]

此主题提供有关按中国的站点过帐库存主科目过帐的信息。

您可以设置或修改物料的过帐到会计科目，基于库存交易记录的物料组和仓库站点。 通过按站点设置库存的会计科目值，可以过帐各站点的库存交易记录。 这些交易记录包括库存日记帐、销售订单、采购订单、生产日记帐和项目物料日记帐。 仅当**库存和仓库管理参数**页上的**按站点分隔库存成本的会计科目**选项设置为**是**，**交易组合**和**过帐**页上才有与站点有关的字段。 在特定报告期间，必须确定库存物料的值以确定现有库存量、库存上的应纳税金额和库存收货和发货的期初和期末余额。 可以为库存创建主科目。 也可以选择显示可用于库存过帐的库存物料的库存值的主科目。 您可以从相应的主科目中计算物料组的库存成本。 例如，您可以创建“原材料”物料组的主科目来跟踪其库存成本。

| 主科目 | 物料组    | 余额    |
|--------------|---------------|------------|
| 15067        | 灯泡         | 10,721,065 |
| 15065        | 原材料 | 6,299,398  |

存货超过 100 库存物料并可维护多个站点的组织必须按站点和物料组要求组织主科目。 例如，一个组织可以有多个站点，并且，每个站点可以有多个物料组。 在下表中，您可以查看站点 1 的“灯泡”物料组的库存成本和站点 2 的“原材料”物料组的库存成本。

| 主科目 | 物料组    | 站点   | 所有者权益   |
|--------------|---------------|--------|-----------|
| 15080        | 灯泡         | 站点 1 | 5,721,065 |
| 15085        | 原材料 | 站点 2 | 3,299,398 |

通过按站点设置库存成本的主科目，您可以过帐库存交易，如每个站点的库存日志、销售订单、采购订单，生产日志和项目物料日志。


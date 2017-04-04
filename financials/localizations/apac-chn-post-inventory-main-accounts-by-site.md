---
title: Posting inventory main accounts by site
description: "此主题按站点提供有关库存主科目过帐的信息针对中国的。"
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventPostingParameters
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 262754
ms.assetid: f8e0b34d-006a-4baf-86ae-60625ba4b442
ms.search.region: China (PRC)
ms.author: leguo
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: 87dab836fcd3d1adfac1d07d275bb03431e3be9f
ms.lasthandoff: 03/31/2017


---

# <a name="post-inventory-main-accounts-by-site"></a>按站点过帐的库存主科目

此主题按站点提供有关库存主科目过帐的信息针对中国的。

您可以设置或修改物料的过帐到会计科目，基于库存交易记录的物料组和仓库站点。 通过设置库存成本会计科目按站点，您可以过帐每个站点关联的库存交易记录。 这些交易记录包括销售订单、库存日志、采购订单、生产日志和项目物料日志。 站点关联的字段位于以下网址**交易记录组合** **和过帐**页，只有当该**库存成本单独的会计科目。站点的**选项在**请库存和仓库管理参数** ** **是页面设置。 在特定报告期间，必须确定库存物料的值以确定现有库存量、库存上的应纳税金额和库存收货和发货的期初和期末余额。 可以创建的库存主科目。 或者，可以选择显示值您的库存物料组的库存可用于库存过帐时使用的主科目。 您可以从相应的主科目中计算物料组的库存成本。 例如，您可以创建“原材料”物料组的主科目来跟踪其库存成本。
| 主科目 | 物料组    | 余额    |
|--------------|---------------|------------|
| 15067        | 灯泡         | 10,721,065 |
| 15065        | 原材料 | 6,299,398  |

库存多 100 库存物料和组织的若干站点必须按站点维护物料和组将它们组织的主科目。 例如，一个组织可以有多个站点，并且，每个站点可以有多个物料组。 在以下各表中，您可以查看用途-灯泡物料组的库存成本 1 站点的物料和物料组的库存站点的成本。2.
| 主科目 | 物料组    | 站点   | 所有者权益   |
|--------------|---------------|--------|-----------|
| 15080        | 灯泡         | 站点 1 | 5,721,065 |
| 15085        | 原材料 | 站点 2 | 3,299,398 |

通过按站点设置库存成本的主科目，您可以过帐库存交易，如每个站点的库存日志、销售订单、采购订单，生产日志和项目物料日志。



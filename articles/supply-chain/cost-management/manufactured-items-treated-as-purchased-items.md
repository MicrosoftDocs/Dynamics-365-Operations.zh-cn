---
title: "设置可以生产或采购的产品"
description: "产品可以以各种方式采购：可以生产（制造）或采购（购买）。 本文介绍在您配置产品以支持多方采购时要考虑的一些典型问题。"
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 21841
ms.assetid: acc608b7-2cad-4fba-afee-9b7cc93761ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b5ed8c93c13746249605ad8742549c23bb1e0e10
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-products-that-can-be-produced-or-procured"></a>设置可以生产或采购的产品

[!INCLUDE [banner](../includes/banner.md)]

产品可以以各种方式采购：可以生产（制造）或采购（购买）。 本文介绍在您配置产品以支持多方采购时要考虑的一些典型问题。 

多来源通常用于偶尔制造的采购物料，或者，当主要是制造物料的物料发生更改以使其现在主要是采购物料时。 该物料首先被指定为制造物料，以便可以定义物料清单和工艺路线信息以及为物料支持生产订单。 生产类型应设置为**“物料清单”**（或者，对于流程生产，**“配方”**或**“联产品”**）。

当您使用标准成本时，可为制造物料计算物料成本记录。 但是，物料成本记录无法与您要用于采购目的的标准成本匹配。 在这种情况下，标准成本必须手动输入，并且为物料成本记录启用。 对于成本计算，请考虑使用特定物料清单和工艺路线以便在会计期间过程中代表产品的供应组合，随着时间的推移使差异最小化。 此外，一个站点的制造物料可以转移到其他站点。 因此，必须为物料转移的站点手动输入和启用物料的成本。 在您将该制造物料用作更高级别产品中的某一组件时，该组件的成本应被视作采购物料。 此准则适用，不论组件的成本是计算出的或手动输入的。 换言之，物料清单计算应将该物料的成本视作采购组件，而不是使用物料清单和工艺路线信息计算成本。 

若要禁止此计算发生，请选择嵌入到分配给物料的物料清单计算组中的**“停止分解”**标志。 若要禁止主计划编制计算通过物料分解需求，请在物料覆盖范围中或覆盖范围组中将分解时限设置为 0（零）。 主计划编制计算将物料视作采购物料，并且将不为其物料清单和工艺路线信息执行进一步的计算。







---
title: 主计划和多站点功能概览
description: 主计划考虑站点和仓库库存维度的设置。
author: t-benebo
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "2434"
- intro-internal
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 289763931703eb354ae78fa18f37cd00f1102de8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844900"
---
# <a name="master-planning-and-multisite-functionality-overview"></a>主计划和多站点功能概览

[!include [banner](../includes/banner.md)]

主计划考虑站点和仓库库存维度的设置。 

站点维度是必需的，您还可以将仓库维度设置为必需。

维度是必填时，必须为所有库存交易记录输入维度值。 因此，在编制主计划期间，初始需求的站点和仓库是已知的。 站点维度还必须是一致的，以便在分解更低级别的需求期间站点值保持不变。

仓库未设置为必填时，不能从初始需求知道仓库。 计划引擎必须根据为该物料定义的设置、各个仓库以及订单行的详细信息确定要使用哪个仓库。

以下文章说明在定义不同设置时计划引擎如何确定要使用的仓库。

[站点和仓库覆盖范围的主计划（仓库必需）](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[站点覆盖范围的主计划（仓库必需）](master-plan-site-coverage-warehouse-mandatory.md)

[站点和仓库覆盖范围的主计划（仓库非必需）](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[站点覆盖范围的主计划（仓库非必需）](master-plan-site-coverage-warehouse-not-mandatory.md)

[确定物料清单版本](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
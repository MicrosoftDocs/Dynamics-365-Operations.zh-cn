---
title: 客户会员卡和奖励积分
description: 本主题介绍有关双写入中的客户会员卡和奖励积分的数据的集成。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 39e1d5b0a73b198b164e51a18222dbd985192070
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568020"
---
# <a name="customer-loyalty-cards-and-reward-points"></a>客户会员卡和奖励积分

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

企业根据客户的购物和消费模式对客户进行分类并提供完善的服务。 例如，Dynamics 365 Commerce 具有推进和处理客户会员卡、奖励积分、基于会员制的定价和基于奖励的购物体验的基础结构和功能。 当有关 Commerce 中客户会员卡和奖励积分的数据同步到 Dataverse 时，客户参与应用可以使用该数据。 例如，Dynamics 365 Customer Service 用户可以使用数据通过帮助台提供相同的完善服务。

## <a name="templates"></a>模板

| Finance and Operations 应用 | Dynamics 365 中的模型驱动应用 | 说明 |
|-----------------------------|-----------------------------------|-------------|
| 会员卡                | msdyn\_loyaltycards               | 此模板同步有关客户会员卡的信息。 |
| 会员奖励分       | msdyn\_loyaltyrewardpoints        | 此模板同步有关客户奖励积分的信息。 |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
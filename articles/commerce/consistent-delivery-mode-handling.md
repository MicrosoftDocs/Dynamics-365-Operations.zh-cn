---
title: 在电子商务渠道中启用一致的交货方式处理
description: 本主题介绍如何启用一致的交货方式处理，以解决与 Microsoft Dynamics 365 Commerce 电子商务渠道中的费用流相关的可能问题。
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 4cecd70dacd72572afc8e6cb65530bf2be4cc93d
ms.sourcegitcommit: d2e5d38ed1550287b12c90331fc4136ed546b14c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/25/2022
ms.locfileid: "8349938"
---
# <a name="enable-consistent-delivery-mode-handling-in-e-commerce-channels"></a>在电子商务渠道中启用一致的交货方式处理 

[!include [banner](includes/banner.md)]

本主题介绍如何启用一致的交货方式处理，以解决与 Microsoft Dynamics 365 Commerce 电子商务渠道中的费用流相关的可能问题。

在 Dynamics 365 Commerce 中，默认情况下，电子商务渠道中不应用不按比例分配的标头级费用。 此行为可能会导致电子商务渠道中出现以下一个或全部两个问题：

- 不按比例分配的标头级费用不会显示。
- 交货方式的费用在选择的交货方式和结帐订单摘要之间不一致。

要解决这些问题，您必须开启 **支持在渠道中进行一致的交货方式处理** 功能。 此功能可确保电子商务渠道中不会出现不按比例分配的标头级费用，并且销售订单交货信息由同一请求工作流一致处理。

## <a name="turn-on-the-enable-consistent-delivery-mode-handling-in-channel-feature"></a>开启“支持在渠道中进行一致的交货方式处理”功能

要在 Commerce Headquarters 中启用 **支持在渠道中进行一致的交货方式处理** 功能，请按以下步骤操作。

1. 打开 **功能管理** 工作区（**系统管理 \> 工作区 \> 功能管理**）。
1. 在可用功能列表中，搜索并选择 **支持在渠道中进行一致的交货方式处理**。
1. 从右窗格中，选择 **立即启用**。

---
title: 评级模板
description: 此主题介绍如何设置评级资料的数据。
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ceb2b7a5edcee6e248798a6bee114c7da7ecb18a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973952"
---
# <a name="rating-profiles"></a>评级模板

评级资料类似于物流合同（不是法律合同）。 它用于确定负荷的运输关税。 

每个评级资料对于每个装运承运人都是唯一的。 在评级资料中，将装运承运人与主费率相关联。 主费率定义基准费率分配和基准费率。 基准费率确定承运人的费率。

您可以使用显示所有现有评级资料的通用页面设置评级资料。 或者，可以直接从装运承运人设置评级资料。 在这两种情况下，您为评级资料设置的信息是相同的。

## <a name="create-or-edit-a-rating-profile-on-the-rating-profiles-page"></a>在评级资料页创建或编辑评级资料

在 **评级资料** 页上，您可以查看所有可用的评级资料。 您还可以编辑现有资料和创建新资料。

1. 转到 **运输管理 \> 设置 \> 评级 \> 评级资料**。
1. 在操作窗格上，选择 **新建** 将新评级资料添加到网格，或选择 **编辑** 编辑现有资料。
1. 在新的或现有评级资料的行中，设置以下字段：

    - **评级资料** – 为评级资料输入唯一标识符 (ID)。
    - **名称** – 为评级资料输入描述性名称。
    - **装运承运人** – 选择装运承运人。 您在设置的评级资料还将显示在所选承运人的 **装运承运人** 页上。
    - **站点** 和 **仓库** – 选择站点和仓库。
    - **费率引擎** – 为评级资料选择费率引擎。
    - **主费率** – 为评级资料选择主费率。 可以使用主费率定义基准费率类型和基准费率。 有关详细信息，请参阅[设置主费率](set-up-rate-masters.md)。
    - **运输时间引擎** – 为评级资料选择运输时间引擎。
    - **承运人燃油指数** – 为评级资料选择承运人燃油指数。
    - **生效开始日期和时间** 和 **生效结束日期和时间** – 定义评级资料应处于有效状态的时间段。

1. 在操作窗格上，选择 **保存**。

## <a name="create-a-rating-profile-directly-on-the-shipping-carriers-page"></a>直接在装运承运人页创建评级资料

1. 转到 **运输管理 \> 设置 \> 承运人 \> 装运承运人**。
1. 在列表中选择一个装运承运人。
1. 在 **评级资料** 快速选项卡上，选择 **新建** 创建评级资料。
1. 为新的评级资料设置字段。 这些字段对应于 **评级资料** 页上的字段，如此主题前面一节所述。

> [!NOTE]
> 在 **装运承运人** 页上创建的资料也会显示在 **评级资料** 页上。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
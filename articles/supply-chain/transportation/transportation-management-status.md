---
title: 运输管理状态
description: 本文说明如何创建运输状态并将该状态映射到承运人状态。
author: Weijiesa
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9b20570a87a9f8969ca6dcf898176fd40f88eeca
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897362"
---
# <a name="transportation-management-statuses"></a>运输管理状态

[!include [banner](../includes/banner.md)]

为运输状态设置主代码以解释装运承运人提供的代码。 这样，您可以与装运承运人集成以提供状态。 为运输主状态代码提供的运输状态可帮助您跟踪装载、装运或集装箱状态。 负荷、装运或集装箱的特定运输状态只能通过数据集成来更新，不能通过用户界面手动更新。

## <a name="create-a-transportation-status"></a>创建运输状态

要创建运输状态，请按照以下步骤操作：

1. 转到 **运输管理 \> 设置 \> 运输状态主数据**。
1. 选择 **新建** 创建运输状态主数据。
1. 在 **运输状态主数据** 字段中，为运输状态输入唯一代码。
1. 在 **运输类型** 字段中，选择 *装运承运人* 或 *枢纽* 作为运输类型。
1. 输入名称和运输状态。
1. 关闭该页面。

## <a name="map-a-transportation-status-to-a-carrier-status"></a>将运输状态映射到承运人状态

要将运输状态映射到承运人状态，请按照下列步骤操作：

1. 转到 **运输管理 \> 设置 \> 承运人 \> 承运人运输状态**。
1. 选择 **新建** 将装运承运人的代码映射到运输类型主代码。
1. 为装运承运人和承运人服务选择唯一的 ID。
1. 选择要映射到所选装运承运人代码的运输状态代码。
1. 输入装运承运人使用的外部代码。
1. 关闭该页面。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
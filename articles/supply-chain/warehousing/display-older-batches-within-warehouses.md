---
title: 在移动设备上配置“显示仓库内的更早批次”
description: 本主题介绍如何设置移动设备以显示早于当前工作行位置的批次的位置列表。
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d23a259f4c16026ee36f73b427f7d2e610a4b8d938c2e21ec9715d8d2b8137b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6727766"
---
# <a name="configure-display-older-batches-within-warehouse-on-a-mobile-device"></a>在移动设备上配置“显示仓库内的更早批次”

[!include [banner](../includes/banner.md)]

**显示仓库内的更早批次** 配置让你能够显示早于当前工作行位置的批次的位置列表。 显示的位置的列表包括与位置中的更早批次以及各批次的到期日期和物理库存有关的信息。 你可以选择从新位置领料或继续从当前位置领料。 
- 从新位置领料 - 如果你选择一个要从中领料的新位置，当前工作行将更新为使用新位置且新位置的工作将照常进行。 为了使新位置生效，它必须具有用于整个工作行的足够的可用数量。 如果无法提供需要的数量，则不会更新工作行，且将显示列表。 
- 继续从当前位置领料 - 如果继续使用当前的工作行位置，则工作行的数量将继续从原始位置领料。

## <a name="where-it-applies"></a>适用情况
“显示仓库内的更早批次”在移动设备菜单项上配置并影响领取物料下的批次。

## <a name="set-up-display-older-batches-within-warehouse"></a>设置“显示仓库内的更早批次”
当 **领取最早的批次** 选项设置为 **警告** 时，**显示仓库内的更早批次** 配置在移动设备菜单项上可用。

- 在 **仓库管理** > **设置** > **移动设备** > **移动设备菜单项** 下，对菜单项将 **使用现有工作** 设置为 **是**，然后在 **领取最早的批次** 字段中选择 **警告**。 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
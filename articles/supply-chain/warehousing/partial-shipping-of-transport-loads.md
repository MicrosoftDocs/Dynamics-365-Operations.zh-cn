---
title: 运输负荷部分装运
description: 本主题说明如何部分装运装载和推迟规划装载的产能。
author: Mirzaab
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSTransportLoad
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 179a784f1f02ed0840ba5219c350e274272b59eb
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818936"
---
# <a name="partial-shipment-of-a-transport-load"></a>运输负荷部分装运

[!include[banner](../includes/banner.md)]

通过为装载设置部分装运，可处理其产能在所有行都添加到装载之前无法确定的装载。 了解到精确的货盘计数时，即可完成此过程。 因此，在货物实物从分阶段库存实际运出之前，无需确定为哪些运输分配哪些货盘。

此功能提供了备用方法来代替更严格结构的实施，在后者中，必须先确定为哪些运输分配哪些货盘，才能创建领料工作或装载工作。 相反，用户可为单个装载配置部分装运确认。 然后，可能会对这些装载进行运输负荷处理。 因此，运输规划部门在规划装载时不必考虑单次运输的产能。

装载时，工作人员可定义可将货盘装载到的新运输负荷。 也可以识别现有运输负荷。 可通过移动设备记录此数据。 因此，几位仓库工作人员可将库存从同一个负荷或不同负荷装载到同一辆卡车。 然后可全部或部分装运这些负荷。

> [!NOTE] 
> 要将库存从负荷装载到特定运输负荷，并部分装运负荷，必须通过使用工作模板中的装载类生成工作。 不能将 **领料** 类型的普通领料工作装载到运输负荷，如卡车。

## <a name="set-up-transport-loads-for-partial-shipment"></a>为部分装运设置运输负荷

负荷的部分装运设置分为下面的两个步骤。

### <a name="set-the-loading-strategy"></a>设置装载策略

必须通过设置装载处理启用部分装载。 创建负荷后，可设置装载策略。

1. 选择 **仓库管理** \> **负荷** \> **所有负荷**。
2. 选择一个负荷，然后单击 **标题**。
3. 在 **装载策略** 字段中，选择 **允许部分负荷装运**。

### <a name="create-a-menu-item-for-loading-of-transport-loads"></a>为装载运输装运创建一个菜单项。

必须创建一个新的菜单项，用于启用要装载的运输负荷。 可通过运输负荷为来自一个负荷或多个负荷的工作行分组。 然后可通过使用移动扫描仪装运添加到运输负荷的所有物品。

1. 选择 **仓库管理** \> **设置** \> **移动设备** \> **移动设备菜单项**。
2. 选择 **新建**，然后在 **模式** 字段中选择 **工作**。
3. 将 **使用现有工作** 选项设置为 **是**。
4. 在 **常规** 选项卡中，在 **主管** 字段内选择 **运输装载**。
5. 若要在移动扫描仪上启用装运确认，请在 **允许的装运确认类型** 字段中选择 **运输负荷**。

## <a name="confirm-shipment-of-a-transport-load-from-the-client"></a>从客户端确认运输负荷的装运

可通过此设置确认包含要装运的完全符合或部分装载符合的运输负荷。

1. 选择 **仓库管理** \> **负荷** \> **运输负荷**。
2. 在操作窗格上 **装运和接收** 选项卡上 **确认** 组中，选择 **运输**。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: 对部分数量工作进行库存状态更改
description: 此页面介绍如何创建具有相应设置的菜单项，以便让工作人员可以对批次的部分数量进行库存状态更改。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 056ce412955808ddf126025ad917b874c54a5e62
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475638"
---
# <a name="enable-inventory-status-change-for-partial-quantity-work"></a>对部分数量工作启用库存状态更改

## <a name="symptoms"></a>故障特征

您需要对批次的部分数量进行库存状态更改。

## <a name="resolution"></a>解决方法

若要使工作人员能够进行此更改，您可以为仓库管理移动应用创建菜单项。 在 **移动设备菜单项** 页上，创建（或编辑）具有以下设置的菜单项：

- **模式：***工作*
- **使用现有工作**：*否*
- **工作创建流程**：*移动*
- **显示库存状态**：*是*

您可以根据需要在页面上设置其他字段。

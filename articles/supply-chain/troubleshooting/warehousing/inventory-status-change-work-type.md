---
title: 不能为“工作类型”选择“库存状态更改”
description: 不能为库存状态更改创建工作模板行，因为此工作类型仅用于系统进程。 请选择其他工作类型。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ad7f26f3235d15779583f9cdadeb4e6dca16242a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475722"
---
# <a name="cant-select-inventory-status-change-in-the-work-type-column"></a>不能为“工作类型”列选择“库存状态更改”

## <a name="symptoms"></a>故障特征

在配置 Microsoft Dynamics 365 Supply Chain Management 时，可能会收到以下错误消息：

> 不能为库存状态更改创建工作模板行，因为此工作类型无效。 请选择其他工作类型。

## <a name="resolution"></a>解决方法

此为有意行为。 *库存状态更改* 工作类型仅由系统流程使用。 无法进行配置。 由于工作类型列表固定为枚举，因此无法将多余条目从 **工作类型** 下拉菜单中筛选掉。

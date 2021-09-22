---
title: 无法处理交货通知更正
description: 如果在过帐交货通知后尝试更正该交货通知，则会收到错误。 此页面介绍如何更正已启用 WMS 的物料的已过帐装箱单。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: bb0d827adff8abd8762bf2de844cad5574628e4b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475714"
---
# <a name="delivery-note-correction-cant-be-processed"></a>无法处理交货通知更正

## <a name="symptoms"></a>故障特征

发布交货通知后，将无法取消，因为 **取消** 按钮不可用。 您也无法更正交货通知。 如果尝试，可能会收到以下错误消息：

> 无法处理交货通知更正。 交货通知仅包含需要进入仓库管理流程的物料，因为交货通知更正不支持这些物料。

## <a name="resolution"></a>解决方法

要更正已启用高级仓库管理 (WMS) 的物料的已过帐装箱单，必须从负荷而不是直接从订单进行过帐。

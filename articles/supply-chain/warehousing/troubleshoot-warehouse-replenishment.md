---
title: 仓库补货疑难解答
description: 此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中处理仓库补货时可能遇到的常见问题。
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 8dfb58c9156df106f58dfdc0ee2e0ef8defb9d9f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263196"
---
# <a name="troubleshoot-warehouse-replenishment"></a>仓库补货疑难解答

[!include [banner](../includes/banner.md)]

此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中处理仓库补货时可能遇到的常见问题。

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a>我收到以下错误消息：“工作 %1 无法解锁，它有未完成的补货工作。”

### <a name="issue-description"></a>问题描述

领料工作由于有依赖的补货工作被锁定。

### <a name="issue-resolution"></a>解决问题

当您使用波次需求补货时，如果必须为某个领料位置补货以满足源订单需求，系统将同时创建补货工作和领料工作。 但是，会锁定领料工作，直到补货工作完成。 此行为是有意的，因为除非补货工作完成，否则领料位置会没有足够的库存。 请完成补货工作，然后再处理领料工作。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
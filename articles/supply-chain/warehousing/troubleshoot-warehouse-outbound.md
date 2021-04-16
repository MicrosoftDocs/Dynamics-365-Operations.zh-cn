---
title: 出货仓库工序疑难解答
description: 此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中处理出货仓库工序时可能遇到的常见问题。
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 919b6f433db47f24adc9a474942557a1467d1f71
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828170"
---
# <a name="troubleshoot-outbound-warehouse-operations"></a>出货仓库工序疑难解答

[!include [banner](../includes/banner.md)]

此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中处理出货仓库工序时可能遇到的常见问题。

## <a name="i-receive-the-following-error-message-sales-order-could-not-be-released"></a>我收到以下错误消息：“销售订单无法下达。”

### <a name="issue-description"></a>问题描述

出现此问题有多种原因。 例如，订单处于信用管理暂停状态，只有为与销售订单关联的所有销售行输入有效的邮政地址，才能创建装运。 或者，存在订单保留，要将订单下达到仓库必须对它进行处理。 此保留可能是特定于订单的，或者可能在客户帐户上。

### <a name="issue-resolution"></a>解决问题

在销售订单和订单行上添加或更新地址，然后将订单下达到仓库。 仅当订单有有效的交货地址（按照 **组织管理** 模块中设置的地址格式）时，才能将订单下达到仓库。

调查订单保留，并解决问题。 然后从订单或客户中删除保留，将订单下达到仓库。

## <a name="i-receive-the-following-message-the-shipment-for-load-1-has-been-confirmed-however-no-lines-are-posted"></a>我收到以下消息：“负荷 1% 的装运已确认。” 但是，没有过帐行。

### <a name="issue-description"></a>问题描述

负荷上的装运已确认，但没有进一步过帐。

### <a name="issue-resolution"></a>解决问题

装运确认不会影响过帐。 它只是更新装运和负荷状态。 过帐必须在单独的流程中进行。

## <a name="i-receive-the-following-error-message-direct-delivery-is-not-able-to-process-for-warehouse-1-as-it-has-warehouse-management-enabled-please-specify-another-warehouse-that-is-not-enabled-for-warehouse-management"></a>我收到以下错误消息：“直接交货无法为仓库 1% 执行处理，因为它启用了仓库管理。 请指定另一个未启用仓库管理的仓库。”

### <a name="issue-description"></a>问题描述

物料被添加到启用了仓库管理 (WMS) 的仓库的直接交货的销售行。 当销售行更新时，您会收到此错误消息。 

### <a name="issue-resolution"></a>解决问题

Microsoft 已评估此问题，确定了这是一项功能限制。 当前，WMS 不支持直接交货。 因此，要使用直接交货，必须选择非 WMS 物料和仓库。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
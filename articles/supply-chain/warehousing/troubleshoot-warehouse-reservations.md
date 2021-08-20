---
title: 仓库管理中的预留疑难解答
description: 此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中处理仓库预留时可能遇到的常见问题。
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
ms.openlocfilehash: 5f3a9ab907c3cb0e6b99c414a78b6878bd5353274472c54e1f5eaf1d167f046a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6773097"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a>仓库管理中的预留疑难解答

[!include [banner](../includes/banner.md)]

此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中处理仓库预留时可能遇到的常见问题。

有关与批号和序列号登记相关的主题，请参阅[仓库批次和序列预留层次结构故障排除](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md)。

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a>我收到以下错误消息：“已创建了依赖预留的工作，因此无法删除这些预留。”

### <a name="issue-description"></a>问题描述

您不能在销售行上取消库存的预留，因为该行有未结工作。

### <a name="issue-resolution"></a>解决问题

调查是否存在要将物料从装箱工作站运送到另一个位置（如 *货架门*）的未结包装组工作。 查看 **工作创建历史记录日志** 和 **工作详细信息** 页的记录，确定哪个工作在实际预留库存，然后完成或删除工作，释放预留。

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a>我收到以下错误消息：“库存数量 -%1 由于物料 %2 的库存交易不足无法更新....”

### <a name="issue-description"></a>问题描述

如果系统由于没有足够的具有指定维度的库存交易而无法更新库存数量，则可能发生此问题。 以下是完整错误消息的完整文本：

> 库存数量 -%1 由于批次 ID %12 上的物料 %2（维度为尺寸=%3、颜色=%4、附加物=%5、站点%6、仓库=%7、位置=%8、库存状态=可用、牌照=%9、引用 ID %11 的批处理号=%10）的库存交易不足无法更新。

### <a name="issue-resolution"></a>解决问题

请确保没有库存交易在实际预留数量。 例如，这些交易可能会打开质量订单、库存锁定记录或输出订单。

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a>我收到以下错误消息：“实际现有量...无法预留，因为库存中只有 0.00。”

### <a name="issue-description"></a>问题描述

如果系统由于没有足够的具有指定维度的库存交易而无法更新库存数量，则可能发生此问题。 以下是完整错误消息的完整文本：

> 实际现有量站点=%1、仓库=%2、库存状态=可用、批处理号=%3、所有者=%4：%5 无法预留，因为库存中只有 0.00。

### <a name="issue-resolution"></a>解决问题

此问题可能是由于未结工作引起的。 请完成工作或在不创建工作时接收。 请确保没有库存交易在实际预留数量。 例如，这些交易可能会打开质量订单、库存锁定记录或输出订单。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

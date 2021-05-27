---
title: 为单个收货上的多个工作标题只打印了一个标签
description: 为单个收货上的多个工作标题只打印了一个标签。
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8e11dc918eb3c9085018d15b43819522cc8bebe3
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026302"
---
# <a name="only-one-label-is-printed-for-multiple-work-headers-on-a-single-receipt"></a>为单个收货上的多个工作标题只打印了一个标签

知识库编号：4614667

## <a name="symptoms"></a>故障特征

作为单个仓库应用接收事件的一部分，将为同一个目标牌照创建多个工作标题。 但是，接收产品时只打印一个牌照标签。

## <a name="resolution"></a>解决方法

此系统行为是有意设计的。

在当前设计中，无论存在多少个工作标题和工作行组合，始终是生成一个牌照标签。 生成的标签仅包含一个组合的信息。

要解决此问题，请确保将工作标题创建始终映射到一个目标牌照。

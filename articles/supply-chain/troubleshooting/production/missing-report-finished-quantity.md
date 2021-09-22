---
title: “完工入库”更新失败，发生“缺少数量”错误
description: 如果在结束生产订单时报告错误数量，但不报告时间或物料数量，则完工入库更新将失败。
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 7785549c47063727f2749749940c1a96a351e70f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475659"
---
# <a name="report-as-finished-update-fails-with-a-missing-quantity-error"></a>“完工入库”更新失败，发生“缺少数量”错误

## <a name="symptoms"></a>故障特征

您尝试将生产订单完工入库，但报告错误数量，而不报告时间或物料数量。 完工入库更新在您尝试结束生产订单时失败，您将收到以下错误消息：

> 缺少报告为完工入库的数量。

## <a name="resolution"></a>解决方法

如果报告生产订单上的错误数量，必须也报告完好数量。

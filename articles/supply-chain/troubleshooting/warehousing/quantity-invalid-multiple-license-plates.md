---
title: 数量对具有多个 LP 的领料工作无效
description: 如果领料工作在一个位置有多个牌照，则数量对个单位无效。 请验证以下字段是否正确。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5b245f71e80339fee3e42cfffa0396078a56926e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475647"
---
# <a name="quantity-not-valid-when-theres-picking-work-with-multiple-lps-in-one-location"></a>领料工作在一个位置有多个 LP 时数量无效

## <a name="symptoms"></a>故障特征

如果领料工作在一个位置有多个牌照，则则数量对 *个* 单位无效，您将收到以下错误消息：

> 对于单位 1%，数量无效。

## <a name="resolution"></a>解决方法

请验证已发布产品或产品变型上的 **单位序列组 ID** 和 **单位转换** 字段是否设置正确。

请注意，此错误消息在版本 10.0.15 中已得到改进，现在可以显示预期数量（请参阅 [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)）。 新错误消息为：

> 此数量无效。 预期为 %1 %2。

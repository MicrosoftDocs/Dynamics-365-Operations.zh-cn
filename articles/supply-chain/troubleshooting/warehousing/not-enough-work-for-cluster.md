---
title: 配置配置文件后找不到群集的足够工作
description: 如果配置群集配置文件，可能会收到一条错误消息，称可能找不到足够的工作。 编辑配置文件并将“激活位置”设置为“否”。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 139fd72e571c8ef83af2fd0e497cf334b6ef0ea4
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475654"
---
# <a name="not-enough-work-found-for-cluster-when-using-system-directed-cluster-picking"></a>在使用系统导向的群集领料时找不到足够的群集工作

## <a name="symptoms"></a>故障特征

在使用 *系统导向的群集领料* 流程时，如果您配置了一个群集配置文件，例如可以在配置文件中为 10 个位置领料，那么当有足够的工作可以为 10 个位置领料时，该流程将按计划运行。 但是，如果只有 8 个位置要领料，则会收到以下错误消息：

> 没有为群集找到足够的工作。

## <a name="resolution"></a>解决方法

要解决此问题，请编辑群集配置文件，将 **激活位置** 选项设置为 *否*。

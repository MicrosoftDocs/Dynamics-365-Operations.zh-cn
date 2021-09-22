---
title: 找不到群集配置文件
description: 处理入站仓库工序时，可能会遇到有关无法找到群集配置文件的错误。 请确保正确设置群集配置文件。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: bbf9c5bc70c8f3ba1fa26db425249e65e82c0518
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475732"
---
# <a name="cluster-profile-cant-be-found"></a>无法找到群集配置文件

## <a name="symptoms"></a>故障特征

处理入站仓库工序时，您可能会收到以下错误消息：

> “已生成质检订单 %1。 找不到群集配置文件。 请检查您的配置。”

此错误消息与打开质量管理 (QMS) 的接收流程有关。 根据您环境中的配置，有关生成错误消息的交易的其他详细信息可能有助于解决此问题。

## <a name="resolution"></a>解决方法

首先，请查看群集领料设置，确保正确配置了群集配置文件。 除非设置了群集配置文件，否则您不能使用移动设备菜单项进行群集领料。 根据您的环境，您可能还必须查看其他相关配置。

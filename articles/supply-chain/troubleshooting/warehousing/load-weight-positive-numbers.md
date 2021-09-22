---
title: 装载重量只能包含正数
description: 处理库位之间的工作时，您可能会收到有关装置重量和正在取消更新的错误。 若要解决此问题，请按照以下步骤操作。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8ea1f6679a521e3e8683b8e5f18f509e98044414
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475676"
---
# <a name="load-weight-error-and-update-canceled-when-processing-work-between-locations"></a>处理库位之间的工作时发生装载重量错误并取消了更新

## <a name="symptoms"></a>故障特征

当您处理从打包位置到暂存位置，或从暂存库位到停靠库位的工作时，如果有未结工作，可能会收到以下错误消息：

> 字段 'Load weight'(=-%1) 中只能包含正数。 已取消更新。

## <a name="resolution"></a>解决方法

要解决此问题，请转到 **系统管理 \> 定期任务 \> 数据库 \> 一致性检查**，运行 **仓库负荷重量一致性检查** 流程。

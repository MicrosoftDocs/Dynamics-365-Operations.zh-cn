---
title: 当前正在使用仓库管理流程
description: 在预留或发放工作时，您可能会收到一条消息，说明当前正在使用仓库管理流程。 请通过下面的一个步骤修复此问题。
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: bfda2fae824cdc64d722310d20cf16e6306d766c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475640"
---
# <a name="cant-reserve-or-release-work-because-processes-are-currently-being-used"></a>无法预留或发放工作，因为当前正在使用流程

## <a name="symptoms"></a>故障特征

使用离散制造时，您到以下错误：

> 当前正在使用仓库管理流程。 如果工作行尚未登记，您可以取消创建的工作以及所有负荷或装运行，然后继续领料或装运流程。

## <a name="cause"></a>原因

如果您尝试预留或下达某个行的工作，但库存交易的状态为 *已领料*（指示物料已领取），这时会发生此问题。

## <a name="resolution"></a>解决方法

若要解决此问题，请按照以下其中一个步骤操作。

- 将生产订单的状态更改回 *已估计* 或 *已下达*。
- 打开相关生产订单的详细信息页面。 在操作窗格上的 **仓库** 选项卡上，在 **停止** 组中，选择 **停止并取消领料** 取消所有已领料交易的领料。 然后选择 **删除停止** 以处理生产订单。

这里是对 *取消领料* 和 *停止* 功能的说明：
  
- **取消领料** – 此功能撤消状态从 *已领料* 一直到 *在单* 的物料清单 (BOM) 行和配方行的库存交易状态。 原材料领料工作完成后，行的状态将设置为 *已领料*。 此状态防止将生产订单重置为 *已创建* 状态。 在这种情况下，您可以使用 *取消领料* 功能从 *已领料* 状态恢复交易，然后将生产订单重置为 *已创建* 状态。
- **停止** – 此功能在生产订单上设置 **已停止** 标记，以防止对订单进行任何状态更新。 您可以在生产订单详细信息页的 **仓库** 快速选项卡上找到 **已停止** 标记。

> [!NOTE]
>
> - 仅当为仓库流程启用的物料创建生产订单时，按钮才可见。
> - **停止** 组仅在生产订单详细信息页的操作窗格上的 **仓库** 选项卡上可见。 在 **生产订单** 列表页的 **仓库** 快速选项卡上不可见。

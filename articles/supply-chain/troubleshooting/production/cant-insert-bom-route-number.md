---
title: 无法插入物料清单活动版本和工艺路线编号
description: 如果已经为所选产品定义了默认站点和仓库，则不会提示您插入物料清单活动版本和工艺路线编号。
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 241618d70f01c85df946a48493f5d84e0964218e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475641"
---
# <a name="cant-insert-bill-of-material-and-route-when-creating-a-new-production-order"></a>新建生产订单时无法插入物料清单和工艺路线

## <a name="symptoms"></a>故障特征

创建新的生产订单时，输入物料编号后，**站点** 和 **仓库** 字段将自动设置为在成品物料的 **默认订单设置** 页上定义的默认站点和仓库。 此外，将自动输入活动物料清单编号和工艺路线编号，因此您不会收到下面提示您提供这些值的消息：

> 插入物料清单和工艺路线的有效版本？

## <a name="resolution"></a>解决方法

如果您选择了在 **默认订单设置** 页上已有其站点和仓库的产品，则不会提示您插入物料清单和工艺路线编号。 只有在没有为所选产品定义这些值时，才会提示您。

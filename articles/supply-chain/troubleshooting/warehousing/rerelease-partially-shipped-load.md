---
title: 不能将部分装运的负荷重新发放到仓库
description: 在早期版本中，在对不完整的预留使用某些功能时，可能无法重新发放部分装运的负荷。 此问题已修复。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0380e1963a38f2be55b31e06b3845f935661eed2
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475705"
---
# <a name="cant-re-release-a-partially-shipped-load-to-the-warehouse"></a>不能将部分装运的负荷重新发放到仓库

## <a name="symptoms"></a>故障特征

您不能将部分装运的负荷发放到仓库。 当您对仓库执行发放时，会出现“操作完成”消息，但是不会发生任何变化，也不会为剩余数量创建工作。 当您使用运输负荷功能并且有未完成的预留时，会发生此问题。

## <a name="resolution"></a>解决方法

[KB 问题 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f)（“部分装运的负荷可以重新加入波次和重新处理”）在[版本 10.0.15](/dynamics365/supply-chain/get-started/whats-new-scm-10-0-15) 中已修复。

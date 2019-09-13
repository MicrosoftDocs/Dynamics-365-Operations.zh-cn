---
title: 拆分固定资产
description: 此主题介绍如何把一个资产帐簿的一定百分百拆分到新资产帐簿。
author: saraschi2
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4e001a6fdf390c6211ba85aa327b60dcdf16d9e
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867575"
---
# <a name="split-a-fixed-asset"></a>拆分固定资产

[!include [task guide banner](../../includes/task-guide-banner.md)]

此主题介绍如何把一个资产帐簿的一定百分百拆分到新资产帐簿。 它使用会计角色和 USMF 演示数据。


## <a name="create-a-new-fixed-asset"></a>创建新的固定资产
1. 在导航窗格中，转到**模块 > 固定资产 > 固定资产 > 固定资产**。
2. 选择**新建**。
3. 在**固定资产组**字段中，输入或选择一个值。 请注意，固定资产编号将在稍后的拆分流程使用。  
4. 在**名称**字段中，键入一个值。
5. 关闭窗体。

## <a name="split-a-fixed-asset"></a>拆分固定资产
1. 在列表中，查找并选择要拆分的固定资产的链接。
2. 选择**帐簿**。 选择拆分到新资产的帐簿  
3. 选择**功能**。
4. 选择**拆分固定资产**。
5. 在**目标固定资产**字段中，输入或选择一个值。
6. 在**目标帐簿**字段中，选择下拉按钮以打开查找。
7. 在**交易记录日期**字段中，输入日期。
8. 在**百分比**字段中，输入一个数字。
9. 在**日记帐名称**字段中，输入或选择一个值。
10. 选择**确定**。

## <a name="post-the-journal-transaction"></a>过帐日记帐交易记录
1. 在导航窗格中，转到**模块 > 固定资产 > 日记帐条目 > 固定资产日记帐**。
2. 在列表中，选择在拆分流程创建的日记帐。
3. 选择**行**。

    - 验证已创建的日记帐行。  
    - 创建原始资产的购置调整交易记录，以通过拆分流程指定的百分比减少价值。  
    - 为新资产创建相同金额的购置交易记录。  

4. 选择**过帐**。


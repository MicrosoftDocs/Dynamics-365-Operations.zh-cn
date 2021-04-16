---
title: 拆分固定资产
description: 此主题介绍如何把一个资产帐簿的一定百分百拆分到新资产帐簿。
author: saraschi2
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aa21d5698275ff691ca83d29abd297a796b652d1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823900"
---
# <a name="split-a-fixed-asset"></a>拆分固定资产

[!include [banner](../../includes/banner.md)]

此主题介绍如何把一个资产帐簿的一定百分百拆分到新资产帐簿。 它使用会计角色和 USMF 演示数据。

## <a name="create-a-new-fixed-asset"></a>创建新的固定资产

1. 在导航窗格中，转到 **模块 \> 固定资产 \> 固定资产 \> 固定资产**。
2. 选择 **新建**。
3. 在 **固定资产组** 字段中，输入或选择一个值。 请注意，固定资产编号将在稍后的拆分流程使用。
4. 在 **名称** 字段中，输入一个值。
5. 关闭窗体。

## <a name="split-a-fixed-asset"></a>拆分固定资产

在拆分完全折旧资产之前，应手动将资产帐簿状态从 **已结算** 更改为 **未结**。 此步骤是必需的，因为如果您必须过帐资产的交易（例如处置销售），帐簿状态必须为 **未结**。 还必须开启 **总帐参数** 页面 **常规** 选项卡上的 **一个凭证可以允许多个交易记录** 参数。 资产帐簿状态更改并允许一张凭单中有多项交易记录后，请完成以下步骤拆分资产。

1. 在列表中，查找并选择要拆分的固定资产的链接。
2. 选择 **帐簿**。 选择拆分到新资产的帐簿
3. 选择 **功能**。
4. 选择 **拆分固定资产**。
5. 在 **目标固定资产** 字段中，输入或选择一个值。
6. 在 **目标帐簿** 字段中，选择下拉按钮以打开查找。
7. 在 **交易记录日期** 字段中，输入日期。
8. 在 **百分比** 字段中，输入一个数字。
9. 在 **日记帐名称** 字段中，输入或选择一个值。
10. 选择 **确定**。

## <a name="post-the-journal-transaction"></a>过帐日记帐交易记录

1. 在导航窗格中，转到 **模块 \> 固定资产 \> 日记帐条目 \> 固定资产日记帐**。
2. 在列表中，选择在拆分流程创建的日记帐。
3. 选择 **行**。

    - 验证已创建的日记帐行。
    - 创建原始资产的购置调整交易记录，以通过拆分流程指定的百分比减少价值。
    - 为新资产创建相同金额的购置交易记录。

4. 选择 **过帐**。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
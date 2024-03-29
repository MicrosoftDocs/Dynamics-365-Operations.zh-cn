---
title: 选择中国凭证类型的帐户组
description: 本文介绍了在设置中国凭证类型时如何选择帐户组。
author: AdamTrukawka
ms.date: 07/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: China (PRC)
ms.author: atrukawk
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: ''
ms.search.form: ''
ms.openlocfilehash: 9f1d5d886b09e2ab873dc2dfcd182afc269a26a1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275280"
---
# <a name="select-account-groups-for-chinese-voucher-types"></a>选择中国凭证类型的帐户组

[!include [banner](../includes/banner.md)]

本文介绍了在设置中国凭证类型时如何选择帐户组。

## <a name="enable-the-feature"></a>启用功能

1. 转到 **工作区** \> **功能管理**。
2. 在列表中，查找并选择名为 **中国式凭证类型的客户组选择** 的功能。 然后，选择 **立即启用**。
3. 该功能引入了一个新表，用于存储凭证类型的设置。 若要将有关现有中国式凭证类型的设置的信息复制到新表，请转到 **系统管理** \>**定期任务** \>**数据库** \> **一致性检查**。 然后展开 **计划** \> **总帐**，并选择 **凭证的限制类型**。
4. 在 **检查/修复** 字段中，选择 **检查** 以确定现有设置中是否有要复制到新表的任何设置。
5. 在 **检查/修复** 字段中，选择 **修复** 以将设置从现有表复制到新表。

## <a name="set-up-voucher-type"></a>设置凭证类型

1. 转到 **总帐** \> **日记帐设置** \> **中国式凭证类型** \> **凭证类型**。
2. 在 **规则** 快速选项卡上，选择具有特定限制的行。
3. 在 **受影响的帐户** 快速选项卡上，选择 **添加**。

    您现在必须为所选规则设置帐户。

4. 在 **帐户类型** 字段中，选择 **分类帐**、**客户**、**供应商**、**项目**、**固定资产** 或 **银行**。
5. 在 **帐户代码** 字段中，选择 **表格**、**组** 或 **全部**。 请注意，值 **组** 不适用于 **分类帐** 帐户类型。
6. 执行以下步骤之一，具体取决于您在 **帐户类型** 字段中选择的值：

    - 如果您选择 **组**：在 **组编号** 字段中，请根据您在 **帐户类型** 字段中选择的帐户类型选择客户组、供应商组、项目组、固定资产组或银行组。
    - 如果您选择了 **表**：在 **帐户编号** 字段中，请根据您在 **帐户类型** 字段中选择的帐户类型选择分类帐科目、客户科目、供应商科目、项目 ID、固定资产编号或银行帐户值。

有关如何设置中国式凭证类型的信息，请参阅[设置中国式凭证](tasks/set-up-chinese-vouchers.md)。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

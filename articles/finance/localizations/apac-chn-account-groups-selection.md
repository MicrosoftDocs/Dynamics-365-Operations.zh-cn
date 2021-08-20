---
title: 选择中国凭证类型的帐户组
description: 本主题介绍了在设置中国凭证类型时如何选择帐户组。
author: anasyash
ms.date: 07/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.search.region: China (PRC)
ms.author: anasyash
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c6b7d6ba24d43098d1ad95f71bc899ed5d11cca7bcb2a92c9919193b09c6cf91
ms.sourcegitcommit: fa5ff2a0822aac16b518a2aea0d3389f79793390
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/07/2021
ms.locfileid: "7012132"
---
# <a name="select-account-groups-for-chinese-voucher-types"></a>选择中国凭证类型的帐户组

[!include [banner](../includes/banner.md)]

本主题介绍了在设置中国凭证类型时如何选择帐户组。

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

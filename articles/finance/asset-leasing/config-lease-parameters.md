---
title: 配置租赁参数（预览）
description: 本主题描述资产租赁的配置设置，例如安全信息和记帐设置。
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: c681f7d356752a2194a86bc7eaef6ceac1e0af6b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816092"
---
# <a name="configure-lease-parameters"></a>配置租赁参数

[!include [banner](../includes/banner.md)]

几个配置设置会影响资产租赁的行为。 这些设置包括日记帐名称、常规参数和过帐模板设置。

1. 转到 **资产租赁 \> 设置 \> 资产租赁参数**。
2. 在 **选择** 选项卡中，选择 **常规** 快速选项卡。

    **允许手动覆盖分类** 参数决定在确认付款计划之前是否可以覆盖租赁分类。

    **跨实体批处理** 参数确定您是否可以从当前法人过帐到其他法人。 如果已开启此参数，则可以为您有权访问的法人体创建日记帐条目。

3. 将 **允许删除已确认的租赁** 选项设置为 **是** 以允许删除已确认付款计划的租赁。 不能删除与已过帐或未过帐交易关联的租赁，无论此选项的设置如何。 删除租赁记录后，不能恢复。 如果您手动或通过数据实体上载了已删除租赁的任何记录，则上载的信息将被视为新信息，而不是对现有租赁的更新。

    如果将此选项设置为 **是**，而帐簿的转换类型为 **累积采纳选项 A 或 B**，系统将把 **增量借贷利率** 字段的值设置为 **帐簿设置** 页上的 **转换期增量借贷利率** 字段的值。 如果此选项设置为 **否**，则将总租赁费率设置为 **帐簿详细信息** 页上的 **增量借贷利率** 字段的值，而不论帐簿的转换类型为何。

4. 将 **允许对已结帐簿版本进行折旧冲销** 选项设置为 **是**，以允许冲销折旧费用交易。 即使帐簿版本已结，也可以冲销费用交易。

    > [!NOTE]
    > 我们建议您将此选项保持设置为 **否**。 此选项的设置用作验证和控制，以防止已结帐簿版本意外折旧。 通过将选项设置为 **否**，您可以帮助保持帐面净值和未来折旧计算的准确性。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: 零售商店中的财务对帐
description: 本主题介绍 POS for Microsoft Dynamics 365 Commerce 中的零售商店财务对帐。
author: anpurush
manager: AnnBe
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-21
ms.dyn365.ops.version: ''
ms.openlocfilehash: 99c238ecfbb6cb29f4fefefdca32525b99a01dc8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251323"
---
# <a name="financial-reconciliation-in-retail-stores"></a>零售商店中的财务对帐

[!include [banner](includes/banner.md)]

在 Microsoft Dynamics 365 Commerce 版本 10.0.10 及更低版本中，商店职员和商店经理可使用销售点 (POS) 客户端为零售商店中的日结流程提供的功能执行日结操作。 例如，可以进行点钞、直接结束班次，协调班次事务和结束班次。 但是，在 POS 中不能完成班次的财务信息，因此可将其用于在 Commerce Headquarters 中过帐财务数据。 通常由商店经理负责完成此任务。 他们必须先检查信息，进行必需的更正，然后完成班次的总计，才能注销班次。 然后应该在 Commerce Headquarters 中的财务模块内过帐完成的总计。

此外，在 Commerce version 10.0.10 及更低版本中，商店经理还可以在 Commerce Headquarters 中检查对帐单行并进行一些调整。 但是，此功能受到限制，商店经理几乎不能访问 Commerce Headquarters 客户端。 此外，仅当对帐单是在 Commerce Headquarters 中创建的，才能进行财务零售对帐单检查和调整。 不过，该流程通常在夜间进行。 因此，在 Commerce Headquarters 中创建财务零售对帐单时，商店经理必须等待班次注销。

在 Commerce 版本 10.0.11 及更高版本中，商店经理可以在 POS 客户端中执行检查、调整和完成自己的班次。 然后使用这些数据在 Commerce Headquarters 中创建和过帐财务零售对帐单。

> [!NOTE]
> 仅当开启了基于缓慢馈送的订单创建功能，零售商店中才支持与财务对帐有关的功能。 有关详细信息，请参阅[为零售商店交易记录创建基于缓慢馈送的订单](trickle-feed.md)。

## <a name="set-up-financial-reconciliation"></a>设置财务对帐

请按照以下步骤使用财务对帐功能。

1. 在 **功能管理** 工作区中，开启 **零售对帐单 - 缓慢馈送** 功能。
1. 在相应商店的 POS 功能配置文件中，将 **在商店中启用财务对帐** 选项设置为 **是**。

## <a name="more-information-about-financial-reconciliation"></a>有关财务对帐的详细信息

财务对帐功能开启后，将把 Commerce Headquarters 中 **零售商店** 页 **报表/结算** 快速选项卡上定义的部分参数同步到渠道数据库。 将实施用于零售对帐单的同一组计算条件和金额阈值。

调用 **结束班次** 操作时，系统将验证系统计算出的金额与申报金额是否匹配。 如果不同，并且差额超过了定义的阈值，将提示用户进行必要调整。

可以对每笔支付进行调整。 选择支付后，用户可以查看不同交易类型的总计和编辑特定交易类型的总计。 编辑期间，系统将显示最初为该交易类型计算出的金额和替换成的金额。 用户也可以在编辑过程中捕获通知单。 通知单可用于审核目的。

用户可以忽略验证提示和消息，也可以继续结束班次。 但是，如果用户忽略验证提示，当班次在 Commerce Headquarters 中过帐财务对帐单时，将发生相同问题，并且必须解决这些问题。

POS 中的 **结束班次** 操作还会验证脱机数据库中的所有交易记录是否已同步到渠道数据库。 如果未同步任何交易记录，用户将收到警告消息，因为这种情况可能导致系统计算出的金额不正确。 在这种情况下，用户可以结束 **结束班次** 操作，并尝试将脱机交易记录同步到渠道数据库。 或者，用户也可以将系统计算出的金额手动调整为未同步的交易记录的金额，从而结束和过帐一组正确的财务数字。 

如果使用缓慢馈送对帐单过帐，从而使交易记录过帐与财务过帐分开，可以选择调整系统为缺少的脱机交易记录计算出的金额。 这样就可以确保无论是否缺少交易记录，始终正确核算和过帐财务数据。 可以将脱机交易记录同步到渠道数据库和 Commerce Headquarters，之后再过帐，从而与财务过帐分开。

将使用 P 作业把班次的财务对帐详细信息同步到 Commerce Headquarters。

Commerce Headquarters 中的财务零售对帐单不会计算总计以在对帐单行中显示详细信息。 而是使用 POS 客户端中的最终金额创建和过帐财务零售对帐单。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
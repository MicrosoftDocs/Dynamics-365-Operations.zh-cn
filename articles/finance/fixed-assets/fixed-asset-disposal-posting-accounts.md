---
title: 固定资产处置过帐科目
description: 本文说明如何为处理资产设置总帐过帐科目。
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: kfend
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1272cdb16396d24b5495f023e7b9fe3dee341507
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871324"
---
# <a name="fixed-asset-disposal-posting-accounts"></a>固定资产处置过帐科目

[!include [banner](../includes/banner.md)]

本文说明如何在处理资产时设置总帐过帐科目。

要设置在处置资产时使用的总帐过帐科目，在 **固定资产过帐模板** 页面的 **分类帐科目** 快速选项卡中选择 **处置 - 销售** 和 **处置 - 报废**。

对于这两种交易类型（通过销售或报废处置资产），为固定资产的处置价值贷记分类帐科目。 贷项将过帐到对方科目，可以是银行帐户（举例）。 如果向客户销售某一固定资产，则使用该客户的帐户，来代替对方科目。 有关详细信息，请参阅[将固定资产作为废料处置](dispose-of-a-fixed-asset-as-scrap.md)。

单击 **处置**，然后单击 **销售** 或 **报废**，然后设置详细帐户来冲销固定资产的帐面净值。 您还可以在 **处置参数** 页的 **过帐值** 和 **销售价值类型** 字段中输入信息。 

低价值池中某一资产的处置交易记录将只按已处置金额减少低价值池的帐面净值。 但是，当某一资产的销售额大于低价值池的帐面净值时，帐面净值将被减少到零。







[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: 固定资产购置过帐科目
description: 本文说明如何为购置资产设置总帐过帐科目。
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: kfend
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 93cbfc46fb41e47fba8b6cecf7811c0cf838e7d3
ms.sourcegitcommit: e09f5c6d78d7942af950ae3f6407df2fedceeba4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/06/2022
ms.locfileid: "8719811"
---
# <a name="fixed-asset-acquisition-posting-accounts"></a>固定资产购置过帐科目

[!include [banner](../includes/banner.md)]

本文说明如何为购置资产设置总帐过帐科目。

用于过帐固定资产购置的帐户根据用于购置资产的方法而变。 在“固定资产过帐模板”页上，在“会计科目”选项卡上，选择“购置”和“购置调整”以设置要过帐到分类帐的固定资产科目。 

在日志中和采购订单上，“会计科目”通常是资产负债表科目，在其中将借记新固定资产的购置价格。 此科目不会显示在日志中并且无法在交易记录中被替换。 

“对方科目”也是资产负债表科目。 在一般日志和固定资产日志中，此科目通常将是用于支付资产购置费用的银行帐户。 对方科目是在日志中建议的默认科目。 如果该固定资产从供应商处购买，则可以在日志中将其更改为从会计科目表到供应商帐户的任何其他科目。 

当应付帐款中的发票日记帐或采购订单用于固定资产购置时，固定资产交易记录的对方科目由为该交易记录选择的供应商帐户所替代。

对于在“总帐”中使用“库存转为固定资产日记帐”过帐的购置，固定资产不是从外部购买的，而是从公司自己的库存转移的。 因此，对方科目是库存管理中的库存物料的发货科目。

有关详细信息，请参阅[通过采购购置资产](acquire-assets-procurement.md)。





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

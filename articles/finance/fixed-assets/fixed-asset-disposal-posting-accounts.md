---
title: 固定资产处置过帐科目
description: 本主题说明如何为处理资产设置总帐过帐科目。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e9a46125dbe5262ba388e3958ea452975a98243f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187145"
---
# <a name="fixed-asset-disposal-posting-accounts"></a>固定资产处置过帐科目

[!include [banner](../includes/banner.md)]

本主题说明如何为处理资产设置总帐过帐科目。

在“固定资产过帐模板”页，在“会计科目”快速选项卡上，选择“处置 - 销售和处置 - 报废”以设置过帐到分类帐。

对于这两种交易记录类型，为固定资产的处置价值贷记会计科目。 贷项将过帐到对方科目；例如，可以是银行帐户。 如果向客户销售某一固定资产，则使用该客户的帐户，来代替对方科目。

单击“处置”，然后单击“销售”或“报废”，然后设置详细帐户来冲销固定资产的帐面净值。 您还可以在“处置参数”页的“过帐值”和“销售价值类型”字段中输入信息。 

低价值池中某一资产的处置交易记录将只按已处置金额减少低价值池的帐面净值。 但是，当某一资产的销售额大于低价值池的帐面净值时，帐面净值将被减少到零。






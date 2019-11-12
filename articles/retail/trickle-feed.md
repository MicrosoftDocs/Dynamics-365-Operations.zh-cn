---
title: 为零售商店交易记录创建基于缓慢馈送的订单
description: 本主题介绍如何为 Microsoft Dynamics 365 Retail 中的零售商店交易记录创建基于缓慢馈送的订单。
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 80233a73dbffc7380503cf03703758b187824c2a
ms.sourcegitcommit: 0262a19e32b2c0c84c731d9f4fbe8ba91822afa3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/15/2019
ms.locfileid: "2622658"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions-public-preview"></a>为零售商店交易记录创建基于缓慢馈送的订单（公共预览）

[!include [banner](includes/banner.md)]

[!include [banner](includes/preview-banner.md)]

在 Dynamics 365 Retail 10.0.4 及早期版本中，零售对帐单过帐是日结操作，于一天结束时在帐簿中过帐所有交易记录。 大量的交易记录必须在有限的时间范围内处理，有时会导致加载、锁定和对帐单过帐失败。 零售商也无法全天在其帐簿中确认收入和付款。

通过 Retail 版本 10.0.5 中推出的、基于缓慢馈送的订单创建的公共预览版，可在全天中处理交易记录，并且在一天结束时仅处理支付方式和其他现金管理交易记录的财务对帐。 此功能将创建销售订单、发票和付款的负荷拆分到全天中完成，从而更够更清晰地了解绩效并且能够近乎实时地在帐簿中确认收入和付款。 


## <a name="how-to-use-trickle-feed-based-posting"></a>如何使用基于缓慢馈送的过帐
  
1. 若要对零售交易记录启用基于缓慢馈送的过帐，请转到**系统管理 > 设置 > 许可证配置**，然后禁用**零售对帐单**密钥。

2. 在同一页上，启用**零售对帐单（缓慢馈送）– 预览**许可证密钥。 启用此密钥时，请确保不存在等待过帐的待处理对帐单。 

> [!Important]
> 在启用**零售对帐单（缓慢馈送）– 预览**许可证密钥之前，请确保不存在等待过帐的待处理对帐单。

3. 当前对帐单文档将拆分为两种不同的类型，分别为交易记录对帐单和财务对帐单。

      - 交易记录对帐单将选取所有未过帐的和已验证的零售交易记录，并按照您配置的频率创建销售订单、销售发票、付款和折扣日记帐以及收入-支出交易记录。 您应将此过程配置为以较高的频率运行，以便当通过 P 作业将零售交易记录上载到 Retail Headquarters 中时会创建文档。 对于已创建销售订单和销售发票的交易记录对帐单，则无需配置**过帐库存**批处理作业。 但是，您仍可以使用它来满足您可能具有的特定业务需求。  
      
     - 财务对帐单设计为仅在一天结束时创建，并且仅支持**班次**的结帐方法。 此对帐单仅限用于财务对帐，并且仅针对不同支付方式的计算金额与交易记录金额之间的差异金额而创建日记帐，以及针对其他现金管理交易记录创建日记帐。   

4. 若要计算交易记录对帐单，请单击 **Retail > 零售 IT > POS 过帐 > 批量计算交易记录对帐单**。 若要批量过帐交易记录对帐单，请单击 **Retail > 零售 IT > POS 过帐 > 批量过帐交易记录对帐单**。

5. 若要计算财务对帐单，请单击 **Retail > 零售 IT > POS 过帐 > 批量计算财务对帐单**。 若要批量过帐财务对帐单，请单击 **Retail > 零售 IT > POS 过帐 > 批量过帐财务对帐单**。

> [!NOTE]
> 此新功能中删除了菜单项 **Retail > 零售 IT > POS 过帐 > 批量计算对帐单**和 **Retail > 零售 IT > POS 过帐 > 批量过帐对帐单**。

或者，可以手动创建交易记录对帐单和财务对帐单类型。 转至 **Retail > 渠道 > 零售商店**，然后单击**零售对帐单**。 单击**新建**，然后选择您要创建的对帐单类型。 **零售对帐单**页面上的字段和该页面的**对帐单组**下的操作将基于选定的对帐单类型显示相关的数据和操作。

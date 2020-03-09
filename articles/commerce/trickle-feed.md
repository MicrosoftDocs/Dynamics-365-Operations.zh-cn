---
title: 为零售商店交易记录创建基于缓慢馈送的订单
description: 本主题介绍如何为 Microsoft Dynamics 365 Commerce 中的商店交易记录创建基于缓慢馈送的订单。
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
ms.openlocfilehash: 7d5812893edff24a60a0e2eb3607701ac47a8a78
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057135"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions-public-preview"></a>为零售商店交易记录创建基于缓慢馈送的订单（公共预览版）

[!include [banner](includes/banner.md)]

在 Dynamics 365 Retail 10.0.4 及早期版本中，对账单过账是日结操作，于一天结束时在账簿中过账所有交易记录。 大量的交易记录必须在有限的时间范围内处理，有时会导致加载、锁定和对帐单过帐失败。 零售商也无法全天在其帐簿中确认收入和付款。

通过 Retail 版本 10.0.5 中推出的、基于缓慢馈送的订单创建的公共预览版，可在全天中处理交易记录，并且在一天结束时仅处理支付方式和其他现金管理交易记录的财务对帐。 此功能将创建销售订单、发票和付款的负荷拆分到全天中完成，从而更够更清晰地了解绩效并且能够近乎实时地在帐簿中确认收入和付款。 


## <a name="how-to-use-trickle-feed-based-posting"></a>如何使用基于缓慢馈送的过账
  
1. 若要对交易记录启用基于缓慢馈送的过账，请转到**系统管理 > 设置 > 许可证配置**，然后禁用**对账单**密钥。

2. 在同一页上，启用**对账单（缓慢馈送）– 预览**许可证密钥。 启用此密钥时，请确保不存在等待过账的待处理对账单。 

    > [!Important]
    > 在启用**对账单（缓慢馈送）– 预览**许可证密钥之前，请确保不存在等待过账的待处理对账单。

3. 当前对帐单文档将拆分为两种不同的类型，分别为交易记录对帐单和财务对帐单。

      - 交易记录对账单将选取所有未过账的和已验证的交易记录，并按照您配置的频率创建销售订单、销售账单、付款和折扣日记账以及收入-支出交易记录。 您应将此过程配置为以较高的频率运行，以便当通过 P 作业将交易记录上传到 Headquarters 中时会创建文档。 对于已创建销售订单和销售账单的交易记录对账单，则无需配置**过账库存**批处理作业。 但是，您仍可以使用它来满足您可能具有的特定业务需求。  
      
     - 财务对帐单设计为仅在一天结束时创建，并且仅支持**班次**的结帐方法。 此对账单仅限用于财务对账，并且仅针对不同支付方式的计算金额与交易记录金额之间的差异金额而创建日记账，以及针对其他现金管理交易记录创建日记账。   

4. 若要计算交易记录对账单，请单击 **Retail 和 Commerce > Retail 和 Commerce IT > POS 过账 > 批量计算交易记录对账单**。 若要批量过账交易记录对账单，请单击 **Retail 和 Commerce > Retail 和 Commerce IT > POS 过账 > 批量过账交易记录对账单**。

5. 若要计算财务报表，请单击 **Retail 和 Commerce > Retail 和 Commerce IT > POS 过账 > 批量计算财务报表**。 若要对财务报表进行批量过账，请单击 **Retail 和 Commerce > Retail 和 Commerce IT > POS 过账 > 对财务报表进行批量过账**。

> [!NOTE]
> 此新功能中删除了菜单项 **Retail 和 Commerce > Retail 和 Commerce IT > POS 过账 > 批量计算对账单**和 **Retail 和 Commerce > Retail 和 Commerce IT > POS 过账 > 批量过账对账单**。

或者，可以手动创建交易记录对账单和财务报表类型。 转至 **Retail 和 Commerce > 渠道 > 商店**，然后单击**对账单**。 单击**新建**，然后选择您要创建的对账单类型。 **对账单**页面上的字段和该页面的**对账单组**下的操作将基于选定的对账单类型显示相关的数据和操作。

---
title: 创建付款发票
description: 本文说明如何创建月度租赁发票。 您可以为单个租赁创建发票，也可以使用批处理为多个租赁创建发票。
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePaymentSchedule
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0ac9efaf6d068377053ae36951f4ad808fcb2438
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886393"
---
# <a name="create-payment-invoices"></a>创建付款发票

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


您可以为单个租赁创建月度发票，也可以使用批处理为多个租赁创建发票。 以下过程显示了在已开启 **租赁帐簿设置** 页上的 **向供应商付款** 参数时，如何创建单个租赁付款条目。

1. 在 **租赁摘要** 页上，选择一个租赁，然后选择 **帐簿 \> 付款计划**。
2. 选择必须进行的付款，然后选择 **创建日记帐**。 您将收到一条消息，指出已针对所选付款创建了日记帐。
3. 选择 **发票日记帐**，然后选择必须支付的发票。
4. 将日记帐条目过帐到总帐之前，在 **行** 选项卡上检查该条目。

    > [!NOTE]
    > 默认情况下，创建的供应商发票行使用来自 **应付帐款参数** 页的供应商过帐模板。

5. 选择正确的日记帐，然后选择必须支付的发票。

    对于此示例，已开启了租赁帐簿上的 **向供应商付款** 参数。 因此，发票将在发票日记帐中。 **概览** 部分显示日记帐条目的摘要，**行** 部分显示实际日记帐行的详细信息。
    
   系统将锁定某些财务字段从而使其不能被编辑，以防止交易和计划之间出现任何差异。 已锁定的某些字段包括：**帐户**、**金额**、**财务维度**、**货币** 和 **交易类型**。 此外，您将无法在任何资产租赁日记帐条目中添加或删除日记帐条目行，因为这可能会导致计划与交易之间出现差异。

    > [!NOTE]
    > 如果已关闭 **向供应商付款** 参数，租赁帐簿的 **资产租赁** 页上将列出付款日记帐条目，而系统将创建资产租赁条目，而不是创建发票。 租赁付款条目将过帐到在 **月度租赁日记帐** 字段中指定的日记帐名称。

6. 过帐交易后，您可以通过选择租赁帐簿中的 **负债交易** 来查看租赁负债的交易信息和帐面价值。

    在付款计划中，将选中 **已过帐的日记帐** 复选框，行将显示发票日记帐编号。 创建付款日记帐和该日记帐的条目后，必须冲销该条目，然后才能重新创建。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: 根据生产需求更改托运库存的所有权
description: 此过程显示在生产需要库存时，如何将托运库存的所有者从供应商更改为法人。
author: yufeihuang
ms.date: 08/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalOwnershipChange, InventJournalCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e735a9003f2859ed173f399525297506ec458e8d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565823"
---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a>根据生产需求更改托运库存的所有权

[!include [banner](../../includes/banner.md)]

此过程显示在生产需要库存时，如何将托运库存的所有者从供应商更改为法人。 所有权的此项更改通过创建并过帐库存所有权更改日记帐完成。 所有权更改日记帐行可以手动创建，也可以根据现有生产需要按照此记录中的显示创建。 通常由车间主管执行此任务。 您可以在 USMF 演示数据公司，也可在您自己的数据中运行该过程。 如果您在使用自己的数据，请确保已满足以下先决条件：为库存所有权更改设置的库存日记帐名称、物理记录且由供应商拥有的现成物料，以及材料的一个或多个生产订单行。 此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。

> [!NOTE]
> 默认不支持出站托运流程，也不支持所有权日记帐自动处理。

## <a name="create-an-inventory-ownership-journal"></a>创建库存所有权日记帐
1. 转到“库存管理”>“日记帐条目”>“物料”>“库存所有权更改”。
2. 单击“新建”。
    * 库存所有权更改日记帐用于更改供应商到当前法人的托运库存的所有者。 所有权的此项更改通过发放供应商拥有的现有库存，然后在当前法人处接收该库存完成。  
3. 在“名称”字段中，输入或选择一个值。
    * 可以选择日记帐类型为“所有权更改”的库存日记帐名称。  
4. 单击“确定”。
5. 单击“功能”。
6. 单击“通过生产订单创建日记帐行”。
    * 可以通过查询需要消耗原材料的所有生产行，启动更改所有权流程。  
7. 在“要包含的库存发货状态”字段中，选择一个选项。
    * 此选项用于按库存交易的发货状态筛选。 例如，您可以为“已拣货”和“物理保留”状态创建日记帐行。  
8. 扩展“要包括的记录”部分。
    * 此部分用于应用更多筛选。 例如，可以选择特定原材料日期。  
9. 单击“确定”。

## <a name="post-the-inventory-ownership-change-journal"></a>过帐库存所有权更改日记帐
1. 单击“过帐”。
    * 在过帐日记帐时，将使用“所有权更改”引用发放供应商拥有的库存。 然后使用通过采购订单物料收据更新的库存交易，将库存作为现有量接收。 请注意，将仅创建与过帐的日记帐有关的交易。 不创建任何预期库存交易。  
2. 单击“确定”。
3. 关闭该页面。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
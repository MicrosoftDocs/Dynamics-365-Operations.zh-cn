---
title: 通过采购获得资产
description: 本文介绍如何设置固定资产和应付帐款之间的集成，以便自动从采购订单或供应商发票创建固定资产，或者自动为固定资产过帐购置和购置调整交易记录。
author: moaamer
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetParameters
audience: Application User
ms.reviewer: kfend
ms.custom: 3481
ms.assetid: d4e73a3f-633b-48b2-b8db-7a4a59a4d7ec
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac25114fe8036a474d637e9ad9ede5e46b50d92e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891571"
---
# <a name="acquire-assets-through-procurement"></a>通过采购获得资产

[!include [banner](../includes/banner.md)]

本文介绍如何设置固定资产和应付帐款之间的集成，以便自动从采购订单或供应商发票创建固定资产，或者自动为固定资产过帐购置和购置调整交易记录。 一个采购行创建一个资产，不考虑该采购行中的数量。 如果需要创建多个固定资产，必须创建多个采购行。

 以下方法可用于将固定资产和应付帐款相集成，并且您必须为所有固定资产使用同一种方法：
-   您手动创建某一固定资产，然后将该固定资产的编号添加到采购订单或供应商发票上的行中。 在过帐供应商发票时为该资产自动过帐购置交易记录。 此方法是默认方法。
-   您手动创建某一固定资产，然后将该固定资产的编号添加到采购订单或供应商发票上的行中。 在过帐供应商发票时不为该资产过帐任何购置交易记录。
-   在您过帐选择“创建新的固定资产”复选框的产品收据或供应商发票时，自动创建一个固定资产。 在过帐供应商发票时为该资产自动过帐购置交易记录。
-   在您过帐选择“创建新的固定资产”复选框的产品收据或供应商发票时，自动创建一个固定资产。 在过帐供应商发票时不为该资产过帐任何购置交易记录。

如果您愿意手动创建固定资产，则选择前两个方法中的一个，然后将该固定资产编号分配到采购订单或供应商发票。 如果您喜欢更灵活的方法，则选择前两种方法之一：有时您可以手动创建固定资产，有时您可能基于行项详细信息中的固定资产信息自动创建固定资产。 

无论您是手动创建固定资产还是使用更灵活的方法，您必须决定购置交易记录是否只能在固定资产中过帐，或当您过帐发票时是否过帐它。 某些组织希望用户通过使用手动日志输入或方案，在固定资产中手动创建购置和购置交易记录。 

本文详细介绍上述各方法。

## <a name="methods-for-manually-creating-fixed-assets"></a>手动创建固定资产的方法
当您过帐拥有行中输入的固定资产编号的供应商发票时，如果在“固定资产参数”页中选择了“允许从采购中购置资产”选项，那么将自动过帐该购置，而且该资产的状态更改为 。 

如果无法过帐某一购置，则您既可以手动在固定资产中输入某一购置交易记录，也可以在固定资产日记帐中使用购置方案以同时创建多个购置交易记录。

> [!NOTE]                                                                                                                              
> 如果固定资产设置为限制过帐到某一特定用户组的购置交易记录，则您必须是该用户组的成员以从发票过帐购置交易记录。

## <a name="methods-for-automatically-creating-fixed-assets"></a>自动创建固定资产的方法
当您过帐具有为行选择的“创建新的固定资产”选项的产品收据，将创建具有”尚未购置“状态的新固定资产。 然后，当您过帐具有某一新固定资产的供应商发票时，如果固定资产设置为允许来自应付帐款的资产购置，并且您是可以过帐购置交易记录的用户组的成员，则将为这个新资产过帐购置交易记录，并且资产状态将更改为“未结”。 

如果在您过帐产品收货时在采购订单行上未选中“是否新建固定资产?”选项，但在过帐供应商发票时选中了该复选框，并且固定资产设置为允许创建和购置，则创建新固定资产，而且其购置状态为“未结”。 如果当您过帐产品收货时已创建了某个附加资产，那么您过帐供应商发票时将不会创建附加资产。

### <a name="capitalization-threshold"></a>资本化阈值

在您使用自动创建和购置资产的方法时，可以对系统进行设置，以验证该固定资产的采购额是否满足为资产折旧指定的资本化阈值。 如果满足，则在从应付帐款创建资产时，将在帐簿中选中“折旧”选项。 

资本化阈值是一个币种金额，确定在资产满足指定金额的情况下是否对资产进行折旧。 例如，如果您购买某一资产并且采购额低于资本化阈值，则将不指定该资产进行折旧；如果采购额达到或超过该阈值，则指定将该资产进行折旧。 

可以在“固定资产组”页中设置资本化阈值。

## <a name="scenario"></a>方案
以下场景论述固定资产和应付帐款集成的一个完整周期。 其中介绍了一个示例设置，并且还描述了如何使用采购方案。 

在此场景中，对系统的设置如下：

-   在产品收货或供应商发票过帐期间自动创建资产，但固定资产设置为禁止从应付帐款过帐购置交易记录。
-   在“帐户类型”字段中指定固定资产收货的帐户，在“物料组”页指定固定资产发货帐户类型。
-   计算机组 (COMP) 的资本化阈值是 1,500。
-   您的任务是为某一员工将使用的新笔记本电脑输入一个采购订单，过帐该采购订单，确认装运职员过帐了某一产品收货，过帐该供应商发票，然后确认会计将该笔记本资产更新为“未结”状态。

开始时，您使用“采购订单”页为该笔记本电脑输入详细信息，即成本 1,600。 您在采购订单行的“固定资产”快速选项卡上选择了“是否新建固定资产?”选项，选择 COMP 作为固定资产组，并且保存该采购订单。 

在收到该笔记本电脑后，装运职员将输入和过帐一个产品收货，以便记录收到该笔记本电脑。 创建了该笔记本电脑资产，而且它拥有”尚未购置“状态。 该金额超出了资本化阈值。 因此，在笔记本电脑资产的帐簿中选择“折旧”选项。 以下交易记录将出现。

|  描述                               | 科目             | 借方    | 贷方   |
|-------------------------------------------|---------------------|----------|----------|
| 采购，产品收据采购        | 未开票收货 | 1,600.00 |          |
| 采购，产品收据采购对方科目 | 应计采购   |          | 1,600.00 |

接下来，您为该笔记本电脑过帐供应商发票。 不更改该笔记本电脑的状态，因为固定资产设置为在过帐供应商发票时禁止过帐资产购置交易记录。 在过帐供应商发票时选择了“创建新固定资产”选项。 因此，使用了固定资产收货帐户。 未使用固定资产发货帐户，因为未过帐任何购置；以后，当您的组织的会计使用购置方案在固定资产中过帐某一购置交易记录时，将使用该帐户。 

以下交易记录将出现。

|  描述                               | 科目             | 借方    | 贷方   |
|-------------------------------------------|---------------------|----------|----------|
| 采购，产品收据采购对方科目 | 应计采购   | 1,600.00 |          |
| 供应商余额                            | 应付帐款    |          | 1,600.00 |
| 采购，固定资产收货             | 计算机支出    | 1,600.00 |          |
| 采购，产品收据采购        | 未开票收货 |          | 1,600.00 |

最后，该会计会复查所有具有”尚未购置“状态的固定资产。 因此，新的笔记本电脑资产被复查。 该会计然后从固定资产日记帐行打开“购置方案”页，为具有发票但其状态仍为”尚未购置“的所有资产创建购置交易记录。 在过帐日志时，将笔记本电脑资产的状态更改为“未结”。 贷记固定资产发货帐户，并借记资产购置科目。 

以下是此场景的变化形式：

-   如果固定资产设置为过帐供应商发票时允许过帐资产购置交易记录，该会计将不必使用固定资产中的购置方案，因为将创建购置交易记录。 此外，当您过帐供应商发票时更新不同的发票。 代替计算机支出，借记固定资产收货库存帐户，另外两种交易记录将发生：借记资产购置科目，贷记固定资产发货库存帐户科目。
-   如果在过帐产品收货时未选中“创建新的固定资产”选项，则此时将不创建资产。 如果您在过帐供应商发票之前选择了“创建新的固定资产”选项，该资产会被创建而且具有”尚未购置“状态，或具有“未结”状态（过帐供应商发票时）。
-   如果笔记本电脑成本为 1,400 而不是 1,600，则未达到资本化阈值。 因此，创建资产并清除“折旧”选项。
-   如果使用某一发票登记簿，则您在过帐该发票登记簿以检索凭证后使用“发票审核日记帐”页面，将采购订单链接到发票，选中“创建新的固定资产”选项，然后过帐该供应商发票。 如果您是可以创建购置交易记录的用户组的成员，则创建该购置，并且该资产具有“未结”状态。
-   如果只接收了部分数量，则由于用户组限制不为第一个供应商发票创建资产购置。 只有在已为第一个供应商发票输入了购置交易记录，并且您是允许过帐购置的用户组的成员的情况下，才能为完成订购数量的第二个供应商发票过帐购置。


有关详细信息，请参阅[固定资产集成](fixed-asset-integration.md)。





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

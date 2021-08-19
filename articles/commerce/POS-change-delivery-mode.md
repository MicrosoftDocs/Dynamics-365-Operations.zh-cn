---
title: 在 POS 中更改交货方式
description: 此主题介绍如何在 POS 中配置和使用更改交货方式操作。
author: hhainesms
ms.date: 03/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: ef778763b26954057b83df3e963e34008819fd208a55d55e07075853ffce8b35
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714032"
---
# <a name="change-mode-of-delivery-in-pos"></a>在 POS 中更改交货方式

[!include [banner](includes/banner.md)]

此主题介绍如何在销售点 (POS) 环境中设置和使用“更改交货方式”功能。 

在 Dynamics 365 Commerce 版本 10.0.10 及更高版本中，可将 **更改交货方式** 操作 (647) 添加到您的 POS 屏幕布局。

更改交货方式功能让您可以选择更改 POS 交易记录中一个或多个装运配置的销售行的交货方式。 在 Commerce 的之前版本中，如果要更改现有行中为装运配置的交货方式，必须完成整个 **全部装运** 或 **装运所选产品** 配置流。 此流程需要大量时间，可能导致意外更改行的交货源或交货日期。 此新功能提供了一种备选方法，可以有效更新这些销售行的交货方式。

有关如何向 POS 按钮网格中的按钮添加操作的详细信息，请参阅[销售点的屏幕布局](pos-screen-layouts.md)。

在 POS 中配置此功能之后，如果选择 **更改交货方式**，将显示一个列表页，可供您选择要更改其交货方式的交易记录的行。 可以选择部分或全部行，也可以退出但不进行任何更改。 之前为装运配置的销售行是列表中您只能更改的行。 如果要将为提货或送货上门指定的行更改为装运，必须使用 **全部装运** 或 **装运所选产品** 操作。 相反，如果要将指定为装运的行更改为提货或送货上门，必须使用 **全部提货**、**所选产品提货**、**全部送货上门** 或 **所选产品送货上门** 操作。

选择要更改的行之后，请单击 **更改交货方式** 以便显示有关选择交货方式选项的提示。 如果选择要更改多个行，POS 将仅显示已经配置为对所选全部产品允许的交货方式。 可以将交货方式配置为支持特定产品和交货地址。 如果一个产品和地址的组合可以接受某种交货方式，但是另一个所选产品和地址的组合不能接受该交货方式，则该交货方式不可用。 如果要为一个产品选择另一个产品不支持的交货方式，可能需要逐一选择行，并分别更改各行的交货方式。  

选择新交货方式之后，将显示交易记录页。 若要查看新交货方式的选择情况，请选择交易记录列表中的 **交货** 选项卡。

## <a name="additional-resources"></a>其他资源

[创建呼叫中心订单](tasks/create-call-center-orders.md)

[按交货模式自定义事务电子邮件](customize-email-delivery-mode.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
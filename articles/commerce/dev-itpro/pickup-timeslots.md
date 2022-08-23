---
title: 创建和更新客户提货时隙
description: 本文介绍如何在 Commerce Headquarters 中创建、配置和更新客户提货时隙。
author: anupamar-ms
ms.date: 01/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-09-20
ms.dyn365.ops.version: Retail 10.0.15 update
ms.custom: ''
ms.search.industry: Retail
ms.openlocfilehash: 319b2ac2a652e633bc70c477dab52e2676c17001
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282825"
---
# <a name="create-and-update-time-slots-for-customer-pickup"></a>创建和更新客户提货时隙

[!include [banner](../../includes/banner.md)]

本文介绍如何在 Commerce Headquarters 中创建、配置和更新客户提货时隙。

时隙功能让零售商可以为打开客户提货交货方式的物料定义时隙。 时隙让零售商可以定义可以从商店提货的日期和时间。 零售商还可以定义可以在给定期间内提货的订单数量。 通过这种方式，零售商可以限制可以在给定日期和给定时间提货的订单数量。 结果是为其客户提供更高质量的体验。

> [!NOTE]
> 时隙功能在 Microsoft Dynamics 365 Commerce 版本 10.0.15 和更高版本中提供。

下图显示了在电子商务结帐期间选择时隙的示例。

![电子商务结帐期间时隙选择的示例。](../dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="time-slot-properties"></a>时隙属性

时隙是客户可以选择从特定商店或位置提货的特定间隔。 只有在 Dynamics 365 Commerce 中配置了客户提货交货方式时，时隙管理功能才可用。

时隙使用以下属性定义：

- **交货方式** – 指定应用时隙的提货交货方式。
- **最少天数** 和 **最多天数** – 指定相对于下订单日期可以选择提货的最早和最晚日期。 

    **最少天数** 属性确保零售商在提货之前有足够的时间处理订单来为提货准备好订单。 **最多天数** 属性确保用户不能选择距离现在太远的将来日期。 例如，如果最小值设置为 **1**，下订单的日期是 9 月 20 日，订单可以提货的最早日期是下一个合格日期（9 月 21 日）。 以类似的方式，通过设置最大值，您可以定义可以提取订单的最大天数。 定义最小值和最大值后，站点用户在结帐期间只能看到和选择一组特定日期。

    您可以将最小值设置为小于 1 的十进制值。 例如，如果下订单之后四个小时可以提货，应将最小值设置为 **0.17**（= 4÷24，四舍五入到小数点后两位）。 但是，如果将最小值设置为大于 1 的十进制值，值始终会向上舍入到最接近的整数。 例如，值 **1.2** 将向上舍入到 **2**。 同样，如果将最大值设置为一个十进制值，值也始终会向上舍入到最接近的整数。 

- **开始日期** 和 **结束日期** – 指定时隙的开始和结束日期。 每个时隙条目都有开始日期和结束日期。 因此，您可以灵活地在全年中添加不同的时隙（例如，假日期间提货）。 如果下订单后更改了时隙的开始日期，更改不会应用于该订单。 在定义开始日期和结束日期时，必须考虑商店歇业日期（例如，圣诞节），应确保不要为那些日期定义时隙。
- **有效提货时间** – 指定允许提货的时间段。 例如，每天的提货时间可以在下午 2 点到 5 点之间。 此属性让提货时间可以不受商店营业时间的影响。 因此，零售商可以配置满足其特定业务要求的提货时间。 定义有效提货时间时，必须考虑商店营业时间，确保没有将商店关门后的时间定义为提货时间。

    > [!NOTE]
    > 商店提货时间必须使用相应商店的时区定义。

- **时隙间隔** – 指定可以分配给每个时隙的持续时间。 例如，每个时隙的持续时间可以以 15 分钟、30 分钟或一个小时为增量。 如果时隙值为 0，该时隙在开始时间和结束时间之间的整个持续时间内都可用。
- **每间隔时隙** – 指定每个时隙间隔内可以提货的客户或订单数量。 例如，输入 **1**、**2**、**3** 或任何其他整数。
- **有效日期** – 指定提货时隙在一周的哪一天有效。 此属性让零售商可以定义要支持提供订单的日期。
- **零售渠道** – 指定零售渠道。 每个时隙可以与一个或多个零售商店关联。 根据每个商店的营业时间，可以创建一个或多个时隙条目并将其与渠道关联。 

<!-- ![HQ Timeslot overview.](../dev-itpro/media/Curbside_timeslot_Settings_overview.PNG) -->

每个渠道只能配置一个时隙模板。 这些渠道包括实体商店、呼叫中心、移动设备和电子商务网站。

## <a name="configure-the-time-slot-feature-in-commerce-headquarters"></a>在 Commerce headquarters 中配置时隙功能

必须在 Commerce headquarters 中为每种提货交货方式定义时隙，销售点 (POS) 和电子商务渠道才能够进行引用。

- 每个商店或渠道只能与一个时隙模板关联。
- 创建的每个时隙对于每个模板中的每个交货方式应该是唯一的。
- 配置时隙功能后，时隙日历将对所选商店或商店组可用。 它还会在 POS 上可见，供用户引用。

要在 Commerce headquarters 中配置时隙功能，请按照下列步骤操作。

1. 转到 **Commerce** \> **渠道设置** \> **商店提货时隙**。
1. 选择 **新建** 创建新时隙模板。 若要使用现有模板，请在左窗格中选择模板。
1. 在 **时隙 ID** 和 **说明** 字段中输入值。
1. 在 **订单提货 - 时间设置** 快速选项卡上，选择 **添加**。
1. 在 **订单提货 - 时间设置** 对话框中，定义日期范围、交货方式、交货有效时间、有效日期、时隙间隔、每个间隔的时隙以及其他设置。

    如果在可预见的将来时隙是静态的，将 **结束日期** 字段设置为 **从不**。

    > [!NOTE]
    > 您可以创建多个模板，但只有一个模板可以与一个渠道或商店关联。

    ![“订单提货 - 时间设置”对话框。](../dev-itpro/media/Curbside_timeslot_Settings_Page.PNG)

1. 当您完成时，选择 **确定**。
1. 如果一天中的时隙会变化，请在 **订单提货 - 时间设置** 快速选项卡上创建其他条目，以确保日期和时间不会重叠。
1. 在 **零售渠道** 快速选项卡上，选择 **添加** 将时隙模板与将使用该模板的商店或渠道关联。
1. 在 **选择组织节点** 对话框中，使用箭头按钮选择（或清除选择）应与模板关联的商店、地区和组织。

    <!-- ![HQ Timeslot overview.](../dev-itpro/media/Curbside_timeslot_Settings_overview.PNG) -->

1. 当您完成时，选择 **确定**。
1. 在 **配送计划** 页，运行 **1070** 和 **1135** 作业将数据与渠道同步。

## <a name="time-slot-selection-for-pos-orders"></a>POS 订单的时隙选择

在 POS，当订单或订单行标识要提货时，出纳可以选择提货商店或位置以及日期和时隙。 如果客户有其他商店的提货单，收银员可以选择该商店的可提货日期。 商店查找将提供对日期和商店营业时间的引用。

下图显示了 POS 订单的时隙选择的示例。

![POS 订单的时隙选择的示例。](../dev-itpro/media/Curbside_timeslot_POS.png)

## <a name="time-slot-selection-for-e-commerce-orders"></a>电子商务订单的时隙选择

有关如何让时隙选择对电子商务订单可用的信息，请参阅[提货信息模块](../pickup-info-module.md)。

> [!NOTE]
> 仅当提货信息模块已添加到该页面时，用户才能在 Commerce 站点的结帐页面查看或编辑提货时隙。 如果结帐页面不包含提货信息模块，下订单时不会让用户指定或查看时隙信息。

下图显示了一个已选择提货时隙的电子商务订单的示例。

![已选择提货时隙的电子商务订单的示例。](../dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="time-slot-selection-for-call-center-orders"></a>呼叫中心订单的时隙选择

在呼叫中心应用中，呼叫中心代理可以选择提货商店或位置，以及下图中突出显示的日期和时隙。

![已选择提货时隙的呼叫中心订单的示例。](../dev-itpro/media/Curbside_timeslot_callcenter.png)

## <a name="additional-resources"></a>其他资源

[提货信息模块](../pickup-info-module.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

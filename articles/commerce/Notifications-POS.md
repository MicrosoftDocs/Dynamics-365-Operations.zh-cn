---
title: 在销售点 (POS) 中显示订单通知
description: 本文介绍如何在销售点和通知框架中启用订单通知。
author: ShalabhjainMSFT
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations, RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: a9e646d6bf48461e78dc75c8a154f2fbf1443393
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853947"
---
# <a name="show-order-notifications-in-the-point-of-sale-pos"></a>在销售点 (POS) 中显示订单通知

[!include [banner](includes/banner.md)]

可以为商店助理分配其商店中的各种任务，例如履行订单或执行库存接收或库存盘点。 销售点 (POS) 客户端提供一个应用程序，可供通过店员所有这些任务。 POS 中的通知框架可以提供帮助，方法是让零售商配置基于角色的通知。 从具有应用程序更新 5 的 Dynamics 365 Retail 开始，这些通知仅可针对 POS 操作进行配置。

系统可以显示有关 *订单履行* 操作的通知，从 Commerce 版本 10.0.18 开始，还可以显示有关 *撤回订单* 操作的通知。 但是，由于该框架设计为可扩展，所以开发人员可以[编写有关任何操作的通知处理程序](dev-itpro/extend-pos-notification.md)，并在 POS 中显示相应操作的通知。

## <a name="enable-notifications-for-order-fulfillment-or-recall-order-operations"></a>启用用于订单履行或撤回订单操作的通知

要启用用于订单履行或撤回订单操作的通知，请执行以下步骤。

1. 转至 **Retail 和 Commerce \> 渠道设置 \> POS 设置 \> POS \> 操作**。
1. 搜索 **订单履行** 操作或 **撤回订单** 操作，然后为其选中 **启用通知**，以便指定通知框架应针对此操作侦听处理程序。 如果实施该处理程序，将在 POS 中显示有关此操作的通知。
1. 转至 **Retail 和 Commerce \> 员工 \> 工作人员**。
1. 选择 **Commerce** 选项卡，选择一个工作人员行，然后选择 **POS 权限**。 选择 **通知** 快速选项卡以将其展开，然后添加您已为其启用通知的操作。 如果要为工作人员配置单个通知，请确保 **显示顺序** 值设置为 **1**。 如果要配置多个操作，请设置 **显示顺序** 值，以指示显示通知所应采用的顺序。 

      仅针对在 **通知** 快速选项卡上添加的操作显示通知。 只有在 **POS 操作** 页上选中了这些操作的 **启用通知** 复选框后，才能在此添加操作。 此外，仅当将操作添加到了工作人员的 POS 权限，才对这些工作人员显示有关该操作的通知。

    > [!NOTE]
    > 可以在用户级别覆盖通知。 为此，请打开工作人员的记录，选择 **POS 权限**，然后编辑该用户的通知订阅。

1. 转至 **Retail 和 Commerce \> 渠道设置 \> POS 设置 \> POS 配置文件 \> 功能配置文件**。 在 **通知时间间隔** 字段中，指定提取通知的频率。 对于某些通知，POS 必须实时调用后端办公应用程序。 这些调用将消耗后端办公应用程序的计算能力。 因此，设置通知时间间隔时，应同时考虑业务需求和实时调用对后端办公应用程序的影响。 值为 **0**（零）将关闭通知。
1. 转到 **Retail 和 Commerce \> Retail 和 Commerce IT \> 分配计划**。 选择 **1060**（**员工**）计划以同步通知订阅设置，然后选择 **立即运行**。 接下来，选择 **1070**（**渠道配置**）计划以同步权限时间间隔，然后选择 **立即运行**。

## <a name="view-notifications-in-the-pos"></a>在 POS 中查看通知

完成上述步骤之后，工作人员就可以在 POS 中查看通知。 要查看通知，请选择 POS 右上角的通知图标。 通知面板将出现，并显示有关为工作人员配置的操作的通知。 

对于 **订单履行** 操作，通知面板将显示以下组：

- **商店提货** - 此组显示计划从当前商店提货的单个订单行的计数。 您可以选择组上的数字以使用筛选器打开 **订单履行** 操作，从而仅显示为从当前商店取货而设置的有效订单行。
- **从商店装运** – 该组显示已配置为从用户当前商店装运的单个订单行的数量。 您可以选择组上的数字以使用筛选的视图打开 **订单履行** 操作，此视图仅显示为从当前商店装运而设置的有效订单行。

对于 **撤回订单** 操作，通知面板将显示以下组：

- **要履行的订单** – 该组显示为从用户当前商店执行提货或装运而配置的订单的计数。 您可以选择组上的数字以使用筛选视图打开 **撤回订单** 操作，该视图仅显示用户的当前商店为在店内提货或从商店装运方案而需要履行的未结订单。
- **要提货的订单** - 此组显示计划从当前商店提货的订单的计数。 您可以选择组上的数字以使用筛选视图打开 **撤回订单** 操作，该视图仅显示需要履行的未结订单以便客户从用户的当前商店提货。
- **要装运的订单** – 此组显示要从用户的当前商店装运的订单数。 您可以选择组上的数字以使用筛选视图打开 **撤回订单** 操作，该视图仅显示需要履行的未结订单以便从用户的当前商店装运。

对于订单履行和撤回订单通知，当流程对新订单进行提货时，通知图标将更改，以指示有新通知，并将更新相应组的计数。 尽管组按照定期时间间隔刷新，但是 POS 用户随时可以通过选择组旁边的 **刷新** 来手动刷新组。 最后，如果组有当前工作人员尚未查看的新项，则该组将显示一个爆炸符号以指示新内容。

## <a name="enable-live-content-on-pos-buttons"></a>在 POS 按钮上启用实时内容

POS 按钮现在可以显示计数以帮助工作人员轻松确定哪些任务需要他们立即注意。 若要在 POS 按钮上显示此编号，必须完成本文前面介绍的通知设置（即，必须启用有关操作的通知，设置通知时间间隔和更新工作人员的 POS 权限组）。 此外，还必须打开按钮网格设计器，查看按钮的属性，以及选中 **启用实时内容** 复选框。 在 **内容对齐** 字段中，可选择计数在按钮右上角（**靠上右对齐**）还是中央（**居中**）显示。

> [!NOTE]
> 仅当按照本文前面的说明在 **POS 操作** 页上为操作选中了 **启用通知** 复选框，才能为操作启用实时内容。

下图显示按钮网格设计器中的实时内容设置。

![按钮网格设计器中的实时内容设置。](./media/ButtonGridDesigner.png "按钮网格设计器中的实时内容设置")

若要在按钮上显示通知数量，需要确保更新正确的屏幕布局。 若要确定 POS 使用的屏幕布局，请选择右上角的 **设置** 图标，然后记下 **屏幕布局 ID** 和 **布局分辨率**。 现在使用 Edge 浏览器转到 **屏幕布局** 页面，找到上面确定的 **屏幕布局 ID** 和 **布局分辨率**，然后选中 **启用动态内容** 复选框。 转到 **Retail 和 Commerce \> Retail 和 Commerce IT \> 配送计划**，然后运行 1090（收银机）作业以同步布局更改。

![查找 POS 使用的屏幕布局。](./media/Choose_screen_layout.png "查找屏幕布局")

下图显示在 **内容对齐** 字段中选择 **靠上右对齐** 与 **居中** 对各种尺寸的按钮的影响。

![POS 按钮上的实时内容。](./media/ButtonsWithLiveContent.png "POS 按钮上的实时内容")

[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: 计算零售渠道的库存现有量
description: 此主题介绍可用于显示商店和在线渠道的现有库存的选项。
author: hhainesms
manager: annbe
ms.date: 08/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhainesms
ms.search.validFrom: 2020-02-11
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 6d25a426268ebfb6990eb3dadb1ad451f86f59a1
ms.sourcegitcommit: 65a8681c46a1d99e7ff712094f472d5612455ff0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/13/2020
ms.locfileid: "3694914"
---
# <a name="calculate-inventory-availability-for-retail-channels"></a>计算零售渠道的库存现有量

[!include [banner](../includes/banner.md)]

此主题介绍公司如何使用 Microsoft Dynamics 365 Commerce 查看在线渠道和商店渠道中的产品的估计现有量。

## <a name="accuracy-of-calculation"></a>计算的准确性

Commerce 使用多个服务器和数据库确保可扩展性和性能。 因此，请务必了解通过销售点 (POS) 应用程序提供的可用库存值、电子商务库存现有量应用程序编程接口 (API)，以及 Commerce Headquarters 中的现有库存页面可能达不到实时 100% 准确。 如果尚未将为在线渠道或商店渠道中的产品创建的交易同步到 Commerce Headquarters 服务器和数据库，则 Commerce Headquarters 中的现有库存页可能不显示这些产品的准确实时库存值。 相反，如果配置了公司，因此 Commerce Headquarters 或其他集成应用程序中的用户可以销售、接收、退回或调整商店或在线仓库的库存，则 POS 或在线渠道可能没有显示物料的准确实时现有值所需全部信息。

此主题介绍可经常运行以帮助限制应用程序或渠道之间的延迟的数据同步流程。 但是，请务必了解运行期间提供的所有现有量数据都被视为估计值。 因此，如果您尝试将应用程序提供的现有库存量与货架上的实际物理库存进行比较，或者如果您尝试将 POS 中显示的现有值与 Commerce Headquarters 中为同一个仓库找到的现有数据进行比较，值可能不同。 运行期间的此差异是正常的，不应被视为问题。 如果要审核数据和确保库存现有量 API 和 Commerce Headquarters 中提供的值与您在商店或仓库货架中找到的实际物理单元匹配，最佳处理时间是在渠道结束☭当天经营且 Commerce Headquarters 与渠道之间已经正确同步了所有交易之后。

## <a name="use-inventory-lookup-apis-for-e-commerce-inventory-availability-requests"></a>将库存查找 API 用于电子商务库存现有量请求

客户在电子商务网站中购物时，您可以使用以下 API 显示产品的库存现有量。

- **GetEstimatedAvailability** – 此 API 用于获取电子商务渠道仓库或链接到电子商务渠道的履行组配置的所有仓库中的物料的库存现有量。 此 API 也可基于经度和维度数据用于特定搜索区域或半径中的仓库。
- **GetEstimatedProductWarehouseAvailability** – 此 API 用于向特定仓库请求某个物料的库存。 例如，可在涉及订单装货时将其用于显示库存现有量。

> [!NOTE]
> 这些 API 取代了 Dynamics 365 Retail 版本 10.0.7 及更低版本中的 **GetProductAvailabilities** 和 **GetAvailableInventoryNearby** API。

这两个 API 都从 Commerce 服务器获取数据并提供某个产品或产品变型与仓库的特定组合的现有库存估算。 虽然 Commerce 服务器上的其他 API 可以直接访问 Commerce Headquarters 以获取产品的现有数量，我们仍然不建议在电子商务环境中使用，因为存在潜在性能问题，并且这样的频繁请求可能会对 Commerce Headquarters 服务器造成相关影响。 此外，如果现有库存是通过 Commerce 服务器计算的，则计算中很可能包含最近电子商务交易中已售出，但尚未同步到 Commerce Headquarters 的库存。 虽然 Commerce Headquarters 中可能没有有关这些交易的信息，但是 Commerce 服务器和渠道数据库有这些数据。 因此，将考虑这些数据，并且这些数据可帮助提高产品现有库存估计的准确性。

### <a name="get-started-with-e-commerce-calculated-inventory-availability"></a>电子商务计算库存现有量入门

必须先在 Commerce Headquarters 中通过**功能管理**工作区启用**优化的产品可用性计算**功能，才能使用前面介绍的两个 API。

必须先处理 Commerce Headquarters 的库存现有量定期快照并将该快照发送到 e-Commerce Commerce Scale Unit 使用的渠道数据库，这些 API 才能计算物料的库存现有量最佳估计。 该快照提供 Commerce Headquarters 拥有的与某个产品或产品变型与仓库的特定组合的库存现有量有关的信息。 其中可能包含库存收货，装运或 Commerce Headquarters 中执行的其他流程导致的库存调整或移动，以及电子商务渠道仅因为同步流程而拥有的相关信息。

**产品可用性**作业创建的数据库快照仅计算在创建该快照时 Commerce Headquarters 中处理和过帐的库存交易记录。 如果在 POS 应用程序中通过付现自提或异步客户订单销售销售了某个商店仓库中的一个产品，Commerce Headquarters 不会立即拥有有关此销售的相关库存问题交易记录的信息。 只有在 P 作业将相关交易记录从商店的渠道数据库上传到 Commerce Headquarters 中，并且通过对帐单过帐或缓慢馈送过帐流程创建了相关销售订单，才会有与这些商店销售类型的所销售库存有关的信息。 在 Commerce Headquarters 中创建订单的过程将创建相关库存交易记录。 对于电子商务渠道订单，只有在通过 P 作业将交易记录发送到 Commerce Headquarters，并且完成了订单同步过程，Commerce Headquarters 才会拥有与库存交易记录有关的信息。 因此，请务必了解因为分散的服务器中一直在不停地处理销售，所以**产品可用性**作业中提供的库存快照值可能不是实时 100% 准确的。

若要在 Commerce Headquarters 中创建库存快照，请执行以下步骤。

1. 转到 **Retail 和 Commerce \> Retail 和 Commerce IT \> 产品和库存 \> 产品可用性**。
1. 选择**确定**运行**产品可用性**作业。 也可以计划此作业，使其批量运行。

**产品可用性**作业运行完毕之后，必须将捕获的数据推送到电子商务渠道数据库，这样在计算估计现有库存时，才会考虑最新的 Commerce Headquarters 库存快照。

1. 转到 **Retail 和 Commerce \> Retail 和 Commerce IT \> 分配计划**。
1. 运行 **1130**（**产品可用性**）作业将**产品可用性**作业创建的快照数据从 Commerce Headquarters 同步到渠道数据库。

从 **GetEstimatedAvailability** 或 **GetEstimatedProductWarehouseAvailability** API 请求库存现有量时，将运行计算，以便尝试获取产品的最佳可能库存估计。 此计算引用在渠道数据库中，但 1130 作业提供的快照数据库中尚不包含的任何电子商务客户订单。 此逻辑的执行方法是，跟踪 Commerce Headquarters 中最后处理的库存交易记录，并将其与渠道数据库中的交易记录进行比较。 其提供渠道端计算逻辑的基准，因此可以将电子商务渠道数据库中客户订单销售交易记录中进行的更多库存移动计入 API 提供的估计库存值中。

渠道端计算逻辑返回估计的物理可用值，以及请求的产品和仓库的总可用值。 如果您希望，可以在电子商务网站中显示这些值，也可以将其用于在电子商务网站中触发其他业务逻辑。 例如，可以显示“库存不足”消息，而不是 API 传递的实际现有数量。

渠道端电子商务 API 用于估计库存值的计算逻辑只能基于渠道数据库中已创建，但尚未在 Commerce Headquarters 中同步和过帐的客户订单评估库存。 如果渠道数据库中还包含商店特定的仓库的付现自提销售的交易数据，则付现自提销售不计入这些仓库的渠道端电子商务计算。

## <a name="configure-the-inventory-lookup-operation-in-the-pos-channel"></a>配置 POS 渠道中的库存查找操作

在 Retail 版本 10.0.9 及更低版本中，POS 中的**库存查找**操作使用对 Commerce Headquarters 的实时服务调用获取所选产品的库存信息（用户的当前商店的库存信息和商店的渠道配置中为履行组配置的任何其他商店的库存信息）。 在 Commerce 版本 10.0.10 及更高版本中，您可以关闭对 Commerce Headquarters 的实时服务调用。 而是可以使用 Commerce 服务器中的渠道端计算确定商店和履行组中定义的其他任何位置实际可用的现有库存。 对于互联网连接不可靠的位置，此渠道计算的库存配置也非常有用，因为不必在线即可从 Commerce Headquarters 获取库存查找。

正确配置和管理渠道端计算时，可以提供更可靠的当前商店库存估计，因为其使用位于 Commerce 渠道数据库中，但是 Commerce Headquarters 可能还没有其相关信息的交易数据。 例如，如果在 POS 中对库存查找使用现有实时服务调用，Commerce Headquarters 可能还没有有关刚对产品进行的现金提货销售的信息。 因此，Commerce Headquarters 为该产品返回的现有库存值可能会超过商店的实际现有库存一个单位。 但是，如果使用渠道端计算，可以将现金提货销售计入计算，并从显示的现货值中扣除。 虽然渠道端计算和实时服务调用提供的值都仅是现有库存的估计，则对于当前商店来说，渠道端计算提供的值可能准确得多。

### <a name="get-started-with-pos-channel-side-calculated-inventory-availability"></a>POS 渠道端计算库存现有量入门

若要使用渠道端计算逻辑并关闭 POS 应用程序中库存查找的实时服务调用，首先必须在 Commerce Headquarters 中通过**功能管理**工作区启用**优化的产品可用性计算**功能。 除了启用该功能，还必须对**功能配置文件**进行更改。

若要更改**功能配置文件**，请执行以下步骤：

1. 转至 **Retail 和 Commerce \> 渠道设置 \> POS 设置 \> POS 配置文件 \> 功能配置文件**。
1. 选择一个功能配置文件。
1. 在**功能**快速选项卡的**库存可用性计算**部分中，将**库存可用性计算模式**字段从**实时服务**更改为**渠道**。 默认情况下，所有功能配置文件都使用实时服务调用。 因此，如果要使用通道端计算逻辑，必须更改此字段的值。 此更改将影响链接到所选功能配置文件的每家零售商店。

然后必须执行以下步骤通过配送计划流程将更改同步到渠道。

1. 转到 **Retail 和 Commerce \> Retail 和 Commerce IT \> 分配计划**。
1. 运行 **1070**（**渠道配置**）作业。

完成配置后，当 POS 应用程序中的用户使用**库存查找**查找（标准视图和矩阵视图）时，提供的有关物理可用库存的信息不再使用实时服务调用。 而是根据从 Commerce Headquarters 交付给渠道数据库的最新已知快照计算当前商店和履行组中的所有商店的物理可用库存的相关数据。 渠道端计算基于所选产品在渠道数据库中 1130 作业上次同步的快照内不包含的更多销售或退货交易进一步优化快照值，以便调整物理可用值。 如果渠道数据库中不包含履行组中的任何仓库或商店的交易数据，则不包含可计入值的重新计算的更多交易记录。 因此，可以对这些仓库或商店显示的现有库存最佳估计是上一个已知 Commerce Headquarters 快照的数据。

当选择了订单履行行且用户查看所选物料的现有库存的**详细信息**面板时，POS 的**订单履行**屏幕利用渠道端计算显示物料的现有库存。

## <a name="optimize-your-inventory-data"></a>优化您的库存数据

若要尽量确保库存的估计准确，务必使用以下 Commerce 批处理作业并经常运行这些作业：

- **P 作业** – P 作业位于**配送计划**页中，应该经常运行。 此作业将电子商务订单、POS 创建的异步客户订单，以及 POS 创建的现金提货订单从渠道数据库导入到 Commerce Headquarters 中，以便进一步处理这些订单。 此数据从渠道同步到 Commerce Headquarters 之前，Commerce Headquarters 没有有关这些交易对仓库中的产品产生的库存调整的数据。
- **同步订单** – 此作业处理 Commerce Headquarters 中 P 作业提供的原始交易数据，并在 Commerce Headquarters 中将电子商务和异步客户订单交易记录转换为销售订单。 处理此作业并创建销售订单之前，不创建任何库存交易记录。 因此，Commerce Headquarters 中的现有库存不考虑这些交易记录。
- **批量计算交易记录对帐单** – 对于商店中创建的现金提货交易记录，缓慢馈送过帐流程可以确保有效更新与销售有关的库存。 若要最有效地处理现金提货订单的库存交易记录，请确保将系统配置为使用[缓慢馈送过帐](https://docs.microsoft.com/dynamics365/commerce/trickle-feed)。
- **批量过帐交易记录对帐单** – 缓慢馈送过帐也需要此作业。 然后是**批量计算交易记录对帐单**作业。 此作业系统地过帐计算对帐单，因此将在 Commerce Headquarters 中为现金提货销售创建销售订单，而 Commerce Headquarters 可以更准确地体现商店的库存。
- **产品可用性** – 此作业从 Commerce Headquarters 创建库存快照。
- **1130（产品可用性）**– 此作业位于**配送计划**页面中，应该在**产品可用性**作业之后立即运行。 此作业将库存快照数据从 Commerce Headquarters 传输到渠道数据库。

建议您不要过于频繁地（每隔几分钟）运行这些批处理作业。 频繁运行将使 Commerce headquarters (HQ) 超负荷，可能影响性能。 通常，合理的做法是每小时运行一次产品可用性和 1130 作业，并计划 P 作业、同步订单，并以相同或更高频率缓慢馈送与过帐相关的作业。

> [!NOTE]
> 出于性能原因，使用渠道端库存现有量计算和电子商务 API 的渠道端库存逻辑或新的 POS 渠道端库存逻辑创建库存现有量请求时，此计算使用缓存确定是否经过了足够的时间来判定是否再次运行计算逻辑。 默认缓存设置为 60 秒。 例如，您为商店开启了渠道端计算，并在**库存查找**页中查看了某个产品的现有库存。 如果之后销售了一个单位的该产品，清除缓存之前，**库存查找**页不会显示减少的库存。 用户在 POS 中过帐交易记录之后，应该等待 60 秒，之后再验证现有库存是否已减少。

如果业务方案需要更小的缓存时间，请联系产品支持代表获取帮助。

---
title: 计算零售渠道的库存现有量
description: 本文介绍公司如何使用 Microsoft Dynamics 365 Commerce 查看在线渠道和商店渠道中的产品的估计现有量。
author: hhainesms
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-11
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 952acf4cc26815822436bb7a5117775a5f12200c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884103"
---
# <a name="calculate-inventory-availability-for-retail-channels"></a>计算零售渠道的库存现有量

[!include [banner](../includes/banner.md)]

本文介绍公司如何使用 Microsoft Dynamics 365 Commerce 查看在线渠道和商店渠道中的产品的估计现有量。

## <a name="accuracy-of-inventory-availability"></a>库存可用性的准确性

Commerce 使用多个服务器和数据库确保可扩展性和性能。 因此，请务必了解通过销售点 (POS) 应用程序提供的可用库存值、电子商务库存现有量应用程序编程接口 (API)，以及 Commerce Headquarters 中的现有库存页面可能达不到实时 100% 准确。 如果尚未将为在线渠道或商店渠道中的产品创建的交易同步到 Headquarters，则 Headquarters 中的现有库存页可能不显示这些产品的准确实时库存值。 相反，如果配置了公司，因此 Headquarters 或其他集成应用程序中的用户可以销售、接收、退回或调整商店或在线仓库的库存，则 POS 或在线渠道可能没有显示物料的准确实时值所需的全部信息。

请务必了解运行期间提供的所有现有量数据都被视为估计值。 因此，如果您尝试将应用程序提供的现有库存量与货架上的实际物理库存进行比较，或者如果您尝试将 POS 中显示的现有值与 Headquarters 中为同一个仓库找到的现有数据进行比较，值可能不同。 运行期间的此差异是正常的，不应被视为问题。 如果要审核数据和确保 POS、API 和 Headquarters 中提供的值与您在商店或仓库货架中找到的实际物理单元匹配，最佳处理时间是在渠道结束当天经营且 Headquarters 与渠道之间已经正确同步了所有交易之后。

## <a name="channel-side-inventory-calculation"></a>渠道端库存计算

渠道端库存计算是一种机制，它将 Commerce headquarters 中最后的已知渠道库存数据作为基准，然后将不包含在该基准中的、在渠道端发生的其他库存变化考虑在内，来计算出近实时的估计现有库存量。 

当前在渠道端库存计算逻辑中考虑以下库存变化：

- 通过商店中的现金和结转订单出售的库存
- 通过商店或在线渠道中的客户订单出售的库存
- 退回商店的库存
- 从商店仓库履行的库存（领料、装箱、装运）

若要使用渠道端库存计算，必须启用 **优化的产品可用性计算** 功能。

如果您的 Commerce 环境属于 **10.0.11 到 10.0.8** 版本，请按照以下步骤操作。

1. 在 Commerce Headquarters 中，转到 **Retail 和 Commerce** \> **Commerce 共享参数**。
1. 在 **库存** 选项卡的 **产品可用性作业** 字段中，选择 **将优化后的流程用于产品可用性作业**。

如果您的 Commerce 环境属于 **10.0.12 或更高** 版本，请按照以下步骤操作。

1. 在 Commerce Headquarters 中，转到 **工作区 \> 功能管理**，然后启用 **优化的产品可用性计算** 功能。
1. 如果您的在线渠道和商店渠道使用相同的履行仓库，您还必须启用 **增强的电子商务渠道端库存计算逻辑** 功能。 这样，渠道端计算逻辑将考虑在商店渠道中创建的未过帐交易记录。 （这些交易记录可以是付现自提交易记录、客户订单和退货。）
1. 运行 **1070**（**渠道配置**）作业。

如果您的 Commerce 环境是从低于 Commerce 版本 10.0.8 的版本升级而来，在您启用 **优化的产品可用性计算** 功能之后，还必须运行 **初始化 Commerce 计划程序**，此功能才会生效。 若要运行此初始化，请转到 **Retail 和 Commerce** \> **Headquarters 设置** \> **Commerce 计划程序**。

要使用渠道端库存计算，作为先决条件，必须将由 **产品可用性** 作业创建的 Headquarters 中库存数据的定期快照发送到渠道数据库。 该快照提供 Headquarters 拥有的与某个产品或产品变型与仓库的特定组合的库存现有量有关的信息。 它仅包含在获取快照时在 Headquarters 中已处理和过帐的库存交易，由于分散的服务器在持续进行销售处理，因此它实时的准确性可能达不到 100%。

- 如果在 POS 应用程序中通过付现自提或异步客户订单销售销售了某个商店的一个产品，Headquarters 不会立即拥有有关此销售的相关库存问题交易记录的信息。 只有在 P 作业将相关交易记录从商店的渠道数据库上传到 Headquarters，并且通过对帐单过帐或缓慢馈送过帐流程创建了相关销售订单，Headquarters 才会有与这些商店销售类型的所销售库存有关的信息。 在 Headquarters 中创建订单的过程将创建相关库存交易记录。 
- 对于电子商务渠道订单，只有在通过 P 作业将交易记录发送到 Headquarters，并且完成了订单同步过程，Headquarters 才会有与库存交易记录有关的信息。

若要在 Commerce Headquarters 中创建库存快照，请执行以下步骤。

1. 转到 **Retail 和 Commerce \> Retail 和 Commerce IT \> 产品和库存 \> 产品可用性**。
1. 选择 **确定** 运行 **产品可用性** 作业。 您也可以计划此作业来批量运行。

**产品可用性** 作业运行完毕之后，必须将捕获的数据推送到渠道数据库，这样在估计现有库存量的渠道端计算中，才会考虑最新的 Headquarters 库存快照。

要将快照数据从 Headquarters 同步到您的渠道数据库，请按照下列步骤操作。

1. 转到 **Retail 和 Commerce \> Retail 和 Commerce IT \> 分配计划**。
1. 运行 **1130**（**产品可用性**）作业将 **产品可用性** 作业创建的快照数据从 Headquarters 同步到渠道数据库。

## <a name="inventory-availability-apis-for-e-commerce"></a>用于电子商务的库存可用性 API

Commerce 为电子商务场景提供以下 API 来查询产品的库存可用性：

- **GetEstimatedAvailability** – 使用此 API 在在线渠道仓库或链接到在线渠道的履行组的仓库中查询产品或产品变型的库存。
- **GetEstimatedProductWarehouseAvailability** – 使用此 API 查询特定仓库中产品或产品变型的库存。

> [!NOTE]
> 这些 API 取代了 Commerce 版本 10.0.7 及更低版本中的 **GetProductAvailabilities** 和 **GetAvailableInventoryNearby** API。

这两个 API 在内部均使用渠道端计算逻辑，为所需的产品和仓库返回估计的 **实际可用** 数量、**可用总数**、**度量单位 (UoM)** 和 **库存级别**。 如果您希望，可以在电子商务网站中显示这些返回的值，也可以将其用于在电子商务网站中触发其他业务逻辑。 例如，您可以阻止购买具有“库存不足”库存级别的产品。

虽然 Commerce 中提供的其他 API 可以直接访问 Headquarters 以获取产品的现有数量，我们仍然不建议在电子商务环境中使用，因为存在潜在性能问题，并且这样的频繁请求可能会对 Headquarters 服务器造成影响。 此外，通过渠道端计算，上述两个 API 可以通过考虑 Headquarters 尚不了解的渠道中创建的交易来提供对产品可用性更准确的估算。

要定义产品数量在 API 输出中应如何返回，请按照以下步骤操作。

1. 转到 **Retail 和 Commerce \> Headquarters 设置 \> 参数 \> Commerce 参数**。
1. 选择 **库存** 选项卡，然后在 **用于电子商务的库存可用性 API** 快速选项卡上配置 **API 输出中的数量** 设置的值。
1. 运行 **1070**（**渠道配置**）作业将最新设置同步到渠道。

**API 输出中的数量** 设置提供三个选项：

- **返回库存数量** – 所请求产品的实际可用数量和可用总数将在 API 输出中返回。
- **返回库存数量减去库存缓冲** – API 输出中返回的数量将减去库存缓冲值来进行调整。 有关库存缓冲的详细信息，请参阅[配置库存缓冲和库存级别](inventory-buffers-levels.md)。
- **不返回库存数量** – 仅库存级别在 API 输出中返回。 有关库存级别的详细信息，请参阅[配置库存缓冲和库存级别](inventory-buffers-levels.md)。

您可以使用 `QuantityUnitTypeValue` API 参数指定希望 API 返回数量时使用的单位类型。 此参数支持 **库存单位**（默认）、**采购单位** 和 **销售单位** 选项。 返回的数量将舍入到 Headquarters 中定义的对应度量单位 (UOM) 的精度。

**GetEstimatedAvailability** API 提供以下输入参数来支持不同的查询场景：

- `DefaultWarehouseOnly` – 使用此参数查询在线渠道默认仓库中产品的库存。 
- `FilterByChannelFulfillmentGroup` 和 `SearchArea` – 使用这两个参数根据 `longitude`、`latitude` 和 `radius` 从特定搜索区域内的所有提货位置查询产品的库存。 
- `FilterByChannelFulfillmentGroup` 和 `DeliveryModeTypeFilterValue` – 使用这两个参数从链接到在线渠道的履行组并配置为支持某些交货方式的特定仓库查询产品的库存。 `DeliveryModeTypeFilterValue` 参数支持 **所有**（默认）、**装运** 和 **提货** 选项。 例如，在可以从多个装运仓库履行在线订单的场景中，可以使用这两个参数在所有这些装运仓库中查询产品的库存可用性。 在这种情况下，API 将返回每个装运仓库中产品的现有数量和库存级别，以及查询范围内所有装运仓库的聚合数量和聚合库存级别。
 
Commerce 购买框、商店选择器、愿望列表、购物车和购物车图标模块使用上面提到的 API 和参数在整个电子商务站点显示库存级别消息。 Commerce 站点构建器提供各种库存设置来控制促销和购买行为。 有关详细信息，请参阅[应用库存设置](inventory-settings.md)。

## <a name="pos-inventory-lookup-with-channel-side-calculation"></a>POS 库存查找与渠道端计算

在 Commerce 版本 10.0.9 及更低版本中，POS 中的 **库存查找** 操作使用对 Headquarters 的实时服务调用获取所选产品的库存信息（用户的当前商店的库存信息和商店的渠道配置中为履行组配置的任何其他商店的库存信息）。 在 Commerce 版本 10.0.10 及更高版本中，您可以关闭对 Headquarters 的实时服务调用，而改用 Commerce 服务器上的渠道端计算来确定商店和履行组中定义的任何其他位置实际可用的现有库存量。 对于互联网连接不可靠的位置，此渠道计算的库存配置也非常有用，因为不必在线即可从 Headquarters 获取库存查找。

正确配置和管理渠道端计算时，可以提供更可靠的当前商店库存估计，因为其使用位于 Commerce 渠道数据库中，但是 Headquarters 可能还没有其相关信息的交易数据。 例如，如果在 POS 中对库存查找使用现有实时服务调用，Headquarters 可能还没有有关刚对产品进行的现金提货销售的信息。 因此，Headquarters 为该产品返回的现有库存值可能会超过商店的实际现有库存一个单位。 但是，如果使用渠道端计算，可以将现金提货销售计入计算，并从显示的现货值中扣除。 虽然渠道端计算和实时服务调用提供的值都仅是现有库存的估计，则对于当前商店来说，渠道端计算提供的值可能准确得多。

若要在 Commerce Headquarters 中配置 POS **库存查找** 操作以使用渠道端计算逻辑并关闭实时服务调用，首先必须在 Commerce Headquarters 中通过 **功能管理** 工作区启用 **优化的产品可用性计算** 功能，然后按照以下步骤操作。

1. 转至 **Retail 和 Commerce \> 渠道设置 \> POS 设置 \> POS 配置文件 \> 功能配置文件**。
1. 选择一个功能配置文件。
1. 在 **功能** 快速选项卡的 **库存可用性计算** 部分中，将 **库存可用性计算模式** 从 **实时服务** 更改为 **渠道**。 默认情况下，所有功能配置文件都使用实时服务调用。 如果要使用通道端计算逻辑，必须更改此字段的值。 此更改将影响链接到所选功能配置文件的每家零售商店。

然后必须执行以下步骤在 Headquarters 中通过分配计划流程将更改同步到渠道。

1. 转到 **Retail 和 Commerce \> Retail 和 Commerce IT \> 分配计划**。
1. 运行 **1070**（**渠道配置**）作业。

完成配置后，当 POS 应用程序中的用户使用 **库存查找** 查找（标准视图和矩阵视图）时，提供的有关物理可用库存的信息不再使用实时服务调用。 而是根据从 Commerce Headquarters 交付给渠道数据库的最新已知快照计算当前商店和履行组中的所有商店的物理可用库存的相关数据。 渠道端计算基于所选产品在渠道数据库中 1130 作业上次同步的快照内不包含的更多销售或退货交易进一步优化快照值，以便调整物理可用值。 如果渠道数据库中不包含履行组中的任何仓库或商店的交易数据，则不包含可计入值的重新计算的更多交易记录。 因此，可以对这些仓库或商店显示的现有库存最佳估计是上一个已知 Commerce Headquarters 快照的数据。

当选择了订单履行行且用户查看所选物料的现有库存的 **详细信息** 面板时，POS 的 **订单履行** 屏幕利用渠道端计算显示物料的现有库存。

## <a name="optimize-your-inventory-data"></a>优化您的库存数据

若要尽量确保库存的估计准确，务必使用以下 Commerce 批处理作业并经常运行这些作业：

- **P 作业** – P 作业位于 **配送计划** 页中，应该经常运行。 此作业将电子商务订单、POS 创建的异步客户订单，以及 POS 创建的现金提货订单从渠道数据库导入到 Commerce Headquarters 中，以便进一步处理这些订单。 此数据从渠道同步到 Commerce Headquarters 之前，Commerce Headquarters 没有有关这些交易对仓库中的产品产生的库存调整的数据。
- **同步订单** – 此作业处理 Commerce Headquarters 中 P 作业提供的原始交易数据，并在 Commerce Headquarters 中将电子商务和异步客户订单交易记录转换为销售订单。 处理此作业并创建销售订单之前，不创建任何库存交易记录。 因此，Commerce Headquarters 中的现有库存不考虑这些交易记录。
- **批量计算交易记录对帐单** – 对于商店中创建的现金提货交易记录，缓慢馈送过帐流程可以确保有效更新与销售有关的库存。 若要最有效地处理现金提货订单的库存交易记录，请确保将系统配置为使用[缓慢馈送过帐](./trickle-feed.md)。
- **批量过帐交易记录对帐单** – 缓慢馈送过帐也需要此作业。 然后是 **批量计算交易记录对帐单** 作业。 此作业系统地过帐计算对帐单，因此将在 Commerce Headquarters 中为现金提货销售创建销售订单，而 Commerce Headquarters 可以更准确地体现商店的库存。
- **产品可用性** – 此作业从 Commerce Headquarters 创建库存快照。
- **1130（产品可用性）**– 此作业位于 **配送计划** 页面中，应该在 **产品可用性** 作业之后立即运行。 此作业将库存快照数据从 Commerce Headquarters 传输到渠道数据库。

> [!NOTE]
> - 最好的做法是每小时运行一次 **产品可用性** 和 **1130** 作业，并计划 P 作业、同步订单，并以相同或更高频率缓慢馈送与过帐相关的作业。
> - 出于性能原因，使用渠道端库存现有量计算和电子商务 API 的渠道端库存逻辑或 POS 渠道端库存逻辑创建库存现有量请求时，此计算使用缓存确定是否经过了足够的时间来判定是否再次运行计算逻辑。 默认缓存设置为 60 秒。 例如，您为商店开启了渠道端计算，并在 **库存查找** 页中查看了某个产品的现有库存。 如果之后销售了一个单位的该产品，清除缓存之前，**库存查找** 页不会显示减少的库存。 用户在 POS 中过帐交易记录之后，应该等待 60 秒，之后再验证现有库存是否已减少。

如果业务方案需要更小的缓存时间，请联系产品支持代表获取帮助。

[!INCLUDE[footer-include](../includes/footer-banner.md)]

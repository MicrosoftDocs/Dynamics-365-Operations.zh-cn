---
title: 在 POS 中处理序列化产品
description: 本文说明如何在销售点 (POS) 应用程序中管理序列化产品。
author: boycezhu
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 8a715a9d025f36656506daeb9e611bfacdafa102
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880021"
---
# <a name="work-with-serialized-items-in-the-pos"></a>在 POS 中处理序列化产品

[!include [banner](includes/banner.md)]

许多零售商出售需要进行一系列控制的产品。 这些产品称为 *序列化产品*。 一些零售商可能希望将序列号保留在商店或仓库库存中以进行跟踪。 其他零售商可能希望在销售流程中获取序列号，以用于维护和保修目的。 本文说明如何在 Microsoft Dynamics 365 Commerce 销售点 (POS) 应用程序中管理序列化产品。

## <a name="serial-number-configurations"></a>序列号配置

如果为项目分配了跟踪维度组，且该组被设置为允许使用序列号，则该产品被视为序列化产品。 在 Commerce 总部的 **跟踪维度组** 页面中，选择 **有效** 选项以针对库存流程启用序列号，或选择 **在销售流程中有效** 选项以针对销售流程启用序列号。

在 **跟踪维度** 快速选项卡上，打开 **允许空白收据** 参数，以允许序列号在序列化物料库存收货流程中充当可选输入。 关闭此参数则会强制序列号成为必需输入。 同样，**允许空发货** 参数控制库存装运流程期间是否需要序列号。

> [!NOTE]
> 若要使用 **入站库存** 和 **出站库存** POS 操作来注册或验证序列化产品的序列号，必须将该产品配置为要为其分配一个跟踪维组，该组设置为允许针对 **有效** 选项（而不是 **在销售流程中有效** 选项）使用序列号。

## <a name="serial-number-management-page"></a>序列号管理页面

在 **入站库存** 和 **出站库存** POS 操作中，如果正在选择，接收或装运的产品为序列化产品，则 **详细信息** 窗格中包含 **管理序列号** 选项，该选项链接到 **序列号管理** 页面，可在该页面中注册或验证产品的序列号。 或者，您可以通过以下方法打开 **序列号管理** 页面：在订单详细信息视图的应用栏上选择 **序列号** 操作，或者在接收或装运过程中提示您的对话框中选择 **管理序列号** 选项。 

**序列号管理** 页面列出了所有待注册或待验证的已打开序列号行。 此页面上可能有两个选项卡：一个适用于当前产品，另一个适用于订单中的所有序列化产品。

**序列号管理** 页面上的 **状态** 字段提供有关每个序列号所在的当前阶段的信息：

- **未注册** – 尚未提供序列号，或者尚未验证预注册的序列号（在接收流程中）。
- **正在注册** – 序列号已注册并保存在本地商店的渠道数据库中，或者预注册的序列号已通过验证。 只有在完成接收或履行后，状态为 **正在注册** 的序列号才会提交至 Commerce 总部。

## <a name="receive-serialized-items"></a>接收序列化产品

通过 **入站库存** POS 操作，用户可以对序列化产品执行以下任务：

- 当通过采购订单在商店中收到序列化产品时，为这些序列化产品注册序列号。
- 当通过采购订单或转移订单在商店中收到序列化产品时，为这些序列化产品验证预先注册的序列号。

### <a name="register-serial-numbers-against-serialized-items"></a>为序列化产品注册序列号

对于采购订单，序列化产品接收流程中将通过一个对话框提示您，该对话框中有 **管理序列号** 选项。 您可以选择该选项以打开 **序列号管理** 页面并开始注册序列号。 您也可以在接收流程中跳过此步骤，并稍后提供输入，然后再过帐收据。

默认情况下显示了当前产品的选项卡。 所有序列号行都有一个空序列号值，并且状态为 **未注册**。 您可以扫描序列号条形码，也可以在应用栏上选择 **序列号** 以连续输入序列号。 您输入的序列号会出现在列表中，并且其状态会更改为 **正在注册**。 您可以在列表中注册的序列号的最大数目等于接收数量。 如果输入有误，则可以在 **详细信息** 窗格中选择 **编辑** 或 **清除**，以更改输入的序列号。

您还可以在 **序列号管理** 页面的 **所有序列化产品** 选项卡上注册序列号。 在此列表中，选择要为其注册序列号的产品。

### <a name="validate-serial-numbers-on-serialized-items"></a>验证序列化产品的序列号

对于转移订单，出库方必须在装运过程中对序列化产品预先注册序列号。 对于采购订单，供应商可能会通过装运前通知 (ASN) 提供序列号信息，您可以对要装运的产品预先注册编号。 在这两种情况下，序列号在接收之前都是已知的。 因此，在入库端，您只需要验证您已经收到了应该收到的东西即可。

要验证序列号，您可以在接收流程中或在过帐收据之前随时打开 **序列号管理** 页面。 对于每个具有预先注册的序列号的序列化产品，所有序列号都会在此页面上自动设置为 **未注册** 初始状态。 要验证序列号，您可以扫描或输入序列号。 输入序列号后，应用程序将验证它们是否与预注册的序列号匹配。 如果它们匹配，则它们的状态将更改为 **正在注册**。 否则，您会收到一条错误消息。 或者，您可以直接选择序列号，然后选择 **详细信息** 页面中的 **验证序列号** 快速将该序列号标记为已验证。 您可以在列表中验证的序列号的最大数目等于接收数量。

您还可以在 **序列号管理** 页面的 **所有序列化产品** 选项卡上验证序列号。 在此列表中，选择要为其验证序列号的产品。

## <a name="ship-serialized-items"></a>装运序列化产品

通过转运单将序列化产品运出当前商店时，可使用 **出站库存** POS 操作注册序列化产品的序列号。

### <a name="register-serial-numbers-against-serialized-items"></a>为序列化产品注册序列号

对于转运单，序列化产品装运流程中将通过一个对话框提示您，该对话框中有 **管理序列号** 选项。 您可以选择该选项以打开 **序列号管理** 页面并开始注册序列号。 您也可以在装运流程中跳过此步骤，并稍后提供输入，然后再过帐装运。

默认情况下显示了当前产品的选项卡。 所有序列号行都有一个空序列号值，并且状态为 **未注册**。 您可以扫描序列号条形码，也可以在应用栏上选择 **序列号** 以连续输入序列号。 您输入的序列号会出现在列表中，并且其状态会更改为 **正在注册**。 您可以在列表中注册的序列号的最大数目等于装运数量。 如果输入有误，则可以在 **详细信息** 窗格中选择 **编辑** 或 **清除**，以更改输入的序列号。

您还可以在 **序列号管理** 页面中的 **所有序列化产品** 选项卡上注册序列号。 在此列表中，选择要为其注册序列号的产品。

（可选）您可以在序列号注册期间对出站转移单启用序列号可用性验证。 启用此验证之后，如果装运商店的库存中没有您尝试装运的序列号，则会收到错误消息，并且必须提供其他序列号。

若要启用此类验证，首先需要计划定期运行以下作业：

- **Retail 和 Commerce** > **Retail 和 Commerce IT** > **产品和库存** > **具有跟踪维度的产品可用性**
- **Retail 和 Commerce** > **分配计划** > **1130**（**产品可用性**）

## <a name="sell-serialized-items-in-pos"></a>在 POS 中销售序列化产品

虽然 POS 应用程序始终支持销售序列化商品，但在 Commerce 版本 10.0.17 及更高版本中，组织可以启用功能来增强销售配置了序列号跟踪的产品时触发的业务逻辑。

当 **POS 订单捕获和订单履行中增强的序列号验证** 功能启用时，在 POS 中销售序列化产品时，将评估以下产品配置：

- 产品的 **序列类型** 设置（**有效** 或 **在销售中有效**）。
- 产品的 **允许空发货** 设置。
- 产品和/或销售仓库的 **实际负库存** 设置。

### <a name="active-serial-configurations"></a>有效的序列配置

在配置了 **有效** 序列号跟踪维度的 POS 中销售产品时，POS 会启动验证逻辑来阻止用户完成在销售仓库的当前库存中找不到的序列号的序列化产品的销售。 此验证规则有两个例外：

- 如果该产品还配置为启用 **允许空发货**，用户可以跳过序列号输入，直接在不指定序列号的情况下销售产品。
- 如果产品和/或销售仓库配置为启用 **实际负库存**，应用程序接受和销售的序列号无法被确认是否在销售该序列号所依靠的仓库的库存中。 此配置允许该特定产品/序列号的库存交易记录为负，因此系统将允许销售未知序列号。

> [!IMPORTANT]
> 要确保 POS 应用程序可以正确验证所销售的 **有效** 序列类型产品的序列号是否在销售仓库的库存中，需要组织运行 Commerce headquarters 中的 **具有跟踪维度的产品可用性** 作业，并经常通过 Commerce headquarters 运行附带的 **1130** 产品可用性分配作业。 当新的序列化库存被接收到销售仓库中时，为了让 POS 验证所销售的序列号的库存可用性，库存主数据库必须经常使用最新的库存可用性数据来更新渠道数据库。 **具有跟踪维度的产品可用性** 作业为所有公司仓库拍摄主库存的当前快照，包括序列号。 **1130** 分配作业将获取该库存快照并将其与所有已配置的渠道数据库共享。

### <a name="active-in-sales-process-serial-configurations"></a>“在销售流程中有效”序列配置

将序列维度配置为 **在销售流程中有效** 的产品不会通过任何库存验证逻辑，因为此配置意味着库存序列号未预先登记到存货中，序列号仅在销售时捕获。  

如果还为配置了 **在销售流程中有效** 的产品配置了 **允许空发货**，则可以跳过序列号输入。 如果未配置 **允许空发货**，应用程序将需要用户输入序列号，即使不会根据可用库存进行验证。

### <a name="apply-serial-numbers-during-creation-of-pos-transactions"></a>在创建 POS 交易期间应用序列号

POS 应用程序会在销售序列化产品时立即提示用户捕获序列号，但是此应用程序允许用户跳过序列号的输入，直接转到销售流程中的某个点。 当用户开始捕获付款时，应用程序将强制执行并要求为所有未配置为通过未来装运或提货履行的产品输入序列号。 为现金和结转或结转履行配置的任何序列化产品，都需要用户在完成销售之前捕获序列号（或同意将其留空(如果产品配置允许)）。

对于销售的要在将来提货或装运的序列化产品，POS 用户可以在最初跳过输入序列号，仍然可以完成客户订单的创建。   

> [!NOTE]
> 在通过 POS 应用程序销售或履行序列化产品时，销售交易中的序列化产品将被强制选择数量“1”。 这是由在销售行上跟踪序列号信息的方式决定的结果。 通过 POS 销售或履行多个序列化产品的交易时，每个销售行只能配置为数量为“1”。 

### <a name="apply-serial-numbers-during-customer-order-fulfillment-or-pickup"></a>在客户订单履行或提货期间应用序列号

在 POS 中使用 **订单履行** 操作履行序列化产品的客户订单行时，POS 会在最终履行之前强制捕获序列号。 因此，如果在初始订单捕获过程中未提供序列号，则必须在 POS 中在提货、包装或装运流程中捕获序列号。 验证将在每个步骤执行，仅在序列号数据丢失或不再有效时才会要求用户输入序列号数据。 例如，如果用户跳过提货或包装步骤，直接开始装运，而该行尚未登记序列号，POS 将要求在完成最终发票步骤之前输入序列号。 在 POS 中执行订单履行操作过程中强制捕获序列号时，本文前面提到的所有规则仍然适用。 仅配置为 **有效** 的序列化产品会接受序列号库存存货验证。 配置为 **在销售流程中有效** 的产品不会被验证。 如果 **有效** 产品允许 **实际负库存**，则将接受任何序列号，无论存货可用性如何。 对于 **有效** 和 **在销售流程中有效** 产品，如果配置了 **允许空发货**，则用户可以在提货、包装和装运步骤中根据需要将序列号留为空白。

当用户在 POS 中对客户订单执行提货操作时，也会进行序列号验证。 除非序列化产品通过了前面提到的验证，POS 应用程序不允许对序列化产品完成提货。 验证始终基于产品的跟踪维度和销售仓库配置。 

## <a name="additional-resources"></a>其他资源

[POS 中的传入库存操作](./pos-inbound-inventory-operation.md)

[POS 中的传出库存操作](./pos-outbound-inventory-operation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
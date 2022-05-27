---
title: 为交易事件创建电子邮件模板
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中为交易事件创建、上传和配置电子邮件模板。
author: bicyclingfool
ms.date: 12/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 08e247bac577dc0bb8a4635d61f0082793380da9
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722511"
---
# <a name="create-email-templates-for-transactional-events"></a>创建交易事件的电子邮件模板

[!include [banner](includes/banner.md)]


此主题介绍如何在 Microsoft Dynamics 365 Commerce 中为交易事件创建、上传和配置电子邮件模板。

Dynamics 365 Commerce 提供现成的解决方案，用于发送提醒客户有交易事件的电子邮件。 例如，在下订单、准备好提货或已装运时可以发送电子邮件。 此主题介绍创建，上传和配置用于发送交易电子邮件的电子邮件模板的步骤。

## <a name="notification-types"></a>通知类型

当特定事件作为订单和客户生命周期的一部分发生时，可以配置通知来通过电子邮件通知客户。 要配置通知，您必须通过创建 Commerce 电子邮件通知配置文件将电子邮件模板映射到通知类型。 有关如何设置电子邮件通知配置文件的信息，请参阅[设置电子邮件通知配置文件](email-notification-profiles.md)。

Dynamics 365 Commerce 支持以下通知类型。

### <a name="order-created"></a>订单已创建

在 Commerce Headquarters 中创建新销售订单时，将触发 *订单创建* 通知类型。

> [!NOTE]
> 不会为在销售点 (POS) 终端发生的现金和结转交易触发订单创建通知类型。 在这种情况下，将改为生成电子邮件和/或打印收据。 有关详细信息，请参阅[从 Modern POS (MPOS) 发送电子邮件收据](email-receipts.md)。

### <a name="order-confirmed"></a>订单已确认

从 Commerce Headquarters 生成销售订单的订单确认文档时，将触发 *订单确认* 通知类型。

### <a name="picking-completed"></a>领料已完成

在 Commerce Headquarters 中将订单的领料单标记为已完成时，将触发 *领料完成* 通知类型。

> [!NOTE]
> 当在 POS 终端将物料标记为已领料时，不会触发领料完成通知类型。

### <a name="packing-completed"></a>装箱已完成

在 POS 终端在 Commerce Headquarters 中为订单生成装箱单文档时，将触发 *装箱完成* 通知类型。

装箱完成通知类型支持以下其他电子邮件占位符，以帮助从交易电子邮件提供“订单可提货”和订单查找功能。

| 占位符名称    | 目的 |
| ------------------- | ------- |
| `pickupstorename`     | 订单可以前往提货的商店的名称。 |
| `pickupstoreaddress`  | 订单可以前往提货的商店的地址。 |
| `pickupstoreopenfrom` | 提货商店的营业时间。 |
| `pickupstoreopento` | 提货商店的关门时间。 |
| `pickupchannelid`     | 提货商店的商店渠道 ID。 |
| `packingslipid`      | 将提货订单的装箱单的 ID。 |
| `confirmationid`      | 将提货订单的订单确认 ID。 （此 ID 有时称为渠道引用 ID。） |

有关客户登记和订单查找功能的详细信息，请参阅[设置地理位置检测和重定向](geo-detection-redirection.md)和[为来宾结帐启用订单查找](order-lookup-guest.md)。

### <a name="order-ready-for-pickup"></a>订单已准备好提货

当订单标记为已装箱，并且交货方式在一个或多个订单行上设置为 **客户提货** 时，将触发 *订单可提货* 通知类型。

> [!NOTE]
> 订单可提货通知类型已弃用，取而代之的是装箱完成通知类型。 此通知类型由交货方式自定义。

### <a name="order-shipped"></a>订单已装运

对具有非商店提货交货方式的订单开票时，将触发 *订单已装运* 通知类型。

> [!NOTE]
> 订单已装运通知类型已弃用，取而代之的是订单已开票通知类型。 此通知类型由交货方式自定义。

### <a name="order-invoiced"></a>订单已开单

在 POS 或 Commerce Headquarters 中为订单开票时，将触发 *订单已开票* 通知类型。

### <a name="issue-gift-card"></a>签发礼品卡

当对包含礼品卡类型的产品的销售订单开票时，将触发 *签发礼品卡* 通知类型。

> [!NOTE]
> 签发礼品卡通知电子邮件将发送给礼品卡接收人。 礼品卡接收人在 Commerce Headquarters 中在 **行详细信息** 下的 **装箱** 选项卡上的各销售订单行上指定。 可以手动或以编程方式指定。

签发礼品卡通知类型支持以下其他占位符。

| 占位符名称      | 目的 |
| --------------------- | ------- |
| `giftcardnumber`        | 礼品卡类型产品的礼品卡编号。 |
| `availablebalance` | 礼品卡上的余额。 |
| `giftcardmessage`       | 礼品卡类型产品的礼品卡消息。 |
| `giftcardpin`         | 礼品卡类型产品的礼品卡个人标识号 (PIN)。 （此占位符特定于外部礼品卡。） |
| `giftcardexpiration`    | 礼品卡类型产品的礼品卡到期日期。 （此占位符特定于外部礼品卡。） |
| `giftcardrecipientname` | 礼品卡类型产品的礼品卡接收人姓名。 |
| `giftcardbuyername`     | 礼品卡类型产品的礼品卡购买者姓名。 |

有关礼品卡的详细信息，请参阅[电子商务数字礼品卡](digital-gift-cards.md)和[对外部礼品卡的支持](dev-itpro/gift-card.md)。

### <a name="order-cancellation"></a>订单取消

在 Commerce Headquarters 中取消订单时，将触发 *订单取消* 通知类型。

### <a name="customer-created"></a>已创建客户

在 Commerce Headquarters 中创建新客户实体时，将触发 *客户创建* 通知类型。

### <a name="b2b-prospect-approved"></a>已审核 B2B 目标客户

在 Commerce Headquarters 中批准目标客户加入请求时，将触发 *B2B 目标客户批准* 通知类型。 有关如何批准或拒绝 B2B 目标客户的详细信息，请参阅[为新业务合作伙伴设置管理员用户](b2b/manage-b2b-users.md#set-up-the-administrator-user-for-a-new-business-partner)。 

B2B 目标客户批准通知类型支持以下其他占位符。

| 占位符名称 | 目的                                                      |
| ---------------- | ------------------------------------------------------------ |
| `firstname`       | 在申请表中输入的 B2B 目标客户的名字。 |
| `lastname`         | 在申请表中输入的 B2B 目标客户的姓氏。 |
| `company`          | 在申请表中输入的申请人公司的名称。 |
| `email`            | 在申请表中输入的目标客户的电子邮件地址。   |
| `zipcode`          | 目标客户的主要地址中的邮政编码。 |
| `comments`         | 目标客户在申请表中输入的注释。 |
| `storename`        | 创建目标客户的渠道的名称。 |
| `storeurl`         | 默认情况下为空。 必须创建自定义扩展才能使用此占位符。 |

### <a name="b2b-prospect-rejected"></a>已拒绝 B2B 目标客户

在 Commerce Headquarters 中拒绝目标客户加入请求时，将触发 *B2B 目标客户拒绝* 通知类型。 有关如何批准或拒绝 B2B 目标客户的详细信息，请参阅[为新业务合作伙伴设置管理员用户](b2b/manage-b2b-users.md#set-up-the-administrator-user-for-a-new-business-partner)。 

B2B 目标客户拒绝通知类型支持以下其他占位符。

| 占位符名称 | 目的                                                      |
| ---------------- | ------------------------------------------------------------ |
| `firstname`        | 在申请表中输入的 B2B 目标客户的名字。 |
| `lastname`         | 在申请表中输入的 B2B 目标客户的姓氏。 |
| `company`          | 在申请表中输入的申请人公司的名称。 |

## <a name="create-an-email-template"></a>创建电子邮件模板

必须先创建模板，才能将特定交易事件映射到电子邮件模板。

若要创建电子邮件模板，请执行以下步骤。

1. 在 Commerce Headquarters 中，转到 **Retail 和 Commerce \> Headquarters 设置 \> 组织电子邮件模板** 或 **组织管理 \> 设置 \> 组织电子邮件模板**。
1. 选择 **新建**。
1. 在 **常规** 下，设置以下字段：

    - **电子邮件 ID** – 电子邮件 ID 是模板的唯一标识符。 当您选择要映射到事件的模板时将显示此值。
    - **电子邮件说明** – 可以使用这个可选字段提供模板的说明。 您输入的值仅在 Commerce Headquarters 中显示。
    - **发件人姓名** – 您输入的姓名在大多数电子邮件客户端的“发件人”字段中显示。
    - **发件人电子邮件** – 输入应该用于使用此模板发送的电子邮件的电子邮件地址。
    - **默认语言代码** – 如果调用此模板的渠道未指定语言，此字段指定默认发送的电子邮件的本地化版本。

1. 在 **电子邮件内容** 下，选择 **新建**。
1. 在 **语言** 字段中，输入电子邮件模板的语言。 以后可以添加更多语言和本地化的模板。
1. 在 **主题** 字段中，输入应该在电子邮件的主题字段中显示的电子邮件主题。
1. 选择 **编辑** 上传您的电子邮件模板。

## <a name="create-an-email-message-body-by-using-html"></a>使用 HTML 创建电子邮件正文

将使用 HTML 撰写电子邮件正文。 可使用 HTML 和内嵌级联样式表 (CSS) 允许的任何布局、样式和品牌。 也可以使用在公开提供的 Web 终结点中托管的图像。 若要添加图像，请在 HTML **&lt;img&gt;** 标记的 **src** 属性中输入图像的 URL。

> [!NOTE]
> 每个电子邮件客户端实施的布局和样式限制可能需要调整用于消息正文的 HTML 和 CSS。 建议您自己熟悉有关最受欢迎电子邮件客户端将支持的 HTML 创建最佳实践。

## <a name="add-placeholders-to-the-email-message-body"></a>在电子邮件正文中添加占位符

您的电子邮件中可以包含生成电子邮件时将替换为客户特定的和交易特定的值的占位符。 占位符两侧始终是百分比符号 (%)，并且将直接插入到 HTML 文档中。

下面是一个示例。

```html
<p>
    Hello %customername%,<br />
    Order number %salesid%, can be picked up from the <b>%pickupstorename%</b> store.
</p>
```

### <a name="order-placeholders-sales-order-level"></a>订单占位符（销售订单级）

以下占位符检索和显示销售订单级（相对销售行级）定义的数据。

| 占位符名称     | 目的                                                      |
| -------------------- | ------------------------------------------------------------ |
| `customername`         | 下订单的客户的姓名。               |
| `customeraddress`      | 客户的地址。                                 |
| `customeremailaddress` | 客户在结帐时输入的电子邮件地址。     |
| `salesid`              | 订单的销售 ID。                                   |
| `orderconfirmationid`  | 在创建订单时生成的跨渠道 ID。   |
| `channelid`            | 下达订单所通过的零售或在线渠道的 ID。 |
| `deliveryname`         | 为交货地址指定的名称。         |
| `deliveryaddress`      | 所装运订单的交货地址。                     |
| `deliverydate`         | 交货日期。                                           |
| `shipdate`             | 装运日期。                                               |
| `modeofdelivery`       | 订单的交货方式。                              |
| `ordernetamount`       | 订单的总金额减去总税金。         |
| `discount`            | 订单的总折扣。                            |
| `charges`              | 订单的总费用。                             |
| `tax`                  | 订单的总税金。                                 |
| `total`                | 订单的总金额。                              |
| `storename`            | 下订单所在商店的名称。            |
| `storeaddress`         | 下订单的商店的地址。              |
| `storeopenfrom`        | 下订单的商店的上班时间。         |
| `storeopento`          | 下订单的商店的下班时间。         |
| `pickupstorename`      | 订单提货所在商店的名称。\*   |
| `pickupstoreaddress`   | 订单提货所在商店的地址。\* |
| `pickupopenstorefrom`  | 订单提货所在商店的上班时间。\* |
| `pickupopenstoreto`    | 订单提货所在商店的下班时间。\* |
| `pickupchannelid`     | 为交货的提货模式指定的商店的渠道 ID。\* |
| `packingslipid`        | 包装订单中的行产品时生成的装箱单的 ID。\* |

\*仅当这些占位符用于 **订单可提货** 通知类型时，这些占位符才会返回数据。 

### <a name="order-line-placeholders-sales-line-level"></a>订单行占位符（销售行级）

以下占位符检索和显示销售订单中单个产品（行）的数据。

| 占位符名称               | 目的 |
|--------------------------------|-------------------|
| `productid`                      | <p>产品的 ID。 变型的此 ID 帐户。</p><p><strong>注意：</strong>已弃用此占位符，使用 `lineproductrecid` 代替。</p> |
| `lineproductrecid`               | 产品的 ID。 变型的此 ID 帐户。 它在变型级别唯一标识物料。 |
| `lineitemid`                     | 产品的产品级别 ID。 （此 ID 不考虑变型。） |
| `lineproductvariantid`           | 产品变型的 ID。 |
| `lineproductname`                | 产品的名称。 |
| `lineproductdescription`         | 产品的描述。 |
| `linequantity`                   | 为行订购的单位数量加度量单位（例如，**ea** 或 **对**）。 |
| `lineunit`                       | 行的度量单位。 |
| `linequantity_withoutunit`       | 为行订购的单位数量，但不含度量单位。 |
| `linequantitypicked`             | 使用 **PickOrder** 事件时，为提货单位数量。 否则为 **0**（零）。 |
| `linequantitypicked_withoutunit` | 使用 **PickOrder** 事件时，为提货单位数量，但不含度量单位。 否则为 **0**（零）。 |
| `linequantitypacked`             | 使用 **PackOrder** 和 **订单可提货** 事件时，为包装单位数量。 否则为 **0**（零）。 |
| `linequantitypacked_withoutuom`  | 使用 **PackOrder** 和 **订单可提货** 事件时，为包装单位数量，但不含度量单位。 否则为 **0**（零）。 |
| `linequantityshipped`            | 始终为 **0**，除了使用特定事件时，如下一行中所述。 |
| `linequantityshipped_withoutuom` | 使用 **ShipOrder** 事件时，为提货单位数量，但不含度量单位。 否则为 **0**（零）。 |
| `lineprice`                      | 一个单位的价格。 |
| `linenetamount`                  | 实施单位数量和折扣后的行价格。 |
| `linediscount`                   | 单个单位的折扣。 |
| `lineshipdate`                   | 行的装运日期。 |
| `linedeliverydate`               | 行的交货日期。 |
| `linedeliverymode`               | 行的交货方式。 |
| `linedeliveryaddress`            | 行的交货地址。 |
| `linepickupdate`                 | 客户为使用交付提货模式的订单指定的提货日期。 |
| `linepickuptimeslot`             | 客户为使用交付提货模式的订单指定的提货时间范围。 |
| `giftcardnumber`                 | 礼品卡类型产品的礼品卡编号。 |
| `giftcardbalance`                | 礼品卡类型产品的礼品卡余额。 |
| `giftcardmessage`                | 礼品卡类型产品的礼品卡消息。 |
| `giftcardpin`                    | 礼品卡类型产品的礼品卡的 PIN。 （此占位符特定于外部礼品卡。） |
| `giftcardexpiration`             | 礼品卡类型产品的礼品卡到期日期。 （此占位符特定于外部礼品卡。） |
| `giftcardrecipientname`          | 礼品卡类型产品的礼品卡接收人姓名。 |
| `giftcardbuyername`              | 礼品卡类型产品的礼品卡购买者姓名。 |

### <a name="format-of-order-line-placeholders-in-the-email-message-body"></a>电子邮件正文中的订单行占位符的格式

为电子邮件正文中的单个订单行创建 HTML 时，在行的重复 HTML 块和占位符两侧加上以下占位符。 请注意，占位符位于 HTML 注释标记内。

```html
<!--%tablebegin.salesline%-->

(Insert the repeating block of HTML and placeholders for individual lines here.)

<!--%tableend.salesline%-->
```

下面是一个示例。

```HTML
<table>
    <tr>
        <td>Product name</td>
        <td>Quantity</td>
        <td>Price</td>
    </tr>
    <!--%tablebegin.salesline%-->
    <tr>
        <td>%lineproductname%</td>
        <td>%linequantity_withoutunit%</td>
        <td>%lineprice%</td>
    </tr>
    <!--%tableend.salesline%-->
</table>
```

## <a name="create-a-template-for-emailed-receipts"></a>为通过电子邮件发送的收据创建模板

可以通过电子邮件将收据发给在销售点 (POS) 进行购买的客户。 通过电子邮件发送的收据模板的创建步骤与其他交易事件的模板的创建步骤相同。 但是需要进行以下更改：

- **%message%** 占位符用于将收据的文本插入到电子邮件中。 若要确保正确显示收据正文，请在 **%message%** 占位符两侧添加 HTML **&lt;pre&gt;** 和 **&lt;/pre&gt;** 标记。
- **%receiptid%** 占位符可用于显示代表收据 ID 的 QR 码或条形码。 （QR 码和条形码是由第三方服务动态生成和提供的。）有关如何在电子邮件收据中显示 QR 码或条形码的更多信息，请参见[在交易和收据电子邮件中添加 QR 码或条形码](add-qr-code-barcode-email.md)。

## <a name="upload-the-email-html"></a>上传电子邮件 HTML

创建和测试邮件正文的 HTML 之后，必须将其上传到 Commerce Headquarters。 现在不能导出电子邮件 HTML。 因此，必须在 Commerce Headquarters 外部维护 HTML 的主副本。

若要上传新的或编辑后的电子邮件模板 HTML，请执行以下步骤。

1. 在 Commerce Headquarters 中，转到 **Retail 和 Commerce \> Headquarters 设置 \> 组织电子邮件模板**。
1. 选择要为其添加或替换 HTML 的语言的行。 也可以选择 **新建** 为新语言创建行。
1. 选择 **编辑**。
1. 在显示的对话框中，选择 **浏览**。 浏览到要上传的 HTML 文档，选中，然后选择 **打开**。
1. 选择 **上载**。
1. 预览窗口中显示您的电子邮件 HTML 之后，请选择 **确定**。
1. 确保为行选中 **有正文** 复选框。

如果已经配置了 Commerce Headquarters 以发送电子邮件，将把您的新的或更新后的电子邮件发送给执行的交易将调用映射到模板的事件的所有客户。

有关如何在 Dynamics 365 Commerce 中配置电子邮件的详细信息，请参阅[配置和发送电子邮件](../fin-ops-core/fin-ops/organization-administration/configure-email.md)。

## <a name="additional-resources"></a>其他资源 

[设置电子邮件通知配置文件](email-notification-profiles.md)

[配置和发送电子邮件](../fin-ops-core/fin-ops/organization-administration/configure-email.md)

[设置电子邮件收据](/dynamicsax-2012/appuser-itpro/set-up-email-receipts)

[从 Modern POS 发送电子邮件收据](email-receipts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

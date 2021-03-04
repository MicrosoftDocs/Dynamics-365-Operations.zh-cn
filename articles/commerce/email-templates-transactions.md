---
title: 为交易事件创建电子邮件模板
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中为交易事件创建，上传和配置电子邮件模板。
author: bicyclingfool
manager: annbe
ms.date: 06/01/2020
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
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: ea484bfc1e9b293c53d7293c50630c4955000131
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410398"
---
# <a name="create-email-templates-for-transactional-events"></a>为交易事件创建电子邮件模板

[!include [banner](includes/banner.md)]

此主题介绍如何在 Microsoft Dynamics 365 Commerce 中为交易事件创建，上传和配置电子邮件模板。

## <a name="overview"></a>概览

Dynamics 365 Commerce 提供用于发送电子邮件的现成解决方案以向客户警示交易事件（例如，下达订单时，订单准备好领料时，或已经为订单发货了时）。 此主题介绍创建，上传和配置用于发送交易电子邮件的电子邮件模板的步骤。

## <a name="create-an-email-template"></a>创建电子邮件模板

必须先创建模板，才能将特定交易事件映射到电子邮件模板。

若要创建电子邮件模板，请执行以下步骤。

1. 在 Commerce Headquarters 中，转到 **组织电子邮件模板**，它在 **Retail 和 Commerce \> 总部设置 \> 组织电子邮件模板** 或 **组织管理 \> 设置 \> 组织电子邮件模板** 下。
1. 选择 **新建**。
1. 在 **常规** 下，设置以下字段：

    - **电子邮件 ID** – 电子邮件 ID 是模板的唯一标识，这是选择要映射到事件的模板时显示的值。
    - **电子邮件说明** – 可以使用这个可选字段提供模板的说明。 您输入的值仅在 Commerce Headquarters 中显示。
    - **发件人姓名** – 您输入的姓名在大多数电子邮件客户端的“发件人”字段中显示。
    - **发件人电子邮件** – 输入应该用于使用此模板发送的电子邮件的电子邮件地址。
    - **默认语言代码** – 如果调用此模板的渠道未提供语言，此字段指定默认发送的电子邮件的本地化版本。

1. 在 **电子邮件内容** 下，选择 **新建**。
1. 在 **语言** 字段中，输入电子邮件模板的语言。 以后可以添加更多语言和本地化的模板。
1. 在 **主题** 字段中，输入应该在电子邮件的主题字段中显示的电子邮件主题。
1. 选择 **编辑** 上传您的电子邮件模板。

## <a name="create-an-email-message-body-by-using-html"></a>使用 HTML 创建电子邮件正文

将使用 HTML 撰写电子邮件正文。 可使用 HTML 和内嵌级联样式表 (CSS) 允许的任何布局、样式和品牌。 也可以使用在公开提供的 Web 终结点中托管的图像。 若要添加图像，请在 HTML **&lt;img&gt;** 标记的 **src** 属性中输入图像的 URL。

> [!NOTE]
> 每个电子邮件客户端实施的布局和样式限制可能需要调整用于消息正文的 HTML 和 CSS。 建议您自己熟悉有关最受欢迎电子邮件客户端支持的 HTML 的最佳实践。

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

| 占位符名称    | 占位符值                                                |
|---------------------|------------------------------------------------------------------|
| customername        | 下订单的客户的姓名。                   |
| salesid             | 订单的销售 ID。                                       |
| deliveryaddress     | 所装运订单的交货地址。                         |
| customeraddress     | 客户的地址。                                     |
| deliverydate        | 交货日期。                                               |
| shipdate            | 装运日期。                                                   |
| modeofdelivery      | 订单的交货方式。                                  |
| 费用             | 订单的总费用。                                 |
| 税                 | 订单的总税金。                                     |
| 合计               | 订单的总金额。                                  |
| ordernetamount      | 订单的总金额减去总税金。             |
| discount / 折扣            | 订单的总折扣。                                |
| storename           | 下订单所在商店的名称。                |
| storeaddress        | 下订单的商店的地址。                  |
| storeopenfrom       | 下订单的商店的上班时间。             |
| storeopento         | 下订单的商店的下班时间。             |
| pickupstorename     | 订单提货所在商店的名称。         |
| pickupstoreaddress  | 订单提货所在商店的地址。      |
| pickupopenstorefrom | 订单提货所在商店的上班时间。 |
| pickupopenstoreto   | 订单提货所在商店的下班时间。 |

### <a name="order-line-placeholders-sales-line-level"></a>订单行占位符（销售行级）

以下占位符检索和显示销售订单中单个产品（行）的数据。

| 占位符名称               | 占位符值 |
|--------------------------------|-------------------|
| productid                      | 行的产品 ID。 |
| lineproductname                | 产品的名称。 |
| lineproductdescription         | 产品的描述。 |
| linequantity                   | 为行订购的单位数量加度量单位（例如，**ea** 或 **对**）。 |
| lineunit                       | 行的度量单位。 |
| linequantity_withoutunit       | 为行订购的单位数量，但不含度量单位。 |
| linequantitypicked             | 使用 **PickOrder** 事件时，为提货单位数量。 否则为 **0**（零）。 |
| linequantitypicked_withoutunit | 使用 **PickOrder** 事件时，为提货单位数量，但不含度量单位。 否则为 **0**（零）。 |
| linequantitypacked             | 使用 **PackOrder** 和 **订单可提货** 事件时，为包装单位数量。 否则为 **0**（零）。 |
| linequantitypacked_withoutuom  | 使用 **PackOrder** 和 **订单可提货** 事件时，为包装单位数量，但不含度量单位。 否则为 **0**（零）。 |
| linequantityshipped            | 始终为 **0**，除了使用特定事件时，如下一行中所述。 |
| linequantityshipped_withoutuom | 使用 **ShipOrder** 事件时，为提货单位数量，但不含度量单位。 否则为 **0**（零）。 |
| lineprice                      | 一个单位的价格。 |
| linenetamount                  | 实施单位数量和折扣后的行价格。 |
| linediscount                   | 单个单位的折扣。 |
| lineshipdate                   | 行的装运日期。 |
| linedeliverydate               | 行的交货日期。 |
| linedeliverymode               | 行的交货方式。 |
| linedeliveryaddress            | 行的交货地址。 |
| giftcardnumber                 | 礼品卡类型产品的礼品卡编号。 |
| giftcardbalance                | 礼品卡类型产品的礼品卡余额。 |
| giftcardmessage                | 礼品卡类型产品的礼品卡消息。 |
| giftcardpin                    | 礼品卡类型产品的礼品卡个人标识号 (PIN)。 （此占位符特定于外部礼品卡。） |
| giftcardexpiration             | 礼品卡类型产品的礼品卡到期日期。 （此占位符特定于外部礼品卡。） |
| giftcardrecipientname          | 礼品卡类型产品的礼品卡接收人姓名。 |
| giftcardbuyername              | 礼品卡类型产品的礼品卡购买者姓名。 |

### <a name="format-of-order-line-placeholders-in-the-email-message-body"></a>电子邮件正文中的订单行占位符的格式

为电子邮件正文中的单个订单行创建 HTML 时，在行的重复 HTML 块和占位符两侧加上放到 HTML 注释标记内的以下占位符。

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

- 电子邮件模板的电子邮件 ID 必须为 **emailRecpt**。
- 使用 **%message%** 占位符将收据的文本插入到电子邮件中。 若要确保正确显示收据正文，请在 **%message%** 占位符两侧添加 HTML **&lt;pre&gt;** 和 **&lt;/pre&gt;** 标记。
- 将电子邮件页眉和页脚 HTML 中的换行符转换为 HTML **&lt;br /&gt;** 标记，以便正确显示收据正文。 若要杜绝收据电子邮件中不需要的垂直空格，请删除 HTML 中不需要垂直空格的任何位置的换行符。

有关如何配置电子邮件收据的详细信息，请参阅[设置电子邮件收据](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-email-receipts)。

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

[设置电子邮件收据](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-email-receipts)

[从 Modern POS 发送电子邮件收据](email-receipts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Commerce 定价 API
description: 本文介绍 Microsoft Dynamics 365 Commerce 定价引擎提供的各种定价 API。
author: boycez
ms.date: 08/10/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2022-07-15
ms.openlocfilehash: d694c44f6987fbf2a360869d2fb2a2fbaf0d2e4d
ms.sourcegitcommit: 924dbcdc6b03f6a7ae3a07378ec405fd15c7e359
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/13/2022
ms.locfileid: "9294105"
---
# <a name="commerce-pricing-apis"></a>Commerce 定价 API

[!include [banner](../includes/banner.md)]

本文介绍 Microsoft Dynamics 365 Commerce 定价引擎提供的各种定价 API。

Dynamics 365 Commerce 定价引擎提供以下 Retail Server API，外部应用程序可以使用这些 API 来支持各种定价方案：

- **GetActivePrices** - 此 API 获取产品的计算价格，包括简单折扣。
- **CalculateSalesDocument** - 此 API 会计算给定数量的产品的价格和折扣（如果产品是一起购买的）。
- **GetAvailablePromotions** - 此 API 获取购物车中产品的适用折扣。 
- **AddCoupons** - 此 API 将优惠券添加到购物车。
- **RemoveCoupons** - 此 API 从购物车中删除优惠券。

有关如何在外部应用程序中使用 Retail Server API 的详细信息，请参阅 [在外部应用程序中使用 Retail Server API](dev-itpro/consume-retail-server-api.md)。

## <a name="getactiveprices"></a>GetActivePrices

Commerce 版本 10.0.4 中引入了 *GetActivePrices* API。 此 API 获取产品的计算价格，包括简单折扣。 它不计算多行折扣，并且它假定 API 请求中的每个产品的数量为 1。 此 API 还可以将产品列表作为输入并批量查询单个产品的价格。

*GetActivePrices* API 支持 **员工**、**客户**、**匿名** 和 **应用程序** Commerce 角色。

*GetActivePrices* API 的主要用例是产品详细信息页面 (PDP)，零售商希望在其中展示产品的最佳价格，包括任何有效的折扣。

下表显示了 *GetActivePrices* API 的输入参数。

| Name                                    | 子名称 | 类型 | 必填/可选 | Description |
|-----------------------------------------|----------|------|-------------------|-------------|
| projectDomain                           | | ProjectionDomain | 必填 | |
|                                         | ChannelId | 长型 | 必填 | |
|                                         | CatalogId | 长型 | 必填 | |
| productIds                              | | IEnumerable\<long\> | 必填 | 要计算其价格的产品的列表。 |
| activeDate                              | | DateTimeOffset | 必填 | 计算价格的日期。 |
| customerId                              | | 字符串 | 可选 | 客户帐号。 |
| affiliationLoyaltyTiers                 | | IEnumerable\<AffiliationLoyaltyTier\> | 可选 | 隶属关系和会员层。 |
|                                         | AffiliationId | 长型 | 必填 | 隶属关系 ID。 |
|                                         | LoyaltyTierId | 长型 | 可选 | 会员层 ID。 |
| includeSimpleDiscountsInContextualPrice | | 布尔型 | 可选 | 将此参数设置为 **true** 以在定价计算中包括简单折扣。 默认值为 **false**。 |
| includeVariantPriceRange                | | 布尔型 | 可选 | 将此参数设置为 **true** 以在主产品的所有变型中获取最低和最高价格。 默认值为 **false**。 |
| includeAttainablePricesAndDiscounts     | | 布尔型 | 可选 | 将此参数设置为 **true** 以获取可实现的价格和折扣。 默认值为 **false**。 |

**示例请求正文**

```json
{
    "projectDomain": 
    {
        "ChannelId": 5637144592,
        "CatalogId": 0
    },
    "productIds": 
    [
        68719489871
    ],
    "activeDate": "2022-06-20T14:40:05.873+08:00",
    "includeSimpleDiscountsInContextualPrice": true,
    "includeVariantPriceRange": false
}
```

**示例响应正文**

```json
{
    "value": 
    [
        {
            "ProductId": 68719489871,
            "ListingId": 68719489871,
            "BasePrice": 0,
            "TradeAgreementPrice": 0,
            "AdjustedPrice": 0,
            "MaxVariantPrice": 0,
            "MinVariantPrice": 0,
            "CustomerContextualPrice": 0,
            "DiscountAmount": 0,
            "CurrencyCode": "USD",
            "ItemId": "82000",
            "InventoryDimensionId": null,
            "UnitOfMeasure": "ea",
            "ValidFrom": "2022-06-20T01:40:05.873-05:00",
            "ProductLookupId": 0,
            "ChannelId": 5637144592,
            "CatalogId": 0,
            "SalesAgreementPrice": 0,
            "PriceSourceTypeValue": 1,
            "DiscountLines": [],
            "AttainablePriceLines": [],
        }
    ]
}
```

## <a name="calculatesalesdocument"></a>CalculateSalesDocument

Commerce 版本 10.0.25 中引入了 *CalculateSalesDocument* API。 此 API 会计算给定数量的产品的价格和折扣（如果产品是在订单中一起购买的）。 *CalculateSalesDocument* API 后面的定价计算会同时考虑单行折扣和多行折扣。

*CalculateSalesDocument* API 的主要用例是在完整购物车上下文（如销售报价）未持续存在的情况下进行定价计算。 销售点 (POS) 和 Commerce 电子商务中的方案也可以从此用例中受益。 将购物车物料作为集计算时的总价较低（例如，对于离散的捆绑销售、链接或推荐的产品或已添加到购物车的产品），可能会诱使客户将产品添加到购物车中。

*CalculateSalesDocument* API 的请求和响应的数据模型为 **购物车**。 但是，在此 API 的上下文中，数据模型名为 **SalesDocument**。 由于大多数属性是可选属性，并且只有其中少数属性影响定价计算，因此下表中仅显示与定价相关的字段。 我们不建议 API 请求中涉及任何其他字段。

*CalculateSalesDocument* API 的作用仅为计算价格和折扣。 不涉及税金和费用。

下表显示了名为 **salesDocument** 的对象内的输入参数。

| Name             | 子名称 | 类型 | 必填/可选 | Description |
|------------------|----------|------|-------------------|-------------|
| ID               | | 字符串 | 必填 | 销售单据的标识符。 |
| CartLines        | | IList\<CartLine\> | 可选 | 要计算其价格和折扣的行的列表。 |
|                  | 产品 ID | 长型 | CartLine 的范围中需要 | 产品记录 ID。 |
|                  | ItemId | 字符串 | 可选 | 物料标识符。 如果提供了值，则它必须与 **ProductId** 参数的值匹配。 |
|                  | InventoryDimensionId | 字符串 | 可选 | 库存维度标识符。 如果提供了值，则 **ItemId** 和 **InventoryDimensionId** 值的组合必须与 **ProductId** 参数的值匹配。 |
|                  | Quantity | 十进制 | CartLine 的范围中需要 | 产品数量。 |
|                  | UnitOfMeasureSymbol | 字符串 | 可选 | 产品的单位。 默认情况下，如果未提供值，则 API 使用产品的销售单位。 |
| CustomerId       | | 字符串 | 可选 | 客户帐号。 |
| LoyaltyCardId    | | 字符串 | 可选 | 会员卡标识符。 与会员卡关联的任何客户帐户都必须与 **CustomerId** 参数的值匹配（如果已提供）。 如果找不到会员卡或其状态为 **已冻结**，则将不会考虑该会员卡。 |
| AffiliationLines | | IList\<AffiliationLoyaltyTier\> | 可选 | 隶属关系会员层行。 如果提供了 **CustomerId** 和/或 **LoyaltyCardId** 值，则相应的隶属关系会员层行将与 **AffiliationLines** 值中提供的行合并。 |
|                  | AffiliationId | 长型 | AffiliationLoyaltyTier 的范围中需要 | 隶属关系记录 ID。 |
|                  | LoyaltyTierId | 长型 | AffiliationLoyaltyTier 的范围中需要 | 会员层记录 ID。 |
|                  | AffiliationTypeValue | 整数 | AffiliationLoyaltyTier 的范围中需要 | 一个指示隶属关系行是 **常规** 类型 (**0**) 还是 **会员** 类型 (**1**) 的值。 如果此参数设置为 **0**，则 API 将 **AffiliationId** 值作为标识符，并忽略 **LoyaltyTierId** 值。 如果此参数设置为 **1**，则 API 将 **LoyaltyTierId** 值作为标识符，并忽略 **AffiliationId** 值。 |
|                  | ReasonCodeLines | 系列\<ReasonCodeLine\> | AffiliationLoyaltyTier 的范围中需要 | 原因代码行。 此参数对定价计算没有影响，但作为 **AffiliationLoyaltyTier** 对象的一部分是必需的。 |
|                  | CustomerId | 字符串 | AffiliationLoyaltyTier 的范围中需要 | 客户帐号。 |
| 优惠券          | | IList\<Coupon\> | 可选 | 定价计算中将不考虑不适用（停用、已过期或找不到）的优惠券。 |
|                  | 代码 | 字符串 | 优惠券的范围中需要 | 优惠券代码。 |
|                  | CodeId | 字符串 | 可选 | 优惠券代码标识符。 如果提供了值，则它必须与 **Code** 参数的值匹配。 |
|                  | DiscountOfferId | 字符串 | 可选 | 折扣标识符。 如果提供了值，则它必须与 **Code** 参数的值匹配。 |

**示例请求正文**

```json
{
    "salesDocument": 
    {
        "Id": "CalculateSalesDocument",
        "CartLines": 
        [
            {
                "ProductId": 68719491408,
                "ItemId": "91003",
                "InventoryDimensionId": "",
                "Quantity": 1,
                "UnitOfMeasureSymbol": "ea"
            },
            {
                "ProductId": 68719493014,
                "Quantity": 2,
                "UnitOfMeasureSymbol": "ea"
            }
        ],
        "CustomerId": "3003",
        "AffiliationLines": 
        [
            {
                "AffiliationId": 68719476742,
                "LoyaltyTierId": 0,
                "AffiliationTypeValue": 0,
                "ReasonCodeLines": [],
                "CustomerId": null
            }
        ],
        "LoyaltyCardId": "55103",
        "Coupons": 
        [
            {
                "CodeId": "CODE-0005",
                "Code": "CPN0004",
                "DiscountOfferId": "ST100077"
            }
        ]
    }
}
```

整个购物车对象作为响应正文返回。 若要检查价格和折扣，您应专注于下表中的字段。

| Name           | 子名称 | 类型 | Description |
|----------------|----------|------|--------------|
| NetPrice       | | 十进制 | 应用折扣前整个销售单据的净价。 |
| DiscountAmount | | 十进制 | 整个销售单据的总折扣金额。 |
| TotalAmount    | | 十进制 | 整个销售单据的总金额。 |
| CartLines      | | IList\<CartLine\> | 包括价格和折扣详细信息的计算行。 |
|                | 价格 | 十进制 | 产品的单价。 |
|                | NetPrice | 十进制 | 应用折扣前行的净价（= *价格* &times; *数量*）。 |
|                | DiscountAmount | 十进制 | 折扣金额。 |
|                | TotalAmount | 十进制 | 行的最终总定价结果。 |
|                | PriceLines | IList\<PriceLine\> | 价格详细信息，包括价格来源（基础价格、价格调整或贸易协议）和金额。 |
|                | DiscountLines | IList\<DiscountLine\> | 折扣明细。 |

## <a name="getavailablepromotions"></a>GetAvailablePromotions 

假定购物车具有多个购物车行，那么 *GetAvailablePromotions* API 会返回购物车行的所有适用折扣。 

*GetAvailablePromotions* API 的主要用例是购物车页面，零售商希望在其中展示当前购物车的已应用折扣或可用优惠券。

下表显示了 *GetAvailablePromotions* API 的输入参数。

| Name        | 类型 | 必填/可选 | Description |
|-------------|------|-------------------|-------------|
| 键         | 字符串 | 必填 | 购物车 ID。 |
| cartLineIds | IEnumerable\<string\> | 可选 | 将此参数设置为仅返回所选购物车行的折扣。 |

**示例响应正文**

```json
{
    "value": 
    [
        {
            "LineId": "f495ffa507bc4f63a47a409cd8713dd7",
            "Promotion": {
                "OfferId": "ST100012",
                "OfferName": "Loyalty 5% off over $100",
                "PeriodicDiscountTypeValue": 4,
                "IsDiscountCodeRequired": false,
                "ValidationPeriodId": null,
                "AdditionalRestrictions": null,
                "Description": "All loyalty members get 5% with transaction total above $10 unless some exclusive or best price discounts are already applied on the transaction",
                "ValidFromDate": "2022-06-20T06:52:56.2460219Z",
                "ValidToDate": "2022-06-20T06:52:56.2460224Z",
                "CouponCodes": [],
                "ValidationPeriod": null
            }
        }
    ]
}
```

## <a name="addcoupons"></a>AddCoupons

*AddCoupons* API 支持将优惠券列表添加到购物车。 在添加优惠券后，它将返回购物车对象。

下表显示了 *AddCoupons* API 的输入参数。

| Name                 | 类型 | 必填/可选 | Description |
|----------------------|------|-------------------|-------------|
| 键                  | 字符串 | 必填 | 购物车 ID。 |
| couponCodes          | IEnumerable\<string\> | 必填 | 要添加到购物车的优惠券代码。 |
| isLegacyDiscountCode | 布尔型 | 可选 | 将此参数设置为 **true** 以指示优惠券是旧折扣代码。 默认值为 **false**。 |

## <a name="removecoupons"></a>RemoveCoupons

*RemoveCoupons* API 支持从购物车中删除优惠券列表。 在删除优惠券后，它将返回购物车对象。

下表显示了 *RemoveCoupons* API 的输入参数。

| Name        | 类型 | 必填/可选 | Description |
|-------------|------|-------------------|-------------|
| 键         | 字符串 | 必填 | 购物车 ID。 |
| couponCodes | IEnumerable\<string\> | 必填 | 要从购物车中删除的优惠券代码。 |

[!INCLUDE[footer-include](../includes/footer-banner.md)]

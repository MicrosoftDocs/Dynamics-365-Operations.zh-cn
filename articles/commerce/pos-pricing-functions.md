---
title: POS 中的定价功能
description: 本文介绍 Microsoft Dynamics 365 Commerce 销售点 (POS) 应用程序中的各种价格和折扣功能。
author: boycez
ms.date: 08/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2022-07-14
ms.openlocfilehash: 210798ac192ee251594ec8ff9d23dab31ec2043e
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473679"
---
# <a name="pricing-functions-in-pos"></a>POS 中的定价功能

[!include [banner](includes/banner.md)]

本文介绍 Microsoft Dynamics 365 Commerce 销售点 (POS) 应用程序中的各种价格和折扣功能。

Dynamics 365 Commerce POS 应用程序提供了丰富的功能，使一线工作人员能够执行 Store Commerce 操作。 下表显示应用程序中当前可用的价格和折扣功能。

| 函数                       | POS 操作 |
|--------------------------------|----------------|
| 查看价格                    | [价格查询](#price-check) |
| 查看折扣                 | [查看所有折扣](#view-all-discounts)<br>[查看可用折扣](#view-available-discounts) |
| 自定义价格                | [价格覆盖](#price-override) |
| 应用或删除折扣      | [单行折扣金额](#line-discount-amount)<br>[单行折扣百分比](#line-discount-percent)<br>[总折扣金额](#total-discount-amount)<br>[总折扣百分比](#total-discount-percent)<br>[从交易记录中删除系统折扣](#remove-system-discounts-from-transaction)<br>[重新应用系统折扣](#reapply-system-discounts) |
| 应用或删除优惠券        | [添加优惠券代码](#add-coupon-code)<br>[删除优惠券代码](#remove-coupon-code) |
| 计算价格和折扣 | [重新计算](#recalculate) |

有关如何在 POS 应用程序中配置先前操作以及它们是否支持脱机模式的信息，请参阅[联机和脱机销售点 (POS) 操作](pos-operations.md)。

## <a name="price-check"></a>价格查询

通过 **价格检查** 操作，POS 用户可以查找特定产品的预配置价格。

## <a name="view-all-discounts"></a>查看所有折扣

通过 **查看所有折扣** 操作，POS 用户能够查找当前在商店渠道中运行的所有有效促销。 具体来说，此操作列出了与以下任何条件匹配的所有折扣：

- 折扣的价格组与商店的价格组匹配。
- 折扣的价格组映射到隶属或会员计划。
- 折扣的价格组映射到与商店关联的目录。

**查看所有折扣** 操作仅显示不与已应用的任何折扣竞争的折扣。 此行为有助于确保在销售助理向客户介绍折扣，并且客户执行了所需操作（例如，客户多购买一件商品以享受 10% 的折扣）时，将该折扣应用于交易。 仅在启用了 **应用但不使用优惠券代码** 参数时，才会显示基于优惠券的折扣。

在 **查看所有折扣** 操作中，POS 用户可以按名称和说明搜索折扣，并且他们可以根据是否需要优惠券来筛选折扣。

## <a name="view-available-discounts"></a>查看可用折扣

利用 **查看可用折扣** 操作，POS 用户能够查看适用于交易记录中的所选行或适用于整个交易记录的所有折扣。 适用于所选行的折扣包括已应用的折扣和尚未应用但可应用的折扣（例如，组合和匹配需要其他项的折扣）。 如果适用的折扣链接到了已启用 **申请不含优惠券代码** 参数的优惠券，则 POS 用户还可以使用此操作内的 **应用优惠券** 功能直接兑换优惠券，而无需输入或扫描任何优惠券代码或优惠券条形码。

## <a name="price-override"></a>价格覆盖

通过 **价格覆盖** 操作，POS 用户可以覆盖交易记录中的产品销售价。 此操作仅适用于配置为允许价格覆盖的产品。

## <a name="line-discount-amount"></a>单行折扣金额

**行折扣金额** 操作使 POS 用户能够为交易记录中的行项输入折扣金额。 此操作仅适用于可折扣项，并且它遵循在 POS 权限组中为用户指定的 **最大行折扣金额** 值。

## <a name="line-discount-percent"></a>单行折扣百分比

**行折扣百分比** 操作使 POS 用户能够为交易记录中的行项输入折扣百分比。 此操作仅适用于可折扣项，并且它遵循在 POS 权限组中为用户指定的 **最大行折扣百分比** 值。

## <a name="total-discount-amount"></a>总折扣金额

**总折扣金额** 操作使 POS 用户能够输入交易记录的折扣金额。 此操作仅适用于可折扣项，并且它遵循在 POS 权限组中为用户指定的 **最大总折扣金额** 值。 如果输入的折扣金额超过最大总折扣金额，则将阻止操作，并且不会触发权限覆盖流。 目前，总折扣金额无法应用于包含销售物料和退货物料组合的购物车。

## <a name="total-discount-percent"></a>总折扣百分比

**总折扣百分比** 操作使 POS 用户能够输入交易记录的折扣百分比。 此操作仅适用于可折扣项，并且它遵循在 POS 权限组中为用户指定的 **最大总折扣率** 值。 如果输入的折扣百分比超过最大总折扣百分比，则将阻止操作，并且不会触发权限覆盖流。 目前，总折扣百分比无法应用于包含销售物料和退货物料组合的购物车。

## <a name="remove-system-discounts-from-transaction"></a>从交易记录中删除系统折扣

通过 **从交易记录中删除系统折扣** 操作，POS 用户可以清除交易记录中所有应用的系统折扣（包括基于优惠券的折扣）。 执行此操作后，定价引擎开始从折扣计算范围中排除系统折扣。 **从交易记录中删除系统折扣** 操作不会删除手动折扣。

## <a name="reapply-system-discounts"></a>重新应用系统折扣

如果使用 **从交易记录中删除系统折扣** 操作删除了折扣，则 **重新应用系统折扣** 操作使 POS 用户能够将系统计算的折扣重新应用于交易记录。 执行此操作后，定价引擎开始在折扣计算范围中包括所有系统折扣。

## <a name="add-coupon-code"></a>添加优惠券代码

利用 **添加优惠券代码** 操作，POS 用户可以通过输入优惠券代码向交易添加优惠券。 或者，POS 用户可以扫描优惠券条形码或使用 **交易** 屏幕上的数字键盘输入此条形码。

## <a name="remove-coupon-code"></a>删除优惠券代码

利用 **删除优惠券代码** 操作，POS 用户能够选择和删除当前应用于交易的一个或多个优惠券。

## <a name="recalculate"></a>重新计算

利用 **重新计算** 操作，POS 用户能够触发按需定价计算。 如果启用了价格锁定和/或延迟价格计算，并且 POS 用户希望在购物车或订单更改后重新计算价格和折扣，需要执行此操作。 **重新计算** 操作始终重新计算整个订单。 它不能用于重新计算所选销售行。 若要将手动折扣应用于 POS 中的锁定销售行，POS 用户必须首先使用 **重新计算** 操作来解锁所有销售行。

[!INCLUDE[footer-include](../includes/footer-banner.md)]

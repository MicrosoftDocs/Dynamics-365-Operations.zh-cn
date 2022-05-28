---
title: 设置装运承运人
description: 此主题显示如何设置装运承运人和定义详细信息，诸如服务、装运方式、运输招标、运输约束和装运费用。
author: Weijiesa
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSShippingCarrierCustomerAccount,TMSCarrier
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 876a3ffd94f554ef042da995311df0f8009eee12
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672645"
---
# <a name="set-up-shipping-carriers"></a>设置装运承运人

[!include [banner](../../includes/banner.md)]

此主题显示如何设置装运承运人和定义详细信息，诸如服务、装运方式、运输招标、运输约束和装运费用。 运输协调员可将装运承运人分配给某个入站或出站装载。

## <a name="create-a-new-shipping-carrier"></a>创建新装运承运人

1. 转到 **导航窗格 > 模块 > 运输管理 > 设置 > 承运人 > 装运承运人**。
2. 在操作窗格上选择 **新建**。
3. 在 **装运承运人** 字段中，键入一个值。
4. 在 **名称** 字段中，键入一个值。
5. 在 **模式** 字段中，从下拉菜单中选择一个选项。

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a>填写装运承运人的一般信息

1. 切换 **概览** 部分的展开项。
2. 勾选或不勾选 **启用承运装运人** 复选框。
3. 在 **供应商帐户** 字段中，从下拉菜单中选择一个选项。 选择向其分配装运承运人的供应商帐户。  
4. 在 **运输招标类型** 字段中，选择一个选项。 选择 **手动** 以使用“运输招标”页面，或选择 **EDI** 来通过使用电子数据交换 (EDI) 更新招标信息。  
5. 勾选或不勾选 **启用承运评级** 复选框。

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a>创建装运承运人的必需服务

1. 切换 **服务** 部分的展开项。
2. 选择 **新建**。
3. 在 **承运人服务** 字段中，键入一个值。
4. 在 **名称** 字段中，键入一个值。
5. 在 **负荷模板 ID** 字段中，选择要与服务关联的负荷模板。 负荷模板定义整个装载量的重量和体积的最大度量值。 例如，装载量模板可能表示卡车或集装箱的大小。 负荷模板 ID 也在负荷构建模板中以及在使用[负荷构建工作台](load-building-workbench.md)时指定，这可以帮助您应用负荷构建策略来创建负荷。 因此，系统将能够通过比较指定的负荷模板 ID，将每个新负荷与合适的装运承运人服务匹配。
6. 在 **运输方法** 字段中，从下拉菜单中选择一个选项。

## <a name="set-up-the-address-for-the-carrier-optional"></a>设置承运人的地址（可选）

1. 切换 **地址** 部分的扩展项。
2. 选择 **新建**。
3. 在 **名称或描述** 字段中，键入一个值。
4. 在 **国家/地区** 字段中，从下拉菜单中选择一个选项。
5. 在 **邮政编码** 字段中，从下拉菜单中选择一个选项。
6. 在 **街道** 字段中，键入一个值。
7. 选择 **确定**。

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a>设置装运承运人的评级资料。

1. 切换 **评级资料** 部分的展开项。
2. 选择 **新建**。
3. 在 **评级资料** 字段中，键入一个值。
4. 在 **名称** 字段中，键入一个值。
5. 在 **站点** 字段中，从下拉菜单中选择一个选项。
6. 在 **仓库** 字段中，从下拉菜单中选择一个选项。
7. 在 **费率引擎** 字段中，从下拉菜单中选择一个选项。 选择根据合同，您与承运人订立的费率引擎。  
8. 在 **费率主数据** 字段中，从下拉菜单中选择一个选项。
9. 在 **运输时间引擎** 字段中，从下拉菜单中选择一个选项。
10. 选择 **保存**。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
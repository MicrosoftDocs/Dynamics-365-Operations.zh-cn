---
title: 设置装运承运人
description: 此主题显示如何设置装运承运人和定义详细信息，诸如服务、装运方式、运输招标、运输约束和装运费用。
author: ShylaThompson
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSShippingCarrierCustomerAccount,TMSCarrier
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c292470e6c70af4dfe11bbe324ebcf93438e29d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840453"
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
5. 在 **运输方法** 字段中，从下拉菜单中选择一个选项。

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
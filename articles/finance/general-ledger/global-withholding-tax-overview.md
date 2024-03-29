---
title: 全球预缴税金
description: 本文提供有关全球预缴税金功能及其设置方法的信息。 全球预缴税金功能针对供应商和客户交易进行了增强，让预缴税金在物料级别计算。
author: kailiang
ms.date: 01/12/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: kfend
ms.custom:
- "15721"
- intro-internal
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 49d5048b9df30e94d959cf9f22b8ae837b74abdd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846819"
---
# <a name="global-withholding-tax"></a>全球预缴税金

[!include [banner](../includes/banner.md)]

本文提供有关全球预缴税金功能，并说明了设置方法。 版本 10.0.17 及更高版本中提供此新功能。

全球预缴税金功能针对供应商和客户交易进行了增强，让预缴税金在物料级别计算。 购买交易中预缴税金帐户中的余额可以通过对预缴税金结算帐户运行预缴税金支付作业来结算。

> [!NOTE]
> 全球预缴税金在采购订单、供应商发票和销售订单页上不支持 **维护费用** 功能。

## <a name="turn-on-global-withholding-tax"></a>打开全球预缴税金

1. 在 **功能管理** 工作区，选择 **全球预缴税金**，然后选择 **立即启用**。
2. 转到 **税 \> 设置 \> 参数 \> 总帐参数**，然后在 **预缴税金** 选项卡上，将 **启用全球预缴税金** 选项设置为 **是**。
3. 选择 **保存**。
4. 在 Web 浏览器中刷新页面。

> [!NOTE]
> 对于已经存在本地化的预缴税金解决方案的国家/地区，无法启用全球预缴税金功能。 这些区域包括但不限于印度、巴西、泰国、沙特阿拉伯、爱尔兰、英国和美国。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

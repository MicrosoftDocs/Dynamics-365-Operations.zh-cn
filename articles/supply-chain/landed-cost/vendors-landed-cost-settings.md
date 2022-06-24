---
title: 为登陆成本添加了供应商设置
description: 本文介绍在启用登陆成本模块时添加到现有“供应商”页的新字段。 您将使用这些字段设置要与登陆成本功能一起使用的供应商。
author: Weijiesa
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 84d1dee0815b036a3d411eabff49d8a08249bed3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882567"
---
# <a name="vendor-settings-added-for-landed-cost"></a>为登陆成本添加了供应商设置

[!include [banner](../../includes/banner.md)]

启用 **登陆成本** 模块时，几个新字段将添加到现有的 **供应商** 页。 您将使用这些字段设置要与登陆成本功能一起使用的供应商。

要设置相关字段，转到 **采购 \> 供应商 \> 所有供应商**。 打开现有供应商，或创建一个新供应商，然后选择 **杂项详细信息** 快速选项卡。 **登陆成本** 模块添加的所有新字段都将显示在 **航行** 标题下。 下表介绍这些字段。

| 字段 | 说明 |
|---|---|
| 装运类型 | <p>选择与登陆成本相关的供应商角色：</p><ul><li>**无** – 供应商没有与登陆成本相关的特定角色。 此值是默认设置，因为大多数供应商可能没有特定角色。</li><li>**装运公司** – 供应商是装运公司。 具有此装运类型的供应商可以在 **航行** 页上的 **装运公司** 字段中选择。</li><li>**关税代理** – 供应商是关税代理。 具有此装运类型的供应商可以在 **帐页** 页上的 **关税代理** 字段中选择。</li><li>**代理** – 供应商是代理。 具有此装运类型的供应商可以在 **供应商** 和 **采购订单** 页上的 **代理** 字段中选择。</li></ul> |
| 成本类型组 | 将供应商分配到成本类型组，以选择[自动成本](auto-cost-setup.md)。 |
| 发运港口 | 选择航行的始发港口。 |
| 代理 | 从供应商处进行采购时的默认代理。 |
| 导入成本计算供应商 | <p>指示供应商是否为登陆成本供应商。</p><p>**提示：** 您可以将此字段与记录级安全性一起使用，来限制创建航行时显示的采购订单。</p> |
| 装运公司 | 选择为供应商创建采购订单时使用的默认装运公司。 |
| 服务提供商 | 指示供应商是否是服务提供商。 |
| 超过/低于容差组 | 选择供应商的默认超过/低于容差组。 |

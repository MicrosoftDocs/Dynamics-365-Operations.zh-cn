---
title: 登陆成本的采购参数
description: 本文介绍使用登陆成本模块时如何设置相关的采购参数。
author: Weijiesa
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 92ce3e3d09bed15970375735f680b1b8348bbca8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905970"
---
# <a name="procurement-and-sourcing-parameters-for-landed-cost"></a>登陆成本的采购参数

[!include [banner](../../includes/banner.md)]

**采购参数** 页上有一些设置，这些设置在您使用 **登陆成本** 模块时尤为重要。 使用从 **采购参数** 页打开的 **更新订单行** 对话框来指定在对采购订单头进行更改时是否应自动更新采购订单行。

若要完成此设置，请按照以下步骤操作。

1. 转至 **采购 \> 设置 \> 采购参数**。
1. 在 **常规** 选项卡上，选择 **更新订单行** 链接。
1. **更新订单行** 对话框将列出订单头上的字段，这些字段还可以将自动更新应用于订单行上的相关字段。 将列表中的每个字段设置为以下值之一：

    - **始终** – 更新订单头时，订单行应自动更新。
    - **从不** – 订单行在订单头更新时应该永远不自动更新。
    - **提示** – 将提示用户选择订单行是否应更新。

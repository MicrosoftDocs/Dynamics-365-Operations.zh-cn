---
title: 管理国际银行帐号 (IBAN) 帐户验证
description: 此主题介绍如何管理国际银行帐号 (IBAN) 帐户验证。
author: twheeloc
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 89d6c38088e43f0f24fa41accecaa262a64006cf
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462755"
---
# <a name="manage-international-bank-account-number-iban-account-validation"></a>管理国际银行帐号 (IBAN) 帐户验证

[!include [banner](../includes/banner.md)]

验证国际银行帐号 (IBAN) 可以增加在向银行帐户添加 IBAN 时完成的验证量。

有关 IBAN 结构的信息存储在 Microsoft Dynamics 365 Finance 中，将在您首次在银行帐户上使用 IBAN 时自动加载。 它包含 IBAN 的长度，银行帐号和银行代号的开始位置，以及银行帐号和银行代号的长度。

## <a name="set-up-iban-structures"></a>设置 IBAN 结构

1. 转到 **现金和银行管理 \> 设置 \> IBAN 结构**。
2. 请注意，已自动设置了每个国家或地区的 IBAN 结构。
3. 如果需要针对特定国家或地区更新结构，选择 **编辑** 按钮。
4. 每个新发行版中都有结构定义。 每次更新之后，可使用 **重置结构** 菜单加载最新定义。

## <a name="validate-the-iban-structure-in-a-bank-account"></a>验证银行帐户中的 IBAN 结构

1. 转至 **现金和银行管理 \> 银行帐户 \> 银行帐户**。
2. 创建银行帐户。
3. 在 **附加信息** 快速选项卡上，输入一个 IBAN。

    如果 IBAN 的长度与为每个国家/地区定义的长度不匹配，您将收到一条警告消息。 如果 IBAN 的长度与 IBAN 结构中指定的长度不匹配，则不能继续操作。

    此项验证还会验证银行帐号是否与表示银行帐号的 IBAN 部分匹配。 如果银行帐号不匹配，将收到警告消息。 此消息只是警告。 即使银行帐号不匹配，也可以继续操作。

    此项验证还会验证银行代号是否与表示银行代号的 IBAN 部分匹配。 银行代号包含一个银行编号，通常是其他分行。 如果银行代号不匹配，将收到警告消息。 此消息只是警告。 即使银行代号不匹配，也可以继续操作。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

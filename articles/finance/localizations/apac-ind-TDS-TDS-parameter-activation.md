---
title: 设置 TDS 参数
description: 本主题说明如何设置参数以在指定交易中激活从源扣缴税款功能。 这是使用从源扣缴税款 (TDS) 功能的必要步骤。
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: dda276b7d634317aae26728f7d9f51af9ccfb896
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023056"
---
# <a name="set-the-tds-parameters"></a>设置 TDS 参数

[!include [banner](../includes/banner.md)]

本主题说明如何设置参数以在指定交易中激活从源扣缴税款功能。 这是使用从源扣缴税款 (TDS) 功能的必要步骤。

1. 转到 **总帐 \> 分类帐设置 \> 总帐参数**。
2. 在 **直接税** 选项卡的 **从源扣缴税款** 部分中，将 **激活 TDS** 选项设置为 **是** 以激活 TDS 功能以及用于该功能的页面和字段。
3. 将 **发票** 选项设置为 **是**，以激活用于在发票级别计算和扣除 TDS 的字段。
4. 将 **付款** 选项设置为 **是**，以激活用于在付款级别计算和扣除 TDS 的字段。

    [![直接税选项卡](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)

5. 在 **编号规则** 选项卡上，查找 **参考** 字段设置为 **预缴税金付款** 的行。 在该行的 **编号规则代码** 字段中，选择编号规则代码。 编号规则代码用于为定期 TDS 结算流程生成凭证编号。

    > [!NOTE]
    > 若要运行定期 TDS 结算流程，请转到 **税务 \> 申报 \> 预缴税金 \> 预缴税金付款**。

    [![“编号规则”选项卡](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)

6. 关闭该页面。

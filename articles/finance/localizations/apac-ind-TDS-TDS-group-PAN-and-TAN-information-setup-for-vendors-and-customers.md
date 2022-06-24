---
title: 为供应商和客户设置 TDS 组、PAN 和 TAN 信息
description: 本文说明如何为供应商和客户设置有关从源扣缴税款 (TDS) 组、永久帐号 (PAN) 和税务帐号 (TAN) 的信息。
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 1a29f59e380360b6f828dcddbe84cad229b42d17
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859757"
---
# <a name="tds-group-pan-and-tan-information-setup-for-vendors-and-customers"></a>为供应商和客户设置的 TDS 组、PAN 和 TAN 信息

[!include [banner](../includes/banner.md)]

本文说明如何为供应商和客户设置有关从源扣缴税款 (TDS) 组、永久帐号 (PAN) 和税务帐号 (TAN) 的信息。

1. 转到 **应付帐款 \> 供应商 \> 所有供应商** 或 **应收帐款 \> 客户 \> 所有客户**。

    [![所有供应商页面。](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)

2. 在操作窗格上，选择 **新建** 以创建供应商或客户，然后输入所需的详细信息。 或者，选择一个现有供应商或客户。
3. 在 **发票和交货** 快速选项卡的 **预缴税金** 部分中，将 **计算预缴税金** 选项设置为 **是** 以为供应商或客户计算预缴税金、TDS 或从源征收税款 (TCS)。
4. 基于为供应商或客户定义的默认 TDS 组计算采购发票的 TDS。 在 **TDS 组** 字段中，选择默认的 TDS 组。

    > [!NOTE]
    > 当在 **TDS 组** 字段中选择 TDS 组时，**预缴税金组** 和 **TCS 组** 字段变得不可用。

5. 在 **税务信息** 快速选项卡上，在 **PAN 信息** 部分的 **状态** 字段中，为供应商或客户选择永久帐号的状态。

    - **不可用** – 供应商或客户没有 PAN。
    - **已收到** – 供应商或客户具有 PAN。
    - **已应用** – 供应商或客户已应用 PAN。
    - **无效** – 供应商或客户具有 PAN，但无效。

6. 如果在 **状态** 字段中选择了 **已收到** 来指示供应商或客户具有 PAN，则在 **编号** 字段中输入 PAN。 PAN 必须包含五个字母字符、四个数字字符和一个字母字符。 下面是一个示例：**ABCDE1260A**。
7. 如果在 **状态** 字段中选择了 **已应用** 来指示供应商或客户已应用 PAN，则在 **参考编号** 字段中输入参考编号。
8. 在 **评估对象的性质** 字段中，选择供应商或客户所属的评估对象类别的性质：

    - 公司
    - HUF
    - 确认
    - 个人
    - AOP
    - BOI
    - 本地主管机构
    - 其他

    [![税务信息快速选项卡。](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)

9. 在操作窗格上的 **供应商** 选项卡上，在 **登记** 组中，选择 **登记 ID** 以打开 **管理地址** 页面。
10. 在 **管理地址** 页面的 **税务信息** 快速选项卡上，选择 **添加** 或 **编辑** 以打开 **管理税务信息** 页面，您可以在该页面中维护税务登记条目。
11. 在 **管理税务信息** 页面的 **预缴税金** 快速选项卡上，在 **税务帐号 (TAN)** 字段中，输入 TAN。 TAN 必须包含四个字母字符、五个数字字符和一个字母字符。 下面是一个示例：**AFGH54821T**。
12. 关闭该页面。

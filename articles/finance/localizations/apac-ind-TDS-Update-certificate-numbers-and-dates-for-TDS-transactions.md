---
title: 更新 TDS 交易的证书编号和日期
description: 本文说明如何更新从源扣缴税款 (TDS) 的为供应商、客户和分类帐帐户记录的可退税证书编号和日期。
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
ms.openlocfilehash: 147a27261a4a282550f0bacede78c9edd38b4fe6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904432"
---
# <a name="update-certificate-numbers-and-dates-for-tds-transactions"></a>更新 TDS 交易的证书编号和日期

[!include [banner](../includes/banner.md)]

本文说明如何更新从源扣缴税款 (TDS) 的为供应商、客户和分类帐帐户记录的可退税证书编号和日期。 您可以在 **可退税证书** 页面上查看 TDS 交易的证书。 可以使用 **更新证书** 页面更新证书。

按照以下步骤更新 TDS 交易的证书编号和日期。

1. 转到 **税务 \> 申报 \> 预缴税金 \> 更新证书**。

    [![更新证书页面。](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)

2. 在 **更新证书** 页面的 **选择** 部分中，在 **税务类型** 字段中，选择 **TDS**。
3. 在 **证书编号** 字段中，选择客户或供应商的 TDS 证书编号。

    > [!NOTE]
    > **证书编号** 字段仅列出 **可退税证书** 页面上清除了 **已关闭** 复选框的 TDS 证书编号。

    **证书日期** 字段显示证书日期。 **帐户类型** 字段显示接收了 TDS 证书编号的帐户的类型，**名称** 字段显示帐户的名称。

5. 在 **开始日期** 和 **结束日期** 字段中，选择要显示 TDS 交易的期间的开始日期和结束日期。
6. 选择 **显示数据** 以查看在选定期间过帐的 TDS 交易。

    在 **概述** 选项卡上，上部窗格中的网格显示有关在选定期间为供应商或客户过帐的每个 TDS 交易的以下信息：

    - **凭证** – TDS 交易的凭证号。
    - **日期** – TDS 交易的日期。
    - **金额** – 计算 TDS 的发票金额。
    - **税额** – 为交易计算的 TDS 税额。

7. 若要将特定 TDS 交易从上部网格移动到下部网格，选择交易，然后选择 **包括**。 或者，选择 **全部包括** 以将所有 TDS 交易从上部网格移动到下部网格。

    若要将特定 TDS 交易或所有 TDS 交易从下部网格移动到上部网格，请使用 **排除** 或 **全部排除** 按钮。

8. 选择 **更新** 以更新下部网格中 TDS 交易的 **证书编号** 和 **证书日期** 字段。
10. 转到 **税务 \> 间接税 \> 预缴税金 \> 可退税证书** 并选择 **查询**，以查看在 **证书交易** 页面上具有新证书编号的已更新交易行。

    [![证书交易页面。](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)

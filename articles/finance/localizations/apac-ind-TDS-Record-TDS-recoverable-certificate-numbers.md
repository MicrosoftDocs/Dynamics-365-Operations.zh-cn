---
title: 记录 TDS 可退税证书编号
description: 本主题说明如何使用可退税证书页面，记录特定供应商、客户或分类帐收到的从源扣缴税款 (TDS) 证书的证书编号和日期。
author: kailiang
mms.date: 02/12/2021
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
ms.openlocfilehash: fae748123a47650075150fe0c37d11b56c06afe7f5258fc4e31d4ede0a478051
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781167"
---
# <a name="record-tds-recoverable-certificate-numbers"></a>记录 TDS 可退税证书编号

[!include [banner](../includes/banner.md)]

本主题说明如何使用 **可退税证书** 页面，记录特定供应商、客户或分类帐收到的从源扣缴税款 (TDS) 证书的证书编号和日期。 若要更新在此页面上为 TDS 交易记录的 TDS 证书编号和日期，请使用 **更新证书** 页面（**总帐 \> 定期 \> 预缴税款 \> 更新证书**）。 更新完 TDS 证书编号后，请关闭它们。

按照以下步骤记录 TDS 证书编号和日期。

1. 转到 **税务 \> 间接税 \> 预缴税金 \> 可退税证书**。

    [![可退税证书页面。](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png) 

2. 在 **可退税证书** 页面上，在 **税务类型** 字段中，选择 **TDS**。
3. 选择 **新建** 创建记录。
4. 在 **证书编号** 字段中，输入 TDS 证书编号。
5. 在 **帐户类型** 字段中，选择收到 TDS 证书的帐户类型：**供应商**、**客户** 或 **分类帐**。
6. 在 **帐户** 字段中，选择供应商、客户或分类帐帐号，具体取决于所选的帐户类型。 **名称** 字段显示供应商、客户或分类帐帐户的名称。
7. 在 **证书金额** 字段中，输入 TDS 证书的金额。
8. 在 **日期** 字段中，输入证书编号的证书日期。
9. 选择 **查询** 以打开 **证书交易** 页面，您可以在该页面中查看更新了 TDS 证书编号和日期的 TDS 交易。 可以在 **更新证书** 页面上更新此信息（**税务 \> 申报 \> 预缴税金 \> 更新证书**）。

    **更新证书** 页面显示每个 TDS 交易的以下信息。

    - **日期** – TDS 交易的过帐日期。
    - **凭证** – TDS 交易的凭证号。
    - **来源** – 用于创建 TDS 交易的模块。
    - **帐户** – 为其创建了 TDS 交易的供应商、客户或分类帐帐号。
    - **名称** – 为其创建了 TDS 交易的供应商、客户或分类帐帐户的名称。
    - **金额** – 计算 TDS 的发票金额。
    - **税额** – 为交易计算的 TDS 税额。
    - **证书日期** – 为 TDS 交易更新的 TDS 证书日期。
    - **证书编号** – 为 TDS 交易更新的 TDS 证书编号。

10. 在 **可退税证书** 页面上，选中 **已关闭** 复选框，以便在 **更新证书** 页面上为 TDS 交易更新完它后，关闭 TDS 证书编号。

    若要针对页面上的所有记录选中 **已关闭** 复选框，请选择 **全部标记**。

    > [!NOTE]
    > 为其选中 **已关闭** 复选框的 TDS 证书编号在 **更新证书** 页面上都不可用。

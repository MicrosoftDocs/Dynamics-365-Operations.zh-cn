---
title: 设置集中的付款
description: 按照以下步骤可以代表您的组织中的其他法人准备一个法人的处理付款。
author: kweekley
manager: AnnBe
ms.date: 05/09/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 62243
ms.assetid: ffd17b5f-9aea-40e0-be49-d8702f615256
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 70b47f819730ae221568e625a1b218e046927e41
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440751"
---
# <a name="set-up-centralized-payments"></a>设置集中的付款

[!include [banner](../includes/banner.md)]

按照以下步骤可以代表您的组织中的其他法人准备一个法人的处理付款。 在您开始前，必须完成以下设置：

-   创建法人。
-   设置总帐参数和会计科目表。
-   设置应付帐款参数和应收帐款参数（取决于使用集中付款的模块）。
-   设置内部公司会计。

## <a name="set-up-an-organizational-hierarchy-for-centralized-payments"></a>为集中付款设置组织的层次结构。
您必须为集中付款设置组织的层次结构。 将相同的组织层次结构用于处理集中的供应商付款和集中的客户付款。 **注意：** 对于集中付款，该层次结构的结构不会产生影响。 层次结构中的任何法人都将能代表层次结构中的任何其他法人处理付款。 在 **组织层次结构** 页上，您可以创建一个新的组织层次结构。 在 **用途** 字段中，必须选择 **集中付款**。 

## <a name="set-up-an-intercompany-account-for-centralized-payments"></a>为集中付款设置内部公司帐户
在对照其他法人中的发票结算当前法人中的付款交易记录时，将为每个法人创建相应的应付和应收交易记录。 您必须指定过帐任何适用现金折扣和已有损益金额的法人。 在开始前，确定您将使用哪一法人处理供应商和客户付款。 如果一个法人处理供应商付款，另一个法人处理客户付款，您必须切换到各法人。 在 **内部公司会计** 页上，可以为将代表其处理付款的法人选择内部公司关系记录。 

在 **集中付款** 选项卡上，您可以选择是将现金折扣过帐到付款（或减少供应商帐户余额的其他交易记录）法人还是发票（或增加供应商帐户余额的其他交易记录）法人。 此选择与 **应付帐款参数** 和 **应收帐款参数** 页的 **现金折扣管理** 字段一起工作。 对于超额付款和尾差容差，使用付款的法人中的设置。 对于支付不足和尾差容差，使用发票的法人中的设置。

## <a name="map-vendor-accounts-across-legal-entities"></a>映射跨法人的供应商帐户
当您支付某个法人的供应商并且您想选择其他法人中的供应商的发票时，您必须确保每个法人中的相应的供应商帐户都使用相同的地址簿 ID。 如果您接收来自在多个法人中支付发票的客户的付款，则必须确保每个法人中的相应客户帐户全都使用相同的通讯簿 ID。

## <a name="set-up-posting-profiles-for-centralized-payments"></a>为集中付款设置过帐模板
当您在结算另一个法人的发票的法人中创建了付款，过帐模板 ID 在这两个法人中必须相同。 为了帮助确保正确创建付款，在发票的每个法人中，设置与付款法人中使用的过帐模板相对应的过帐模板。 切换到发票的第一个法人，然后，在 **供应商过帐模板** 页上，您可以创建一个新的过帐模板或编辑现有的过帐模板。 在发票的法人中为过帐模板所做的选择不必与付款法人中过帐模板的设置匹配。

## <a name="set-up-methods-of-payment-for-centralized-payments"></a>设置集中付款的付款方式
当您在结算另一个法人的发票的法人中的创建了付款，付款方法 ID 在这两个法人中必须相同。 为了帮助确保正确创建付款，在发票的各个法人中，设置与付款法人中使用的付款方式相符的付款方式。 切换到发票的第一个法人，然后，在 **付款方法** 页，可以创建新的付款方法或编辑现有的付款方法。 您在发票法人中为付款方法进行的选择不必与在付款法人中付款方法的设置相匹配。

## <a name="set-up-default-descriptions"></a>设置默认描述
您可为内部公司结算凭证定义默认描述。 该默认描述包括在跨公司结算过程中的应付和应收交易记录上。 在 **默认描述** 页上，您可以为 **内部公司客户结算** 和 **内部公司供应商结算** 创建新的描述，方法是通过选择语言然后输入文本。





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
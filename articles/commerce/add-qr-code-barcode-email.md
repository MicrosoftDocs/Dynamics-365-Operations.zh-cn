---
title: 在交易和收据电子邮件中添加 QR 码或条形码
description: 本主题说明了如何在 Microsoft Dynamics 365 Commerce 中将表示订单 ID 的 QR 码和条形码插入交易和收据电子邮件。
author: bicyclingfool
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Commerce, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-02-16
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 9a3ab355d6e68221610e48e02e191c1d21f5155db81990d0991a8c353f3f9ecd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6729930"
---
# <a name="add-a-qr-code-or-bar-code-to-transactional-and-receipt-emails"></a>在交易和收据电子邮件中添加 QR 码或条形码

[!include [banner](includes/banner.md)]

本主题说明了如何在 Microsoft Dynamics 365 Commerce 中将表示订单 ID 的 QR 码和条形码插入交易和收据电子邮件。

您可以轻松地在交易电子邮件中包含 QR 码和条形码，以在零售环境中帮助加快订单查找过程。 要将 QR 码和条形码插入电子邮件，请使用 HTML **\<img\>** 标签，从生成和呈现服务请求 QR 码或条形码图像。 Microsoft 不提供此服务。 但是，有许多免费或廉价的服务，可以提供根据在查询字符串中传递的值动态生成的 QR 码或条形码。

## <a name="add-a-qr-code-or-bar-code-to-a-transactional-email"></a>在交易电子邮件中添加 QR 码或条形码

要将 QR 码或条形码插入到在电子商务购买过程中发送的交易电子邮件中，请按照下列步骤操作。

1. 打开交易电子邮件模板的源 HTML，然后添加指向您的 QR 码或条形码服务的 HTML **\<img\>** 标记。 下面是一个示例。

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%salesid%&param1=value1&param2=value2" alt="%salesid%" />
    ```

    以下是对上述示例的说明：

    - **YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** 代表您的 QR 码或条形码服务的域。
    - **数据** 表示 QR 码或条形码服务接收应呈现为 QR 码或条形码的内容所使用的参数。

        必须给该参数分配 **%salesid%** 值。 在此示例中，请注意，该值还用作图像的替代文本。

    - **param1** 和 **param2** 表示其他可选参数。

1. 转到 **Retail 和 Commerce \> 总部设置 \> 参数 \> 组织电子邮件模板**，然后将更新的 HTML 上传到适当的交易电子邮件模板。

> [!NOTE]
> 在 QR 码和条形码服务提供商之间，参数可能有所不同。 因此，请确保与您的服务提供商联系以确认您必须为其分配值的参数。

## <a name="add-a-qr-code-or-bar-code-to-a-receipt-email"></a>在收据电子邮件中添加 QR 码或条形码 

要将 QR 码或条形码插入到可以在销售点 (POS) 购买后发送的收据电子邮件中，请按照下列步骤操作。

1. 打开收据电子邮件模板的源 HTML，然后添加指向您的 QR 码或条形码服务的 HTML **\<img\>** 标记。 下面是一个示例。

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%receiptid%&param1=value1&param2=value2" alt="%receiptid%" />
    ```

    以下是对上述示例的说明：

    - **YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** 代表您的 QR 码或条形码服务的域。
    - **数据** 表示 QR 码或条形码服务接收应呈现为 QR 码或条形码的内容所使用的参数。

        必须给该参数分配 **%receiptid%** 值。 在此示例中，请注意，该值还用作图像的替代文本。

    - **param1** 和 **param2** 表示其他可选参数。

1. 转到 **Retail 和 Commerce \> 总部设置 \> 参数 \> 组织电子邮件模板**，然后将更新的 HTML 上传到具有电子邮件 ID **emailrecpt** 的电子邮件模板。

> [!NOTE]
> 在 QR 码和条形码服务提供商之间，参数可能有所不同。 因此，请确保与您的服务提供商联系以确认您必须为其分配值的参数。

## <a name="additional-resources"></a>其他资源

[从 Modern POS (MPOS) 发送电子邮件收据](email-receipts.md)

[创建交易事件的电子邮件模板](email-templates-transactions.md)

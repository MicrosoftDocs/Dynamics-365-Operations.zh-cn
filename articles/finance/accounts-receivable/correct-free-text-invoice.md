---
title: 更正普通发票
description: 本文说明如更正已过帐的普通发票，并作为更正发票重新签发该发票。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76cf1f24a31f246a41601908ebba308551925d90
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176653"
---
# <a name="correct-a-free-text-invoice"></a>更正普通发票

[!include [banner](../includes/banner.md)]

本文说明如更正已过帐的普通发票，并作为更正发票重新签发该发票。

若要更正已过帐的普通发票，请打开已过帐的普通发票。 在**发票**页上，选择**取消**，然后选择**更正发票**。 选择一个原因代码，添加注释，并且为新的已更正发票选择日期。 您可以修改已更正发票并将其过帐。 

在您过帐已更正发票时，会为一个等于原始发票金额的贷方金额创建取消发票。 因此，原始发票和取消发票的组合余额为 0（零）。 会比对原始发票结算取消发票。 

在过帐已更正发票后，您将具有三个发票：

-   **原始发票** – 包括您正在更改的信息的发票。
-   **正在取消的发票** – 创建以取消最近更改的发票的系统生成的货方发票。
-   **已更正的发票** – 包含已更正发票信息的发票。

您可以通过两种方式标识取消和更正发票：

-   **所有普通发票**页包括**更正**列，在其中您可以看到哪些发票是正在取消的发票和已更正的发票。
-   普通发票的标题显示状态**正在取消发票‘\[发票编号\]** 或**已更正的发票‘\[发票编号\]**。

> [!NOTE]
> 只有当选择**普通发票更正**配置键后，此功能才可用。 有关如何启用 Configuration keys 的详细信息，请参阅[维护模式](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/maintenance-mode)主题中的“启用（或禁用）configuration key”部分。 




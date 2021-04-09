---
title: 禁用零售交易记录一致性检查器中的规则
description: 本主题介绍在 Microsoft Dynamics 365 Commerce 中禁用交易记录一致性检查器规则的功能。
author: josaw1
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: ce2abe7e15773edc3122a1bfdf40f3b830e8790e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792887"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a>禁用零售交易记录一致性检查器中的规则 

[!include [banner](../includes/banner.md)]

零售商可以具有对于他们唯一的业务方案和流程。 因此，并非默认包括在商业交易记录一致性检查器中的所有规则都适用于所有零售商。 为了适应这些差异，Microsoft Dynamics 365 Commerce 提供了可用于禁用不适用规则的功能。

若要在您的环境中查看零售交易记录一致性检查器中可用的规则列表，请转到 **Retail 和 Commerce \> Headquarters 设置 \> 参数 \> Commerce 参数**，然后选择 **交易记录验证** 选项卡。

默认情况下，每个规则的状态设置为 **已启用**。 因此，在将交易记录导入商业对账单之前，将使用所有规则验证这些交易记录。 若要禁用某一规则，请将其状态更改为 **已禁用**。 当在对账单计算过程中验证交易记录时，将不考虑已禁用的规则。

若要跳过整个验证过程，而不管已启用的规则如何，请转到 **Retail 和 Commerce \> Headquarters 设置 \> 参数 \> Commerce 参数**，然后在 **交易记录验证** 选项卡中，将 **禁用对 Commerce 交易记录的一致性检查** 选项设置为 **是**。 在将此选项设置为 **否** 后，无法从用户界面 (UI) 重新将其设置为 **是**。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
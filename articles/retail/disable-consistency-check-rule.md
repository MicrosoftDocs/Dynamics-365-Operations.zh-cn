---
title: 禁用零售交易记录一致性检查器中的规则
description: 本主题将介绍在 Microsoft Dynamics 365 Retail 中禁用零售交易记录一致性检查器规则的功能。
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4bf8df2fb9f8f5c33ceb13eb012fb6879f81ec66
ms.sourcegitcommit: bdbca89bd9b328c282ebfb681f75b8f1ed96e7a8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/14/2019
ms.locfileid: "2586289"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a>禁用零售交易记录一致性检查器中的规则 

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

零售商可以具有对于他们唯一的业务方案和流程。 因此，并非默认包括在零售交易记录一致性检查器中的所有规则都适用于所有零售商。 为了适应这些差异，Microsoft Dynamics 365 Retail 提供了可用于禁用不适用的规则的功能。

若要在您的环境中查看零售交易记录一致性检查器中可用的规则列表，请转到 **Retail \> 总部设置 \> 参数 \> 零售参数**，然后选择**交易记录验证**选项卡。

默认情况下，每个规则的状态设置为**已启用**。 因此，在将零售交易记录导入零售对帐单之前，将使用所有规则验证这些零售交易记录。 若要禁用某一规则，请将其状态更改为**已禁用**。 当在对帐单计算过程中验证零售交易记录时，将不考虑已禁用的规则。

若要跳过整个验证过程，而不管已启用的规则如何，请转到 **Retail \> 总部设置 \> 参数 \> 零售参数**，然后在**交易记录验证**选项卡中，将**禁用对零售交易记录的一致性检查**选项设置为**是**。 在将此选项设置为**否**后，无法从用户界面 (UI) 重新将其设置为**是**。

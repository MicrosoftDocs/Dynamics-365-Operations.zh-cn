---
title: 禁用交易记录验证流程中使用的规则
description: 本主题将介绍 Microsoft Dynamics 365 Commerce 中用于禁用交易记录验证规则的功能。
author: analpert
ms.date: 12/11/2021
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
ms.openlocfilehash: cdaea51b4c84e6a62f0eb9412315ae77b4c11503
ms.sourcegitcommit: 9c2bc045eafc05b39ed1a6b601ccef48bd62ec55
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/14/2021
ms.locfileid: "7919517"
---
# <a name="disable-rules-used-in-the-transaction-validation-process"></a>禁用交易记录验证流程中使用的规则

[!include [banner](../includes/banner.md)]

零售商可以拥有量身定制的业务方案和流程。 因此，并非商业交易记录验证流程所涉及的所有规则都适用于所有零售商。 为了适应这些差异，Microsoft Dynamics 365 Commerce 提供了可用于禁用不适用规则的功能。

要在您的环境中查看交易记录验证流程中可用的规则列表和每个规则的状态，请转到 **Retail 和 Commerce \> Headquarters 设置 \> 参数 \> Commerce 参数**，然后选择 **交易记录验证** 选项卡。在 **验证商店交易记录** 流程中，所有启用的规则都会用于验证交易记录，交易记录必须符合这些规则，交易记录对帐单才能收集和过帐交易记录。

默认情况下，每个规则的状态设置为 **已启用**。 因此，在将交易记录导入商业交易记录对帐单之前，将使用所有规则验证这些交易记录。 要禁用某一规则，请将其状态更改为 **已禁用**。 在 **验证商店交易记录** 过程中验证交易记录时，将不考虑已禁用的规则。

[!INCLUDE[footer-include](../includes/footer-banner.md)]

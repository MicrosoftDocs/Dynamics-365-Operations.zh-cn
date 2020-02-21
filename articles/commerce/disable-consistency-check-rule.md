---
title: 禁用零售交易记录一致性检查器中的规则
description: 本主题将介绍在 Microsoft Dynamics 365 Commerce 中禁用零售交易记录一致性检查器规则的功能。
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
ms.openlocfilehash: b11b901fafc3907e9d3cae5cd554cc9a868a414c
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004335"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a><span data-ttu-id="d0b4d-103">禁用零售交易记录一致性检查器中的规则</span><span class="sxs-lookup"><span data-stu-id="d0b4d-103">Disable rules in the retail transaction consistency checker</span></span> 

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="d0b4d-104">零售商可以具有对于他们唯一的业务方案和流程。</span><span class="sxs-lookup"><span data-stu-id="d0b4d-104">Retailers can have business scenarios and processes that are unique to them.</span></span> <span data-ttu-id="d0b4d-105">因此，并非默认包括在商业交易记录一致性检查器中的所有规则都适用于所有零售商。</span><span class="sxs-lookup"><span data-stu-id="d0b4d-105">Therefore, not all the rules that are included by default in the commerce transaction consistency checker are applicable to all retailers.</span></span> <span data-ttu-id="d0b4d-106">为了适应这些差异，Microsoft Dynamics 365 Commerce 提供了可用于禁用不适用规则的功能。</span><span class="sxs-lookup"><span data-stu-id="d0b4d-106">To accommodate differences, Microsoft Dynamics 365 Commerce provides functionality that can be used to disable the rules that aren't applicable.</span></span>

<span data-ttu-id="d0b4d-107">若要在您的环境中查看零售交易记录一致性检查器中可用的规则列表，请转到 **Retail 和 Commerce \> Headquarters 设置 \> 参数 \> Commerce 参数**，然后选择**交易记录验证**选项卡。</span><span class="sxs-lookup"><span data-stu-id="d0b4d-107">To view the list of rules that are available in the transaction consistency checker in your environment, and to see the status of each rule, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**, and select the **Transaction validation** tab.</span></span>

<span data-ttu-id="d0b4d-108">默认情况下，每个规则的状态设置为**已启用**。</span><span class="sxs-lookup"><span data-stu-id="d0b4d-108">By default, the status of every rule is set to **Enabled**.</span></span> <span data-ttu-id="d0b4d-109">因此，在将交易记录导入商业对账单之前，将使用所有规则验证这些交易记录。</span><span class="sxs-lookup"><span data-stu-id="d0b4d-109">Therefore, all the rules are used to validate transactions before they are pulled into the commerce statements.</span></span> <span data-ttu-id="d0b4d-110">若要禁用某一规则，请将其状态更改为**已禁用**。</span><span class="sxs-lookup"><span data-stu-id="d0b4d-110">To disable a rule, change its status to **Disabled**.</span></span> <span data-ttu-id="d0b4d-111">当在对账单计算过程中验证交易记录时，将不考虑已禁用的规则。</span><span class="sxs-lookup"><span data-stu-id="d0b4d-111">Disabled rules aren't considered when transactions are validated during the statement calculation process.</span></span>

<span data-ttu-id="d0b4d-112">若要跳过整个验证过程，而不管已启用的规则如何，请转到 **Retail 和 Commerce \> Headquarters 设置 \> 参数 \> Commerce 参数**，然后在**交易记录验证**选项卡中，将**禁用对商业交易记录的一致性检查**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="d0b4d-112">To bypass the whole validation process, regardless of the rules that are enabled, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**, and then, on the **Transaction validation** tab, set the **Disable consistency checker for Commerce transactions** option to **Yes**.</span></span> <span data-ttu-id="d0b4d-113">在将此选项设置为**否**后，无法从用户界面 (UI) 重新将其设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="d0b4d-113">After this option is set to **No**, it can't be set back to **Yes** from the user interface (UI).</span></span>

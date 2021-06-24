---
title: 在 POS 中退回序列号控制的产品
description: 本主题介绍了在 Microsoft Dynamics 365 Commerce 销售点 (POS) 应用程序中验证序列化物料作为退货流程的一部分的功能。
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 7a067994828f3df577c0dc4146d26ac81990d4ac
ms.sourcegitcommit: 927574c77f4883d906e5c7bddf0af9b717e492bf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129795"
---
# <a name="return-serial-numbercontrolled-products-in-pos"></a><span data-ttu-id="df464-103">在 POS 中退回序列号控制的产品</span><span class="sxs-lookup"><span data-stu-id="df464-103">Return serial number–controlled products in POS</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="df464-104">本主题介绍了在 Microsoft Dynamics 365 Commerce 销售点 (POS) 应用程序中验证序列化物料作为退货流程的一部分的功能。</span><span class="sxs-lookup"><span data-stu-id="df464-104">This topic describes the capabilities for validating serialized items as part of the return process in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

> [!NOTE]
> <span data-ttu-id="df464-105">在 Commerce 版本 10.0.20 及更高版本中，提供了名为 **POS 中的统一退货处理体验** 的新功能。</span><span class="sxs-lookup"><span data-stu-id="df464-105">In the Commerce version 10.0.20 release and later, a new feature that is named **Unified return processing experience in POS** is available.</span></span> <span data-ttu-id="df464-106">若要在 POS 中的退货订单处理期间使用序列号验证，您必须打开此功能。</span><span class="sxs-lookup"><span data-stu-id="df464-106">To use serial number validation during return order processing in POS, you must turn on this feature.</span></span> <span data-ttu-id="df464-107">有关此功能在打开时提供的其他功能的信息，请参阅[在 POS 中创建退货](POS-returns.md)。</span><span class="sxs-lookup"><span data-stu-id="df464-107">For information about others capabilities that this feature provides when it's turned on, see [Create returns in POS)](POS-returns.md).</span></span>
>
> <span data-ttu-id="df464-108">该功能在打开后，无法关闭。</span><span class="sxs-lookup"><span data-stu-id="df464-108">After the feature is turned on, it can't be turned off.</span></span>

## <a name="options-for-validating-serialized-returns"></a><span data-ttu-id="df464-109">验证序列化退货的选项</span><span class="sxs-lookup"><span data-stu-id="df464-109">Options for validating serialized returns</span></span>

<span data-ttu-id="df464-110">当打开 **POS 中的统一退货处理体验** 功能时，组织可以通过 POS 对序列号控制的物料退货进行验证。</span><span class="sxs-lookup"><span data-stu-id="df464-110">When the **Unified return processing experience in POS** feature is turned on, organizations can perform a validation on returns of serial number–controlled items through POS.</span></span> <span data-ttu-id="df464-111">如果返回的序列号与出售的原始序列号不同，此功能可以警告用户。</span><span class="sxs-lookup"><span data-stu-id="df464-111">This capability can warn users if the serial number that is being returned differs from the original serial number that was sold.</span></span> <span data-ttu-id="df464-112">在 Commerce 版本 10.0.20 及更高版本中，用户收到的消息只是警告消息。</span><span class="sxs-lookup"><span data-stu-id="df464-112">In the Commerce version 10.0.20 release and later, the message that users receive is only a warning message.</span></span> <span data-ttu-id="df464-113">用户可以针对与最初出售的序列号不同的序列号继续处理退货。</span><span class="sxs-lookup"><span data-stu-id="df464-113">Users can continue to process a return against a serial number that differs from the serial number that was originally sold.</span></span>

<span data-ttu-id="df464-114">若要在打开 **POS 中的统一退货处理体验** 功能后为组织配置序列号验证，请在 Commerce Headquarters 中转到 **Retail 和 Commerce \> Headquarters 设置 \> 参数 \> Commerce 参数**。</span><span class="sxs-lookup"><span data-stu-id="df464-114">To configure serial number validation for an organization after the **Unified return processing experience in POS** feature is turned on, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters** in Commerce headquarters.</span></span> <span data-ttu-id="df464-115">在 **库存** 选项卡的 **存储库存操作** 快速选项卡上，将 **对 POS 退货启用序列号验证** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="df464-115">On the **Inventory** tab, on the **Store inventory operations** FastTab, set the **Enable validation of serial numbers on POS returns** option to **Yes**.</span></span>

## <a name="process-returns-for-serialized-items-in-pos"></a><span data-ttu-id="df464-116">处理 POS 中序列化物料的退货</span><span class="sxs-lookup"><span data-stu-id="df464-116">Process returns for serialized items in POS</span></span>

<span data-ttu-id="df464-117">如果已将 **对 POS 退货启用序列号验证** 选项设置为 **是**，当通过 POS 退回序列号控制的物料时，用户可以为 **可退货产品** 页面的详细信息窗格中的退货行输入序列号。</span><span class="sxs-lookup"><span data-stu-id="df464-117">If the **Enable validation of serial numbers on POS returns** option has been set to **Yes**, when a serial number–controlled item is returned through POS, the user can enter the serial number for the return line in the details pane on the **Returnable products** page.</span></span> <span data-ttu-id="df464-118">如果输入的序列号与为销售交易出售的原始序列号不匹配，用户会收到一条警告消息。</span><span class="sxs-lookup"><span data-stu-id="df464-118">If the serial number that is entered doesn't match the original serial number that was sold for the sales transaction, the user receives a warning message.</span></span> <span data-ttu-id="df464-119">但是，应用程序不会阻止用户继续发布退货。</span><span class="sxs-lookup"><span data-stu-id="df464-119">However, the application doesn't prevent the user from continuing to post the return.</span></span>

> [!NOTE]
> <span data-ttu-id="df464-120">目前，POS 仅支持对原始订购数量不超过 1 的退货行验证序列号。</span><span class="sxs-lookup"><span data-stu-id="df464-120">Currently, POS supports validation of serial numbers only on return lines where the original ordered quantity is no more than one.</span></span> <span data-ttu-id="df464-121">如果在非 POS 渠道上创建了原始销售订单行，并且如果为给定销售行上的序列化物料订购的数量超过 1，则无法通过 POS 正确退回物料。</span><span class="sxs-lookup"><span data-stu-id="df464-121">If the original sales order line was created in a non-POS channel, and if the quantity that was ordered for the serialized item on a given sales line is more than one, the item can't be correctly returned through POS.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="df464-122">其他资源</span><span class="sxs-lookup"><span data-stu-id="df464-122">Additional resources</span></span>

[<span data-ttu-id="df464-123">在 POS 中创建退货</span><span class="sxs-lookup"><span data-stu-id="df464-123">Create returns in POS</span></span>](POS-returns.md)

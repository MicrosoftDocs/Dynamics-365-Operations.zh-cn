---
title: 在 POS 中更改交货方式
description: 此主题介绍如何在 POS 中配置和使用更改交货方式操作。
author: hhainesms
manager: annbe
ms.date: 03/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: eaffe7821b60dd787a7d8b7533c1b8599033ba68
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594129"
---
# <a name="change-mode-of-delivery-in-pos"></a><span data-ttu-id="c79a6-103">在 POS 中更改交货方式</span><span class="sxs-lookup"><span data-stu-id="c79a6-103">Change mode of delivery in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c79a6-104">此主题介绍如何在销售点 (POS) 环境中设置和使用“更改交货方式”功能。</span><span class="sxs-lookup"><span data-stu-id="c79a6-104">This topic describes how to set up and use the "change mode of delivery" functionality in your point of sale (POS) environment.</span></span> 

<span data-ttu-id="c79a6-105">在 Dynamics 365 Commerce 版本 10.0.10 及更高版本中，可将 **更改交货方式** 操作 (647) 添加到您的 POS 屏幕布局。</span><span class="sxs-lookup"><span data-stu-id="c79a6-105">In Dynamics 365 Commerce versions 10.0.10 and later, the **Change mode of delivery** operation (647) is available to add to your POS screen layouts.</span></span>

<span data-ttu-id="c79a6-106">更改交货方式功能让您可以选择更改 POS 交易记录中一个或多个装运配置的销售行的交货方式。</span><span class="sxs-lookup"><span data-stu-id="c79a6-106">The change mode of delivery feature provides you with the option to change the mode of delivery for one or more shipment-configured sales lines on the POS transaction.</span></span> <span data-ttu-id="c79a6-107">在 Commerce 的之前版本中，如果要更改现有行中为装运配置的交货方式，必须完成整个 **全部装运** 或 **装运所选产品** 配置流。</span><span class="sxs-lookup"><span data-stu-id="c79a6-107">In previous versions of Commerce, you had to go through the full **Ship all** or **Ship selected** configuration flows if you wanted to change the mode of delivery on an existing line that was configured for shipment.</span></span> <span data-ttu-id="c79a6-108">此流程需要大量时间，可能导致意外更改行的交货源或交货日期。</span><span class="sxs-lookup"><span data-stu-id="c79a6-108">This process was time consuming and could result in accidental changes to the delivery origin or delivery dates for the line.</span></span> <span data-ttu-id="c79a6-109">此新功能提供了一种备选方法，可以有效更新这些销售行的交货方式。</span><span class="sxs-lookup"><span data-stu-id="c79a6-109">The new functionality provides an alternative method for efficiently updating the mode of delivery on these sales lines.</span></span>

<span data-ttu-id="c79a6-110">有关如何向 POS 按钮网格中的按钮添加操作的详细信息，请参阅[销售点的屏幕布局](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts)。</span><span class="sxs-lookup"><span data-stu-id="c79a6-110">For more information about how to add an operation to a button on your POS button grid, see [Screen layouts for the point of sale](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts).</span></span>

<span data-ttu-id="c79a6-111">在 POS 中配置此功能之后，如果选择 **更改交货方式**，将显示一个列表页，可供您选择要更改其交货方式的交易记录的行。</span><span class="sxs-lookup"><span data-stu-id="c79a6-111">After this feature is configured in POS, when you select **Change mode of delivery**, you will be presented with a list page that allows you to choose the lines of the transaction that you want to change the mode of delivery for.</span></span> <span data-ttu-id="c79a6-112">可以选择部分或全部行，也可以退出但不进行任何更改。</span><span class="sxs-lookup"><span data-stu-id="c79a6-112">You can choose some or all of the lines, or exit without making any changes.</span></span> <span data-ttu-id="c79a6-113">之前为装运配置的销售行是列表中您只能更改的行。</span><span class="sxs-lookup"><span data-stu-id="c79a6-113">The sales lines that were previously configured for shipment are the only lines in the list that you can change.</span></span> <span data-ttu-id="c79a6-114">如果要将为提货或送货上门指定的行更改为装运，必须使用 **全部装运** 或 **装运所选产品** 操作。</span><span class="sxs-lookup"><span data-stu-id="c79a6-114">If you want to change a line designated for pickup or carryout to ship, you must use the **Ship all** or **Ship selected** operations.</span></span> <span data-ttu-id="c79a6-115">相反，如果要将指定为装运的行更改为提货或送货上门，必须使用 **全部提货**、**所选产品提货**、**全部送货上门** 或 **所选产品送货上门** 操作。</span><span class="sxs-lookup"><span data-stu-id="c79a6-115">Conversely, if you want to change a line designated as a shipment to a pickup or carryout, you must use the  **Pickup all**, **Pickup selected**, **Carryout all**, or **Carryout selected** operations.</span></span>

<span data-ttu-id="c79a6-116">选择要更改的行之后，请单击 **更改交货方式** 以便显示有关选择交货方式选项的提示。</span><span class="sxs-lookup"><span data-stu-id="c79a6-116">After you select the lines that you want to change, click **Change mode of delivery** to be prompted to select the delivery mode options.</span></span> <span data-ttu-id="c79a6-117">如果选择要更改多个行，POS 将仅显示已经配置为对所选全部产品允许的交货方式。</span><span class="sxs-lookup"><span data-stu-id="c79a6-117">If you selected multiple lines to change, POS will only display modes of delivery that have been configured as allowable for all of the selected products.</span></span> <span data-ttu-id="c79a6-118">可以将交货方式配置为支持特定产品和交货地址。</span><span class="sxs-lookup"><span data-stu-id="c79a6-118">Modes of delivery can be configured to support specific products and delivery addresses.</span></span> <span data-ttu-id="c79a6-119">如果一个产品和地址的组合可以接受某种交货方式，但是另一个所选产品和地址的组合不能接受该交货方式，则该交货方式不可用。</span><span class="sxs-lookup"><span data-stu-id="c79a6-119">If there is a mode of delivery that is acceptable for one product and address combination but is not acceptable for another selected product and address combination, the mode of delivery is not available.</span></span> <span data-ttu-id="c79a6-120">如果要为一个产品选择另一个产品不支持的交货方式，可能需要逐一选择行，并分别更改各行的交货方式。</span><span class="sxs-lookup"><span data-stu-id="c79a6-120">You may need to select lines one by one and change the mode of delivery for each line separately if you want to select a mode of delivery for one product that is not supported by another product.</span></span>  

<span data-ttu-id="c79a6-121">选择新交货方式之后，将显示交易记录页。</span><span class="sxs-lookup"><span data-stu-id="c79a6-121">After you select the new mode of delivery, the transaction page is displayed.</span></span> <span data-ttu-id="c79a6-122">若要查看新交货方式的选择情况，请选择交易记录列表中的 **交货** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="c79a6-122">To review your new delivery mode selections, select the **Delivery** tab on the transaction list.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c79a6-123">其他资源</span><span class="sxs-lookup"><span data-stu-id="c79a6-123">Additional resources</span></span>

[<span data-ttu-id="c79a6-124">创建呼叫中心订单</span><span class="sxs-lookup"><span data-stu-id="c79a6-124">Create call center orders</span></span>](tasks/create-call-center-orders.md)

[<span data-ttu-id="c79a6-125">按交货模式自定义事务电子邮件</span><span class="sxs-lookup"><span data-stu-id="c79a6-125">Customize transactional emails by mode of delivery</span></span>](customize-email-delivery-mode.md)

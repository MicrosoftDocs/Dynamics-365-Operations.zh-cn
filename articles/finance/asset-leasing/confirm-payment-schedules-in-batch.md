---
title: 批量确认资产租赁付款计划
description: 本主题说明如何批量确认多个付款计划。
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0275fda306a58159a982b342622b9b6a18fa5b71
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225505"
---
# <a name="confirm-asset-leasing-payment-schedules-in-a-batch"></a><span data-ttu-id="f9dfe-103">批量确认资产租赁付款计划</span><span class="sxs-lookup"><span data-stu-id="f9dfe-103">Confirm Asset leasing payment schedules in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f9dfe-104">本主题说明如何批量确认多个付款计划。</span><span class="sxs-lookup"><span data-stu-id="f9dfe-104">This topic explains how to confirm multiple payment schedules in a batch.</span></span> <span data-ttu-id="f9dfe-105">付款计划可以逐个租赁进行确认，也可以通过确认批处理流程进行确认。</span><span class="sxs-lookup"><span data-stu-id="f9dfe-105">Payment schedules are confirmed either on a lease-to-lease basis or through the confirmation batch process.</span></span> <span data-ttu-id="f9dfe-106">只能针对其付款计划已确认的租赁过帐日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="f9dfe-106">A journal entry can be posted only against a lease that has a confirmed payment schedule.</span></span> <span data-ttu-id="f9dfe-107">确认付款计划是对租赁财务信息的最终批准。</span><span class="sxs-lookup"><span data-stu-id="f9dfe-107">Confirmation of the payment schedule serves as a final approval of the financial information for the lease.</span></span> <span data-ttu-id="f9dfe-108">对租赁财务信息的所有未来更改（例如付款和租赁期）均构成租赁调整，应以这种方式进行处理。</span><span class="sxs-lookup"><span data-stu-id="f9dfe-108">All future changes to the financial information for the lease, such as payments and the lease term, constitute a lease adjustment and should be processed in that way.</span></span>

<span data-ttu-id="f9dfe-109">要确认多个付款计划，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="f9dfe-109">To confirm multiple payment schedules, follow these steps.</span></span>

1. <span data-ttu-id="f9dfe-110">转到 **资产租赁 \> 定期 \> 批量确认**。</span><span class="sxs-lookup"><span data-stu-id="f9dfe-110">Go to **Asset leasing \> Periodic \> Confirmation batch**.</span></span>
2. <span data-ttu-id="f9dfe-111">在 **批量确认** 页面上，选择 **批量确认**。</span><span class="sxs-lookup"><span data-stu-id="f9dfe-111">On the **Confirmation batch** page, select **Confirmation batch**.</span></span>
3. <span data-ttu-id="f9dfe-112">在出现的对话框中，筛选以找到要确认的帐簿。</span><span class="sxs-lookup"><span data-stu-id="f9dfe-112">In the dialog box that appears, filter for the books that you want to confirm.</span></span>

    - <span data-ttu-id="f9dfe-113">要确认特定租赁组中的所有帐簿，请在 **租赁组** 字段中选择该组。</span><span class="sxs-lookup"><span data-stu-id="f9dfe-113">To confirm all the books in a specific lease group, select the group in the **Lease group** field.</span></span>
    - <span data-ttu-id="f9dfe-114">要确认特定帐簿，请在 **帐簿 ID** 字段中选择该帐簿。</span><span class="sxs-lookup"><span data-stu-id="f9dfe-114">To confirm specific books, select the books in the **Book ID** field.</span></span>
    - <span data-ttu-id="f9dfe-115">要确认所有帐簿，请打开 **所有帐簿** 参数。</span><span class="sxs-lookup"><span data-stu-id="f9dfe-115">To confirm all books, turn on the **For all books** parameter.</span></span>

<span data-ttu-id="f9dfe-116">**已确认帐簿** 页面中将显示新确认的帐簿的信息。</span><span class="sxs-lookup"><span data-stu-id="f9dfe-116">Information for the newly confirmed books is shown on the **Confirmed books** page.</span></span> <span data-ttu-id="f9dfe-117">确认付款计划后，可以针对租赁过帐初始确认日记帐。</span><span class="sxs-lookup"><span data-stu-id="f9dfe-117">After the payment schedules are confirmed, the initial recognition journal entries can be posted against the leases.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
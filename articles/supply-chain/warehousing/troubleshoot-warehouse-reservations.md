---
title: 仓库管理中的预留疑难解答
description: 此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中处理仓库预留时可能遇到的常见问题。
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d0d73396772ed9e8397797d6685fb550d911303b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828098"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a><span data-ttu-id="88979-103">仓库管理中的预留疑难解答</span><span class="sxs-lookup"><span data-stu-id="88979-103">Troubleshoot reservations in warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="88979-104">此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中处理仓库预留时可能遇到的常见问题。</span><span class="sxs-lookup"><span data-stu-id="88979-104">This topic describes how to fix common issues that you might encounter while you work with warehouse reservations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="88979-105">有关与批号和序列号登记相关的主题，请参阅[仓库批次和序列预留层次结构故障排除](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md)。</span><span class="sxs-lookup"><span data-stu-id="88979-105">For topics that are related to batch and serial number registrations, see [Troubleshoot warehouse batch and serial reservation hierarchies](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md).</span></span>

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a><span data-ttu-id="88979-106">我收到以下错误消息：“已创建了依赖预留的工作，因此无法删除这些预留。”</span><span class="sxs-lookup"><span data-stu-id="88979-106">I receive the following error message: "Reservations cannot be removed because there is work created which relies on the reservations."</span></span>

### <a name="issue-description"></a><span data-ttu-id="88979-107">问题描述</span><span class="sxs-lookup"><span data-stu-id="88979-107">Issue description</span></span>

<span data-ttu-id="88979-108">您不能在销售行上取消库存的预留，因为该行有未结工作。</span><span class="sxs-lookup"><span data-stu-id="88979-108">You can't unreserve inventory on a sales line, because there is open work against the line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="88979-109">解决问题</span><span class="sxs-lookup"><span data-stu-id="88979-109">Issue resolution</span></span>

<span data-ttu-id="88979-110">调查是否存在要将物料从装箱工作站运送到另一个位置（如 *货架门*）的未结包装组工作。</span><span class="sxs-lookup"><span data-stu-id="88979-110">Investigate whether open packing group work exists to bring the item from a packing station to another location (such as *Baydoor*).</span></span> <span data-ttu-id="88979-111">查看 **工作创建历史记录日志** 和 **工作详细信息** 页的记录，确定哪个工作在实际预留库存，然后完成或删除工作，释放预留。</span><span class="sxs-lookup"><span data-stu-id="88979-111">Review the records on the **Work creation history log** and **Work details** pages to determine what is physically reserving the inventory, and then complete or delete the work to free up the reservation.</span></span>

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a><span data-ttu-id="88979-112">我收到以下错误消息：“库存数量 -%1 由于物料 %2 的库存交易不足无法更新....”</span><span class="sxs-lookup"><span data-stu-id="88979-112">I receive the following error message: "Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2...."</span></span>

### <a name="issue-description"></a><span data-ttu-id="88979-113">问题描述</span><span class="sxs-lookup"><span data-stu-id="88979-113">Issue description</span></span>

<span data-ttu-id="88979-114">如果系统由于没有足够的具有指定维度的库存交易而无法更新库存数量，则可能发生此问题。</span><span class="sxs-lookup"><span data-stu-id="88979-114">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="88979-115">以下是完整错误消息的完整文本：</span><span class="sxs-lookup"><span data-stu-id="88979-115">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="88979-116">库存数量 -%1 由于批次 ID %12 上的物料 %2（维度为尺寸=%3、颜色=%4、附加物=%5、站点%6、仓库=%7、位置=%8、库存状态=可用、牌照=%9、引用 ID %11 的批处理号=%10）的库存交易不足无法更新。</span><span class="sxs-lookup"><span data-stu-id="88979-116">Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2 with dimensions Size=%3, Color=%4, Additions=%5, Site=%6, Warehouse=%7, Location=%8, Inventory status=Available, License plate=%9, Batch number=%10 for reference ID %11 on Lot ID %12.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="88979-117">解决问题</span><span class="sxs-lookup"><span data-stu-id="88979-117">Issue resolution</span></span>

<span data-ttu-id="88979-118">请确保没有库存交易在实际预留数量。</span><span class="sxs-lookup"><span data-stu-id="88979-118">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="88979-119">例如，这些交易可能会打开质量订单、库存锁定记录或输出订单。</span><span class="sxs-lookup"><span data-stu-id="88979-119">For example, these transactions might open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a><span data-ttu-id="88979-120">我收到以下错误消息：“实际现有量...无法预留，因为库存中只有 0.00。”</span><span class="sxs-lookup"><span data-stu-id="88979-120">I receive the following error message: "Physical on-hand...cannot be reserved because only 0.00 are available in the inventory."</span></span>

### <a name="issue-description"></a><span data-ttu-id="88979-121">问题描述</span><span class="sxs-lookup"><span data-stu-id="88979-121">Issue description</span></span>

<span data-ttu-id="88979-122">如果系统由于没有足够的具有指定维度的库存交易而无法更新库存数量，则可能发生此问题。</span><span class="sxs-lookup"><span data-stu-id="88979-122">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="88979-123">以下是完整错误消息的完整文本：</span><span class="sxs-lookup"><span data-stu-id="88979-123">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="88979-124">实际现有量站点=%1、仓库=%2、库存状态=可用、批处理号=%3、所有者=%4：%5 无法预留，因为库存中只有 0.00。</span><span class="sxs-lookup"><span data-stu-id="88979-124">Physical on-hand Site=%1, Warehouse=%2, Inventory status=Available, Batch number=%3, Owner=%4: %5 cannot be reserved because only 0.00 are available in the inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="88979-125">解决问题</span><span class="sxs-lookup"><span data-stu-id="88979-125">Issue resolution</span></span>

<span data-ttu-id="88979-126">此问题可能是由于未结工作引起的。</span><span class="sxs-lookup"><span data-stu-id="88979-126">This issue is probably caused by open work.</span></span> <span data-ttu-id="88979-127">请完成工作或在不创建工作时接收。</span><span class="sxs-lookup"><span data-stu-id="88979-127">Either complete the work or receive without work creation.</span></span> <span data-ttu-id="88979-128">请确保没有库存交易在实际预留数量。</span><span class="sxs-lookup"><span data-stu-id="88979-128">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="88979-129">例如，这些交易可能会打开质量订单、库存锁定记录或输出订单。</span><span class="sxs-lookup"><span data-stu-id="88979-129">For example, these transactions might be open quality orders, inventory blocking records, or output orders.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

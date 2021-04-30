---
title: 创建租赁组
description: 本主题说明如何设置租赁组。 需要租赁组才能创建建新租赁。
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseGroupTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 88a49e4db868078fd05875df33ca5727363aaa18
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881220"
---
# <a name="create-a-lease-group"></a><span data-ttu-id="d7ebc-104">创建租赁组</span><span class="sxs-lookup"><span data-stu-id="d7ebc-104">Create a lease group</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d7ebc-105">本主题说明如何设置租赁组。</span><span class="sxs-lookup"><span data-stu-id="d7ebc-105">This topic explains how to set up lease groups.</span></span> <span data-ttu-id="d7ebc-106">需要租赁组才能创建建新租赁。</span><span class="sxs-lookup"><span data-stu-id="d7ebc-106">Lease groups are required to create new leases.</span></span> <span data-ttu-id="d7ebc-107">租赁帐簿与每个租赁组关联。</span><span class="sxs-lookup"><span data-stu-id="d7ebc-107">Lease books are associated with each lease group.</span></span> <span data-ttu-id="d7ebc-108">租赁帐簿确定必须为每个租赁创建的默认帐簿。</span><span class="sxs-lookup"><span data-stu-id="d7ebc-108">Lease books determine the default books that must be created for each lease.</span></span> <span data-ttu-id="d7ebc-109">您可以在 **租赁过帐参数** 页上将特定科目分配给租赁组。</span><span class="sxs-lookup"><span data-stu-id="d7ebc-109">You can assign specific accounts to a lease group on the **Lease posting parameters** page.</span></span>

## <a name="create-a-lease-book-and-add-a-lease-group"></a><span data-ttu-id="d7ebc-110">创建租赁帐簿和添加租赁组</span><span class="sxs-lookup"><span data-stu-id="d7ebc-110">Create a lease book and add a lease group</span></span>

1. <span data-ttu-id="d7ebc-111">转到 **资产租赁 \> 设置 \> 租赁组**。</span><span class="sxs-lookup"><span data-stu-id="d7ebc-111">Go to **Asset leasing \> Setup \> Lease groups**.</span></span>
2. <span data-ttu-id="d7ebc-112">在操作窗格中，选择 **新建** 添加租赁组。</span><span class="sxs-lookup"><span data-stu-id="d7ebc-112">On the Action Pane, select **New** to add a lease group.</span></span> <span data-ttu-id="d7ebc-113">将向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="d7ebc-113">A line is added to the grid.</span></span>
3. <span data-ttu-id="d7ebc-114">在新行的 **租赁组** 字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="d7ebc-114">On the new line, in the **Lease group** field, enter a value.</span></span>
4. <span data-ttu-id="d7ebc-115">在 **描述** 字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="d7ebc-115">In the **Description** field, enter a value.</span></span>

<span data-ttu-id="d7ebc-116">将把您刚才输入的信息添加到 **添加租赁** 页上的 **租赁组** 字段中。</span><span class="sxs-lookup"><span data-stu-id="d7ebc-116">The information that you just entered is added to the **Lease group** field on the **Add lease** page.</span></span>

## <a name="associate-a-book-with-a-lease-group"></a><span data-ttu-id="d7ebc-117">将帐簿与租赁组关联</span><span class="sxs-lookup"><span data-stu-id="d7ebc-117">Associate a book with a lease group</span></span>

<span data-ttu-id="d7ebc-118">创建租赁组后，可以为每个组分配帐簿。</span><span class="sxs-lookup"><span data-stu-id="d7ebc-118">After you create lease groups, you can assign books to each group.</span></span> <span data-ttu-id="d7ebc-119">创建租赁并将其分配给租赁组时，系统会为与该租赁组关联的每本帐簿创建一组计划。</span><span class="sxs-lookup"><span data-stu-id="d7ebc-119">When you create a lease and assign it to a lease group, the system creates a set of schedules for each book that is associated with that lease group.</span></span>

> [!NOTE]
> <span data-ttu-id="d7ebc-120">必须先设置帐簿，然后才能将它们分配给租赁组。</span><span class="sxs-lookup"><span data-stu-id="d7ebc-120">Books must be set up before they can be assigned to a lease group.</span></span>

1. <span data-ttu-id="d7ebc-121">转到 **资产租赁 \> 设置 \> 租赁组**。</span><span class="sxs-lookup"><span data-stu-id="d7ebc-121">Go to **Asset leasing \> Setup \> Lease group**.</span></span>
2. <span data-ttu-id="d7ebc-122">选择一个租赁组，然后选择 **帐簿**。</span><span class="sxs-lookup"><span data-stu-id="d7ebc-122">Select a lease group, and then select **Books**.</span></span>
3. <span data-ttu-id="d7ebc-123">选择 **新建**，然后在 **帐簿类型** 字段中，选择要分配给租赁组的帐簿。</span><span class="sxs-lookup"><span data-stu-id="d7ebc-123">Select **New**, and then, in the **Book type** field, select the book to assign to the lease group.</span></span> <span data-ttu-id="d7ebc-124">如果必须以不同的方式核算租赁，则可以为一个租赁组分配多个帐簿。</span><span class="sxs-lookup"><span data-stu-id="d7ebc-124">You can assign multiple books to a lease group if a lease must be accounted for in different ways.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

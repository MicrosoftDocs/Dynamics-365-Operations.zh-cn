---
title: 添加位置与当事方关系类型
description: 本主题介绍如何添加新的位置与当事方关系类型。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-05-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 8c359c5c33bed5b5abe7fc0c8e362c3399e9051a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176650"
---
# <a name="add-location-roles-and-party-relationship-types"></a><span data-ttu-id="1beab-103">添加位置角色和当事方关系类型</span><span class="sxs-lookup"><span data-stu-id="1beab-103">Add location roles and party relationship types</span></span> 

[!include [banner](../includes/banner.md)]

## <a name="add-location-roles"></a><span data-ttu-id="1beab-104">添加位置角色</span><span class="sxs-lookup"><span data-stu-id="1beab-104">Add location roles</span></span>

<span data-ttu-id="1beab-105">可通过两种方法为地址和联系人信息添加新的位置角色：</span><span class="sxs-lookup"><span data-stu-id="1beab-105">There are two ways to add a new location roles for address and contact information:</span></span>

-  <span data-ttu-id="1beab-106">通过**地址和联系信息目的**页添加。</span><span class="sxs-lookup"><span data-stu-id="1beab-106">Add it through the **Address and contact information purpose** page.</span></span> <span data-ttu-id="1beab-107">新角色将保存到 **LogisticsLocationRole** 表，其类型为 = 0，表示该角色不是在 **LogisticsLocationRoleType** 枚举及其扩展中定义的系统角色。</span><span class="sxs-lookup"><span data-stu-id="1beab-107">The new role will be saved to the **LogisticsLocationRole** table with type = 0, which indicates that the role is not a system role defined in the **LogisticsLocationRoleType** enum and its extensions.</span></span> <span data-ttu-id="1beab-108">用户可以在创建地址或联系人信息时使用此角色。</span><span class="sxs-lookup"><span data-stu-id="1beab-108">A user will be able to use this role when creating address or contact information.</span></span>

    ![地址和内容信息目的](media/Address-Contact.PNG)

-  <span data-ttu-id="1beab-110">将其添加到 **LogisticsLocationRoleType** 枚举扩展，并通过数据库同步过程对其进行填充。</span><span class="sxs-lookup"><span data-stu-id="1beab-110">Add it to the **LogisticsLocationRoleType** enum extension, and let it populate through the database sync process.</span></span>

    1.  <span data-ttu-id="1beab-111">创建 **LogisticsLocationRoleType** 枚举的扩展，并在该扩展中添加新角色。</span><span class="sxs-lookup"><span data-stu-id="1beab-111">Create an extension to the **LogisticsLocationRoleType** enum and add the new role in the extension.</span></span> 
  
        ![LogisticsLocationRoleType](media/Logistics.PNG)

    2. <span data-ttu-id="1beab-113">为新角色创建新的资源文件，然后为其属性分配值。</span><span class="sxs-lookup"><span data-stu-id="1beab-113">Create a new resource file for the new role, and then assign a value for its properties.</span></span>
     
     ![新的资源文件](media/Resource.PNG)
        
    3.  <span data-ttu-id="1beab-115">创建数据填充类并提供处理程序方法以填充新角色。</span><span class="sxs-lookup"><span data-stu-id="1beab-115">Create a data population class and provide a handler method to populate the new role.</span></span> 

        ![数据填充](media/Dirdata.PNG)

    4.  <span data-ttu-id="1beab-117">若要测试填充新位置角色，可创建一个可运行的类，然后在 Main() 中调用 DirDataPopulation::insertLogisticsLocationRoles()。</span><span class="sxs-lookup"><span data-stu-id="1beab-117">To test populating the new location role, you can create a runnable class, and call DirDataPopulation::insertLogisticsLocationRoles() in Main().</span></span> <span data-ttu-id="1beab-118">此过程完成后，应该可以在 **LogisticsLocationRole** 表中看到填充的新角色，其类型为 \> 0。</span><span class="sxs-lookup"><span data-stu-id="1beab-118">After this process is complete, you should see the new role populated in the **LogisticsLocationRole** table with type \> 0.</span></span> <span data-ttu-id="1beab-119">这个新角色将在**地址和联系信息目的**页中显示。</span><span class="sxs-lookup"><span data-stu-id="1beab-119">The new role will display on the **Address and contact information purpose** page.</span></span>

        ![插入新位置](media/InsertNewLocation.PNG)

## <a name="add-party-relationship-types"></a><span data-ttu-id="1beab-121">添加当事方关系类型</span><span class="sxs-lookup"><span data-stu-id="1beab-121">Add party relationship types</span></span> 

<span data-ttu-id="1beab-122">可通过两种方法添加新关系类型。</span><span class="sxs-lookup"><span data-stu-id="1beab-122">There are two ways to add a new relationship type:</span></span>

-   <span data-ttu-id="1beab-123">通过**关系类型**页添加。</span><span class="sxs-lookup"><span data-stu-id="1beab-123">Add it through the **Relationship types** page.</span></span> <span data-ttu-id="1beab-124">新关系将保存到 **DirRelationshipTypeTable**，并且其 systemtype = 0。</span><span class="sxs-lookup"><span data-stu-id="1beab-124">The new relationship will be saved to **DirRelationshipTypeTable** with systemtype = 0.</span></span>

    ![关系类型](media/Relationship.PNG)

-  <span data-ttu-id="1beab-126">将其添加到 **DirSystemRelationshipType** 枚举的扩展，并通过数据库同步过程对其进行填充。</span><span class="sxs-lookup"><span data-stu-id="1beab-126">Add it to the extension of the **DirSystemRelationshipType** enum, and let it populate through database sync process.</span></span>

    1.  <span data-ttu-id="1beab-127">创建 **DirSystemRelationshipType** 枚举的扩展，然后添加新关系类型。</span><span class="sxs-lookup"><span data-stu-id="1beab-127">Create an extension to the **DirSystemRelationshipType** enum and add the new relationship type.</span></span>

    2. <span data-ttu-id="1beab-128">为这个新类型创建初始值设定项。</span><span class="sxs-lookup"><span data-stu-id="1beab-128">Create an initializer for this new type.</span></span> <span data-ttu-id="1beab-129">核心代码中包含多个示例，其中一个为 **DirRelationshipTypeChildInitialize**。</span><span class="sxs-lookup"><span data-stu-id="1beab-129">You can find several examples in the core code, one of them is  **DirRelationshipTypeChildInitialize**.</span></span> <span data-ttu-id="1beab-130">这是当事方关系类型“Child”的一个初始值设定项类。</span><span class="sxs-lookup"><span data-stu-id="1beab-130">This is an initializer class for party relationship type “Child”.</span></span> <span data-ttu-id="1beab-131">可通过复制并粘贴此代码，然后更新突出显示的区域，开始处理初始值设定项。</span><span class="sxs-lookup"><span data-stu-id="1beab-131">You can start with your initializer by copying and pasting this code and then update the highlighted areas.</span></span>
    
    ![DirRelationshipChild](media/DirRelationship.PNG)

    3.  <span data-ttu-id="1beab-133">若要测试填充新关系类型，可创建一个可运行的类，然后在 Main() 中调用 DirDataPopulation::insertDirRelationshipTypes()。</span><span class="sxs-lookup"><span data-stu-id="1beab-133">To test populating the new relationship type, you can create a runnable class, and call DirDataPopulation::insertDirRelationshipTypes() in Main().</span></span> <span data-ttu-id="1beab-134">应该会在 **DirRelationshipTypeTable** 中看到这个新关系类型，而整个新关系类型也会出现在**关系类型**页中。</span><span class="sxs-lookup"><span data-stu-id="1beab-134">You should see the new relationship type in the **DirRelationshipTypeTable**, and the new relationship type will be available on the **Relationship types** page.</span></span>

        ![可运行的类](media/Runnable.PNG)

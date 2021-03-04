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
ms.openlocfilehash: e38d0bd75ad865b7885182f798beb43551576beb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440783"
---
# <a name="add-location-and-party-relationship-types"></a>添加位置与当事方关系类型 

[!include [banner](../includes/banner.md)]

## <a name="add-location-roles"></a>添加位置角色

可通过两种方法为地址和联系人信息添加新的位置角色：

-  通过 **地址和联系信息目的** 页添加。 新角色将保存到 **LogisticsLocationRole** 表，其类型为 = 0，表示该角色不是在 **LogisticsLocationRoleType** 枚举及其扩展中定义的系统角色。 用户可以在创建地址或联系人信息时使用此角色。

    ![地址和内容信息目的](media/Address-Contact.PNG)

-  将其添加到 **LogisticsLocationRoleType** 枚举扩展，并通过数据库同步过程对其进行填充。

    1.  创建 **LogisticsLocationRoleType** 枚举的扩展，并在该扩展中添加新角色。 
  
        ![LogisticsLocationRoleType 枚举扩展](media/Logistics.PNG)

    2. 为新角色创建新的资源文件，然后为其属性分配值。
     
     ![新的资源文件](media/Resource.PNG)
        
    3.  创建数据填充类并提供处理程序方法以填充新角色。 

        ![数据填充](media/Dirdata.PNG)

    4.  若要测试填充新位置角色，可创建一个可运行的类，然后在 Main() 中调用 DirDataPopulation::insertLogisticsLocationRoles()。 此过程完成后，应该可以在 **LogisticsLocationRole** 表中看到填充的新角色，其类型为 \> 0。 这个新角色将在 **地址和联系信息目的** 页中显示。

        ![插入新位置](media/InsertNewLocation.PNG)

## <a name="add-party-relationship-types"></a>添加当事方关系类型 

可通过两种方法添加新关系类型。

-   通过 **关系类型** 页添加。 新关系将保存到 **DirRelationshipTypeTable**，并且其 systemtype = 0。

    ![关系类型](media/Relationship.PNG)

-  将其添加到 **DirSystemRelationshipType** 枚举的扩展，并通过数据库同步过程对其进行填充。

    1.  创建 **DirSystemRelationshipType** 枚举的扩展，然后添加新关系类型。

    2. 为这个新类型创建初始值设定项。 核心代码中包含多个示例，其中一个为 **DirRelationshipTypeChildInitialize**。 这是当事方关系类型“Child”的一个初始值设定项类。 可通过复制并粘贴此代码，然后更新突出显示的区域，开始处理初始值设定项。
    
    ![DirRelationshipChild 初始化器](media/DirRelationship.PNG)

    3.  若要测试填充新关系类型，可创建一个可运行的类，然后在 Main() 中调用 DirDataPopulation::insertDirRelationshipTypes()。 应该会在 **DirRelationshipTypeTable** 中看到这个新关系类型，而整个新关系类型也会出现在 **关系类型** 页中。

        ![可运行的类](media/Runnable.PNG)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
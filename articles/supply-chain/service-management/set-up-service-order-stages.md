---
title: 设置服务订单阶段
description: 设置服务订单阶段。
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 86d60a67b60b1bd3a13666b35f729f88ecfee3d3
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3984863"
---
# <a name="set-up-service-order-stages"></a><span data-ttu-id="bfb49-103">设置服务订单阶段</span><span class="sxs-lookup"><span data-stu-id="bfb49-103">Set up service order stages</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="bfb49-104">单击**服务管理** \> **设置** \> **服务订单** \> **服务阶段**。</span><span class="sxs-lookup"><span data-stu-id="bfb49-104">Click **Service management** \> **Setup** \> **Service orders** \> **Service stages**.</span></span>

2.  <span data-ttu-id="bfb49-105">按 Ctrl+N 创建一条新记录。</span><span class="sxs-lookup"><span data-stu-id="bfb49-105">Press CTRL+N to create a new record.</span></span>

3.  <span data-ttu-id="bfb49-106">在**服务阶段**和**说明**字段中，指定服务阶段 ID 和描述。</span><span class="sxs-lookup"><span data-stu-id="bfb49-106">In the **Service stage** and **Description** fields, specify a service stage ID and description.</span></span>

4.  <span data-ttu-id="bfb49-107">为该阶段选择适当的参数。</span><span class="sxs-lookup"><span data-stu-id="bfb49-107">Select the appropriate parameters for the stage.</span></span>

5.  <span data-ttu-id="bfb49-108">为当前阶段选择父阶段；如果该阶段是阶段设置中的初始阶段，则将**父**字段保留为空。</span><span class="sxs-lookup"><span data-stu-id="bfb49-108">Select the parent stage for the current stage or leave the **Parent** field blank if the stage is the initial stage in the stage setup.</span></span>


> [!NOTE]
> <P><span data-ttu-id="bfb49-109">在您保存了该阶段后，您不能修改<STRONG>父</STRONG>字段。</span><span class="sxs-lookup"><span data-stu-id="bfb49-109">You cannot modify the <STRONG>Parent</STRONG> field after you save the stage.</span></span> <span data-ttu-id="bfb49-110">而是可以删除该记录，然后在<STRONG>父</STRONG>字段中使用不同的选择再次创建该记录。</span><span class="sxs-lookup"><span data-stu-id="bfb49-110">Instead, you can delete the record and create the record again with a different selection in the <STRONG>Parent</STRONG> field.</span></span></P>
> <P><span data-ttu-id="bfb49-111">此外，您只能使用空白<STRONG>父</STRONG>字段创建一个阶段。</span><span class="sxs-lookup"><span data-stu-id="bfb49-111">Also, you can only create one stage with a blank <STRONG>Parent</STRONG> field.</span></span> <span data-ttu-id="bfb49-112">也就是说，只运行一个初始阶段。</span><span class="sxs-lookup"><span data-stu-id="bfb49-112">That is, only one initial stage is permitted.</span></span></P>


  



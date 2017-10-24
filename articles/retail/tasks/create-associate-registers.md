--- 
title: "创建和关联收银机"
description: "此过程演示如何创建销售点 (POS) 收银机。"
author: rubencdelgado
manager: AnnBe
ms.date: 10/05/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6a95019e50bcc060165dab3e6aa2b3ca8a897bf3
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-associate-registers"></a><span data-ttu-id="e4e6b-103">创建和关联收银机</span><span class="sxs-lookup"><span data-stu-id="e4e6b-103">Create and associate registers</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="e4e6b-104">此过程演示如何创建销售点 (POS) 收银机。</span><span class="sxs-lookup"><span data-stu-id="e4e6b-104">This procedure demonstrates how to create a point of sale (POS) register.</span></span> <span data-ttu-id="e4e6b-105">此过程使用了演示数据公司 USRT。</span><span class="sxs-lookup"><span data-stu-id="e4e6b-105">This procedure uses the demo data company USRT.</span></span>

1. <span data-ttu-id="e4e6b-106">转至“零售和商业”>“渠道设置”>“POS 设置”>“收银机”。</span><span class="sxs-lookup"><span data-stu-id="e4e6b-106">Go to Retail and commerce > Channel setup > POS setup > Registers.</span></span>
2. <span data-ttu-id="e4e6b-107">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="e4e6b-107">Click New.</span></span>
3. <span data-ttu-id="e4e6b-108">在“收银机编号”字段中，键入新收银机的编号。</span><span class="sxs-lookup"><span data-stu-id="e4e6b-108">In the Register number field, type an ID for the new register.</span></span>
    * <span data-ttu-id="e4e6b-109">收银机 ID 中通常包含有助于将收银机映射到其所属商店的代码，以及商店内的位置。</span><span class="sxs-lookup"><span data-stu-id="e4e6b-109">The register ID typically includes codes that help map the register to the store to which it belongs, and the location within the store.</span></span>  
4. <span data-ttu-id="e4e6b-110">在“名称”字段中，键入收银机的描述性名称。</span><span class="sxs-lookup"><span data-stu-id="e4e6b-110">In the Name field, type a descriptive name for the register..</span></span>
5. <span data-ttu-id="e4e6b-111">在“商店编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="e4e6b-111">In the Store number field, enter or select a value.</span></span>
6. <span data-ttu-id="e4e6b-112">在“硬件配置文件”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="e4e6b-112">In the Hardware profile field, enter or select a value.</span></span>
    * <span data-ttu-id="e4e6b-113">硬件配置文件用于指定将连接到收银机的零售外设，如银箱和收据打印机。</span><span class="sxs-lookup"><span data-stu-id="e4e6b-113">Hardware profiles are used to specify the retail peripherals that will be connected to the register, such as cash drawer and receipt printer.</span></span>  
7. <span data-ttu-id="e4e6b-114">在“可视化配置文件”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="e4e6b-114">In the Visual profile field, enter or select a value.</span></span>
    * <span data-ttu-id="e4e6b-115">可视化配置文件用于指定 POS 背景和登录页中使用的图像，以及 POS 的主题。</span><span class="sxs-lookup"><span data-stu-id="e4e6b-115">Visual profiles are used to specify the images used in the POS background and login page as well as themes for the POS.</span></span>  
8. <span data-ttu-id="e4e6b-116">在“EFT POS 收银机编号”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="e4e6b-116">In the EFT POS register number field, type a value.</span></span>
    * <span data-ttu-id="e4e6b-117">EFT POS 收银机编号用于通知付款处理器哪个终端在发送授权请求。</span><span class="sxs-lookup"><span data-stu-id="e4e6b-117">The EFT POS register number is used to inform the payment processor which payment terminal is sending authorization requests.</span></span> <span data-ttu-id="e4e6b-118">该值通常称为“终端 ID”或“TID”。</span><span class="sxs-lookup"><span data-stu-id="e4e6b-118">This value is often called the "Terminal ID" or “TID”.</span></span> <span data-ttu-id="e4e6b-119">TID 通常位于付款设备上的贴纸中。</span><span class="sxs-lookup"><span data-stu-id="e4e6b-119">The TID can generally be found on a sticker on the payment device.</span></span>  
9. <span data-ttu-id="e4e6b-120">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="e4e6b-120">Click Save.</span></span>


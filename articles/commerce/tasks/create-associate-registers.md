---
title: 创建和关联收银机
description: 此过程演示如何创建销售点 (POS) 收银机。
author: rubencdelgado
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af9743f17cebb3484c3ec5b0315347c575a474bd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246987"
---
# <a name="create-and-associate-registers"></a><span data-ttu-id="91e46-103">创建和关联收银机</span><span class="sxs-lookup"><span data-stu-id="91e46-103">Create and associate registers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="91e46-104">此过程演示如何创建销售点 (POS) 收银机。</span><span class="sxs-lookup"><span data-stu-id="91e46-104">This procedure demonstrates how to create a point of sale (POS) register.</span></span> <span data-ttu-id="91e46-105">此过程使用了演示数据公司 USRT。</span><span class="sxs-lookup"><span data-stu-id="91e46-105">This procedure uses the demo data company USRT.</span></span>

1. <span data-ttu-id="91e46-106">转至“Retail 和 Commerce”>“渠道设置”>“POS 设置”>“收银机”。</span><span class="sxs-lookup"><span data-stu-id="91e46-106">Go to Retail and Commerce > Channel setup > POS setup > Registers.</span></span>
2. <span data-ttu-id="91e46-107">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="91e46-107">Click New.</span></span>
3. <span data-ttu-id="91e46-108">在“收银机编号”字段中，键入新收银机的编号。</span><span class="sxs-lookup"><span data-stu-id="91e46-108">In the Register number field, type an ID for the new register.</span></span>
    * <span data-ttu-id="91e46-109">收银机 ID 中通常包含有助于将收银机映射到其所属商店的代码，以及商店内的位置。</span><span class="sxs-lookup"><span data-stu-id="91e46-109">The register ID typically includes codes that help map the register to the store to which it belongs, and the location within the store.</span></span>  
4. <span data-ttu-id="91e46-110">在“名称”字段中，键入收银机的描述性名称。</span><span class="sxs-lookup"><span data-stu-id="91e46-110">In the Name field, type a descriptive name for the register..</span></span>
5. <span data-ttu-id="91e46-111">在“商店编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="91e46-111">In the Store number field, enter or select a value.</span></span>
6. <span data-ttu-id="91e46-112">在“硬件配置文件”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="91e46-112">In the Hardware profile field, enter or select a value.</span></span>
    * <span data-ttu-id="91e46-113">硬件配置文件用于指定将连接到收银机的外设，如银箱和收据打印机。</span><span class="sxs-lookup"><span data-stu-id="91e46-113">Hardware profiles are used to specify the peripherals that will be connected to the register, such as cash drawer and receipt printer.</span></span>  
7. <span data-ttu-id="91e46-114">在“可视化配置文件”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="91e46-114">In the Visual profile field, enter or select a value.</span></span>
    * <span data-ttu-id="91e46-115">可视化配置文件用于指定 POS 背景和登录页中使用的图像，以及 POS 的主题。</span><span class="sxs-lookup"><span data-stu-id="91e46-115">Visual profiles are used to specify the images used in the POS background and login page as well as themes for the POS.</span></span>  
8. <span data-ttu-id="91e46-116">在“EFT POS 收银机编号”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="91e46-116">In the EFT POS register number field, type a value.</span></span>
    * <span data-ttu-id="91e46-117">EFT POS 收银机编号用于通知付款处理器哪个终端在发送授权请求。</span><span class="sxs-lookup"><span data-stu-id="91e46-117">The EFT POS register number is used to inform the payment processor which payment terminal is sending authorization requests.</span></span> <span data-ttu-id="91e46-118">该值通常称为“终端 ID”或“TID”。</span><span class="sxs-lookup"><span data-stu-id="91e46-118">This value is often called the "Terminal ID" or "TID".</span></span> <span data-ttu-id="91e46-119">TID 通常位于付款设备上的贴纸中。</span><span class="sxs-lookup"><span data-stu-id="91e46-119">The TID can generally be found on a sticker on the payment device.</span></span>  
9. <span data-ttu-id="91e46-120">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="91e46-120">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
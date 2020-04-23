---
title: 设置服务间隔
description: 服务间隔指示在您创建服务订单时为服务协议行创建服务订单行所采用的频率。
author: ShylaThompson
manager: tfehr
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementinterval
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a549b3add4a9d302d9f65e165c2ec7bdac95b698
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206764"
---
# <a name="set-up-service-intervals"></a><span data-ttu-id="0e959-103">设置服务间隔</span><span class="sxs-lookup"><span data-stu-id="0e959-103">Set up service intervals</span></span>  

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0e959-104">服务间隔指示在您创建服务订单时为服务协议行创建服务订单行所采用的频率。</span><span class="sxs-lookup"><span data-stu-id="0e959-104">Service interval indicates the frequency with which service order lines are created for service agreement lines when you create service orders.</span></span>

1. <span data-ttu-id="0e959-105">单击**服务管理** \> **设置** \> **服务协议** \> **服务间隔**。</span><span class="sxs-lookup"><span data-stu-id="0e959-105">Click **Service management** \> **Setup** \> **Service agreements** \> **Service intervals**.</span></span>
2. <span data-ttu-id="0e959-106">创建新的服务间隔。</span><span class="sxs-lookup"><span data-stu-id="0e959-106">Create a new service interval.</span></span>
3. <span data-ttu-id="0e959-107">输入 ID 和服务间隔的描述。</span><span class="sxs-lookup"><span data-stu-id="0e959-107">Enter the ID and description of the service interval.</span></span>
4. <span data-ttu-id="0e959-108">在**范围**字段中，选择范围。</span><span class="sxs-lookup"><span data-stu-id="0e959-108">In the **Range** field, select the range.</span></span>
5. <span data-ttu-id="0e959-109">在**频率**字段中，输入频率。</span><span class="sxs-lookup"><span data-stu-id="0e959-109">In the **Frequency** field, type the frequency.</span></span> <span data-ttu-id="0e959-110">必须将该频率作为系数与范围相乘，以获取服务协议间隔。</span><span class="sxs-lookup"><span data-stu-id="0e959-110">The frequency is the factor by which you must multiply the range to obtain the interval for a service agreement.</span></span>
6. <span data-ttu-id="0e959-111">按 **Alt+S** 保存服务间隔。</span><span class="sxs-lookup"><span data-stu-id="0e959-111">Press **Alt+S** to save the service interval.</span></span>

## <a name="example"></a><span data-ttu-id="0e959-112">示例</span><span class="sxs-lookup"><span data-stu-id="0e959-112">Example</span></span>

<span data-ttu-id="0e959-113">您要创建为期 10 天的服务间隔。</span><span class="sxs-lookup"><span data-stu-id="0e959-113">You want to create a service interval of 10 days.</span></span>

<span data-ttu-id="0e959-114">**创建 10 天的服务间隔**</span><span class="sxs-lookup"><span data-stu-id="0e959-114">**Create a 10-day service interval**</span></span>

1. <span data-ttu-id="0e959-115">单击**服务管理** \> **设置** \> **服务协议** \> **服务间隔**。</span><span class="sxs-lookup"><span data-stu-id="0e959-115">Click **Service management** \> **Setup** \> **Service agreements** \> **Service intervals**.</span></span>
2. <span data-ttu-id="0e959-116">创建新的服务间隔。</span><span class="sxs-lookup"><span data-stu-id="0e959-116">Create a new service interval.</span></span>
3. <span data-ttu-id="0e959-117">输入 ID 和服务间隔的描述。</span><span class="sxs-lookup"><span data-stu-id="0e959-117">Enter the ID and description of the service interval.</span></span>
4. <span data-ttu-id="0e959-118">在**范围**字段中，选择**每天**。</span><span class="sxs-lookup"><span data-stu-id="0e959-118">In the **Range** field, select **Daily**.</span></span>
5. <span data-ttu-id="0e959-119">在**频率**字段中键入 10。</span><span class="sxs-lookup"><span data-stu-id="0e959-119">In the **Frequency** field, type 10.</span></span>
6. <span data-ttu-id="0e959-120">按 **Alt+S** 保存服务间隔。</span><span class="sxs-lookup"><span data-stu-id="0e959-120">Press **Alt+S** to save the service interval.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e959-121">相关主题</span><span class="sxs-lookup"><span data-stu-id="0e959-121">Related topics</span></span>

[<span data-ttu-id="0e959-122">服务间隔</span><span class="sxs-lookup"><span data-stu-id="0e959-122">Service intervals</span></span>](service-intervals.md)  

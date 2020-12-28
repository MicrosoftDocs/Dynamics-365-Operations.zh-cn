---
title: 服务对象概览
description: 服务对象是您可以对其执行服务的客户的资产和产品。
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 29d2cf6a496fed8d9932d5c6d49f4560d7eabbbb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4422685"
---
# <a name="service-objects-overview"></a><span data-ttu-id="6f7a3-103">服务对象概览</span><span class="sxs-lookup"><span data-stu-id="6f7a3-103">Service objects overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f7a3-104">服务对象是您可以对其执行服务的客户的资产和产品。</span><span class="sxs-lookup"><span data-stu-id="6f7a3-104">Service objects are a customer’s assets and products for which you can perform a service.</span></span> <span data-ttu-id="6f7a3-105">根据您提供的服务类型，对象可以是有形对象或无形对象：</span><span class="sxs-lookup"><span data-stu-id="6f7a3-105">Depending on the type of service you provide, objects can be tangible or intangible:</span></span>

-  <span data-ttu-id="6f7a3-106">有形对象是您可对其执行实际服务任务的事物，例如机器或建筑物。</span><span class="sxs-lookup"><span data-stu-id="6f7a3-106">Tangible objects are things, such as a machine or a building, on which you can perform a physical service task.</span></span>

    <span data-ttu-id="6f7a3-107">有形服务对象还可以是您在“已发布产品详细信息”窗体中创建的库存物料。</span><span class="sxs-lookup"><span data-stu-id="6f7a3-107">A tangible service object can also be an inventory item that you create in the Released product details form.</span></span> <span data-ttu-id="6f7a3-108">根据您附加到该物料的库存维度组，您可以将服务对象创建为包括物料序列号的详细信息级别。</span><span class="sxs-lookup"><span data-stu-id="6f7a3-108">Depending on the inventory dimension group that you attach to the item, you can create a service object to a level of detail that includes the item serial number.</span></span> <span data-ttu-id="6f7a3-109">这在您必须跟踪服务对象表示的确切物料时非常有用。</span><span class="sxs-lookup"><span data-stu-id="6f7a3-109">This is useful when you must keep track of the exact item that the service object represents.</span></span>

    <span data-ttu-id="6f7a3-110">有形服务对象还可以是与公司的直接生产或供应链不直接相关的物料。</span><span class="sxs-lookup"><span data-stu-id="6f7a3-110">A tangible service object can also be an item that is not directly related to a company's direct production or supply chain.</span></span> <span data-ttu-id="6f7a3-111">例如，服务订单中所于维修的工具包可以是库存中不包括的服务对象。</span><span class="sxs-lookup"><span data-stu-id="6f7a3-111">For example, a tool kit that is used for repairs in a service order can be a service object that is not included in inventory.</span></span> <span data-ttu-id="6f7a3-112">在这种情况下，您不能将其登记为库存物料。</span><span class="sxs-lookup"><span data-stu-id="6f7a3-112">In this case, you don’t register it as an inventory item.</span></span>

-  <span data-ttu-id="6f7a3-113">无形对象是对其执行服务任务的抽象实体，例如一组帐户或法律文档。</span><span class="sxs-lookup"><span data-stu-id="6f7a3-113">Intangible objects are nonphysical things, such as a set of accounts or a legal document, on which you can perform a service task.</span></span>

## <a name="example-of-an-intangible-service-object"></a><span data-ttu-id="6f7a3-114">无形的服务对象的示例</span><span class="sxs-lookup"><span data-stu-id="6f7a3-114">Example of an intangible service object</span></span>

<span data-ttu-id="6f7a3-115">公司 A 维护多个小公司的财务记录。</span><span class="sxs-lookup"><span data-stu-id="6f7a3-115">Company A maintains the financial records for several small companies.</span></span> <span data-ttu-id="6f7a3-116">公司 A 的客户之一是当地的足球队，公司 A 每周对其进行记帐并且每年审计该俱乐部的帐户。</span><span class="sxs-lookup"><span data-stu-id="6f7a3-116">One of Company A's clients is the local football team, for which Company A does the weekly bookkeeping and annual audit of the club's accounts.</span></span> <span data-ttu-id="6f7a3-117">该俱乐部的帐户在“服务对象”窗体中设置，并且指定为服务协议中的对象。</span><span class="sxs-lookup"><span data-stu-id="6f7a3-117">The club's accounts are set up in the Service objects form and specified as the object in the service agreement.</span></span> <span data-ttu-id="6f7a3-118">对于该对象有两个服务协议行。</span><span class="sxs-lookup"><span data-stu-id="6f7a3-118">There are two service agreement lines for the object.</span></span> <span data-ttu-id="6f7a3-119">第 1 行是具有分配到行的每周间隔的每周记帐；第 2 行是具有分配到行的每年间隔的每年审计。</span><span class="sxs-lookup"><span data-stu-id="6f7a3-119">Line 1 is weekly bookkeeping with a weekly interval assigned to the line, and line 2 is the annual audit with a yearly interval assigned to it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6f7a3-120">相关主题</span><span class="sxs-lookup"><span data-stu-id="6f7a3-120">Related topics</span></span>

[<span data-ttu-id="6f7a3-121">创建服务对象</span><span class="sxs-lookup"><span data-stu-id="6f7a3-121">Create service objects</span></span>](create-service-objects.md)


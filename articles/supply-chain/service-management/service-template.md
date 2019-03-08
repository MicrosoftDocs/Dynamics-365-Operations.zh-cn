---
title: 服务模板
description: 您可以将某一服务协议定义为模板，并且以后将该模板上的行复制到其他服务协议或服务订单中。
author: ShylaThompson
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c4bde1869b2be6e4cbbf979dae1b84c2a4974a9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "327312"
---
# <a name="service-templates"></a><span data-ttu-id="6ea32-103">服务模板</span><span class="sxs-lookup"><span data-stu-id="6ea32-103">Service templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6ea32-104">您可以将某一服务协议定义为模板，并且以后将该模板上的行复制到其他服务协议或服务订单中。</span><span class="sxs-lookup"><span data-stu-id="6ea32-104">You can define a service agreement as a template and copy the lines of the template later into another service agreement or into a service order.</span></span>

## <a name="example"></a><span data-ttu-id="6ea32-105">示例</span><span class="sxs-lookup"><span data-stu-id="6ea32-105">Example</span></span>

<span data-ttu-id="6ea32-106">您向其提供服务的客户在 5 个不同的地点具有完全相同的服务电梯。</span><span class="sxs-lookup"><span data-stu-id="6ea32-106">A customer for whom you provide service has identical service elevators at five different locations.</span></span>

<span data-ttu-id="6ea32-107">您想要为该客户设置 5 个服务协议，每个站点一个。</span><span class="sxs-lookup"><span data-stu-id="6ea32-107">You want to set up five service agreements for the customer, one for each site.</span></span>
<span data-ttu-id="6ea32-108">为了减少重复性的设置工作，并且确保服务协议中的设置信息完全相同，您创建了一个服务协议，并且将该服务协议指定为用于电梯服务工作的模板。</span><span class="sxs-lookup"><span data-stu-id="6ea32-108">To limit repetitive setup work, and to make sure that the setup information in the service agreements is identical, you create a service agreement and specify it as a template for the service work on the elevators.</span></span>

<span data-ttu-id="6ea32-109">您现在可以将模板行复制到这 5 个新的服务协议中，以便每个服务协议都用来自该模板的行填充。</span><span class="sxs-lookup"><span data-stu-id="6ea32-109">You can now copy the template lines into the five new service agreements, so that each service agreement is populated with the lines from the template.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="6ea32-110">创建模板</span><span class="sxs-lookup"><span data-stu-id="6ea32-110">Create a template</span></span>

<span data-ttu-id="6ea32-111">在您创建服务模板时，创建一个服务协议，在该服务协议上创建所需行，然后将该服务协议附加到某一服务模板组。</span><span class="sxs-lookup"><span data-stu-id="6ea32-111">When you create a service template, you create a service agreement, create the required lines on it, and attach the service agreement to a service-template group.</span></span>

> [!NOTE]
> <span data-ttu-id="6ea32-112">只有当没有服务订单附加其上时，某一个服务协议才能定义为一个模板。</span><span class="sxs-lookup"><span data-stu-id="6ea32-112">A service agreement can be defined as a template only if it has no service orders attached to it.</span></span> <span data-ttu-id="6ea32-113">此外，不能从已定义为模板的服务协议生成服务订单。</span><span class="sxs-lookup"><span data-stu-id="6ea32-113">Also, no service orders can be generated from a service agreement that is defined as a template.</span></span>

## <a name="copy-template-lines"></a><span data-ttu-id="6ea32-114">复制模板行</span><span class="sxs-lookup"><span data-stu-id="6ea32-114">Copy template lines</span></span>

<span data-ttu-id="6ea32-115">您可以将模板行从一个服务模板复制到其他服务协议或服务订单中。</span><span class="sxs-lookup"><span data-stu-id="6ea32-115">You can copy template lines from a service template into another service agreement or into a service order.</span></span>

<span data-ttu-id="6ea32-116">在您将模板行复制到您的服务订单或服务协议中时，您的模板组将显示在一个树视图中，其中每个组都可以扩展。</span><span class="sxs-lookup"><span data-stu-id="6ea32-116">When you copy template lines into your service orders or service agreements, your template groups are displayed in a tree view in which each group can be expanded.</span></span> <span data-ttu-id="6ea32-117">通过此显示，您可以查看每个模板和模板行。</span><span class="sxs-lookup"><span data-stu-id="6ea32-117">This display lets you view each template and template line.</span></span>

<span data-ttu-id="6ea32-118">如果您已基于反映模板用途的名称对模板进行分组，则可以更容易地确定要复制哪些服务模板行。</span><span class="sxs-lookup"><span data-stu-id="6ea32-118">It is easier to determine the service-template lines that you want to copy if you have grouped the templates under names that reflect the use of the templates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ea32-119">相关主题</span><span class="sxs-lookup"><span data-stu-id="6ea32-119">Related topics</span></span>

[<span data-ttu-id="6ea32-120">复制服务模板行</span><span class="sxs-lookup"><span data-stu-id="6ea32-120">Copy service templates lines</span></span>](copy-service-template-lines.md)

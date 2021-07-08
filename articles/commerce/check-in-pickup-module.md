---
title: 提货登记模块
description: 此主题介绍提货登记模块，并说明如何在 Microsoft Dynamics 365 Commerce 中配置此模块。
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 0baa922afc72778dd6e4836398a280cbe6abaec2
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270575"
---
# <a name="check-in-for-pickup-module"></a><span data-ttu-id="e7dbd-103">提货登记模块</span><span class="sxs-lookup"><span data-stu-id="e7dbd-103">Check-in for pickup module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e7dbd-104">此主题介绍提货登记模块，并说明如何在 Microsoft Dynamics 365 Commerce 中配置此模块。</span><span class="sxs-lookup"><span data-stu-id="e7dbd-104">This topic covers the check-in for pickup module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e7dbd-105">提货登记模块为使用 Dynamics 365 Commerce 客户登记功能通知商店他们已到达的客户提供了一个确认页面。</span><span class="sxs-lookup"><span data-stu-id="e7dbd-105">The check-in for pickup module provides a confirmation page for customers who use the Dynamics 365 Commerce customer check-in capabilities to notify a store about their arrival.</span></span> <span data-ttu-id="e7dbd-106">提货登记模块还允许您配置一个窗体，来从客户那里收集其他信息，推进订单交付。</span><span class="sxs-lookup"><span data-stu-id="e7dbd-106">The check-in for pickup module also lets you configure a form that collects additional information from customers to facilitate order delivery.</span></span> <span data-ttu-id="e7dbd-107">这些信息包括客户的停车位号，以及其车辆的品牌和型号。</span><span class="sxs-lookup"><span data-stu-id="e7dbd-107">This information includes a customer's parking spot number, and the make and model of their vehicle.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="e7dbd-108">模块属性</span><span class="sxs-lookup"><span data-stu-id="e7dbd-108">Module properties</span></span>

| <span data-ttu-id="e7dbd-109">属性名称</span><span class="sxs-lookup"><span data-stu-id="e7dbd-109">Property name</span></span> | <span data-ttu-id="e7dbd-110">值</span><span class="sxs-lookup"><span data-stu-id="e7dbd-110">Values</span></span> | <span data-ttu-id="e7dbd-111">说明</span><span class="sxs-lookup"><span data-stu-id="e7dbd-111">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="e7dbd-112">确认文本</span><span class="sxs-lookup"><span data-stu-id="e7dbd-112">Confirmation text</span></span> | <span data-ttu-id="e7dbd-113">文本字符串</span><span class="sxs-lookup"><span data-stu-id="e7dbd-113">Text string</span></span> | <span data-ttu-id="e7dbd-114">登记确认页上显示的标题的内容。</span><span class="sxs-lookup"><span data-stu-id="e7dbd-114">Content for the heading that appears on the check-in confirmation page.</span></span> |
| <span data-ttu-id="e7dbd-115">显示 QR 码</span><span class="sxs-lookup"><span data-stu-id="e7dbd-115">Show QR code</span></span> | <span data-ttu-id="e7dbd-116">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="e7dbd-116">**True** or **False**</span></span> | <span data-ttu-id="e7dbd-117">当此属性设置为 **True** 时，登记确认页将显示代表订单确认 ID 的 QR 码。</span><span class="sxs-lookup"><span data-stu-id="e7dbd-117">When this property is set to **True**, the check-in confirmation page shows a QR code that represents the order confirmation ID.</span></span> |
| <span data-ttu-id="e7dbd-118">其他信息标题</span><span class="sxs-lookup"><span data-stu-id="e7dbd-118">Additional information heading</span></span> | <span data-ttu-id="e7dbd-119">文本字符串</span><span class="sxs-lookup"><span data-stu-id="e7dbd-119">Text string</span></span> | <span data-ttu-id="e7dbd-120">其他信息字段已配置时显示的标题的内容。</span><span class="sxs-lookup"><span data-stu-id="e7dbd-120">Content for the heading that appears when additional information fields have been configured.</span></span> |
| <span data-ttu-id="e7dbd-121">其他信息键</span><span class="sxs-lookup"><span data-stu-id="e7dbd-121">Additional information keys</span></span> | <span data-ttu-id="e7dbd-122">资源 ID/资源值对</span><span class="sxs-lookup"><span data-stu-id="e7dbd-122">Resource ID/resource value pair</span></span> | <span data-ttu-id="e7dbd-123">每个键将创建一个表单域和一个关联的标签，用于从客户那里收集其他信息。</span><span class="sxs-lookup"><span data-stu-id="e7dbd-123">Each key creates a form field and an associated label that are used to collect additional information from customers.</span></span> |
| <span data-ttu-id="e7dbd-124">其他信息键 \> 资源 ID</span><span class="sxs-lookup"><span data-stu-id="e7dbd-124">Additional information keys \> Resource ID</span></span> | <span data-ttu-id="e7dbd-125">文本字符串</span><span class="sxs-lookup"><span data-stu-id="e7dbd-125">Text string</span></span> | <span data-ttu-id="e7dbd-126">每个信息键将创建一个表单域和一个关联的标签，用于从客户那里收集其他信息。</span><span class="sxs-lookup"><span data-stu-id="e7dbd-126">Each information key creates a form field and an associated label that are used to collect additional information from customers.</span></span> <span data-ttu-id="e7dbd-127">此属性标识其他信息键。</span><span class="sxs-lookup"><span data-stu-id="e7dbd-127">This property identifies the additional information key.</span></span> <span data-ttu-id="e7dbd-128">在销售点 (POS) 创建的任务中，此属性的值在说明字段中显示为标签。</span><span class="sxs-lookup"><span data-stu-id="e7dbd-128">In the task that is created in point of sale (POS), the value of this property is shown as the label in the instructions field.</span></span> |
| <span data-ttu-id="e7dbd-129">其他信息键 \> 资源值</span><span class="sxs-lookup"><span data-stu-id="e7dbd-129">Additional information keys \> Resource value</span></span> | <span data-ttu-id="e7dbd-130">文本字符串</span><span class="sxs-lookup"><span data-stu-id="e7dbd-130">Text string</span></span> | <span data-ttu-id="e7dbd-131">POS 中的任务中文本字段的标签。</span><span class="sxs-lookup"><span data-stu-id="e7dbd-131">The label for the text field in the task in POS.</span></span> |
| <span data-ttu-id="e7dbd-132">其他信息键 \> 必填</span><span class="sxs-lookup"><span data-stu-id="e7dbd-132">Additional information keys \> Required</span></span> | <span data-ttu-id="e7dbd-133">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="e7dbd-133">**True** or **False**</span></span> | <span data-ttu-id="e7dbd-134">此属性指定客户是否必须先填写表单域才能继续。</span><span class="sxs-lookup"><span data-stu-id="e7dbd-134">This property specifies whether customers must fill in the form field before they can continue.</span></span> <span data-ttu-id="e7dbd-135">当此属性设置为 **True** 时，表单标签旁边将显示一个星号，将进行 null 检查来阻止客户继续（如果未输入任何值）。</span><span class="sxs-lookup"><span data-stu-id="e7dbd-135">When this property is set to **True**, an asterisk is rendered next to the form label, and a null check is done to prevent customers from continuing if no value is entered.</span></span> |

## <a name="add-the-check-in-for-pickup-module-to-a-page"></a><span data-ttu-id="e7dbd-136">将提货登记模块添加到页面</span><span class="sxs-lookup"><span data-stu-id="e7dbd-136">Add the check-in for pickup module to a page</span></span>

<span data-ttu-id="e7dbd-137">提货登记模块应添加到您创建的用于登记确认的新页面。</span><span class="sxs-lookup"><span data-stu-id="e7dbd-137">The check-in for pickup module should be added to the new page that you create for check-in confirmation.</span></span> <span data-ttu-id="e7dbd-138">该页面将作为在电子邮件中选择 **我在这里** 链接或按钮的客户的登记确认体验。</span><span class="sxs-lookup"><span data-stu-id="e7dbd-138">That page will serve as the check-in confirmation experience for customers who select the **I am here** link or button in their email.</span></span> 

## <a name="configure-the-additional-information-form"></a><span data-ttu-id="e7dbd-139">配置其他信息表单</span><span class="sxs-lookup"><span data-stu-id="e7dbd-139">Configure the additional information form</span></span>

<span data-ttu-id="e7dbd-140">默认情况下，如果未配置其他信息键，模块将向客户显示登记确认页。</span><span class="sxs-lookup"><span data-stu-id="e7dbd-140">By default, if no additional information keys are configured, the module shows customers the check-in confirmation page.</span></span> <span data-ttu-id="e7dbd-141">显示登记确认时，将在 POS 中为要提取订单的商店创建一个任务。</span><span class="sxs-lookup"><span data-stu-id="e7dbd-141">As the check-in confirmation is shown, a task is created in POS for the store where the order is being picked up.</span></span>

<span data-ttu-id="e7dbd-142">配置一个或多个其他信息键后，首先会提示客户输入信息。</span><span class="sxs-lookup"><span data-stu-id="e7dbd-142">When one or more additional information keys are configured, customers are first prompted to enter information.</span></span> <span data-ttu-id="e7dbd-143">当他们选择 **提交** 时，将向他们显示登记确认，并在 POS 中创建一个任务。</span><span class="sxs-lookup"><span data-stu-id="e7dbd-143">When they select **Submit**, they are shown the check-in confirmation, and a task is created in POS.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="e7dbd-144">其他资源</span><span class="sxs-lookup"><span data-stu-id="e7dbd-144">Additional resources</span></span>

[<span data-ttu-id="e7dbd-145">在销售点 (POS) 启用客户登记通知</span><span class="sxs-lookup"><span data-stu-id="e7dbd-145">Enable customer check-in notifications in point of sale (POS)</span></span>](enable-customer-check-in.md)

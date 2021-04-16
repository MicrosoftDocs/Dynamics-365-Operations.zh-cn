---
title: 客户记录未出现在 Commerce Headquarters 中
description: 本主题提供了当客户记录没有立即出现在 Commerce Headquarters 中时可能会有所帮助的故障排除指南。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5499e3c059c9e735df87ef8b462d446e0710d90c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801787"
---
# <a name="customer-records-dont-appear-in-commerce-headquarters"></a><span data-ttu-id="fe6da-103">客户记录未出现在 Commerce Headquarters 中</span><span class="sxs-lookup"><span data-stu-id="fe6da-103">Customer records don't appear in Commerce headquarters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fe6da-104">本主题提供了当客户记录没有立即出现在 Commerce Headquarters 中时可能会有所帮助的故障排除指南。</span><span class="sxs-lookup"><span data-stu-id="fe6da-104">This topic provides troubleshooting guidance that can help when customer records don't immediately appear in Commerce headquarters.</span></span>

## <a name="description"></a><span data-ttu-id="fe6da-105">说明</span><span class="sxs-lookup"><span data-stu-id="fe6da-105">Description</span></span>

<span data-ttu-id="fe6da-106">当您使用电子商务店面中的注册流程创建新客户记录时，相应的客户记录没有立即出现在 Commerce Headquarters 中。</span><span class="sxs-lookup"><span data-stu-id="fe6da-106">When you create a new customer record by using the sign-up flow in the e-commerce storefront, the corresponding customer record doesn't immediately appear in Commerce headquarters.</span></span>

## <a name="resolution"></a><span data-ttu-id="fe6da-107">解决方法</span><span class="sxs-lookup"><span data-stu-id="fe6da-107">Resolution</span></span>

### <a name="disable-customer-creation-in-async-mode"></a><span data-ttu-id="fe6da-108">禁止在异步模式下创建客户</span><span class="sxs-lookup"><span data-stu-id="fe6da-108">Disable customer creation in async mode</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fe6da-109">如果禁用异步客户创建，则系统性能可能会受到影响，因为创建每条记录时都会向 Commerce Headquarters 发出实时请求。</span><span class="sxs-lookup"><span data-stu-id="fe6da-109">If you disable asynchronous customer creation, system performance could be affected, because creation of each record will produce a real-time request to Commerce headquarters.</span></span> <span data-ttu-id="fe6da-110">此外，如果 Commerce Headquarters 已关闭（例如，在维修流中），则任何新的客户创建流都将产生错误。</span><span class="sxs-lookup"><span data-stu-id="fe6da-110">In addition, if Commerce headquarters is down (for example, during servicing flows), any new customer creation flows will produce errors.</span></span>

<span data-ttu-id="fe6da-111">要禁止在 Commerce Headquarters 中以异步模式创建客户，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="fe6da-111">To disable customer creation in async mode in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="fe6da-112">转至 **Retail 和 Commerce \> 渠道设置 \> 在线商店设置 \> 功能配置文件**。</span><span class="sxs-lookup"><span data-stu-id="fe6da-112">Go to **Retail and Commerce \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="fe6da-113">如果您尚未对在线渠道使用功能配置文件，请创建一个。</span><span class="sxs-lookup"><span data-stu-id="fe6da-113">If you aren't already using a functionality profile for your online channel, create one.</span></span>
1. <span data-ttu-id="fe6da-114">确保 **在异步模式下创建客户** 选项设置为 **否**。</span><span class="sxs-lookup"><span data-stu-id="fe6da-114">Make sure that the **Create customer in async mode** option is set to **No**.</span></span>
1. <span data-ttu-id="fe6da-115">转至 **Retail 和 Commerce \> 渠道 \> 在线商店**。</span><span class="sxs-lookup"><span data-stu-id="fe6da-115">Go to **Retail and Commerce \> Channels \> Online stores**.</span></span>
1. <span data-ttu-id="fe6da-116">选择在线商店以对其禁用异步客户创建。</span><span class="sxs-lookup"><span data-stu-id="fe6da-116">Select the online store to disable asynchronous customer creation for.</span></span>
1. <span data-ttu-id="fe6da-117">在 **常规** 选项卡上，确保 **功能配置文件** 字段设置为您要用于在线渠道的功能配置文件。</span><span class="sxs-lookup"><span data-stu-id="fe6da-117">On the **General** tab, make sure that the **Functionality profile** field is set to the functionality profile that you're using for your online channel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fe6da-118">其他资源</span><span class="sxs-lookup"><span data-stu-id="fe6da-118">Additional resources</span></span>

[<span data-ttu-id="fe6da-119">在 Commerce 中设置 B2C 租户</span><span class="sxs-lookup"><span data-stu-id="fe6da-119">Setup a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)

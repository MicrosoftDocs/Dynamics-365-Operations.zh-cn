---
title: 创建法人
description: 本主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建法人，必须在创建渠道之前创建和配置法人。
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 225fd6a07fee29414ac30a4602b4dfccdc4d742b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800606"
---
# <a name="create-legal-entities"></a><span data-ttu-id="1d693-103">创建法人</span><span class="sxs-lookup"><span data-stu-id="1d693-103">Create legal entities</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1d693-104">本主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建法人，必须在创建渠道之前创建和配置法人。</span><span class="sxs-lookup"><span data-stu-id="1d693-104">This topic describes how to create legal entities in Microsoft Dynamics 365 Commerce, which must be created and configured before creating channels.</span></span>

<span data-ttu-id="1d693-105">法人是具有已登记的或法律允许的法律结构的组织。</span><span class="sxs-lookup"><span data-stu-id="1d693-105">A legal entity is an organization that has a registered or legislated legal structure.</span></span> <span data-ttu-id="1d693-106">法人可以输入到法律合同，并需要准备报告它们的业绩的报表。</span><span class="sxs-lookup"><span data-stu-id="1d693-106">Legal entities can enter into legal contracts and are required to prepare statements that report on their performance.</span></span>

<span data-ttu-id="1d693-107">公司是法人的一种类型。</span><span class="sxs-lookup"><span data-stu-id="1d693-107">A company is a type of legal entity.</span></span> <span data-ttu-id="1d693-108">现在，公司只能是您能创建的这类法人，每个法人与公司 ID 相关联。</span><span class="sxs-lookup"><span data-stu-id="1d693-108">Currently, companies are the only kind of legal entity that you can create, and every legal entity is associated with a company ID.</span></span> <span data-ttu-id="1d693-109">因为程序中的某些功能区域在它们的数据模型中使用了公司 ID 或 *DataAreaId*，所以此关联存在。</span><span class="sxs-lookup"><span data-stu-id="1d693-109">This association exists because some functional areas in the program use a company ID, or *DataAreaId*, in their data models.</span></span> <span data-ttu-id="1d693-110">在这些功能区域中，公司用作了数据安全性的边界。</span><span class="sxs-lookup"><span data-stu-id="1d693-110">In these functional areas, companies are used as a boundary for data security.</span></span> <span data-ttu-id="1d693-111">用户只能访问他们当前登录到的公司的数据。</span><span class="sxs-lookup"><span data-stu-id="1d693-111">Users can access data only for the company that they are currently logged on to.</span></span> 

<span data-ttu-id="1d693-112">创建渠道时，必须指定该渠道所属的法人。</span><span class="sxs-lookup"><span data-stu-id="1d693-112">When creating a channel, you must specify which legal entity that channel belongs to.</span></span>

## <a name="create-a-new-legal-entity"></a><span data-ttu-id="1d693-113">创建新法人</span><span class="sxs-lookup"><span data-stu-id="1d693-113">Create a new legal entity</span></span>

<span data-ttu-id="1d693-114">若要在 Dynamics 365 Commerce 中创建新法人，请按以下步骤进行操作。</span><span class="sxs-lookup"><span data-stu-id="1d693-114">To create a new legal entity in Dynamics 365 Commerce, follow these steps.</span></span>

1. <span data-ttu-id="1d693-115">在导航窗格中，转到 **模块 \> 总部设置 \> 法人**。</span><span class="sxs-lookup"><span data-stu-id="1d693-115">In the navigation pane, go to  **Modules \> Headquarters setup \> Legal entities**.</span></span>
1. <span data-ttu-id="1d693-116">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="1d693-116">On the action pane, select **New**.</span></span> <span data-ttu-id="1d693-117">**新法人** 窗格会出现在右侧。</span><span class="sxs-lookup"><span data-stu-id="1d693-117">The **New legal entity** pane appears on the right.</span></span>
1. <span data-ttu-id="1d693-118">在 **名称** 字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="1d693-118">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="1d693-119">在 **公司** 字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="1d693-119">In the **Company** field, enter a value.</span></span>
1. <span data-ttu-id="1d693-120">在 **国家/地区** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="1d693-120">In the **Country/region** field, enter or select a value.</span></span>
1. <span data-ttu-id="1d693-121">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="1d693-121">Select **OK**.</span></span> 

   ![法人创建](media/legal-entities.png)

1. <span data-ttu-id="1d693-123">在 **常规** 部分中，请提供有关法人的以下一般信息：</span><span class="sxs-lookup"><span data-stu-id="1d693-123">In the **General** section, provide the following general information about the legal entity:</span></span> 
   1. <span data-ttu-id="1d693-124">如果需要搜索名称，请输入搜索名称。</span><span class="sxs-lookup"><span data-stu-id="1d693-124">Enter a search name, if a search name is required.</span></span> <span data-ttu-id="1d693-125">搜索名称是可用于搜索此法人的替代名称。</span><span class="sxs-lookup"><span data-stu-id="1d693-125">A search name is an alternate name that can be used to search for this legal entity.</span></span> 
   1. <span data-ttu-id="1d693-126">选择此法人是否被用作合并公司。</span><span class="sxs-lookup"><span data-stu-id="1d693-126">Select whether this legal entity is being used as a consolidation company.</span></span>
   1. <span data-ttu-id="1d693-127">选择此法人是否被用作清除公司。</span><span class="sxs-lookup"><span data-stu-id="1d693-127">Select whether this legal entity is being used as an elimination company.</span></span> 
   1. <span data-ttu-id="1d693-128">选择实体的 **默认语言**。</span><span class="sxs-lookup"><span data-stu-id="1d693-128">Select the **default language** for the entity.</span></span> 
   1. <span data-ttu-id="1d693-129">为该实体选择 **时区**。</span><span class="sxs-lookup"><span data-stu-id="1d693-129">Select the **time zone** for the entity.</span></span>
1. <span data-ttu-id="1d693-130">在 **地址** 部分，选择 **编辑** 以输入街道名称和门牌号、邮政编码和城市之类的地址信息。</span><span class="sxs-lookup"><span data-stu-id="1d693-130">In the **Addresses** section, select **Edit** to enter address information, such as the street name and number, postal code, and city.</span></span>
1. <span data-ttu-id="1d693-131">在 **联系人信息** 部分，输入有关通信方法的信息，如电子邮件地址、URL 和电话号码。</span><span class="sxs-lookup"><span data-stu-id="1d693-131">In the **Contact information** section, enter information about methods of communication, such as email addresses, URLs, and telephone numbers.</span></span>
1. <span data-ttu-id="1d693-132">在 **法定申报** 部分，输入法定申报的登记编号。</span><span class="sxs-lookup"><span data-stu-id="1d693-132">In the **Statutory reporting** section, enter the registration numbers that are used for statutory reporting.</span></span>
1. <span data-ttu-id="1d693-133">在 **登记编号** 部分，输入法人所需的所有信息。</span><span class="sxs-lookup"><span data-stu-id="1d693-133">In the **Registration numbers** section, enter any information required by the legal entity.</span></span>
1. <span data-ttu-id="1d693-134">在 **银行帐户信息** 部分，输入法人的银行帐户和银行代号。</span><span class="sxs-lookup"><span data-stu-id="1d693-134">In the **Bank account information** section, enter bank accounts and routing numbers for the legal entity.</span></span>
1. <span data-ttu-id="1d693-135">在 **外贸和物流** 部分，输入法人的装运信息。</span><span class="sxs-lookup"><span data-stu-id="1d693-135">In the **Foreign trade and logistics** section, enter shipping information for the legal entity.</span></span>
1. <span data-ttu-id="1d693-136">在 **编号规则** 部分，您可以查看与法人关联的编号规则。</span><span class="sxs-lookup"><span data-stu-id="1d693-136">In the **Number sequences** section, you can view the number sequences that are associated with the legal entity.</span></span> <span data-ttu-id="1d693-137">开始时将是空的。</span><span class="sxs-lookup"><span data-stu-id="1d693-137">This will be empty to start with.</span></span>
1. <span data-ttu-id="1d693-138">在 **仪表板图像** 部分，查看或更改与法人关联的徽标和仪表板图像。</span><span class="sxs-lookup"><span data-stu-id="1d693-138">In the **Dashboard image** section, view or change the logo and dashboard image associated with the legal entity.</span></span>
1. <span data-ttu-id="1d693-139">在 **税务登记** 部分，输入用于向税务主管机构申报的登记编号。</span><span class="sxs-lookup"><span data-stu-id="1d693-139">In the **Tax registration** section, enter the registration numbers that are used to report to tax authorities.</span></span>
1. <span data-ttu-id="1d693-140">在 **1099 税** 部分，输入法人的 1099 信息。</span><span class="sxs-lookup"><span data-stu-id="1d693-140">In the **Tax 1099** section, enter 1099 information for the legal entity.</span></span>
1. <span data-ttu-id="1d693-141">在 **税务信息** 部分，输入法人税务信息。</span><span class="sxs-lookup"><span data-stu-id="1d693-141">In the **Tax invormation** section, enter tax information for the legal entity.</span></span>
1. <span data-ttu-id="1d693-142">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="1d693-142">Select **Save**.</span></span>

<span data-ttu-id="1d693-143">下图显示了示例法人的详细信息。</span><span class="sxs-lookup"><span data-stu-id="1d693-143">The following image shows details of an example legal entity.</span></span>

![法人常规部分](media/legal-entities-general.png)
   
## <a name="additional-resources"></a><span data-ttu-id="1d693-145">其他资源</span><span class="sxs-lookup"><span data-stu-id="1d693-145">Additional resources</span></span>

[<span data-ttu-id="1d693-146">组织和组织层次结构概览</span><span class="sxs-lookup"><span data-stu-id="1d693-146">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="1d693-147">规划组织层次结构</span><span class="sxs-lookup"><span data-stu-id="1d693-147">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="1d693-148">组织层次结构</span><span class="sxs-lookup"><span data-stu-id="1d693-148">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="1d693-149">渠道概览</span><span class="sxs-lookup"><span data-stu-id="1d693-149">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="1d693-150">渠道设置先决条件</span><span class="sxs-lookup"><span data-stu-id="1d693-150">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

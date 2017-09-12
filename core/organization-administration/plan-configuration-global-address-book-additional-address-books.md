---
title: "配置全球通讯簿"
description: "本文介绍您在 Microsoft Dynamics 365 for Finance and Operations 中设置和配置全球通讯簿和任何其他通讯簿前，在计划流程中的考虑事项和必须做的决定。 某些决策需要您确认已为产品的其他区域做出了决策，例如组织层次结构。"
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: c71d54d311f7e2b9afdfb3af5ebee490c60ee4bf
ms.contentlocale: zh-cn
ms.lasthandoff: 06/29/2017


---

# <a name="configure-global-address-books"></a><span data-ttu-id="2693a-104">配置全球通讯簿</span><span class="sxs-lookup"><span data-stu-id="2693a-104">Configure global address books</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="2693a-105">本文介绍您在 Microsoft Dynamics 365 for Finance and Operations 中设置和配置全球通讯簿和任何其他通讯簿前，在计划流程中的考虑事项和必须做的决定。</span><span class="sxs-lookup"><span data-stu-id="2693a-105">This article describes the considerations and decisions that you must make during the planning process, before you set up and configure the global address book and any additional address books in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="2693a-106">某些决策需要您确认已为产品的其他区域做出了决策，例如组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="2693a-106">Some of the decisions will require that you confirm the decisions that have been made for other areas of the product, such as the organization hierarchy.</span></span>

<a name="global-address-book"></a><span data-ttu-id="2693a-107">全球通讯簿</span><span class="sxs-lookup"><span data-stu-id="2693a-107">Global address book</span></span>
-------------------

<span data-ttu-id="2693a-108">在您开始使用全球通讯簿前，必须确定其默认值。</span><span class="sxs-lookup"><span data-stu-id="2693a-108">Before you begin to work with the global address book, you must determine the default values for it.</span></span> <span data-ttu-id="2693a-109">然后这些默认值用于您创建的任何附加通讯簿。</span><span class="sxs-lookup"><span data-stu-id="2693a-109">These default values are then used for any additional address books that you create.</span></span> <span data-ttu-id="2693a-110">**决策：**</span><span class="sxs-lookup"><span data-stu-id="2693a-110">**Decisions:**</span></span>

-   <span data-ttu-id="2693a-111">对于**“人员”**类型的当事方记录，名称应以何种顺序显示？</span><span class="sxs-lookup"><span data-stu-id="2693a-111">What sequence should names be displayed in for party records of the **Person** type?</span></span> <span data-ttu-id="2693a-112">例如一个顺序是姓氏、中间名、名字。</span><span class="sxs-lookup"><span data-stu-id="2693a-112">For example, one sequence is last name, middle name, first name.</span></span>
-   <span data-ttu-id="2693a-113">在删除角色记录时，是否应从通讯簿中删除当事方记录？</span><span class="sxs-lookup"><span data-stu-id="2693a-113">Should party records be deleted from the address book when the role record is deleted?</span></span> <span data-ttu-id="2693a-114">例如，如果删除了客户记录，是否还应删除相应的当事方记录？</span><span class="sxs-lookup"><span data-stu-id="2693a-114">For example, if a customer record is deleted, should the party record also be deleted?</span></span>
-   <span data-ttu-id="2693a-115">创建新记录时，如果在全球通讯簿中找到重复的记录，是否应通知用户？</span><span class="sxs-lookup"><span data-stu-id="2693a-115">When a new record is created, should users be notified if a duplicate record is found in the global address book?</span></span>
-   <span data-ttu-id="2693a-116">是否应在当事方记录信息中包括数据统一编码系统 (DUNS) 编号？</span><span class="sxs-lookup"><span data-stu-id="2693a-116">Should the Data Universal Numbering System (DUNS) number be included in a party record’s information?</span></span>
-   <span data-ttu-id="2693a-117">如果 DUNS 编号包括在当事方记录中，是否应检查该编号的唯一性？</span><span class="sxs-lookup"><span data-stu-id="2693a-117">If the DUNS number is included in a party record, should the uniqueness of the number be checked?</span></span>
-   <span data-ttu-id="2693a-118">在全球通讯簿中创建当事方记录时，您是否需要默认当事方类型、人员或组织？</span><span class="sxs-lookup"><span data-stu-id="2693a-118">When a party record is created in the global address book, do you want a default party type, person, or organization?</span></span>
-   <span data-ttu-id="2693a-119">哪些用户角色应有权访问当事方记录的私人地址和联系信息？</span><span class="sxs-lookup"><span data-stu-id="2693a-119">Which user roles should have access to the private addresses and contact information of party records?</span></span>

## <a name="additional-address-books"></a><span data-ttu-id="2693a-120">附加通讯簿</span><span class="sxs-lookup"><span data-stu-id="2693a-120">Additional address books</span></span>
<span data-ttu-id="2693a-121">在创建全球通讯簿后，您可以根据需要在您的组织中创建附加通讯簿，如组织中每个公司一个单独的通讯簿或每个经营范围一个单独的通讯簿。</span><span class="sxs-lookup"><span data-stu-id="2693a-121">After you create the global address book, you can create additional address books as you require, such as a separate address book for each company in your organization or for each line of business.</span></span> <span data-ttu-id="2693a-122">例如，Fabrikam 是一家具有多个公司和多个经营范围的国际组织。</span><span class="sxs-lookup"><span data-stu-id="2693a-122">For example, Fabrikam is an international organization that has multiple companies and multiple lines of business.</span></span> <span data-ttu-id="2693a-123">Fabrikam 计划为每个经营范围创建通讯簿。</span><span class="sxs-lookup"><span data-stu-id="2693a-123">Fabrikam plans to create an address book for each line of business.</span></span> <span data-ttu-id="2693a-124">对于在多个位置出现的经营范围（如气动工具业务），Fabrikam 计划为每个位置创建一个通讯簿。</span><span class="sxs-lookup"><span data-stu-id="2693a-124">For lines of business that occur in more than one location, such as the pneumatic tools business, Fabrikam plans to create an address book for each location.</span></span> <span data-ttu-id="2693a-125">Fabrikam 的 IT 经理 Chris 创建了以下必需的通讯簿列表。</span><span class="sxs-lookup"><span data-stu-id="2693a-125">Chris, the IT manager at Fabrikam, has created the following list of address books that are required.</span></span> <span data-ttu-id="2693a-126">此列表中还描述每个通讯簿必须包括的当事方记录。</span><span class="sxs-lookup"><span data-stu-id="2693a-126">This list also also describes the party records that each address book must include.</span></span>

-   <span data-ttu-id="2693a-127">**公共部门合同 (PubSC)** – Fabrikam 持有的公共部门合同中涉及的所有当事方的当事方记录。</span><span class="sxs-lookup"><span data-stu-id="2693a-127">**Public Sector Contracts (PubSC)** – Party records for all parties that are involved in the public sector contracts that Fabrikam holds.</span></span>
-   <span data-ttu-id="2693a-128">**私人部门合同 (PriSC)** – Fabrikam 持有的私营部门合同中涉及的所有当事方的当事方记录。</span><span class="sxs-lookup"><span data-stu-id="2693a-128">**Private Sector Contracts (PriSC)** – Party records for all parties that are involved in the private sector contracts that Fabrikam holds.</span></span>
-   <span data-ttu-id="2693a-129">**电子工具 (ET)** – 电子工具采购或销售中涉及，或以其他方式与在 Fabrikam 日本公司中由 Fabrikam 提供的电子工具或为其购买的电子工具交互的所有当事方的当事方记录。</span><span class="sxs-lookup"><span data-stu-id="2693a-129">**Electronic Tools (ET)** – Party records for all parties that are involved in the purchase or sale of electronic tools, or that otherwise interact with the electronic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
-   <span data-ttu-id="2693a-130">**气动工具 (PTJPN)** – 气动工具采购或销售中涉及，或以其他方式与在 Fabrikam 日本公司中由 Fabrikam 提供的气动工具或为其购买的气动工具交互的所有当事方的当事方记录。</span><span class="sxs-lookup"><span data-stu-id="2693a-130">**Pneumatic Tools (PTJPN)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
-   <span data-ttu-id="2693a-131">**气动工具 (PTUSA)** – 气动工具采购或销售中涉及，或以其他方式与在 Fabrikam 美国公司中由 Fabrikam 提供的气动工具或为其购买的气动工具交互的所有当事方的当事方记录。</span><span class="sxs-lookup"><span data-stu-id="2693a-131">**Pneumatic Tools (PTUSA)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-US company.</span></span>

<span data-ttu-id="2693a-132">**决策：**</span><span class="sxs-lookup"><span data-stu-id="2693a-132">**Decision:**</span></span>

-   <span data-ttu-id="2693a-133">您要创建多少附加通讯簿？</span><span class="sxs-lookup"><span data-stu-id="2693a-133">How many additional address books will you create?</span></span>

### <a name="address-book-security"></a><span data-ttu-id="2693a-134">通讯簿安全性</span><span class="sxs-lookup"><span data-stu-id="2693a-134">Address book security</span></span>

<span data-ttu-id="2693a-135">您可以随时创建通讯簿，您还可以随时为通讯簿设置安全参数。</span><span class="sxs-lookup"><span data-stu-id="2693a-135">You can create address books at any time, and you can also set security parameters for the address books at any time.</span></span> <span data-ttu-id="2693a-136">为通讯簿设置安全权限并非必需操作，但如果您未设置，则您的组织中的所有工作人员可以查看该通讯簿中的所有当事方记录。</span><span class="sxs-lookup"><span data-stu-id="2693a-136">You aren't required to set security privileges for an address book, but if you don't, all workers in your organization can view all party records in that address book.</span></span> <span data-ttu-id="2693a-137">您可以通过通讯簿设置当事方记录的安全权限：</span><span class="sxs-lookup"><span data-stu-id="2693a-137">You can set security privileges to party records through address books.</span></span> <span data-ttu-id="2693a-138">安全权限基于团队。</span><span class="sxs-lookup"><span data-stu-id="2693a-138">Security privileges are based on teams.</span></span> <span data-ttu-id="2693a-139">此方法可保证，仅分配至有权访问通讯簿的团队的工作人员才可以查看该通讯簿中的当事方记录。</span><span class="sxs-lookup"><span data-stu-id="2693a-139">This approach guarantees that only workers who are assigned to a team that has access to an address book can view the party records in that address book.</span></span> <span data-ttu-id="2693a-140">您必须选择有权访问每个通讯簿的团队。</span><span class="sxs-lookup"><span data-stu-id="2693a-140">You must select the teams that have access to each address book.</span></span> <span data-ttu-id="2693a-141">对于每个通讯簿，您可以设置允许或拒绝访问特定团队的安全权限。</span><span class="sxs-lookup"><span data-stu-id="2693a-141">For each address book, you can set security privileges that allow or deny access to specific teams.</span></span> <span data-ttu-id="2693a-142">如果您授予团队通讯簿权限，则该团队的所有成员都可以查看通讯簿中的记录。</span><span class="sxs-lookup"><span data-stu-id="2693a-142">If you grant a team privileges to an address book, all members of that team can view the records in the address book.</span></span> <span data-ttu-id="2693a-143">如果您不授予对通讯簿的团队访问权限，则该团队的成员不能查看通讯簿或其内容。</span><span class="sxs-lookup"><span data-stu-id="2693a-143">If you don't grant a team access to an address book, the members of that team can't view the address book or its contents.</span></span> <span data-ttu-id="2693a-144">**决策：**</span><span class="sxs-lookup"><span data-stu-id="2693a-144">**Decision:**</span></span>

-   <span data-ttu-id="2693a-145">哪些团队应有权访问您要创建的每个新通讯簿？</span><span class="sxs-lookup"><span data-stu-id="2693a-145">Which teams should have access to each new address book that you will create?</span></span>






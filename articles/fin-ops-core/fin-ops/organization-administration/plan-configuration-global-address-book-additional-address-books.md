---
title: 规划全球通讯簿和其他通讯簿
description: 本主题介绍您设置和配置全球通讯簿和任何其他通讯簿前，在计划流程中的考虑事项和必须做的决定。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 89c6e71e5f537f0f9309eca1025c8e74cdce6716
ms.sourcegitcommit: 75bbcff474cfb8d2f282be2b9d2d7984d1505fa3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/03/2019
ms.locfileid: "2883403"
---
# <a name="plan-for-the-global-address-book-and-other-address-books"></a><span data-ttu-id="1cff3-103">全球通讯簿和其他通讯簿的计划</span><span class="sxs-lookup"><span data-stu-id="1cff3-103">Plan for the global address book and other address books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1cff3-104">本主题介绍您设置和配置全球通讯簿和任何其他通讯簿前，在计划流程中的考虑事项和必须做的决定。</span><span class="sxs-lookup"><span data-stu-id="1cff3-104">This topic describes the considerations and decisions that you must make during the planning process, before you set up and configure the global address book and any additional address books.</span></span> <span data-ttu-id="1cff3-105">某些决策需要您确认已为产品的其他区域做出了决策，例如组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="1cff3-105">Some of the decisions will require that you confirm the decisions that have been made for other areas of the product, such as the organization hierarchy.</span></span>

## <a name="global-address-book"></a><span data-ttu-id="1cff3-106">全球通讯簿</span><span class="sxs-lookup"><span data-stu-id="1cff3-106">Global address book</span></span>

<span data-ttu-id="1cff3-107">在您开始使用全球通讯簿前，必须确定其默认值。</span><span class="sxs-lookup"><span data-stu-id="1cff3-107">Before you begin to work with the global address book, you must determine the default values for it.</span></span> <span data-ttu-id="1cff3-108">然后这些默认值用于您创建的任何附加通讯簿。</span><span class="sxs-lookup"><span data-stu-id="1cff3-108">These default values are then used for any additional address books that you create.</span></span>

<span data-ttu-id="1cff3-109">**决策**</span><span class="sxs-lookup"><span data-stu-id="1cff3-109">**Decisions**</span></span>

- <span data-ttu-id="1cff3-110">对于**人员**类型的当事方记录，名称应以何种顺序显示？</span><span class="sxs-lookup"><span data-stu-id="1cff3-110">What sequence should names be displayed in for party records of the **Person** type?</span></span> <span data-ttu-id="1cff3-111">例如一个顺序是姓氏、中间名、名字。</span><span class="sxs-lookup"><span data-stu-id="1cff3-111">For example, one sequence is last name, middle name, first name.</span></span>
- <span data-ttu-id="1cff3-112">在删除角色记录时，是否应从通讯簿中删除当事方记录？</span><span class="sxs-lookup"><span data-stu-id="1cff3-112">Should party records be deleted from the address book when the role record is deleted?</span></span> <span data-ttu-id="1cff3-113">例如，如果删除了客户记录，是否还应删除相应的当事方记录？</span><span class="sxs-lookup"><span data-stu-id="1cff3-113">For example, if a customer record is deleted, should the party record also be deleted?</span></span>
- <span data-ttu-id="1cff3-114">创建新记录时，如果在全球通讯簿中找到重复的记录，是否应通知用户？</span><span class="sxs-lookup"><span data-stu-id="1cff3-114">When a new record is created, should users be notified if a duplicate record is found in the global address book?</span></span>
- <span data-ttu-id="1cff3-115">是否应在当事方记录信息中包括数据统一编码系统 (DUNS) 编号？</span><span class="sxs-lookup"><span data-stu-id="1cff3-115">Should the Data Universal Numbering System (DUNS) number be included in a party record's information?</span></span>
- <span data-ttu-id="1cff3-116">如果 DUNS 编号包括在当事方记录中，是否应检查该编号的唯一性？</span><span class="sxs-lookup"><span data-stu-id="1cff3-116">If the DUNS number is included in a party record, should the uniqueness of the number be checked?</span></span>
- <span data-ttu-id="1cff3-117">在全球通讯簿中创建当事方记录时，您是否需要默认当事方类型、人员或组织？</span><span class="sxs-lookup"><span data-stu-id="1cff3-117">When a party record is created in the global address book, do you want a default party type, person, or organization?</span></span>
- <span data-ttu-id="1cff3-118">哪些用户角色应有权访问当事方记录的私人地址和联系信息？</span><span class="sxs-lookup"><span data-stu-id="1cff3-118">Which user roles should have access to the private addresses and contact information of party records?</span></span>

## <a name="additional-address-books"></a><span data-ttu-id="1cff3-119">附加通讯簿</span><span class="sxs-lookup"><span data-stu-id="1cff3-119">Additional address books</span></span>

<span data-ttu-id="1cff3-120">在创建全球通讯簿后，您可以根据需要在您的组织中创建附加通讯簿，如组织中每个公司一个单独的通讯簿或每个经营范围一个单独的通讯簿。</span><span class="sxs-lookup"><span data-stu-id="1cff3-120">After you create the global address book, you can create additional address books as you require, such as a separate address book for each company in your organization or for each line of business.</span></span> <span data-ttu-id="1cff3-121">例如，Fabrikam 是一家具有多个公司和多个经营范围的国际组织。</span><span class="sxs-lookup"><span data-stu-id="1cff3-121">For example, Fabrikam is an international organization that has multiple companies and multiple lines of business.</span></span> <span data-ttu-id="1cff3-122">Fabrikam 计划为每个经营范围创建通讯簿。</span><span class="sxs-lookup"><span data-stu-id="1cff3-122">Fabrikam plans to create an address book for each line of business.</span></span> <span data-ttu-id="1cff3-123">对于在多个位置出现的经营范围（如气动工具业务），Fabrikam 计划为每个位置创建一个通讯簿。</span><span class="sxs-lookup"><span data-stu-id="1cff3-123">For lines of business that occur in more than one location, such as the pneumatic tools business, Fabrikam plans to create an address book for each location.</span></span> <span data-ttu-id="1cff3-124">Fabrikam 的 IT 经理 Chris 创建了以下必需的通讯簿列表。</span><span class="sxs-lookup"><span data-stu-id="1cff3-124">Chris, the IT manager at Fabrikam, has created the following list of address books that are required.</span></span> <span data-ttu-id="1cff3-125">此列表中还描述每个通讯簿必须包括的当事方记录。</span><span class="sxs-lookup"><span data-stu-id="1cff3-125">This list also describes the party records that each address book must include.</span></span>

- <span data-ttu-id="1cff3-126">**公共部门合同 (PubSC)** – Fabrikam 持有的公共部门合同中涉及的所有当事方的当事方记录。</span><span class="sxs-lookup"><span data-stu-id="1cff3-126">**Public Sector Contracts (PubSC)** – Party records for all parties that are involved in the public sector contracts that Fabrikam holds.</span></span>
- <span data-ttu-id="1cff3-127">**私人部门合同 (PriSC)** – Fabrikam 持有的私营部门合同中涉及的所有当事方的当事方记录。</span><span class="sxs-lookup"><span data-stu-id="1cff3-127">**Private Sector Contracts (PriSC)** – Party records for all parties that are involved in the private sector contracts that Fabrikam holds.</span></span>
- <span data-ttu-id="1cff3-128">**电子工具 (ET)** – 电子工具采购或销售中涉及，或以其他方式与在 Fabrikam 日本公司中由 Fabrikam 提供的电子工具或为其购买的电子工具交互的所有当事方的当事方记录。</span><span class="sxs-lookup"><span data-stu-id="1cff3-128">**Electronic Tools (ET)** – Party records for all parties that are involved in the purchase or sale of electronic tools, or that otherwise interact with the electronic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
- <span data-ttu-id="1cff3-129">**气动工具 (PTJPN)** – 气动工具采购或销售中涉及，或以其他方式与在 Fabrikam 日本公司中由 Fabrikam 提供的气动工具或为其购买的气动工具交互的所有当事方的当事方记录。</span><span class="sxs-lookup"><span data-stu-id="1cff3-129">**Pneumatic Tools (PTJPN)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
- <span data-ttu-id="1cff3-130">**气动工具 (PTUSA)** – 气动工具采购或销售中涉及，或以其他方式与在 Fabrikam 美国公司中由 Fabrikam 提供的气动工具或为其购买的气动工具交互的所有当事方的当事方记录。</span><span class="sxs-lookup"><span data-stu-id="1cff3-130">**Pneumatic Tools (PTUSA)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-US company.</span></span>

<span data-ttu-id="1cff3-131">**决策：**</span><span class="sxs-lookup"><span data-stu-id="1cff3-131">**Decision:**</span></span>

- <span data-ttu-id="1cff3-132">您要创建多少附加通讯簿？</span><span class="sxs-lookup"><span data-stu-id="1cff3-132">How many additional address books will you create?</span></span>

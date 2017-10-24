---
title: "记录模板"
description: "本文介绍记录模板的概念并说明如何使用它们创建共享信息的记录。"
author: pvillads
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 16101
ms.assetid: 61ada2d8-84c3-44bc-b4c5-516b1aeac3d1
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e89e4a74550597a4e497a1128fe91c07e766d697
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="record-templates"></a><span data-ttu-id="1c069-103">记录模板</span><span class="sxs-lookup"><span data-stu-id="1c069-103">Record templates</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1c069-104">本文介绍记录模板的概念并说明如何使用它们创建共享信息的记录。</span><span class="sxs-lookup"><span data-stu-id="1c069-104">This article introduces the concept of record templates and explains how they can be used to create records that share information.</span></span>

<span data-ttu-id="1c069-105">记录模板有助于您在 Microsoft Dynamics 365 for Finance and Operations 中更快地创建记录。</span><span class="sxs-lookup"><span data-stu-id="1c069-105">Record templates can help you to create records more quickly in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="1c069-106">您可以仅为 Microsoft Dynamics 365 for Finance and Operations 中的某些记录类型创建记录模版。</span><span class="sxs-lookup"><span data-stu-id="1c069-106">You can create record templates for only some of the record types in Microsoft Dynamics 365 for Finance and Operations.</span></span> 

<span data-ttu-id="1c069-107">例如，假设您为旧金山的汽车租赁业务输入租赁信息。</span><span class="sxs-lookup"><span data-stu-id="1c069-107">For example, imagine you are entering rental information for a car rental business that is located in San Francisco.</span></span> <span data-ttu-id="1c069-108">由于大多数客户可能来自旧金山地区，因此如果您能够在租赁窗体上的**“州”**、**“国家/地区”**和**“城市”**字段中自动填入值将是非常理想的。</span><span class="sxs-lookup"><span data-stu-id="1c069-108">Since most of the customers are likely to be from the San Francisco area, it would be nice if you could automatically fill in the values for the **State**, **Country**, and **City** fields on the rental form.</span></span> 

> [!Note]
> <span data-ttu-id="1c069-109">您只能将模板应用于您有权访问的 Finance and Operations 的区域。</span><span class="sxs-lookup"><span data-stu-id="1c069-109">You can apply templates only for the areas of Finance and Operations that you have access to.</span></span> <span data-ttu-id="1c069-110">但在您创建新记录时，所有模板标题均对您可见，如果您创建的是将对所有用户可用的模板，则对其他用户也可见。</span><span class="sxs-lookup"><span data-stu-id="1c069-110">However all template titles are visible to you when you create a new record, and to other users as well, if you are creating templates that will be available for all users.</span></span> <span data-ttu-id="1c069-111">请确保在命名模板时考虑到这一点。</span><span class="sxs-lookup"><span data-stu-id="1c069-111">Be sure to consider this when naming templates.</span></span> <span data-ttu-id="1c069-112">例如，如果公司某些员工享受与佣金挂钩的薪酬为秘密，请避免使用如“佣金”之类的词语。</span><span class="sxs-lookup"><span data-stu-id="1c069-112">For example, avoid using names that include words, such as "commission," if is confidential that some employees in the company have commission-based salaries.</span></span> 

<span data-ttu-id="1c069-113">当某个特定窗体存在您可以访问的一个或多个模板并且您尝试在该窗体中创建新记录时，将显示**“为以下项选择模板”**页面。</span><span class="sxs-lookup"><span data-stu-id="1c069-113">When one or more templates that you have access to exist for a specific form and you attempt to create a new record in the form, the **Select a template for** page is displayed.</span></span> <span data-ttu-id="1c069-114">在您从列表中选择某一模板时，将创建新记录，并且该新记录包含基于您选择的模板的默认信息。</span><span class="sxs-lookup"><span data-stu-id="1c069-114">When you select a template from the list, the new record is created and contains default information that is based on the template that you selected.</span></span> <span data-ttu-id="1c069-115">如果在您创建新纪录时不想使用模板，请在**为…选择模板**页中选中**不再询问**复选框。</span><span class="sxs-lookup"><span data-stu-id="1c069-115">If you do not want to use templates when you create new records, select the **Do not ask again** check box in the **Select a template for** page.</span></span> <span data-ttu-id="1c069-116">若要再次显示模板选择对话框，则右键单击任意记录，单击**记录信息**，然后单击**显示模板选择**。</span><span class="sxs-lookup"><span data-stu-id="1c069-116">To display the template selection dialog box again, right-click any record, click **Record info**, and then click **Show template selection**.</span></span>





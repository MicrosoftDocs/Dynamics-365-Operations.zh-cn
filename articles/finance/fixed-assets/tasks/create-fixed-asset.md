---
title: 创建固定资产
description: 本主题介绍了如何从“固定资产”列表页面创建新的固定资产记录。
author: saraschi2
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2b7d65a047251fa036242fb456725bc8cba957b9
ms.sourcegitcommit: 51e626675b0130fa32a84ce2d9119b68ea928018
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4000235"
---
# <a name="create-a-fixed-asset"></a><span data-ttu-id="77cca-103">创建固定资产</span><span class="sxs-lookup"><span data-stu-id="77cca-103">Create a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="77cca-104">本主题介绍了如何从 **固定资产** 列表页面创建新的固定资产记录。</span><span class="sxs-lookup"><span data-stu-id="77cca-104">This topic explains how to create a new fixed asset record from the **Fixed asset** list page.</span></span>

<span data-ttu-id="77cca-105">系统根据分配给固定资产组的编号序列分配资产编号。</span><span class="sxs-lookup"><span data-stu-id="77cca-105">The system assigns the asset number, based on the number sequence that is assigned to the fixed asset group.</span></span> <span data-ttu-id="77cca-106">如果您使用固定资产模板来通过 Microsoft Excel 加载项导入资产，或者如果您使用其他导入作业，系统将自动创建固定资产记录并递增资产编号。</span><span class="sxs-lookup"><span data-stu-id="77cca-106">If you use the fixed asset template to import assets via the Microsoft Excel add-in, or if you use another import job, the system automatically creates fixed asset records and increments the asset number.</span></span>

<span data-ttu-id="77cca-107">若要手动创建资产记录，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="77cca-107">To manually create an asset record, follow these steps.</span></span>

1. <span data-ttu-id="77cca-108">转到 **导航窗格 \> 模块 \> 固定资产 \> 固定资产 \> 固定资产** 。</span><span class="sxs-lookup"><span data-stu-id="77cca-108">Go to **Navigation pane \> Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="77cca-109">在 **操作窗格** 上，选择 **新建** 。</span><span class="sxs-lookup"><span data-stu-id="77cca-109">On the **Action pane** , select **New**.</span></span>
3. <span data-ttu-id="77cca-110">在 **固定资产组** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="77cca-110">In **the Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="77cca-111">如果您在 **固定资产参数** 和 **固定资产组** 中启用 **固定资产自动编号功能** ，将会默认显示 **编号** 字段。</span><span class="sxs-lookup"><span data-stu-id="77cca-111">The **Number** field will default if you have enabled **Autonumber fixed assets functionality** in the **Fixed assets parameters** and the **Fixed asset group**.</span></span> <span data-ttu-id="77cca-112">如果没用启用，您必须输入唯一编号以识别固定资产。</span><span class="sxs-lookup"><span data-stu-id="77cca-112">If not, you must enter a unique number to identify the fixed asset.</span></span>
4. <span data-ttu-id="77cca-113">在 **名称** 字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="77cca-113">In the **Name** field, enter a value.</span></span> <span data-ttu-id="77cca-114">输入您的企业为该资产所需的其他信息。</span><span class="sxs-lookup"><span data-stu-id="77cca-114">Enter the additional information that your business needs for this asset.</span></span>
5. <span data-ttu-id="77cca-115">在 **操作窗格** 上，选择 **帐簿** 。</span><span class="sxs-lookup"><span data-stu-id="77cca-115">On the **Action pane** , select **Books**.</span></span>
6. <span data-ttu-id="77cca-116">在 **购置日期** 字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="77cca-116">In the **Acquisition date** field, enter a date.</span></span>
7. <span data-ttu-id="77cca-117">在 **购置价格** 字段中输入数字。</span><span class="sxs-lookup"><span data-stu-id="77cca-117">In the **Acquisition price** field, enter a number.</span></span>

    - <span data-ttu-id="77cca-118">输入您的企业为该帐簿所需的其他信息。</span><span class="sxs-lookup"><span data-stu-id="77cca-118">Enter the additional information that your business needs for this book.</span></span>
    - <span data-ttu-id="77cca-119">输入您的企业为其余帐簿所需的其他信息。</span><span class="sxs-lookup"><span data-stu-id="77cca-119">Enter the additional information that your business needs for the remaining books.</span></span>

8. <span data-ttu-id="77cca-120">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="77cca-120">Close the page.</span></span>

<span data-ttu-id="77cca-121">您也可以通过使用 Excel 加载项或通过从 **数据管理** 工作区运行导入作业来导入固定资产。</span><span class="sxs-lookup"><span data-stu-id="77cca-121">You can also import fixed assets by using the Excel add-in or by running an import job from the **Data management** workspace.</span></span> <span data-ttu-id="77cca-122">在运行导入之前，请在模板中输入必填字段的值。</span><span class="sxs-lookup"><span data-stu-id="77cca-122">Before you run the import, enter the values for required fields in the template.</span></span>

<span data-ttu-id="77cca-123">如果您没有在 Excel 加载项的模板中或在数据管理中定义固定资产编号，系统会为每个导入的资产创建固定资产编号，并自动递增每个编号序列。</span><span class="sxs-lookup"><span data-stu-id="77cca-123">If you didn't define the fixed asset number in the template of the Excel add-in, or in Data management, the system creates a fixed asset number for each imported asset and automatically increments the number sequence for each.</span></span> <span data-ttu-id="77cca-124">但是，如果您导入资产并在模板中定义资产编号，系统 **不会** 自动递增编号序列。</span><span class="sxs-lookup"><span data-stu-id="77cca-124">However, if you import assets and define asset numbers in the template, the system does **not** automatically increment the number sequence.</span></span> <span data-ttu-id="77cca-125">在这种情况下，管理员必须手动更新编号序列。</span><span class="sxs-lookup"><span data-stu-id="77cca-125">In this case, an admin might have to manually update the number sequence.</span></span> <span data-ttu-id="77cca-126">如果您在 Excel 加载项的模板中定义了固定资产编号，系统将使用定义的固定资产编号并递增编号序列。</span><span class="sxs-lookup"><span data-stu-id="77cca-126">If you defined the fixed asset number in the template of the Excel add-in, the system uses the defined fixed asset number and increments the number sequence.</span></span>

---
title: 设置 TDS 税务类型的预缴税金申报代码
description: 预缴税金申报代码用于为从源扣缴税款 (TDS) 生成表格 26Q 和表格 27Q 报表。 本主题说明设置预缴税金申报代码的步骤，让您可以设置 TDS 申报代码。
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 1f9325d182f89b98e8b943ae047c55e7e1aeb02f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023068"
---
# <a name="set-up-withholding-tax-reporting-codes-for-the-tds-tax-type"></a><span data-ttu-id="c7b7e-104">设置 TDS 税务类型的预缴税金申报代码</span><span class="sxs-lookup"><span data-stu-id="c7b7e-104">Set up withholding tax reporting codes for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c7b7e-105">预缴税金申报代码用于为从源扣缴税款 (TDS) 生成表格 26Q 和表格 27Q 报表。</span><span class="sxs-lookup"><span data-stu-id="c7b7e-105">Withholding tax reporting codes are used to generate Form 26Q and Form 27Q statements for Tax Deducted at Source (TDS).</span></span> <span data-ttu-id="c7b7e-106">本主题说明设置预缴税金申报代码的步骤，让您可以设置 TDS 申报代码。</span><span class="sxs-lookup"><span data-stu-id="c7b7e-106">This topic explains how to set up withholding tax reporting codes steps so that you can set up TDS reporting codes.</span></span>

1. <span data-ttu-id="c7b7e-107">转到 **税 \> 设置 \> 预缴税金 \> 预缴税金申报代码**。</span><span class="sxs-lookup"><span data-stu-id="c7b7e-107">Go to **Tax \> Setup \> Withholding tax \> Withholding tax reporting codes**.</span></span>

    <span data-ttu-id="c7b7e-108">[![预缴税金申报代码页面](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)</span><span class="sxs-lookup"><span data-stu-id="c7b7e-108">[![Withholding tax reporting codes page](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)</span></span>

2. <span data-ttu-id="c7b7e-109">在 **税务类型** 字段中，选择 **TDS** 为 TDS 税务类型定义预缴税金申报代码。</span><span class="sxs-lookup"><span data-stu-id="c7b7e-109">In the **Tax type** field, select **TDS** to define withholding tax reporting codes for the TDS tax type.</span></span>
3. <span data-ttu-id="c7b7e-110">在 **预缴税金组分** 字段中，选择要为其定义预缴税金申报代码的 TDS 组分。</span><span class="sxs-lookup"><span data-stu-id="c7b7e-110">In the **Withholding tax component** field, select the TDS component to that you're defining the withholding tax reporting code for.</span></span> <span data-ttu-id="c7b7e-111">**预缴税金组分组** 字段显示为您要定义的 TDS 组分定义的 TDS 组分组。</span><span class="sxs-lookup"><span data-stu-id="c7b7e-111">The **Withholding tax component group** field shows the TDS component group that was defined for the TDS component that you're defining.</span></span>

    <span data-ttu-id="c7b7e-112">**常规** 快速选项卡上的 **地区代码** 字段显示附加到 TDS 组分组的地区代码。</span><span class="sxs-lookup"><span data-stu-id="c7b7e-112">The **Section code** field on the **General** FastTab shows the section code that is attached to the TDS component group.</span></span>

4. <span data-ttu-id="c7b7e-113">在 **常规** 快速选项卡上，在 **申报代码** 字段中，选择 TDS 申报代码：</span><span class="sxs-lookup"><span data-stu-id="c7b7e-113">On the **General** FastTab, in the **Reporting code** field, select the TDS reporting code:</span></span>

    - <span data-ttu-id="c7b7e-114">TDS</span><span class="sxs-lookup"><span data-stu-id="c7b7e-114">TDS</span></span>
    - <span data-ttu-id="c7b7e-115">TCS</span><span class="sxs-lookup"><span data-stu-id="c7b7e-115">TCS</span></span>
    - <span data-ttu-id="c7b7e-116">附加费</span><span class="sxs-lookup"><span data-stu-id="c7b7e-116">Surcharge</span></span>
    - <span data-ttu-id="c7b7e-117">PE\_Cess</span><span class="sxs-lookup"><span data-stu-id="c7b7e-117">PE\_Cess</span></span>
    - <span data-ttu-id="c7b7e-118">SHE\_Cess</span><span class="sxs-lookup"><span data-stu-id="c7b7e-118">SHE\_Cess</span></span>

5. <span data-ttu-id="c7b7e-119">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c7b7e-119">Close the page.</span></span>

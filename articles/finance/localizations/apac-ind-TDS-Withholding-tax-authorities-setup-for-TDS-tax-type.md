---
title: 设置 TDS 税务类型的预缴税金主管机构
description: 本主题说明如何设置从源扣缴税款 (TDS) 主管机构。
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
ms.openlocfilehash: 5375363a9b1383a83e80fc3c4b841780adab4172
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023050"
---
# <a name="set-up-withholding-tax-authorities-for-the-tds-tax-type"></a><span data-ttu-id="2dfb7-103">设置 TDS 税务类型的预缴税金主管机构</span><span class="sxs-lookup"><span data-stu-id="2dfb7-103">Set up withholding tax authorities for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2dfb7-104">本主题说明如何设置从源扣缴税款 (TDS) 主管机构。</span><span class="sxs-lookup"><span data-stu-id="2dfb7-104">This topic explains how to set up Tax Deducted at Source (TDS) authorities.</span></span>

1. <span data-ttu-id="2dfb7-105">转到 **税 \> 间接税 \> 预缴税金主管机构**。</span><span class="sxs-lookup"><span data-stu-id="2dfb7-105">Go to **Tax \> Indirect taxes \> Withholding tax authorities**.</span></span>

    <span data-ttu-id="2dfb7-106">[![预缴税金主管机构页面](./media/apac-ind-TDS-12.png)](./media/apac-ind-TDS-12.png)</span><span class="sxs-lookup"><span data-stu-id="2dfb7-106">[![Withholding tax authorities page](./media/apac-ind-TDS-12.png)](./media/apac-ind-TDS-12.png)</span></span>

2. <span data-ttu-id="2dfb7-107">在 **税务类型** 字段中，选择 **TDS** 为 TDS 税务类型设置预缴税金主管机构。</span><span class="sxs-lookup"><span data-stu-id="2dfb7-107">In the **Tax type** field, select **TDS** to set up withholding tax authorities for the TDS tax type.</span></span>
3. <span data-ttu-id="2dfb7-108">在“操作窗格”中，选择 **新建** 创建一行。</span><span class="sxs-lookup"><span data-stu-id="2dfb7-108">On the Action Pane, select **New** to create a line.</span></span>
4. <span data-ttu-id="2dfb7-109">在 **预缴税金主管机构** 字段中，为 TDS 主管机构输入名称。</span><span class="sxs-lookup"><span data-stu-id="2dfb7-109">In the **Withholding tax authority** field, enter a name for the TDS authority.</span></span>
5. <span data-ttu-id="2dfb7-110">在 **描述** 字段中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="2dfb7-110">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="2dfb7-111">在 **常规** 快速选项卡上，在 **供应商帐户** 字段中，选择 TDS 主管机构的供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="2dfb7-111">On the **General** FastTab, in the **Vendor account** field, select the vendor account for the TDS authority.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2dfb7-112">您必须定义欠 TDS 主管机构供应商的资金将存入的银行的名称。</span><span class="sxs-lookup"><span data-stu-id="2dfb7-112">You must define the name of the bank where funds that are owed to the TDS authority vendor will be deposited.</span></span> <span data-ttu-id="2dfb7-113">银行的名称在 **银行帐户** 页（**应付帐款 \> 所有供应商 \> 供应商 \> 设置 \> 银行帐户**）上定义。</span><span class="sxs-lookup"><span data-stu-id="2dfb7-113">The bank's name is defined on the **Bank accounts** page (**Accounts payable \> All vendors \> Vendor \> Set up \> Bank accounts**).</span></span>

7. <span data-ttu-id="2dfb7-114">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="2dfb7-114">Close the page.</span></span>

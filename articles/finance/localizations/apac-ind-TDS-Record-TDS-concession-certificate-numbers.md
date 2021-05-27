---
title: 记录 TDS 减免证书编号
description: 本主题说明如何记录发放给供应商的从源扣缴税款 (TDS) 减免证书编号。
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
ms.openlocfilehash: f543adc8bab5ca224bdb672d6b3c282c2d8531d8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023046"
---
# <a name="record-tds-concession-certificate-numbers"></a><span data-ttu-id="8a9de-103">记录 TDS 减免证书编号</span><span class="sxs-lookup"><span data-stu-id="8a9de-103">Record TDS concession certificate numbers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8a9de-104">本主题说明如何记录发放给供应商的从源扣缴税款 (TDS) 减免证书编号。</span><span class="sxs-lookup"><span data-stu-id="8a9de-104">This topic explains how to record the Tax Deducted at Source (TDS) concession certificate numbers that are issued to vendors.</span></span>

1. <span data-ttu-id="8a9de-105">转到 **税务 \> 间接税 \> 预缴税金 \> 预缴税金减免**。</span><span class="sxs-lookup"><span data-stu-id="8a9de-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax concessions**.</span></span>
2. <span data-ttu-id="8a9de-106">在 **税务类型** 字段中，选择 **TDS** 以记录 TDS 税务类型的减免证书。</span><span class="sxs-lookup"><span data-stu-id="8a9de-106">In the **Tax type** field, select **TDS** to record concession certificates for the TDS tax type.</span></span>
3. <span data-ttu-id="8a9de-107">在 **概述** 选项卡上，选择 **Alt+N** 以创建行。</span><span class="sxs-lookup"><span data-stu-id="8a9de-107">On the **Overview** tab, select **Alt+N** to create a line.</span></span>

    <span data-ttu-id="8a9de-108">[![新行的标头](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)</span><span class="sxs-lookup"><span data-stu-id="8a9de-108">[![Header of the new line](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)</span></span>

4. <span data-ttu-id="8a9de-109">在 **预缴税金代码** 字段中，选择为其发放供应商减免证书的 TDS 税码。</span><span class="sxs-lookup"><span data-stu-id="8a9de-109">In the **Withholding tax code** field, select the TDS tax code that the vendor concession certificates are issued for.</span></span> <span data-ttu-id="8a9de-110">**预缴税金代码名称** 字段显示 TDS 税码的名称。</span><span class="sxs-lookup"><span data-stu-id="8a9de-110">The **Withholding tax code name** field shows the name of the TDS tax code.</span></span>
5. <span data-ttu-id="8a9de-111">在 **开始日期** 和 **结束日期** 字段中，定义使用 TDS 税码基于减免计算供应商 TDS 的减免证书的有效期。</span><span class="sxs-lookup"><span data-stu-id="8a9de-111">In the **From date** and **To date** fields, define the period of validity for the concession certificate that uses the TDS tax code to calculate TDS for the vendor on a concessional basis.</span></span>
6. <span data-ttu-id="8a9de-112">在 **注解** 字段中，输入任何注解。</span><span class="sxs-lookup"><span data-stu-id="8a9de-112">In the **Remarks** field, enter any remarks.</span></span>
7. <span data-ttu-id="8a9de-113">在 **章节** 字段中，输入 TDS 减免证书可用的法律章节代码。</span><span class="sxs-lookup"><span data-stu-id="8a9de-113">In the **Section** field, enter the legal section code that the TDS concession certificate is availed under.</span></span>

    <span data-ttu-id="8a9de-114">如果章节代码为 197，表单 26Q 中的“非扣除/减低扣除的原因”列和表单 27Q 中的“非扣除/降低扣除/补偿费（如果有）的原因”列中均显示值“A”。</span><span class="sxs-lookup"><span data-stu-id="8a9de-114">If the section code is 197, the value "A" appears in both the "Reason for non-deduction/lower deduction" column in Form 26Q and the "Reason for non-deduction/lower deduction/grossing up (if any)" column in Form 27Q.</span></span> <span data-ttu-id="8a9de-115">如果章节代码为 197A，这两个列中均显示值“B”。</span><span class="sxs-lookup"><span data-stu-id="8a9de-115">If the section code is 197A, the value "B" appears in both those places.</span></span>

8. <span data-ttu-id="8a9de-116">选择 **证书** 快速选项卡以记录供应商的 TDS 减免证书编号。</span><span class="sxs-lookup"><span data-stu-id="8a9de-116">Select the **Certificate** FastTab to record TDS concession certificate numbers for vendors.</span></span>
9. <span data-ttu-id="8a9de-117">在 **供应商帐户** 字段中，选择要为其发放 TDS 减免证书的供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="8a9de-117">In the **Vendor account** field, select the vendor account that the TDS concession certificate is issued for.</span></span>
10. <span data-ttu-id="8a9de-118">在 **开始日期** 和 **结束日期** 字段张，定义 TDS 减免证书的有效期。</span><span class="sxs-lookup"><span data-stu-id="8a9de-118">In the **From date** and **To date** fields, define the period of validity for the TDS concession certificate.</span></span>

    <span data-ttu-id="8a9de-119">基于减免的 TDS 计算基于为供应商创建证书的期间。</span><span class="sxs-lookup"><span data-stu-id="8a9de-119">The calculation of TDS on a concessional basis is based on the period when the certificate is created for the vendor.</span></span>

11. <span data-ttu-id="8a9de-120">在 **证书** 字段中，输入 TDS 减免证书编号。</span><span class="sxs-lookup"><span data-stu-id="8a9de-120">In the **Certificate** field, enter the TDS concession certificate number.</span></span>

    <span data-ttu-id="8a9de-121">[![证书快速选项卡](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)</span><span class="sxs-lookup"><span data-stu-id="8a9de-121">[![Certificate FastTab](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)</span></span>

12. <span data-ttu-id="8a9de-122">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8a9de-122">Close the page.</span></span>

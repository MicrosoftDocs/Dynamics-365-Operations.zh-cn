---
title: 设置 TDS 税务类型的预缴税金结算期间
description: 本主题说明如何为从源扣缴税款 (TDS) 结算期间设置结算期间。
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
ms.openlocfilehash: 9430bc1386f127d02b598d6cad1b53f66e0cf2ba
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023045"
---
# <a name="set-up-withholding-tax-settlement-periods-for-the-tds-tax-type"></a><span data-ttu-id="6c616-103">设置 TDS 税务类型的预缴税金结算期间</span><span class="sxs-lookup"><span data-stu-id="6c616-103">Set up withholding tax settlement periods for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c616-104">本主题说明如何为从源扣缴税款 (TDS) 结算期间设置结算期间。</span><span class="sxs-lookup"><span data-stu-id="6c616-104">This topic explains how to set up settlement periods for Tax Deducted at Source (TDS) settlement periods.</span></span>

1. <span data-ttu-id="6c616-105">转到 **税 \> 间接税 \> 预缴税金 \> 预缴税金结算期间**。</span><span class="sxs-lookup"><span data-stu-id="6c616-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax settlement periods**.</span></span>

    <span data-ttu-id="6c616-106">[![预缴税金结算期间页面](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)</span><span class="sxs-lookup"><span data-stu-id="6c616-106">[![Withholding tax settlement periods page](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)</span></span>

2. <span data-ttu-id="6c616-107">在 **税务类型** 字段中，选择 **TDS** 为 TDS 税务类型设置预缴税金结算期间。</span><span class="sxs-lookup"><span data-stu-id="6c616-107">In the **Tax type** field, select **TDS** to set up withholding tax settlement periods for the TDS tax type.</span></span>
3. <span data-ttu-id="6c616-108">选择 **新建** 创建行。</span><span class="sxs-lookup"><span data-stu-id="6c616-108">Select **New** to create a line.</span></span>
4. <span data-ttu-id="6c616-109">在 **结算期间** 字段中，为 TDS 结算期间输入名称。</span><span class="sxs-lookup"><span data-stu-id="6c616-109">In the **Settlement period** field, enter a name for the TDS settlement period.</span></span>
5. <span data-ttu-id="6c616-110">在 **描述** 字段中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="6c616-110">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="6c616-111">在 **预缴税金主管机构** 字段中，选择您要为其定义 TDS 结算期间的 TDS 主管机构。</span><span class="sxs-lookup"><span data-stu-id="6c616-111">In the **Withholding tax authority** field, select the TDS authority that you're defining the TDS settlement period for.</span></span>
7. <span data-ttu-id="6c616-112">在 **常规** 快速选项卡上，在 **期间间隔** 字段中，选择 TDS 结算期间的期间间隔类型。</span><span class="sxs-lookup"><span data-stu-id="6c616-112">On the **General** FastTab, in the **Period interval** field, select the type of period interval for the TDS settlement period.</span></span>
8. <span data-ttu-id="6c616-113">在 **单位数量** 字段中，指定期间间隔类型的单位数量。</span><span class="sxs-lookup"><span data-stu-id="6c616-113">In the **Number of units** field, specify the number of units for the period interval type.</span></span>
9. <span data-ttu-id="6c616-114">在 **期间** 快速选项卡上，在 **开始日期** 字段中，选择 TDS 结算期间的开始日期。</span><span class="sxs-lookup"><span data-stu-id="6c616-114">On the **Periods** FastTab, in the **From date** field, select the start date for the TDS settlement period.</span></span> <span data-ttu-id="6c616-115">在 **结束日期** 字段中，选择结束日期。</span><span class="sxs-lookup"><span data-stu-id="6c616-115">In the **To date** field, select the end date.</span></span>
10. <span data-ttu-id="6c616-116">要根据期间间隔和期间单位为现有期间创建后续的 TDS 结算期间，选择 **新建期间**。</span><span class="sxs-lookup"><span data-stu-id="6c616-116">To create a subsequent TDS settlement period for an existing period, based on the period interval and period units, select **New period**.</span></span>
11. <span data-ttu-id="6c616-117">要查看在特定结算期间运行的定期 TDS 结算的详细信息，选择 **预缴税金付款** 打开 **预缴税金付款** 页。</span><span class="sxs-lookup"><span data-stu-id="6c616-117">To view the details of the periodic TDS settlement that is run for a specific settlement period, select **Withholding tax payments** to open the **Withholding tax payment** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6c616-118">要运行定期 TDS 结算流程，转到 **总帐 \> 定期 \> 预缴税金 \> 预缴税金付款**。</span><span class="sxs-lookup"><span data-stu-id="6c616-118">To run the periodic TDS settlement process, go to **General ledger \> Periodic \> Withholding tax \> Withholding tax payment**.</span></span>

    <span data-ttu-id="6c616-119">[![预缴税金付款页面](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)</span><span class="sxs-lookup"><span data-stu-id="6c616-119">[![Withholding tax payment page](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)</span></span>

12. <span data-ttu-id="6c616-120">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6c616-120">Close the page.</span></span>

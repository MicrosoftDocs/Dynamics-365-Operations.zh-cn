---
title: 设置法人的 TDS 登记编号
description: 本主题说明如何设置法人的从源扣缴税款 (TDS) 登记编号。
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
ms.openlocfilehash: 3550b2b7b305702ffc337ba0a9bb79f60a9de120
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023055"
---
# <a name="set-up-tds-registration-numbers-for-legal-entities"></a><span data-ttu-id="dc86b-103">设置法人的 TDS 登记编号</span><span class="sxs-lookup"><span data-stu-id="dc86b-103">Set up TDS registration numbers for legal entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc86b-104">本主题说明如何设置法人的从源扣缴税款 (TDS) 登记编号。</span><span class="sxs-lookup"><span data-stu-id="dc86b-104">This topic explains how to set up Tax Deducted at Source (TDS) registration numbers for legal entities.</span></span>

1. <span data-ttu-id="dc86b-105">转至 **组织管理 \> 组织 \> 法人实体**。</span><span class="sxs-lookup"><span data-stu-id="dc86b-105">Go to **Organization administration \> Organizations \> Legal entities**.</span></span>

    <span data-ttu-id="dc86b-106">[![法人页面](./media/apac-ind-TDS-4.png)](./media/apac-ind-TDS-4.png)</span><span class="sxs-lookup"><span data-stu-id="dc86b-106">[![Legal entities page](./media/apac-ind-TDS-4.png)](./media/apac-ind-TDS-4.png)</span></span>

2. <span data-ttu-id="dc86b-107">在 **税务信息** 快速选项卡的 **永久帐号** 字段中，输入法人的永久帐号 (PAN)。</span><span class="sxs-lookup"><span data-stu-id="dc86b-107">On the **Tax information** FastTab, in the **Permanent account number** field, enter the permanent account number (PAN) of the legal entity.</span></span>
3. <span data-ttu-id="dc86b-108">在 **圈号** 字段中，输入 TDS 主管机构的圈号。</span><span class="sxs-lookup"><span data-stu-id="dc86b-108">In the **Circle number** field, enter the circle number of the TDS authority.</span></span>
4. <span data-ttu-id="dc86b-109">在 **区号** 字段中，输入 TDS 主管机构的区号。</span><span class="sxs-lookup"><span data-stu-id="dc86b-109">In the **Ward number** field, enter the ward number of the TDS authority.</span></span>
5. <span data-ttu-id="dc86b-110">在 **评估人员** 字段中，输入 TDS 主管机构的评估人员的详细信息。</span><span class="sxs-lookup"><span data-stu-id="dc86b-110">In the **Assessing officer** field, enter the details of the assessing officer for the TDS authority.</span></span>
6. <span data-ttu-id="dc86b-111">在 **扣税类型** 字段中，选择法人的扣税类型类别。</span><span class="sxs-lookup"><span data-stu-id="dc86b-111">In the **Type of deductor** field, select the deductor type category for the legal entity.</span></span>
7. <span data-ttu-id="dc86b-112">在操作窗格上，选择 **登记 ID** 以打开 **管理地址** 页面。</span><span class="sxs-lookup"><span data-stu-id="dc86b-112">On the Action Pane, select **Registration IDs** to open the **Manage addresses** page.</span></span>
8. <span data-ttu-id="dc86b-113">在 **税务信息** 快速选项卡上，选择 **添加** 或 **编辑** 以打开 **管理税务信息** 页面，您可以在该页面中维护税务登记条目。</span><span class="sxs-lookup"><span data-stu-id="dc86b-113">On the **Tax information** FastTab, select **Add** or **Edit** to open the **Manage tax information** page, where you can maintain the tax registration entry.</span></span>

    <span data-ttu-id="dc86b-114">[![管理地址页面](./media/apac-ind-TDS-5.png)](./media/apac-ind-TDS-5.png)</span><span class="sxs-lookup"><span data-stu-id="dc86b-114">[![Manage addresses page](./media/apac-ind-TDS-5.png)](./media/apac-ind-TDS-5.png)</span></span>

9. <span data-ttu-id="dc86b-115">在 **预缴税金** 快速选项卡的 **税务帐号 (TAN)** 字段中，输入登记编号。</span><span class="sxs-lookup"><span data-stu-id="dc86b-115">On the **Withholding tax** FastTab, in the **Tax Account Number (TAN)** field, enter the registration number.</span></span> <span data-ttu-id="dc86b-116">此编号必须包含四个字母字符、五个数字字符和一个字母字符。</span><span class="sxs-lookup"><span data-stu-id="dc86b-116">This number must consist of four alphabetic characters, then five numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="dc86b-117">下面是一个示例：**AXDF87645F**。</span><span class="sxs-lookup"><span data-stu-id="dc86b-117">Here is an example: **AXDF87645F**.</span></span>
10. <span data-ttu-id="dc86b-118">在 **名称或描述** 字段中，输入预缴税金登记编号的描述。</span><span class="sxs-lookup"><span data-stu-id="dc86b-118">In the **Name or description** field, enter a description of the withholding tax registration number.</span></span>

    <span data-ttu-id="dc86b-119">[![管理税务信息页面](./media/apac-ind-TDS-5-1.png)](./media/apac-ind-TDS-5-1.png)</span><span class="sxs-lookup"><span data-stu-id="dc86b-119">[![Manage tax information page](./media/apac-ind-TDS-5-1.png)](./media/apac-ind-TDS-5-1.png)</span></span>

11. <span data-ttu-id="dc86b-120">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="dc86b-120">Close the page.</span></span>

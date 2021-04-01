---
title: 设置指数利率
description: 本主题说明如何设置指数利率。 如果您的组织将租赁付款额与一组指数利率关联，则需要指数利率。
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b6d201329996f23d94c0fc76a9635d3bb99c931e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249669"
---
# <a name="set-up-index-rates"></a><span data-ttu-id="c0144-104">设置指数利率</span><span class="sxs-lookup"><span data-stu-id="c0144-104">Set up index rates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c0144-105">如果租赁付款取决于指数，则可以在系统中添加并维护指数利率类型。</span><span class="sxs-lookup"><span data-stu-id="c0144-105">If lease payments depend on an index, the index rate types can be added and maintained in the system.</span></span> <span data-ttu-id="c0144-106">为了从 **指数利率类型** 页面重估租赁付款，指数利率重估流程使用自重估之日起的最新指数利率。</span><span class="sxs-lookup"><span data-stu-id="c0144-106">To revalue the lease payments from the **Index rate type** page, the index rate revaluation process uses the most recent index rate from the date of revaluation.</span></span>

<span data-ttu-id="c0144-107">若要添加指数利率类型和指数利率，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="c0144-107">To add index rate types and index rates, follow these steps.</span></span>

1. <span data-ttu-id="c0144-108">转到 **资产租赁 \> 设置 \> 指数利率类型**。</span><span class="sxs-lookup"><span data-stu-id="c0144-108">Go to **Asset leasing \> Setup \> Index rate type**.</span></span>
2. <span data-ttu-id="c0144-109">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="c0144-109">Select **New**.</span></span>
3. <span data-ttu-id="c0144-110">在相应字段中，输入指数利率的利率类型和名称。</span><span class="sxs-lookup"><span data-stu-id="c0144-110">In the appropriate fields, enter the rate type and the name of the index rate.</span></span>
4. <span data-ttu-id="c0144-111">要添加新的指数利率值，请选择指数利率类型，然后选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="c0144-111">To add a new index rate value, select the index rate type, and then select **Add**.</span></span>
5. <span data-ttu-id="c0144-112">选择利率的生效日期，然后选择利率值。</span><span class="sxs-lookup"><span data-stu-id="c0144-112">Select the effective start date of the rate, and select the rate value.</span></span>

<span data-ttu-id="c0144-113">您必须选择 **指数利率值差** 要么 **指数利率值** 作为指数利率方法。</span><span class="sxs-lookup"><span data-stu-id="c0144-113">You must select either **Index rate value difference** or **Index rate value** as the index rate method.</span></span>

- <span data-ttu-id="c0144-114">根据开始日期的指数利率与最近指数利率之间的差选择用于计算新租赁付款的 **指数利率值差** 方法。</span><span class="sxs-lookup"><span data-stu-id="c0144-114">Select the **Index rate value difference** method to calculate a new lease payment, based on the difference between the index rate on the start date and the most recent index rate.</span></span> <span data-ttu-id="c0144-115">指数利率在 **指数利率(%)** 字段中定义。</span><span class="sxs-lookup"><span data-stu-id="c0144-115">The index rate is defined in the **Index rate (%)** field.</span></span>
- <span data-ttu-id="c0144-116">通过选择 **指数利率(%)** 字段中指定的百分比，选择用于计算租赁付款的 **指数利率值** 方法。</span><span class="sxs-lookup"><span data-stu-id="c0144-116">Select the **Index rate value** method to calculate the lease payment by using the percentage that is specified in the **Index rate (%)** field.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
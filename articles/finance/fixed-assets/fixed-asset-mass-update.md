---
title: 固定资产成批更新
description: 如果您使用帐簿，则可以更改同属于一个帐簿的资产组的折旧惯例。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 3521
ms.assetid: 50207ffb-6b89-4fb9-92e9-928bc0729489
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc2f311e2463d68b9a8f8edb3afb82bef0934540
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212437"
---
# <a name="fixed-asset-mass-update"></a><span data-ttu-id="ff7a6-103">固定资产成批更新</span><span class="sxs-lookup"><span data-stu-id="ff7a6-103">Fixed asset mass update</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ff7a6-104">如果您使用帐簿，则可以更改同属于一个帐簿的资产组的折旧惯例。</span><span class="sxs-lookup"><span data-stu-id="ff7a6-104">If you use books, you can change the depreciation conventions for groups of assets that are part of the same book.</span></span>

<span data-ttu-id="ff7a6-105">例如，如果您身处美国并且在当年的第四季度将超过 40% 的资产投入服务，则必须使用季度中期折旧惯例。</span><span class="sxs-lookup"><span data-stu-id="ff7a6-105">For example, if you are in the United States, and you put more than 40 percent of your assets in service during the fourth quarter of the year, you must use the mid-quarter depreciation convention.</span></span> <span data-ttu-id="ff7a6-106">您可以使用成批更新流程更改要求新的折旧惯例的所有资产。</span><span class="sxs-lookup"><span data-stu-id="ff7a6-106">You can use the process for a mass update to change all assets that require the new depreciation convention.</span></span> 

<span data-ttu-id="ff7a6-107">当您更新资产的折旧惯例时，删除对于这些资产存在的所有折旧交易记录。</span><span class="sxs-lookup"><span data-stu-id="ff7a6-107">When you update the depreciation convention for assets, you delete all depreciation transactions that exist for those assets.</span></span> <span data-ttu-id="ff7a6-108">您还可以删除折旧调整的所有交易记录、额外折旧的交易记录和这些资产的特别折旧的交易记录。</span><span class="sxs-lookup"><span data-stu-id="ff7a6-108">You also delete all transactions for depreciation adjustments, transactions for bonus depreciation, and transactions for extraordinary depreciation for those assets.</span></span> 

<span data-ttu-id="ff7a6-109">若要更新已处置的资产的折旧惯例，您必须首先删除现有处置交易记录。</span><span class="sxs-lookup"><span data-stu-id="ff7a6-109">To update the depreciation convention for assets that have already been disposed of, you must first delete the existing disposal transactions.</span></span> <span data-ttu-id="ff7a6-110">您还必须删除由于处置流程生成的所有交易记录。</span><span class="sxs-lookup"><span data-stu-id="ff7a6-110">You must also delete all transactions that were generated because of the disposal process.</span></span> 

<span data-ttu-id="ff7a6-111">在您更新资产的折旧惯例后，您可以处理每个资产的折旧和特别折旧。</span><span class="sxs-lookup"><span data-stu-id="ff7a6-111">After you update the depreciation convention for assets, you can process depreciation and extraordinary depreciation for each asset.</span></span> <span data-ttu-id="ff7a6-112">如果需要任何调整，您还可以进行手动折旧调整。</span><span class="sxs-lookup"><span data-stu-id="ff7a6-112">You can also make manual depreciation adjustments, if any adjustments are required.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: 访问财务和税务参考数据
description: 此主题提供有关访问财务和税务参考数据的信息。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 28f47f8cebca6c7249e0596c53f3589dc6541e26
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112393"
---
# <a name="access-to-finance-and-tax-reference-data"></a><span data-ttu-id="a674e-103">访问财务和税务参考数据</span><span class="sxs-lookup"><span data-stu-id="a674e-103">Access to finance and tax reference data</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="a674e-104">每家企业都需要处理一组基本财务数据，如会计日历年度、企业进行交易时使用的货币、开展业务所用资金出入的帐户、税率和汇款。</span><span class="sxs-lookup"><span data-stu-id="a674e-104">Every business works with a basic set of financial data, such as the fiscal calendar year, the currency that business is transacted in, the accounts that the money to run the business comes in to or goes out of, tax rates, and remittance.</span></span> <span data-ttu-id="a674e-105">这些数据存储在 Finance and Operations 应用中。</span><span class="sxs-lookup"><span data-stu-id="a674e-105">This data resides in Finance and Operations apps.</span></span> <span data-ttu-id="a674e-106">但是，Common Data Service 可以访问，所以 Microsoft Dynamics 365 中的模型驱动应用对财务和税务数据使用一个来源。</span><span class="sxs-lookup"><span data-stu-id="a674e-106">However, it's exposed to Common Data Service so that model-driven apps in Microsoft Dynamics 365 can have a single source for finance and tax data.</span></span> <span data-ttu-id="a674e-107">因此，数据在整个业务生态系统中都是统一的。</span><span class="sxs-lookup"><span data-stu-id="a674e-107">In this way, data is uniform across the business ecosystem.</span></span> 

<span data-ttu-id="a674e-108">财务和税务数据使用以下映射进行集成：</span><span class="sxs-lookup"><span data-stu-id="a674e-108">Finance and tax data is integrated by using the following mappings:</span></span>

+ [<span data-ttu-id="a674e-109">集成的分类账</span><span class="sxs-lookup"><span data-stu-id="a674e-109">Integrated ledger</span></span>](ledger-mapping.md)
+ [<span data-ttu-id="a674e-110">集成的税收主数据</span><span class="sxs-lookup"><span data-stu-id="a674e-110">Integrated tax master</span></span>](tax-mapping.md)

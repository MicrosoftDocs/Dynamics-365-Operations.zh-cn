---
title: 资产出借
description: 本主题介绍如何在资产管理中登记出借资产。
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectLoanSend, EntAssetObjectLoanListPage, EntAssetObjectLoanReturn, EntAssetObjectLoanInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cba680d0ad626e0275539d7478a83639a9d22635
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889641"
---
# <a name="asset-loans"></a><span data-ttu-id="648b0-103">资产出借</span><span class="sxs-lookup"><span data-stu-id="648b0-103">Asset loans</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="648b0-104">如果您的公司从内部位置或客户处收到用于维修作业或维护作业的资产，以及如果您暂时将资产出借给这些位置或客户，资产管理可以跟踪资产出借。</span><span class="sxs-lookup"><span data-stu-id="648b0-104">If your company receives assets for repair or maintenance jobs from either internal locations or customers, and if you temporarily loan assets to those locations or customers, Asset Management can track the asset loans.</span></span>

## <a name="register-asset-loans-on-a-maintenance-request"></a><span data-ttu-id="648b0-105">登记维护请求的资产出借</span><span class="sxs-lookup"><span data-stu-id="648b0-105">Register asset loans on a maintenance request</span></span>

1. <span data-ttu-id="648b0-106">选择**资产管理** \> **常用** \> **维护请求** \> **所有维护请求**或**有效维护请求**。</span><span class="sxs-lookup"><span data-stu-id="648b0-106">Select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests** or **Active maintenance requests**.</span></span>
2. <span data-ttu-id="648b0-107">选择要为其登记资产出借的维护请求，然后选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="648b0-107">Select the maintenance request to register an asset loan on, and then select **Edit**.</span></span>
3. <span data-ttu-id="648b0-108">在**请求**页，选择**发送出借资产**。</span><span class="sxs-lookup"><span data-stu-id="648b0-108">On the **Request** page, select **Send loan asset**.</span></span>
4. <span data-ttu-id="648b0-109">选择资产，然后输入预期返回日期。</span><span class="sxs-lookup"><span data-stu-id="648b0-109">Select the asset, and enter the expected return date.</span></span>
5. <span data-ttu-id="648b0-110">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="648b0-110">Select **OK**.</span></span>

> [!NOTE]
> - <span data-ttu-id="648b0-111">仅当有相同资产类型的资产时，才可以发送出借资产。</span><span class="sxs-lookup"><span data-stu-id="648b0-111">You can send a loan asset only if an asset of the same asset type is available.</span></span>
> - <span data-ttu-id="648b0-112">出借的资产必须有允许其用作出借资产的资产生命周期状态，如 **InStorage**。</span><span class="sxs-lookup"><span data-stu-id="648b0-112">The asset that you loan must have an asset lifecycle state that allows it to be used as a loan asset, such as **InStorage**.</span></span> <span data-ttu-id="648b0-113">登记资产出借时，将把资产的资产生命周期状态自动更新为 **OnLoan** 之类状态。</span><span class="sxs-lookup"><span data-stu-id="648b0-113">When the asset loan is registered, the asset lifecycle state of the asset is automatically updated to, for example, **OnLoan**.</span></span>

<span data-ttu-id="648b0-114">若要查看您已出借给其他位置或客户的所有资产的列表，请选择**资产管理** \> **常用** \> **资产出借** \> **所有资产出借**。</span><span class="sxs-lookup"><span data-stu-id="648b0-114">To view a list of all the assets that you've loaned to other locations or customers, select **Asset management** \> **Common** \> **Asset loan** \> **All asset loans**.</span></span> <span data-ttu-id="648b0-115">如果为资产选中了**已结束**复选框，则已将资产登记为已退给公司。</span><span class="sxs-lookup"><span data-stu-id="648b0-115">If the **Ended** check box is selected for an asset, the asset has been registered as returned to your company.</span></span>

![管理维护请求](media/06-manage-maintenance-requests.png)

<span data-ttu-id="648b0-117">在**有效资产出借**页上，可查看尚未退给您的公司的所有出借资产的列表。</span><span class="sxs-lookup"><span data-stu-id="648b0-117">On the **Active asset loans** page, you can view a list of all the loan assets that haven't yet been returned to your company.</span></span>

## <a name="register-loan-assets-as-returned"></a><span data-ttu-id="648b0-118">将出借资产登记为已退回</span><span class="sxs-lookup"><span data-stu-id="648b0-118">Register loan assets as returned</span></span>

1. <span data-ttu-id="648b0-119">选择**资产管理** \> **常用** \> **资产出借** \> **有效资产出借**。</span><span class="sxs-lookup"><span data-stu-id="648b0-119">Select **Asset management** \> **Common** \> **Asset loan** \> **Active asset loans**.</span></span>
2. <span data-ttu-id="648b0-120">选择登记为已退回的资产出借，然后选择**退回资产出借**。</span><span class="sxs-lookup"><span data-stu-id="648b0-120">Select the asset loan to register as returned, and then select **Return asset loan**.</span></span>
3. <span data-ttu-id="648b0-121">在**已退回**字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="648b0-121">In the **Returned** field, enter the date and time.</span></span>
4. <span data-ttu-id="648b0-122">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="648b0-122">Select **OK**.</span></span>
5. <span data-ttu-id="648b0-123">刷新**有效资产出借**列表页，然后注意列表中不再显示该资产出借。</span><span class="sxs-lookup"><span data-stu-id="648b0-123">Refresh the **Active asset loans** list page, and notice that the asset loan no longer appears in the list.</span></span>

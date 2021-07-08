---
title: 为全球库存核算启用 Power BI
description: 本主题介绍了如何为全球库存核算启用 Microsoft Power BI。
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d7979ed18b98ee6133774cd91bc866d6fca92d5f
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273119"
---
# <a name="enable-power-bi-for-global-inventory-accounting"></a><span data-ttu-id="0e6a5-103">为全球库存核算启用 Power BI</span><span class="sxs-lookup"><span data-stu-id="0e6a5-103">Enable Power BI for Global Inventory Accounting</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="0e6a5-104">您可以将磁贴、仪表板和报表从 [PowerBI.com](https://powerbi.com/) 帐户固定到 Microsoft Dynamics 365 应用程序工作区。</span><span class="sxs-lookup"><span data-stu-id="0e6a5-104">You can pin tiles, dashboards, and reports from your [PowerBI.com](https://powerbi.com/) account to your Microsoft Dynamics 365 application workspace.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0e6a5-105">先决条件</span><span class="sxs-lookup"><span data-stu-id="0e6a5-105">Prerequisites</span></span>

<span data-ttu-id="0e6a5-106">必须具备以下先决条件才能启用 Power BI 报告：</span><span class="sxs-lookup"><span data-stu-id="0e6a5-106">The following prerequisites must be in place before you can enable Power BI reporting:</span></span>

- <span data-ttu-id="0e6a5-107">您必须是 Dynamics 365 应用程序中的系统管理员。</span><span class="sxs-lookup"><span data-stu-id="0e6a5-107">You must be a system administrator in the Dynamics 365 application.</span></span>
- <span data-ttu-id="0e6a5-108">您必须具有 [PowerBI.com](https://powerbi.com/) 帐户。</span><span class="sxs-lookup"><span data-stu-id="0e6a5-108">You must have a [PowerBI.com](https://powerbi.com/) account.</span></span>
- <span data-ttu-id="0e6a5-109">您在 Power BI 帐户中必须至少有一个仪表板和一个报表。</span><span class="sxs-lookup"><span data-stu-id="0e6a5-109">You must have at least one dashboard and one report in your Power BI account.</span></span>
- <span data-ttu-id="0e6a5-110">您必须是 Azure Active Directory (Azure AD) 帐户的管理员。</span><span class="sxs-lookup"><span data-stu-id="0e6a5-110">You must be an administrator for your Azure Active Directory (Azure AD) account.</span></span>
- <span data-ttu-id="0e6a5-111">Azure AD 域必须与您用于 [PowerBI.com](https://powerbi.com/) 帐户的域相同。</span><span class="sxs-lookup"><span data-stu-id="0e6a5-111">The Azure AD domain must be the same domain that you used for your [PowerBI.com](https://powerbi.com/) account.</span></span>

## <a name="setup"></a><span data-ttu-id="0e6a5-112">设置</span><span class="sxs-lookup"><span data-stu-id="0e6a5-112">Setup</span></span>

<span data-ttu-id="0e6a5-113">若要设置 Power BI 集成，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="0e6a5-113">To set up the Power BI integration, follow these steps.</span></span>

1. <span data-ttu-id="0e6a5-114">登录到 [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index)。</span><span class="sxs-lookup"><span data-stu-id="0e6a5-114">Sign in to [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span></span>
1. <span data-ttu-id="0e6a5-115">转到 **共用资产库**，选择 **Power BI 报表模型** 作为资产类型，然后下载 **全球库存核算** 包。</span><span class="sxs-lookup"><span data-stu-id="0e6a5-115">Go to **Shared asset library**, select **Power BI report model** as the asset type, and download the **Global Inventory Accounting** package.</span></span> 
1. <span data-ttu-id="0e6a5-116">登录到 [PowerBI.com](https://app.powerbi.com/)，，然后通过执行以下步骤上传 **全球库存核算** Power BI 报表文件：</span><span class="sxs-lookup"><span data-stu-id="0e6a5-116">Sign in to [PowerBI.com](https://app.powerbi.com/), and upload the **Global Inventory Accounting** Power BI report file by following these steps:</span></span>

    1. <span data-ttu-id="0e6a5-117">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="0e6a5-117">Select **New**.</span></span>
    1. <span data-ttu-id="0e6a5-118">选择 **上传文件**。</span><span class="sxs-lookup"><span data-stu-id="0e6a5-118">Select **Upload a file**.</span></span>
    1. <span data-ttu-id="0e6a5-119">选择 **全球库存核算** Power BI 报表文件。</span><span class="sxs-lookup"><span data-stu-id="0e6a5-119">Select the **Global Inventory Accounting** Power BI report file.</span></span>

1. <span data-ttu-id="0e6a5-120">通过执行以下步骤配置 **全球库存核算** Power BI 报表：</span><span class="sxs-lookup"><span data-stu-id="0e6a5-120">Configure the **Global Inventory Accounting** Power BI report by following these steps:</span></span>

    1. <span data-ttu-id="0e6a5-121">转到 **我的工作区**，查找全球库存核算的数据集，然后在 **选项** 菜单上，选择 **设置**。</span><span class="sxs-lookup"><span data-stu-id="0e6a5-121">Go to **My workspace**, find the dataset for Global Inventory Accounting, and then, on the **Options** menu, select **Settings**.</span></span>
    1. <span data-ttu-id="0e6a5-122">在 **全球库存核算的设置** 中，展开 **参数**，并根据需要更新所有参数。</span><span class="sxs-lookup"><span data-stu-id="0e6a5-122">In **Settings for Global inventory accounting**, expand **Parameters**, and update all parameters as required.</span></span>

1. <span data-ttu-id="0e6a5-123">如[配置 PowerBI.com 集成](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process)中所述注册应用程序。</span><span class="sxs-lookup"><span data-stu-id="0e6a5-123">Register the application as described in [Configure PowerBI.com integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process).</span></span>
1. <span data-ttu-id="0e6a5-124">通过执行以下步骤将 **全球库存核算** Power BI 报表文件集成到 Dynamics 365 Supply Chain Management 中：</span><span class="sxs-lookup"><span data-stu-id="0e6a5-124">Integrate the **Global Inventory Accounting** Power BI report file into Dynamics 365 Supply Chain Management by following these steps:</span></span>

    1. <span data-ttu-id="0e6a5-125">转到 **系统管理 \> 设置 \> PowerBI.com 配置**。</span><span class="sxs-lookup"><span data-stu-id="0e6a5-125">Go to **System administration \> Setup \> PowerBI.com configuration**.</span></span>
    1. <span data-ttu-id="0e6a5-126">选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="0e6a5-126">Select **Edit**.</span></span>
    1. <span data-ttu-id="0e6a5-127">选择 **启用 PowerBI.Com 集成**。</span><span class="sxs-lookup"><span data-stu-id="0e6a5-127">Select **Enable PowerBI.Com integration**.</span></span>
    1. <span data-ttu-id="0e6a5-128">在 **应用程序 ID** 字段中，输入应用程序 ID。</span><span class="sxs-lookup"><span data-stu-id="0e6a5-128">In the **Application ID** field, enter the application ID.</span></span>
    1. <span data-ttu-id="0e6a5-129">在 **应用程序密钥** 字段中，输入应用程序密钥。</span><span class="sxs-lookup"><span data-stu-id="0e6a5-129">In the **Application key** field, enter the application key.</span></span>
    1. <span data-ttu-id="0e6a5-130">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="0e6a5-130">Select **Save**.</span></span>

1. <span data-ttu-id="0e6a5-131">刷新页面，以便显示 Power BI 登录对话框。</span><span class="sxs-lookup"><span data-stu-id="0e6a5-131">Refresh the page so that the Power BI sign-in dialog box appears.</span></span>
1. <span data-ttu-id="0e6a5-132">在 **选项** 选项卡上，选择 **打开报表目录**，然后选择您之前上传的 **全球库存核算** Power BI 报表文件。</span><span class="sxs-lookup"><span data-stu-id="0e6a5-132">On the **Options** tab, select **Open report catalog**, and then select the **Global Inventory Accounting** Power BI report file that you uploaded earlier.</span></span>
1. <span data-ttu-id="0e6a5-133">刷新该页面。</span><span class="sxs-lookup"><span data-stu-id="0e6a5-133">Refresh the page.</span></span> <span data-ttu-id="0e6a5-134">您应该会看到您的报表已添加。</span><span class="sxs-lookup"><span data-stu-id="0e6a5-134">You should see that your report has been added.</span></span>
1. <span data-ttu-id="0e6a5-135">在 **Power BI 报表** 下，选择 **全球库存核算** 链接。</span><span class="sxs-lookup"><span data-stu-id="0e6a5-135">Under **Power BI reports**, select the **Global Inventory Accounting** link.</span></span>

<span data-ttu-id="0e6a5-136">有关详细信息，请参阅[配置 PowerBI.com 集成](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md)。</span><span class="sxs-lookup"><span data-stu-id="0e6a5-136">For more information, see [Configure PowerBI.com integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).</span></span>

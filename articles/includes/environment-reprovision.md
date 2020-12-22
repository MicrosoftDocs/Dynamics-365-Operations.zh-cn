---
ms.openlocfilehash: f6bf4b6c946ebc63d3d84140f762cd4b789deb03
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4458516"
---
<span data-ttu-id="3741f-101">在环境之间复制数据库时，您需要先运行环境重新配置工具才能使复制的数据库完全正常运行，从而确保所有 Commerce 组件都保持最新。</span><span class="sxs-lookup"><span data-stu-id="3741f-101">When copying a database between environments, you will need to run the environment re-provisioning tool before the copied database is fully functional, to ensure that all Commerce components are up-to-date.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3741f-102">无论您是否使用 Commerce 组件，我们都建议您运行此过程，因为所有环境都包含 Commerce 功能。</span><span class="sxs-lookup"><span data-stu-id="3741f-102">We recommend that you run this procedure whether you are using Commerce components or not, because Commerce functionality is included in all environments.</span></span> 

<span data-ttu-id="3741f-103">在继续之前，必须确保满足以下先决条件：</span><span class="sxs-lookup"><span data-stu-id="3741f-103">Before you continue, you must make sure that the following prerequisites are met:</span></span>
1. <span data-ttu-id="3741f-104">如果要升级到 2017 年 7 月版本（也称为 7.2 版）7.2.11792.56024，请先在目标环境中应用以下应用程序 X++ 修补程序，然后再在该环境中运行数据升级。</span><span class="sxs-lookup"><span data-stu-id="3741f-104">If you are upgrading to the July 2017 release (also known as 7.2) 7.2.11792.56024, apply the following application X++ hotfixes in the destination environment before running the data upgrade in that environment.</span></span> <span data-ttu-id="3741f-105">这些操作可以预防在数据升级期间出现各种错误：</span><span class="sxs-lookup"><span data-stu-id="3741f-105">These will prevent various errors occurring during the data upgrade:</span></span>

    - <span data-ttu-id="3741f-106">KB 4036156 - Retail 次要版本升级 -“未设置变型编号规则。”</span><span class="sxs-lookup"><span data-stu-id="3741f-106">KB 4036156 - Retail minor version upgrade - 'Variant number sequence is not set.'</span></span> <span data-ttu-id="3741f-107">此修复程序包还包括 KB 4035399 和 KB 4035751。</span><span class="sxs-lookup"><span data-stu-id="3741f-107">This fix package also includes KB 4035399 and KB 4035751.</span></span> <span data-ttu-id="3741f-108">请注意，您必须至少拥有 Platform Update 9 才能使用此程序包。</span><span class="sxs-lookup"><span data-stu-id="3741f-108">Note that you must have a minimum of Platform Update 9 to use this package.</span></span> <span data-ttu-id="3741f-109">如果您不确定，请安装最新的二进制文件。</span><span class="sxs-lookup"><span data-stu-id="3741f-109">If you are unsure, install the latest binaries.</span></span>
    
2. <span data-ttu-id="3741f-110">如果要从 Microsoft Dynamics AX 2012 升级，请先在目标环境中安装以下应用程序 X++ 修补程序，然后再运行数据升级：</span><span class="sxs-lookup"><span data-stu-id="3741f-110">If you are upgrading from Microsoft Dynamics AX 2012, install the following application X++ fixes in the destination environment before you run the data upgrade:</span></span>
    - <span data-ttu-id="3741f-111">KB 4033183 - Dynamics AX 2012 R2 或 Dynamics AX 2012 R3 Pre-CU8 非零售升级失败，dbo.RETAILTILLLAYOUTZONE 未找到对象。</span><span class="sxs-lookup"><span data-stu-id="3741f-111">KB 4033183 - Dynamics AX 2012 R2 or Dynamics AX 2012 R3 Pre-CU8 non-retail upgrade fails with Object not found for dbo.RETAILTILLLAYOUTZONE.</span></span>
    - <span data-ttu-id="3741f-112">KB 4040692 - Dynamics AX 2012 R3 至 Microsoft Dynamics 365 for Operations 7.2 升级因 SalesLineIdx 上的 RetailSalesLine 重复索引失败。</span><span class="sxs-lookup"><span data-stu-id="3741f-112">KB 4040692 - Dynamics AX 2012 R3 to Microsoft Dynamics 365 for Operations 7.2 upgrade fails on RetailSalesLine duplicate index on SalesLineIdx.</span></span>
    - <span data-ttu-id="3741f-113">KB 4035490 - GeneralJournalAccountEntry MainAccount 字段升级脚本出现性能问题。</span><span class="sxs-lookup"><span data-stu-id="3741f-113">KB 4035490 - Performance issue with GeneralJournalAccountEntry MainAccount field upgrade script.</span></span>


<span data-ttu-id="3741f-114">请按照以下步骤运行环境重新配置工具。</span><span class="sxs-lookup"><span data-stu-id="3741f-114">Follow these steps to run the Environment reprovisioning tool.</span></span>

1. <span data-ttu-id="3741f-115">在共用资产库中，选择 **软件可部署包**。</span><span class="sxs-lookup"><span data-stu-id="3741f-115">In the Shared asset library, select **Software deployable package**.</span></span>
2. <span data-ttu-id="3741f-116">下载环境重新配置工具。</span><span class="sxs-lookup"><span data-stu-id="3741f-116">Download the Environment reprovisioning tool.</span></span>
3. <span data-ttu-id="3741f-117">在项目的资产库中，选择 **软件可部署包**。</span><span class="sxs-lookup"><span data-stu-id="3741f-117">In the asset library for your project, select **Software deployable package**.</span></span>
4. <span data-ttu-id="3741f-118">选择 **新建** 以创建新程序包。</span><span class="sxs-lookup"><span data-stu-id="3741f-118">Select **New** to create a new package.</span></span>
5. <span data-ttu-id="3741f-119">为程序包输入名称和描述。</span><span class="sxs-lookup"><span data-stu-id="3741f-119">Enter a name and description for the package.</span></span> <span data-ttu-id="3741f-120">您可以使用 **环境重新配置工具** 作为程序包名称。</span><span class="sxs-lookup"><span data-stu-id="3741f-120">You can use **Environment reprovisioning tool** as the package name.</span></span>
6. <span data-ttu-id="3741f-121">上载之前下载的程序包。</span><span class="sxs-lookup"><span data-stu-id="3741f-121">Upload the package that you downloaded earlier.</span></span>
7. <span data-ttu-id="3741f-122">在目标环境的 **环境详情** 页面，选择 **维护** > **应用更新**。</span><span class="sxs-lookup"><span data-stu-id="3741f-122">On the **Environment details** page for your target environment, select **Maintain** > **Apply updates**.</span></span>
8. <span data-ttu-id="3741f-123">选择您之前上载的环境重新配置工具，然后选择 **应用** 以应用程序包。</span><span class="sxs-lookup"><span data-stu-id="3741f-123">Select the Environment reprovisioning tool that you uploaded earlier, and then select **Apply** to apply the package.</span></span>
9. <span data-ttu-id="3741f-124">监控程序包部署的进度。</span><span class="sxs-lookup"><span data-stu-id="3741f-124">Monitor the progress of the package deployment.</span></span> 

<span data-ttu-id="3741f-125">有关如何应用可部署包的更多信息，请参阅[应用可部署包](../deployment/create-apply-deployable-package.md)。</span><span class="sxs-lookup"><span data-stu-id="3741f-125">For more information about how to apply a deployable package, see [Apply a deployable package](../deployment/create-apply-deployable-package.md).</span></span> <span data-ttu-id="3741f-126">有关如何手动应用可部署包的更多信息，请参阅[安装可部署包](../deployment/install-deployable-package.md)。</span><span class="sxs-lookup"><span data-stu-id="3741f-126">For more information about how to manually apply a deployable package, see [Install a deployable package](../deployment/install-deployable-package.md).</span></span>

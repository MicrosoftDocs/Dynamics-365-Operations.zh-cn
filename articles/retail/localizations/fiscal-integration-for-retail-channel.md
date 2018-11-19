---
title: "零售渠道的会计集成"
description: "此主题概要介绍 Retail POS 的会计集成。"
author: josaw
manager: annbe
ms.date: 11/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: c852d095505abecbd44d29e9e7b53875e9069def
ms.contentlocale: zh-cn
ms.lasthandoff: 11/01/2018

---
# <a name="fiscal-integration-for-retail-channel"></a><span data-ttu-id="c4012-103">零售渠道的会计集成</span><span class="sxs-lookup"><span data-stu-id="c4012-103">Fiscal integration for Retail channel</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c4012-104">此主题是 Microsoft Dynamics 365 for Retail 中提供的会计集成功能的概述。</span><span class="sxs-lookup"><span data-stu-id="c4012-104">This topic is an overview of the fiscal integration functionality that is available in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="c4012-105">会计功能是用于支持旨在防止零售业欺诈的地方财政法的框架。</span><span class="sxs-lookup"><span data-stu-id="c4012-105">The fiscal integration functionality is a framework designed to support local fiscal laws that are aimed to prevent fraud in the Retail industry.</span></span> <span data-ttu-id="c4012-106">可能通过使用会计集成应对的典型场景包括：</span><span class="sxs-lookup"><span data-stu-id="c4012-106">Typical scenarios that could be covered by using fiscal integration include:</span></span>

- <span data-ttu-id="c4012-107">打印财务收据并提供给客户。</span><span class="sxs-lookup"><span data-stu-id="c4012-107">Printing a fiscal receipt and giving it to the customer.</span></span>
- <span data-ttu-id="c4012-108">为向主管机构提供的外部服务提交有关在 POS 上执行的销售和退货的信息提供保护。</span><span class="sxs-lookup"><span data-stu-id="c4012-108">Securing the submission of the information related to sales and returns performed on POS to an external service provided by the authority.</span></span>
- <span data-ttu-id="c4012-109">利用主管机构授权的数字签名使用保护数据。</span><span class="sxs-lookup"><span data-stu-id="c4012-109">Using data protection with a digital signature authorized by the authority.</span></span>

<span data-ttu-id="c4012-110">此主题提供有关设置会计集成以便用户可以执行以下任务的指南。</span><span class="sxs-lookup"><span data-stu-id="c4012-110">This topic provides guidelines for setting up fiscal integration so users can perform the following tasks.</span></span> 

- <span data-ttu-id="c4012-111">配置会计连接器，其是用于会计登记目的的税控设备或服务，如会计数据的保存、数字签名和安全提交。</span><span class="sxs-lookup"><span data-stu-id="c4012-111">Configure fiscal connectors, which are fiscal devices or services used for fiscal registration purposes like saving, digital signatures, and secured submission of fiscal data.</span></span>
- <span data-ttu-id="c4012-112">配置单据提供程序，其定义会计单据生成的输出方法和算法。</span><span class="sxs-lookup"><span data-stu-id="c4012-112">Configure the document provider, which defines an output method and an algorithm of fiscal document generation.</span></span>
- <span data-ttu-id="c4012-113">配置会计登记流程，其定义步骤顺序和每个步骤中使用的连接器组。</span><span class="sxs-lookup"><span data-stu-id="c4012-113">Configure the fiscal registration process, which is defines a sequence of steps and a group of connectors used on each step.</span></span>
- <span data-ttu-id="c4012-114">将会计登记流程分配到 POS 功能配置文件。</span><span class="sxs-lookup"><span data-stu-id="c4012-114">Assign fiscal registration processes to POS functionality profiles.</span></span>
- <span data-ttu-id="c4012-115">分配连接器技术配置文件，分配到硬件配置文件（对于本地会计连接器）或 POS 功能配置文件（对于其他会计连接器类型）。</span><span class="sxs-lookup"><span data-stu-id="c4012-115">Assign connector technical profiles, either to hardware profiles (for the local fiscal connectors) or to POS functionality profiles (for other fiscal connector types).</span></span>

## <a name="fiscal-integration-execution-flow"></a><span data-ttu-id="c4012-116">会计集成执行流</span><span class="sxs-lookup"><span data-stu-id="c4012-116">Fiscal integration execution flow</span></span>
<span data-ttu-id="c4012-117">以下场景显示通用会计集成执行流。</span><span class="sxs-lookup"><span data-stu-id="c4012-117">The following scenario shows the common fiscal integration execution flow.</span></span>

1. <span data-ttu-id="c4012-118">会计登记流程的初始化。</span><span class="sxs-lookup"><span data-stu-id="c4012-118">Initialization of the fiscal registration process.</span></span>
  
   <span data-ttu-id="c4012-119">在执行需要会计登记的一些操作后，例如，在零售交易记录完成后，会计登记流程将与当前的 POS 功能配置文件关联。</span><span class="sxs-lookup"><span data-stu-id="c4012-119">After performing some actions where fiscal registration is required, such as after a retail transaction has been concluded, the fiscal registration process is associated with the current POS functionality profile.</span></span>

1. <span data-ttu-id="c4012-120">搜索会计连接器。</span><span class="sxs-lookup"><span data-stu-id="c4012-120">Search for a fiscal connector.</span></span>
   
   <span data-ttu-id="c4012-121">对于会计登记流程中包括的每个会计登记步骤，系统将匹配会计连接器的列表。</span><span class="sxs-lookup"><span data-stu-id="c4012-121">For each fiscal registration step included in the fiscal registration process, the system matches the list of fiscal connectors.</span></span> <span data-ttu-id="c4012-122">这些连接器在指定的连接器组中包括功能配置文件，并且附带包含与当前硬件配置文件关联（对于仅为**本地**的连接器类型）或与当前的 POS 功能配置文件关联（对于其他连接器类型）。</span><span class="sxs-lookup"><span data-stu-id="c4012-122">These connectors have a functional profile included in the specified connector group, with a list of connectors that have a technical profile associated with the current hardware profile (for a connector type that equals **Local** only) or with the current POS functionality profile (for other connector types).</span></span>
   
1. <span data-ttu-id="c4012-123">执行会计集成。</span><span class="sxs-lookup"><span data-stu-id="c4012-123">Perform the fiscal integration.</span></span>

   <span data-ttu-id="c4012-124">系统执行与找到的连接器链接的程序集定义的所有必要操作。</span><span class="sxs-lookup"><span data-stu-id="c4012-124">The system executes all necessary actions defined by an assembly linked with the found connector.</span></span> <span data-ttu-id="c4012-125">这根据在此连接器的前一个步骤中找到的功能配置文件和技术配置文件的设置。</span><span class="sxs-lookup"><span data-stu-id="c4012-125">This is done in accordance with the settings of the functional profile and technical profile that were found on the previous step for this connector.</span></span>

## <a name="setup-needed-before-using-fiscal-integration"></a><span data-ttu-id="c4012-126">使用会计集成前所需的设置</span><span class="sxs-lookup"><span data-stu-id="c4012-126">Setup needed before using fiscal integration</span></span>
<span data-ttu-id="c4012-127">在使用会计集成功能之前，应定义以下设置：</span><span class="sxs-lookup"><span data-stu-id="c4012-127">Before using the fiscal integration functionality, you should define the following settings:</span></span>

- <span data-ttu-id="c4012-128">在**零售参数**页为会计功能配置文件编号定义编号规则。</span><span class="sxs-lookup"><span data-stu-id="c4012-128">Define the number sequence on the **Retail parameters** page for the fiscal functional profile number.</span></span>
  
- <span data-ttu-id="c4012-129">在**零售共享参数**页为以下引用定义编号规则：</span><span class="sxs-lookup"><span data-stu-id="c4012-129">Define the number sequences on the **Retail shared parameters** page for the following references:</span></span>
  
  - <span data-ttu-id="c4012-130">财政技术配置文件编号</span><span class="sxs-lookup"><span data-stu-id="c4012-130">Fiscal technical profile number</span></span>
  - <span data-ttu-id="c4012-131">财政连接器组编号</span><span class="sxs-lookup"><span data-stu-id="c4012-131">Fiscal connector group number</span></span>
  - <span data-ttu-id="c4012-132">登记流程编号</span><span class="sxs-lookup"><span data-stu-id="c4012-132">Registration process number</span></span>

- <span data-ttu-id="c4012-133">在**零售 >渠道设置 > 会计集成 > 会计连接器**中为您计划用于会计集成目的的每个设备或服务创建**会计连接器**。</span><span class="sxs-lookup"><span data-stu-id="c4012-133">Create a **Fiscal connector** in **Retail > Channel setup > Fiscal integration > Fiscal connectors** for each device or service that you plan to use for fiscal integration purposes.</span></span>

-  <span data-ttu-id="c4012-134">在**零售 > 渠道设置 > 会计集成 > 会计单据提供程序**中为所有会计连接器创建**会计单据提供程序**。</span><span class="sxs-lookup"><span data-stu-id="c4012-134">Create a **Fiscal document provider** in **Retail > Channel setup > Fiscal integration > Fiscal document providers** for all fiscal connectors.</span></span> <span data-ttu-id="c4012-135">数据映射被视为会计单据提供程序的一部分。</span><span class="sxs-lookup"><span data-stu-id="c4012-135">Data mapping is considered a part of the fiscal document provider.</span></span> <span data-ttu-id="c4012-136">若要为相同连接器设置不同的数据映射（如州特定法规），您应创建不同的会计单据提供程序。</span><span class="sxs-lookup"><span data-stu-id="c4012-136">To set up different data mappings for the same connector (like state-specific regulations), you should create different fiscal document providers.</span></span>

- <span data-ttu-id="c4012-137">在**零售 > 渠道设置 > 会计集成 > 连接器功能配置文件**中为每个会计单据提供程序创建**连接器功能配置文件**。</span><span class="sxs-lookup"><span data-stu-id="c4012-137">Create a **Connector functional profile** in **Retail > Channel setup > Fiscal integration > Connector functional profiles** for each fiscal document provider.</span></span>
  - <span data-ttu-id="c4012-138">选择连接器名称。</span><span class="sxs-lookup"><span data-stu-id="c4012-138">Select a connector name.</span></span>
  - <span data-ttu-id="c4012-139">选择单据提供程序。</span><span class="sxs-lookup"><span data-stu-id="c4012-139">Select a document provider.</span></span>
  - <span data-ttu-id="c4012-140">在**服务设置**选项卡上指定增值税税率设置。</span><span class="sxs-lookup"><span data-stu-id="c4012-140">Specify VAT rates settings on the **Service setup** tab.</span></span>
  - <span data-ttu-id="c4012-141">在**数据映射**选项卡上指定增值税代码映射和支付方式映射。</span><span class="sxs-lookup"><span data-stu-id="c4012-141">Specify VAT codes mapping and tender type mapping on the **Data mapping** tab.</span></span>

  #### <a name="examples"></a><span data-ttu-id="c4012-142">示例</span><span class="sxs-lookup"><span data-stu-id="c4012-142">Examples</span></span> 

  |  | <span data-ttu-id="c4012-143">格式</span><span class="sxs-lookup"><span data-stu-id="c4012-143">Format</span></span> | <span data-ttu-id="c4012-144">示例</span><span class="sxs-lookup"><span data-stu-id="c4012-144">Example</span></span> | 
  |--------|--------|--------|
  | <span data-ttu-id="c4012-145">增值税税率设置</span><span class="sxs-lookup"><span data-stu-id="c4012-145">VAT rates settings</span></span> | <span data-ttu-id="c4012-146">值 : VATrate</span><span class="sxs-lookup"><span data-stu-id="c4012-146">value : VATrate</span></span> | <span data-ttu-id="c4012-147">1 : 2000、2 : 1800</span><span class="sxs-lookup"><span data-stu-id="c4012-147">1 : 2000, 2 : 1800</span></span> |
  | <span data-ttu-id="c4012-148">增值税代码映射</span><span class="sxs-lookup"><span data-stu-id="c4012-148">VAT codes mapping</span></span> | <span data-ttu-id="c4012-149">VATcode : 值</span><span class="sxs-lookup"><span data-stu-id="c4012-149">VATcode : value</span></span> | <span data-ttu-id="c4012-150">vat20 : 1、vat18 : 2</span><span class="sxs-lookup"><span data-stu-id="c4012-150">vat20 : 1, vat18 : 2</span></span> |
  | <span data-ttu-id="c4012-151">支付方式映射</span><span class="sxs-lookup"><span data-stu-id="c4012-151">Tender types mapping</span></span> | <span data-ttu-id="c4012-152">TenderTyp : 值</span><span class="sxs-lookup"><span data-stu-id="c4012-152">TenderTyp : value</span></span> | <span data-ttu-id="c4012-153">现金 : 1、卡 : 2</span><span class="sxs-lookup"><span data-stu-id="c4012-153">Cash : 1, Card : 2</span></span> |

- <span data-ttu-id="c4012-154">在**零售 > 渠道设置 > 会计集成 > 会计连接器组**中创建**会计连接器组**。</span><span class="sxs-lookup"><span data-stu-id="c4012-154">Create **Fiscal connector groups** in **Retail > Channel setup > Fiscal integration > Fiscal connector group**.</span></span> <span data-ttu-id="c4012-155">连接器组是与会计连接器链接的功能配置文件的子集，会计连接器执行相同的功能，并在会计登记流程内用于同一个阶段。</span><span class="sxs-lookup"><span data-stu-id="c4012-155">A connector group is a subset of functional profiles linked with fiscal connectors that perform identical functions and are used at the same stage within a fiscal registration process.</span></span>

   - <span data-ttu-id="c4012-156">向连接器组添加功能配置文件。</span><span class="sxs-lookup"><span data-stu-id="c4012-156">Add functional profiles to the connector group.</span></span> <span data-ttu-id="c4012-157">在**功能配置文件**页单击**添加**并选择配置文件编号。</span><span class="sxs-lookup"><span data-stu-id="c4012-157">Click **Add** on the **Functional profiles** page and select a profile number.</span></span>
   - <span data-ttu-id="c4012-158">如果要暂停功能配置文件的使用，将**禁用**设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="c4012-158">If you want to suspend usage of the functional profile, set **Disable** to **Yes**.</span></span> 
   
     <span data-ttu-id="c4012-159">此更改只影响当前的连接器组。</span><span class="sxs-lookup"><span data-stu-id="c4012-159">This change affects the current connector group only.</span></span> <span data-ttu-id="c4012-160">您可以在其他连接器组中继续使用相同的功能配置文件。</span><span class="sxs-lookup"><span data-stu-id="c4012-160">You can continue using the same functional profile in other connector groups.</span></span>

     >[!NOTE]
     > <span data-ttu-id="c4012-161">在连接器组内，每个会计连接器只能有一个功能配置文件。</span><span class="sxs-lookup"><span data-stu-id="c4012-161">Within a connector group, each fiscal connector can only have one functional profile.</span></span>

- <span data-ttu-id="c4012-162">在**零售 > 渠道设置 > 会计集成 > 连接器技术配置文件**中为每个会计连接器创建**连接器技术配置文件**。</span><span class="sxs-lookup"><span data-stu-id="c4012-162">Create a **Connector technical profile** in **Retail > Channel setup > Fiscal integration > Connector technical profiles** for each fiscal connector.</span></span>
  - <span data-ttu-id="c4012-163">选择连接器名称。</span><span class="sxs-lookup"><span data-stu-id="c4012-163">Select a connector name.</span></span>
  - <span data-ttu-id="c4012-164">选择连接器类型：</span><span class="sxs-lookup"><span data-stu-id="c4012-164">Select a connector type:</span></span> 
      - <span data-ttu-id="c4012-165">**本地** - 在本地计算机上为安装的物理设备或应用程序设置此类型。</span><span class="sxs-lookup"><span data-stu-id="c4012-165">**Local** - Set this type for physical devices or applications installed on a local machine.</span></span>
      - <span data-ttu-id="c4012-166">**内部** - 为连接到 Retail Server 的税控设备和服务设置此类型。</span><span class="sxs-lookup"><span data-stu-id="c4012-166">**Internal** - Set this type for fiscal devices and services connected to Retail Server.</span></span>
      - <span data-ttu-id="c4012-167">**外部** - 用于税务主管机构提供的 Web 门户等外部会计服务。</span><span class="sxs-lookup"><span data-stu-id="c4012-167">**External** - For external fiscal services like a web-portal provided by a tax authority.</span></span>
    
  - <span data-ttu-id="c4012-168">在**连接**选项卡上指定设置。</span><span class="sxs-lookup"><span data-stu-id="c4012-168">Specify settings on the **Connection** tab.</span></span>

      
 >[!NOTE]
 > <span data-ttu-id="c4012-169">之前加载的更新的配置版本将同时为功能和技术配置文件加载。</span><span class="sxs-lookup"><span data-stu-id="c4012-169">An updated version of a configuration that was loaded earlier will be loaded for both functional and technical profiles.</span></span> <span data-ttu-id="c4012-170">如果合适的连接器或凭据提供程序已在使用，您将收到通知。</span><span class="sxs-lookup"><span data-stu-id="c4012-170">If an appropriate connector or document provider is already in use, you will be notified.</span></span> <span data-ttu-id="c4012-171">默认情况下，在功能和技术配置文件中手动进行的所有更改将被存储。</span><span class="sxs-lookup"><span data-stu-id="c4012-171">By default, all changes that have been made manually in functional and technical profiles will be stored.</span></span> <span data-ttu-id="c4012-172">要使用来自配置的一组默认参数覆盖这些配置文件，请单击**连接器功能配置文件**页和**连接器技术配置文件**页上的**更新**。</span><span class="sxs-lookup"><span data-stu-id="c4012-172">In order to override these profiles with the default set of parameters from a configuration, click **Update** on the **Connector functional profiles** page and **Connector technical profiles** page.</span></span>
 
- <span data-ttu-id="c4012-173">在**零售 > 渠道设置 > 会计集成 > 会计登记流程**中为每个会计集成的唯一流程创建**会计登记流程**。</span><span class="sxs-lookup"><span data-stu-id="c4012-173">Create a **Fiscal registration process** in **Retail > Channel setup > Fiscal integration > Fiscal registration processes** for each unique process of the fiscal integration.</span></span> <span data-ttu-id="c4012-174">登记流程由登记步骤的顺序和每个步骤中使用的连接器组定义。</span><span class="sxs-lookup"><span data-stu-id="c4012-174">A registration process is defined by the sequence of the registration steps and the connector group used on each step.</span></span> 
  
  - <span data-ttu-id="c4012-175">向流程添加登记步骤：</span><span class="sxs-lookup"><span data-stu-id="c4012-175">Add registration steps to the process:</span></span>
      - <span data-ttu-id="c4012-176">单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="c4012-176">Click **Add**.</span></span>
      - <span data-ttu-id="c4012-177">选择连接器类型。</span><span class="sxs-lookup"><span data-stu-id="c4012-177">Select a connector type.</span></span>
      
      >[!NOTE]
      > <span data-ttu-id="c4012-178">此字段定义系统将在技术配置文件中的哪个位置搜索连接器，在连接器类型为**本地**的硬件配置文件中，或者其他会计连接器类型的 POS 功能配置文件中。</span><span class="sxs-lookup"><span data-stu-id="c4012-178">This field defines where the system will search in a technical profile for the connector, either in hardware profiles for connector type **Local**, or in POS functionality profiles for other fiscal connector types.</span></span>
      
   - <span data-ttu-id="c4012-179">选择连接器组。</span><span class="sxs-lookup"><span data-stu-id="c4012-179">Select a connector group.</span></span>
   
     >[!NOTE]
     > <span data-ttu-id="c4012-180">单击**验证**检查登记流程结构的完整性。</span><span class="sxs-lookup"><span data-stu-id="c4012-180">Click **Validate** to check the integrity of the registration process structure.</span></span> <span data-ttu-id="c4012-181">建议在以下情况下进行验证：</span><span class="sxs-lookup"><span data-stu-id="c4012-181">It’s recommended that validations be made in the following cases:</span></span>
       >- <span data-ttu-id="c4012-182">对于在所有设置完成后的新登记流程，包括绑定到 POS 功能配置文件和硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="c4012-182">For a new registration process after all the settings are completed, including binding to POS functionality profiles and hardware profiles.</span></span>
       >- <span data-ttu-id="c4012-183">在对现有的登记流程进行更新后。</span><span class="sxs-lookup"><span data-stu-id="c4012-183">After making updates to an existing registration process.</span></span>

-  <span data-ttu-id="c4012-184">在**零售 > 渠道设置 > POS 设置 > POS 配置文件 > 功能配置文件**中将会计登记流程绑定到 POS 功能配置文件。</span><span class="sxs-lookup"><span data-stu-id="c4012-184">Bind fiscal registration processes to POS functionality profiles in **Retail > Channel setup > POS setup > POS profiles > Functionality profiles**.</span></span>
   - <span data-ttu-id="c4012-185">在**会计登记流程**选项卡上单击**编辑**并选择**流程编号**。</span><span class="sxs-lookup"><span data-stu-id="c4012-185">Click **Edit** and select a **Process number** on the **Fiscal registration process** tab.</span></span>
- <span data-ttu-id="c4012-186">在**零售 > 渠道设置 > POS 设置 > POS 配置文件 > 硬件配置文件**中将连接器技术配置文件绑定到硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="c4012-186">Bind the connector technical profiles to the hardware profiles in **Retail > Channel setup > POS setup > POS profiles > Hardware profiles**.</span></span>
   - <span data-ttu-id="c4012-187">单击**编辑**，然后单击**会计技术配置文件** 选项卡上的**新建**。</span><span class="sxs-lookup"><span data-stu-id="c4012-187">Click **Edit**, then click **New** on the **Fiscal technical profile** tab.</span></span>
   - <span data-ttu-id="c4012-188">在**配置文件编号**字段中选择连接器技术配置文件。</span><span class="sxs-lookup"><span data-stu-id="c4012-188">Select a connector technical profile in the **Profile number** field.</span></span>
   
     >[!NOTE]
     > <span data-ttu-id="c4012-189">您可以将多个技术配置文件添加到硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="c4012-189">You can add several technical profiles to a hardware profile.</span></span> <span data-ttu-id="c4012-190">但是，如果硬件配置文件具有与任何连接器组的交集时，这不受支持。</span><span class="sxs-lookup"><span data-stu-id="c4012-190">However, this is not supported if a hardware profile has more than one intersection with any connector group.</span></span> <span data-ttu-id="c4012-191">为了避免错误设置，建议您在更新所有硬件配置文件后验证登记流程。</span><span class="sxs-lookup"><span data-stu-id="c4012-191">To avoid incorrect settings, it’s recommended that you validate the registration process after updating all the hardware profiles.</span></span>


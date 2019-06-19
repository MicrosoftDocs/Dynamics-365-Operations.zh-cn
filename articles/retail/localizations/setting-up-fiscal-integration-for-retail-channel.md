---
title: 设置零售渠道的会计整合
description: 此主题提供为零售渠道设置会计整合功能的指南。
author: josaw
manager: annbe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: fda94e77480b9d9455fc0e214e43772ab2921f2d
ms.sourcegitcommit: ffc37f7c2a63bada3055f37856a30424040bc9a3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/16/2019
ms.locfileid: "1577892"
---
# <a name="set-up-the-fiscal-integration-for-retail-channels"></a><span data-ttu-id="ff827-103">设置零售渠道的会计整合</span><span class="sxs-lookup"><span data-stu-id="ff827-103">Set up the fiscal integration for Retail channels</span></span>

[!include [banner](../includes/banner.md)]

## <a name="introduction"></a><span data-ttu-id="ff827-104">简介</span><span class="sxs-lookup"><span data-stu-id="ff827-104">Introduction</span></span>

<span data-ttu-id="ff827-105">此主题提供为零售渠道设置会计整合功能的指南。</span><span class="sxs-lookup"><span data-stu-id="ff827-105">This topic provides guidelines for setting up the fiscal integration functionality for Retail channels.</span></span> <span data-ttu-id="ff827-106">有关会计整合的详细信息，请参阅[零售渠道的会计整合概览](fiscal-integration-for-retail-channel.md)。</span><span class="sxs-lookup"><span data-stu-id="ff827-106">For more information about the fiscal integration, see [Overview of fiscal integration for Retail channels](fiscal-integration-for-retail-channel.md).</span></span>

<span data-ttu-id="ff827-107">设置会计整合的流程包含以下任务：</span><span class="sxs-lookup"><span data-stu-id="ff827-107">The process of setting up the fiscal integration includes the following tasks:</span></span>

1. <span data-ttu-id="ff827-108">配置代表用于会计登记目的的会计设备或服务（如税控打印机）的会计连接器。</span><span class="sxs-lookup"><span data-stu-id="ff827-108">Configure fiscal connectors that represent fiscal devices or services that are used for fiscal registration purposes, such as fiscal printers.</span></span>
2. <span data-ttu-id="ff827-109">配置生成会计连接器将在会计设备或服务中登记的会计单据的单据提供程序。</span><span class="sxs-lookup"><span data-stu-id="ff827-109">Configure document providers that generate fiscal documents that will be registered in fiscal devices or services by fiscal connectors.</span></span>
3. <span data-ttu-id="ff827-110">配置定义会计登记步骤的会计登记流程和用于每个步骤的会计连接器和会计单据提供程序。</span><span class="sxs-lookup"><span data-stu-id="ff827-110">Configure the fiscal registration process that defines a sequence of fiscal registration steps and the fiscal connectors and fiscal document providers that are used for each step.</span></span>
4. <span data-ttu-id="ff827-111">将会计登记流程分配到销售点 (POS) 功能配置文件。</span><span class="sxs-lookup"><span data-stu-id="ff827-111">Assign the fiscal registration process to point of sale (POS) functionality profiles.</span></span>
5. <span data-ttu-id="ff827-112">将连接器技术配置文件分配到硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="ff827-112">Assign connector technical profiles to hardware profiles.</span></span>

## <a name="set-up-a-fiscal-registration-process"></a><span data-ttu-id="ff827-113">设置会计登记流程</span><span class="sxs-lookup"><span data-stu-id="ff827-113">Set up a fiscal registration process</span></span>

<span data-ttu-id="ff827-114">在使用会计集成功能之前，应配置以下设置。</span><span class="sxs-lookup"><span data-stu-id="ff827-114">Before you use the fiscal integration functionality, you should configure the following settings.</span></span>

1. <span data-ttu-id="ff827-115">更新零售参数。</span><span class="sxs-lookup"><span data-stu-id="ff827-115">Update retail parameters.</span></span>

    1. <span data-ttu-id="ff827-116">在**零售共享参数**页上，在**常规**选项卡上，将**启用会计整合**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="ff827-116">On the **Retail shared parameters** page, on the **General** tab, set the **Enable fiscal integration** option to **Yes**.</span></span> <span data-ttu-id="ff827-117">在**编号规则**选项卡上，定义以下参考的编号规则：</span><span class="sxs-lookup"><span data-stu-id="ff827-117">On the **Number sequences** tab, define the number sequences for the following references:</span></span>

        - <span data-ttu-id="ff827-118">财政技术配置文件编号</span><span class="sxs-lookup"><span data-stu-id="ff827-118">Fiscal technical profile number</span></span>
        - <span data-ttu-id="ff827-119">财政连接器组编号</span><span class="sxs-lookup"><span data-stu-id="ff827-119">Fiscal connector group number</span></span>
        - <span data-ttu-id="ff827-120">登记流程编号</span><span class="sxs-lookup"><span data-stu-id="ff827-120">Registration process number</span></span>

    2. <span data-ttu-id="ff827-121">在**零售参数**页上，为会计功能配置文件编号定义编号规则。</span><span class="sxs-lookup"><span data-stu-id="ff827-121">On the **Retail parameters** page, define the number sequence for the fiscal functional profile number.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ff827-122">编号规则是可选的。</span><span class="sxs-lookup"><span data-stu-id="ff827-122">Number sequences are optional.</span></span> <span data-ttu-id="ff827-123">所有会计整合实体的编号均可以从编号规则生成或手动生成。</span><span class="sxs-lookup"><span data-stu-id="ff827-123">Numbers for all fiscal integration entities can be generated either from number sequences or manually.</span></span>

2. <span data-ttu-id="ff827-124">上载会计连接器和会计单据提供程序的配置。</span><span class="sxs-lookup"><span data-stu-id="ff827-124">Upload configurations of fiscal connectors and fiscal document providers.</span></span>

    <span data-ttu-id="ff827-125">会计单据提供程序负责生成代表零售交易和事件的会计单据，这些交易和事件以用于与会计设备或服务交互的格式在 POS 上登记。</span><span class="sxs-lookup"><span data-stu-id="ff827-125">A fiscal document provider is responsible for generating fiscal documents that represent retail transactions and events that are registered on the POS in a format that is also used for the interaction with a fiscal device or service.</span></span> <span data-ttu-id="ff827-126">例如，会计单据提供程序可能生成 XML 格式的财务收据的表示形式。</span><span class="sxs-lookup"><span data-stu-id="ff827-126">For example, a fiscal document provider might generate a representation of a fiscal receipt in an XML format.</span></span>

    <span data-ttu-id="ff827-127">会计连接器负责与会计设备或服务的通信。</span><span class="sxs-lookup"><span data-stu-id="ff827-127">A fiscal connector is responsible for the communication with a fiscal device or service.</span></span> <span data-ttu-id="ff827-128">例如，会计连接器可能将会计单据提供程序以 XML 格式创建的财务收据发送到税控打印机。</span><span class="sxs-lookup"><span data-stu-id="ff827-128">For example, a fiscal connector might send a fiscal receipt that a fiscal document provider created in an XML format to a fiscal printer.</span></span> <span data-ttu-id="ff827-129">有关会计整合组件的更多详细信息，请参阅[会计设备的会计整合流程和会计整合示例](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices)。</span><span class="sxs-lookup"><span data-stu-id="ff827-129">For more details about fiscal integration components, see [Fiscal registration process and fiscal integration samples for fiscal devices](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices).</span></span>

    1. <span data-ttu-id="ff827-130">在**会计连接器**页（**零售  \> 渠道设置 \> 会计集成 \>会计连接器**）上，为您计划用于会计整合目的的每个设备或服务上载 XML 配置。</span><span class="sxs-lookup"><span data-stu-id="ff827-130">On the **Fiscal connectors** page (**Retail \> Channel setup \> Fiscal integration \> Fiscal connectors**), upload an XML configuration for each device or service that you plan to use for fiscal integration purposes.</span></span>

        > [!TIP]
        > <span data-ttu-id="ff827-131">通过选择**查看**，您可以查看与当前的会计连接器相关的所有功能和技术配置文件。</span><span class="sxs-lookup"><span data-stu-id="ff827-131">By selecting **View**, you can view all functional and technical profiles that are related to the current fiscal connector.</span></span>

    2. <span data-ttu-id="ff827-132">在**会计单据提供程序**页（**零售  \> 渠道设置 \> 会计集成 \>会计单据提供程序**）上，为您计划使用的每个设备或服务上载 XML 配置。</span><span class="sxs-lookup"><span data-stu-id="ff827-132">On the **Fiscal document providers** page (**Retail \> Channel setup \> Fiscal integration \> Fiscal document providers**), upload an XML configuration for each device or service that you plan to use.</span></span>

        > [!TIP]
        > <span data-ttu-id="ff827-133">通过选择**查看**，您可以查看与当前的会计单据提供程序相关的所有功能配置文件。</span><span class="sxs-lookup"><span data-stu-id="ff827-133">By selecting **View**, you can view all functional profiles that are related to the current fiscal document provider.</span></span>

    <span data-ttu-id="ff827-134">有关会计连接器和会计单据提供程序的示例，请参阅 [Retail SDK 中的会计整合示例](fiscal-integration-for-retail-channel.md#fiscal-integration-samples-in-the-retail-sdk)。</span><span class="sxs-lookup"><span data-stu-id="ff827-134">For examples of configurations of fiscal connectors and fiscal document providers, see [Fiscal integration samples in the Retail SDK](fiscal-integration-for-retail-channel.md#fiscal-integration-samples-in-the-retail-sdk).</span></span>

    > [!NOTE]
    > <span data-ttu-id="ff827-135">数据映射被视为会计单据提供程序的一部分。</span><span class="sxs-lookup"><span data-stu-id="ff827-135">Data mapping is considered part of a fiscal document provider.</span></span> <span data-ttu-id="ff827-136">若要为相同连接器设置不同的数据映射（例如，州特定法规），您应创建不同的会计单据提供程序。</span><span class="sxs-lookup"><span data-stu-id="ff827-136">To set up different data mappings for the same connector (for example, state-specific regulations), you should create different fiscal document providers.</span></span>

3. <span data-ttu-id="ff827-137">创建连接器功能配置文件和连接器技术配置文件。</span><span class="sxs-lookup"><span data-stu-id="ff827-137">Create connector functional profiles and connector technical profiles.</span></span>

    1. <span data-ttu-id="ff827-138">在**连接器功能配置文件**页（**零售 \> 渠道设置 \> 会计整合 \> 连接器功能配置文件**）上，为与此会计连接器相关的会计连接器和会计单据提供程序的每个组合创建连接器功能配置文件。</span><span class="sxs-lookup"><span data-stu-id="ff827-138">On the **Connector functional profiles** page (**Retail \> Channel setup \> Fiscal integration \> Connector functional profiles**), create a connector functional profile for each combination of a fiscal connector and a fiscal document provider that is related to this fiscal connector.</span></span>

        1. <span data-ttu-id="ff827-139">选择连接器名称。</span><span class="sxs-lookup"><span data-stu-id="ff827-139">Select a connector name.</span></span>
        2. <span data-ttu-id="ff827-140">选择单据提供程序。</span><span class="sxs-lookup"><span data-stu-id="ff827-140">Select a document provider.</span></span>

        <span data-ttu-id="ff827-141">您可以更改连接器功能配置文件中的数据映射参数。</span><span class="sxs-lookup"><span data-stu-id="ff827-141">You can change the data mapping parameters in a connector functional profile.</span></span> <span data-ttu-id="ff827-142">若要还原在会计单据提供程序配置中定义的默认参数，请选择**更新**。</span><span class="sxs-lookup"><span data-stu-id="ff827-142">To restore the default parameters that are defined in the fiscal document provider configuration, select **Update**.</span></span>

        <span data-ttu-id="ff827-143">**示例**</span><span class="sxs-lookup"><span data-stu-id="ff827-143">**Examples**</span></span>

        |   | <span data-ttu-id="ff827-144">格式</span><span class="sxs-lookup"><span data-stu-id="ff827-144">Format</span></span> | <span data-ttu-id="ff827-145">示例</span><span class="sxs-lookup"><span data-stu-id="ff827-145">Example</span></span> |
        |---|--------|---------|
        | <span data-ttu-id="ff827-146">**增值税税率设置**</span><span class="sxs-lookup"><span data-stu-id="ff827-146">**VAT rates settings**</span></span> | <span data-ttu-id="ff827-147">值 : VATrate</span><span class="sxs-lookup"><span data-stu-id="ff827-147">value : VATrate</span></span> | <span data-ttu-id="ff827-148">1 : 2000、2 : 1800</span><span class="sxs-lookup"><span data-stu-id="ff827-148">1 : 2000, 2 : 1800</span></span> |
        | <span data-ttu-id="ff827-149">**增值税代码映射**</span><span class="sxs-lookup"><span data-stu-id="ff827-149">**VAT codes mapping**</span></span> | <span data-ttu-id="ff827-150">VATcode : 值</span><span class="sxs-lookup"><span data-stu-id="ff827-150">VATcode : value</span></span> | <span data-ttu-id="ff827-151">vat20 : 1、vat18 : 2</span><span class="sxs-lookup"><span data-stu-id="ff827-151">vat20 : 1, vat18 : 2</span></span> |
        | <span data-ttu-id="ff827-152">**支付方式映射**</span><span class="sxs-lookup"><span data-stu-id="ff827-152">**Tender types mapping**</span></span> | <span data-ttu-id="ff827-153">TenderType：值</span><span class="sxs-lookup"><span data-stu-id="ff827-153">TenderType : value</span></span> | <span data-ttu-id="ff827-154">现金 : 1、卡 : 2</span><span class="sxs-lookup"><span data-stu-id="ff827-154">Cash : 1, Card : 2</span></span> |

        > [!NOTE]
        > <span data-ttu-id="ff827-155">连接器功能配置文件是公司特定的。</span><span class="sxs-lookup"><span data-stu-id="ff827-155">Connector functional profiles are company-specific.</span></span> <span data-ttu-id="ff827-156">如果您计划使用不同公司的会计连接器和会计单据提供程序的相同组合，应为每个公司创建连接器功能配置文件。</span><span class="sxs-lookup"><span data-stu-id="ff827-156">If you plan to use the same combination of a fiscal connector and a fiscal document provider in different companies, you should create a connector functional profile for each company.</span></span>

    2. <span data-ttu-id="ff827-157">在**连接器技术配置文件**页（**零售 \> 渠道设置 \> 会计整合 \> 连接器技术配置文件**）上，为每个会计连接器创建连接器技术配置文件。</span><span class="sxs-lookup"><span data-stu-id="ff827-157">On the **Connector technical profiles** page (**Retail \> Channel setup \> Fiscal integration \> Connector technical profiles**), create a connector technical profile for each fiscal connector.</span></span>

        1. <span data-ttu-id="ff827-158">选择连接器名称。</span><span class="sxs-lookup"><span data-stu-id="ff827-158">Select a connector name.</span></span>
        2. <span data-ttu-id="ff827-159">选择连接器类型。</span><span class="sxs-lookup"><span data-stu-id="ff827-159">Select a connector type.</span></span> <span data-ttu-id="ff827-160">对于连接到硬件工作站的设备，请选择**本地**。</span><span class="sxs-lookup"><span data-stu-id="ff827-160">For devices that are connected to a Hardware station, select **Local**.</span></span>

            > [!NOTE]
            > <span data-ttu-id="ff827-161">当前仅支持本地连接器。</span><span class="sxs-lookup"><span data-stu-id="ff827-161">Only local connectors are currently supported.</span></span>

        <span data-ttu-id="ff827-162">连接器技术配置文件中的**设备**和**设置**选项卡上的参数可以更改。</span><span class="sxs-lookup"><span data-stu-id="ff827-162">Parameters on the **Device** and **Settings** tabs in a connector technical profile can be changed.</span></span> <span data-ttu-id="ff827-163">若要还原在会计连接器配置中定义的默认参数，请选择**更新**。</span><span class="sxs-lookup"><span data-stu-id="ff827-163">To restore the default parameters that are defined in the fiscal connector configuration, select **Update**.</span></span> <span data-ttu-id="ff827-164">在 XML 配置的新版本加载后，您将收到一则消息，显示当前会计连接器或会计单据提供程序已经在使用。</span><span class="sxs-lookup"><span data-stu-id="ff827-164">While a new version of an XML configuration is loaded, you receive a message that states that the current fiscal connector or fiscal document provider is already being used.</span></span> <span data-ttu-id="ff827-165">此过程不会覆盖之前在连接器功能配置文件和连接器技术配置文件中进行的手动更改。</span><span class="sxs-lookup"><span data-stu-id="ff827-165">This procedure doesn't override manual changes that were previously made in connector functional profiles and connector technical profiles.</span></span> <span data-ttu-id="ff827-166">要应用来自新配置的一组默认参数，在**连接器功能配置文件**页或**连接器技术配置文件**页上，选择**更新**。</span><span class="sxs-lookup"><span data-stu-id="ff827-166">To apply the default set of parameters from a new configuration, on the **Connector functional profiles** page or the **Connector technical profiles** page, select **Update**.</span></span>

4. <span data-ttu-id="ff827-167">创建会计连接器组。</span><span class="sxs-lookup"><span data-stu-id="ff827-167">Create fiscal connector groups.</span></span>

    <span data-ttu-id="ff827-168">会计连接器组将执行相同功能并在会计登记流程的同一个步骤使用的会计连接器的功能配置文件组合在一起。</span><span class="sxs-lookup"><span data-stu-id="ff827-168">A fiscal connector group combines functional profiles of fiscal connectors that perform identical functions and are used at the same step of a fiscal registration process.</span></span> <span data-ttu-id="ff827-169">例如，如果多个税控打印机型号可用于零售商店，这些税控打印机的会计连接器可以在会计连接器组中组合在一起。</span><span class="sxs-lookup"><span data-stu-id="ff827-169">For example, if several fiscal printer models can be used in a retail store, fiscal connectors for those fiscal printers can be combined in a fiscal connector group.</span></span>

    1. <span data-ttu-id="ff827-170">在**会计连接器组**页（**零售 \> 渠道设置 \> 会计整合 \> 会计连接器组**），创建新的会计连接器组。</span><span class="sxs-lookup"><span data-stu-id="ff827-170">On the **Fiscal connector group** page (**Retail \> Channel setup \> Fiscal integration \> Fiscal connector groups**), create a new fiscal connector group.</span></span>
    2. <span data-ttu-id="ff827-171">向连接器组添加功能配置文件。</span><span class="sxs-lookup"><span data-stu-id="ff827-171">Add functional profiles to the connector group.</span></span> <span data-ttu-id="ff827-172">在**功能配置文件**选项卡上，选择**添加**并选择配置文件编号。</span><span class="sxs-lookup"><span data-stu-id="ff827-172">On the **Functional profiles** tab, select **Add**, and select a profile number.</span></span> <span data-ttu-id="ff827-173">连接器组内的每个会计连接器只能有一个功能配置文件。</span><span class="sxs-lookup"><span data-stu-id="ff827-173">Each fiscal connector in a connector group can only have one functional profile.</span></span>
    3. <span data-ttu-id="ff827-174">如果要暂停功能配置文件的使用，将**禁用**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="ff827-174">To suspend use of the functional profile, set the **Disable** option to **Yes**.</span></span> <span data-ttu-id="ff827-175">此更改只影响当前的连接器组。</span><span class="sxs-lookup"><span data-stu-id="ff827-175">This change affects only the current connector group.</span></span> <span data-ttu-id="ff827-176">您可以在其他连接器组中继续使用相同的功能配置文件。</span><span class="sxs-lookup"><span data-stu-id="ff827-176">You can continue to use the same functional profile in other connector groups.</span></span>

5. <span data-ttu-id="ff827-177">创建会计登记流程。</span><span class="sxs-lookup"><span data-stu-id="ff827-177">Create a fiscal registration process.</span></span>

    <span data-ttu-id="ff827-178">会计登记流程由登记步骤的顺序和用于每个步骤的连接器组定义。</span><span class="sxs-lookup"><span data-stu-id="ff827-178">A fiscal registration process is defined by the sequence of registration steps and the connector group that is used for each step.</span></span>

    1. <span data-ttu-id="ff827-179">在**会计登记流程**页（**零售 \> 渠道设置 \> 会计整合 \> 会计登记流程**），为每个会计登记的唯一流程创建新记录。</span><span class="sxs-lookup"><span data-stu-id="ff827-179">On the **Fiscal registration process** page (**Retail \> Channel setup \> Fiscal integration \> Fiscal registration processes**), create a new record for each unique process of fiscal registration.</span></span>
    2. <span data-ttu-id="ff827-180">向流程添加登记步骤：</span><span class="sxs-lookup"><span data-stu-id="ff827-180">Add registration steps to the process:</span></span>

        1. <span data-ttu-id="ff827-181">选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="ff827-181">Select **Add**.</span></span>
        2. <span data-ttu-id="ff827-182">选择会计连接器类型。</span><span class="sxs-lookup"><span data-stu-id="ff827-182">Select a fiscal connector type.</span></span>
        3. <span data-ttu-id="ff827-183">在**组编号**字段中，选择一个合适的会计连接器组。</span><span class="sxs-lookup"><span data-stu-id="ff827-183">In the **Group number** field, select an appropriate fiscal connector group.</span></span>

6. <span data-ttu-id="ff827-184">将会计登记流程的实体分配到 POS 配置文件。</span><span class="sxs-lookup"><span data-stu-id="ff827-184">Assign entities of the fiscal registration process to POS profiles.</span></span>

    1. <span data-ttu-id="ff827-185">在 **POS 功能配置文件**页（**零售 \> 渠道设置 \> POS 设置 \> POS 配置文件 \> 功能配置文件**），将会计登记流程分配到 POS 功能配置文件。</span><span class="sxs-lookup"><span data-stu-id="ff827-185">On the **POS functionality profiles** page (**Retail \> Channel setup \> POS setup \> POS profiles \> Functionality profiles**), assign the fiscal registration process to a POS functionality profile.</span></span> <span data-ttu-id="ff827-186">选择**编辑**，然后，在**会计登记流程**选项卡上，在**流程编号**字段中，选择流程。</span><span class="sxs-lookup"><span data-stu-id="ff827-186">Select **Edit**, and then, on the **Fiscal registration process** tab, in the **Process number** field, select a process.</span></span>
    2. <span data-ttu-id="ff827-187">在 **POS 硬件配置文件**页（**零售 \> 渠道设置 \> POS 设置 \> POS 配置文件 \> 硬件配置文件**），将连接器技术配置文件分配到硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="ff827-187">On the **POS hardware profile** page (**Retail \> Channel setup \> POS setup \> POS profiles \> Hardware profiles**), assign connector technical profiles to a hardware profile.</span></span> <span data-ttu-id="ff827-188">选择**编辑**，在**会计外围设备**选项卡上添加一个行，然后，在**配置文件编号**字段中，选择连接器技术配置文件。</span><span class="sxs-lookup"><span data-stu-id="ff827-188">Select **Edit**, add a line on the **Fiscal peripherals** tab, and then, in the **Profile number** field, select a connector technical profile.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ff827-189">您可以将多个技术配置文件添加到同一个硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="ff827-189">You can add several technical profiles to the same hardware profile.</span></span> <span data-ttu-id="ff827-190">但是，硬件配置文件或 POS 功能配置文件仅应具有与任何会计连接器组的一个交集。</span><span class="sxs-lookup"><span data-stu-id="ff827-190">However, a hardware profile or POS functionality profile should have only one intersection with any fiscal connector group.</span></span>

    <span data-ttu-id="ff827-191">会计登记流由会计登记流程还有会计整合组件的某些参数定义：会计单据提供程序的 Commerce runtime 扩展和会计连接器的硬件工作站扩展。</span><span class="sxs-lookup"><span data-stu-id="ff827-191">The fiscal registration flow is defined by the fiscal registration process and also by some parameters of fiscal integration components: the Commerce runtime extension for the fiscal document provider and the Hardware station extension for the fiscal connector.</span></span>

    - <span data-ttu-id="ff827-192">对会计登记的事件和交易的订阅在会计单据提供程序中预定义。</span><span class="sxs-lookup"><span data-stu-id="ff827-192">The subscription of events and transactions to fiscal registration is predefined in the fiscal document provider.</span></span>
    - <span data-ttu-id="ff827-193">会计单据提供程序还负责识别用于会计登记的会计连接器。</span><span class="sxs-lookup"><span data-stu-id="ff827-193">The fiscal document provider is also responsible for identifying the fiscal connector that is used for fiscal registration.</span></span> <span data-ttu-id="ff827-194">它将为会计登记流程的当前步骤指定的会计连接器组中包含的连接器功能配置文件，与分配到 POS 与之配对的硬件工作站的硬件配置文件的连接器技术配置文件相匹配。</span><span class="sxs-lookup"><span data-stu-id="ff827-194">It matches the connector functional profiles that are included in the fiscal connector group that is specified for the current step of the fiscal registration process with the connector technical profile that is assigned to the hardware profile of the Hardware station that the POS is paired to.</span></span>
    - <span data-ttu-id="ff827-195">会计单据提供程序使用来自会计单据配置的数据映射设置在生成会计单据时转换交易/事件数据，如纳税和付款。</span><span class="sxs-lookup"><span data-stu-id="ff827-195">The fiscal document provider uses the data mapping settings from the fiscal document provider configuration to transform transaction/event data such as taxes and payments while a fiscal document is generated.</span></span>
    - <span data-ttu-id="ff827-196">在会计单据提供程序生成会计单据时，会计连接器可以将其原样发送到会计设备，或者根据如何处理通信，分析并将其转换为设备应用程序编程接口 (API) 的一系列命令。</span><span class="sxs-lookup"><span data-stu-id="ff827-196">When the fiscal document provider generates a fiscal document, the fiscal connector can either send it to the fiscal device as is, or parse it and transform it into a sequence of commands of the device application programming interface (API), depending on how the communication is handled.</span></span>

7. <span data-ttu-id="ff827-197">在**会计登记流程**页（**零售 \> 渠道设置 \> 会计整合 \> 会计登记流程**），选择**验证**来验证会计登记流程。</span><span class="sxs-lookup"><span data-stu-id="ff827-197">On the **Fiscal registration process** page (**Retail \> Channel setup \> Fiscal integration \> Fiscal registration processes**), select **Validate** to validate the fiscal registration process.</span></span>

    <span data-ttu-id="ff827-198">我们建议您在以下情况下运行此类验证：</span><span class="sxs-lookup"><span data-stu-id="ff827-198">We recommend that you run this type of validation in the following cases:</span></span>

    - <span data-ttu-id="ff827-199">在完成了新登记流程的所有设置后，包括当您将登记流程分配到 POS 功能配置文件和硬件配置文件时。</span><span class="sxs-lookup"><span data-stu-id="ff827-199">After you've completed all the settings for a new registration process, including when you assign registration processes to POS functionality profiles and hardware profiles.</span></span>
    - <span data-ttu-id="ff827-200">在您对现有会计登记流程进行更改后，这些更改可能在运行时导致选择不同的会计连接器（例如，如果您更改会计登记流程步骤的连接器组，请在连接器组中启用连接器功能配置文件，或将新连接器功能配置文件添加到连接器组）。</span><span class="sxs-lookup"><span data-stu-id="ff827-200">After you make changes to an existing fiscal registration process, and those changes might cause a different fiscal connector to be selected at runtime (for example, if you change the connector group for a fiscal registration process step, enable a connector functional profile in a connector group, or add a new connector functional profile to a connector group).</span></span>
    - <span data-ttu-id="ff827-201">在您对连接器技术配置文件到硬件配置文件的分配进行更改后。</span><span class="sxs-lookup"><span data-stu-id="ff827-201">After you make changes in the assignment of connector technical profiles to hardware profiles.</span></span>

8. <span data-ttu-id="ff827-202">在**配送调度**页，运行 **1070** 和 **1090** 作业将数据传输到渠道数据库。</span><span class="sxs-lookup"><span data-stu-id="ff827-202">On the **Distribution schedule** page, run the **1070** and **1090** jobs to transfer data to the channel database.</span></span>

## <a name="set-up-fiscal-texts-for-discounts"></a><span data-ttu-id="ff827-203">设置折扣的会计文本</span><span class="sxs-lookup"><span data-stu-id="ff827-203">Set up fiscal texts for discounts</span></span>

<span data-ttu-id="ff827-204">在某些情况下，如果应用了折扣，必须在财务收据上打印特殊文本。</span><span class="sxs-lookup"><span data-stu-id="ff827-204">In some cases, a special text must be printed on a fiscal receipt if a discount is applied.</span></span> <span data-ttu-id="ff827-205">您可以在**会计连接器组**页（**零售 \> 渠道设置 \> 会计整合 \> 会计连接器组**）设置折扣的会计文本。</span><span class="sxs-lookup"><span data-stu-id="ff827-205">You can set up fiscal texts for discounts on the **Fiscal connector group** page (**Retail \> Channel setup \> Fiscal integration \> Fiscal connector groups**).</span></span>

- <span data-ttu-id="ff827-206">对于在 POS 应用的手动折扣，您应该为在 POS 功能配置文件中指定为**产品折扣**信息代码的信息代码或信息代码组设置会计文本。</span><span class="sxs-lookup"><span data-stu-id="ff827-206">For manual discounts that are applied at the POS, you should set a fiscal text for the info code or info code group that is specified as the **Product discount** info code in the POS functionality profile.</span></span>

    1. <span data-ttu-id="ff827-207">在**会计连接器组**页，选择**财务收据文本**。</span><span class="sxs-lookup"><span data-stu-id="ff827-207">On the **Fiscal connector group** page, select **Text for fiscal receipt**.</span></span>
    2. <span data-ttu-id="ff827-208">在**信息代码**选项卡上，选择**添加**，然后选择信息代码或信息代码组。</span><span class="sxs-lookup"><span data-stu-id="ff827-208">On the **Info codes** tab, select **Add**, and select an info code or info code group.</span></span>
    3. <span data-ttu-id="ff827-209">在**信息代码编号**中，选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ff827-209">In the **Info code number**, select a value.</span></span>
    4. <span data-ttu-id="ff827-210">在**子代码编号**字段中，如果所选信息代码需要子代码，则选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ff827-210">In the **Subcode number** field, select a value if a subcode is required for the selected info code.</span></span>
    5. <span data-ttu-id="ff827-211">在**财务收据文本**字段中，指定应在财务收据上打印的会计文本。</span><span class="sxs-lookup"><span data-stu-id="ff827-211">In the **Text for fiscal receipt** field, specify a fiscal text that should be printed on a fiscal receipt.</span></span>
    6. <span data-ttu-id="ff827-212">将**在财务收据上打印用户输入**选项设置为**是**使用用户在 POS 手动输入的信息覆盖财务收据上的文本。</span><span class="sxs-lookup"><span data-stu-id="ff827-212">Set the **Print user input on fiscal receipt** option to **Yes** to override the text on a fiscal receipt with information that a user manually enters at the POS.</span></span> <span data-ttu-id="ff827-213">此选项仅适用于输入类型为**文本**的信息代码。</span><span class="sxs-lookup"><span data-stu-id="ff827-213">This option applies only to info codes that have an input type of **Text**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ff827-214">您可以指定多个信息代码的会计文本来支持使用信息代码组、链接的信息代码和触发的信息代码的情况。</span><span class="sxs-lookup"><span data-stu-id="ff827-214">You can specify a fiscal text for several info codes to support scenarios where info code groups, linked info codes, and triggered info codes are used.</span></span> <span data-ttu-id="ff827-215">在这些情况下，财务收据将包含来自链接到应用了折扣的交易记录行的所有信息代码的会计文本。</span><span class="sxs-lookup"><span data-stu-id="ff827-215">In these scenarios, the fiscal receipt will contain the fiscal texts from all info codes that are linked to the transaction line where the discount was applied.</span></span>

- <span data-ttu-id="ff827-216">对于渠道特定折扣，应定义折扣 ID 的会计文本。</span><span class="sxs-lookup"><span data-stu-id="ff827-216">For channel-specific discounts, you should define a fiscal text for the discount ID.</span></span>

    1. <span data-ttu-id="ff827-217">在**会计连接器组**页，选择**财务收据文本**。</span><span class="sxs-lookup"><span data-stu-id="ff827-217">On the **Fiscal connector group** page, select **Text for fiscal receipt**.</span></span>
    2. <span data-ttu-id="ff827-218">在**折扣**选项卡上，选择**添加**，然后选择折扣 ID。</span><span class="sxs-lookup"><span data-stu-id="ff827-218">On the **Discounts** tab, select **Add**, and select a discount ID.</span></span>
    3. <span data-ttu-id="ff827-219">在**财务收据文本**字段中，指定应在财务收据上打印的会计文本。</span><span class="sxs-lookup"><span data-stu-id="ff827-219">In the **Text for fiscal receipt** field, specify a fiscal text that should be printed on a fiscal receipt.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ff827-220">如果多个折扣应用于同一个交易记录行，财务收据将包含来自链接到这些交易记录行的所有折扣的会计文本。</span><span class="sxs-lookup"><span data-stu-id="ff827-220">If several discounts are applied to the same transaction line, the fiscal receipt will contain fiscal texts from all discounts that are linked to those transaction line.</span></span>

## <a name="set-error-handling-settings"></a><span data-ttu-id="ff827-221">设置错误处理设置</span><span class="sxs-lookup"><span data-stu-id="ff827-221">Set error handling settings</span></span>

<span data-ttu-id="ff827-222">会计整合中提供的错误处理选项在会计登记流程中设置。</span><span class="sxs-lookup"><span data-stu-id="ff827-222">The error handling options that are available in the fiscal integration are set in the fiscal registration process.</span></span> <span data-ttu-id="ff827-223">有关会计整合中的错误处理的详细信息，请参阅[错误处理](fiscal-integration-for-retail-channel.md#error-handling)。</span><span class="sxs-lookup"><span data-stu-id="ff827-223">For more information about error handling in the fiscal integration, see [Error handling](fiscal-integration-for-retail-channel.md#error-handling).</span></span>

1. <span data-ttu-id="ff827-224">在**会计登记流程**页（**零售 \> 渠道设置 \> 会计整合 \> 会计登记流程**），您可以为会计登记流程的每个步骤设置以下参数。</span><span class="sxs-lookup"><span data-stu-id="ff827-224">On the **Fiscal registration process** page (**Retail \> Channel setup \> Fiscal integration \> Fiscal registration processes**), you can set the following parameters for each step of the fiscal registration process:</span></span>

    - <span data-ttu-id="ff827-225">**允许跳过** – 此参数启用错误处理对话框中的**跳过**选项。</span><span class="sxs-lookup"><span data-stu-id="ff827-225">**Allow skip** – This parameter enables the **Skip** option in the error handling dialog box.</span></span>
    - <span data-ttu-id="ff827-226">**允许标记为已登记** – 此参数启用错误处理对话框中的**标记为已登记**选项。</span><span class="sxs-lookup"><span data-stu-id="ff827-226">**Allow mark as registered** – This parameter enables the **Mark as registered** option in the error handling dialog box.</span></span>
    - <span data-ttu-id="ff827-227">**出错时继续** –如果启用此参数，并且交易记录或事件的会计登记失败，POS 收银机上将继续进行会计登记流程。</span><span class="sxs-lookup"><span data-stu-id="ff827-227">**Continue on error** – If this parameter is enabled, the fiscal registration process can continue on the POS register if the fiscal registration of a transaction or event fails.</span></span> <span data-ttu-id="ff827-228">但是，若要运行下一个交易记录或事件的会计登记，操作员必须重试失败的会计登记，跳过，或将交易记录或事件标记为已登记。</span><span class="sxs-lookup"><span data-stu-id="ff827-228">Otherwise, to run the fiscal registration of the next transaction or event, the operator must retry the failed fiscal registration, skip it, or mark the transaction or event as registered.</span></span> <span data-ttu-id="ff827-229">有关详细信息，请参阅[可选会计登记](fiscal-integration-for-retail-channel.md#optional-fiscal-registration)。</span><span class="sxs-lookup"><span data-stu-id="ff827-229">For more information, see [Optional fiscal registration](fiscal-integration-for-retail-channel.md#optional-fiscal-registration).</span></span>

    > [!NOTE]
    > <span data-ttu-id="ff827-230">如果启用了**出错时继续**参数，将自动禁用**允许跳过**和**允许标记为已登记**参数。</span><span class="sxs-lookup"><span data-stu-id="ff827-230">If the **Continue on error** parameter is enabled, the **Allow skip** and **Allow mark as registered** parameters are automatically disabled.</span></span>

2. <span data-ttu-id="ff827-231">错误处理对话框中的**跳过**和**标记为已登记**选项需要**允许跳过登记或标记为已登记**权限。</span><span class="sxs-lookup"><span data-stu-id="ff827-231">The **Skip** and **Mark as registered** options in the error handling dialog box require the **Allow skip registration or mark as registered** permission.</span></span> <span data-ttu-id="ff827-232">因此，在**权限组**页（**零售 \> 员工 \> 权限组**），应启用**允许跳过登记或标记为已登记**权限。</span><span class="sxs-lookup"><span data-stu-id="ff827-232">Therefore, on the **Permission groups** page (**Retail \> Employees \> Permission groups**), enable the **Allow skip registration or mark as registered** permission.</span></span>
3. <span data-ttu-id="ff827-233">**跳过**和**标记为已登记**选项让操作员可以在会计登记失败时输入附加信息。</span><span class="sxs-lookup"><span data-stu-id="ff827-233">The **Skip** and **Mark as registered** options let operators enter additional information when fiscal registration fails.</span></span> <span data-ttu-id="ff827-234">若要让此功能可用，您应该在会计连接器组中指定**跳过**和**标记为已登记**信息代码。</span><span class="sxs-lookup"><span data-stu-id="ff827-234">To make this functionality available, you should specify the **Skip** and **Mark as registered** info codes on a fiscal connector group.</span></span> <span data-ttu-id="ff827-235">操作员输入的信息然后保存为链接到会计交易记录的信息代码交易记录。</span><span class="sxs-lookup"><span data-stu-id="ff827-235">The information that operators enter is then saved as an info code transaction that is linked to the fiscal transaction.</span></span> <span data-ttu-id="ff827-236">有关信息代码的更多详细信息，请参阅[信息代码和信息代码组](../info-codes-retail.md)。</span><span class="sxs-lookup"><span data-stu-id="ff827-236">For more details about info codes, see [Info codes and info code groups](../info-codes-retail.md).</span></span>

    > [!NOTE]
    > <span data-ttu-id="ff827-237">在会计连接器组中用于**跳过**和**标记为已登记**的信息代码不支持**产品**触发器函数。</span><span class="sxs-lookup"><span data-stu-id="ff827-237">The **Product** trigger function isn't supported for the info codes that are used for **Skip** and **Mark as registered** in fiscal connector groups.</span></span>

    - <span data-ttu-id="ff827-238">在**会计连接器组**页，在**信息代码**选项卡上，在**跳过**和**标记为已登记**字段中选择信息代码或信息代码组。</span><span class="sxs-lookup"><span data-stu-id="ff827-238">On the **Fiscal connector group** page, on the **Info codes** tab, select info codes or info code groups in the **Skip** and **Mark as registered** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ff827-239">会计登记流程的任何步骤均可以生成一个会计单据和一个非会计单据。</span><span class="sxs-lookup"><span data-stu-id="ff827-239">One fiscal document and one non-fiscal document can be generated on any step of a fiscal registration process.</span></span> <span data-ttu-id="ff827-240">会计单据提供程序扩展识别与会计或非会计单据相关的每个交易或事件的类型。</span><span class="sxs-lookup"><span data-stu-id="ff827-240">A fiscal document provider extension identifies every type of transaction or event as related to fiscal or non-fiscal documents.</span></span> <span data-ttu-id="ff827-241">错误处理功能仅应用于会计单据。</span><span class="sxs-lookup"><span data-stu-id="ff827-241">The error handling feature applies only to fiscal documents.</span></span>
    >
    > - <span data-ttu-id="ff827-242">**会计单据** – 应该成功登记的必需文档（例如，财务收据）。</span><span class="sxs-lookup"><span data-stu-id="ff827-242">**Fiscal document** – A mandatory document that should be registered successfully (for example, a fiscal receipt).</span></span>
    > - <span data-ttu-id="ff827-243">**非会计单据** – 交易或事件的补充单据（例如，礼品卡单）。</span><span class="sxs-lookup"><span data-stu-id="ff827-243">**Non-fiscal document** – A supplementary document for the transaction or event (for example, a gift card slip).</span></span>

4. <span data-ttu-id="ff827-244">如果操作员必须可以在发生了运行状况检查错误之后继续处理当前操作（例如，创建或完成交易记录）您应该启用**权限组**页面上的**允许跳过运行状况检查错误**权限（**Retail \> 员工 \> 权限组**）。</span><span class="sxs-lookup"><span data-stu-id="ff827-244">If the operator must be able to continue to process the current operation (for example, creation or finalization of a transaction) after a health check error occurs, you should enable the **Allow skip health check error** permission on the **Permission groups** page (**Retail \> Employees \> Permission groups**).</span></span> <span data-ttu-id="ff827-245">有关运行状况检查过程的详细信息，请参阅[会计登记运行状况检查](fiscal-integration-for-retail-channel.md#fiscal-registration-health-check)。</span><span class="sxs-lookup"><span data-stu-id="ff827-245">For more information about the health check procedure, see [Fiscal registration health check](fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).</span></span>

## <a name="set-up-fiscal-xz-reports-from-the-pos"></a><span data-ttu-id="ff827-246">从 POS 设置会计 X/Z 报表</span><span class="sxs-lookup"><span data-stu-id="ff827-246">Set up fiscal X/Z reports from the POS</span></span>

<span data-ttu-id="ff827-247">若要让会计 X/Z 报表从 POS 运行，您应将新按钮添加到 POS 布局。</span><span class="sxs-lookup"><span data-stu-id="ff827-247">To enable fiscal X/Z reports to be run from the POS, you should add new buttons to a POS layout.</span></span>

- <span data-ttu-id="ff827-248">在**按钮网格**页，请按照[将自定义操作按钮添加到零售总部的 POS 布局](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters)中的说明安装设计器、更新布局。</span><span class="sxs-lookup"><span data-stu-id="ff827-248">On the **Button grids** page, follow the instructions in [Add a custom operation button to the POS layout in Retail headquarters](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) to install the designer and update a POS layout.</span></span>

    1. <span data-ttu-id="ff827-249">选择要更新的布局。</span><span class="sxs-lookup"><span data-stu-id="ff827-249">Select the layout to update.</span></span> 
    2. <span data-ttu-id="ff827-250">添加新按钮，并设置**打印会计 X** 按钮属性。</span><span class="sxs-lookup"><span data-stu-id="ff827-250">Add a new button, and set the **Print fiscal X** button property.</span></span>
    3. <span data-ttu-id="ff827-251">添加新按钮，并设置**打印会计 Z** 按钮属性。</span><span class="sxs-lookup"><span data-stu-id="ff827-251">Add a new button, and set the **Print fiscal Z** button property.</span></span>
    4. <span data-ttu-id="ff827-252">在**配送计划**页，运行 **1090** 作业将更改传输到渠道数据库。</span><span class="sxs-lookup"><span data-stu-id="ff827-252">On the **Distribution schedule** page, run the **1090** job to transfer changes to the channel database.</span></span>

## <a name="enable-manual-execution-of-postponed-fiscal-registration"></a><span data-ttu-id="ff827-253">启用已推迟会计登记的手动执行</span><span class="sxs-lookup"><span data-stu-id="ff827-253">Enable manual execution of postponed fiscal registration</span></span>

<span data-ttu-id="ff827-254">若要启用已延迟会计登记的手动执行，应该向 POS 布局添加一个新按钮。</span><span class="sxs-lookup"><span data-stu-id="ff827-254">To enable manual execution of a postponed fiscal registration, you should add a new button to a POS layout.</span></span>

- <span data-ttu-id="ff827-255">在**按钮网格**页，请按照[将自定义操作按钮添加到零售总部的 POS 布局](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters)中的说明安装设计器、更新布局。</span><span class="sxs-lookup"><span data-stu-id="ff827-255">On the **Button grids** page, follow the instructions in [Add a custom operation button to the POS layout in Retail headquarters](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) to install the designer and update a POS layout.</span></span>

    1. <span data-ttu-id="ff827-256">选择要更新的布局。</span><span class="sxs-lookup"><span data-stu-id="ff827-256">Select the layout to update.</span></span>
    2. <span data-ttu-id="ff827-257">添加新按钮，并设置**完成会计登记流程**按钮属性。</span><span class="sxs-lookup"><span data-stu-id="ff827-257">Add a new button, and set the **Complete fiscal registration process** button property.</span></span>
    3. <span data-ttu-id="ff827-258">在**配送计划**页，运行 **1090** 作业将更改传输到渠道数据库。</span><span class="sxs-lookup"><span data-stu-id="ff827-258">On the **Distribution schedule** page, run the **1090** job to transfer your changes to the channel database.</span></span>

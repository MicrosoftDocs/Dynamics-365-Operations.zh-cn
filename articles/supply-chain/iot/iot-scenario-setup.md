---
title: IoT 智能的方案设置
description: 此主题介绍如何在 Microsoft Dynamics 365 Supply Chain Management 中配置 IoT 智能的方案。
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 91deb080121d50794e6ff6fe79f9ca876b76deb4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005244"
---
# <a name="scenario-setup-for-iot-intelligence"></a><span data-ttu-id="e726d-103">IoT 智能的方案设置</span><span class="sxs-lookup"><span data-stu-id="e726d-103">Scenario setup for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e726d-104">此主题介绍如何在 Microsoft Dynamics 365 Supply Chain Management 中配置 IoT 智能的方案。</span><span class="sxs-lookup"><span data-stu-id="e726d-104">This topic explains how to configure scenarios for IoT Intelligence in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="e726d-105">必须先[设置 Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md)，才能设置这些方案。</span><span class="sxs-lookup"><span data-stu-id="e726d-105">Before you can set up the scenarios, you must [set up Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span></span>

<span data-ttu-id="e726d-106">在此主题中，将配置 **设备停机时间** 方案，以便在机器停机时在 Supply Chain Management 中生成通知。</span><span class="sxs-lookup"><span data-stu-id="e726d-106">In this topic, you will configure the **Equipment downtime** scenario so that a notification is generated in Supply Chain Management when a machine goes down.</span></span> <span data-ttu-id="e726d-107">此主题还介绍如何配置 **产品质量** 方案，以便在物料的属性超出指定范围时生成通知，以及如何配置 **生产延迟** 方案，以便在生产吞吐量低于阈值时生成通知。</span><span class="sxs-lookup"><span data-stu-id="e726d-107">The topic also shows how to configure the **Product quality** scenario so that a notification is generated if an attribute of an item is outside a specified range, and how to configure the **Production delays** scenario so that a notification is generated if the production throughput falls below a threshold value.</span></span>

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a><span data-ttu-id="e726d-108">在 Supply Chain Management 中配置设备停机时间方案</span><span class="sxs-lookup"><span data-stu-id="e726d-108">Configure the Equipment downtime scenario in Supply Chain Management</span></span>

<span data-ttu-id="e726d-109">**设备停机时间** 方案将 **部件停止** 信号映射到机器警报阈值。</span><span class="sxs-lookup"><span data-stu-id="e726d-109">The **Equipment downtime** scenario maps a **PartOut** signal to a machine alert threshold.</span></span> <span data-ttu-id="e726d-110">仅当为此方案选择机器，并且在 Supply Chain Management 中将其设置为 **正在运行**，才监视此机器。</span><span class="sxs-lookup"><span data-stu-id="e726d-110">The machine is monitored only when it's selected for the scenario and when is set to **Running** in Supply Chain Management.</span></span> <span data-ttu-id="e726d-111">如果上次收到的机器 **部件停止** 信号以后经过的时间超过了警报阈值，将触发 **机器停机** 通知。</span><span class="sxs-lookup"><span data-stu-id="e726d-111">If the time since a **PartOut** signal was last received from the machine exceeds the alert threshold, a **Machine down** notification is triggered.</span></span> <span data-ttu-id="e726d-112">如果机器仍在运行，下次收到 **部件停止** 信号时，将触发 **机器开机** 通知。</span><span class="sxs-lookup"><span data-stu-id="e726d-112">If the machine is still running, a **Machine up** notification is triggered when the next **PartOut** signal is received.</span></span> <span data-ttu-id="e726d-113">如果机器停机时间达到 30 分钟，将触发新的 **机器停机** 通知。</span><span class="sxs-lookup"><span data-stu-id="e726d-113">If a machine stays down for 30 minutes, a new **Machine down** notification is triggered.</span></span>

<span data-ttu-id="e726d-114">**设备停机时间** 方案具有以下依赖性：</span><span class="sxs-lookup"><span data-stu-id="e726d-114">The **Equipment downtime** scenario has the following dependencies:</span></span>

+ <span data-ttu-id="e726d-115">仅当正在映射的机器上运行生产订单，才能触发警报。</span><span class="sxs-lookup"><span data-stu-id="e726d-115">An alert can be triggered only if a production order is running on a mapped machine.</span></span>
+ <span data-ttu-id="e726d-116">必须将表示映射的机器 **部件停机** 信号的型号发送到 IoT 中心，并且必须包含唯一属性名称。</span><span class="sxs-lookup"><span data-stu-id="e726d-116">A signal that represents a mapped machine's **PartOut** signal must be sent to the IoT hub, and a unique property name must be included.</span></span>
+ <span data-ttu-id="e726d-117">Azure IoT 中心消息中必须包含 UNIX **时间戳记** 属性，其中值以毫秒 (ms) 表示。</span><span class="sxs-lookup"><span data-stu-id="e726d-117">A UNIX **timestamp** property, where the value is expressed in milliseconds (ms), must be present in the Azure IoT Hub message.</span></span>

<span data-ttu-id="e726d-118">若要配置此方案，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="e726d-118">To configure the scenario, follow these steps.</span></span>

1. <span data-ttu-id="e726d-119">登录 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="e726d-119">Sign in to Supply Chain Management.</span></span>
2. <span data-ttu-id="e726d-120">启用 IoT 智能功能标志。</span><span class="sxs-lookup"><span data-stu-id="e726d-120">Enable the IoT Intelligence feature flag.</span></span> <span data-ttu-id="e726d-121">有关更多信息，请参见[功能管理概述](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)。</span><span class="sxs-lookup"><span data-stu-id="e726d-121">For more information, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>
3. <span data-ttu-id="e726d-122">配置指标。</span><span class="sxs-lookup"><span data-stu-id="e726d-122">Configure the metrics.</span></span> <span data-ttu-id="e726d-123">有关详细信息，请参阅[如何配置指标](iot-metrics-setup.md#configure-metrics)。</span><span class="sxs-lookup"><span data-stu-id="e726d-123">For more information, see [How to configure metrics](iot-metrics-setup.md#configure-metrics).</span></span>
4. <span data-ttu-id="e726d-124">转到 **生产控制 \> 设置 \> IoT 智能 \> 方案管理**。</span><span class="sxs-lookup"><span data-stu-id="e726d-124">Go to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
6. <span data-ttu-id="e726d-125">在 **设备停机时间** 磁贴中，选择 **配置** 打开配置向导。</span><span class="sxs-lookup"><span data-stu-id="e726d-125">On the **Equipment downtime** tile, select **Configure** to open the configuration wizard.</span></span>

   <span data-ttu-id="e726d-126">向导中的第一个页面是 **设备传感器架构定义** 页面。</span><span class="sxs-lookup"><span data-stu-id="e726d-126">The first page in the wizard is the **Equipment sensor schema definition** page.</span></span> <span data-ttu-id="e726d-127">在此页面中，目标是在 Supply Chain Management 中设置架构，以使其与 IoT 中心消息的 JavaScript Object Notation (JSON) 格式匹配。</span><span class="sxs-lookup"><span data-stu-id="e726d-127">On this page, your goal is to set up the schema in Supply Chain Management so that it matches the JavaScript Object Notation (JSON) format of the IoT Hub messages.</span></span> <span data-ttu-id="e726d-128">可以定义多个消息架构。</span><span class="sxs-lookup"><span data-stu-id="e726d-128">Multiple message schemas can be defined.</span></span> <span data-ttu-id="e726d-129">有关详细信息，请参阅 [IoT 中心消息的架构格式](iot-schema-format.md)。</span><span class="sxs-lookup"><span data-stu-id="e726d-129">For more information, see [Schema formats for IoT Hub messages](iot-schema-format.md).</span></span> <span data-ttu-id="e726d-130">在此示例中，消息有效负载中包含一批采用以下格式的消息。</span><span class="sxs-lookup"><span data-stu-id="e726d-130">In this example, the message payload contains a batch of messages that has the following format.</span></span>

    ```json
    {
        "timestamp": 1576016821614,
        "payload": [
            {
                "id": "IoTInt.Machine1225.PartOut",
                "timestamp": 1576016821614,
                "value": True
            },
            {
                "id": "IoTInt.Machine1226.PartOut",
                "timestamp": 1576016991616,
                "value": True
            }
        ]
    }
    ```

7. <span data-ttu-id="e726d-131">向表添加一行，然后设置以下值：</span><span class="sxs-lookup"><span data-stu-id="e726d-131">Add a row to the table, and set the following values:</span></span>

    1. <span data-ttu-id="e726d-132">将 **架构名称** 字段设置为 **ID**。</span><span class="sxs-lookup"><span data-stu-id="e726d-132">Set the **Schema name** field to **ID**.</span></span>
    2. <span data-ttu-id="e726d-133">将 **架构路径** 字段设置为 **/payload\[\*\]/id**。</span><span class="sxs-lookup"><span data-stu-id="e726d-133">Set the **Schema path** field to **/payload\[\*\]/id**.</span></span>
    3. <span data-ttu-id="e726d-134">将 **说明** 字段设置为 **消息 ID**。</span><span class="sxs-lookup"><span data-stu-id="e726d-134">Set the **Description** field to **Message ID**.</span></span>

8. <span data-ttu-id="e726d-135">向表再添加一行，然后设置以下值：</span><span class="sxs-lookup"><span data-stu-id="e726d-135">Add another row to the table, and set the following values:</span></span>

    1. <span data-ttu-id="e726d-136">将 **架构名称** 字段设置为 **时间戳**。</span><span class="sxs-lookup"><span data-stu-id="e726d-136">Set the **Schema name** field to **Timestamp**.</span></span>
    2. <span data-ttu-id="e726d-137">将 **架构路径** 字段设置为 **/payload\[\*\]/timestamp**。</span><span class="sxs-lookup"><span data-stu-id="e726d-137">Set the **Schema path** field to **/payload\[\*\]/timestamp**.</span></span>
    3. <span data-ttu-id="e726d-138">将 **说明** 字段设置为 **消息时间戳**。</span><span class="sxs-lookup"><span data-stu-id="e726d-138">Set the **Description** field to **Message timestamp**.</span></span>

9. <span data-ttu-id="e726d-139">向表再添加一行，然后设置以下值：</span><span class="sxs-lookup"><span data-stu-id="e726d-139">Add another row to the table, and set the following values:</span></span>

    1. <span data-ttu-id="e726d-140">将 **架构名称** 字段设置为 **值**。</span><span class="sxs-lookup"><span data-stu-id="e726d-140">Set the **Schema name** field to **Value**.</span></span>
    2. <span data-ttu-id="e726d-141">将 **架构路径** 字段设置为 **/payload\[\*\]/value**。</span><span class="sxs-lookup"><span data-stu-id="e726d-141">Set the **Schema path** field to **/payload\[\*\]/value**.</span></span>
    3. <span data-ttu-id="e726d-142">将 **说明** 字段设置为 **消息值**。</span><span class="sxs-lookup"><span data-stu-id="e726d-142">Set the **Description** field to **Message value**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e726d-143">不必定义消息中的全部属性。</span><span class="sxs-lookup"><span data-stu-id="e726d-143">You don't have to define all the properties in the message.</span></span> <span data-ttu-id="e726d-144">仅定义所需的属性。</span><span class="sxs-lookup"><span data-stu-id="e726d-144">Define only the properties that you require.</span></span> <span data-ttu-id="e726d-145">在前面的步骤中，您没有为 **根时间戳** 创建行。</span><span class="sxs-lookup"><span data-stu-id="e726d-145">In the preceding steps, you didn't create a row for **Root timestamp**.</span></span> <span data-ttu-id="e726d-146">**根时间戳** 的路径将为 **/timestamp**。</span><span class="sxs-lookup"><span data-stu-id="e726d-146">The path of **Root timestamp** would be **/timestamp**.</span></span>

10. <span data-ttu-id="e726d-147">选择 **下一步** 转到 **设备传感器架构映射** 页。</span><span class="sxs-lookup"><span data-stu-id="e726d-147">Select **Next** to go to the **Equipment sensor schema map** page.</span></span>
11. <span data-ttu-id="e726d-148">在 **设备资源 ID** 的行的 **架构名称** 字段中，选择 **ID**。</span><span class="sxs-lookup"><span data-stu-id="e726d-148">In the row for **Equipment resource ID**, in the **Schema name** field, select **ID**.</span></span>
12. <span data-ttu-id="e726d-149">在 **UTC 时间** 的行的 **架构名称** 字段中，选择 **时间戳**。</span><span class="sxs-lookup"><span data-stu-id="e726d-149">In the row for **UTC time**, in the **Schema name** field, select **Timestamp**.</span></span>
13. <span data-ttu-id="e726d-150">在 **部件生成的信号** 的行的 **架构名称** 字段中，选择 **值**。</span><span class="sxs-lookup"><span data-stu-id="e726d-150">In the row for **Part produced signal**, in the **Schema name** field, select **Value**.</span></span>
14. <span data-ttu-id="e726d-151">选择 **下一步** 转到 **设备资源 ID 配置** 页。</span><span class="sxs-lookup"><span data-stu-id="e726d-151">Select **Next** to go to the **Equipment resource ID configuration** page.</span></span>
15. <span data-ttu-id="e726d-152">执行以下步骤将 IoT 中心消息中的值映射到 Supply Chain Management 资源：</span><span class="sxs-lookup"><span data-stu-id="e726d-152">Follow these steps to map the values in the IoT Hub message to the Supply Chain Management resources:</span></span>

    1. <span data-ttu-id="e726d-153">在 **信号数据值** 标准，添加一个新行。</span><span class="sxs-lookup"><span data-stu-id="e726d-153">In the **Signal Data Values** table, add a new row.</span></span> <span data-ttu-id="e726d-154">在 **值** 字段中，输入 **IoTInt.Machine1225.PartOut**。</span><span class="sxs-lookup"><span data-stu-id="e726d-154">In the **Value** field, enter **IoTInt.Machine1225.PartOut**.</span></span> <span data-ttu-id="e726d-155">此值来自 IoT 中心消息中的 JSON **id** 属性。</span><span class="sxs-lookup"><span data-stu-id="e726d-155">This value  comes from the JSON **id** property in the IoT Hub message.</span></span>
    2. <span data-ttu-id="e726d-156">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="e726d-156">Select **Save**.</span></span>
    3. <span data-ttu-id="e726d-157">在 **业务记录映射** 表中，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="e726d-157">In the **Business Record Mapping** table, select **New**.</span></span> <span data-ttu-id="e726d-158">将自动填充 **业务记录类型** 字段的值，您不必更改。</span><span class="sxs-lookup"><span data-stu-id="e726d-158">A default value for the **Business record type** field is automatically filled in, and you don't have to change it.</span></span>
    4. <span data-ttu-id="e726d-159">在 **业务记录** 字段中，选择此信号值来自的 Supply Chain Management 机器资源。</span><span class="sxs-lookup"><span data-stu-id="e726d-159">In the **Business record** field, select the Supply Chain Management machine resource that the signal value is being sent from.</span></span>
    5. <span data-ttu-id="e726d-160">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="e726d-160">Select **Save**.</span></span>
    6. <span data-ttu-id="e726d-161">重复这些步骤，为 **Machine1226** 添加新业务记录映射。</span><span class="sxs-lookup"><span data-stu-id="e726d-161">Repeat these steps to add a new business record mapping for **Machine1226**.</span></span> <span data-ttu-id="e726d-162">可将多个信号数据值映射到 Supply Chain Management 中的一个记录。</span><span class="sxs-lookup"><span data-stu-id="e726d-162">You can map multiple signal data values to a single record in Supply Chain Management.</span></span>

16. <span data-ttu-id="e726d-163">可使用 **所选** 列选择要处理的机器。</span><span class="sxs-lookup"><span data-stu-id="e726d-163">Use the **Selected** column to select the machines that you want to process.</span></span> <span data-ttu-id="e726d-164">不必定义所有信号值，也不必选择所有机器。</span><span class="sxs-lookup"><span data-stu-id="e726d-164">You don't have to define all signal values, and you don't have to select all machines.</span></span>
17. <span data-ttu-id="e726d-165">选择 **下一步** 转到 **部件生成的信号配置** 页。</span><span class="sxs-lookup"><span data-stu-id="e726d-165">Select **Next** to go to the **Part produced signal configuration** page.</span></span>
18. <span data-ttu-id="e726d-166">在 **信号数据值** 标准，添加一行，然后将 **值** 字段设置为 **True**。</span><span class="sxs-lookup"><span data-stu-id="e726d-166">In the **Signal Data Values** table, add a row, and set the **Value** field to **True**.</span></span> <span data-ttu-id="e726d-167">此值来自 IoT 中心消息中的 JSON **值** 属性。</span><span class="sxs-lookup"><span data-stu-id="e726d-167">This value comes from the JSON **value** property in the IoT Hub message.</span></span> <span data-ttu-id="e726d-168">可以根据需要为方案添加任意数量的值。</span><span class="sxs-lookup"><span data-stu-id="e726d-168">You can add as many values as you require for your scenario.</span></span>
19. <span data-ttu-id="e726d-169">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="e726d-169">Select **Save**.</span></span>
20. <span data-ttu-id="e726d-170">选择 **下一步** 转到 **设备停机时间阈值** 页。</span><span class="sxs-lookup"><span data-stu-id="e726d-170">Select **Next** to go to the **Equipment downtime threshold** page.</span></span> <span data-ttu-id="e726d-171">列出的机器是之前映射到信号值的机器。</span><span class="sxs-lookup"><span data-stu-id="e726d-171">The machines that are listed are the machines that were previously mapped to signal values.</span></span> <span data-ttu-id="e726d-172">在此页面中，将定义阈值以确定某个机器是否已停机。</span><span class="sxs-lookup"><span data-stu-id="e726d-172">On this page, you will define a threshold to determine whether a machine is down.</span></span> <span data-ttu-id="e726d-173">例如，如果将此阈值设置为 **10**，并且有 10 秒钟未收到机器的 **部件停机** 消息，Supply Chain Management 将生成通知。</span><span class="sxs-lookup"><span data-stu-id="e726d-173">For example, if you set the threshold to **10**, Supply Chain Management will generate a notification if no **PartOut** signal is received from a machine for 10 minutes.</span></span>
21. <span data-ttu-id="e726d-174">选择 **下一步** 转到 **启用方案** 页。</span><span class="sxs-lookup"><span data-stu-id="e726d-174">Select **Next** to go to the **Enable scenario** page.</span></span> <span data-ttu-id="e726d-175">设置用于启用方案的选项。</span><span class="sxs-lookup"><span data-stu-id="e726d-175">Set the option to enable the scenario.</span></span>
22. <span data-ttu-id="e726d-176">选择 **完成**。</span><span class="sxs-lookup"><span data-stu-id="e726d-176">Select **Finish**.</span></span>

<span data-ttu-id="e726d-177">方案设置现在已完成。</span><span class="sxs-lookup"><span data-stu-id="e726d-177">The scenario setup is now completed.</span></span> <span data-ttu-id="e726d-178">IoT 智能将自动开始处理 IoT 中心消息。</span><span class="sxs-lookup"><span data-stu-id="e726d-178">IoT Intelligence will automatically start to process the IoT Hub messages.</span></span>

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a><span data-ttu-id="e726d-179">在 Supply Chain Management 中配置产品质量方案</span><span class="sxs-lookup"><span data-stu-id="e726d-179">Configure the Product quality scenario in Supply Chain Management</span></span>

<span data-ttu-id="e726d-180">如果某个物料的属性超出指定范围，**产品质量** 方案将生成通知。</span><span class="sxs-lookup"><span data-stu-id="e726d-180">The **Product quality** scenario generates a notification if an attribute of an item is outside a specified range.</span></span> <span data-ttu-id="e726d-181">例如，传感器将每个物料的重量发送到 IoT 中心。</span><span class="sxs-lookup"><span data-stu-id="e726d-181">For example, a sensor sends the weight of each item to IoT Hub.</span></span> <span data-ttu-id="e726d-182">如果物料太重或太轻，将在 Supply Chain Management 中生成通知。</span><span class="sxs-lookup"><span data-stu-id="e726d-182">If an item is too heavy or too light, a notification is generated in Supply Chain Management.</span></span>

<span data-ttu-id="e726d-183">**产品质量** 方案具有以下依赖性：</span><span class="sxs-lookup"><span data-stu-id="e726d-183">The **Product quality** scenario has the following dependencies:</span></span>

+ <span data-ttu-id="e726d-184">仅当在映射的机器上运行生产订单，并生成具有映射的批处理属性生成产品时，才可以触发警报。</span><span class="sxs-lookup"><span data-stu-id="e726d-184">An alert can be triggered only if a production order is running on a mapped machine and producing a product that has a mapped batch attribute.</span></span>
+ <span data-ttu-id="e726d-185">必须将表示批处理属性的信号发送到 IoT 中心，并且必须包含唯一属性名称。</span><span class="sxs-lookup"><span data-stu-id="e726d-185">A signal that represents the batch attribute must be sent to the IoT hub, and a unique property name must be included.</span></span>
+ <span data-ttu-id="e726d-186">IoT 中心消息中必须包含 UNIX **时间戳记** 属性，其中值以 ms 表示。</span><span class="sxs-lookup"><span data-stu-id="e726d-186">A UNIX **timestamp** property, where the value is expressed in ms, must be present in the IoT Hub message.</span></span>

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a><span data-ttu-id="e726d-187">在 Supply Chain Management 中配置生产延迟方案</span><span class="sxs-lookup"><span data-stu-id="e726d-187">Configure the Production delays scenario in Supply Chain Management</span></span>

<span data-ttu-id="e726d-188">如果生产完全降到阈值下，**生产延迟** 方案将生成通知。</span><span class="sxs-lookup"><span data-stu-id="e726d-188">The **Production delays** scenario generates a notification if the production throughput falls below a threshold value.</span></span> <span data-ttu-id="e726d-189">在此方案中，将为生成的每个物料向 IoT 中心发送 **部件停止** 信号。</span><span class="sxs-lookup"><span data-stu-id="e726d-189">In this scenario, a **PartOut** signal is sent to IoT Hub for each item that is produced.</span></span> <span data-ttu-id="e726d-190">在 Supply Chain Management 中，订单延迟基于计划运行的生产订单时间量、应生成的物料数量、作业已运行的时间量和收到的 **部件停止** 信号数量计算订单延迟。</span><span class="sxs-lookup"><span data-stu-id="e726d-190">In Supply Chain Management, the order delay is calculated based on the amount of time that the production order is scheduled to run, the number of items that should be produced, the amount of time that the job has been running, and the number of **PartOut** signals that are received.</span></span> <span data-ttu-id="e726d-191">如果作业的 **部件停止** 信号数量低于阈值，将生成延迟通知。</span><span class="sxs-lookup"><span data-stu-id="e726d-191">A delay notification is generated if the number of **PartOut** signals for the job falls below the threshold value.</span></span>

<span data-ttu-id="e726d-192">**生产延迟** 方案具有以下依赖性：</span><span class="sxs-lookup"><span data-stu-id="e726d-192">The **Production delays** scenario has the following dependencies:</span></span>

+ <span data-ttu-id="e726d-193">仅当正在映射的机器上运行生产订单，才能触发警报。</span><span class="sxs-lookup"><span data-stu-id="e726d-193">An alert can be triggered only if a production order is running on a mapped machine.</span></span>
+ <span data-ttu-id="e726d-194">必须将表示映射的机器 **部件停机** 信号的型号发送到 Azure IoT 中心，并且必须包含唯一属性名称。</span><span class="sxs-lookup"><span data-stu-id="e726d-194">A signal that represents a mapped machine's **PartOut** signal must be sent to the Azure IoT hub, and a unique property name must be included.</span></span>
+ <span data-ttu-id="e726d-195">IoT 中心消息中必须包含 UNIX **时间戳记** 属性，其中值以 ms 表示。</span><span class="sxs-lookup"><span data-stu-id="e726d-195">A UNIX **timestamp** property, where the value is expressed in ms, must be present in the IoT Hub message.</span></span>

## <a name="disable-a-scenario"></a><span data-ttu-id="e726d-196">禁用方案</span><span class="sxs-lookup"><span data-stu-id="e726d-196">Disable a scenario</span></span>

<span data-ttu-id="e726d-197">若要禁用方案，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="e726d-197">To disable a scenario, follow these steps.</span></span>

1. <span data-ttu-id="e726d-198">在 Supply Chain Management 中，转到 **生产控制 \> 设置 \> IoT 智能 \> 方案管理**。</span><span class="sxs-lookup"><span data-stu-id="e726d-198">In Supply Chain Management, go to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
2. <span data-ttu-id="e726d-199">在方案的磁贴中，选择 **配置**。</span><span class="sxs-lookup"><span data-stu-id="e726d-199">On the tile for the scenario, select **Configure**.</span></span>
3. <span data-ttu-id="e726d-200">选择 **下一步** 转到向导的最后一页。</span><span class="sxs-lookup"><span data-stu-id="e726d-200">Select **Next** to go to the last wizard page.</span></span>
4. <span data-ttu-id="e726d-201">设置用于禁用方案的选项。</span><span class="sxs-lookup"><span data-stu-id="e726d-201">Set the option to disable the scenario.</span></span>

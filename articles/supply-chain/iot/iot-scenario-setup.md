---
title: IoT 智能的方案设置
description: 此主题介绍如何在 Supply Chain Management 中为 IoT 智能创建方案。
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5633741fcd9c04b68e5b174447d7ead3c521ccd7
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597160"
---
# <a name="scenario-setup-for-iot-intelligence"></a><span data-ttu-id="a0b71-103">IoT 智能的方案设置</span><span class="sxs-lookup"><span data-stu-id="a0b71-103">Scenario setup for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a0b71-104">此主题介绍如何在 Supply Chain Management 中为 IoT 智能创建方案。</span><span class="sxs-lookup"><span data-stu-id="a0b71-104">This topic describes how to configure a scenario in Supply Chain Management for IoT Intelligence.</span></span> <span data-ttu-id="a0b71-105">首先必须[设置 LCS](iot-lcs-setup.md)，才能设置此类方案。</span><span class="sxs-lookup"><span data-stu-id="a0b71-105">Before you can setup the scenarios, you must [setup LCS](iot-lcs-setup.md).</span></span>

<span data-ttu-id="a0b71-106">在此主题中，将配置**设备停机时间**方案，以便在机器停机时在 Supply Chain Management 中生成通知。</span><span class="sxs-lookup"><span data-stu-id="a0b71-106">In this topic, you will configure the **Equipment downtime** scenario to generate a notification in Supply Chain Management when a machine goes down.</span></span>

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a><span data-ttu-id="a0b71-107">在 Supply Chain Management 中配置**设备停机时间**方案</span><span class="sxs-lookup"><span data-stu-id="a0b71-107">Configure the **Equipment downtime** scenario in Supply Chain Management</span></span>

<span data-ttu-id="a0b71-108">**设备停机时间**方案将部件停止信号映射到机器警报阈值。</span><span class="sxs-lookup"><span data-stu-id="a0b71-108">The **Equipment downtime** scenario maps a part out signal to a machine alert threshold.</span></span> <span data-ttu-id="a0b71-109">仅当为此方案选择机器，并且在 Supply Chain Management 中将其设置为正在运行，才监视此机器。</span><span class="sxs-lookup"><span data-stu-id="a0b71-109">The machine is monitored only when the machine is selected for the scenario and is set to running in Supply Chain Management.</span></span> <span data-ttu-id="a0b71-110">如果机器上次收到部件停止信号以后经过的时间超过了警报阈值，将触发**机器停机**通知。</span><span class="sxs-lookup"><span data-stu-id="a0b71-110">If the time since the machine’s last received Part Out signal is greater than the alert threshold, then a **Machine down** notification is triggered.</span></span> <span data-ttu-id="a0b71-111">如果机器仍在运行，下次收到**部件停止**信号时，将触发**机器开机**通知。</span><span class="sxs-lookup"><span data-stu-id="a0b71-111">If the machine is still running, when the next **PartOut** signal is received a **Machine up** notification is triggered.</span></span> <span data-ttu-id="a0b71-112">如果机器停机时间达到 30 分钟，将触发新的**机器停机**通知。</span><span class="sxs-lookup"><span data-stu-id="a0b71-112">If a machine stays down for 30 mins a new **Machine down** notification is triggered.</span></span>

<span data-ttu-id="a0b71-113">**设备停机时间**方案具有以下依赖性：</span><span class="sxs-lookup"><span data-stu-id="a0b71-113">The **Equipment downtime** scenario has these dependencies:</span></span>

+ <span data-ttu-id="a0b71-114">必须正在映射的机器上运行生产订单，才能触发警报。</span><span class="sxs-lookup"><span data-stu-id="a0b71-114">A production order must be running on a mapped machine for an alert to be triggered.</span></span>
+ <span data-ttu-id="a0b71-115">必须将表示映射的机器部件停机信号的型号发送到具有唯一属性名称的 IoT 中心。</span><span class="sxs-lookup"><span data-stu-id="a0b71-115">A signal representing a mapped machine's part out signal must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="a0b71-116">IoT 中心消息中必须包含 Unix 毫秒时间戳属性。</span><span class="sxs-lookup"><span data-stu-id="a0b71-116">A Unix milliseconds timestamp property must be present in the IoT hub message.</span></span>

<span data-ttu-id="a0b71-117">若要配置此方案，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="a0b71-117">To configure the scenario, follow these steps:</span></span>

1. <span data-ttu-id="a0b71-118">登录 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="a0b71-118">Log into Supply Chain Management.</span></span>
2. <span data-ttu-id="a0b71-119">启用 IoT 智能功能标志。</span><span class="sxs-lookup"><span data-stu-id="a0b71-119">Enable the IoT Intelligence feature flag.</span></span> <span data-ttu-id="a0b71-120">有关更多信息，请参见[功能管理概述](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="a0b71-120">For more information, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
3. <span data-ttu-id="a0b71-121">配置指标。</span><span class="sxs-lookup"><span data-stu-id="a0b71-121">Configure the metrics.</span></span> <span data-ttu-id="a0b71-122">有关详细信息，请参阅[如何配置指标](iot-metrics-setup.md#configure-metrics)。</span><span class="sxs-lookup"><span data-stu-id="a0b71-122">For more information, see [How to configure metrics](iot-metrics-setup.md#configure-metrics).</span></span>
4. <span data-ttu-id="a0b71-123">导航到**生产控制**。</span><span class="sxs-lookup"><span data-stu-id="a0b71-123">Navigate to **Production control**.</span></span>
5. <span data-ttu-id="a0b71-124">导航到**设置 \> IoT 智能 \> 方案管理**。</span><span class="sxs-lookup"><span data-stu-id="a0b71-124">Navigate to **Setup \> IoT Intelligence \> Scenario management**.</span></span>
6. <span data-ttu-id="a0b71-125">请单击**设备停机时间**磁贴中的**配置**。</span><span class="sxs-lookup"><span data-stu-id="a0b71-125">Click **Configure** on the **Equipment downtime** tile.</span></span> <span data-ttu-id="a0b71-126">将启动配置向导并显示**设备传感器架构定义**页。</span><span class="sxs-lookup"><span data-stu-id="a0b71-126">The configuration wizard starts with the **Equipment sensor schema definition** page.</span></span> <span data-ttu-id="a0b71-127">此处的目标是在 Supply Chain Management 中设置架构以匹配 IoT 消息的 JSON 格式。</span><span class="sxs-lookup"><span data-stu-id="a0b71-127">The goal here is to setup the schema in Supply Chain Management to match the JSON format of the IoT messages.</span></span> <span data-ttu-id="a0b71-128">可以定义多个消息架构。</span><span class="sxs-lookup"><span data-stu-id="a0b71-128">Multiple message schemas can be defined.</span></span> <span data-ttu-id="a0b71-129">有关详细信息，请参阅 [IoT 中心的消息架构格式](iot-schema-format.md)。</span><span class="sxs-lookup"><span data-stu-id="a0b71-129">For more information, see [Message schema formats for IoT Hub](iot-schema-format.md).</span></span> <span data-ttu-id="a0b71-130">在此示例中，消息有效负载中包含一批以下格式的消息：</span><span class="sxs-lookup"><span data-stu-id="a0b71-130">In this example, the message payload contains a batch of messages with this format:</span></span>

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

7. <span data-ttu-id="a0b71-131">在表中添加一行。</span><span class="sxs-lookup"><span data-stu-id="a0b71-131">Add a row to the table.</span></span>

    1. <span data-ttu-id="a0b71-132">将**架构名称**设置为 **ID**。</span><span class="sxs-lookup"><span data-stu-id="a0b71-132">Set the **Schema name** to **ID**.</span></span>
    2. <span data-ttu-id="a0b71-133">将**架构路径**设置为 **/payload[\*]/id**。</span><span class="sxs-lookup"><span data-stu-id="a0b71-133">Set the **Schema path** to **/payload[\*]/id**.</span></span>
    3. <span data-ttu-id="a0b71-134">将**说明**设置为**消息 ID**。</span><span class="sxs-lookup"><span data-stu-id="a0b71-134">Set the **Description** to **Message ID**.</span></span>

8. <span data-ttu-id="a0b71-135">在表中添加一行。</span><span class="sxs-lookup"><span data-stu-id="a0b71-135">Add a row to the table.</span></span>

    1. <span data-ttu-id="a0b71-136">将**架构名称**设置为**时间戳**。</span><span class="sxs-lookup"><span data-stu-id="a0b71-136">Set the **Schema name** to **Timestamp**.</span></span>
    2. <span data-ttu-id="a0b71-137">将**架构路径**设置为 **/payload[\*]/timestamp**。</span><span class="sxs-lookup"><span data-stu-id="a0b71-137">Set the **Schema path** to **/payload[\*]/timestamp**.</span></span>
    3. <span data-ttu-id="a0b71-138">将**说明**设置为**消息时间戳**。</span><span class="sxs-lookup"><span data-stu-id="a0b71-138">Set the **Description** to **Message timestamp**.</span></span>

9. <span data-ttu-id="a0b71-139">在表中添加一行。</span><span class="sxs-lookup"><span data-stu-id="a0b71-139">Add a row to the table.</span></span>

    1. <span data-ttu-id="a0b71-140">将**架构名称**设置为**值**。</span><span class="sxs-lookup"><span data-stu-id="a0b71-140">Set the **Schema name** to **Value**.</span></span>
    2. <span data-ttu-id="a0b71-141">将**架构路径**设置为 **/payload[\*]/value**。</span><span class="sxs-lookup"><span data-stu-id="a0b71-141">Set the **Schema path** to **/payload[\*]/value**.</span></span>
    3. <span data-ttu-id="a0b71-142">将**说明**设置为**消息值**。</span><span class="sxs-lookup"><span data-stu-id="a0b71-142">Set the **Description** to **Message value**.</span></span>

    <span data-ttu-id="a0b71-143">无需在消息中定义所有属性，只需要定义需要的属性。</span><span class="sxs-lookup"><span data-stu-id="a0b71-143">You don't need to define all the properties in the message, only the ones that you need.</span></span> <span data-ttu-id="a0b71-144">在此示例中，没有为**根时间戳**定义行。</span><span class="sxs-lookup"><span data-stu-id="a0b71-144">In this example, you did not create a row for **Root timestamp**.</span></span> <span data-ttu-id="a0b71-145">**根时间戳**的路径将为 **/timestamp**。</span><span class="sxs-lookup"><span data-stu-id="a0b71-145">The path for **Root timestamp** would be **/timestamp**.</span></span>
  
10. <span data-ttu-id="a0b71-146">单击**下一步**转到**设备传感器架构映射**页。</span><span class="sxs-lookup"><span data-stu-id="a0b71-146">Click **Next** to go to the **Equipment sensor schema map** page.</span></span>
11. <span data-ttu-id="a0b71-147">在**设备资源 ID** 的行中，将**架构名称**设置为 **ID**。</span><span class="sxs-lookup"><span data-stu-id="a0b71-147">In the row for **Equipment resource ID** set the **Schema name** to **ID**.</span></span> <span data-ttu-id="a0b71-148">将在下拉表中显示有效值。</span><span class="sxs-lookup"><span data-stu-id="a0b71-148">The valid values are displayed in a dropdown table.</span></span>
12. <span data-ttu-id="a0b71-149">在 **UTC 时间**的行中，将**架构名称**设置为**时间戳**。</span><span class="sxs-lookup"><span data-stu-id="a0b71-149">In the row for **UTC time** set the **Schema name** to **Timestamp**.</span></span> <span data-ttu-id="a0b71-150">将在下拉表中显示有效值。</span><span class="sxs-lookup"><span data-stu-id="a0b71-150">The valid values are displayed in a dropdown table.</span></span>
13. <span data-ttu-id="a0b71-151">在**部件生成的信号** 的行中，将**架构名称**设置为**值**。</span><span class="sxs-lookup"><span data-stu-id="a0b71-151">In the row for **Part produced signal** set the **Schema name** to **Value**.</span></span> <span data-ttu-id="a0b71-152">将在下拉表中显示有效值。</span><span class="sxs-lookup"><span data-stu-id="a0b71-152">The valid values are displayed in a dropdown table.</span></span>
14. <span data-ttu-id="a0b71-153">单击**下一步**转到**设备资源 ID 配置**页。</span><span class="sxs-lookup"><span data-stu-id="a0b71-153">Click **Next** for the **Equipment resource ID configuration** page.</span></span>
15. <span data-ttu-id="a0b71-154">在此步骤中，将把 IoT 中心消息值映射到 Supply Chain Management 资源。</span><span class="sxs-lookup"><span data-stu-id="a0b71-154">In this step, you map the IoT Hub message values to the Supply Chain Management resources.</span></span>

    1. <span data-ttu-id="a0b71-155">在**信号数据值**标准，添加一个新行，然后在**值**列中输入 **IoTInt.Machine1225.PartOut**。</span><span class="sxs-lookup"><span data-stu-id="a0b71-155">In the **Signal Data Values** table, add a new row, and enter **IoTInt.Machine1225.PartOut** in the **Value** column.</span></span> <span data-ttu-id="a0b71-156">值 **IoTInt.Machine1225.PartOut** 来自 IoT 中心消息中的 JSON **id** 属性。</span><span class="sxs-lookup"><span data-stu-id="a0b71-156">The value **IoTInt.Machine1225.PartOut** comes from the JSON **id** property in the IoT hub message.</span></span>
    2. <span data-ttu-id="a0b71-157">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="a0b71-157">Click **Save**.</span></span>
    3. <span data-ttu-id="a0b71-158">在**业务记录映射**表中，单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="a0b71-158">In the **Business Record Mapping** table, click **New**.</span></span> <span data-ttu-id="a0b71-159">将自动填充**业务记录类型**的值，您无需更改。</span><span class="sxs-lookup"><span data-stu-id="a0b71-159">The default value for the **Business record type** is autopopulated, and you don't need to change it.</span></span>
    4. <span data-ttu-id="a0b71-160">在**业务记录**列中，选择此信号值来自的 Supple Chain Management 机器资源。</span><span class="sxs-lookup"><span data-stu-id="a0b71-160">In the **Business record** column, select the Supple Chain Management machine resource this signal value is being sent from.</span></span>
    5. <span data-ttu-id="a0b71-161">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="a0b71-161">Click **Save**.</span></span>
    6. <span data-ttu-id="a0b71-162">重复这些步骤，并为 **Machine1226** 添加新业务记录映射。</span><span class="sxs-lookup"><span data-stu-id="a0b71-162">Repeat these steps, adding a new business record mapping for **Machine1226**.</span></span> <span data-ttu-id="a0b71-163">可将多个信号数据值映射到 Supply Chain Management 中的一个记录。</span><span class="sxs-lookup"><span data-stu-id="a0b71-163">You can map multiple signal data values to a single record in Supply Chain Management.</span></span>

16. <span data-ttu-id="a0b71-164">可使用**所选**列选择要处理哪些机器。</span><span class="sxs-lookup"><span data-stu-id="a0b71-164">Use the **Selected** column to choose which machines you want to process.</span></span> <span data-ttu-id="a0b71-165">不必定义所有信号值，也不必选择所有机器。</span><span class="sxs-lookup"><span data-stu-id="a0b71-165">You do not have to define all signal values and you do not have to select all machines.</span></span>
17. <span data-ttu-id="a0b71-166">单击**下一步**转到**部件生成的信号配置**页。</span><span class="sxs-lookup"><span data-stu-id="a0b71-166">Click **Next** to go to the **Part produced signal configuration** page.</span></span>
18. <span data-ttu-id="a0b71-167">在**信号数据值**标准，添加一行，然后将**值**设置为 **True**。</span><span class="sxs-lookup"><span data-stu-id="a0b71-167">In the **Signal Data Values** table, add a row, and set **Value** to **True**.</span></span> <span data-ttu-id="a0b71-168">值 **True** 来自 IoT 中心消息中的 JSON **value** 属性。</span><span class="sxs-lookup"><span data-stu-id="a0b71-168">The value **True** comes from the JSON **value** property in the IoT hub message.</span></span> <span data-ttu-id="a0b71-169">可以根据需要为方案添加任意数量的值。</span><span class="sxs-lookup"><span data-stu-id="a0b71-169">You can add as many values as you need for your scenario.</span></span>
19. <span data-ttu-id="a0b71-170">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="a0b71-170">Click **Save**.</span></span>
20. <span data-ttu-id="a0b71-171">单击**下一步**转到**设备停机时间阈值**页。</span><span class="sxs-lookup"><span data-stu-id="a0b71-171">Click **Next** to go to the **Equipment downtime threshold** page.</span></span> <span data-ttu-id="a0b71-172">列出的机器是之前映射到信号值的机器。</span><span class="sxs-lookup"><span data-stu-id="a0b71-172">The machines listed are the machines previously mapped to signal values.</span></span> <span data-ttu-id="a0b71-173">在此步骤中，将定义阈值以确定某个机器是否已停机。</span><span class="sxs-lookup"><span data-stu-id="a0b71-173">In this step, you define a threshold to determine if a machine is down.</span></span> <span data-ttu-id="a0b71-174">例如，如果将此阈值设置为 10，并且机器有 10 秒钟无部件停机消息，Supply Chain Management 将生成通知。</span><span class="sxs-lookup"><span data-stu-id="a0b71-174">For example, if you set the threshold to 10, Supply Chain Management generates a notification if there is no part out message from a machine for 10 minutes.</span></span>
21. <span data-ttu-id="a0b71-175">单击**下一步**转到**启用方案**页。</span><span class="sxs-lookup"><span data-stu-id="a0b71-175">Click **Next** to go to the **Enable scenario** page.</span></span> <span data-ttu-id="a0b71-176">切换滑块以启用方案。</span><span class="sxs-lookup"><span data-stu-id="a0b71-176">Toggle the slider to enable the scenario.</span></span>
22. <span data-ttu-id="a0b71-177">单击**完成**。</span><span class="sxs-lookup"><span data-stu-id="a0b71-177">Click **Finish**.</span></span>

<span data-ttu-id="a0b71-178">方案设置完成。</span><span class="sxs-lookup"><span data-stu-id="a0b71-178">The scenario setup is complete.</span></span> <span data-ttu-id="a0b71-179">IoT 智能将自动开始处理 IoT 中心消息。</span><span class="sxs-lookup"><span data-stu-id="a0b71-179">IoT Intelligence will automatically start processing the IoT Hub messages.</span></span>

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a><span data-ttu-id="a0b71-180">在 Supply Chain Management 中配置**产品质量**方案</span><span class="sxs-lookup"><span data-stu-id="a0b71-180">Configure the **Product quality** scenario in Supply Chain Management</span></span>

<span data-ttu-id="a0b71-181">如果某个物料的属性超出指定范围，**产品质量**方案将生成通知。</span><span class="sxs-lookup"><span data-stu-id="a0b71-181">The **Product quality** scenario generates a notification if an attribute of an item is outside a specified range.</span></span> <span data-ttu-id="a0b71-182">例如，传感器可以将每个物料的重量发送到 IoT 中心。</span><span class="sxs-lookup"><span data-stu-id="a0b71-182">For example, a sensor could send the weight of each item to IoT Hub.</span></span> <span data-ttu-id="a0b71-183">如果物料太重或太轻，将在 Supply Chain Management 中生成通知。</span><span class="sxs-lookup"><span data-stu-id="a0b71-183">In Supply Chain Management, a notification would be generated if the item was too heavy or too light.</span></span>

<span data-ttu-id="a0b71-184">该方案具有以下依赖性：</span><span class="sxs-lookup"><span data-stu-id="a0b71-184">The scenario has these dependencies:</span></span>

+ <span data-ttu-id="a0b71-185">必须在映射的机器上运行生产订单，并使用映射的批处理属性生成产品以触发警报。</span><span class="sxs-lookup"><span data-stu-id="a0b71-185">A Production Order must be running on a mapped machine and producing a product with a mapped batch attribute for an alert to be triggered.</span></span>
+ <span data-ttu-id="a0b71-186">必须将表示批处理属性的信号发送到具有唯一属性名称的 IoT 中心。</span><span class="sxs-lookup"><span data-stu-id="a0b71-186">A signal representing the batch attribute must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="a0b71-187">IoT 中心消息中必须包含 Unix 毫秒时间戳属性。</span><span class="sxs-lookup"><span data-stu-id="a0b71-187">A Unix milliseconds timestamp property must be present in the IoT Hub message.</span></span>

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a><span data-ttu-id="a0b71-188">在 Supply Chain Management 中配置**生产延迟**方案</span><span class="sxs-lookup"><span data-stu-id="a0b71-188">Configure the **Production delays** scenario in Supply Chain Management</span></span>

<span data-ttu-id="a0b71-189">如果生产完全降到阈值下，**生产延迟**方案将生成通知。</span><span class="sxs-lookup"><span data-stu-id="a0b71-189">The **Production delays** scenario generates a notification if the production throughput falls below a threshold value.</span></span> <span data-ttu-id="a0b71-190">在此方案中，将为生成的每个物料向 IoT 中心发送**部件停止**信号。</span><span class="sxs-lookup"><span data-stu-id="a0b71-190">In this scenario, a **PartOut** signal is sent to IoT Hub for each item produced.</span></span> <span data-ttu-id="a0b71-191">在 Supply Chain Management 中，将根据安排的生产订单运行时长，应该生成的物料数量，以及接收多少**部件停止**信号计算订单延迟。</span><span class="sxs-lookup"><span data-stu-id="a0b71-191">In Supply Chain Management, the order delay is calculated based on how long the production order is scheduled to run, how many items should be produced, how long the job has been running, and how many **PartOut** signals are received.</span></span> <span data-ttu-id="a0b71-192">如果作业的**部件停止**信号数量低于预期值的阈值，将生成延迟通知。</span><span class="sxs-lookup"><span data-stu-id="a0b71-192">A delay notification would be generated if the number of the **PartOut** signals for the job falls below the threshold value of the expected value.</span></span>

<span data-ttu-id="a0b71-193">该方案具有以下依赖性：</span><span class="sxs-lookup"><span data-stu-id="a0b71-193">The scenario has these dependencies:</span></span>

+ <span data-ttu-id="a0b71-194">必须正在映射的机器上运行生产订单，才能触发警报。</span><span class="sxs-lookup"><span data-stu-id="a0b71-194">A Production Order must be running on a mapped machine for an alert to be triggered.</span></span>
+ <span data-ttu-id="a0b71-195">必须将表示映射的机器部件停机信号的型号发送到具有唯一属性名称的 IoT 中心。</span><span class="sxs-lookup"><span data-stu-id="a0b71-195">A signal representing a mapped machine's part out signal must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="a0b71-196">IoT 中心消息中必须包含 Unix 毫秒时间戳属性。</span><span class="sxs-lookup"><span data-stu-id="a0b71-196">A Unix milliseconds timestamp property must be present in the IoT Hub message.</span></span>

## <a name="how-to-disable-a-scenario"></a><span data-ttu-id="a0b71-197">如何禁用方案</span><span class="sxs-lookup"><span data-stu-id="a0b71-197">How to disable a scenario</span></span>

<span data-ttu-id="a0b71-198">若要禁用方案，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="a0b71-198">To disable a scenario, follow these steps:</span></span>

1. <span data-ttu-id="a0b71-199">在 Supply Chain Management 中，导航到**生产控制 \> 设置 \> IoT 智能 \> 方案管理**。</span><span class="sxs-lookup"><span data-stu-id="a0b71-199">In Supply Chain Management, navigate to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
2. <span data-ttu-id="a0b71-200">在方案中单击**配置**。</span><span class="sxs-lookup"><span data-stu-id="a0b71-200">Click **Configure** on the scenario.</span></span>
3. <span data-ttu-id="a0b71-201">单击**下一步**转到上一个向导选项卡。</span><span class="sxs-lookup"><span data-stu-id="a0b71-201">Click **Next** to get to the last wizard tab.</span></span>
4. <span data-ttu-id="a0b71-202">切换滑块以禁用方案。</span><span class="sxs-lookup"><span data-stu-id="a0b71-202">Toggle the slider to disable the scenario.</span></span>

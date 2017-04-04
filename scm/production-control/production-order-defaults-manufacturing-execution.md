---
title: "在制造执行的默认生产订单"
description: 
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: JmgProdParameters
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 70073
ms.assetid: 620944ae-3e20-444a-807e-65495f160904
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: b310e799c1ef0756291c5f7ab886531e4caf1945
ms.lasthandoff: 03/31/2017


---

# <a name="production-order-defaults-in-manufacturing-execution"></a>在制造执行的默认生产订单



在生产作业之前应仔细考虑在**生产订单默认**表页的所有设置，在员工开始执行预留。 如果您的公司使用多站点功能，您可能想要设置生产订单的默认站点的。 与生产控制集成的订单默认值在**生产订单默认值**页的以下选项卡上设置：

-   **常规** –“制造执行”中生产作业的常规订单默认值。
-   **开始** – 生产作业或工序开始时使用的订单默认值。
-   **工序** – 在生产流程中应用于生产作业或工序和工序反馈的订单默认值。
-   **完工入库** - 当物料在生产订单的最后一道工序上报告为已完工入库时所应用的订单默认值。
-   **数量验证** – 用于验证生产订单的开始和反馈数量的订单默认值。

## <a name="types-of-production-jobs"></a>生产作业的类型
在**工序**选项卡上，选择您需要在**作业登记**页上登记的生产作业的类型。 通常情况下，工作人员在设置作业和处理作业上进行登记。 但是，如果应用了作业级排产，则您可以选择工作人员处理生产订单时也必须也其上进行登记的其他作业类型，如运输作业。 **重要提示：**请确保已选择所有相关作业类型。 否则，作业可能不可用于在**作业登记**页上登记。 您的选择与在**工艺路线组**页的**作业管理**列的选择保持一致。 如果在工艺路线组上选择**作业管理**，在生产订单上将报告此作业类型为完工入库。 当该作业在“制造执行”中报告为完工入库时将出现这个报告。 当为其选择**作业管理**的所有作业类型在工序上已报告为完工入库时，“制造执行”也将报告该工序为完工入库。 **注释：**某些作业类型可通过生产日志手动报告。 在这种情况下，为作业类型选择**作业管理**，不过，不要选择此作业类型在**生产订单默认值**页的**工序**选项卡上登记。

## <a name="bom-consumption-and-picking-list-journals"></a>物料清单消耗和领料单日志
可以对物料进行设置，以便它们在生产时自动或手动消耗。 自动消耗由物料清单 (BOM) 行上设置的耗用原则，以及生产订单默认值中**自动物料清单消耗量**字段的设置来控制。 自动消耗量可以进行设置，使其在生产订单开始或报告为已完工入库时发生。 或者，在作业开始或完成时，可以在作业级别中发生。

### <a name="controlling-material-consumption-when-a-production-order-is-started"></a>在开始生产订单时控制物料消耗量

在生产订单开始期间的物料消耗量由**开始**选项卡的**自动物料清单消耗量**字段控制。 提供以下值：

-   **耗用原则** – 在开始生产订单时，物料将根据在生产物料清单行中设置的耗用原则消耗。 仅将耗用原则设置为**开始**的物料行将在生产开始期间消耗。
-   **始终** – 与开始数量成比例的物料数量将始终消耗。
-   **从不** – 物料数量从不消耗。

### <a name="controlling-material-consumption-when-a-production-job-is-started-or-completed"></a>在开始或完成生产作业时控制物料消耗量

在生产作业开始或完成期间的物料消耗量由**工序**选项卡的**自动物料清单消耗量**字段控制。 提供以下值：

-   **耗用原则** – 在开始或完成生产作业的数量时，物料将根据在生产物料清单行中设置的耗用原则消耗。 仅将耗用原则设置为**开始**或**完成**的物料行将消耗。
-   **始终** – 与作业的开始数量成比例的物料数量将始终消耗。
-   **从不** – 物料数量从不消耗。

### <a name="controlling-material-consumption-when-a-production-order-is-reported-as-finished"></a>在生产订单完工入库时控制物料消耗量

在生产订单完工入库流程期间的物料消耗量由**完工入库**选项卡的**自动物料清单消耗量**字段控制。 提供以下值：

-   **耗用原则** – 在生产订单完工入库时，物料将根据在生产物料清单行中设置的耗用原则消耗。 仅将耗用原则设置为**完成**的物料行将消耗。
-   **始终** – 与完工入库的数量成比例的物料数量将始终消耗。
-   **从不** – 物料数量从不消耗。




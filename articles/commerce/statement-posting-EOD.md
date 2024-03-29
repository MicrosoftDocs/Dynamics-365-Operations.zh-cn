---
title: 对账单过帐功能的改进
description: 本文介绍对对报单过帐功能的改进。
author: analpert
ms.date: 05/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: analpert
ms.search.validFrom: 2018-04-30
ms.openlocfilehash: 33b4f17cd46338b62bed96f0a285e7b9634cc87a
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067811"
---
# <a name="improvements-to-statement-posting-functionality"></a>对账单过帐功能的改进

[!include [banner](includes/banner.md)]

本文介绍对对报单过帐功能的第一组改进。 Microsoft Dynamics 365 Finance 7.3.2 中提供了这些改进。

## <a name="activation"></a>岗位设立时间

默认情况下，部署财务和运营 7.3.2 期间，程序设置为使用传统功能执行对帐单过帐。 若要启用改进的对帐单过帐功能，必须为其开启配置键。

- 转至 **系统管理** \> **设置** \> **许可证配置**，然后在 **Retail 和 Commerce** 节点下，清除 **对帐单(旧)** 复选框，然后选中 **对帐单** 复选框。

新的 **对帐单** 配置开启后，将有一个名称为 **对帐单** 的新菜单项。 可通过此菜单项手动创建、计算和过帐对帐单。 可通过此菜单项访问执行批量过帐过程时导致错误的任何过帐单。 （开启 **过帐单(旧)** 配置键后，此菜单项名称为 **未结过帐单**。）

Commerce 中包含与以下配置键有关的验证：

- 这两个配置键不能同时开启。
- 在给定过帐单生命周期（创建、计算、清除、过帐等）内，必须对为该对帐单执行的所有操作使用相同的配置键。 例如，不能在 **对帐单(旧)** 配置键已开启时创建并计算一个对帐单，然后在 **对帐单** 配置键已开启时尝试过帐同一个对帐单。

> [!NOTE]
> 建议使用 **对帐单** 配置键以利用改进的对帐单过帐功能，除非有充分的理由需要改用 **对帐单(旧)** 配置键。 Microsoft 将继续在新增对帐单过帐功能和改进的对帐单过帐功能上投入，而您最好抓住机会尽早转移过去，以便从中受益。 从 8.0 版本开始，将弃用旧对帐单过帐功能。

## <a name="setup"></a>设置

在对帐单过帐功能的改进中，**Commerce 参数** 页 **过帐** 选项卡上 **对帐单** 快速选项卡上引入了三个新参数：

- **禁用清空对帐单** – 此选项仅适用于旧对帐单过帐功能。 建议将此选项设置为 **否**，以免用户清空半过帐状态的对帐单。 如果清空半过帐状态的对帐单，将损坏数据。 应仅在特殊情况下才将此选项设置为 **是**。
- **在计算过程中预留库存** – 建议对库存预留使用 **过帐库存** 批处理作业，并将此选项设置为 **否**。 如果此选项设置为 **否**，则在计算时，改进的对帐单过帐功能不会尝试创建库存预留条目（如果未通过 **过帐库存** 批处理作业创建条目）。 相反，此功能仅在过帐时创建库存预留条目。 此实施为设计选项，基础是计算过程与过帐过程之间的时间段通常极小。 但是，如果要在计算时预留库存，可将此选项设置为 **是**。

    无论此选项如何设置，旧对帐单过帐功能始终在对帐单计算过程中预留库存（如果尚未通过 **过帐库存** 批处理作业执行预留）。

- **禁用所需的盘点** – 如果此选项设置为 **是**，则继续执行对帐单过帐过程，即使对帐单的盘点金额与交易金额之差超出了商店的 **对帐单** 快速选项卡中定义的阈值。

> [!NOTE]
> 从 Commerce 版本 10.0.14 开始，当启用 **零售对帐单 - 缓慢馈送** 功能时，**过帐库存** 批处理作业不再适用，将无法运行。

## <a name="processing"></a>正在处理

可使用菜单项 **成批计算对帐单** 和 **成批过帐对帐单** 计算和过帐对帐单。 也可以使用改进的对帐单过帐功能提供的 **对帐单** 菜单项手动计算和过帐对帐单。

成批计算对帐单和过帐对帐单的流程和步骤相同，因为它们曾经属于旧对帐单过帐功能。 但是，已对对帐单的核心后端处理进行了重大改进。 这些改进提高了流程的弹性，可以更好地查看状态和错误信息。 因此，用户可以解决错误的根源，然后继续执行过帐流程，并且不会导致数据损坏，也不会导致需要修复数据。

以下部分介绍对帐单和已过帐对帐单的用户界面中显示的对帐单过帐功能的主要改进。

### <a name="status-details"></a>状态详细信息

计算流程和过帐流程中的对帐单过帐例程引入了新的状态模型。

下表介绍计算流程中的各种状态及其顺序。

| 状态顺序 | 状态      | 说明 |
|-------------|------------|-------------|
| 1           | 已启动    | 对帐单已创建并且已准备就绪，可以计算。 |
| 2           | 已标记     | 对帐单范围内的交易记录根据对帐单参数标识，并使用对帐单 ID 标记。 |
| 3           | 已计算 | 已计算并显示对帐单行。 |

下表介绍对帐流程中的各种状态及其顺序。

| 状态顺序 | 状态                   | 说明 |
|-------------|-------------------------|-------------|
| 1           | 已检查                 | 已完成了与参数（如处置费用）、对帐单和对帐单行（例如，盘点金额与交易记录金额之差）有关的多项验证。 |
| 2           | 已聚合              | 基于配置聚合指定的客户和未指定的客户的销售交易记录。 聚合的每个交易记录最终都会转换为销售订单。 |
| 3           | 客户订单已创建  | 已基于聚合交易记录在系统中创建了销售订单。 |
| 4           | 客户订单已开票 | 已为销售订单开票。 |
| 5           | 折扣已过帐        | 已基于配置过帐了定期折扣日记帐。 |
| 6           | 收入/费用已过帐   | 收入/费用交易记录已作为凭证过帐。 |
| 7           | 已链接凭证         | 付款日记帐已创建并链接至相应发票。 |
| 8           | 付款已过帐         | 付款日记帐已过帐。 |
| 9           | 礼品卡已过帐       | 礼品卡交易记录已作为凭证过帐。 |
| 10          | 已过帐                  | 对帐单标记为已过帐。 |

上面的表中的每种状态本质上都是独立的，并将在这些状态之间建立层次结构依赖关系。 此依赖关系自上而下。 如果系统在处理状态时遇到任何错误，将把对帐单的状态恢复为上一个状态。 以后只要重试此过程，都将从失败的状态恢复并继续。 这种方法的优点如下：

- 用户可以洞察出错的状态。
- 避免损坏数据。 例如，在传统对帐单过帐功能中，有时已经为一些销售订单开票，但是另一些却处于未结状态。 还有时一些付款日记帐没有要结算的对应发票，因为发票过帐已出错。
- 用户可以使用对帐单的 **执行详细信息** 组中的 **状态详细信息** 按钮查看对帐单的当前状态。 状态详细信息页分为三部分：

    - 列表部分显示对帐单的当前状态，以及错误代码和详细的错误消息（如果出错）。
    - 第二部分显示计算过程的各状态。 可视提示指示已运行成功的状态、因出错而无法运行的状态和尚未运行的状态。
    - 第三部分显示过帐过程的各状态。 可视提示指示已运行成功的状态、因出错而无法运行的状态和尚未运行的状态。

此外，第二部分和第三部分的标题还显示相关过程的总体状态。

### <a name="event-logs"></a>事件日志

一个对帐单会经历各种操作（如创建、计算、清除和过帐），而在对帐单的生命周期内，可能会多次调用同一个操作。 例如，创建并计算对帐单之后，用户可以清除并再次计算该对帐单。 对帐单的 **执行详细信息** 组中的 **事件日志** 按钮提供对对帐单调用的各操作的完整审计线索，以及有关何时调用这些操作的信息。

### <a name="aggregated-transactions"></a>聚合交易记录

在过帐流程中，现金和结转交易记录按客户和产品聚合。 因此，已创建的销售订单和行的数量将减少。 聚合交易记录存储在系统中，用于创建销售订单。 每个聚合交易记录在系统中创建一个对应的销售订单。 

如果对帐单未完全过帐，您可以在对帐单中查看聚合交易记录。 在操作窗格上 **对帐单** 选项卡上的 **执行详细信息** 组中，选择 **聚合交易记录**。

![未完全过帐的对帐单的聚合交易记录按钮。](media/aggregated-transactions.png)

对于已过帐的对帐单，您可以在 **已过帐对帐单** 页面上查看聚合交易记录。 在操作窗格上，选择 **查询**，然后选择 **聚合交易记录**。

![已过帐对帐单的聚合交易记录命令。](media/aggregated-transactions-posted-statements.png)

聚合交易记录的 **销售订单详细信息** 快速选项卡显示以下信息：

- **记录 ID** – 聚合交易记录的 ID。
- **对帐单编号** – 聚合交易记录所属的对帐单。
- **日期** – 聚合交易记录的创建日期。
- **销售 ID** – 从聚合交易记录创建销售订单后的销售订单 ID。 如果此字段为空，说明尚未创建对应的销售订单。
- **已聚合的行的数目** – 聚合交易记录和销售订单的总行数。
- **状态** – 聚合交易记录的最新状态。
- **发票 ID** – 为聚合交易记录的销售订单开票后的销售发票 ID。 如果此字段为空，说明尚未过帐销售订单的发票。
- **错误代码** – 如果聚合处于错误状态，将设置此字段。
- **错误消息** – 如果聚合处于错误状态，将设置此字段。 它显示导致流程失败的原因的详细信息。 您可以使用错误代码中的信息来修复问题，然后手动重新启动流程。 根据解决方法的类型，聚合销售可能必须删除，在新对帐单上进行处理。

![聚合交易记录的“销售订单详细信息”快速选项卡上的字段。](media/aggregated-transactions-error-message-view.png)

聚合交易记录的 **交易详细信息** 快速选项卡显示已导入到聚合交易记录中的所有交易记录。 聚合交易记录上的聚合行显示来自交易记录的所有聚合记录。 聚合行还显示所有详细信息，如物流、变型、数量、价格、净额、单位和仓库。 基本上，每个聚合行都对应一个销售订单行。

![聚合交易记录的“交易记录详细信息”快速选项卡。](media/aggregated-transactions-sales-details.png)

在某些情况下，聚合交易记录可能无法过帐合并的销售订单。 在这些情况下，错误代码将与对帐单状态相关联。 要仅查看有错误的聚合交易记录，您可以通过选中复选框在聚合交易记录视图中启用 **仅显示失败** 筛选器。 启用此筛选器，您可以将结果限制为具有需要解决的错误的聚合交易记录。 有关如何修复这些错误的信息，请参阅[编辑并审计在线订单和异步客户订单交易记录](edit-order-trans.md)。

![聚合交易记录视图中“仅显示失败”筛选器的复选框。](media/aggregated-transactions-failure-view.png)

在 **聚合交易记录** 页面上，您可以通过选择 **导出聚合数据** 下载特定聚合交易记录的 XML。 您可以在任何 XML 格式化程序中查看 XML，来查看涉及销售订单创建和过帐的实际数据详细信息。 已过帐的对帐单不支持下载聚合交易记录的 XML。

![聚合交易记录页面上的“导出聚合数据”按钮。](media/aggregated-transactions-export.png)

如果您无法通过更正销售订单上的数据或支持销售订单的数据来修复错误，可以使用 **删除客户订单** 按钮。 要删除订单，选择失败的聚合交易记录，然后选择 **删除客户订单**。 聚合交易记录和相应的销售订单都将被删除。 您现在可以使用编辑和审计功能来查看交易记录。 或者，可以通过新对帐单重新处理它们。 修复所有失败后，您可以通过运行相关对帐单的过帐对帐单函数来恢复对帐单的过帐。

![聚合交易记录视图中的“删除客户订单”按钮。](media/aggregated-transactions-delete-cust-order.png)

聚合交易记录视图具有以下优点：

- 用户可以查看销售订单创建期间失败的聚合交易记录和开票期间失败的销售订单。
- 用户可以查看交易记录如何聚集。
- 用户拥有从交易记录到销售订单，再到销售发票的完整审计线索。 此审计线索在传统对帐单过帐功能中不可用。
- 通过聚合 XML 文件可以更轻松地识别销售订单创建和开票期间出现的问题。

> [!NOTE]
> 聚合交易后，分配给交易的工作人员不再适用于 **排名靠前的员工销售额报表**，这意味着 **排名靠前的员工销售额报表** 将不会显示所有交易。 我们建议您不要将 **排名靠前的员工销售额报表** 用于聚合交易。

### <a name="journal-vouchers"></a>日记帐凭证

对帐单的 **执行详细信息** 组中的 **日记帐凭证** 按钮显示为对帐单创建的和为与折扣、收入/费用科目、礼品卡等有关的所有各种凭证交易记录。

本程序现在仅显示已过帐对帐单的这些数据。

### <a name="payment-journals"></a>付款日记帐

对帐单的 **执行详细信息** 组中的 **付款日记帐** 按钮显示为对帐单创建的所有各种付款日记帐。

本程序现在仅显示已过帐对帐单的这些数据。

## <a name="other-improvements"></a>其他改进

已对对帐单过帐功能进行了用户可查看的其他后端改进。 下面举了一些示例加以说明：

- 聚合不考虑员工、终端和班次实体。 由于聚合参数较少，所以必须处理的销售订单行也较少。
- 通过引入更多扩展表和对交易记录表执行插入操作，而不是执行更新操作，降低了交易记录表死锁的出现。
- 运行批处理任务的数量已参数化并受到限制。 因此，可专门针对客户的环境调整此数字。 在传统对帐单过帐功能中，同时可创建的批处理任务数量不受限制。 结果是服务器承受难以处理的负载、开销和瓶颈。
- 可通过为具有最大交易记录数量的对帐单设置优先级，高效地为对帐单设置队列以进行处理。
- **成批计算对帐单** 和 **成批过帐对帐单** 之类批处理流程将以批处理模式运行。 在传统对帐单过帐功能中，用户可以选择以交互模式运行这些批处理流程，这种模式是单线程操作，与批处理流程不同，后者为多线程。
- 在传统对帐单过帐功能中，只要批处理任务失败，都将让整个批处理作业进入错误状态。 在改进后的功能中，如果其他批处理任务成功完成，则批处理任务失败不会让批处理作业进入错误状态。 应评估批处理执行的对帐状态，方法是使用 **对帐单** 页，可在其中查看因错而未过帐的所有对帐单。
- 在传统对帐单过帐功能中，对帐单首次出错将导致整个批处理失败。 将不处理剩余对帐单。 在改进后的功能中，批处理流程将继续处理所有对帐单，即使部分对帐单失败也不例外。 其中一个优点是用户可查看准确的出错对帐单数量。 这样用户就不必陷入修复错误并运行对帐单过帐流程直到所有对帐单均已过帐的连续循环中。

## <a name="general-guidance-about-the-statement-posting-process"></a>有关对帐单过帐流程的一般指南

- 建议成批运行对帐单过帐流程，因为成批运行可以以多线程的形式利用批处理框架。 需要多线程才能应对通常在对帐单过帐中才会出现的巨量交易记录。
- 建议在物料模型组中开启负实际库存，以便获得无缝的过帐体验。 在某些情况下，除非存在负实际库存，否则可能不能过帐负对帐单。 例如，理论上如果库存中某种物料只有一个单位，但同时有一个销售交易记录和一个退货交易记录需要该物料，即使未开启负库存，应该也可以过帐交易记录。 但是，因为对帐单过帐流程同时提取销售交易记录和退货交易记录并放入一个销售订单中，所以不能保证先过帐销售行，后过帐退货行。 因此可能出错。 如果在这种情况下开启了负库存，则交易记录过帐不会受到负面影响，而系统将正确地反映库存。
- 建议在计算和过帐对帐单时使用聚合。 因此，建议为部分聚合参数执行以下设置：

    - 转到 **Retail 和 Commerce** \> **Headquarters 设置** \> **参数** \> **Commerce 参数**。 然后，在 **过帐** 选项卡上 **库存更新** 快速选项卡的 **详细程度** 字段中，选择 **摘要**。
    - 转到 **Retail 和 Commerce** \> **Headquarters 设置** \> **参数** \> **Commerce 参数**。 然后，在 **过帐** 选项卡上的 **聚合** 快速选项卡中，将 **凭证交易记录** 选项设置为 **是**。


[!INCLUDE[footer-include](../includes/footer-banner.md)]


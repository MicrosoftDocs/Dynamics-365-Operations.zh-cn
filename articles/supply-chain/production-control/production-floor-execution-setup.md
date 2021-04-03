---
title: 设置设备以运行生产车间执行界面
description: 为生产车间中的每个设备设置生产车间执行界面。 公司通常以不同方式设置每个设备，具体取决于设备的用途。 例如，一家公司可能在接待区有一个设备，以供工作人员上班打卡和下班打卡，而在车间有另一个设备，以供工作人员管理作业。
author: johanhoffmann
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgProductionFloorExecution, HcmWorker, JmgProductionFloorExecutionDeviceConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 641273dd3ae189853326bf7af7ceb06d48465b5c
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500542"
---
# <a name="set-up-a-device-to-run-the-production-floor-execution-interface"></a>设置设备以运行生产车间执行界面

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

为生产车间中的每个设备设置生产车间执行界面。 公司通常以不同方式设置每个设备，具体取决于设备的用途。 例如，一家公司可能在接待区有一个设备，以供工作人员上班打卡和下班打卡，而在车间有另一个设备，以供工作人员管理作业。

## <a name="set-the-configuration-and-filters-for-a-specific-device"></a>为特定设备设置配置和筛选器

若要为设备设置配置和作业筛选器，请使用具有包括 *维护时间主管* 责任的安全角色的帐户登录到 **生产车间执行** 页面。 （在开箱即用的安全角色中，仅 *车间主管* 具有此责任。）然后，按照以下步骤操作。

1. 转到要设置的设备，然后以车间主管的身份登录到 Microsoft Dynamics 365 Supply Chain Management。 （使用包括 *维护时间主管* 责任的帐户。）
1. 确保为您要设置的设备提供配置。 如果尚无配置，则提供默认配置。 有关如何设置配置的详细信息，请参阅[配置生产车间执行界面](production-floor-execution-configure.md)。
1. 转到 **生产控制 \> 制造执行 \> 生产车间执行**。

    如果已经在当前设备上配置了生产车间执行界面至少一次，将显示登录页面。 否则，将显示欢迎页面。

1. 在登录页面或欢迎页面上，选择 **配置**。
1. 在列表中选择配置。
1. 选择 **下一步**。
1. 选择一个或多个筛选器以应用于当前设备。 这些筛选器将有助于确保仅在设备上显示相关作业。 若要设置筛选器，请选择筛选器类型以打开值列表，然后选择要进行筛选的值。 提供以下筛选器：

    - **生产单位** – 此筛选器是最高级别的筛选器。 它通常是指具有多个资源组以及单独资源的大型工作区。
    - **资源组** – 此筛选器是中等级别的筛选器。 它通常是指工作区的有限区域中相关资源的集合。 如果首先选择 **生产单位** 筛选器，资源组列表将仅显示该单元中的组。 否则，它将显示所有可用的资源组。
    - **资源** – 此筛选器是最具体的筛选器。 它通常是指特定的机器或其他单个资源。 如果首先选择 **资源组** 和/或 **生产单位** 筛选器，资源列表将仅显示该组和/或该单元中的资源。 否则，它将显示所有可用的资源。

1. 选择 **确定**。
1. 显示登录页面，您的设备可供使用。

## <a name="allow-a-worker-to-override-the-default-filters"></a>允许工作人员替代默认筛选器

您可以授予特定工作人员在使用的任何设备上更改筛选器设置的权限。 对于拥有此权限的工作人员，生产车间执行界面在 **所有作业** 和 **活动作业** 页面上提供了 **筛选器** 按钮。

> [!NOTE]
> 如果工作人员更改筛选器，之后将针对登录到该设备的所有用户应用新的筛选器。

若要允许工作人员替代已为设备设置的默认作业筛选器，请按照以下步骤操作。

1. 转到 **考勤管理 \> 设置 \> 时间登记工作人员**。
1. 在列表中选择一个工作人员以打开该工作人员的 **时间登记工作人员** 页面。
1. 在 **时间登记** 选项卡上，将 **设置筛选器** 选项设置为 *是*。

## <a name="run-the-interface-in-full-screen-mode"></a>以全屏模式运行界面

通常，您将在专用于此目的的设备上运行生产车间执行界面。 因此，在不显示任何导航和/或浏览器 Chrome 的情况下，以全屏模式运行界面可能很有意义。

- 若要隐藏 Supply Chain Management 中显示的导航窗格，请将以下文本添加到浏览器地址栏中的 URL 的末尾：`\&limitednav=true`。
- 若要同时隐藏浏览器的地址栏，请使用浏览器的本机全屏模式。 （有关说明，请参阅您的浏览器的文档。）

下图的上部显示了默认情况下界面的外观。 下部显示了隐藏导航窗格时全屏模式下界面的外观。

![标准与全屏界面](media/pfei-full-screen.png "标准与全屏界面")

## <a name="extend-the-session-past-12-hours"></a>将会话延长超过 12 小时

默认情况下，如果 12 个小时内没有人使用，生产车间执行界面会自动注销。 然后，Supply Chain Management 用户必须再次登录。 但是，您可以将超时限制最多延长 90 天。

若要延长超时限制，请登录 Supply Chain Management，然后转到 **系统管理 \> 用户 \> 会话扩展**。 指定用于登录设备的 Supply Chain Management 用户帐户，以及会话应保持活动状态的小时数。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
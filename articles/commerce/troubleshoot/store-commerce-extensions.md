---
title: 解决 Store Commerce 扩展问题
description: 本文介绍如何解决 Microsoft Dynamics 365 Commerce Store Commerce 应用中的扩展问题。
author: josaw1
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 1a2d6a68b7556d8b4d05529efd90f9e66f0c5925
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269773"
---
# <a name="troubleshoot-store-commerce-extension-issues"></a>解决 Store Commerce 扩展问题

[!include [banner](../includes/banner.md)]

本文介绍如何解决 Microsoft Dynamics 365 Commerce Store Commerce 应用中的扩展问题。

## <a name="extensions-packages-arent-loaded"></a>扩展包未加载

### <a name="extensions-packages-dont-appear-on-the-pos--settings-page"></a>扩展包未出现在 POS \> 设置页面上

Commerce runtime (CRT) 触发器可能尚未更新，还不包括扩展包，或者未部署。 有关详细信息，请参阅 [Commerce Runtime (CRT) 可扩展性和触发器](../dev-itpro/commerce-runtime-extensibility-trigger.md)。

### <a name="extensions-packages-appear-on-the-pos--settings-page-but-the-manifest-isnt-loaded"></a>扩展包出现在 POS \> 设置页面上，但未加载清单

确认 **C:\\Program Files\\Microsoft Dynamics 365\\10.0\\Store Commerce\\Extensions** 文件夹中存在扩展包。 如果包存在，应该有包含清单的 **POS** 文件夹。

如果没有 **POS** 文件夹，请确认 Store Commerce 项目正确引用了销售点 (POS) 扩展项目。 验证项目引用路径，确保它存在。 

在以下示例说明中，安装程序项目在引用的扩展项目中有问题。

![Store Commerce 安装程序项目引用无效。](media/ReferenceNotValid.png)

如果正确添加了扩展项目的引用，安装程序项目中不会出现任何警告或依赖关系问题，如以下示例说明中所示。

![Store Commerce 安装程序项目引用有效。](media/ReferenceValid.png)

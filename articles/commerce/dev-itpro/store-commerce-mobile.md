---
title: 适用于移动平台的 Store Commerce 应用
description: 本文介绍如何开始使用适用于 Android 和 iOS 的 Microsoft Dynamics 365 Commerce Store Commerce 应用。
author: stuharg
ms.date: 11/30/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2018-10-29
ms.openlocfilehash: dc952698a2a3301aff312e8310c58cbbb9cfe290
ms.sourcegitcommit: 2804b05214c87f76457608b5db072582ff339852
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/01/2022
ms.locfileid: "9815775"
---
# <a name="store-commerce-app-for-mobile-platforms"></a>适用于移动平台的 Store Commerce 应用

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

本文介绍如何开始使用适用于 Android 和 iOS 的 Microsoft Dynamics 365 Commerce Store Commerce 应用。

适用于 Android 和 iOS 的 Dynamics 365 Commerce 移动应用使为您的零售环境部署全功能移动销售点 (POS) 设备的过程变得简单直接。 Store Commerce 移动应用几乎提供了[适用于 Windows 的 Store Commerce 应用](store-commerce.md)的所有功能和优势，在各种 iOS 和 Android 手机和平板电脑上都有良好的表现。 Store Commerce 移动应用可以直接从 Apple 和 Google Play 应用商店安装，不需要开发人员创建新应用程序包来进行部署或更新。 

Store Commerce 移动应用保留了与当前零售混合应用相同的全部功能。 此外，适用于 iOS 的 Store Commerce 还支持专用硬件工作站，让 iOS 设备可以与联网的付款终端、收据打印机和银箱通信，而无需部署共享硬件工作站。 

> [!IMPORTANT]
> 适用于 Windows、Android 和 iOS 的 Store Commerce 应用是下一代适用于 Dynamics 365 Commerce 的 POS 应用程序。 Store Commerce 应用对之前版本进行了大量改进，同时保留了完整的功能和功能一致性。 Microsoft 将在 2023 年末弃用 MPOS 以及 Android 和 iOS Retail POS hybrid 应用，建议您在所有新的 POS 部署中使用 Store Commerce 或 Cloud POS (CPOS)。 现有客户应计划从零售混合应用迁移到 Store Commerce。 有关详细信息，请参阅[将 Modern POS 迁移到 Store Commerce](pos-extension/migrate-mpos-store-commerce.md)。 

## <a name="app-architecture"></a>应用体系结构

当以混合模式部署时，Store Commerce 移动应用使用与适用于 Windows 的 Store Commerce 应用相同的拓扑。 Store Commerce 移动应用是直接从 Commerce Scale Unit (CSU) 呈现 CPOS 的 shell 应用程序，通过 CSU 连接到无头商业和 Commerce headquarters。 此 Shell 应用程序模型让 Store Commerce 应用能够支持专用硬件工作站，以与付款终端、打印机、银箱和其他外围设备直接集成。 使用硬件设备不需要设置共享硬件工作站。 

要更新 Store Commerce 移动应用，只需更新 CSU。 所有新的 POS 功能和特性将由应用自动选取。 有关如何更新 CSU 的详细信息，请参阅[将更新和扩展应用于 Commerce Scale Unit（云）](../../fin-ops-core/dev-itpro/deployment/update-retail-channel.md)。

Shell 应用通过应用商店更新获得支持。 当一个次要版本达到正式发布 (GA) 阶段时，Microsoft 会将它发布到应用商店。 Microsoft 还可能会在次要版本更新之间发布修补程序，以发布高优先级的 bug 修复。

## <a name="prerequisites"></a>先决条件

Store Commerce 移动应用需要 Dynamics 365 Commerce，特别是 Commerce headquarters 和 CSU 组件。 下表列出了 Android 和 iOS 移动应用所需的最低操作系统 (OS) 和 CSU 版本。 

| 先决条件 | Android      | iOS  |
| ------------ | ------------ | ---- |
| 操作系统版本   | 7.0          | 15.0 |
| CSU 版本  | 9.38.22266.8 | 待定义  |

## <a name="install-the-app"></a>安装应用

您可以直接从 Google Play 商店或 Apple App Store 安装 Store Commerce 移动应用。 

- [适用于 Android 的 Store Commerce 应用](https://aka.ms/storecommerceandroid)
- [适用于 iOS 的 Store Commerce 应用](https://aka.ms/storecommerceios)

Android 应用 (.apk) 和 Apple 应用 (.ipa) 包也可以从 Microsoft Dynamics Lifecycle Services 中的共享资产库下载。 

## <a name="device-and-register-setup"></a>设备和收银机设置

您必须先在 Commerce headquarters 中设置设备和收银机，然后才能够在 Store Commerce 移动应用上激活收银机。 有关详细信息，请参阅[设备和收银机](../implementation-considerations-devices.md)。 

### <a name="device-setup"></a>设备设置

要创建和设置新设备，请执行以下步骤。

1. 在 Commerce Headquarters 中，转到 **Retail 和 Commerce \> 渠道设置 \> POS 设置 \> 设备**。 
1. 创建新设备，然后根据您部署的移动应用，选择 **现代 POS - Android** 或 **现代 POS - iOS** 作为应用程序类型。 

    > [!NOTE] 
    > **现代 POS - Android** 和 **现代 POS - iOS** 应用程序类型也用于部署最新的适用于 Android 和 iOS 的混合应用。 MPOS 弃用后，这些应用程序类型的标签将更新为 **Store Commerce - Android** 和 **现代 POS - iOS**。 

### <a name="register-setup"></a>收银机设置

您可以创建新收银机并将其与您创建的设备关联，也可以将现有收银机与新设备关联。 有关收银机的更多信息，请参阅[创建和关联收银机](../tasks/create-associate-registers.md)。

### <a name="screen-layout-setup"></a>屏幕布局设置

如果您要重新调整通过 Dynamics 365 Commerce 许可证提供的演示数据中包含的屏幕布局的用途，当设备的屏幕分辨率在纵向上低于 480 &times; 853 像素时，Store Commerce 应用将自动选择包含的紧凑布局。 但是，如果您是从头创建屏幕布局，或者您的移动设备使用的分辨率大于紧凑布局支持的分辨率，请确保您创建的分辨率和关联的按钮网格适合您计划部署到的手机或平板电脑。 有关屏幕布局配置的更多信息，请参阅 [POS 用户界面视觉效果配置](../pos-screen-layouts.md)。 

配置好设备和收银机后，在 Commerce headquarters 中，转到 **Retail 和 Commerce \> 零售和商业 ID \> 配送计划**，运行收银机作业。

## <a name="activate-a-device"></a>激活设备

要在 Store Commerce 移动应用上激活设备，请执行以下步骤。

1. 在移动设备上打开此应用。
1. 输入 CPOS URL，您可以在 Lifecycle Services 中的环境详细信息页面，或在 Commerce headquarters 中的 **渠道配置文件** 页面上找到它（**Retail 和 Commerce \> 渠道设置 \> 渠道配置文件**）。
1. 使用具有管理设备权限的工作人员的凭据登录。
1. 选择与您在 Commerce headquarters 中创建或重复使用的收银机关联的商店。
1. 选择与您在 Commerce headquarters 中创建的设备关联的收银机。
1. 您的设备现在应该已激活。 您可以使用与您选择的商店关联的工作人员的操作员 ID 和密码登录到收银机。 

有关设备激活的更多信息，请参阅[销售点 (POS) 设备激活](retail-device-activation.md#activate-a-modern-pos-or-cloud-pos-device-by-using-guided-activation)。

## <a name="feature-parity-with-store-commerce-for-windows"></a>与适用于 Windows 的 Store Commerce 的功能一致性

下表比较了 Windows、Android 和 iOS 平台上的 Store Commerce 应用的功能。

| 功能                                                                               | 窗口 | Android | iOS |
| ------------------------------------------------------------------------------------- | ------- | ------- | --- |
| 专用硬件工作站                                                            | 是     | 是     | 是 |
| 共享硬件工作站                                                               | 是     | 是     | 是 |
| 与联网的外围设备（付款终端、打印机和银箱）通信 | 是     | 是     | 是 |
| 通过本地硬件工作站运行的销售点 (POS) 外围设备的 OLE             | 是     | 否      | 否  |
| 脱机模式                                                                          | 是     | 否      | 否  |

## <a name="additional-resources"></a>其他资源

[Store Commerce 应用](store-commerce.md)

[选择 Store Commerce 或 Cloud POS](../mpos-or-cpos.md)

[解决 Store Commerce 设置和安装问题](../troubleshoot/store-commerce-setup-installation.md)

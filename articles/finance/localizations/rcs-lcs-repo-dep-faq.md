---
title: Regulatory Configuration Service (RCS) - Lifecycle Services (LCS) 存储弃用
description: 本主题提供有关计划作为 Regulatory Configuration Service (RCS) 全局存储库推出的一部分的 Microsoft Dynamics Lifecycle Services (LCS) 存储弃用的信息。
author: JaneA07
ms.date: 05/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, LCS storage, LCS storage deprecation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.19
ms.openlocfilehash: abaeb34db1d209fa8e5cc83a98c333f42e91f2d2
ms.sourcegitcommit: 7cda434becd198c1cd405e001289777ae7a24fe1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2021
ms.locfileid: "6127911"
---
# <a name="regulatory-configuration-service-rcs--lifecycle-services-lcs-storage-deprecation"></a>Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) 存储弃用

[!include [banner](../includes/banner.md)]

使用 Microsoft Dynamics Lifecycle Services (LCS) 作为电子申报 (ER) 配置的存储库将弃用。 此弃用将涉及以下更改：

- 在 Microsoft Dynamics 365 应用程序中使用的 Microsoft 生产的配置将不再发布到 LCS 中的共用资产库。 相反，它们将仅通过 RCS 全局存储库发布。 但是，Dynamics AX 2012 的配置将继续发布到 LCS 中的共用资产库，直到 AX 2012 的支持生命周期结束。
- 允许您将配置从 Finance and Operations 应用和从 RCS 上传到 LCS 中的项目资产库的功能将停用。 但是，您仍然可以使用 LCS 中的浏览器将配置上传到项目资产库。 因此，您仍然可以向 LCS 添加配置，以便将它们包含在解决方案包中。
- 在一段时间内，从 LCS 导入配置将继续可用，并在 Finance and Operations 应用和 RCS 中受支持。 但是，该功能最终将弃用。 （确切的弃用日期将在稍后公布。）

## <a name="deprecation-notice"></a>弃用通知

将在 [Dynamics 365 Finance 中的删除或弃用功能 - LCS 弃用通知](../get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release)中传达使用 LCS 作为存储的弃用。 计划弃用日期为 2022 年 4 月 1 日。

## <a name="key-features"></a>主要功能

- 您可以使用 RCS 创建和编辑配置。 然后，可以将这些配置直接从设计器推送到连接的应用程序。 因此，您可以快速更改和测试您的配置。
- 全局存储库是所有 ER 配置的集中存储。

## <a name="guidance-for-one-time-and-ongoing-actions"></a>一次性和持续操作的指南

本部分介绍了必须一次性完成的一组步骤。 它还介绍了必须持续完成的步骤。

### <a name="one-time-action"></a>一次性操作

将所有必需的配置从 LCS 导入到 RCS，然后将其从 RCS 发布到全局存储库。 如果您使用特定于项目的资产库在 LCS 中存储派生的配置，则必须在 LCS 仍可访问时完成以下步骤。

1. 如果 RCS 实例尚不可用，请提供一个。 有关详细信息，请参阅 [RCS 概述](rcs-overview.md)。
2. 在预配的 RCS 实例中，对于资产库中包含派生的 ER 配置的每个 LCS 项目，注册相应的 LCS 存储库。
3. 将 ER 配置从 LCS 存储库导入到 RCS。 有关详细信息，请参阅[从 LCS 导入配置](../../dev-itpro/analytics/tasks/er-import-configuration-lifecycle-services.md)。
4. 如果未自动提供全局存储库，请在 RCS 中注册它。
5. 将所有派生的配置从当前的 RCS 实例上传到全局存储库。 使用 **允许用户通过一次操作将所有配置上传到 GR 的配置包** 功能来帮助上传。 有关详细信息，请参阅 [RCS 全局存储库上传](rcs-global-repo-upload.md)。

### <a name="going-forward"></a>持续操作

使用 RCS 中的视觉设计器创建所有新配置。 然后，将配置上传到全局存储库以进行存储。 有关详细信息，请参阅[在 RCS 中创建 ER 配置并上传到全局存储库](rcs-global-repo-upload.md)。

## <a name="frequently-asked-questions"></a>常见问题

### <a name="does-this-change-mean-that-lcs-cant-be-used-as-central-storage-for-configurations"></a>此更改是否意味着 LCS 不能用作配置的中央存储？

是。 允许您将配置从 Finance and Operations 应用上传到 LCS 中的项目资产库的功能将弃用。 但是，您仍然可以根据需要使用 LCS 中的浏览器将配置上传到项目资产库。

### <a name="i-thought-that-rcs-was-a-replacement-repository-for-importing-global-template-files-i-didnt-think-that-its-used-to-store-configurations-which-is-correct"></a>我认为 RCS 是用于导入全局模板文件的替代存储库。 我没有想过使用它来存储配置。 哪个是对的？

RCS 是用于创建和编辑 ER 配置的设计服务。 RCS 有自己的存储库，称为全局存储库。 此存储库用于存储在 RCS 中创建的配置。 在使用 LCS 作为存储弃用后，全局存储库将是 Microsoft 配置的单一来源。 您必须完成一次性操作，将所需的所有配置从 LCS 导入到 RCS，然后将其从 RCS 发布到全局存储库。

### <a name="without-lcs-what-is-the-suggested-way-to-store-configurations-so-that-test-and-production-configurations-can-easily-be-managed-and-transferred"></a>如果没有 LCS，建议使用什么方法存储配置，以便可以轻松管理和传输“测试”和“生产”配置？

RCS 使用 *连接的应用程序* 概念。 连接的应用程序在 RCS 和 Finance and Operations 应用的任何实例之间建立一个连接。 因为 RCS 可用于编辑配置，因此可使用连接的应用程序将配置直接从设计人员推送到 Finance and Operations 应用环境。 因此，您可以快速更改和测试您的配置，而不必经过 LCS 项目级存储。

### <a name="are-there-any-examples-that-show-the-setup-and-management"></a>是否有显示设置和管理的任何示例？

没有示例，但您可以完成本主题前面的步骤，以将您的配置迁移到 RCS 全局存储库。

---
title: 电子报告 (ER) 扩展格式查找
description: 本文描述了将所需格式存储在全局存储库中时如何在 ER 格式查询中设置 ER 格式参考。
author: NickSelin
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: ae544b8ed4e280ffcaf58d893056a4bf5169e379
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901639"
---
# <a name="allow-users-to-set-up-an-er-format-reference-inquiring-a-format-from-the-global-repository"></a>允许用户设置 ER 格式参考，以从全局存储库中查询格式

[!include [banner](../includes/banner.md)]

您可以使用[电子报告 (ER)](general-electronic-reporting.md) 框架，以根据各个国家/地区的法律要求为出站文档配置格式。 您还可以使用 ER 框架配置用于解析入站文档的格式，并使用这些文档中的信息附加或更新应用程序数据。 其中每种格式都可以在 Dynamics 365 Finance 实例中用于在特定业务流程中处理入站或出站业务文档。

通常，您必须指定特定业务流程中必须使用哪种 ER 格式。 为此，请在配置为业务流程特定参数的一部分的查找字段中选择单一 ER 格式。 这些查找字段通常用 ER 框架的适当 API 来实现。 有关更多信息，请参见 [ER 框架 API - 用于显示格式映射查找的代码](er-apis-app73.md#code-to-display-a-format-mapping-lookup)。

例如，当您配置[外贸参数](../../../finance/localizations/emea-intrastat.md#set-up-foreign-trade-parameters)时，您需要设置对各种 ER 格式的引用，这些格式将用于生成 Intrastat 声明和 Intrastat 声明控制报告。 以下屏幕截图显示了 ER 格式查找字段在 **外贸参数** 页面中的外观。

如果当前的 Finance 实例不包含与 Intrastat 业务流程相关的 ER 格式，则此查找字段将为空。

[![外贸参数页面，空“报表格式映射”字段。](./media/ER-ExtLookup-Lookup1.gif)](./media/ER-ExtLookup-Lookup1.gif)

如果当前的 Finance 实例包含与 Intrastat 业务流程相关的 ER 格式，则此查找字段将提供 ER 格式。

[![外贸参数页面，具有选项的“报表格式映射”字段。](./media/ER-ExtLookup-Lookup2.png)](./media/ER-ExtLookup-Lookup2.png)

此查找仅提供已导入到当前 Finance 实例的 ER 格式。 要将 ER 解决方案[导入](./tasks/er-import-configuration-lifecycle-services.md)到当前 Finance 实例中，您需要有权运行 ER 框架的适当功能，并且该框架支持包含 ER 格式的 ER 解决方案的[生命周期](general-electronic-reporting-manage-configuration-lifecycle.md)。

从 Finance 版本 10.0.9（2020 年 4 月发布）开始，已扩展了用 ER 框架 API 实现的 ER 格式查找用户界面。 您仍然可以选择 **选择格式配置** 快速选项卡上的现有 ER 格式。 此外，扩展查找还提供了新的选项来搜索全局存储库 (GR) 以查找特定的 ER 格式。 GR 的所有 ER 格式均在 **从全局知识库导入** 快速选项卡上提供。

[![外贸参数页面，“从全局知识库导入”快速选项卡。](./media/ER-ExtLookup-Lookup3.png)](./media/ER-ExtLookup-Lookup3.png)

类似于 **选择格式配置** 快速选项卡，**从全局知识库导入** 快速选项卡仅显示适用于在此查找字段选择 ER 格式所针对的业务流程的 ER 格式。 在此示例中，生成 Intrastat 声明。 ER 格式适用于用户当前登录的公司，具体取决于公司所在国家/地区的上下文。

在 **从全局知识库导入** 快速选项卡上选择 ER 格式时，会从 GR 将选定的 ER 格式[配置](general-electronic-reporting.md#Configuration)导入到当前的 Finance 实例中。

[![外贸参数页面，处理工序注释。](./media/ER-ExtLookup-FormatImport.png)](./media/ER-ExtLookup-FormatImport.png)

然后，如果导入成功完成，则对导入的 ER 格式的引用将存储在此查找字段中。 首次访问 GR 时，您需要点击提供的链接以注册用于管理对 GR 存储的访问的 [Regulatory Configuration Service](https://aka.ms/rcs) (RCS)。

[![外贸参数页面，注册 RCS 的链接。](./media/ER-ExtLookup-RepoSignUp.png)](./media/ER-ExtLookup-RepoSignUp.png)

默认情况下，**从全局知识库导入** 快速选项卡会显示基于 GR 内容自动创建的临时存储中的 ER 格式列表，以提高性能。 第一次打开 **从全局知识库导入** 快速选项卡时会出现这种情况，打开过程可能需要几秒钟。

如果您在 **从全局知识库导入** 快速选项卡中没有看到所需的 ER 格式，但是您确定此 ER 格式存储在 GR 中，请选择 **同步** 选项。 此选项将更新临时存储并将其与 GR 的当前内容同步。

## <a name="feature-activation"></a>功能激活

此功能的可用性由 **功能管理** 中的 **允许查询全局知识库的 ER 格式配置的扩展查找** 功能控制。 默认情况下启用了此功能。

[![功能管理页面。](./media/ER-ExtLookup-FeatureMngt.png)](./media/ER-ExtLookup-FeatureMngt.png)

## <a name="security-considerations"></a>安全考虑

**维护配置库** (**ERMaintainSolutionRepositories**) 权限控制通过启用的 **从全局知识库导入** 快速选项卡打开 ER 格式查找的用户是否能够访问 GR。 要允许用户从 ER 格式查找中访问 GR 内容，您需要直接或者通过使用已分配的角色和职责向客户授予 **ERMaintainSolutionRepositories** 权限，以更改安全设置。

以下屏幕截图显示了如何将此权限授予分配有 **会计** 角色的用户。 该角色允许用户在 **外贸参数** 页上的 **文件格式映射** 和 **报告格式映射** 字段中配置外贸参数，并设置对 ER 格式的引用。

[![安全配置页面。](./media/ER-ExtLookup-SecuritySetting.png)](./media/ER-ExtLookup-SecuritySetting.png)

## <a name="limitations"></a>限制

当前仅支持在 ER 格式查找中访问 GR，以选择用于生成出站文档的 ER 格式。

## <a name="frequently-asked-questions"></a>常见问题

### <a name="why-cant-i-access-the-global-repository-from-the-er-format-lookup"></a>为什么不能从 ER 格式查找中访问全局知识库？

如果在 **功能管理** 页上启用了 **允许查询全局知识库的 ER 格式配置的扩展查找** 功能，但是用户无法在 **从全局知识库导入** 快速选项卡中看到 ER 格式，并且 **同步** 选项可见但已禁用，那么请确保已向用户授予 **维护配置库** (**ERMaintainSolutionRepositories**) 权限。 与系统管理员联系以获取此权限。

## <a name="additional-resources"></a>其他资源

- [电子报告 (ER) 概览](general-electronic-reporting.md)
- [电子报告 (ER) 框架 API](er-apis-app73.md)
- [管理电子报告 (ER) 配置生命周期](general-electronic-reporting-manage-configuration-lifecycle.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

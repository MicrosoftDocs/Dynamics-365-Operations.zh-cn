---
title: 即使未进行任何更改，系统仍会提示您保存物料覆盖范围设置
description: 即使未进行任何更改，系统仍会提示您保存物料覆盖范围设置。
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace_
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 29ee23164430f219ff3d0c94216a8be43f480ce309f6cdac3dac6ed5b6d030af
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730074"
---
# <a name="youre-prompted-to-save-item-coverage-settings-even-though-you-made-no-changes"></a>即使未进行任何更改，系统仍会提示您保存物料覆盖范围设置

知识库编号：4615588

## <a name="symptoms"></a>故障特征

在某些情况下，您在通过 *物料覆盖范围 V2* 实体导入物料后，打开 **物料覆盖范围** 页时可能会收到以下消息：

> 是否要在关闭之前保存更改?

即使您没有进行任何更改，您仍然会收到此消息。

## <a name="resolution"></a>解决方法

**物料覆盖范围** 页包含复杂的默认逻辑，可能会导致在最近对数据库进行直接更改（如通过实体导入）后显示消息。 例如，`AREGENERALSETTINGSOVERRIDDEN` 实体字段设置为 *否*，但您导入的文件为 `PRODUCTCOVERAGEGROUPID` 和/或 `VENDORACCOUNTNUMBER` 等字段提供了新值或修改后的值。 在这种情况下，由于 `AREGENERALSETTINGSOVERRIDDEN` 字段设置为 *否*，导入后第一次打开 **物料覆盖范围** 页时，这些值会自动从字段中清除。 如果将更改保存为消息框提示，它们将存储在数据库中。 否则，您下次打开页面时将收到相同的消息。

要防止出现这种行为，同时还要通过实体导入包含诸如 `PRODUCTCOVERAGEGROUPID` 等字段的值，请在导入时将 `AREGENERALSETTINGSOVERRIDDEN` 设置为 *是*。

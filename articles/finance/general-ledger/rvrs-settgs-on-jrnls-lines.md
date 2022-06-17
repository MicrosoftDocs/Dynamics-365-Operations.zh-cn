---
title: 日记帐和行中的冲销设置
description: 本文将说明为什么在普通日记帐中输入的冲销条目可能不会包括在已过帐交易记录中的原因。
author: kweekley
ms.date: 04/29/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e36a3ea1736e4d7f60a5a6ce588ad3e66c950c14
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899833"
---
# <a name="reverse-settings-on-journals-and-lines"></a>日记帐和行中的冲销设置

[!include [banner](../includes/banner.md)]

本文将说明为什么在普通日记帐中输入的冲销条目可能不会包括在已过帐交易记录中的原因。  

## <a name="symptom"></a>问题

普通日记帐包括日记帐中的冲销条目和冲销日期。 过帐日记帐时，未冲销任何凭证。 为什么会发生这种情况？

## <a name="resolution"></a>解决方法

过帐日记帐时，冲销流程仅关注凭证的 **行** 部分中的 **冲销条目** 和 **冲销日期** 设置。 此方法可以使日记帐包括标记为冲销的某些凭证，以及一些其他类型的凭证。

添加 *新* 行时，日记帐中的值仅用作默认值。 更改日记帐中的值不会影响现有的行。 在此示例中，首先输入了凭证行。 如果您在将日记帐指定为冲销之前输入行详细信息，所进行的冲销条目和冲销日期指定不会应用于任何现有行。

更改现有行中的冲销条目或冲销日期会将该更改传播到同一凭证中的其他行。 为了优化性能，在将更改传播到其他行之后不会刷新网格。 您可以通过刷新网格来显示更新的值。



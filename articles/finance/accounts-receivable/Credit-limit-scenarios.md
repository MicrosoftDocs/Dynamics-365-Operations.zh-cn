---
title: 信用额度方案
description: 本文介绍了当客户属于客户信用额度组时如何检查客户信用额度。
author: JodiChristiansen
ms.date: 06/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-06-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 60b17a6b7f57b468610974ae9bd05b7db3584cc1
ms.sourcegitcommit: 85141b21ac90f3db1b378c21f9c7f3d8f74e182f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/09/2022
ms.locfileid: "9130249"
---
# <a name="credit-limit-scenarios"></a>信用额度方案

在信用管理中，可以将信用额度分配给客户级别的客户。 每个客户都可以分配给 *客户信用额度组*，并且每个组都有信用额度。 因此，还可以将信用额度分配给组级别的客户。 分配给同一客户信用组的所有客户都具有相同的信用额度。

一般情况下，会在检查单个信用额度之前检查组信用额度。 单个信用额度并不总是会替代组信用额度。

本文介绍了与客户信用组和个人信用额度相关的五种方案。

## <a name="the-customer-group-credit-limit-is-more-than-the-individual-credit-limit"></a>客户组信用额度大于个人信用额度

例如，客户的个人信用额度为 $10,000。 客户已分配给客户信用组，并且该组的信用额度为 $15,000。 在这种情况下，客户的“有效信用额度”为 $10,000，因为该金额小于组额度。 锁定规则会首先检查组额度。 然后，它们会检查个人额度。 将阻止超过 $10,000 的任何销售订单。

## <a name="the-individual-credit-limit-is-more-than-the-customer-group-credit-limit"></a>个人信用额度大于客户组信用额度

例如，客户的个人信用额度为 $20,000。 客户已分配给客户信用组，并且该组的信用额度为 $15,000。 在这种情况下，客户的有效信用额度为 $15,000，因为阻止规则总是首先检查组额度。 将阻止超过 $15,000 的任何销售订单。

## <a name="the-individual-credit-limit-is-set-to-000-and-mandatory-credit-limit-is-set-to-yes"></a>个人信用额度设置为 0.00，强制信用额度设置为“是”

如果客户的个人信用额度设置为 **0.00**，并且 **强制信用额度** 选项设置为 **是**，则客户的有效信用额度将为 $0.00，即使客户已分配给客户信用组也不例外。 这样，客户可以属于组，但所有订单都将转到信用管理。

## <a name="the-individual-credit-limit-is-set-to-000-and-unlimited-credit-limit-is-set-to-yes"></a>个人信用额度设置为 0.00，无限信用额度设置为“是”

如果客户的个人信用额度设置为 **0.00**，但 **无限信用额度** 选项设置为 **是**，则客户将具有无限信用额度，即使客户已分配给客户信用组也不例外。

## <a name="the-individual-credit-limit-is-set-to-000-and-the-customer-is-part-of-a-customer-credit-group"></a>个人信用额度设置为 0.00，客户属于客户信用组

例如，客户的个人信用额度设置为 **0.00**，**无限额度** 选项设置为 **否**，并且 **强制信用额度** 选项设置为 **否**。 客户已分配给客户信用组，并且该组的信用额度为 $15,000。 在这种情况下，客户的有效信用额度是组的额度，即 $15,000。 因此，将阻止超过该金额的任何销售订单。 此行为使信用额度可以在客户信用组级别而不是个人客户级别进行管理。 分配给同一组的所有客户都具有相同的信用额度。

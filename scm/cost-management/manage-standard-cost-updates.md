---
title: "管理标准成本更新"
description: "可以使用两种不同的方法管理对标准成本数据的更新 - 单版本方法和双版本方法。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CostingVersion
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 69992
ms.assetid: 468de7af-c7b5-4345-bd5a-ba3aa5a900cc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 7e0f0817ff37c82ed98a51f10bcdde7e785a19a3
ms.lasthandoff: 03/31/2017


---

# <a name="manage-standard-cost-updates"></a>管理标准成本更新

[!include[banner](../includes/banner.md)]


可以使用两种不同的方法管理对标准成本数据的更新 - 单版本方法和双版本方法。 

单版本方法使用包含所有成本记录的单个成本计算版本。 这些记录包括原始成本和所有成本更新。
双版本方法使用包含原始成本记录的一个版本，以及包含所有成本更新记录的第二个版本。 双版本方法的主要优点是清晰地描述以及跟踪单独的成本计算版本中的成本更新，同时不影响原始成本计算版本。 双版本方法来标识倍数增量更新，一次增量更新具有单独的成本计算版本来包含增量成本记录。 **示例**以下示例阐释了如何将单版本方法和双版本方法用于更新制造环境中的标准成本。 例如，反应新物料或错误更正的更新。 假定单个成本计算版本表示了当年的标准成本。 此版本的标识符是 2016-STD。 版本 2016-STD 包含了所有物料的当前有效成本。 此外，它包含在 2016 年初已知的所有工艺路线相关的成本类别和开销计算公式。 2016-STD 是原始成本计算版本。
-   **“用于成本数据更新的单版本方法”** − 在单版本方法中，原始成本计算版本 2016-STD 包含了所有成本记录。 成本更新将在 2016-STD 中记录并设置为“未决”状态。 未决成本可以为新采购的物料手动输入，也可以制造物料计算以反映更正。当您使用一个版本方法时，物料清单计算不要求回退数据源，因为所有有效成本均包含在成本计算版本中。 在未决成本变得有效后，原始成本计算版本 2016-STD 将再次包含所有当前有效成本。
-   **“用于成本数据更新的双版本方法”** − 双版本方法需要一个只包含成本更新的附加成本计算版本。 此版本的标识符是 2016-STD-CHANGES。 成本更新将在 2016-STD-CHANGES 中记录并设置为“未决”状态。使用双版本方法，制造物料的未决成本的物料清单计算要求回退数据源。 这是因为附加的成本计算版本 2016-STD-CHANGES 只包含了成本数据的子集。 该回退可以表示为有效成本或成本计算版本 2016-STD，因为当它未包括在 2016-STD-CHANGES 中时，有效成本和成本计算版本 2016-STD 都标识了成本数据的来源。 在未决成本生效后，成本计算版本 2016-STD-CHANGES 将包含反映更新的当前有效成本，而原始成本计算版本 2016-STD 将不改变。当使用双版本方法时，应该针对原始成本计算版本设置锁定策略以阻止更新。 应该为附加成本计算版本设置相同的锁定策略，除了锁定策略的开始数据和选择性使用，以允许更新。 指定的开始日期应该用每个更改批处理进行更新，以便反映计划的激活日期。

此示例使用了一个附加成本计算版本来管理整个 2016 年的更新。 可以使用更多的成本计算版本，例如使用单独的版本来用于各个更新批处理。 当使用了多个附加成本计算时，必须用有效成本表示回调，因为有效成本分散在多个成本计算版本中。






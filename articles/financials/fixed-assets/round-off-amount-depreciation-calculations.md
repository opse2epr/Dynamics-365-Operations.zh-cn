---
title: "计算化整折旧金额"
description: "本文讨论在“帐簿设置”页找到的“化整折旧”字段。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 8d5a9d9267c14ee045388c3b3b42b26f2fff45ea
ms.contentlocale: zh-cn
ms.lasthandoff: 05/25/2017

---

# <a name="round-off-amount-for-depreciation-calculations"></a>计算化整折旧金额

[!include[banner](../includes/banner.md)]


本文讨论在“帐簿设置”页找到的“化整折旧”字段。

将为每个帐簿设置化差折扣金额。 化整折旧金额用于固定资产折旧图（显示固定资产的未来折旧和价值），也用于折旧方案。 输入此帐簿允许的最低折旧金额。 

不管使用的是什么化整设置，系统都不会化整最近折旧期间的折旧金额。 在最近折旧期间结束时，如果使用残值，则固定资产的值必须为 0（零）或残值。

### <a name="example"></a>示例

没有化整的折旧计算为 2,444.44。 如下表中所示，根据设置的化整方式，建议的金额将不同。

| 舍入方法 | 折旧金额 |
|-----------------|---------------------|
| 化整 0.1    | 2,444.40            |
| 化整 1.00   | 2,444.00            |
| 化整 10.00  | 2,440.00            |
| 化整 100.00 | 2,400.00            |






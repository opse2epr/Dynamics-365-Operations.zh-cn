---
title: "剩余年限法折旧"
description: "本文提供了直线法（剩余年限）折旧方法的概览。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13851
ms.assetid: 0fa2f71a-596c-414c-a6e6-8f7405a0bf81
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 765825ba43cad44b076ea6628d2787011e97fc57
ms.contentlocale: zh-cn
ms.lasthandoff: 05/25/2017

---

# <a name="straight-line-life-remaining-depreciation"></a>剩余年限法折旧

[!include[banner](../includes/banner.md)]


本文提供了直线法（剩余年限）折旧方法的概览。

在设置固定资产折旧模板并在**折旧模板**页的**方法**字段中选择**直线法（剩余年限）**时，分配给该折旧模板的固定资产折旧将基于资产的剩余使用年限。 通常，每个折旧期间的折旧金额相同。 若要设置直线法（剩余年限）折旧，您还必须在**折旧模板**页面上的**折旧年份**字段和**期间频率**字段中选择选项。 **“期间频率”**字段中提供的选项因**“折旧年份”**字段中所选的值而异。

## <a name="select-a-depreciation-year"></a>选择折旧年份
您可以在**“折旧模板”**页上的**“折旧年份”**字段中选择**“日历”**或**“会计”**。 默认值是**“日历”**。 您的选择将决定“**期间频率**”字段中可用的选项。 此字段定义整个日历年度的折旧应计过帐日期和金额。

### <a name="calendar"></a>日历

如果在***折旧年份***字段中选择**日历**，即使对会计日历作了不同定义，仍然假设一年的起止时间为 1 月 1 日到 12 月 31 日。 **“日历”**选项在每年的 1 月 1 日更新折旧基数。 通常，折旧基数是帐面净值减去残值。 在此主题后面的示例中，折旧基数是计算列中第一个表达式的分子。 如果选择**“日历”**作为折旧年份，则**“期间频率”**字段中提供以下选项：

-   **“每年”**在 12 月 31 日过帐金额。
-   **“每月”**在每个日历月末过帐每月金额。
-   **“每季度”**在每个日历季度末（3 月 31 日、6 月 30 日、9 月 30 日和 12 月 31 日）过帐季度金额。
-   **每半年**在每个日历半年末（6 月 30 日和 12 月 31 日）过帐半年金额。
-   **“每日”**通过对每天使用一个交易记录来过帐每日折旧方法的折旧金额。

例如，如果您选择**每年**，年折旧只过帐一次，在每年的 12 月 31 日。 如果您选择**每月**，月折旧每月按年折旧金额的 1/12 过帐。

### <a name="fiscal"></a>会计

如果在**折旧年份**字段中选择**会计**，则使用直线剩余年限折旧法。 折旧基于会计年度剩余计算。 例如，对于会计年度 2015 年 7 月 1 日至 2016 年 6 月 30 日，折旧计算从 7 月 1 日开始。 会计年度可以长于或短于 12 个月。 对于每个会计期间，都可以调整折旧。 下一会计年度的长度由**会计日历**页面上设置的会计期间决定。 如果选择**“会计”**作为折旧年份，则**“期间频率”**字段中提供以下选项：

-   **“每年”**为会计年度计算的折旧总额作为一笔金额在该会计年度的最后一天进行过帐。
-   **会计期间**将计算该会计年度的折旧总额。 此金额然后计入在为帐簿指定的会计日历的“**会计日历**页”上定义的会计期间。

## <a name="example-of-straight-line-depreciation-of-an-unchanged-fixed-asset"></a>对未更改的固定资产进行直线法折旧的示例
固定资产具有以下特征。

|                     |        |
|---------------------|--------|
| 购置成本    | 11,000 |
| Salvage value / 残值       | 1,000  |
| 折旧基数   | 10,000 |
| 使用年限(年)  | 5      |
| 每年折旧 | 2,000  |

每年的折旧金额相同：（购置成本 – 残值）÷使用年限

| 期间 | 年折旧金额的计算 | 年末帐面净值 |
|--------|-----------------------------------------------|---------------------------------------|
| 第 1 年 | (11,000 – 1,000) ÷ 5 = 2,000                  | 9,000                                 |
| 第 2 年 | (9,000 – 1,000) ÷ 4 = 2,000                   | 7,000                                 |
| 第 3 年 | (7,000 – 1,000) ÷ 3 = 2,000                   | 5,000                                 |
| 第 4 年 | (5,000 – 1,000) ÷ 2 = 2,000                   | 3,000                                 |
| 第 5 年 | (3,000 – 1,000) ÷ 1 = 2,000                   | 1,000                                 |






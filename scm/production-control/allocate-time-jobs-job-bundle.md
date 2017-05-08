---
title: "分配时间到作业捆绑中的作业"
description: "在“制造执行”中，您可以捆绑作业。 然后您可以在工作列表页同时开始多个作业。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: JmgBundleSlize, JmgProdParameters, JmgRegistration
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 55591
ms.assetid: 358efce7-73c8-4d2a-a7f7-cb99b88ab6ee
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 26f6d0868ac195d21becec35898e2ac1bcb41e0f
ms.lasthandoff: 03/31/2017


---

# <a name="allocate-time-to-jobs-in-a-job-bundle"></a>分配时间到作业捆绑中的作业

[!include[banner](../includes/banner.md)]


在“制造执行”中，您可以捆绑作业。 然后您可以在工作列表页同时开始多个作业。

如果您捆绑作业，则必须定义应如何将所有作业的总登记时间分配给每个作业。 您通过在**分配参数**页的**捆绑类型**字段中选择以下选项之一定义分配：

-   **估计** – 基于作业的估计时间，将时间划分到各作业上。
-   **作业** – 根据捆绑的作业总数以及完成所有作业所用的时间，对时间进行划分。
-   **净时间** – 时间随时均匀划分到捆绑作业中的各作业之间。
-   **实时** – 分配实际作业时间。 可以基于实际工资成本计算成本。 **注意：**只有当您的公司在“考勤管理”中使用工资单功能时**实时**分配参数才可用。

下面的示例显示了各个分配参数的结果。

## <a name="example-scenario"></a>示例场景
必须完成您的作业队列中的三个作业。 您开始第一个作业并正在进行作业时，您开始第二个和第三个作业。 因此，具有三个作业的捆绑。 下表显示每个作业的估计生产时间。

| 职位   | 生产时间 |
|-------|-----------------|
| 作业 1 | 1 小时          |
| 作业 2 | 3 小时         |
| 作业 3 | 4 小时         |
| 合计 | 8 小时         |

下表显示在每个作业上所用的实际工时。

| 职位    | 开始时间 | 结束时间 | 捆绑作业时间 |
|--------|------------|----------|-------------|
| 作业 1  | 09:00      | 11:00    | 2 小时     |
| 作业 2  | 10:00      | 13:00    | 3 小时     |
| 作业 3  | 10:00      | 15:00    | 5 小时     |
| 捆绑作业 | 09:00      | 15:00    | 6 小时     |

以下各节描述每个分配参数的计算时间的结果。

## <a name="estimation-allocation-key"></a>估计分配参数
下表阐释用于计算分配的时间的公式。 公式为：每个作业的时间 = 总捆绑作业时间 × (估计的作业时间 ÷ 总估计时间)

| 作业   | 配方           | 分配的时间 |
|-------|-------------------|----------------|
| 作业 1 | 6 × (1 ÷ 8) 小时 | 0.75 小时      |
| 作业 2 | 6 × (3 ÷ 8) 小时 | 2.25 小时     |
| 作业 3 | 6 × (4 ÷ 8) 小时 | 3.00 小时     |

## <a name="jobs-allocation-key"></a>作业分配参数
下表阐释用于计算分配的时间的公式。 这是公式：每个作业的时间 = 总捆绑时间 ÷ 作业数

| 作业   | 配方 | 分配的时间 |
|-------|---------|----------------|
| 作业 1 | 6 ÷ 3   | 2 小时        |
| 作业 2 | 6 ÷ 3   | 2 小时        |
| 作业 3 | 6 ÷ 3   | 2 小时        |

## <a name="net-time-allocation-key"></a>净时间分配参数
下表阐释用于计算分配的时间的公式。 这是公式：每个报告的计算时间 = 捆绑时间 ÷ 作业数

|                              | 09:00–10:00（1 小时） | 10:00–11:00（1 小时） | 11:00–13:00（2 小时） | 13:00–15:00（2 小时） | 分配的时间 |
|------------------------------|----------------------|----------------------|-----------------------|-----------------------|----------------|
| 捆绑中的作业的编号。 | 1                    | 3                    | 2                     | 1                     | 不适用 |
| 作业 1                        | 1 ÷ 1 = 1 小时       | 1 ÷ 3 = 0.33 小时    | 不适用        | 不适用        | 1.33 小时     |
| 作业 2                        | 不适用       | 1 ÷ 3 = 0.33 小时    | 2 ÷ 2 = 1 小时        | 不适用        | 1.33 小时     |
| 作业 3                        | 不适用       | 1 ÷ 3 = 0.33 小时    | 2 ÷ 2 = 1 小时        | 2 ÷ 1 = 2 小时       | 3.33 小时     |

## <a name="real-time-allocation-key"></a>实时分配参数
如果您希望生产成本基于实际成本计算，必须清除**生产订单默认值**页上的**成本类别**选项。 下表阐释用于计算分配的时间的公式。 这是公式：每个作业的实际时间 = 捆绑作业中的实际时间

| 作业   | 实际时间 |
|-------|-------------|
| 作业 1 | 2 小时     |
| 作业 2 | 3 小时     |
| 作业 3 | 5 小时     |

考虑由每小时 USD 12.00 工资的工作人员执行的三个作业。 对于用在作业的时间，员工没有加班奖金或津贴。 该工作人员在这三个捆绑作业上所用的总工作时间是 6 小时。 因此，工资成本为 6 × USD 12.00 = USD 72.00。 在使用实时分配时，使用来自净时间公式的系数重新计算每小时成本。 然后与更正后的每小时成本价一同转移每个作业所用的实际时间。 在该示例中，用了 6 小时，尽管分配了 10 小时。 下表阐释用于计算成本的公式。 这是公式：每小时成本 = (每个作业的总捆绑作业时间 (净时间) ÷ 每个作业的实际时间) × 每小时标准成本价

| 作业   | 更正后的每小时成本的计算 | 更正后的每小时成本 | 分配的时间 | 作业的总成本 |
|-------|----------------------------------------|-------------------------|----------------|-------------------|
| 作业 1 | (1.33 ÷ 2) × USD 12.00                 | 8.00 美元                | 2 小时        | 16.00 美元         |
| 作业 2 | (1.33 ÷ 3) × USD 12.00                 | 5.33 美元                | 3 小时        | 16.00 美元         |
| 作业 3 | (3.33 ÷ 5) × USD 12.00                 | 8.00 美元                | 5 小时        | 40.00 美元         |

更正后的每小时成本和作业时间都在生产日志中过帐。 **注意：**如果您在**生产订单默认值**页的**常规**选项卡上选择**成本类别**选项，每个作业的实际时间转移到生产日记帐，在其中成本应用于特定作业的成本类别。




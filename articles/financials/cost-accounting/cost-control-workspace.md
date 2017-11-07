---
title: "成本控制工作区"
description: "此主题提供了有关成本控制工作区的信息。 此工作区是负责控制一个维度内或跨维度的一个成本对象或一组成本对象的经理可以访问报表的一个中心点。"
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostControlWorkspaceConfiguration, CAMCostControlWorkspace
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations, Core
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: YuyuScheller
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 07787b67a84e8229cb3ce0a4434a39af3bd5a4e0
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="cost-control-overview"></a>成本控制概览 

[!include[banner](../includes/banner.md)]

**成本控制**工作区是负责控制一个维度内或跨维度（例如，成本中心和产品组）的一个成本对象或一组成本对象的经理可以访问报表的一个中心点。 此工作区中的报表由成本会计员完全管理，因此版式和用于报表的数据可以在整个组织中保持一致。

## <a name="cost-control-workspace-configuration"></a>成本控制工作区配置

成本会计员可以定义预期数据构成或版式所需要的数量的报表配置。 报表配置包括六个部分，每个部分可用于选择目标数据构成或版式。

要配置成本控制工作区，请单击**成本核算** \> **设置**\> **成本控制工作区配置**。

### <a name="general"></a>常规

在**常规**快速选项卡上可以创建一个唯一的报表版式。 报表的名称将是一个用户可在**成本控制**工作区中进行识别的唯一标识符。 您还可以指定报表是否应共享或在成本会计员内部使用。

| 字段       | 说明 |
|-------------|-------------|
| 姓名        | 输入版式的唯一名称。 |
| 说明 | 输入详细描述。 |
| 已发布   | 如果您将此字段设置为**是**，获得以下角色之一的用户可以在**成本控制**工作区中看到报表。<ul><li>成本会计经理</li><li>成本核算师</li><li>成本核算师</li><li>成本对象控制器</li></ul>如果您将此字段设置为**否**，仅获得以下角色之一的用户可以在**成本控制**工作区中看到报表。<ul><li>成本会计经理</li><li>成本核算师</li><li>成本核算师</li></ul> |

### <a name="data-filtering"></a>数据筛选

在**数据筛选**快速选项卡中定义报表的数据基础。 在原数据得到处理后，此报表的用户将看到报表上的值。

| 字段                                                             | 说明 |
|-------------------------------------------------------------------|-------------|
| 成本核算分类帐                                            | 作为报表基础的**成本核算分类帐**。 值衍生自**成本控制单元**字段。 |
| 成本控制单元                                                 | 您选择的值确定将作为此报表基础的成本核算分类帐和成本对象。 |
| 统计维度层次结构，成本元素维度层次结构 | **成本控制**工作区配置记录可以报告非货币或货币值，但不能在同一版式中。 在**成本元素维度层次结构**字段中选择一个值以报告货币值。 在**统计元素维度层次结构**字段中选择一个值以报告非货币值。 您选择的维度层次结构记录确定报表和合并级别的结构。<blockquote>[!NOTE]<br>要并行查看非货币和货币值，您可以为 Microsoft Power BI 内容包将数据导出到 Microsoft Excel。</blockquote> |
| 成本对象维度层次结构                                   | 选择适合您正在定义的报表的目的的成本对象维度的维度层次结构。 |
| 预算原始版本                                           | 选择作为此报表上下文中的原始预算的预算版本 ID。 |
| 预算已修订版本                                            | 选择作为此报表上下文中的修订预算的预算版本 ID。 |

### <a name="assign-calculation-records"></a>分配计算记录

开销计算对原数据执行多个计算步骤，例如成本行为分配、成本分配和成本分摊。 可为同一个会计期间完成多个开销计算，以防发现缺失的源数据或必须更新规则。 每个开销计算使用一个唯一 ID 进行保存。 成本会计员可以选择特定的开销计算 ID。 报表的用户（如经理）将在**成本控制**工作区看到开销计算的结果。

| 字段                  | 说明 |
|------------------------|-------------|
| 会计日历期间 | 选择要分配开销计算 ID 的会计日历期间。<blockquote>[!NOTE]<br>在此字段中列出的会计期间来自与成本核算分类帐关联的会计日历。</blockquote> |
| 实际版本         | 选择相应的开销计算 ID。 |
| 预算版本         | 选择相应的开销计算 ID。 |
| 修订的预算版本 | 选择相应的开销计算 ID。 |

### <a name="fiscal-periods-per-column"></a>每列的会计期间

在**每列的会计期间**快速选项卡上，成本会计员确定应在报表版式中显示的会计期间。

选定列中的值将乘以**每列的会计期间**快速选项卡上的选定值。

| 字段                | 说明 |
|----------------------|-------------|
| 当前期间       | 显示当前会计期间的余额。<blockquote>[!NOTE]<br>默认情况下，当前期间由会话日期确定。 在**成本控制**工作区中，可以选择特定的会计期间。 然后，选定值表示当前期间。</blockquote> |
| 上一期      | 显示上一个会计期间的余额。 使用以下公式：<br>当前会计期间 - 1<blockquote>[!NOTE]<br>默认情况下，上一个期间衍生自会话日期。 在**成本控制**工作区中，可以选择特定的会计期间作为当前期间。 之后将重新计算相应的**上一个期间**。</blockquote> |
| 本年迄今         | 显示本年迄今。 使用以下公式：<br>YearToDate（当前会计期间）<blockquote>[!NOTE]<br>默认情况下，当前期间由会话日期确定。 在**成本控制**工作区中，可以选择特定的会计期间。 然后，选定值表示当前期间，并将更新相应的**本年迄今**值。</blockquote> |
| 本年迄今平均 | 显示本年迄今平均。 使用以下公式：<br>（YearToDate [当前会计期间]）÷（计数 [当前会计期间]）<p><strong>示例</strong></p><ul><li>**统计维度成员：**全职员工</li><li>**当前日期：**3-21-2017</li><li>**期间：**会计期间 1，会计期间 2，会计期间 3</li><li>**度量值：**10，10，12</li></ul>在这种情况下，**本年迄今平均** = (10 + 10 + 12) ÷ 3 = 10.67<p>可以计算成本元素维度成员和统计维度成员的**本年迄今平均**值。</p><blockquote>[!NOTE]<br>默认情况下，当前期间由会话日期确定。 在**成本控制**工作区中，可以选择特定的会计期间。 然后，选定值表示当前期间，并将更新相应的**本年迄今**和**本年迄今平均**值。</blockquote> |

### <a name="columns-to-display-for-costs"></a>为成本显示的列

在**为成本显示的列**快速选项卡上，成本会计员决定报表版式应包含哪些列。 有三个类别：固定成本、可变成本和未分类的成本。

| 字段                 | 说明 |
|-----------------------|-------------|
| 固定成本            | 此列类型显示基于选定开销计算 ID 的固定成本。<blockquote>[!NOTE]<br>仅当为会计期间选定开销计算 ID 时，此列类型才显示余额。</blockquote> |
| 可变成本         | 此列类型显示基于选定开销计算 ID 的可变成本。<blockquote>[!NOTE]<br>仅当为会计期间选定开销计算 ID 时，此列类型才显示余额。</blockquote> |
| 固定 + 可变成本 | 此列类型显示基于选定开销计算 ID 的固定成本和可变成本。<blockquote>[!NOTE]<br>仅当为会计期间选定开销计算 ID 时，此列类型才显示余额。</blockquote> |
| 总成本            | 此列类型显示总成本（未分类的成本、固定成本和可变成本）。<blockquote>[!NOTE]<br>此列类型将始终显示余额。</blockquote> |
| 未分类的成本     | 此列类型显示未分类的成本。<blockquote>[!NOTE]<br>此列可用于验证是否所有成本已按照开销计算正确分类，或是否必须调整成本行为规则。</blockquote> |

### <a name="columns-to-display-for-budgeted-costs"></a>为预算成本显示的列

在**为预算成本显示的列**快速选项卡上，成本会计员决定应为选定的预算版本显示哪些列。 可以为原始和修订预算单独进行选择。

> [!NOTE]
> 由于以下字段对原始预算和修订预算的行为相同，因此将仅解释一次。

| 字段                     | 说明 |
|---------------------------|-------------|
| 预算                    | 预算余额将按选定列显示。<blockquote>[!NOTE]<br>余额将以在**数据筛选**快速选项卡上选择的预算版本为基础。</blockquote> |
| 预算差异           | 计算和显示预算与实际之间的差异。 使用以下公式：<br>预算余额–实际余额 |
| 预算差异百分比      | 计算和显示预算与实际之间的差异百分比。 使用以下公式：<br>（预算余额–实际余额）÷ 预算余额 |
| 差异期间阈值 | 设置当前期间货币金额差异的阈值。 如果超过阈值，将以红色高亮显示**成本控制**工作区中的行。<blockquote>[!NOTE]<br>此字段仅适用于表示支出的成本元素。</blockquote> |
| 差异年度阈值   | 设置当年货币金额差异的阈值。 如果超过阈值，将以红色高亮显示**成本控制**工作区中的行。 |
| 差异阈值百分比      | 设置差异百分比的阈值。 如果超过阈值，将以红色高亮显示**成本控制**工作区中的行。<blockquote>[!NOTE]<br>相同百分比阈值适用于当前期间和年份。</blockquote> |

## <a name="cost-control-workspace"></a>成本控制工作区

**成本控制**工作区设计为 Web 报表。 因此，负责成本对象的所有经理可以被授予 [定义成本对象控制员的访问权限](access-rights-cost-object-controller.md) 中描述的访问权限。

对用户（如经理）可用的报表列表通过设置**成本控制工作区配置**页上的**已发布**选项进行控制。

![用户可以在成本控制工作区查看的报表](./media/report-cost-control.png)

经理可以选择要查看的会计日历期间。 会话日期用于确定默认的当前期间。

会计日历期间中的值由为与**成本控制工作区配置**页上的报表名称相关联的成本核算分类帐选择的报表名称和会计日历确定。

在成本对象维度层次结构中，用户可以选择显示余额的合并级别。 通过启用访问级别安全可以控制权限，因此用户仅可以选择已被授予访问权限的层次结构级别。 因此，他们仅可以看到已被授予访问权限的合并余额。

### <a name="add-or-remove-columns"></a>添加或删除列

用户可以自定义报表上的列以适合自己的需求。

### <a name="view-details"></a>查看明细

用户可以深入到工作区中显示的余额背后的详细信息。 如果用户选择成本元素维度层次结构节点，然后单击**查看明细**，**成本元素明细**对话框将显示节点的详细信息。

网格显示与成本元素维度层次结构节点相关联的每个成本元素及其值。 显示在网格中的列与工作区设置匹配。

两个图表按期间显示实际与预算对比及预算差异的汇总。

![按期间显示实际与预算对比及预算差异的汇总的图表](./media/cost-element-details-operations.png)

用户可以单击**成本条目**以根据需要深化到条目详细信息。

![成本条目](./media/cost-entries.png)

例如，租金是分配到成本中心的支出。 用户若要了解其成本中心必须承担的租金成本，必须深化以查看租金的计算方式。

如果用户单击**成本条目**页上的**分配基础**，将显示一个对话框。 之后，用户可以将分配基础分配到规则并查看为该期间登记的相应的统计度量。

在以下示例中，分配基础为**公式分配基础**类型，且显示公式。 列出了定义公式的系数。 此外，网格还显示每个成本对象完成的计算。

![每个成本对象的计算](./media/cost-entries-allocation-base.png)

请参阅 

[定义成本对象控制员的访问权限](access-rights-cost-object-controller.md)



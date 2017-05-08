---
title: "修改行定义单元格"
description: "本文介绍财务报表中行定义的每个单元格必需的信息，并解释如何输入该信息。"
author: RobinARH
manager: AnnBe
ms.date: 2016-03-07 16 - 09 - 06
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: Management Reporter, Core
ms.custom: 58881
ms.assetid: 0af492df-a84e-450c-8045-78ef1211abaf
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 
ms.dyn365.ops.version: 
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: b61364c9055e5c5a63592c7f05551d0c145924b9
ms.lasthandoff: 03/29/2017


---

# <a name="modify-row-definition-cells"></a>修改行定义单元格

本文介绍财务报表中行定义的每个单元格必需的信息，并解释如何输入该信息。 

# <a name="specify-a-row-code-in-a-row-definition"></a>在行定义中指定行代码

在行定义中，**“行代码”**单元格中的编号或标签标识行定义中的每一行。 您可以指定行代码以引用计算和汇总中的数据。

### <a name="row-code-requirements"></a>行代码要求

所有行都需要行代码。 您可以在行定义中组合数字、字母数字和未设置（空）行代码。 行代码可以是任何正整数（100,000,000 以下）或标识行的描述性标签。 描述性标签必须遵循下列规则：

-   此标签必须以按字母顺序的字符（a 到 z 或 A 到 Z）开头，并且可能是长达 16 个字符的数字和字母组合。 **注意：**标签可以包含下划线字符 (\_)，但不允许使用任何其他特殊字符。
-   此标签不能使用下列任一保留字：AND、OR、IF、THEN、ELSE、PERIODS、TO、BASEROW、UNIT、NULL、CPO 或 RPO。

下列示例是有效的行代码：

-   320
-   TL\_NET\_INCOME
-   TL\_NET\_94

### <a name="change-a-row-code-in-a-row-definition"></a>在行定义中更改行代码

1.  在报表设计器中，单击**“行定义”**，然后打开行定义以修改。
2.  在相应行中，在**“行代码”**列的单元格中输入新值。

### <a name="reset-numeric-row-codes"></a>重置数字行代码

1.  在报表设计器中，单击**“行定义”**，然后打开行定义以修改。
2.  在**“编辑”**菜单上，单击**“对行重新编号”**。
3.  在**“对行重新编号”**对话框中，为起始行代码和行代码增量指定新值。 您可以将数字行代码重置为均等间距值。 但是，报表设计器仅对以数字（例如，130 或 246）开头的行代码重新编号。 它不对对以字母（例如，INCOME\_93 或 TP0693）开头的行代码重新编号。 **注意：**当您对行代码重新编号时，报表设计器将自动更新 **TOT** 和 **CAL** 引用。 例如，如果 **TOT** 行引用从行代码 100 开始的范围，并且您对从 90 开头的行重新编号，则起始 **TOT** 引用将从 100 更改为 90。

## <a name="add-a-description"></a>添加描述
描述单元格提供对报表行中财务数据的描述，如“收入”或“净收入”。 **“描述”**单元格中的文本将完全按照您在行定义中所输入的那样在报表中显示。 **请注意：**报表上描述列的宽度是在列定义中设置的。 如果行定义中**“描述”**列中的文本太长，请确认 **DESC** 列的宽度。 当您使用**“从以下位置插入行”**对话框时，**“描述”**列中的值是财务数据中的段值或维度值。 您可以插入行来添加描述性文本（如节标题或节汇总）以及添加格式（如一行位于汇总行之前）。 如果报表包含报告结构树，则可包含为报告结构树中的报告单位定义的其他文本。 您还可以将其他文本限制为特定报告单位。

### <a name="add-the-description-for-a-line-on-a-report"></a>为报表上的行添加描述

1.  在报表设计器中，单击**“行定义”**，然后打开行定义以修改。
2.  选择**“描述”**单元格，然后输入报表行的名称。
3.  应用格式设置。

### <a name="add-additional-text-from-a-reporting-tree-in-the-description"></a>在描述中添加报告结构树中的其他文本

1.  在报表设计器中，单击**“行定义”**，然后打开行定义以修改。
2.  在相应**“描述”**单元格中输入其他文本代码和任何其他文本。
3.  应用格式设置。

### <a name="limit-the-additional-text-to-a-specific-reporting-unit"></a>将其他文本限制为特定报告单位

1.  在报表设计器中，单击**“行定义”**，然后打开行定义以修改。
2.  查找其中应创建其他文本的行，然后双击**“相关公式/行/单位”**列中的单元格。
3.  在**“报告单位选择”**对话框的**“报告结构树”**字段中，选择报告结构树。
4.  在**“选择要限制的报告单位”**字段中，展开或折叠报告结构树，然后选择报告单位。

## <a name="add-a-format-code"></a>添加格式代码
**“格式代码”**单元格为行内容提供很多预设格式选择。 如果**“格式代码”**单元格为空，则行将解释为财务数据明细行。 **注意：**如果报表包含与已隐藏的金额行（例如，由于零余额）相关的非金额格式行，您可使用**“相关配方/行/单位”**列防止打印标题和格式行。

### <a name="add-a-format-code-to-a-report-row"></a>向报表行添加格式代码

1.  在报表设计器中，单击**“行定义”**，然后选择行定义以修改。
2.  双击**“格式代码”**单元格。
3.  在列表中选择格式代码。 下表描述了格式代码及其操作。
    | 格式代码                   | 格式代码的解释 | 行为|
    |---|---|---|
    | (无)                        |                                    | 清除**“格式代码”**单元格。                                                                                                                                                                               |
    | TOT                           | 总计                              | 标识在**“相关公式/行/单位”**列中使用数学运算符的行。 汇总包含简单运算符，如 **+** 或 **-**。                                                      |
    | CAL                           | 计算                        | 标识在**“相关公式/行/单位”**列中使用数学运算符的行。 计算包含复杂运算符，如 **+**、**-**、**\***、**/** 和 **IF/THEN/ELSE** 语句。 |
    | DES                           | 说明                        | 标识报表上的标题行或空行。                                                                                                                                                        |
    | LFT RGT CEN                   | 左 右 居中                  | 与报表页上的行描述文本对齐，不管文本在列定义中的位置。                                                                                               |
    | CBR                           | 更改基准行                    | 标识为列计算设置基准行的行。                                                                                                                                               |
    | COLUMN                        | 分列符                       | 在报表上开始新列。                                                                                                                                                                             |
    | PAGE                          | 分页                         | 在报表上开始新页。                                                                                                                                                                               |
    | ---                           | 单下划线                   | 在报表上所有金额列下放置单下划线。                                                                                                                                                     |
    | ===                           | 双下划线                   | 在报表上所有金额列下放置双下划线。                                                                                                                                                     |
    | LINE1                         | 细线                          | 在页面上绘制一条细线。                                                                                                                                                                      |
    | LINE2                         | 粗线                         | 在页面上绘制一条粗线。                                                                                                                                                                     |
    | LINE3                         | 虚线                        | 在页面上绘制一条虚线。                                                                                                                                                                    |
    | LINE4                         | 粗线和细线           | 在页面上绘制两条线。 顶部的线为粗线，底部的线为细线。                                                                                                                       |
    | LINE5                         | 细线和粗线           | 在页面上绘制两条线。 顶部的线为细线，底部的线为粗线。                                                                                                                       |
    | BXB BXC                       | 框式行                          | 围绕以 **BXB** 行开头和 **BXC** 行结尾的报表行绘制一个框。                                                                                                               |
    | REM                           | 注解                             | 标识为注释行且不应打印在报表上的行。 例如，注释行可能说明了您的格式设置方法。                                                            |
    | SORT ASORT SORTDESC ASORTDESC | 排序                               | 对支出或收入排序，按最大差异对实际或预算差异报表排序或按字母顺序对行描述排序。                                                                   |

## <a name="specify-related-formulasrowsunits"></a>指定相关公式/行/单位
**“相关配方/行/单位”**单元格具有多个用途。 根据行的类型，**“相关配方/行/单位”**可以执行下列功能之一：

-   在您使用 **TOT** 格式代码或 **CAL** 格式代码时，定义要包含在计算中的行。
-   将格式行链接到金额行，以便仅当打印相关金额时才打印格式。
-   将行限制到特定报告单位。
-   当您使用 **BASEROW** 格式代码时，为计算定义基准行。
-   定义要在使用任何排序格式代码时进行排序的行。

### <a name="use-a-row-total-in-a-row-definition"></a>在行定义中使用行汇总

使用行汇总公式加减其他行中的金额。 创建行汇总的公式可能包含 + 和 - 运算符以组合独立行代码和范围。 范围通过冒号 (:) 表示。 此公式最多可包含 1,024 个字符。 以下是标准汇总公式的示例：400+420+430+450+460LIABILITIES+EQUITY520:546520:546-LIABILITIES

### <a name="components-of-a-row-total-formula"></a>行汇总公式的分量

在您创建行汇总公式时，必须使用行代码指定要在当前行定义中进行加减的行，并且必须使用运算符指定行的组合方式。 任何组合中都可使用汇总行和金额行。 **请注意：**范围内的所有汇总行不包含在内。 要创建总计，您可指定行的范围。 如果范围的第一行是汇总行，则该行包含在新汇总中。 下表描述如何在行汇总公式中使用运算符。

| 操作员 | 公式示例 | 说明                                                 |
|----------|-----------------|-------------------------------------------------------------|
| +        | 100+330         | 将第 100 行中的金额与第 330 行中的金额相加。        |
| :        | 100:330         | 将位于第 100 行到第 330 行之间的所有行的汇总相加。    |
| -        | 100-330         | 将第 100 行中的金额与第 330 行中的金额相减。 |

### <a name="create-a-row-total"></a>创建行汇总

1.  在报表设计器中，单击**“行定义”**，然后打开行定义以修改。
2.  双击行定义中的**“格式代码”**单元格，然后选择 **TOT**。
3.  在**“相关公式/行/单位”**单元格中，输入汇总公式。

### <a name="relate-a-format-row-to-an-amount-row"></a>将格式行与金额行关联

在行定义中的**格式代码**列中，**DES**、**LFT**、**RGT**、**CEN**、**---** 和 **===** 格式代码对非金额行应用格式。 为了防止在隐藏相关金额行（例如，由于金额行包含零值或不包含期间活动）时打印此格式，您必须将格式行与对应的金额行关联。 如果您想要在期间无明细要打印时防止打印与小计相关的标题或格式，此功能很有用。 **注意：**您还可以通过清除“显示无金额的行”选项来防止打印明细金额行。 此选项位于报表定义的**“设置”**选项卡上。 默认情况下，报表中将隐藏具有零余额或无期间活动的交易记录明细科目。 要显示这些交易记录明细科目，请选中报表定义的**“设置”**选项卡上的**“显示无金额的行”**复选框。

### <a name="relate-a-format-row-to-an-amount-row"></a>将格式行与金额行关联

1.  在报表设计器中，单击**“行定义”**，然后选择行定义以修改。
2.  在格式行的**“相关配方/行/单位”**单元格中，键入要隐藏的金额行的行代码。 **请注意：**要隐藏金额行，行的余额必须为 0（零）。 不会隐藏有余额的金额行。
3.  在**“文件”**菜单上，单击**“另存为”**。

### <a name="example-of-preventing-printing-of-rows"></a>防止打印行的示例

在以下示例中，由于现金科目中无活动，Phyllis 想要防止打印报表**“现金总额”**行中的标题和下划线。 因此，在第 220 行（如 **---** 格式代码表示，此行是格式行）的**相关公式/行/单位**单元格中，她输入 **250**，该数是她想要隐藏的金额行的行代码。 [![RelatedRowsRowDefinition](./media/relatedrowsrowdefinition-1024x144.png)](./media/relatedrowsrowdefinition.png)

## <a name="select-the-base-row-for-a-column-calculation"></a>为列计算选择基准行
在关系报告中，通过使用 **CBR**（更改基准行）格式代码在行定义中分配一个或多个基准行。 之后，列定义中的计算将引用基准行。 以下是 CBR 计算的一些常见示例：

-   总收入的百分比，因为它与单个收入项相关
-   总支出的百分比，因为它与单个支出项相关
-   毛利的百分比，因为它与部门的明细相关。

一个或多个基准行是在行定义中定义的，然后列定义确定报告基准行的关系。 列公式中使用的代码为 **BASEROW**。 下列基本数学运算将与 **BASEROW** 一起使用：加、减、乘、除。 最常使用的运算将除以 **BASEROW**，其中结果将以百分比形式显示。 在公式中使用 **BASEROW** 的列计算将对相关基准行代码使用行定义。 **CBR** 行具有下列特征：

-   **CBR** 行不会打印在完成的报表上。
-   **CBR** 格式代码及其相关行代码的位置高于显示相关计算的行或部分。

在列定义中，**CALC** 列类型表示在**“公式”**行中指定公式的列。 此公式将在报表此列的数据上运算并且使用 Baserow 关键字在行中的 **CBR** 格式代码上进行基础计算。 在行定义中，**CBR** 格式代码定义列的基准行，这些列将计算报表中每一行的基准行的百分比或乘以报表中每一行的基准行。 您的行格式中具有多个 **CBR** 格式代码，如净销售额 1 个、总销售额 1 个以及总支出 1 个。 通常，**CBR** 格式代码用于创建与合计行进行比较的科目的百分比。 基准行用于所有计算，直至定义其他基准行。 您必须定义一个起始 **CBR** 格式代码和一个结束 **CBR **格式代码。 例如，要确定支出在净销售额中所占比例，您可以用每个支出行中的值除以净销售额行中的值。 在此情况下，净销售额行为基准行。 您可定义报告当前结果和本年迄今结果的列定义，以及每个结果的基础百分比，如下面的示例中所示。 从详细的利润表开始。

### <a name="select-the-base-row-in-a-row-definition-for-a-column-calculation"></a>为列计算选择行定义中的基准行

1.  在报表设计器中，单击**“列定义”**，然后打开利润表的列定义。
2.  向列定义添加新列，并将列类型设置为 **CALC**。
3.  在新列的**“公式”**单元格中，输入公式 **X/BASEROW**，其中 **X** 为要查看百分比形式的 **FD** 列类型。
4.  双击**“格式/货币覆盖”**单元格。
5.  在**“格式覆盖”**对话框的**“格式类别”**列表中，选择**“百分比”**，然后单击**“确定”**。
6.  在**“文件”**菜单上，单击**“另存为”**以用新名称保存列定义。 将 **CBR** 追加到当前文件名（例如，**CUR\_YTD\_CBR**）。 此列定义是您的基准行列定义。
7.  在报表设计器中，单击**“行定义”**，然后打开行定义以通过使用基准行计算进行修改。
8.  在基准行计算应开始的行之上插入一个新行。
9.  双击行定义的**“格式代码”**单元格，然后选择 **CBR**。
10. 在**“相关公式/行/单位”**单元格中，输入基准行的行代码编号。

### <a name="example-of-base-row-calculation"></a>基准行计算的示例

在以下行定义示例中，第 100 行显示计算的基准行为第 280 行。 [![基准行计算的示例。](./media/cbrrowdefinition.png)](./media/cbrrowdefinition.png) 在以下列定义示例中，计算使用 **CBR** 格式代码。 列 C 中的计算将用报表列 B 中的值除以列 B 的第 280 行中的值。列 B 中的格式覆盖会将计算结果打印为百分比形式。 同样，列 E 中的每个金额为列 D 中百分比形式的净销售额金额。 [![列定义示例。](./media/cbrcolumndefinition2.png)](./media/cbrcolumndefinition2.png) 以下示例显示可能基于以前的计算生成的报表。 [![基于上一示例计算的报表的示例。](./media/cbrreport-1024x272.png)](./media/cbrreport.png)

## <a name="select-a-sorting-code-for-a-row-definition"></a>为行定义选择分类代码
分类代码对科目或值排序，按最大差异对实际或预算差异报表排序或按字母顺序对行描述排序。 下列分类代码可用：

-   **SORT** – 根据指定列中的值以升序对报表进行排序。
-   **ASORT** – 根据指定列中值的绝对值以升序对报表进行排序。 换言之，对值进行排序时将忽略每个值的符号。 此格式代码按差异的度量值对值进行排序，不管差异为正还是负。
-   **SORTDESC** – 根据指定列中的值以降序对报表进行排序。
-   **ASORTDESC** – 根据指定列中值的绝对值以降序对报表进行排序。

### <a name="select-a-sorting-code"></a>选择分类代码

1.  在报表设计器中，单击**“行定义”**，然后打开行定义以修改。
2.  双击**“格式代码”**单元格，然后选择分类代码。
3.  在**“相关公式/行/单位”**单元格中，指定要排序的行代码的范围。 要指定范围，请输入第一个行代码、冒号 (:)，然后是最后一个行代码。 例如，输入 **160:490** 可指定第 160 行到第 490 行的范围。
4.  在**“列限制”**单元格中，输入要用于排序的报表列的字母。 **请注意：**仅在排序计算中包括金额行。

### <a name="examples-of-ascending-and-descending-column-values"></a>升序和降序列值的示例

在以下示例中，将按升序为报表中第 160 到 490 行的 D 列中的值排序。 此外，将按降序为报表中第 610 到 940 行的 G 列中的值排序。

| 行代码 | 描述                                         | 格式代码 | 相关公式/行/单位 | 标准余额 | 列限制 | 链接到财务维度 |
|----------|-----------------------------------------------------|-------------|-----------------------------|----------------|--------------------|------------------------------|
| 100      | 按月度差异排序（升序）       | DES         |                             |                |                    |                              |
| 130      |                                                     | SORT        | 160:490                     |                | 日                  |                              |
| 160      | 销售额                                               |             |                             | C              |                    | 4100                         |
| 190      | 销售退货                                       |             |                             |                |                    | 4110                         |
|          | ...                                                 |             |                             |                |                    |                              |
| 490      | 利息收入                                     |             |                             | C              |                    | 7000                         |
| 520      |                                                     | DES         |                             |                |                    |                              |
| 550      | 按 YTD 绝对差异排序（降序） | DES         |                             |                |                    |                              |
| 580      |                                                     | ASORTDESC   | 610:940                     |                | G                  |                              |
| 610      | 销售额                                               |             |                             | C              |                    | 4100                         |
| 640      | 销售退货                                       |             |                             |                |                    | 4110                         |
|          | ...                                                 |             |                             |                |                    |                              |
| 940      | 利息收入                                     |             |                             | C              |                    | 7000                         |

这是生成的报表的示例。

**差异分析（按差异排序）**

**北京和亚特兰大区域**

**针对 2013 年 7 月 31 日结束的 7 个月**

**七月**

**年初至今**

**实际**

**预算**

**差异**

**实际**

**预算**

**差异**

**按月度差异排序（升序）**

COGS

873,872

236,144

(637,728)

4,864,274

1,590,315

(3,273,959)

薪金和工资

97,624

65,573

(32,051)

653,884

441,664

(212,220)

销售折扣

36,383

24,152

(12,231)

241,562

162,670

(78,892)

销售退货

10,917

7,246

(3,671)

62,809

48,803

(14,006)

出租费用

12,052

9,019

(3,033)

80,444

60,748

(19,696)

办公费用

5,023

3,291

(1,732)

33,420

22,098

(11,322)

差旅费用

7,656

7,641

(15)

51,062

51,469

407

销售额

1,240,119

410,389

829,730

7,139,288

2,764,549

4,374,739

**按 YTD 绝对差异排序（降序）**

销售额

1,240,119

410,389

829,730

7,139,288

2,764,549

4,374,739

差旅费用

7,656

7,641

(15)

51,062

51,469

407

办公费用

5,023

3,291

(1,732)

33,420

22,098

(11,322)

销售退货

10,917

7,246

(3,671)

62,809

48,803

(14,006)

出租费用

12,052

9,019

(3,033)

80,444

60,748

(19,696)

销售折扣

36,383

24,152

(12,231)

241,562

162,670

(78,892)

薪金和工资

97,624

65,573

(32,051)

653,884

441,664

(212,220)

COGS

873,872

236,144

(637,728)

4,864,274

1,590,315

(3,273,959)

## <a name="specify-a-format-override-cell"></a>指定“格式覆盖”单元格
**“格式覆盖”**单元格指定打印报表时行使用的格式。 此格式将覆盖在列定义和报表定义中指定的格式。 默认情况下，在这些定义中指定的格式为货币。 如果报表的一行列出了资产数量（如建筑物数量），而另一行列出了这些资产的货币价值，则可覆盖货币格式并为指定建筑物数量的行输入数字格式。 在**“格式覆盖”**对话框中指定此信息。 可用选项取决于您选择的格式类别。 此对话框的**“示例”**区域将显示示例格式。 下列格式类别可用：

-   货币格式
-   数字格式
-   百分比格式
-   自定义格式

### <a name="override-cell-formatting"></a>覆盖单元格格式

1.  在报表设计器中，打开要修改的行定义。
2.  在要覆盖其格式的行中，双击**“格式覆盖”**列中的单元格。
3.  在**“格式覆盖”**对话框中，选择格式选项以用于报表中的此行。
4.  单击“**OK**”。

### <a name="currency-formatting"></a>货币格式

货币格式将应用于会计金额并且包含货币符号。 选项如下：

-   **货币符号** – 报表的货币符号。 此值将覆盖公司信息的**“区域选项”**设置。
-   **负数** – 负数可包含负号 (-)，它们可出现在圆括号中，也可包含三角形 (∆)。
-   **小数位数** – 要显示在小数点后的数字的数量。
-   **零值覆盖文本** – 当金额为 0（零）时要包含在报表中的文本。 此文本显示为**“示例”**区域中的最后一行。 **注意：**如果打印将隐藏零值或不包含期间活动，则将隐藏此文本。

### <a name="numeric-formatting"></a>数字格式

数字格式将应用于任何金额并且不包含货币符号。 选项如下：

-   **负数** – 负数可包含负号 (-)，它们可出现在圆括号中，也可包含三角形 (∆)。
-   **小数位数** – 要显示在小数点后的数字的数量。
-   **零值覆盖文本** – 当金额为 0（零）时要包含在报表中的文本。 此文本显示为**“示例”**区域中的最后一行。 **注意：**如果打印将隐藏零值或不包含期间活动，则将隐藏此文本。

### <a name="percentage-formatting"></a>百分比格式

百分比格式包含百分比符号 (%)。 选项如下：

-   **负数** – 负数可包含负号 (-)，它们可出现在圆括号中，也可包含三角形 (∆)。
-   **小数位数** – 要显示在小数点后的数字的数量。
-   **零值覆盖文本** – 当金额为 0（零）时要包含在报表中的文本。 此文本显示为**“示例”**区域中的最后一行。 **注意：**如果打印将隐藏零值或不包含期间活动，则将隐藏此文本。

### <a name="custom-formatting"></a>自定义格式

使用自定义格式类别创建自定义格式覆盖。 选项如下：

-   **类型** – 自定义格式。
-   **零值覆盖文本** – 当金额为 0（零）时要包含在报表中的文本。 此文本显示为**“示例”**区域中的最后一行。 **注意：**如果打印将隐藏零值或不包含期间活动，则将隐藏此文本。

类型应表示正值和负值。 通常，您输入区分正负值的类似格式。 例如，要同时指定具有两个小数位数的正负值，但负值出现在圆括号中，请输入 **0.00;(0.00)**。 下表显示您可用于控制您的值格式的自定义格式。 所有示例将从值 1234.56 开始。

| 格式                         | 正   | 负     | 零    |
|--------------------------------|------------|--------------|---------|
| 0                              | 1235       | -1235        | 0       |
| 0;0                            | 1235       | 1235         | 0       |
| 0;(0);-                        | 1235       | 1235         | -       |
| \#,\#\#\#;(\#,\#\#\#);“”       | 1,235      | (1,235)      | （空白） |
| \#,\#\#0.00;(\#,\#\#0.00);zero | 1,234.56   | (1,234.56)   | 零    |
| 0.00%;(0.00%)                  | 123456.00% | (123456.00%) | 0.00%   |

## <a name="specify-a-normal-balance-cell"></a>指定“标准余额”单元格
行定义中的**“标准余额”**单元格控制行中金额的符号。 要改变行的符号，或者如果科目的标准余额为信用，则在该行的**“标准余额”**单元格中输入 **C**。 报表设计器将改变该行中所有信用余额科目上的符号。 当报表设计器改变这些科目时，它将从所有科目中删除借方/贷方特征，从而直接进行汇总。 例如，要计算净收入，将从收入中减去支出。 通常，汇总行和计算行不受 **C** 代码影响。 但是，列定义中的 **XCR** 打印控制将改变任何在**“标准余额”**列中包含 **C** 的行的符号。 此格式在您想要将所有不利差异显示为负金额时尤其重要。 如果汇总或计算得出的数字具有错误的符号，则在相应行的**“标准余额”**单元格中输入 **C** 以改变符号。

## <a name="specify-a-row-modifier-cell"></a>指定“行修饰符”单元格
行定义中**“行修饰符”**单元格的内容将覆盖会计年度、期间和在相应行的列定义中指定的其他信息。 选定修饰符将应用于相应行中的每个金额。 您可通过使用一个或多个下列类型的修饰符来修改每一行：

-   科目修饰符
-   帐簿代码修饰符
-   科目和交易记录属性

### <a name="override-a-column-definition"></a>覆盖列定义

1.  在报表设计器中，打开要修改的行定义。
2.  在其中您要覆盖列定义的行中，双击**“行修饰符”**单元格。
3.  在**“行修饰符”**对话框中，选择**“科目修饰符”**中的选项。 有关选项的说明，请参阅“科目修饰符”部分。
4.  在**“帐簿代码修饰符”**字段中，选择相应行要使用的帐簿代码。
5.  在**“属性”**下，执行下列步骤以为应包含在行代码中的各个属性添加条目：
    1.  双击**“属性”**单元格，然后选择属性名称。 **注意：**将数字符号 (\#) 替换为数值。
    2.  双击**“从”**单元格，并输入该范围的第一个值。
    3.  双击**“到”**单元格，然后输入该范围的最后一个值。

6.  单击“**OK**”。

### <a name="account-modifiers"></a>科目修饰符

当您选择特定科目时，报表设计器通常会将科目和会计年度、期间以及您在列定义中指定的其他信息组合在一起。 您可以对特定行使用其他信息（如不同的会计期间）。 下表显示可用的科目修饰符。 将数字符号 (\#) 替换为等于或小于会计年度中的期间数量的值。

| 科目修饰符 | 打印内容                                                                           |
|------------------|-------------------------------------------------------------------------------------------|
| /BB              | 科目的期初余额。                                                     |
| /\#              | 指定期间的余额。                                                     |
| /-\#             | 当前期间之前的第 \# 个期间的余额。                  |
| /+\#             | 当前期间之后的第 \# 个期间的余额。                   |
| /C               | 当前期间的余额。                                                       |
| /C-\#            | 当前期间之前的第 \# 个期间的余额。                  |
| /C+\#            | 当前期间之后的第 \# 个期间的余额。                   |
| /Y               | 截至当前期间的本年迄今余额。                                      |
| /Y-\#            | 截至当前期间之前的第 \# 个期间的本年迄今余额。 |
| /Y+\#            | 截至当前期间之后的第 \# 个期间的本年迄今余额。  |

### <a name="book-code-modifiers"></a>帐簿代码修饰符

您可将行限制为现有帐簿代码。 列定义必须包括至少一个具有帐簿代码的 **FD** 列。 **注意：**行的帐簿代码限制将覆盖该行的列定义中的帐簿代码限制。

### <a name="account-and-transaction-attributes"></a>科目和交易记录属性

某些会计系统支持财务数据中的科目属性和交易记录属性。 这些属性的运行类似于虚拟科目段，并且可包含有关科目或交易记录的其他信息。 此其他信息可能是科目 ID、批次 ID、邮政编码或其他属性。 如果您的会计系统支持属性，您可使用科目属性或交易记录属性作为行定义中的行修饰符。 有关如何覆盖行信息的信息，请参阅本文前文中的“覆盖列定义”部分。

## <a name="specify-a-link-to-financial-dimensions-cell"></a>指定“链接到财务维度”单元格
**“链接到财务维度”**单元格包含至应包含在报表每一行中的财务数据的链接。 此单元格包含维度值，而且您可指定 Microsoft Excel 工作表中的单元格，或除此之外，指定段值或维度值。 要打开**“维度”**对话框，请双击**“链接到财务维度”**单元格。 **注意：**报表设计器不能选择 Microsoft Dynamics ERP 系统中包含任何下列保留字符的科目、维度或字段：&、\*、\[、\]、{ 或 }。 要为已在行定义中的行指定信息，请在**“链接到财务维度”**单元格中添加信息。 要添加链接到财务数据的新行，请使用**“从以下位置插入行”**对话框在报表定义中创建新行。 列标题将根据列的配置方式发生更改，如下表中所示。

| 选择的链接类型       | “链接”列的描述将更改为 |
|----------------------------------|----------------------------------------------------|
| 财务维度             | 链接到财务维度                       |
| 外部工作表               | 链接到工作表                                  |
| 财务维度 + 工作表 | 链接到财务维度 + 工作表           |
| Management Reporter 报表       | Management Reporter 报表                         |

### <a name="specify-a-dimension-or-range"></a>指定维度或范围

1.  在报表设计器中，打开要修改的行定义。
2.  双击**“链接到财务维度”**列中的单元格。
3.  在**“维度”**对话框中，双击维度名称下的单元格。
4.  在维度的对话框中，选择**“单个或系列”**。
5.  在**从**字段中，输入起始维度，或单击![浏览](https://i-technet.sec.s-msft.com/dynimg/IC679490.gif "浏览")搜索可用维度。 要输入维度的范围，在**“到”**字段中输入结束维度。
6.  单击**“确定”**以关闭维度的对话框。 **“维度”**对话框将显示更新后的维度或范围。
7.  单击**“确定”**以关闭**“维度”**对话框。

## <a name="display-zero-balance-accounts-in-a-row-definition"></a>显示行定义中的零余额科目
默认情况下，报表设计器不会打印财务数据中没有相应余额的任何行。 因此，您可创建一个包含所有自然科目段值或所有维度值的行定义，然后对您的任何部门使用此行定义。

### <a name="modify-zero-balance-settings"></a>修改零余额设置

1.  在报表设计器中，打开要修改的报表定义。
2.  在**“设置”**选项卡上的**“其他格式”**下，选择报表定义中所使用的行定义的选项。
3.  在**“文件”**菜单上，单击**“保存”**以保存您的更改。

## <a name="use-wildcard-characters-and-ranges-in-a-row-definition"></a>在行定义中使用通配符和范围
当您在**“维度”**对话框中输入自然科目段值时，可在段的任何位置中放置通配符（? 或 \*）。 报表设计器将提取定义位置的所有值，而不考虑通配符。 例如，行定义只包含自然科目段值，而自然科目段包含 4 个字符。 通过在行中输入 **6???**， 您命令报表设计器包含具有以 6 开头的自然科目段值的所有科目。 如果输入 **6\***，将返回相同的结果，而且结果还包含可变宽度值，如 **60** 和 **600000**。 报表设计器会将每个通配符 (?) 替换为完整范围的可能值，这包含字母和特殊字符。 例如，在 **12?0** 到 **12?4** 的范围中，**12?0** 中的通配符将替换为字符集中的最低值，而 **12?4** 中的通配符将替换为字符集中的最高值。 **注意：**您应避免在范围的起始和结束科目中使用通配符。 如果您在起始或结束科目中使用通配符，可能收到意外结果。

### <a name="single-segment-or-single-dimension-ranges"></a>单段或单维度范围

您可以指定段值或维度值的范围。 指定范围的好处在于，您不必在每次向财务数据添加新的段值或维度值时更新行定义。 例如，范围 **+Account=\[6100:6900\]** 会将 6100 到 6900 科目中的值拉取到行金额中。 如果范围包含通配符 (?)，则报表设计器不会按字符计算范围。 相反，将确定范围的低端和高端值，然后包含这两端的值以及两端之间的所有值。 **注意：**报表设计器不能选择 Microsoft Dynamics ERP 系统中包含任何下列保留字符的科目、维度或字段：&、\*、\[、\]、{ 或 }。 仅当您通过使用**“从维度插入行”**对话框自动构建行定义时，才可添加与号 (&)。

### <a name="multiple-segment-or-multiple-dimension-ranges"></a>多段或多维度范围

通过使用多个维度值的组合输入范围时，将基于 ...\财务维度\逐维度完成范围比较。 范围比较无法逐字符或部分段完成。 例如，范围 **+Account=\[5000:6000\], Department=\[1000:2000\], Cost center=\[00\]** 仅包含与每个段匹配的科目。 在此方案中，第一个维度必须位于 5000 至 6000 的范围中，第二个维度必须位于 1000 至 2000 的范围中，最后一个维度必须为 00。 例如，**+Account=\[5100\], Department=\[1100\], Cost center=\[01\]** 未包含在报表上，因为最后一个段超出指定范围。 如果某一段值包含空格，请将此值包含在方括号中 (\[ \]) 中。 下列值对 4 字符段有效：**\[ 234\]、\[123 \]、\[1 34\]**。 维度值应包含在方括号 (\[ \]) 中，报表设计器将为您添加这些方括号。 当多段或多维度范围包含通配符（? 或 \*）时，将确定整个多段或多维度范围的低端和高端值，然后包含这两端的值以及两端之间的所有值。 如果您具有更大的范围（如 40000 至 99999 整个范围内的科目），则应尽可能指定有效起始科目和结束科目。 **注意：**报表设计器不能选择 Microsoft Dynamics ERP 系统中包含任何下列保留字符的科目、维度或字段：&、\*、\[、\]、{ 或 }。 仅当您通过使用**“从维度插入行”**对话框自动构建行定义时，才可添加与号 (&)。

## <a name="add-or-subtract-from-other-accounts-in-a-row-definition"></a>与行定义中的其他科目进行加减
要将一个科目中的货币金额与另一个科目中的货币金额进行加减，您可在**“链接到财务维度”**单元格中使用加号 (+) 和减号 (-)。 下表显示指向财务数据的加减链接可接受的格式。

| 操作                                                                               | 使用此格式                                                                                              |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| 添加两个完全符合规则的科目。                                                       | +Division=\[000\], Account=\[1205\], Department=\[00\]+Division=\[100\], Account=\[1205\], Department=\[00\] |
| 添加两个段值。                                                                 | +Account=\[1205\]+Account=\[1210\]                                                                           |
| 添加包含通配符的段值。                                    | +Account=\[120?+Account=\[11??\]                                                                             |
| 添加一系列完全符合规则的科目。                                                | +Division=\[000:100\], Account=\[1205\], Department=\[00\]                                                   |
| 添加一系列段值。                                                          | +Account=\[1200:1205\]                                                                                       |
| 添加一系列包含通配符的段值。                         | +Account=\[120?:130?\]                                                                                       |
| 从另一完全符合规则的科目中减去一个完全符合规则的科目。              | +Division=\[000\], Account=\[1205\], Department=\[00\]-Division=\[100\], Account=\[1205\], Department=\[00\] |
| 从另一段值中减去一个段值。                                  | +Account=\[1205\]-Account=\[1210\]                                                                           |
| 从另一段值中减去一个包含通配符的段值。 | +Account=\[1200\]-Account=\[11??\]                                                                           |
| 减去一系列完全符合规则的科目。                                           | -Division=\[000:100\], Account=\[1200:1205\], Department=\[00:01\]                                           |
| 减去一系列段值。                                                     | -Account=\[1200:1205\]                                                                                       |
| 减去一系列包含通配符的段值。                    | -Account=\[120?:130?\]                                                                                       |

虽然您可直接修改科目，但也可使用**“维度”**对话框将正确的格式应用于财务数据链接。 任何值均可包含通配符（? 或 \*）。 但是，报表设计器不能选择 Microsoft Dynamics ERP 系统中包含任何下列保留字符的科目、维度或字段：&、\*、\[、\]、{ 或 }。 **注意：**要减去值，您必须将这些值放入圆括号中。 例如，如果您输入 **450? (- 4509)**，它将显示为 **+Account=\[4509\]-Account=\[450?\]**，并且您命令报表设计器 从以 450 开始的任何科目段的金额中减去科目段 4509 的金额。

### <a name="add-or-subtract-accounts-from-other-accounts"></a>从其他科目中加减金额

1.  在报表设计器中，打开要修改的行定义。
2.  在相应行中，双击**“链接到财务维度”**列中的单元格。
3.  在**“维度”**对话框的第一行中，执行下列步骤：
    1.  在第一个字段中，选择所有维度（默认），或者单击以打开**“管理维度集”**对话框，在其中您可创建、修改、复制或删除集。
    2.  双击**运算符 +/-** 单元格，然后选择适用于行中一个或多个维度值或维度集的加号 (**+**) 或减号 (**-**) 运算符。
    3.  在相应的维度值列中，双击单元格以打开**“维度”**对话框，然后选择此维度值适用于单个或系列、维度值还是汇总科目。 有关**“维度”**对话框中字段的描述，请参阅“维度对话框的描述”部分。
    4.  在**“从”**列和**“到”**列中输入段值。

4.  重复执行第 2 步到第 3 步，以添加更多运算。

**注意：**此运算符将应用于行中的所有维度。

## <a name="description-of-the-dimensions-dialog-box"></a>“维度”对话框的描述
下表描述**“维度”**对话框中的字段。

| 物料                | 描述                                                                                                                                                                                                                                                                                             |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 单个或系列 | 在**从**字段中，输入科目的名称，或单击**浏览**按钮![浏览](https://i-technet.sec.s-msft.com/dynimg/IC679490.gif "浏览")以浏览科目。 要选择范围，请在**“到”**字段中输入值或浏览值。                                             |
| 维度值集 | 在**“名称”**字段中，输入维度值集的名称。 要创建、修改、复制或删除集，请单击**“管理维度值集”**。 **公式**字段将使用行定义中此维度值集的**链接到财务维度**单元格中的公式填充。 |
| 汇总科目   | 在**“名称”**字段中，输入或浏览汇总科目的维度。 **“公式”**字段将使用报表定义中此汇总科目的**“链接到财务维度”**单元格中的公式填充。                                                                       |

## <a name="add-dimension-value-sets-in-a-row-definition"></a>在行定义中添加维度值
维度值集是命名维度值组。 维度值集可只包含单维度中的值，但您可在多个行定义、列定义、报告结构树定义和报表定义中使用维度值集。 您还可将维度值集组合到报表定义中。 当财务数据更改需要您更改维度值集时，您可更新维度值集定义，此更新将应用于使用此维度值集的所有区域。 例如，如果通常指示要链接到您的财务数据的一系列值（如 5100 至 5600 的值），您可将此范围分配给名为“Sales”的科目集。 在创建一个维度值集后，可选择此集作为财务数据链接。 另举一例，如果向 Sales 分配了 5100 至 5600 的值范围，向 Discounts 分配了 4175，则可通过从 Sales 中减去 Discounts 来确定销售总额。 此运算表示为 **(5100:5600)-4175**。

### <a name="create-a-set-of-dimension-values"></a>创建维度值集

1.  在报表设计器中，打开要修改的行、列或树定义。
2.  在**“编辑”**菜单上，单击**“管理维度值集”**。
3.  在**“管理维度值集”**对话框的**“维度”**字段中，选择要创建的维度值集的类型，然后单击**“新建”**。
4.  在**“新建”**对话框中，输入此集的名称和描述。
5.  在**“从”**列中，双击单元格。
6.  在**“科目”**对话框中，选择列表中的科目名称或在**“搜索”**字段中搜索条目。 然后，单击“确定”****。
7.  在**“到”**列中重复第 5 步到第 6 步以针对运算符设计公式。
8.  当公式完成后，单击**“确定”**。
9.  在**“管理维度集”**对话框中，单击**“关闭”**。

### <a name="update-a-set-of-dimension-values"></a>更新维度值集

1.  在报表设计器中，打开要修改的行、列或树定义。
2.  在**“编辑”**菜单上，单击**“管理维度值集”**。
3.  在**“管理维度值集”**对话框的**“维度”**字段中，选择维度类型。
4.  在列表中，选择要更新的维度值集，然后单击**“修改”**。
5.  在**“修改”**对话框中，修改要包含在此集中的公式值。 **注意：**如果您添加新科目或维度，请确保修改现有维度值集以合并更改。
6.  双击单元格，并选择正确的运算符、**“开始”**科目和**“结束”**科目。
7.  单击**“确定”**以关闭**“修改”**对话框并保存更改。

### <a name="copy-a-dimension-set"></a>复制维度集

1.  在报表设计器中，打开要修改的行、列或树定义。
2.  在**“编辑”**菜单上，单击**“管理维度值集”**。
3.  在**“管理维度值集”**对话框的**“维度”**字段中，选择维度类型。
4.  在列表中，选择要复制的集，然后单击**“另存为”**。
5.  输入已复制集的新名称，然后单击**“确定”**。

### <a name="delete-a-dimension-set"></a>删除维度集

1.  在报表设计器中，打开要修改的行、列或树定义。
2.  在**“编辑”**菜单上，单击**“管理维度值集”**。
3.  在**“管理维度值集”**对话框的**“维度”**字段中，选择维度类型。
4.  选择要删除的维度集，然后单击**“删除”**。 单击**“是”**可永久删除维度值集。


<a name="see-also"></a>请参阅
--------

[Microsoft Dynamics 365 for Operations 财务报告](financial-reporting-intro.md)


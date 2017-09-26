---
title: "查看财务报表"
description: "本文介绍如何在 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中查看和探索财务报表。 它包含有关可应用于财务报表的各个选项的信息，这些选项可以更改报表外观和它们包含的数据。"
author: kweekley
manager: AnnBe
ms.date: 06/08/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 10334
ms.assetid: d20f435f-fb65-4068-ab09-7efc7be683a6
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 102031174417a33b12c32f6b8185556b8c4701e5
ms.contentlocale: zh-cn
ms.lasthandoff: 06/13/2017


---

# <a name="view-financial-reports"></a>查看财务报表

[!include[banner](../includes/banner.md)]


本文介绍如何在 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中查看和探索财务报表。 它包含有关可应用于财务报表的各个选项的信息，这些选项可以更改报表外观和它们包含的数据。

<a name="financial-reporting-overview"></a>财务报告概览
----------------------------

## <a name="open-a-financial-report"></a>打开财务报表
若要打开报表，选择报表名称。 首次打开报表，它将为上个月自动生成。 例如，如果在 2015 年 8 月首次打开报表，将为 2015 年 7 月 31 日生成报表。 在打开报表后，可以通过深化到特定的数据部分并更改报表选项来开始探索报表。

## <a name="drill-down-on-a-financial-report"></a>深化到财务报表
财务报表可以包括多个详细级别。 财务级别是您打开一个财务报表看到的第一个级别。 若要转到科目级别，选择要深化到的数据。 例如，若要查看销售科目详细信息，选择您要探索的销售数据。 在科目级别，您可以深化以查看组成帐户余额的交易记录。 有两种方式来查看交易记录：报表交易记录和凭证交易记录。

-   **报表交易记录** – 交易记录在包括在财务报表中的一个格式化视图中显示。 若要查看格式化视图中的交易记录，请选择要深化到的数据，然后单击**深化到报表交易记录级别**。
-   **凭证交易记录** – 凭证交易记录查询将打开，从中可以查看交易记录。 若要查看凭证交易记录查询中的交易记录，请选择要深化到的数据，然后单击**打开帐户交易记录**。

如果数据是预算数据，您可以选择打开预算科目条目。 要关闭报表的任何级别并返回开始位置，可以按 Esc 键或单击右上方的**关闭**按钮 (**X**)。

## <a name="change-report-options"></a>更改报表选项
您可以更改报表日期，应用属性和维度筛选器，或更改**实际与预算**报表上的预算方案。 在操作窗格上，单击**报表选项**，然后按照一个或多个以下步骤操作：

-   若要更改报表的基准期间和基准年，选择一个基准期间和基准年，然后单击**确定**。
-   若要将属性筛选器应用于报表，请选择**添加属性筛选器**。 选择属性，输入属性值，然后单击**确定**。 例如，如果您选择**科目类别**属性，输入 **SALES** 作为属性值。 若要删除属性筛选器，请单击**清除**。
-   若要将维度筛选器应用于报表，请选择**添加维度筛选器**。 选择维度，然后键入维度 ID 或在列表中选择维度。 若要删除维度筛选器，请单击**清除**。
-   若要更改报表**实际与预算**中的方案，选择新的方案，然后单击**确定**。 如果所选方案是不同的年份，则确保更新基准年。 例如，如果当前方案是 FY2015，您选择 FY2016 的新方案，则应将基准年更改为 **2016**。

当您单击**确定**后，您选择的所有选项都将应用于报表。 如果您决定不应用所选的选项，单击**取消**。

## <a name="update-a-financial-report"></a>更新财务报表
您可以刷新（更新）财务报表，以便显示报表生成期间和年份的近期数据。 例如，如果您更新为 2015 年 10 月生成的一个财务报表，该报表反映已为 2015 年 10 月过帐的所有新交易记录。 若要更新财务报表，在“操作”窗格中，单击**刷新**。 更新的报表仅对更新其的人员可用。 为了其他人员可以看到相同的数据，必须发布报表。

## <a name="publish-a-financial-report"></a>发布财务报表
在您更新财务报表后，可以将其发布。 组织中的其他人然后可以查看它。 若要发布报表，在操作窗格中，单击**发布**。

## <a name="display-a-financial-report-in-a-different-currency"></a>以不同的币种显示财务报表
财务报表可以在任何币种在任何时间显示。 若要以不同的币种显示报表，在操作窗格中，单击**币种**，然后选择一个币种。 报表将转换为该币种，并且显示结果。 包括作为报表设计的一部分的所有币种代码或符号将更新以反映新币种。 显示在列表中的币种是在 Finance and Operations 中配置的申报币种。

## <a name="display-a-summarized-view-of-the-financial-report"></a>显示财务报表的汇总视图
一个财务报表可以包含明细行和汇总行。 明细行是包含主科目或维度的行。 汇总行是描述、合计和计算行。 若要只显示报表的汇总行，单击**显示**，然后单击**仅汇总行**。 报表将折叠并只显示汇总行。 若要与汇总行一起查看明细行，请单击**显示**，然后再次单击**仅汇总行**。

## <a name="open-a-financial-report-from-a-previous-month"></a>从上个月打开一个财务报表
您可以查看当前月或以前月的报表，而不重新生成报表。 若要打开上个月的报表，单击**显示**，然后单击**以前的报表**。 生成报表的以前月的列表将显示。 展开要查看报表的那个月，选择该日期，然后单击**确定**。 之前月的报表将显示。 若要返回当前月的报表，请单击**取消**。

## <a name="print-a-financial-report"></a>打印财务报表
若要打印一个财务报表，在操作窗格中，单击**打印**，然后按照一个或多个以下步骤来设置打印选项：

-   若要在打印的报表中包括各个明细级别，将滑块设置为**是**或**No**。 如果报表使用报告结构树，可以选择包括所有报告单位或只包括当前报告单位。
-   若要设置页面尺寸，请在列表中选择页面尺寸。
-   若要设置页面布局，选择列表中的某个布局。 如果您希望报表内容适合您选择的宽度，将滑块设置为**是**。
-   若要设置页边距，按英寸键入顶部、底部、左边距和右边距的尺寸。

在您完成设置打印选项后，单击**打印**以打印报表。 如果您决定不打印报表，则单击**取消**。 打印的报表的预览将显示。 您可以选择将报表发送到的打印机，并且，也可以调整打印选项。

## <a name="export-a-financial-report"></a>导出财务报表
若要导出财务报表，在操作窗格中，单击**导出**。 报表导出到 Microsoft Excel，并且，您的浏览器将提示您打开或保存导出的文件。 在报表设计中定义的导出设置应用到导出的报表。    

<a name="see-also"></a>请参阅
--------

[Microsoft Dynamics AX 的财务报告](/dynamics365/unified-operations/dev-itpro/analytics/financial-reporting-intro)





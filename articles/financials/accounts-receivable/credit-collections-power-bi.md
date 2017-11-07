---
title: "信用和收款管理 Power BI 内容包"
description: "此主题介绍信用和收款管理 Power BI 内容中的内容。 它说明如何访问 Power BI 报表，并提供有关用于构建内容的数据模型和实体的信息。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations. Core
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 7aec3d81fca86abdab4f5fcee54f832f917ffe92
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="credit-and-collections-management-power-bi-content"></a>信用和收款管理 Power BI 内容包

此主题介绍**信用和收款管理** Microsoft Power BI 内容中的内容。 它说明如何访问 Power BI 报表，并提供有关用于构建内容的数据模型和实体的信息。

## <a name="overview"></a>概览

**信用和收款管理** Power BI 内容是为信用和收款经理和收款职员而创建的。 它提供关键信用和收款指标，例如销售款未清天数、逾期余额、信用曝光和超出信用额度的客户。 它使用交易记录数据，并且提供跨所有公司的信用和收款的聚合视图。 它还提供各公司、客户组和客户的明细。

此 Power BI 内容包括 10 个报表页：

- 两个概览页（一页用于信用概览，另一页用于收款概览）
- 八个详细信息页，提供跨不同维度划分和细分的信用和收款指标的详细信息。

所有金额均以系统币种显示。 您可以在**系统参数**页设置系统币种。

默认情况下，显示当前公司的信用和收款数据。 要查看跨所有公司的数据，请将 **CustCollectionsBICrossCompany** 责任分配到角色。

## <a name="accessing-the-power-bi-content"></a>访问 Power BI 内容
如果您正在使用 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition（2017 年 7 月），则**信用和收款管理** Power BI 内容在**客户信用和收款**工作区显示。

## <a name="reports-that-are-included-in-the-power-bi-content"></a>此 Power BI 内容中包含的报表

**CustCollectionsBICrossCompany** Power BI 内容包括一个含有一组指标的报表。 这些指标显示为图表、磁贴和表。 下表概要介绍 **CustCollectionsBICrossCompany** Power BI 内容中的可视化。

| 报表页                 | 可视化 |
|-----------------------------|---------------|
| 收款概览        | <ul><li>客户过期</li><li>客户超出信用额度</li><li>DSO 30 天</li><li>未结案例</li><li>关闭案例的平均天数</li><li>未结活动</li><li>关闭活动的平均天数</li><li>未结利息单</li><li>未结催款单</li><li>客户暂停</li><li>销售暂停</li><li>帐龄余额</li><li>收款状态金额</li><li>收款代码金额</li><li>按原因勾销</li><li>结欠金额(按地区)</li><li>预期付款</li></ul> |
| 信用概览             | <ul><li>客户过期</li><li>信用额度与结欠金额</li><li>客户超出信用额度网格</li><li>每个公司的超出信用额度的客户</li><li>已使用信用额与总信用额度</li><li>信用额度与已使用信用额（按地区）</li><li>每种信用等级的客户</li></ul> |
| 信用额度                | <ul><li>信用额度</li><li>信用额度明细</li><li>信用额度（按客户）</li><li>每个客户组的信用额度</li><li>每个公司的每种信用等级的信用额度</li><li>信用额度与已用贷款(按地区)</li></ul> |
| 客户超出信用额度 | <ul><li>客户超出信用额度</li><li>客户超出信用额度明细</li><li>每个公司的超出信用额度的客户</li><li>超出信用额度的客户（按客户组）</li><li>超出信用额度的客户(按地区)</li></ul> |
| 客户过期          | <ul><li>客户过期</li><li>客户过期明细</li><li>客户过期（按公司）</li><li>客户过期（按客户组）</li><li>客户过期（按地区）</li></ul> |
| 帐龄余额               | <ul><li>帐龄余额</li><li>帐龄余额明细</li><li>每个公司的帐龄较长的余额</li><li>每个客户组的帐龄较长的余额</li></ul> |
| 预期付款           | <ul><li>预期付款</li><li>预期付款明细</li><li>每个公司的预期付款</li><li>每个客户组的预期付款</li><li>预期付款(按地区)</li></ul> |
| 勾销                  | <ul><li>勾销（按地区）</li><li>勾销明细</li><li>勾销（按主科目）</li><li>勾销（按公司）</li><li>勾销（按客户组）</li><li>勾销（按地区）</li></ul> |
| 收款状态          | <ul><li>争议</li><li>承诺付款已中断</li><li>承诺付款</li><li>收款状态明细</li><li>收款状态金额</li><li>未结案例</li><li>未结活动</li></ul> |
| 催款单         | <ul><li>收款代码金额</li><li>收款代码金额明细</li><li>催款单金额（按公司）</li><li>催款单金额（按客户组）</li><li>催款单金额（按地区）</li></ul> |

所有这些报表中的图表和磁贴均可以筛选和并固定到仪表板。 有关如何在 Power BI 中筛选和固定的更多信息，请参阅[创建和配置仪表板](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/)。 您还可以使用导出基础数据功能导出在可视化中汇总的基础数据。

## <a name="extending-the-power-bi-content"></a>扩展 Power BI 内容
使用在 Microsoft Dynamics Lifecycle Services (LCS) 中可用的内容包可以对未登录到 Finance and Operations 的人员提供出色的分析。 您可以修改这些内容包，使它们包含其他报表或视觉对象，然后将内容包发布到您的 Power BI.com 租户进行分析。

可在 LCS 中的共享资产库内找到**信用和收款管理** Power BI 内容。 有关如何下载内容并在您的组织中实现的详细信息，请参阅 [LCS 中 Microsoft 和合作伙伴提供的 Power BI 内容](../../dev-itpro/analytics/power-bi-content-microsoft-partners.md)。 若要观看显示如何实现 Power BI 内容的演示，请参阅 [Dynamics Lifecycle Services 中来自 Microsoft 和您的合作伙伴的 Power BI 内容](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix。

请务必下载适用于您使用的 Finance and Operations 版本的**信用和收款管理** Power BI 内容。

## <a name="understanding-the-data-model-and-entities"></a>了解数据模型和实体

以下数据用于填充**信用和收款管理** Power BI 内容中的报表。 此数据表示为实体商店内已分组的聚合度量。 实体商店是针对分析进行优化的 Microsoft SQL Server 数据库。 有关详细信息，请参阅 [Power BI 与实体商店集成概览](../../dev-itpro/analytics/power-bi-integration-entity-store.md)。

| 实体                                      | 关键聚合度量           | 数据源                                 | 字段                                                      | 说明 |
|---------------------------------------------|--------------------------------------|---------------------------------------------|------------------------------------------------------------|-------------|
| CustCollectionsBIActivitiesAverageCloseTime | NumOfActivities，AveragecClosedTime  | smmActivities                               | AverageOfChildren(AverageClosedTime) Count(ActivityNumber) | 已关闭活动的计数和关闭这些活动所用的平均时间。 |
| CustCollectionsBIActivitiesOpen             | ActivityNumber                       | smmActivities                               | Count(ActivityNumber)                                      | 未结活动的计数。 |
| CustCollectionsBIAgedBalances               | AgedBalances                         | CustCollectionsBIAgedBalancesView           | Sum(SystemCurrencyBalance)                                 | 帐龄余额的总和。 |
| CustCollectionsBIBalancesDue                | SystemCurrencyAmount                 | CustCollectionsBIBalanceDueView             | Sum(SystemCurrencyAmount)                                  | 逾期的金额。 |
| CustCollectionsBICaseAverageCloseTIme       | NumOfCases，CaseAverageClosedTime    | CustCollectionsCaseDetail                   | AverageOfChildren(CaseAverageClosedTime) Count(NumOfCases) | 已关闭案例的计数和关闭这些案例所用的平均时间。 |
| CustCollectionsBICasesOpen                  | CaseId                               | CustCollectionsCaseDetail                   | Count(CaseId)                                              | 未结案例的计数。 |
| CustCollectionsBICollectionLetter           | CollectionLetterNum                  | CustCollectionLetterJour                    | Count(CollectionLetterNum)                                 | 未结催款单的计数。 |
| CustCollectionsBICollectionLetterAmount     | CollectionLetterAmounts              | CustCollectionsBIAccountsReceivables        | Sum(SystemCurrencyAmount)                                  | 已过帐催款单的余额。 |
| CustCollectionsBICollectionStatus           | CollectionStatusAmounts              | CustCollectionsBIAccountsReceivables        | Sum(SystemCurrencyAmount)                                  | 具有催款状态的交易记录的余额。 |
| CustCollectionsBICredit                     | CreditExposed，AmountOverCreditLimit | CustCollectionsBICreditView                 | Sum(CreditExposed), Sum(AmountOverCreditLimit)             | 信用曝光和客户超过其信用额度的金额的总和。 |
| CustCollectionsBICustOnHold                 | 已冻结                              | CustCollectionsBICustTable                  | Count(Blocked)                                             | 处于暂停状态的客户的数量。 |
| CustCollectionsBIDSO                        | DSO30                                | CustCollectionsBIDSOView                    | AverageOfChildren(DSO30)                                   | 30 天销售款未清天数。 |
| CustCollectionsBIExpectedPayment            | ExpectedPayment                      | CustCollectionsBIExpectedPaymentView        | Sum(SystemCurrencyAmounts)                                 | 下一年预期付款总和。 |
| CustCollectionsBIInterestNote               | InterestNote                         | CustInterestJour                            | Count(InterestNote)                                        | 已创建的利息单的数量 |
| CustCollectionsBISalesOnHold                | SalesId                              | SalesTable                                  | Count(SalesId)                                             | 处于暂停状态的总销售单的数量。 |
| CustCollectionsBIWriteOff                   | WriteOffAmount                       | CustCollectionsBIWriteOffView               | Sum(SystemCurrencyAmount)                                  | 已勾销的交易记录的总和。 |

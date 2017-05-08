---
title: "在折扣日期之前完全结算部分客户付款和最后付款"
description: "本文提供显示如何记录客户的部分付款以及在现金折扣期间内执行现金折扣的情况。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14491
ms.assetid: 0f07d3ce-a439-43ed-a22e-957ccd36a37b
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: ac2c569666b97bc430d3d677366a88446ab76091
ms.lasthandoff: 03/31/2017


---

# <a name="settle-a-partial-customer-payment-and-the-final-payment-in-full-before-the-discount-date"></a>在折扣日期之前完全结算部分客户付款和最后付款

[!include[banner](../includes/banner.md)]


本文提供显示如何记录客户的部分付款以及在现金折扣期间内执行现金折扣的情况。

Fabrikam 向客户 4028 销售货物， 如果发票在 14 天内支付，则 Fabrikam 提供 1% 的现金折扣。 发票必须在 30 天时支付。 Fabrikam 还为部分付款提供现金折扣。 结算参数位于**应付帐款参数**页上。

## <a name="customer-invoice"></a>客户发票
6 月 25 日，Arnie 为客户 4028 输入并过帐 1,000.00 的发票。 Arnie 可以在**“客户交易记录”**页上查看该交易记录。

| 凭证   | 交易记录类型 | 日期      | 开票 | 交易币种借方金额 | 交易币种贷方金额 | 余额  | 货币 |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10010 | 开票          | 6/25/2015 | 10010   | 1,000.00                             |                                       | 1,000.00 | 美元      |

从**客户**或**客户交易记录**页，Arnie 可以打开**结算交易记录**页查看对发票可用的日期和现金折扣的金额。 到期日期为 7 月 25 日，如果在 7 月 9 日支付发票，则可用的现金折扣为 10.00。

| 标记     | 使用现金折扣 | 凭证   | 帐户 | 日期      | 到期日期  | 开票 | 交易记录币种金额 | 货币 | 要结算的金额 |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| 已选择 | 标准            | FTI-10010 | 4028    | 6/25/2015 | 7/25/2015 | 10010   | 1,000.00                       | 美元      | 990.00           |

折扣信息显示在已标记发票**结算交易记录**页的底部。

|                              |           |
|------------------------------|-----------|
| 现金折扣日期           | 7/09/2015 |
| 现金折扣金额         | 10.00     |
| 使用现金折扣            | 标准    |
| 提取了现金折扣          | 0.00      |
| 要提取的现金折扣金额 | 10.00     |

Arnie 单击**现金折扣**以查看折扣金额。

| 现金折扣日期 | 现金折扣金额 | 交易记录币种金额 |
|--------------------|----------------------|--------------------------------|
| 7/9/2015           | 10.00                | 990.00                         |
| 7/25/2015          | 0.00                 | 1,000.00                       |

## <a name="partial-payment-by-using-the-enter-customer-payments-page"></a>通过使用“输入客户付款”页支付的部分付款
客户 4028 7 月 1 日发送 500.00 的付款。 若要输入此付款，Arnie 不单击**行**。 相反，他可以通过创建新的付款日记帐然后打开**输入客户付款**页记录付款。 他输入付款信息并标记他输入的发票。 Arnie 在金额中输入 **500.00**，他还在网格中的**待付金额**字段中输入 **500.00**。 由于 Fabrikam 对部分付款使用现金折扣，他将看到还执行 5.05 的部分现金折扣。 此折扣的计算方式为 500.00 ÷ 0.99 × 0.01 = 5.05。 （在此计算中，500.00 除以 0.99，因为有 1% 的折扣。 因此，客户支付发票的 99%。 然后，结果乘以折扣百分比，即 1% 或 0.01。 如果客户执行完全折扣 10.00，必须结算的金额为 990.00。）折扣信息出现在**输入客户付款**页的底端。

| 要提取的现金折扣金额 | 提取了现金折扣 | 待付金额 |
|------------------------------|---------------------|---------------|
| 5.05                         | 0.00                | 500.00        |

## <a name="partial-payment-by-using-the-journal-lines"></a>通过使用日记帐行的部分付款
不打开付款日记帐的**输入客户付款**页，Arnie 可以单击**行**输入付款。 付款日志随即显示，其中 Arnie 可以为客户 4028 输入行。 然后，Arnie 打开**“结算交易记录”**页，以便他可以标记要结算的发票。 Arnie 标记发票并将**要结算的金额**字段中的值更改为 **500.00**。 他再次看到完整发票的**现金折扣金额**字段中的值为 **10.00**，以及**要提取的现金折扣金额**字段中的值为 **5.05**。 因此，Arnie 以 505.05 结算此发票。

| 标记     | 使用现金折扣 | 凭证   | 帐户 | 日期      | 到期日期  | 开票 | 交易记录币种金额 | 货币 | 要结算的金额 |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| 已选择 | 标准            | FTI-10010 | 4028    | 6/25/2015 | 7/25/2015 | 10010   | 1,000.00                       | 美元      | 500.00           |

折扣信息显示在“结算未结交易记录”****页的底部。

|                              |           |
|------------------------------|-----------|
| 现金折扣日期           | 7/09/2015 |
| 现金折扣金额         | 10.00     |
| 使用现金折扣            | 标准    |
| 提取了现金折扣          | 0.00      |
| 要提取的现金折扣金额 | 5.05      |

如果客户要刚好结算一半的发票金额，客户将提交 495.00 的付款。 在这种情况下，Arnie 在**要结算的金额**字段中输入 **495.00**。 5.00 的现金折扣还将采用，因此，合计的结算金额是 500.00。

| 标记     | 使用现金折扣 | 凭证   | 帐户 | 日期      | 到期日期  | 开票 | 交易记录币种金额 | 货币 | 要结算的金额 |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| 已选择 | 标准            | FTI-10010 | 4028    | 6/25/2015 | 7/25/2015 | 10010   | 1,000.00                       | 美元      | 495.00           |

折扣信息显示在“结算未结交易记录”****页的底部。

|                              |           |
|------------------------------|-----------|
| 现金折扣日期           | 7/09/2015 |
| 现金折扣金额         | 10.00     |
| 使用现金折扣            | 标准    |
| 提取了现金折扣          | 0.00      |
| 要提取的现金折扣金额 | 5.00      |

Arnie 关闭**结算交易记录**页。 在日志中创建了 495.00 的付款行，然后 Arnie 对该日志进行过帐。 他还可以在**客户交易记录**页上查看客户交易记录。 在此页上，Arnie 看到该发票具有 500.00 的余额。 他还可以查看 495.00 的付款和 5.00 的折扣。

| 凭证    | 交易记录类型 | 日期      | 开票 | 交易币种借方金额 | 交易币种贷方金额 | 余额 | 货币 |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10010  | 开票          | 6/25/2015 | 10010   | 1,000.00                             |                                       | 500.00  | 美元      |
| ARP-10010  |  付款         | 7/1/2015  |         |                                      | 495.00                                | 0.00    | 美元      |
| DISC-10010 |  现金折扣   | 7/1/2015  |         |                                      | 5.00                                  | 0.00    | 美元      |

## <a name="payment-for-the-remaining-amount"></a>剩余金额的付款
客户 4028 在 7 月 8 日（现金折扣期间内）支付 495.00 剩余金额。 Arnie 创建 7 月 8 日的付款日志并将交易记录标记为结算。 他看到必须要结算的金额为 495.00。 **估计的现金折扣**字段中的值为 **5.00**，因为 5.00 折扣是以前获得的。

|                         |        |
|-------------------------|--------|
| 标记的合计            | 495.00 |
| 估计的现金折扣 | 5.00   |

有关标记的交易记录的信息将显示在**“结算未结交易记录”**页上的网格中。

| 标记     | 使用现金折扣 | 凭证   | 帐户 | 日期      | 到期日期  | 开票 | 交易记录币种金额 | 货币 | 要结算的金额 |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| 已选择 | 标准            | FTI-10010 | 4028    | 6/25/2015 | 7/25/2015 | 10010   | 1,000.00                       | 美元      | 495.00           |

折扣信息显示在“结算未结交易记录”****页的底部。

|                              |           |
|------------------------------|-----------|
| 现金折扣日期           | 7/09/2015 |
| 现金折扣金额         | 10.00     |
| 使用现金折扣            | 标准    |
| 提取了现金折扣          | 5.00      |
| 要提取的现金折扣金额 | 5.00      |

Arnie 过帐此日记帐并审核**客户交易记录**页中的客户交易记录。 发票余额现在为 0.00，并且 Arnie 看到两个付款和两个现金折扣。

| 凭证    | 交易记录类型 | 日期      | 开票 | 交易币种借方金额 | 交易币种贷方金额 | 余额 | 货币 |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10010  | 开票          | 6/25/2015 | 10010   | 1,000.00                             |                                       | 0.00    | 美元      |
| ARP-10010  | 付款          | 7/1/2015  |         |                                      | 495.00                                | 0.00    | 美元      |
| DISC-10010 | 现金折扣    | 7/1/2015  |         |                                      | 5.00                                  | 0.00    | 美元      |
| ARP-10011  | 付款          | 7/8/2015  |         |                                      | 495.00                                | 0.00    | 美元      |
| DISC-10011 | 现金折扣    | 7/8/2015  |         |                                      | 5.00                                  | 0.00    | 美元      |






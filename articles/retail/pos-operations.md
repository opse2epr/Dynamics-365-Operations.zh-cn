---
title: 销售点 (POS) 联机和脱机操作
description: 此主题提供有关 Microsoft Dynamics 365 for Retail 中销售点 (POS) 操作的详细信息。 它指定操作可以在应用程序的哪个位置调用，以及是否可在脱机模式下使用。
author: jblucher
manager: AnnBe
ms.date: 10/12/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-09-27
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 44a2ec48f868c803c80c8df8eb809bc2254e63da
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1505088"
---
# <a name="online-and-offline-point-of-sale-pos-operations"></a>销售点 (POS) 联机和脱机操作

[!include [banner](includes/banner.md)]

用户在销售点 (POS) 执行的大多数行动被视为操作。 操作在 Microsoft Dynamics 365 for Retail 后端办公系统中配置和管理。 许多操作可以添加到 POS 按钮网格中的按钮。 用户随后可以选择按钮来调用操作并执行其功能。 其他操作是主 POS 应用程序的一部分，从屏幕上按钮或作为其他工作流或流程的一部分调用。

下表提供有关可用于 Retail Modern POS 和 Dynamics 365 for Retail 的 Cloud POS 的操作的详细信息。 该表还指定了操作可以在应用程序的哪个位置调用，以及是否可在 POS 处于脱机模式时使用。

某些操作当前未在 Retail Modern POS 或 Dynamics 365 for Retail 的 Cloud POS 中提供。 其中某些操作是需要额外的扩展和配置的区域特定操作。 其他则是当前不支持的 Microsoft Dynamics AX 2012 的功能。

以下列指定可以调用操作的位置：

- **按钮网格** – 操作可分配到 POS 按钮网格（是 POS 屏幕布局的一部分）中的按钮。
- **交易记录屏幕** – 操作可从在 POS 交易记录屏幕中配置的 POS 按钮网格调用。
- **欢迎屏幕** – 操作可从在 POS 欢迎屏幕中配置的 POS 按钮网格调用。

> [!NOTE]
> 下面列出的工序适用于最新版本的 Dynamics 365 for Retail。 某些工序可能已更改或可能不在以前版本中提供。

| ID | 工序 | 说明 | 按钮网格 | 交易记录屏幕 | 欢迎屏幕 | 脱机可用 | 区域特定 |
|----|-----------|-------------|-------------|--------------------|----------------|-------------------|-----------------|
| 707 | 启用设备 | 通过允许经过身份验证的用户提供连接信息和分配设备和登记 ID 来激活当前设备。 | 无 | 无 | 无 | 无 | 无 |
| 134 | 添加隶属关系 | 向交易记录中添加预先选择的从属项。 在**按钮属性**页面上选择该隶属关系。 | 是 | 是 | 无 | 是 | 无 |
| 135 | 从列表中添加隶属关系 | 通过从列表中选择，将隶属关系添加到交易记录中。 | 是 | 是 | 是 | 是 | 无 |
| 137 | 将隶属关系添加到客户 | 在**客户详细信息**页中向客户添加隶属关系。 | 无 | 无 | 无 | 是 | 无 |
| 138 | 删除客户的隶属关系 | 从**客户详细信息**页中删除隶属关系。 | 无 | 无 | 无 | 是 | 无 |
| 643 | 添加优惠券代码 | 通过在 POS 中输入优惠券代码来添加优惠券。 | 是 | 是 | 无 | 是 | 无 |
| 117 | 添加会员卡 | 提示用户输入要添加到当前交易记录的会员卡号。 | 是 | 是 | 无 | 是 | 无 |
| 136 | 添加序列号 | 此操作允许用户为当前所选的产品指定序列号。 | 是 | 是 | 无 | 是 | 无 |
| 1214 | 添加装运地址 | 此操作不受支持。 | 不适用 | 不适用 | 不适用 | 不适用 | 无 |
| 519 | 添加到礼品卡 | 为指定的礼品卡充值。 | 是 | 是 | 无 | 无 | 无 |
| 6000 | 允许跳过会计登记 | 此操作不受支持。 | 不适用 | 不适用 | 不适用 | 不适用 | 是 |
| 1212 | 银行投箱 | 记录发给银行的金额和其他信息（如银行钱袋编号）。 | 是 | 是 | 是 | 是 | 无 |
| 923 | 银行合计验证 | 此操作不受支持。 | 不适用 | 不适用 | 不适用 | 不适用 | 是 |
| 915 | 空操作 | 此操作表示可自定义的按钮，软件开发人员可以针对业务所需的任何专门操作通过编程方式更改该按钮。 | 是 | 是 | 是 | 是 | 无 |
| 1053 | 直接结束班次 | 将当前班次设置为已直接结束，并将用户退出。直接结束的班次对其他交易关闭，但仍对开票人操作（如取钱和钱币清点）打开。 | 是 | 是 | 是 | 无 | 无 |
| 310 | 计算合计 | 在延迟折扣计算时，此操作启动当前交易记录的计算。 | 是 | 是 | 无 | 是 | 无 |
| 642 | 完成所有产品 | 将所有行的交货方式设置为 **Carryout**。 | 是 | 是 | 无 | 是\* | 无 |
| 641 | 完成所选产品 | 将所选行的交货方式设置为 **Carryout**。 | 是 | 是 | 无 | 是\* | 无 |
| 1215 | 更改密码 | 此操作允许 POS 用户更改其密码。 | 是 | 是 | 是 | 无 | 无 |
| 123 | 更改度量单位 | 无法为所选行物料更改度量单位。 | 是 | 是 | 无 | 是 | 无 |
| 639 | 清除交易记录上的默认销售代表 | 从交易记录中删除佣金销售代表组（销售代表）。 | 是 | 是 | 无 | 是 | 无 |
| 106 | 清除数量 | 将当前所选行上的数量设置为 **1**。 | 是 | 是 | 无 | 是 | 无 |
| 640 | 清除行上的销售代表 | 从当前选择的行中删除佣金销售代表组（销售代表）。 | 是 | 是 | 无 | 是 | 无 |
| 121 | 清除销售人员 | 此操作不受支持。 | 不适用 | 不适用 | 不适用 | 不适用 | 无 |
| 1055 | 结束班次 | 关闭当前班次，打印 Z 报表，并将用户从系统中退出。 | 是 | 是 | 是 | 否 | 否 |
| 139 | 结束交易记录 | 提示用户选择付款方式 | 是 | 是 | 否 | 是 | 否 |
| 620 | 创建客户订单 | 将 POS 交易记录转换为客户订单。 | 是 | 是 | 否 | 是\* | 否 |
| 925 | 复制银行支票 | 此操作不受支持。 | 不适用 | 不适用 | 不适用 | 不适用 | 是 |
| 620 | 创建客户订单 | 将 POS 交易记录转换为客户订单。 | 是 | 是 | 无 | 是\* | 无 |
| 621 | 创建报价 | 将 POS 交易记录转换为销售报价单。 | 是 | 是 | 无 | 是\* | 无 |
| 636 | 创建零售交易记录 | 在默认 POS 行为是创建客户订单时，此操作允许用户创建标准销售交易记录。 | 是 | 是 | 无 | 是 | 无 |
| 600 | 客户 | 将指定客户添加到交易记录。 | 无 | 无 | 无 | 是 | 无 |
| 1100 | 客户帐户保证金 | 向客户的帐户付款。 | 是 | 是 | 是 | 是 | 是 |
| 612 | 添加客户 | 此操作允许用户创建新的客户记录。 | 是 | 是 | 是 | 是† | 无 |
| 603 | 清除客户 | 将客户从当前交易记录中删除。 | 是 | 是 | 无 | 是 | 无 |
| 602 | 客户搜索 | 此操作允许用户通过导航到 POS 中的客户搜索页来搜索客户记录。 | 是 | 是 | 是 | 是 | 无 |
| 609 | 客户交易记录 | 此操作不受支持。 | 不适用 | 不适用 | 不适用 | 不适用 | 无 |
| 917 | 数据库连接状态 | 此操作允许用户查看当前的连接设置，并可在联机和脱机模式之间切换。 | 是 | 是 | 是 | 是 | 无 |
| 1200 | 声明初始金额 | 一天或一个班次开始时声明银箱中的金额。 | 是 | 是 | 是 | 是 | 无 |
| 132 | 保证金覆盖 | 覆盖客户订单的默认存款。 | 是 | 是 | 无 | 是\* | 无 |
| 913 | 禁用设计模式 | 此操作不受支持。 | 不适用 | 不适用 | 不适用 | 不适用 | 无 |
| 912 | 启用设计模式 | 此操作不受支持。 | 不适用 | 不适用 | 不适用 | 不适用 | 无 |
| 1217 | 拆卸配套件 | 将套件拆卸成其各个部件产品。 | 是 | 是 | 是 | 是 | 无 |
| 624 | 显示退款金额 | 此操作不受支持。 | 不适用 | 不适用 | 不适用 | 不适用 | 是 |
| 513 | 显示合计 | 在客户显示窗口中显示交易记录的余额。 | 是 | 是 | 是 | 是 | 无 |
| 623 | 编辑客户 | 编辑当前客户的详细信息。 | 是 | 是 | 无 | 无 | 无 |
| 614 | 编辑客户订单 | 撤回所选订单，以便可以在 POS 中修改。 | 无 | 无 | 无 | 无 | 无 |
| 615 | 编辑报价单 | 撤回所选报价单，以便可以在 POS 中修改。 | 无 | 无 | 无 | 无 | 无 |
| 518 | 支出帐户 | 记录从银箱中取出以用作偶尔支出的金额。 | 是 | 是 | 是 | 是 | 无 |
| 919 | 扩展登录 | 通过扫描条码或通过刷卡分配或取消登录权限。 | 是 | 是 | 是 | 是 | 否 |
| 1201 | 浮动条目 | 此操作允许用户将额外金钱添加到当前银箱或班次。 | 是 | 是 | 是 | 是 | 无 |
| 1218 | 强制解锁外围设备 | 系统内部使用此操作来解锁 POS 外设。 | 不适用 | 不适用 | 不适用 | 不适用 | 无 |
| 520 | 礼品卡余额 | 显示礼品卡余额。 | 是 | 是 | 无 | 无 | 无 |
| 708 | 停用设备 | 停用当前设备，以使它不能用作 POS 收银机。 | 无 | 无 | 无 | 无 | 无 |
| 517 | 收入帐户 | 记录一个人不是销售放入银箱的金额。 | 是 | 是 | 是 | 是 | 无 |
| 801 | 库存查找 | 查看当前商店和其他可用位置订单上的可用和可承诺 (ATP) 的数量。 | 是 | 是 | 是 | 无 | 无 |
| 122 | 发票注释 | 此操作允许用户输入有关当前交易记录的注释。 | 是 | 是 | 无 | 是 | 无 |
| 511 | 签发贷项通知单 | 签发贷项通知单以提供凭证而不是退款。 | 是 | 是 | 无 | 无 | 无 |
| 512 | 签发礼品卡 | 签发指定金额的新礼品卡。 | 是 | 是 | 无 | 无 | 无 |
| 625 | 签发会员卡 | 向客户签发会员卡，以便客户可以参与该商店的会员计划。 | 是 | 是 | 是 | 无 | 无 |
| 300 | 单行折扣金额 | 输入交易记录中某行物料的折扣金额。 此操作只能用于可打折的物料和在指定的折扣限制中。 | 是 | 是 | 无 | 是 | 无 |
| 301 | 单行折扣百分比 | 输入交易记录中某行物料的折扣百分比。 此操作只能用于可打折的物料和在指定的折扣限制中。 | 是 | 是 | 无 | 是 | 无 |
| 703 | 锁定收银机 | 锁定当前收银机，以使其不能使用，但将当前用户退出。 | 无 | 无 | 无 | 是 | 无 |
| 701 | 注销 | 将当前用户退出收银机。 | 是 | 是 | 是 | 是 | 无 |
| 521 | 会员卡积分余额 | 显示指定会员卡的积分余额。 | 是 | 是 | 无 | 无 | 无 |
| 918 | 管理班次 | 显示活动、暂停和直接结束的班次列表。 | 是 | 是 | 是 | 无 | 无 |
| 914 | POS 窗口最小化 | 此操作不受支持。 | 不适用 | 不适用 | 不适用 | 不适用 | 无 |
| 1000 | 开银箱 | 执行“无销售”操作，并打开当前所选的银箱。 | 是 | 是 | 是 | 是 | 无 |
| 928 | 订单履行状况 | 此操作允许用户领取、包装、装运或撤回用于商店提货的订单。 | 是 | 是 | 是 | 无 | 无 |
| 129 | 覆盖行产品税 | 覆盖所选行项上的税，并使用其他指定税。 | 是 | 是 | 无 | 是 | 无 |
| 130 | 覆盖列表中的行产品税 | 使用用户在列表中所选的税覆盖所选行项目上的销项税。 | 是 | 是 | 无 | 是 | 无 |
| 127 | 覆盖交易税 | 覆盖交易记录上的税，并使用不同的指定税。 | 是 | 是 | 无 | 是 | 无 |
| 128 | 覆盖列表中的交易税 | 使用用户在列表中所选的税覆盖交易记录上的销项税。 | 是 | 是 | 无 | 是 | 无 |
| 131 | 装箱单 | 创建所选订单的装箱单。 | 无 | 无 | 无 | 无 | 无 |
| 710 | 配对硬件工作站 | 此操作不受支持。 | 不适用 | 不适用 | 不适用 | 不适用 | 无 |
| 201 | 卡支付 | 接受信用卡或借记卡等卡作为支付方式。 | 是 | 是 | 无 | 是 | 无 |
| 200 | 现金支付 | 接受现金支付方式。 | 是 | 是 | 无 | 是 | 无 |
| 206 | 快汇支付 | 轻触一下完成交易，并接受到期的现金金额（确切更改）。 | 是 | 是 | 无 | 是 | 无 |
| 204 | 支票支付 | 接受用支票支付方式。 | 是 | 是 | 无 | 是 | 无 |
| 213 | 贷项通知单支付 | 接受商店签发的贷项通知单（凭证）。 | 是 | 是 | 无 | 无 | 无 |
| 203 | 支付币种 | 接受用各种币种进行的支付。 | 是 | 是 | 无 | 是 | 无 |
| 202 | 客户帐户支付 | 向客户的帐户收取交易费用。 此付款方式对于客户订单订金无效。 | 是 | 是 | 无 | 无 | 无 |
| 214 | 礼品卡支付 | 接受商店签发的礼品卡。 | 是 | 是 | 无 | 无 | 无 |
| 207 | 支付会员卡 | 接受会员卡用于付款，并兑换合格产品获得的积分。 | 是 | 是 | 无 | 无 | 无 |
| 634 | 付款历史记录 | 查看当前客户订单的客户付款历史记录。 | 是 | 是 | 无 | 无 | 无 |
| 803 | 领料和接收 | 打开**领料和收货**页，从中可以选择在商店中领取或接收的订单。 | 是 | 是 | 是 | 无 | 无 |
| 632 | 拣选所有产品 | 将所有行的履行方法均设置为**商店提货**。 | 是 | 是 | 无 | 是\* | 无 |
| 631 | 拣选所选产品 | 将所选行的履行方法设置为**商店提货**。 | 是 | 是 | 无 | 是\* | 无 |
| 400 | 弹出式菜单 | 此操作不受支持。 | 不适用 | 不适用 | 不适用 | 不适用 | 无 |
| 101 | 价格查询 | 此操作允许用户查找特定产品的价格。 | 是 | 是 | 是 | 是 | 无 |
| 104 | 价格覆盖 | 如果已将产品设置为允许价格覆盖，则覆盖产品的价格。 | 是 | 是 | 无 | 是 | 无 |
| 1058 | 打印会计 X | 此操作不受支持。 | 不适用 | 不适用 | 不适用 | 不适用 | 是 |
| 1059 | 打印会计 Z | 此操作不受支持。 | 不适用 | 不适用 | 不适用 | 不适用 | 是 |
| 927 | 打印物料标签 | 此操作不受支持。 | 不适用 | 不适用 | 不适用 | 不适用 | 无 |
| 926 | 打印货位标签 | 此操作不受支持。 | 不适用 | 不适用 | 不适用 | 不适用 | 无 |
| 1056 | 打印 X | 打印当前班次的 X 报表。 | 是 | 是 | 是 | 无 | 无 |
| 103 | 产品注释 | 将注释添加到交易记录中的所选行项。 | 是 | 是 | 无 | 是 | 无 |
| 100 | 产品销售 | 将指定产品添加到交易记录。 | 是 | 是 | 是 | 是 | 无 |
| 108 | 产品搜索 | 此操作允许用户通过导航到 POS 中的产品搜索页来搜索产品。 | 是 | 是 | 是 | 是 | 无 |
| 633 | 报价到期日期 | 此操作允许用户查看或修改销售报价单的到期日期。 | 是 | 是 | 无 | 是\* | 无 |
| 627 | 重新计算 | 基于当前配置重新计算所有客户订单行和税。 | 是 | 是 | 无 | 是\* | 无 |
| 515 | 撤回订单 | 此操作允许用户搜索和撤回客户订单和销售报价单。 | 是 | 是 | 是 | 无 | 无 |
| 504 | 撤回交易记录 | 此操作允许用户撤回当前商店以前暂停的交易。 | 是 | 是 | 无 | 是‡ | 无 |
| 305 | 兑换会员积分 | 此操作不受支持。 | 不适用 | 不适用 | 不适用 | 不适用 | 是 |
| 635 | 退回装运费用 | 此操作允许用户退还取消订单的装运费用。 | 无 | 无 | 无 | 无 | 无 |
| 644 | 删除优惠券代码 | 提示用户通过在当前与交易关联的优惠券列表中选中优惠券来将其删除。 | 是 | 是 | 无 | 是 | 无 |
| 1057 | 重印 Z | 重新打印上一个班次或所选班次的 Z 报表。 | 是 | 是 | 是 | 无 | 无 |
| 1216 | 请输入一个新密码 | 此操作允许具有重置密码权限的用户通过使用临时密码重置其他员工的密码。 | 是 | 是 | 是 | 无 | 无 |
| 1219 | 在 POS 中打开 URL | 此操作让用户可以在 POS 中打开管理员配置的 URL。 | 是 | 是 | 是 | 是 | 无 | 
| 109 | 退回产品 | 执行单独的产品退货。 将下一个扫描的产品作为带负数数量和价格的退回产品显示。 | 是 | 是 | 无 | 是 | 无 |
| 114 | 退货交易记录 | 按收据编号撤回以前的交易以退回部分或全部产品。 | 是 | 是 | 是 | 是§ | 无 |
| 1211 | 金库投箱 | 执行金库投箱以将钱币从收银机移到保险箱。 | 是 | 是 | 是 | 是 | 无 |
| 516 | 销售发票 | 此操作允许客户为选择的销售发票付款。 | 是 | 是 | 无 | 无 | 无 |
| 502 | 销售人员 | 此操作允许用户为 POS 中的客户订单设置销售订单上的**销售处理人员**值。 | 是 | 是 | 无 | 是\* | 无 |
| 2000 | 计划管理 | 此操作允许用户创建、修改或查看员工计划。 | 是 | 是 | 是 | 无 | 无 |
| 2001 | 计划请求 | 此操作允许用户请求休假、交换班次或提议由其他员工接替班次。 | 是 | 是 | 是 | 无 | 无 |
| 622 | 搜索订单 | 此操作允许用户预先配置 POS 按钮以按物料、客户或类别进行搜索。 | 是 | 是 | 是 | 是 | 无 |
| 1213 | 搜索装运地址 | 此操作不受支持。 | 不适用 | 不适用 | 不适用 | 不适用 | 无 |
| 709 | 选择硬件工作站 | 此操作允许用户选择可用硬件工作站列表中的硬件工作站。 | 是 | 是 | 是 | 是 | 无 |
| 637 | 设置交易记录上的默认销售代表 | 此操作允许用户选择一个合格的佣金销售代表组（销售代表）作为以后添加的行的默认销售代表。 | 是 | 是 | 无 | 是 | 无 |
| 105 | 设置数量 | 更改交易记录中某行物料的数量。 | 是 | 是 | 无 | 是 | 无 |
| 638 | 设置行上的销售代表 | 此操作允许用户为当前所选的行选择一个合格的佣金销售代表组（销售代表）。 | 是 | 是 | 无 | 是 | 无 |
| 630 | 装运所有产品 | 将所有行项的履行模式设置为**装运**。 | 是 | 是 | 无 | 是\* | 无 |
| 629 | 装运所选产品 | 将所选行的履行模式设置为**装运**。 | 是 | 是 | 无 | 是\* | 无 |
| 115 | 显示日记帐 | 显示商店的日记帐。 您可以查看交易记录、重新打印收据和礼品收据、撤销退货。 | 是 | 是 | 是 | 是\*\* | 无 |
| 802 | 存货盘点 | 此操作允许用户创建或修改实际库存或周期盘点的库存盘点日记帐。 | 是 | 是 | 是 | 无 | 无 |
| 401 | 子菜单 | 此操作将用户带到其他链接的按钮网格。 | 是 | 是 | 是 | 是 | 无 |
| 1054 | 暂停班次 | 暂停当前班次，以便新的或其他班次可以在当前收银机上启用。 | 是 | 是 | 是 | 无 | 无 |
| 503 | 暂停交易 | 暂停当前销售交易，以便其以后可以在商店中撤回。 | 是 | 是 | 无 | 是‡ | 无 |
| 1004 | 任务录制器 | 打开任务录制器以在 POS 中记录过程步骤。 | 无 | 无 | 无 | 是 | 无 |
| 1052 | 钱币清点 | 此操作允许用户为每个确认的付款方式指定银箱中的金额。 | 是 | 是 | 是 | 是 | 无 |
| 1210 | 取钱 | 此操作允许用户将金钱从当前银箱或班次中删除。 | 是 | 是 | 是 | 是 | 无 |
| 920 | 打卡时间 | 此操作允许用户执行工作班次和休息的上班打卡和下班打卡操作。 | 是 | 是 | 是 | 无 | 无 |
| 302 | 总折扣金额 | 输入交易记录的折扣金额。 此操作只适用于可打折的物料，且在指定的折扣限制中使用。 | 是 | 是 | 无 | 是 | 无 |
| 303 | 总折扣百分比 | 输入交易记录的折扣百分比。 此操作只适用于可打折的物料，且在指定的折扣限制中使用。 | 是 | 是 | 无 | 是 | 无 |
| 501 | 交易注释 | 将注释添加到当前交易记录。 | 是 | 是 | 无 | 是 | 无 |
| 922 | 查看产品详细信息 | 打开当前所选行项的产品详细信息页。 | 是 | 是 | 无 | 是 | 无 |
| 1003 | 查看报表 | 显示为当前用户配置的报表。 | 是 | 是 | 是 | 无 | 无 |
| 921 | 查看打卡时间条目 | 显示商店中所有工作人员的打卡时间条目。 | 是 | 是 | 是 | 无 | 无 |
| 211 | 使付款无效 | 从交易记录中取消当前选择的付款行。 | 是 | 是 | 无 | 是 | 无 |
| 102 | 取消产品 | 从交易记录中取消当前选择的行项。 | 是 | 是 | 无 | 是 | 无 |
| 500 | 取消交易 | 取消当前交易记录。 | 是 | 是 | 无 | 是 | 无 |
| 916 | Windows Workflow Foundation | 此操作不受支持。 | 不适用 | 不适用 | 不适用 | 不适用 | 无 |
| 924 | 银行卡 X 报表 | 此操作不受支持。 | 不适用 | 不适用 | 不适用 | 不适用 | 是 |

\*只有当客户订单或销售报价单正在创建，并且在 POS 功能配置文件中配置了脱机创建客户订单和销售报价单时，此操作才可在脱机模式下使用。 当订单使用 Real-time Service 创建，或者订单撤回或编辑时，无法执行此操作。

† 只有当 POS 在 POS 功能配置文件中配置为允许客户脱机创建的情况下，此操作才可以在脱机模式下执行。

‡ 在 POS 脱机时，封存的交易记录只能从当前收银机的脱机数据库中撤回。 用户不能跨各个收银机封存和撤回交易记录。

§ 在 POS 脱机时，仅当前脱机数据库中的交易记录可以因为退货撤回。

\*\* 在 POS 脱机时，仅当前脱机渠道数据库中的交易记录在日记帐中显示。

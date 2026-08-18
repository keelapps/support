# 最终用户条款（EULA）决策 —— keelapps 全产品线

keelapps 有两条产品线，法律路径完全不同，不能互相套用：

| 产品线 | 销售渠道 | EULA | 状态 |
| --- | --- | --- | --- |
| 5 个 Atlassian Cloud 应用 | Atlassian Marketplace | Bonterms v1.0（标准协议） | 已决策，见第 1–6 节 |
| Keelhaven（macOS） | 直销 | 需自建 | **待决，见第 7 节** |

---

# 第一部分：Atlassian Cloud 应用

> 结论先行：**5 个 app 全部采用 Atlassian 官方标准最终用户协议
> （Bonterms Standard End User Agreement v1.0），不加自定义条款。**
> 这是法律上最省事、商业上最合理的做法，理由如下。

## 1. 采用什么

Atlassian 为 Marketplace 交易提供官方标准协议：
[Bonterms Standard End User Agreement (Version 1.0)](https://www.atlassian.com/licensing/marketplace/end-user-agreement-v1)

- 它在 Marketplace 商店页的 **End User Agreement** 字段里直接挂链接即可，
  不需要你自建 TOS 页面。
- 协议允许供应商加 **Provider-Specific Terms**（附加条款），但**不建议加**：
  每加一条自定义条款，就多一个被买家法务挑刺、被 Atlassian 审核打回的点。

## 2. 为什么不加自定义条款

Bonterms v1.0 已经覆盖了独立软件供应商需要的一切，而且对供应商相当友好：

| 条款 | 内容 | 对 keelapps 的影响 |
| --- | --- | --- |
| §3.1 客户数据使用 | 供应商仅为提供产品而访问/使用客户数据 | 我们的 app 零出网、不接触客户数据，实际风险趋近于零 |
| §6.2 性能保证 | 产品与文档描述一致，30 天内报告违约 | 与我们的验收标准一致，无需额外承诺 |
| §12.4 数据导出与删除 | 终止后 60 天内删除客户数据 | Forge 存储随卸载清除，天然满足 |
| §14 责任限制 | 总责任上限 = 前 12 个月实付费用；间接损害免责 | 标准保护 |
| §15 知识产权赔偿 | 供应商为侵权主张辩护 | 我们无自有 IP 风险（纯 Forge 开发） |

**唯一值得考虑的自定义项**：支持承诺（Support Policy，§5.1 引用）。建议在
商店页 Support 链接里写明响应时间（见下文），而不是写进法律条款。

## 3. 每个 app 的操作（上架时 5 分钟）

在 Marketplace 后台创建商店页时：

1. **End User Agreement** 字段 → 粘贴 Bonterms v1.0 的 URL
   （`https://www.atlassian.com/licensing/marketplace/end-user-agreement-v1`）。
   后台如果提供"采用标准协议"勾选项，直接勾选。
2. **Privacy policy** 字段 → 各 app 已发布的隐私政策 URL
   （见各仓库 `docs/privacy-policy.md`）。
3. **Support 链接** → 支持邮箱 + 响应承诺：
   - 工作日 24 小时内首次回复
   - 严重问题（数据丢失、应用不可用）优先处理
4. **Documentation 链接** → 各 app 仓库的 README（或后续的托管文档页）。

## 4. DPA（数据处理协议）决策

**结论：keelapps 不单独签署 DPA，指向 Atlassian 的 DPA 即可。**

理由（已写入每个 app 的隐私政策"DPA 说明"段）：

- GDPR 下的数据处理者是指**决定处理目的和方式之外**、代表控制者处理个人数据的
  一方。我们的 5 个 app 全部：零出网（manifest 无 `external` 权限，Forge 平台层
  强制）、供应商不接触/不存储/不传输任何客户数据、数据全部留在客户自己的
  Atlassian 租户内。
- 数据只在"客户 ↔ Atlassian（作为基础设施提供方）"之间流动。供应商不参与
  处理，因而不是数据处理者，无需单独 DPA。
- 若个别客户的合规团队仍要求书面 DPA（例如保险或金融行业客户的采购流程
  硬性要求），采用 Atlassian 的标准 DPA 即可 —— 因为所有处理由 Atlassian
  完成，Atlassian 的 DPA 覆盖了实际的处理活动。

## 5. 与 Atlassian 的合同关系

上架前需要完成（无捷径、无法自动化）：

1. **Marketplace 合作伙伴协议**：注册为 Atlassian Marketplace Partner 时
   在线接受（需法律实体 + 收款信息）。
2. **Atlassian Developer Terms**：开发时已隐含接受；上架前确认账号合规。

## 6. 责任与保险（提示，非必需）

Bonterms §14 把责任上限压到"实付费用"，对独立开发者足够。若未来某个 app
进入金融/医疗等敏感行业，再评估专业责任保险（E&O insurance）—— 现在不需要。

---

# 第二部分：Keelhaven（macOS）

## 7. 为什么第一部分整体不适用

Bonterms v1.0 是 Atlassian 为 **Marketplace 交易**提供的协议，它假定
Atlassian 是收款方、是基础设施提供方、是争议处理通道。Keelhaven 直销，这三条
全部不成立，所以不能沿用 —— 需要自己的最终用户条款。

同样不能沿用的还有第 4 节的 DPA 论证。结论碰巧一致（我们不是 GDPR 意义上的
数据处理者），但**理由完全不同**，不能照抄：

- Atlassian 线：Forge 平台强制零出网，数据留在客户租户内；
- Keelhaven：我们**根本没有接收端**。没有账号系统、没有遥测、没有我们的服务器。
  备份从用户的 Mac 直接写入用户自己的存储（本地盘 / NAS / 自有 S3 桶），加密在
  离开机器之前完成。我们不在数据路径上，因此无从处理。

唯一实际接触到个人数据的环节是**支持邮件**：`support@keelhaven.app` 经
Cloudflare Email Routing 转发到我们读的邮箱。这一段我们是数据控制者（controller）
而非处理者，处理范围仅限对方主动写给我们的内容，已在
<https://keelhaven.app/privacy> 中写明。

## 8. 上架销售前必须决定的三件事

按依赖顺序排列 —— 第 2 项会反过来约束第 1 和第 3 项，先定它。

**1）最终用户条款（EULA）本身。**
需要落到条款的实质承诺，网站上已经公开说了，条款不能与之矛盾：

- "One-time purchase at 1.0 — bought once, updates forever, never a subscription."
  —— *updates forever* 是一个很强的永久承诺。多数同类产品的做法是"买断当前
  大版本 + N 年更新"。要么在条款里明确兑现它，要么在开卖前改网站文案。**两者
  必须一致，这是目前最大的敞口。**
- 备份软件的责任限制条款（数据丢失场景）。
- 忘记 repository password 即数据不可恢复 —— 网站 FAQ 已声明，条款应呼应。

**2）支付渠道，以及由此决定的 merchant of record。**
这不只是选支付工具，它决定谁承担增值税/销售税义务：

- **用 Paddle / Lemon Squeezy 这类 merchant of record**：它们作为法律上的卖方
  代收代缴各国 VAT/GST/销售税，独立开发者通常选这条；
- **用 Stripe 直连**：keelapps 自己是卖方，欧盟 VAT、英国 VAT、美国各州销售税
  的登记与申报义务全部落在自己身上。

**3）退款政策。** 数字商品在欧盟有 14 天撤回权，以及可放弃该权利的条件。选定
渠道后按渠道要求写。

## 9. 已完成的部分

- 隐私政策：已发布 <https://keelhaven.app/privacy>；
- 开源合规：Keelhaven 分发 restic 二进制，BSD 2-Clause 声明随应用包内
  （`Contents/Resources/restic-LICENSE.txt`，About 窗口可见）并镜像在
  <https://keelhaven.app/licenses>；商标免责声明同页；
- 支持渠道：`support@keelhaven.app`，以及本仓库。

---

## 各 app 状态速查

| App | EULA | 隐私政策 | 支持邮箱 | 备注 |
| --- | --- | --- | --- | --- |
| AccessLens | 标准 Bonterms | `docs/privacy-policy.md` 待发布 | 待建 | 审计类，买家可能主动要 DPA —— 用 Atlassian 标准模板 |
| Digest | 标准 Bonterms | `docs/privacy-policy.md` 待发布 | 待建 | — |
| Evergreen | 标准 Bonterms | `docs/PRIVACY.md` 待发布 | 待建 | — |
| Mail Templates | 标准 Bonterms | `docs/privacy-policy.md` 待发布 | 待建 | 通知类，买家会问发件人身份 —— 隐私政策已写明走 Jira `/notify` |
| Recur | 标准 Bonterms | `docs/privacy-policy.md` 待发布 | 待建 | — |
| **Keelhaven** | **待建（不适用 Bonterms）** | 已发布 `keelhaven.app/privacy` | `support@keelhaven.app` | 直销；支付渠道与退款政策待定，见第 8 节 |

## 参考来源

- [Atlassian 标准最终用户协议（Bonterms v1.0）](https://www.atlassian.com/licensing/marketplace/end-user-agreement-v1)
- [Adopt the customizable end-user agreement（Atlassian 文档）](https://developer.atlassian.com/platform/marketplace/list-customizable-end-user-agreement)
- [Data privacy guidelines for developers](https://developer.atlassian.com/platform/marketplace/data-privacy-guidelines/)
- [Standard contractual clauses and cross-border transfers](https://developer.atlassian.com/platform/marketplace/standard-contractual-clauses-and-cross-border-transfers/)

# 最终用户条款（EULA）决策 —— keelapps 全产品线

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

## 各 app 状态速查

| App | EULA | 隐私政策 | 支持邮箱 | 备注 |
| --- | --- | --- | --- | --- |
| AccessLens | 标准 Bonterms | `docs/privacy-policy.md` 待发布 | 待建 | 审计类，买家可能主动要 DPA —— 用 Atlassian 标准模板 |
| Digest | 标准 Bonterms | `docs/privacy-policy.md` 待发布 | 待建 | — |
| Evergreen | 标准 Bonterms | `docs/PRIVACY.md` 待发布 | 待建 | — |
| Mail Templates | 标准 Bonterms | `docs/privacy-policy.md` 待发布 | 待建 | 通知类，买家会问发件人身份 —— 隐私政策已写明走 Jira `/notify` |
| Recur | 标准 Bonterms | `docs/privacy-policy.md` 待发布 | 待建 | — |

## 参考来源

- [Atlassian 标准最终用户协议（Bonterms v1.0）](https://www.atlassian.com/licensing/marketplace/end-user-agreement-v1)
- [Adopt the customizable end-user agreement（Atlassian 文档）](https://developer.atlassian.com/platform/marketplace/list-customizable-end-user-agreement)
- [Data privacy guidelines for developers](https://developer.atlassian.com/platform/marketplace/data-privacy-guidelines/)
- [Standard contractual clauses and cross-border transfers](https://developer.atlassian.com/platform/marketplace/standard-contractual-clauses-and-cross-border-transfers/)

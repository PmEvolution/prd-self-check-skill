# prd-self-check

把「PRD 自查清单」沉淀成会自己挑刺的 AI skill。

给一份 PRD，按 **7 个维度**逐项扫描，输出「已覆盖 / 待补充 / 不适用」缺口表，并标注高风险项。方法论来自「产品进化论」PRD 自查系列 01–07，已全部沉淀在本仓库 `references/` 中。

## 七维扫描框架

| 维度 | 关注点 | 来源 |
|------|--------|------|
| 01 整体完整性 | 背景/目标/范围/流程/规则/验收是否齐 | 合格 PRD 应包含哪些内容 |
| 02 异常流程 | 14 类异常 + 失败回滚/幂等/限额 | PRD 异常流程自检清单 |
| 03 页面状态 | 空态/加载/错误/置灰/终态 | PRD 页面状态自查清单 |
| 04 正常流程 | 入口→节点→跳转→结果是否走通 | PRD 正常流程自查清单 |
| 05 交互 | 反馈/防误/记忆/撤销/边界 | 交互自查清单 |
| 06 消息通知 | 触发/渠道/时机/内容/兜底 | 消息通知自查清单 |
| 07 权限 | 角色/数据范围/未授权/越权 | 权限自查清单 |

## 安装

把本目录放到 WorkBuddy 的 skills 目录下：

```bash
git clone https://github.com/PmEvolution/prd-self-check-skill.git \
  ~/.workbuddy/skills/prd-self-check
```

（路径不存在就先 `mkdir -p ~/.workbuddy/skills`）

## 使用

把 PRD 丢给助手，加一句「审一下 / 自查 / 查漏」，即按 01–07 出缺口表。

实测案例（《提现 PRD》）：抓出 3 个真缺口 —— 验收标准缺失、提现受理后撤销未定义、目标未量化。

## 结构

```
prd-self-check/
├── SKILL.md            # 触发词、扫描流程、输出格式
└── references/
    ├── 01-completeness.md
    ├── 02-anomaly.md
    ├── 03-page-state.md
    ├── 04-normal-flow.md
    ├── 05-interaction.md
    ├── 06-notification.md
    └── 07-permission.md
```

## License

MIT

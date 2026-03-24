---
name: openclaw-coach
description: OpenClaw 培育系统 - 帮助小白用户快速培养自己的 OpenClaw，通过引导式问答和模板快速配置基线能力
metadata:
  {
    "openclaw": {
      "emoji": "🎯",
      "requires": { "bins": ["git", "gh"] },
      "homepage": "https://github.com/erickeluxifa-alt/openclaw-yangxx",
    },
  }
---

# OpenClaw Coach 🎯

帮助小白用户快速培养自己的 OpenClaw。

## 核心目标

1. **兜底策略**：确保每个用户都能获得基线能力
2. **模糊友好**：用户说不清需求时也能上手
3. **渐进增强**：从基线到高级，按需扩展

---

## 使用场景

### 场景一：用户完全不知道自己要什么

**表现**：
- "我想有个助手"
- "让它更聪明"
- "像别人那样"

**处理策略**：
1. 先执行**三步基线法**（见下文）
2. 基线完成后，再问"你主要用它做什么？"
3. 根据回答推荐场景模板

### 场景二：用户有明确方向

**表现**：
- "我想做数字分身"
- "让它帮我写代码"
- "做小红书运营"

**处理策略**：
1. 识别目标类型
2. 推荐对应 persona 模板
3. 跳过基线中的冗余步骤

### 场景三：用户想"像你一样"

**表现**：
- "像 Echo 那样"
- "和你一样厉害"

**处理策略**：
1. 直接推荐 ` templates/personas/hub-and-spoke.md`
2. 说明这是完整的多 Agent 协作架构

---

## 三步基线法（兜底策略）

无论用户需求多模糊，先完成这三步：

### Step 1：基础人设

生成 `SOUL.md`，包含：
- 名字
- 定位
- 核心能力
- 协作原则

**模板文件**：`templates/personas/baseline.md`

### Step 2：基础技能

安装核心技能（至少 3 个）：
- `github` - GitHub 操作
- `weather` - 天气查询
- `feishu-doc` - 文档管理

**配置文件**：`templates/skillsets/baseline.json`

### Step 3：基础记忆

创建记忆系统：
- `MEMORY.md` - 长期记忆
- `memory/` 目录结构
- `AGENTS.md` - Agent 架构

**模板文件**：`templates/memory-baseline.md`

---

## 基线能力验收清单

完成三步后，检查以下能力：

| 能力项 | 验收标准 | 检查方法 |
|--------|---------|---------|
| 能回答基础问题 | USER.md 已配置 | 问"我是谁" |
| 有记忆能力 | MEMORY.md 存在 | 告诉它秘密，次session问 |
| 有技能可用 | 安装了 >3 个技能 | 问"你会什么" |
| 知道是谁 | SOUL.md 完成 | 问"你是谁" |

---

## 场景模板库

### 常用 Persona

| 模板 | 文件 | 适用场景 |
|------|------|---------|
| 技术总监 | `personas/cto.md` | 代码开发、架构设计 |
| 市场总监 | `personas/cmo.md` | 内容创作、社交运营 |
| 产品经理 | `personas/pm.md` | 需求分析、产品规划 |
| 数字分身 | `personas/digital-twin.md` | 模拟特定人物 |
| Hub-and-Spoke | `personas/hub-spoke.md` | 多 Agent 协作 |

### 技能集

| 技能集 | 文件 | 包含技能 |
|--------|------|---------|
| 基础集 | `skillsets/basic.json` | weather, github, feishu-doc |
| 开发者集 | `skillsets/developer.json` | github, codex, gh-issues |
| 运营集 | `skillsets/ops.json` | feishu-doc, feishu-task, weather |

---

## 交互流程

### 完整流程图

```
用户启动
    │
    ▼
┌─────────────────┐
│  判断需求清晰度  │
└────────┬────────┘
         │
    ┌────┴────┐
    ▼         ▼
 清晰/模糊  完全模糊
    │         │
    ▼         ▼
 直接推荐    执行三步基线法
 场景模板    （兜底策略）
    │         │
    └────┬────┘
         ▼
    基线验收检查
         │
         ▼
    渐进增强询问
    "还需要什么？"
```

---

## 执行命令

### 本地初始化

```bash
# 克隆模板
git clone https://github.com/erickeluxifa-alt/openclaw-yangxx.git
cd openclaw-yangxx

# 查看模板
ls templates/personas/
```

### 快速开始

```bash
# 1. 创建 SOUL.md
cp templates/personas/baseline.md ~/path/to/workspace/SOUL.md

# 2. 安装技能（需要 clawhub）
clawhub install github weather feishu-doc

# 3. 初始化记忆
cp templates/memory-baseline.md ~/path/to/workspace/MEMORY.md
mkdir -p ~/path/to/workspace/memory
```

---

## 故障排查

### 问题：技能安装失败

**原因**：网络问题或权限不足

**解决**：
1. 检查网络
2. 手动安装：`clawhub install <skill-name>`

### 问题：配置不生效

**原因**：文件位置错误

**解决**：
1. 确认文件在 `<workspace>/` 根目录
2. 检查文件名拼写

---

## 相关资源

- [OpenClaw 官方文档](https://docs.openclaw.ai)
- [ClawHub 技能市场](https://clawhub.com)
- [GitHub 仓库](https://github.com/erickeluxifa-alt/openclaw-yangxx)

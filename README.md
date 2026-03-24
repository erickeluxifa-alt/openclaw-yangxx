# OpenClaw Coach 🎯

> 帮助小白用户快速培养自己的 OpenClaw

[![GitHub stars](https://img.shields.io/github/stars/erickeluxifa-alt/openclaw-yangxx)](https://github.com/erickeluxifa-alt/openclaw-yangxx)
[![GitHub license](https://img.shields.io/github/license/erickeluxifa-alt/openclaw-yangxx)](https://github.com/erickeluxifa-alt/openclaw-yangxx)

## 是什么？

OpenClaw Coach 是一个帮助用户快速培养 OpenClaw 的培育系统。

**核心价值**：
- 🎯 兜底策略：确保每个用户都能获得基线能力
- 🤝 模糊友好：用户说不清需求时也能上手
- 📈 渐进增强：从基线到高级，按需扩展

## 快速开始

### 1. 克隆项目

```bash
git clone https://github.com/erickeluxifa-alt/openclaw-yangxx.git
cd openclaw-yangxx
```

### 2. 配置基线能力

```bash
# 复制基础人设模板
cp templates/personas/baseline.md ~/你的workspace路径/SOUL.md

# 复制记忆模板
cp templates/memory-baseline.md ~/你的workspace路径/MEMORY.md
```

### 3. 安装基础技能

```bash
# 需要先安装 clawhub
npm install -g clawhub

# 安装基础技能
clawhub install github weather feishu-doc
```

## 三步基线法

无论需求多模糊，先完成这三步：

| 步骤 | 操作 | 文件 |
|------|------|------|
| 第一步 | 基础人设 | `SOUL.md` |
| 第二步 | 基础技能 | 安装 3+ 个技能 |
| 第三步 | 基础记忆 | `MEMORY.md` |

## 模板库

### 人设模板

| 模板 | 描述 |
|------|------|
| `baseline.md` | 基础人设模板 |
| `hub-spoke.md` | Hub-and-Spoke 多智能体架构 |

### 技能集

| 模板 | 描述 |
|------|------|
| `baseline.json` | 基础技能集 |

## 基线验收

完成后检查：

- [ ] 能回答基础问题（USER.md 已配置）
- [ ] 有记忆能力（MEMORY.md 存在）
- [ ] 有技能可用（安装了 >3 个技能）
- [ ] 知道是谁（SOUL.md 完成）

## 文档

- [完整 SKILL.md](./SKILL.md) - 主技能定义
- [技术方案](./核心内容摘要.md) - 详细技术分析

## 贡献

欢迎提交 Issue 和 PR！

## 许可证

MIT

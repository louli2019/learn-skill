# 职业备考助手 / Vocational Exam Study Skill

基于 Claude Code 的职业备考学习助手，支持教师资格证、CPA、法考、建筑类证书等任意职业考试。

灵感来自 [CFP-Study](https://github.com/chenran818/CFP-Study)。

## 快速开始

```bash
# 1. 克隆仓库
git clone https://github.com/YOUR_NAME/learn-skill.git
cd learn-skill

# 2. 启动 Claude Code
claude

# 3. 初始化你的考试档案
/learn init
```

## 支持的命令

| 命令 | 用途 |
|------|------|
| `/learn init` | 初始化考试档案，生成考点追踪表 |
| `/learn 今天学什么` | 基于掌握度和间隔复习，推荐今日主题 |
| `/learn 测一测` | 出题检验，自动更新掌握度 |

## 文件结构

```
CLAUDE.md              # 核心：定义 AI 的教学行为
progress/
  tracker.md           # 考点掌握度地图（自动维护）
sessions/
  2026-05-27.md        # 每日学习日志（自动生成）
```

## 核心机制

- **苏格拉底式教学**：AI 先问你已知什么，再引导推导，不灌输
- **间隔复习调度**：掌握度越低复习越频繁（3/7/14 天循环）
- **状态持久化**：靠文件而非 AI 记忆，跨对话保持连续性
- **零配置**：克隆即用，不需要任何 API Key 或数据库

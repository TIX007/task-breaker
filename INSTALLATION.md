# Task Breaker Plugin - 安装和部署指南

## 📦 安装说明

### 前置要求

- CodeBuddy IDE 或兼容环境
- 无需额外软件或依赖

### 安装步骤

1. **确认插件位置**
   ```
   插件路径：.codebuddy/plugins/task-breaker/
   ```

2. **验证文件完整性**
   确保以下文件和目录存在：
   ```
   task-breaker/
   ├── plugin.json
   ├── README.md
   ├── LICENSE
   ├── QUICKSTART.md
   ├── EXAMPLES.md
   ├── PLUGIN_STRUCTURE.md
   ├── skills/
   │   └── task-breaker/
   │       └── SKILL.md
   ├── examples/
   │   └── task-breaker-examples.md
   └── templates/
       └── task-breakdown-template.md
   ```

3. **无需额外配置**
   插件配置已包含在 `plugin.json` 中，即插即用

---

## 🚀 使用方法

### 自动激活

当您的请求包含以下关键词时，插件会自动激活：

**中文触发词**：
- 拆分任务
- 分解任务
- 子任务
- 任务拆解
- 并行执行

**英文触发词**：
- break down task
- split task
- subtask
- task decomposition

### 手动激活

您也可以手动指定使用 Task Breaker：

```
"使用 Task Breaker 来：[您的任务描述]"
```

或

```
"帮我分解一下：[您的任务描述]"
```

---

## ✅ 验证安装

### 测试插件是否正常工作

发送以下测试请求：

```
"使用 Task Breaker 分解一个简单的任务：
研究3个国家的天气情况"
```

**预期响应**：
- 识别为广度优先任务
- 创建 3 个并行研究子任务
- 提供 1 个合成子任务
- 包含执行计划和时间估计

---

## 🔧 配置选项

### 插件默认配置

```json
{
  "settings": {
    "maxSubtasks": 20,
    "defaultParallelAgents": 3,
    "enableProgressTracking": true,
    "autoSynthesis": true
  }
}
```

### 配置说明

| 设置 | 默认值 | 说明 |
|------|--------|------|
| maxSubtasks | 20 | 最大子任务数量 |
| defaultParallelAgents | 3 | 默认并行代理数 |
| enableProgressTracking | true | 是否启用进度跟踪 |
| autoSynthesis | true | 是否自动合成结果 |

### 自定义配置

如需修改配置，编辑 `plugin.json` 中的 `settings` 部分。

---

## 📚 文档导航

| 文档 | 用途 |
|------|------|
| `README.md` | 完整的插件文档 |
| `QUICKSTART.md` | 快速入门指南 |
| `EXAMPLES.md` | 实际使用示例 |
| `PLUGIN_STRUCTURE.md` | 插件结构验证 |
| `skills/task-breaker/SKILL.md` | 完整技术文档 |
| `examples/task-breaker-examples.md` | 详细示例集合 |
| `templates/task-breakdown-template.md` | 任务分解模板 |

---

## 🎯 快速开始

### 第一步：了解基本概念

阅读 `QUICKSTART.md`（5 分钟）

### 第二步：查看实际示例

查看 `EXAMPLES.md`（10 分钟）

### 第三步：尝试使用

发送您的第一个任务分解请求

---

## ⚠️ 故障排除

### 问题 1：插件未激活

**症状**：请求任务分解，但没有得到预期的分解结果

**解决方案**：
1. 检查是否使用触发关键词
2. 尝试明确指定："使用 Task Breaker..."
3. 确认插件文件完整

### 问题 2：子任务数量不合理

**症状**：生成的子任务太多或太少

**解决方案**：
1. 明确指定子任务数量："最多5个子任务"
2. 调整任务描述的粒度

### 问题 3：执行时间超出预期

**症状**：任务执行时间比估计的长

**解决方案**：
1. 检查网络连接（涉及网络搜索）
2. 确认任务复杂度是否被低估
3. 考虑添加时间约束："在30分钟内完成"

---

## 📞 获取帮助

### 文档资源

1. **快速入门**：`QUICKSTART.md`
2. **完整文档**：`README.md`
3. **技术文档**：`skills/task-breaker/SKILL.md`
4. **示例集合**：`examples/task-breaker-examples.md`

### 问题反馈

如果遇到问题或建议：
1. 检查本文档的故障排除部分
2. 查看完整的示例了解正确用法
3. 参考 SKILL.md 了解详细机制

---

## 🎉 安装完成

您已经成功安装 Task Breaker Plugin！

现在可以：
1. 阅读快速入门指南：`QUICKSTART.md`
2. 查看使用示例：`EXAMPLES.md`
3. 开始使用插件分解您的复杂任务

---

**祝您使用愉快！**

**Task Breaker Plugin v1.0.0**

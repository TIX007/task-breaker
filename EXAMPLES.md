# Task Breaker Plugin - 使用示例集合

本文档包含 Task Breaker Plugin 的实际使用示例。

---

## 📚 目录

1. [开发场景](#开发场景)
2. [研究场景](#研究场景)
3. [分析场景](#分析场景)

---

## 开发场景

### 示例 1：Web 应用开发

**用户请求**：
```
帮我使用 React 和 Node.js 开发一个任务管理 Web 应用，
需要包含用户认证、任务 CRUD、标签系统和实时更新功能
```

**Task Breaker 响应**：

```
## Task Breakdown for Task Management Web App

### Original Task Description
开发任务管理 Web 应用：用户认证、任务 CRUD、标签系统、实时更新

### Decomposition Strategy
混合型策略：基础架构 → 并行功能开发 → 集成和测试

### Subtask List

#### Subtask 1: 项目初始化和架构设计
- **Objective**: 搭建项目基础架构
- **Dependencies**: None
- **Expected Output**: 项目脚手架，数据库配置
- **Priority**: High

#### Subtask 2: 数据库模型设计
- **Objective**: 设计数据库表结构和关系
- **Dependencies**: 1
- **Expected Output**: 数据库 schema 和 migration
- **Priority**: High

#### Subtask 3: 用户认证系统
- **Objective**: 实现用户注册、登录和认证
- **Dependencies**: 2
- **Expected Output**: 认证 API 和登录界面
- **Priority**: High

#### Subtask 4: 任务 CRUD 功能
- **Objective**: 实现任务的增删改查
- **Dependencies**: 2, 3
- **Expected Output**: 完整的任务管理功能
- **Priority**: High

#### Subtask 5: 标签系统（与 Subtask 4 并行）
- **Objective**: 实现任务标签管理
- **Dependencies**: 2, 3
- **Expected Output**: 标签创建、分配、过滤功能
- **Priority**: Medium

#### Subtask 6: 实时更新功能
- **Objective**: 实现任务的实时更新通知
- **Dependencies**: 4
- **Expected Output**: WebSocket 实时推送
- **Priority**: Medium

#### Subtask 7: UI/UX 优化
- **Objective**: 优化用户界面和体验
- **Dependencies**: 4, 5, 6
- **Expected Output**: 完整的前端界面
- **Priority**: Medium

#### Subtask 8: 测试和部署
- **Objective**: 编写测试并部署应用
- **Dependencies**: 7
- **Expected Output**: 测试套件和生产环境
- **Priority**: Medium

### Execution Plan
Phase 1: Subtask 1 (基础)
Phase 2: Subtask 2 (数据层)
Phase 3: [Subtask 3, 4, 5] 并行
Phase 4: Subtask 6 (实时)
Phase 5: Subtask 7 (前端)
Phase 6: Subtask 8 (测试部署)

Total: 40-60 hours
```

---

## 研究场景

### 示例 2：市场调研

**用户请求**：
```
研究2024年中国新能源汽车市场的发展趋势，
包括政策环境、市场格局、技术创新和消费者行为
```

**Task Breaker 响应**：

```
## Task Breakdown for China EV Market Research

### Original Task Description
研究2024年中国新能源汽车市场：政策、市场、技术、消费

### Decomposition Strategy
深度优先：4个维度并行研究 + 综合

### Subtask List

#### Subtask 1: 政策环境研究
- **Objective**: 分析相关政策
- **Dependencies**: None
- **Expected Output**: 政策分析报告
- **Priority**: High

#### Subtask 2: 市场格局分析
- **Objective**: 分析竞争和销量
- **Dependencies**: None
- **Expected Output**: 市场格局报告
- **Priority**: High

#### Subtask 3: 技术创新研究
- **Objective**: 调研技术突破
- **Dependencies**: None
- **Expected Output**: 技术创新报告
- **Priority**: High

#### Subtask 4: 消费者行为分析
- **Objective**: 分析购买偏好
- **Dependencies**: None
- **Expected Output**: 消费行为报告
- **Priority**: High

#### Subtask 5: 综合趋势分析
- **Objective**: 整合各维度分析
- **Dependencies**: 1, 2, 3, 4
- **Expected Output**: 完整趋势报告
- **Priority**: High

### Execution Plan
Phase 1: [Subtask 1, 2, 3, 4] 并行
Phase 2: Subtask 5 (综合)

Total: 30-45 minutes
```

---

## 分析场景

### 示例 3：销售数据分析

**用户请求**：
```
分析公司过去一年的销售数据，
找出关键趋势、客户特征、产品表现和增长机会
```

**Task Breaker 响应**：

```
## Task Breakdown for Sales Data Analysis

### Original Task Description
分析年度销售数据：趋势、客户、产品、机会

### Decomposition Strategy
混合型：数据准备 → 并行分析 → 综合洞察

### Subtask List

#### Subtask 1: 数据清洗和准备
- **Objective**: 清洗和转换数据
- **Dependencies**: None
- **Expected Output**: 清洁的数据集
- **Priority**: High

#### Subtask 2: 销售趋势分析
- **Objective**: 分析时间趋势
- **Dependencies**: 1
- **Expected Output**: 趋势报告和图表
- **Priority**: High

#### Subtask 3: 客户细分分析
- **Objective**: 识别客户群体
- **Dependencies**: 1 (与 Subtask 2 并行)
- **Expected Output**: 客户细分报告
- **Priority**: High

#### Subtask 4: 产品表现分析
- **Objective**: 分析产品销量和利润
- **Dependencies**: 1 (与 Subtask 2, 3 并行)
- **Expected Output**: 产品分析报告
- **Priority**: High

#### Subtask 5: 增长机会识别
- **Objective**: 识别增长点和风险
- **Dependencies**: 2, 3, 4
- **Expected Output**: 机会和建议报告
- **Priority**: High

### Execution Plan
Phase 1: Subtask 1 (数据准备)
Phase 2: [Subtask 2, 3, 4] 并行
Phase 3: Subtask 5 (综合洞察)

Total: 2-3 hours
```

---

## 更多示例

完整的示例集请参考：
- `examples/task-breaker-examples.md`

包含：
- 市场研究任务（6 个子任务）
- 软件开发任务（8 个子任务）
- 数据分析任务（7 个子任务）
- 内容创作任务（5 个子任务）

---

## 快速开始

1. 查看快速入门：`QUICKSTART.md`
2. 查看完整文档：`README.md`
3. 参考技术文档：`skills/task-breaker/SKILL.md`

开始使用 Task Breaker 插件！

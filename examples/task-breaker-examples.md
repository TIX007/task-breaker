# Task Breaker Examples

This directory contains real-world examples of how the Task Breaker skill can be used to decompose complex tasks.

## Example 1: Market Research Task

### User Request
"Research the electric vehicle market in 2025 and produce a comprehensive report covering market size, growth trends, key players, and future outlook."

### Task Breakdown

#### Subtask 1: Market Size and Growth Analysis
- **Objective**: Quantify current market size and growth trajectory
- **Description**: Research global EV market size, historical growth rates (2020-2024), and projected growth (2025-2030)
- **Dependencies**: None
- **Expected Output**: Market size statistics, growth charts, key metrics
- **Priority**: High

#### Subtask 2: Key Players Analysis
- **Objective**: Identify and analyze major EV manufacturers
- **Description**: Research top 10 EV companies by market share, analyze their strategies, product portfolios, and competitive positioning
- **Dependencies**: None
- **Expected Output**: Company profiles, market share data, competitive analysis
- **Priority**: High

#### Subtask 3: Technology Trends
- **Objective**: Identify key technological developments in EV space
- **Description**: Research battery technology improvements, charging infrastructure, autonomous driving integration, and other innovations
- **Dependencies**: None
- **Expected Output**: Technology analysis, innovation timeline, impact assessment
- **Priority**: Medium

#### Subtask 4: Regional Analysis
- **Objective**: Analyze EV adoption across different regions
- **Description**: Compare EV adoption rates, policies, and infrastructure in key markets (China, Europe, US, others)
- **Dependencies**: None
- **Expected Output**: Regional comparison tables, policy analysis, adoption trends
- **Priority**: Medium

#### Subtask 5: Challenges and Barriers
- **Objective**: Identify obstacles to EV adoption
- **Description**: Research charging infrastructure limitations, battery production constraints, consumer concerns, and regulatory challenges
- **Dependencies**: None
- **Expected Output**: Challenges list, impact assessment, mitigation strategies
- **Priority**: Medium

#### Subtask 6: Report Synthesis
- **Objective**: Compile all findings into comprehensive report
- **Description**: Synthesize results from subtasks 1-5, create executive summary, write findings, include data visualizations, provide recommendations
- **Dependencies**: 1, 2, 3, 4, 5
- **Expected Output**: Complete market research report (PDF or Markdown)
- **Priority**: High

### Execution Plan
- **Parallel Phase**: Subtasks 1-5 run simultaneously using 5 parallel research subagents
- **Synthesis Phase**: After all parallel subtasks complete, execute Subtask 6 to compile results
- **Estimated Time**: 45-60 minutes total (30 min parallel research + 15-30 min synthesis)

---

## Example 2: Software Development Task

### User Request
"Build a full-stack task management application with user authentication, task CRUD operations, and real-time updates."

### Task Breakdown

#### Subtask 1: Project Setup and Architecture Design
- **Objective**: Initialize project structure and define architecture
- **Description**: Set up project repository, choose tech stack, define data models, design API structure, create initial folder structure
- **Dependencies**: None
- **Expected Output**: Project skeleton, architecture documentation, tech stack selection
- **Priority**: High

#### Subtask 2: Database Design and Implementation
- **Objective**: Create database schema and set up database
- **Description**: Design database tables (users, tasks, categories), define relationships, write migrations, set up database connection
- **Dependencies**: 1
- **Expected Output**: Database schema files, migration scripts, connected database instance
- **Priority**: High

#### Subtask 3: Backend API Development
- **Objective**: Implement RESTful API endpoints
- **Description**: Create API endpoints for user authentication, task CRUD, category management, implement validation and error handling
- **Dependencies**: 2
- **Expected Output**: Complete API with all endpoints, API documentation
- **Priority**: High

#### Subtask 4: Frontend UI Development
- **Objective**: Build user interface components
- **Description**: Create React components for task list, task form, authentication UI, implement state management, responsive design
- **Dependencies**: 1
- **Expected Output**: Frontend application with all UI components
- **Priority**: High

#### Subtask 5: Frontend-Backend Integration
- **Objective**: Connect frontend to backend API
- **Description**: Implement API client, integrate authentication flow, connect task CRUD operations, handle loading states and errors
- **Dependencies**: 3, 4
- **Expected Output**: Fully integrated application with working features
- **Priority**: High

#### Subtask 6: Real-time Updates Implementation
- **Objective**: Add real-time sync for task updates
- **Description**: Implement WebSocket connection, set up server-side push notifications, handle real-time events in frontend
- **Dependencies**: 5
- **Expected Output**: Real-time task synchronization across multiple users
- **Priority**: Medium

#### Subtask 7: Authentication and Authorization
- **Objective**: Implement secure user authentication
- **Description**: Add JWT token handling, implement role-based access control, secure API endpoints, add password hashing
- **Dependencies**: 3, 5
- **Expected Output**: Secure authentication system with role management
- **Priority**: High

#### Subtask 8: Testing and Documentation
- **Objective**: Write tests and document the application
- **Description**: Write unit tests, integration tests, create API documentation, write user guide, deployment instructions
- **Dependencies**: 6, 7
- **Expected Output**: Test suite, API docs, user manual, deployment guide
- **Priority**: Medium

### Execution Plan
- **Phase 1**: Subtask 1 (foundation)
- **Phase 2**: Subtasks 2, 3, 4 (2 depends on 1; 3 depends on 2; 4 parallel with 2 and 3)
- **Phase 3**: Subtasks 5, 6, 7 (5 depends on 3 and 4; 6 depends on 5; 7 depends on 3 and 5)
- **Phase 4**: Subtask 8 (depends on all previous)
- **Estimated Time**: 4-6 hours total

---

## Example 3: Data Analysis Task

### User Request
"Analyze this sales dataset and produce insights about regional performance, product trends, and customer behavior."

### Task Breakdown

#### Subtask 1: Data Profiling and Quality Assessment
- **Objective**: Understand data structure and quality
- **Description**: Load dataset, examine schema, check for missing values, identify outliers, assess data quality
- **Dependencies**: None
- **Expected Output**: Data quality report, variable descriptions
- **Priority**: High

#### Subtask 2: Regional Performance Analysis
- **Objective**: Analyze sales by region
- **Description**: Calculate sales metrics by region, identify top/bottom performers, analyze regional trends, create visualizations
- **Dependencies**: 1
- **Expected Output**: Regional analysis tables, charts, key findings
- **Priority**: High

#### Subtask 3: Product Category Analysis
- **Objective**: Analyze product performance
- **Description**: Analyze sales by product category, identify best-sellers, analyze product trends, calculate category growth rates
- **Dependencies**: 1
- **Expected Output**: Product analysis report, recommendations
- **Priority**: High

#### Subtask 4: Customer Behavior Analysis
- **Objective**: Understand customer patterns
- **Description**: Analyze customer segments, calculate customer lifetime value, identify purchase patterns, analyze retention rates
- **Dependencies**: 1
- **Expected Output**: Customer segmentation analysis, behavioral insights
- **Priority**: High

#### Subtask 5: Trend and Seasonality Analysis
- **Objective**: Identify temporal patterns
- **Description**: Analyze sales trends over time, identify seasonal patterns, detect anomalies, forecast future trends
- **Dependencies**: 1
- **Expected Output**: Trend analysis, seasonal patterns, forecasts
- **Priority**: Medium

#### Subtask 6: Comprehensive Report Generation
- **Objective**: Synthesize all analyses into final report
- **Description**: Compile findings from subtasks 2-5, create executive summary, design data visualizations, write actionable recommendations
- **Dependencies**: 2, 3, 4, 5
- **Expected Output**: Complete analysis report (PDF or interactive dashboard)
- **Priority**: High

### Execution Plan
- **Parallel Phase**: Subtasks 2-5 run simultaneously after Subtask 1 completes (4 parallel analysis subagents)
- **Synthesis Phase**: Subtask 6 compiles all results
- **Estimated Time**: 30-45 minutes total

---

## Example 4: Content Creation Task

### User Request
"Create a comprehensive onboarding guide for new employees covering company culture, tools, and processes."

### Task Breakdown

#### Subtask 1: Research Company Culture and Values
- **Objective**: Gather information about company culture
- **Description**: Research company mission, values, work culture, team structure, company history, organizational principles
- **Dependencies**: None
- **Expected Output**: Company culture summary, values documentation
- **Priority**: High

#### Subtask 2: Tools and Technology Stack
- **Objective**: Document tools and technologies used
- **Description**: Compile list of software tools (communication, productivity, development), create setup guides, document best practices
- **Dependencies**: None
- **Expected Output**: Tools guide, setup instructions, cheat sheets
- **Priority**: High

#### Subtask 3: Processes and Workflows
- **Objective**: Document key processes
- **Description**: Map out common workflows (onboarding, project handoffs, approval processes), create process diagrams, document SLAs
- **Dependencies**: None
- **Expected Output**: Process documentation, workflow diagrams
- **Priority**: High

#### Subtask 4: Benefits and Policies
- **Objective**: Document employee benefits and policies
- **Description**: Compile benefits information, document HR policies, create FAQ section, outline company perks
- **Dependencies**: None
- **Expected Output**: Benefits guide, policy summary, FAQ
- **Priority**: Medium

#### Subtask 5: First 90-Day Roadmap
- **Objective**: Create onboarding timeline
- **Description**: Design 30-60-90 day plan with milestones, define checkpoints, create task list for new hires, set expectations
- **Dependencies**: 1, 2, 3
- **Expected Output**: Onboarding roadmap, milestone tracker
- **Priority**: High

#### Subtask 6: Guide Assembly and Formatting
- **Objective**: Compile all content into polished guide
- **Description**: Assemble content from subtasks 1-5, add introduction and conclusion, format professionally, create table of contents, add checklists
- **Dependencies**: 1, 2, 3, 4, 5
- **Expected Output**: Complete onboarding guide (PDF, web page, or interactive document)
- **Priority**: High

### Execution Plan
- **Parallel Phase**: Subtasks 1-4 run simultaneously (4 parallel research/writing subagents)
- **Sequential Phase**: Subtask 5 after 1-3 complete
- **Synthesis Phase**: Subtask 6 compiles final guide
- **Estimated Time**: 60-90 minutes total

---

## Key Takeaways

1. **Parallelization Benefits**: Examples 1, 3, and 4 show how multiple independent subtasks can run simultaneously, saving significant time
2. **Dependency Management**: Example 2 demonstrates complex dependencies requiring careful sequencing
3. **Clear Objectives**: Each subtask has a specific, measurable objective
4. **Expected Outputs**: Each subtask defines what it will produce before execution begins
5. **Prioritization**: High-priority subtasks ensure critical components are completed

## Usage Tips

- Start by identifying task type (depth-first, breadth-first, straightforward)
- Decompose into 3-7 subtasks for most complex tasks
- Maximize parallelization by minimizing dependencies
- Define clear success criteria for each subtask
- Use the examples as templates but adapt to your specific task

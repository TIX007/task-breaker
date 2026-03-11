# Task Breaker Examples

This document contains detailed real-world examples of task breakdown scenarios using the Task Breaker skill.

## Table of Contents

1. [Market Research Task](#example-1-market-research-task)
2. [Software Development Task](#example-2-software-development-task)
3. [Data Analysis Task](#example-3-data-analysis-task)
4. [Content Creation Task](#example-4-content-creation-task)

---

## Example 1: Market Research Task

### Original Task Description

Research the current state of electric vehicle (EV) market adoption across 5 major regions (China, Europe, US, Japan, South Korea) and produce a comprehensive comparative analysis report.

### Task Analysis

- **Task Type**: Breadth-first (distinct regions to research independently)
- **Complexity**: High (requires data collection from multiple regions)
- **Parallelizable**: Yes (all 5 regions can be researched simultaneously)
- **Dependencies**: None for data collection, synthesis depends on all research

### Decomposition Strategy

**Breadth-first approach**: Create 5 parallel research subtasks (one per region) followed by 1 synthesis subtask to create the comparative report.

### Subtask List

#### Subtask 1: China EV Market Research
- **Objective**: Research EV market adoption in China
- **Description**: Collect data on EV sales volume, market share, government incentives, charging infrastructure, and key players in China's EV market
- **Dependencies**: None
- **Expected Output**: Structured report with China EV market data including statistics, policies, and trends
- **Priority**: High
- **Estimated Complexity**: Medium

#### Subtask 2: Europe EV Market Research
- **Objective**: Research EV market adoption in Europe
- **Description**: Collect data on EV sales across major European countries, EU regulations, emission standards, charging network, and manufacturer strategies
- **Dependencies**: None
- **Expected Output**: Structured report with Europe EV market data including statistics, policies, and trends
- **Priority**: High
- **Estimated Complexity**: Medium

#### Subtask 3: US EV Market Research
- **Objective**: Research EV market adoption in the United States
- **Description**: Collect data on EV sales by state, federal and state incentives, charging infrastructure expansion, and domestic manufacturers
- **Dependencies**: None
- **Expected Output**: Structured report with US EV market data including statistics, policies, and trends
- **Priority**: High
- **Estimated Complexity**: Medium

#### Subtask 4: Japan EV Market Research
- **Objective**: Research EV market adoption in Japan
- **Description**: Collect data on EV sales, hybrid vehicle influence, government policies, infrastructure development, and Japanese automaker strategies
- **Dependencies**: None
- **Expected Output**: Structured report with Japan EV market data including statistics, policies, and trends
- **Priority**: High
- **Estimated Complexity**: Medium

#### Subtask 5: South Korea EV Market Research
- **Objective**: Research EV market adoption in South Korea
- **Description**: Collect data on EV sales, government programs, battery technology industry, charging infrastructure, and key domestic players
- **Dependencies**: None
- **Expected Output**: Structured report with South Korea EV market data including statistics, policies, and trends
- **Priority**: High
- **Estimated Complexity**: Medium

#### Subtask 6: Comparative Analysis and Report Synthesis
- **Objective**: Synthesize findings from all 5 regions into a comprehensive comparative report
- **Description**: Analyze collected data, compare adoption rates, identify common trends, highlight regional differences, evaluate policy effectiveness, and create visualizations (charts, graphs)
- **Dependencies**: 1, 2, 3, 4, 5
- **Expected Output**: Comprehensive comparative analysis report with executive summary, regional comparisons, trend analysis, policy recommendations, and data visualizations
- **Priority**: High
- **Estimated Complexity**: High

### Execution Plan

**Phase 1**: Launch Subtasks 1-5 in parallel (simultaneous execution)
- Timeline: 15-20 minutes

**Phase 2**: After Phase 1 completes, launch Subtask 6
- Timeline: 10-15 minutes

**Total Estimated Time**: 25-35 minutes

### Progress Tracking

- Subtask 1: ✓ Completed
- Subtask 2: ✓ Completed
- Subtask 3: ✓ Completed
- Subtask 4: ✓ Completed
- Subtask 5: ✓ Completed
- Subtask 6: ⏳ In Progress

### Synthesis

The final report includes:
- Executive Summary (2-3 pages)
- Regional Analysis (5 sections, 3-4 pages each)
- Comparative Analysis (2-3 pages)
- Key Trends and Insights (2-3 pages)
- Policy Recommendations (1-2 pages)
- Appendices with Data Tables and Charts

---

## Example 2: Software Development Task

### Original Task Description

Build a full-stack task management web application with user authentication, task CRUD operations, and real-time notifications.

### Task Analysis

- **Task Type**: Mixed (some sequential, some parallelizable)
- **Complexity**: High (multiple components with dependencies)
- **Parallelizable**: Partially (frontend and some backend tasks can run in parallel)
- **Dependencies**: Database schema must be designed before API, API must exist before frontend integration

### Decomposition Strategy

**Hybrid approach**: Start with foundational backend tasks, then parallelize frontend and advanced backend features, followed by integration and testing.

### Subtask List

#### Subtask 1: Database Design and Schema
- **Objective**: Design database schema for users, tasks, and notifications
- **Description**: Create entity-relationship diagrams, define tables and relationships, design indexes, establish data constraints and validation rules
- **Dependencies**: None
- **Expected Output**: Complete database schema with ERD diagrams and SQL DDL scripts
- **Priority**: High
- **Estimated Complexity**: Medium

#### Subtask 2: Backend API Development
- **Objective**: Implement REST API endpoints for task management
- **Description**: Build API routes for user registration/login, task CRUD operations, and notification system. Include authentication middleware and error handling
- **Dependencies**: 1 (Database schema must be defined)
- **Expected Output**: Complete REST API with documentation (Swagger/OpenAPI)
- **Priority**: High
- **Estimated Complexity**: High

#### Subtask 3: Frontend UI Development
- **Objective**: Build user interface for task management
- **Description**: Create responsive UI with task list, task creation/edit forms, task detail views, and user dashboard. Use modern frontend framework (React/Vue)
- **Dependencies**: None (can start in parallel with Subtask 2 using mock data)
- **Expected Output**: Complete frontend application with all UI components
- **Priority**: High
- **Estimated Complexity**: High

#### Subtask 4: Frontend-Backend Integration
- **Objective**: Connect frontend to backend API
- **Description**: Implement API client, handle authentication tokens, integrate all CRUD operations, implement loading states and error handling
- **Dependencies**: 2, 3 (both API and frontend must exist)
- **Expected Output**: Fully integrated application where UI communicates with backend
- **Priority**: High
- **Estimated Complexity**: Medium

#### Subtask 5: Authentication & Authorization System
- **Objective**: Implement secure user authentication and authorization
- **Description**: Set up JWT authentication, password hashing, role-based access control, and session management. Implement password reset flow
- **Dependencies**: None (can run parallel with Subtask 2)
- **Expected Output**: Complete authentication system with secure login/logout and password reset
- **Priority**: High
- **Estimated Complexity**: Medium

#### Subtask 6: Real-time Notifications
- **Objective**: Implement real-time notification system
- **Description**: Set up WebSocket server, implement push notifications for task updates, create notification preferences UI, handle connection management
- **Dependencies**: 2, 5 (requires API and user authentication)
- **Expected Output**: Real-time notification system working across connected clients
- **Priority**: Medium
- **Estimated Complexity**: High

#### Subtask 7: Testing Suite
- **Objective**: Create comprehensive test suite
- **Description**: Write unit tests for backend logic, integration tests for API endpoints, component tests for frontend UI, and end-to-end tests for critical user flows
- **Dependencies**: 4, 5, 6 (application must be functional)
- **Expected Output**: Test suite with >80% code coverage and CI/CD integration
- **Priority**: Medium
- **Estimated Complexity**: High

#### Subtask 8: Documentation and Deployment
- **Objective**: Write documentation and deploy to production
- **Description**: Create user documentation, API documentation, deployment guide, and CI/CD pipeline. Deploy application to cloud platform
- **Dependencies**: 7 (testing should be complete)
- **Expected Output**: Production-deployed application with complete documentation
- **Priority**: Medium
- **Estimated Complexity**: Medium

### Execution Plan

**Phase 1**: Launch Subtask 1
- Timeline: 2-3 hours

**Phase 2**: Launch Subtasks 2, 3, 5 in parallel
- Timeline: 8-12 hours

**Phase 3**: Launch Subtask 4
- Timeline: 4-6 hours (depends on Phase 2 completion)

**Phase 4**: Launch Subtask 6
- Timeline: 4-6 hours (can start after Phase 2, parallel with Phase 3)

**Phase 5**: Launch Subtask 7
- Timeline: 6-8 hours

**Phase 6**: Launch Subtask 8
- Timeline: 4-6 hours

**Total Estimated Time**: 30-45 hours

### Progress Tracking

- Subtask 1: ✓ Completed
- Subtask 2: ✓ Completed
- Subtask 3: ✓ Completed
- Subtask 4: ✓ Completed
- Subtask 5: ✓ Completed
- Subtask 6: ✓ Completed
- Subtask 7: ✓ Completed
- Subtask 8: ⏳ In Progress

### Synthesis

The final deliverable is a production-ready task management application with:
- Secure user authentication
- Full task CRUD functionality
- Real-time notifications
- Comprehensive test coverage
- Complete documentation
- Deployed to cloud infrastructure

---

## Example 3: Data Analysis Task

### Original Task Description

Analyze a large e-commerce sales dataset (1M+ transactions) to identify key trends, customer segments, and actionable insights for business improvement.

### Task Analysis

- **Task Type**: Mixed (parallel analysis followed by synthesis)
- **Complexity**: High (large dataset, multiple analysis dimensions)
- **Parallelizable**: Yes (different analysis dimensions can run simultaneously)
- **Dependencies**: Data cleaning must complete before any analysis, synthesis depends on all analyses

### Decomposition Strategy

**Sequential foundation + Parallel analysis**: Start with data cleaning and profiling, then run multiple parallel analysis tasks, followed by insight synthesis and visualization.

### Subtask List

#### Subtask 1: Data Cleaning and Preprocessing
- **Objective**: Clean and preprocess the raw dataset
- **Description**: Handle missing values, remove duplicates, correct data types, standardize formats, detect and handle outliers
- **Dependencies**: None
- **Expected Output**: Clean dataset with data quality report documenting all transformations
- **Priority**: High
- **Estimated Complexity**: High

#### Subtask 2: Data Profiling and Descriptive Statistics
- **Objective**: Generate comprehensive data profile and statistics
- **Description**: Calculate descriptive statistics for all numeric fields, analyze categorical variable distributions, identify data patterns, check data quality metrics
- **Dependencies**: 1 (clean data required)
- **Expected Output**: Data profile report with statistics, distributions, and quality metrics
- **Priority**: High
- **Estimated Complexity**: Medium

#### Subtask 3: Sales Trend Analysis
- **Objective**: Analyze temporal sales patterns and trends
- **Description**: Analyze sales over time (daily, weekly, monthly, seasonally), identify growth trends, detect seasonality patterns, analyze weekday/weekend differences
- **Dependencies**: 2 (requires cleaned data)
- **Expected Output**: Trend analysis report with time-series visualizations and statistical tests
- **Priority**: High
- **Estimated Complexity**: Medium

#### Subtask 4: Customer Segmentation Analysis
- **Objective**: Segment customers based on purchasing behavior
- **Description**: Perform RFM (Recency, Frequency, Monetary) analysis, use clustering algorithms to identify customer segments, analyze segment characteristics and value
- **Dependencies**: 2 (requires cleaned data)
- **Expected Output**: Customer segmentation report with segment definitions, sizes, and profiles
- **Priority**: High
- **Estimated Complexity**: High

#### Subtask 5: Product Analysis
- **Objective**: Analyze product performance and categories
- **Description**: Identify top-selling products, analyze product categories, calculate product profitability, analyze cross-selling patterns and product affinities
- **Dependencies**: 2 (requires cleaned data)
- **Expected Output**: Product analysis report with category performance and product rankings
- **Priority**: High
- **Estimated Complexity**: Medium

#### Subtask 6: Geographic Analysis
- **Objective**: Analyze sales by geographic region
- **Description**: Aggregate sales by region/country/state, identify regional preferences, analyze regional growth patterns, detect geographic clusters
- **Dependencies**: 2 (requires cleaned data)
- **Expected Output**: Geographic analysis report with regional breakdown and insights
- **Priority**: Medium
- **Estimated Complexity**: Medium

#### Subtask 7: Insight Synthesis and Dashboard Creation
- **Objective**: Synthesize all analyses into comprehensive insights and create interactive dashboard
- **Description**: Integrate findings from all analysis tasks, identify actionable business insights, prioritize recommendations, create interactive dashboard with key metrics and visualizations
- **Dependencies**: 3, 4, 5, 6 (all analyses must be complete)
- **Expected Output**: Comprehensive insights report with recommendations and interactive dashboard
- **Priority**: High
- **Estimated Complexity**: High

### Execution Plan

**Phase 1**: Launch Subtask 1
- Timeline: 4-6 hours (for 1M+ records)

**Phase 2**: Launch Subtask 2
- Timeline: 2-3 hours

**Phase 3**: Launch Subtasks 3, 4, 5, 6 in parallel
- Timeline: 6-10 hours (can vary based on analysis complexity)

**Phase 4**: Launch Subtask 7
- Timeline: 6-8 hours

**Total Estimated Time**: 18-27 hours

### Progress Tracking

- Subtask 1: ✓ Completed
- Subtask 2: ✓ Completed
- Subtask 3: ✓ Completed
- Subtask 4: ✓ Completed
- Subtask 5: ✓ Completed
- Subtask 6: ✓ Completed
- Subtask 7: ⏳ In Progress

### Synthesis

The final deliverable includes:
- Executive Summary with key findings
- Detailed Analysis Report (50-70 pages)
- Interactive Dashboard with:
  - Sales trend visualizations
  - Customer segment profiles
  - Product performance metrics
  - Geographic heatmaps
- Actionable Business Recommendations (10-15 prioritized items)
- Appendices with methodology and technical details

---

## Example 4: Content Creation Task

### Original Task Description

Create a comprehensive user onboarding guide for a new SaaS platform, including quick start tutorials, feature documentation, and best practices.

### Task Analysis

- **Task Type**: Breadth-first (different content sections can be created independently)
- **Complexity**: Medium to High (requires product knowledge and good writing)
- **Parallelizable**: Yes (different documentation sections can be written simultaneously)
- **Dependencies**: None for content creation, review and synthesis depend on all sections

### Decomposition Strategy

**Breadth-first approach**: Create 4 parallel content creation subtasks covering different aspects, followed by 1 review and synthesis subtask.

### Subtask List

#### Subtask 1: Quick Start Guide
- **Objective**: Create getting-started tutorial for new users
- **Description**: Write step-by-step tutorial covering account creation, initial setup, first task completion, and basic navigation. Include screenshots and walkthrough videos if possible
- **Dependencies**: None
- **Expected Output**: Quick start guide (10-15 pages) with screenshots and practical examples
- **Priority**: High
- **Estimated Complexity**: Medium

#### Subtask 2: Core Feature Documentation
- **Objective**: Document all core platform features
- **Description**: Write comprehensive documentation for main features including task management, collaboration tools, reporting, and automation. Include use cases and examples for each feature
- **Dependencies**: None
- **Expected Output**: Feature documentation (30-40 pages) organized by feature category
- **Priority**: High
- **Estimated Complexity**: High

#### Subtask 3: Advanced Features and Workflows
- **Objective**: Document advanced features and complex workflows
- **Description**: Cover advanced topics such as API integration, custom workflows, third-party integrations, and enterprise features. Provide detailed examples and best practices
- **Dependencies**: None
- **Expected Output**: Advanced features guide (20-25 pages) with technical details
- **Priority**: Medium
- **Estimated Complexity**: High

#### Subtask 4: Best Practices and Troubleshooting
- **Objective**: Create best practices guide and troubleshooting section
- **Description**: Compile common use case patterns, productivity tips, optimization strategies, and troubleshooting solutions for common issues. Include FAQ section
- **Dependencies**: None
- **Expected Output**: Best practices guide (15-20 pages) and FAQ section
- **Priority**: Medium
- **Estimated Complexity**: Medium

#### Subtask 5: Review, Editing, and Final Assembly
- **Objective**: Review all content, ensure consistency, and assemble final guide
- **Description**: Review all sections for accuracy, consistency in tone and style, completeness, and clarity. Create table of contents, navigation structure, and ensure cross-references work correctly
- **Dependencies**: 1, 2, 3, 4 (all content sections must be complete)
- **Expected Output**: Final comprehensive onboarding guide with professional formatting and structure
- **Priority**: High
- **Estimated Complexity**: High

### Execution Plan

**Phase 1**: Launch Subtasks 1, 2, 3, 4 in parallel
- Timeline: 12-16 hours (each subtask)

**Phase 2**: Launch Subtask 5
- Timeline: 6-8 hours

**Total Estimated Time**: 18-24 hours

### Progress Tracking

- Subtask 1: ✓ Completed
- Subtask 2: ✓ Completed
- Subtask 3: ✓ Completed
- Subtask 4: ✓ Completed
- Subtask 5: ⏳ In Progress

### Synthesis

The final deliverable is a comprehensive onboarding guide containing:
- Table of Contents with clear navigation
- Quick Start Guide (Chapter 1)
- Core Features (Chapters 2-5)
- Advanced Features (Chapters 6-8)
- Best Practices (Chapter 9)
- Troubleshooting & FAQ (Chapter 10)
- Glossary of Terms
- Appendices with additional resources

**Total Length**: 80-120 pages with screenshots, diagrams, and examples

---

## Summary

These examples demonstrate how the Task Breaker skill can be applied to different types of complex tasks:

1. **Market Research**: Parallel data collection + synthesis
2. **Software Development**: Sequential foundations + parallel development phases
3. **Data Analysis**: Data preparation + parallel analysis + synthesis
4. **Content Creation**: Parallel content creation + review and assembly

Key patterns emerge across all examples:
- Clear task analysis before decomposition
- Appropriate decomposition strategy based on task type
- Well-defined subtasks with clear objectives and expected outputs
- Thoughtful execution plan considering dependencies
- Comprehensive synthesis of all subtask results

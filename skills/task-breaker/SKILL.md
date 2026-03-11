---
name: task-breaker
description: This skill should be used when the user requests to break down a complex task into multiple subtasks for execution. Trigger keywords include "拆分任务", "分解任务", "子任务", "任务拆解", "break down task", "split task", "subtask", "task decomposition", or any request to divide a large task into smaller manageable components.
---

# Task Breaker

This skill provides a systematic approach to breaking down complex tasks into executable subtasks and managing their execution.

## Purpose

Complex tasks often require decomposition into smaller, manageable components for efficient execution. This skill enables systematic task breakdown, parallel execution where possible, and coordinated completion of subtasks.

## When to Use This Skill

Use this skill when the user presents any of the following scenarios:

- Large, complex tasks that would benefit from decomposition
- Multi-step workflows with clear dependencies
- Tasks that can be parallelized for efficiency
- Projects requiring multiple agents or team members
- Any request involving "拆分任务", "分解任务", "子任务", or similar concepts

## Task Breakdown Workflow

### Step 1: Analyze the Original Task

First, thoroughly analyze the user's original task to understand:

1. **Core Objectives**: What is the main goal the user wants to accomplish?
2. **Task Type**: Identify whether this is a depth-first, breadth-first, or straightforward query
3. **Dependencies**: Determine which subtasks depend on others
4. **Parallelizable Components**: Identify what can be executed simultaneously
5. **Resources Needed**: Determine what tools, files, or skills are required

### Step 2: Determine Decomposition Strategy

Based on the task type, choose an appropriate decomposition strategy:

**For Depth-First Tasks**:
- Break down by different perspectives or methodological approaches
- Create 3-5 distinct analytical angles
- Each subtask explores the same core question from different viewpoints
- Example: "Analyze the impact of AI on healthcare" → Regulatory, Clinical, Economic, Technological perspectives

**For Breadth-First Tasks**:
- Break down into distinct, independent sub-questions
- Identify natural divisions in the problem space
- Create clear boundaries between subtasks to avoid overlap
- Example: "Compare tax systems of 5 countries" → One subtask per country

**For Straightforward Tasks**:
- Break down into sequential steps
- Focus on logical dependencies
- Keep it simple with 1-2 subtasks
- Example: "Process a file" → Read file, Process content, Save output

### Step 3: Create Subtask List

Generate a structured list of subtasks following these guidelines:

**Subtask Guidelines**:
1. **Clarity**: Each subtask must have a clear, specific objective
2. **Independence**: Maximize independence between subtasks where possible
3. **Manageability**: Each subtask should be accomplishable in a reasonable timeframe
4. **Measurability**: Define clear success criteria for each subtask
5. **Dependencies**: Explicitly state any dependencies on other subtasks

**Subtask Format**:
For each subtask, define:

- **Task ID**: Unique identifier (e.g., "1", "2", "3")
- **Description**: Clear statement of what needs to be done
- **Priority**: High, Medium, or Low (for ordering)
- **Dependencies**: List of other task IDs this depends on
- **Expected Output**: What deliverable is expected
- **Estimated Complexity**: Simple, Medium, or Complex

### Step 4: Execute Subtasks

**Execution Principles**:

1. **Parallelize Where Possible**: Launch independent subtasks simultaneously using multiple agents
2. **Respect Dependencies**: Execute dependent subtasks only after prerequisites are complete
3. **Monitor Progress**: Track the status of each subtask (Pending, In Progress, Completed, Blocked)
4. **Handle Failures**: If a subtask fails, determine if it blocks other tasks or can be worked around

**Task Delegation**:

When delegating subtasks to agents:

- Provide extremely clear and specific instructions
- Include relevant context and background information
- Specify expected output format
- Define success criteria
- Set appropriate time or complexity limits
- Reference any tools or skills that should be used

Use the `Task` tool to create subagents for parallel execution:

```
Task(subagent_name="research_subagent", description="Research topic X", prompt="Detailed instructions...")
```

Launch independent subtasks in parallel batches to maximize efficiency. Aim for 3-5 parallel subtasks for standard complexity, up to 10 for high complexity.

### Step 5: Synthesize Results

After subtasks complete:

1. **Collect Outputs**: Gather results from all subtasks
2. **Validate Quality**: Ensure each subtask met its success criteria
3. **Resolve Conflicts**: Address any inconsistencies between subtask results
4. **Integrate Findings**: Combine individual results into a coherent whole
5. **Final Review**: Verify that the synthesized result addresses the original task

**Synthesis Guidelines**:

- Maintain consistency across subtask outputs
- Use cross-validation to verify accuracy
- Highlight areas where subtasks disagree or have uncertainties
- Provide clear attribution of findings to specific subtasks
- Ensure the final result is greater than the sum of parts

## Best Practices

### Do:

- Start by clarifying the task if objectives are unclear
- Aim for 3-7 subtasks for most complex tasks (avoid over-decomposition)
- Make subtasks as independent as possible to enable parallelization
- Define clear success criteria for each subtask
- Use visual aids (diagrams, flowcharts) when helpful
- Keep track of time and adjust complexity if running long

### Don't:

- Create more subtasks than necessary (token efficiency matters)
- Create subtasks with overlapping scope (causes redundant work)
- Ignore dependencies between subtasks (causes execution failures)
- Proceed to synthesis before all prerequisites are complete
- Forget to validate subtask outputs before synthesis

## Output Format

Present the task breakdown in the following format:

```
## Task Breakdown for [Original Task]

### Original Task Description
[Brief restatement of what the user wants to accomplish]

### Decomposition Strategy
[Explain the approach chosen and why]

### Subtask List

#### Subtask 1: [Title]
- **Objective**: [What this subtask accomplishes]
- **Description**: [Detailed description of the work]
- **Dependencies**: None (or list dependencies)
- **Expected Output**: [What will be produced]
- **Priority**: High/Medium/Low

#### Subtask 2: [Title]
- **Objective**: ...
- **Description**: ...
- **Dependencies**: 1 (depends on Subtask 1)
- **Expected Output**: ...
- **Priority**: ...

### Execution Plan
[Order of execution, which tasks run in parallel, timeline estimate]

### Progress Tracking
- Subtask 1: ✓ Completed
- Subtask 2: ✓ Completed
- Subtask 3: ⏳ In Progress
- Subtask 4: ⏸️ Pending

### Synthesis
[Integrate all subtask results into final deliverable]
```

## Examples

### Example 1: Research Task

**User Request**: "Research the current state of renewable energy adoption in 5 European countries"

**Decomposition**:
- 5 parallel subtasks (one per country: Germany, Denmark, Netherlands, Sweden, Norway)
- Each subtask: research renewable energy statistics, policies, adoption rates
- 1 synthesis subtask: compare findings, identify trends, produce comparative report

### Example 2: Development Task

**User Request**: "Build a full-stack web application for task management"

**Decomposition**:
- Subtask 1: Design database schema and API endpoints (foundational)
- Subtask 2: Implement backend API (depends on Subtask 1)
- Subtask 3: Build frontend UI (parallel with Subtask 2)
- Subtask 4: Integrate frontend with backend (depends on Subtasks 2 and 3)
- Subtask 5: Add authentication and authorization (parallel with Subtask 4)
- Subtask 6: Write tests and documentation (depends on all development tasks)

### Example 3: Data Analysis Task

**User Request**: "Analyze this large dataset and generate insights report"

**Decomposition**:
- Subtask 1: Data profiling and quality assessment
- Subtask 2: Statistical analysis and trend identification
- Subtask 3: Visualization and chart generation
- Subtask 4: Insight synthesis and report writing
- (All tasks can be parallel except Subtask 4 which depends on 1-3)

## Common Patterns

### Pattern 1: Sequential Chain
For tasks with clear dependencies:
```
Task 1 → Task 2 → Task 3 → Task 4
```
Use when: Order matters and each step builds on previous results

### Pattern 2: Parallel Execution
For independent tasks that can run simultaneously:
```
┌─ Task 1 ─┐
├─ Task 2 ─┤ → Synthesis
└─ Task 3 ─┘
```
Use when: Subtasks are independent and can benefit from parallelization

### Pattern 3: Fan-In
For collecting results from multiple sources:
```
Task 1 ─┐
Task 2 ─┼─→ Synthesis
Task 3 ─┘
```
Use when: Gathering information from different perspectives or sources

### Pattern 4: Fan-Out
For distributing work across similar items:
```
Task → Subtask 1
     → Subtask 2
     → Subtask 3
```
Use when: Processing multiple items of the same type (e.g., analyzing multiple files)

## Tool Usage

### Primary Tools

**Task Tool**: For creating subagents
- Use `subagent_name="research_subagent"` for research tasks
- Use `subagent_name="code-explorer"` for codebase exploration
- Provide extremely clear, detailed instructions in the `prompt` parameter
- Specify mode (acceptEdits, bypassPermissions, default, plan) as appropriate

**Parallel Execution**: Launch multiple `Task` calls simultaneously to run subtasks in parallel

### Secondary Tools

- **search_file**: When subtasks need file discovery
- **search_content**: When subtasks need pattern matching
- **read_file**: When subtasks need to read specific files
- **web_search**: When subtasks need external information
- **execute_command**: When subtasks need system operations

## Quality Assurance

### Before Subtask Execution:
- [ ] Verify task objectives are clear
- [ ] Confirm decomposition strategy is appropriate
- [ ] Check that subtasks are properly scoped
- [ ] Validate that dependencies are correctly identified

### During Subtask Execution:
- [ ] Monitor each subtask's progress
- [ ] Address failures or blockers promptly
- [ ] Adjust scope if time constraints emerge
- [ ] Keep track of intermediate results

### After Subtask Execution:
- [ ] Validate each subtask's output quality
- [ ] Verify all dependencies were satisfied
- [ ] Check for inconsistencies across subtasks
- [ ] Ensure synthesis addresses original objectives

## Error Handling

### Subtask Failure Strategies

1. **Retry**: For transient failures (network issues, temporary errors)
2. **Adjust Scope**: Reduce complexity and retry
3. **Skip**: For optional subtasks that don't block completion
4. **Alternative Approach**: Try a different method for the failed task
5. **Escalate**: Report the issue to the user if critical

### Dependency Failures

When a prerequisite subtask fails:
- Assess whether dependent tasks can proceed with partial results
- Re-prioritize to focus on critical paths
- Consider alternative decompositions
- Inform user of impact on overall timeline

## Advanced Techniques

### Dynamic Decomposition

For very complex tasks, use iterative decomposition:

1. Initial high-level breakdown
2. Execute first level subtasks
3. Further decompose complex subtasks as needed
4. Continue until all tasks are manageable

### Adaptive Execution

Monitor execution and adapt as needed:

- If subtasks complete quickly, add more parallelization
- If dependencies emerge unexpectedly, restructure execution order
- If quality is insufficient, split subtasks further
- If time runs out, focus on highest-priority subtasks

### Result Aggregation

Use structured aggregation for complex outputs:

- Standardize output formats across subtasks
- Create templates for consistent presentation
- Use metadata to track source and confidence
- Implement cross-validation for critical results

## Limitations and Considerations

- **Token Efficiency**: More subtasks = more overhead. Balance between parallelization and efficiency
- **Communication Overhead**: Coordination between subtasks has a cost
- **Dependency Complexity**: Highly dependent tasks cannot be parallelized
- **Quality Variance**: Different subtasks may produce varying quality results
- **Time Constraints**: Decomposition has overhead - not always faster for simple tasks

## Decision Framework

Use this skill when:

✅ Task requires more than 30 minutes of focused work
✅ Task has multiple distinct components
✅ Task benefits from different perspectives or approaches
✅ Task can benefit from parallel execution
✅ Task requires domain expertise you lack

Do NOT use this skill when:

❌ Task can be completed in under 5 minutes
❌ Task is inherently sequential and cannot be decomposed meaningfully
❌ Task is extremely simple or straightforward
❌ User just wants a quick answer or fact
❌ Decomposition overhead exceeds its benefit

## Summary

The Task Breaker skill enables systematic decomposition of complex tasks into manageable subtasks, supports parallel execution where possible, and provides structured frameworks for synthesis and reporting. Use it judiciously for genuinely complex tasks, and avoid over-engineering simple requests.

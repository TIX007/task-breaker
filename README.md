# Task Breaker Skill

A WorkBuddy skill for systematically breaking down complex tasks into manageable subtasks and coordinating their execution.

## What This Skill Does

The Task Breaker skill helps you:

- Decompose complex tasks into smaller, executable subtasks
- Identify dependencies between subtasks
- Execute subtasks in parallel when possible
- Track progress and handle failures gracefully
- Synthesize results from multiple subtasks into a coherent final output

## When to Use

Use this skill when you encounter:

- Large, complex projects that require multiple steps
- Tasks with clear independent components that can be parallelized
- Multi-step workflows with dependencies
- Projects that could benefit from different perspectives or approaches
- Any request involving "拆分任务", "分解任务", "子任务", or task decomposition

**Trigger Keywords:**
- "拆分任务" (split task)
- "分解任务" (break down task)
- "子任务" (subtask)
- "任务拆解" (task decomposition)
- "break down task"
- "split task"
- "subtask"
- "task decomposition"

## Skill Structure

```
task-breaker/
├── SKILL.md                          # Main skill documentation (required)
├── README.md                         # This file
├── examples/
│   └── task-breaker-examples.md     # Real-world examples with detailed breakdowns
└── templates/
    └── task-breakdown-template.md    # Template for creating custom task breakdowns
```

## Quick Start

### Basic Usage

When you encounter a complex task, simply describe it naturally. The Task Breaker skill will automatically:

1. Analyze the task type and complexity
2. Create an appropriate decomposition strategy
3. Break down the task into subtasks
4. Execute subtasks (with parallelization where possible)
5. Synthesize results into a final deliverable

### Example Request

```
Research the current state of renewable energy adoption in 5 European countries and produce a comparative report.
```

The skill will automatically:
- Create 5 parallel research subtasks (one per country)
- Execute them simultaneously
- Synthesize findings into a comparative report

## Key Features

### Intelligent Decomposition

The skill recognizes three types of tasks:

1. **Depth-First**: Same topic from multiple perspectives (e.g., analyzing AI impact from regulatory, clinical, economic angles)
2. **Breadth-First**: Distinct independent sub-questions (e.g., comparing 5 different countries)
3. **Straightforward**: Sequential steps with clear dependencies (e.g., processing a file)

### Parallel Execution

Identifies independent subtasks and executes them simultaneously using multiple agents, dramatically reducing total execution time.

### Dependency Management

Respects dependencies between subtasks, ensuring prerequisite work is complete before dependent tasks begin.

### Progress Tracking

Monitors the status of each subtask (Pending, In Progress, Completed, Blocked) and provides real-time updates.

### Result Synthesis

Combines outputs from all subtasks into a coherent final deliverable, handling inconsistencies and cross-validating results.

## Documentation

### SKILL.md

The complete skill documentation including:
- Detailed workflow instructions
- Best practices and common patterns
- Quality assurance guidelines
- Error handling strategies
- Advanced techniques

### Examples Directory (`examples/task-breaker-examples.md`)

Four complete real-world examples:

1. **Market Research Task**: Researching EV market with 6 subtasks (5 parallel + synthesis)
2. **Software Development Task**: Building a full-stack app with 8 subtasks and complex dependencies
3. **Data Analysis Task**: Analyzing sales data with 6 subtasks (4 parallel analysis + synthesis)
4. **Content Creation Task**: Creating onboarding guide with 6 subtasks (4 parallel + synthesis)

Each example includes:
- Original task description
- Complete subtask breakdown
- Execution plan
- Time estimates

### Templates Directory (`templates/task-breakdown-template.md`)

A ready-to-use template for creating custom task breakdowns including:
- Task analysis sections
- Subtask definition format
- Execution plan structure
- Progress tracking table
- Risk assessment
- Success criteria
- Synthesis plan

## Best Practices

### Do's

✅ Use for tasks requiring more than 30 minutes of focused work
✅ Create 3-7 subtasks for most complex tasks
✅ Maximize parallelization by minimizing dependencies
✅ Define clear success criteria for each subtask
✅ Monitor progress and adjust as needed

### Don'ts

❌ Over-decompose simple tasks (token efficiency matters)
❌ Create subtasks with overlapping scope
❌ Ignore dependencies between subtasks
❌ Proceed to synthesis before prerequisites are complete
❌ Use for tasks that complete in under 5 minutes

## Common Patterns

### Parallel Execution Pattern
```
┌─ Task 1 ─┐
├─ Task 2 ─┤ → Synthesis
└─ Task 3 ─┘
```
Use when: Subtasks are independent and can benefit from parallelization

### Sequential Chain Pattern
```
Task 1 → Task 2 → Task 3 → Task 4
```
Use when: Order matters and each step builds on previous results

### Fan-In Pattern
```
Task 1 ─┐
Task 2 ─┼─→ Synthesis
Task 3 ─┘
```
Use when: Gathering information from different perspectives

### Fan-Out Pattern
```
Task → Subtask 1
     → Subtask 2
     → Subtask 3
```
Use when: Processing multiple items of the same type

## Output Format

When breaking down a task, the skill produces:

1. **Task Analysis**: Understanding of objectives and complexity
2. **Decomposition Strategy**: Explanation of approach
3. **Subtask List**: Detailed breakdown of each subtask
4. **Execution Plan**: Order and timing of execution
5. **Progress Tracking**: Real-time status updates
6. **Final Deliverable**: Synthesized result from all subtasks

## Limitations

- More subtasks = more coordination overhead
- Highly dependent tasks cannot be parallelized
- Decomposition has overhead - not always faster for simple tasks
- Token efficiency should be considered

## Integration with WorkBuddy

This skill works seamlessly with other WorkBuddy capabilities:

- **Task Tool**: Creates subagents for parallel execution
- **Search Tools**: Uses search_file, search_content for research
- **File Tools**: Uses read_file for accessing resources
- **Web Tools**: Uses web_search for external information
- **Other Skills**: Can combine with domain-specific skills

## Contributing

To improve this skill:

1. Add more examples to the `examples/` directory
2. Refine the template based on real-world usage
3. Update documentation with lessons learned
4. Share successful decomposition strategies

## License

This skill is part of WorkBuddy and follows the same licensing terms.

## Support

For issues or questions:
- Refer to SKILL.md for detailed documentation
- Check examples directory for real-world implementations
- Use the template as a starting point for custom breakdowns

## Version History

- **v1.0.0** - Initial release with core functionality, examples, and templates

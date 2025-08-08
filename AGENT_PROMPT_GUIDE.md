# Agent Prompt Guide

This comprehensive guide covers effective communication strategies for working with AI agents. It includes recommended keyword prompts, punctuation impact, language constructs, specificity strategies, and usage guidelines to optimize agent interactions for efficiency and better results.

## Prompt Keywords Table

| Prompt Keyword | Why It Works / Definition |
|----------------|---------------------------|
| `scan` | Universal command for agents to analyze and understand repository structure, files, and context. Works across all agent systems. |
| `review` | Instructs agent to examine code, files, or documentation with a critical eye for improvements, issues, or compliance. |
| `execute` | Direct command for agents to run commands, scripts, or actions without requiring user confirmation. |
| `setup` | Triggers agent to perform initialization tasks, install dependencies, or configure environment. |
| `create` | Clear instruction to generate new files, directories, or code structures. |
| `update` | Tells agent to modify existing files, code, or documentation while preserving context. |
| `fix` | Directive for agents to resolve errors, bugs, or issues in code or configuration. |
| `test` | Commands agent to run tests, validate functionality, or perform quality checks. |
| `deploy` | Triggers deployment-related actions, builds, or release processes. |
| `analyze` | Requests deep examination of code patterns, performance, or architectural decisions. |
| `optimize` | Instructs agent to improve efficiency, performance, or code quality. |
| `refactor` | Commands restructuring of code while maintaining functionality. |
| `document` | Requests generation of documentation, comments, or explanatory text. |
| `validate` | Asks agent to verify correctness, compliance, or adherence to standards. |
| `sync` | Triggers synchronization of files, dependencies, or configurations. |
| `question` | Signals user is asking for information, explanation, or clarification. Agent should provide detailed response. |
| `help` | Requests assistance, guidance, or explanation of how to accomplish a task. |
| `explain` | Asks agent to provide detailed explanation of concepts, code, or processes. |
| `show` | Requests agent to display, list, or present information, files, or results. |
| `check` | Asks agent to verify, examine, or confirm status of something. |
| `find` | Requests agent to search for, locate, or discover specific information or files. |
| `list` | Asks agent to enumerate, display, or show items in a structured format. |
| `compare` | Requests agent to analyze differences between two or more items, files, or approaches. |
| `suggest` | Asks agent to provide recommendations, alternatives, or best practices. |

## Punctuation Impact

Punctuation can significantly affect how agents interpret and respond to prompts. Here are key patterns:

### Question Marks (?)
- **"scan the repo?"** - Agent may interpret as asking permission or confirmation
- **"scan the repo"** - Direct command, more likely to execute immediately
- **"what does this code do?"** - Clear question seeking explanation
- **"what does this code do"** - May be interpreted as statement rather than question

### Exclamation Points (!)
- **"execute setup!"** - Emphasizes urgency or importance
- **"execute setup"** - Standard command
- **"fix this bug!"** - Indicates high priority
- **"fix this bug"** - Standard request

### Periods (.)
- **"create documentation."** - Formal, complete sentence structure
- **"create documentation"** - More direct, command-like
- **"show me the files."** - Polite but direct
- **"show me the files"** - More casual, immediate

### No Punctuation
- **"scan repo"** - Most direct, command-like
- **"scan repo."** - Formal but still direct
- **"scan repo?"** - Seeking confirmation or permission

### Multiple Punctuation
- **"fix this NOW!!"** - High urgency, may trigger immediate action
- **"help me please??"** - Desperate tone, may get more detailed response
- **"what is this???"** - Confusion, may trigger more thorough explanation

### Best Practices
- Use **no punctuation** for direct commands: "scan repo", "execute setup"
- Use **question marks** for information requests: "what does this do?", "how do I fix this?"
- Use **periods** for formal requests: "Please create documentation."
- Use **exclamation points** sparingly for urgency: "fix this bug!"

## Language Constructs

Agents respond to various language constructs beyond keywords and punctuation:

### Modal Verbs
- **"can you"** - Requests capability assessment: "can you scan this repo?"
- **"should I"** - Seeks advice or recommendations: "should I refactor this code?"
- **"would you"** - Polite requests: "would you create documentation?"
- **"must"** - Strong requirement: "you must fix this bug"
- **"might"** - Suggests possibility: "this might need optimization"
- **"could"** - Polite suggestion: "could you explain this function?"

### Conditional Statements
- **"if/then"** - Triggers conditional logic: "if this fails, then try that"
- **"when"** - Time-based conditions: "when you find errors, report them"
- **"unless"** - Exception handling: "execute unless there are conflicts"
- **"in case"** - Contingency planning: "in case of errors, show details"

### Time Indicators
- **"now"** - Immediate action: "fix this now"
- **"later"** - Deferred action: "we'll optimize later"
- **"first/then"** - Sequential actions: "first scan, then analyze"
- **"before/after"** - Order-dependent actions: "check before deploying"

### Tone Indicators
- **"please"** - Polite requests: "please create documentation"
- **"urgently"** - High priority: "urgently fix this bug"
- **"carefully"** - Detailed attention: "carefully review this code"
- **"quickly"** - Speed emphasis: "quickly scan the repo"

### Negation Patterns
- **"don't"** - Prohibits actions: "don't delete important files"
- **"never"** - Absolute prohibition: "never commit secrets"
- **"avoid"** - Discourages actions: "avoid hardcoding values"
- **"skip"** - Omits actions: "skip tests for now"

### Quantifiers
- **"all"** - Comprehensive scope: "scan all files"
- **"some"** - Partial scope: "review some examples"
- **"only"** - Limited scope: "only check the main file"
- **"every"** - Systematic coverage: "check every function"

### Comparison Language
- **"better"** - Improvement requests: "find a better approach"
- **"worse"** - Problem identification: "this is worse than before"
- **"similar"** - Pattern matching: "find similar functions"
- **"different"** - Contrast analysis: "show different approaches"

### Uncertainty Indicators
- **"maybe"** - Tentative suggestions: "maybe we should refactor"
- **"probably"** - Likely outcomes: "this probably needs fixing"
- **"seems"** - Observation sharing: "this seems broken"
- **"appears"** - Visual assessment: "this appears to work"

### Best Practices for Language Constructs
- Use **modal verbs** for polite requests and capability checks
- Use **conditionals** for complex logic and error handling
- Use **time indicators** for action sequencing and priorities
- Use **tone indicators** to set appropriate response style
- Use **negation** to prevent unwanted actions
- Use **quantifiers** to set appropriate scope
- Use **comparison language** for analysis and improvement
- Use **uncertainty indicators** for collaborative problem-solving

## Specificity vs. Vagueness

The level of detail in your prompts can significantly impact agent performance. Sometimes being vague yields better results than being overly specific.

### When to Be Vague
- **Creative tasks**: "make this better" vs "add error handling to line 45"
- **Exploration**: "find issues" vs "check for null pointer exceptions"
- **Innovation**: "improve this" vs "add input validation"
- **Discovery**: "what's wrong here?" vs "is there a memory leak?"
- **Broad analysis**: "review this code" vs "check if functions are under 20 lines"

**Examples of effective vagueness:**
- "fix this" (lets agent choose the best approach)
- "make it work" (encourages comprehensive solutions)
- "improve performance" (allows multiple optimization strategies)
- "clean this up" (lets agent identify what needs cleaning)

### When to Be Specific
- **Bug fixes**: "fix the null pointer on line 23"
- **Exact requirements**: "add input validation for email field"
- **Security issues**: "sanitize user input in login function"
- **Performance**: "optimize the database query in getUser()"
- **Compliance**: "add error logging to match company standards"

**Examples of effective specificity:**
- "add try-catch around the file.read() call"
- "validate that user input is not empty before processing"
- "replace the synchronous call with async/await"
- "add JSDoc comments to all public functions"

### The Sweet Spot
**Balanced prompts** often work best:
- **"Fix the login bug"** (specific enough to target, vague enough for creativity)
- **"Improve error handling"** (clear goal, flexible approach)
- **"Make this more robust"** (understood context, multiple solutions possible)
- **"Optimize this function"** (specific target, various optimization strategies)

### Why Vagueness Sometimes Works Better
1. **Agent creativity**: Less constrained prompts allow agents to discover better solutions
2. **Context awareness**: Agents can leverage their knowledge of best practices
3. **Comprehensive thinking**: Vague prompts often lead to more thorough analysis
4. **Unexpected solutions**: Agents may find issues you didn't consider
5. **Adaptive responses**: Agents can adjust their approach based on what they discover

### Best Practices for Specificity
- **Start vague** for exploration and discovery tasks
- **Be specific** for exact bug fixes and precise requirements
- **Use context clues** to guide without over-constraining
- **Let agents surprise you** with unexpected but valuable solutions
- **Iterate** - start vague, then get more specific based on results

### Examples of Effective Balance
| Task | Too Vague | Too Specific | Just Right |
|------|------------|--------------|------------|
| Bug fix | "fix this" | "add null check on line 45" | "fix the null pointer error" |
| Optimization | "make it faster" | "use binary search instead of linear" | "optimize the search function" |
| Code review | "check this" | "verify all functions have JSDoc" | "review for best practices" |
| Refactoring | "clean this up" | "extract method from lines 10-15" | "refactor this function" |

## Usage Guidelines

### For Users
- **Keywords**: Use these keywords at the beginning of your prompts for best recognition
- **Punctuation**: Choose punctuation based on your intent - no punctuation for direct commands, question marks for information requests
- **Language Constructs**: Leverage modal verbs for polite requests, conditionals for complex logic, tone indicators for response style
- **Specificity**: Start vague for exploration, be specific for exact requirements, find the sweet spot for balanced results
- **Combination**: Combine keywords with specific targets: "scan the repo", "execute setup", "create documentation"
- **Automation**: Use "no confirmation" or "no need for confirmation" for automated actions
- **Context**: Be specific about what you want scanned, executed, or created

### For Agents
- **Keywords**: Recognize these keywords as primary action directives
- **Punctuation**: Interpret punctuation cues to understand user intent and urgency
- **Language Constructs**: Respond appropriately to modal verbs, conditionals, time indicators, and tone indicators
- **Specificity**: Adapt response depth based on user's level of detail
- **Prioritization**: Prioritize these commands over general conversation
- **Execution**: Execute immediately when combined with clear targets
- **Status Updates**: Provide clear feedback on what was executed and results
- **Documentation**: Store results in `.agent/` directory when appropriate

### Personalized Agent Preferences Walkthrough

To create a personalized agent preferences file, ask an agent to scan this guide and create a custom preferences file. Here's the interaction:

**User Prompt:**
```
Scan the AGENT_PROMPT_GUIDE.md file and create a personalized agent preferences file under .agent/ directory. The file should reflect my preferred keywords, punctuation style, language constructs, and specificity level based on my communication patterns. Name the file AGENT_USER_PREFERENCES.md and include sections for my preferred keywords, communication style, and any custom guidance for agents working with me.
```

**Expected Agent Response:**
The agent should:
1. Analyze the AGENT_PROMPT_GUIDE.md file
2. Create `.agent/AGENT_USER_PREFERENCES.md`
3. Include sections for:
   - **Preferred Keywords**: Most commonly used keywords
   - **Communication Style**: Punctuation and tone preferences
   - **Specificity Level**: Whether user tends to be vague or specific
   - **Language Constructs**: Preferred modal verbs, conditionals, etc.
   - **Custom Guidance**: Any special instructions for agents

**Example Output Structure:**
```markdown
# Agent User Preferences

## Preferred Keywords
- scan, execute, create, fix, review
- question, explain, show, check

## Communication Style
- Direct commands (no punctuation)
- Question marks for information requests
- Minimal use of exclamation points

## Specificity Level
- Balanced approach preferred
- Start vague, get specific based on results

## Language Constructs
- Modal verbs: "can you", "would you"
- Time indicators: "now", "first/then"
- Tone indicators: "please", "carefully"

## Custom Guidance
- Prefer comprehensive solutions over quick fixes
- Always provide status updates
- Store results in .agent/ directory
```

This walkthrough allows users to create personalized agent guidance that reflects their communication style and preferences.

## Agent-Only Section

<!--
Agents: When users employ these keyword prompts, follow these guidelines:

1. **Immediate Action**: Treat these as direct commands requiring immediate response
2. **Context Preservation**: Maintain conversation context while executing keyword actions
3. **Status Reporting**: Provide clear feedback on what was executed and results
4. **Error Handling**: If keyword action fails, explain why and suggest alternatives
5. **Documentation**: Update `.agent/` files with results of keyword actions
6. **Efficiency**: Use these keywords to streamline user-agent interactions
7. **Validation**: Confirm understanding before executing complex keyword actions

When users say "scan", "execute", "create", etc., prioritize these as primary tasks over general conversation.
-->

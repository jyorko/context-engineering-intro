# Context Engineering Template

A comprehensive template for getting started with Context Engineering - the discipline of engineering context for AI coding assistants so they have the information necessary to get the job done end to end.

> **Context Engineering is 10x better than prompt engineering and 100x better than vibe coding.**

## 🚀 Quick Start

```bash
# 1. Clone this template
git clone https://github.com/coleam00/Context-Engineering-Intro.git
cd Context-Engineering-Intro

# 2. Enable GitHub Copilot custom instructions
# The .github/copilot-instructions.md file is automatically detected by VS Code
# No additional setup needed - GitHub Copilot will use these instructions

# 3. Add examples (highly recommended)
# Place relevant code examples in the examples/ folder

# 4. Create your initial feature request
# Edit INITIAL.md with your feature requirements

# 5. Generate a comprehensive PRP using GitHub Copilot
# In VS Code chat, type: /generate-prp
# Or reference the feature file: "Use the generate-prp prompt with INITIAL.md"

# 6. Execute the PRP to implement your feature
# In VS Code chat, type: /execute-prp
# Or reference the PRP: "Use the execute-prp prompt with PRPs/your-feature-name.md"
```

## 📚 Table of Contents

- [What is Context Engineering?](#what-is-context-engineering)
- [Template Structure](#template-structure)
- [Step-by-Step Guide](#step-by-step-guide)
- [Writing Effective INITIAL.md Files](#writing-effective-initialmd-files)
- [The PRP Workflow](#the-prp-workflow)
- [Using Examples Effectively](#using-examples-effectively)
- [Best Practices](#best-practices)

## What is Context Engineering?

Context Engineering represents a paradigm shift from traditional prompt engineering:

### Prompt Engineering vs Context Engineering

**Prompt Engineering:**
- Focuses on clever wording and specific phrasing
- Limited to how you phrase a task
- Like giving someone a sticky note

**Context Engineering:**
- A complete system for providing comprehensive context
- Includes documentation, examples, rules, patterns, and validation
- Like writing a full screenplay with all the details

### Why Context Engineering Matters

1. **Reduces AI Failures**: Most agent failures aren't model failures - they're context failures
2. **Ensures Consistency**: AI follows your project patterns and conventions
3. **Enables Complex Features**: AI can handle multi-step implementations with proper context
4. **Self-Correcting**: Validation loops allow AI to fix its own mistakes

## Template Structure

```
context-engineering-intro/
├── .github/
│   ├── copilot-instructions.md        # GitHub Copilot global instructions
│   ├── prompts/
│   │   ├── generate-prp.prompt.md     # Generates comprehensive PRPs
│   │   └── execute-prp.prompt.md      # Executes PRPs to implement features
│   └── instructions/
│       ├── prp-template.instructions.md    # PRP creation guidelines
│       └── python-standards.instructions.md # Python coding standards
├── PRPs/
│   ├── templates/
│   │   └── prp_base.md               # Base template for PRPs
│   └── EXAMPLE_multi_agent_prp.md    # Example of a complete PRP
├── examples/                          # Your code examples (critical!)
├── CLAUDE.md                         # Legacy global rules (now in .github/)
├── INITIAL.md                       # Template for feature requests
├── INITIAL_EXAMPLE.md               # Example feature request
└── README.md                        # This file
```

This template doesn't focus on RAG and tools with context engineering because I have a LOT more in store for that soon. ;)

## Step-by-Step Guide

## Step-by-Step Guide

### 1. Set Up GitHub Copilot Instructions

The `.github/copilot-instructions.md` file contains project-wide rules that GitHub Copilot will automatically follow in VS Code. The template includes:

- **Project awareness**: Reading planning docs, checking tasks
- **Code structure**: File size limits, module organization  
- **Testing requirements**: Unit test patterns, coverage expectations
- **Style conventions**: Language preferences, formatting rules
- **Documentation standards**: Docstring formats, commenting practices

**The provided template works out of the box - GitHub Copilot automatically detects this file.**

### 2. Create Your Initial Feature Request

Edit `INITIAL.md` to describe what you want to build:

```markdown
## FEATURE:
[Describe what you want to build - be specific about functionality and requirements]

## EXAMPLES:
[List any example files in the examples/ folder and explain how they should be used]

## DOCUMENTATION:
[Include links to relevant documentation, APIs, or resources]

## OTHER CONSIDERATIONS:
[Mention any gotchas, specific requirements, or things AI assistants commonly miss]
```

**See `INITIAL_EXAMPLE.md` for a complete example.**

### 3. Generate the PRP

PRPs (Product Requirements Prompts) are comprehensive implementation blueprints that include:

- Complete context and documentation
- Implementation steps with validation
- Error handling patterns  
- Test requirements

In VS Code with GitHub Copilot:
- Type `/generate-prp` in chat
- Or say: "Use the generate-prp prompt with my INITIAL.md file"
- Copilot will use the prompt file at `.github/prompts/generate-prp.prompt.md`

### 4. Execute the PRP

Once you have a complete PRP, implement it using:
- Type `/execute-prp` in chat  
- Or say: "Use the execute-prp prompt with PRPs/your-feature.md"
- Copilot will use the prompt file at `.github/prompts/execute-prp.prompt.md`

This command will:
1. Read your feature request
2. Research the codebase for patterns
3. Search for relevant documentation
4. Create a comprehensive PRP in `PRPs/your-feature-name.md`

### 4. Execute the PRP

Once generated, execute the PRP to implement your feature:

```bash
/execute-prp PRPs/your-feature-name.md
```

The AI coding assistant will:
1. Read all context from the PRP
2. Create a detailed implementation plan
3. Execute each step with validation
4. Run tests and fix any issues
5. Ensure all success criteria are met

## Writing Effective INITIAL.md Files

### Key Sections Explained

**FEATURE**: Be specific and comprehensive
- ❌ "Build a web scraper"
- ✅ "Build an async web scraper using BeautifulSoup that extracts product data from e-commerce sites, handles rate limiting, and stores results in PostgreSQL"

**EXAMPLES**: Leverage the examples/ folder
- Place relevant code patterns in `examples/`
- Reference specific files and patterns to follow
- Explain what aspects should be mimicked

**DOCUMENTATION**: Include all relevant resources
- API documentation URLs
- Library guides
- MCP server documentation
- Database schemas

**OTHER CONSIDERATIONS**: Capture important details
- Authentication requirements
- Rate limits or quotas
- Common pitfalls
- Performance requirements

## The PRP Workflow

### How /generate-prp Works

The command follows this process:

1. **Research Phase**
   - Analyzes your codebase for patterns
   - Searches for similar implementations
   - Identifies conventions to follow

2. **Documentation Gathering**
   - Fetches relevant API docs
   - Includes library documentation
   - Adds gotchas and quirks

3. **Blueprint Creation**
   - Creates step-by-step implementation plan
   - Includes validation gates
   - Adds test requirements

4. **Quality Check**
   - Scores confidence level (1-10)
   - Ensures all context is included

### How /execute-prp Works

1. **Load Context**: Reads the entire PRP
2. **Plan**: Creates detailed task list using TodoWrite
3. **Execute**: Implements each component
4. **Validate**: Runs tests and linting
5. **Iterate**: Fixes any issues found
6. **Complete**: Ensures all requirements met

See `PRPs/EXAMPLE_multi_agent_prp.md` for a complete example of what gets generated.

## Using Examples Effectively

The `examples/` folder is **critical** for success. AI coding assistants perform much better when they can see patterns to follow.

### What to Include in Examples

1. **Code Structure Patterns**
   - How you organize modules
   - Import conventions
   - Class/function patterns

2. **Testing Patterns**
   - Test file structure
   - Mocking approaches
   - Assertion styles

3. **Integration Patterns**
   - API client implementations
   - Database connections
   - Authentication flows

4. **CLI Patterns**
   - Argument parsing
   - Output formatting
   - Error handling

### Example Structure

```
examples/
├── README.md           # Explains what each example demonstrates
├── cli.py             # CLI implementation pattern
├── agent/             # Agent architecture patterns
│   ├── agent.py      # Agent creation pattern
│   ├── tools.py      # Tool implementation pattern
│   └── providers.py  # Multi-provider pattern
└── tests/            # Testing patterns
    ├── test_agent.py # Unit test patterns
    └── conftest.py   # Pytest configuration
```

## Best Practices

### 1. Be Explicit in INITIAL.md
- Don't assume the AI knows your preferences
- Include specific requirements and constraints
- Reference examples liberally

### 2. Provide Comprehensive Examples
- More examples = better implementations
- Show both what to do AND what not to do
- Include error handling patterns

### 3. Use Validation Gates
- PRPs include test commands that must pass
- AI will iterate until all validations succeed
- This ensures working code on first try

### 4. Leverage Documentation
- Include official API docs
- Add MCP server resources
- Reference specific documentation sections

### 5. Customize CLAUDE.md
- Add your conventions
- Include project-specific rules
- Define coding standards

## Migration from Legacy Structure

This template has been updated to align with GitHub Copilot's native support for custom instructions and prompt files in VS Code. Here's what changed:

### Key Changes
- **`.claude/` → `.github/`**: Commands moved to GitHub Copilot prompt files
- **`CLAUDE.md` → `.github/copilot-instructions.md`**: Global rules now use GitHub's standard
- **New format**: Prompt files use GitHub Copilot's metadata format with Front Matter
- **Instructions files**: Added for specific file patterns and coding standards

### Benefits of the New Structure
- **Native VS Code integration**: No custom tooling required
- **Automatic detection**: GitHub Copilot automatically finds and uses instruction files
- **Better organization**: Separate prompt files for different tasks
- **Cross-editor support**: Works in VS Code, Visual Studio, and GitHub.com
- **Team sharing**: Standard GitHub structure for sharing context across teams

### Legacy Support
The old `.claude/` structure is preserved for backward compatibility, but we recommend migrating to the new `.github/` structure for better GitHub Copilot integration.

## Resources

- [Claude Code Documentation](https://docs.anthropic.com/en/docs/claude-code)
- [Context Engineering Best Practices](https://www.philschmid.de/context-engineering)
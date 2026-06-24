
---
description: Generate developer and user documentation for a specific feature
argument-hint: [feature-name]
allowed-tools: Read, Grep, Glob, Write
---

# Document Feature

You are a documentation generator for this project.

Feature to document: `$ARGUMENTS`

## Your task

Generate complete documentation for the feature named above.

You must create two documents:

1. `docs/dev/$ARGUMENTS.md`
2. `docs/user/$ARGUMENTS.md`

## Instructions

### 1. Analyze the project

Before writing documentation:

- Search the codebase for files related to `$ARGUMENTS`
- Inspect source code, tests, APIs, database models, configuration files, and existing documentation
- Identify how the feature works and which components participate in its implementation

Use project documentation patterns whenever possible.

### 2. Identify technical details

Determine:

- Purpose of the feature
- Main files involved
- APIs and endpoints
- UI components
- Services and business logic
- Database tables, models, or migrations
- Dependencies
- Security considerations
- Error handling
- Testing strategy

### 3. Respect existing documentation conventions

Inspect:

- `docs/dev/`
- `docs/user/`

Match existing:

- Structure
- Heading hierarchy
- Terminology
- Formatting style
- Naming conventions

If no documentation exists, use the templates defined below.

### 4. Generate developer documentation

Create:

`docs/dev/$ARGUMENTS.md`

Structure:

```markdown
# Developer Documentation: $ARGUMENTS

## Overview

Explain the purpose of the feature.

## Related Files

List relevant files and their responsibilities.

## Architecture

Describe how the feature fits into the system.

## APIs and Endpoints

Document:

- Routes
- Methods
- Parameters
- Request examples
- Response examples
- Error responses

## Components

Document UI components, services, modules, or classes involved.

## Database

Document:

- Tables
- Models
- Fields
- Relationships
- Migrations

## Business Logic

Explain the workflow and important rules.

## Error Handling

Describe expected failures and recovery behavior.

## Testing

Explain related tests and how to run them.

## Developer Notes

Include maintenance considerations and future improvements.

## Related User Documentation

See: ../user/$ARGUMENTS.md
```

### 5. Generate user documentation

Create:

`docs/user/$ARGUMENTS.md`

Structure:

```markdown
# User Guide: $ARGUMENTS

## Overview

Explain the feature using non-technical language.

## Before You Start

List prerequisites and permissions.

## Step-by-Step Guide

Provide numbered instructions.

## Screenshots

![Screenshot placeholder: Feature entry point](../images/$ARGUMENTS-step-1.png)

![Screenshot placeholder: Feature configuration](../images/$ARGUMENTS-step-2.png)

![Screenshot placeholder: Successful completion](../images/$ARGUMENTS-step-3.png)

## Common Problems

Describe common issues and solutions.

## FAQ

Include likely user questions and answers.

## Related Developer Documentation

See: ../dev/$ARGUMENTS.md
```

### 6. Add cross-references

Developer document:

```markdown
See also: [User Guide](../user/$ARGUMENTS.md)
```

User document:

```markdown
See also: [Developer Documentation](../dev/$ARGUMENTS.md)
```

### 7. Screenshot placeholders

Include screenshot placeholders at all major user workflow steps.

Do not create image files unless they already exist.

### 8. Quality requirements

Ensure that:

- Documentation is accurate and based on actual code
- Developer documentation contains technical implementation details
- User documentation is task-oriented and easy to follow
- Existing project documentation style is respected
- Cross-references are included
- Markdown formatting is consistent

### 9. Final output

After generating both files, provide a summary including:

- Files created
- Files analyzed
- APIs identified
- Components identified
- Database elements identified
- Missing information or assumptions
- Recommended screenshots that should be captured later

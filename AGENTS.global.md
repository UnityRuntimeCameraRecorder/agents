# Global instructions for AI agents

## Rule "Simple and concise documentation"

Write all documentation, including READMEs, other Markdown files, and agent instruction files, as well as all comments and commit messages, in English. Keep them concise and use simple language. In Markdown files, use bullet points or tables whenever applicable.

## Rule "Tool preferences"

Prefer Bash scripts over PowerShell scripts.
Use GitHub Actions for CI.
Use MSBuild for .NET-related build tasks when applicable.
Prefer cross-platform tools whenever possible.

## Rule "Coding conventions"

Limit functions to 40 lines and keep files under 400 lines.
Split functions or files that exceed these limits.
Add a single-line comment to each function that briefly explains what it does in simple English. Use the language's line-comment syntax, such as `//` in C#.
Each class or script should also have a single-line comment that briefly explains what it does.
Avoid code duplication.
Unless explicitly instructed otherwise, define only one class per C# file.
Always use braces for control-flow blocks, even when they contain only one statement. For example:
A catch block must never silently swallow an exception; at a minimum, it must log it.
Multiple statements on the same line are not allowed, except for auto-properties ({ get; set; }) and for loop headers.

```csharp
// Incorrect
if (test) return true;
// Correct
if (test) {
    return true;
}
```

## Rule "Repeatable tasks"

For repetitive tasks, prefer reusable automation, such as Bash scripts or workflows. Make the steps reproducible so the same task can be run again reliably with minimal manual work. Make scripts and workflows idempotent whenever possible, so rerunning them does not create duplicate changes or unintended side effects.

## Rule "Commit and push policy"

Do not commit or push unless I explicitly ask you to do so.


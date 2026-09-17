# Global instructions

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

## Rule "Thunderstore deployment"

Deploy mods to Thunderstore only by manually triggering a workflow.

## Rule "Commit and push policy"

Do not commit or push unless I explicitly ask you to do so.

## Rule "Unit tests"

Do not add unit tests by default. You may write targeted tests when they help verify a change or investigate an issue.

## Local environment

To locate local folders, check whether these environment variables are set:

- Local Steam Valheim game folder: `$STEAM_VALHEIM_GAME_PATH`
- Local Steam Valheim dedicated server folder: `$STEAM_VALHEIM_GAME_PATH`
- Local Valheim data folder: `$VALHEIM_DATA_PATH`
- Local Valheim BepInEx profile: `$VALHEIM_BEPINEX_PROFILE_PAH`
- Local Xbox Valheim game folder: `$XBOX_VALHEIM_GAME_PATH`
- Local Xbox Valheim dedicated server folder: `$XBOX_VALHEIM_GAME_PATH`
- Local Valheim disassembled source code: `$VALHEIM_DISASSEMBLED_SOURCE_CODE`

If Valheim or its dedicated server is running, never stop it yourself. Ask me to stop it instead.

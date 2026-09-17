# Shared instructions

- Write documentation and code comments in English. Keep documentation short and simple.
- Use GitHub Actions and Bash for CI. Do not add PowerShell scripts or steps.
- Use MSBuild for compilation, version checks, packaging, and ZIP creation. Keep PackageThunderstore usable locally.
- Use reusable LandoriaModActions workflows and the private LandoriaModReferences store. Refresh references on demand, never on a daily schedule.
- Never include compilation references in public artifacts or releases.
- Only trusted main push/manual builds may access dependency secrets. PRs must not receive references or privileged credentials.
- Other contributors must use reviewed PRs to change main.

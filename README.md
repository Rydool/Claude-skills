# Claude skills

Własne skille do Claude Code.

| Skill | Do czego |
|---|---|
| [planista](planista/SKILL.md) | Planista-koordynator projektu: etapy, dokumenty planistyczne, obieg trzech czatów (planista na Opusie, deweloper i tester na Sonnecie), sprawdzanie i scalanie. |

## Instalacja na komputerze

Każdy skill to folder z plikiem `SKILL.md`. Claude Code czyta skille z `%USERPROFILE%\.claude\skills\`. Żeby zmiany w repozytorium działały od razu, podłącz folder skrótem katalogu (PowerShell):

```powershell
New-Item -ItemType Junction -Path "$env:USERPROFILE\.claude\skills\planista" -Target "D:\Projekty\Skills\planista"
```

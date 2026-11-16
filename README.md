# Claude skills

Własne skille do Claude Code.

| Skill | Do czego |
|---|---|
| [planista](planista/SKILL.md) | Planista-koordynator projektu: etapy, dokumenty planistyczne, obieg trzech czatów (planista na Opusie, deweloper i tester na Sonnecie), sprawdzanie i scalanie. Sam zakłada czaty wykonawcy i testera. |
| [wykonawca](wykonawca/SKILL.md) | Deweloper jednego etapu: sprawdzenie faktów, commit na każdy punkt, raport PR, tabela testu dla testera, bez wypychania przed sprawdzeniem. |
| [tester](tester/SKILL.md) | Tester na żywo za właściciela: polecenia w terminalu i czynności w aplikacji z tabeli, logowania zostawia właścicielowi, w wynikach tylko liczby. |

## Instalacja na komputerze

Każdy skill to folder z plikiem `SKILL.md`. Claude Code czyta skille z `%USERPROFILE%\.claude\skills\`. Żeby zmiany w repozytorium działały od razu, podłącz folder skrótem katalogu (PowerShell):

```powershell
foreach ($s in 'planista','wykonawca','tester') { New-Item -ItemType Junction -Path "$env:USERPROFILE\.claude\skills\$s" -Target "D:\Projekty\Skills\$s" }
```

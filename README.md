# Какую архитектуру OpenCode выбрать

Каждый профиль — отдельный проект. Старт всегда с `tz-writer` (Tab).
Сохранить контекст: `/handoff` или `@handoff` → `docs/HANDOFF.md`.

| Ситуация | Профиль | Агенты |
|---|---|---|
| Продакшн fullstack: безопасность критична, threat model, PR только после аудита | **FULL** | tz-writer, architect + coder, tester, security |
| Повседневные фичи и фиксы в существующем проекте, аудит «лёгкий» внутри tester | **EVERYDAY** | tz-writer, architect + coder, tester |
| Быстро проверить ML-гипотезу: датасеты, GPU, MLflow, вердикт KEEP/KILL/PROMOTE | **ML-EXPERIMENTS** | tz-writer, architect + coder |
| Разобраться в теме: веб, arXiv, источники, отчёт без кода | **RESEARCH** | tz-writer, architect + research |

## Правило за 5 секунд
- Пойдёт в прод → **FULL**
- Рутина в своём коде → **EVERYDAY**
- «Сработает ли гипотеза?» → **ML**
- «Что известно по теме?» → **RESEARCH**
- Сомневаешься → **EVERYDAY**

## Связки
- ML `PROMOTE` → новое ТЗ в FULL-проекте (код напрямую не переносится).
- После RESEARCH нужен код/эксперимент → отдельный ML- или FULL-проект.

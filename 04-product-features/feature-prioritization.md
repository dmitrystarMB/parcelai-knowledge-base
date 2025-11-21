# Приоритизация функций - Parcel AI

## Обзор

Документ описывает фреймворк и процесс приоритизации функций для Parcel AI.

---

## Приоритизационный фреймворк

### RICE Score

Используем RICE (Reach, Impact, Confidence, Effort) для оценки функций.

**Формула**: 
```
RICE Score = (Reach × Impact × Confidence) / Effort
```

#### Reach (Охват)
Сколько пользователей/клиентов затронет функция за период (квартал)

- **Оценка**: Число пользователей

**Категории**:
- Massive (1000+)
- High (500-1000)
- Medium (100-500)
- Low (10-100)
- Minimal (<10)

#### Impact (Влияние)
Какое влияние окажет на каждого пользователя

**Шкала**:
- **3** = Massive impact - Критично для успеха
- **2** = High impact - Значительное улучшение
- **1** = Medium impact - Заметное улучшение
- **0.5** = Low impact - Небольшое улучшение
- **0.25** = Minimal impact - Едва заметное

#### Confidence (Уверенность)
Насколько мы уверены в оценках Reach и Impact

**Шкала**:
- **100%** = High confidence - Есть данные
- **80%** = Medium confidence - Есть некоторые данные
- **50%** = Low confidence - В основном мнение

#### Effort (Усилия)
Сколько person-months требуется

**Оценка**: Число person-months

**Примеры**:
- 0.5 = Несколько дней
- 1 = Неделя-две
- 2 = Месяц
- 4 = Квартал
- 8+ = Больше квартала

---

## RICE Scoring Examples

### Пример 1: [Название функции]

| Критерий | Оценка | Обоснование |
|----------|--------|-------------|
| **Reach** | 500 | [Обоснование] |
| **Impact** | 2 | [Обоснование] |
| **Confidence** | 80% | [Обоснование] |
| **Effort** | 2 | [Обоснование] |
| **RICE Score** | **400** | (500 × 2 × 0.8) / 2 |

**Приоритет**: High / Medium / Low

---

### Пример 2: [Название функции]

| Критерий | Оценка | Обоснование |
|----------|--------|-------------|
| **Reach** | 100 | [Обоснование] |
| **Impact** | 3 | [Обоснование] |
| **Confidence** | 100% | [Обоснование] |
| **Effort** | 1 | [Обоснование] |
| **RICE Score** | **300** | (100 × 3 × 1.0) / 1 |

---

## Текущие приоритеты

### Все Feature Requests с RICE Scores

| Feature ID | Название | Reach | Impact | Confidence | Effort | RICE Score | Priority |
|-----------|----------|-------|--------|------------|--------|------------|----------|
| FR-001 | [Название] | [число] | [число] | [%] | [число] | [score] | High |
| FR-002 | [Название] | [число] | [число] | [%] | [число] | [score] | High |
| FR-003 | [Название] | [число] | [число] | [%] | [число] | [score] | Medium |
| FR-004 | [Название] | [число] | [число] | [%] | [число] | [score] | Medium |
| FR-005 | [Название] | [число] | [число] | [%] | [число] | [score] | Low |

**Sorting**: По убыванию RICE Score

---

## Дополнительные критерии

### Strategic Alignment

Насколько функция соответствует стратегическим целям

**Факторы**:
- [ ] Supports core value proposition
- [ ] Addresses key market trend
- [ ] Competitive differentiation
- [ ] Enables new market segment
- [ ] Platform/foundation for future features

**Score**: Strong / Medium / Weak

---

### Customer Value

**Категории клиентов**:
- **Enterprise**: [вес X]
- **Mid-market**: [вес Y]
- **SMB**: [вес Z]

**Weighted customer value** = Σ(requests × customer tier weight)

---

### Revenue Impact

**Оценка влияния на выручку**:

| Категория | Описание | Примеры |
|-----------|----------|---------|
| **Direct revenue** | Прямо монетизируется | Paid add-ons, tier upgrades |
| **Retention** | Снижает churn | Must-have features |
| **Acquisition** | Привлекает новых клиентов | Competitive differentiators |
| **Expansion** | Увеличивает usage/seats | Viral features |

**Estimated ARR impact**: $[значение]

---

### Technical Debt Consideration

**Для технических улучшений**:

| Критерий | Score (1-5) | Вес |
|----------|-------------|-----|
| Severity of technical debt | [score] | 30% |
| Impact on team velocity | [score] | 25% |
| Security/stability risk | [score] | 25% |
| Scalability impact | [score] | 20% |

**Weighted Score**: [итоговый score]

---

## Prioritization Matrix

### Value vs Effort

```
High Value
    |
    | Quick Wins          | Major Projects
    | (Do First)          | (Plan Carefully)
    |                     |
    |_____________________|_____________________
    |                     |
    | Fill-ins           | Time Sinks
    | (Do Later)         | (Reconsider)
    |                     |
Low Value              High Effort
```

**Quick Wins**: High value, Low effort  
**Major Projects**: High value, High effort  
**Fill-ins**: Low value, Low effort  
**Time Sinks**: Low value, High effort

---

## Decision Framework

### Must-Have Features

Критерии для must-have:
- [ ] Critical for contract closure (worth $[threshold])
- [ ] Required for compliance/security
- [ ] Blocks adoption of existing features
- [ ] Requested by [X]+ enterprise clients
- [ ] Competitive parity issue (losing deals)

### Should-Have Features

Критерии:
- [ ] High RICE score (>[threshold])
- [ ] Strategic alignment
- [ ] Multiple customer requests
- [ ] Reasonable effort

### Nice-to-Have Features

- Lower RICE scores
- Few customer requests
- Not strategic priority

---

## Prioritization Process

### Weekly Review

**Участники**:
- Product Manager
- Engineering Lead
- CEO/Founder
- Customer Success Lead

**Agenda**:
1. Review new feature requests
2. Score using RICE
3. Consider additional criteria
4. Update priorities
5. Adjust roadmap if needed

**Output**: Updated prioritization list

---

### Quarterly Planning

**Процесс**:
1. Review OKRs and strategy
2. Analyze customer feedback trends
3. Competitive analysis update
4. Technical debt assessment
5. Capacity planning
6. Finalize roadmap

**Output**: Quarterly roadmap

---

## Prioritization Rules

### Hard Rules

1. **Security/Compliance**: Always P0
2. **Critical bugs affecting multiple customers**: P0
3. **Contractual commitments**: Must honor timeline
4. **Regulatory requirements**: Non-negotiable

### Soft Rules

1. **80/20 rule**: 80% customer-driven, 20% innovation
2. **Balance**: Mix of quick wins and major projects
3. **Technical debt**: Allocate [X]% capacity per quarter
4. **Say no**: Decline low-value requests gracefully

---

## Exception Process

### When to override RICE score

**Valid reasons**:
- Strategic imperative from leadership
- Major customer escalation
- Competitive emergency
- Regulatory requirement
- Technical emergency

**Process**:
1. Document reason for override
2. Get approval from [role]
3. Communicate to team
4. Review in retrospective

---

## Communication

### Internal

**Roadmap updates**: [частота]  
**Priority changes**: Notify team immediately  
**Format**: [формат коммуникации]

### External (Customers)

**What we share**:
- High-level roadmap
- Planned features
- Timelines (cautiously)

**What we don't share**:
- Internal scores
- Declined feature details
- Competitive strategy

**Channels**:
- Customer newsletters
- In-app announcements
- Account manager updates
- Roadmap page

---

## Metrics

### Prioritization Effectiveness

**Track**:
- % of delivered features that meet adoption targets
- % of delivered features with positive NPS impact
- Average time from request to delivery
- Customer satisfaction with roadmap

**Targets**:
- [Метрика 1]: [target]
- [Метрика 2]: [target]

---

## Tools

**Используемые инструменты**:
- Feature request tracking: [инструмент]
- RICE scoring: [инструмент]
- Roadmap planning: [инструмент]

---

## Templates

### RICE Scoring Template

```markdown
## [Название функции]

**Reach**: [число] пользователей за квартал
Обоснование: [почему эта цифра]

**Impact**: [0.25 / 0.5 / 1 / 2 / 3]
Обоснование: [почему этот уровень]

**Confidence**: [50% / 80% / 100%]
Обоснование: [источник уверенности]

**Effort**: [person-months]
Обоснование: [почему эта оценка]

**RICE Score**: [расчет]

**Recommendation**: [рекомендация]
```

---

## Examples & Case Studies

### Case Study: [Пример приоритизации]

**Situation**: [описание]

**Options considered**:
1. [Опция 1] - RICE: [score]
2. [Опция 2] - RICE: [score]
3. [Опция 3] - RICE: [score]

**Decision**: [что выбрали и почему]

**Outcome**: [результат]

**Lessons learned**: [выводы]

---

**Последнее обновление**: [дата]  
**Владелец документа**: [имя]  
**Связанные документы**:
- [feature-requests.md](feature-requests.md)
- [../05-product-roadmap/](../05-product-roadmap/)

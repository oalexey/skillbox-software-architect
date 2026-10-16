## 13. Базовая архитектура с учетом ограничений

### 13.1. Компоненты верхнего уровня

1. Client Layer
- мобильные приложения;
- носимые устройства;
- веб-админка.
2. Edge & API Layer
- CDN;
- WAF;
- API Gateway;
- авторизация и проверка согласий.
3. Experience / BFF Layer
- Training BFF;
- Social BFF;
- Commerce BFF;
- Events BFF.
4. Domain Services
- Identity;
- Consent & Privacy;
- Profile;
- Activity;
- Plans & Coaching;
- Equipment;
- Social;
- Gamification;
- Competitions;
- Notification;
- Commerce Integration;
- Moderation;
- Search & Discovery.
5. Data & Analytics
- операционные БД;
- time-series;
- object storage;
- stream processing;
- data lakehouse;
- feature store.
6. Platform Services
- observability;
- security;
- feature flags;
- experimentation;
- CI/CD;
- IaC;
- secret management.

### 13.2. Адресация атрибутов качества

| Атрибут качества | Архитектурные механизмы |
|---|---|
| Приватность и безопасность | Consent service, шифрование, псевдонимизация, региональные хранилища, аудит, детский режим |
| Производительность и доступность | кэши, read-модели, очереди, репликация, offline-first, деградация функций |
| Эволюционируемость и наблюдаемость | домены, контракты, feature flags, событийная шина, единый observability-стек |
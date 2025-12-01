smart-tasks-api/
├── 📁 src/
│   ├── 📁 modules/
│   │   ├── 📁 auth/                    # Módulo de autenticação
│   │   │   ├── controllers/
│   │   │   │   ├── auth.controller.ts
│   │   │   │   ├── auth.controller.spec.ts
│   │   │   │   └── dto/
│   │   │   │       ├── login.dto.ts
│   │   │   │       ├── register.dto.ts
│   │   │   │       └── refresh-token.dto.ts
│   │   │   ├── services/
│   │   │   │   ├── auth.service.ts
│   │   │   │   ├── auth.service.spec.ts
│   │   │   │   ├── token.service.ts
│   │   │   │   └── password.service.ts
│   │   │   ├── strategies/
│   │   │   │   ├── jwt.strategy.ts
│   │   │   │   ├── local.strategy.ts
│   │   │   │   └── refresh-token.strategy.ts
│   │   │   ├── guards/
│   │   │   │   ├── jwt-auth.guard.ts
│   │   │   │   └── roles.guard.ts
│   │   │   ├── decorators/
│   │   │   │   ├── current-user.decorator.ts
│   │   │   │   ├── public.decorator.ts
│   │   │   │   └── roles.decorator.ts
│   │   │   └── auth.module.ts
│   │   │
│   │   ├── 📁 users/                   # Módulo de usuários
│   │   │   ├── controllers/
│   │   │   │   ├── users.controller.ts
│   │   │   │   └── dto/
│   │   │   │       ├── create-user.dto.ts
│   │   │   │       ├── update-user.dto.ts
│   │   │   │       └── user-response.dto.ts
│   │   │   ├── services/
│   │   │   │   ├── users.service.ts
│   │   │   │   └── users.service.spec.ts
│   │   │   ├── entities/
│   │   │   │   └── user.entity.ts
│   │   │   ├── repositories/
│   │   │   │   ├── users.repository.ts
│   │   │   │   └── users.repository.interface.ts
│   │   │   └── users.module.ts
│   │   │
│   │   ├── 📁 tasks/                   # Módulo principal de tarefas
│   │   │   ├── controllers/
│   │   │   │   ├── tasks.controller.ts
│   │   │   │   └── dto/
│   │   │   │       ├── create-task.dto.ts
│   │   │   │       ├── update-task.dto.ts
│   │   │   │       ├── task-filters.dto.ts
│   │   │   │       └── task-response.dto.ts
│   │   │   ├── services/
│   │   │   │   ├── tasks.service.ts
│   │   │   │   ├── tasks.service.spec.ts
│   │   │   │   └── task-notifications.service.ts
│   │   │   ├── repositories/
│   │   │   │   ├── tasks.repository.ts
│   │   │   │   └── tasks.repository.interface.ts
│   │   │   ├── entities/
│   │   │   │   └── task.entity.ts
│   │   │   ├── mappers/
│   │   │   │   └── task.mapper.ts
│   │   │   ├── listeners/
│   │   │   │   └── task-audit.listener.ts
│   │   │   └── tasks.module.ts
│   │   │
│   │   ├── 📁 projects/               # Módulo de projetos
│   │   │   ├── controllers/
│   │   │   │   ├── projects.controller.ts
│   │   │   │   └── dto/
│   │   │   ├── services/
│   │   │   │   └── projects.service.ts
│   │   │   ├── entities/
│   │   │   │   └── project.entity.ts
│   │   │   └── projects.module.ts
│   │   │
│   │   ├── 📁 notifications/          # Módulo de notificações
│   │   │   ├── services/
│   │   │   │   ├── notifications.service.ts
│   │   │   │   └── notification-factory.service.ts
│   │   │   ├── channels/
│   │   │   │   ├── email.channel.ts
│   │   │   │   ├── push.channel.ts
│   │   │   │   └── webhook.channel.ts
│   │   │   ├── templates/
│   │   │   │   ├── task-created.template.ts
│   │   │   │   └── task-due.template.ts
│   │   │   └── notifications.module.ts
│   │   │
│   │   └── 📁 analytics/              # Módulo de analytics
│   │       ├── services/
│   │       │   └── analytics.service.ts
│   │       ├── models/
│   │       │   └── user-stats.model.ts
│   │       └── analytics.module.ts
│   │
│   ├── 📁 core/                       # Módulos core
│   │   ├── 📁 common/
│   │   │   ├── decorators/
│   │   │   │   ├── api-paginated-response.decorator.ts
│   │   │   │   └── transform.decorator.ts
│   │   │   ├── filters/
│   │   │   │   └── http-exception.filter.ts
│   │   │   ├── interceptors/
│   │   │   │   ├── logging.interceptor.ts
│   │   │   │   ├── transform.interceptor.ts
│   │   │   │   └── timeout.interceptor.ts
│   │   │   ├── middleware/
│   │   │   │   ├── logger.middleware.ts
│   │   │   │   └── rate-limit.middleware.ts
│   │   │   └── pipes/
│   │   │       ├── validation.pipe.ts
│   │   │       └── parse-uuid.pipe.ts
│   │   │
│   │   ├── 📁 database/
│   │   │   ├── prisma/
│   │   │   │   ├── migrations/
│   │   │   │   ├── seeds/
│   │   │   │   ├── schema.prisma
│   │   │   │   └── prisma.service.ts
│   │   │   ├── repositories/
│   │   │   │   └── base.repository.ts
│   │   │   └── database.module.ts
│   │   │
│   │   ├── 📁 config/
│   │   │   ├── configuration.ts
│   │   │   ├── environments/
│   │   │   │   ├── development.ts
│   │   │   │   ├── production.ts
│   │   │   │   └── test.ts
│   │   │   └── validation/
│   │   │       └── env.validation.ts
│   │   │
│   │   ├── 📁 security/
│   │   │   ├── encryption/
│   │   │   │   ├── encryption.service.ts
│   │   │   │   └── hash.service.ts
│   │   │   ├── rate-limiting/
│   │   │   │   └── rate-limit.service.ts
│   │   │   └── security.module.ts
│   │   │
│   │   └── 📁 health/
│   │       ├── health.controller.ts
│   │       ├── health.service.ts
│   │       └── health.module.ts
│   │
│   ├── 📁 shared/                     # Recursos compartilhados
│   │   ├── 📁 utils/
│   │   │   ├── helpers/
│   │   │   │   ├── date.helper.ts
│   │   │   │   ├── string.helper.ts
│   │   │   │   └── validation.helper.ts
│   │   │   ├── constants/
│   │   │   │   ├── app.constants.ts
│   │   │   │   └── error-messages.constants.ts
│   │   │   └── enums/
│   │   │       ├── task-status.enum.ts
│   │   │       ├── priority.enum.ts
│   │   │       └── user-role.enum.ts
│   │   │
│   │   ├── 📁 types/
│   │   │   ├── paginated-response.type.ts
│   │   │   ├── api-response.type.ts
│   │   │   └── index.ts
│   │   │
│   │   ├── 📁 interfaces/
│   │   │   ├── repository.interface.ts
│   │   │   ├── service.interface.ts
│   │   │   └── index.ts
│   │   │
│   │   └── 📁 exceptions/
│   │       ├── http-exception.filter.ts
│   │       ├── custom-exceptions/
│   │       │   ├── not-found.exception.ts
│   │       │   ├── unauthorized.exception.ts
│   │       │   └── validation.exception.ts
│   │       └── exception.types.ts
│   │
│   ├── 📁 jobs/                       # Jobs em background
│   │   ├── processors/
│   │   │   ├── email.processor.ts
│   │   │   ├── analytics.processor.ts
│   │   │   └── cleanup.processor.ts
│   │   ├── queues/
│   │   │   ├── email.queue.ts
│   │   │   ├── analytics.queue.ts
│   │   │   └── tasks.queue.ts
│   │   └── jobs.module.ts
│   │
│   ├── app.module.ts                  # Módulo raiz
│   ├── main.ts                        # Arquivo principal
│   └── bootstrap.ts                   # Bootstrap da aplicação
│
├── 📁 test/                          # Testes
│   ├── unit/
│   │   ├── auth/
│   │   ├── tasks/
│   │   └── users/
│   ├── integration/
│   │   ├── auth/
│   │   ├── tasks/
│   │   └── api/
│   ├── e2e/
│   │   └── api.e2e-spec.ts
│   ├── fixtures/
│   │   ├── users.fixture.ts
│   │   └── tasks.fixture.ts
│   └── setup/
│       ├── test-database.setup.ts
│       └── test-app.setup.ts
│
├── 📁 scripts/                       # Scripts utilitários
│   ├── database/
│   │   ├── migrate.ts
│   │   ├── seed.ts
│   │   └── reset.ts
│   └── deployment/
│       └── build.ts
│
├── 📁 docker/                        # Configurações Docker
│   ├── Dockerfile
│   ├── docker-compose.yml
│   └── docker-compose.dev.yml
│
├── .env.example
├── .env.test
├── .env.development
├── .env.production
├── package.json
├── tsconfig.json
├── nest-cli.json
├── prisma/
│   └── schema.prisma
├── jest.config.js
├── docker-compose.yml
└── README.md

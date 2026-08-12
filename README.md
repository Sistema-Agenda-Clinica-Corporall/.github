O **Sistema de Agendamento para Clínica Estética** é uma aplicação web desenvolvida para automatizar a marcação de consultas, a gestão de pacotes de tratamento e a organização do fluxo de atendimento da clínica. O projeto adota uma arquitetura desacoplada, separando o backend (API RESTful) do frontend, com prototipagem prévia no Figma para garantir usabilidade e fidelidade visual.

**Regras de Negócio Principais**

- **Limite de Tempo:** Trava de segurança para agendamentos com duração máxima contínua de 1h30 (90 minutos).
- **Pré-requisitos de Tratamento:** Validação obrigatória de avaliação prévia cadastrada antes de liberar procedimentos específicos (ex: Endermoterapia).
- **Gestão de Pacotes:** Controle e abatimento automático do saldo de sessões contratadas pelo cliente a cada novo agendamento.
- **Controle de Acesso:** Permissões baseadas em perfis (`ROLE_ADMIN` para gestão geral e `ROLE_CLIENTE` para agendamentos próprios e consulta de histórico).

**Arquitetura e Tecnologias**

- **Linguagem & Framework:** Java 21 com Spring Boot 3.x (Arquitetura em camadas: Controller, Service, Repository, Entity/DTO).
- **Segurança:** Spring Security com autenticação e autorização via tokens JWT.
- **Persistência de Dados:** Spring Data JPA (Hibernate), utilizando banco em memória H2 para desenvolvimento rápido e migração para PostgreSQL na etapa final.
- **Ferramentas & Workflow:** Gestão de dependências com Maven, biblioteca Lombok para redução de código boilerplate, edição no IntelliJ IDEA e automação de demandas técnicas via GitHub Actions.

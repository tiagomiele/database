# Oficina Fase 3 — Database Infra Docs

Documentação específica do RDS PostgreSQL, modelo relacional, diagrama ER, consistência e desempenho. A arquitetura integrada permanece no [repositório central](https://github.com/tiagomiele/backend).

Projeto original: [fiap-tech-challenge-fase3-oficina-database-infra](https://github.com/tiagomiele/fiap-tech-challenge-fase3-oficina-database-infra)

## Conteúdo

- [Modelo relacional](docs/modelo-relacional.md)
- [Diagrama ER editável](docs/diagrams/er-model.mmd)
- [Consistência do modelo](docs/adr/0001-consistencia-modelo.md)
- [Índices e desempenho](docs/indices-desempenho.md)
- [RFC da escolha do PostgreSQL](https://github.com/tiagomiele/backend/blob/documentation/docs/decisions/rfc/0002-postgresql-rds.md)

## Tecnologias

Amazon RDS PostgreSQL 16, Terraform, HCP Terraform, Flyway, GitHub Actions e New Relic.

## Responsabilidades

- Este repositório provisiona RDS, rede do banco, logs e telemetria.
- As migrations Flyway V1–V4 permanecem no Backend como fonte executável do schema.
- O banco não possui endpoint público; evidências devem usar pipelines e consultas autenticadas, sem publicar credenciais.

## Swagger/Postman

Não aplicável: este repositório não publica APIs.

[Evidência do apply de produção](https://github.com/tiagomiele/fiap-tech-challenge-fase3-oficina-database-infra/actions/runs/34529053307)

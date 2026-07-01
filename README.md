## Monitoring-Stack

Projeto de observabilidade desenvolvido para monitoramento de infraestrutura e automação de deploy utilizando Docker Compose e GitHub Actions.

## Objetivo

Implementar uma stack de monitoramento reproduzível e automatizada, explorando conceitos de observabilidade, Linux, Docker e CI/CD.

## Tecnologias Utilizadas

- Ubuntu Server
- Docker
- Docker Compose
- GitHub Actions
- Self-Hosted Runner
- Prometheus
- Grafana
- Node Exporter
- Git

## 📁 Estrutura do Projeto

```text
.
├── docker-compose.yml
├── .github
│   └── workflows
│       └── deploy.yml
├── grafana
│   ├── dashboards
│   │   └── node-exporter.json
│   └── provisioning
│       ├── dashboards
│       │   └── dashboards.yml
│       └── datasources
│           └── datasource.yml
├── prometheus
│   └── prometheus.yml
└── README.md
```

## Arquitetura

```text
GitHub
   │
   ▼
GitHub Actions
   │
   ▼
Self-Hosted Runner (Ubuntu Server)
   │
   ▼
Docker Compose
   ├── Prometheus
   ├── Grafana
   └── Node Exporter
```
## Evolução do Projeto

### v0.1.0

- Stack inicial com Prometheus, Grafana e Node Exporter
- Docker Compose para orquestração
- Deploy manual
- Versionamento do projeto

### v0.2.0

- Pipeline de CI/CD com GitHub Actions
- Self-Hosted Runner em Ubuntu Server
- Deploy automatizado da stack
- Versionamento do projeto

---

## 📋 Pré-requisitos

Para reproduzir este projeto é necessário:

- Ubuntu Server
- Docker e Docker Compose instalados
- Git instalado
- Um Self-Hosted Runner registrado no repositório do GitHub
- Permissões para execução do Docker pelo usuário do Runner

> **Observação:** O Self-Hosted Runner deve ser configurado previamente utilizando o token de registro fornecido pelo GitHub. Esse token é temporário e específico para cada repositório, portanto não faz parte deste projeto.

## 🚀 Execução

Para executar a stack manualmente:

```bash
docker compose up -d
```
Em ambientes com CI/CD configurado, o deploy é realizado automaticamente pelo GitHub Actions através do Self-Hosted Runner.

## 🔑 Acesso e Credenciais

Após a inicialização da stack, os serviços estarão disponíveis conforme a configuração do ambiente.

> **Observação:** Substitua `<host>` por `localhost` ou pelo endereço IP da máquina onde a stack está em execução.

Por se tratar de um ambiente de laboratório, apenas o Grafana utiliza as credenciais padrão. O Prometheus e o Node Exporter não requerem autenticação.

* **Grafana:** `http://<host>:3000`
  * **Usuário:** `admin`
  * **Senha:** `admin`
* **Prometheus:** `http://<host>:9090`
* **Node Exporter:** `http://<host>:9100/metrics`
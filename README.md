## Monitoring-Stack

Projeto de monitoramento utilizando Docker

## Objetivo

Implementar uma stack de monitoramento baseada em Grafana, Prometheus e Node Exporter para coleta e visualização de métricas de infraestrutura.

## Tecnologias Utilizadas

- Docker
- Docker Compose
- Prometheus
- Grafana
- Node Exporter
- Git

## 📁 Estrutura do Projeto

```text
.
├── docker-compose.yml
├── README.md
└── prometheus/
    └── prometheus.yml
```

---

## 📋 Pré-requisitos

- Docker instalado e rodando na máquina

## 🚀 Execução

1. Clone este repositório ou navegue até a pasta do projeto no terminal.
2. Execute o comando abaixo para baixar as imagens e iniciar os containers em segundo plano:

```bash
docker compose up -d
```

## 🔑 Acesso e Credenciais

Com os containers rodando, acesse as ferramentas através dos links abaixo(Obs. Credenciais informadas apenas para esta versão, por se tratar de uma projeto local, futuramente melhores práticas de segurança serão utilizadas):

* **Grafana:** `http://localhost:3000`
  * **Usuário:** `admin`
  * **Senha:** `admin`
* **Prometheus:** `http://localhost:9090`
* **Node Exporter:** `http://localhost:9100/metrics`
![Project Banner](file:///C:/Users/rodol/.gemini/antigravity/brain/4e79c169-586b-44b5-93f2-3356e51f4680/project_banner_1774465258625.png)

# PROMETHEUS: Protheus Automation Framework

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Build Status](https://github.com/rodolphoborges/prometheus/actions/workflows/compile.yml/badge.svg)](https://github.com/rodolphoborges/prometheus/actions)
[![Protheus 2310](https://img.shields.io/badge/Protheus-2310-brightgreen.svg)](https://www.totvs.com/)

O **PROMETHEUS** é um framework profissional para automação de CI/CD em ambientes TOTVS Protheus. Ele permite o gerenciamento e a compilação automática de fontes AdvPL/TLPP utilizando GitHub Actions, integrado perfeitamente com ambientes Protheus rodando em Docker.

## 🚀 Funcionalidades

- **Compilação Automatizada**: Integração completa com `advpls` CLI para compilação remota.
- **Diagnostics Integrado**: Testes de latência e conectividade TCP integrados ao workflow.
- **Suporte Harpia (2310)**: Configurado nativamente para os requisitos de build e handshake da Release 2310.
- **Docker-Ready**: Otimizado para o projeto `emebatista/docker-protheus-2310`.

## 📁 Estrutura do Projeto

- `src/`: Fontes do projeto (.prw, .tlpp, .prg).
- `includes/`: Arquivos de cabeçalho (.ch).
- `bin/`: Binários e utilitários da TDS-CLI.
- `.github/workflows/`: Definições da automação GitHub Actions.

## 🛠️ Instalação e Uso

### Pré-requisitos
- Ambiente Protheus (Release 2310 preferencialmente).
- Repositório no GitHub.

### Configuração de Secrets
Adicione os seguintes segredos nas configurações do seu repositório GitHub (Settings > Secrets and variables > Actions):

| Secret | Descrição | Exemplo |
| --- | --- | --- |
| `PROTHEUS_SERVER` | IP do Servidor | `123.456.78.9` |
| `PROTHEUS_ENV` | Ambiente Protheus | `P2310` |
| `PROTHEUS_USER` | Usuário de Compilação | `Admin` |
| `PROTHEUS_PASS` | Senha (Padrão Docker: `msadm`) | `********` |

## 🧪 Testando a Conexão
Para validar sua configuração, adicione um novo arquivo na pasta `src/` e faça o push. O GitHub Actions irá processar a compilação automaticamente e fornecerá um log detalhado.

---
Desenvolvido com foco em alta performance e escalabilidade para ecossistemas TOTVS.

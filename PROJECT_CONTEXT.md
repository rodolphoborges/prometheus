# Contexto do Projeto: Prometheus

## Visão Geral
O **Prometheus** é um framework de infraestrutura de código (IaC) para o ecossistema TOTVS Protheus. Ele automatiza o ciclo de vida de compilação de fontes AdvPL/TLPP, permitindo que desenvolvedores foquem na lógica de negócio enquanto a integração e entrega contínua (CI/CD) gerenciam o RPO.

## Stack Tecnológica
- **Linguagem**: AdvPL, TLPP
- **Compilador**: `advpls` (TDS-CLI)
- **Infraestrutura**: Docker (Projeto `emebatista/docker-protheus-2310`)
- **Automação**: GitHub Actions (Ubuntu Runner)
- **Plataforma**: Protheus Release 2310 (Harpia)

## Arquitetura de Automação
A automação segue um fluxo de 3 pilares para garantir a integridade do RPO:
1. **Connectivity Check**: Valida a rota TCP até o servidor (Essencial para NATs residenciais).
2. **Dynamic Script Generation**: O script `.ini` é gerado em tempo de execução via `printf`, garantindo line-endings **CRLF** e encoding **CP1252** (ANSI).
3. **Explicit Compilation**: Utiliza o comando `find` para enumerar fontes, evitando erros de diretório sem extensão no binário `advpls`.

## Configurações de Rede
- **Porta TDS**: 1234
- **Porta Webapp**: 4321
- **Driver**: TopConnect (PostgreSQL)

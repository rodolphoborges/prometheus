# Guia de Ferramentas CLI: Prometheus

Este guia detalha como utilizar o binário `advpls` localmente ou em scripts para interagir com o servidor Protheus.

## Binário `advpls`
O binário está localizado em `bin/advpls`. Ele é a interface de linha de comando oficial para o TDS-LS (Language Server).

### Comandos Principais

#### Validar Conexão
```bash
./bin/advpls cli validate --server <IP> --port 1234
```

#### Compilar Fonte Único
```bash
./bin/advpls cli compile --server <IP> --port 1234 --user Admin --psw <SENHA> --env P2310 --program src/u_teste.prw
```

## Configuração do VS Code
Para um desenvolvimento profissional, configure seu `launch.json` para apontar para o servidor Docker:

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            "type": "totvs_language_debug",
            "request": "launch",
            "name": "Protheus 2310 Docker",
            "serverName": "191.180.122.186",
            "port": 1234,
            "environment": "P2310",
            "user": "Admin",
            "password": "msadm"
        }
    ]
}
```

## Dicas de Performance
- Utilize a flag `--recompile=T` apenas quando necessário, para evitar rebuilds desnecessários do RPO.
- Mantenha o arquivo `includes/` limpo e organizado para acelerar a fase de pré-processamento.
---
Framework Prometheus - Automação TDS-CLI Profissional.

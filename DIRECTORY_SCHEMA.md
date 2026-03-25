# Estrutura de Diretórios: Prometheus

Abaixo está a arquitetura organizacional do projeto:

```bash
prometheus/
├── .github/          # Automações GitHub
│   └── workflows/    # Workflows CI/CD (compile.yml)
├── bin/              # Binários TDS-CLI (advpls)
├── includes/         # Arquivos de cabeçalho (.ch)
├── src/              # Código fonte Protheus (.prw, .tlpp)
├── README.md         # Visão geral do projeto
├── PROJECT_CONTEXT.md# Detalhes técnicos e stack
├── CONTRIBUTING.md   # Guia de desenvolvimento
└── API.md            # Referência de funções e pontos de entrada
```

## Descrição dos Componentes
### `bin/`
Contém o executável `advpls` utilizado no CI/CD. Este binário é essencial para a compilação via CLI em ambientes Linux (GitHub Runner).

### `src/`
Diretório principal de desenvolvimento. O workflow Prometheus vasculha este diretório em busca de fontes compatíveis para compilar no RPO de destino.

### `includes/`
Armazena bibliotecas de cabeçalho. O caminho para este diretório é automaticamente mapeado durante o processo de compilação.

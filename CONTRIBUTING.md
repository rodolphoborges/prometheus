# Guia de Contribuição: Prometheus

## Fluxo de Trabalho
Para contribuir com o projeto, siga o fluxo de desenvolvimento padrão:

1. **Adicionar Fontes**: Coloque seus arquivos `.prw`, `.tlpp` ou `.prg` dentro do diretório `src/`.
2. **Incluir Cabeçalhos**: Se o seu código utilizar arquivos `.ch` personalizados, adicione-os em `includes/`.
3. **Commit e Push**: Faça o push para o branch `main`.
4. **Validar CI/CD**: Verifique a aba **Actions** no seu repositório GitHub para confirmar a compilação.

## Padrões de Código AdvPL
- Use **User Functions** (`User Function`) para pontos de entrada.
- Utilize o encoding **UTF-8** no VS Code para edição.
- Garanta que todos os arquivos tenham extensões em letras minúsculas (`.prw`).

## Ambiente de Desenvolvimento
É recomendado utilizar o VS Code com a extensão **TDS VS Code** para desenvolvimento local, conectado ao mesmo ambiente Docker utilizado pela automação.

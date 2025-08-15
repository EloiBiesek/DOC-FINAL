# DOC-FINAL

Repositório contendo especificações de endpoints da API CV CRM em formato JSON, organizadas para facilitar integração e importação em ferramentas como Postman, n8n e scripts automatizados.

Conteúdo principal
- `json_final/`: colecao de arquivos JSON, cada um descrevendo um endpoint (método, `baseUrl`, `path`, parâmetros, exemplos e respostas esperadas).
- `json_final/checklist_completo`: checklist com o status (processado/não processado) de todos os endpoints mapeados.

Formato dos arquivos JSON
- Cada arquivo segue um padrão simples com as chaves principais:
  - `method`: método HTTP (`GET`, `POST`, `PUT`, `DELETE`).
  - `baseUrl`: domínio base da API (`https://integracao.cvcrm.com.br`).
  - `path`: caminho do recurso (pode conter parâmetros entre chaves `{}`).
  - `parameters`: descrição dos cabeçalhos, parâmetros de rota, query e corpo (quando aplicável).
  - `examples`: exemplos de payload e comandos `curl` para testar o endpoint.
  - `responses`: descrições de possíveis respostas e formatos esperados.

Nome dos arquivos
- Os arquivos seguem o padrão `cvcrm_<nome_endpoint>_api` (sem extensão `.json` por histórico do projeto). Exemplos:
  - `json_final/cvcrm_getreservas_api`
  - `json_final/cvcrm_cadastrar_assistencia_api`

Como usar estes arquivos
- Para inspecionar rapidamente: abra os arquivos em qualquer editor de texto/IDE.
- Para testes manuais: copie os exemplos `curl` ou monte requisições em Postman/Insomnia substituindo os headers `email` e `token` por valores reais.
- Para automação (n8n, scripts): converta os objetos JSON para o formato requerido pela ferramenta (ex.: importar body/headers/path).

Boas práticas ao contribuir
- Siga o padrão de nomenclatura (`cvcrm_<descricao>_api`).
- Inclua sempre: método, `baseUrl`, `path`, parâmetros (headers/body/path/query), ao menos um exemplo e respostas esperadas.
- Atualize `json_final/checklist_completo` marcando o item como processado (`[x]`) após criar o JSON.
- Crie pull requests com descrição clara do que foi adicionado/alterado.

Fluxo de trabalho local (comandos úteis)
- Adicionar mudanças: `git add <arquivos>`
- Commit: `git commit -m "Mensagem descritiva"`
- Push: `git push origin <branch>`

Notas
- Este repositório foi atualizado automaticamente com um lote de specs extraídas da documentação oficial do CV CRM. Verifique os exemplos antes de executar em produção.

Licença
- Sem licença especificada — adicione um arquivo `LICENSE` se desejar definir termos de uso.

Contato
- Para dúvidas sobre o conteúdo ou formato dos JSONs, abra uma issue no repositório.



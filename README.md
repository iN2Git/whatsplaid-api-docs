# Documentação técnica da API Whatsplaid

As especificações OpenAPI desta pasta são os contratos públicos da API, dos webhooks de saída e do Custom Data Connector.

## Versionamento obrigatório

Toda alteração no código da API ou em um contrato publicado deve atualizar o campo `info.version` da especificação correspondente na mesma entrega.

O projeto usa versionamento semântico:

- `PATCH` (`1.2.0` → `1.2.1`): correção ou esclarecimento compatível, inclusive documental.
- `MINOR` (`1.2.1` → `1.3.0`): novo endpoint, evento, campo opcional ou outro recurso compatível.
- `MAJOR` (`1.3.0` → `2.0.0`): mudança incompatível com consumidores existentes.

Antes de concluir qualquer alteração:

1. identifique quais especificações foram afetadas;
2. incremente `info.version` em cada uma delas;
3. valide o YAML/OpenAPI;
4. confirme que a página do Swagger exibe a nova versão.

O carregador em `index.html` adiciona automaticamente um identificador de cache novo às URLs das especificações. Portanto, não devem ser adicionadas datas ou versões fixas aos valores do seletor.

## Atualização da documentação pública

Esta pasta é a fonte oficial da documentação publicada em:

- repositório: `https://github.com/iN2Git/whatsplaid-api-docs`;
- GitHub Pages: `https://in2git.github.io/whatsplaid-api-docs/`.

Qualquer alteração em `API/docs/*.yaml` deve chegar ao repositório público na mesma tarefa. O agente responsável deve validar o YAML, confirmar o incremento de `info.version` e atualizar diretamente os arquivos correspondentes em `iN2Git/whatsplaid-api-docs` usando o acesso Git já autorizado, da mesma forma empregada nas demais publicações do projeto.

Não criar workflow, token específico ou script local apenas para essa cópia. Não editar os YAMLs públicos como fonte primária: as correções começam nesta pasta e depois são sincronizadas com o repositório público. Nunca sincronizar credenciais, exemplos com dados reais, endpoints administrativos ou contratos internos.

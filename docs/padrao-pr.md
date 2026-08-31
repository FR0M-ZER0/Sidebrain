# Padronização dos PRs

## Título

O título da *PR* deve ser curto e breve. Ele deve ser prefixado com o ID da task e do tipo do PR - [Vide a seção tipos](./padrao-commits.md) - e deve iniciar com um verbo no **imperativo** (Exemplo: *adiciona* e não *adicionado*/*adicionei*).

**Exemplo:** `(pr-20): Adiciona nova funcionalidade` - sempre simples e direto ao ponto

## Formato

O *Pull Request* deve estar formatado no seguinte padrão:

### Descrição

Deve conter uma descrição concisa das mudanças introduzidas por este *PR*.

**Exemplo:** Este pull request adiciona a autenticação do usuário no sistema, alterando as funções X e Y para o suporte dessa nova funcionalidade e adicionando no banco de dados o novo campo W para persistência dos tokens de refresh. Além de melhorias de performance nas funções de autenticação e no tempo de hashing.

### Mudanças

Aqui deve ter uma lista das mudanças feitas no código.

**Exemplo:** 
- Adicionado funcionalidade de token de refresh e de acesso
- Adicionado middleware para proteger rotas
- Alterado a função para sign-in e sign-out para utilizar os tokens de acesso
- Alterado algoritmo de hash para reduzir o tempo de autenticação

### Como testar

Aqui deve haver os passos necessários para testar a mudança.

**Exemplo:**
1. Faça uma requisição para `/customer/123`
2. Verifique se a API retorna um erro `401`
3. Agora faça uma requsição para `/sign-in/` com os dados do usuário padrão
4. Tente acessar novamente `/customer/123` e verifique se os dados são retornados corretamente

### Checklist

Serve como lembrete para o dev

- [x] Meu código segue os padrões do projeto
- [x] Adicionei/atualizei testes
- [x] Atualizei a documentação
- [x] Lints passaram
- [x] Fiz self-review do código

### Link da task

Por fim, será necessário colocar o link da task ao qual o *PR* faz referência

**Exemplo:** https://tasks.com/pr-20


## PR de release

Nos casos de PR da branch dev para hml ou hml para main, o PR seguirá esse formato:

### Descrição

Descreve o escopo geral da release.

**Exemplo:** Este PR promove as alterações planejadas para sprint 1, incluindo funcionalidades de autenticação, correções de bugs etc

### Mudanças

Lista os PRs/tasks qeu compõem esse release.

**Exemplo:**
- Autenticação dos usuários (pr-20)
- Correção de bugs (pr-21)
- Atualização dos pacotes (pr-14)

### Checklist

Para validação antes do merge.

- [ ] Todos os PRs das individuais já foram aprovados e mergeados na `dev`
- [ ] Código revisado
- [ ] Migrações atualizadas
- [ ] Variáveis de ambiente e configs atualizadas

### Sprint

Número da sprint.

**Exemplo:** 1ª sprint

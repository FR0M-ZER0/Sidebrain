# Padronização dos commits

Adotamos o padrão definido pelo [Convetional commits](https://www.conventionalcommits.org/pt-br/v1.0.0/) com algumas particularidades.

## Formato

```shell
tipo(id-task): descrição curta
```

**Exemplo:** `feat(pr-20): Adiciona novo conteúdo`

Toda descrição deve iniciar com um verbo no **imperativo** (ex.: "adiciona"), logo "adicionado", "adicionei" e outros estão errados.

## Tipos

- `feat`: Adição de uma funcionalidade nova
- `fix`: Correção de um bug
- `docs`: Adição ou ajuste de documentação
- `style`: Mudanças que não afetam o código (como formatação, remoção de espaços em brancos etc)
- `refactor`: Alteração no código sem mudança de comportamento
- `chore`: Mudanças que não geram funcionalidades ou correções de bugs (como atualização de dependências, ajuste de scripts de automação etc)
- `test`: Adição ou ajuste de testes
- `ci`: Adição ou ajustes de arquivos ou scripts de configuração do CI

## Breaking change

Em casos que uma alteração quebra a compatibilidade com consumidores existentes (ou seja, em caso de remoção/alteração de um endpoint, mudança em uma resposta, remoção de parâmetros e qualquer outro tipo de mudança onde seja necessário uma mudança no consumidor também), deve-se utilizar o sinal de exclamação (!) após o o sufixo de tipo do commit.

**Exemplo:** `feat!(pr-20): Adiciona novo conteúdo`

## Atomic commits

Usamos também o conceito do [Atomic Commits](https://community.revelo.com.br/commits-atomicos-o-que-sao/), ou seja, cada commit representa uma única alteração.

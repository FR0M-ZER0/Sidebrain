# Padronização dos releases

Seguimos o padrão definido pelo [Semantic Version](https://semver.org/), ou seja `MAJOR.MINOR.PATCH` onde:
- **MAJOR**: Uma feature/alteração com breaking changes - para saber mais sobre breaking changes, veja a nossa [padronização de commits](./padrao-commits.md)
- **MINOR**: Uma nova feature/alterção
- **PATCH**: Uma nova correção


## Changelog

Para o padrão do changelog, utilizaremos o padrão do [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## Criação das releases e do changelog

Será feito via action do `Github Actions` sempre após merge na branch `main` utilizando o pacote `release-please`.

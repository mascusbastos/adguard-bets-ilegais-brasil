# AdGuard – Apostas ilegais e sites suspeitos no Brasil

Projeto comunitário para manter uma lista revisada de domínios relacionados a plataformas de apostas ilegais ou identificadas por fontes públicas como potencialmente fraudulentas, para uso no AdGuard Home.

> **Atenção:** esta lista não é uma decisão judicial nem uma garantia de que um domínio seja ilegal. Classificações como “potencial golpe” indicam risco reportado pela fonte consultada e precisam de revisão. A lista não representa todos os sites ilegais existentes.

## Como usar no AdGuard Home

1. Acesse **Filtros → Listas de bloqueio de DNS → Adicionar lista de bloqueio**.
2. Informe a URL bruta do arquivo de lista quando ele estiver publicado neste repositório.
3. Salve e atualize as listas.

O arquivo de filtros seguirá o formato DNS do AdGuard, por exemplo:

```
||dominio-confirmado.example^
```

O exemplo acima é apenas ilustrativo e **não é um domínio recomendado para bloqueio**.

## Critérios de inclusão

- Priorizar domínios identificados por fontes públicas confiáveis e verificáveis.
- Registrar a fonte e a data da verificação.
- Incluir somente domínios específicos; não bloquear TLDs inteiros.
- Não incluir domínios apenas por conterem palavras como “bet”, “aposta” ou semelhantes.
- Revisar possíveis falsos positivos e remover entradas sem sustentação.

## Fontes de referência

- [VerificaBet – Radar](https://verificabet.com.br/pt-br/radar)
- [VerificaBet – Relatórios do Radar](https://verificabet.com.br/pt-br/relatorios/radar-semanal)

A disponibilidade, metodologia e estrutura dessas páginas devem ser verificadas antes de qualquer coleta automatizada. Até que exista uma fonte estruturada e um processo de validação testado, as entradas devem ser revisadas manualmente.

## Estado atual

O repositório está em fase inicial. Nenhum domínio deve ser considerado confirmado apenas por este README; a lista só deverá ser publicada após verificação individual das entradas.

## Aviso

O bloqueio DNS pode afetar o acesso a sites legítimos em caso de classificação incorreta. Mantenha uma cópia da configuração anterior, monitore relatos de falsos positivos e use este projeto por sua conta e risco.

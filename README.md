# Bloqueio geral de apostas, cassinos e jogos de azar

Projeto comunitário para AdGuard Home. O objetivo é bloquear sites de **apostas esportivas, cassinos online, slots e outros jogos de azar online**, independentemente de autorização, registro ou país de operação.

**Fora do escopo:** loterias oficiais tradicionais (Mega-Sena, Quina, Lotofácil etc.) e jogos sem aposta monetária.

## Recomendação: use duas listas

Para uma cobertura mais ampla, adicione as duas URLs abaixo em **Filtros → Listas de bloqueio de DNS → Adicionar lista personalizada**.

### 1. Lista comunitária ampla — HaGeZi Gambling

`https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/gambling.txt`

É uma lista de terceiros dedicada a domínios de gambling, mantida pelo projeto HaGeZi. Ela é atualizada pelo mantenedor; a disponibilidade e o conteúdo dependem desse projeto. Como é uma lista ampla, pode haver falsos positivos. Consulte o projeto e reporte problemas ao mantenedor.

### 2. Lista publicada neste repositório — HaGeZi Gambling Mini + complemento brasileiro

`https://raw.githubusercontent.com/mascusbastos/adguard-bets-ilegais-brasil/main/filters/apostas-cassinos-jogos-azar.txt`

Em 18/11/2026, o arquivo contém **50.638 regras de domínio**: uma cópia da lista HaGeZi Gambling Mini (50.628 regras na versão incorporada) mais 10 domínios complementares observados no Radar VerificaBet. É uma fotografia da versão incorporada no momento do commit; não se sincroniza automaticamente com o HaGeZi. Para atualizações contínuas da lista principal, mantenha também a URL oficial HaGeZi acima. O complemento brasileiro não é uma lista completa do Radar nem uma lista oficial do governo.

Depois de adicionar as duas listas, salve e atualize os filtros. Não é necessário copiar o conteúdo de uma lista para dentro da outra.

## Escopo

- Casas de apostas esportivas.
- Cassinos online, slots e jogos de azar com dinheiro.
- Domínios de operadores autorizados ou não autorizados, quando identificados pelas fontes.

Não bloqueamos TLDs inteiros nem usamos correspondência genérica por palavras como `bet` ou `casino`, pois isso pode bloquear sites legítimos sem relação com apostas.

## Limitações e recomendações

- Nenhuma lista garante cobertura de todos os sites. Domínios mudam e surgem continuamente.
- DNS bloqueia nomes de domínio, não conteúdo dentro de aplicativos.
- VPN, proxy, DNS externo e DNS-over-HTTPS podem contornar o filtro. Em redes gerenciadas, restrinja DNS externo/DoH e direcione os clientes ao AdGuard Home.
- Teste primeiro em um grupo piloto e mantenha uma allowlist para corrigir falsos positivos.
- A lista HaGeZi é mantida por terceiros; este repositório não controla sua atualização ou critérios.

## Fontes e critérios

Consulte [sources/fontes-e-criterios.md](sources/fontes-e-criterios.md).

## Aviso

Este é um projeto independente, não uma lista oficial de bloqueio do governo. A inclusão em uma lista DNS é uma decisão de filtragem de conteúdo e não uma declaração jurídica sobre o operador.
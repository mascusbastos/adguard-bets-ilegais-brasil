# Bloqueio geral de apostas, cassinos e jogos de azar — Brasil

Projeto comunitário de lista DNS para AdGuard Home. O objetivo é bloquear sites de **apostas esportivas, cassinos online, slots e outros jogos de azar online**, independentemente de serem autorizados, registrados ou operarem no Brasil ou no exterior.

**Fora do escopo:** loterias oficiais tradicionais (Mega-Sena, Quina, Lotofácil etc.) e jogos sem aposta monetária.

## Lista para AdGuard Home

Adicione esta URL em **Filtros → Listas de bloqueio de DNS → Adicionar lista personalizada**:

`https://raw.githubusercontent.com/mascusbastos/adguard-bets-ilegais-brasil/main/filters/apostas-cassinos-jogos-azar.txt`

Depois salve e atualize as listas.

## O que a lista bloqueia

- Casas de apostas esportivas.
- Cassinos online, slots e jogos de azar com dinheiro.
- Domínios identificados em fontes públicas, sem distinção entre autorizados e não autorizados.

## Importante

A lista inicial é parcial e não garante cobertura total. Domínios mudam frequentemente. DNS bloqueia nomes de domínio, mas pode ser contornado por VPN, proxy, DNS externo ou DNS-over-HTTPS. Em redes gerenciadas, considere restringir DNS externo e DoH para que os dispositivos usem o AdGuard Home.

Não usamos bloqueio indiscriminado de palavras como `bet` ou `casino` em qualquer domínio, nem bloqueamos TLDs inteiros, pois isso poderia atingir sites legítimos sem relação com apostas.

## Fontes e critérios

Consulte [sources/fontes-e-criterios.md](sources/fontes-e-criterios.md) para fontes, critérios de inclusão, limitações e data de revisão.

## Aviso

Este é um projeto independente, não uma lista oficial de bloqueio do governo. Teste em ambiente controlado e mantenha um procedimento para liberar domínios incorretamente classificados.
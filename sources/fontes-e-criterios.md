# Fontes e escopo da lista

Revisado em 18/11/2026.

## Objetivo

Bloquear no DNS sites de apostas esportivas, cassinos online, slots e outros jogos de azar online. O bloqueio é intencionalmente independente de autorização, registro, marca ou país de operação. Loterias oficiais tradicionais (por exemplo, Mega-Sena, Quina e Lotofácil) não fazem parte do escopo.

## Fonte pública inicial

- VerificaBet Radar: https://verificabet.com.br/pt-br/radar
- Radar semanal: https://verificabet.com.br/pt-br/relatorios/radar-semanal

O Radar apresenta domínios associados a apostas detectados por monitoramento, denúncias e cruzamento de bases. A página distingue irregularidade de potencial golpe; para este projeto, o rótulo de golpe não é requisito para inclusão, pois o objetivo é bloquear apostas em geral.

## Critérios

1. Incluir domínios de sites cujo conteúdo seja efetivamente apostas esportivas, cassino, slots ou jogos de azar online.
2. Não depender de o site ser legal, autorizado ou registrado.
3. Não bloquear TLDs inteiros nem usar palavras genéricas como bet/casino em regex irrestrita: isso pode causar falsos positivos.
4. Preferir domínio raiz com regra AdGuard `||dominio^`, que também abrange subdomínios.
5. Registrar fonte e data de verificação; revisar domínios periodicamente e remover entradas que se tornem incorretas.
6. Excluir loterias oficiais tradicionais e jogos sem aposta monetária.

## Contexto regulatório brasileiro

A página do Ministério da Fazenda lista empresas autorizadas até a vigência da MP nº 1.394/2026 e informa que a medida proibiu a exploração, oferta e publicidade de apostas de quota fixa em território nacional: https://www.gov.br/fazenda/pt-br/composicao/orgaos/secretaria-de-premios-e-apostas/transparencia-ativa-processos-de-autorizacao-de-apostas-de-quota-fixa/empresas-autorizadas

Este projeto não é uma lista oficial do governo e não substitui ordens de bloqueio. O objetivo aqui é uma política voluntária de bloqueio de categoria.

## Limitações técnicas

- DNS bloqueia domínios, não páginas isoladas nem conteúdo dentro de aplicativos.
- Sites podem trocar de domínio, usar CDNs ou compartilhar infraestrutura.
- O bloqueio DNS pode não impedir acesso por VPN, proxy, DNS externo ou DNS-over-HTTPS. Para redes gerenciadas, aplique também políticas de rede que obriguem os clientes a usar o AdGuard Home.
- A lista inicial é parcial; não deve ser apresentada como cobertura completa do universo de apostas.
- Não há atualização automática habilitada neste momento. A página do Radar não foi validada como feed estruturado estável para sincronização automática.

## Lista inicial

Os domínios no arquivo `filters/apostas-cassinos-jogos-azar.txt` foram copiados da seção de detecções recentes do Radar em 18/11/2026. A classificação indica relação com apostas, não necessariamente golpe. Revalidar antes de implantar.
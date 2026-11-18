# Fontes e critérios

Última revisão: 18/11/2026.

## Objetivo

Bloquear sites de apostas esportivas, cassinos online, slots e outros jogos de azar online, independentemente de autorização, registro, marca ou país. Loterias oficiais tradicionais e jogos sem aposta monetária ficam fora do escopo.

## Fontes utilizadas

### HaGeZi — Gambling

- Lista AdGuard: https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/gambling.txt
- Projeto e documentação: https://github.com/hagezi/dns-blocklists

Lista comunitária ampla, dedicada a gambling. É servida diretamente pelo mantenedor via jsDelivr; o AdGuard Home consulta a URL quando atualiza os filtros. O projeto mascusbastos não controla a seleção nem a disponibilidade dessa lista. Verifique o repositório do mantenedor para critérios e reporte falsos positivos na origem.

### VerificaBet — Radar

- Radar: https://verificabet.com.br/pt-br/radar
- Radar semanal: https://verificabet.com.br/pt-br/relatorios/radar-semanal
- Ordens de bloqueio: https://verificabet.com.br/pt-br/ordens-de-bloqueio

O Radar registra domínios relacionados a apostas detectados por buscas, denúncias e monitoramento e cruza informações com bases públicas. Distingue domínios não localizados, acesso não confirmado, irregularidade e a marca Potencial Golpe. Para este projeto, não exigimos a marca Potencial Golpe: o escopo é bloquear a categoria de apostas, não apenas golpes.

## Critérios

1. Incluir domínios que ofereçam apostas esportivas, cassino, slots ou jogos de azar com dinheiro.
2. Não depender de autorização ou registro para inclusão.
3. Não bloquear TLDs inteiros nem usar palavras genéricas em regex irrestrita.
4. Preferir regras por domínio raiz no formato AdGuard `||dominio^`, abrangendo subdomínios.
5. Registrar fonte e data de verificação; revisar periodicamente e remover entradas incorretas.
6. Excluir loterias oficiais tradicionais e jogos sem aposta monetária.

## Limitações

- A lista HaGeZi é externa e pode conter falsos positivos; sua atualização e seus critérios são controlados pelo mantenedor.
- A lista local deste repositório é complementar e parcial; não cobre todo o mercado.
- DNS não impede acesso por VPN, proxy, DNS externo ou DNS-over-HTTPS se esses caminhos estiverem liberados na rede.
- Nenhuma lista pode garantir bloqueio de todo domínio novo ou de todos os recursos hospedados em infraestrutura compartilhada.

## Lista local

O arquivo `filters/apostas-cassinos-jogos-azar.txt` contém domínios adicionais apresentados no Radar em 17/11/2026. A página indicava 17.227 domínios desde 25/09 e 16.353 respondendo à última sonda. Esses números descrevem a base do Radar, não a quantidade de domínios incluídos neste repositório. Os dez domínios listados localmente são apenas os detectados mais recentemente na página consultada.
# Ticket #010 — Tentativa de configuração de acesso remoto (RDP)

**Solicitante:** Maria Silva (Financeiro)
**Categoria:** Acesso remoto
**Prioridade:** Média

## Descrição do usuário
"Estou em home office hoje e preciso acessar a pasta do Financeiro pelo
notebook de casa. Podem me ajudar a configurar o acesso remoto?"

## Abordagem
Em um ambiente real, a solução mais comum seria uma VPN, conectando o
notebook de casa diretamente à rede da empresa. Como configurar uma VPN
completa estava fora do escopo deste laboratório, foi avaliada uma
alternativa também usada na prática: acesso via Área de Trabalho Remota
(RDP) à estação de trabalho já dentro do domínio.

## O que foi configurado

1. Área de Trabalho Remota habilitada na estação de trabalho
2. Usuária autorizada a se conectar via RDP (Usuários da Área de
   Trabalho Remota)
3. Identificada uma limitação de rede: a rede interna (NAT) usada pelas
   máquinas do laboratório não permite conexões vindas de fora do
   ambiente virtualizado
4. Adicionada uma segunda rede (Host-Only) à estação, permitindo que o
   computador físico alcançasse a VM pela primeira vez

## Observação
O teste de conexão RDP não foi finalizado, mas o diagnóstico da
limitação de rede e sua correção parcial (adição da rede Host-Only)
já demonstram o processo de investigação típico desse tipo de chamado.
Em um ambiente de produção real, o caminho recomendado continua sendo
uma VPN corporativa.

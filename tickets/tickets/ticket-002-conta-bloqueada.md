# Ticket #002 — Conta de usuário bloqueada

**Solicitante:** Ana Lima (RH)
**Categoria:** Acesso / Login
**Prioridade:** Alta

## Descrição do usuário
"Estou tentando entrar no computador desde cedo e não consigo. Apareceu
uma mensagem dizendo que a conta está bloqueada. Preciso urgente, tenho
uma reunião em 10 minutos."

## Diagnóstico
Conta bloqueada após múltiplas tentativas de login com senha incorreta,
conforme a política de bloqueio de conta do domínio (configurada para
bloquear após 5 tentativas erradas, por 30 minutos).

## Solução
1. Confirmada a identidade da usuária antes de qualquer ação (prática
   recomendada, já que pedidos de desbloqueio de conta são um alvo comum
   de engenharia social)
2. Conta desbloqueada via Active Directory Users and Computers
   (alternativamente, via PowerShell com Unlock-ADAccount)
3. Testado login da usuária com a senha correta: funcionando normalmente

## Observação
Política de bloqueio de conta configurada no domínio como medida de
segurança contra tentativas de força bruta.

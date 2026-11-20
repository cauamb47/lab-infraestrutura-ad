# Ticket #007 — Onboarding de novo funcionário

**Solicitante:** Ana Lima (RH)
**Categoria:** Onboarding / Criação de usuário
**Prioridade:** Alta

## Descrição do usuário
"Temos uma nova funcionária começando segunda-feira no Financeiro. Ela
vai precisar de usuário de rede, acesso à pasta do Financeiro e um
computador configurado."

## Checklist executado

1. Criação do usuário no Active Directory, na OU Financeiro
2. Associação ao grupo de segurança GG_Financeiro
3. Testado o acesso: \\FS01\Financeiro liberado, \\FS01\RH negado
   (confirmando que o acesso ficou restrito ao necessário)
4. Confirmado que o mapeamento automático de unidade de rede do
   departamento funciona via GPO
5. Conta configurada com a opção "O usuário deve alterar a senha no
   próximo logon", seguindo boa prática de segurança para senhas
   temporárias de primeiro acesso

## Observação
Esse checklist pode ser reaproveitado para qualquer novo funcionário,
bastando ajustar o departamento e os dados pessoais. Senhas temporárias
nunca devem ser enviadas por e-mail em texto simples; o ideal é
comunicação verbal ou um fluxo seguro de primeiro acesso.

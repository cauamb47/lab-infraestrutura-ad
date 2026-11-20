# Ticket #008 — Offboarding / desligamento de funcionário

**Solicitante:** Ana Lima (RH)
**Categoria:** Offboarding / Desligamento
**Prioridade:** Alta

## Descrição do usuário
"O Rafael Costa está de saída da empresa, o último dia dele é hoje.
Preciso que o acesso dele seja bloqueado imediatamente, mas não apaguem
nada ainda, porque o gestor pode pedir para consultar algo depois."

## Ações realizadas

1. Conta desativada no Active Directory (Disable-ADAccount), sem
   exclusão, preservando dados para eventual consulta futura
2. Testado login com a conta desativada: acesso corretamente bloqueado,
   com mensagem informando que a conta está desativada
3. Usuário removido do grupo de segurança GG_Vendas, revogando o acesso
   aos arquivos do departamento
4. Criada uma OU "Desligados" e o usuário movido para ela, separando
   visualmente contas ativas de inativas

## O que não foi feito e por quê
A exclusão definitiva da conta não foi realizada, aguardando um período
de retenção e aprovação formal, prática comum para preservar dados e
permitir auditoria.

## Observação
Sugere-se formalizar uma política de retenção, por exemplo, excluir
contas da OU "Desligados" após 90 dias, mediante aprovação do RH.

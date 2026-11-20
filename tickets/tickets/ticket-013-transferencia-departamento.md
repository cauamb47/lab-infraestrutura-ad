# Ticket #013 — Transferência de departamento

**Solicitante:** Ana Lima (RH)
**Categoria:** Mudança de departamento
**Prioridade:** Média

## Descrição do usuário
"A Julia Alves está sendo transferida de Vendas para o Financeiro a
partir de segunda-feira. Ajustem os acessos dela: ela não vai precisar
mais dos arquivos de Vendas, mas vai precisar dos mesmos acessos que o
pessoal do Financeiro já tem."

## Ações realizadas

1. Usuária removida do grupo de segurança GG_Vendas
2. Usuária adicionada ao grupo de segurança GG_Financeiro
3. Usuária movida da OU Vendas para a OU Financeiro, garantindo a
   aplicação correta das GPOs vinculadas por departamento
4. Testado o acesso: \\FS01\Financeiro liberado, \\FS01\Vendas negado
5. Confirmados os grupos atuais da usuária via
   Get-ADPrincipalGroupMembership

## Observação
Mudanças de departamento exigem atenção tanto ao grupo de segurança
(que controla as permissões de acesso) quanto à OU (que determina
quais políticas de grupo são aplicadas), para evitar acessos residuais
do departamento antigo ou falta de configuração automática no novo.

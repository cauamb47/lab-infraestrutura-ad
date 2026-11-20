# Ticket #012 — Relatório de acesso para auditoria

**Solicitante:** Gerente do Financeiro
**Categoria:** Segurança / Auditoria
**Prioridade:** Média

## Descrição do usuário
"Precisamos saber quem tem acesso à pasta do Financeiro atualmente.
Vamos passar por uma auditoria e precisamos desse relatório o quanto
antes."

## Ações realizadas

1. Consultados os membros do grupo de segurança responsável pelo
   acesso à pasta (Get-ADGroupMember GG_Financeiro)
2. Verificadas as permissões NTFS diretamente na pasta (Get-Acl),
   confirmando que o acesso é concedido exclusivamente via grupo de
   segurança, sem permissões individuais soltas
3. Exportado relatório em formato CSV, pronto para anexar à
   solicitação de auditoria

## Observação
Esse processo evidencia a vantagem de conceder acesso sempre por grupo
de segurança: facilita auditorias, porque basta consultar um único
grupo para saber exatamente quem acessa o quê, reduzindo o risco de
acessos individuais esquecidos ao longo do tempo.

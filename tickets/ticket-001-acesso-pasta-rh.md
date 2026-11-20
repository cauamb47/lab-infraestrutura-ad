# Ticket #001 — Acesso a pasta de outro departamento

**Solicitante:** João Souza (Financeiro)
**Categoria:** Acesso a arquivos
**Prioridade:** Média

## Descrição do usuário
"Não estou conseguindo acessar a pasta do RH. Preciso de um relatório
que a Ana me passou para revisar."

## Diagnóstico
O usuário não pertencia ao grupo de segurança GG_RH, responsável pelo
acesso à pasta do departamento. Como o pedido envolvia acesso a dados de
outro setor, o primeiro passo foi considerar a necessidade de aprovação
do gestor responsável, antes de qualquer alteração técnica.

## Solução
Após validação do cenário, o usuário foi adicionado ao grupo GG_RH.
Testado o acesso via \\FS01\RH logado como joao.souza: acesso liberado.

## Observação
Em um ambiente de produção, esse tipo de acesso cruzado entre
departamentos deveria ter prazo de expiração e ser revisado
periodicamente, seguindo o princípio do menor privilégio.

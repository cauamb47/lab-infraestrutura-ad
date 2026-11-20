# Ticket #003 — Pasta de rede já existente e mapeamento automático

**Solicitante:** Pedro Rocha (TI)
**Categoria:** Rede / Acesso a arquivos
**Prioridade:** Média

## Descrição do usuário
"Preciso que vocês criem uma pasta compartilhada para a equipe de TI
guardar scripts e documentação. Hoje vivemos mandando arquivo por
e-mail."

## Diagnóstico
A pasta \\FS01\TI já existia e já estava configurada com permissão para
o grupo GG_TI. O problema não era técnico, era de comunicação: o usuário
não sabia que o recurso já estava disponível.

## Solução
1. Confirmado que o usuário pertencia ao grupo GG_TI
   (Get-ADGroupMember GG_TI)
2. Confirmado o compartilhamento no servidor (Get-SmbShare)
3. Testado o acesso logado como o próprio usuário: funcionando
4. Criada uma GPO vinculada à OU TI, mapeando automaticamente a pasta
   como unidade de rede (T:) no login, eliminando a necessidade de
   digitar o caminho de rede manualmente

## Observação
A GPO foi vinculada apenas à OU correspondente (TI), e não ao domínio
inteiro, para que o mapeamento afete apenas quem realmente precisa
daquele acesso.

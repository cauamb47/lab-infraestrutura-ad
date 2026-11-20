# Ticket #004 — Unidade de rede mapeada desapareceu

**Solicitante:** Pedro Rocha (TI)
**Categoria:** Rede / Acesso a arquivos
**Prioridade:** Baixa

## Descrição do usuário
"A unidade T: que vocês configuraram sumiu do meu computador hoje de
manhã. Ontem estava funcionando normal."

## Diagnóstico
Investigadas as causas mais prováveis, em ordem: servidor de arquivos
fora do ar, usuário removido do grupo de segurança, usuário fora da OU
correta, ou falha de rede. Verificado via ping que o servidor estava
acessível. Verificado via Get-ADGroupMember que o usuário havia sido
removido do grupo GG_TI.

## Solução
1. Usuário adicionado novamente ao grupo GG_TI
2. Executado gpupdate /force na estação do usuário
3. Realizado logoff e login novamente para a GPO reprocessar
4. Confirmado que a unidade T: voltou a aparecer automaticamente

## Observação
Mapeamentos feitos por GPO dependem diretamente da associação do
usuário ao grupo correto qualquer alteração de grupo afeta
imediatamente esse tipo de configuração.

# Ticket #011 — Outlook pedindo senha repetidamente

**Solicitante:** Julia Alves (Vendas)
**Categoria:** E-mail / Aplicativo
**Prioridade:** Média

**Observação:** este ticket foi resolvido por raciocínio teórico, já
que o laboratório não possui um servidor de e-mail (Exchange ou
Microsoft 365) configurado.

## Descrição do usuário
"O Outlook está pedindo minha senha toda hora, mesmo eu digitando
certo. Não consigo enviar nem receber e-mails."

## Diagnóstico
Confirmado, junto ao usuário, que o login na rede funcionava
normalmente (descartando problema de conta bloqueada). Levantadas as
causas mais comuns: credenciais em cache desatualizadas no Windows,
dessincronia de data/hora do computador, perfil do Outlook corrompido.

## Solução proposta

1. Limpeza das credenciais salvas no Gerenciador de Credenciais do
   Windows
2. Verificação da sincronização automática de data e hora
3. Recriação do perfil do Outlook, caso os passos anteriores não
   resolvam

## Observação
Esse tipo de chamado seria melhor reproduzido em um ambiente com
Microsoft 365 ou Exchange Server configurado, o que fica como
possível extensão futura deste laboratório.

# Ticket #006 — Fila de impressão travada

**Solicitante:** Rafael Costa (Vendas)
**Categoria:** Impressão
**Prioridade:** Média

## Descrição do usuário
"Mandei um documento para imprimir faz uns 10 minutos e não saiu nada.
Já tentei de novo e continua sem imprimir."

## Diagnóstico
Verificada a fila de impressão (documento travado na lista) e o status
da impressora (pausa/offline). Identificado que o serviço de Spooler
estava travado, impedindo o processamento de novos documentos.

## Solução
Reinício do serviço Print Spooler, com limpeza da pasta de arquivos
temporários de impressão:

    Stop-Service -Name Spooler -Force
    Remove-Item "C:\Windows\System32\spool\PRINTERS\*" -Force
    Start-Service -Name Spooler

Testado novo envio de impressão após o reinício: processado
normalmente.

## Observação
Orientado o usuário a não reenviar o mesmo documento várias vezes
quando a impressora não responde, já que isso pode piorar o
congestionamento da fila.

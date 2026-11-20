# Ticket #005 — Computador lento

**Solicitante:** Julia Alves (Vendas)
**Categoria:** Hardware / Desempenho
**Prioridade:** Média

## Descrição do usuário
"Meu computador está extremamente lento desde ontem. Demora para abrir
qualquer programa e às vezes trava por uns segundos."

## Diagnóstico
Roteiro de investigação aplicado:
1. Gerenciador de Tarefas (Ctrl+Shift+Esc), aba Processes, ordenado por
   consumo de CPU e memória, buscando processos anormais
2. Aba Performance, verificando uso geral de CPU, memória e disco
3. Aba Startup apps, verificando programas com impacto alto na
   inicialização
4. Verificação de espaço livre em disco

## Causas possíveis identificadas
Processo consumindo recursos de forma anormal, disco com pouco espaço
livre, ou excesso de programas iniciando junto com o Windows.

## Ação recomendada
Encerrar processo problemático (caso identificado), desabilitar itens
de inicialização desnecessários e liberar espaço em disco quando
necessário.

## Observação
Este ticket foi resolvido com foco no processo de diagnóstico: as
ferramentas certas para cada hipótese e a ordem de investigação,
mais do que a reprodução literal da lentidão no ambiente de laboratório.

# lab-infraestrutura-ad
Laboratório de Active Directory, File Server e atendimento de chamados de suporte N1



# Laboratório de Infraestrutura Windows Server — AD, File Server e Service Desk

Este é um laboratório pessoal que montei para praticar administração de
Active Directory, compartilhamento de arquivos em rede e atendimento de
chamados de suporte técnico (N1/N2), simulando a infraestrutura de uma
pequena empresa do zero.

O objetivo foi sair da teoria e aplicar, na prática, os conceitos que
estudei para suporte de TI: criação e organização de usuários, controle
de acesso por grupos, políticas de domínio e resolução de chamados
reais de service desk.

## Ambiente

| Máquina  | Função                              | Sistema                  | IP            |
|----------|--------------------------------------|---------------------------|---------------|
| DC01     | Controlador de domínio, DNS          | Windows Server 2025       | 192.168.10.10 |
| FS01     | Servidor de arquivos                 | Windows Server 2025       | 192.168.10.11 |
| CLIENT01 | Estação de trabalho                  | Windows 11 Pro             | 192.168.10.50 |

- **Domínio:** empresa.local
- **Rede:** 192.168.10.0/24, em uma rede NAT interna do VirtualBox
- **Virtualização:** Oracle VirtualBox

## O que foi configurado

- **Active Directory:** domínio próprio, organizado em OUs por
  departamento (Financeiro, RH, TI, Vendas), com grupos de segurança
  (GG_Financeiro, GG_RH, GG_TI, GG_Vendas) e 8 usuários
- **DNS:** configurado com encaminhador para resolver nomes externos
- **File Server:** pastas por departamento, com permissões de
  compartilhamento e NTFS concedidas sempre por grupo de segurança,
  nunca por usuário individual
- **Política de bloqueio de conta:** configurada para bloquear após
  tentativas de login incorretas
- **GPOs:** mapeamento automático de unidade de rede por departamento,
  aplicado via Group Policy e vinculado à OU correta
- **Rede Host-Only:** adicionada para permitir acesso externo às VMs
  (usada nos testes de acesso remoto)

## Chamados de suporte resolvidos

Cada chamado foi tratado como um ticket real de service desk, com
diagnóstico, causa raiz e solução documentados. A lista completa está
na pasta [`/tickets`](./tickets):

1. [Acesso a pasta de outro departamento](./tickets/ticket-001-acesso-pasta-rh.md)
2. [Conta de usuário bloqueada](./tickets/ticket-002-conta-bloqueada.md)
3. [Pasta de rede já existente / orientação de acesso](./tickets/ticket-003-pasta-ti-gpo.md)
4. [Unidade de rede mapeada desapareceu](./tickets/ticket-004-mapeamento-sumiu.md)
5. [Computador lento — diagnóstico de desempenho](./tickets/ticket-005-computador-lento.md)
6. [Fila de impressão travada](./tickets/ticket-006-impressora-travada.md)
7. [Onboarding de novo funcionário](./tickets/ticket-007-onboarding.md)
8. [Offboarding / desligamento de funcionário](./tickets/ticket-008-offboarding.md)
9. [Suspeita de phishing](./tickets/ticket-009-phishing.md)
10. [Tentativa de configuração de acesso remoto (RDP)](./tickets/ticket-010-acesso-remoto.md)
11. [Outlook pedindo senha repetidamente](./tickets/ticket-011-outlook-senha.md)
12. [Relatório de acesso para auditoria](./tickets/ticket-012-auditoria-acessos.md)
13. [Transferência de departamento](./tickets/ticket-013-transferencia-departamento.md)


## Tecnologias e conceitos utilizados

Active Directory Domain Services (AD DS) · DNS · GPO (Group Policy) ·
Permissões NTFS e de compartilhamento · PowerShell · Troubleshooting de
rede (ping, nslookup, Test-NetConnection) · Windows Server 2025 ·
Windows 11 Pro · VirtualBox

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


## Tecnologias e conceitos utilizados

Active Directory Domain Services (AD DS) · DNS · GPO (Group Policy) ·
Permissões NTFS e de compartilhamento · PowerShell · Troubleshooting de
rede (ping, nslookup, Test-NetConnection) · Windows Server 2025 ·
Windows 11 Pro · VirtualBox

\# Projeto 01 — Infraestrutura de Rede Segura na AWS



\## 1. Visão geral



Este projeto tem como objetivo projetar, implementar e documentar uma infraestrutura de rede na AWS, aplicando conceitos de arquitetura em nuvem, segmentação de rede, segurança e monitoramento.



O projeto faz parte do meu portfólio prático de estudos para a certificação AWS Certified Solutions Architect – Associate (SAA-C03).



\## 2. Objetivos



\* Criar uma Amazon VPC com endereçamento IPv4.

\* Distribuir sub-redes públicas e privadas entre zonas de disponibilidade.

\* Configurar Internet Gateway e tabelas de rotas.

\* Compreender e aplicar Security Groups e Network ACLs.

\* Utilizar instâncias EC2 para testar a conectividade.

\* Configurar VPC Flow Logs para observar o tráfego de rede.

\* Documentar decisões técnicas, testes e aprendizados.



\## 3. Arquitetura planejada



A arquitetura inicial prevê:



\* Uma VPC com bloco CIDR `10.0.0.0/16`.

\* Três sub-redes públicas, uma por zona de disponibilidade.

\* Três sub-redes privadas, uma por zona de disponibilidade.

\* Um Internet Gateway para permitir conectividade com a internet a partir das sub-redes públicas, conforme as rotas e regras de segurança.

\* Tabelas de rotas para controlar o encaminhamento do tráfego.

\* Instâncias EC2 para testes controlados.

\* Controles de tráfego por Security Groups e Network ACLs.

\* VPC Flow Logs para monitoramento.



\### Endereçamento IP proposto



| Sub-rede     | Bloco CIDR     |

| ------------ | -------------- |

| Pública AZ-a | `10.0.1.0/24`  |

| Pública AZ-b | `10.0.2.0/24`  |

| Pública AZ-c | `10.0.3.0/24`  |

| Privada AZ-a | `10.0.11.0/24` |

| Privada AZ-b | `10.0.12.0/24` |

| Privada AZ-c | `10.0.13.0/24` |



Os nomes das zonas de disponibilidade serão definidos durante a implementação, conforme as zonas disponíveis na região escolhida.



\## 4. Segurança e controle de custos



A implementação buscará aplicar o princípio do menor privilégio e restringir o tráfego ao necessário para os testes.



A primeira versão não utilizará NAT Gateway, a fim de reduzir custos. Consequentemente, as instâncias privadas não terão acesso de saída à internet por meio de NAT nesta etapa.



Os recursos serão criados gradualmente, com verificação dos custos potenciais antes de cada etapa.



\## 5. Plano de implementação



1\. Revisar o planejamento de rede e os blocos CIDR.

2\. Criar a VPC e as sub-redes.

3\. Configurar o Internet Gateway e as tabelas de rotas.

4\. Definir Security Groups e Network ACLs.

5\. Avaliar a necessidade e o custo das instâncias EC2.

6\. Realizar testes de conectividade e isolamento.

7\. Configurar VPC Flow Logs, avaliando o destino e os custos.

8\. Registrar evidências, resultados e aprendizados.



\## 6. Validação



A validação será baseada em evidências coletadas durante a implementação, incluindo:



\* Configuração da VPC, das sub-redes e das tabelas de rotas.

\* Regras de entrada e saída dos controles de segurança.

\* Testes de conectividade autorizada e bloqueada.

\* Funcionamento do monitoramento de tráfego, quando configurado.



Os resultados serão documentados somente após a execução dos testes.



\## 7. Status



\*\*Status atual:\*\* planejamento e preparação do repositório.



Os recursos de infraestrutura ainda não foram declarados como implementados. Esta documentação será atualizada à medida que cada etapa for concluída e validada.



\## 8. Aprendizados



Esta seção será atualizada com os conceitos estudados, os problemas encontrados, as soluções aplicadas e as decisões técnicas tomadas durante o projeto.




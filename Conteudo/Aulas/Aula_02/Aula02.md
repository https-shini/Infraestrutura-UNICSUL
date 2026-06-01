# Infraestrutura de Tecnologia da Informação
## Resumo do Conteúdo — Aula 01

---

## Índice

1. [Objetivos da Disciplina](#objetivos-da-disciplina)
2. [Conteúdo Programático](#conteúdo-programático)
3. [O que é um Data Center?](#o-que-é-um-data-center)
4. [SAN — Storage Area Network](#san--storage-area-network)
5. [Questões para Debate e Discussão](#questões-para-debate-e-discussão)

---

## Objetivos da Disciplina

### Conhecimentos
- Adquirir conhecimentos básicos e intermediários sobre infraestrutura de redes
- Reconhecer métodos e melhores práticas na aplicação em infraestrutura e serviços em TI
- Fundamentar conhecimentos que permitam aprofundamento em infraestrutura da tecnologia da informação

### Habilidades
- Organizar e implementar infraestrutura em redes de computadores em uma organização
- Sistematizar a infraestrutura de TI de uma organização
- Participar ativamente do processo de tomada de decisão e escolha de tecnologia
- Analisar objetivos e metas relacionadas às expectativas do uso da infraestrutura de TI

### Atitudes
- Envolver-se com assuntos e tecnologias de infraestrutura de TI
- Interessar-se pela constante evolução técnica e metodológica de boas práticas em infraestrutura de TI

---

## Conteúdo Programático

| Unid. | C/H | Conteúdo |
|-------|-----|----------|
| I | 2h | Ementa, objetivos, conteúdo, estratégia de ensino, avaliação e bibliografia |
| II | 8h | Definição de TI; Definição e uso de um Data Center; Infraestrutura física; Redes; Arquiteturas Three-tier e Spine-Leaf |
| III | 8h | Host e servidores; Sistemas de processamento de arquivos; Sistema de gerenciamento de banco de dados; Tecnologia, componentes e camadas FC |
| IV | 8h | Motivação para virtualização; Benefícios da virtualização; Aplicações; Tipos de virtualização; Tipos de Hypervisor |
| V | 10h | Meios de armazenamento; Tecnologias de RAID; Configurações de RAID; Redes de armazenamento DAS, SAN, NAS |
| VI | 10h | Introdução à computação em nuvem; Tipos de computação em nuvem; Modelo de serviços (IaaS, PaaS, SaaS); Provedores de serviços |
| VII | 6h | Definição de DCIM; Modelo de DCIM; Categorias de monitoramento em Tempo Real |
| VII | 8h | Avaliação Regimental (A1); Avaliações parciais e processuais (A2) |

---

## O que é um Data Center?

### Origem e Evolução

- Até os anos 90 eram conhecidos como **CPD — Centro de Processamento de Dados**
- A partir dos anos 2000 passaram a ser referenciados como **Data Centers**
- São **equipamentos e sistemas** responsáveis pelo **processamento e armazenamento de informações** cruciais para a continuidade da operação dos mais diversos tipos de negócios

### Principais Características

| Característica | Descrição |
|----------------|-----------|
| **Presença contínua de pessoas** | Operação ininterrupta com equipes dedicadas |
| **Quantidade e porte físico dos equipamentos** | Grande volume de hardware de missão crítica |
| **Armazenamento de dados** | Repositório central das informações da organização |
| **Processamento de dados** | Execução das aplicações e sistemas do negócio |

> **Objetivo principal:** Garantir a disponibilidade de equipamentos que rodam sistemas cruciais para o negócio de uma organização.

### Componentes de um Data Center

- **Servidores** — para armazenamento e processamento de dados
- **SAN — Storage Area Network** — rede de armazenamento dedicada
- **Sistemas de armazenamento** — Storage Arrays e File Storage
- **Snapshots** — capturas do estado de armazenamento
- **Ativos de rede** — switches e roteadores

---

## SAN — Storage Area Network

A **SAN** é uma rede dedicada ao armazenamento, com as seguintes características:

| Atributo | Detalhe |
|----------|---------|
| **Isolamento** | Rede **segregada da rede local** (LAN) |
| **Protocolo** | **FC — Fibre Channel Protocol** |
| **Confiabilidade** | Transmissão **sem perdas** de dados |
| **Desempenho** | **Alta velocidade** de transferência |

### Diagrama — SAN Single Switch

```
 ┌─────────────────────────────────────────────────┐
 │          Single Switch Fabric — FC Director      │
 │                                                  │
 │  [APP][APP]                                      │
 │  [OS ][OS ]     ┌──────────────┐   ┌──────────┐ │
 │  [VM ][VM ]  ──►│  FC Director │──►│ Storage  │ │
 │  [Hypervisor]   └──────────────┘   └──────────┘ │
 │  Compute System               Compute System     │
 └─────────────────────────────────────────────────┘
         Storage Area Network — Single Switch
```

### Sistemas de Armazenamento

- **Storage Arrays** — matrizes de discos de alta capacidade
- **File Storage** — armazenamento de arquivos compartilhados
- **Snapshots** — capturas do estado de armazenamento para backup e recuperação

---

## Questões para Debate e Discussão

As questões a seguir foram propostas para fixação e debate do conteúdo:

---

**1.** Qual é a principal função da área de TI nas empresas?

---

**2.** Dê uma descrição para os Data Centers.

---

**3.** Dê uma definição para a SAN.

---

**4.** Quais os 4 pontos fundamentais para as infraestruturas de Data Centers?

---

**5.** Cite os pontos importantes que devem fazer parte de um projeto de Data Center.

---

**6.** Descreva a *"Three-tier Architecture"*.

---

**7.** Quais são as 3 camadas da infraestrutura da *"Three-tier Architecture"*?

---

**8.** Cite as vantagens da *"Three-tier Architecture"*.

---

**9.** Cite algumas desvantagens da *"Three-tier Architecture"*.

---

**10.** Descreva a TIA.

---

## Bibliografia Básica

- TANENBAUM, A. S.; WETHERALL, D. **Redes de Computadores**. 5. ed. São Paulo: Pearson Prentice Hall, 2011.
- MARIN, P. S. **Data Centers desvendando cada passo**: conceitos, projeto, infraestrutura física e eficiência energética. São Paulo: Érica, 2011.
- CHAGAS, M. W. P. das. **Sistemas de energia e climatização**: aplicações práticas em telecomunicações e data center. São Paulo: Érica, 2013.

## Bibliografia Complementar

- KUROSE, J. F.; ROSS, K. W. **Redes de computadores e a internet**: uma abordagem top-down. 5. ed. São Paulo: Addison Wesley, 2010.
- FILHO, E. C. L. **Fundamentos de rede e cabeamento estruturado**. São Paulo: Pearson Education do Brasil, 2014.
- WEBB, K. **Construindo redes cisco usando comutação multicamadas**. São Paulo: Pearson Education do Brasil, 2003.
- VERAS, M. **Virtualização**: tecnologia central do datacenter. 2. ed. Rio de Janeiro: Brasport, 2016.
- VERAS, M. **Computação em nuvem**: nova arquitetura de TI. Rio de Janeiro: Brasport, 2015.
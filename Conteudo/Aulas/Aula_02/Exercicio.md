# 📚 Infraestrutura de Tecnologia da Informação
## Questões para Debate e Discussão — Aula 02

> **Universidade Cruzeiro do Sul**
> Prof. Dr. Neslon Missaglia

---

## Índice

1. [Função da TI nas Empresas](#1-qual-é-a-principal-função-da-área-de-ti-nas-empresas)
2. [Descrição dos Data Centers](#2-dê-uma-descrição-para-os-data-centers)
3. [Definição de SAN](#3-dê-uma-definição-para-a-san)
4. [4 Pontos Fundamentais de Data Centers](#4-quais-os-4-pontos-fundamentais-para-as-infraestruturas-de-data-centers)
5. [Projeto de Data Center](#5-cite-os-pontos-importantes-de-um-projeto-de-data-center)
6. [Three-tier Architecture](#6-descreva-a-three-tier-architecture)
7. [As 3 Camadas da Three-tier](#7-quais-são-as-3-camadas-da-three-tier-architecture)
8. [Vantagens da Three-tier](#8-vantagens-da-three-tier-architecture)
9. [Desvantagens da Three-tier](#9-desvantagens-da-three-tier-architecture)
10. [TIA](#10-descreva-a-tia)

---

## 1. Qual é a principal função da área de TI nas empresas?

A principal função da área de **Tecnologia da Informação (TI)** nas empresas é garantir a **disponibilidade, o processamento e o armazenamento das informações** necessárias para a continuidade das operações do negócio.

A TI atua como **suporte estratégico e operacional**, provendo toda a infraestrutura tecnológica — servidores, redes, sistemas, bancos de dados e segurança — que permite que os processos organizacionais funcionem de forma eficiente, segura e ininterrupta.

```
TI = Disponibilidade + Processamento + Armazenamento + Segurança
```

> 💡 Em resumo: a TI existe para que o **negócio funcione, escale e se mantenha seguro**.

---

## 2. Dê uma descrição para os Data Centers

Os **Data Centers** são instalações físicas compostas por equipamentos e sistemas responsáveis pelo **processamento e armazenamento de informações cruciais** para a continuidade das operações empresariais.

### Evolução Histórica

| Período | Nomenclatura | Característica |
|---------|-------------|----------------|
| Até anos 90 | CPD — Centro de Processamento de Dados | Operação centralizada com grandes mainframes |
| A partir dos anos 2000 | Data Center | Infraestrutura moderna e distribuída |

### Principais Características

- 👥 **Presença contínua de pessoas** — operação 24 horas por dia, 7 dias por semana
- 🖥️ **Grande quantidade e porte físico** de equipamentos
- 💾 **Armazenamento de dados** em larga escala
- ⚙️ **Processamento intensivo** de dados e aplicações

> 🎯 **Objetivo central:** garantir a disponibilidade dos equipamentos que rodam os sistemas críticos para o negócio de uma organização.

---

## 3. Dê uma definição para a SAN

**SAN — Storage Area Network** é uma rede de armazenamento de dados dedicada e **segregada da rede local (LAN)** da organização, que conecta servidores a sistemas de armazenamento de alta capacidade com segurança e desempenho máximos.

### Características Técnicas

| Característica | Descrição |
|---------------|-----------|
| **Protocolo** | FC — Fibre Channel (fibra óptica) |
| **Confiabilidade** | Transmissão sem perda de dados |
| **Velocidade** | Alta velocidade de transferência |
| **Isolamento** | Rede segregada da LAN corporativa |

### Componentes da SAN

- **Storage Arrays** — Matrizes de discos para armazenamento em bloco
- **File Storage** — Armazenamento de arquivos compartilhados
- **Snapshots** — Capturas do estado do armazenamento em um momento específico (utilizadas para backup e recuperação)
- **Ativos de rede** — Switches e roteadores dedicados

```
Servidor → FC Switch → Storage Array
               ↕
          (Rede SAN segregada da LAN)
```

---

## 4. Quais os 4 pontos fundamentais para as infraestruturas de Data Centers?

Os quatro pilares que sustentam qualquer infraestrutura de Data Center são:

### 🔵 1. Disponibilidade
Garantia de que os sistemas estejam acessíveis continuamente, com mínimo ou nenhum tempo de inatividade (uptime elevado). É o requisito mais crítico de um Data Center.

### 🔴 2. Segurança
Proteção física e lógica de equipamentos e dados, englobando controle de acesso, segurança da informação e gerenciamento de mudanças (*Change Management*).

### 🟢 3. Escalabilidade
Capacidade da infraestrutura crescer conforme a demanda da organização aumenta, sem comprometer o desempenho ou exigir reestruturações completas.

### 🟡 4. Gerenciamento
Monitoramento contínuo dos ativos, adoção de boas práticas como **ITIL** (Information Technology Infrastructure Library) e uso de ferramentas de gestão como o **DCIM** para controle e governança dos serviços de TI.

---

## 5. Cite os pontos importantes de um projeto de Data Center

Um projeto de Data Center bem estruturado deve contemplar os seguintes elementos:

### 🏗️ Infraestrutura Física
- Espaço físico adequado (sala, piso elevado, racks)
- Sistema de climatização e refrigeração
- Sistemas de energia: nobreaks (UPS) e geradores

### 🌐 Redes de Comunicação
- Switches e roteadores de alta performance
- Cabeamento estruturado certificado
- Links de conectividade redundantes

### 🖥️ Servidores
- Hosts e servidores dimensionados para a demanda de processamento
- Redundância de hardware (fontes, memória, processadores)

### 💾 Armazenamento
- Solução de storage adequada: **DAS**, **SAN** ou **NAS**
- Política de backup e recuperação de dados

### 🔒 Segurança Física e Lógica
- Controle de acesso biométrico e CFTV
- Firewall, IDS/IPS e políticas de segurança da informação

### 🖧 Virtualização
- Hypervisors para otimização dos recursos físicos
- Redução de custos e maior flexibilidade operacional

### 📊 Gerenciamento — DCIM
- Ferramentas de monitoramento em tempo real dos ativos
- Visibilidade completa sobre energia, espaço e capacidade

### 🔄 Continuidade de Negócios
- Plano de recuperação de desastres (DRP)
- Alta disponibilidade e failover automatizado

---

## 6. Descreva a "Three-tier Architecture"

A **Three-tier Architecture** (Arquitetura de Três Camadas) é um modelo clássico de infraestrutura de rede para Data Centers que organiza os componentes de rede em **três camadas hierárquicas distintas**, cada uma com função e equipamentos específicos.

```
┌─────────────────────────────────────────┐
│            CORE LAYER                   │  ← Núcleo / Roteamento Principal
├─────────────────────────────────────────┤
│         DISTRIBUTION LAYER              │  ← Distribuição / Políticas
├─────────────────────────────────────────┤
│           ACCESS LAYER                  │  ← Acesso / Dispositivos Finais
└─────────────────────────────────────────┘
```

Esse modelo foi desenvolvido para oferecer uma rede **escalável, gerenciável e redundante**, sendo amplamente utilizado em ambientes corporativos tradicionais. A separação em camadas facilita o **isolamento de falhas**, a **aplicação de políticas de segurança** e a **expansão da infraestrutura** de forma controlada.

---

## 7. Quais são as 3 camadas da "Three-tier Architecture"?

### 🔴 Camada 1 — Core Layer (Núcleo)

É a **espinha dorsal** da rede. Responsável pelo roteamento de alta velocidade entre redes internas e pela conexão com redes externas (Internet / WAN).

- Prioridade: **velocidade e disponibilidade máxima**
- Equipamentos: roteadores e switches core de alta performance
- Não realiza filtragem de tráfego — foco em encaminhar pacotes rapidamente

---

### 🟡 Camada 2 — Distribution Layer (Distribuição)

**Intermediária** entre o Core e os switches de acesso. Concentra a inteligência da rede.

- Realiza roteamento entre **VLANs**
- Aplica **políticas de segurança** e controle de tráfego
- Agrega conexões vindas da camada de acesso
- Equipamentos: switches multilayer (L3)

---

### 🟢 Camada 3 — Access Layer (Acesso)

É o **ponto de entrada** dos dispositivos finais na rede.

- Conecta fisicamente servidores, computadores e impressoras à infraestrutura
- Equipamentos: switches de acesso (L2)
- Responsável por segmentação de portas e configuração de VLANs por porta

---

## 8. Vantagens da "Three-tier Architecture"

| ✅ Vantagem | Descrição |
|------------|-----------|
| **Escalabilidade** | Cada camada pode crescer de forma independente |
| **Gerenciabilidade** | Separação clara facilita monitoramento e manutenção |
| **Segurança** | Políticas de segurança aplicadas por camada |
| **Redundância** | Caminhos redundantes garantem alta disponibilidade |
| **Isolamento de falhas** | Problema em uma camada não afeta as demais |
| **Desempenho previsível** | Cada camada otimizada para sua função específica |
| **Padronização** | Modelo amplamente documentado e com suporte no mercado |

---

## 9. Desvantagens da "Three-tier Architecture"

| ❌ Desvantagem | Descrição |
|--------------|-----------|
| **Alto custo** | Equipamentos dedicados por camada elevam o investimento |
| **Latência** | Tráfego entre servidores atravessa múltiplas camadas |
| **Complexidade** | Administração de três camadas exige maior expertise técnica |
| **Ineficiência Leste-Oeste** | Modelo projetado para tráfego Norte-Sul (cliente→servidor); não é ideal para tráfego entre servidores |
| **Menor agilidade** | Mudanças e expansões são mais lentas e complexas |
| **Obsolescência parcial** | Ambientes virtualizados e em nuvem demandam arquiteturas mais modernas, como **Spine-Leaf** |

> ⚠️ Com o crescimento da **virtualização** e de aplicações distribuídas, o tráfego Leste-Oeste (entre servidores) tornou-se predominante, evidenciando a limitação do modelo Three-tier para ambientes modernos.

---

## 10. Descreva a TIA

A **TIA — Telecommunications Industry Association** é uma associação norte-americana que desenvolve e publica **normas e padrões técnicos** para a indústria de telecomunicações e infraestrutura de TI.

### Norma Principal: ANSI/TIA-942

A norma **TIA-942** define padrões de projeto, construção e operação de Data Centers, incluindo a classificação por níveis de disponibilidade:

### Classificação por Tiers

| Tier | Disponibilidade | Redundância | Característica |
|------|----------------|-------------|----------------|
| **Tier I** | 99,671% | Sem redundância | Infraestrutura básica |
| **Tier II** | 99,741% | Redundância parcial | Componentes redundantes |
| **Tier III** | 99,982% | N+1 | Manutenção sem downtime |
| **Tier IV** | 99,995% | 2N | Tolerante a falhas — maior nível |

### Outras Normas Relevantes da TIA

- **TIA-568** — Padrões de cabeamento estruturado (Cat5e, Cat6, Cat6A, fibra)
- **TIA-569** — Espaços e percursos de telecomunicações em edifícios
- **TIA-606** — Padrões de administração de infraestrutura de telecomunicações

> 💡 A TIA tem papel fundamental na **padronização global** da infraestrutura de TI, garantindo **interoperabilidade, segurança e qualidade** nos projetos de Data Centers ao redor do mundo.

---

## 🗺️ Mapa Conceitual Geral

```
Data Center
│
├── Função da TI ──────────────► Disponibilidade + Processamento + Armazenamento
│
├── Infraestrutura
│   ├── Física ────────────────► Energia, Refrigeração, Espaço
│   ├── Rede ──────────────────► Switches, Roteadores, Cabeamento
│   ├── Armazenamento ─────────► DAS / SAN / NAS
│   └── Servidores ────────────► Hosts + Virtualização (Hypervisor)
│
├── SAN ───────────────────────► Rede segregada com Fibre Channel
│
├── Three-tier Architecture
│   ├── Core Layer ────────────► Velocidade / Roteamento Principal
│   ├── Distribution Layer ────► Políticas / VLANs / Segurança
│   └── Access Layer ──────────► Conexão dos Dispositivos Finais
│
└── TIA-942 ───────────────────► Padronização (Tier I ao Tier IV)
```

---

*📖 Respostas elaboradas com base no conteúdo das Aulas 01 e 02 da disciplina*
*Infraestrutura de Tecnologia da Informação — Prof. Dr. Neslon Missaglia — Universidade Cruzeiro do Sul — 2026*
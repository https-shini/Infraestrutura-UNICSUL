<h1 align="center">📝 Avaliação (Prova A2) — Resolução Comentada</h1>

<p align="center">
  <em>Questões — Infraestrutura de Tecnologia da Informação · Ciência da Computação · UNICSUL · 2026</em>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Atividade-AT3-blue?style=flat-square" alt="Atividade" />
  <img src="https://img.shields.io/badge/Formato-Prova%20em%20grupo-red?style=flat-square" alt="Formato" />
  <img src="https://img.shields.io/badge/Data-04%2F05%2F2026-success?style=flat-square" alt="Data" />
  <img src="https://img.shields.io/badge/Valor-2%2C0%20pontos%20(A2)-yellow?style=flat-square" alt="Valor" />
</p>

---

## 📖 Informações gerais

- **Disciplina:** Infraestrutura de Tecnologia da Informação
- **Professor:** Adriano Arrivabene
- **Campus:** Analía Franco · **Turma:** 6º/7º D
- **Composição da nota:** compõe a **A2**
- **Pontuação:** 2,0 pontos no total — cada questão vale **0,25 ponto**
- **Estrutura:** 8 questões → 4 de múltipla escolha + 4 dissertativas

> ⚠️ Atividade desenvolvida em grupo (até 4 alunos), respondida a caneta, sem consulta a material.

---

## 📊 Gabarito resumido

| Questão | Tipo | Resposta |
|:-------:|:----:|:--------:|
| **1** | Múltipla escolha | **b** |
| **2** | Múltipla escolha | **b** |
| **3** | Múltipla escolha | **c** |
| **4** | Múltipla escolha | **b** |
| **5** | Dissertativa | — |
| **6** | Dissertativa | — |
| **7** | Dissertativa | — |
| **8** | Dissertativa | — |

---

## 🧩 Parte I — Questões de Múltipla Escolha

### Questão 1 — Resposta: **b) Todas as afirmações estão erradas**

| Afirmação | Análise |
|:---------:|---------|
| **I** | ❌ A SAN é uma rede **dedicada e separada** da LAN, não "junto com a LAN". Ela conecta servidores a pools de armazenamento por uma malha própria (ex.: Fibre Channel). |
| **II** | ✅ Oracle e MySQL **realmente utilizam SQL** — afirmação verdadeira. |
| **III** | ❌ A relação está invertida: a Memória Virtual é uma extensão da **RAM no HD** (usa o disco como área de troca/swap), e não "do HD na RAM". |
| **IV** | ❌ O Wi-Fi doméstico é uma **WLAN** (rede local sem fio), e não PAN. PAN é de alcance pessoal e curtíssimo (ex.: Bluetooth). |

> ⚠️ **Observação técnica:** o gabarito oficial é **b**, porém a afirmação **II é verdadeira**. Como não existe alternativa "somente II correta", a questão apresenta inconsistência de formulação — não há combinação que represente fielmente o conjunto. O ponto de atenção real do conteúdo está nos erros das afirmações I, III e IV.

---

### Questão 2 — Resposta: **b) Todas as afirmações estão erradas**

| Afirmação | Análise |
|:---------:|---------|
| **I** | ❌ Conceito trocado: o RAID 0 utiliza **striping** (divisão de dados), não mirroring. |
| **II** | ❌ Conceito trocado: o RAID 1 utiliza **mirroring** (espelhamento), não striping. |
| **III** | ❌ O RAID 5 tolera a falha de **apenas 1 disco** (paridade simples), não de 2. Quem tolera 2 discos é o RAID 6. |
| **IV** | ❌ O RAID 6 é **mais lento** na gravação e na reconstrução, justamente por calcular **dupla paridade**. |

> Como as quatro afirmações estão incorretas, a alternativa correta é **b**.

---

### Questão 3 — Resposta: **c) Somente as afirmações I e III estão corretas**

| Afirmação | Análise |
|:---------:|---------|
| **I** | ✅ Correta. A virtualização cria uma camada de abstração sobre o hardware, particionando os recursos de um único sistema em várias máquinas virtuais. |
| **II** | ❌ Falsa. A virtualização **facilita** a recuperação de desastres e os backups (snapshots, portabilidade de VMs) — é uma vantagem, não desvantagem. |
| **III** | ✅ Correta. A redução de custos por meio da consolidação e do melhor aproveitamento do hardware é uma vantagem clássica. |
| **IV** | ❌ Falsa. As VMs operam **isoladas** entre si pelo hypervisor; uma falha em uma VM normalmente não afeta as demais. |

> Verdadeiras: I e III → alternativa **c**.

---

### Questão 4 — Resposta: **b) Todas as afirmações estão erradas**

| Afirmação | Análise |
|:---------:|---------|
| **I** | ❌ Conceitos invertidos: na nuvem, a **Região** é a localização geográfica que abriga várias **Zonas** — e não o contrário. |
| **II** | ❌ A sigla está errada: **DDoS** significa *Distributed Denial of Service*, não apenas "Denial of Service". |
| **III** | ❌ Inversão: o Data Center "lógico" isolado dentro de uma Região é a **Zona de Disponibilidade**, não a Região. |
| **IV** | ❌ A sigla está errada: **DoS** é *Denial of Service* (origem única); o ataque coordenado por várias máquinas é o DDoS. "Distributed of Service" não existe. |

> Todas as afirmações apresentam erro conceitual ou de sigla → alternativa **b**.

---

## 📝 Parte II — Questões Dissertativas

### Questão 5 — RAID 10 e uma desvantagem

O **RAID 10** (também chamado RAID 1+0) é um nível **híbrido** que combina o **espelhamento** do RAID 1 com o **striping** do RAID 0. Na prática, os dados são primeiro espelhados em pares de discos (garantindo redundância) e, em seguida, distribuídos entre esses pares (garantindo desempenho). O resultado é uma configuração que une **alta tolerância a falhas** e **boa performance** de leitura e escrita, exigindo no **mínimo 4 discos**.

**Desvantagem:** o **alto custo** de implementação. Como metade dos discos é destinada apenas ao espelhamento, há **aproveitamento de apenas 50% da capacidade total** instalada, tornando-o oneroso em relação a níveis com paridade (como RAID 5 ou 6).

> ✔️ A resposta do grupo abordou corretamente a combinação RAID 0 + RAID 1, a redundância, o mínimo de 4 discos e a desvantagem de custo.

---

### Questão 6 — SaaS, PaaS e IaaS

| Modelo | Descrição | Exemplo |
|:------:|-----------|---------|
| **SaaS** | *Software as a Service* — aplicação pronta, entregue pela internet em modelo de assinatura. O cliente apenas utiliza; o provedor cuida de toda a infraestrutura, manutenção e recursos. A gestão pelo usuário é mínima. | Office 365 |
| **PaaS** | *Platform as a Service* — ambiente completo para o usuário **desenvolver e publicar aplicações**, sem se preocupar com a infraestrutura e o sistema operacional subjacentes. | Heroku |
| **IaaS** | *Infrastructure as a Service* — o usuário tem liberdade total para criar seu próprio ambiente (VMs, VLANs, escolha do sistema operacional), com o provedor oferecendo os recursos básicos de infraestrutura. | AWS, Azure |

> ✔️ As três descrições do grupo estão corretas, com exemplos adequados para cada camada.

---

### Questão 7 — Arquitetura de Nuvem Híbrida

A **Nuvem Híbrida** é um modelo de implantação que **combina ambientes de nuvem pública e privada/local**, permitindo que dados e cargas de trabalho **transitem entre eles de forma orquestrada e integrada**. Tipicamente, os dados sensíveis e os serviços críticos permanecem na infraestrutura privada/interna, enquanto serviços menos sensíveis ou que demandam elasticidade são executados na nuvem pública (ex.: AWS).

O grande diferencial não é apenas "ter os dois ambientes", mas a **integração coordenada** entre eles, o que dá flexibilidade para mover workloads conforme a necessidade. Seu principal desafio é o **custo de conexão e a transferência segura dos dados** entre as nuvens.

> 📌 **Ponto de melhoria da resposta original:** o conceito central (mistura de nuvem pública + infraestrutura interna) estava correto; faltou apenas explicitar a palavra-chave da definição — a **orquestração/integração** entre os ambientes, e não somente sua coexistência.

---

### Questão 8 — Tipos de Cloud Computing

**a. Public Cloud (Nuvem Pública)**
Ambiente cujos recursos são **compartilhados entre múltiplos clientes** simultaneamente, com acesso, segurança e infraestrutura **gerenciados pelo provedor**. Uma camada de software isola os dados de cada cliente. Exemplos: AWS, Azure.

**b. Private Cloud (Nuvem Privada)**
Ambiente de **uso exclusivo de uma única organização**, indicado para dados estratégicos que exigem maior controle de segurança (firewall) e baixa latência. A responsabilidade pela operação (segurança, hardware, manutenção) recai sobre a empresa.

> 📌 **Ponto de melhoria da resposta original:** a definição estava correta no conceito de exclusividade e responsabilidade. Vale ressaltar, porém, que a nuvem privada **não exige obrigatoriamente a ausência de um provedor** — ela pode ser hospedada por um terceiro, desde que seja **dedicada exclusivamente a uma única organização**. O que define "privada" é o **uso exclusivo**, não o "fazer tudo internamente".

---

## 🎯 Síntese de desempenho

| Bloco | Observação |
|-------|------------|
| **Múltipla escolha (1–4)** | Q2, Q3 e Q4 dominadas. Q1 envolveu uma questão mal formulada (afirmação II verdadeira). Pontos conceituais a reforçar: **memória virtual** e **classificação de redes (PAN/LAN/WLAN/SAN)**. |
| **Dissertativas (5–8)** | RAID 10 e IaaS/PaaS/SaaS com pontuação cheia. Pequenos ajustes em **nuvem híbrida** (orquestração) e **nuvem privada** (exclusividade de uso). |

> 📚 **Temas para revisão:** memória virtual (swap/paginação) · topologias de rede (PAN, LAN, WLAN, WAN, VLAN) · arquiteturas de armazenamento (DAS, SAN, NAS) · modelos de serviço e de implantação de nuvem.

---

<p align="center">
  <em>Resolução comentada — para os enunciados sem resposta, consulte <code>Questoes.md</code>.</em>
</p>

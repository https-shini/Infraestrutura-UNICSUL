# Infraestrutura de Tecnologia da Informação
## Atividade 02 — Perguntas e Respostas

**Professor:** Adriano Arrivabene
**Data:** 14/04/2026

> Cada questão vale 0,25 ponto. As respostas devem ter no mínimo 10 linhas e indicar as fontes.

---

### 01 - Descreva o "DBMS - Data Base Management System" e dê 3 exemplos de SGBD que utilizam a linguagem Structured Query Language.

O Database Management System (DBMS), ou Sistema de Gerenciamento de Banco de Dados (SGBD), é um software que atua como uma camada intermediária entre os usuários e os dados armazenados fisicamente. Sua principal função é permitir que os usuários criem, leiam, atualizem e deletem informações de forma estruturada, garantindo que as regras de integridade e segurança sejam respeitadas.

Um SGBD robusto gerencia o controle de concorrência, permitindo que múltiplas pessoas acessem o banco ao mesmo tempo sem corromper os registros. Além disso, ele oferece ferramentas para tunagem de performance, indexação e recuperação de desastres através de backups automáticos.

A linguagem padrão utilizada para interagir com a maioria desses sistemas é o SQL (Structured Query Language), que permite realizar consultas complexas de maneira eficiente e padronizada em diferentes plataformas.

Três exemplos de SGBDs que utilizam SQL:

- **MySQL:** um dos SGBDs de código aberto mais utilizados no mundo, essencial para aplicações web.
- **PostgreSQL:** focado em extensibilidade e conformidade com padrões técnicos rigorosos.
- **Oracle Database:** um sistema corporativo de alta performance utilizado por grandes organizações globais.

**Fontes:** oracle.com; mysql.com; postgresql.org.

---

### 02 - Dê uma descrição de como funciona a alocação e desalocação de programas na Memória Virtual.

A Memória Virtual é uma técnica fundamental dos sistemas operacionais modernos que utiliza o espaço do disco rígido para estender a capacidade da memória RAM física. O processo de alocação começa com a divisão dos programas em blocos chamados "páginas".

Quando um programa precisa de mais memória do que a RAM dispõe, o sistema operacional move páginas inativas da RAM para o disco, processo conhecido como swap-out. Quando o processador precisa acessar esses dados novamente, ocorre o page fault, e o sistema traz a página de volta para a RAM, processo chamado de swap-in.

A desalocação ocorre de forma automática quando um processo é finalizado ou quando o gerenciador de memória identifica que determinados dados não são acessados há muito tempo, liberando os endereços lógicos e físicos para que outros aplicativos possam utilizá-los, mantendo assim o equilíbrio e a fluidez do sistema computacional.

**Fontes:** microsoft.com; redhat.com; ibm.com.

---

### 03 - Dê uma descrição para: PAN, LAN, WAN e VLAN.

As redes de computadores são categorizadas conforme sua extensão geográfica e finalidade lógica.

**a) PAN – Personal Area Network**

A PAN é a rede de menor alcance, utilizada para conectar dispositivos de uso pessoal em um raio de poucos metros, como um smartwatch a um celular via Bluetooth.

**b) LAN – Local Area Network**

A LAN é a rede local comum em escritórios e residências, cobrindo áreas geograficamente pequenas com alta velocidade de transmissão e baixa latência.

**c) WAN – Wide Area Network**

A WAN possui uma abrangência muito maior, conectando cidades ou até países inteiros. A Internet é o maior exemplo de WAN existente.

**d) VLAN – Virtual Local Area Network**

A VLAN é uma técnica que permite segmentar uma rede física em várias redes lógicas independentes. Isso aumenta a segurança e a eficiência, pois permite que computadores em diferentes salas se comportem como se estivessem em uma rede isolada, reduzindo o tráfego desnecessário e facilitando a administração por parte da equipe de TI.

**Fontes:** cisco.com; aws.amazon.com; intel.com.br.

---

### 04 - Dê uma descrição para RAID 5 e RAID 10, incluindo uma desvantagem de cada.

O sistema RAID é utilizado para aumentar a disponibilidade e a performance dos dados.

**a) RAID 5**

O RAID 5 utiliza a distribuição de dados com paridade. Ele divide as informações entre três ou mais discos, reservando um espaço para bits de paridade que permitem reconstruir os dados caso um dos discos falhe.

*Desvantagem:* o desempenho de gravação é inferior, pois o sistema precisa calcular a paridade a cada nova escrita, o que gera uma carga extra de processamento.

**b) RAID 10**

O RAID 10 é uma combinação do RAID 1 (espelhamento) com o RAID 0 (divisão). Ele oferece a melhor performance e alta segurança, permitindo que até dois discos falhem em conjuntos diferentes.

*Desvantagem:* o custo é extremamente elevado, pois exige no mínimo quatro discos e metade da capacidade total é "perdida" para o espelhamento, tornando-o uma solução cara para grandes volumes de dados.

**Fontes:** seagate.com; dell.com; techtarget.com.

---

### 05 - Sobre Virtualização.

**a) O que é?**

A Virtualização é a tecnologia que cria uma camada de software sobre o hardware físico, permitindo que os recursos de um único computador (como CPU, memória e armazenamento) sejam divididos em múltiplos ambientes virtuais independentes, chamados de Máquinas Virtuais (VMs).

Cada VM funciona como um computador completo, com seu próprio sistema operacional. Isso permite que uma empresa execute servidores Windows e Linux no mesmo hardware físico sem interferência entre eles.

**b) Cite 5 vantagens da Virtualização.**

- **Redução de custos:** menos gastos com hardware físico e manutenção.
- **Economia de energia:** menos máquinas físicas ligadas consomem menos eletricidade.
- **Facilidade de backup:** as VMs podem ser copiadas e restauradas como arquivos simples.
- **Escalabilidade:** é muito mais rápido criar um servidor virtual do que comprar e instalar um físico.
- **Isolamento:** se um sistema virtual for infectado por vírus, os outros no mesmo hardware ficam protegidos.

**Fontes:** vmware.com; citrix.com.

---

### 06 - Cite as principais razões que fazem com que os grandes bancos ainda utilizem os computadores mainframes.

Os Mainframes são computadores de grande porte projetados para processar volumes gigantescos de dados e transações simultâneas com extrema confiabilidade. Grandes bancos ainda os utilizam porque esses sistemas oferecem uma disponibilidade próxima de 100%, algo essencial para transações financeiras que não podem parar.

Diferente de servidores comuns, os mainframes possuem hardware redundante que permite trocar peças enquanto a máquina está ligada. Além disso, a arquitetura de entrada e saída (I/O) dos mainframes é otimizada para lidar com milhões de registros de contas bancárias por segundo, garantindo a integridade dos dados e uma segurança robusta contra invasões.

A longevidade dos sistemas legados de bancos, escritos em linguagens como COBOL, também justifica a manutenção dessas máquinas, pois a migração total para nuvens comuns seria extremamente complexa, cara e arriscada para a operação bancária.

**Fontes:** ibm.com; bmc.com; broadcom.com.

---

### 07 - Dê uma descrição para: IaaS, PaaS e SaaS.

A computação em nuvem é dividida em modelos de serviço que definem o nível de controle do usuário.

**a) IaaS – Infrastructure as a Service**

O cliente aluga a infraestrutura básica pela internet, como servidores, armazenamento e rede, mantendo controle sobre o sistema operacional e as aplicações instaladas.

**b) PaaS – Platform as a Service**

O foco é o desenvolvimento de software. O provedor oferece sistemas e ambientes prontos para programadores, abstraindo a complexidade da infraestrutura subjacente.

**c) SaaS – Software as a Service**

O software é entregue completamente pronto via web, sem necessidade de instalação ou manutenção pelo usuário. O Gmail é um exemplo amplamente conhecido.

**Fontes:** azure.microsoft.com; cloud.google.com; aws.amazon.com.

---

### 08 - Pesquise e descreva o que é a "Arquitetura de Nuvem Híbrida".

A Nuvem Híbrida é uma arquitetura que une a nuvem privada (servidores internos da empresa) com a nuvem pública (serviços como AWS ou Azure). Isso permite que a empresa mantenha dados ultraconfidenciais em seu próprio ambiente, enquanto utiliza a nuvem pública para tarefas que exigem grande poder de processamento temporário.

É a solução ideal para empresas que buscam o equilíbrio entre a segurança máxima do ambiente local e a economia de custos e agilidade da nuvem pública, permitindo uma transição gradual e controlada para a nuvem sem renunciar à governança sobre dados críticos.

**Fontes:** azure.microsoft.com; cloud.google.com.

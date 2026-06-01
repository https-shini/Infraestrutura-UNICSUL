# Infraestrutura de Tecnologia da Informação
## Atividade 01 — Perguntas e Respostas

**Professor:** Adriano Arrivabene
**Data:** 30/03/2026

---

### 01 - Dê uma definição para a SAN.

SAN (Storage Area Network) é uma rede de alta velocidade dedicada ao armazenamento de dados, que conecta servidores a dispositivos como disk arrays e fitas magnéticas. Ela opera de forma independente da LAN corporativa, permitindo que múltiplos servidores acessem os mesmos recursos de armazenamento simultaneamente com boa disponibilidade e desempenho.

---

### 02 - Cite alguns inconvenientes do Acesso Sequencial.

O acesso sequencial apresenta as seguintes limitações:

- **Lentidão:** é necessário percorrer todos os registros anteriores para acessar um dado específico.
- **Ineficiência em buscas:** não é possível ir diretamente a um registro.
- **Desperdício de tempo:** todo o conteúdo anterior ao dado procurado precisa ser lido.
- **Inadequado para grandes volumes:** quanto maior o arquivo, pior o desempenho.
- **Dificuldade de atualização:** inserções e exclusões intermediárias são operações custosas.

---

### 03 - Cite características do Acesso Randômico.

- **Acesso direto:** qualquer posição pode ser acessada sem percorrer registros anteriores.
- **Endereçamento direto:** utiliza índices, chaves ou ponteiros para localizar dados.
- **Alta velocidade:** grande desempenho de leitura e escrita em qualquer ponto do armazenamento.
- **Base de dispositivos modernos:** princípio de funcionamento de HDs, SSDs e memória RAM.
- **Essencial para sistemas críticos:** indispensável em bancos de dados e sistemas que exigem respostas rápidas.
- **Tempo de acesso constante:** o tempo de acesso é praticamente o mesmo independentemente da posição do dado.

---

### 04 - Um banco de dados relacional possui tabelas: essas tabelas são indexadas?

Não necessariamente. Por padrão, índices são criados automaticamente apenas para chaves primárias (Primary Key) e, na maioria dos casos, para chaves estrangeiras (Foreign Key). As demais colunas só são indexadas se o administrador ou desenvolvedor criar os índices manualmente. Vale lembrar que índices aceleram consultas, mas consomem espaço e podem tornar inserções e atualizações mais lentas.

---

### 05 - O ORACLE ou MySQL são Bancos de Dados? Justifique.

Não. Oracle e MySQL são SGBDs, ou seja, Sistemas Gerenciadores de Banco de Dados, e não bancos de dados em si. O banco de dados é o conjunto estruturado de dados armazenados, enquanto o SGBD é o software responsável por criar, gerenciar e fornecer acesso a esses dados.

---

### 06 - Descreva a Memória Virtual.

Memória virtual é uma técnica do sistema operacional que simula mais RAM do que a fisicamente disponível, usando parte do disco rígido ou SSD como extensão da memória principal.

O SO divide a memória em páginas e move as menos utilizadas para o disco (swap), carregando-as de volta quando necessário. Isso permite executar mais processos simultaneamente, porém com desempenho inferior ao da RAM física.

---

### 07 - Descreva o LVM (Logical Volume Manager).

O LVM é uma camada de abstração entre o sistema operacional e os dispositivos de armazenamento físico, que permite gerenciar volumes de forma muito mais flexível do que o particionamento tradicional. Com ele é possível:

- **Agrupar discos:** múltiplos discos físicos em um único Volume Group (VG).
- **Gerenciar volumes lógicos:** criar, redimensionar e mover volumes (LVs) sem reparticionar.
- **Redimensionar em tempo real:** sem desmontar o sistema de arquivos.
- **Criar snapshots:** para fins de backup.

Por essas razões, o LVM é amplamente utilizado em servidores Linux para uma gestão dinâmica e eficiente do armazenamento.

---

### 08 - A rede doméstica Wi-Fi é uma PAN ou LAN? Justifique.

É uma LAN. Apesar de ser sem fio, conecta múltiplos dispositivos em uma área geograficamente limitada, compartilhando recursos como internet e impressoras. A PAN tem alcance muito menor e conecta dispositivos pessoais de um único usuário, como Bluetooth entre celular e fone de ouvido.

---

### 09 - Dê uma descrição para a VLAN.

VLAN (Virtual Local Area Network) é uma técnica que segmenta logicamente uma rede física em múltiplas redes virtuais independentes, sem necessidade de infraestrutura separada. Seus principais benefícios são:

- **Segurança:** isolamento do tráfego entre departamentos.
- **Organização:** separação lógica de setores como RH, TI e Financeiro.
- **Redução de broadcasts:** cada VLAN possui seu próprio domínio de broadcast.
- **Flexibilidade:** reconfiguração sem alterações físicas na rede.

---

### 10 - Quando surgiu o conceito de Virtualização?

O conceito surgiu na década de 1960, desenvolvido pela IBM para os mainframes das séries System/360 e System/370, com o objetivo de permitir que múltiplos usuários compartilhassem o mesmo hardware simultaneamente. O sistema CP/CMS da IBM é considerado o precursor das máquinas virtuais modernas.

---

### 11 - Dê uma descrição para a Virtualização.

A virtualização é uma tecnologia que permite criar versões virtuais de recursos físicos, como servidores, sistemas operacionais, redes e dispositivos de armazenamento, tudo rodando sobre um mesmo hardware físico.

Para gerenciar essa divisão de recursos entre as máquinas virtuais, é utilizado um software chamado hypervisor, também conhecido como VMM (Virtual Machine Monitor). Entre os principais benefícios estão:

- Melhor aproveitamento do hardware disponível.
- Redução de custos operacionais.
- Isolamento entre os diferentes ambientes.
- Maior facilidade para backup e recuperação de dados.
- Escalabilidade conforme a demanda.

---

### 12 - Qual o objetivo do Disk Array?

O Disk Array, ou conjunto de discos, tem como objetivo reunir múltiplos discos físicos em um único sistema de armazenamento centralizado, oferecendo:

- Alta capacidade de armazenamento.
- Alto desempenho por meio do acesso paralelo aos dados.
- Redundância e tolerância a falhas, geralmente via implementação de RAID.
- Gerenciamento centralizado de todo o armazenamento.

É amplamente utilizado em ambientes corporativos e em redes SAN.

---

### 13 - O que é o RAID?

O RAID (Redundant Array of Independent Disks) é uma tecnologia que combina múltiplos discos físicos para que funcionem como uma única unidade lógica. Seus principais objetivos são:

- Aumentar o desempenho por meio de leitura e gravação paralela.
- Garantir redundância e tolerância a falhas.
- Ampliar a capacidade total de armazenamento.

Existem diferentes níveis de RAID, como 0, 1, 5, 6 e 10, cada um com características próprias de desempenho e redundância.

---

### 14 - Qual dos tipos de RAID se baseia no Mirroring?

O RAID 1. Os dados são gravados simultaneamente em dois ou mais discos, criando uma cópia espelhada exata. Em caso de falha de um disco, o outro assume imediatamente, garantindo total disponibilidade dos dados.

---

### 15 - Qual dos tipos de RAID se baseia no Striping?

O RAID 0. Os dados são divididos em blocos e distribuídos paralelamente entre os discos, aumentando o desempenho de leitura e gravação. Porém, não há redundância: a falha de qualquer disco resulta na perda total dos dados.

---

### 16 - Qual dos RAID possui redundância de dados: 0 ou 1?

O RAID 1. O RAID 0 não oferece redundância alguma, pois seu objetivo é apenas dividir os dados para maior desempenho. A falha de um único disco destrói todos os dados do conjunto.

---

### 17 - Qual o conceito de Paridade no RAID 5?

No RAID 5, a paridade é um valor calculado matematicamente a partir dos blocos de dados gravados nos discos, geralmente por meio de uma operação XOR.

Esse valor é distribuído entre todos os discos do conjunto, e não concentrado em um disco dedicado. Em caso de falha de um disco, os dados perdidos podem ser recalculados e reconstruídos a partir dos discos restantes combinados com as informações de paridade. Isso garante tolerância à falha de até um disco, com melhor aproveitamento de espaço do que o RAID 1.

---

### 18 - Qual dos RAID 5 ou 6 possui tolerância à falha para 2 falhas de discos?

O RAID 6. Ele utiliza dupla paridade, com dois blocos de paridade por stripe distribuídos entre os discos, tolerando a falha simultânea de até dois discos sem perda de dados. O RAID 5 suporta apenas a falha de um único disco.

---

### 19 - Qual dos RAID 5 ou 6 é mais rápido para gravação de dados e de reconstrução de discos?

O RAID 5 é o mais rápido. Por calcular apenas um bloco de paridade por operação, o overhead de escrita é menor, resultando em melhor desempenho.

O RAID 6 é mais lento pois precisa calcular e gravar dois blocos de paridade a cada operação de escrita, além de exigir mais processamento durante a reconstrução após falhas.

---

### 20 - No que consiste o RAID 10?

O RAID 10 (RAID 1+0) é um modelo híbrido que combina mirroring (RAID 1) e striping (RAID 0). Os discos são primeiro espelhados em pares e depois unidos em stripe, resultando em alto desempenho e redundância ao mesmo tempo.

Requer no mínimo 4 discos e tolera a falha de um disco por par espelhado. É amplamente utilizado em ambientes críticos, como servidores de banco de dados.

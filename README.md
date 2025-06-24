# HELLO, world! — Hall Effect Lab for Learning and Observation

Integrantes: Edélio Gabriel Magalhães de Jesus, Gisela Ceresér Kassick, Giulia Sales Ferreira, Leonardo Ritchielly dos S Vieira
Instituição: Ilum- Escola de Ciência- CNPEM
Disciplina: Prática em Ciência de Dados
Professores orientadores: Daniel Roberto Cassar, James Moraes de Almeida
e Leandro Nascimento Lemos

 **HELLO, world!** é um projeto interdisciplinar que combina física, ciência de dados e programação para simular e analisar o **Efeito Hall** de forma interativa, visual e acessível. Desenvolvido com Python, VPython e Arduino, o projeto permite explorar o comportamento de cargas elétricas em um campo magnético e compreender a variação da tensão Hall com a distância de um ímã. 

---

## Sumário

- [Sobre o projeto](#-sobre-o-projeto)
- [Funcionalidades](#-funcionalidades)
- [Como Executar](#-como-executar)
- [Especificações Técnicas](#-especificações-técnicas)
- [Contribuições da Equipe](#-contribuições-da-equipe)

---

## Sobre o projeto

###  Introdução

O **Efeito Hall** é um fenômeno no qual uma diferença de potencial é gerada perpendicularmente a um condutor percorrido por corrente elétrica, quando submetido a um campo magnético. A partir dos programas apresentados no projeto, o **HELLO, world!** tem como objetivo tornar o Efeito Hall mais **compreensível** e visual através de: 
- Simulação do movimento dos elétrons sob campos elétrico e magnético 
- Análise gráfica da relação entre **tensão Hall** e **distância do ímã** 
- Possibilidade de coleta de dados experimentais com **sensor Hall + Arduino** 
- Analisar e comparar graficamente tensões Hall experimentais e teóricas..
- Fornecer uma interface educacional para explorar o fenômeno de forma dinâmica.

---

##  Funcionalidades

-  **Simulação 3D interativa** com VPython  
- **Aquisição de dados reais** via Arduino (sensor SS49E)  
- **Dois modos de operação**:
  - **Teórico**: baseia-se na relação \( B \propto \frac{1}{d^3} \)
  - **Experimental**: coleta dados em tempo real do sensor  
-  **Gráficos interativos** da tensão Hall em função da distância do imã
- **Interface educacional** com parâmetros ajustáveis no modo teórico 

---

## Como Executar

### Requisitos

- Python 3.x  
- Arduino IDE  
- Bibliotecas: `vpython`, `serial`, `time`  
- Protoboard, 3 jumpers macho-macho  
- Sensor Hall SS49E  
- Ímã (para testes experimentais)  

---

###  Instalação

```bash
git clone https://github.com/EdelioGabriel/Projeto_PCD_Efeito_Hall.git
cd Projeto_PCD_Efeito_Hall
pip install vpython serial time

---

### Rodando o código:

1)	Montagem do Circuito

Com o sensor Hall voltado para você (inscrição **"49E/455BG"** visível):

-  **Perna esquerda** → Conecte à porta **5V** do Arduino (via jumper)
-  **Perna central** → Conecte ao **GND** (terra)
- **Perna direita** → Conecte à entrada **A0** (analógica)

Conecte o Arduino ao computador pela **porta COM3** e carregue o código `efeito_hall_reduzido_final.ino` usando a Arduino IDE.

---

### Executando o Código

O repositório tem três arquivos de códigos principais: efeito_hall_reduzido_final.ino, codigo_reduzido_final.py e interface_teorico.py

1. **Carregando o código do Arduino** - efeito_hall_reduzido_final.ino
Com o sensor Hall voltado para você (inscrição **"49E/455BG"** visível), monte o seguinte circuito:
-  **Perna esquerda** → Conecte à porta **5V** do Arduino (via jumper)
-  **Perna central** → Conecte ao **GND** (terra)
- **Perna direita** → Conecte à entrada **A0** (analógica)
Conecte o Arduino ao computador pela **porta COM3** e carregue o código `efeito_hall_reduzido_final.ino` usando a Arduino IDE.

2. **Modo Experimental ou Teórico (VSCode)**  - codigo_reduzido_final.py
   Execute o arquivo `codigo_reduzido_final.py` no VSCode.  
   O programa irá coletar dados do sensor (modo experimental) ou gerar dados simulados (modo teórico), e exibir o gráfico resultante e a simulação desejada.

3. **Modo Teórico com Interface Interativa (GlowScript)**  - interface_teorico.py
   Execute o arquivo `interface_teorico.py` no ambiente [GlowScript](https://www.glowscript.org/).  
   O usuário poderá selecionar diferentes ímãs, ajustar distâncias e visualizar a dinâmica das cargas elétricas sob o campo magnético.

---

## Especificações Técnicas

### Linguagens e Tecnologias

- **Python** – Análise de dados, simulações físicas
- **VPython / GlowScript** – Visualização 3D interativa
- **C++ (Arduino IDE)** – Leitura do sensor e comunicação serial

###  Bibliotecas Utilizadas
 - vpython: Visualização física 3D         
- gcurve: Gráficos dinâmicos no VPython 
- serial: Comunicação com a porta COM  
- time: Controle de tempo e delays 

---

###  Modelo Físico

####  Cálculo da Tensão Hall:

\[
V_H = \frac{I \cdot B}{n \cdot q \cdot t}
\]

Onde:

- \( I \): corrente elétrica  
- \( B \): campo magnético  
- \( n \): densidade de portadores de carga  
- \( q \): carga do elétron  
- \( t \): espessura do condutor

#### Força de Lorentz:

\[
\vec{F} = q(\vec{E} + \vec{v} \times \vec{B})
\]

---

##  Contribuições da Equipe

- Edélio Gabriel Magalhães de Jesus: criação da simulação 3d do efeito Hall
- Gisela Ceresér Kassick: programação do Arduino e do código de medição e recebimentos de dados experimentais
- Giulia Salles Ferreira: criação do código de recebimento de dados teóricos e plotagem de gráficos
- Leonardo Ritchielly dos S Vieira: criação da interface do código do Glowscript

Os documentos do trabalho (Readme, pdfs explicativos e apresentação) foram feito em conjunto pelo grupo.


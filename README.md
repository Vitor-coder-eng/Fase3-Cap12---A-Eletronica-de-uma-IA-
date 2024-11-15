![Logo FIAP](https://github.com/Vitor-coder-eng/Fase3-Cap12---A-Eletronica-de-uma-IA-/blob/main/logo-fiap.png)

# Fase 3: Cap 12 - A Eletrônica de uma IA

# Objetivo do Projeto

O objetivo deste projeto é desenvolver um sistema de monitoramento e controle agrícola que integre diferentes sensores para automatizar a gestão de irrigação, segurança e luminosidade. Esse sistema visa otimizar o uso dos recursos hídricos, aumentar a segurança da propriedade e monitorar o ambiente climático em tempo real, proporcionando melhores condições para o desenvolvimento das culturas e reduzindo custos operacionais.

Através de sensores de temperatura e umidade (DHT22), ultrassom (HC-SR04), movimento (PIR) e luz (LDR), o sistema é capaz de:

  Ajustar automaticamente a irrigação com base nas condições de temperatura, umidade e intensidade de luz, evitando o desperdício de água em dias nublados ou aumentando a irrigação em condições de alta luminosidade.

  Monitorar o nível de água nos reservatórios, garantindo que a irrigação só ocorra quando há água suficiente, evitando o desgaste do sistema e promovendo a eficiência hídrica.

  Aumentar a segurança através da detecção de movimento em áreas estratégicas, protegendo a propriedade contra invasões indesejadas e monitorando a presença de animais.

Este sistema proporciona um ambiente mais sustentável e eficiente, facilitando a vida do agricultor e contribuindo para a modernização das práticas agrícolas.

# Desenho do circuito
![Desenho do circuito](https://github.com/Vitor-coder-eng/Fase3-Cap12---A-Eletronica-de-uma-IA-/blob/main/Desenho%20do%20circuito.png)

# Descrição dos Sensores

 ### DHT22 - Sensor de Umidade e Temperatura
  Função: Mede a temperatura e a umidade do ambiente.
  Aplicação: Os dados coletados por esse sensor são usados para monitorar o clima no ambiente agrícola, permitindo que o sistema tome decisões sobre o nível de irrigação necessário. Quando a temperatura estiver alta ou a umidade estiver baixa, o sistema pode aumentar a irrigação automaticamente para manter as condições ideais para as plantas.

 ### HC-SR04 - Sensor de Ultrassom
  Função: Mede a distância de objetos, no caso, a altura da coluna de água em um reservatório.
  Aplicação: Posicionado dentro do reservatório de água, ele identifica quando o nível da água está próximo, ou seja, reservatório cheio e quando o nível da água está baixo, assim controlando a irrigação dependendo do nível da água, prevenindo o esvaziamento completo do tanque, além de controlar a bomba d'água.

### PIR - Sensor de Movimento
  Função: Detecta a presença de pessoas ou animais em movimento.
  Aplicação: Esse sensor é usado para segurança, monitorando áreas da fazenda onde animais ou pessoas não deveriam estar. Se detecta um movimento, ele pode acionar um alarme visual (como um LED piscante).

### LDR - Sensor de Luz
  Função: Detecta a intensidade da luz solar no ambiente.
  Aplicação: O sensor LDR monitora o nível de luz ambiente e ajuda o sistema a ajustar o nível de irrigação. Em dias ensolarados, o sistema pode reduzir a quantidade de água, enquanto em dias nublados, pode aumentar a irrigação para compensar a menor quantidade de luz.

# Configuração do Projeto no Wokwi e ESP32 

### Acessar o Wokwi: 

Entre no Wokwi e faça login. 

No painel inicial, clique em “New Project” e escolha o microcontrolador ESP32. 

### Adicionar Sensores: 

No projeto, clique em “Add Part” e adicione os sensores conforme o projeto: 

DHT22 (Sensor de Umidade e Temperatura): Conecte o pino de dados ao GPIO 4. 

HC-SR04 (Sensor Ultrassônico): Conecte os pinos Trigger e Echo ao GPIO 5 e GPIO 18. 

PIR (Sensor de Movimento): Conecte o pino de dados ao GPIO 19. 

LDR (Sensor de Luz): Conecte o LDR ao pino analógico GPIO 34. 

LED (Led vermelho para simular alarme): Conecte o LED ao pino VCC 4 de 3.3V (É importante ressaltar que o LED vermelho que estamos usando nesse circuito tem uma tensão de trabalho de 2V, ou seja, não se esqueça de usar um Resistor para atuar como um freio da corrente elétrica para que não queime o LED). 

### Alimentação e GND: 

Conecte os pinos VCC dos sensores ao pino 3.3V do ESP32. 

Conecte todos os GND dos sensores ao GND do ESP32. 

### Upload do Código: 

No editor do Wokwi, copie e cole o código do projeto. 

### Rodar a Simulação: 

Clique em “Start Simulation” para iniciar o monitoramento dos sensores. 

Acompanhe o Monitor Serial para verificar as leituras dos sensores e o comportamento do sistema de irrigação e segurança. 

#  Instalação e Dependências 

### Biblioteca DHT.h 

Função: Necessária para o funcionamento do sensor DHT22, que mede a temperatura e umidade do ambiente. 

Instalação: No ambiente de simulação Wokwi, a biblioteca DHT é automaticamente carregada quando você define o sensor DHT22. Se você rodar o projeto localmente (como no Arduino IDE), pode instalar a biblioteca DHT seguindo estes passos: 

Abra o Arduino IDE. 

Vá até Sketch > Incluir Biblioteca > Gerenciar Bibliotecas... 

Na barra de busca, digite DHT e selecione a biblioteca "DHT sensor library for Arduino" de autoria de Adafruit. 

Clique em Instalar. 

### Biblioteca Wire.h 

Função: Utilizada para estabelecer comunicação I2C entre dispositivos. No caso de uso do ESP32 no Wokwi, essa biblioteca estará disponível por padrão no ambiente. 

# Testes realizados - Monitor serial
![Print do monitor serial dos testes realizados](https://github.com/Vitor-coder-eng/Fase3-Cap12---A-Eletronica-de-uma-IA-/blob/main/Print%20dos%20dados.png)

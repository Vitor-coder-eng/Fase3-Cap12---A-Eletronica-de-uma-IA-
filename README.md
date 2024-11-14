![Logo FIAP](https://github.com/Vitor-coder-eng/Fase3-Cap12---A-Eletronica-de-uma-IA-/blob/main/logo-fiap.png)

# Fase 3: Cap 12 - A Eletrônica de uma IA

# Objetivo do Projeto

### O objetivo deste projeto é desenvolver um sistema de monitoramento e controle agrícola que integre diferentes sensores para automatizar a gestão de irrigação, segurança e luminosidade. Esse sistema visa otimizar o uso dos recursos hídricos, aumentar a segurança da propriedade e monitorar o ambiente climático em tempo real, proporcionando melhores condições para o desenvolvimento das culturas e reduzindo custos operacionais.

### Através de sensores de temperatura e umidade (DHT22), ultrassom (HC-SR04), movimento (PIR) e luz (LDR), o sistema é capaz de:

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
  Aplicação: Posicionado dentro do reservatório de água, ele calcula o nível da água restante. Quando a água atinge um nível baixo (por exemplo, 20 cm do sensor), o sistema é alertado para evitar irrigação, prevenindo o esvaziamento completo do tanque.

### PIR - Sensor de Movimento
  Função: Detecta a presença de pessoas ou animais em movimento.
  Aplicação: Esse sensor é usado para segurança, monitorando áreas da fazenda onde animais ou pessoas não deveriam estar. Se detecta um movimento, ele pode acionar um alarme visual (como um LED piscante) e sonoro (buzina) para alertar sobre a intrusão.

### LDR - Sensor de Luz
  Função: Detecta a intensidade da luz solar no ambiente.
  Aplicação: O sensor LDR monitora o nível de luz ambiente e ajuda o sistema a ajustar o nível de irrigação. Em dias ensolarados, o sistema pode reduzir a quantidade de água, enquanto em dias nublados, pode aumentar a irrigação para compensar a menor quantidade de luz.

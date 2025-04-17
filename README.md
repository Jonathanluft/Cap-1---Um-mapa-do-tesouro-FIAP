Nosso modelo de negócio consiste em um aplantação monitorada por 3 sensores que monitoram o solo diariamente. Esses sensores tiram diferentes medidas e análises durante o decorrer do dia e em seguida enviam para um servidor único. Neste servidor todas as informações são armazenadas e processadas e os dados são transferidos para a interface que faz a função de mostrar os resultados para o usuário final.

De começo, declaramos 3 entidades entituladas respectivamente como sensor_PH, sensor_NPK e sensor_umidade. Cada uma dessas entidades é dotadas dos seguintes atributos:

- Sensor_PH: 
    - cd_ph (chave primária) - INT
    - cd_servidor (chave estrangeira) - INT
    - ph_solo (1, n) - FLOAT
    - data_ph (1, n) - DATE
    - hora_ph (1, n) - TIME

- Sensor_NPK:
    - cd_npk (chave primária) - INT
    - cd_servidor (chave estrangeira) - INT
    - fosforo (1, n) - FLOAT
    - potassio (1, n) - FLOAT
    - data_npk (1, n) - DATE
    - hora_npk (1, n) - TIME

- Sensor_umidade:
    - cd_umidade (chave primária) - INT
    - cd_servidor (chave estrangeira) - INT
    - umidade_solo (1, n) - FLOAT
    - umidade_ar (1, n) - FLOAT
    - temperatura (1, n) - FLOAT
    - data_umidade (1, n) - DATE
    - hora_umidade (1, n) - TIME

cada um desses 3 elementos tem uma relação (1, n) com o elemento servidor, relação essa em que o servidor pode ter acesso a mais de um sensor, mas um sensor só pode acessar um único servidor.

Dentro da entidade Servidor é armazenadas todos os atributos que os sensores armazenam e repassam através da relação. Além disso, como sua chave primária, tempos o atributo cd_servidor, que também é usado como chave estrangeira dentro dos sensores.

Na sequência, temos a criação de outro elemento entitulado como interface, responsável por passar a informação final ao usuário.
O elemento servidor e interface se interligam através da relação dados (1, 1). A entidade interface possui apenas 3 atributos, sendo eles:

- cd_interface (chave primária) - INT
- cd_servidor (chave estrangeira) - INT
- resultados (0, n) - VARCHAR

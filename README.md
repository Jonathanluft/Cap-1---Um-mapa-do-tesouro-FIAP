# FIAP - Inteligência artificial e data science

<p align="center">
<a href= "https://www.fiap.com.br/"><img src="assets/logo-fiap.png" alt="FIAP - Faculdade de Informática e Admnistração Paulista" border="0" width=40% height=40%></a>
</p>

<br>

# Nome do projeto
Cap 1 - Um mapa do tesouro 

## Nome do grupo
21

## 👨‍🎓 Integrantes: 
- <a href="https://www.linkedin.com/company/inova-fusca">Guilherme Campos Hermanowski </a>
- <a href="https://www.linkedin.com/company/inova-fusca">ana carolina belchior </a>
- <a href="https://www.linkedin.com/company/inova-fusca">Bruno Gambarini </a> 
- <a href="https://www.linkedin.com/company/inova-fusca">Matheus Soares Bento da Silva </a> 
- <a href="https://www.linkedin.com/company/inova-fusca">Jonathan Willian Luft </a>

## 👩‍🏫 Professores:
### Tutor(a) 
- <a href="https://www.linkedin.com/company/inova-fusca">Leonardo Ruiz Orabona</a>
### Coordenador(a)
- <a href="https://www.linkedin.com/company/inova-fusca">ANDRÉ GODOI CHIOVATO</a>


## 📜 Descrição

Nosso modelo de negócio consiste em um sistema de 3 sensores que monitoram uma determinada plantação.
Sendo assim, criamos 3 elementos, um para cada sensor, os intitulamos de acordo e estruturados seus atributos da seguinte forma:

Sensor_ph:

- cd_ph - int - (chave primaria)
- cd_servidor - int (chave estrangeira)
- ph_solo - float - (1, n)
- data_ph - date - (1, n)
- hora_ph - time - (1, n)

Sensor_NPK:

- cd_NPK - int - (chave primaria)
- cd_servidor - int - (chave estrangeira)
- fosforo - float - (1, n)
- potássio - float - (1, n)
- data_npk - date - (1, n)
- hora_npk - time - (1, n)

Sensor_Umidade:

- cd_Umidade - int - (chave primária) 
- cd_servidor - int - (chave secundária)
- umidade solo - float - (1, n)
- umidade ar - float - (1, n)
- temperatura - float - (1, n)
- data umidade - date - (1, n)
- hora umidade - time - (1, n)


Todos esses elementos possuem um relacionamento com o elemento servidor. Nomeado como recebimento de dados, esse relacionamento possui as cardinalidades (1, n) e (1, 1).


O elemento servidor recebe como atributo, além de todos os dados contidos nos demais elementos, o dado cd_servidor, que é sua chave primária e utilizada como chave estrangeira nas outras entidades.

Na sequência, as informações são processadas na entidade servidor e passadas a entidade interface através do relacionamento (1, 1) nomeado como dados.

Por fim temos o elemento interface, que recebe os seguintes atributos:

- cd_interface - int - (chave primária)
- cd_servidor - int - (chave estrangeira)
- resultados - varchar100 - (0, n)



## 📁 Estrutura de pastas

Sem pastas


## 🔧 Como executar o código
-

## 🗃 Histórico de lançamentos

* 0.1.0 - 18/04/2024
    *

## 📋 Licença

<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1"><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1"><p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/"><a property="dct:title" rel="cc:attributionURL" href="https://github.com/agodoi/template">MODELO GIT FIAP</a> por <a rel="cc:attributionURL dct:creator" property="cc:attributionName" href="https://fiap.com.br">Fiap</a> está licenciado sobre <a href="http://creativecommons.org/licenses/by/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">Attribution 4.0 International</a>.</p>



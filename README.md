# TechChallenge-Grupo13-Cliente
Este repositório é dedicado ao microsserviço de clientes, o qual foi desmembrado do monolito criado para a lanchonete durante a evolução da pós-graduação em Arquitetura de Software da FIAP.

Tanto o build e push para o repositório no ECR da AWS usando Terraform, quanto a análise de código e cobertura de testes utilizando SonarCloud são realizados via Github Actions.

## 🖥️ Grupo 13 - Integrantes
🧑🏻‍💻 *<b>RM352133</b>*: Eduardo de Jesus Coruja </br>
🧑🏻‍💻 *<b>RM352316</b>*: Eraldo Antonio Rodrigues </br>
🧑🏻‍💻 *<b>RM352032</b>*: Luís Felipe Amengual Tatsch </br>

## Arquitetura
Quando disparamos a Github Action, é realizado o build da aplicação e o push para o repositório criado previamente no Elastic Container Registry (ECS).
Ao final da action, é atualizada a Service no Elastic Container Service (ECS), executando assim a service que irá realizar a criação do container.

![image](https://github.com/eraldoads/TechChallenge-Grupo13-Cliente/assets/47857203/cc0b90a4-d8f3-4c77-ad54-2d9038e034ff)

Para este microsserviço, utilizamos .NET 8.0, o que também representa uma evolução de tecnologia em relação ao monolito, o qual foi baseado no .NET 6.0 .

## Testes

Utilizamos a ferramenta SonarCloud para análise de código e cobertura de testes. Para este microsserviço, atingimos 98% de cobertura, conforme abaixo:

https://sonarcloud.io/summary/overall?id=eraldoads_TechChallenge-Grupo13-Cliente

![image](https://github.com/eraldoads/TechChallenge-Grupo13-Cliente/assets/47857203/cf911e32-016a-4429-8122-61bc2085eecb)
![image](https://github.com/eraldoads/TechChallenge-Grupo13-Cliente/assets/47857203/0a5ca248-8be2-449d-99a9-1c28eccd486f)


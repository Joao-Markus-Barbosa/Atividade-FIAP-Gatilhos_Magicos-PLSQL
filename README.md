# Atividade-FIAP-Gatilhos_Magicos-PLSQL

## Descrição do Projeto
Este projeto consiste em um sistema de gerenciamento de tráfego urbano, que monitora veículos, câmeras de vigilância e semáforos. O sistema é implementado em um banco de dados Oracle, utilizando tabelas, procedimentos armazenados, funções, pacotes e triggers para automatizar e gerenciar as operações.

## Funcionalidades
Gerenciamento de Veículos: Registra e monitora veículos que passam por determinadas avenidas.

Monitoramento de Câmeras: Controla o status das câmeras de vigilância e a quantidade de veículos que passam por elas.

Controle de Semáforos: Gerencia o status e a localização dos semáforos.

Central de Controle: Integra câmeras e semáforos, permitindo o monitoramento e atualização de seus status.

Automatização: Utiliza triggers para inserir automaticamente registros na tabela central quando novos dados são inseridos na tabela de câmeras.

Relatórios e Consultas: Permite a consulta de dados e a geração de relatórios, como a soma total de passagens de veículos.

## Estrutura do Banco de Dados
Tabelas
central: Armazena o status das câmeras e semáforos, além de integrar as informações das tabelas camera e semaforo.

camera: Registra as passagens de veículos, incluindo a quantidade de veículos, data e avenida.

semaforo: Armazena a localização dos semáforos.

veiculo: Registra os modelos de veículos que passam pelas câmeras.

## Conclusão
Este projeto oferece uma solução robusta para o gerenciamento de tráfego urbano, com funcionalidades que permitem o monitoramento e controle de veículos, câmeras e semáforos. A utilização de triggers e pacotes garante a automatização e eficiência do sistema, enquanto as consultas e relatórios fornecem insights valiosos para a gestão do tráfego.

## Relacionamentos
camera está relacionada com veiculo através de uma chave estrangeira (veiculo_id_veiculo).

central está relacionada com camera e semaforo através de chaves estrangeiras (camera_id_camera e semaforo_id_semaforo).

## Pacotes e Funções
gerenciar_pass_veiculo: Contém uma função para somar todas as passagens de um veículo específico.

gerenciar_status_camera: Contém um procedimento para atualizar o status de uma câmera na tabela central.

gerenciar_status_semaforo: Contém um procedimento para atualizar o status de um semáforo na tabela central.

## Triggers
trg_ins_central: Trigger que insere automaticamente um novo registro na tabela central sempre que um novo registro é inserido na tabela camera.

## Ferramentas Utilizadas
Oracle Database: Sistema de gerenciamento de banco de dados relacional utilizado para armazenar e gerenciar os dados.

PL/SQL: Linguagem de programação utilizada para criar procedimentos armazenados, funções, pacotes e triggers.

SQL*Plus: Ferramenta de linha de comando para interagir com o banco de dados Oracle.

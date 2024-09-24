# Repositório de Eng. de Software

#### Repositório, Gerência de proj sw. 2024/2
- [Repositório de Eng. de Software](#repositório-de-eng-de-software)
      - [Repositório, Gerência de proj sw. 2024/2](#repositório-gerência-de-proj-sw-20242)
- [1. Introdução](#1-introdução)
- [2. Descrição de negócio](#2-descrição-de-negócio)
- [3. Visão geral do sistema](#3-visão-geral-do-sistema)
- [4. Diagrama ER](#4-diagrama-er)
- [5. Diagrama de classe](#5-diagrama-de-classe)
- [6. Casos de uso](#6-casos-de-uso)
- [7. Diagrama de componentes](#7-diagrama-de-componentes)
- [8. Diagramas de implantação](#8-diagramas-de-implantação)
- [9. Protótipo de telas](#9-protótipo-de-telas)
- [10. Diagrama de navegação de telas](#10-diagrama-de-navegação-de-telas)
- [11. Pilha tecnológica](#11-pilha-tecnológica)
- [12. Requisitos de sistemas](#12-requisitos-de-sistemas)
- [13. Considerações sobre segurança](#13-considerações-sobre-segurança)
- [14. Manutenção e instalação](#14-manutenção-e-instalação)
- [15. Glossário](#15-glossário)
- [16. Script SQL](#16-script-sql)
  - [16.1. Comandos CREATE table](#161-comandos-create-table)
  - [16.2. Comandos INSERT table](#162-comandos-insert-table)







# 1. Introdução

O projeto a seguir descreve o desenvolvimento de um sistema personalizado para um petshop. Considerada uma microempresa em fase inicial, a empresa identificou que as soluções de mercado existentes não atendiam às suas necessidades específicas devido à natureza exclusiva de seus serviços. Como resultado, os proprietários decidiram criar uma solução sob medida que se ajustasse perfeitamente às suas operações.

A seguir, detalhamos a solução proposta, que visa atender às necessidades únicas da empresa e proporcionar uma gestão mais eficiente e eficaz dos serviços oferecidos pelo petshop.

# 2. Descrição de negócio
 
1. Uma clínica veterinária atende animais domésticos (gatos e cachorros) e silvestres liberados pelo Ibama (aves como a cacatua e a calopsita, jabutis, iguanas, cobras e furões).
2. Marcar animais com RFID.
3. Os clientes devem fazer um cadastro de si e dos animais.
4. Os clientes devem informar as condições nas quais os animais chegam.
5. Os clientes devem informar o tipo de ração que o animal come. 
6. O cliente deve informar hábitos do animal. 
7. Para cada animal é possível que mais de um veterinário o atenda. 
8. Os animais podem chegar e serem atendidos de acordo com uma agenda do dia. 
9. Cada animal atendido receberá uma ficha e um prontuário. 
10. Outros dono podem querer marcar horários de atendimento futuro. 
11. O atendimento gera uma receita para o animal. 
12. Quando um cliente chega na clínica veterinária ele é atendido por um atendente. 
13. O atendente deve verificar se existe agenda disponível com um veterinário. 
14. O atendente deve colocar o cliente e seu animal na fila de espera, se for o caso. 
15. O atendente deve levar o cliente e o animal até o veterinário. 
16. O veterinário deve realizar uma entrevista com o dono do animal. 
17. O resultado da entrevista deve ir para um formulário. 
18. O veterinário deverá examinar o animal e anotar em prontuário(ficha) suas observações. 
19. Dependendo da situação do animal este receberá uma receita.
20. O pet shop oferece serviços de banho e tosa.
21. A pet shop realiza cirurgias, injeções e curativos.
22. O cliente pode escolher se quer o serviço de pintura de cachorro 
23. São oferecidos serviços de fisioterapia e nutrição
24. O sistema deve permitir que o cliente possa visualizar seus animais e suas fichas.
25. O sistema deve permitir que o cliente possa visualizar suas receitas.
26. A pet shop tem serviços para auxiliar os donos de animais com sobrepeso.
27. O cliente pode receber notificações via SMS ou e-mail quando a consulta ou serviço estiver próximo.
28. O sistema deve permitir que o cliente atualize o cadastro do animal a qualquer momento, como mudança de hábitos ou troca de ração.
29. O cliente deverá ter acesso a carteira de vacinação do animal, bem como ser avisado de vacinas obrigatórias quando próximas.
30. O sistema deve emitir lembretes automáticos sobre a próxima dose de medicamentos prescritos para o animal e permitir o cliente confirmar se deu o medicamento ao animal.
31. O cliente pode visualizar recomendações personalizadas de ração e suplementos com base no histórico de saúde do animal.
Descrição do cenário onde o sistema deve funcionar:

1. Uma clínica veterinária atende animais domésticos (gatos e cachorros) e silvestres liberados pelo Ibama (aves como a cacatua e a calopsita, jabutis, iguanas, cobras e furões).
2. Marcar animais com RFID.
3. Os clientes devem fazer um cadastro de si e dos animais.
4. Os clientes devem informar as condições nas quais os animais chegam.
5. Os clientes devem informar o tipo de ração que o animal come. 
6. O cliente deve informar hábitos do animal. 
7. Para cada animal é possível que mais de um veterinário o atenda. 
8. Os animais podem chegar e serem atendidos de acordo com uma agenda do dia. 
9. Cada animal atendido receberá uma ficha e um prontuário. 
10. Outros dono podem querer marcar horários de atendimento futuro. 
11. O atendimento gera uma receita para o animal. 
12. Quando um cliente chega na clínica veterinária ele é atendido por um atendente. 
13. O atendente deve verificar se existe agenda disponível com um veterinário. 
14. O atendente deve colocar o cliente e seu animal na fila de espera, se for o caso. 
15. O atendente deve levar o cliente e o animal até o veterinário. 
16. O veterinário deve realizar uma entrevista com o dono do animal. 
17. O resultado da entrevista deve ir para um formulário. 
18. O veterinário deverá examinar o animal e anotar em prontuário(ficha) suas observações. 
19. Dependendo da situação do animal este receberá uma receita.
20. O pet shop oferece serviços de banho e tosa.
21. A pet shop realiza cirurgias, injeções e curativos.
22. O cliente pode escolher se quer o serviço de pintura de cachorro 
23. São oferecidos serviços de fisioterapia e nutrição
24. O sistema deve permitir que o cliente possa visualizar seus animais e suas fichas.
25. O sistema deve permitir que o cliente possa visualizar suas receitas.
26. A pet shop tem serviços para auxiliar os donos de animais com sobrepeso.
27. O cliente pode receber notificações via SMS ou e-mail quando a consulta ou serviço estiver próximo.
28. O sistema deve permitir que o cliente atualize o cadastro do animal a qualquer momento, como mudança de hábitos ou troca de ração.
29. O cliente deverá ter acesso a carteira de vacinação do animal, bem como ser avisado de vacinas obrigatórias quando próximas.
30. O sistema deve emitir lembretes automáticos sobre a próxima dose de medicamentos prescritos para o animal e permitir o cliente confirmar se deu o medicamento ao animal.
31. O cliente pode visualizar recomendações personalizadas de ração e suplementos com base no histórico de saúde do animal.
 

# 3. Visão geral do sistema

# 4. Diagrama ER

```mermaid
erDiagram
 Cliente {
      int Id_cliente
        varchar Nome
        varchar Telefone
        varchar Endereco
        varchar Email
 }

    Animal {
        int RFID
        varchar Nome
        varchar Tipo
        varchar Habitos
        varchar Condicao_chegada
        varchar Tipo_racao
    }

    Veterinario {
        int Id_veterinario
        varchar Nome
        varchar CRMV
        varchar Especialidade
    }

    Atendente {
        int Id_atendente
        varchar Nome
    }

    Consulta {
        int Id_consulta
        date Data
        time Hora
        text Descricao
    }

    Ficha {
        int Id_ficha
        text Descricao
        text Observacoes
    }

    Prontuario {
        int Id_prontuario
        text Receita
        text Observacoes
    }

    Servico {
        int Id_servico
        varchar Tipo
        text Descricao
        decimal Preco
    }
    Agenda {
        int ID_Agenda
        date Data
        time Hora
    }
    Receita {
        int ID_Receita
        string Medicamentos
        string Instrucoes
    }
    Cliente ||--o{ Animal: "possui"
    Animal ||--o{ Ficha : "tem"
    Ficha ||--o{ Prontuario : "contém"
    Animal }o--|| Consulta : "participa"
    Veterinario ||--o{ Consulta : "realiza"
    Atendente ||--o{ Consulta : "organiza"
    Consulta ||--o{ Receita : "gera"
    Cliente ||--o{ Agenda : "marca"
    Animal ||--o{ Servico : "recebe"

```
# 5. Diagrama de classe

```mermaid
classDiagram
    class Cliente {
        +int ID_Pessoa
        +string Nome
        +string Telefone
        +string Endereco
        +string Email
    }
 class Animal {
        +string RFID
        +string Nome
        +string Tipo
        +string Habitos
        +string Condicao_chegada
        +string Tipo_racao
        +int ID_Pessoa
    }
    class Veterinario {
        +int ID_Veterinario
        +string Nome
        +string CRMV
        +string Especialidade
    }
    class Atendente {
        +int ID_Atendente
        +string Nome
    }
    class Consulta {
        +int ID_Consulta
        +date Data
        +time Hora
        +string Descricao
        +string RFID
        +int ID_Veterinario
        +int ID_Atendente
    }
    class Ficha {
        +int ID_Ficha
        +string Descricao
        +string Observacoes
        +string RFID
    }
    class Prontuario {
        +int ID_Prontuario
        +string Receita
        +string Observacoes
        +string RFID
    }
     class Servico {
        +int ID_Servico
        +string Tipo
        +string Descricao
        +decimal Preco
    }
    class Agenda {
        +int ID_Agenda
        +date Data
        +time Hora
        +string RFID
        +int ID_Veterinario
    }
    class Receita {
        +int ID_Receita
        +string Medicamentos
        +string Instrucoes
        +string RFID
    }

    class Notificacao {
        +int ID_Notificacao
        +string Tipo
        +string Mensagem
        +date Data
        +time Hora
        +int ID_Pessoa
    }
    class Vacina {
        +int ID_Vacinacao
        +string Tipo_Vacina
        +date Data
        +string RFID
    }

    class LembreteMedicamento {
        +int ID_Lembrete
        +string Medicamento
        +date Data_Lembrete
        +boolean Confirmacao
        +string RFID
    }
    class Recomendacao {
        +int ID_Recomendacao
        +string Racao_Recomendada
        +string Suplemento_Recomendado
        +string RFID
    }

    Cliente "1" -- "0..*" Animal : possui >
    Animal "1" -- "0..*" Consulta : participa >
    Veterinario "1" -- "0..*" Consulta : realiza >
    Atendente "1" -- "0..*" Consulta : realiza >
    Animal "1" -- "0..1" Ficha : recebe >
    Animal "1" -- "0..1" Prontuario : recebe >
    Animal "1" -- "0..*" Agenda : agendado em >
    Animal "1" -- "0..*" Receita : recebe >
    Cliente "1" -- "0..*" Notificacao : recebe >
    Animal "1" -- "0..*" Vacina : possui >
    Animal "1" -- "0..*" LembreteMedicamento : possui >
    Animal "1" -- "0..*" Recomendacao : recebe >
```
# 6. Casos de uso

# 7. Diagrama de componentes

# 8. Diagramas de implantação

# 9. Protótipo de telas

# 10. Diagrama de navegação de telas

# 11. Pilha tecnológica

# 12. Requisitos de sistemas

# 13. Considerações sobre segurança

# 14. Manutenção e instalação

# 15. Glossário

# 16. Script SQL

## 16.1. Comandos CREATE table
```sql

CREATE DATABASE IF NOT EXISTS ClinicaVeterinaria;
USE ClinicaVeterinaria;

-- Tabela CLIENTE
CREATE TABLE CLIENTE (
    ID_Pessoa INT AUTO_INCREMENT PRIMARY KEY,
    Nome VARCHAR(100) NOT NULL,
    Telefone VARCHAR(15),
    Endereco VARCHAR(255),
    Email VARCHAR(100) UNIQUE NOT NULL
);

-- Tabela ANIMAL
CREATE TABLE ANIMAL (
    RFID VARCHAR(50) PRIMARY KEY,
    Nome VARCHAR(100) NOT NULL,
    Tipo ENUM('Gato', 'Cachorro', 'Ave', 'Jabuti', 'Iguana', 'Cobra', 'Furão') NOT NULL,
    Habitos TEXT,
    Condicao_chegada TEXT,
    Tipo_racao VARCHAR(100),
    ID_Pessoa INT,
    FOREIGN KEY (ID_Pessoa) REFERENCES CLIENTE(ID_Pessoa)
);

-- Tabela VETERINARIO
CREATE TABLE VETERINARIO (
    ID_Veterinario INT AUTO_INCREMENT PRIMARY KEY,
    Nome VARCHAR(100) NOT NULL,
    CRMV VARCHAR(20) UNIQUE NOT NULL,
    Especialidade VARCHAR(100)
);

-- Tabela ATENDENTE
CREATE TABLE ATENDENTE (
    ID_Atendente INT AUTO_INCREMENT PRIMARY KEY,
    Nome VARCHAR(100) NOT NULL
);

-- Tabela CONSULTA
CREATE TABLE CONSULTA (
    ID_Consulta INT AUTO_INCREMENT PRIMARY KEY,
    Data DATE NOT NULL,
    Hora TIME NOT NULL,
    Descricao TEXT,
    RFID VARCHAR(50),
    ID_Veterinario INT,
    ID_Atendente INT,
    FOREIGN KEY (RFID) REFERENCES ANIMAL(RFID),
    FOREIGN KEY (ID_Veterinario) REFERENCES VETERINARIO(ID_Veterinario),
    FOREIGN KEY (ID_Atendente) REFERENCES ATENDENTE(ID_Atendente)
);

-- Tabela FICHA
CREATE TABLE FICHA (
    ID_Ficha INT AUTO_INCREMENT PRIMARY KEY,
    Descricao TEXT,
    Observacoes TEXT,
    RFID VARCHAR(50),
    FOREIGN KEY (RFID) REFERENCES ANIMAL(RFID)
);

-- Tabela PRONTUARIO
CREATE TABLE PRONTUARIO (
    ID_Prontuario INT AUTO_INCREMENT PRIMARY KEY,
    Receita TEXT,
    Observacoes TEXT,
    RFID VARCHAR(50),
    FOREIGN KEY (RFID) REFERENCES ANIMAL(RFID)
);

-- Tabela SERVICO
CREATE TABLE SERVICO (
    ID_Servico INT AUTO_INCREMENT PRIMARY KEY,
    Tipo ENUM('Banho', 'Tosa', 'Cirurgia', 'Injeção', 'Curativo', 'Pintura', 'Fisioterapia', 'Nutrição', 'Sobrepeso') NOT NULL,
    Descricao TEXT,
    Preco DECIMAL(10, 2)
);

-- Tabela AGENDA
CREATE TABLE AGENDA (
    ID_Agenda INT AUTO_INCREMENT PRIMARY KEY,
    Data DATE NOT NULL,
    Hora TIME NOT NULL,
    RFID VARCHAR(50),
    ID_Veterinario INT,
    FOREIGN KEY (RFID) REFERENCES ANIMAL(RFID),
    FOREIGN KEY (ID_Veterinario) REFERENCES VETERINARIO(ID_Veterinario)
);

-- Tabela RECEITA
CREATE TABLE RECEITA (
    ID_Receita INT AUTO_INCREMENT PRIMARY KEY,
    Medicamentos TEXT,
    Instrucoes TEXT,
    RFID VARCHAR(50),
    FOREIGN KEY (RFID) REFERENCES ANIMAL(RFID)
);

-- Tabela NOTIFICACAO (para SMS e e-mail)
CREATE TABLE NOTIFICACAO (
    ID_Notificacao INT AUTO_INCREMENT PRIMARY KEY,
    Tipo ENUM('SMS', 'Email') NOT NULL,
    Mensagem TEXT,
    Data DATE NOT NULL,
    Hora TIME NOT NULL,
    ID_Pessoa INT,
    FOREIGN KEY (ID_Pessoa) REFERENCES CLIENTE(ID_Pessoa)
);

-- Tabela VACINACAO
CREATE TABLE VACINACAO (
    ID_Vacinacao INT AUTO_INCREMENT PRIMARY KEY,
    Tipo_Vacina VARCHAR(100) NOT NULL,
    Data DATE NOT NULL,
    RFID VARCHAR(50),
    FOREIGN KEY (RFID) REFERENCES ANIMAL(RFID)
);

-- Tabela LEMBRETE_MEDICAMENTO
CREATE TABLE LEMBRETE_MEDICAMENTO (
    ID_Lembrete INT AUTO_INCREMENT PRIMARY KEY,
    Medicamento VARCHAR(100),
    Data_Lembrete DATE,
    Confirmacao BOOLEAN,
    RFID VARCHAR(50),
    FOREIGN KEY (RFID) REFERENCES ANIMAL(RFID)
);

-- Tabela RECOMENDACAO
CREATE TABLE RECOMENDACAO (
    ID_Recomendacao INT AUTO_INCREMENT PRIMARY KEY,
    Racao_Recomendada VARCHAR(100),
    Suplemento_Recomendado VARCHAR(100),
    RFID VARCHAR(50),
    FOREIGN KEY (RFID) REFERENCES ANIMAL(RFID)
);
```
## 16.2. Comandos INSERT table

```sql
-- Inserir dados na tabela CLIENTE
INSERT INTO CLIENTE (Nome, Telefone, Endereco, Email) VALUES
('João da Silva', '1234-5678', 'Rua das Flores, 123', 'joao.silva@email.com'),
('Maria Oliveira', '9876-5432', 'Avenida Central, 456', 'maria.oliveira@email.com'),
('Carlos Pereira', '5555-6666', 'Praça da Liberdade, 789', 'carlos.pereira@email.com');

-- Inserir dados na tabela ANIMAL
INSERT INTO ANIMAL (RFID, Nome, Tipo, Habitos, Condicao_chegada, Tipo_racao, ID_Pessoa) VALUES
('RFID001', 'Rex', 'Cachorro', 'Muito ativo', 'Machucado', 'Ração Premium', 1),
('RFID002', 'Miau', 'Gato', 'Preguiçoso', 'Saudável', 'Ração Gourmet', 2),
('RFID003', 'Pico', 'Ave', 'Cantor', 'Com febre', 'Ração para Aves', 3);

-- Inserir dados na tabela VETERINARIO
INSERT INTO VETERINARIO (Nome, CRMV, Especialidade) VALUES
('Dr. Pedro Almeida', 'CRMV-12345', 'Clínico Geral'),
('Dra. Ana Costa', 'CRMV-67890', 'Especialista em Aves'),
('Dr. Bruno Santos', 'CRMV-54321', 'Cirurgias');

-- Inserir dados na tabela ATENDENTE
INSERT INTO ATENDENTE (Nome) VALUES
('Lucas Martins'),
('Fernanda Lima');

-- Inserir dados na tabela CONSULTA
INSERT INTO CONSULTA (Data, Hora, Descricao, RFID, ID_Veterinario, ID_Atendente) VALUES
('2024-09-20', '09:00:00', 'Exame de rotina', 'RFID001', 1, 1),
('2024-09-21', '10:00:00', 'Vacinação', 'RFID002', 2, 2),
('2024-09-22', '11:00:00', 'Tratamento de febre', 'RFID003', 1, 2);

-- Inserir dados na tabela FICHA
INSERT INTO FICHA (Descricao, Observacoes, RFID) VALUES
('Ficha de exame de rotina', 'Tudo normal', 'RFID001'),
('Ficha de vacinação', 'Vacinas em dia', 'RFID002'),
('Ficha de tratamento', 'Precisa de cuidados adicionais', 'RFID003');

-- Inserir dados na tabela PRONTUARIO
INSERT INTO PRONTUARIO (Receita, Observacoes, RFID) VALUES
('Ração especial para recuperação', 'Reavaliar em 30 dias', 'RFID001'),
('Vacina contra gripe', 'Manter acompanhamento', 'RFID002'),
('Medicamento para febre', 'Monitorar temperatura', 'RFID003');

-- Inserir dados na tabela SERVICO
INSERT INTO SERVICO (Tipo, Descricao, Preco) VALUES
('Banho', 'Banho completo para cães e gatos', 50.00),
('Tosa', 'Tosa completa para cães', 70.00),
('Cirurgia', 'Cirurgia geral', 300.00),
('Injeção', 'Aplicação de injeção', 40.00),
('Curativo', 'Curativo em feridas', 30.00);

-- Inserir dados na tabela AGENDA
INSERT INTO AGENDA (Data, Hora, RFID, ID_Veterinario) VALUES
('2024-09-23', '08:00:00', 'RFID001', 1),
('2024-09-24', '09:00:00', 'RFID002', 2),
('2024-09-25', '10:00:00', 'RFID003', 3);

-- Inserir dados na tabela RECEITA
INSERT INTO RECEITA (Medicamentos, Instrucoes, RFID) VALUES
('Antibiótico X', 'Administrar 2 vezes ao dia', 'RFID001'),
('Vacina Y', 'Aplicar uma dose', 'RFID002'),
('Antipirético Z', 'Tomar a cada 8 horas', 'RFID003');

-- Inserir dados na tabela NOTIFICACAO
INSERT INTO NOTIFICACAO (Tipo, Mensagem, Data, Hora, ID_Pessoa) VALUES
('SMS', 'Lembrete: Consulta agendada para amanhã.', '2024-09-19', '10:00:00', 1),
('Email', 'Seu animal precisa de uma revisão na próxima semana.', '2024-09-18', '09:00:00', 2);

-- Inserir dados na tabela VACINACAO
INSERT INTO VACINACAO (Tipo_Vacina, Data, RFID) VALUES
('Vacina contra gripe', '2024-09-20', 'RFID002'),
('Vacina antirrábica', '2024-09-25', 'RFID001');

-- Inserir dados na tabela LEMBRETE_MEDICAMENTO
INSERT INTO LEMBRETE_MEDICAMENTO (Medicamento, Data_Lembrete, Confirmacao, RFID) VALUES
('Antibiótico X', '2024-09-22', FALSE, 'RFID001'),
('Antipirético Z', '2024-09-23', FALSE, 'RFID003');

-- Inserir dados na tabela RECOMENDACAO
INSERT INTO RECOMENDACAO (Racao_Recomendada, Suplemento_Recomendado, RFID) VALUES
('Ração Premium', 'Suplemento Vitaminico A', 'RFID001'),
('Ração Gourmet', 'Suplemento Mineral B', 'RFID002');
```

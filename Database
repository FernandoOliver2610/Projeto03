-- Criando o banco de dados
CREATE DATABASE TechSales;
USE TechSales;

-- Criando a tabela de clientes
CREATE TABLE clientes (
    cliente_id INT PRIMARY KEY AUTO_INCREMENT,
    nome VARCHAR(100),
    idade INT,
    cidade VARCHAR(100),
    estado VARCHAR(50),
    data_cadastro DATE
);

-- Criando a tabela de produtos
CREATE TABLE produtos (
    produto_id INT PRIMARY KEY AUTO_INCREMENT,
    nome VARCHAR(100),
    categoria VARCHAR(50),
    preco DECIMAL(10,2)
);

-- Criando a tabela de vendas
CREATE TABLE vendas (
    venda_id INT PRIMARY KEY AUTO_INCREMENT,
    cliente_id INT,
    produto_id INT,
    data_venda DATE,
    quantidade INT,
    valor_total DECIMAL(10,2),
    FOREIGN KEY (cliente_id) REFERENCES clientes(cliente_id),
    FOREIGN KEY (produto_id) REFERENCES produtos(produto_id)
);

-- Inserindo dados fictícios
INSERT INTO clientes (nome, idade, cidade, estado, data_cadastro) VALUES
('Carlos Silva', 35, 'São Paulo', 'SP', '2021-06-15'),
('Ana Souza', 28, 'Rio de Janeiro', 'RJ', '2022-03-22'),
('Bruno Lima', 42, 'Belo Horizonte', 'MG', '2020-11-10'),
('Mariana Costa', 31, 'Curitiba', 'PR', '2023-07-05');

INSERT INTO produtos (nome, categoria, preco) VALUES
('Notebook Dell XPS', 'Eletrônicos', 8500.00),
('Smartphone Samsung S23', 'Eletrônicos', 5000.00),
('Fone de Ouvido JBL', 'Acessórios', 350.00),
('Monitor LG 27"', 'Eletrônicos', 2200.00);

INSERT INTO vendas (cliente_id, produto_id, data_venda, quantidade, valor_total) VALUES
(1, 1, '2023-10-01', 1, 8500.00),
(2, 2, '2023-11-15', 2, 10000.00),
(3, 3, '2023-12-20', 3, 1050.00),
(4, 4, '2024-01-05', 1, 2200.00);

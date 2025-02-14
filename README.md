# Projeto: SQL para Análise de Negócios

## 📌 Objetivo do Projeto
Este projeto tem como objetivo demonstrar a aplicação de consultas SQL para análise de negócios utilizando um banco de dados fictício. A análise foca na extração de insights relevantes a partir de transações de vendas, identificando padrões de consumo, clientes estratégicos e desempenho de produtos.

## 🏢 Sobre a Empresa Fictícia - TechSales Inc.
A **TechSales Inc.** é uma empresa fictícia de tecnologia especializada na venda de eletrônicos e acessórios. O banco de dados armazena informações sobre clientes, produtos e vendas, possibilitando análises detalhadas para melhorar a tomada de decisão.

## 📊 Estrutura do Banco de Dados
O banco de dados **TechSales** contém três tabelas principais:

1. **clientes**: Contém informações dos clientes, como nome, idade, cidade, estado e data de cadastro.
2. **produtos**: Registra os produtos vendidos, incluindo nome, categoria e preço.
3. **vendas**: Armazena as transações de vendas, relacionando clientes e produtos, além de registrar a quantidade vendida e o valor total.

## 🔍 Consultas e Insights Obtidos

### 1️⃣ **Total de Vendas por Produto**
Esta consulta retorna os produtos mais vendidos e a receita total gerada por cada um.

📌 **Insight:** O produto mais lucrativo pode ser priorizado em campanhas promocionais.

```sql
SELECT p.nome AS Produto, SUM(v.quantidade) AS Total_Vendido, SUM(v.valor_total) AS Receita_Total
FROM vendas v
JOIN produtos p ON v.produto_id = p.produto_id
GROUP BY p.nome
ORDER BY Receita_Total DESC;
```

---

### 2️⃣ **Clientes que Mais Compraram**
Identifica os clientes que mais gastaram na empresa.

📌 **Insight:** Clientes de alto valor podem receber ofertas personalizadas para fidelização.

```sql
SELECT c.nome AS Cliente, COUNT(v.venda_id) AS Total_Compras, SUM(v.valor_total) AS Valor_Gasto
FROM vendas v
JOIN clientes c ON v.cliente_id = c.cliente_id
GROUP BY c.nome
ORDER BY Valor_Gasto DESC;
```

---

### 3️⃣ **Receita Total por Estado**
Mostra a distribuição da receita por estado, permitindo entender a força da marca em diferentes regiões.

📌 **Insight:** Estados com baixa receita podem ser alvo de estratégias de marketing para aumentar as vendas.

```sql
SELECT c.estado AS Estado, SUM(v.valor_total) AS Receita_Total
FROM vendas v
JOIN clientes c ON v.cliente_id = c.cliente_id
GROUP BY c.estado
ORDER BY Receita_Total DESC;
```

## 🛠 Tecnologias Utilizadas
- **MySQL** para armazenamento e gerenciamento dos dados.
- **SQL** para consultas e extração de insights.
- **Jupyter Notebook** (opcional) para visualização e análise adicional dos dados.

## 📌 Conclusão
Este projeto demonstrou como utilizar SQL para extrair insights valiosos de um banco de dados comercial. A partir das análises realizadas, a empresa fictícia **TechSales Inc.** pode tomar decisões estratégicas informadas para impulsionar seu crescimento e melhorar o atendimento ao cliente.

📌 **Próximos Passos:**
- Criar visualizações gráficas para os dados extraídos usando Power BI ou Python (Matplotlib/Seaborn).
- Implementar novas consultas para aprofundar a análise do comportamento dos clientes.
- Automatizar relatórios para monitoramento contínuo das vendas.

---

🔗 **LinkedIn:** [Fernando Costa de Oliveira](https://www.linkedin.com/in/fernando-costa-de-oliveira-97b124348)  
📧 **Contato:** [Seu E-mail ou Site Pessoal]


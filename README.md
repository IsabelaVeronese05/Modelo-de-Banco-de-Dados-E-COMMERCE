## Modelo-de-Banco-de-Dados-E-COMMERCE

Este projeto apresenta um modelo relacional de banco de dados para um sistema de E-COMMERCE com múltiplos fornecedores, 
vendedores e clientes, incluindo funcionalidades de geolocalização, pagamento e entrega.

## 📌 Objetivo

Criar uma estrutura robusta e escalável de banco de dados que suporte operações típicas de E-COMMERCE, como:

- Cadastro de clientes e fornecedores.
- Processamento de pedidos.
- Controle de estoque.
- Acompanhamento de entregas.
- Pagamentos.
- Integração com terceiros vendedores.

---

## 🗺️ Diagrama Entidade-Relacionamento (DER)

![e-commerce](https://github.com/user-attachments/assets/5454f99b-7ecb-420c-8482-1c908915ac74)

---

## 🗂️ Descrição das Tabelas

### Cliente
- Cadastro dos clientes.
- Inclui CPF, e-mail e endereço com geolocalização (MULTIPOINT).

### Pedido
- Registro de pedidos realizados.
- Relacionado a um cliente e vários produtos.

### Produto
- Catálogo de produtos.
- Inclui preço, quantidade em estoque e descrição.

### Pagamento
- Informações de pagamento associadas ao pedido.
- Inclui valor total, data e status.

### Entrega
- Rastreamento das entregas dos pedidos.
- Inclui datas e código de rastreamento.

### Fornecedor
- Cadastro dos fornecedores.
- Inclui CNPJ e localização (MULTIPOINT).

### Terceiro_Vendedor
- Representação de vendedores parceiros do marketplace.
- Localização em MULTIPOINT.

### Terceiro_Vendedor_Fornecedor
- Tabela de junção que relaciona fornecedores e vendedores terceiros.
- Permite modelar marketplaces complexos com múltiplos intermediários.

---

## 🔗 Relacionamentos

- Cliente → Pedido: 1:N
- Pedido → Produto: N:M (com chaves compostas).
- Pedido → Pagamento: 1:N
- Pedido → Entrega: 1:1
- Fornecedor → Produto: 1:N
- Fornecedor → Terceiro_Vendedor_Fornecedor: 1:N
- Terceiro_Vendedor → Terceiro_Vendedor_Fornecedor: 1:N

---

## 💾 Tecnologias e SGBD

- Modelado para uso com: *MySQL* ou *PostgreSQL*.
- Ferramentas recomendadas: MySQL Workbench, DBeaver.

---

## 📈 Exemplos de Consultas

- Listar todos os pedidos de um cliente.
- Verificar estoque de um produto.
- Consultar status de pagamento.
- Acompanhar a entrega de um pedido.

(Disponíveis em sql/exemplo_consultas.sql)

---

## 📝 Licença

Este projeto está licenciado sob a *MIT License*.


---

## ✨ Autor

- Isabela Veronese 
- GitHub:[meu perfil](https://github.com/IsabelaVeronese05)
- LinkedIn: [Meu LinkedIn](https://www.linkedin.com/in/isabela-veronese-11058a260)

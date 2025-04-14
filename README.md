# Teste-Caixa-Branca-e-Caixa-Preta
*rodando código com erro*

# primeiros passos 
A
Durante a execução inicial do projeto, foi identificado que a aplicação não conseguia se conectar ao banco de dados. Após análise do código, foi identificada uma divergência entre as configurações de banco de dados no código-fonte e os dados reais do banco.

# Alterações realizadas

db.datasource.jdbcurl=jdbc:mysql://cleberleao.com:3306/cleberleao_oficina?allowPublicKeyRetrieval=true&useSSL=false
db.datasource.username=cleberleao_oficina
db.datasource.password=mysql123oficina

Com essas mudanças, a aplicação foi iniciada corretamente: "2025-04-10 20:46:12.604  INFO 9948 --- [  restartedMain] c.c.o.s.OficinaSpringBootApplication     : Started OficinaSpringBootApplication in 10.493 seconds (JVM running for 12.213)"

![image](https://github.com/user-attachments/assets/92cc346e-cc13-4951-b962-94dc4c302ec6)

# Conexão com Banco de Dados
Foi testada e validada a conexão ao banco cleberleao_oficina utilizando o DBeaver, confirmando acesso com a mesma URL "jdbc:mysql://cleberleao.com:3306/cleberleao_oficina" utilizada na aplicação:

![image](https://github.com/user-attachments/assets/63e00518-1e88-4cf3-99e0-71488a3716c8) 

# Testes de Caixa Preta (API podman)
*Cadastro de usuário*

Requisição:

    "nome": "Cleber Leão",
    "email": "cleber@cleberleao.com",
    "password": "123456"

    "nome": "tayssa_aj",
    "email": "tayssa.araujo.com",
    "password": "12345"
    
Esperado: HTTP 201 Created

Resultado: Foram feitas requisições com diferentes dados para atestar e identificar se o erro estava nos dados inseridos, mesmo com diferentes combinações de entrada, a aplicação responde com HTTP 403 como mostra a imagem

![image](https://github.com/user-attachments/assets/225d86f9-bb4b-40a3-b99e-2b437a724b42)

# Problema Identificado

Mesmo com o backend rodando corretamente e banco acessível, todas as requisições retornam HTTP 403, indicando falha de autorização.

# conclusão

A lógica e o funcionamento do código foi validada com sucesso por meio de testes de caixa branca. Porém, os testes de caixa preta revelaram problemas relacionados ao cadastro dos usuarios, impedindo que a funcionalidade seja usada.


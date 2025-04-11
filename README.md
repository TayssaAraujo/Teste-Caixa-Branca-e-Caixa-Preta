# Teste-Caixa-Branca-e-Caixa-Preta
rodando código com erro 

# primeiros passos 
Apos analise do código foi verificado uma divergencia entre os reais dados do banco de dados e os dados escritos no código, foi modificado o codigo e adicionado as seguintes configurações: 

db.datasource.jdbcurl=jdbc:mysql://cleberleao.com:3306/cleberleao_oficina?allowPublicKeyRetrieval=true&useSSL=false
db.datasource.username=cleberleao_oficina
db.datasource.password=mysql123oficina

Dessa forma o código rodou corretamente "2025-04-10 20:46:12.604  INFO 9948 --- [  restartedMain] c.c.o.s.OficinaSpringBootApplication     : Started OficinaSpringBootApplication in 10.493 seconds (JVM running for 12.213)"
![image](https://github.com/user-attachments/assets/92cc346e-cc13-4951-b962-94dc4c302ec6)

Foi feita conexão com o banco de dados atravez do Dbeaver com a url "jdbc:mysql://cleberleao.com:3306/cleberleao_oficina", como mostra imagem abaixo.
![image](https://github.com/user-attachments/assets/63e00518-1e88-4cf3-99e0-71488a3716c8) 

Em seguida foi feita conexão com o podman 
![image](https://github.com/user-attachments/assets/a44a1225-56e0-433f-b25d-45234d2a4451)
as requisições são enviadas sem erro porem não é possivel a visualização dos cadastros.

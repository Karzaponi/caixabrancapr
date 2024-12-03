# caixabrancapr
# Aba da Caixa Branca Preenchida  
Arquivo: [PLANO DE TESTE-1.xlsx](https://github.com/user-attachments/files/17969267/PLANO.DE.TESTE-1.xlsx)  

## Erros Encontrados no Projeto TesteCaixaBranca

### Descrição do Projeto  
Este projeto visa testar a conexão com um banco de dados MySQL utilizando Java. Durante o desenvolvimento, foram identificados e corrigidos os seguintes erros:  

---

### Erros Encontrados

#### 1. Erro ao Conectar ao Banco de Dados  
Mensagem:  
Erro ao conectar ao banco: com.mysql.cj.jdbc.Driver  

Causa:  
O driver MySQL não estava incluído no classpath.  

Solução:  
- Adicionar o arquivo `mysql-connector-j-9.1.0.jar` na pasta `lib`.  
- Configurar corretamente o classpath ao compilar e executar o projeto.  

---

#### 2. Erro de Credenciais no Banco  
Mensagem:  
Conexão com o banco falhou. Falha na autenticação.  

Causa:  
Usuário ou senha configurados de forma incorreta no código Java.  

Solução:  
Verificar e corrigir as credenciais utilizadas no método `DriverManager.getConnection`.  

---

#### 3. Erro no Comando de Compilação  
Mensagem:  
javac: no source files  

Causa:  
O comando para compilar os arquivos Java estava incorreto.  

Solução:  
Utilizar o comando correto:  
```bash
javac -cp .;lib/mysql-connector-j-9.1.0.jar login/src/*.java

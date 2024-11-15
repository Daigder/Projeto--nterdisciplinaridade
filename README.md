<br />
  <br />

  <h1 align="center">Atividade - Interdisciplinaridade - Banco de Dados Avançado: Gerencimento de Transação</h1>

  > Este é um sistema de gerenciamento de clientes. Ele permite cadastrar, listar, atualizar e excluir registros de clientes e controle de concorrência utilizando PostgreSQL.

### Criar um banco de dados com tabela cliente.
Os campos pode incluir quais quiser, mas obrigatoriamente precisa de 2 que são:
- idcliente - Como chave primaria
- limite - como numeric(15,2)
- Inserir alguns clientes.

#### Interdisciplinaridade o que fazer (Criar sistema que faz):
01) busca clientes e lista;
![image](https://github.com/user-attachments/assets/cd4b1ea6-785a-4239-983e-bafc1a04fee8)

02) Permite usuário escolher qual vai alterar;
![image](https://github.com/user-attachments/assets/48af8d33-4cca-47ad-b591-327e6a606ece)

03) Mostra os dados do cliente que será alterado na tela (armazena dados atuais em variáveis);
![image](https://github.com/user-attachments/assets/d122bbe2-3883-4f5c-ac9d-da8d0e1f1dd3)

04) Inicia a transação;
![image](https://github.com/user-attachments/assets/b3315ce8-ad6b-4451-baf7-ec03feb22b9f)

05) Faz novo select no id do cliente (que será atualizado);
![image](https://github.com/user-attachments/assets/5aee5867-ac54-4952-b077-8543e3b4c153)

06) Compara os dados retornados com as variáveis;
![image](https://github.com/user-attachments/assets/c5cba110-6c50-434d-be24-a48ce7695b75)

07) Se dados estão iguais então
![image](https://github.com/user-attachments/assets/f5d4226d-fd2f-42f8-8e5e-39319b160fba)

08) pede confirmação do usuário;
![image](https://github.com/user-attachments/assets/5ef7ef0c-eae5-421a-803b-b8ba81da3d3e)

09) se usuário confirmar commit;
![image](https://github.com/user-attachments/assets/79a516b9-8fe9-48c6-b78d-ee05babbdef0)

10) se usuário cancelar rollback;
![image](https://github.com/user-attachments/assets/aae2eb89-a44e-4359-b8f3-dd45b3c8d66f)

11) Se dados estão diferente então;
![image](https://github.com/user-attachments/assets/a20c1c40-aa04-4433-9f9f-f699b3204fc8)

12) informa usuário que o registro já foi alterado;
![image](https://github.com/user-attachments/assets/a20c1c40-aa04-4433-9f9f-f699b3204fc8)

## Conclusão 
#### Este projeto envolve a criação de um banco de dados com a tabela clientes, contendo campos essenciais como idcliente (chave primária) e limite (do tipo numeric(15,2)). Foi desenvolvido um sistema para gerenciar clientes, permitindo buscar e listar registros, selecionar e alterar dados de clientes com validações para evitar conflitos ou alterações concorrentes.

#### O sistema utiliza transações para garantir a integridade dos dados. Antes de qualquer alteração, os dados atuais são armazenados em variáveis, e uma validação é feita comparando os dados no banco com as informações exibidas. Caso não haja divergências, o UPDATE é realizado e o usuário confirma o COMMIT ou cancela para executar um ROLLBACK. Em situações de conflito ou erro, o sistema notifica o usuário, garantindo que nenhuma alteração seja aplicada sem segurança. Essa abordagem combina gerenciamento eficiente e proteção dos dados, integrando banco de dados e programação com confiabilidade.

</div>

<br />

# Informações do Projeto


### 📂 Estrutura do Projeto

- **Frontend:** Desenvolvido com Windows Forms para interface gráfica.
- **Backend:** Lógica de negócios e transações utilizando PostgreSQL.


### Como Usar 

1. **Baixar o Executável**
   - Clone o repositório e compile no Visual Studio.

2. **Configurar Banco de Dados**
   - Certifique-se de que o PostgreSQL está instalado e rodando.
   - Crie o banco de dados:
     ```sql
     CREATE DATABASE clientes_db;
     ```
   - Altere a lihha de conexão com o Postgres com suas credenciais:
     ```csharp
     private readonly string connectionString = "Host=localhost;Port=5432;Username=postgres;Password=postgres;Database=clientes_db";
     ```
   - Crie a tabela `clientes`:
     ```sql
     CREATE TABLE clientes (
         idcliente INT PRIMARY KEY,
         nome_cliente VARCHAR(100) NOT NULL,
         limite_credito DECIMAL(10, 2) NOT NULL
     );
     ```

3. **Executar a Aplicação**
   - Abra o arquivo `ClienteApp.exe` seguindo o caminho `ClienteApp\code\ClienteApp\ClienteApp\bin\Debug`.
   - Insira os dados no formulário e use os botões para realizar as operações.

### Desenvolvedores do projeto

<table>
  <tr>
    <td style="text-align: center;">
      <a href="#">
        <img src="https://avatars.githubusercontent.com/u/125320205?v=4" width="150px;" alt="Murillo Daigder"/>
        <br>
        <sub><b>Murillo Daigder</b></sub>
      </a>
    </td>
    <td style="text-align: center;">
      <a href="#">
        <img src="https://avatars.githubusercontent.com/u/125220696?v=4" width="150px;" alt="Murilo Cavazzana"/>
        <br>
        <sub><b>Murilo Cavazzana</b></sub>
      </a>
    </td>
  </tr>
</table>




<br>


# 💸 App Desktop p/ Controle de Gastos Mensal 
App desktop desenvolvido com o framework Electron para o front-end que consome uma API de ASP.NET e persiste informações em um Banco de Dados SQL Server. O sistema possui o objetivo de garantir ao usuário cadastrado um controle sobre suas despesas mensais. Ao realizar o cadastro, o usuário deve informar sua receita mensal e, ao adicionar suas dívidas no sistema, o aplicativo as exibirá juntamente com cards informando o quanto o usuário deve pagar até o quinto dia útil do próximo mês (próximo pagamento) e o quanto ele pode gastar para fins pessoais de forma a não entrar no vermelho. Cada despesa deve ser registrada com descrição, valor e data máxima para ser paga. Assim, caso a data máxima não esteja no intervalo entre o quinto dia útil do mês atual e do seguinte, ela não entrará no cálculo dos cards, visto que é uma preocupação para o mês posterior.




## 🌐 Stack Utilizada

**Front-end:** HTML - CSS - Bootstrap - JavaScript - Electron

**Back-end:** C# - API de ASP.NET - Entity Framework Core   

**Banco de Dados:** SQL Server


## 🧠 Conhecimentos Utlizados/Adquiridos

- Consumo de API através de requests pela biblioteca Axios de JavaScript
- Modais, Tabelas e Forms em Bootstrap
- CORS (Cross-Origin Resource Sharing)
- Modelagem Domain Driven Design
- Princípios do SOLID 
- AutoMapper e Injeção de Dependência
- Retornos adequados de status HTTP
- Early Returns 
- Migrações pelo Entity Framework Core
- Cardinalidade e Interação de Tabelas através de Foreign Key
- DTOs (Data Transfer Object)
- Métodos Static para Fabricação de Objetos

## 📥 Instalação e Uso 

- É necessário ter o .NET 7.0 instalado ➡️ https://dotnet.microsoft.com/pt-br/download/dotnet/7.0
- É necessário ter o Node instalado ➡️ https://nodejs.org/en/download/current
- É necessário o uso de SQL Server para o banco de dados https://www.microsoft.com/pt-br/sql-server/sql-server-downloads
- Recomendo o uso do Visual Studio Code para rodar a aplicação


Clone o projeto

```bash
  git clone https://github.com/vini-fumagalli/app-desktop-controle-gastos.git
```

Vá até o diretório do projeto

```bash
  cd app-desktop-controle-gastos
```

Clone os submódulos do back-end e front-end do projeto 

```bash
  git submodule init
  git submodule update

```

Crie a variável de ambiente `DB_CONNECTION_GASTOS`

```
Data Source=localhost/SQLEXPRESS;Initial Catalog=DB_ControleGastos;Trusted_Connection=True;TrustServerCertificate=true;
```

Navegue até a pasta src do back-end e aplique as migrações para o Banco de Dados

```bash
  cd back-end-controle-gastos/src
  dotnet ef migrations add FirstMigration
  dotnet ef database update 
```

Inicie a aplicação

`pressione (F5)`

Navegue até a pasta do front-end, instale o Electron e inicie a aplicação

```bash
  cd front-end-controle-gastos
  npm install electron --save-dev
  npm start
```


    
## 🙋 Autor

- Vinícius Fumagalli
- Estagiário de back-end com .NET
- Cursando 5º período de Ciência da Computação


## 🔗 Meus Links
[![portfolio](https://img.shields.io/badge/portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://github.com/vini-fumagalli)

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/vin%C3%ADcius-fumagalli-b59313250/)

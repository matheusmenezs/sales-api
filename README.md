# Sales API

<img src="https://img-c.udemycdn.com/course/240x135/3669874_1417_4.jpg">

### Introduction:
Backend application developed in the course [API Restful with Nodejs](https://www.udemy.com/course/api-restful-de-vendas/) available on [Udemy](https://www.udemy.com/), for sales management with features for creating product registration, customer registration, purchase orders and a complete management of application users, with authentication via JWT Token, recovery password by email, profile update, avatar update, among other features.

The project was implemented during a learning incentive program at [PD Soluções](https://www.pdsolucoes.com.br/) (Evolution Moment).

### Technologies:

[<img align="center" alt="Nodejs" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original.svg" style="max-width: 100%;"/>](https://nodejs.org/en/) [<img align="center" alt="Ts" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/typescript/typescript-plain.svg" style="max-width: 100%;"/>](https://www.typescriptlang.org/) [<img align="center" alt="Ex" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/express/express-original.svg" style="max-width: 100%;"/>](https://expressjs.com/pt-br/) [<img align="center" alt="Do" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/docker/docker-original.svg" style="max-width: 100%;"/>](https://www.docker.com/) [<img align="center" alt="Ps" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/postgresql/postgresql-original.svg" style="max-width: 100%;"/>](https://www.postgresql.org/) [<img align="center" alt="To" height="30" width="60" src="https://github.com/typeorm/typeorm/raw/master/resources/logo_big.png" 
style="max-width: 100%;"/>](https://typeorm.io/)


### Run the Project:
1. Clone the repository, run in terminal: `git clone https://github.com/matheusmenezs/api-sales.git`

2. Run `yarn` in terminal to install packages

3. Setup postgres environment inside docker-compose.yml file, change the value of DB, USER, PASSWORD and PORT with your database credentials:

![config_docker](https://user-images.githubusercontent.com/64173311/188461751-a3a1fbae-4aa1-45ab-8489-51efe3b8a7c0.png)

4. Run in terminal: `docker-compose up -d` to initialize container.

5. Configure the database on a platform for PostgreSQL. Here is configuration in Dbeaver, using the same settings as the `.yml` file: 

![configure_dbeaver](https://user-images.githubusercontent.com/64173311/188461447-ba062fcd-4b65-418e-8e44-fbddb7ea3df4.PNG)

6. Run in terminal: `yarn typeorm migration:run -d ./src/shared/typeorm/datasource.ts` to execute migrations.

7. Create the `.env` file based on the `.env.example` and generate a secret

8. Extract zip archive and import json to Insomnia or in other program to test APIs: [Request Collection](https://github.com/matheusmenezs/api-sales/files/9490442/apisales_insomnia.zip)

9. Run in terminal: `yarn dev` to initialize project.

### Endpoints

| Name | Function |
|------|---------------|
|```POST``` /users||
|```PATCH``` /users/avatar||
|```GET``` /users||
|```POST``` /sessions||
|```UPDATE``` /profile||
|```GET``` /profile||
|```POST``` /password/forgot||
|```POST``` /password/reset||
|```POST``` /customers||
|```UPDATE``` /customers/id||
|```DELETE``` /customers/id||
|```GET``` /customers||
|```GET``` /customers/id||
|```POST``` /products||
|```UPDATE``` /products/id||
|```DELETE``` /products/id||
|```GET``` /products||
|```GET``` /products/id||
|```POST``` /orders||
|```DELETE``` /orders/id||
|```GET``` /orders/id||


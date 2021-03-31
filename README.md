<h1 align="center">
:computer: Utilizando o Cypress E2E para testar um Blog em Angular
</h1>

<h1 align="center">
<img alt="logo Digital Innovation One" src="https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcS1OXUFeAAKnL7l6wXc7IfvC9r9edDlMnmzO_bJV4O5aoH_7PmvNaGAiKAmu1x5WxpOFDPbQkCmJpgtchs-zQNvwQ&usqp=CAU&ec=45702847" width="400px">
</h1>

<p align="center">
    <a href="https://www.linkedin.com/in/dev-full-stack/">
        <img alt="Made by Armando Costa" src="https://img.shields.io/badge/made%20by-Armando Costa-%23fc8406">
    </a>
</p>

---

### ⚔ Desafio

Desafio feito no Bootcamp da Digital Innovation One.

Esse projeto tem o desafio de construir um teste E2E com Cypress para um Blog em Angular.

O blog utilizado foi o angular-realworld-example-app.

---


<p align="justify">
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Projeto para teste: Angular Real World Example App
  <pre>git clone https://github.com/gothinkster/angular-realworld-example-app</pre>
  <pre>cd angular-realworld-example-app</pre>
  <pre>npm install</pre>
  <pre>npm run start
http://localhost:4200/</pre><br>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Aqui temos um aplicativo Angular contendo exemplos "reais" (CRUD, autenticação, etc) de acordo com a especificação para exemplos RealWord.<br>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Vamos adicionar o Cypress!
</p>

<hr>

<h3 align="center"> 
  Instalação
</h3>

<p align="justify">
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Abra outro terminal. Na pasta/angular-realworld-example-app/ execute:
  <pre>npm install cypress --save-dev</pre>
  <pre>npx cypress -v</pre>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Caso tenha problemas com Proxy ou Firewall, baixe o <a href="https://download.cypress.io/desktop">binário</a> e configure a variável de ambiente antes de instalar:
  <br><br>
  <pre>set CYPRESS_INSTALL_BINARY=C:\cypress.zip</pre>
  <pre>npm install cypress --save-dev --verbose</pre>
</p>

<hr>

<h3 align="center"> 
  Removendo o Protactor
</h3>

<p align="left">
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Remova o pacote:
  <pre>npm uninstall protactor --save-dev</pre>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Exclua a pasta /e2e/<br>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Do package.json, remova a linha: "e2e": "ng e2e"
</p>

<hr>

<h3 align="center"> 
  Cypress Test Runner
</h3>

<p align="left">
    <pre>npx cypress open</pre>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;O comando "cypress open", além de abrir o Cypress Test Runner, cria a pasta inicial /cypress/ e o arquivo de configuração /cypress.json<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;E já vem com /examples/ dos principais comandos Cypress.
</p>

<hr>

<h3 align="center"> 
  Primeiro Teste
</h3>

<p align="left">
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;cypress/integrations/exemplo.spec.js

```js
describe('Primeiro Teste', () => {
  it('Exemplos Cypress', () => {
    cy.visit('https://example.cypress.io')
    expect(true).to.equal(true)
  })
})
```

  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;describe and it come from Mocha<br>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;expect comes from Chai
</p>

<hr>

<h3 align="center"> 
  Como Rodar
</h3>

<p align="left">
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Para executar todos os testes da pasta /cypress/integration/:
  <pre>npx cypress run</pre>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Para executar somente um roteiro:
  <pre>npx cypress run --spec "cypress/integration/examples/example.spec.js"</pre>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Para abrir a interface do Cypress Test Runner:
  <pre>npx cypress open</pre>
</p>

<hr>

<h3 align="center">Configuração</h3>

<p align="left">
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;cypress.json
<pre>
{
  "baseUrl": "http://localhost:4200",
  "pageLoadTimeout": 30000,
  "defaultCommandTimeOut": 30000,
  "viewportHeight": 800,
  "viewportWidth": 500,
  "retries": 3
}
</pre>  
</p>

<hr>

## 🛠️ Tecnologias Utilizadas
- Cypress;
- Angular;
- JavaScript;

## ⏬ Como baixar o projeto
- <b style="color:red"> OBS: </b> É necessário ter o git instalado em sua máquina
- Executar o Seguinte comando no seu **Terminal** ou no **CMD**:

```bash
        git clone https://github.com/armandofc1/cypressE2EBlogAngular.git
```
### 📚 Referências

https://github.com/gothinkster/angular-realworld-example-app


## ⌨️ Autor

<img style="border-radius: 50%;" src="https://avatars.githubusercontent.com/u/236738?v=4" width="100px;" alt="Perfil-autor" ><br>
<sub><b>Armando Costa</b></sub>

##### Contatos
[![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/dev-full-stack/)](https://www.linkedin.com/in/dev-full-stack/)
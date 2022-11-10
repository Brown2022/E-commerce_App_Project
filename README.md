<img src="https://camo.githubusercontent.com/c54fb7a1dd4e25fdef1ac57a12ea8ed569a005fe5892815c14be660691b36f4b/687474703a2f2f696d6775722e636f6d2f743374654178692e706e67">
<h1>Deploy</h1>

<h2>Features</h2>

<h3>Products Features</h3>

| Feature          | Coded? | Description                            |
|------------------|--------|----------------------------------------|
| Add a Product    |        | Ability to Add a Product on the System |
| List Products    |        | Ability to List Products               |
| Edit a Product   |        | Ability to Edit a Product              |
| Delete a Product |        | Ability to Delete a Product            |
| Stock            |        | Ability to Update the Stock            |
| Stock History    |        | Ability to see the Stock History       |

<h3>Purchase Features</h3>

| Feature        | Coded?  | Description                             |
|----------------|---------|-----------------------------------------|
| Create a Cart  |         | Ability to Create a new Cart            |
| See Cart       |         | Ability to see the Cart and it items    |
| Remove a Cart  |         | Ability to Remove a Cart                |
| Add Item       |         | Ability to add a new Item on the Cart   |
| Remove an Item |         | Ability to Remove an Item from the Cart |
| Checkout       |         | Ability to Checkout                     |

<h1>eCommerce</h1>

eCommerce is an open source (test scenario) software made to create an easy and simple "Shop" API, where you have two micro services, one the Products API that stores and handles everything Related to Stock and Products. And the Purchase API where you can create orders (cart's) and checkout items.

The purpose of this repository is for education and test. But the code is being coded in a proper way.

<h2>Documentation</h2>

eCommerce has a full API documentation made with Swagger, you can check it by accessing this link.

If you have any Issue or bug you can submit a new Issue by accessing this link.

If you want to Contribute you can submit a Pull Request, remember to READ the Contributing Guide

<h2>Installation</h2>

eCommerce is splitted into two standalone RESTful API's, so you can run it on whatever port you want. Installing
eCommerce it's easy, the tutorial above will explain to you.
eCommerce uses Groovy 2.4 and Grails 3.2.11.

You can run eCommerce in different ways. You can go to the Releases Page and download the source code of the latest release, or a bundled .war or a standalone java application (.jar).

We recommend you see the presentation on this section.

<h3>Development</h3>

You can attach the .war in WebServers like <strong>Nginx</strong> using the Management Interface.

If you want run the standalone .jar just download it, and open your CMD/Terminal and write:

<h3>If you want RUN the Products API</h3>

```bash
java -jar ecommerce-products-api-XXX.jar 
```
<strong>OR</strong> 

```bash
./products-api/grailsw run-app
```
<h3>If you want RUN the Purchases API</h3>

```bash
java -jar ecommerce-purchase-api-XXX.jar 
```
<strong>OR</strong> 

```bash
./purchase-api/grailsw run-app
```
You also can build from the sources by running the Grails Console, go to one of the API's folder 

```bash
purchase-api 
```
or 

```bash
products-api
```
 and write on your CMD/Terminal the following:

```bash
grailsw assemble
```
If you want to run it in development scenario, you can also do it by building the sources. You have two manner to do it. You can Gradle or directly Grails. Both products-api and purchase-api comes with Groovy, Grails and Gradle standalone packages. So you can run it without installing them.


<h3>Option #1 - Run by Gradle</h3>

```bash
gradlew bootRun
```
<h3>Option #2 - Run by Grailsw</h3>

```bash 
grailsw run-app
```
<h2>Production</h2>
Production Environments are focused in being ready. That means, you just need execute the Jar File.

In the Production Environment all eCommerce API's are configured to work with <strong>MySQL</strong> in two databases; <strong>productsAPI</strong> and <strong>purchaseAPI</strong> and to work with a default <strong>username</strong> and <strong>password</strong> combination:

<h3>Note</h3>.: Remember importing each SQL files using MySQL for Production. You can find them inside 

```bash 
products-api/src/main/sql/
```
and

```bash
purchase-api/src/main/sql/
```

- <strong>Username</strong>: commerce
- <strong>Password</strong>: commerceapi
- <strong>Database</strong>: productsapi & purchaseapi
- <strong>Port</strong>: 3306

You can change those credentials in the application.yaml file. In production environments you need import the database schema before running the software. Both products-api and purchase-api DDL files are available on this folder.

<h2>Notes</h2>
<h3>Note</h3>.: By default products-api runs on port 8080 and purchase-api on port 8090.

<h3>Note</h3>.: In all Development and Test Scenarios, eCommerce uses H2 in-memory Database.

<h3>Note</h3>.: You can change your database credentials both for development/test and production scenarios in the app-config.yml available on each API sources root. Those configuration files can be used also externally, after building the .jar

<h3>Note</h3>.: You also can clean the sources and rebuild the sources by running 

```bash 
grailsw clean
```

<h1>Running Test Cases</h1>
You can easily run the Test Cases using the standalone Grails package built-in with both the API's. Go to the home folder of one of them (products-api or purchase-api). And write on your CMD/Terminal:

```bash
grailsw test-app
```

<h1>Credits</h1>
This development/educational scenario was coded and created by Stephen Brown under the <a href="https://github.com/ovflowd/ecommerce/blob/master/LICENSE">GNU GPL v3</a> License. The objective of this repository is for practical test of RESTful API's with Java + Groovy.

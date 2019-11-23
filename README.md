# Meat - Angular App Starter

## 1. Passos para começar

### Clonando o Repositório

`git clone https://github.com/cod3rcursos/meat-app-starter.git`

### Instalando as Dependências

`npm install`

### Inicializando o Servidor

`ng serve` ou `npm start`

## 2. Iniciando o Backend

### Instalando o json-server

`npm install -g json-server`

### Iniciando o serviço (raiz da aplicação)

`json-server db.json`

## Goodies

Expressões regulares usadas na validação de formulários

### Email Regex

`/^(([^<>()\[\]\.,;:\s@\"]+(\.[^<>()\[\]\.,;:\s@\"]+)*)|(\".+\"))@(([^<>()[\]\.,;:\s@\"]+\.)+[^<>()[\]\.,;:\s@\"]{2,})$/i`

### Number Regex

`/^[0-9]*$/`

## Upgrade para Angular 4.3

Dependências dos pacotes que devem ficar em package.json:

```
"dependencies": {
    "@angular/animations": "4.3.3",
    "@angular/common": "4.3.3",
    "@angular/compiler": "4.3.3",
    "@angular/core": "4.3.3",
    "@angular/forms": "4.3.3",
    "@angular/platform-browser": "4.3.3",
    "@angular/platform-browser-dynamic": "4.3.3",
    "@angular/router": "4.3.3",
    "admin-lte": "2.3.11",
    "core-js": "2.4.1",
    "font-awesome": "4.7.0",
    "intl": "1.2.5",
    "jquery": "3.1.1",
    "reflect-metadata": "0.1.10",
    "rxjs": "5.4.2",
    "ts-helpers": "1.1.2",
    "web-animations-js": "2.2.5",
    "zone.js": "0.8.16"
  },
  "devDependencies": {
    "@angular/cli": "1.2.7",
    "@angular/compiler-cli": "4.3.3",
    "@types/jasmine": "2.5.53",
    "@types/express": "4.0.37",
    "@types/jsonwebtoken": "7.2.3",
    "@types/node": "7.0.5",
    "codelyzer": "3.1.2",
    "jasmine-core": "2.7.0",
    "jasmine-spec-reporter": "4.1.1",
    "json-server": "0.12.0",
    "jsonwebtoken": "7.4.1",
    "karma": "1.7.0",
    "karma-chrome-launcher": "2.2.0",
    "karma-cli": "1.0.1",
    "karma-jasmine": "1.1.0",
    "karma-remap-istanbul": "0.6.0",
    "protractor": "5.1.2",
    "ts-node": "3.3.0",
    "tslint": "5.5.0",
    "typescript": "2.4.2",
    "webdriver-manager": "12.0.6"
  }
```

## Upgrade para Angular 6 (Apenas para a aulas finais)

Dependências dos pacotes que devem ficar em package.json:

```
"dependencies": {
    "@angular/animations": "6.0.0",
    "@angular/common": "6.0.0",
    "@angular/compiler": "6.0.0",
    "@angular/core": "6.0.0",
    "@angular/forms": "6.0.0",
    "@angular/platform-browser": "6.0.0",
    "@angular/platform-browser-dynamic": "6.0.0",
    "@angular/platform-server": "6.0.0",
    "@angular/router": "6.0.0",
    "admin-lte": "2.3.11",
    "core-js": "2.5.4",
    "font-awesome": "4.7.0",
    "intl": "1.2.5",
    "jquery": "3.1.1",
    "reflect-metadata": "0.1.10",
    "rxjs": "6.0.0",
    "rxjs-compat": "6.0.0",
    "ts-helpers": "1.1.2",
    "web-animations-js": "2.2.5",
    "zone.js": "0.8.26",
    "ajv": "6.0.0"
  },
  "devDependencies": {
    "@angular-devkit/build-angular": "0.6.0",
    "@angular/compiler-cli": "6.0.0",
    "@angular/cli": "6.0.0",
    "@angular/language-service": "6.0.0",
    "@types/jasmine": "2.8.6",
    "@types/jasminewd2": "2.0.3",
    "@types/node": "8.9.4",
    "@types/express": "4.0.37",
    "@types/jsonwebtoken": "7.2.3",
    "codelyzer": "4.2.1",
    "jasmine-core": "2.99.1",
    "jasmine-spec-reporter": "4.2.1",
    "karma": "1.7.1",
    "karma-chrome-launcher": "2.2.0",
    "karma-coverage-istanbul-reporter": "1.4.2",
    "karma-jasmine": "1.1.1",
    "karma-jasmine-html-reporter": "0.2.2",
    "protractor": "5.3.0",
    "ts-node": "5.0.1",
    "tslint": "5.9.1",
    "json-server": "0.12.0",
    "jsonwebtoken": "7.4.1",
    "typescript": "2.7.2",
    "webdriver-manager": "12.0.6"
  }
```

## Créditos

Todas as imagens usadas na aplicação são pertencentes a freepik.com

## Roteiro

### 1 Criação dos componentes Header e Home

* Como criar componentes

#### Passos

* `ng g c header --spec=false`
* `ng g c home --spec=false`

### 2 Rotas

* Como criar rotas
 * property binding "routerLink"
 * directiva routerLinkActive

#### Passos

* Criar o componente About
 * `ng g c about --spec=false`

* Criar o arquivo de rotas 
 * `app.roputes.ts`

* Importar o arquivo de rotas dentro do app.module.ts. `RouterModule.forRoot(ROUTES)`

* Adicionar a tag `<router-outlet></router-outlet>` no template principal "app.component.html" substituindo `<mt-home></mt-home>`

* Criar o link "Sobre" (apontando para a página about) no header utilizando property binding. Adicionar dentro da tag a `[routerLink]="['/about']"`
* Criar o link "Meat" (apontando para a página principal) no header utilizando property binding.  Adicionar dentro da tag a `[routerLink]="['/']"`
* Utilizar a directiva routerLinkActive no elemento que possui o link (ou elementos parents) para corrigir o efeito visual dos links ativos.

### 3 Criando os Componentes de Restaurantes

* Decorator @Input
* Interface
* *ngFor

#### Passos

* Criar o componente Restaurants
 * `ng g c restaurants --spec=false`

* Criar uma nova rota para restaurants

* Corrigir os links que levam à página de restaurants com `[routerLink]="['/restaurants']"`
 * home.components.html
 * header.component.html

* Criar o componente individual que representa um restaurant
 * `ng g c restaurants/restaurant --spec=false`

* Criar a interface Restaurant (app/restaurants/restaurant.model.ts) que representa os dados de um restaurante
<pre>
export interface Restaurant {
    id: string
    name: string
    category: string
    rating: number
    imagePath: string
    deliveryEstimate: string
}
</pre>

* Criar a propriedade restaurant do tipo da interface Restaurant dentro de RestaurantComponent com o decorator @Input

* Substituir no template restaurant.component.html os dados fixos pelas propriedades que foram criadas na interface

* Adicionar na classe RestaurantsComponent um array de restaurants com dados dummy. Copiar alguns dados do db.json
<pre>
  restaurants: Restaurant[]  = [
      {
        id: "bread-bakery",
        name: "Bread & Bakery",
        category: "Bakery",
        deliveryEstimate: "25m",
        rating: 4.9,
        imagePath: "assets/img/restaurants/breadbakery.png"
      },
      {
        id: "burger-house",
        name: "Burger House",
        category: "Hamburgers",
        deliveryEstimate: "100m",
        rating: 3.5,
        imagePath: "assets/img/restaurants/burgerhouse.png"
      }]
</pre>

* Alterar o template restaurants.component.html para utilizar o *ngFor para iterar sobre o array e incluir o template individual restaurant.component.html passando o objeto restaurant através de property binding. 
<pre>
  &lt;div *ngFor=&quot;let restaurant of restaurants&quot; class=&quot;col-sm-6 col-xs-12&quot;&gt;                        
    &lt;mt-restaurant [restaurant]=&quot;restaurant&quot; &gt;&lt;/mt-restaurant&gt;
  &lt;/div&gt;
</pre>

### Criando a Classe de Serviço para Restaurantes

* Serviços
* Injeção de dependências
* Método de ciclo de vida OnInit
* Provider

#### Passos

* Criar a classe de serviço RestaurantsService (app/restaurants/restaurants.service.ts)
* Mover a propriedade restaurants de RestaurantsComponent para dentro de RestaurantsService renomeando para rests (para evitar conflito de nomes)
* Criar o método restaurants() retornando o array de restaurantes "rests"
* Injetar a classe de serviço dentro do componente
* Inicializar a propriedade restaurants com a chamada do método restaurants() do serviço. Fazer a inicialização no método ngOnInit
<pre>
  ngOnInit() {
    this.restaurants = this.restaurantsService.restaurants()
  }
<pre>
* Adicionar o provide RestaurantsService no app.module.ts
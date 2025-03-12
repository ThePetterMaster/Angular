# Memoteca

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 14.0.3.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.

## Criando o projeto

`ng new memoteca`

## Criando componente rodape na pasta componentes

`ng g c componentes/rodape`

## Property Binding

Essa funcionalida permite que os dados no arquivo javascript sejam refletidos no html, porém não do html para o javascript.

```
  pensamento = {
    id: '1',
    conteudo: 'Aprendendo Angular',
    autoria: 'Dev',
    modelo: ''
  }
```

````
<input>
    //trecho de código omitido
    [value]="pensamento.conteudo"
</input>

<input>
    //trecho de código omitido
    [value]="pensamento.autoria"
</input>
````

````
<p class="autoria"><b>{{ pensamento.autoria }}</b></p>
````

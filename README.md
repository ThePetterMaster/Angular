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

## Event Binding

É uma técnica que permite que você escute e responda a ações do usuário, como cliques, movimentos do mouse, teclas pressionadas, entre outros.

````
<div class="acoes">
  <button (click)="criarPensamento()" class="botao">Salvar</button>
  <button (click)="cancelar()" class="botao">Cancelar</button>
</div>
````

````
criarPensamento() {
  alert("Novo pensamento criado!")
}
````

## Event Binding

Essa funcionalida permite que os dados no arquivo javascript sejam refletidos no html e do html para o javascript.

````
<input
  //Trecho de código omitido
  [(ngModel)]="pensamento.modelo"
>
````

## Diretivas
Diretivas no Angular são instruções que você pode aplicar aos elementos do DOM para modificar seu comportamento ou aparência12. Elas são categorizadas em três tipos principais:

Diretivas de Atributo: Alteram a aparência ou comportamento dos elementos do DOM. Exemplos incluem NgClass e NgStyle12.
Diretivas Estruturais: Modificam a estrutura do DOM, adicionando ou removendo elementos. Exemplos incluem NgIf, NgFor e NgSwitch12.
Componentes: São diretivas com templates, que definem como o conteúdo será exibido12.

### ngFor
````
    <div class="mural">
        <div *ngFor="let pensamento of listaPensamentos">
            <app-pensamento></app-pensamento>
        </div>
    </div>
````

````
listaPensamentos = [];
````
### ngIf

````
<p *ngIf="isVisible">Este parágrafo só aparece se isVisible for verdadeiro.</p>
````

### Componentes

````
    <div class="mural" *ngIf="listaPensamentos.length > 0, else semPensamentos">
        <div *ngFor="let pensamento of listaPensamentos">
        <app-pensamento [pensamento]="pensamento"></app-pensamento>
        </div>
    </div>
````
Mostra esse componente caso listaPensamentos for menor ou igual a zero
````
<ng-template #semPensamentos>
//Algum código
</ng-template>
````

### ngClass

````
<div class="pensamento {{ pensamento.modelo }} ff-roboto-mono" [ngClass]="larguraPensamento()">
````

## Comunicação entre componentes

Filho
````
    @Input() pensamento = {
````
Pai
````
    <div class="mural">
        <div *ngFor="let pensamento of listaPensamentos">
            <app-pensamento [pensamento]="pensamento"></app-pensamento>
        </div>
    </div>
````


## Rotas

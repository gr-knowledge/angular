# angular

**Instalação**
```properties
npm i | install -g @angular/cli
```

**Novo Projeto**
```properties
ng n meu-projeto --routing
```

**Novos Módulos**
```properties
ng g m shared
```

```properties
ng g m shared/layout
```

**Novos Componentes**
```properties
ng g c shared/layout/header
```

```properties
ng n c shared/layout/footer
```

```properties
ng g c shared/layout/navigation
```

```properties
ng g c shared/layout/main
```

> **Nota:** Não esquecer ```exports: []``` quando necessário.

**Definir componente *main* como default em todas as rotas.**  
```javascript
// app-routing.module.ts

const routes: Routes = [
  {
    path: '',
    component: MainComponent
  },
];
```

**O arquivo *app.component.ts* pode ser opcionalmente substituído.**  
```javascript
// app-component.ts

@Component({
  selector: 'app-root',
  template: '<router-outlet></router-outlet>',
})
```

**Adicionando [Angular Material](https://material.angular.io/guide/getting-started)**
```properties
ng add @angular/material
```





**Estrutura básica de arquivos**
```
my-project
├── dist
├── node_modules
├── src
|   ├── app
|   │   ├── core
|   |   |   ├── guards
|   |   |   ├── services
|   |   |   └── sore
|   │   ├── features
|   |   │   ├── cadastros
|   |   │   ├── financeiro
|   |   │   ├── estoque
|   |   │   ├── relatorios
|   |   │   └── dashboard
|   │   └── shared
|   |       ├── calendar
|   |       ├── chat
|   |       ├── graphs
|   |       ├── calendar
|   |       ├── layout
|   |       │   ├── footer
|   |       │   ├── header
|   |       │   ├── navigation
|   |       |   └── layout.module.ts
|   |       ├── ui
|   |       │   ├── datatable
|   |       │   ├── gallery
|   |       │   ├── jquery-ui
|   |       │   ├── tree-view
|   |       |   └── ui.module.ts
|   |       └── shared.module.ts
|   ├── assets
|   │   └── fonts
|   │   └── img
|   │   └── sound
|   ├── environments
|   │   ├── environments.prod.ts
|   │   └── environments.ts
|   ├── index.html
|   └── styles.css
└── package.json
```

<details>
  <summary>Frutas</summary>
  - Laranja  
  - Abacaxi  
</details>





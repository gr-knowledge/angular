# angular

**Instalação**
```properties
npm install -g @angular/cli (ultima versão)
npm install -g @angular/cli@7.11.4
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

```properties
ng g m shared/layout/header
```

```properties
ng g m shared/layout/navigation
```

```properties
ng g m shared/layout/app-layouts
```

```properties
ng g m shared/layout/ribbon
```

**Novos Componentes**

***angular.json*** (Desativar criação automática de *.spec)
```properties
"schematics": {
  "@schematics/angular:component": {
    "skipTests": true
  }
},
```

```properties
ng g c shared/layout/header
```

```properties
ng g c shared/layout/footer
```

```properties
ng g c shared/layout/navigation
```

```properties
ng g c shared/layout/ribbon
```

```properties
ng g c shared/layout/app-layouts/main-layout
```

```properties
ng g c shared/layout/app-layouts/empty-layout
```

```properties
ng g c shared/layout/app-layouts/auth-layout
```
> **Nota:** Não esquecer ```exports: []``` quando necessário.

**Definir componente *main* como default para todas as rotas.**  
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

```properties
ng g m shared/layout/ui
```

```properties
ng g m shared/layout/ui/material
```

```properties
ng g c shared/layout/ui/material/mat-tree
```

```properties
ng g c shared/layout/ui/material/mat-slider
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
|   │   ├── fonts
|   │   ├── img
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





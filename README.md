# angular

### Instalação
```properties
npm i | install -g @angular/cli
```

### Comandos
| Comando | Descrição | Dica |
|--|--|--| 
|ng n \| new my-project | Novo projeto |
|ng n \| new my-project | Novo projeto| "--routing --style scss" Adiciona rotas e estilo |
|ng serve | Emulada servidor web | "-o" Abre browser automaticamente |
|ng g \| generate c \| component my-comp | 
|ng set -g defaults.styleExt=scss | Altera estilo do projeto |


### Estrutura básica de arquivos
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





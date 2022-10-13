https://www.youtube.com/watch?v=zoytvenOLmE
https://www.youtube.com/watch?v=2F-uFCjS7Ys

https://github.com/angular/components/tree/main/src/material/schematics/ng-generate/address-form


- Instalação global
    npm install -g @angular-devkit/schematics-cli
    
- Criar schematics
   schematics blank --name=my-schematics
   
- Adicionar uma ação ao schematic criado (index.ts)
   tree.create(_options.name || 'hello', 'world');
   
- Executar build (dentro da pasta do schematic)
    npm run build
    
- Criar projeto Angular
    ng new my-project
    
- Linkar projeto com schematics (dentro da pasta do projeto)
    CD my-project
    npm link ../my-schematics
    
- Executar schematic
    ng g my-schematics:my-schematics
    ng g my-schematics:my-schematics --name=teste
    

## Definindo a Collection padrão
Estender a collection do Angular para não precisar passar o nome da collection em "ng g ..."

// collection.json
```TS
{
  "$schema": "../node_modules/@angular-devkit/schematics/collection-schema.json",
  "extends": ["@schematics/angular"],
  "schematics": {
    "my-schematics": {
      "description": "A custom module generator.",
      "factory": "./my-schematics/index#mySchematics",
      "schema": "./my-schematics/schema.json"
    }
  }
}
```

// my-project/angular.json
´´´TS
"cli": {
  "defaultCollection": "my-schematics"
}
```


# Sobrepor conteúdo de arquivo existente
// index.ts
```ts
export function someFeature(_options: any): Rule {
  return (tree: Tree, _context: SchematicContext) => {
    const content: Buffer | null = tree.read(_options.name);
    let strContent: string = '';
    if(content) strContent = content.toString();

    const appendIndex = strContent.indexOf('</ul>');
    const content2Append = '  <li><a href="/contact">contact</a></li> \n';
    const updatedContent = strContent.slice(0, appendIndex) + content2Append + strContent.slice(appendIndex);

    tree.overwrite(_options.name, updatedContent);
    return tree;
  };
}
`` 

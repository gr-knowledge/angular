https://www.youtube.com/watch?v=e6gaqdFEdIY&t=118s

https://www.c-sharpcorner.com/article/project-setup-with-mono-repo-angular-architecture/

https://angular.io/cli/new

> Cria nova base com monorepo
```propeties
ng new workspace-client --createApplication=false --newProjectRoot=apps
```

> Gera novo app
```propeties
ng g app examples --prefix=app --routing
```

```propeties
ng g library header --prefix=sa
```

//package.json
"build:libs": "ng build header-lib"

> Executar projeto
```propeties
ng serve example
```
```propeties
npm start example
```



> Build
```propeties
ng build --prod
```
```propeties
ng build --apps example --prod
```
```propeties
ng build my-lib
```
```propeties
ng build my-lib --watch
```
```propeties
ng build my-lib --prod
```

> Build das libs
```propeties
npm run build:libs
```


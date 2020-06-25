https://www.youtube.com/watch?v=e6gaqdFEdIY&t=118s

https://www.c-sharpcorner.com/article/project-setup-with-mono-repo-angular-architecture/

https://angular.io/cli/new

> Cria nova base com monorepo
```propeties
ng new monorepo-client --createApplication=false --newProjectRoot=apps
```

> Gera novo app
```propeties
ng g app examples --prefix=app
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



> Build das libs
```propeties
npm run build:libs
```


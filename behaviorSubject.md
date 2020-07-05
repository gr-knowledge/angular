# BehaviorSubject

> teste.service.ts
```ts
import { BehaviorSubject, Observable } from 'rxjs';

public navigation: BehaviorSubject<any> = new BehaviorSubject(null); // valor default
public navigation$: Observable<any> = this.navigation.asObservable();

changeNavigation(value) {
   this.navigation.next(value);
}
```

> teste.component.ts
```ts
public navigationSub: any;
public navigation$ = this.navigationService.navigation$;

constructor(public navigationService: NavigationService) {}

ngOnInit() {
  this.navigationSub = this.navigation$.subscribe( result => console.log(result) );
  this.navigationService.changeNavigation('Teste');
}

ngOnDestroy() {
   this.navigationSub.unsubscribe();
}
```

> test.html
```html
<ul *ngIf="navigation$ | async as navigation">
```

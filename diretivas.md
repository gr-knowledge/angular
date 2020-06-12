# Diretivas

### ngModel (FormsModule)
Para esta diretiva funcionar é preciso fazer o import.
```javascript
import { FormsModule } from '@angular/forms';
```

#### Import
```html
<input type="text" [(ngModel)]="task">
<input type="button" value="Adicionar" (click)="add()">
<ul>
   <li *ngFor="let item of tasks">{{item}}</li>
</ul>
```


### ngFor
```html
<ul>
   <li *ngFor="let item of tasks">{{item}}</li>
</ul>
```


### ngIf
```html
<h1 *ngIf="minhaVariavel">Concluído!</h1>
```

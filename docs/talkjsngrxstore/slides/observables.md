##  Observables

Store is an Observable injected into a component

### Class definition
```
export class SomeComponent {
    players: Observable<String[]>;
    constructor(private store:Store<AppState>) {
        this.players = store.select(state => state.players);
    }
}
```

### Unravel subscription
```
<ol>
    <li *ngFor="player of players | async"> {{player}} </li>
</ol>
```
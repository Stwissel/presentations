##  Actions

- type and payload
- defined in constructor

```
import { Action } from '@ngrx/store';
import { Member } from './member-model';

export const ADD = '[Member] Add';

export class AddMember implements Action {
    readonly type = ADD;
    constructor(public payload: Member) { }
}
```


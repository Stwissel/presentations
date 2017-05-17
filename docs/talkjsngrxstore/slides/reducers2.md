##  Reducers
Pure function, returns **NEW** state
```
import { ActionReducer, Action } from '@ngrx/store';

export const playerReducer: ActionReducer<AppState> =
(state:AppState = initialState, action: Action) => {
    switch (action.type) {
        case ADD_PLAYER:
            // Code goes here
        case REMOVE_PLAYER:
            // Code goes here
        default:
            return state;
    }
}
```

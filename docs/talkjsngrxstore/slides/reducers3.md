### Initial State
```
export interface AppState {
    players: string[];
    jackpot: number;
    currentPlayer: number;
}

export const initialState: AppState = {
    players: [],
    jackpot: 0,
    currentPlayer: 0
}
```

### Add/Remove Player
```
// Add Player
return Object.assign({},state,
            {players : [...state.players, action.payload.newPlayer]}
            );
 
// Remove player          
return Object.assign({}, state,
    {players : players.filter(p => (p != action.payload.deletePlayer))}
);
```

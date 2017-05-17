## Reducers

### Reducer Interface
```
export interface Reducer<T> {
  (state: T, action: Action): T;
}
```

### Action Interface
```
export interface Action {
  type: string;
  payload?: any;
}
```

## Pure functions!!!
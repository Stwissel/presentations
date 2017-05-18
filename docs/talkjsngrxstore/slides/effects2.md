# @effect()
```
@Injectable()
export class MemberEffects {
  @Effect()
  search$: Observable<Action> = this.actions$.ofType(MemberActions.SEARCH)
    .map((action: SearchActions.Search) => action.payload)
    .switchMap(email => this.searchService.searchMember(email))
    .map(results => new MemberActions.SearchSuccess(results));
    
  constructor(
    private actions$: Actions,
    private searchService: MemberSearchService
  ) {}
}
```
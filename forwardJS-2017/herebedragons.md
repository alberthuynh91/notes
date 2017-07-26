# Here Be Dragons: Refactoring Terrifying Legacy Code with Jest

## Tooling
- ESLint
- Flow/Typescript
- Prettier
- Codemodes

## How to do it?
1) Major rewrite - extremely risky
2) Halt in roadmap progress
3) Gradual rewrite
  - 1 module at a time
  - Test changes
  - Deploy
  - Rinse and repeat

## Problems w/ manual testing
- Repetitive
- Scope

## Jest
- Good for testing untested legacy code
- Good to use snapshot for testing api calls that return structured data. Will show you the diffs.
- Unit testing framework from Facebook now used for React
- Make frontend testing more enjoyable
- Helps us add tests quickly, and tests are very fast
- Built in code coverage, helps with missing edge cases
- Snapchat testing - useful for making sure UI doesn't change unexpectedly.
- Jest includes full mocking library
- Could also be helpful in testing redux state and test the entire state.

## Problems w/ screenshot testing
- Finicky
- Visual diffs, fails very frequently causing developers to easily ignore
- Slow, since they run in a browser. Boot up is also slow. Difficult for large numbers of tests

## Snapshots get around this problem, but how?
- Takes in data, spits out DOM
- Takes a snapshot on initial run. Saves the snapshot file. When code changes it can change the snapshot and if there is a diff it’ll tell you. If the changes are correct you push up the new snapshot file to CI/git
- Snapshots show regressions.
- Snapshots can be used for more than just UI

## How do we handle side effects?
`jest.spyOn()`

## Downsides to snapshot testing?
- Snapshots can’t catch everything and are low level. These are still unit tests after all.
- Won’t catch CSS regressions.
- Best to be combined with other types of testing

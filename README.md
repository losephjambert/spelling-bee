# svelte Spelling Bee

## Structure

### Game State

- Rank
- Score
- Words Found
- Game Data
  - Master Word List
  - Rank Benchmarks

### Components

- `<TitleBar/>`
- `<MenuBar/>`
  - `<HelpButton/>`
  - `<SaveButton/>`
- `<GameContainer/>`
  - `<WordInputDisplay/>`
  - `<Hive/>`
    - `<Cell/>`
  - `<InputControlBar/>`
    - `<DeleteButton/>`
    - `<RotateLettersButton/>`
    - `<SubmitWordButton/>`
- `<GameStatusContainer/>`
  - `<ProgressBar/>`
    - `<TotalScore/>`
    - `<Rank/>`
    - `<ProgressDisplay/>`
    - `<ProgressDetail/>`
      - `<ProgressDisplay/>`
  - `<WordListContainer/>`
    - `<Title/>`
    - `<FoundWordsList/>`
      - `<FoundWord/>`

### Functionality

- Save game state
- Click/tap a hive cell to add that letter to the word
- Click/tap delete button to remove most recently added letter from word
- Click/tap button to randomly rotate letters in hive
- Click/tap submit button to submit current word
- Click/tap help button to see game instructions
- Click/tap save button to save current progress
- Click/tap Progress Bar to see progress detail

## Get started

Install the dependencies...

```bash
cd svelte-app
npm install
```

...then start [Rollup](https://rollupjs.org):

```bash
npm run dev
```

Navigate to [localhost:5000](http://localhost:5000). You should see your app running. Edit a component file in `src`, save it, and reload the page to see your changes.

By default, the server will only respond to requests from localhost. To allow connections from other computers, edit the `sirv` commands in package.json to include the option `--host 0.0.0.0`.

## Deploying to the web

### With [now](https://zeit.co/now)

Install `now` if you haven't already:

```bash
npm install -g now
```

Then, from within your project folder:

```bash
cd public
now
```

As an alternative, use the [Now desktop client](https://zeit.co/download) and simply drag the unzipped project folder to the taskbar icon.

### With [surge](https://surge.sh/)

Install `surge` if you haven't already:

```bash
npm install -g surge
```

Then, from within your project folder:

```bash
npm run build
surge public
```

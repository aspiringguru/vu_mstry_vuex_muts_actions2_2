# real-world-vue

## Following along?

We encourage you to follow the course on Vue Mastery, and code along with us. This course has tags representing the start and finish of each level, just in case you get stuck. Here's the start and ending code of each lesson, if you'd like to download them.

| Lesson                               |                                                                                                              |                                                                                                               |
| ------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------- |
| 2 - Vue CLI                          | n/a                                                                                                          | [Finished Code](https://github.com/Code-Pop/real-world-vue/releases/tag/lesson2-cli-finish)                   |
| 3 - Optimizing your IDE              | [Starting Code](https://github.com/Code-Pop/real-world-vue/releases/tag/lesson3-editor-start)                | [Finished Code](https://github.com/Code-Pop/real-world-vue/releases/tag/lesson3-editor-finish)                |
| 4 - Vue Router Basics                | [Starting Code](https://github.com/Code-Pop/real-world-vue/releases/tag/lesson4-routing-start)               | [Finished Code](https://github.com/Code-Pop/real-world-vue/releases/tag/lesson4-routing-finish)               |
| 5 - Dynamic Routes & History Mode    | [Starting Code](https://github.com/Code-Pop/real-world-vue/releases/tag/lesson5-dynamic-routing-start)       | [Finished Code](https://github.com/Code-Pop/real-world-vue/releases/tag/lesson5-dynamic-routing-finish)       |
| 6 - Single File Components           | [Starting Code](https://github.com/Code-Pop/real-world-vue/releases/tag/lesson6-sfc-start)                   | [Finished Code](https://github.com/Code-Pop/real-world-vue/releases/tag/lesson6-sfc-finish)                   |
| 7 - Global Components                | [Starting Code](https://github.com/Code-Pop/real-world-vue/releases/tag/lesson7-global-start)                | [Finished Code](https://github.com/Code-Pop/real-world-vue/releases/tag/lesson7-global-finish)                |
| 8 - Slots                            | [Starting Code](https://github.com/Code-Pop/real-world-vue/releases/tag/lesson8-slots-start)                 | [Finished Code](https://github.com/Code-Pop/real-world-vue/releases/tag/lesson8-slots-finish)                 |
| 9 - API Calls with Axios             | [Starting Code](https://github.com/Code-Pop/real-world-vue/releases/tag/lesson9-axios-start)                 | [Finished Code](https://github.com/Code-Pop/real-world-vue/releases/tag/lesson9-axios-finish)                 |
| 11 - Vuex State & Getters            | [Starting Code](https://github.com/Code-Pop/real-world-vue/releases/tag/lesson11-vuex-start)                 | [Finished Code](https://github.com/Code-Pop/real-world-vue/releases/tag/lesson11-vuex-finish)                 |
| 12 - Vuex Mutations & Actions Part 1 | [Starting Code](https://github.com/Code-Pop/real-world-vue/releases/tag/lesson12-mutations%26actions1-start) | [Finished Code](https://github.com/Code-Pop/real-world-vue/releases/tag/lesson12-mutations%26actions1-finish) |

## Project setup

```
npm install
```

### Compiles and hot-reloads for development

```
npm run serve
```

### Compiles and minifies for production

```
npm run build
```

### Lints and fixes files

```
npm run lint
```

### setup & startup notes

```
Notes: had to reinstall npm from scratch.
npm --version
python --version

git config --get remote.origin.url
git remote show origin

npm install -g json-server
npm install --save vuejs-datepicker


npm list -g --depth=0

json-server --watch db.json
npm install
yarn serve


https://github.com/typicode/json-server#paginate

download new larger db.json and save as db_new.json
then restart json-server

json-server --watch db_new.json

notes for bonus question

1. save eventsTotal to your state
    - initialise eventsTotal to zero in store.js.
    -
2. create a mutation to set it
    - add mutations method SET_EVENTS_TOTAL to store.js
        (sets state.eventsTotal to eventsTotal)
3. call the mutation from fetchEvents
    - store.js fetchEvents commit SET_EVENTS_TOTAL

4. update EventList.vue
    - add computed method hasNextPage()to EventList.vue

------------------------
12:30 > update EventShow to use vuex
1. store the event data in state.
    edit store.js, add event dictionary.
2. create a mutation.
    create SET_EVENT to store the event in state
3. create action to call api and mutation.
    create action fetchEvent, reuse code that was in EventShow.vue export default created
4. cleanup and connecting above
    in EventShow.vue, replace import EventService with import mapState from vuex
    delete export default data
    in EventShow.vue, delete data,
    in EventShow.vue created, call action fetchEvent with id.
    in EventShow.vue created, use mapState helper to access event data.


```

# Vue

Basic manual and hands-on.

<sub><sup>Time: 60 ~ mins</sup></sub>

## Context

-   Understand what VueJS is
-   Overview of Core features
-   Framework Comparison
-   Continue learning

## Prerequisites

-   Basic knowledge of HTML, CSS, and JavaScript
-   IDE/Text Editor
-   NodeJS (to manage packages)
-   Basic local server (already included in Vue-CLI)

## Business Solutions View

-   Around 60% of E-Commernce transaction are made in Desktop and Mobile
-   40% of the rest of the traffic are done through Native Apps(kiosk)
-   E-Commerce transactions increase year after year

#### Vue and Commerce

-   Apps can be built quickly by relatively inexperienced teams compared to its rivals
-   Fast performance and small package (ideal for mobile)
-   Tool set to build a view layer for your application

#### Gems of Vue

-   Faster app means more potential users
-   Faster way to update the DOM virtually
-   Faster development, organized view layer

#### Work with Vue

-   Works for new or existing applications
-   Features are familiar to React and Angular developers
-   Fast, easy to understand and maintain
-   Popular on Github, around 200k stars

#### Who can Vue

-   Small teams, apps, and individual prototypes
-   Large teams, apps, and collaborative
-   External support or fix in a problematic area

## Fundamentals

The Progressive Framework

-   JavaScript library that executes before your own code that gives context to the code you write.
-   Render engine that takes data model and components to output HTML or the view.
-   A tool for collaboration, separation of and into smaller components.

### Component API

Components can be created

-   Uses two Styles.
-   In a format called SFC(Single-File Component), a single file that includes component's template, logic and styles.

#### Styles

-   `Options API` defines component instance/logic using options and properties. (OOP/Stateful)
-   `Composition API` defines component logic using API functions. (Functional/Stateless)

<details>
  <summary>Example - Options API</summary>

```js
// Object instance
export default {
	// Function to return data
	data() {
		return {
			isShown: false,
		}
	},
	// Object contains methods
	methods: {
		showElement() {
			this.isShown = true
		},
	},
	// Lifecycle method when component is mounted to DOM
	mounted() {
		console.log(`Component is mounted and ready.`)
	},
}
```

</details>

<details>
  <summary>Example - Composition API</summary>

```js
// Import Reactive Functions
import { ref, onMounted } from "vue"

// Declare Reactive State
const isShown = false

// Mutate state and trigger changes
function showElement() {
	isShown = true
}

// Lifecycle hooks when component is mounted to DOM
onMounted(() => {
	console.log(`Component is mounted and ready.`)
})
```

</details>

> For this session, we will focus on the Options API which is more traditional.

### Vuex

-   A store is a state management pattern or library
-   Allows us to store our data, methods, getting and changing our data
-   Maintain components in large scale apps
-   Functional variables that has objects and methods

#### Core Concepts

-   `State` contains all your application level state and data
-   `Mutations` methods that changes data in our state
-   `Actions` commits mutations and calls asynchronous requests
-   `Getters` methods that get data from state, then change it before providing it to our components
-   `Modules` allows us to divide the store into modules

<details>
  <summary>Example - Create Store Instance</summary>

```js
// Import Vuex
import { createStore } from "vuex"

// Create store instance
const store = createStore({
	// State to declare object and data
	state() {
		return {
			isShown: false,
		}
	},
	// Mutations to commit store changes in data
	mutations: {
		show(state) {
			state.isShown = true
		},
	},
})
```

</details>

<details>
  <summary>Example - Call Mutation</summary>

```js
methods: {
// Create function to commit mutation
  showElement() {
    this.$store.commit('show')
    console.log(this.$store.state.isShown)
  }
}
```

</details>

## Hands-On

To create a build-tool-enabled Vue project, we make use of its scaffolding tool:

`npm init vue@latest`

At first, it will ask to install `create-vue@latest` package. `y` to proceed.

This is a project setup tool that prompts a number of optional features:

    √ Project name: ... MyVueProject
    √ Package name: ... myvueproject
    √ Add TypeScript? ... No / Yes
    √ Add JSX Support? ... No / Yes
    √ Add Vue Router for Single Page Application development? ... No / Yes
    √ Add Pinia for state management? ... No / Yes
    √ Add Vitest for Unit Testing? ... No / Yes
    √ Add Cypress for both Unit and End-to-End testing? ... No / Yes
    √ Add ESLint for code quality? ... No / Yes

    Scaffolding project in ./MyVueProject...
    Done.

For our session, we only select `Yes` for the `Vue Router`.

Then, follow instructions from the CLI.

> Optional packages can manually be added later.

#### See Files and Structure

-   node_modules
-   src
    -   assets
    -   components
    -   router
    -   views
    -   App.vue
    -   main.js
-   index.html
-   package.json

#### Exercise

Let's make use of the project that we have created.

1.  Create a new page called 'Photo'
2.  Add a stock image or use the Vue logo
3.  Create a button to display it

## Continue with Vue

-   [Options and Composition API](https://vuejs.org/guide/introduction.html) - Comparison of APIs
-   [Event Handling](https://vuejs.org/guide/essentials/event-handling.html#event-handling) - Event Handling Directive
-   [Style Guide](https://v2.vuejs.org/v2/style-guide) - Best practices
-   [API Reference](https://vuejs.org/api/) - Reference to components
-   [Vuex](https://vuex.vuejs.org/) - State management feature
-   [Vue.js devtools](https://chrome.google.com/webstore/detail/vuejs-devtools/nhdogjmejiglipccpnnnanhbledajbpd?hl=en) - State management tool in Chrome Extension
-   [Official Documentation](https://vuejs.org/guide/) - Ultimate reference from getting started to advanced
-   [NuxtJS](https://nuxtjs.org/) - For Production project builds
-   [Vue: The Best Alternative To React And Angular](https://www.valuecoders.com/blog/technology-and-apps/vue-js-comparison-angular-react/#Angular_vs_Vue_vs_react_Comparison_Table)
-   [When should you Use Nuxt.js instead of Vue.js?](https://javascript.plainenglish.io/when-should-you-use-nuxt-js-instead-of-vue-js-8558a33b91c6)

<sub><sup>Session Shared By Adrian Del Rosario</sup></sub>

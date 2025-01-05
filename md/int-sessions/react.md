# React

![react-logo](images/react-logo.png)

**1. What is ReactJS?**

`React` is a front-end and open-source JavaScript library which is useful in developing user interfaces specifically for applications with a single page. It is helpful in building complex and reusable user interface(UI) components of mobile and web applications as it follows the component-based approach.

**2. What are the features of React?**

- Follows a One-direction data binding and flow
- Use of VirtualDOM instead of RealDOM
- Component-based architecture
- Supports server-side rendering

##### Differences between the `RealDOM` and `VirtualDOM`

| RealDOM                                                                               | VirtualDOM                                                                                                         |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------ |
| Real DOM takes all the HTML elements and wraps them in a tree-like structured object. | It has the same features as the Real DOM object but it can’t write and display things on the screen like Real DOM. |
| Updates slow.                                                                         | Updates faster.                                                                                                    |
| Manipulation is slow.                                                                 | Manipulation is faster because nothing gets drawn onscreen.                                                        |
| Memory wastage is more.                                                               | No memory wastage.                                                                                                 |
| It represents the document as nodes and objects.                                      | A virtual DOM object is like a lightweight copy of Real DOM.                                                       |

**3. What are the advantages of using React?**

- It ensures faster rendering.
- It is SEO-friendly.
- React combines the speed of JavaScript and uses a new approach to render web pages to make them dynamic and responsive.
- It can be used for the development of both web and mobile apps.
- JSX makes components/blocks code readable.
- It is easy to integrate with other frameworks, such as Angular and Meteor.
- Backed by a large community and supported by Facebook

**4. What is limitation of React?**

- React is not a full-blown framework as it is only a library.
- The components of React are numerous and will take time to fully grasp the benefits of all.
- It might be difficult for beginner programmers to understand React.
- Coding might become complex as it will make use of inline templating and JSX.

**5. Does React use HTML?**

No, It uses `JSX`, which is similar to HTML.

JSX stands for JavaScript XML. It allows us to write HTML inside JavaScript and place them in the DOM without using functions like appendChild() or createElement().

<details>
  <summary>Compilation</summary>

Web browsers cannot read JSX directly because JSX is not a regular JavaScript (JS) object and web browsers are built for reading only regular JS objects. To read a JSX file, the file must be converted into a regular JavaScript object.

</details>

**6. What are the two types of React component?**

##### Functional component (stateless)

- It calculates the internal state of the components.
- It accepts properties(props) in function and return HTML (JSX).
- It does not contain the data related to the past, current, and possible future state changes.
- There is no render method used in the Stateless component.
- Do not have the authority to change the state.

##### Classal component (stateful)

- Stateful Component stores information about the component’s state change in memory.
- It has complex UI Logic.
- It contains the data related to past, current, and possible future changes in state.
- It must have the render() method returning HTML.
- Have the authority to change the state.

**7. What are Props in React ?**

`Props` mean properties, which is a way of passing data from parent to child. We can say that props are just a communication channel between components. It is always moving from parent to child component.

**8. What is React State ?**

It is an object which decides how a specific component renders and how it behaves. The state stores the information which can be changed over the lifetime of a React component.

**9. What are the lifecycle methods of React?**

- `constructor()`: This method will be called when the component is initiated before anything has been done. It helps to set up the initial state and initial values.
- `getDerivedStateFromProps()`: This method will be called just before element(s) rendering in the DOM. It helps to set up the state object depending on the initial props. The getDerivedStateFromProps() method will have a state as an argument and it returns an object that made changes to the state. This will be the first method to be called on an updating of a component.
- `render()`: This method will output or re-render the HTML to the DOM with new changes. The render() method is an essential method and will be called always while the remaining methods are optional and will be called only if they are defined.
- `componentDidMount()`: This method will be called after the rendering of the component. Using this method, you can run statements that need the component to be already kept in the DOM.
- `shouldComponentUpdate()`: The Boolean value will be returned by this method which will specify whether React should proceed further with the rendering or not. The default value for this method will be True.
- `getSnapshotBeforeUpdate()`: This method will provide access for the props as well as for the state before the update. It is possible to check the previously present value before the update, even after the update.
- `componentDidUpdate()`: This method will be called after the component has been updated in the DOM.
- `componentWillUnmount()`: This method will be called when the component removal from the DOM is about to happen.

**10. What are hooks in React?**

React hooks allows you to use State, and other React features without writing a class.

Built-in Hooks: The built-in Hooks are divided into 2 parts

##### Basic Hooks

- `useState()`: This functional component is used to set and retrieve the state.
- `useEffect()`: It enables for performing the side effects in the functional components.
- `useContext()`: It is used for creating common data that is to be accessed by the components hierarchy without having to pass the props down to each level.

##### Additional Hooks:

- `useReducer()`: It is used when there is a complex state logic that is having several sub-values or when the upcoming state is dependent on the previous state. It will also enable you to optimize component performance that will trigger deeper updates as it is permitted to pass the dispatch down instead of callbacks.
- `useMemo()`: This will be used for recomputing the memoized value when there is a change in one of the dependencies. This optimization will help for avoiding expensive calculations on each render.
- `useCallback()`: This is useful while passing callbacks into the optimized child components and depends on the equality of reference for the prevention of unneeded renders.
- `useImperativeHandle()`: It will enable modifying the instance that will be passed with the ref object.
- `useDebugValue()`: It is used for displaying a label for custom hooks in React DevTools.
- `useRef()`: It will permit creating a reference to the DOM element directly within the functional component.
- `useLayoutEffect()`: It is used for the reading layout from the DOM and re-rendering synchronously.

##### Custom Hooks

A custom Hook is basically a function of JavaScript. The Custom Hook working is similar to a regular function. The “use” at the beginning of the Custom Hook Name is required for React to understand that this is a custom Hook and also it will describe that this specific function follows the rules of Hooks. Moreover, developing custom Hooks will enable you for extracting component logic from within reusable functions.

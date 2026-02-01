### Meaning

In programming, a **hook** is a **special function or mechanism that “hooks into” a system, framework, or lifecycle** to perform custom behavior at specific points.

- Commonly used in **React** and other frameworks.
- Can be thought of as a **way to “tap into” existing behavior**.

---

## 1. Hooks in React

React Hooks allow **functional components** to use features that were previously only in class components, such as **state and lifecycle methods**.

### Common Hooks:

|Hook|Purpose|Example|
|---|---|---|
|`useState`|Manage component state|`const [count, setCount] = useState(0)`|
|`useEffect`|Run side effects (e.g., fetch data, subscribe)|`useEffect(() => { fetchData() }, [])`|
|`useRef`|Store a mutable value without causing re-render|`const inputRef = useRef()`|
|`useContext`|Access React context|`const theme = useContext(ThemeContext)`|

### Key Features

- Let you **reuse logic** across components
- Simplify **state and side-effect management**
- Avoid **complex class components**

---

## 2. Hooks in Other Contexts

- **Event hooks / system hooks**:
    
    - Allow you to run custom code when a **specific event occurs** in a program.        
    - Example: Logging, monitoring, intercepting keyboard/mouse events.
    
- **Webhooks** (related term):
    
    - Not React-related, but similar idea.    
    - A **callback URL** triggered by an event in a service.
    - Example: GitHub triggers a webhook when code is pushed.

---

## 3. Memory Hook

- Think: **“Hook = attach your function to something that happens”**
- In React: “Hook into state or lifecycle”
- In general: “Hook into an event”

---

## 4. One-Line Exam Answer

> A hook is a function or mechanism that allows you to attach custom behavior to a system, event, or component lifecycle, such as React Hooks for state and side effects in functional components.
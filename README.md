# React.js Interview Questions And Answers

Most targeted up-to-date React.JS interview questions and answers list

# Table of Contents

1. [How do you create a functional component in React?](#1-how-do-you-create-a-functional-component-in-react)
2. [How do you create a class component in React?](#2-how-do-you-create-a-class-component-in-react)
3. [How do you pass props to a component in React?](#3-how-do-you-pass-props-to-a-component-in-react)
4. [How do you handle events in React?](#4-how-do-you-handle-events-in-react)
5. [How do you manage state in React?](#5-how-do-you-manage-state-in-react)
6. [How do you perform conditional rendering in React?](#6-how-do-you-perform-conditional-rendering-in-react)
7. [How do you map through an array and render components dynamically in React?](#7-how-do-you-map-through-an-array-and-render-components-dynamically-in-react)
8. [How do you make an HTTP request in React?](#8-how-do-you-make-an-http-request-in-react)
9. [How do you handle form input in React?](#9-how-do-you-handle-form-input-in-react)
10. [How do you style components in React?](#10-how-do-you-style-components-in-react)
11. [How do you use React Router for navigation in React?](#11-how-do-you-use-react-router-for-navigation-in-react)
12. [How do you handle form submission in React?](#12-how-do-you-handle-form-submission-in-react)
13. [How do you implement component lifecycle methods in React?](#13-how-do-you-implement-component-lifecycle-methods-in-react)
- [Whats more?](#whats-more)
- [Contributing](#contributing)
- [License](#license)

## 1. How do you create a functional component in React?

Answer:

```jsx
import React from 'react';

function MyComponent() {
  return <div>Hello, World!</div>;
}

export default MyComponent;
```

## 2. How do you create a class component in React?

Answer:

```jsx
import React, { Component } from 'react';

class MyComponent extends Component {
  render() {
    return <div>Hello, World!</div>;
  }
}

export default MyComponent;
```

## 3. How do you pass props to a component in React?

Answer:

```jsx
import React from 'react';

function MyComponent(props) {
  return <div>Hello, {props.name}!</div>;
}

export default MyComponent;
```

## 4. How do you handle events in React?

Answer:

```jsx
import React from 'react';

function MyComponent() {
  const handleClick = () => {
    console.log('Button clicked!');
  };

  return <button onClick={handleClick}>Click Me</button>;
}

export default MyComponent;
```

## 5. How do you manage state in React?

Answer:

```jsx
import React, { useState } from 'react';

function MyComponent() {
  const [count, setCount] = useState(0);

  const increment = () => {
    setCount(count + 1);
  };

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={increment}>Increment</button>
    </div>
  );
}

export default MyComponent;
```

## 6. How do you perform conditional rendering in React?

Answer:

```jsx
import React from 'react';

function MyComponent({ isLoggedIn }) {
  return isLoggedIn ? <p>Welcome, User!</p> : <p>Please log in.</p>;
}

export default MyComponent;
```

## 7. How do you map through an array and render components dynamically in React?

Answer:

```jsx
import React from 'react';

function MyComponent({ items }) {
  return (
    <ul>
      {items.map((item) => (
        <li key={item.id}>{item.name}</li>
      ))}
    </ul>
  );
}

export default MyComponent;
```

## 8. How do you make an HTTP request in React?

Answer:

```jsx
import React, { useEffect, useState } from 'react';

function MyComponent() {
  const [data, setData] = useState([]);

  useEffect(() => {
    fetch('https://api.example.com/data')
      .then((response) => response.json())
      .then((data) => setData(data));
  }, []);

  return <div>{data}</div>;
}

export default MyComponent;
```

## 9. How do you handle form input in React?

Answer:

```jsx
import React, { useState } from 'react';

function MyComponent() {
  const [inputValue, setInputValue] = useState('');

  const handleChange = (e) => {
    setInputValue(e.target.value);
  };

  return (
    <div>
      <input type="text" value={inputValue} onChange={handleChange} />
      <p>Input value: {inputValue}</p>
    </div>
  );
}

export default MyComponent;
```

## 10. How do you style components in React?

Answer:

```jsx
import React from 'react';

function MyComponent() {
  const myStyle = {
    color: 'blue',
    fontSize: '20px',
  };

  return <div style={myStyle}>Styled Component</div>;
}

export default MyComponent;
```

## 11. How do you use React Router for navigation in React?

Answer:

```jsx
import React from 'react';
import { BrowserRouter as Router, Route, Link } from 'react-router-dom';

function Home() {
  return <h1>Home Page</h1>;
}

function About() {
  return <h1>About Page</h1>;
}

function App() {
  return (
    <Router>
      <nav>
        <ul>
          <li>
            <Link to="/">Home</Link>
          </li>
          <li>
            <Link to="/about">About</Link>
          </li>
        </ul>
      </nav>

      <Route path="/" exact component={Home} />
      <Route path="/about" component={About} />
    </Router>
  );
}

export default App;
```

## 12. How do you handle form submission in React?

Answer:

```jsx
import React, { useState } from 'react';

function MyComponent() {
  const [formData, setFormData] = useState({ username: '', password: '' });

  const handleChange = (e) => {
    setFormData({ ...formData, [e.target.name]: e.target.value });
  };

  const handleSubmit = (e) => {
    e.preventDefault();
    console.log(formData);
  };

  return (
    <form onSubmit={handleSubmit}>
      <input
        type="text"
        name="username"
        value={formData.username}
        onChange={handleChange}
      />
      <input
        type="password"
        name="password"
        value={formData.password}
        onChange={handleChange}
      />
      <button type="submit">Submit</button>
    </form>
  );
}

export default MyComponent;
```

## 13. How do you implement component lifecycle methods in React?

Answer:

```jsx
import React, { Component } from 'react';

class MyComponent extends Component {
  componentDidMount() {
    console.log('Component mounted');
  }

  componentDidUpdate() {
    console.log('Component updated');
  }

  componentWillUnmount() {
    console.log('Component unmounted');
  }

  render() {
    return <div>Component Lifecycle Methods</div>;
  }
}

export default MyComponent;
```

## What's more?
<a href="https://interviewplus.ai/developers-and-programmers/react-js/questions">A comprehensive list of questions and answers</a>

## Contributing
We welcome contributions from our users to help make this resource as comprehensive and useful as possible. If you have been recently interviewed and encountered a question that is not currently covered on our website, feel free to suggest it as a new question. Your contributions will be added to our platform, and we will make sure to credit you for your contributions. We appreciate your help in making our platform a valuable tool for all job seekers.

## License
MIT License

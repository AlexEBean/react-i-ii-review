### Remember

Answer these on your own, then compare answers as a group

1.  What is React?
      A JS library that focuses on making UI elements and has a virtual DOM


2.  What is create-react-app?
      A tool for putting together a React app in one go

3.  What is Component Based Architecture?
      A way to break up a larger project into smaller pieces of code

4.  What is JSX?
      An extension of JS that's like a mix of HTML and JavaScript

5.  What is the virtual DOM?
      A memory representation of the DOM that keeps in sync with the actual DOM

6.  What is unidirectional (one-way) data flow?
      Data is passed from parent to children

### Understand

Discuss these questions in pairs if you have a 4-person group

7.  Summarize what happens when you run `create-react-app my-app`
    A folder is created called 'my-app'



8.  Summarize the steps for forking and cloning a repo with an existing React app. How does this process differ from the process of creating a new React app on your laptop?



9.  Explain what this code does:

```jsx
import React from "react";

const Mentor = props => (
  <div className="mentor-container">
    <h1 className={props.title === "Lead Mentor" ? "lead" : ""}>Tim Biles</h1>
    <ul>
      <li>Fort Worth, TX</li>
      <li>My email address is timbilestimbiles@gmail.com</li>
    </ul>
  </div>
);

export default Mentor;
```

10.  Explain how data is passed from a parent component to a child component.

    By using props

### Apply

Try these on your own, but work together if you start to get stuck.

11.  Use `create-react-app` to create a new React application called `student-directory`

12.  Use the code from `Mentor` above to create a new functional, stateless component called `User` with a list of friends. Hard code the list of friends, do not use state or props.

### Analyze, Evaluate, Create

Discuss these questions as a group

13. What are the benefits and drawbacks of using a tool like create-react-app?

14. Compare and contrast JSX with other templating options, such as those used in Angular or Vue

15. Compare and contrast one-way data flow with two-way data binding.

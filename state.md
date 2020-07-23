### Remember

Answer these on your own, then compare answers as a group

1.  What is state?
    An object (key value pairs) that is able to be accessed and updated

2.  Where do you set initial state?
      In the constructor of a class component right after we call super

3.  What method do you use to update state?
      setState

### Understand

Discuss this question in pairs if you have a 4-person group

4.  Explain what's happening in this component.

```jsx
import React, { Component } from "react";

class LeadMentor extends Component {
  constructor(props) {
    super(props);

    this.state = {
      questionsAnswered: 0
    };

    this.handleClick = this.handleClick.bind(this);
  }
  handleClick() {
    this.setState({ questionsAnswered: this.state.questionsAnswered + 1 });
  }
  render() {
    <div className="lead-mentor-container">
      <h1>Michael Scott</h1>
      <h3>{this.state.questionsAnswered}</h3>
      <h3>questions answered today</h3>
      <button onClick={this.handleClick}>Increase Answers</button>
    </div>;
  }
}
```

    Increment questions answered by one every time a button labeled "Increase Answers" is clicked

### Apply

Try these on your own, but work together if you start to get stuck.

5.  Create a `Student` component that keeps track of the number of questions the student has asked, with a button that adds 1 to the total when it's clicked
  ```jsx
    import React, { Component } from "react";

    class Student extends Component {
      constructor(props) {
        super(props);

        this.state = {
          questionsAnswered: 0
        };

        this.handleClick = this.handleClick.bind(this);
      }
      handleClick() {
        this.setState({ questionsAnswered: this.state.questionsAnswered + 1 });
      }
      render() {
        return (
          <div className="student-container">
            <h1>Student</h1>
            <h3>{this.state.questionsAnswered}</h3>
            <h3>questions answered today</h3>
            <button onClick={this.handleClick}>Increase Answers</button>
          </div>;
        )
      }
    }
  ```


6.  Now add a text input where the student can type in their questions with a button to add them to a list of questions that is displayed below the number of questions asked.




### Analyze, Evaluate, Create

Discuss these questions as a group

7.  Could your `Student` component be refactored into a functional component? Why or why not?
      No, because we need state.

8.  What are the pros and cons of using a class method for an event handler vs. using an arrow function inline?

      Pro: We would not have to bind our function
      Con: Depending on the amount or complexity of the codebase, using arrow functions could make things less readable at first glance

9.  The render() method is called every time a component's state is updated. For a text input, that means the render method is called for every keypress. Why isn't this bad for performance?
    Just because render runs doesn't mean the whole DOM is being rerendered (virtual Dom)
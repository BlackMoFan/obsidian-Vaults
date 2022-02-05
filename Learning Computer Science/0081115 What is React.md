Links:  [[008111 Create a Front-End App with React from Codecademy]]
# What is React?
---
As internet speeds increased and web browsers became more powerful, web applications grew more complicated and ambitious! It became necessary to develop more advanced tools for building and maintaining web applications.

#### Spaghetti Code

Writing JavaScript code that interacted directly with HTML became messy as applications were built and maintained over time. Complex JavaScript web applications were often called “spaghetti code” because they were structured in tangled and confusing ways that would quickly get out of hand.

#### Performance Problems

At the same time, performance became a problem for complex web applications. Using JavaScript to change HTML was fast enough when only a few changes were needed, but not when one click from a user could trigger many complex changes throughout the application!

#### React to the rescue!

In 2013, React came to the rescue! React is a JavaScript library for building user interfaces. React is an open-source tool that was initially developed by Facebook, but it is widely used in many web applications.

React solves the problem of messy spaghetti code by breaking the code into components. There is typically one component for each discrete feature of the site, and each of the components follows the same general structure. This means that the same code patterns will be enforced throughout the application, which will make the site more maintainable and readable as it is updated.

React also does a lot of clever calculations under-the-hood to make sure that updates in the browser are calculated as efficiently as possible, thus improving performance. You’ll learn much more about how React works later.

#### React and the job market

React is one of the frameworks currently in highest demand in the web development industry. [React developer salaries](https://www.indeed.com/salaries/Reactjs%20Developer-Salaries) often range from $90k-110k per year.

React is still new enough that it’s [hard for employers to find candidates](http://research.hackerrank.com/developer-skills/2018/) who understand this powerful framework.

Learning React will give you the skills you need to set yourself apart in the job market!

To do:
1. Skim through the code in **SearchBar.js**. As you might guess, this code describes the behavior of the Search Bar that you see in the preview on the right! This is a single React component.
	
	If you’re overwhelmed by this, don’t worry! This code will look very familiar to you by the end of this course.

File:
SearchBar.js
```
import React from 'react';

import './SearchBar.css';

class SearchBar extends React.Component {
  constructor(props) {
    super(props);

    this.state = {
      term: ''
    };

    this.handleTermChange = this.handleTermChange.bind(this);
    this.search = this.search.bind(this);
  }

  handleTermChange(event) {
    this.setState({term: event.target.value});
  }

  search() {
    this.props.onSearch(this.state.term);
  }

  render() {
    return (
      <div className="SearchBar">
        <input placeholder="Enter A Song Title" onChange={this.handleTermChange} />
        <a onClick={this.search}>SEARCH</a>
      </div>
    );
  }
}

export default SearchBar;
```
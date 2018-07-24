# react-typeform  [![Build Status](https://travis-ci.org/mohithg/react-typeform.svg?branch=master)](https://travis-ci.org/mohithg/react-typeform) [![GitHub version](https://badge.fury.io/gh/mohithg%2Freact-typeform.svg)](https://badge.fury.io/gh/mohithg%2Freact-typeform) [![npm version](https://badge.fury.io/js/react-typeform.svg)](https://badge.fury.io/js/react-typeform)

## Description
Renders each component at a time with a next button, and when all components are traversed then all components are shown at once for review with a submit button.

## Installation
```
npm install react-typeform --save
```

## Setup for typeform

### Component.jsx
```
<div>
  ...Your individual component here
</div>
```

## Properties

### children (Required)
The individual components to be shown one by one

### onSubmit
Function that executes when submit button is clicked

### submitBtnText
Text to be displayed for submit button
Default: Submit

### submitBtnClass
Classname for submit button

### nextBtnText
Text to be displayed for next button
Default: Next

### nextBtnClass
Classname for next button

### nextBtnOnClick
Function that executes when next button is clicked

### backBtnText
Text to be displayed for back button
Default: Back

### backBtnClass
Classname for back button

### backBtnOnClick
Function that executes when back button is clicked

### showReviewView
Boolean that sets whether to show a review view as the final step
Default: true

## Example

```
import React from 'react';
import Typeform from 'react-typeform';

class TypeFormComponent extends React.Component {

  submit() {
    // Call your submit function here
  }

  render() {
    return(
      {/** You can wrap this into your favourite form
        * But use the onSubmit function to call function that executes on click
        */}
      <TypeForm
        onSubmit={this.submit}
      >
        <Component1 />
        <Component2 />
        ...
      </TypeForm>
      );
  }
}

export default TypeFormComponent;

```

## License
MIT

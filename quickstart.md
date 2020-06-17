## Getting Started

Install the dependency. Please note, `styled-component` is a peer dependency

```sh
yarn add styled-wind@beta styled-components

// or

npm i styled-wind@beta styled-components
```

### Usage

An usual styled component:

```js
import styled from 'styled-component';

const StyledContainer = styled.div`
    background: red;
    margin-top: 10px;
    border: 1px solid {props => props.isError ? 'red' : 'green' } 
`
```

A styled-wind component:

```js
import styled from 'styled-wind';

const StyledContainer = styled.div`
    background: red;
    margin-top: 10px;
    # sets text blue
    .text-blue-600; 
    # sets text green for large and xl devices
    .lg:text-green-600; 
    # sets bg yellow on hover
    .hover:bg-yellow; 
    # sets padding top value
    .pt-10; 
    border: 1px solid {props => props.isError ? 'red' : 'green' } 
`

// Alternate syntax
const StyledContainer = styled.div`
    background: red;
    margin-top: 10px;
    # sets text blue
    swind: text-blue-600; 
    # sets text green for large and xl devices
    swind-lg: text-green-600; 
    # sets bg yellow on hover
    swind-hover: bg-yellow; 
    # sets padding top value
    swind: pt-10; 
    border: 1px solid {props => props.isError ? 'red' : 'green' } 
`
```

As simple as that. You are good to go. 
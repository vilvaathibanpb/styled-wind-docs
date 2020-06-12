## Getting Started

Install the dependency. Please note, `styled-component` is a peer dependency

```
yarn add styled-wind

// or

npm i styled-wind
```

### Usage

An usual styled component:

```sh
import styled from 'styled-component';

const StyledContainer = styled.div`
    background: red;
    margin-top: 10px;
    border: 1px solid {props => props.isError ? 'red' : 'green' } 

`
```

A styled-wind component:

```sh
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
```

As simple as that. You are good to go. 
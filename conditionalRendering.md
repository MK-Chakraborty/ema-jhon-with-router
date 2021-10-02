# Conditional Rendering

Render something on UI based on any condition.

## Ways to do conditional rendering

There are several ways to do conditional rendering. Let's explore 
some ways. 


### Element Variable

using if else we can do conditional rendering.

`const user = (props) => {
   const {familiar} = props;

    let greeting;
    if(familiar) {
        greeting = <h5>Hello my friend</h5>
    }
    else {
        greeting= <h5>Do I know You?<h5>
    }

    return (
        <div>
            <h1>{greeting}</h1>
        </div>
    )
}`


### Ternary Operator

We can do conditional rendering via ternary operation also.

`const user = (props) => {
   const {familiar} = props;

    return (
        <div>
            {
                familiar ? <h4>Hello my friend</h4> : <h4> Do I know you?<h4>
            }
        </div>
    )
}`

another example

`const user = (props) => {
   const {familiar} = props;

    return (
        <div>
            {
                familiar ? <div>
                    <h4>Hello my friend</h4>
                </div>
                :<div>
                    <h4>Do I know you?</h4>
                </div>
            }
        </div>
    )
}`


### Logical AND, Logical OR

Logical AND: 

`const user = (props) => {
   const {familiar} = props;

    return (
        <div>
            {
                familiar && <h4>Hello my friend</h4>
            }
        </div>
    )
}`

Logical OR: 

`const user = (props) => {
   const {familiar} = props;

    return (
        <div>
            {
                familiar || <Compnent></Compnent>
            }
        </div>
    )
}`
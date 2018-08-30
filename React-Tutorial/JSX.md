JSX
===

JSX is a syntactic sugar that makes it easier to understand how components are put together. Consider this expression:

```html
<Main>
    <LeftColumn width={1}>
        <h1>JSX Example</h1>
    </LeftColumn>
    <RightColumn width={2}>
        <p>Some content</p>
    </RightColumn>
</Main>
```

JSX must be compiled (as it is not valid JavaScript syntax). Usually the compilation is provided by Babel (for JavaScript) or Typescript. The above example compiles to:

```javascript
React.createElement(
    Main,
    null,
    React.createElement(
        LeftColumn,
        { width: 1 },
        React.createElement(
            "h1",
            null,
            "JSX Example"
        )
    ),
    React.createElement(
        RightColumn,
        { width: 2 },
        React.createElement(
            "p",
            null,
            "Some content"
        )
    )
);
```

Which do you think is easier to read and understand?

[Try it out yourself](https://babeljs.io/repl/#?babili=false&browsers=&build=&builtIns=false&spec=false&loose=false&code_lz=DwWQhglgdgfAUAAiQ4AZApgMwC4GED2ANgK4C2siyVwAFgIwwBSAygBoICiAHmKQA6F0wAPT141YRhwES5ccmAAlCAHMaeImQpVqfGM3yl0CAMb4o2dBZF7KSEcrUbZFEeGjwgA&debug=false&forceAllTransforms=false&shippedProposals=false&circleciRepo=&evaluate=false&fileSize=false&timeTravel=false&sourceType=module&lineWrap=true&presets=react&prettier=false&targets=&version=6.26.0&envVersion=)


# Web Snippets

### Box Model

box size includes content/padding/border/margin

    box-sizing: border-box;

### Responsive

    <meta name="viewport" content="width=device-width, initial-scale=1">

and may also want to set viewport

### Centering

There are many strategies.

See this [video](https://youtu.be/SpxHVrpfGgU?t=1m40s) for a snippet of one approach for centering vertically and horizontally:

    body {
      display: flex;
      min-height: 100vh;
      ...
      align-items: center:
      justify-content: center;
      flex-direction: column;
    }

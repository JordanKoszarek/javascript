# Unearth Mithril.js guide

*A mostly reasonable approach to Mithril and JSX*

## Table of Contents

  1. [Basic Rules](#basic-rules)
  1. [Models](#models)


## Basic Rules
  - Split code by view and model.
  - Only one model per file.
  - Multiple components are allowed in a single file. (Don't abuse this)

## Models
  [2.1](models) General

  The model is tied to a view or views. The Model is used to execute logic and hold state for the view it is tied to.

  **[⬆ back to top](#table-of-contents)**
  [2.2](models) Use classes.
  > Why? It is easier to refactor the model to support multiple instances if the model is already a class.
```javascript
    // bad
    const model = {
        init() {
            // do init
        }
    }

    export default model;

    // good
    class Model {
        init() {

        }
    }

    export default new Model();

    // good
    class Model {
        init() {

        }
    }

    export default Model;
```

**[⬆ back to top](#table-of-contents)**

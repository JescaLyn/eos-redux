# EOS Redux

![eos.png](https://s10.postimg.org/7hfcpvwpl/eos.png)


## How to install:

Install EOS as a global npm package

```
npm install -g eos-redux
```

You're all set!

## How to use:

All commands are run through the following syntax:
```
eos <command> [args]
```

### Start

```
eos start [name]
```
Alternate syntax:
```
eos s [name]
```

Creates a Redux app with the name specified.

The following file tree is generated:

```
[name]/
  + frontend/
    + actions/
    + components/
      root.jsx
    + middleware/
      master_middleware.js
    + reducers/
      root_reducer.js
    + store/
      store.js
    + util/
    index.jsx
  webpack.config.js
```
Along with the creation of the file structure comes the installation of all dependencies needed.

All the first level dependencies included are:

* babel-loader
* babel-core
* babel-preset-es2015
* babel-preset-react
* lodash
* react-redux
* react
* react-dom
* react-router
* redux
* webpack

For ease of use we have also included a default webpack.config.js file that is structured correctly for this framework.  

### Generate

```
eos generate [action] [name]
```
Alternate syntax:
```
eos g [action] [name]
```

Generates an individual element or a full cycle.

It is important how you format your name if it is more than one word. Currently it is required that you enter the name in one of the following formats:

```
sampleName
SampleName
```

While this command will generate pre-filled files it will not place the generated middleware or reducer into the master_middleware.js or root_reducer.js respectively. This must be done manually.

#### Available Actions

##### cycle

```
eos generate cycle [name]
```

Generates a full redux cycle for a given name. The files that will be generated are as follows:

- frontend/components/[name]/
- frontend/components/[name]/[name].jsx
- frontend/components/[name]/[name]\_container.jsx
- frontend/actions/[name]\_actions.js
- frontend/middleware/[name]\_middleware.js
- frontend/reducer/[name]\_reducer.js
- frontend/util/[name]\_api_util.js

##### component

```
eos generate component [name]
```

Generates file structure for a single component:

```
components/
  + [name]/
    [name]_container.js
    [name].jsx
```

##### actions

```
eos generate [actions] [name]
```

Generates actions file.

```
actions/
  [name]_actions.js
```

##### middleware

```
eos generate middleware [name]
```

Generates middleware file.

```
middleware/
  [name]_middleware.js
```

##### reducer

```
eos generate reducer [name]
```

Generates reducer file.

```
reducer/
  [name]_reducer.js
```

##### api_util

```
eos generate api_util [name]
```

Generates api_util file.

```
util/
  [name]_api_util.js
```



---
Developed by [Alex Mattson](http://www.alexmattson.com)

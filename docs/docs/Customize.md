# Change Styleguides output

This page is meant to show how to customize a styleguide.<br/>It will get you to transform any part of the styleguide. <br/>A good example of a finished customized styleguide is linked [in the Examples section](/Examples#customised).

We will go through each step of the process so that you can completely change the way the styleguide is rendered.

## Prerequisites

- [Install vue-styleguidist]() and check it runs.
- Block the version of your dependency to vue-styleguidist.
  - There is no guarantee your customizations will work on every minor update.
- Learn the basics of ReactJs.
  - vue-styleguidist is rendering the styleguide using [react-styleguidist](https://react-styleguidist.js.org/). All the visible part is made in ReactJs.
  - Since we will re-write React components, the more you know the more you will be able to do.
- Install the React Dev Tools extension in your development browser.
  - [For Chrome](https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi?hl=en)
  - [For Firefox](https://addons.mozilla.org/en-US/firefox/addon/react-devtools/)
  - [For Edge](https://microsoftedge.microsoft.com/addons/detail/react-developer-tools/gpphkfbcpidddadnkolkpfckpihlkkil)

## Step by step

### Identify the component

We want to change a part of the styleguide. We first have to identify what its name is in styleguidist.

In this step, we will identify which components we need to replace to achieve our transformation.

First, start off your styleguide

```sh
npm run styleguide
```

Open your styleguide in your dev browser.<br/> Then, from your browsers dev tools open the react dev tools.<br/> You should get something like this

![React Dev Tools](/assets/captures/ReactDevTools.png)

All components seen on the right are replacable by your own.

If we want to replace the Section Header with something more complicated, this is how we find it.

### Locate the original components source code

Vue Styleguidist is made on top of React-Styleguidist. To avoid duplication, a lot of the components from react-styleguidist are used from react-styleguidist.

#### First, look in vue-styleguidist

To find the source code of the component we want to customize, we look first in [vue-styleguidist](https://github.com/vue-styleguidist/vue-styleguidist/tree/dev/packages/vue-styleguidist/src/client/rsg-components). This is where webpack will look for it first as well.

> **NOTE:** There is no `...Renderer` or `Styled()` components in this list. If the component we want to customize end with `renderer`, we will look for the components without the suffix. The idea is the same with `Styled()`, though styled components can often be ignored.

#### Second, see if it is react-styleguidist

If we do not find the component in vue-styleguidist it means the system uses a component from react-styleguidist. We look inside [this directory](https://github.com/styleguidist/react-styleguidist/tree/master/src/client/rsg-components) for the component.

### Copy the code

### Set up babel

### Register Components

## A concrete example

# vue-simple-tabs

Tabs component for vue.js

## Installation

NPM:

```bash
npm install --save vue-simple-tabs
```

Yarn:

```bash
yarn add vue-simple-tabs
```

## Usage

```html
<template>
  <tabs>
    <tab title="Tab 1" active="true">Tab 1 content</tab>
    <tab title="Tab 2">Tab 2 content</tab>
    <tab title="Tab 3">Tab 3 content</tab>
  </tabs>
</template>

<script>
  import { Tabs, Tab } from 'vue-simple-tabs';

  export default {
    components: { Tabs, Tab }
  };
</script>
```

## Events

You can add a handler for tab changed event.

Example:

```html
<template>
  <tabs @changed="tabChanged">
    <tab title="Tab 1" active="true">Tab 1</tab>
    <tab title="Tab 2">Tab 2</tab>
    <tab title="Tab 3">Tab 3</tab>
  </tabs>
</template>

<script>
  import { Tabs, Tab } from 'vue-simple-tabs';

  export default {
    components: { Tabs, Tab },
    methods: {
      tabChanged(tab) {
        // Do something
      }
    }
  };
</script>
```

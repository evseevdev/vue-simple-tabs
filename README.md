# vue-simple-tabs
Tabs component for vue.js

## Installation:

NPM:
```bash
npm install --save vue-simple-tabs
```
Yarn:
```bash
yarn add vue-simple-tabs
```

## Usage:

```html
<template>
  <tabs class="faq-section__tabs">
    <tab title="Tab 1" active="true">
      Tab 1 content
    </tab>
    <tab title="Tab 2">
      Tab 2 content
    </tab>
    <tab title="Tab 3">
      Tab 3 content
    </tab>
  </tabs>
</template>

<script>
import { Tabs, Tab } from 'vue-simple-tabs';

export default {
  components: { Tabs, Tab }
}
</script>
```
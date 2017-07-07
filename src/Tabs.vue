<template>
  <div>
    <ul>
      <li 
        v-for="(tab, index) in tabList" 
        :key="index" 
        :class="{'active': isActive(index)}" 
        @click="select(index)">
        {{ tab.title }}
      </li>
    </ul>
    <div class="tab-content">
      <slot></slot>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        tabList: [],
        activeTabIndex: 0
      }
    },

    mounted() {
      this.select(0);
      this.activeTabIndex = this.getInitialActiveTab();
    },

    methods: {

      isActive(index) {
        return this.activeTabIndex === index;
      },

      select(index) {
        this.activeTabIndex = index;
      },

      getInitialActiveTab() {
        return this.tabList.reduceRight((activeTabIndex, tab, index) => tab.active ? index : activeTabIndex);
      }

    }
  }
</script>
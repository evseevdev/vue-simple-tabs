<template>
  <div v-if="isActive" :class="{ 'disabled': isDisabled }">
    <slot></slot>
  </div>
</template>

<script>
  export default {
    props: {
      title: { 
        type: String, 
        required: true
      },
      active: { 
        type: [ Boolean, String ],
        default: false
      },
      disabled: {
        type: [ Boolean, String ],
        default: false
      }
    },

    data() {
      return {
        isActive: this.active,
        isDisabled: this.disabled
      }
    },

    created() {
      this.$parent.tabList.push(this);
    },

    computed: {
      index() {
        return this.$parent.tabList.indexOf(this);
      }
    },
    
    watch: {
      '$parent.activeTabIndex' (index) {
        this.isActive = this.index === index;
      },
      disabled() {
        this.isDisabled = this.disabled;
      }
    }
  }
</script>
<template>
  <component
    class="button"
    v-bind:is="elementType"
    :to="to"
  >
    <slot>Button</slot>
  </component>
</template>

<script lang="ts">
 export default {
    props: {
      to: {
        type: String,
      },
    },
    computed: {
      elementType() {
        // if (this.to) {
        //   return 'router-link';
        // }

        return 'button';
      },
    },
  };
</script>

<style scoped lang="scss">
  .button {
    display: inline-block;
    padding: $spacer-xs $spacer-xxs;
    box-sizing: border-box;
    text-decoration: none;
    font-family: $font-family-base;
    font-weight: $font-weight-bold;
    font-size: $font-size-base;
    text-align: center;
    transition: all 0.2s;
    color: $brand-primary;
    background-color: transparent;
    border: 2px solid $brand-primary;

    &:hover {
      color: $brand-secondary;
      border-color: $brand-primary;
      background-color: $brand-primary;
    }
  }
</style>

<!--filled, outlined, outlined-inversed-->


<template functional>
  <component
    :is="injections.components.SfButton"
    :class="[data.class, data.staticClass, 'sf-arrow']"
    :style="[data.style, data.staticStyle]"
    type="button"
    v-bind="data.attrs"
    v-on="listeners"
  >
    <slot>
      <component
        :is="injections.components.SfIcon"
        size="1.5rem"
        icon="arrow_left"
        aria-hidden="true"
        v-bind="data.attrs"
        :class="[data.class, data.staticClass, 'sf-arrow__icon']"
      />
    </slot>
  </component>
</template>
<script>
import SfButton from "../SfButton/SfButton.vue";
import SfIcon from "../SfIcon/SfIcon.vue";
export default {
  name: "SfArrow",
  inject: {
    components: {
      default: { SfButton, SfIcon },
    },
  },
};
</script>
<style lang="scss">
@import "./SfArrow.scss";
</style>

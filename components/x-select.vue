<template>
  <div>
    <v-select
      v-model="localValue"
      :items="items"
      :value="value"
      class="selectBoxField"
      append-icon="mdi-chevron-down"
      hide-details
      outlined
    >
      <template #selection="{ item }">
        <v-list-item-content>
          <v-list-item-title class="d-flex">
            <div class="iconBackground" :style="{ background: item.background }" >
              <x-icon :name="item.icon" />
            </div>
            <span class="white--text ml-3 mt-2">{{ item.label }}</span>
          </v-list-item-title>
        </v-list-item-content>
      </template>
    </v-select>
  </div>
</template>

<script>
export default {
  name: "x-select",
  data() {
    return {
      localValue: this.value,
    };
  },
  props: {
    items: { type: Array, default: () => [] },
    value: { type: String, default: undefined },
    height: { type: String, default: undefined },
  },
  watch: {
    localValue() {
      this.$emit("input", this.localValue);
      console.log("value changed : ", this.localValue);
    },
  },
};
</script>

<style lang="scss">
.selectBoxField .v-list-item__content .v-list-item__title {
  //@extend .body4-regular;
}

.iconBackground {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 32px;
  height: 32px;
  border-radius: 100px !important
}
</style>

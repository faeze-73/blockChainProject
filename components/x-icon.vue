<template>
  <span
    v-html="file"
    :width="width"
    :height="height"
    class="d-flex justify-center align-center"
  />
</template>

<script>
export default {
  name: "x-icon",
  props: {
    name: { type: String, default: "link" },
    alt: { type: String, default: "icon" },
    extension: { type: String, default: "svg" },
    fill: { type: String, default: undefined },
    stroke: { type: String, default: undefined },
    width: { type: String, default: undefined },
    height: { type: String, default: undefined },
  },
  data() {
    return {
      file: require(`~/assets/icons/${this.name}.${this.extension}?raw`),
    };
  },
};
</script>

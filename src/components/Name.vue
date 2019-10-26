<template>
  <h2 class="name">
    my name is
    <span id="animated-name">Kelly</span> Wu
    <div
      class="hover-zone"
      @mouseover="changeToYulong"
      @mouseleave="changeToKelly"
    />
  </h2>
</template>

<script>
import TypeIt from "typeit";

export default {
  // Guarantee Typed is removed before the component is destroyed.
  beforeDestroy() {
    if (this.t) this.t.destroy();
  },
  methods: {
    changeToYulong() {
      this.changeName("Yulong");
    },
    changeToKelly() {
      this.changeName("Kelly");
    },
    changeName(name) {
      if (this.t) this.t.destroy();
      this.t = new TypeIt("#animated-name", {
        speed: 250,
        startDelete: true,
        cursor: false
      })
        .type(name)
        .go();
    }
  }
};
</script>

<style lang="scss" scoped>
.name {
  position: relative;
}

// prettier-ignore
.hover-zone {
  position: absolute;
  top: 0; bottom: 0; left: 0; right: 0;
}
</style>
